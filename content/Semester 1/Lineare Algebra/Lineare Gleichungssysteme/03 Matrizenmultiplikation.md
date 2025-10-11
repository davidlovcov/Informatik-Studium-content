## Matrix $\cdot$ Spalte = Spalte
---
$$
A \cdot \vec{x} = A \cdot \begin{bmatrix} x_1 \\ x_2 \\ \dots\end{bmatrix}
= x_1 \cdot \begin{bmatrix} \text{1. Spalte} \\ \dots  \\ \dots \end{bmatrix} + x_2 \cdot \begin{bmatrix} \text{2. Spalte} \\ \dots  \\ \dots \end{bmatrix} + \dots 
$$
## Zeile $\cdot$ Matrix = Zeile
---
$$
\vec{x} \cdot A = \begin{bmatrix}x_1 & x_2 & \dots\end{bmatrix} \cdot A = x_1 \cdot \begin{bmatrix} \text{1. Zeile}\ \dots\end{bmatrix} + x_2 \cdot \begin{bmatrix} \text{2. Zeile}\ \dots\end{bmatrix} + \dots
$$
**Beispiel.:**
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

## Matrix $\cdot$ Matrix = Matrix
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

### Variante 1 (Zeilen-Sicht)
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

### Variante 2 (Spalten-Sicht)
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

### Wichtige Bemerkungen
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
## Reelles Skalarprodukt
---
- Hat man eine Zeile oder Spalte $\vec{a}$ und $\vec{b}$ so kann man das reelle Skalarprodukt so definieren:

$$
\begin{aligned}
\lt \ \vec{a},\ \vec{b} \ \gt \ = \sum_{i = 1}^n a_i \cdot b_i \ (=  \lt \ \vec{b}, \ \vec{a}  \ \gt)
\end{aligned}
$$

<hr>

<div style="display: flex; justify-content: space-between;">

  <a href="02 Eliminationsmethode">← Zurück</a>

  <!--<a href="">Weiter →</a>-->

</div>