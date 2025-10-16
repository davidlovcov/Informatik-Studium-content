
## Rückführung: Matrix $\cdot$ Spalte und Zeile $\cdot$ Matrix
### Matrix $\cdot$ Spalte = Spalte
---
$$
A \cdot \vec{x} = A \cdot \begin{bmatrix} x_1 \\ x_2 \\ \dots\end{bmatrix}
= x_1 \cdot \begin{bmatrix} \text{1. Spalte} \\ \dots  \\ \dots \end{bmatrix} + x_2 \cdot \begin{bmatrix} \text{2. Spalte} \\ \dots  \\ \dots \end{bmatrix} + \dots 
$$
#### Beispiel
---
$$
\begin{aligned}
\begin{bmatrix}
1 & 2 & 1 \\
3 & 8 & 1 \\
0 & 4 & 1
\end{bmatrix} \cdot

\begin{bmatrix}
1 \\
2 \\
1
\end{bmatrix} =

1 \cdot 
\begin{bmatrix}
1 \\
3 \\
0
\end{bmatrix} +
2 \cdot
\begin{bmatrix}
2 \\
8 \\
4
\end{bmatrix} +
1 \cdot
\begin{bmatrix}
1 \\
1 \\
1
\end{bmatrix} =

\begin{bmatrix}
1 + 4 + 1 \\
3 + 16 + 1 \\
0 + 8 + 1
\end{bmatrix} =
\begin{bmatrix}
6 \\
20 \\
9
\end{bmatrix}

\end{aligned}
$$
### Zeile $\cdot$ Matrix = Zeile
---
$$
\vec{x} \cdot A = \begin{bmatrix}x_1 & x_2 & \dots\end{bmatrix} \cdot A = x_1 \cdot \begin{bmatrix} \text{1. Zeile}\ \dots\end{bmatrix} + x_2 \cdot \begin{bmatrix} \text{2. Zeile}\ \dots\end{bmatrix} + \dots
$$
#### Beispiel
---
$$
\begin{aligned}
&\begin{bmatrix}1 & 2 & 1\end{bmatrix} \cdot 
\begin{bmatrix}
1 & 2 & 1 \\
3 & 8 & 1 \\
0 & 4 & 1
\end{bmatrix} = 1 \cdot \begin{bmatrix} 1 & 2 & 1 \end{bmatrix} + 2 \cdot \begin{bmatrix} 3 & 8 & 1 \end{bmatrix} + 1 \cdot \begin{bmatrix} 0 & 4 & 1 \end{bmatrix}

\\\\= &\begin{bmatrix} 1 & 2 & 1\end{bmatrix} + \begin{bmatrix} 6 & 16 & 2\end{bmatrix} + \begin{bmatrix} 0 & 4 & 1\end{bmatrix}
\\\\\\= &\begin{bmatrix}7 & 22 & 4\end{bmatrix}

\end{aligned}
$$

## Wichtige Bemerkungen
---
- Bei der Matrizenmultiplikation darf die Reihenfolge nicht vertauscht werden
$$
\begin{aligned}
A \cdot B \ne B \cdot A
\end{aligned}
$$
- Die Reihenfolge in der man sie auswertet ist egal
$$
\begin{aligned}
A \cdot B \cdot C = (A \cdot B) \cdot C = A \cdot (B \cdot C)
\end{aligned}
$$
- Die Anzahl der Spalten $A$ und Anzahl der Zeilen $B$ müssen übereinstimmen. Es gilt:
	- $m$ = Anzahl der Reihen in $A$
	- $n$ = Anzahl der Spalten in $A$ = Anzahl der Zeilen in $B$
	- $p$ = Anzahl der Spalten in B

- Die Schreibweise für Matrixdimensionen lautet $A \in \mathbb{R}^{m \times n}$

## 1. und 2.Form (Spalten- und Reihenmultiplikation)
---
- Zusammenführung von Spalten- und Reihenmultiplikation zu Matrizenmultiplikation
$$
\begin{aligned}
A \cdot B =

