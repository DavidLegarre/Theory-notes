# Secret sharing
Protocol to share keys between multiple people
$$
(n,t)
$$
Where $n$ is the total number of people to be shared the key with, and $t$ is the minimum amount of people that must be at the same time to recover the secret key. So, $t<n$ must always hold. 
Each member also has assigned a value $s$ 

## Recovering secret key
To recover the secret key, we must evaluate the polynomial formed by the **Lagrange polynomials** and evaluate them at $0$. Also, given a private value $p$.

**Lagrange polynomials**: 
$$
\lambda_{i}^{i,j}(x)=\prod
_{i,j\in I\ i\not=j}
\frac{x-j}{i-j}
$$

Final polynomial for the set of participants $\{1,2\}$ when $t=2$:
$$
s=s_1\lambda_{1}^{1,2}(0)+s_2\lambda_{2}^{1,2}(0)\mod p
$$

