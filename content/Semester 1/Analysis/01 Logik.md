## Disjunktion (ODER)
---
- Aussage $A \vee B$ ist wahr, wenn einer oder beide der Aussagen wahr sind

| $A$ | $B$ | $A \vee A$ |
| --- | --- | ---------- |
| F   | F   | F          |
| F   | W   | W          |
| W   | F   | W          |
| W   | W   | W          |
- Es handelt sich hierbei um ein inklusives Oder
### Beispiel
---
$A:\quad 2 + 2 = 4$
$B:\quad 2 + 2 = 5$
$\Rightarrow$ Aussage $A \vee B$ ist wahr

$C: 4 + 2 = 1$
$D: 9 + 2 = 4$
$\Rightarrow$ Aussage $C \vee D$ ist falsh

## Konjunktion (UND)
---
- Aussage $A \wedge B$ ist wahr, wenn beide Aussagen wahr sind

| $A$ | $B$ | $A \wedge B$ |
| --- | --- | ------------ |
| F   | F   | F            |
| F   | W   | F            |
| W   | F   | F            |
| W   | W   | W            |

### Beispiel
---
$A: 2 + 3 = 5$
$B : 5 + 3 = 8$
$\Rightarrow$ Aussage $A \wedge B$ ist wahr

$C: 3 + 4 = 7$
$D: 9 + 9 = 3$
$\Rightarrow$ Aussage $C \wedge D$ ist falsch

## Negation (NICHT)
---
- invertiert die Aussage

| $A$ | $\overline{A}$ | $\overline{\overline{A}}$ |
| --- | -------------- | ------------------------- |
| F   | W              | F                         |
| W   | F              | W                         |

### Beispiel
---
$A: 4 + 3 = 4$
$B: 2 + 4 = 6$
$\Rightarrow$ Aussage $\overline{A \wedge B}$ ist wahr

$C: 9 + 2 = 11$
$D: 3 + 11 = 14$
$\Rightarrow$ Aussage $\overline{C \wedge D}$ ist falsch

## Implikation (Folgt)
---
- A impliziert B
- Wenn A dann B
- A ist hinreichend für B
- B ist notwendig für A

| $A$ | $B$ | $A \Rightarrow B$ |
| --- | --- | ----------------- |
| F   | F   | W                 |
| F   | W   | W                 |
| W   | F   | F                 |
| W   | W   | W                 |
- Die Aussage ist wahr, wenn B wahr ist, unabhängig von A
### Beispiel
---
$A: 2 + 2 = 5 \Rightarrow$ falsch
$B: 3 + 4 = 2 \Rightarrow$ falsch

Aussage $A \Rightarrow B$ ist wahr

$C: 4 + 2 = 6 \Rightarrow$ wahr
$D: 4 + 15 = 8 \Rightarrow$ falsch

Aussage $C \Rightarrow D$ ist falsch

> [!NOTE] Satz 1.1
>Äquivalente Aussagen:
>
>$A \Rightarrow B$
>
>$\overline{A} \vee B$
>
>$\overline{B} \Rightarrow \overline{A}$

| $A$ | $B$ | $\overline{A}$ | $\overline{B}$ | $A \Rightarrow B$ | $\overline{A} \vee B$ | $\overline{B} \Rightarrow \overline{A}$ |
| --- | --- | -------------- | -------------- | ----------------- | --------------------- | --------------------------------------- |
| F   | F   | W              | W              | W                 | W                     | W                                       |
| F   | W   | W              | F              | W                 | W                     | W                                       |
| W   | F   | F              | W              | F                 | F                     | F                                       |
| W   | W   | F              | F              | W                 | W                     | W                                       |

### Kontraposition vs Negation vs Umkehrung
---
#### Kontraposition
---
$\overline{B} \Rightarrow \overline{A}$ ist gleichwertig mit $A \Rightarrow B$

#### Negation
---
$\overline{A \Rightarrow B}$ verneint die Aussage

#### Umkehrung
---
$B \Rightarrow A$ weder gleichwertig mit Kontraposition noch der Negation

## Äquivalenz
---
- $A$ gilt, wenn $B$ gilt

| $A$ | $B$ | $A \Leftrightarrow B$ | $A \Rightarrow B$ | $B \Rightarrow A$ | ($A \Rightarrow B$) $\wedge$ ($B \Rightarrow A$) |
| --- | --- | --------------------- | ----------------- | ----------------- | ------------------------------------------------ |
| F   | F   | W                     | W                 | W                 | W                                                |
| F   | W   | F                     | W                 | F                 | F                                                |
| W   | F   | F                     | F                 | W                 | F                                                |
| W   | W   | W                     | W                 | W                 | W                                                |

> [!NOTE] Satz 1.2
> Äquivalente Aussagen:
> 
> $A \Leftrightarrow B$
> 
> ($A \Rightarrow B$) $\wedge$ ($B \Rightarrow A$)
### Beispiel
---
$n \in \mathbb{N}$ ist genau dann eine gerade Zahl, wenn $n$ durch 2 teilbar ist
## Allaussagen (für alle)
---
**Allquantor** $\forall$ "für alle"

### Beispiel
---
$\forall x \in \mathbb{R} \setminus \{0\}: x^2 \gt 0$

## Existenzaussagen (es gibt)
---
**Existenzquantor** $\exists$ "es gibt/ex existiert"

### Beispiel
---
$\exists x \in \mathbb{Z}: x^2 = 4$

## Negation von Allaussagen und Existenzaussagen
---
$\overline{\forall x: A(x)} \Leftrightarrow \exists x: \overline{(A(x))}$
$\overline{(\forall x: A(x))} \Leftrightarrow \exists x: \overline{(A(x))}$

$\overline{\exists: A(x)} \Leftrightarrow \forall x: \overline{A(x)}$

$Aussage$: "Es gibt ein Schneckenhaus, das gegen den Uhrzeigersinn gedreht ist"

$\overline{Aussage}$: "Alle Schneckenhäuser, sind nicht gegen den Uhrzeigersinn gedreht"

<hr>

<div style="display: flex; justify-content: space-between;">

  <a href="Semester 1/Analysis">← Zurück</a>

  <!--<a href="">Weiter →</a>-->

</div>