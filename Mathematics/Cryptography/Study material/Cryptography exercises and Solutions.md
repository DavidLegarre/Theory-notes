```toc
```
## Exercise 2 PS1

The codes of three subjects are $LA,CS,\text{ and }DS$. We only encrypt the codes of these subjects ($\mathcal{M}=\{LA,CS,DS\}$) and we use a shift cipher to do it. Compute the probability that $C=GV$ if, according to the number of enrolments, it is considered the following distribution over $\mathcal{M}$
$$
P[M=LA]=0.5,\ P[M=DS]=0.2,\ P[M=CS]=0.3
$$
What is the probability that $DS$ is the plaintext if we observe $GV$ as the encrypted message? Does the scheme have perfect secrecy?

### Solution

Uses a substitution cipher:
$$
Enc_{k}=m+k\mod 26
$$
Question: $P(M=DS|C=GV)$

By [[Bayes' Theorem]]:
$$
P(M=DS|C=GV)=
\frac{P(C=GV|M=DS)P(M=DS)}{P(C=GV)}
$$
We know that:
$$
P(C=GV|M=DS)=
\frac{1}{26}
$$

Since, only one $k$ can move $DS\to GV\mod 26$ and since $m,k$ both lie in $\mathbb{Z}_{26}$ no matter the value of $k$ as long as it is a multiple of the value that holds $E_{k}(DS)=GV$ in this case $k=3$

To Calculate $P(C=GV)$ , since from $\mathcal{M}$ we can only obtain $C=GV$ when $m \in\{LA,DS\}$  we can:

$$
\begin{align*}
P(C=GV)&=\Sigma_{k \in \mathcal{K}}^{}\ P(C=GV,k) \\
&= P(C=GV,k=3)+P(C=GV,k=21)\\
&= P(m=LA)\cdot \frac{1}{26}+P(m=DS)\cdot \frac{1}{26}\\
&= [P(m=LA)+P(m=DS)]\cdot \frac{1}{26}\\
&= [0.5+0.2]\cdot \frac{1}{26}\\
&= \frac{7}{260}
\end{align*}
$$

Then we have that:

$$
\begin{align*}
P(M=DS|C=GV)&= \frac{P(C=GV|M=DS)P(M=DS)}{P(C=GV)}\\
&= \frac{\frac{1}{26}\cdot0.2}{\frac{7}{260}}\\
&= \frac{2}{7}
\end{align*}
$$

Since $P(M=DS|C=GV)\not=P(M=DS)$ the schema has no perfect secrecy

## 
