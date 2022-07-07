# Modular arithmetic
![[Pasted image 20220604213817.png]]

## Congruence
Given an integer $n>1$ called a **modulus**, two integers *a* and *b* are said to be **congruent** modulo *n*, if n is a divisor of their difference (if: $(a-b) mod\ n=0$). Represented as
$$
a\equiv B\mod n
$$
### Properties
$$
\begin{aligned}
a\equiv c\mod n\\
b\equiv d\mod n
\end{aligned}
\begin{cases} 
\begin{aligned} 
a\pm b&\equiv c\pm d&\mod n \\
a\cdot b&\equiv c\cdot d&\mod n \\
a^{k}&\equiv c^{k}&\mod n&,\ k\geq0
\end{aligned}
\end{cases}
$$
## Inverse
We then define the set of residue classes *modulo* *n* as the set:
$$
\mathbb{Z}_{n}=\{0,1,\dots,n-1\} 
$$
The inverse of a number modulo *n* is defined as:
$$
\begin{aligned}
ab&\equiv1&\mod n\\
b&=a^{-1}&\mod n
\end{aligned}
$$
We can calculate the inverse by using the [[Euclidean Algorithm]].

We then define inverse  set of *n* as;
$$
\mathbb{Z}^{*}_{n}=\{a\in\mathbb{Z}_{n}, s.t.\ \gcd(a,n)=1\}
$$

### Euler's Totient function
We define the function $\varphi$ that returns the size of $\mathbb{Z}^{*}_{n}$ 
$$
\begin{cases}
\varphi(p)=p-1 \\
\varphi(p\cdot q)=\varphi(p)\varphi(q) \\
\varphi(p^d)=\varphi(p)p^{d-1}
\end{cases}
$$
Where, $p$ and $q$ are said to be prime numbers and $d$ an integer.

### Euler's theorem
$$
\begin{aligned}
\forall a\in\mathbb{Z}_{n}\ s.t.\ \gcd(a,n)=1\\
a^{\varphi(n)}\equiv1\mod n
\end{aligned}
$$
## Modular exponentiation

To calculate large exponents (e.g. $4^{400}\mod 15$) we must use the modular exponentiation method.
Let, $a^{b}\mod n$ then:
* compute $\lfloor{\frac{b}{2}}\rfloor$ until $b=1$

E.g. $4^{400}\mod 15$
![[Pasted image 20220604232859.png]]
$$4^{400}\equiv 1\mod 15$$
