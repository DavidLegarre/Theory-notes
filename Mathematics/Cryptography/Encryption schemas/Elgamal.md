# ElGamal 
Connects to: [[Encryption schema properties]]

## Keygen

1. On an input security parameter $\lambda$, choose a cyclic group $G$ of prime order $p$, and a generator $g$ of $G$.  Choosing $p\ s.t.\ p=2q+1$ where $q$ is a prime number. 
2. With $|G|=q$
3. Sample $x\ s.t.\ x\in\mathbb{Z}_{n}^{*}$, then: $s_{k}=x$ and with $H=g^{x}$   then:  $p_{k}=(g,h)$ 

## Encryption

With a random $r\in\mathbb{Z}_{q}^{*}$

* **Classic**:
	* $c=(c_{0},c_{1})=(g^{r},m·h^{r})$
* **Lifted**:
	* $c=(c_{0},c_{1})=(g^{r}, g^{m}·h^{r})$

## Decryption 

* **Classic**:
$$
m=\frac{C_1}{C_{0}^{x}} 
= \frac{h^{r}·m}{(g^{r})^{x}}
= \frac{m·(g^{x})^{r}}{(g^{r})^{x}}
= m· \frac{g^{xr}}{g^{xr}}
= m
$$
* **Lifted**:
$$
m=\log_{g}\frac{c_1}{c_{0}^{x}}
=\log_{g} \frac{g^{m+xr}}{(g^{r})^{x}}
=\log_{g}g^{m}
= m
$$
# Security

- It is random, and $|G|=q$ is prime, so is [[CPA]] secure
- It is malleable ([[CCA]] unsafe) $\hat{c}(c_{0}^{2},c_{1}^{2})\to m^{2}$ 
- Complex to crack, we need to solve $\log_{g}(h)=x$ (hard problem)
 
