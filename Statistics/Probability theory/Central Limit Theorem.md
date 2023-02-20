```ad-summary 
title:Defintion 
In [[Probability Theory]] the **central limit theorem (CLT)** establishes 
that, in many situations, for indetically distributed independent samples, 
the standardized sample mean tends towards the standard normal distribution even if the original variables themselves are not normally distributed
```

![[Pasted image 20230220173223.png]]


Let $\{X_{1},\ldots,X_{n}\}$ be a sequence of random samples, that is, a sequence of i.i.d random variables drawn from a distribution of expected value given by $\mu$ and finite variance given by $\sigma^{2}$. Suppose we are interested in the sample average:
$$
\overline{X}_{n}\equiv \frac{X_{1}+\ldots+X_{n}}{n} 
$$
The classical central limit theorem states that as $n$ gets larger, the distribution of the difference between the sample average $\overline{X}_{n}$ and its limit $\mu$, when multiplied by the factor $\sqrt{n}$ approximates the normal distribution with mean $0$ and variance $\sigma^{2}$.

```ad-summary 
title:Classical CLT
Suppose $\{X_{1},\ldots,X_{n},\ldots\}$ is a sequence of i.i.d random varibles with $\mathbb{E}[X_{i}]=\mu$ and $Var[X_{i}]=\sigma^{2}<\infty$. Then as $n$ approaches infinity, the random variables $\sqrt{n}(\overline{X}_{n}-\mu)$ converge in distribution to a normal $\mathcal{N}(0,\sigma^{2})$:
$$
\sqrt{n}(\overline{X}_{n}-\mu)\to \mathcal{N}(0,\sigma^{2})
$$
```
