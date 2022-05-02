# Security principles - Cryptography
There are 3 main security principles that must hold:

1.  ***Security is not possible without randomness***
2.  ***Security is relative to the computational resources of the adversary***
3.  ***Design your cryptographic schemes to be secure against an attacker that knows how they work*** (Kerckhoffs's Principle, 1883)

In order to calculate most of the problems we need to take into account [[Combinatorics]].
# Encryption
![[Pasted image 20220426111015.png]]

* Alice (A) wants to send a message (known as **plaintext**) to Bob (B)
* To keep the message secret A sends an encrypted message (known as **ciphertext**) to B
* and Eve (E) wants to get information about the message

## Encryption notation
An *encryption scheme* is composed of three algorithms: (*Keygen*, *Enc*, *Dec*). 
* Where $\lambda$ is the keylength or security parameter
* $m$ is the message or plaintext
* $c$  is the ciphertext
* $k$ is the encryption key
* $k'$ is the decryption key
Then, we say we have symmetric encryption when $k=k'$ 
![[Pasted image 20220426123238.png]]

## Encryption algorithms
In order to have good encrypted communications, we need the algorithms that we use to be secure (that follows the security principles) and [efficient](Algorithms#Efficient algorithms).  

## Security level
We say that a cryptographic scheme has *n-bit security* if the best known attack requires $2^n$ steps