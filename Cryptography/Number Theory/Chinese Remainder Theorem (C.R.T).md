# Chinese Remainder Theorem (C.R.T)
Let $a,b\in\mathbb{N}$ be coprime, and let $n=ab$. Then, for each $x\in\mathbb{Z}_{n}$, there exists a unique pair $(y,z)\in\mathbb{Z}_{a}\times\mathbb{Z}_{b}$ such that:
$$
\begin{align*}
x&\equiv y\mod a\\
x&\equiv z\mod b
\end{align*}
$$

Then we can recover $x$ as:
$$
x=by(b^{-1}\mod a)+az(a^{-1}\mod b)
$$
Then, in the case that all numbers are coprime between them. We can calculate the CRT as:

![[Pasted image 20220707183411.png]]


We need to use [[Euclidean Algorithm]]
