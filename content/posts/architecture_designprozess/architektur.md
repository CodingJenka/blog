+++
draft = true
date = 2023-11-05T09:00:11+01:00
title = "The software architect. This unknown suspekt."
description = ""
slug = ""
authors = []
tags = ["architecture", "software architect"]
categories = []
externalLink = ""
series = ["architecture design process"]
+++


> _you can find the englisch version [here](https://codingjenka.github.io/blog/posts/architecture_designprozess/architecture.md)_

---
## Der Architekt, der nicht nur Entwickler ist.
Letztens sagte ein CTO-Mensch in einem Gespräch zu mir, nachdem ich zu ihm meinte, meine Leidenschaft sei die ```Software Architektur```:

>Aber jeder Entwickler sollte doch über Architektur Bescheid wissen, das ist ja nichts, was _extra_ gemacht werden muss...

_Liebe Produktmanager, liebe CTOs:_
Doch, leider ist Software Architektur etwas, das _extra_ gemacht werden muss.

<br/> Software Architektur geht über OOP hinaus. Es ist nichts, was man nur einmal macht und dann nie wieder anfässt. Architektur ist immer ganzheitlich. Architektur evolviert. Der Softwarearchitekt möchte nicht nur ein schönes System entwerfen, er möchte es auch stabil, sprich langlebig aufstellen. Er ist Gestalter und Statiker zugleich. 

Macht man das nebenher? Aus Kostensicht gesehen, wäre es wohl schön, wenn dem so wäre. Die Erfahrung lehrt uns jedoch etwas anderes...

Dieser Post möchte einmal das unbekannte Wesen, den "_Softwarearchitekten_" beleuchten und einen kurzen Abriss über diese ominöse "_Softwarearchitektur_" geben.

Disclaimer vornweg: Dies spiegelt natürlich nur meine subjektive Ansicht wieder. Da es keine allgemeingültige Definition beider Begriffe gibt (sic!), ist das Folgende natürlich nur _eine_ Meinung von vielen. Auch garantiere ich nicht, dass ich in ein paar Jahren etwas komplett anderes darüber erzählen werde :)

