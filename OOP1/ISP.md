### Richtig
```java
interface Worker {
    void work();
}

interface Eater {
    void eat();
}

class Robot implements Worker {
    @Override
    public void work() {
        // Implementierung der Arbeit eines Roboters
    }
}
```

### Falsch
```java
interface Worker {
    void work();
    void eat();
}

class Robot implements Worker {
    @Override
    public void work() {
        // Implementierung der Arbeit eines Roboters
    }

    // Ein Roboter kann nicht essen, daher ist die Methode irreführend
    @Override
    public void eat() {
    }
}
```
