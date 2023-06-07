```ad-summary 
title:Binomial Distribution

With parameters $n$ and $p$ is the discrete probability distribution of the number of successes in a sequence of $n$ independent experiments. (Multiple coin tosses)
```

# [[Probability Mass Function (PMF)]]

Let the random variable $X$, $X$ follows the binomial distribution with parameters $n \in \mathbb{N}$ and $p \in  [0,1]$ , we write $X\sim B(n,p)$. The probability of getting exactly $k$ successes in $n$ independent Bernoulli trials is given by the PMF:

$$
P(X=k)=\begin{pmatrix}n \\ k\end{pmatrix}
p^{k}(1-p)^{n-k}
$$
for $k=0,1,2,\dots,n$ where:
$$
\begin{pmatrix}n \\ k\end{pmatrix}
=
\frac{n!}{k!(n-k)!}
$$
$k$ successes occur with probability $p^{k}$ and $n-k$ failures occur with probability $(1-p)^{n-k}$. However, the $k$ successes can occur anywhere among the $n$ trials, and there are $\begin{pmatrix}n \\ k\end{pmatrix}$ different ways of distributing $k$ successes in a sequence of $n$ trials.
