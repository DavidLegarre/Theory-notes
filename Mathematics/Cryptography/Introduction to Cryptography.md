# Fundamental Security Principles

1. **Security depends on the resources of the attacker**: We say that a cryptographic scheme is secure if there are not efficient attacks
2. **Kerckhoffs' principle**: Design the your system so that it is secure even if the attacker knows all of its algorithms
3. **Security is impossible without randomness**

## Security Parameter

The way to achieve this is through a natural number that we call the _security parameter_, usually denoted by $\lambda$. The information about both security and efficiency will be expressed in terms of the security parameter.

## Security Level 

```ad-abstract
A cryptographic scheme has $n$-bit security if the best known attack requires $2^n$ steps. When the best known attack is a brute-force attack, then $n=\lambda$.
```

## Confusion and Diffusion

```ad-abstract
title:Confusion
**Confusion**: each bit of the ciphertext depends on several parts of the key. In the other words, the relation between key and ciphertext must not be clear to any attacker
```

```ad-abstract
title: Diffusion

```

## Security

* [[CPA Security]]
* [[CCA Security]]

## Types of Encryption

 1. [[Symmetric Encryption]]

## Encryption Schemes

* [[Shift cipher (Caesar's)]]
* [[One-Time-Pad]]
* [[Block Ciphers]]
