![[Pasted image 20230114221221.png]]

The main parts of an encryption are defined as:
* $m$ (message): The content Alice (A) wants to encrypt and send to Bob (B)
* $c$ (ciphertext): The text that hides $m$
* $k$ (secret key): The secret key used to encrypt the message

A symmetric encryption scheme always consists of 3 algorithms:

1. **KeyGen**: Chooses some random key $k$ of length $\lambda$, according to some probability distribution
2. **Enc**: Uses the secret key $k$ to encrypt a message $m$, and outputs the encrypted message $c$: 
$$
c = Enc_k(m)
$$
3. **Dec**: Uses the secret key $k$ to decrypt the ciphertext $c$ and recover the original message:
$$
m=Dec_k(c)
$$
## Correctness:

For encryption scheme to be correct it must follow that 
$$\forall k,m\quad m = Dec_k(Enc_k(m))$$

## Perfect secrecy
An encryption scheme has perfect secrecy when, for a uniformly random $k$, all ciphertexts $c$ and all pairs of messages $m_{0}, m_{1}$ follow:
$$
P(c=E_{k}(m_{0}))=P(c=E_{k}(m_{1}))
$$
This means that the ciphertext produced reveals absolutely no information about the underlying plaintext, besides its length. We formalize this by saying that, given a ciphertext and two messages, the ciphertext has the same probability of corresponding to each of the messages.
