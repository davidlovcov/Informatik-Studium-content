## Allgemein
---
	Eine *Deklaration* führt eine Entität im Programm ein. Die Deklaration beinhalten einen Bezeichner und Datentypen. Später kann mit dem Bezeichner auf die Deklaration verwiesen werden. Man nennt es auch *referenzieren*

- Entität = Attribut
- Es gibt verschiedene Arten von Entitäten
- Alles muss deklariert sein

## Einfache Datentypen
---
- Computer speichern Daten in digitaler Form
- Diese werden in Bits oder Bytes zusammengefasst
	- Kleinstmögliche Größe 1 Bit
	- 1 Byte = $2^8 \text{ Bits oder 256 Bits}$
- Man kann also pro Byte 256 verschiedene Werte speichern
- Bei der Deklaration gibt der Datentyp an, wie viel Speicher wir benötigen

### Der Datentyp *int*
---
- Größe: 4 Bytes = $2^{32} \text{ Bits}$
- Gibt an, dass es sich um Ganzzahlen handelt
- $–2147483648 \text{ bis } 2147483647$ können dargestellt werden also ($-2^{31} \text{ bis } 2^{31} - 1$) *-1 wegen der Null*
- Attributdeklaration: 
````java
int livingSpace;
````

- Das ***;*** Semikolon ist wichtig um zu sagen, dass die Deklaration abgeschlossen ist

	Ein *Literal* ist die Repräsentation eines konkreten Wertes von einem Datentyp im Quellcode.

- Ganzzahlen dürfen als Dezimalzahlen geschrieben werden
- Ganzzahlen-Literale können für die Initialisierung verwendet werden
- Bedeutet man will dem Attribut einen Wert zuweisen
- Erst wenn das Programm läuft wird es zugewiesen
```java
int numbersOfRooms = 1;
```

### Der Datentyp *boolean*
---
- Oft benötigen wir Wahrheitswerte wie: hat ein Auto oder ist krank
- 1 Bit groß
- Kann entweder wahr oder falsch sein (true oder false | 1 oder 0)
- Oft beginnt ein boolean-Attribut mit *is* im Bezeichner um eine Aussagekraft zu haben
```java
// Attributendeklaration
boolean isKitchenIncluded;
boolean isCarParkIncluded;
```
Mit Initialisierung:
```java
// Attributendeklaration mit Initialisierung
boolean isKitchenIncluded = true;
boolean isCarParkIncluded = false;
```

### Der Datentyp *char*
---
- Speicherung von einzelnen Zeichen
- 2 Bytes groß
```java
char c = 'a';
```

**Escape-Sequenzen/Fluchtsymbole**
- Es gibt Symbole die nicht als char-Literal dargestellt werden können
- Dafür braucht man ein Fluchtsymbol die als Ersatzdarstellung dient

| Zeichen | Bedeutung                   |
| ------- | --------------------------- |
| \n      | Zeilenschaltung (Newline)   |
| \t      | Horizontaler Tabulator      |
| \\"     | Doppeltes Anführungszeichen |
| \\'     | Einfaches Anführungszeichen |
| \\\     | Backslash                   |
- Diese Zeichen zählen selbst als ein Zeichen obwohl sie mit zweien geschrieben werden
```java
char a = 'a';
char singlequote = '\'';
char newline = '\n'
```

### Der Datentyp *String*
---
- Eine Kette aus Zeichen (Zeichenkette)
- Wird mit **""** statt **''** deklariert
```java
String name; // Deklaration
String surname = "Lovcov" // Deklaration mit Initialisierung
```

<hr>

<div style="display: flex; justify-content: space-between;">

  <a href="07 Fachsprache 1">← Zurück</a>

  <a href="09 Instanzen">Weiter →</a>

</div>