# Permutations

A permutation of a set is an ordering of the set

> A permutation is an ordered combination

## Permutations with repetition

When we have a set of size $n$ and we want subset of size $r$, in this case we have $n$ choices to make $r$ times. We then know that the number of permutations is calculated with:

$$
n^r
$$
## Permutations without repetition

In this case, after each choice we have one element less. So, then the formula is 
$$\frac{n!}{(n-r)!}$$
Since, at the beginning we have $n$ choices but after that we have one less, up until $r$.
With $n=4$ and $r=2$:
$$
\frac{4!}{(4-2)!}=\frac{4!}{2!}=\frac{4*(4-1)*(4-2)*(4-3)}{2*(2-1)}
=\frac{4*3*2*1}{2*1}=\frac{4*3*\cancel{2*1}}{\cancel{2*1}}=4*3
$$
To avoid using this formula we use the notation:
$$
P(n,r)={}^nP_r={}_nP_r=\frac{n!}{(n-r)!}
$$


# Combinations
Combinations are ways to determine the number of possible arrangements in a collection of items, but where the order does not matter.

## Combinations without repetition

Similarly to permutations without repetition, but since in this case we don't care about order, we must **reduce** the number of possibilities, we will reduce this by taking into account the number of permutations for our set of size $r$ and divide by that, so:
$$
\frac{n!}{(n-r)!}* \frac{1}{r!}= \frac{n!}{r!(n-r)!}
$$
In this case we follow the notation:
$$
C(n,r)= {}^{n}C_{r}={}_nC_r=
\begin{pmatrix}n\\r\end{pmatrix}= \frac{n!}{r!(n-r)!}
$$

