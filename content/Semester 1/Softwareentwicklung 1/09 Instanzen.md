## Allgemein
---
- **Eine Klasse ist** nur eine **abstrakte Beschreibung**
- Sie ist sozusagen **eine Vorlage** oder **Blaupause** für Objekte
- Wir müssen Objekte erstellen bzw. **Instanzen**

```java
class Flat {
	int livingSpace;
	int pricePerSqrMeter;
	int numberOfRooms;
	String address;
	boolean isKitchenIncluded;
	boolean isParkingAvailable
}
```
$$
\begin{aligned}
\downarrow
\end{aligned}
$$
![[Pasted image 20251011081052.png| 400]]

## Schlüsselwort _new_
---
- Erzeugt ein einzelnes neues Objekt (Instanz) auf Grundlage einer Klasse $\Rightarrow$ **Instanziierung**
- Stellt Speicherplatz im Arbeitsplatz bereit $\Rightarrow$ **Allokation**
- Gibt eine Referenz auf das Objekt bzw. die Speicheradresse in der das Objekt gespeichert ist

```java
new Flat();
```

- Diese Schreibweise führt die Instanziierung durch
- **Problem:** Die Adresse oder Referenz muss irgendwie abgespeichert werden
- **Lösung:** In eine Variable vom Datentypen der Klasse also _Flat_

```java
Flat myFavouriteFlat = new Flat();
```

- Wir erstellen ein Variable vom Datentypen _Flat_ um zu zeigen, dass wir dort Instanzen der Klassen _Flat_ einspeichern wollen
- Wir weisen ihm den Wert zu, welcher bei der Instanziierung herausgegeben wird, also die Speicheradresse der neuen Instanz

<hr>

<div style="display: flex; justify-content: space-between;">

  <a href="08 Datentypen">← Zurück</a>

  <a href="10 Fachsprache 2">Weiter →</a>

</div>