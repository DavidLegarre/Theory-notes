```ad-abstract
title: Definition

A Chosen-plaintext attack (CPA) is a type of attack that can be performed on a security scheme, based on the assumption that the attacker can obtain the ciphertexts for arbitrary plaintexts (via an "oracle"). 
```

## Steps of the attack

1. The attacker choses $n$ plaintexts
2. The attacker sends these $n$ plaintexts to the encryption *oracle*
3. The encryption oracle will then encrypt the attacker's plaintext and send back the ciphertexts 
4. The attacker receives the the ciphertexts back in a way that it knows from which message came each ciphertext 
5. Based on this, the attacker can attempt to extract either the whole key or parts of it. 

## Advantage

1. The adversary outputs two plaintexts $m_{0}$ and $m_{1}$
2. A bit $b$ is chosen uniformly at random: $b\in \{0, 1\}$
3. The adversary receives the encryption of $m_{b}$, and attempts to "guess" which plaintext it received, and outputs the bit $b$.

Let $W_{b}$ be the event that the adversary outputs $1$ in experiment $b$, then we say that the advantage the adversary has is calculated as:
$$
Adv(\mathcal{A})=|P(W_{0})-P(W_{1})|
$$


![[Pasted image 20230123144552.png]]

## CPA Secure

```ad-abstract
title:definition
We will say an encryption scheme is CPA secure if the scheme is not deterministic, a.k.a. there's at least some randomness. 
```
