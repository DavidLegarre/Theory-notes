![[Pasted image 20230114221221.png]]

A **symmetric-key encryption (SKE) scheme** consists of the following algorithms:

* **KeyGen**: a randomized algorithm that outputs a **key** $k\in \mathcal{K}$
* **Enc**: a (possibly randomized) algorithm that takes a key $k\in \mathcal{K}$ and **plaintext** $m\in \mathcal{M}$ as input and outputs a **ciphertext** $c\in \mathcal{C}$
* **Dec**: a deterministic algorithm that takes a key $k\in \mathcal{K}$ and ciphertext $c\in \mathcal{C}$ as input, and outputs a plaintext $m\in \mathcal{M}$.

We call $\mathcal{K}$ the **key space**, $\mathcal{M}$ the **message space**, and $\mathcal{C}$ the **ciphertext space** of the scheme. Sometimes we refer to the entire scheme (the collection of all three algorithms) by a single variable $\Sigma$. When we do so, we write $\Sigma$.KeyGen, $\Sigma$.Enc, … to refer to its components