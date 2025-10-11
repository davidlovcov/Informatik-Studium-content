## Ziele:
- Zahlendarstellung zu anderen Basen (Binärzahlen, Hexadezimalzahlen)
- Konvertierung von einem in anderen Zahlensystem
- Arithmetik in anderen Zahlensystem (Rechnung)
- Darstellung im Rechner (intern)
- Vorzeichenbehaftete Zahlen im Rechner darstellen
- BCD-Codes: oft verwendete Zahlen im boole'sche System
## Dezimalsystem 
---
$$243_{10}$$
$$= 2 \cdot 100 + 4 \cdot 10 + 3 \cdot 1$$
$$= 2 \cdot 10^2 + 4 \cdot 10^1 + 3 \cdot 10^0$$
$$\sum_{i=0}^{n-1} a_i \cdot 10^i$$


dabei ist 10 die Basis $b$
$$\sum_{i=0}^{n-1} a_i \cdot b^i$$
## Binärsystem
---
Basis $b = 2$ 
Es gilt allgemein: $0 \le a_i \lt b$ 

also: **$a_i \in \{0,\,1\}$**  

bsp.: 
$$1011_2$$
$$=1 \cdot 2^0 + 1 \cdot 2^1 + 1 \cdot 2^3$$
$$=11_{10}$$
### Addition
genauso wie im Dezimalsystem:
$$
\begin{array}{r}
	1010_2 \\
+ \;1110_2 \\
 \hline
	11000_2
\end{array}\;=\;
\begin{array}{r}
	10_{10} \\
+ \; 14_{10} \\
\hline
24_{10}
\end{array}
$$

### Subtraktion
$$
\begin{array}{r}
1010\quad0111_2 \\
-\quad1001\quad1100_2 \\
\hline 0000\quad1011_2
\end{array}
$$

## Hexadezimalsystem
---
Basis $b = 16$ 
also gilt: $0 \le a_i \lt 16$

$a_i \in \{\text{0, ... , 9, A, ... , F}\}$

Dez.: 10 11 12 13 14 15
Hex.:  A  B. C  D.  E.  F

$2E_{16} = 0x2E$

### Konversion von Dezimal in Hex
---
$$
\begin{aligned}
42_{10} : 16 &= 2 &&\text{Rest } 10\ (A) \\
2 : 16 &= 0 &&\text{Rest } 2 \\
\\[-4pt]
42_{10} &= 2A_{16} = 2 \cdot 16^1 + A \cdot 16^0
\end{aligned}
$$

#### Konversion zwischen Hex und Binär
$$
\begin{array}{c|c}
\text{Bin} & \text{Hex} \\ \hline
0000 & 0 \\
0001 & 1 \\
0010 & 2 \\
0011 & 4 \\
0100 & 5 \\
0101 & 6 \\
0110 & 7 \\
0111 & 8 \\
1000 & 9 \\
1001 & A \\
1010 & B \\
1011 & C \\
1100 & D \\
1110 & E \\
1111 & F \\
\end{array}
$$
- Diese Tabelle zeigt, dass man direkt konvertieren kann
Beispiel $2E_{16}$:
$$
\begin{aligned}
2_{16} &= 0010_2 \\
E_{16} &= 1110_2 \\
\text{-> } 2E_{16} &= 0010\;1110_2
\end{aligned}
$$


## Rationale Zahlen
---
 n   m
$\overline{14},\overline{25} = 1 \cdot 10^1 + 4\cdot10^0 + 2\cdot10^{-1} + 5 \cdot10^{-2}$


$$\sum_{-m}^{n-1} a_i \cdot b^i = \sum_{0}^{n-1} a_i \cdot b^i + \sum_{-m}^{-1} a_i \cdot b^i$$

#### in Binär umrechnen:
$$
\begin{aligned}
0,25 \cdot 2 &= 0,5 \\
0,5 \cdot 2 &= 1 \\\\
\text{-> }0,25_{10} &= 0,01_2 \\
\text{-> }14,25_10 &= 1110,01_2
\end{aligned}
$$

 $$
 \begin{aligned}
 0,625 \cdot 2 &= 1,25 \\
 0,25 \cdot 2 &= 0,5 \\
 0,5 \cdot 2 &= 1 \\\\
 \text{-> }0,625_{10} &= 0,101_1
\end{aligned}
$$

#### Periodizität
Beispiel 0,1:
$$
\begin{aligned}
0,1 \cdot 2 &= 0,2 \\
0,2 \cdot 2 &= 0,4 \\
0,4 \cdot 2 &= 0,8 \\
0,8 \cdot 2 &= 1,6 \\
0,6 \cdot 2 &= 1,2 \\
0,2 \cdot 2 &= 0,4 \\
0,4 \cdot 2 &= 0,8 \\
0,8 \cdot 2 &= 1,6 \\
&\dots \\
\text{-> } &0,00\overline{011}
\end{aligned}
$$
## Zahlendarstellung Binär
$[0; \,2^n - 1]$

$$
\begin{array}{r@{\quad}r}
000 & 0 \\
001 & 1 \\
010 & 2 \\
011 & 3 \\
100 & 4 \\
101 & 5 \\
110 & 6 \\
111 & 7
\end{array}
$$
N = 8 -> Byte

$[0; \,2^8 - 1]$
$[0; \,255]$

