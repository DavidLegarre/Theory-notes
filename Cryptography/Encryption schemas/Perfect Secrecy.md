# Perfect secrecy
An encryption scheme has perfect secrecy when, for a uniformly random $k$, all ciphertexts $c$ and all pairs of messages $m_{0}, m_{1}$ follow:
$$
P(c=E_{k}(m_{0}))=P(c=E_{k}(m_{1}))
$$
This means that the ciphertext produced reveals absolutely no information about the underlying plaintext, besides its length. We formalize this by saying that, given a ciphertext and two messages, the ciphertext has the same probability of corresponding to each of the messages.
