## Allgemein
Wir können durch benachbarte Einträge Minimierungen durchführen, was zu einer Optimierung des Schaltnetzes führen kann. Dies funktioniert nur wenn sie sich durch einen Wert einzigen unterscheiden

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
### Benachbarter Eintrag mit nur einer Unterscheidung
$(\overline{x_3} \wedge x_2 \wedge \overline{x_1}) \vee (\overline{x_3} \wedge x_2 \wedge x_1) = (\overline{x_3} \wedge x_2) \wedge \cancel{(\overline{x_1} \vee x_1)} = \overline{x_3} \wedge x_2$ 

## Karnaugh-Veitch-Diagramm (KV-Diagramm)
---
Mit dem KV-Diagramm können wir die Minimierung einfacher gestalten

### 1. KV-Diagramm aufstellen
---
Man sollte die Elemente so aufstellen, dass sie ich jeweils gegenseitig nur um 1 Bit unterscheiden.

![[1.png | 500]]

### 2. Zeilennummern der Funktion aufschreiben
---
- Wir sehen, dass für die erste Reihe der Funktion $y_0$  $\overline{x_3}, \overline{x_2}, \overline{x_1}$ gilt
- Also müssen wir es auch dort eintragen, wo sich alle drei schneiden
	- Das wäre oben-links

![[2.png | 500]]

- Die nächste Zeile $y_1$ hat die Elemente $\overline{x_3}, \overline{x_2}, x_1$
- Also müssen wir die Zeilennummer $1$ in der 1. Zeile und 2. Spalte eintragen, da sich dort diese Elemente schneiden

![[3.png | 500]]

Dies führen wir fort, bis wir alle Zeilennummern eingetragen haben

![[4.png | 500]]

### 3. Wertigkeiten der Funktion eintragen
---
- Wir schauen dafür in die Tabelle und schauen jetzt erstmal in welchen Zeilen der Funktion sich die 0en befinden
	$\Rightarrow$ 0. Zeile, 1. Zeile, 4. Zeile und 7. Zeile
- Nun können wir die Nullen in die jeweiligen Nummern eintragen

![[5.png | 500]]

- Das selbe machen wir für die 1en
	$\Rightarrow$ 2. Zeile, 3. Zeile, 5. Zeile und 6. Zeile

![[6.png | 500]]

### 4. Nachbarn markieren
---
Nun müssen wir die aneinander gereihten Nachbarn markieren
Dabei gilt:
- man markiert in $2^n$ Schritten. In diesem Beispiel können wir nur 2, 4 und 8 Nachbarn markieren
- man darf auch die Ecken miteinander verbinden
- man darf über das KV-Diagramm hinaus markieren. Man stelle sich vor, es sei eine Kugel

In unserem Fall können wir 2 Nachbarn markieren
1. 2 und 3
2. 2 und 6
![[7.png | 500]]

### 5. Elemente aufschreiben und Minterm bilden
---
1. Für die 2 und 3 sehen wir, dass sie durch $x_2$ und $\overline{x_3}$ dargestellt werden kann
2. 2 und 6 kann durch $x_2$ und $x_3$ dargestellt werden
3. die 5 ist alleine und wird durch $x_1, \overline{x_2}$ und $x_3$ dargestellt

$\Rightarrow y = (x_2 \wedge \overline{x_3}) \vee (x_2 \wedge x_3) \vee (x_1 \wedge \overline{x_2} \wedge x_3)$

<div style="display: flex; justify-content: space-between;">

  <a href="03 Anwendung von Bubble Pushing">← Zurück</a>

  <!-- <a href="04 Minimierung durch benachbarte Einträge ">Weiter →</a> -->

</div>