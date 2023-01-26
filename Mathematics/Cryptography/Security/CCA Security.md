```ad-abstract
title:Definition
A Chosen-cihpertext attack (CCA) is a type of attack that can be performed on a security scheme to try and see if there's a posibility that when a change is applied to a ciphertext see those same changes in the decrypted plaintext
```
## Malleability

```ad-abstract
title:Malleability
A scheme is said to be *malleable* if it is possible to modify a ciphertext and cause a *predictable change* to the plaintext.
```

## Steps of the attack

Start with the same steps as if it was a [[CPA Security|CPA]] attack.

After that:
1. The adversary sends a new ciphertext to the oracle (with this new cipher being different from $c_{b}$) and does so $l$ times. 
2. For each ciphertext sent the oracle returns the decrypted message.

## Advantage

1. The adversary sends a new ciphertext $l$ 
2. A bit $b$ is chosen uniformly at random: $b\in\{0,1\}$
3. The adversary receives the decryption of $c^{l}$, and again attempts to guess which message came from if either $m_{1}$ or $m_{0}$.

This usually done by generating a set of ciphertexts from modifying the ciphertexts outputted by $m_{0}$ and $m_{1}$ and see if this changes are visible in the newly decrypted message.

$$
\begin{align*}
c_{1}^{'}&= c_{1}\oplus 0\ldots01\\
m_{1}^{'}&= Dec_{k}(c_{1}^{'})\\
b^{'}&=
\begin{cases}
1\quad \text{if}\ m_{1}^{'}=m_{1}\oplus 0\ldots01\\
0\quad \text{Otherwise} 
\end{cases}
\end{align*}
$$


![[Pasted image 20230126220853.png]]