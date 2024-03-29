```toc
```

``` ad-abstract
A block cipher of length $l$ is an encryption scheme that encrypts a message of fixed length $l$
```

When encrypting a large message, we will split it into blocks of length $l$ and encrypt each block, using the same key. For this we need a block cipher that satisfies:

1. **Confusion**: Each bit of the ciphertext depends on several parts of the key. In other words, the relation between key and ciphertext must not be clear to any attacker
2. **Diffusion**: Small changes in the plaintext result in significant changes in the ciphertext. 

## Difference between Stream and Block ciphers



## Modes of operation

### Electronic Codebook (ECB) mode

The most straightforward approach:

![[Pasted image 20230118162227.png]]

$$c_{i}=E_{k}(m_{i})$$

This mode presents several weaknesses: If the same message is encrypted twice, then the same ciphertext is obtained. This provides the attacker with some information. 

In the case of an image this is the result:
![[Pasted image 20230118162339.png]]![[Pasted image 20230118162343.png]]

### Cipher Block Chaining (CBC) mode

The next way would be to:
#### Encryption
$$
\begin{align*}
c_{i}&= F_{k}(m_{i}\oplus c_{i-1})\\
\text{return}&\quad c_{0}||c_{1}||\ldots||c_{\mathcal{l}}
\end{align*}
$$

#### Decryption
$$
\begin{align*}
m_{i}&= F^{-1}_{k}(c_{i})\oplus c_{i-1}\\
return&\quad m_{1}||\ldots||m_{l}
\end{align*}
$$


![[Pasted image 20230131003004.png]]

For this we need to define $c_{0}$, to do this we will use *IV* the initialization vector.

In this mode, the encryption of a block influences the encryption of all the following blocks. The downside of this approach is that it can't be parallelized to optimize the calculations.

### Output FeedBack  (OFB) Mode

This mode actually turns a block cipher into a stream cipher, by recomputing a key each time.
$$
\begin{align*}
w_{i}&= E_{k}(w_{i-1})\\
c_{i}&= m_{i}\oplus w_{i}
\end{align*}
$$
![[Pasted image 20230118162912.png]]

Again, we need an IV to feed the OFB. This mode allows us to precompute a set of keys $w_{i}$ in advance for later use in  the communications. 

### Counter (CTR) Mode

It chooses a **public** random counter ($ctr$ or $nonce$) that is chosen at the beginning of the
communication, and is increased by $1$ after each iteration.
$$
\begin{align*}
ctr_{i}&=ctr_{i-1}+1\\
c_{i}&= m_{i}\oplus E_{k}(ctr_{i})
\end{align*}
$$
![[Pasted image 20230219214936.png]]
![[Pasted image 20230219214942.png]]

## Error propagation

Let $C_{i}$ be ciphertext block $i$, and $P_{i}$ be plaintext block $i$

| Mode | Effect of bit errors in $C_{i}$                                | Effect of bit errors in the $IV$ or $nonce$ |
| ---- | -------------------------------------------------------------- | ------------------------------------------- |
| ECB  | Random bit errors in $P_{i}$                                   | -                                           |
| CBC  | Random bit errors in $P_{i}$, Specific bit errors in $P_{i+1}$ | Specific errors in $P_{1}$                  |
| CFB  | Specific bit errors in $P_{i},P_{i+1},\ldots$                  | Random bit errors in $P_{1},\ldots$         |
| OFB  | Specific bit errors in $P_{i}$                                 | Random bit errors in $P_{1},\ldots$         |
| CTR  | Specific bit errors in $P_{i}$                                 | Random bit errors in $P_{i}$ for bit error in $ctr_{i}$                                            |
