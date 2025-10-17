Wir können durch Bubble Pushing die Gatter so verändern, dass wir nur noch NAND- oder NOR-Gatter haben

## Disjunktive Normalform
---
### Als Term:
$$
\begin{aligned}
y &= \overline{\overline{(\overline{x_3} \wedge x_2 \wedge \overline{x_1}) \vee (\overline{x_3} \wedge x_2 \wedge x_1) \vee (x_3 \wedge \overline{x_2} \wedge x_1) \vee (x_3 \wedge x_2 \wedge \overline{x_1})}} \\\\

&= \overline{\overline{(\overline{x_3} \wedge x_2 \wedge \overline{x_1})} \wedge \overline{(\overline{x_3} \wedge x_2 \wedge x_1)} \wedge \overline{(x_3 \wedge \overline{x_2} \wedge x_1)} \wedge \overline{(x_3 \wedge x_2 \wedge \overline{x_1})}}
\end{aligned}
$$
### Als Schaltnetz:

![[disjunktive_schaltung_bubble_pushing.png]]

## Konjunktive Normalform
---
### Als Term:
$$
\begin{aligned}
y &= \overline{\overline{(\overline{x_3} \vee \overline{x_2} \vee \overline{x_1}) \wedge (\overline{x_3} \vee \overline{x_2} \vee x_1) \wedge (x_3 \vee \overline{x_2} \vee \overline{x_1}) \wedge (x_3 \vee x_2 \vee x_1)}} \\\\
&= \overline{\overline{(\overline{x_3} \vee \overline{x_2} \vee \overline{x_1})} \vee \overline{(\overline{x_3} \vee \overline{x_2} \vee x_1)} \vee \overline{(x_3 \vee \overline{x_2} \vee \overline{x_1})} \vee \overline{(x_3 \vee x_2 \vee x_1)}}
\end{aligned}
$$
### Als Schaltnetz:

![[konjunktive_schaltung_bubble_pushing.png]]

<hr>

<div style="display: flex; justify-content: space-between;">

  <a href="02 Zweistufige Schaltungsentwürfe">← Zurück</a>

  <a href="04 Minimierung durch benachbarte Einträge ">Weiter →</a>

</div>