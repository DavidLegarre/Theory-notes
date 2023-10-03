# 0 Expectation and Variance

Expectation of a random variable is defined as:
$$
E[X]=\sum\limits_{i=1}^{\infty}x_{i}P(X=x)
$$
For discrete RV, and for continuous RV:
$$
E[X]=\int_{-\infty}^{\infty}xf(x)dx
$$
# 1 Law of Iterated Expectations

The law of iterated Expectations (LIE) states that:
$$
E[X]=E[E[X|Y]]
$$
The expected value of $X$ is equal to the expectation over the conditional Expectation of $X$ given $Y$.

## 1.1 Proof of LIE

First, we can express the expectation over conditional expectations as a weighted sum over all possible values of $Y$, and similarly express the conditional expectations using summation too:
$$
\begin{align*}
E[E[X|Y]]&=\sum\limits_{y}E[X|Y=y]P(Y=y)\\
&=\sum\limits_{y}\sum\limits_{x}xP(X=x|Y=y)P(Y=y)\\
&=\sum\limits_{y}\sum\limits_{x}xP(X=x)P(Y=y|X=x)\\
&=\sum\limits_{x}xP(X=x)\sum\limits_{y}P(Y=y|X=x)\\
&= \sum\limits_{x}xP(X=x)\\
&= E[X]
\end{align*}
$$

# 2 Law of Total Variance

The Law of Total Variance (LTV) states the following
$$
var[Y]=E[var[Y|X]]+var(E[Y|X])
$$
# 2.1 Proof of LTV

LTV can be proved almost immediately using LIE an the definition of variance:
$$
\begin{align*}
var(Y)&= E[Y^2]-E[Y]^2\\
&= E[E[Y^{2}|X]]-E[E[Y|X]]^{2}\\
&= E[var[Y|X]+E[Y]^{2}]-E[E[Y|X]]^{2}\\
&= E[var[Y|X]]+(E[E[Y]^{2}]-E[E[Y|X]]^{2})\\
&= E[var[Y|X]]+var(E[Y|X])
\end{align*}
$$

