---
date: 2023-08-16
tags: 
- Mathe
- Uni
- Unter Thema
---
Ein **planarer** oder **plättbarer Graph** ist in der [[Graphen]]theorie ein [Graph](https://de.wikipedia.org/wiki/Graph_(Graphentheorie) "Graph (Graphentheorie)"), der auf einer Ebene, mit Punkten für die [Knoten](https://de.wikipedia.org/wiki/Knoten_(Graphentheorie) "Knoten (Graphentheorie)") und Linien für die [Kanten](https://de.wikipedia.org/wiki/Kante_(Graphentheorie) "Kante (Graphentheorie)"), dargestellt werden kann, sodass sich keine Kanten schneiden.

---
## Definition

Ein Graph G = ( V , E ) heißt **planar** oder **plättbar**, wenn er eine Einbettung in die [Ebene](https://de.wikipedia.org/wiki/Euklidische_Ebene "Euklidische Ebene") besitzt; das heißt, er kann in der Ebene _gezeichnet_ werden, so dass seine Kanten durch [Jordan-Kurven](https://de.wikipedia.org/wiki/Jordan-Kurve "Jordan-Kurve") repräsentiert werden, welche sich nur in gemeinsamen Endpunkten schneiden. Die **Einbettung** (auch _Zeichnung_) des Graphen ist ein [ebener Graph](https://de.wikipedia.org/wiki/Ebener_Graph "Ebener Graph"). Nach dem [Satz von Wagner und Fáry](https://de.wikipedia.org/wiki/Satz_von_Wagner_und_F%C3%A1ry "Satz von Wagner und Fáry") existiert für jeden planaren Graphen auch eine Einbettung, in welcher seine Kanten als Strecken dargestellt sind.

Durch die Einbettung wird die Ebene in zusammenhängende _Gebiete_ oder _Flächen_ geteilt, die von den Kanten des Graphen begrenzt werden. Die begrenzenden Kanten eines Gebietes bilden seinen Rand. Das unbeschränkte Gebiet um den Graphen herum wird _äußeres Gebiet_ oder _äußere Fläche_ genannt. Zwei Einbettungen heißen _äquivalent_, wenn es eine [isomorphe Abbildung](https://de.wikipedia.org/wiki/Isomorphie_von_Graphen "Isomorphie von Graphen") zwischen den Rändern ihrer Gebiete gibt.

---
## Verwandte Begriffsbildungen

Ein Graph heißt **maximal planar** oder [Dreiecksgraph](https://de.wikipedia.org/wiki/Dreiecksgraph "Dreiecksgraph"), wenn er planar ist und ihm keine [Kante](https://de.wikipedia.org/wiki/Kante_(Graphentheorie) "Kante (Graphentheorie)") hinzugefügt werden kann, ohne dass dadurch seine Planarität verloren geht.

Ein Graph heißt **fast planar** oder _kritisch planar_, wenn der Graph durch Entfernen eines beliebigen Knotens planar wird. Beispiel: [K5](https://de.wikipedia.org/wiki/Vollst%C3%A4ndiger_Graph "Vollständiger Graph") ist fast planar.

Ein Graph heißt **außerplanar** (oft auch **außenplanar** oder **kreisartig planar**), wenn er sich so in die [Ebene](https://de.wikipedia.org/wiki/Ebene_(Mathematik) "Ebene (Mathematik)") einbetten lässt, dass alle seine [Knoten](https://de.wikipedia.org/wiki/Knoten_(Graphentheorie) "Knoten (Graphentheorie)") auf dem Rand ein und desselben Gebiets liegen.

---
## Eigenschaften
- Der [Satz von Kuratowski](https://de.wikipedia.org/wiki/Satz_von_Kuratowski) gibt eine nicht-geometrische Charakterisierung von planaren Graphen. Er besagt, dass ein [Graph](https://de.wikipedia.org/wiki/Graph_(Graphentheorie) "Graph (Graphentheorie)") genau dann planar ist, wenn er keinen [Teilgraphen](https://de.wikipedia.org/wiki/Teilgraph "Teilgraph") besitzt, der ein [Unterteilungsgraph](https://de.wikipedia.org/wiki/Unterteilungsgraph "Unterteilungsgraph") des [vollständigen Graphen](https://de.wikipedia.org/wiki/Vollst%C3%A4ndiger_Graph "Vollständiger Graph") $K_{5}$ oder des vollständig [bipartiten Graphen](https://de.wikipedia.org/wiki/Bipartiter_Graph "Bipartiter Graph") $K_{3,3}$ ist. Einen Unterteilungsgraph erhält man, indem man wiederholt eine [Kante](https://de.wikipedia.org/wiki/Kante_(Graphentheorie) "Kante (Graphentheorie)") durch ein [inzidentes](https://de.wikipedia.org/wiki/Inzidenz_(Graphentheorie) "Inzidenz (Graphentheorie)") Kantenpaar ersetzt. Alternativ kann man formulieren, dass ein Graph genau dann planar ist, wenn er weder den $K_{5}$ noch den $K_{3,3}$ als [Minor](https://de.wikipedia.org/wiki/Minor_(Graphentheorie) "Minor (Graphentheorie)") enthält.
- Aus dem [Eulerschen Polyedersatz](https://de.wikipedia.org/wiki/Eulerscher_Polyedersatz "Eulerscher Polyedersatz") ergibt sich, dass die Gebietsanzahl jeder Einbettung dieselbe ist.
- Für einen planaren Graphen ohne Schleifen und Mehrfachkanten ergibt sich aus dem Polyedersatz die Abschätzung | E | ≤ 3 ⋅ | V | − 6 . Dies lässt sich für dreiecksfreie Graphen mit mindestens 3 Knoten noch auf die folgende Ungleichung verbessern: | E | ≤ 2 ⋅ | V | − 4 
- Ist ein planarer Graph [3-fach zusammenhängend](https://de.wikipedia.org/wiki/K-Zusammenhang "K-Zusammenhang"), so sind alle seine Einbettungen (bis auf eine globale Umorientierung) äquivalent.
- Ein planarer Graph mit n ≥ 3 Knoten ist genau dann maximal planar, wenn er 3 ⋅ n − 6 Kanten hat.
- Ein planarer Graph kann höchstens [5-fach zusammenhängend](https://de.wikipedia.org/wiki/K-Zusammenhang "K-Zusammenhang") sein und es gibt immer einen Knoten mit Knotengrad höchstens 5.
- Nach dem Koebe-Andreev-Thurston-Theorem existiert für jeden planaren Graphen eine assoziierte [Kreispackung](https://de.wikipedia.org/wiki/Kreispackung "Kreispackung"), deren Kontaktgraph isomorph zum Ursprungsgraph ist.

Die Planarität eines [[Graphen]] lässt sich mit verschiedenen [Algorithmen](https://de.wikipedia.org/wiki/Algorithmus "Algorithmus") in linearer [Laufzeit](https://de.wikipedia.org/wiki/Laufzeit_(Informatik) "Laufzeit (Informatik)") testen.

### Der Eulerscher Polyedersatz
Der [Eulersche Polyedersatz](https://de.wikipedia.org/wiki/Eulerscher_Polyedersatz "Eulerscher Polyedersatz") besagt, dass jeder endliche [zusammenhängende]([[zusammenhängende Graphen]]) planare [[Graphen]] mit | V | [Knoten](https://de.wikipedia.org/wiki/Knoten_(Graphentheorie) "Knoten (Graphentheorie)"), | E | [Kanten](https://de.wikipedia.org/wiki/Kante_(Graphentheorie) "Kante (Graphentheorie)") und | F | Flächen folgende [Gleichung](https://de.wikipedia.org/wiki/Gleichung "Gleichung") erfüllt:

| V | − | E | + | F | = 2 

In einem endlichen zusammenhängenden einfachen planaren Graphen wird jede Fläche von mindestens drei Kanten begrenzt, und jede Kante berührt höchstens zwei Flächen. Mit dem Polyedersatz kann man zeigen, dass für diese Graphen gilt:

| E | ≤ 3 ⋅ | V | − 6 

Der Polyedersatz gilt auch für konvexe [Polyeder](https://de.wikipedia.org/wiki/Polyeder "Polyeder"). Dies ist kein Zufall: Jedes konvexe Polyeder kann mithilfe des [Schlegeldiagramms](https://de.wikipedia.org/wiki/Schlegeldiagramm "Schlegeldiagramm") des Polyeders, einer [Zentralprojektion](https://de.wikipedia.org/wiki/Zentralprojektion "Zentralprojektion") des Polyeders auf eine [Ebene](https://de.wikipedia.org/wiki/Ebene_(Mathematik) "Ebene (Mathematik)"), deren Projektionszentrum nahe dem Zentrum einer [Seitenfläche](https://de.wikipedia.org/wiki/Seitenfl%C3%A4che "Seitenfläche") des Polyeders liegt, in einen zusammenhängenden einfachen planaren Graphen umgewandelt werden. Nicht jeder planare Graph entspricht auf diese Weise einem konvexen Polyeder: Die [Bäume](https://de.wikipedia.org/wiki/Baum_(Graphentheorie) "Baum (Graphentheorie)") zum Beispiel nicht.

Der [Satz von Steinitz](https://de.wikipedia.org/wiki/Satz_von_Steinitz "Satz von Steinitz") besagt, dass die aus konvexen [Polyedern](https://de.wikipedia.org/wiki/Polyeder "Polyeder") gebildeten [[Graphen]] genau die endlichen [3-fach zusammenhängenden](https://de.wikipedia.org/wiki/K-Zusammenhang "K-Zusammenhang") einfachen planaren Graphen sind. Im Allgemeinen gilt der Polyedersatz für jedes Polyeder, dessen Flächen einfache [Polygone](https://de.wikipedia.org/wiki/Polygon "Polygon") sind, die unabhängig von ihrer Konvexität eine Oberfläche bilden, die [topologisch](https://de.wikipedia.org/wiki/Topologie_(Mathematik) "Topologie (Mathematik)") äquivalent zu einer [Kugel](https://de.wikipedia.org/wiki/Kugel "Kugel") sind.