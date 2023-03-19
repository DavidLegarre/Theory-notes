The number of generators is computed as phi(|Zp*|) with p=13, the result is 4. You will notice that 2 is a generator, the other 3 generators are those "a" values such that 2^(gcd(12,alpha)=1) mod 13 = a. In this case gcd(12,alpha)=1 for 5,7,11. Therefore you have to comput 2^5 mod 13, 2^7 mod 13, 2^11 mod 13 for having the other 3 generators (6,7,11). As a result the 4 generators are 2,6,7,11.

ord(g^k) = p -1 / k if k divisible by p, if not, ord(g^k) = p - 1 ( gcd (p-1, k).


Find all generators in $\mathbb{Z}_{13}^{*}$. Find also all the subgroups and their generators

The number of generators is computed as $\varphi(|\mathbb{Z}_{p}^{*}|)$  with $p=13$, the result is $4$. You will notice that $2$ is a generator that $\langle2\rangle=\mathbb{Z}_{13}^{*}$.  The other generators of the group are those $\alpha$ values such that $2^{\alpha}\gets{gcd(12,\alpha)=1}\mod13$. 

The generators are for each divisor $k$ of $ord(G)$ we then have the group $G$ can be generated as $\langle a^{\frac{ord(G)}{k}}\rangle$. 