\begin{bmatrix}
\leftarrow \vec{a}_1 \rightarrow \\ 
\leftarrow \vec{a}_2 \rightarrow \\
\dots \\
\leftarrow \vec{a}_n \rightarrow
\end{bmatrix}

\cdot

\begin{bmatrix}
\uparrow & \uparrow &  & \uparrow \\
\vec{b}_1 & \vec{b}_2 & \dots & \vec{b}_n \\
\downarrow & \downarrow & & \downarrow
\end{bmatrix} &= 

\begin{bmatrix}
\uparrow & \uparrow &  & \uparrow \\
A \cdot \vec{b}_1 & A \cdot \vec{b}_2 & \dots & A \cdot \vec{b}_n \\
\downarrow & \downarrow & & \downarrow
\end{bmatrix} 

\\\\\\
&=
\begin{bmatrix}
\leftarrow \vec{a}_1 \cdot B \rightarrow \\ 
\leftarrow \vec{a}_2 \cdot B \rightarrow \\
\dots \\
\leftarrow \vec{a}_n \cdot B \rightarrow
\end{bmatrix}

\end{aligned}
$$
### Beispiele
---
#### 1. Form (Spalten-Bild)
---
$$
\begin{aligned}
\begin{bmatrix}
1 & 2 \\
3 & 4 
\end{bmatrix}
\cdot
\begin{bmatrix}
-1 & 0 \\
1 & 1
\end{bmatrix}
=
\begin{bmatrix}

\begin{bmatrix}
1 & 2 \\
3 & 4
\end{bmatrix}
\cdot
\begin{bmatrix}
-1 \\
1
\end{bmatrix},
\begin{bmatrix}
1 & 2 \\
3 & 4
\end{bmatrix}
\cdot
\begin{bmatrix}
0 \\
1
\end{bmatrix}


\end{bmatrix}
=
\begin{bmatrix}
-1 
\cdot
\begin{bmatrix}
1 \\
3
\end{bmatrix}
+
1
\cdot
\begin{bmatrix}
2 \\
4
\end{bmatrix},

0 
\cdot
\begin{bmatrix}
1 \\
3
\end{bmatrix}
+
1
\cdot
\begin{bmatrix}
2 \\
4
\end{bmatrix}



\end{bmatrix}
=

\begin{bmatrix}
1 & 2 \\
1 & 4
\end{bmatrix}
\end{aligned}
$$
- Die Spalten von $A$ wirken auf $B$
#### 2. Form (Zeilen-Bild)
---
$$
\begin{aligned}
\begin{bmatrix}
1 & 2 \\
3 & 4 
\end{bmatrix}
\cdot
\begin{bmatrix}
-1 & 0 \\
1 & 1
\end{bmatrix}
=
\begin{bmatrix}
\begin{bmatrix}
1 & 2
\end{bmatrix}
\cdot
\begin{bmatrix}
-1 & 0 \\
1 & 1
\end{bmatrix}\\

\begin{bmatrix}
3 & 4
\end{bmatrix}
\cdot
\begin{bmatrix}
-1 & 0 \\
1 & 1
\end{bmatrix}
\end{bmatrix}=

\begin{bmatrix}
1 \cdot 
\begin{bmatrix}
-1 & 0
\end{bmatrix}
+
2 \cdot
\begin{bmatrix}
1 & 1
\end{bmatrix}\\
3 \cdot
\begin{bmatrix}
-1 & 0
\end{bmatrix}
+
4 \cdot
\begin{bmatrix}
1 & 1
\end{bmatrix}
\end{bmatrix} =

\begin{bmatrix}
1 & 2 \\
1 & 4
\end{bmatrix}

