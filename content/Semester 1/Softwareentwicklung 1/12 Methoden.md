## Definition
---
- Methoden sind da, um Operationen oder Tätigkeiten durchzuführen
- Zum Beispiel _autoFahren()_ oder _rennen()_
- Methoden werden üblich in der Klasse definiert
- Der Returntyp muss immer angegeben werden
- Will man nichts zurückgeben, so schreibt man einfach _void_ als Returntyp

## Methodenaufruf
---
Gehen wir davon aus, dass wir eine Klasse Auto haben und diese hat die Methoden oder Tätigkeiten _fahren_, _blinken_, _blinkerAusschalten_ und _fahrtdauerAusgeben_ 

```java
class Auto {
    int fahrtdauer;
    String blinkrichtung;
    boolean isBlinkerAn;

    // Aufbau: Rückgabewert Methodenname (Parameter) {Methodenrumpf}
    void fahren() {
        /* 
            Hier wäre dann bspw. Logik zum Fahren und sagen wir mal, 
            dass wir jede Sekunde die fahrtdauer um 1 erhöhen
         */
    }

    void blinken(String blinkrichtung) {
        this.isBlinkerAn = true;
        this.blinkrichtung = blinkrichtung;
    }

    void blinkerAusschalten() {
        this.isBlinkerAn = false;
    }

    int fahrtdauerAusgeben() {
        return this.fahrtdauer;
    }
}
```
So können wir diese Methoden nutzen:
```java
class EineKlasse {
    public static void main(String args[]) {
        // Wir erstellen zuerst ein neues Auto Objekt
        Auto einAuto = new Auto();
        
        // Danach rufen wir die Methoden auf
        einAuto.fahren();

        // Wir müssen auch beachten, ob wir Parameterwerte übergeben müssen
        einAuto.blinken("Rechts");

        einAuto.blinkerAusschalten()

        // Die Methode gibt ja die Fahrtdauer zurück. Wir müssen sie irgendwo abspeichern. Dafür erstellen wir die Variable fahrtdauer
        int fahrtdauer = einAuto.fahrtdauerAusgeben;
    }
}
```

Wir könnten theoretisch auch auf die Fahrtdauer mit
```java
int fahrtdauer = einAuto.fahrtdauer;
```
zugreifen. Jedoch wird es empfohlen später setter und getter zu nutzen und die Variablen in einer Klasse privat zu halten.

<hr>

<div style="display: flex; justify-content: space-between;">

  <a href="11 Konstruktoren">← Zurück</a>

  <a href="13 Fachsprache 3">Weiter →</a>

</div>