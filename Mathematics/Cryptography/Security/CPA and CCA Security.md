## CPA security
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

## CCA Security

```ad-abstract
title:Definition
A Chosen-cihpertext attack (CCA) is a type of attack that can be performed on a security scheme to try and see if there's a posibility that when a change is applied to a ciphertext see those same changes in the decrypted plaintext
```
## Malleability

```ad-abstract
title:Malleability
A scheme is said to be *malleable* if it is possible to modify a ciphertext and cause a *predictable change* to the plaintext.
```

![[Pasted image 20230126220853.png]]

## Summary

Given the situation in which an Adversary $A$ has access to a Challenger $C$. The CPA schema is defined as a "game" in which $A$ must send two messages at the same time to $C$ and this will choose at random one of the two messages, encrypt it, and return it back to $A$. Then, if $A$ has a better chance to guess which message that cipher belongs to (i.e. better than random $\frac{1}{2}$). 

If the can gain this advantage using only these actions:

* $A$ can perform any efficient algorithm  
* $A$ can send any message to get the cipher from $C$ while this messages are different from the one we are trying to obtain. 

We will say it is CPA secure

If this holds, we then can check for CCA security. Following the same "game" but with an extra action

* Now, $A$ can send also ciphers to be decrypted for as long as that cipher is not the same one as the one we are trying to obtain

### Important notice

Every time $A$ sends a message to $C$ if the schema specifies a new key is generated then a new key is generated for each message as if a new conversation has started.