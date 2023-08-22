### Richtig
```java
class Customer {
    private String name;
    private String email;

    public Customer(String name, String email) {
        this.name = name;
        this.email = email;
    }

    public void sendInvoice(Invoice invoice) {
        // Logik zum Senden der Rechnung per E-Mail
    }
}
```

### Falsch
```java
class Customer {
    private String name;
    private String email;

    public Customer(String name, String email) {
        this.name = name;
        this.email = email;
    }

    public void sendInvoice(Invoice invoice) {
        // Hier sollte keine E-Mail-Logik vorhanden sein
    }

    public void saveToDatabase() {
        // Hier sollte keine Datenbank-Logik vorhanden sein
    }
}
```
