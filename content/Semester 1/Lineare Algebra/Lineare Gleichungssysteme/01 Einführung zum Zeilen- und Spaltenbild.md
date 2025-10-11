## Zeilenbild
---
**Gegeben:**
- $n$ lineare Gleichungen
- $n$ Unbekannte in den Gleichungen
	- mit $n \in \mathbb{N}$

**Beispiel: (Lineares Gleichungssystem mit $n = 2$**
$$
\begin{aligned}
2x + y &= 0 \qquad \text{1. Zeile / Gleichung} \\
-x + 2y &= 5 \qquad \text{2. Zeile / Gleichung}
\end{aligned}
$$
**Matrixform:**
$$
\begin{bmatrix}
2 & 1 \\
-1 & 2
\end{bmatrix}

\cdot

\begin{bmatrix}
x \\
y
\end{bmatrix}

=

\begin{bmatrix}
0 \\
5
\end{bmatrix}

\Rightarrow

A \cdot \vec{x} = \vec{b}
$$


- erster Teil = $A$
- zweiter Teil = $\vec{x}$
- dritter Teil = $\vec{b}$

$$
\begin{aligned}
&\text{1. Zeile: } &2x + y = 0 &\Rightarrow y = -2x\\
&\text{2. Zeile: } &-x + 2y = 5 &\Rightarrow y = \frac{1}{2}x + \frac{5}{2}
\end{aligned}
$$
**Graphische Darstellung:**
![[Bildschirmfoto 2025-10-08 um 22.53.35.png | 600]]

$\to x = -1 \text{ und } y = 2$ erfüllen beide lineare Gleichungen

## Spaltenbild
---
$$
x \cdot
\begin{bmatrix}
2 \\
-1
\end{bmatrix}
+ y \cdot
\begin{bmatrix}
1 \\
2
\end{bmatrix}
=
\begin{bmatrix}
0 \\
5
\end{bmatrix}
$$
- Man sucht die richtige Zahlen für $x$ und $y$, sodass die die Summe von $A$ und $\vec{x}$ die Spalte $\vec{b}$ ergibt
- Gelöst wird das ganze mit $x = -1$ und $y = 2$

$$
-1 \cdot
\begin{bmatrix}
2 \\
-1
\end{bmatrix}
+
2 \cdot
\begin{bmatrix}
1 \\
2
\end{bmatrix}
=
\begin{bmatrix}
-2 \\
1
\end{bmatrix}
+
\begin{bmatrix}
2 \\
4
\end{bmatrix}
=
\begin{bmatrix}
0 \\
5
\end{bmatrix}
$$

> [!Definition 1.1] Linearkombination
> Wenn $n$ Spalten gegeben sind also $\vec{a}_1, \dots, \vec{a}_n$ so nennen wir diese Verknüpfung
> $$
> \begin{aligned}
> \lambda_1 \cdot \vec{a}_1 + \dots + \lambda_n \cdot \vec{a}_n
> \end{aligned}
> $$
>  mit Zahlen $\lambda_1, \dots, \lambda_n \in \mathbb{R}$ eine Linearkombination dieser Spalten

**Graphische Darstellung**
![[Bildschirmfoto 2025-10-08 um 23.51.03.png | 600]]
$\Rightarrow$ Man sieht, dass wir -1 mal x verwenden (blau) und 2 mal y (grün) und kommen damit auf die Spalte $\vec{b}$

## Lineare Gleichungssysteme mit $n = 3$
---
**Bsp.:**
$$
\begin{aligned}
2x - y &= 0 &\text{1. Zeile / Gleichung} \\
-x + 2y - z &= -1 &\text{2. Zeile / Gleichung} \\
{}-3y + 4 z&= 0 &\text{3. Zeile / Gleichung}
\end{aligned}
$$
**Matrixform:**
$$
\begin{bmatrix}
2 & 1 & 0 \\
-1 & 2 & -3 \\
0 & -1 & 4
\end{bmatrix}
\cdot
\begin{bmatrix}
x \\
y \\
z 
\end{bmatrix}
=
\begin{bmatrix}
0 \\
-1 \\
0 
\end{bmatrix}
$$

### Als Zeilenbild
---
$$
\begin{aligned}
&\text{1. Zeile: }\quad 2x - y &= 0 &\Rightarrow y = -2x\\
&\text{2. Zeile: }\quad -x + 2y - 3z &= -1 &\Rightarrow y = \frac{1}{2}x + \frac{3}{2}z - \frac{1}{2}\\
&\text{3. Zeile: }\quad  -3y + 4z &= 0 &\Rightarrow y = \frac{3}{4}z
\end{aligned}
$$

$\Rightarrow$ 1. Zeile bildet eine Ebene, da man irgendeinen Wert für $z$ einsetzen kann
$\Rightarrow$ 3. Zeile bildet eine Ebene, da man irgendeinen Wert für $x$ einsetzen kann

**Graphische Darstellung:**
![[Bildschirmfoto 2025-10-09 um 00.49.30.png | 600]]
$\Rightarrow$ Nun nimmt man die Gerade an der sich die 2 Ebenen schneiden und zeichnet die 2. Ebene ein um den genauen Schnittpunkt zu erkennen
![[Pasted image 20251009071607.png | 600]]
$\Rightarrow$ Man sieht, dass sich der Schnittpunkt bei (0, 0, 0) befindet
$\Rightarrow$ Auch erkennt man, dass es bei höheren $n$ immer unübersichtlicher wird. Ab $n = 4,\ 5,\ 6,\ \dots$  nicht mehr vorstellbar

### Als Spaltenbild
---
$$
x \cdot
\begin{bmatrix}
2 \\
-1 \\
0
\end{bmatrix}
+
y \cdot
\begin{bmatrix}
-1 \\
2 \\
-3
\end{bmatrix}
+ z \cdot
\begin{bmatrix}
0 \\
-1 \\
4
\end{bmatrix}
=
\begin{bmatrix}
0 \\
-1 \\
4
\end{bmatrix}
$$

$\Rightarrow$ Wir müssen nun für $x$, $y$ und $z$ so die Werte einsetzen, damit die Summe der Spalten $A$ die Spalte $\vec{b}$ ergibt
$\Rightarrow$ Beim genauen hinschauen erkennen wir, dass $z$ den selben Wert wie die Spalte $\vec{b}$ besitzt
	$\Rightarrow$ Damit können wir sagen, dass wir für $x$ und $y$ 0 einsetzen können und für $z = 1$  damit das Gleichungssystem gelöst ist
$$
0 \cdot
\begin{bmatrix}
2 \\
-1 \\
0
\end{bmatrix}
+
0 \cdot
\begin{bmatrix}
-1 \\
2 \\
-3
\end{bmatrix}
+ 1 \cdot
\begin{bmatrix}
0 \\
-1 \\
4
\end{bmatrix}
=
\begin{bmatrix}
0 \\
0 \\
0
\end{bmatrix}
+
\begin{bmatrix}
0 \\
0 \\
0
\end{bmatrix}
+
\begin{bmatrix}
0 \\
-1 \\
4
\end{bmatrix}
=
\begin{bmatrix}
0 \\
-1 \\
4
\end{bmatrix}
$$
**Graphische Darstellung:**
![[Pasted image 20251009073614.png | 600]]
Anmerkung: (Man sieht $\vec{b}$  nicht, da er in $\vec{x3}$ ist, Punkt D)

- Wenn wir eine neue $\vec{b}$ Spalte haben, müssen wir die Linearkombination von neu lösen

**Bsp.: (mit den alten $A$ Spalten)**
$$
\vec{b}_{neu} = 
\begin{bmatrix}
1 \\
1 \\
-3
\end{bmatrix}
$$
$$
x \cdot
\begin{bmatrix}
2 \\
-1 \\
0
\end{bmatrix}
+
y \cdot
\begin{bmatrix}
-1 \\
2 \\
-3
\end{bmatrix}
+ z \cdot
\begin{bmatrix}
0 \\
-1 \\
4
\end{bmatrix}
=
\begin{bmatrix}
1 \\
1 \\
-3
\end{bmatrix}
$$

$\Rightarrow$ Beim genauerem hinsehen erkennen wir, dass wir für $x = 1$ und $y = 1$ einsetzen müssen damit wir auf $\vec{b}$ kommen. Für $z = 0$ 

$$
1 \cdot
\begin{bmatrix}
2 \\
-1 \\
0
\end{bmatrix}
+
1 \cdot
\begin{bmatrix}
-1 \\
2 \\
-3
\end{bmatrix}
+ 0 \cdot
\begin{bmatrix}
0 \\
-1 \\
4
\end{bmatrix}
=
\begin{bmatrix}
2 \\
-1 \\
0
\end{bmatrix}
+
\begin{bmatrix}
-1 \\
2 \\
-3
\end{bmatrix}
+
\begin{bmatrix}
0 \\
0 \\
0
\end{bmatrix}
=
\begin{bmatrix}
1 \\
1 \\
-3
\end{bmatrix}
$$
![[Pasted image 20251009074714.png | 600]]
**$\vec{b}$ zeigt auf den Punkt D**

## Kann man jede neue Spalte $\vec{b}$ berechnen?
---
### Als Spaltenbild
---
> [!Definition 1.2] Spaltenbild
> $A \cdot \vec{x}$ ist die Linearkombination der Spalten der Matrix $A$
> $$
> A \cdot \vec{x}
> =
> A \cdot
> \begin{bmatrix}
> x_1 \\
> x_2 \\
> \dots
> \end{bmatrix}
> =
> x_1 \cdot
>  \begin{bmatrix}
> \text{1. Spalte} \\
> \dots \\
> \dots
> \end{bmatrix}
> +
>  x_2 \cdot
>  \begin{bmatrix}
> \text{2. Spalte} \\
> \dots \\
> \dots
> \end{bmatrix}
>  +
>  x_3 \cdot
>  \begin{bmatrix}
> \text{3. Spalte} \\
> \dots \\
> \dots
> \end{bmatrix}
> +
> \dots
> $$
> Mit der Matrix
> $$
> A = 
> \begin{bmatrix}
> \text{1. Spalte} & \text{2. Spalte} & \dots \\
> \dots \\
> \dots
> \end{bmatrix}
> $$

**Bsp.:**
Neue Spalte berechnen, die sich aus $A \cdot \vec{x}$ ergibt
$$
A = 
\begin{bmatrix}
2 & 5 \\
1 & 3
\end{bmatrix}
\qquad
\vec{x}
\begin{bmatrix}
1 \\
2
\end{bmatrix}
$$
$$
A \cdot \vec{x} =
\begin{bmatrix}
2 & 5 \\
1 & 3
\end{bmatrix}
\cdot
\begin{bmatrix}
1 \\
2
\end{bmatrix}
=
1 \cdot
\begin{bmatrix}
2 \\
1
\end{bmatrix}
+
2 \cdot
\begin{bmatrix}
5 \\
3
\end{bmatrix}
=
\begin{bmatrix}
12 \\
7
\end{bmatrix}
= \vec{b}
$$
### Als Zeilenbild
---
> [!Definition 1.4] Zeilenbild
> $A \cdot \vec{x}$ zeilenweise Produkt berechnen
>  $$
> A \cdot \vec{x}
> =
> A \cdot
> \begin{bmatrix}
> x_1 \\
> x_2 \\
> \dots
> \end{bmatrix}
> =
> \begin{bmatrix}
> x_1 \cdot a_{11} + x_2 \cdot a_{12} + \dots \\
> x_1 \cdot a_{21} + x_2 \cdot a_{22} + \dots \\
> \cdots
> \end{bmatrix}
> $$
> mit der Matrix
> $$
> A =
> \begin{bmatrix}
> a_{11} & a_{12} & \dots \\
> a_{21} & a_{22} & \dots \\
> \dots
> \end{bmatrix}
> $$

**Bsp.:**
Neue Spalte berechnen, die sich aus $A \cdot \vec{x}$ ergibt
$$
A =
\begin{bmatrix}
2 & 5 \\
1 & 3
\end{bmatrix}
\qquad
\vec{x} =
\begin{bmatrix}
1 \\
2
\end{bmatrix}
$$
$$
A \cdot \vec{x} =
\begin{bmatrix}
2 & 5 \\
1 & 3
\end{bmatrix}
\cdot
\begin{bmatrix}
1 \\
2
\end{bmatrix}
=
\begin{bmatrix}
2 \cdot 1 + 5 \cdot 2 \\
1 \cdot 1 + 3 \cdot 2
\end{bmatrix}
=
\begin{bmatrix}
12 \\
7
\end{bmatrix}
$$

## Wann ist es nicht möglich auf die Spalte $\vec{b}$ zu kommen?
---
**Bsp.:**
$$
A =
\begin{bmatrix}
1 & 2 \\
1 & 2
\end{bmatrix}
\qquad
\vec{x} =
\begin{bmatrix}
x_1 \\
x_2
\end{bmatrix}
\qquad
\vec{b} = 
\begin{bmatrix}
1 \\
0
\end{bmatrix}
$$
$\Rightarrow$ Wir sehen, dass die Spalten 1 und 2 bei $A$ gleich bzw. Vielfache voneinander sind
	$\Rightarrow$ Alle Spalten sind Linearkombination von $\begin{bmatrix}1 \\ 1\end{bmatrix}$ 

> [!Definition 1.4] Lineare Abhängigkeit
> Wenn mindestens eine Spalte die Linearkombination von einer anderen ist, so ist die Menge der Spalten **linear abhängig**
> Ansonsten immer **linear unabhängig*

> [!Satz1.1] Lösbarkeit von Linearen Gleichungssystem
> Die Gleichung $A \cdot \vec{x} = \vec{b}$ kann nur eindeutig auf ein $\vec{x}$ gelöst werden, wenn die Spalten von $A$ linear unabhängig ist

