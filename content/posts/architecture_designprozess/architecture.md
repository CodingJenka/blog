+++
draft = false
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

---

## The architect who is not only a developer.
Recently, a CTO person said to me, after I told him, my passion is ``software architecture``:

> But every developer should know about architecture, it's not something that needs to be done _extra_...''.

_Dear product managers, dear CTOs:_
Yes, unfortunately software architecture is something that has to be done _extra_.

Software architecture goes beyond OOP. It is not something you do once and then never touch again. Architecture is always holistic. Architecture evolves. The software architect does not only want to design a beautiful system, he also wants to make it stable, i.e. durable. He is a designer and structural engineer at the same time.

Do you do that on the side? From a cost perspective, it would probably be nice if that were the case. However, experience teaches us otherwise...

This post would like to shed some light on the unknown entity, the "_software architect_" and give a short outline about this ominous "_software architecture_".

Disclaimer beforehand: This reflects of course only my subjective view. Since there is no universal definition of both terms (sic!), the following is, of course, only _one_ opinion among many. Also I don't guarantee that I will tell something completely different about it in a few years :)

---
## The architect's goal
The architect loves ```quality```. 

He seeks them out in the requirements and knows that a system must have both, quality as well as function.
Like the civil architect, the software architect wants to build something that meets the needs of the user in terms of function and structure and, ideally, is durable over a long period of time.
A system should not only work. It should work _well_.  

The problem with technical systems, however, is that they can rot faster than fallen fruit in the warm late autumn. And if you don't pay attention, then at some point, in the truest sense of the word, the worm is within the system (and with that the maximum number of bad puns for this text is reached...). :)).
That systems erode is beyond question. The question is how fast this happens. Controlling this is also the architect's responsibility.

So the architect not only wants to create, he also wants to preserve. He is the builder, restorer and anti-aging manager of the system. (And, because he also likes the CTO, he naturally wants to maintain the quality of the system at calculable costs as constant as possible).

--- 
## _THE_ architecture.
First of all: There is no such thing as _the_ architecture. Systems are like living organisms. Individual and with quirks. If you try to create a one-size-fits-all solution, you will fail very quickly. Just as systems change, architecture must change as well.

Here, the list of factors influencing an architecture is nearly unlimited.

Some examples:

- Where is the company located? A startup has a different architectural focus than an established company. 
- Where is the product located? 
- How is the company structured? 
- What does the team for a product look like? 
- ...
- 
Good architecture adapts to different circumstances.

A good architect recognizes the signs of the times and sets the guard rails for necessary measures for the evolution of architecture.

## Architecture: An Attempt at Definition
Unfortunately, there is no universal definition for software architecture. However, we'll give it a try anyway...

### First try: ISO

ISO standards are actually always good to define things. That's why at the beginning of ISO/IEC 42010:2007 . It says:
> [Architecture is ]The fundamental organization of a system, embodied in its components, their relationships to each other and to the environment, and the principles guiding its design and evolution.

So software architecture organizes something inside and connects something with the outside. It establishes principles as guidelines that influence the design and development of the system.

So far not bad...

### Second try: Martin Fowler
Martin Fowler once said that architecture....
>are all the decisions that are difficult to change.

Also very good!

### Third try: Further...

Other views see architecture as the bridge between requirements engineering and actual implementation. Architecture includes the initial creation as well as the long-term development of the system.

### Butter by the fishes: Architecture is therefore...

... somehow all of the above. It builds the bridge between theory (technicality) and the actual translation into code. To be able to build this bridge, essential features have to be distilled. If one knows the system-relevant in function and quality, one can also bring structure and order into it. This requires brainpower and is therefore, as is often the case with tasks that require brainpower, not something that can be done at short notice, let alone quickly revised.

---

## Architektur in the enterprise environment
Michael Keeling said in his book [Design it!](https://amzn.eu/d/jdcArBr) that software always lives in a system context. System (ancient Greek sýstēma) is, according to Wikipedia, a..:

>...whole composed of several individual parts.

However, as techies we have to be careful: System is not only to be thought of technically, but also socially.

Sure, technically our software forms a system. It runs somewhere and is somehow operated by someone. It exchanges data with other systems and is developed by us as a team.

Stupidly, there is another "_out there_" that also somehow interacts with our system. Users use it. Ideally with joy. If there are problems with the system, the development team has to come back and, in the best case, just explain something. If it comes down to the wire, maybe even fix something.

Our company wants to make cash with the system. If this occurs in combination with satisfied customers, this would of course be a double bingo. At the same time, such a company also likes to express its wishes to the team (are then these ominous boundary conditions, e.g. business goals, budget, trends, etc.). ...) and thus also has an influence on the actual application.

All these factors shape the product and must be taken into account in the architecture.

---

## Architecture is... a lived value!

We don't want finished plans from the drawing board. As I said: Architecture evolves. We have to take care of this. This is only and exclusively possible if our ideas undergo a regular reality check - even if only half-finished. Our understanding is not that of others. That's why we have to get feedback from as many sides as possible, i.e. as many stakeholders as possible. Regularly.

---
## Summary

Is architecture something that every developer should be able to do? Sure. The question is: Does a developer even want to consider this always and permanently in his daily work? I mean no. Many factors (time, money, knowledge, _pragmatism_...) usually lead to the fact that just these conceptual tasks fall under the table, if one should not direct his attention specifically to it.

Do we need a dedicated architect in the team? Basically not. But we need an understanding and acceptance of the necessity of the role.


---
(deutsch)
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