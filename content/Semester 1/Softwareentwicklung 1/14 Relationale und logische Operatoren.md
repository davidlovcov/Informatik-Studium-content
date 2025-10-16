Operatoren werden benötigt um z. B. zwischen zwei Werten zu vergleichen und eine Aussage treffen zu können. Es wird entweder *true* oder *false* ausgegeben

**Allgemeine Form:** Operand_A Operator Operand_B

## Vergleichsoperatoren Tabelle
---

| Operator | Prüft auf (true wenn)                    |
| -------- | ---------------------------------------- |
| ==       | Gleichheit (nicht zu verwechseln mit  =) |
| !=       | Ungleichheit                             |
| <        | kleiner                                  |
| >        | größer                                   |
| <=       | kleiner oder gleich                      |
| >=       | größer oder gleich                       |

Dabei kann man die ersten zwei auch auf **chars** und **booleans** anwenden. Den Rest nur auf **numerische Werte**.

```java
/* Gleichheit */
5 == 5 // True
5 == 2 // False

/* Ungleichheit */
2 != 6 // True
3 != 3 // False

/* kleiner */
8 < 13 // True
13 < 8 // False

/* größer */
4 > 2 // True
2 > 2 // False

/* kleiner oder gleich */
4 <= 4 // True
4 <= 6 // True

4 <= 3 // False

/* größer oder gleich */
9 >= 9 // True
9 >= 7 // True

9 >= 10 // False
```

<hr>

<div style="display: flex; justify-content: space-between;">

  <a href="13 Fachsprache 3">← Zurück</a>

  <!-- <a href="14 Relationale und logische Operatoren">Weiter →</a> -->

</div>