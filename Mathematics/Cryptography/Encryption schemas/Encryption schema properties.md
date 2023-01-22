# Encryption schema properties
An encryption schema is composed by three [[Computer Science/Algorithms/Algorithms|algorithms]]: KeyGen, Enc, and Dec:
$$
\begin{align*}
m&\underset{Enc_{k}}{\to}c\\
c&\underset{Dec_{k'}}{\to}m
\end{align*}
$$
Remember that c is the ***ciphertext*** and m is the **message**.  A encryption schema must follow
* **Correctness**: It must hold that $\forall m,k\ D_{k}(E_{k}(m))=m$ 
* **Efficient**: Time complexity of both $E_{k}$ and $D_{k}$ must be [[Efficient Algorithms|efficient]].
* **Secure**:
	- It must be complex to predict $m\leftarrow c$ without $k$. Even if the Kerckhoff's principle holds
	- Randomness:
		- [[CPA]] secure ([[Symmetric Encryption#Perfect secrecy|Perfect secrecy]] holds )
	* Is secure against maleability: [[CCA]] secure

## Types of encryption schema
* [[Elgamal]]
* [[RSA]]
