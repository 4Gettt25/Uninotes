---
date: 2023-08-19
tags:
- "OOP1"
---
## Eigenschaften
Java ermöglicht es, Code in modularen Einheiten zu organisieren, um die Wartbarkeit und Wiederverwendbarkeit zu verbessern. Ein Modul kann eine Klasse, eine Schnittstelle oder sogar ein Paket sein. Hier sind einige Schlüsselkonzepte:

1. **Pakete (Packages):**
    - Pakete organisieren Klassen und Schnittstellen in logische Gruppen.
    - Sie verhindern Namenskonflikte, indem sie Namensräume schaffen.
    - Paketdeklaration: `package com.example.myapp;`
2. **Sichtbarkeit (Access Modifiers):**
    - `public`: Öffentlich sichtbar, von überall zugänglich.
    - `protected`: Zugriff nur innerhalb derselben Klasse und derselben Paket-Hierarchie.
    - `default` (kein Modifier): Zugriff nur innerhalb des Pakets.
    - `private`: Zugriff nur innerhalb derselben Klasse.
3. **Klassenpfad (Classpath):**
    - Der Klassenpfad gibt an, wo Java nach Klassen sucht, wenn sie benötigt werden.
    - Dies ermöglicht die Verwendung von Klassen aus anderen Paketen oder Bibliotheken.
4. **Import von Klassen:**
    - Mit dem `import`-Statement können Klassen aus anderen Paketen verwendet werden.
    - `import com.example.myapp.MyClass;`
5. **JAR-Dateien (Java Archive):**
    - JAR-Dateien sind Container für Klassen, Ressourcen und Metadaten.
    - Sie ermöglichen die Verteilung von Bibliotheken und Anwendungen in einem einzigen Paket.
6. **Modulsystem (Java 9+):**
    - Ab Java 9 können Anwendungen in Module unterteilt werden, um Abhängigkeiten besser zu verwalten und die Sichtbarkeit zu kontrollieren.
    - Das `module-info.java`-File definiert, welche Pakete sichtbar sind und welche Abhängigkeiten bestehen.

Hier ist ein Beispiel für die Verwendung von Paketen und Importen:

Angenommen, du hast eine Klasse `Person` im Paket `com.example.model`:
```java
 package com.example.model;

	public class Person {
    // ... Attribut und Methoden hier ...
	}
```

Um diese Klasse in einer anderen Klasse oder einem anderen Paket zu verwenden:
```java
import com.example.model.Person;

	public class Main {
    public static void main(String[] args) {
        Person person = new Person();
        // ... Weitere Verarbeitung der Person ...
    }
}
```

Dieses Beispiel zeigt, wie Java die Modularität durch Pakete und Importe unterstützt. Dies hilft, den Code organisiert und wartbar zu halten.
