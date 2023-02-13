## Diffie-Hellman

In every conversation the pair of players $(A,B)$ each one of them has a secret ($sk$) and a public key ($pk$) .

$pk_{a}$ is accessible to everybody, anybody can encrypt a message using using $pk_{a}$ but
in this case, to decrypt this cipher it is only possible with $sk_{a}$ that only $A$ has access 
to.

In order to establish a communication using DH method:
* $A$ send their $sk_{a}$ encrypted using $pk_{b}$ such as $c_{a}=E_{pk_{b}}(sk_{a})$ 
* $B$ decrypts this message as $D_{sk_{b}}(c_{a})$ and sends back $c_{b}=E_{pk_{a}}(sk_{b})$ 
Now $A,B$ have each others $sk$ and can now communicate by encrypting all of their messages with their respective public keys.

## RSA

* **KeyGen**: On input security parameter $\lambda$, choose two uniformly random prime numbers $p,q$ of bitlength $\lambda/2$ and let $N=pq$. We will work in $\mathbb{Z}_{n}$, and call $N$ and RSA modulus. Choose $e \in \mathbb{Z}_{n}$, and compute:
  $$
  d \equiv e^{-1}\mod \varphi(N)
$$
	notice that since $\exists\ e^{-1}\to gcd(e,\varphi(N))=1$ 
* **Public Key**:
  $$
  pk=(N,e)
$$
* **Secret Key**:
  $$
  sk=d
$$

