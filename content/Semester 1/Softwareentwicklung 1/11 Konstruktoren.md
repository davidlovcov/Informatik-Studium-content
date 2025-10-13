## Definition
---
- Konstruktore werden in einer Klasse definiert und haben den selben Namen, wie die Klasse
- Sie werden nach dem erstellen eines Objektes ausgeführt
- Haben keinen Returntyp
- Hat eine Klasse einen Konstruktor mit Parametern, so müssen bei der Deklaration, in der Parameterklammer, die benötigten Werte eingegeben werden

## Beispiel
---
**Definition in der Klasse**
```java
class Schiff {
    int geschwindigkeit;
    int laenge;

    Schiff(int geschwindigkeit, int laenge) {
        this.geschwindigkeit = geschwindigkeit;
        this.laenge = laenge;
    }
}
```

- Wir sehen, dass wir keinen Returntypen haben und die Werte _geschwindigkeit_ und _laenge_ bei der Initialiseren erhalten wollen

## _this_ Notation
---
- Das _this_ gibt an, dass wir auf die Variablen der Klasse oder Instanz zugreifen wollen

## Initialisierung der Klasse
---
```java
class Beispiel {
    // Der Einstieg eines Java Programmes
    public static void main(String args[]) {
        Schiff langesSchiff = new Schiff(5, 50);
    }
}
```

- Wir erstellen eine Instanz der Klasse Schiff mit den Werten $5$ für die Geschwindigkeit und $50$ für die Länge