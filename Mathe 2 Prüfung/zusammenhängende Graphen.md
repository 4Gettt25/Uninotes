---
date: 2023-08-16
tags: 
- Mathe
- Uni
- Unter Thema
---
Der **Zusammenhang** ist ein mathematischer Begriff aus der [Graphentheorie](https://de.wikipedia.org/wiki/Graphentheorie "Graphentheorie"). Ein [Graph](Graphen) heißt zusammenhängend, wenn seine [Knoten](https://de.wikipedia.org/wiki/Knoten_(Graphentheorie) "Knoten (Graphentheorie)") paarweise durch eine [Kantenfolge](https://de.wikipedia.org/wiki/Kantenfolge "Kantenfolge") verbunden sind.

---
## Definition

### Ungerichtete Graphen
Ein [ungerichteter Graph]([[ungerichtete Graphen]]) G = ( V , E ) heißt _zusammenhängend_, falls es zu je zwei beliebigen [Knoten](https://de.wikipedia.org/wiki/Knoten_(Graphentheorie) "Knoten (Graphentheorie)") v, w  ∈ V einen [ungerichteten Weg](https://de.wikipedia.org/wiki/Ungerichteter_Weg "Ungerichteter Weg") in G mit v als Startknoten und w als Endknoten gibt.

Einen maximalen zusammenhängenden [Teilgraphen](https://de.wikipedia.org/wiki/Teilgraph "Teilgraph") eines Graphen nennt man eine _Komponente_ oder _Zusammenhangskomponente_. Ein nicht zusammenhängender Graph wird durch seine Zusammenhangskomponenten partitioniert. Die größte Zusammenhangskomponente eines Graphen spielt im [Erdős-Rényi-Modell](https://de.wikipedia.org/wiki/Zufallsgraph "Zufallsgraph") eine wichtige Rolle.
### Gerichtete Graphen
Ein [gerichteter Graph]([[gerichtete Graphen]]) G = ( V , E ) heißt _zusammenhängend von einem Knoten_ v _aus_, falls es zu jedem Knoten w aus V von v nach w gibt. G heißt _stark zusammenhängend_, falls G von jedem Knoten aus zusammenhängend ist. Anders formuliert heißt G _stark zusammenhängend_, falls es zwischen zwei beliebigen Knoten v und w aus V sowohl einen gerichteten Weg von v nach w als auch einen gerichteten Weg von nach v  in G gibt.

Ein induzierter [Teilgraph](https://de.wikipedia.org/wiki/Teilgraph "Teilgraph") G[U]für eine Knotenmenge U ⊂ V heißt _starke Zusammenhangskomponente_ von G , falls G [U] stark zusammenhängend ist und nicht zu einem größeren stark zusammenhängenden Teilgraphen von G erweitert werden kann.

Ein [gerichteter Graph]([[gerichtete Graphen]]) heißt _(schwach) zusammenhängend_, falls der zugehörige ungerichtete Graph (also der Graph, der entsteht, wenn man jede gerichtete Kante durch eine ungerichtete Kante ersetzt) zusammenhängend ist.

--- 
### Wichtige Aussagen und Sätze
Relativ leicht zeigt man folgende Aussagen:

1. Jeder zusammenhängende [ungerichtete Graph]([[ungerichtete Graphen]]) mit n [Knoten](https://de.wikipedia.org/wiki/Knoten_(Graphentheorie) "Knoten (Graphentheorie)") enthält mindestens n − 1 [Kanten](https://de.wikipedia.org/wiki/Kante_(Graphentheorie) "Kante (Graphentheorie)").
2. Jeder stark zusammenhängende [gerichtete Graph]([[gerichtete Graphen]]) mit n Knoten enthält mindestens n Kanten.
3. Ein ungerichteter Graph ist genau dann zusammenhängend, wenn er einen [Spannbaum](https://de.wikipedia.org/wiki/Spannbaum "Spannbaum") enthält.
4. Ein gerichteter Graph ist genau dann stark zusammenhängend, wenn seine [Adjazenzmatrix](https://de.wikipedia.org/wiki/Adjazenzmatrix "Adjazenzmatrix") [irreduzibel](https://de.wikipedia.org/wiki/Irreduzible_Matrix "Irreduzible Matrix") ist. Damit ist auch ein ungerichteter Graph genau dann zusammenhängend, wenn seine Adjazenzmatrix irreduzibel ist.
5. Die Klasse aller zusammenhängenden Graphen ist nicht axiomatisierbar.[¹](https://de.wikipedia.org/wiki/Zusammenhang_(Graphentheorie)#cite_note-1)
