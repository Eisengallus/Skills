# Fehlschlüsse

Ein Fehlschluss ist ein Schluss, der gültig aussieht und es nicht ist. Die formalen Fehler stehen
in `syllogismus.md`; hier stehen die, die an Inhalt und Aufbau der Begründung hängen. Zu jedem
steht, woran er zu erkennen ist und wann er **nicht** vorliegt.

## Zirkelschluss (circulus vitiosus) — BR-1

Ein logischer Schluss beweist sein Ergebnis nur, wenn die Prämissen anderweitig feststehen. Zirkel
ist, das zu Beweisende in den Prämissen vorauszusetzen (Puppe, Kleine Schule des juristischen
Denkens, 5. Aufl. 2023, D. V. 1.). Geprüft wird an dem Satz, den der fragliche Grund stützt: am
Ergebnis oder an einem Teilergebnis, auch an einem, das der Text nicht als solches ausweist.
Spielarten:

1. **Das Ergebnis oder ein Teilergebnis als Grund:** „Der Vertrag ist wirksam, weil er gültig
   zustande gekommen ist.“ Ein Synonym des gestützten Satzes ist kein Grund.
2. **Der Kreis über Stationen:** A wird mit B begründet, B mit C, C mit A.
3. **Die eigene These als Maßstab:** Die Gegenansicht wird verworfen, weil sie nicht verlangt, was
   die eigene Ansicht verlangt („sie verkennt, dass …“), oder ihr wird eine „Fiktion“ vorgeworfen,
   die nur besteht, wenn die eigene Ansicht richtig ist (Puppe, C. III. 3.).
4. **Subsumtion unter den umstrittenen Begriff zum Beweis desselben:** Streitig ist, ob X unter den
   Begriff fällt; der Text ordnet X dem Begriff zu und folgert daraus, dass der Begriff X umfasst.
5. **Zirkeldefinition:** Das Bestimmte steht in der Bestimmung (BG-5).

**Kein Zirkel** ist, eine These mit anderen Worten zu verdeutlichen, ihre Folgen zu zeigen oder sie
auf ein Beispiel anzuwenden, solange das nicht als Beweis auftritt; und ein Grund, der eine
Folge der These unabhängig von ihr belegt (Puppe, D. V. 1.). Entlastet ist der Verdacht nur, wenn
der Grund unabhängig von dem Satz feststeht, den er stützt: Der Text nennt für ihn eine Tatsache
oder einen Satz, der nicht schon voraussetzt, was er stützen soll. Dass der Grund nicht
gleichbedeutend ist, genügt nicht. Ein Zirkel ist nie ein Enthymem: Die fehlende Prämisse wäre der
gestützte Satz selbst.

## Petitio principii — BR-2

Eine Prämisse ist so streitig wie der Satz, den sie stützt — das Ergebnis oder ein Teilergebnis,
auch eines, das der Text nicht als solches ausweist —, und hält nur, wenn dieser Satz richtig ist.
Oft steckt sie in einer Bezeichnung: Wer die streitige Position schon „Vermögen“, „Eigentum“ oder
„Pflicht“ nennt, hat die Frage beantwortet, bevor er sie stellt. Prüffrage: Würde die Gegenseite
diese Prämisse bestreiten, und zwar aus demselben Grund, aus dem sie diesen Satz bestreitet?
Entlastet ist der Verdacht nur, wenn die Prämisse unabhängig von diesem Satz feststeht (BR-1).

Petitio principii ist auch: Der einzige Grund für ein wertendes Merkmal ist ein Maßstab, dessen
Anwendung dieselbe Frage ist wie das Merkmal, und der Text nennt für die Anwendung keine Tatsache.
Das ist BR-2, nicht SU-2; die Abgabe des Maßstabs an `[→ recht-methodik]` tritt hinzu.

## Scheinbegründung — BR-3

Ein „weil“, „da“ oder „somit“, dem kein Grund folgt: ein Bekräftigungswort („offensichtlich“,
„zweifellos“), ein Verweis auf Gründe, die nirgends genannt sind („aus den genannten Gründen“), eine
bloße Behauptung an Stelle der Subsumtion. **Zuständigkeit (Kompetenzgrenze Nr. 4):** Eine
Scheinbegründung bekommt das Flag `[→ recht-methodik]` und keine eigene Tabellenzeile — gleich, ob
ein Bekräftigungswort dasteht. **Eigener Befund bleibt sie nur, wenn sie ein Zirkel ist** (der
gestützte Satz mit anderen Worten als Grund, BR-1) **oder eine petitio principii** (BR-2). Verlangt
der eigene Obersatz des Texts ein Merkmal und bejaht der Text es ohne Tatsache, ist das SU-2, keine
Scheinbegründung, außer der einzige Grund ist ein Maßstab, dessen Anwendung dieselbe Frage ist wie
das Merkmal: dann petitio principii (BR-2).

## Scheinbegründung durch Berufung (argumentum ad verecundiam) — BR-4