[//]: # (Er Nicht im Elfenbeinturm. Nicht Monate im Voraus. Nicht ohne das Team. Aber von einer oder mehreren Person&#40;en&#41; im Team, die ein bisschen _extra_ Wissen über die Thematik haben. Es sind genau die Leute, die euch erklären können, wieso ihr gerade eben keine Microservices braucht und wie man euren alten Monolithen schrittweise und vorallem unter Sicht modernisieren kann. )

[//]: # (Und wenn ihr bisher die Erfahrung gemacht habt, dass Euch euer System aufgrund seiner wuchenden technischen Schulden in reglemäßigen x-Jahres Abständen zu erdrücken droht, dann, liebe Produktmanager und CTOs habt ihr wohl keinen Softwarearchitekten im Haus. )

---
## Das Ziel des Architekten
Der Architekt mag ```Qualität```.

Er spürt sie in den Anforderungen der Requirement Ingenieure auf und weiß, dass ein System neben Funktion auch Qualität haben muss.
Wie der zivile Architekt, möchte der Softwarearchitekt etwas bauen, dass in Funktion und Aufbau den Bedürfnissen der Anwender entspricht und am besten über einen langen Zeitraum Beständigkeit aufweist.
Ein System soll nicht nur funktionieren. Es soll _gut_ funktionieren.

Das Problemen mit technischen Systemen ist jedoch, dass diese schneller verfaulen können als Fallobst im warmen Spätherbst. Und wenn man nicht aufpasst, dann ist in einem System irgendwann, im wahrsten Sinne des Wortes, der Wurm drin (und damit ist die maximale Anzahl schlechter Wortspiele auch für diesen Text erreicht... :)).
Dass Systeme erodieren, steht außer Frage. Die Frage ist, wie schnell dies passiert. Dies zu steuern, obliegt ebenfalls dem Aufgabenbereich des Architekten.

Der Architekt will also nicht nur erschaffen, er will auch erhalten. Er ist Bauherr, Restaurator und Anti-Aging-Manager eines Systems.
(_Und, weil er auch den CTO mag, will er natürlich die Qualität des Systems unter kalkulierbaren, möglichst konstanten Kosten aufrecht erhalten._)

---
## _DIE_ Architektur

Allem voran: Es gibt nicht _die_ Architektur. Systeme sind wie lebende Organismen. Individuell und mit Marotten. Versucht man hier ein _Ein-für-Alles_ wird man sehr schnell scheitern. Genauso wie sich Systeme verändern, muss sich auch die Architektur verändern.

Hierbei ist die Liste der Einflussfaktoren auf eine Architektur annähernd unlimitert.

Einige Beispiele:

- Wo befindet sich das Unternehmen? Ein StartUp setzt in der Architektur einen anderen Schwerpunkt als ein etabliertes Unternehmen
- Wo befindet sich das Produkt?
- Wie ist das Unternehmen strukturiert?
- Wie schaut das Team für ein Produkt aus?
- ...

Gute Architektur passt sich den unterschiedlichen Gegebenheiten an.

Ein guter Architekt erkennt die Zeichen der Zeit und setzt die Leitplanken für notwendige Maßnahmen für die Evolution der Architektur.

## Architektur: Ein Definitionversuch
Leider gibt es für Softwarearchitektur keine allgemeingültige Definition. Wir versuchen es aber trotzdem mal...

#### Erster Versuch: ISO
ISO-Standarde sind eigentlich immer gut, um Dinge zu definieren. Deswegen zu Beginn der _ISO/IEC 42010:2007_ .
Da heißt es:
> [Architecture is ]The fundamental organization of a system, embodied in its components, their relationships to each other and to the environment, and the principles guiding its design and evolution.

Also Softwarearchitektur organisiert etwas im Inneren und verbindet etwas mit dem Außen. Sie stellt Prinzipien als Richtlinieren auf, die Einfluss auf das Design und die Entwicklung des Systems haben.

Soweit nicht schlecht...

#### Zweiter Versuch: Martin Fowler
_Martin Fowler_ sagte einmal, dass Architektur...
> all die Entscheidungen sind, die es nur schwer zu ändern gilt.

Auch sehr gut!

#### Dritter Versuch: Weiteres...
Anderer Ansichten sehen die Architektur als Brücke zwischen dem Requirement Engineering und der tatsächlichen Umsetzung.
Architektur umfasst dabei die initiale Erstellung als auch die langfristige Weiterentwicklung des Systems.

#### Butter bei der Fische: Architektur ist also...
... irgendwie all das.
Sie schlägt die Brücke zwischen der Theorie (Fachlichkeit) und der tatsächlichen Übersetzung in Code. Um diese Brücke schlagen zu können, müssen wesentliche Merkmale destilliert werden. Kennt man das Systemrelevante in Funktion und Qualität, kann man auch Struktur und Ordnung hineinbringen.
Sowas erfordert Gehirnschmalz und ist daher, wie so oft bei Aufgaben, die Gehirnschmalz fordern, nicht mal eben kurzfristig mach- geschweige denn schnell mal revidierbar.

--- 

## Architektur im Enterprise Umfeld
[//]: # (Gregor Hohpe nahm einst das Bild des Software Architect Elevators )
Michael Keeling sagte in seinem Buch [Design it!](https://amzn.eu/d/jdcArBr), dass Software stets in einem Systemkontxt lebt. System (altgriechisch sýstēma) ist laut [Wikipedia](https://de.wikipedia.org/wiki/System) ein...:
>...*aus mehreren Einzelteilen zusammengesetztes Gan*zes

Wir müssen als Techis jedoch aufpassen: System ist hier nicht nur technisch, sondern auch sozial zu denken.

Klar, technisch bildet unsere Sofware ein System. Das läuft irgendwo und wird irgendwie von irgend jemanden betrieben. Es tauscht Daten mit anderen Systemen aus und wird von uns als Team entwickelt.

Blöderweise gibt es noch ein "_da draußen_", das auch irgendwie mit unserem System interagiert. Anwender nutzen es. Idealerweise mit Freude. Gibt es Probleme mit dem System, muss das Entwicklerteam wieder anrücken und im besten Fall nur etwas erklären. Wenn es spitz auf Knopf kommt vielleicht aber sogar etwas fixen.

Unser Unternehmen will Cash mit dem System machen. Tritt das in Kombination mit zufriedenen Kunden auf, wäre dies natürlich ein Doppelbingo. Gleichzeitig äußert so ein Unternehmen auch mal gerne _seine_ Wünsche an das Team (sind dann diese ominösen _Randbedingungen_, z.B. Geschäftsziele, Budget, Trends, etc. ...) und hat somit auch Einfluss auf die eigentliche Anwendung.

All diese Faktoren shapen das Produkt und müssen in der Architektur berücksichtigt werden.

---

## Architektur ist... ein gelebter Wert!
Wir wollen keine fertigen Pläne vom Reißbrett. Wie gesagt: Architektur evolviert. Dem müssen wir Sorge tragen. Dies ist nur und ausschließlich möglich, wenn sich unsere Ideen einem regelmäßigen Realitätscheck unterziehen -- auch wenn nur halbfertig. Unser Verständnis ist nicht das der anderen. Daher müssen wir Feedback einholen, von möglichst vielen Seiten, sprich möglichst vielen Stakeholdern. Regelmäßig.

---

## Zusammenfassung
Ist Architektur also etwas, dass jeder Entwickler können sollte? Klar. Die Frage ist: Will ein Entwickler dies überhaupt immer und permanent in seiner täglichen Arbeit berücksichtigen? Ich meine nein. Viele Faktoren (Zeit, Geld, Wissen, _Pragmatismus_...) führen meist dazu, dass gerade diese konzeptuellen Aufgaben unterm Tisch fallen, sollte man nicht gezielt seine Aufmerksam darauf richten.

Brauchen wir einen dedizierten Architekten im Team? Im Grunde nicht. Wir brauchen aber ein Verständnis und die Akzeptanz über die Notwendigkeit der Rolle. 