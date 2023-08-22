---
date: 2023-08-19
tags:
- "OOP1"
---
SOLID ist eine Abkürzung für fünf Designprinzipien, die dazu beitragen, robuste, wartbare und erweiterbare Software zu entwickeln.

1. **S - Single Responsibility Principle ([[SRP]]):** Eine Klasse sollte nur einen Grund haben, sich zu ändern. Sie sollte nur eine Verantwortung haben.
 
2. **O - Open/Closed Principle ([[OCP]]):** Softwareentitäten (Klassen, Module, etc.) sollten offen für Erweiterungen, aber geschlossen für Modifikationen sein. Neue Funktionen sollten durch Erweiterung hinzugefügt werden, ohne den bestehenden Code zu ändern.
  
3. **L - Liskov Substitution Principle ([[LSP]]):** Objekte einer abgeleiteten Klasse sollten ohne Änderung an der erwarteten Funktionalität anstelle von Objekten der Basis (Eltern-) Klasse verwendet werden können.

4. **I - Interface Segregation Principle ([[ISP]]):** Klienten sollten nicht von Interfaces abhängig sein, die sie nicht verwenden. Ein Interface sollte nur die Methoden enthalten, die für seinen spezifischen Verwendungszweck benötigt werden.

5. **D - Dependency Inversion Principle ([[DIP]]):** High-level-Module sollten nicht von Low-level-Modulen abhängen. Beide sollten von abstrakten Abhängigkeiten abhängen. Abstraktionen sollten nicht von Details abhängen, sondern Details von Abstraktionen.