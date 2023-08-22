### Richtig
```java
class Bird {
    void fly() {
        // Flug-Logik
    }
}

class Sparrow extends Bird {
    @Override
    void fly() {
        // Implementierung für den Flug eines Sperlings
    }
}
```

### Falsch
```java
class Bird {
    void fly() {
        // Flug-Logik
    }
}

class Penguin extends Bird {
    @Override
    void fly() {
        // Ein Pinguin kann nicht fliegen, daher ist die Methode                  irreführend
    }
}
```
