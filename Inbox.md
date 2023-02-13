# RSA

## KeyGen

```ad-abstract
On input a security parameter $\lambda$, choose two uniformly random prime numbers $p,q$ of bitlength $\frac{\lambda}{2}$, and let $N=pq$. We will work in $\mathbb{Z}_{n}$, and call $N$ the RSA modulus. Choose $e \in \mathbb{Z}_{n}$ and compute:
$$
d \equiv e^{-1}\mod N
$$

In this case, the public key is:
$$
pk=(N,e)
$$
and the secret key:
$$
sk=d
$$
```

Notice that:
$$
\exists\ e^{-1}\to gcd(e,\varphi(N))=1
$$
So we need to make sure that $e$ is defined of the form
$$
\forall\ e=\varphi(N)\cdot k+1
$$

## Enc

```ad-abstract
Given a message $m \in \mathbb{Z}_{n}$, and the receiver's public key $(N,e)$, output a ciphertext
$$
m^{e}\mod N
$$
```

## Dec

```ad-abstract
Given a ciphertext $c$ and the secret key $d$, output:
$$
c^{d}\mod N
$$
```

# Correctness

Proof $D_{sk}(E_{pk}(m))=m$:

$$
\begin{align*}
c^{d}\mod N&=m^{ed}\mod N\\
&\overset{1}{=} m^{1+\varphi(N)}\mod N\\
&\overset{2}{=} m^{1}\cdot m^{\varphi(N)}\mod N\\
&= m\mod N
\end{align*}
$$
$1:$ Since $ed \equiv1\mod \varphi(N)\to ed=1+\varphi(N)\cdot k$, so we choose $k=1$
$2:$ By [[Modular arithmetic#Euler's theorem|Euler's theorem]] we know that $x^{\varphi(N)} \equiv 1\mod N$

**RSA is only used for key sharing**