Eine belegte Entscheidung als Beleg einer Rechtsfrage ist ein gewöhnlicher Beleg, kein Fehler.
Ersetzt die Berufung den Grund — das Ergebnis ruht allein auf einer Autorität, einem Meinungsstand
(„h. M.“, „allgemein anerkannt“) oder einer Übung, deren Grund der Text nicht wiedergibt, oder der
Text erklärt die Begründung für entbehrlich —, ist das eine Scheinbegründung (Zuständigkeit:
Kompetenzgrenze Nr. 4): Benenne sie an der Stelle ausdrücklich als **Scheinbegründung durch Berufung** und
gib sie mit `[→ recht-methodik]` ab, **ohne eigenen Befund** und ohne Tabellenzeile.
`[→ recht-zitat]` kommt nur zusätzlich, wenn der Nachweis fehlt oder nicht überprüfbar ist. Ob die
Entscheidung tatsächlich so lautet, sagst du nie aus dem Gedächtnis: `[prüfen: Rechtsprechung]`.

Eigener Befund bleiben zwei Fälle: Folgert der Text aus einer tatsächlichen Übung eine Geltung oder
Pflicht, ist das in den Fällen, die `deontik.md` abschließend nennt, der Schritt vom Sein zum Sollen
(DE-3); die fortgesetzte Praxis der Parteien untereinander ist es nicht; betrifft die angeführte
Aussage, wie der Text sie wiedergibt, etwas anderes als den Schluss, den er aus ihr zieht, ist das
ein Schluss ohne Verbindung (SF-6).

## Begriffsvertauschung — BG-1

Ein Wort ändert unvermerkt seine Bedeutung, und ein Satz, der für die erste Bedeutung bewiesen
ist, wird für die zweite in Anspruch genommen (Puppe, D. V. 2.). Gefährlich ist sie, wo die zweite
Bedeutung nur eine Erweiterung der ersten ist. Sie kann auch einen Widerspruch verdecken: Der Text
bejaht und verneint dasselbe Wort, meint aber zweierlei, und übergeht so die Frage, welche
Bedeutung gilt.

## Strohmann — GG-4

Die Gegenposition wird so wiedergegeben, dass sie leicht zu widerlegen ist: verkürzt, verzerrt,
mit ihrem schwächsten Argument statt ihrem stärksten, mit einem ungeschickten Beispiel. Fair ist,
die Gegenposition stark zu machen und auch ihre beste Fassung zu widerlegen (Puppe, E. I. 3.).
Wer ein Nebenargument (eine Beikarte) widerlegt und das tragende liegen lässt, hat die
Gegenposition nicht widerlegt (GG-5).

## Übersehenes Drittes — SF-4

„Wenn nicht A, dann B“ ist nur gültig, wenn A und B alle Möglichkeiten erschöpfen. Aus „der
Rechtspfleger wusste nicht, dass die Forderung nicht besteht“ folgt nicht, dass er glaubte, sie
bestehe; er kann gar keine Vorstellung gehabt haben (Puppe, C. III. 4.). Ein indirekter Beweis,
der die Gegenthese widerlegt, beweist die eigene nur, wenn beide sich wie A und nicht A verhalten.
Befund ist das Dritte, das der Text selbst nennt oder das aus seinen Begriffen folgt, wie im
Beispiel; eines, das nur dein Rechtswissen kennt, steht unter den Grenzen mit `[prüfen: Norm]`.

## Schluss ohne Verbindung (non sequitur) — SF-6

Das Ergebnis enthält etwas, das in keiner Prämisse vorkommt: eine andere Person, einen anderen
Zeitraum, eine andere Rechtsfolge. Prüffrage: Kommt jeder Begriff des Ergebnisses in einer
Prämisse vor, und zwar im selben Sinn? Mitgezählt wird die Prämisse, die die Enthymemprobe oder der
Rechtssatz als Brücke (`syllogismus.md`) zulässt. Nennt der Text für den Schritt das Merkmal, unter
das er einordnet oder an das er die Folge knüpft, und eine Tatsache dazu, ist der Schritt nicht
„ohne Verbindung“; ob die Tatsache das Merkmal belegt, prüft Schritt 5 der `SKILL.md` unverändert.
Die Bezeichnung einer Rechtsfigur, die nur zusammenfasst, was der Text schon gezeigt hat, ist kein
neuer Schluss und für sich kein SF-6.

## Das richtige Ergebnis rettet nichts

Ein Schluss mit Fehler ist falsch, auch wenn sein Ergebnis zufällig stimmt, so wie eine Rechnung
mit Rechenfehler falsch ist (Puppe, D. II. 3.). Ein Befund entfällt nicht deshalb, weil das
Ergebnis aus anderen Gründen vertretbar wäre; er entfällt nur, wenn der Text diese anderen Gründe
selbst anführt (dann ist der Defekt `mittel`).

## Tatsache und Wertung, streitige Tatsache — TW-1 bis TW-3

Siehe `urteile.md`.
