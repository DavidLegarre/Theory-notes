Connects to: [[Euclidean Algorithm]], [[Group Theory]], [[Chinese Remainder Theorem (C.R.T)]]

```toc
```

```ad-abstract
title:Definition
We write the set of integers as:

$$
\mathbb{Z}=\{\ldots,-2,-1,0,1,2,\ldots\}
$$

and the set of natural numbers (nonnegative integers) as:

$$
\mathbb{N}=\{0,1,2,\ldots\}
$$
```

## Divisibility

```ad-summary
title:Definition

Let $a$ and $b$ be integers with $b\not=0$. We say that $b$ *divides* $a$, or that $a$ is *divisible* by $b$ if:

$$
\exists\ c,\ a=bc
$$

We denote this relation as $b\mid a$ read as: "$b$ divides $a$". On the other hand $b\not\mid a$
```

``` ad-summary
title: Definition

A *common divisor* of two integers is $a$ and $b$ is a positive integer $d$ that divides both of them. The *greatest common divisor* $gcd$ of $a$ and $b$ is the largest positive integer $d$ $s.t.$ $d\mid a$ and $d\mid b$. 

$$
d=gcd(a)
$$
``` 

## Modular arithmetic

```ad-abstract
title:Definition
Let $a,n \in \mathbb{Z}$, with $n>0$. We define the remainder (or residue) of a *modulo n* as the remainder of the integer division of $a$ by $n$, denoted as:
<br><br>
$$
a\mod n
$$
```

```ad-abstract
title:Definition
We define the set of residue classes *mod n* as the set:
$$
\mathbb{Z}_{n}=\{0,1,\ldots,n-1\}
$$
```

The elements of $\mathbb{Z}_{n}$ can be viewed as the hours in a clock
![[Pasted image 20230207185515.png]]

## Properties modular arithmetic

```ad-abstract
title:Definition
Let $a,b,z \in \mathbb{Z}$, with $n>0$. Then:
$$
\begin{align*}
(a\mod n)+(b\mod n)&=(a+b)\mod n\\
(a\mod n)·(b\mod n)&= (a·b)\mod n\\
\text{If }b\geq0,\text{ then }(a\mod n)^{b}&= (a^{b})\mod n 
\end{align*}
$$
```

## Congruence

Given an integer $n>1$ called a **modulus**, two integers *a* and *b* are said to be **congruent** modulo *n*, if n is a divisor of their difference (if: $(a-b) mod\ n=0$). Represented as:
$$
a\equiv b\mod n
$$

We say that $a,b$ are *equivalent* in $mod\ n$ 

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


## Modular multiplicative inverse

```ad-abstract
title:Definition
Let $a,x \in \mathbb{Z}$, we say that $x$ is the modular 
multiplicative inverse if:
$$
ax\equiv1\mod n
$$
```

This $x$ is usually written as $a^{-1}$ to denote that it is the inverse of $a$. 

```ad-abstract
title:Definition
We then define the set of all posible inverse *modulo n* we can find as:

$$
\mathbb{Z}_{n}^{*}=\{\forall a \in \mathbb{Z}_{n}:gcd(a,n)=1\}
$$
```

**Remember**: To find the $gcd(a,n)$ we must apply [[Euclidean Algorithm]].

### Euler's Totient function

```ad-abstract
title:Definition
Let $n \in \mathbb{N}$. Then:
If $n=p^{e}$, where $p$ is a prime number and $e \in \mathbb{N}$:
$$
\varphi(n)=(p-1)p^{e-1}
$$
If $n=pq$, where $p,q$ are prime numbers, then:
$$
\varphi(n)=\varphi(n)\varphi(q)
$$
```

We then say that $\varphi(n)$ returns $|\mathbb{Z}_{n}^{*}|$

## Fermat's little Theorem

```ad-abstract
title:Defintion
Let $p$ be a prime number. Then, $\forall x \in \mathbb{Z}$, we have that:
$$
a^{p-1}\equiv1\mod p
$$
```

### Example: $3^{1030}\mod191$

