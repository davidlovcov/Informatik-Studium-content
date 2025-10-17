
## Darstellung einer Funktion in Normalform
---
Es sei eine boolesche Funktion $f(x_1, ..., x_n)$ gegeben. Diese können wir durch eine Wahrheitstabelle darstellen

### Beispiel
---

| $x_3$ | $x_2$ | $x_1$ | $y$ |
| ----- | ----- | ----- | --- |
| 0     | 0     | 0     | 0   |
| 0     | 0     | 1     | 0   |
| 0     | 1     | 0     | 1   |
| 0     | 1     | 1     | 1   |
| 1     | 0     | 0     | 0   |
| 1     | 0     | 1     | 1   |
| 1     | 1     | 0     | 1   |
| 1     | 1     | 1     | 0   |

## Darstellung einer Funktion in Disjunktiver Normalform
---
- Es sei die vorherige boolesche Funktion gegeben 
- Für die Darstellung in Disjunktiver Normalform müssen wir alle Einsmengen der Funktion als Minterme darstellen und mit einem OR verknüpfen

### Definition von Minterm
---
Ein Minterm wird folgendermaßen definiert:
$$
\hat{x_1} \wedge \dots \wedge \hat{x_n} \qquad \hat{x_i} \{x_i, \overline{x_i} \}
$$
$x_i$ hat nur die Werte $x_i$ und $\overline{x_i}$ (1 oder 0)
### Beispiel
---
Zuerst stellen wir die 4 Minterme auf

| $x_3$ | $x_2$ | $x_1$ | $y$ |                                                   |
| ----- | ----- | ----- | --- | ------------------------------------------------- |
| 0     | 0     | 0     | 0   |                                                   |
| 0     | 0     | 1     | 0   |                                                   |
| 0     | 1     | 0     | 1   | $\overline{x_3} \wedge x_2 \wedge \overline{x_1}$ |
| 0     | 1     | 1     | 1   | $\overline{x_3} \wedge x_2 \wedge x_1$            |
| 1     | 0     | 0     | 0   |                                                   |
| 1     | 0     | 1     | 1   | $x_3 \wedge \overline{x_2} \wedge x_1$            |
| 1     | 1     | 0     | 1   | $x_3 \wedge x_2 \wedge \overline{x_1}$            |
| 1     | 1     | 1     | 0   |                                                   |
Dann müssen wir die Minterme miteinander verknüpfen

DNF:
$y = (\overline{x_3} \wedge x_2 \wedge \overline{x_1}) \vee (\overline{x_3} \wedge x_2 \wedge x_1) \vee (x_3 \wedge \overline{x_2} \wedge x_1) \vee (x_3 \wedge x_2 \wedge \overline{x_1})$

## Darstellung einer Funktion in Konjunktiver Normalform
---
- Es sei die vorherige boolesche Funktion gegeben 
- Für die Darstellung in Konjunktiver Normalform müssen wir alle Nullermengen der Funktion als Maxterme darstellen und mit einem AND verknüpfen

### Definition von Maxterm
---
Ein Maxterm wird folgendermaßen definiert:
$$
\hat{x_1} \vee \dots \vee \hat{x_n} \qquad \hat{x_i} \{x_i, \overline{x_i} \}
$$
### Beispiel
---
Zuerst stellen wir die 4 Maxterme auf

| $x_3$ | $x_2$ | $x_1$ | $y$ |                                                          |
| ----- | ----- | ----- | --- | -------------------------------------------------------- |
| 0     | 0     | 0     | 0   | $\overline{x_3} \vee \overline{x_2} \vee \overline{x_1}$ |
| 0     | 0     | 1     | 0   | $\overline{x_3} \vee \overline{x_2} \vee x_1$            |
| 0     | 1     | 0     | 1   |                                                          |
| 0     | 1     | 1     | 1   |                                                          |
| 1     | 0     | 0     | 0   | $x_3 \vee \overline{x_2} \vee \overline{x_1}$            |
| 1     | 0     | 1     | 1   |                                                          |
| 1     | 1     | 0     | 1   |                                                          |
| 1     | 1     | 1     | 0   | $x_3 \vee x_2 \vee x_1$                                  |
Anschließend verknüpfen wir die Maxterme miteinander

KNF:
$y = (\overline{x_3} \vee \overline{x_2} \vee \overline{x_1}) \wedge (\overline{x_3} \vee \overline{x_2} \vee x_1) \wedge (x_3 \vee \overline{x_2} \vee \overline{x_1}) \wedge (x_3 \vee x_2 \vee x_1)$

<div style="display: flex; justify-content: space-between;">

  <a href="index">← Zurück</a>

  <a href="02 Zweistufige Schaltungsentwürfe">Weiter →</a>

</div>