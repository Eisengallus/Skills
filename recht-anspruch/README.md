# recht-anspruch · Anspruchsaufbau-Skill für das deutsche Zivilrecht

Ein Prüfwerkzeug für das **Prüfprogramm** juristischer Texte: Arbeitet ein Gutachten oder Schriftsatz die in
Betracht kommenden Anspruchskategorien vollständig und in tragfähiger Ordnung ab? Teil der Sammlung
[Eisengallus](https://github.com/Eisengallus/Skills), neben `recht-grammatik`, `recht-logik`, `recht-rhetorik`, `recht-methodik`,
`recht-beweis`, `recht-agb` und `recht-zitat`.

> **Keine Rechtsberatung.** Der Skill ist ein Werkzeug und erbringt keine Rechtsdienstleistung im Sinne des
> RDG. Siehe [Rechtlicher Rahmen](#rechtlicher-rahmen).

## Wozu das für die juristische Arbeit gut ist

Die erste Frage jeder Fallbearbeitung lautet: **Welche Ansprüche kommen in Betracht?** Die anderen Skills der
Sammlung setzen nach diesem Schritt an. Sie prüfen Ausdruck, Schluss, Wirkung, Methode und Tatsachengrundlage
eines Weges, der schon gewählt ist. `recht-anspruch` prüft die Wahl selbst: ob eine Kategorie mit Anhalt im Text
übergangen wurde, ob eine Vorfrage übersprungen ist (Delikt vor der Vertragslage, die den Rechtsgrund bestimmt),
ob eine Sperrwirkung übergangen wird (§§ 987 ff. BGB, Vorrang der Leistungskondiktion) und ob die Stufen jedes
Anspruchs getrennt stehen: entstanden, nicht erloschen, durchsetzbar.

Seine erste Frage ist nicht, welche Kategorie fehlt, sondern: **Welchen Prüfauftrag hat sich der Text selbst
gegeben?** Ein Gutachten, das erklärt, nur vertragliche Ansprüche zu prüfen, hat keine Lücke, wenn es das
Deliktsrecht nicht behandelt. Es hat seinen Auftrag beschränkt, und das ist zulässig.

Dabei sagt der Skill **nie**, welche Ansprüche im konkreten Fall bestehen. Er prüft das Programm, nicht das
Ergebnis. Im Sondermodus `schema` gibt er abstrakte Prüfschemata aus: Lehrmaterial, keine Falllösung.

## Platz in der Sammlung

| Skill | Frage | Zuständigkeit |
| --- | --- | --- |
| `recht-grammatik` | Lässt der Wortlaut nur die gemeinte Lesart zu? | Ausdrucksform |
| `recht-logik` | Ergibt sich das Ergebnis zwingend aus den Voraussetzungen? | Schlüssigkeit |
| `recht-rhetorik` | Überzeugt der Text den, für den er geschrieben ist? | Überzeugungskraft |
| `recht-methodik` | Ist der Weg von der Norm zum Ergebnis tragfähig? | Methodenlehre |
| `recht-beweis` | Trägt der Weg von der Behauptung zur Feststellung? | Beweisrecht |
| **`recht-anspruch`** | Sind die in Betracht kommenden Anspruchsgrundlagen vollständig und in tragfähiger Ordnung geprüft? | Prüfprogramm |
| `recht-agb` | Gibt es zu dieser Klausel eine Entscheidung? | Klauselabgleich |
| `recht-zitat` | Ist jeder Nachweis so angegeben, dass man ihn findet? | Belegform |

**Abgrenzung zu Logik und Methodik.** Hier verläuft die schärfste Grenze. `recht-logik` und `recht-methodik`
prüfen einen **Schritt**: Trägt dieser Schluss, ist diese Auslegung vertretbar? `recht-anspruch` prüft das
**Programm**: Welche Grundlagen kommen überhaupt in Betracht, und in welcher Ordnung sind sie abzuarbeiten? Ein
Gutachten kann in jedem einzelnen Schritt einwandfrei sein und trotzdem eine Anspruchsgrundlage übergehen.

Umgekehrt gilt: Steht die Grundlage fest und ist allein die Subsumtion streitig, ist dieser Skill der falsche.
Er verweist dann mit `[→ recht-logik]` oder `[→ recht-methodik]`, statt die Subsumtion selbst zu beurteilen.

## Was der Skill leistet

| Modus | Kommando | Gegenstand |
| --- | --- | --- |
| Schema | `/recht-anspruch:schema` | Nachschlag, keine Prüfung: abstraktes Prüfschema einer Kategorie mit Obersatz-Form, Stufen, typischen Fehlerquellen und Konkurrenzhinweisen |
| Aufbau | `/recht-anspruch:aufbau` | eine Anspruchsprüfung gegen ihr Schema: Stufenfolge, Ebenen der Einwendungen, vermengte Anspruchsgrundlagen |
| Vollständigkeit | `/recht-anspruch:vollstaendigkeit` | ein Gutachten gegen die kanonische Reihenfolge: übergangene Kategorien mit Anhalt im Text, übersprungene Vorfragen, Sperrwirkungen |
| Konkurrenz | `/recht-anspruch:konkurrenz` | behauptete Sperrwirkungen und Anspruchskonkurrenzen: Verdrängung, Sperre, freie Konkurrenz, Durchwirkung |

Der Kategorienrahmen ist die kanonische Reihenfolge des Zivilrechts: vertraglich, vertragsähnlich, dinglich,
deliktisch, bereicherungsrechtlich. Die Reihenfolge ist eine Zweckmäßigkeitsregel der Fallbearbeitung, **kein
Rechtssatz**. Befunde trägt nur ihr harter Kern: die Vorfragen, die eine Kategorie für eine andere beantwortet,
und die Sperren, mit denen eine Kategorie eine andere ausschließt. Versicherungsrechtliche Ansprüche (VVG)
stehen quer zu dieser Reihenfolge.

Jeder Prüfbericht endet mit dem Block „Was ausdrücklich nicht beanstandet wird“: was behandelt oder begründet
ausgeschlossen ist und trägt, was angreifbar aussieht und es nicht ist, und wo die Prüfung endet. Im Modus
`schema` entfällt der Block, dort gibt es keine Befunde.

## Grenzen

Acht Regeln gelten in allen Modi. Sie stehen vollständig in der `SKILL.md` unter *Kompetenzgrenze*.

1. **Nie die Rechtslage des Falls.** Der Skill sagt nie, welche Ansprüche im konkreten Fall bestehen. Er prüft,
   ob das Prüfprogramm vollständig und geordnet ist, und gibt Schemata abstrakt aus.
2. **Kein Norminhalt aus dem Gedächtnis.** Wo ein Schritt von einer Vorschrift oder Entscheidung abhängt,
   setzt der Skill `[prüfen: Norm]` oder `[prüfen: Rechtsprechung]` und formuliert konditional.
   Paragraphennummern, die weder im Ausschnitt noch in den Referenzen stehen, werden nicht erfunden.
3. **Der Sachverhalt ist Vorgabe.** Ein Anhalt für eine Kategorie liegt nur vor, wenn der Text selbst
   Tatsachen nennt, die sie tragen könnten. Hinzugedachte Tatsachen zählen nicht.
4. **Den Zusammenhang lesen, nicht den Satz.** Eine Kategorie, die an anderer Stelle des vorgelegten Textes
   geprüft oder ausgeschlossen wird, ist behandelt.
5. **Ergebnisoffenheit.** Ein vollständiges Programm bleibt vollständig, auch wenn sein Ergebnis unbillig
   erscheint. Ein lückenhaftes bleibt lückenhaft, auch wenn das Ergebnis überzeugt.
6. **Nachbarskills** werden geflaggt, nicht bearbeitet: `[→ recht-logik]`, `[→ recht-grammatik]`,
   `[→ recht-methodik]`, `[→ recht-rhetorik]`, `[→ recht-beweis]`.
7. **Rechtsquellen.** Gesetze, Urteile im Volltext und Gesetzesmaterialien sind frei (§ 5 UrhG). Leitsätze
   kommerzieller Anbieter werden nicht übernommen. Bei Schemata-Sammlungen von Lehrstühlen und Verlagen ist die
   Methode frei, der Wortlaut nicht: paraphrasieren und die Fundstelle nennen. Kommentarliteratur wird nicht
   wiedergegeben (paraphrasieren und die Fundstelle nennen ist zulässig).
8. **Keine Rechtsdienstleistung.** Der Skill ersetzt keine anwaltliche Prüfung.

**Der Nullbefund ist der Regelfall.** Der Abschnitt „Befunde“ ist kein Formularfeld, das gefüllt werden will.
Drei Proben gehen jedem Befund voraus: Ausschnitts-, Tragfähigkeits- und Umkehrprobe. Dazu kommt die
Auflösungsprobe: Eine scheinbare Lücke ist kein Befund, wenn der Text sie selbst auflöst, etwa durch einen
begründeten Ausschluss oder eine erklärte Beschränkung des Auftrags. Eine Kategorie, für die der Text keinen
Anhalt nennt, ist nicht zu prüfen. Der Kanon allein erzeugt keine Prüfpflicht.

**Bewertungsstufen.** `kritisch`, sobald mindestens ein tragender Befund vorliegt; `hinweisbedürftig`, wenn
alle Befunde nachrangig sind; `unauffällig`, wenn es keinen Befund gibt.

**Reichweite.** Der Skill ist für das Zivilrecht ausgebaut. Für andere Teilrechtsordnungen sagt er das, statt
den zivilrechtlichen Rahmen zu übertragen.

## Aufbau

```
README.md                     diese Datei
LICENSE                       MIT-Lizenz (dieselbe wie im Stamm des Repositoriums)
SKILL.md                      Anweisung, Prüfgang und Berichtsform
commands/                     vier Slash-Befehle
references/
  defektkatalog.md            Defekte nach Kategorien, jeder mit seinem Gegenbild; dazu, was kein Befund ist
  zivilrecht/
    reihenfolge.md            kanonische Reihenfolge, Vorfragen-Logik, Sperrwirkungen, freie Konkurrenz
    vertrag-primaer.md        Erfüllungsansprüche: Stufen und Ebenen der Einwendungen
    vertrag-sekundaer.md      System der §§ 280 ff. BGB, Rücktritt und Minderung, Gewährleistung
    vertragsaehnlich.md       Verschulden bei Vertragsanbahnung, Geschäftsführung ohne Auftrag
    dinglich.md               Vindikation, EBV, § 1004 BGB, Besitzschutz, Erbschaftsanspruch, nachbarrechtlicher Ausgleich
    delikt.md                 § 823 Abs. 1 und 2, § 826, § 831 BGB, je Grundlage ein Prüfungsgang
    bereicherung.md           Leistungs- und Nichtleistungskondiktion, Sperren, Entreicherung
    versicherung.md           Haftung und Deckung, Direktanspruch, Forderungsübergang, Einwendungen des VVG
.claude-plugin/  .cursor-plugin/  .codex-plugin/   Manifeste mit Name, Beschreibung und Fassung
```

## Installation

Der Skill besteht aus Textdateien: keine Programme, keine Server, keine Netzverbindung. Kopieren Sie den
Ordner `recht-anspruch/` in den Skill-Ordner Ihres Werkzeugs, bei Claude Code nach `~/.claude/skills/`,
bei Cursor nach `~/.cursor/skills/` und bei Codex nach `~/.codex/skills/`.

Der Ordner enthält `SKILL.md` und `references/`, die Slash-Befehle liegen in `commands/`. Nach dem Neustart
des Werkzeugs steht der Skill bereit.

Für **Microsoft 365 Copilot** gibt es keinen Skill-Ordner. Dort wird `recht-anspruch` in Microsoft Copilot
Studio einem Agenten als **Skill** hinzugefügt, als ZIP-Datei mit `SKILL.md`, `LICENSE`, `references/` und `commands/`,
also mit demselben Prüftext. Slash-Befehle gibt es dort nicht, den Modus nennen Sie in der Anfrage.
Abgerechnet wird über die Copilot Credits des eigenen Microsoft-365-Mandanten (Tenant).

## Aufruf

- Slash-Befehle: `/recht-anspruch:schema`, `/recht-anspruch:aufbau`, `/recht-anspruch:vollstaendigkeit`,
  `/recht-anspruch:konkurrenz`.
- Normale Anfrage: „prüfe die Vollständigkeit des Gutachtens“, „fehlt eine Anspruchsgrundlage“, „stimmt die
  Prüfungsreihenfolge“, „gib mir das Schema zu …“, „ist der Anspruchsaufbau vollständig“.

Wird kein Modus genannt, bestimmt der Skill ihn aus der Anfrage. In den Prüfmodi beginnt er stets mit dem
Prüfauftrag des Textes.

Was in die Zuständigkeit eines Nachbarskills fällt, gibt der Skill per Flag ab und schließt dann mit einer
Übergabezeile. Die Regel dazu steht in der `SKILL.md`.

## Vertraulichkeit

Der Skill wiederholt identifizierende Angaben nicht ohne Not. Die Regel steht in der `SKILL.md` unter „Form
der Ausgabe“.

Der Skill selbst sendet nichts. Er besteht aus Textdateien und ruft keine Netzadresse auf. Der KI-Assistent
dagegen überträgt jeden Text, den Sie ihm vorlegen, an die Rechner des Betreibers des Sprachmodells. Dort wird
er nach dessen Bedingungen verarbeitet. Wer einer Berufsverschwiegenheit, einer Geheimhaltungsabrede oder dem
Datenschutzrecht unterliegt, legt identifizierende Angaben nicht ungeprüft in einen Cloud-Dienst: anonymisieren,
Auszüge verwenden oder in geschlossener Umgebung arbeiten. Für mandatsbezogene Unterlagen sind insbesondere
§§ 203, 204 StGB, § 43e BRAO, § 2 BORA sowie DSGVO und BDSG zu beachten. Datenfluss und Auftragsverarbeitung
beim Betreiber des Sprachmodells sind vorher zu klären.

## Wie der Skill geprüft wird

Jede Fassung wird an frei erfundenen Prüffällen gemessen: an fehlerhaften Texten, in denen der Skill den Fehler
finden soll, und an fehlerfreien, an denen er nichts beanstanden darf. Eine Änderung wird nur übernommen, wenn sie
auf keiner der beiden Seiten schlechter abschneidet.

## Rechtlicher Rahmen

Der Skill erbringt **keine Rechtsdienstleistung** im Sinne des Rechtsdienstleistungsgesetzes. Er gibt keine
Auskunft über die Rechtslage, empfiehlt kein Vorgehen und ersetzt keine anwaltliche Prüfung. Er prüft, ob ein
Text seine eigenen Prüfschritte offenlegt und ob sie zueinander passen. Jede Ausgabe ist von einer
rechtskundigen Person zu prüfen.

Ob der Einsatz unter die KI-Verordnung (Verordnung (EU) 2024/1689) fällt, ist für das konkrete
Einsatzszenario zu prüfen. Anwendungen in der Rechtspflege können als Hochrisiko einzustufen sein; das ist
nicht pauschal zu verneinen.

Gesetze und Gerichtsentscheidungen im Volltext sind gemeinfrei (§ 5 Abs. 1 UrhG). Leitsätze kommerzieller
Anbieter, DIN-Normen und Kommentarliteratur sind urheberrechtlich geschützt. Der Skill übernimmt Leitsätze
nicht, gibt Kommentarliteratur nicht wieder (Paraphrase und Fundstelle sind zulässig) und übernimmt aus
Schemata-Sammlungen die Methode, nicht den Wortlaut.

## Lizenz

[MIT](LICENSE) · © 2026 Eisengallus

Der Name „Eisengallus“, das Signet und die Farbpalette sind Kennzeichen und werden von der Lizenz nicht
erfasst. „Claude“, „Claude Code“, „Anthropic“, „Cursor“, „Codex“ und „Microsoft 365 Copilot“ sind Kennzeichen
ihrer jeweiligen Inhaber und werden ausschließlich beschreibend zur Angabe der Kompatibilität verwendet.
