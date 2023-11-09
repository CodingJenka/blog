+++
title = 'Hexagonal architecture in software systems'
date = 2023-10-21T20:58:54+02:00
draft = true
+++


# Hexagonal architecture in software systems
<p align="center">
<img src="images/alistair.png" alt="drawing" style="width:200px;"/>
</p>


Alistair cockburn, der nette Herr von dem Bild oben, gilt als Begruender des Hexagonalen Architektur Patterns. Der Legende nach zeichnete er einfach mal Software Architektur so auf, wie er sie als besonders gut empfand. Schob ein bisschen was hierhin, was anderes dorthin und ploetzlich ergab sich das bekannte [Hexagon](https://alistair.cockburn.us/hexagonal-architecture/). Da der Name aber manchmal zu Verwirrung fuehrte (braucht man denn wirklich immer sechs Ecken????) tendiert er heutzutage eher dazu, von einer Ports-und-Adapter Architektur zu sprechen. 

## Hexagonal in a nutshell
Grundlegend fuer das Pattern ist eine starke Trennung der Fachlichkeit von der Technik. Anwendungen werden stets technisch agnostisch implementiert. 

Der Kern des Systems -- im wahrsten Sinn des Wortes -- stellt die grundlegende Identität des Systems aus. Also, welche Eigenschaften liegen ihm zugrunde. Was ist sein Charakter. Hierfuer definieren wir Entitaeten und Value Objects, die erstere unterstuetzen. Entitaeten verfuegen neben ihren Eigenschaften bereits ueber inherentes Verhalten. Einige Entitaeten und Value Objekte sind an einer bestimmten Aufgabe staerker gebunden als an anderen. Um dies auszudruecken, koennen wir Aggregate bilden. Verhalten, dass ueber mehrere Aggregate gueltig ist, wird in Domainservices festgehalten. 
Entitaeten mit spezialisierten Eigenschaften und Koennen, Value Objects, organisiert in Aggragten und aggregat-uebergreifende Funktionalitat stellt die Domaene unseres Systems dar. Es ist sein grundlegender Charakter. Das, was dieses System im Kern beschreibt. 







Ausgehend von diesen grundlegenden Eigenmschaften des Systems definieren wir alles, was das System kann. 

