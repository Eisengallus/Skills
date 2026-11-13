# Eisengallus · Prüfwerkzeuge für juristische Texte

Acht Skills für agentische Systeme (Claude Code, Cursor, Codex, Microsoft 365 Copilot). Sie prüfen die **Machart**
juristischer Texte nach deutschem Recht: Wortlaut, Schluss, Überzeugungskraft, Methode, Beweisführung,
Anspruchsaufbau, Klauseln und Belegform. Sie decken keine Rechtsgebiete ab und sagen nicht, wie ein Fall
ausgeht. Geprüft wird, ob ein Text seine eigenen Schritte offenlegt und ob sie tragen.

> **Keine Rechtsberatung.** Die Skills sind Werkzeuge und erbringen keine Rechtsdienstleistung im Sinne des
> Rechtsdienstleistungsgesetzes. Jede Ausgabe ist von einer rechtskundigen Person zu prüfen. Siehe
> [Rechtlicher Rahmen](#rechtlicher-rahmen).

## Die acht Skills

| Skill | Frage | Kommandos |
|---|---|---|
| [`recht-grammatik`](recht-grammatik/) | Lässt der Wortlaut nur die gemeinte Lesart zu? | `:mehrdeutigkeit` `:zeichensetzung` `:norm` `:umformulieren` |
| [`recht-logik`](recht-logik/) | Ergibt sich das Ergebnis zwingend aus den Voraussetzungen? | `:pruefen` `:klausel` `:vergleich` `:norm` `:korrektur` |
| [`recht-rhetorik`](recht-rhetorik/) | Überzeugt der Text den, für den er geschrieben ist? | `:stresstest` `:status` `:gliederung` `:adressat` `:schriftsatz` |
| [`recht-methodik`](recht-methodik/) | Ist der Weg von der Norm zum Ergebnis tragfähig? | `:auslegung` `:analogie` `:relation` `:stil` |
| [`recht-beweis`](recht-beweis/) | Trägt der Weg von der Behauptung zur Feststellung? | `:verfahren` `:last` `:vermutung` `:mass` `:angebot` |
| [`recht-anspruch`](recht-anspruch/) | Sind die Anspruchsgrundlagen vollständig und in tragfähiger Ordnung geprüft? | `:schema` `:aufbau` `:vollstaendigkeit` `:konkurrenz` |
| [`recht-agb`](recht-agb/) | Gibt es zu dieser Klausel eine Entscheidung? | `:abgleich` `:extraktion` `:register` |
| [`recht-zitat`](recht-zitat/) | Ist jeder Nachweis so angegeben, dass man ihn findet? | `:pruefen` `:liste` |

Ein Kommando wird mit dem Namen des Skills aufgerufen, etwa `/recht-beweis:last`. Ohne Kommando genügt eine
Anfrage in eigenen Worten („prüfe die Beweisführung“). Jeder Ordner hat eine eigene `README.md` mit den Modi,
den Grenzen und Beispielen für den Aufruf.

## Wie die Skills zusammenarbeiten

**Ein Befund, ein Eigentümer.** Jede Fehlerart gehört genau einem Skill. Findet ein Skill etwas, das in die
Zuständigkeit eines anderen fällt, prüft er es nicht selbst. Er gibt es mit einem Verweis ab, etwa
`[→ recht-logik]`, und sammelt es am Ende seines Berichts unter „Zur Übergabe“.

Über einem Schriftsatz bietet sich diese Reihenfolge an:

```
/recht-grammatik:mehrdeutigkeit → /recht-methodik:auslegung → /recht-beweis:last
  → /recht-logik:pruefen → /recht-rhetorik:stresstest
```

Erst der Wortlaut, dann die Gewinnung der Prämissen, dann ihre tatsächliche Grundlage, dann der Schluss aus
ihnen, zuletzt die Wirkung auf den Adressaten.

## Gemeinsame Grundsätze

- **Der Nullbefund ist der Regelfall.** Der Abschnitt „Befunde“ ist kein Formularfeld, das gefüllt werden
  will. Ein Befund muss mehrere Proben bestehen, bevor er gemeldet wird. Dass ein Ausschnitt kurz ist oder
  eine Selbstverständlichkeit nicht ausspricht, ist kein Mangel.
- **Kein Norminhalt aus dem Gedächtnis.** Hängt ein Schritt von einer Vorschrift oder Entscheidung ab, setzt
  der Skill `[prüfen: Norm]` oder `[prüfen: Rechtsprechung]` und formuliert konditional. Fundstellen, die nicht
  im Text stehen, werden nicht erfunden.
- **Vertraulichkeit.** Namen, Aktenzeichen und Anschriften werden nur wiederholt, soweit die Beanstandung
  ohne sie nicht verständlich wäre.

## Installation

Die Skills bestehen aus Textdateien: keine Programme, keine Server, keine Netzverbindung. Jeder Skill ist ein
Ordner. Kopieren Sie den Ordner des gewünschten Skills in den Skill-Ordner Ihres Werkzeugs, bei Claude Code
nach `~/.claude/skills/`, bei Cursor nach `~/.cursor/skills/` und bei Codex nach `~/.codex/skills/`.

Nach dem Neustart des Werkzeugs steht der Skill bereit. Die Skills sind unabhängig voneinander. Sie können
einen einzelnen oder alle acht installieren.

Für **Microsoft 365 Copilot** gibt es keinen Skill-Ordner. Dort wird der Skill in Microsoft Copilot Studio
einem Agenten als ZIP-Datei mit `SKILL.md`, `references/` und `commands/` hinzugefügt. Slash-Befehle gibt es
dort nicht, den Modus nennen Sie in der Anfrage.

## Was dieses Repositorium enthält

Enthalten sind die acht Skills: je Ordner die Anweisung (`SKILL.md`), die Referenztexte (`references/`), die
Kommandos (`commands/`), die Manifeste, eine `README.md` und eine Kopie der `LICENSE`, damit der Lizenzvermerk
mitgeht, wenn nur ein einzelner Ordner kopiert wird.

## Wie die Skills geprüft werden

Jede Fassung eines Skills wird an frei erfundenen Prüffällen gemessen: an fehlerhaften Texten, in denen der Skill
den Fehler finden soll, und an fehlerfreien, an denen er nichts beanstanden darf. Eine Änderung wird nur
übernommen, wenn sie auf keiner der beiden Seiten schlechter abschneidet.

## Rückmeldungen

Fehler, Fehlalarme und Vorschläge melden Sie bitte als **Issue** über das Formular: mit dem geprüften Text,
dem Kommando und der Antwort des Skills. Issues sind öffentlich: Verwenden Sie nur erfundene oder vollständig
anonymisierte Texte, ohne Mandats-, Geschäfts- oder personenbezogene Daten. Pull Requests nimmt dieses
Repositorium nicht an. Was aus einem Issue folgt, fließt über eine gemessene neue Fassung ein.

## Herkunft

`recht-grammatik`, `recht-rhetorik` und `recht-logik` gehen auf die drei Pakete des russischen
Damascus-Ink-Trivium von Sofya Smirnova zurück, `recht-logik` dazu auf `logika` von Pavel Rykov:

- [sky-magenta/pravo-grammatika](https://github.com/sky-magenta/pravo-grammatika)
- [sky-magenta/pravo-ritorika](https://github.com/sky-magenta/pravo-ritorika)
- [sky-magenta/pravo-logika](https://github.com/sky-magenta/pravo-logika)
- [EvilFreelancer/logika](https://github.com/EvilFreelancer/logika)

Die Vorbilder stehen unter der MIT-Lizenz. Die drei Skills sind für das deutsche Recht neu geschrieben und
enthalten keinen Text der Vorbilder mehr. Die übrigen fünf Skills sind eigene Arbeiten ohne Vorbild.

## Rechtlicher Rahmen

Die Skills erbringen **keine Rechtsdienstleistung** im Sinne des Rechtsdienstleistungsgesetzes. Sie geben
keine Auskunft über die Rechtslage, empfehlen kein Vorgehen und ersetzen keine anwaltliche Prüfung. Sie prüfen,
ob ein Text seine eigenen Schritte offenlegt und ob sie zueinander passen.

Ob der Einsatz unter die KI-Verordnung (Verordnung (EU) 2024/1689) fällt, ist für das konkrete
Einsatzszenario zu prüfen. Anwendungen in der Rechtspflege können als Hochrisiko einzustufen sein; das ist
nicht pauschal zu verneinen.

Gesetze und Gerichtsentscheidungen im Volltext sind gemeinfrei (§ 5 Abs. 1 UrhG). Leitsätze kommerzieller
Anbieter, DIN-Normen und Kommentarliteratur sind urheberrechtlich geschützt. Die Skills übernehmen Leitsätze
nicht und geben Kommentarliteratur nicht wieder. Zulässig sind Paraphrase und Fundstelle. Von DIN-Normen
nennen sie nur Nummer, Titel, Ausgabestand und Abschnitt. Die Beispiele in den Skills sind frei erfunden. Wo
ein Register oder eine Referenz eine Entscheidung nennt, ist es eine echte Entscheidung mit Fundstelle.

## Lizenz

[MIT](LICENSE) · © 2026 Eisengallus

Die Lizenz erfasst die Texte dieses Repositoriums. Der Name „Eisengallus“, das Signet und die Farbpalette sind
Kennzeichen und werden von ihr nicht erfasst.

„Claude“, „Claude Code“, „Anthropic“, „Cursor“, „Codex“, „Microsoft 365 Copilot“ und „Copilot Studio“ sind
Kennzeichen ihrer jeweiligen Inhaber. Sie werden ausschließlich beschreibend zur Angabe der Kompatibilität
verwendet. Eine Verbindung, Unterstützung oder Billigung durch die Inhaber besteht nicht.
