```ad-summary 
title:Defintion 
The Chinese Remainder Theorem (C.R.T.) states that if one knows the remainders of an integer n by several other integers, the one can determine  uniquely the remainder of division of n by the product of these integers, under the condition that the divisors are pairwise coprime
```

## Statement

Let $n_{1},\ldots,n_{k} \in \mathbb{Z} > 1$, and let $N=n_{1}\cdot n_{2} \ldots n_{k-1} \cdot n_{k}$:

This theorem asserts that if all $n_{i}$ are pairwise coprime, and we have another set of integers as $a_{1},\ldots,a_{k}$ such that $\forall i,\ 0\leq a_{i}<n_{1}$, then there is only one integer $x$ such that $0\leq x<N$

This means that the following system has a solution:
$$
\begin{align*}
x&\equiv a_{1}\mod n_1\\
&\vdots\\
x&\equiv a_{k}\mod n_{k}
\end{align*}
$$
