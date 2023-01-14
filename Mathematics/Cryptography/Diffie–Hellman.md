# Diffie-Hellman
A key exchange protocol. With the following steps:

* On input $\lambda$, $A$ chooses a uniformly random prime number $p$ of bitlength $\lambda$, and determines a cyclic group of order $g$ of $G$.
* $A$ sends $(G,g)$ to $B$.
* $A$ chooses a uniformly random $a\in\mathbb{Z}_{p}$ and computes $A=g^{a}$, and sends $A$ to $B$. Similarly, $B$ chooses a uniformly random $b\in\mathbb{Z}_{p}$, computes $B=g^{b}$, and sends $B$ to $A$.
* Now the final key $K$ is defined as: $A^{b}=(g^{b})^{a}=B^{a}$ 

