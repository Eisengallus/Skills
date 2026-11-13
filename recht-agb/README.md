# recht-agb · Klauselabgleich gegen entschiedene Fälle

Ein Prüfwerkzeug, das eine vorgelegte AGB-Klausel gegen ein Register entschiedener Klauseln (überwiegend
für unwirksam erklärt, dazu gebilligte Gegenbeispiele) abgleicht und die Fundstelle samt gerichtlicher Begründung
nennt. **Der Skill vergleicht Texte. Er beurteilt keine Klausel.** Teil der Sammlung [Eisengallus](https://github.com/Eisengallus/Skills), neben `recht-grammatik`,
`recht-logik`, `recht-rhetorik`, `recht-methodik`, `recht-beweis`, `recht-anspruch` und `recht-zitat`.

> **Keine Rechtsberatung.** Der Skill ist ein Werkzeug und erbringt keine Rechtsdienstleistung im Sinne des
> RDG. Siehe [Rechtlicher Rahmen](#rechtlicher-rahmen).

## Wozu das für die juristische Arbeit gut ist

Ein Klauselabgleich beantwortet eine andere Frage als die übrigen Skills der Sammlung: nicht, ob ein Text gut
gemacht ist, sondern ob eine vorgelegte Klausel mit einer bereits entschiedenen übereinstimmt. Der Skill ist ein
Tatsachenvergleich zweier Texte und enger geschnitten als jeder Nachbarskill:

- Der Skill sagt nie, dass eine Klausel unwirksam ist. Die Wörter „unwirksam“ und „nichtig“ kommen nur als
  gekennzeichnetes Zitat aus einer Entscheidung vor.
- Eine Klausel ohne Registereintrag bleibt unbeurteilt. Kein Eintrag heißt nicht „wirksam“, und das wird
  ausdrücklich gesagt.
- Einbeziehung (§ 305 Abs. 2 BGB), Überraschung (§ 305c BGB) und Individualabrede (§ 305b BGB) prüft der Skill
  nicht. Das sind Feststellungen zum Einzelfall.
- Widersprechen sich zwei Entscheidungen zur selben Klausel, führt der Skill **beide** auf und wählt nicht aus.

Was der Skill sagt, ist eine Tatsache über zwei Texte: Die vorgelegte Klausel entspricht wörtlich oder nahezu
wörtlich einer entschiedenen Klausel, mit dieser Abweichung, und das Gericht hat so begründet. Ob die
Entscheidung übertragbar ist, bleibt offen und ist mit `[prüfen: Übertragbarkeit]` markiert.

Das Register stammt aus Entscheidungen des Bundesgerichtshofs und des Bundesarbeitsgerichts, nach Sachgruppen
geordnet (unter anderem Bau, Miete, Gewerberaum, Arbeit, Kredit und Reise). Instanzgerichte sind nicht
erschlossen. Reichweite und Herkunft beschreibt `references/register/README.md`.

## Platz in der Sammlung

| Skill | Frage | Zuständigkeit |
| --- | --- | --- |
| `recht-grammatik` | Lässt der Wortlaut nur die gemeinte Lesart zu? | Ausdrucksform |
| `recht-logik` | Ergibt sich das Ergebnis zwingend aus den Voraussetzungen? | Schlüssigkeit |
| `recht-rhetorik` | Überzeugt der Text den, für den er geschrieben ist? | Überzeugungskraft |
| `recht-methodik` | Ist der Weg von der Norm zum Ergebnis tragfähig? | Methodenlehre |
| `recht-beweis` | Trägt der Weg von der Behauptung zur Feststellung? | Beweisrecht |
| `recht-anspruch` | Sind die in Betracht kommenden Anspruchsgrundlagen vollständig und in tragfähiger Ordnung geprüft? | Prüfprogramm |
| **`recht-agb`** | Gibt es zu dieser Klausel eine Entscheidung? | Klauselabgleich |
| `recht-zitat` | Ist jeder Nachweis so angegeben, dass man ihn findet? | Belegform |

**Eine andere Art von Aussage.** Die übrigen Skills prüfen die **Machart** eines Textes. `recht-agb` prüft seine
**Übereinstimmung mit einem Bestand**. Diese Aussage ist nachschlagbar, nicht wertend, und genau deshalb trägt
der Skill die enge Kompetenzgrenze.

**Abgabe an die Nachbarskills.** Sie ist hier der Regelfall, kein Randfall. Ob eine Klausel mehrdeutig
formuliert ist, gehört `recht-grammatik`. Ob die Begründung des Registereintrags trägt, gehört `recht-logik`.
Der Skill gibt die Frage ab, statt sie zu beantworten.

## Was der Skill leistet

| Modus | Kommando | Gegenstand |
| --- | --- | --- |
| Abgleich | `/recht-agb:abgleich` | Hauptmodus: vorgelegte Klauseln gegen das Register; Regelung vor Wortlaut, tragender Grund, Art der Abweichung |
| Register | `/recht-agb:register` | Nachschlag, keine Prüfung: welche entschiedenen Klauseln das Register zu einer Sachgruppe führt, mit Fundstelle und tragendem Grund |
| Extraktion | `/recht-agb:extraktion` | aus einem Fließtext die einzelnen AGB-Klauseln herauslösen und abgrenzen, ohne Bewertung; Vorstufe zum Abgleich |

**`einbeziehung` ist bewusst kein Modus.** Die Einbeziehung ist eine Feststellung zum Einzelfall (§ 305 Abs. 2
BGB: Hinweis, Kenntnisnahmemöglichkeit, Einverständnis). Wer sie beantwortet, beurteilt einen konkreten
Vertragsschluss. Der Modus fehlt nicht, er ist abgelehnt.

Der Abgleich ordnet jede Abweichung einer von sechs Arten zu:

| Art | Beispiel | Folge |
| --- | --- | --- |
| wortgleich | Zeichenfolge identisch | Treffer |
| nahezu wörtlich | andere Wortstellung, gleiche Regelung | Treffer, Abweichung benennen |
| verkürzt | eine Voraussetzung fehlt | prüfen, ob sie den tragenden Grund betraf |
| erweitert | eine Ausnahme ist hinzugefügt | Auflösungsprobe, meist kein Treffer |
| gleiches Vokabular, andere Regelung | „Sicherheitseinbehalt“ in anderer Funktion | kein Treffer |
| gleiche Regelung, anderes Vokabular | Umschreibung ohne Fachbegriff | Treffer, die Regelung entscheidet |

Im Abgleich endet jeder Bericht mit dem Block „Was ausdrücklich nicht beanstandet wird“: welche Klauseln das
Register ohne Gegenstück befragt hat, mit dem Zusatz, dass dies keine Aussage über ihre Wirksamkeit ist; wo die
Auflösungsprobe angeschlagen hat; und wo die Prüfbarkeit endet.

## Grenzen

Vier Regeln gelten in allen Modi. Sie stehen vollständig in der `SKILL.md` unter *Kompetenzgrenze*.

1. **Nie „unwirksam“.** Der Skill sagt nie, dass eine Klausel unwirksam ist, auch nicht abgeschwächt („dürfte
   unwirksam sein“, „ist angreifbar“). Diese Wörter stehen in seiner Ausgabe nur als gekennzeichnetes Zitat aus
   einer Entscheidung. Die Übertragbarkeit trägt `[prüfen: Übertragbarkeit]`.
2. **Ohne Registereintrag keine Beurteilung.** Findet der Skill nichts, lautet sein Ergebnis „kein
   Registereintrag“. Er beurteilt die Klausel dann nicht frei nach §§ 307 bis 309 BGB. Kein Eintrag heißt nicht
   „wirksam“, die offene Frage trägt `[prüfen: Norm]`.
3. **Keine Einbeziehung.** Ob AGB wirksam einbezogen wurden, ob eine Klausel überraschend ist oder eine
   Individualabrede vorgeht, benennt der Skill und gibt es ab. Er beantwortet es nicht.
4. **Keine streitige Rechtsfrage.** Widersprechen sich zwei Entscheidungen zur selben Klausel, führt der Skill
   beide auf und kennzeichnet den Streit. Welche Linie trägt, bleibt offen (`[prüfen: Rechtsprechung]`).

**Zitate sind wörtlich.** Entfernt man die Markierung `▸ … ◂`, muss das Zitat Zeichen für Zeichen im vorgelegten
Text stehen. Der Abgleich lebt davon, dass beide Wortlaute unverändert nebeneinander stehen.

**Der Nullbefund ist der Regelfall.** Das Register deckt einen kleinen Ausschnitt des AGB-Rechts ab, die meisten
vorgelegten Klauseln haben dort kein Gegenstück. Ein Treffer wird nur gemeldet, wenn die **Regelung**
übereinstimmt, nicht bloß das Vokabular, und wenn die Abweichung im Wortlaut den tragenden Grund der
Entscheidung nicht berührt. Drei Proben gehen jedem Treffer voraus: Tragfähigkeits-, Umkehr- und
Auflösungsprobe. Die Auflösungsprobe fragt, ob die vorgelegte Klausel das Problem auflöst, an dem die
entschiedene gescheitert ist. Ist das so, ist es kein Treffer.

## Aufbau

```
README.md                     diese Datei
LICENSE                       MIT-Lizenz (dieselbe wie im Stamm des Repositoriums)
SKILL.md                      Anweisung, Befundschwelle und Satzmuster eines Treffers
commands/                     drei Slash-Befehle
references/
  abgleichmethode.md          Regelung vor Wortlaut, tragender Grund, die sechs Abweichungsarten, Randbedingungen eines Treffers
  agb-kontrolle.md            Prüfungsaufbau der §§ 305 bis 310 BGB als Einordnungshilfe, kein Prüfauftrag
  register/
    README.md                 Reichweite des Registers, Dateiübersicht, Herkunft der Klauselwortlaute
    arbeitsrecht.md           Formulararbeitsverträge
    bautraegervertrag.md      Bauträgervertrag
    kaution.md                Kautionsklauseln im Wohnraummietvertrag
    konkurrenzschutz-einkaufszentrum.md     Konkurrenzschutz im Einkaufszentrum (Gewerberaummiete)
    kuendigungsverzicht.md    Kündigungsverzicht und Mindestlaufzeit im Wohnraummietvertrag
    reiserecht.md             Pauschalreiseverträge
    schoenheitsreparaturen-fristenplan.md   Schönheitsreparaturen, starrer und flexibler Fristenplan
    sicherheitsleistung.md    Sicherheiten im Bauvertrag
    tierhaltung.md            Tierhaltungsklauseln im Wohnraummietvertrag
    verbraucherkredit.md      Bankentgelte in Verbraucherdarlehensverträgen
    verguetung-nebenkosten.md Vergütungsnebenabreden
    vertragsstrafe.md         Vertragsstrafe wegen Verzugs
    vob-b-privilegierung.md   VOB/B „als Ganzes“ vereinbart: die vorgeschaltete Prüfstufe
    wertsicherungsklauseln.md Wertsicherungs- und Preisgleitklauseln (preisgebundener Wohnraum)
.claude-plugin/  .cursor-plugin/  .codex-plugin/   Manifeste mit Name, Beschreibung und Fassung
```

Abgeglichen wird ausschließlich gegen `references/register/`. Entscheidungen, die `abgleichmethode.md` zur
Erläuterung der Methode nennt, sind kein Register.

## Installation

Der Skill besteht aus Textdateien: keine Programme, keine Server, keine Netzverbindung. Kopieren Sie den
Ordner `recht-agb/` in den Skill-Ordner Ihres Werkzeugs, bei Claude Code nach `~/.claude/skills/`,
bei Cursor nach `~/.cursor/skills/` und bei Codex nach `~/.codex/skills/`.

Der Ordner enthält `SKILL.md` und `references/`, die Slash-Befehle liegen in `commands/`. Nach dem Neustart
des Werkzeugs steht der Skill bereit.

Für **Microsoft 365 Copilot** gibt es keinen Skill-Ordner. Dort wird `recht-agb` in Microsoft Copilot Studio
einem Agenten als **Skill** hinzugefügt, als ZIP-Datei mit `SKILL.md`, `LICENSE`, `references/` und `commands/`, also mit
demselben Prüftext. Slash-Befehle gibt es dort nicht, den Modus nennen Sie in der Anfrage. Abgerechnet wird
über die Copilot Credits des eigenen Microsoft-365-Mandanten (Tenant).

## Aufruf

- Slash-Befehle: `/recht-agb:abgleich`, `/recht-agb:register`, `/recht-agb:extraktion`.
- Normale Anfrage: Nennen Sie den Modus in eigenen Worten, etwa „gleiche diese Klauseln gegen das Register ab“,
  „welche entschiedenen Klauseln gibt es zur Kaution“, „löse die AGB-Klauseln aus diesem Vertrag heraus“.

Zusammenspiel: Bei einem ganzen Vertrag löst `/recht-agb:extraktion` zuerst die Klauseln heraus,
`/recht-agb:abgleich` gleicht sie danach gegen das Register ab. Die Extraktion trennt zusammengehörige
Regelungen nicht, damit eine Klausel mit der Ausnahme abgeglichen wird, die sie im Vertrag tatsächlich hat.

Was in die Zuständigkeit eines Nachbarskills fällt, sammelt der Skill unter „Zur Übergabe“: Hinter dem
Pflichtblock steht eine Übergabezeile (Skill · Modus · Fundstelle — Befund). Die Regel dazu steht in der
`SKILL.md`.

## Vertraulichkeit

Der Skill wiederholt identifizierende Angaben nicht ohne Not. Namen der Vertragsparteien, Anschriften und
Kennnummern, die für den Abgleich ohne Bedeutung sind, kürzt er im Klauselzitat mit `…`. Er ergänzt niemals
eine Angabe, die im vorgelegten Text nicht steht. Die vollständige Regel steht in der `SKILL.md`.

Das Register gibt veröffentlichte Entscheidungen wieder. Seine Klauselwortlaute stammen aus den amtlichen
Volltexten.

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

Jeder Registereintrag ist gegen den Volltext seiner Entscheidung verifiziert.

## Rechtlicher Rahmen

Der Skill erbringt **keine Rechtsdienstleistung** im Sinne des Rechtsdienstleistungsgesetzes. Er gibt keine
Auskunft über die Rechtslage, empfiehlt kein Vorgehen und ersetzt keine anwaltliche Prüfung. Er vergleicht
vorgelegte Klauseln mit einem Bestand veröffentlichter Entscheidungen und sagt, was in beiden Texten steht. Ob
eine Entscheidung auf die vorgelegte Klausel übertragbar ist, bleibt der rechtlichen Prüfung vorbehalten. Jede
Ausgabe ist von einer rechtskundigen Person zu prüfen.

Ob der Einsatz unter die KI-Verordnung (Verordnung (EU) 2024/1689) fällt, ist für das konkrete
Einsatzszenario zu prüfen. Anwendungen in der Rechtspflege können als Hochrisiko einzustufen sein; das ist
nicht pauschal zu verneinen.

Gesetze und Gerichtsentscheidungen im Volltext sind gemeinfrei (§ 5 Abs. 1 UrhG). Leitsätze kommerzieller
Anbieter, DIN-Normen und Kommentarliteratur sind urheberrechtlich geschützt, ebenso Auswahl und Anordnung in
Kommentarwerken und Handbüchern. Das Register ist ausschließlich aus den Originalentscheidungen gebaut. Ein
Handbuch darf als Fundstellenverzeichnis dienen, seine Formulierungen und seine Systematik gehen nicht in die
Referenzen ein.

## Lizenz

[MIT](LICENSE) · © 2026 Eisengallus

Der Name „Eisengallus“, das Signet und die Farbpalette sind Kennzeichen und werden von der Lizenz nicht
erfasst. „Claude“, „Claude Code“, „Anthropic“, „Cursor“, „Codex“ und „Microsoft 365 Copilot“ sind Kennzeichen
ihrer jeweiligen Inhaber und werden ausschließlich beschreibend zur Angabe der Kompatibilität verwendet.
