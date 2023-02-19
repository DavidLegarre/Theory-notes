Is a [[Block Ciphers|block cipher]] of length 64 and key length 56

To improve the security of DES one can try to apply it two times with different keys:
$$
c=2DES_{k}(m)=DES_{k_{2}}(DES_{k_{1}}(m) )
$$
In order to decrypt this message we then get that:
$$
\begin{align*}
DES_{k_{2}}^{-1}(c)&=DES_{k_1}(m)\\
m&= DES_{k_{1}}^{-1}(DES_{k_{2}}^{-1}(c)) 
\end{align*}
$$
We can define this middle cipher as:
$$
c'=DES_{k_{2}}^{-1}(c)=DES_{k_1}(m)
$$
[[DES.canvas]]
![[Pasted image 20230217202330.png]]

## Meet in the middle attack

![[Pasted image 20230217201016.png]]

The idea of this attack is that Eve has access to the intermediate steps of the encryption. Then, if this is the case then Eve only has to compute the first set of 56 keys and encrypt a message with each one creating a table of possible encryptions. 

When the server decrypts this messages Eve will have $DES_{k_{2}}^{-1}(c)$ that as shown before is the same as $DES_{k_{1}}(m)$ which she has already precomputed. The moment she finds a collision between her table of $k_{1}$ and $c'$ she would've found the key pair.

Thanks to this the security level has dropped significantly, now Eve only has to crack one of the two keys of length 56