\end{aligned}
$$
- Die Zeilen von $A$ wirken auf $B$
## 3. Form (Allgemeine Matrizenmultiplikation)
---
### Reelles Skalarprodukt
---
- Hat man eine Zeile oder Spalte $\vec{a}$ und $\vec{b}$ so kann man das reelle Skalarprodukt so definieren:
$$
\begin{aligned}
\lt \ \vec{a},\ \vec{b} \ \gt \ = \sum_{i = 1}^n a_i \cdot b_i \ (=  \lt \ \vec{b}, \ \vec{a}  \ \gt)
\end{aligned}
$$
$$
\begin{aligned}
\Rightarrow
A \cdot B =
\begin{bmatrix}
\leftarrow \vec{a_1} \rightarrow \\
\leftarrow \vec{a_2} \rightarrow \\
\vdots \\ 
\leftarrow \vec{a_n} \rightarrow
\end{bmatrix} \cdot
\begin{bmatrix}
\uparrow &\uparrow & &\uparrow \\
\vec{b_1} &\vec{b_2}  &... &\vec{b_n} \\
\downarrow &\downarrow & &\downarrow
\end{bmatrix} =
\vec{a_1} \cdot \vec{b_1} + \vec{a_2} \cdot \vec{b_2} + \dots + \vec{a_n} \cdot \vec{b_n}
\end{aligned}
$$
### Nutzung des reellen Skalarprodukts für die Multiplikation
---
- Es gilt: $A \in \mathbb{R}^{m \times n}$ und $B \in \mathbb{R}^{n \times p}$
$$
\begin{aligned}
A \cdot B =
\begin{bmatrix}
\leftarrow \vec{a_1} \rightarrow \\
\leftarrow \vec{a_2} \rightarrow \\
\vdots \\ 
\leftarrow \vec{a_m} \rightarrow
\end{bmatrix} \cdot
\begin{bmatrix}
\uparrow &\uparrow & &\uparrow \\
\vec{b_1} &\vec{b_2}  &... &\vec{b_p} \\
\downarrow &\downarrow & &\downarrow
\end{bmatrix} &=
\begin{bmatrix}
<\vec{a_1}, \vec{b_1}> & <\vec{a_1}, \vec{b_2}> & \dots & <\vec{a_1}, \vec{b_p}> \\
<\vec{a_2}, \vec{b_1}> & <\vec{a_2}, \vec{b_2}> & \dots & <\vec{a_2}, \vec{b_p}> \\
\vdots &\vdots &\ddots &\vdots \\
<\vec{a_m}, \vec{b_1}> & <\vec{a_m}, \vec{b_2}> & \dots & <\vec{a_m}, \vec{b_p}>
\end{bmatrix} \\\\\\ &=
\begin{bmatrix}
\vec{a_{11}} \cdot \vec{b_{11}} + \vec{a_{12}} \cdot \vec{b_{12}} + \cdots + \vec{a_{1n}} \cdot \vec{b_{1n}} 
&& \vec{a_{11}} \cdot \vec{b_{21}} + \vec{a_{12}} \cdot \vec{b_{22}} + \cdots + \vec{a_{1n}} \cdot \vec{b_{2n}} 
&& \dots && \vec{a_{11}} \cdot \vec{b_{p1}} + \vec{a_{12}} \cdot \vec{b_{p2}} + \cdots + \vec{a_{1n}} \cdot \vec{b_{pn}} \\

\vec{a_{21}} \cdot \vec{b_{11}} + \vec{a_{22}} \cdot \vec{b_{12}} + \cdots + \vec{a_{2n}} \cdot \vec{b_{1n}} 
&& \vec{a_{21}} \cdot \vec{b_{21}} + \vec{a_{22}} \cdot \vec{b_{22}} + \cdots + \vec{a_{2n}} \cdot \vec{b_{2n}} 
&& \dots && \vec{a_{21}} \cdot \vec{b_{p1}} + \vec{a_{22}} \cdot \vec{b_{p2}} + \cdots + \vec{a_{2n}} \cdot \vec{b_{pn}} \\
\vdots &&\vdots && \ddots &&\vdots \\

\vec{a_{m1}} \cdot \vec{b_{11}} + \vec{a_{m2}} \cdot \vec{b_{12}} + \cdots + \vec{a_{mn}} \cdot \vec{b_{1n}} 
&& \vec{a_{m1}} \cdot \vec{b_{21}} + \vec{a_{m2}} \cdot \vec{b_{22}} + \cdots + \vec{a_{mn}} \cdot \vec{b_{2n}} 
&& \dots && \vec{a_{m1}} \cdot \vec{b_{p1}} + \vec{a_{m2}} \cdot \vec{b_{p2}} + \cdots + \vec{a_{mn}} \cdot \vec{b_{pn}} \\

