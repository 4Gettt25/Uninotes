---
date: 2023-08-16
tags: 
- Mathe
- Uni
- Unter Thema
---
Ein **Hamiltonkreis** ist ein geschlossener [Pfad](https://de.wikipedia.org/wiki/Weg_(Graphentheorie) "Weg (Graphentheorie)") in einem [[Graphen]], der jeden [Knoten](https://de.wikipedia.org/wiki/Knoten_(Graphentheorie) "Knoten (Graphentheorie)") genau einmal enthält. Die Frage, ob ein solcher Kreis in einem gegebenen Graphen existiert, ist ein wichtiges Problem der [Graphentheorie](https://de.wikipedia.org/wiki/Graphentheorie "Graphentheorie"). Im Gegensatz zum leicht lösbaren [Eulerkreisproblem]([[eulersch]]), bei dem ein Kreis gesucht wird, der alle [Kanten](https://de.wikipedia.org/wiki/Kante_(Graphentheorie) "Kante (Graphentheorie)") genau einmal durchläuft, ist das **Hamiltonkreisproblem** [NP-vollständig](https://de.wikipedia.org/wiki/NP-Vollst%C3%A4ndigkeit "NP-Vollständigkeit").

Man unterscheidet das **Gerichtete Hamiltonkreisproblem** in gerichteten Graphen und das **Ungerichtete Hamiltonkreisproblem** in ungerichteten Graphen. Eine Verallgemeinerung des Hamiltonkreisproblems ist das [Problem des Handlungsreisenden](https://de.wikipedia.org/wiki/Problem_des_Handlungsreisenden "Problem des Handlungsreisenden"), bei dem nach einem _kürzesten_ Hamiltonkreis in einem Graphen mit Kantengewichten gefragt wird.

---
## Geschichte
Namensgeber des Problems ist der irische [Astronom](https://de.wikipedia.org/wiki/Astronom "Astronom") und [Mathematiker](https://de.wikipedia.org/wiki/Mathematiker "Mathematiker") [Sir William Rowan Hamilton](https://de.wikipedia.org/wiki/Sir_William_Rowan_Hamilton "Sir William Rowan Hamilton"), der 1857 das Spiel „The [Icosian Game](https://de.wikipedia.org/wiki/Icosian_Game "Icosian Game")“ erfand (und später verbesserte zum „Traveller's Dodecahedron or A Voyage Round The World“).

Der „Traveller's Dodecahedron“ besteht aus einem hölzernen, regulären [Dodekaeder](https://de.wikipedia.org/wiki/Dodekaeder "Dodekaeder"), wobei die 20 Knoten mit Namen bekannter Städte assoziiert sind. Ziel ist es, eine Reiseroute entlang der [Kanten](https://de.wikipedia.org/wiki/Kante_(Graphentheorie) "Kante (Graphentheorie)") des Dodekaeders zu finden, die jede Stadt genau einmal besucht und dort aufhört, wo sie beginnt.

Zunächst erscheint die Aufgabenstellung ähnlich dem 1736 von [Leonhard Euler](https://de.wikipedia.org/wiki/Leonhard_Euler "Leonhard Euler") (verneinend) gelösten [Königsberger Brückenproblem](https://de.wikipedia.org/wiki/K%C3%B6nigsberger_Br%C3%BCckenproblem "Königsberger Brückenproblem"), einem Spezialfall des [Eulerkreisproblems](https://de.wikipedia.org/wiki/Eulerkreisproblem "Eulerkreisproblem") und Grundsteinlegung der Graphentheorie. Während für das Eulerkreisproblem aber besonders effiziente Lösungs-Algorithmen existieren, ist bekannt, dass beide Varianten des Hamiltonkreisproblems besonders schwer algorithmisch lösbare Probleme sind. Sowohl die gerichtete als auch die ungerichtete Variante des Hamiltonkreisproblems gehört zur Liste der [21 klassischen NP-vollständigen Probleme](https://de.wikipedia.org/wiki/Karps_21_NP-vollst%C3%A4ndige_Probleme "Karps 21 NP-vollständige Probleme"), für die [Richard M. Karp](https://de.wikipedia.org/wiki/Richard_M._Karp "Richard M. Karp") 1972 in seinem berühmten Artikel die Zugehörigkeit zu dieser Klasse von Problemen nachgewiesen hat.

---
## Definition
Sei G = ( V , E ) ein Graph mit | V | = n [Knoten](https://de.wikipedia.org/wiki/Knoten_(Graphentheorie) "Knoten (Graphentheorie)") (oder Ecken) und | E | = m [Kanten](https://de.wikipedia.org/wiki/Kante_(Graphentheorie) "Kante (Graphentheorie)").

G heißt _hamiltonsch_, wenn er einen _Hamiltonkreis_ zulässt, d. h., wenn es einen [Kreis](https://de.wikipedia.org/wiki/Kreis_(Graphentheorie) "Kreis (Graphentheorie)") in G gibt, der alle Knoten aus V enthält. Ein _Hamiltonpfad_ ist ein [Pfad](https://de.wikipedia.org/wiki/Weg_(Graphentheorie) "Weg (Graphentheorie)") in G , der alle Knoten aus V enthält. Hat G Hamiltonpfade, jedoch keinen Hamiltonkreis, so heißt G _semihamiltonsch_.

Zur _Potenz eines Graphen_: Für einen Graphen G und d ∈ N bezeichnet G d den Graphen auf V , bei dem zwei Knoten genau dann [benachbart](https://de.wikipedia.org/wiki/Nachbarschaft_(Graphentheorie) "Nachbarschaft (Graphentheorie)") sind, wenn sie in G einen [Abstand](https://de.wikipedia.org/wiki/Abstand_(Graphentheorie) "Abstand (Graphentheorie)") kleiner gleich d haben. Offenbar gilt G = $G^{1}$ ⊆ $G^{2}$ ⊆ $G^{3}$ ⊆ … .

Ein beliebiges Tupel ( $a_{1}$ , … , $a_{n}$ ) [natürlicher Zahlen](https://de.wikipedia.org/wiki/Nat%C3%BCrliche_Zahl "Natürliche Zahl") heißt _hamiltonsch_, wenn jeder Graph mit n Knoten und punktweise größerer [Gradsequenz](https://de.wikipedia.org/wiki/Gradsequenz "Gradsequenz") hamiltonsch ist. Eine Gradsequenz ( $d_{1}$ , … , $d_{n}$ ) heißt dabei _punktweise größer_ als ( $a_{1}$ , … , $a_{n}$ ) , wenn $d_{i}$ ≥ $a_{i}$ gilt für alle i.

Ein Graph G heißt _hypohamiltonsch_, wenn er keinen hamiltonschen Kreis besitzt, aber zu jedem seiner Knoten ein Kreis existiert, der alle anderen Knoten enthält.

Der _Hamiltonabschluss_ eines Graphen G ist der [Obergraph](https://de.wikipedia.org/wiki/Obergraph "Obergraph") von G mit identischer Knotenmenge und zusätzlich [iterativ](https://de.wikipedia.org/wiki/Iteration "Iteration") eingefügten Kanten, die nichtadjazente Knoten mit Gradsumme größer gleich n miteinander verbinden, solange dies möglich ist. Der Hamiltonabschluss eines Graphen ist eindeutig.

---
## Eigenschaften
Jeder Hamiltonkreis kann durch Entfernen einer seiner [Kanten](https://de.wikipedia.org/wiki/Kante_(Graphentheorie) "Kante (Graphentheorie)") in einen Hamiltonweg umgewandelt werden. Ein Hamiltonweg kann jedoch nur dann zu einem Hamiltonkreis erweitert werden, wenn seine Endknoten benachbart sind.

Alle hamiltonschen Graphen sind 2-[zusammenhängend]([[zusammenhängende Graphen]]), aber ein 2-zusammenhängender Graph muss nicht hamiltonsch sein, zum Beispiel der [Petersen-Graph](https://de.wikipedia.org/wiki/Petersen-Graph "Petersen-Graph").

Ein [eulerscher Graph](https://de.wikipedia.org/wiki/Eulerscher_Graph "Eulerscher Graph"), also ein [zusammenhängender Graph]([[zusammenhängende Graphen]]), in dem jeder [Knoten](https://de.wikipedia.org/wiki/Knoten_(Graphentheorie) "Knoten (Graphentheorie)") einen geraden [Grad](https://de.wikipedia.org/wiki/Grad_(Graphentheorie) "Grad (Graphentheorie)") hat, besitzt notwendigerweise einen Eulerkreis, wobei der geschlossene Weg genau einmal durch jede [Kante](https://de.wikipedia.org/wiki/Kante_(Graphentheorie) "Kante (Graphentheorie)") verläuft. Dieser [Weg](https://de.wikipedia.org/wiki/Weg_(Graphentheorie) "Weg (Graphentheorie)") entspricht einem Hamiltonkreis im zugehörigen [Kantengraphen](https://de.wikipedia.org/wiki/Kantengraph "Kantengraph"), sodass der Kantengraph jedes eulerschen Graphen ein hamiltonscher Graph ist. Kantengraphen können andere Hamiltonkreise haben, die nicht den Eulerkreisen entsprechen, und insbesondere ist der Kantengraph jedes hamiltonschen Graphen selbst hamiltonsch, unabhängig davon, ob der Graph ein eulerscher Graph ist.

Ein [Turniergraph](https://de.wikipedia.org/wiki/Turniergraph "Turniergraph") mit mehr als zwei [Knoten](https://de.wikipedia.org/wiki/Knoten_(Graphentheorie) "Knoten (Graphentheorie)") ist genau dann ein hamiltonscher Graph, wenn er [stark zusammenhängend](https://de.wikipedia.org/wiki/Stark_zusammenh%C3%A4ngend "Stark zusammenhängend") ist.

Die Anzahl der verschiedenen Hamiltonkreise in einem [vollständigen](https://de.wikipedia.org/wiki/Vollst%C3%A4ndiger_Graph "Vollständiger Graph") [ungerichteten Graphen]([[ungerichtete Graphen]]) mit n [Knoten](https://de.wikipedia.org/wiki/Knoten_(Graphentheorie) "Knoten (Graphentheorie)") beträgt 1 / 2 ⋅ ( n − 1 )! und in einem vollständigen [gerichteten Graphen]([[gerichtete Graphen]]) mit n Knoten ( n − 1 ) !. Dabei werden Hamiltonkreise, die bis auf ihren Startknoten gleich sind, nicht mehrfach gezählt.


