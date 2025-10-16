## Definition
---
- Die Inverse Matrix $A^{-1}$ einer quadratischen Matrix $A$ für $A \in \mathbb{R^{n \times n}}$ wird folgendermaßen definiert

$$
\begin{aligned}
A^{-1} \cdot A = A \cdot A^{-1} =

\begin{bmatrix}
1 & 0 & \dots & 0 \\
0 & 1 & \dots & 0 \\
\vdots & \vdots & \ddots & \vdots \\
0 & 0 & \dots & 1
\end{bmatrix}

= I_{n \times n}

\end{aligned}
$$
$\Rightarrow$ Bei recht- oder linksseitiger Multiplikation erhält man die Einheitsmatrix $I_{n \times n}$

## Bedeutung der Einheitsmatrix $I$
---
- Das Produkt einer quadratischen Matrix $A$ mit der passenden Einheitsmatrix $I$ ergibt wieder $A$
     $\Rightarrow$ Einheitsmatrix $I$ verhält sich neutral

## Motivation $I$: Analogie aus den reellen Zahlen
---
- Sei die Inverse von der reellen Zahl $a$ die Variable $c$, so gilt:

$$
\begin{aligned}
c \cdot a = a \cdot c = 1 \\

\Rightarrow c = \frac{1}{a} \quad \text{für} \; a \ne 0

\end{aligned}
$$
- Die 1 ist dabei das neutrale Element

## Motivation $II$: Lösen von Gleichungssystemen
---
$$
\begin{aligned}
A \cdot \vec{x} = \vec{b} \quad &\Leftrightarrow  \quad A^{-1} \cdot A \cdot \vec{x} = A^{-1} \cdot \vec{b} \\

&\Leftrightarrow \quad I_{n \times n} \cdot \vec{x} = A^{-1} \cdot \vec{b}\\
&\Leftrightarrow \quad \vec{x} = A^{-1} \cdot \vec{b}
\end{aligned}
$$
- Wir haben zuvor definiert, dass die Einheitsmatrix $I$ neutral ist
	 $\Rightarrow$ Aus diesem Grund können wir sie aus der Gleichung rausnehmen
- Als Vergleich: $1 \cdot \vec{x} = \vec{x}$

## Invertierbarkeit / Singularität
---
- Existiert die Inverse $A^{-1}$ einer quadratischen Matrix $A \in \mathbb{R^{n \times n}}$, dann sagen wir, dass $A$ invertierbar ist 
- Existiert keine Inverse $A^{-1}$, dann sagen wir, dass $A$ singulär ist
- Die Spalten der Matrix $A$ müssen linear unabhängig sein um invertierbar zu sein
- Das Gleichungssystem $A \cdot \vec{x} = \vec{0}$ muss nur mit $\vec{x} = 0$ lösbar sein, damit Matrix $A$ invertierbar ist 

## Singuläre Matrix
---
- Sehen wir uns als Beispiel die Matrix $A = \left[\begin{smallmatrix} 1 & 3 \\ 2 & 6 \end{smallmatrix}\right]$ an
- Wir erkennen, dass sie linear abhängig ist, da die Spalten vielfache voneinander sind
	  $\Rightarrow$ Die Matrix $A$ ist singulär

Rechnerische Prüfung:
$$
\begin{aligned}

\begin{bmatrix}
1 & 3 \\
2 & 6
\end{bmatrix}

\cdot

\begin{bmatrix}
b_{1,1} & b_{1,2}\\
b_{2,1} & b_{2,2}
\end{bmatrix}

&=

\begin{bmatrix}
1 & 0 \\
0 & 1
\end{bmatrix}
\\\\

\Rightarrow
\begin{bmatrix}
1 & 3 \\
2 & 6
\end{bmatrix}

\cdot

\begin{bmatrix}
b_{1,1} \\
b_{2,1}
\end{bmatrix}

&=

\begin{bmatrix}
1 \\
0
\end{bmatrix}

\\\\

\Rightarrow
\left\{
\begin{array}. 
1 \cdot b_{1,1} + 3 \cdot b_{21} &= 1 \\
2 \cdot b_{1,1} + 6 \cdot b_{21} &= 0
\end{array}
\right\}

\\\\

\text{Erste Gleichung nach $b_{1,1}$ auflösen und in die 2te einsetzen: } 

\\

b_{1,1} &= 1 - 3b_{2,1}

\\\\
2 \cdot (1 - 3b_{2,1}) + 6b_{2,1} &= 0 \\
2 - 6b_{2,1} + 6b_{2,1} &= 0 \\
2 &= 0 \; \unicode{x21af} \quad \Rightarrow \text{nicht lösbar!}

\end{aligned}
$$

## Charakterisierung lineare Unabhängigkeit
---
- Eine Matrix $A$ ist linear unabhängig, wenn es für $\vec{x}$ mit $x \ne 0$ keine Zahl gibt, die bei der Multiplikation von der Matrix $A$ und Vektor $\vec{x}$  als Ergebnis $\vec{0}$ ausgibt

