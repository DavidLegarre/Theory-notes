```ad-summary 
title:Defintion 
Secret Sharing is a system to share secret messages only when a minimum number of participants is met. Let $n$ be the total number of participants and $t$ the threshold (minimum) number of participants needed to recover the secret shared
```

These method consists of two algorithms *sharing* and *reconstructing*

# Sharing algorithm

The idea is to hide the message inside a polynomial: 
Let $a_{1},\ldots,a_{t-1} \in \mathbb{Z}_{p}^{*}$ chosen uniformly and let $S$ be the secret.
$$
f(x)=S+a_{1}x+a_{2}x^{2}+\ldots+a_{t-1}x^{t-1}\mod p
$$
We then can find $S$ when evaluating $f(x)$ at $f(0)$ (by default, unless said otherwise).

Shamir:

For $i \in \{1,\ldots,n\}$ each user receives their secret as:
$$
s_{i}=(i,f(i)\mod p)
$$

Case: $n=t$

$$
S=S_{1}+\ldots+S_{n}
$$

# Reconstructing

## Shamir

Let $f(x)$, and $I$ the set of participants that shared the secret:
$$
f(x)=\sum\limits_{i \in I}a_{i}\delta_{i}(x)
$$

Where $\delta_{i}(x)$ is defined as:
$$
\delta_{i}(x)=\underset{j \in I\setminus i}{\Pi}\frac{x-j}{i-j}
$$
