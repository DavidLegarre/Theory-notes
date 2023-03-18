# RSA
## Keygen
* Choose two distinct prime numbers $p$ and $q$ (These are kept secre)
* Compute $n=pq$. $n$ will be used as the modulus for both
* Chose an integer $e\ s.t.\ e\in\mathbb{Z}_{\phi(n)}^*$ 
* Then calculate $d\equiv e^{-1}\mod\phi(n)$ 

 Then we now have:
 1. Public key as: $P_{k}=(n,e)$
 2. Secret key as: $S_{k}=d$

## Encryption 
$$
E_{pk}(m)\to c=m^{e}\mod n
$$
## Decryption
$$
D_{sk}(c)\to m=c^{d}\mod n
$$

![[Pasted image 20230317173414.png]]

# Encryption schema properties

1. **Efficient algorithms**: keygen ([[Euclidean Algorithm|E.E.A]]), $E_{pk},D_{sk}$([[Modular arithmetic#Modular exponentiation|modular exponentiation]]) 
2. **Correctness**: $D_{sk}(E_{pk}(m))=(m^e)^d=m$ 
3. **Security**:
	1. Need to factorize $N$
	2. Deterministic: weak to [[CPA]]
	3. Malleable: no [[CCA]] secure. A change in $c$ returns a change in $m$.

## RSA Signatures

In order to show authentication, the user who wants to prove it's authentication will publish an RSA scheme with it's public key, and then send this message $(m,m^{d}=\sigma)$, 
since $d$ is the secret key if we then perform $\sigma^{e}=m^{ed}=m'$, we then check if $m=m'$ if this holds then we received a message from the user with the private key to this RSA scheme, if not it is false.

# RSA OAEP

Optical Asymmetric Encryption Padding (OAEP) done in order to avoid malleability in the message, hiding the original message from the ciphertext inside a hash. 

First, let's define two hash functions:
$$
\begin{align*}
&G:\{0,1\}^{k_{0}}\to\{0,1\}^{k_{1+l}}\\
&H:\{0,1\}^{k_{i+l}}\to\{0,1\}^{k_{0}}
\end{align*}
$$

( They are not related, i.e. let $x\in\{0,1\}^{k_{0}},$ $x\not=H(G(x))$ )

## Encryption

1. Let $r\in\{0,1\}^{k_{0}}$ 
2. Then, add padding to the left side of the message of size $k_{1}$ so that
   $$
   m'=\{0\}^{k_{1}}||m
$$
3.  Then, let $s=G(r)\oplus(m')$ 
4.  Then, $t=H(s)\oplus r$ 
5.  $\hat{m}=(t||s)$
6. $\hat{c}=\hat{m}^{e}$

## Decryption

1. $\hat{m}=\hat{c}^{d}$
2. $\hat{m}=(t||s)$
3. $r=H(s)\oplus t$
4. $m'=G(r)\oplus s$
5. $m\gets0||m$

![[Pasted image 20230318211046.png]]
