```ad-abstract
title: Definition
A hush function is an efficient algorithm $H$ such that:
$$
H:\{0,1\}^{*}\to\{0,1\}^l
$$

for some $l\in \mathcal{N}$ and where $\{0,1\}^*$ denotes the set of all bitstrings of arbitrary length
```

Notice that, unlike in encryption, hash functions do not use a secret key. This function compress an arbitrary long set of bits into a, usually, much sorter set of bits (i.e. $|l|<<|*|$).  

## Hash functions qualities

Let $H$ be a hash function. We then say that $H$ is:

* **Collision-resistant**: If it is hard to find two bitstrings $b,b'$ such that $b\not=b'$ and $H(b)=H(b')$. In this case, the pair $(b,b')$ is called a collision of $H$. 

* **Second preimage-resistant**: If, given $b$, it is hard to find $b'\not=b | H(b)=H(b')$ 

* **Preimage-resistant**: If, given $h$ sampled uniformly at random, it is hard to find a bitstring $b | H(b)=h$ 

```ad-abstract
title:Proposition
If $H$ is collision-resistant, then it is second preimage-resistant.
This does not mean that $H$ being collision resistant implies that it is preimage rsistant
```

