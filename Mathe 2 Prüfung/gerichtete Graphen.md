---
date: 2023-08-16
tags: 
- Mathe
- Uni
- Unter Thema
---
Ein **gerichteter [Graph](https://de.wikipedia.org/wiki/Graph_(Graphentheorie) "Graph (Graphentheorie)")** oder **Digraph** (von englisch _directed graph_) besteht aus

- einer [Menge](https://de.wikipedia.org/wiki/Menge_(Mathematik) "Menge (Mathematik)") von [Knoten](https://de.wikipedia.org/wiki/Knoten_(Graphentheorie) "Knoten (Graphentheorie)") ([englisch](https://de.wikipedia.org/wiki/Englische_Sprache "Englische Sprache") vertex/vertices, oft auch _Ecken_ genannt) und
- einer Menge [geordneter Knotenpaare](https://de.wikipedia.org/wiki/Geordnetes_Paar "Geordnetes Paar") E ⊆ V × V von [Kanten](https://de.wikipedia.org/wiki/Kante_(Graphentheorie) "Kante (Graphentheorie)").[1](https://de.wikipedia.org/wiki/Gerichteter_Graph#cite_note-Diestel2010-1)

Die Kanten ( v , w ) ∈ E eines gerichteten Graphen sind [gerichtete Kanten](https://de.wikipedia.org/wiki/Gerichtete_Kante "Gerichtete Kante") ([englisch](https://de.wikipedia.org/wiki/Englische_Sprache "Englische Sprache") directed edge/edges, manchmal auch _Bögen_). Diese werden häufig als Pfeile dargestellt und können nur in einer Richtung durchlaufen werden. Im Gegensatz dazu sind die Kanten eines [ungerichteten Graphen](https://de.wikipedia.org/wiki/Ungerichteter_Graph "Ungerichteter Graph") [ungeordnete Knotenpaare](https://de.wikipedia.org/wiki/Ungeordnetes_Paar "Ungeordnetes Paar") { v , w }. Gerichtete Graphen werden dazu benutzt, Objekte und die dazwischenliegenden Verbindungen, beispielsweise von [endlichen Automaten](https://de.wikipedia.org/wiki/Endlicher_Automat "Endlicher Automat"), darzustellen.

---
## Grundbegriffe
Ein gerichteter Graph ohne [Mehrfachkanten](https://de.wikipedia.org/wiki/Mehrfachkante "Mehrfachkante") und [Schleifen](https://de.wikipedia.org/wiki/Schleife_(Graphentheorie) "Schleife (Graphentheorie)") wird **einfacher Digraph**[2](https://de.wikipedia.org/wiki/Gerichteter_Graph#cite_note-2) (auch **schlichter Digraph**) genannt.

Man sagt, dass eine gerichtete Kante e = ( x , y ) von x nach y geht. Dabei ist x der _Fuß_ (oder _Startknoten_) und y der _Kopf_ (oder _Endknoten_) von e . Weiterhin gilt y als der _direkte Nachfolger_ von x und x als der _direkte Vorgänger_ von y. Falls in einem Graphen von x nach y ein [Pfad](https://de.wikipedia.org/wiki/Pfad_(Graphentheorie) "Pfad (Graphentheorie)") führt, gilt y als ein _Nachfolger_ von x und x als ein _Vorgänger_ von y . Die Kante ( y , x ) heißt _umgedrehte_ oder _invertierte Kante_ von ( x , y ).

Ein gerichteter Graph G heißt [symmetrisch](https://de.wikipedia.org/wiki/Symmetrischer_Graph "Symmetrischer Graph"), falls G zu jeder Kante auch die entsprechende invertierte Kante enthält. Ein ungerichteter Graph lässt sich einfach in einen symmetrischen gerichteten Graphen umwandeln, indem man jede Kante { x , y } durch die zwei gerichteten Kanten ( x , y ) und ( y , x ) ersetzt.

Um eine _Orientierung_ eines [[einfachen ungerichteten Graph]] zu erhalten, muss jeder Kante eine Richtung zugewiesen werden. Jeder auf diese Art konstruierte gerichtete Graph wird **orientierter Graph** genannt. Ein einfach gerichteter Graph darf, im Gegensatz zum orientierten Graphen, zwischen zwei Knoten Kanten in beide Richtungen enthalten.[1](https://de.wikipedia.org/wiki/Gerichteter_Graph#cite_note-Diestel2010-1)[3](https://de.wikipedia.org/wiki/Gerichteter_Graph#cite_note-3)[4](https://de.wikipedia.org/wiki/Gerichteter_Graph#cite_note-4)

Ein _gewichteter Digraph_ ist ein Digraph, dessen Kanten Gewichte zugeordnet werden, wodurch man einen [kantengewichteten Graphen](https://de.wikipedia.org/wiki/Kantengewichteter_Graph "Kantengewichteter Graph") erhält. Ein Digraph mit gewichteten Kanten wird in der Graphentheorie als [Netzwerk](https://de.wikipedia.org/wiki/Netzwerk_(Graphentheorie) "Netzwerk (Graphentheorie)") bezeichnet.[5](https://de.wikipedia.org/wiki/Gerichteter_Graph#cite_note-5)

Die [Adjazenzmatrix](Adjazenzmatrix.md) eines Digraphen (mit Schleifen und Mehrfachkanten) ist eine ganzzahlige [[Matrix]], deren Zeilen und Spalten den Knoten des Digraphen entsprechen. Ein Eintrag a i j außerhalb der [Hauptdiagonalen](https://de.wikipedia.org/wiki/Hauptdiagonale "Hauptdiagonale") gibt die Anzahl der Kanten vom Knoten i zum Knoten j an, und der Eintrag der Hauptdiagonalen a i i entspricht der Anzahl der Schleifen im Knoten i . Die Adjazenzmatrix eines Digraphen ist bis auf Vertauschung von Zeilen und Spalten eindeutig.

Ein Digraph lässt sich auch durch eine [[Inzidenzmatrix]] repräsentieren.

### Zusammenhängende gerichtete Graphen
→ _Hauptartikel: [Zusammenhang (Graphentheorie)](https://de.wikipedia.org/wiki/Zusammenhang_(Graphentheorie) "Zusammenhang (Graphentheorie)")_

Ein gerichteter Graph G  heißt _schwach zusammenhängend_ (oder nur _zusammenhängend_),[6](https://de.wikipedia.org/wiki/Gerichteter_Graph#cite_note-6) falls der **unterliegende Graph** von G , den man mittels Ersetzung aller gerichteter Kanten durch ungerichtete erhält, ein zusammenhängender Graph ist. Ein gerichteter Graph heißt _stark zusammenhängend_ oder _stark,_ wenn je zwei seiner Knoten gegenseitig erreichbar sind. Ein maximaler stark zusammenhängender [Untergraph](https://de.wikipedia.org/wiki/Untergraph "Untergraph") von G ist eine _starke Komponente_.

---
## Eingangs- und Ausgangsgrad
→ _Hauptartikel: [„Gerichtete Graphen“ im Artikel Grad (Graphentheorie)](https://de.wikipedia.org/wiki/Grad_(Graphentheorie)#Gerichtete_Graphen "Grad (Graphentheorie)")_

Die Anzahl der direkten Vorgänger eines Knotens wird _Eingangsgrad_ (auch _Innengrad_) und die Anzahl der direkten Nachfolger _Ausgangsgrad_ (oder _Außengrad_) genannt.

Der Eingangsgrad eines Knotens v in einem Graphen G wird mit $d_{G}$ − (v) und der Außengrad mit $d_{G}$+(v) bezeichnet. Ein Knoten mit $d_{G}$ − (v) = 0 wird **Quelle** und ein Knoten mit $d_{G}$+(v) = 0 wird _Senke_ genannt. Eine Senke heißt _universelle Senke,_ falls sie eingehende Kanten von jedem anderen Knoten hat, falls also ihr Eingangsgrad gleich | V | − 1 ist.

Für gerichtete Graphen ist die Summe aller Eingangsgrade gleich der Summe aller Ausgangsgrade, und beide gleich der Summe der gerichteten Kanten:

∑ v ∈ V d G + ( v ) = ∑ v ∈ V d G − ( v ) = | E | . ![\sum _{{v\in V}}d_{G}^{+}(v)=\sum _{{v\in V}}d_{G}^{-}(v)=|E|\,.](https://wikimedia.org/api/rest_v1/media/math/render/svg/a52463d0e6bc00dceff45ea04c605dce2e2e3583) 

Falls für alle Knoten v ∈ V die Gleichung $d_{G}$+(v) = $d_{G}$-(v) gilt, wird der Graph **balancierter Digraph** genannt.[7](https://de.wikipedia.org/wiki/Gerichteter_Graph#cite_note-7)[8](https://de.wikipedia.org/wiki/Gerichteter_Graph#cite_note-8)
