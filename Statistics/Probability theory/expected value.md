# Expected value
```ad-summary 
title:Defintion 

In [[Probability theory]], the expected value (also called **mean**) is a generalization of the [[weighted average]]. Informally, the expected value is the [[arithmetic mean]] of a large number of independently selected outcomes of a [[random variable]].
```

The expected value of a random variable $X$ is often denoted by $E(X)$, $E[X]$, or $EX$.

## When the random variable has finitely many outcomes:

Consider a [[Random variables]] $X$ with a *finite* list of possible outcomes, each of which has 
probability $p_{1},\ldots,p_{k}$ of occurring. The **expectation** of $X$ is defined as:
$$
E[X]=x_{1}p_{1}+x_{2}p_{2}+\ldots+x_{k}p_{k}
$$

### When the random variable is a density:

Now, consider $X$ to have a [[probability density function]] given by a function $f$:
$$
E[X]=\int_{-\infty}^{\infty}xf(x)dx
$$
