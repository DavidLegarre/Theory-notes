# Algorithms
## Big-O notation

```ad-summary 
title:Defintion 

The Big-O notation is at its heart a mathematical notation, used to
to compare the rate of convergence of functions. Let $n\to f(n)$ and 
$n\to g(n)$ be functions defined over the natural numbers. Then we 
say that $f=O(g)$ if and only if there exists a constant A, such that 
for all $n, \frac{f(n)}{g(n)}\leq A$
```

Actually, the scope of the Big-O notation is a bit wider in mathematics but for 
simplicity I have narrowed it to what is used in algorithm complexity analysis: 
functions defined on the naturals, that have non-zero values, and the case of n
growing to infinity.

### Example

Let's take the case of $f(n)=100n^{2}+10n+1$ and $g(n)=n^{2}$. It is quite clear that both 
of these functions tend to infinity as n tends to infinity. But sometimes knowing the limit is not enough, and we also want to know the *speed* at which the functions approach their limit. Notions like Big-O help compare and classify functions by their speed of convergence. 

Let's find out if $if = O(g)$ by applying the definition. We have $\frac{f(n)}{g(n)}=100 + \frac{10}{n} + \frac{1}{n^{2}}$ Since $\frac{10}{n}$ is $10$ when $n=1$ and is decreasing, and since $\frac{1}{n^{2}}$ is 1 when $n=1$ and is also decreasing, we have $\frac{f(n)}{g(n)}\leq 100 + 10+1=111$. The definition is satisfied because we have found a bound of $\frac{f(n)}{g(n)}(111)$  and so $f=O(g)$ (we say that $f$ is a Big-O pf $n^{2}$).

This means that $f$ tends to infinity approximately the same speed as $g$. Now this may seem like a strange thing to say, because what we have found is that $f$ is at most $111$ times bigger than $g$, or in other words when $g$ grows by $1$, $f$ grows by at most $111$. It may seem that growing $111$ times faster is not "approximately the same speed". 

We don't need to separate functions that grow a fixed number of times faster than each other, but only functions that grow *infinitely* faster than each other. For instance if we take $h(n)=n^{2}*\log(n)$, we see that $\frac{h(n)}{g(n)}=\log(n)$ which tends to infinity with $n$ so $h$ is *not* $O(n^{2})$, because $h$ grows *infinitely* faster than $n^{2}$.

[[Simple Algorithms Complexity]]

## Efficient algorithms

``` ad-tldr
title: Definition.

An algorithm $\mathcal{A}$  is said to be *efficient* (or *polynomial-time*) if there exists a positive polynomial *p* such that, $\forall n\in\mathbb{N}$, when $\mathcal{A}$ receives an input of size *n*, it finishes in at most $p(n)$. 

```

