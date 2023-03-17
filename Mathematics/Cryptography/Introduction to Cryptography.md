Tools: [[Modular arithmetic]]

```toc
```

## Fundamental Security Principles

1. **Security depends on the resources of the attacker**: We say that a cryptographic scheme is secure if there are not efficient attacks
2. **Kerckhoffs' principle**: Design the your system so that it is secure even if the attacker knows all of its algorithms
3. **Security is impossible without randomness**

## Security Parameter

The way to achieve this is through a natural number that we call the _security parameter_, usually denoted by $\lambda$. The information about both security and efficiency will be expressed in terms of the security parameter.

### Security Level 

```ad-abstract
A cryptographic scheme has $n$-bit security if the best known attack requires $2^n$ steps. When the best known attack is a brute-force attack, then $n=\lambda$.
```

To calculate the bits of security of a scheme, Let $N$ be the number of steps of the best known attack and $\lambda$ the security parameter
$$
\lambda=\log_{2}(N)
$$
Brute force case:
$$
\begin{align*}
\lambda&= \log_{2}(N)\\
&= \log_{2}(2^{n})\\
&= n\\
\lambda&= n
\end{align*}
$$
## Confusion and Diffusion

```ad-abstract
title:Confusion
**Confusion**: each bit of the ciphertext depends on several parts of the key. In the other words, the relation between key and ciphertext must not be clear to any attacker
```

```ad-abstract
title: Diffusion
Small changes in the plaintext result in significant changes in the 
ciphertext. More precisely, in any modern block cipher, it is expected that a single bit change in the plaintext should result in at least half of the bits of the ciphertext changing.
```

## Basic parts of a Scheme

The main parts of an encryption scheme are defined as:
* $m$ (message): The content Alice (A) wants to encrypt and send to Bob (B)
* $c$ (ciphertext): The text that hides $m$
* $k$ (secret key): The secret key used to encrypt the message

All encryption schemes consist of the following algorithms:

* **KeyGen**: a randomized algorithm that outputs a **key** $k\in \mathcal{K}$
* **Enc**: a (possibly randomized) algorithm that takes a key $k\in \mathcal{K}$ and **plaintext** $m\in \mathcal{M}$ as input and outputs a **ciphertext** $c\in \mathcal{C}$
* **Dec**: a deterministic algorithm that takes a key $k\in \mathcal{K}$ and ciphertext $c\in \mathcal{C}$ as input, and outputs a plaintext $m\in \mathcal{M}$.

We call $\mathcal{K}$ the **key space**, $\mathcal{M}$ the **message space**, and $\mathcal{C}$ the **ciphertext space** of the scheme. Sometimes we refer to the entire scheme (the collection of all three algorithms) by a single variable $\Sigma$. When we do so, we write $\Sigma$.KeyGen, $\Sigma$.Enc, … to refer to its components

### Correctness:

All encryption scheme $\Sigma$ must satisfy correctness:

$$
\forall\  k \in \mathcal{K},\ m \in \mathcal{M}\quad
P[\Sigma.Dec_{k}(\Sigma.Enc_{k}(m))=m]=1
$$
### Perfect Secrecy

A non necessary condition, we say that an encryption scheme has perfect secrecy when:
Let $\forall k \in \mathcal{K},\forall c \in \mathcal{C},\forall m_{0},m_{1}\in \mathcal{M}\quad$:
$$
P[c=E_{k}(m_{0})]=P[c=E_{k}(m_{1})]
$$
or

$$
P(m|\mathcal{C}=c)=P(m)
$$

This means that the ciphertext produced does not provide any information about the original message, and that ciphertext was equally likely to come from any message.

## Security

* [[CPA and CCA Security]]

## Types of Encryption

 * [[Symmetric Encryption]]

## Encryption Schemes

* [[Shift cipher (Caesar's)]]
* [[One-Time-Pad]]
* [[Block Ciphers]]