\end{bmatrix}
\end{aligned}

$$
$\Rightarrow$ Die Endnismatrix $C$ hat $m$ Zeilen und $p$ Spalten
	$\Rightarrow (m \times n) \cdot (n \times p) = (m \times p)$ oder $A \in \mathbb{R}^{m \times n} \wedge B \in \mathbb{R}^{n \times p} = (A \cdot B) \in \mathbb{R}^{m \times p}$

### Beispiel
---
geg.:
$$
\begin{aligned}
A =
\begin{bmatrix}
2 & 3 & -1 \\
0 & 4 & 1
\end{bmatrix} \;
\text{und} \;
B =
\begin{bmatrix}
1 & -1 \\
-1 & 0 \\
0 & 2
\end{bmatrix} \;
\text{mit} \;
A \in \mathbb{R}^{m \times n},\; B \in \mathbb{R}^{n \times p}
\end{aligned}
$$
$$
\begin{aligned}
A \cdot B =
\begin{bmatrix}
2 & 3 & -1 \\
0 & 4 & 1
\end{bmatrix} \cdot
\begin{bmatrix}
1 & -1 \\
-1 & 0 \\
0 & 2
\end{bmatrix} &=
\begin{bmatrix}
2 \cdot 1 + 3 \cdot (-1) + (-1) \cdot 0 & \quad 2 \cdot (-1) + 3 \cdot 0 + (-1) \cdot 2
\\
0 \cdot 1 + 4 \cdot (-1) + 1 \cdot 0 &0 \cdot (-1) + 4 \cdot 0 + 1 \cdot 2
\end{bmatrix}\\\\ &=
\begin{bmatrix}
-1 & -4 \\
-4 & 2
\end{bmatrix}
\end{aligned}
$$
## 4. Form (Allgemeine Matrizenmultiplikation vertauscht)
---
- Statt Zeilen $\cdot$ Spalten machen wir Spalten $\cdot$ Zeilen
	$\Rightarrow$ Gegenteil des Skalarprodukts

$$
\begin{aligned}
A \cdot B =
\begin{bmatrix}
\uparrow &\uparrow & &\uparrow \\
\vec{a_1} &\vec{a_2}  &... &\vec{a_n} \\
\downarrow &\downarrow & &\downarrow
\end{bmatrix} \cdot

\begin{bmatrix}
\leftarrow \vec{b_1} \rightarrow \\
\leftarrow \vec{b_2} \rightarrow \\
\vdots \\ 
\leftarrow \vec{b_n} \rightarrow
\end{bmatrix}
\end{aligned}
$$
$$
\begin{aligned}
\vec{a_i} \cdot \vec{b_i} =
\begin{bmatrix}
a_{i,1} \\
a_{i,2} \\
\vdots \\
a_{i,m} \\
\end{bmatrix} \cdot

\begin{bmatrix}
b_{i,1} & b_{i,2} & \dots & b_{i,p}
\end{bmatrix} = 

\begin{bmatrix}
a_{i,1} \cdot b_{i,1} & a_{i,1} \cdot b_{i,2} & \dots & a_{i,1} \cdot b_{i,p} \\
a_{i,2} \cdot b_{i,1} & a_{i,2} \cdot b_{i,2} & \dots & a_{i,2} \cdot b_{i,p} \\
\vdots &\vdots & \ddots & \vdots \\
a_{i,m} \cdot b_{i,1} & a_{i,m} \cdot b_{i,2} & \dots & a_{i,m} \cdot b_{i,p}
\end{bmatrix} 
\end{aligned}
$$
$\Rightarrow A \cdot B = \vec{a_1} \cdot \vec{b_1} + \vec{a_2} + \vec{b_2} + \dots + \vec{a_n} \cdot \vec{b_n}$ 

<hr>

<div style="display: flex; justify-content: space-between;">

  <a href="02 Eliminationsmethode">← Zurück</a>

  <!--<a href="">Weiter →</a>-->

</div>