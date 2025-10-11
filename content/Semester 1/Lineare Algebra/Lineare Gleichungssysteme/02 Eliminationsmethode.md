## Gauß-Algorithmus
---
**geg.:**
$$
\begin{aligned}
x + 2y + z &= 2 \quad &\text{1. Zeile / Gleichung}\\
3x + 8y + z &= 12 \quad &\text{2. Zeile / Gleichung}\\
4y + z &= 2 \quad &\text{3. Zeile / Gleichung}
\end{aligned}
$$
**ges.:**
$$
\begin{aligned}
x, y, z
\end{aligned}
$$
**Lös.:**
$$
\begin{bmatrix}
1 & 2 & 1 & \quad 2 \\
3 & 8 & 1 & \quad 12 \\
0 & 4 & 1 & \quad 2
\end{bmatrix}
$$
- Mithilfe von Pivot-Elemente müssen wir eine Zeilen-Stufen-Form herstellen, indem wir Nullen drunter erzeugen 
- Ganz oben links bei $m = 1$ anfangen
- Es gilt $m \ne 0$, sonst Zeilen vertauschen. Wir fangen an indem wir von der 2. Zeile 3 mal die 1. abziehen.
$$
\begin{bmatrix}
1 & 2 & 1 & \quad 2 \\
0 & 2 & -2 & \quad 6 \\
0 & 4 & 1 & \quad 2
\end{bmatrix}
$$
- Anschließend müssen wir von der letzten Zeile 2 mal die 2te Reihe abziehen.
$$
\begin{bmatrix}
1 & 2 & 1 & \quad 2 \\
0 & 2 & -2 & \quad 6 \\
0 & 0 & 5 & \quad -10
\end{bmatrix}
$$
- Damit haben wir jetzt eine Zeile mit nur einer Unbekannten.

> [!NOTE] Unendlich viele Lösungen und keine Lösung
> **Unendlich viele Lösungen:** Wenn komplette letzte Zeile eine Nullzeile ist
> **Keine Lösung:** Wenn $\vec{c}$ keine Null ist aber $U$ eine Nullzeile ist

### Rücksubstitution 
---
$$
\begin{aligned}
\Rightarrow 5z &= -10 \\
z &= -2 \\\\
2y - 2z &= 6 \\
2y - 2 \cdot -2 &= 6 \\
2y + 4 &= 6 \\
2y &= 2 \\
y &= 1 \\\\

x + 2y + z &= 2 \\
x + 2 \cdot 1 + 1 \cdot -2 &= 2 \\
x + 2 - 2 &= 2 \\
x = 2
\end{aligned}
$$
- $\Rightarrow$ für $x = 2$, $y = 1$ und $z = -2$ ist das Lineare Gleichungssystem gelöst
- $\Rightarrow \mathbb{L} = \{2;\ 1;\ -2\}$

### Algorithmus im Detail
---
#### Algorithmus zur Elimination
---
1. Starte mit $m = 1$
2. Finde $m$ Pivot-Element $\ne 0$ in $m$ Zeile. Sonst Zeilen vertauschen
3. Erzeuge Nullen unter dem $m$ Pivot-Element, mithilfe von Addition und Multiplikation der $m$ Zeile auf die nachkommende Zeile
4. Setze $m \rightarrow m + 1$. Schritt 2. - 4. Wiederholen bis kein Pivot-Element ($\ne 0$) mehr gefunden wird oder keine $m$ die letzte Zeile ist
5. Die Matrix $U$ kann als obere Dreiecksmatrix abgelesen werden und die rechte Seite als $\vec{c}$

#### Algorithmus zur Rücksubstitution
---
6. Wenn die $U$ Zeile eine Nullzeile ist aber $\vec{c}$ nicht, dann gibt es keine Lösung $\rightarrow$ AUFHÖREN!
7. Setze $m =$ letzte Zeilenzahl, welche keine "Nullzeile" ist
8. Löse $m$ Zeile nach Variable bei Pivot-Element auf
9. Setze $m \rightarrow m - 1$. Wiederhole Schritt 8.-9. bis $m = 1$
10. Die Lösung $\vec{x}$ kann abgelesen werden