Since $191$ is prime, we can apply Fermat's little Theorem and we know that 
$$
3^{190}\equiv1\mod191
$$
Then if we calculated $1030/191$ we obtain:
$$
1030=190·5+80
$$
So we can rewrite the expression as:
$$
\begin{align*}
3^{1030}&= 3^{190·5+80}\\
&= (3^{190})^{5}·3^{80}\\
&= 1^{5}·3^{80}\\
&= 3^{80}\mod191
\end{align*}
$$
Now we could simplify even more with [[Modular arithmetic#Example|Modular Exponentiation]]

## Euler's theorem

This theorem is a generalization of [[Modular arithmetic#Fermat's little Theorem|Fermat's little Theorem]]

```ad-abstract
title:Definition
Let $\mathbb{Z}_{n}$ for some $n \in \mathbb{N}$, $n>1$. Then $\forall a\in\mathbb{Z}_{n}:\gcd(a,n)=1$:
$$
a^{\varphi(n)}\equiv1\mod n
$$
```

### Example: $3^{402}\mod1000$

We know that $\varphi(1000)=400\iff3^{400}\equiv1\mod1000$

Then we can calculate $3^{402}\mod1000$ as:
$$
\begin{align*}
3^{402}&=3^{400}·3^{2}\\
&\overset{1}{=} 1·3^{2}\\
&= 9\mod1000
\end{align*}
$$
$1:3^{400}\equiv1\mod1000$

## Modular exponentiation

Let $c=1,b,e \in \mathbb{Z}$ and $n \in \mathbb{N}$ then to calculate $c=b^{e}\mod n$:
1. Compute $\lfloor \frac{e}{2}\rfloor$ until $e=1$ every time $e$ is odd take note and save it as a chain
2. Then for each step in this chain do: 
$$
\begin{cases}
c=b^{2}\mod n\quad \text{if }e_{i}\text{ is even} \\
c=c^{2}·b\mod n\quad \text{if }e_{i}\text{ is odd}
\end{cases}   
$$
3. Recover the chain until $e_{i}=e$
## Example $4^{400}\mod15$

Let $c=1,b=4,e=400,n=15$

1. Generate the chain:
$$
400\overset{+0}{\gets}
200\overset{+0}{\gets}
100\overset{+0}{\gets}
50\overset{+0}{\gets}
25\overset{+0}{\gets}
12\overset{+1}{\gets}
6\overset{+0}{\gets}
3\overset{+1}{\gets}
1
$$
2. Calculate "up the chain"
$$
\begin{align*}
1&:4^{2}\equiv1\mod15\\
3&:1^{2}·4\equiv4\mod15\\
6&:4^2\equiv1\mod15\\
12&:1^{2}\equiv1\mod15\\
25&:1^{2}·4\equiv4\mod15\\
50&:4^{2}\equiv1\mod15\\
100&:1^{2}\equiv1\mod15\\
200&:1^{2}\equiv1\mod15\\
400&:1^{2}\equiv1\mod15
\end{align*}
$$
$\therefore 4^{400}\equiv1\mod15$

## Binary Formula

To calculate $a^{b}=\mod n$:

1. Write the exponent $b$ into powers of 2 by writing it in binary, obtaining 
$$
(b)_{2}=(d_{k-1},d_{k-2},\ldots, d_{1},d_{0})
$$
2. Then from the left to right:
$$
\begin{align*}
d_{k-1}:c_{1}&\equiv c_{0}^{2}·a^{d_{k-1}}\mod n\\
d_{k-2}:c_{2}&\equiv c_{1}^{2}·a^{d_{k-2}}\mod n\\
\vdots\\
d_{1}: c_{k-1}&\equiv c_{k-2}^{2}·a^{d_{1}}\mod n\\\\
d_{0}:c_{k}&\equiv c_{k-1}^{2}·a^{d_{0}}\mod n
\end{align*}
$$
## How to convert a number in base 10 to binary easy

Example

| Dividend  | Remainder |
| --------- | --------- |
| $80/2=40$ | $0$         |
| $40/2=20$ | $0$         |
| $20/2=10$ | $0$         |
| $10/2=5$  | $0$         |
| $5/2=2$   | $1$         |
| $2/2=1$   | $0$       |
| $1/2=0$   | $1$          |

By taking the remainder column and write it from bottom to top we obtain

$$
(80)_{2}=1010000
$$

### Example

$3^{80}\mod 191$

Convert exponent to binary:
$$
(80)_{2}=1010000
$$
| $(80)_{2}$ | $c_{0}=1$                                        |
| ---------- | ------------------------------------------------ |
| 1          | $c_{1}\equiv1^{2}·3^{1}=1·3\equiv3\mod191$            |
| 0          | $c_{2}\equiv3^{2}·3^{0}=9·1\equiv9\mod191$            |
| 1          | $c_{3}\equiv9^{2}·3^{1}=81·3=243\equiv52\mod191$ |
| 0          | $c_{4}\equiv52^{2}·3^{0}=2704\equiv30\mod191$         |
| 0          | $c_{5}\equiv30^{2}·3^{0}=900\equiv136\mod191$         |
| 0          | $c_{6}\equiv136^{2}·3^0=(-55)^{2}·1=3025\equiv160\mod191$    |
| 0          | $c_{7}\equiv160^{2}·3^{0}=(-31)^{2}·1=961\equiv6\mod191$|
