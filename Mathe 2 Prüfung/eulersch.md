---
date: 2023-08-16
tags: 
- Mathe
- Uni
- Unter Thema
---
Ein **Eulerkreis** (auch geschlossener **Eulerzug**, **Eulertour**) ist in der [Graphentheorie](https://de.wikipedia.org/wiki/Graphentheorie "Graphentheorie") ein [Zyklus](https://de.wikipedia.org/wiki/Zyklus_(Graphentheorie) "Zyklus (Graphentheorie)"), der alle [Kanten](https://de.wikipedia.org/wiki/Kante_(Graphentheorie) "Kante (Graphentheorie)") eines [[Graphen]] genau einmal enthält.

Ein _offener Eulerzug_ (auch _Eulerpfad_ oder _Eulerweg_) ist gegeben, wenn Start- und Endknoten nicht gleich sein müssen, wenn also statt eines [Zyklus](https://de.wikipedia.org/wiki/Zyklus_(Graphentheorie) "Zyklus (Graphentheorie)") lediglich eine [Kantenfolge](https://de.wikipedia.org/wiki/Weg_(Graphentheorie) "Weg (Graphentheorie)") verlangt wird, welche jede Kante des Graphen genau einmal enthält. Ein bekanntes Beispiel ist das „[Haus vom Nikolaus](https://de.wikipedia.org/wiki/Eulerkreisproblem#Das_Haus_vom_Nikolaus)“.

Ein [[zusammenhängende Graphen]], der einen _Eulerkreis_ besitzt, heißt _eulerscher Graph_. Enthält ein Graph lediglich einen Eulerweg und keinen Eulerkreis, so heißt er _semi-eulerscher Graph_. Die Aufgabe, zu einem gegebenen Graph zu bestimmen, ob dieser eulersch ist oder nicht, wird als **Eulerkreisproblem** bezeichnet. Es geht auf das 1736 von [Leonhard Euler](https://de.wikipedia.org/wiki/Leonhard_Euler "Leonhard Euler") gelöste [Königsberger Brückenproblem](https://de.wikipedia.org/wiki/K%C3%B6nigsberger_Br%C3%BCckenproblem "Königsberger Brückenproblem") zurück. Das Problem existiert auch für [[gerichtete Graphen]] und [Graphen mit Mehrfachkanten](https://de.wikipedia.org/wiki/Graph_mit_Mehrfachkanten "Graph mit Mehrfachkanten").

Entgegen seinem Namen ist der Eulerkreis kein [Kreis](https://de.wikipedia.org/wiki/Kreis_(Graphentheorie) "Kreis (Graphentheorie)"), zumindest wenn der häufigen Definition gefolgt wird, nach der sich in einem Kreis kein [Knoten](https://de.wikipedia.org/wiki/Knoten_(Graphentheorie) "Knoten (Graphentheorie)") wiederholen darf.

---
## Geschichte
Leonhard Euler fragte in seiner Arbeit 1736 zum Königsberger Brückenproblem – übersetzt in die heutige Fachsprache –, ob der durch die Brücken der Stadt gegebene Graph ein semi-eulerscher Graph ist, das heißt, ob ein Eulerweg existiert, und verneinte dies, da der Graph mehr als zwei Knoten mit ungeradem Grad hatte. Euler bewies, dass ein semi-eulerscher Graph höchstens zwei Knoten ungeraden [Grades](https://de.wikipedia.org/wiki/Grad_(Graphentheorie) "Grad (Graphentheorie)") haben kann.[[1]](https://de.wikipedia.org/wiki/Eulerkreisproblem#cite_note-1) Er vermutete und gab ohne Beweis an, dass dies eine hinreichende Bedingung sei: Ein zusammenhängender Graph, in dem jeder Knoten geraden Grad hat, ist ein Eulergraph. Ein Beweis des Satzes wurde zuerst von [Carl Hierholzer](https://de.wikipedia.org/wiki/Carl_Hierholzer "Carl Hierholzer") 1873 veröffentlicht.[2](https://de.wikipedia.org/wiki/Eulerkreisproblem#cite_note-2) Auf dem Beweis basiert der [Algorithmus von Hierholzer](https://de.wikipedia.org/wiki/Algorithmus_von_Hierholzer "Algorithmus von Hierholzer") zum Auffinden eines Eulerwegs.

---
## Charakterisierung
Nach dem Satz von Euler-Hierholzer sind eulersche Graphen leicht zu charakterisieren.

Sei _G_ ein Graph, bei dem höchstens eine Zusammenhangskomponente Kanten enthält. Dann sind folgende Aussagen äquivalent:

1. _G_ ist eulersch,
2. jeder Knoten in _G_ hat [geraden](https://de.wikipedia.org/wiki/Parit%C3%A4t_(Mathematik) "Parität (Mathematik)") Grad.
3. die Kantenmenge von _G_ ist die [Vereinigungsmenge](https://de.wikipedia.org/wiki/Vereinigungsmenge "Vereinigungsmenge") aller Kanten von [paarweise disjunkten](https://de.wikipedia.org/wiki/Paarweise_disjunkt "Paarweise disjunkt") Kreisen.

Analog sind für einen [[gerichtete Graphen]] _G_, bei dem höchstens eine [starke Zusammenhangskomponente](https://de.wikipedia.org/wiki/Zusammenhang_(Graphentheorie)#Gerichtete_Graphen "Zusammenhang (Graphentheorie)") Kanten enthält, folgende Aussagen äquivalent:

1. _G_ ist eulersch,
2. für jeden Knoten in _G_ sind [Eingangsgrad](https://de.wikipedia.org/wiki/Eingangsgrad "Eingangsgrad") und [Ausgangsgrad](https://de.wikipedia.org/wiki/Ausgangsgrad "Ausgangsgrad") gleich.
3. die Kantenmenge von _G_ ist die [Vereinigungsmenge](https://de.wikipedia.org/wiki/Vereinigungsmenge "Vereinigungsmenge") aller Kanten von paarweise disjunkten [gerichteten Kreisen](https://de.wikipedia.org/wiki/Gerichteter_Kreis "Gerichteter Kreis").

---
## Auffinden eines Eulerkreises
Zum Auffinden eines Eulerkreises existieren mehrere Verfahren. Der Algorithmus von Fleury stammt aus dem Jahr 1883 und verfolgt einen sehr einfachen Ansatz, weshalb er eine [Laufzeit](https://de.wikipedia.org/wiki/Laufzeit_(Informatik) "Laufzeit (Informatik)") von der Größenordnung O ( | E | 2 ) hat. Effizienter ist der [Algorithmus von Hierholzer](https://de.wikipedia.org/wiki/Algorithmus_von_Hierholzer "Algorithmus von Hierholzer"), der einen Eulerkreis in Linearzeit berechnet. Er basiert darauf, dass sich ein eulerscher Graph in paarweise kantendisjunkte Kreise zerlegen lässt.

### Algorithmus von Hierholzer
→ _Hauptartikel: [Algorithmus von Hierholzer](https://de.wikipedia.org/wiki/Algorithmus_von_Hierholzer "Algorithmus von Hierholzer")_

1. Wähle einen beliebigen Knoten v 0 des Graphen und konstruiere von v 0 ausgehend einen Kreis K in G, der keine Kante in G zweimal durchläuft.
2. Wenn K ein Eulerkreis ist, brich ab. Andernfalls:
3. Vernachlässige nun alle Kanten des Kreises K .
4. Am ersten Knoten von K , dessen Grad größer 0 ist, wird nun ein weiterer Kreis K' gebildet, der keine Kante in K durchläuft und keine Kante in G zweimal enthält.
5. Füge in K den zweiten Kreis K' ein, indem der Startknoten von K' durch alle Knoten von K' in der richtigen Reihenfolge ersetzt wird.
6. Nenne jetzt den so erhaltenen Kreis K und fahre bei Schritt 2 fort.

Die Laufzeit des Algorithmus ist linear in der Anzahl der Kanten, ist also von der Größenordnung O ( | E | ).