+++
draft = true
date = 2023-10-30T09:00:11+01:00
title = "Architecture pattern for enterprise systems"
description = ""
slug = ""
authors = ["jenka"]
tags = ["architecture", "architecture pattern"]
categories = []
externalLink = ""
series = ["architecture pattern"]
+++

(english)
## Architecture

---
# TODO
(deutsch)
## Architektur
Der Versuch, _Softwarearchitektur_ zu definieren wurde bereits in diesem [Artikel](https://codingjenka.github.io/blog/posts/architecture_designprozess/architecture) unternommen.

Im Folgenden wollen wir uns Pattern anschauen, die uns Martin Fowler in seinem vor fast 20 Jahren erschienenden Buch _"Patterns of Enterprise Applicaton Architecture"_ an die Hand gab. Bevor wir damit starten können, sollten wir jedoch kurz klären, was (1) _Enterprise Systeme_ sind und warum (2) Patterns zur Entwicklung einer Architektur sinnstiftend sein können. 


## Enterprise Systeme
Auch wenn im Titel "Enterprise Application" steht: Diese Pattern bringen Vorteile für alle Art von Anwendungen, da die Merkmal, die er hier für Enterprise Application aufzählt, heutzutage für fast jedes System gültig sind: 

- Eine Konglumerat aus einer Masse von komplexen Daten und nicht minder komplexer Businesslogik
- Irgendeine Form von Persistierung, die diese Masse an komplexen Daten für (fast) die Ewigkeit erhält
- es gibt ein reges Eigenleben dieser Daten: Sie ändern sich, ihre Struktur und ihre Werte (teilweise mehrfach) über die Zeit hinweg
- Die Daten werden von verschiedensten und zahlreichen Anwendern genutzt (in lesend und/oder schreibender Art und Weise), was zu Thematiken wie Konsistenz, Sperren, etc. führt
- Daten müssen den Anwender präsentiert werden, je nach Zielgruppe muss dies in ganz unterschiedlichen Art und Weisen erfolgen
- Und sei das nicht schon genug: Meistens interagiert das gesamte System mit irgendwelchen anderen Systemen

Enterprise Anwendungen können daher sehr groß, aber auch recht überschaubar sein. Ich denke aber, es ist die Gruppe von Anwednungen, mit denen wir Entwickler tagein, tagaus arbeiten _dürfen_. 
Was entscheidend ist: Wir müssen unser System verstanden haben. Seinen Zweck, seine Struktur, seine Besonderheiten. Erst mit diesem Verständnis können wir eine Architecture designen, die passend und somit gut ist. 

## Patterns
Es stellt sich natürlich die Frage: Wenn die Wahl der Architektur von derat maningfaltigen individuellen Faktoren abhängig ist, sind Pattern überhaupt das richtige Werkzeug dafür? Immerhin codieren sie _allgemeingültige_ Ansätze.

Christophger Alexander, ein Architekt für Bauwerke, liefert uns ein sehr schönes Zitat, dass die Funktionalität von Pattern in der Software sehr gut beschreibt: 

> Each pattern describes a problem which occurs over and over again in our environment, and then describes the core of the solution to that problem, in such a way that you can use this solution a million times over, without ever doing it the same way twice.

Patterns sind ein _allgemeingültiger_ Ansatz. Sie entsammen aus der Praxis, und stellen bets practices von Lösungsansätzen für Probleme dar, die in den vielfältigsten Systemen stetig auftreten. Patterns zu kennen, erlaubt uns, gut erprobte Entscheidungen in unser System einbauen zu können. Natürlich stets unter den o.g. Prämissen, dass man sein System kennt und den allgemeinen Lösungsansatz, die uns ein Pattern liefert, entprechend individualisiert. 