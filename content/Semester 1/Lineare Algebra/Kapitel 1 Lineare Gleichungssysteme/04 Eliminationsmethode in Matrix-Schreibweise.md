- Wir können die Schritte bei der Eliminationsmethode mit dem Gauß-Algorithmus in eine Matrix $E$ speichern
- Das gibt den Vorteil, dass wir mit einer einzigen Multiplikation die Elimination durchführen

## Ermittlung von der Matrix $E$ anhand eines Beispiels
---
### Schritt 1
---
$$
\left[
\begin{array}{ccc|c}
1 & 2 & 1 & 2 \\
3 & 8 & 1 & 12 \\
0 & 4 & 1 & 2
\end{array}
\right] 

\longrightarrow

\left[
\begin{array}{ccc|c}
1 & 2 & 1 & 2 \\
0 & 2 & -2 & 6 \\
0 & 4 & 1 & 2
\end{array}
\right]
$$
- Wir multiplizieren die 1. Zeile mit $-3$ und addieren das Produkt davon auf die 2. Zeile

$$
\left[
\begin{array}{ccc}
1 & 0 & 0 \\
-3 & 1 & 0 \\
0 & 0 & 1 
\end{array}
\right] \cdot

\left[
\begin{array}{ccc|c}
1 & 2 & 1 & 2 \\
3 & 8 & 1 & 12 \\
0 & 4 & 1 & 2
\end{array}
\right] 

\longrightarrow

\left[
\begin{array}{ccc|c}
1 & 2 & 1 & 2 \\
0 & 2 & -2 & 6 \\
0 & 4 & 1 & 2
\end{array}
\right]
$$
- Die erste Matrix $E$ nennen wir $E_{2,1}$, da wir aus der 2. Zeile das 1. Element eliminieren
### Schritt 2
---
$$
\left[
\begin{array}{ccc|c}
1 & 2 & 1 & 2 \\
0 & 2 & -2 & 6 \\
0 & 4 & 1 & 2
\end{array}
\right]

\longrightarrow

\left[
\begin{array}{ccc|c}
1 & 2 & 1 & 2 \\
0 & 2 & -2 & 6 \\
0 & 0 & 5 & -10
\end{array}
\right]
$$
- Wir multiplizieren die 2. Zeile mit $-2$ und addieren das Produkt davon auf die 3. Zeile

$$
\left[
\begin{array}{ccc}
1 & 0 & 0 \\
0 & 1 & 0 \\
0 & -2 & 1
\end{array}
\right] \cdot

\left[
\begin{array}{ccc|c}
1 & 2 & 1 & 2 \\
0 & 2 & -2 & 6 \\
0 & 4 & 1 & 2
\end{array}
\right]

\longrightarrow

\left[
\begin{array}{ccc|c}
1 & 2 & 1 & 2 \\
0 & 2 & -2 & 6 \\
0 & 0 & 5 & -10
\end{array}
\right]
$$

- Die zweite Matrix $E$ nenne wir $E_{3,2}$, da wir aus der 3. Zeile das 2. Element eliminieren

### Schritt 3
---
- Nun müssen wir die beiden Matrizen $E$ miteinander multiplizieren und dessen Produkt mit der Matrix $A$ multiplizieren
$$
\begin{aligned}
\Rightarrow E_{3,2} \cdot (E_{2,1} \cdot A) = (E_{3,2} \cdot E_{2,1}) \cdot A &= 

\left(
\left[
\begin{array}{ccc}
1 & 0 & 0 \\
0 & 1 & 0 \\
0 & -2 & 1
\end{array}
\right] \cdot

\left[
\begin{array}{ccc}
1 & 0 & 0 \\
-3 & 1 & 0 \\
0 & 0 & 1 
\end{array}
\right]

\right) \cdot

\left[
\begin{array}{ccc|c}
1 & 2 & 1 & 2 \\
3 & 8 & 1 & 12 \\
0 & 4 & 1 & 2
\end{array}
\right] \\\\\\&=

\begin{bmatrix}
1 & 0 & 0 \\
-3 & 1 & 0 \\
6 & -2 & 1
\end{bmatrix} \cdot

\left[
\begin{array}{ccc|c}
1 & 2 & 1 & 2 \\
3 & 8 & 1 & 12 \\
0 & 4 & 1 & 2
\end{array}
\right] =

\left[
\begin{array}{ccc|c}
1 & 2 & 1 & 2 \\
0 & 2 & -2 & 6 \\
0 & 0 & 5 & -10
\end{array}
\right] = U\\\\\\

\Rightarrow E = E_{3,2} \cdot E_{2,1} &= 

\begin{bmatrix}
1 & 0 & 0 \\
-3 & 1 & 0 \\
6 & -2 & 1
\end{bmatrix}

\end{aligned} 
$$

## Spaltentausch
---
- Mit der Matrix $E$ können wir auch einen Spaltentausch durchführen

$$
\begin{bmatrix}
\uparrow & \uparrow & \uparrow \\
\vec{a_1} & \vec{a_2} & \vec{a_3} \\
\downarrow & \downarrow & \downarrow
\end{bmatrix} \cdot

\begin{bmatrix}
0 & 1 & 0 \\
1 & 0 & 0 \\
0 & 0 & 1
\end{bmatrix} =

\begin{bmatrix}
\uparrow & \uparrow & \uparrow \\
\vec{a_2} & \vec{a_1} & \vec{a_3} \\
\downarrow & \downarrow & \downarrow
\end{bmatrix} \cdot
$$
- In der 1. Zeile der Matrix $E$  sagen wir, dass wir die 1. Spalte mit 0 multiplizieren und danach die 2. Spalte dazu addieren
- In der 2. Zeile der Matrix $E$ sagen wir, dass wir die 2. Spalte mit 0 multiplizieren und danach die 1. Spalte dazu addieren

### Beispiel
---
$$
\begin{aligned}
\begin{bmatrix}
5 & 3 & 1 \\
9 & 1 & 3 \\
5 & 5 & 1 \\
\end{bmatrix} \cdot

\begin{bmatrix}
0 & 1 & 0 \\
1 & 0 & 0 \\
0 & 0 & 1
\end{bmatrix} &=

\begin{bmatrix}
0 \cdot 5 + 3 \cdot 1 + 1 \cdot 0 && 5 \cdot 1 + 3 \cdot 0 + 1 \cdot 0 && 5 \cdot 0 + 3 \cdot 0 + 1 \cdot 1 \\

9 \cdot 0 + 1 \cdot 1 + 3 \cdot 0 && 9 \cdot 1 + 1 \cdot 0 + 3 \cdot 0 && 9 \cdot 0 + 1 \cdot 0 + 3 \cdot 1 \\

5 \cdot 0 + 5 \cdot 1 + 1 \cdot 0 && 5 \cdot 1 + 5 \cdot 0 + 1 \cdot 0 && 5 \cdot 0 + 5 \cdot 0 + 1 \cdot 1
\end{bmatrix} \\\\ &=
\begin{bmatrix}
3 & 5 & 1 \\
1 & 9 & 3 \\
5 & 5 & 1
\end{bmatrix}
\end{aligned}
$$

<hr>

<div style="display: flex; justify-content: space-between;">

  <a href="03 Matrizenmultiplikation">← Zurück</a>

  <a href="05 Inverse Matrix">Weiter →</a>

</div>