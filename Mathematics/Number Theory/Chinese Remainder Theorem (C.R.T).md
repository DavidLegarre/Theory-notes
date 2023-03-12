```ad-summary 
title:Defintion 
For any given number $N \in \mathbb{Z}$ we know by the fundamental theorem 
of arithmetic that $N=n_{k}\cdot\ldots \cdot n_{k_{i}}$ where $n_{k_{i}}$ are prime numbers

Then, we know that there is a multiplicative isomorphism in 

$$
\mathbb{Z}_{n}\cong \mathbb{Z}_{n_{1}}\times \ldots \times \mathbb{Z}_{n_{2}}
$$

The C.R.T. States that when working inside the set $\mathbb{Z}_{n}$ we can work on it's decomposition to ease operations

```


$$
\begin{align*}
6&=2\cdot3\\
\mathbb{Z}_{6}&= \mathbb{Z}_{2}\times \mathbb{Z}_{3}
\end{align*}
$$
| $\mathbb{Z}_{6}$ | $\mathbb{Z}_{2}\cdot \mathbb{Z}_{3}$ |
| ---------------- | ------------------------------------ |
| $0$              | $(0,0)$                              |
| $1$              | $(1,1)$                              |
| $2$              | $(0,2)$                                |
| $3$              | $(1,0)$                                     |
| $4$              | $(0,1)$                                     |
| $5$              |      $(1,2)$                                |

In this case,
$$
\begin{align*}
0 \mod 6 \equiv& (0\mod 2,0\mod 3)\\
1\mod 6\equiv& (1\mod2,1\mod3)\\
2\mod6\equiv&(0\mod2,2\mod3)\\
3\mod6\equiv&(1\mod2,0\mod3)
\end{align*}
$$

# Example


![[Pasted image 20230310200850.png]]

Then to calculate this:

![[Pasted image 20230312171122.png]]

(-5 and 4 are found using [[Euclidean Algorithm#Extended Euclidean Algorithm (EEA)|Extended Euclidean Algorithm]])