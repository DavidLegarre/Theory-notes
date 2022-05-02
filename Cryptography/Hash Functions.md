# Hash functions
## Definition
Hash function definition:
$$
H\ : \{0,1\}^{*}\to\{0,1\}^{l}
$$
for some $l\in\mathbb{N}$ , and where $\{0,1\}^{*}$ denotes the set of all bitstrings of any length. The process of computing a hash is called *hashing*, and the output is referred to as the *hash*.

## Properties

### 1. Collision resistant
We say a hash function $H$ is collision resistant if, given a bitstring $b$ it is hard to find another bitstring $b'$ such that $b\not=b'$ and $H(b)=H(b')$. In this case, the pair $(b,b')$ is called a *collision* of $H$.

### 2. preimage-resistant
Given $h$ sampled uniformly at random, it is hard to find a bitstring $b$ such that $H(b)=h$.

### 3. Second preimage-resistant
Given $b$, it is hard to find $b'=b$ such that they form a collision

If $H$ is collision-resistant, then it is second preimage-resistant.
