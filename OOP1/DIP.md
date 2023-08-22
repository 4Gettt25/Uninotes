### Richtig
```java
interface Switchable {
    void turnOn();
}

class LightBulb implements Switchable {
    @Override
    public void turnOn() {
        // Logik zum Einschalten der Glühbirne
    }
}

class Switch {
    private Switchable device;

    public void connect(Switchable device) {
        this.device = device;
    }

    public void operate() {
        device.turnOn();
    }
}
```

### Falsch
```java
class LightBulb {
    public void turnOn() {
        // Logik zum Einschalten der Glühbirne
    }
}

class Switch {
    private LightBulb device;

    public void connect(LightBulb device) {
        this.device = device;
    }

    // Direkte Abhängigkeit von LightBulb, nicht abstrakt genug
    public void operate() {
        device.turnOn();
    }
}
```


