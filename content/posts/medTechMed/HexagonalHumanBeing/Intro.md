+++
title = 'See the human as a hexagonal architecture system'
date = 2023-10-21T20:58:54+02:00
draft = true
+++


# See the human as a hexagonal architecture system

Oftmals sehen wir uns den Widrigkeiten des Lebens so unfassbar hilflos gegenueber gestellt und vergessen fast vollstaendig, wer wir sind und was uns ausmacht. Wir denken, Momentaufnahmen seien ein Fuer-Immer. Dies fuehrt mitunter in Verzweiflung. 

Beschreiben wir in der Informatik ein derartiges System, eines, dass verschiedenen Anforderungen nicht im ausreichenden Maße gewachsen ist, kaum evolvierbar, als in seiner Implementierung starr, ist und nicht langfristig betrieben werden kann, dann ist dies meist ein Prototyp. 
Wir entwickeln Prototypen, um schnell mal was auszuprobieren. Um zu sehen, ob eine Idee auch fuer ein Problem ein passende Loesung sein kann. Prototypen sind nicht produktionsreif (auch wenn einige CEOs immer wieder versuchen, das Gegenteil zu beweisen und sei es, indem sie es MVP nennen). Klar, sie sind nich ausgereift. Sie haben keinen wirklichen Kern. Sie sind Schablonen, Testballons. 

Wenn wir langlebige Software entwickeln wollen, dann stellen wir diese auf ein solides Designfundament. Wir haben verstanden, gegen welche Probleme es kaempfen soll und denken uns Eigenschaften aus, damit es vielversprechend diesen Kampf gewinnen kann. Wir wissen, wir brauchen Struktur in diesem System. Entropie greift schneller um sich, als uns lieb uns. Sprich: Fehlt Struktur, wird alles ganz schnell zu einem großem Chaos. Keiner blickt mehr durch. Dinge zu verbessern, zu fixen oder zu ergaenzen benoetigt zunehmend mehr Kraft. Irgendwann ist es zu anstrengend und wir kapitulieren. 


Um Struktur in unser System zu bekommen, haben sich schlaue Menschen schlaue Schablonen ausgedacht. Egal ob 3-Tier, Onion oder Hexagonal: Allen gemein ist der Wunsch, sauber verschiedenen Aufgaben zu trennen. Wir erschaffen uns Bereiche, die fuer bestimmte Dinge verantwortlich sind. Trennen wir zum Beispiel das "Was das System macht" von dem "Wie es das umsetzt" befaehigen wir uns, stabile Systeme zu schaffen, die voellig isoliert von einer Außenwelt, den Kern ihres Koennens und ihrer Faehigkeit begreift. Ausgestattet mit diesem Wissen ist es so in der Lage, mit einem bunten, sich stetig aendernden, Katalog an Dingen von außen interagieren zu koennen. 

Warum betrachten wir Menschen nicht so?
Wieso haben wir nicht das gleiche Verstaednis von uns selbst? Kennen unseren Kern und unsere Faehigkeiten und nutzen diese, um mit der Außenwelt in Kontakt treten zu koennen? 
Wieso ist es meist so, dass wir zuerst die Komplexitaet der Anforderungen sehen, die an uns heran getragen werden und  in einem Gefuehl von "Das kann ich nicht / das schaffe ich nicht / dem bin ich nicht gewachsen" verlieren anstatt uns von innen heraus zu betrachten und zu erkennen, auf welche Faehigkeiten wir momentan programmiert sind und welchen Herausforderungen wir uns damit aktuell stellen koennen? 

Diese Serie versucht, den Meschen nach einem hexagonalen Softwarearchitecktur Pattern zu verstehen. 