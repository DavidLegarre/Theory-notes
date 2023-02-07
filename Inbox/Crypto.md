$$
\text{If}\quad gcd(a,n)=1\to\exists \alpha,\beta \therefore
\alpha a+\beta n=1
$$
$$
\alpha a\equiv 1\mod n
$$

## Totient function

Let $n\in \mathbb{N}$. Then:
$\text{If }n=p^{e}, \text{where}\ p\ \text{is a prime and }  e \in \mathbb{N}$
$$
\phi(n)=(p-1)p^{e-1}
$$
If $n=pq$, where $p,q$ are coprime, then:
$$
\phi(n)=\phi(p)\phi(q)
$$

## Euler's theorem
Let $\mathbb{Z}_{n}$ for some $n \in \mathbb{N}$, $n>1$. Then, $\forall a \in \mathbb{Z}_{n} : gcd(a,n)=1$
$$
a^{\phi(n)}\equiv 1\mod n
$$
Example: $3^{402}\mod 1000$
We know that $\phi(1000)=400\to 3^{400}\equiv 1\mod 1000$
$$
3^{402}=3^{400}3^{2}=9\mod 1000
$$

## Fermat's little Theorem
Let $p$ be a prime number. Then, $\forall x \in \mathbb{Z}$, we have that:
$$
x^{p-1}\equiv 1\mod p
$$

Example: $3^{1030}\mod 191$
$$
3^{1030}=3^{\phi(191)\alpha}·3^{\beta}=3^{\beta}\mod 191
$$
Since $\frac{1030}{190}=5, r=80$
$$
3^{\phi(191)·5}·3^{80}=3^{80}\mod 191
$$

## Modular exponenciation
To calculate $c=b^{e}\mod m$

Algorithm:

1. Set $c=1,e'=0$
2. Increase $e'$ by $1$
3. Set $c=(b·c)\mod m$
4. If $e'<e$, go to step $2$, else, $c$ contains the solution to $c\equiv b^{e}\mod m$

## Exercise 5
Compute the two least significant digits of $3^{47}$ (LSB)

This can be calculated as $3^{47}\mod 100$
With Euler's theorem, since $gcd(3,100)=1$
$$
3^{\phi(100)}\equiv1\mod 100
$$
Then:
$$
\begin{align*}
\phi(100)&=\phi(2^{2}·5^{2})=40\\
3^{\phi(100)}&=3^{40}\equiv1\mod 100\\
3^{40}·3^{7}&=3^{7}=87\mod 100
\end{align*}
$$



