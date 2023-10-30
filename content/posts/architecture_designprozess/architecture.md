+++
draft = true
date = 2023-10-30T09:00:11+01:00
title = "The software architect. This unknown suspekt."
description = ""
slug = ""
authors = []
tags = ["architecture", "software architect"]
categories = []
externalLink = ""
series = ["architecture design process"]
+++

(english)
## Architecture

---

(deutsch)
## Der Architekt, der nicht nur Entwickelr ist. 
Ich wurde schon sehr oft mit großen Augen angeschaut, wenn ich sagte, meine Leidenschaft ist die ```Software Architektur```. Da kamen dann Sätze wie: "Aber jeder Entwickler sollte doch über Architektur Bescheid wissen, das ist ja nichts, was _extra_ gemacht werden muss..."

_Liebe Produktmanager, liebe CTOs:_

<br/> Doch, leider ist Software Architektur etwas, das _extra_ gemacht werden muss. Nicht im Elfenbeinturm. Nicht Monate im Voraus. Nicht ohne das Team. Aber von einer oder mehreren Person(en) im Team, die ein bisschen _extra_ Wissen über die Thematik haben. Es sind genau die Leute, die euch erklären können, wieso ihr gerade eben keine Microservices braucht und wie man euren alten Monolithen schrittweise und vorallem unter Sicht modernisieren kann. 

Und wenn ihr bisher die Erfahrung gemacht habt, dass Euch euer System aufgrund seiner wuchenden technischen Schulden in reglemäßigen x-Jahres Abständen zu erdrücken droht, dann, liebe Produktmanager und CTOs habt ihr wohl keinen Softwarearchitekten im Haus. 

---
## Das Ziel des Architekten
Der Architekt mag ```Qualität```.

Er spürt sie in den Anforderungen der Requirement Ingenieure auf und weiß, dass ein System neben Funktion auch Qualität haben muss. 
Wie der zivile Architekt, möchte der Softwarearchitekt etwas bauen, dass in Funktion und Aufbau den Bedürfnissen der Anwender entspricht und am besten über einen langen Zeitraum Beständigkeit aufweist. 
Ein System soll nicht nur funktionieren. Es soll _gut_ funktionieren. 

Das Problemen mit technischen Systemen ist jedoch, dass diese schneller verfaulen können als Fallobst im warmen Spätherbst. Und wenn man nicht aufpasst, dann ist in einem System im wahrsten Sinne des Wortes irgendwann der Wurm drin (und damit ist die maximale Anzahl schlechter Wortspiele auch für diesen Text erreicht... :)). 
Dass Systeme erodieren steht außer Frage. Die Frage ist, wie schnell dies passiert. Dies zu steuern, obliegt ebenfalls dem Aufgabenbereich des Architekten. 

Der Architekt will also nicht nur erschaffen, er will auch erhalten. Er ist Bauherr, Restaurator und Anti-Aging-Manager eines Systems.
(_Und, weil er auch den CTO mag, will er natürlich die Qualität des Systems unter kalkulierbaren, möglichst konstanten Kosten aufrecht erhalten._) 


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
Leider gibt es für Softwarearchitektur keine allgemeingültige Definition. 

Iso-Standarde sind eigentlich immer gut, um Dinge zu definieren. Deswegen zu Beginn der _ISO/IEC 42010:2007_ . 
Da heißt es: 
> [Architecture is ]The fundamental organization of a system, embodied in its components, their relationships to each other and to the environment, and the principles guiding its design and evolution.

Also Softwarearchitektur organisiert etwas im Inneren und verbindet etwas mit dem Außen. Sie stellt Prinzipien als Richtlinieren auf, die Einfluss auf das Design und die Entwicklung des Systems haben. 

_Martin Fowler_ sagte einmal, dass Architektur... 
> all die Entscheidungen sind, die es nur schwer zu ändern gilt. 

Anderer Ansichten sehen die Architektur als Brücke zwischen dem Requirement Engineering und der tatsächlichen Umsetzung. 
Architektur umfasst dabei die initiale Erstellung als auch die langfristige Weiterentwicklung des Systems. 

Für mich ist Architektur die Summe all dieser Definitionen. 
Sie schlägt die Brücke zwischen der Theorie (Fachlichkeit) und der tatsächlichen Übersetzung in Code. Sie unterstützt die Übersetzung Fachlichkeit -- Code, indem sie wesentliche Merkmale destilliert und diese nutzt, um ein System zu strukturieren und zu organisieren. Dies erfordert Gehirnschmalz und ist daher, wie so oft bei Aufgaben, die Gehirnschmalz fordern, nicht mal eben kurzfristig revidierbar. 

## Architektur im Enterprise Umfeld
[//]: # (Gregor Hohpe nahm einst das Bild des Software Architect Elevators )
> 

## Architektur: Als gelebter Wert
 