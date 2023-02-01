![[Pasted image 20230114221221.png]]

The main parts of an encryption are defined as:
* $m$ (message): The content Alice (A) wants to encrypt and send to Bob (B)
* $c$ (ciphertext): The text that hides $m$
* $k$ (secret key): The secret key used to encrypt the message

A **symmetric-key encryption (SKE) scheme** consists of the following algorithms:

* **KeyGen**: a randomized algorithm that outputs a **key** $k\in \mathcal{K}$
* **Enc**: a (possibly randomized) algorithm that takes a key $k\in \mathcal{K}$ and **plaintext** $m\in \mathcal{M}$ as input and outputs a **ciphertext** $c\in \mathcal{C}$
* **Dec**: a deterministic algorithm that takes a key $k\in \mathcal{K}$ and ciphertext $c\in \mathcal{C}$ as input, and outputs a plaintext $m\in \mathcal{M}$.

We call $\mathcal{K}$ the **key space**, $\mathcal{M}$ the **message space**, and $\mathcal{C}$ the **ciphertext space** of the scheme. Sometimes we refer to the entire scheme (the collection of all three algorithms) by a single variable $\Sigma$. When we do so, we write $\Sigma$.KeyGen, $\Sigma$.Enc, … to refer to its components


## Correctness:

An encryption scheme $\Sigma$ satisfies **correctness** if:

$$
\forall k\in\mathcal{K},m\in \mathcal{M}\quad P[\Sigma.Dec(k,\Sigma.Enc(k,m))=m]=1
$$


## Perfect secrecy
An encryption scheme has perfect secrecy when, for a uniformly random $k$, all ciphertexts $c$ and all pairs of messages $m_{0}, m_{1}$ follow:
$$
P(c=E_{k}(m_{0}))=P(c=E_{k}(m_{1}))
$$
This means that the ciphertext produced reveals absolutely no information about the underlying plaintext, besides its length. We formalize this by saying that, given a ciphertext and two messages, the ciphertext has the same probability of corresponding to each of the messages.
