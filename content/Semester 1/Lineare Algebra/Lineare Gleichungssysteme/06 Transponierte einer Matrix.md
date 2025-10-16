## Definition
---
Die Transponierte einer Matrix $A \in \mathbb{R^{m \times n}}$ ist als $A^T$ definiert, in der die Zeilen und Spalten vertauscht sind

$$
\begin{aligned}
A = 
\begin{bmatrix}
\uparrow & \uparrow & &\uparrow \\
\vec{a_1} & \vec{a_2} & \dots &\vec{a_n} \\
\downarrow & \downarrow & &\downarrow \\
\end{bmatrix}

\Rightarrow

A^T = 
\begin{bmatrix}
\leftarrow \vec{a_1} \rightarrow \\ \leftarrow \vec{a_2} \rightarrow \\ \vdots \\ \leftarrow \vec{a_n} \rightarrow \\
\end{bmatrix}

\end{aligned}
$$
$\Rightarrow$ Es gilt: $A^T \in \mathbb{R^{n \times m}}$ 

### Beispiel
---
$$
\begin{aligned}
A = 
\begin{bmatrix}
1 & 4 & 5 \\
7 & 2 & 6 \\
8 & 9 & 3
\end{bmatrix}

\Rightarrow

A^T = 
\begin{bmatrix}
1 & 7 & 8 \\
4 & 2 & 9 \\
5 & 6 & 3
\end{bmatrix}

\end{aligned}
$$
$\Rightarrow$ Man sieht, dass die Diagonalen gleich bleiben

## Transponierte des Produkts zweier Matrizen
---
geg.: $A \in \mathbb{R^{m \times n}}$,  $A \in \mathbb{B^{n \times p}}$

$$
\begin{aligned}
(A \cdot B)^T =

\left(
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
\end{bmatrix}
\right)^T &=

\begin{bmatrix}
<\vec{a_1}, \vec{b_1}> & <\vec{a_1}, \vec{b_2}> & \dots & <\vec{a_1}, \vec{b_p}> \\
<\vec{a_2}, \vec{b_1}> & <\vec{a_2}, \vec{b_2}> & \dots & <\vec{a_2}, \vec{b_p}> \\
\vdots &\vdots &\ddots &\vdots \\
<\vec{a_m}, \vec{b_1}> & <\vec{a_m}, \vec{b_2}> & \dots & <\vec{a_m}, \vec{b_p}>
\end{bmatrix}^T \\\\\\ &=

\begin{bmatrix}
<\vec{a_1}, \vec{b_1}> & <\vec{a_2}, \vec{b_1}> & \dots & <\vec{a_m}, \vec{b_1}> \\
<\vec{a_1}, \vec{b_2}> & <\vec{a_2}, \vec{b_2}> & \dots & <\vec{a_m}, \vec{b_2}> \\
\vdots &\vdots &\ddots &\vdots \\
<\vec{a_1}, \vec{b_p}> & <\vec{a_2}, \vec{b_p}> & \dots & <\vec{a_m}, \vec{b_p}>
\end{bmatrix} \\\\ &=

\begin{bmatrix}
\leftarrow \vec{b_1} \rightarrow \\
\leftarrow \vec{b_2} \rightarrow \\
\vdots \\ 
\leftarrow \vec{b_p} \rightarrow
\end{bmatrix} \cdot
\begin{bmatrix}
\uparrow &\uparrow & &\uparrow \\
\vec{a_1} &\vec{a_2}  &... &\vec{a_m} \\
\downarrow &\downarrow & &\downarrow
\end{bmatrix}\\\\ &= B^T \cdot A^T \\\\

\Rightarrow (A \cdot B)^T &= B^T \cdot A^T

\end{aligned} 
$$
## Inverse einer Transponierten Matrix $A^T$ 
---
$$
\begin{aligned}
&\qquad A \cdot A^{-1} = I_{n \times n} \\
&\Leftrightarrow (A \cdot A^{-1})^T = I^{T}_{n \times n} \\
&\Leftrightarrow (A^{-1})^T \cdot A^T = I_{n \times n} \\\\
&\Rightarrow (A^T)^{-1} = (A^{-1})^T \Rightarrow \text{Transposition und Invertierung darf vertauscht werden}
\end{aligned}
$$

## Symmetrische Matrix
---
Eine Matrix $A \in \mathbb{R^{n \times n}}$ ist symmetrisch wenn $A^T = A$ 

### Beispiel
---
$$
\begin{aligned}
\begin{bmatrix}
3 & 4 & 8 \\
4 & 6 & 0 \\
8 & 0 & 9
\end{bmatrix}

\cdot 

\begin{bmatrix}
3 & 4 & 8 \\
4 & 6 & 0 \\
8 & 0 & 9
\end{bmatrix}

\Rightarrow

\begin{bmatrix}
3 & 4 & 8 \\
4 & 6 & 0 \\
8 & 0 & 9
\end{bmatrix}
\end{aligned}
$$
### Symmetrie bei einer Matrix $B \in \mathbb{R^{m \times n}}$ 
---
Das Produkt aus $B^T \cdot B$ ist symmetrisch
$$
\begin{aligned}
A^T &= (B^T \cdot B)^T \\
&= B^T \cdot (B^T)^T \\
&= B^T \cdot B = A
\end{aligned}
$$

#### Beispiel
---
$$
B =
\begin{bmatrix}
4 & 2 & 2 \\
8 & 9 & 1
\end{bmatrix}, \quad

B^T = 
\begin{bmatrix}
4 & 8 \\
2 & 9 \\
2 & 1
\end{bmatrix}
$$
$$
\begin{aligned}

\text{Zeile $\cdot$ Spalte} \quad

\begin{bmatrix}
4 & 2 & 2 \\
8 & 9 & 1
\end{bmatrix}

\cdot


\begin{bmatrix}
4 & 8 \\
2 & 9 \\
2 & 1
\end{bmatrix}

=

\begin{bmatrix}
24 & 52 \\
52 & 146
\end{bmatrix}
\end{aligned}
$$
$$
\begin{aligned}
\text{Spalte $\cdot$ Zeile} \quad
\begin{bmatrix}
4 & 8 \\
2 & 9 \\
2 & 1
\end{bmatrix}

\cdot

\begin{bmatrix}
4 & 2 & 2 \\
8 & 9 & 1
\end{bmatrix}

=

\begin{bmatrix}
80 & 80 & 16 \\
80 & 85 & 13 \\
16 & 13 & 5
\end{bmatrix}
\end{aligned}
$$

$\Rightarrow$ Das Produkt ist in beiden Multiplikationen symmetrisch