### Beispiel
---
$$
\begin{aligned}

\begin{bmatrix}
1 & 3 \\
2 & 6
\end{bmatrix}

\cdot

\begin{bmatrix}
x_1 \\
x_2
\end{bmatrix}

&=

\begin{bmatrix}
0 \\
0
\end{bmatrix}

\\\\

\begin{bmatrix}
1 & 3 \\
2 & 6
\end{bmatrix}

\cdot

\begin{bmatrix}
3 \\
1
\end{bmatrix}

&=

\begin{bmatrix}
1 \cdot 3 + 3 \cdot (-1) \\
2 \cdot 3 + 6 \cdot (-1)
\end{bmatrix}

=

\begin{bmatrix}
0 \\
0
\end{bmatrix}

\end{aligned}
$$
$\Rightarrow$ linear abhängig da mindestens eine Spalte existiert, die die Spalte $\vec{0}$ erzeugt 

## Inverse einer Matrix ermitteln
---
Nehmen wir dafür als Beispiel die vorherige Matrix und machen sie linear unabhängig

$$
\begin{bmatrix}
1 & 3 \\
2 & 7
\end{bmatrix}

\cdot

\begin{bmatrix}
a & b \\
c & d
\end{bmatrix}

=

\begin{bmatrix}
1 & 0 \\
0 & 1
\end{bmatrix}
$$
### 1. Gauß-Algorithmus anwenden bis man die Zeilen-Stufen-Form erreicht hat
---
$$
\left[
\begin{array}{c c | c c}\
1 & 3 & 1 & 0\\
2 & 7 & 0 & 1
\end{array}
\right]

\quad \Longrightarrow \quad

\left[
\begin{array}{c c | c c}\
1 & 3 & 1 & 0\\
0 & 1 & -2 & 1
\end{array}
\right]
$$
### 2. Jordan-Algorithmus anwenden um alle Pivot-Elemente auf eine 1 zu bringen und über den Pivot-Elementen die Elemente eliminieren
---
$$
\left[
\begin{array}{c c | c c}\
1 & 3 & 1 & 0\\
0 & 1 & -2 & 1
\end{array}
\right]

\quad \Longrightarrow \quad

\left[
\begin{array}{c c | c c}\
1 & 0 & 7 & -3\\
0 & 1 & -2 & 1
\end{array}
\right]
$$
$$
\Rightarrow
A^{-1} =
\begin{bmatrix}
7 & -3 \\
-2 & 1
\end{bmatrix}
$$ **Überprüfung:** $$
\begin{aligned}

\begin{bmatrix}
1 & 3 \\
2 & 7
\end{bmatrix}

\cdot

\begin{bmatrix}
7 & -3 \\
-2 & 1
\end{bmatrix}

=

\begin{bmatrix}
7 + (-6) && -3 + 3 \\
14 + (-14) && (-6) + 7
\end{bmatrix}

=

\begin{bmatrix}
1 & 0 \\
0 & 1
\end{bmatrix}

\end{aligned}
$$
### Gauß-Jordan-Algorithmus
---
Mithilfe des Gauß-Jordan-Algorithmus kann man die Inverse $A^{-1} \in \mathbb{R^{n \times n}}$ einer invertierbaren Matrix $A^{n \times n}$ bestimmen

#### 1. Folgendes Tableau aufstellen
---
$A \quad|\quad I_{n \times n}$ 

#### 2. Gauß-Algorithmus anwenden um die Zeilen-Stufen-Form zu erreichen
---
$U \quad|\quad C$ 

#### 3. Jordan-Algorithmus anwenden um die line Seite durch elementare Zeilenumformung zur Einheitsmatrix zu führen ($\Rightarrow$ Reduzierte Zeilen-Stufen-Form)
---
$I_{n \times n} \quad|\quad A^{-1}$ 

#### 4. Auf der rechten Seite haben wir nun die Inverse $A^{-1}$ 

## Inverse von einem Produkt zweier invertierbaren Matrizen
---
Wir suchen die Inverse des Produktes aus $A \in \mathbb{R^{n \times n}}$ und $B \in \mathbb{R^{n \times n}}$

$$
\begin{aligned}
&(A \cdot B) \cdot (B^{-1} \cdot A^{-1}) \\
&= A \cdot (B \cdot B^{-1}) \cdot A^{-1} \\
&= A \cdot I_{n \times n} \cdot A^{-1} \\
&= A \cdot A^{-1} = I_{n \times x} \\\\

&\Rightarrow (A \cdot B)^{-1} = B^{-1} \cdot A^{-1}

\end{aligned}
$$

<hr>

<div style="display: flex; justify-content: space-between;">

  <a href="04 Eliminationsmethode in Matrix-Schreibweise">← Zurück</a>

  <a href="06 Transponierte einer Matrix">Weiter →</a>

</div>