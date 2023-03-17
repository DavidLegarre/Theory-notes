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
