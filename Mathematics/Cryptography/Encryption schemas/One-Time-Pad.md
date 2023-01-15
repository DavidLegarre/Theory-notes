By making use of the [[Exclusive OR (XOR)]] and defining the length of the message as $\lambda$ 

* $KeyGen:\ k\gets\{0,1\}^{\lambda}$ 

* $E_k(m):\quad m\oplus k$

* $D_{k}(c): c\oplus k$ 


## Proof of correctness

$$\begin{align*}
\forall k,m\to D_{k}(E_{k}(m))&= m\\
k\oplus(m\oplus k)&= m\\
(k \oplus k) \oplus m &= m\\
0 \oplus m &=  m
\end{align*}$$

## Perfect Secrecy

$$
P(c=E_{k}(m_{0}))=P(c=E_{k}(m_{1}))\quad\forall m_{0},m_{1}
$$
$$
\forall m\in \mathcal{M}, c\in \mathcal{C}\to P(\mathcal{M}=m|\mathcal{C}=c)=P(\mathcal{M}=m)
$$

## Attacks

If the key is used twice the a two-time attack can be performed since:
$$
\begin{align*}
c &= m \oplus k\\
c' &= m' \oplus k
\end{align*}
$$Then we can:
$$c \oplus c' = (m \oplus k) \oplus (m' \oplus k)= m \oplus m'$$
This leaks some information from the original message and a frequency-attack can be performed to find the original messages.

## Disadvantages

This schema is the most secure and efficient. The main disadvantages are that you need to somehow manage to send privately a key of the same size as the message to the receiver without anyone else sees it, this makes the whole idea of encrypting the original message obsolete.