# Negative modulo arithmetic
As part of [[Modular arithmetic]] in the case we need to calculate the negative modulo of a number, e.g.:
$$
-17\mod 10
$$
We need to calculate the remainder, to do so, we must find a negative value $q$ that would surpass the value $x$, and then, calculate the difference but in negative such that:
$$
\begin{align}
-17&=q\cdot10+r\\
-17&=-2\cdot10+r\\
-17&=-20+r\\
-17&=-20+3\\
-17&\mod10=3
\end{align}
$$
