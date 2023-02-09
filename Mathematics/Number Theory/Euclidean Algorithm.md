# Euclidean Algorithm

Connects to: [[Modular arithmetic]], [[Computer Science/Algorithms/Algorithms]]
Examples: [[Example Euclidean Algorithm]]

```ad-note
title: Theorem (The Euclidean Algorithm)

Let $a$ and $b$ be positive integers with $a\leq b$ . The following algorithm computes $gcd(a,b)$ in a finite number of steps.

1. Let $r_{0}=a$ and $r_{1}=b$
2. Set $i=1$
3. Divide $r_{i-1}$ by $r_{i}$ to get a quotient $q_i$ and remainder $r_{i+1}$
$$
\begin{align*}
	r_{i-1}=r_{i}·q_{i}+r_{i+1}\quad \text{with } 0\leq r_{i+1}<r_{i}
\end{align*}   
$$
4. If the remainder $r_{i+1}=0$, then $r_{i}=gcd(a,b)$ and the algorithm ends
5. Otherwise, $r_{i+1}>0$, so set $i=i+1$ and repeat step $3$
```

```ad-abstract
title: Proposition
Let $d=gcd(a,b)$:
$$
\forall x,y \in \mathbb{Z}:d\mid ax+by
$$
```


# Extended Euclidean Algorithm (EEA)

``` ad-note
title: Theorem (EEA)

Let $a$ and $b$ be positive integers. Then the equation
$$
ax+by=gcd(a,b)
$$

Always has a solution for the integers $x$ and $y$.
```

![[Pasted image 20230119190513.png]]