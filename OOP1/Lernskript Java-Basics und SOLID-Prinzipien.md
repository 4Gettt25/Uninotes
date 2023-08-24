---
date: 2023-08-19
tags:
- "OOP1"
---
# Lernskript: Java-Basics und SOLID-Prinzipien

## Teil 1: Java-Basics

### 1.1 Einführung in Java

- **Java-Grundlagen**: Was ist Java und warum wird es verwendet?
- **Installation**: Installation von Java Development Kit (JDK) und Entwicklungsumgebung (IDE).
- **Hello World**: Schreiben und Ausführen eines einfachen Java-Programms.

### 1.2 Datentypen und Variablen

- **Variablen**: Deklaration, Initialisierung und Zuweisung.
- **Datentypen**: Ganzzahlen (int, long), Gleitkommazahlen (float, double), Zeichen (char), Booleans.
- **Operatoren**: Arithmetische, Vergleichs- und logische Operatoren.

### 1.3 Kontrollstrukturen

- **Bedingungen**: `if`, `else if`, `else` Anweisungen.
- **Schleifen**: `for`, `while`, `do-while` Schleifen.
- **Schalter-Anweisung**: `switch` für mehrere Fallunterscheidungen.

### 1.4 Arrays

- **Arrays erstellen**: Deklaration, Initialisierung und Zugriff auf Array-Elemente.
- **Schleifen und Arrays**: Iteration durch Arrays mit Schleifen.

### 1.5 Funktionen (Methoden)

- **Methoden definieren und aufrufen**: Parameter, Rückgabewerte.
- **Rekursion**: Grundlagen der rekursiven Methoden.

### 1.6 Objektorientierte Programmierung (OOP)

- **Klassen und Objekte**: Definition von Klassen, Erzeugung von Objekten.
- **Eigenschaften und Methoden**: Klassenattribute und -methoden.
- **Konstruktoren**: Erstellen von Konstruktoren für Klassen.

### 1.7 Vererbung und Polymorphismus

- **Vererbung**: Erstellen von Subklassen und Ableiten von Eigenschaften und Methoden.
- **Polymorphismus**: Verwendung von Schnittstellen und abstrakten Klassen.

## Teil 2: SOLID-Prinzipien

### 2.1 SOLID-Grundlagen

- **Single Responsibility Principle (SRP)**: Die Verantwortung einer Klasse sollte auf eine einzige Aufgabe begrenzt sein.
- **Open-Closed Principle (OCP)**: Klassen sollten für Erweiterungen offen, aber für Änderungen geschlossen sein.
- **Liskov Substitution Principle (LSP)**: Subtypen müssen sich nahtlos durch ihre Basistypen ersetzen lassen.
- **Interface Segregation Principle (ISP)**: Clienten sollten nicht von Schnittstellen abhängig sein, die sie nicht nutzen.
- **Dependency Inversion Principle (DIP)**: Abhängigkeiten sollten von abstrakten Klassen und Schnittstellen statt von konkreten Klassen abgeleitet werden.

### 2.2 Anwendung der SOLID-Prinzipien

- **SRP in Java**: Aufteilung von Klassen in kleinere, spezifische Klassen.
- **OCP in Java**: Verwendung von abstrakten Klassen und Schnittstellen für Erweiterbarkeit.
- **LSP in Java**: Sicherstellung, dass Subtypen die Verträge ihrer Basistypen einhalten.
- **ISP in Java**: Aufteilung von großen Schnittstellen in kleinere, spezifischere Schnittstellen.
- **DIP in Java**: Verwendung von Abhängigkeitsinjektion für lose Kopplung.

## Teil 3: Übungen und Projekte

- **Übungen**: Praktische Übungen zur Vertiefung der Java-Basics und Anwendung der SOLID-Prinzipien.
- **Mini-Projekte**: Kleine Projekte, um das Gelernte in realen Anwendungen umzusetzen.

### 3.1 Mini-Projekt: ToDo-Liste Anwendung

#### Projektbeschreibung

In diesem Mini-Projekt werden wir eine einfache ToDo-Liste-Anwendung erstellen. Diese Anwendung ermöglicht es dem Benutzer, Aufgaben hinzuzufügen, anzuzeigen und zu markieren, wenn sie erledigt sind. Wir werden die SOLID-Prinzipien anwenden, um eine gut strukturierte und erweiterbare Anwendung zu erstellen.

#### Funktionalitäten

1. **Aufgaben hinzufügen**: Der Benutzer kann eine neue Aufgabe mit einer Beschreibung hinzufügen.
2. **Aufgaben anzeigen**: Die Liste der hinzugefügten Aufgaben wird angezeigt.
3. **Aufgaben als erledigt markieren**: Der Benutzer kann Aufgaben als erledigt markieren.

#### Klassenstruktur

- `Task`: Eine Klasse, die eine einzelne Aufgabe repräsentiert.
- `TaskList`: Eine Klasse, die eine Liste von Aufgaben verwaltet.
- `TaskManager`: Eine Klasse, die die Interaktionen mit dem Benutzer handhabt und die Anwendung startet.

#### Anwendung der SOLID-Prinzipien

- **SRP**: Jede Klasse hat eine klare Verantwortung, z.B. `Task` für die Aufgabendetails, `TaskList` für die Verwaltung der Aufgabenliste usw.
- **OCP**: Die `TaskList` ist offen für Erweiterungen, z.B. könnten Filter- oder Sortierfunktionen hinzugefügt werden.
- **LSP**: Die `TaskList` implementiert eine Schnittstelle, die von verschiedenen Implementierungen verwendet werden kann.
- **ISP**: Die Schnittstellen sind spezifisch für ihren Verwendungszweck, z.B. `Task`-Schnittstelle für Aufgabenoperationen.
- **DIP**: Abhängigkeiten werden durch Injektion von Schnittstellen gelöst, z.B. kann die `TaskList`-Implementierung durch Konstruktorinjektion bereitgestellt werden.

### 3.2 Durchführung des Mini-Projekts

1. Erstelle die erforderlichen Klassen: `Task`, `TaskList`, und `TaskManager`.
2. Implementiere die Funktionalitäten entsprechend der Projektbeschreibung.
3. Nutze die Java-Basics wie Klassen, Methoden, Bedingungen und Schleifen, um die Anwendung zu erstellen.
4. Achte darauf, die SOLID-Prinzipien bei der Gestaltung der Klassenstruktur zu berücksichtigen.
5. Teste deine Anwendung gründlich, um sicherzustellen, dass alle Funktionalitäten korrekt funktionieren.

## Teil 4: Ressourcen und Weiterführende Literatur

- **Bücher**: Empfohlene Bücher zur Vertiefung der Java-Programmierung und OOP.
- **Online-Ressourcen**: Websites und Tutorials für fortgeschrittene Java-Themen.