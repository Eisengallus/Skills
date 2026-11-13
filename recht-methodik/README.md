# recht-methodik · Methodik-Skill für das deutsche Recht

Ein Prüfwerkzeug für die **Methode der Rechtsanwendung**: Ist der Weg von der Norm zum Ergebnis tragfähig, und
ist er als solcher offengelegt? Teil der Sammlung [Eisengallus](https://github.com/Eisengallus/Skills), neben `recht-grammatik`,
`recht-logik`, `recht-rhetorik`, `recht-beweis`, `recht-anspruch`, `recht-agb` und `recht-zitat`.

> **Keine Rechtsberatung.** Der Skill ist ein Werkzeug und erbringt keine Rechtsdienstleistung im Sinne des
> RDG. Siehe [Rechtlicher Rahmen](#rechtlicher-rahmen).

## Wozu das für die juristische Arbeit gut ist

Angreifbare Rechtspositionen scheitern oft nicht an der Logik, sondern an einem **verschwiegenen
Methodenschritt**. Eine Analogie wird gezogen, ohne die planwidrige Lücke darzulegen. Das Telos wird gegen den
eindeutigen Wortlaut ausgespielt, ohne die Wortlautgrenze überhaupt zu benennen. Ein Kanon wird zitiert, weil
er zum gewünschten Ergebnis führt, während die anderen drei schweigen. „Sinn und Zweck“ wird zur Chiffre für
das, was man ohnehin wollte.

Jeder dieser Schritte **kann** richtig sein. Er muss aber benannt und begründet werden, sonst trägt er nicht,
und genau dort setzt die Gegenseite an. Der Skill sucht diese Stellen, benennt den Defekt und sagt, was zu
ergänzen ist.

## Platz in der Sammlung

| Skill | Frage | Zuständigkeit |
| --- | --- | --- |
| `recht-grammatik` | Lässt der Wortlaut nur die gemeinte Lesart zu? | Ausdrucksform |
| `recht-logik` | Ergibt sich das Ergebnis zwingend aus den Voraussetzungen? | Schlüssigkeit |
| `recht-rhetorik` | Überzeugt der Text den, für den er geschrieben ist? | Überzeugungskraft |
| **`recht-methodik`** | Ist der Weg von der Norm zum Ergebnis tragfähig? | Methodenlehre |
| `recht-beweis` | Trägt der Weg von der Behauptung zur Feststellung? | Beweisrecht |
| `recht-anspruch` | Sind die in Betracht kommenden Anspruchsgrundlagen vollständig und in tragfähiger Ordnung geprüft? | Prüfprogramm |
| `recht-agb` | Gibt es zu dieser Klausel eine Entscheidung? | Klauselabgleich |
| `recht-zitat` | Ist jeder Nachweis so angegeben, dass man ihn findet? | Belegform |

**Abgrenzung zur Logik.** `recht-logik` fragt, ob der Schluss **aus seinen Prämissen folgt**, `recht-methodik`,
ob man diese Prämissen **so gewinnen durfte**. Ein Syllogismus kann formal einwandfrei sein und gleichwohl auf
einer unzulässigen Analogie beruhen.

**Abgrenzung zum Beweisrecht.** `recht-methodik` prüft die Beweisstation als **Aufbauschritt**: ob sie an der
richtigen Stelle steht und als solche offengelegt ist. `recht-beweis` prüft ihren **Inhalt**. Dass die
Beweisstation fehlt, ist ein Befund der Methodik. Dass die dort getroffene Lastverteilung falsch ist, ist einer
des Beweisrechts.

**Abgrenzung zum Anspruchsaufbau.** Den stufenweisen Aufbau eines Anspruchs (Anspruchsgrundlage,
Tatbestandsmerkmale, Konkurrenzen) gibt der Skill an `recht-anspruch` ab.

## Was der Skill leistet

| Modus | Kommando | Gegenstand |
| --- | --- | --- |
| Auslegung | `/recht-methodik:auslegung` | Wortlaut, Systematik, Historie und Telos, Kanon für Kanon; Wortlautgrenze, Kollisionsregeln, Gewichtung bei Widerstreit; Maßstabsbildung bei normativen Tatbestandsmerkmalen |
| Analogie | `/recht-methodik:analogie` | Lücke, Planwidrigkeit, vergleichbare Interessenlage, Analogieverbote (Art. 103 Abs. 2 GG, belastende Analogie im Eingriffsrecht); Umkehrschluss, Erst-recht-Schluss, teleologische Reduktion und Extension |
| Relation | `/recht-methodik:relation` | Kläger-, Beklagten- und Beweisstation; Zulässigkeit vor Begründetheit; Stellung der Anspruchsprüfung im Relationsaufbau (der Aufbau des Anspruchs selbst gehört zu `recht-anspruch`), Hilfsgutachten |
| Stil | `/recht-methodik:stil` | Gutachten- und Urteilsstil: Obersatz, Definition, Subsumtion, Ergebnis; Stilwahl nach Problemtiefe; Umstellung in den Zielstil |

Jeder Modus hat ein eigenes Berichtsformat. Jeder Bericht endet mit dem Block „Was ausdrücklich nicht
beanstandet wird“: was geprüft wurde und trägt, was angreifbar aussieht und es nicht ist, und wo die Prüfbarkeit
endet.

### Die zentrale Unterscheidung

Auslegung und Rechtsfortbildung trennt der **mögliche Wortsinn**:

- **Auslegung** bewegt sich innerhalb. Sie braucht keine besondere Rechtfertigung.
- **Rechtsfortbildung** überschreitet ihn. Die Analogie erstreckt die Norm, die teleologische Reduktion nimmt
  einen Fall aus. Beides setzt eine **planwidrige** Lücke voraus und ist begründungsbedürftig.

Test: Ist das Ergebnis noch eine Lesart, die ein sprachkundiger Leser dem Wortlaut entnehmen könnte? Ja, dann
Auslegung. Nein, dann Rechtsfortbildung. Der häufigste Methodenfehler ist, den Übertritt nicht zu bemerken und
ihn als „Auslegung nach Sinn und Zweck“ auszugeben.

## Grenzen

Acht Regeln gelten in allen Modi. Sie stehen vollständig in der `SKILL.md` unter *Kompetenzgrenze*.

1. **Kein Norminhalt aus dem Gedächtnis.** Wo ein Schritt von einer Vorschrift, einer Gesetzesfassung oder
   einer Entscheidung abhängt, setzt der Skill `[prüfen: Norm]` oder `[prüfen: Rechtsprechung]` und formuliert
   konditional. Paragraphennummern, die nicht im Text stehen, werden nicht erfunden.
2. **Der Sachverhalt ist Vorgabe.** Fehlt eine Tatsache, die der methodische Schritt voraussetzt, wird die
   Lücke festgehalten, nicht gefüllt. „Das steht hier nicht“ allein ist kein Befund.
3. **Den Zusammenhang lesen, nicht den Satz.** Ein Beleg, der an anderer Stelle des vorgelegten Textes steht,
   ist geliefert. Ein Kanon, den der Verfasser ausdrücklich als unergiebig abtut, ist angesprochen.
4. **Ergebnisoffenheit.** Ein methodisch sauber begründetes Ergebnis bleibt sauber, auch wenn es unbillig
   erscheint. Ein unsauberer Weg bleibt unsauber, auch wenn das Ergebnis überzeugt.
5. **Nachbarskills** werden geflaggt, nicht bearbeitet: `[→ recht-grammatik]`, `[→ recht-logik]`,
   `[→ recht-rhetorik]`, `[→ recht-beweis]`, `[→ recht-anspruch]`.
6. **Keine Rechtsdienstleistung.** Jede Ausgabe ist von einer rechtskundigen Person zu prüfen.
7. **Rechtsquellen.** Gesetze und Urteile im Volltext sind frei (§ 5 Abs. 1 UrhG). Gesetzesmaterialien sind
   frei, mit Änderungsverbot und Quellenangabe (§ 5 Abs. 2, §§ 62, 63 UrhG), und für die historische Auslegung
   nutzbar. Leitsätze kommerzieller Anbieter werden nicht übernommen, Kommentarliteratur und Lehrbücher der
   Methodenlehre werden nicht wiedergegeben (paraphrasieren ist zulässig). Von DIN-Normen, der VOB/C und
   geotechnischen Empfehlungswerken werden nur Nummer, Titel, Ausgabestand und Abschnitt genannt.
8. **Identifizierende Angaben** werden im Bericht nicht ohne Not wiederholt. Ob ein Text einem KI-Werkzeug
   vorgelegt werden durfte, beurteilt der Skill nicht.

**Der Nullbefund ist der Regelfall.** Der Abschnitt „Befunde“ ist kein Formularfeld, das gefüllt werden will.
Vier Proben gehen jedem Befund voraus: Ausschnitts-, Tragfähigkeits-, Umkehr- und Quellenprobe. Dazu kommt die
Auflösungsprobe: Ein methodisch heikler Schritt ist noch kein Defekt, entscheidend ist, ob der Text ihn
offenlegt. Dass ein Ausschnitt kurz ist, eine Norm nicht zitiert oder eine Selbstverständlichkeit nicht
ausspricht, ist kein Mangel.

Für den Relationsaufbau gilt zusätzlich die **Stationenprobe**: Eine Station ist erst dann ein Befund, wenn sie
fehlt, obwohl der Ausschnitt sie verlangt, nicht schon, wenn sie knapp ausfällt.

## Aufbau

```
README.md                     diese Datei
LICENSE                       MIT-Lizenz (dieselbe wie im Stamm des Repositoriums)
SKILL.md                      Anweisung und Berichtsformate der vier Modi
commands/                     vier Slash-Befehle
references/
  auslegungskanones.md        Wortlaut, Systematik, Historie, Telos; Wortlautgrenze, Gesamtbild
  tatbestandsmerkmale.md      normative Tatbestandsmerkmale: der Maßstab und seine Offenlegung
  analogie-reduktion.md       Lücke, Planwidrigkeit, Interessenlage, Verbote, Umkehr- und Erst-recht-Schluss
  unionsrecht-verfassung.md   verfassungs- und unionsrechtskonforme Auslegung, Vorlagepflicht
  relationstechnik.md         Stationen, Zulässigkeit vor Begründetheit, Anspruchsaufbau, Hilfsgutachten
  gutachten-urteilsstil.md    Obersatz, Definition, Subsumtion, Ergebnis; Stilwahl, Mischform
  defektkatalog.md            Katalog der Methodenfehler nach Kategorien
.claude-plugin/  .cursor-plugin/  .codex-plugin/   Manifeste mit Name, Beschreibung und Fassung
```

## Installation

Der Skill besteht aus Textdateien: keine Programme, keine Server, keine Netzverbindung. Kopieren Sie den
Ordner `recht-methodik/` in den Skill-Ordner Ihres Werkzeugs, bei Claude Code nach `~/.claude/skills/`,
bei Cursor nach `~/.cursor/skills/` und bei Codex nach `~/.codex/skills/`.

Der Ordner enthält `SKILL.md` und `references/`, die Slash-Befehle liegen in `commands/`. Nach dem Neustart
des Werkzeugs steht der Skill bereit.

Für **Microsoft 365 Copilot** gibt es keinen Skill-Ordner. Dort wird `recht-methodik` in Microsoft Copilot
Studio einem Agenten als **Skill** hinzugefügt, als ZIP-Datei mit `SKILL.md`, `LICENSE`, `references/` und `commands/`,
also mit demselben Prüftext. Slash-Befehle gibt es dort nicht, den Modus nennen Sie in der Anfrage.
Abgerechnet wird über die Copilot Credits des eigenen Microsoft-365-Mandanten (Tenant).

## Aufruf

- Slash-Befehle: `/recht-methodik:auslegung`, `/recht-methodik:analogie`, `/recht-methodik:relation`,
  `/recht-methodik:stil`.
- Normale Anfrage: „prüfe die Auslegung“, „ist das noch vom Wortlaut gedeckt“, „liegt eine planwidrige Lücke
  vor“, „Umkehrschluss oder Analogie“, „baue die Relation“, „ist der Vortrag schlüssig“, „prüfe den Obersatz“,
  „Gutachten- oder Urteilsstil“.

Ohne nähere Angabe beginnt der Skill mit `auslegung`, geht bei erkennbarer Wortlautüberschreitung zu `analogie`
über und zieht `relation` und `stil` nach der Gattung des Textes heran.

Zusammenspiel: Über einem Schriftsatz lautet der Zyklus `/recht-grammatik:mehrdeutigkeit` →
`/recht-methodik:auslegung` → `/recht-beweis:last` → `/recht-logik:pruefen` → `/recht-rhetorik:stresstest`.
Die Methodik prüft die Gewinnung der Prämissen, das Beweisrecht ihre tatsächliche Grundlage, die Logik den
Schluss aus ihnen.

Einen Befund aus dem Vorlauf können Sie in den nächsten Lauf **mitgeben**. Der Skill führt ihn dann unter „Aus
dem Vorlauf übernommen“ auf, prüft ihn nicht erneut und zählt ihn nicht als eigenen Befund. Umgekehrt sammelt
er unter „Zur Übergabe“, was in die Zuständigkeit eines Nachbarskills fällt: Hinter dem Pflichtblock steht eine
Übergabezeile (Skill · Modus · Fundstelle — Befund). Die Regel dazu steht in der `SKILL.md`.

## Vertraulichkeit

Der Skill wiederholt identifizierende Angaben nicht ohne Not. Aus dem geprüften Text zitiert er nur so viel,
wie der Beleg des Defekts trägt. Namen, Anschriften, Bankverbindungen und Kennnummern, die für den Defekt ohne
Bedeutung sind, kürzt er mit `…`. Er ergänzt niemals eine Angabe, die im Text nicht steht. Die vollständige
Regel steht in der `SKILL.md`.

Der Skill selbst sendet nichts. Er besteht aus Textdateien und ruft keine Netzadresse auf. Der KI-Assistent
dagegen überträgt jeden Text, den Sie ihm vorlegen, an die Rechner des Betreibers des Sprachmodells. Dort wird
er nach dessen Bedingungen verarbeitet. Wer einer Berufsverschwiegenheit, einer Geheimhaltungsabrede oder dem
Datenschutzrecht unterliegt, legt identifizierende Angaben nicht ungeprüft in einen Cloud-Dienst: anonymisieren,
Auszüge verwenden oder in geschlossener Umgebung arbeiten. Für mandatsbezogene Unterlagen sind insbesondere
§§ 203, 204 StGB, § 43e BRAO, § 2 BORA sowie DSGVO und BDSG zu beachten. Datenfluss und Auftragsverarbeitung
beim Betreiber des Sprachmodells sind vorher zu klären.

Alle Beispiele sind **frei erfunden**. Personen, Firmen und Vorgänge existieren nicht.

## Wie der Skill geprüft wird

Jede Fassung wird an frei erfundenen Prüffällen gemessen: an fehlerhaften Texten, in denen der Skill den Fehler
finden soll, und an fehlerfreien, an denen er nichts beanstanden darf. Eine Änderung wird nur übernommen, wenn sie
auf keiner der beiden Seiten schlechter abschneidet.

## Rechtlicher Rahmen

Der Skill erbringt **keine Rechtsdienstleistung** im Sinne des Rechtsdienstleistungsgesetzes. Er gibt keine
Auskunft über die Rechtslage, empfiehlt kein Vorgehen und ersetzt keine anwaltliche Prüfung. Er prüft, ob ein
Text seine eigenen methodischen Schritte offenlegt und ob sie zueinander passen. Jede Ausgabe ist von einer
rechtskundigen Person zu prüfen.

Ob der Einsatz unter die KI-Verordnung (Verordnung (EU) 2024/1689) fällt, ist für das konkrete
Einsatzszenario zu prüfen. Anwendungen in der Rechtspflege können als Hochrisiko einzustufen sein; das ist
nicht pauschal zu verneinen.

Gesetze und Gerichtsentscheidungen im Volltext sind gemeinfrei (§ 5 Abs. 1 UrhG). Leitsätze kommerzieller
Anbieter, DIN-Normen und Kommentarliteratur sind urheberrechtlich geschützt. Der Skill übernimmt Leitsätze
nicht, gibt Kommentarliteratur nicht wieder (Paraphrase und Fundstelle sind zulässig) und nennt von DIN-Normen
nur Nummer, Titel, Ausgabestand und Abschnitt.

## Lizenz

[MIT](LICENSE) · © 2026 Eisengallus

Der Name „Eisengallus“, das Signet und die Farbpalette sind Kennzeichen und werden von der Lizenz nicht
erfasst. „Claude“, „Claude Code“, „Anthropic“, „Cursor“, „Codex“ und „Microsoft 365 Copilot“ sind Kennzeichen
ihrer jeweiligen Inhaber und werden ausschließlich beschreibend zur Angabe der Kompatibilität verwendet.
