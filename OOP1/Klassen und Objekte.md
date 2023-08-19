---
date: 2023-08-19
tags:
- "OOP1"
---
## Eigenschaften
- Klassen sind Baupläne für Objekte. Sie definieren Attribute und Methoden.
- Objekte sind Instanzen von Klassen.
- Beispiel für Klassendefinition:
	```java
	public class Person {
    String name;
    int age;

    void sayHello() {
        System.out.println("Hallo, mein Name ist " + name);
		}
	}
```
 - Objekterstellung und -verwendung:
	 ```java
	 Person person1 = new Person();
	person1.name = "Max";
	person1.age = 30;
	person1.sayHello();
 ```
 