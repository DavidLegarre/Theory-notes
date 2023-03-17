# Group Theory
## Group definition

A group is a set of elements associated to an operation $(G, \circ)$. It must fulfill 3 **properties**:

1. **Closure**:
   $$a,b \in G\to (a\circ b) \in G$$
2. **Associativity**:
   $$
   a,b,c \in G\to (a\circ b)\circ c = a\circ(b\circ c)
$$
3. **Identity**:
$$
e \in G \to \forall a \in G,\ a\circ e=e\circ a=a
$$
4. **Inverses**:
   $$
   \forall a \in G, \exists\ a^{-1},\ a\circ a^{-1}=a^{-1}\circ a =e
$$

## Order of a group

The order of a group is the number of elements in $\mathbb{G}$:
$$
\begin{align*}
ord(\mathbb{G})&=|\mathbb{G}|\\
ord(\mathbb{Z}_{5}^{*})&=4=\phi(5)
\end{align*}
$$

## Subgroups

Defined as:
$$
H\subseteq \mathbb{G}
$$
$H$ has the same properties of $\mathbb{G}$. So $H$ is also a group

## Generators

A subgroup $x$ is a generator if: $|x|=|G|$

### Cyclic groups

$G$ is a cyclic group if it's finite and has a generator:
$$
<g>=\{g^{k}\}=G
$$
If $G$ is a cyclic group, then $|<g>|=\phi(|G|)$ 

## Check if a group has a generator

Let $g$ be the suspected generator of group $G$. Let $d=\{1,\dots\},d\mid|G|$. 
Then let $M=|G|$, if $g^{d}\not=1\ \forall\ d\mid M$, then $g$ is a generator.

### Example

To find all the generators of the group $\mathbb{Z}_{11}^{*}$. We know its size is $m=\varphi(11)=10$. The divisors (or factors) of $10$ are $\{2^{1}, 5^{1}\}$. 

Then $\forall a \in \mathbb{Z}_{11}^{*}$:

![[Pasted image 20230317180417.png]]

Then we know that all the generators of $\mathbb{Z}_{11}^{*}$ are $\{2,6,7,8\}$ 

## Euler's Theorem

Let $G$ be a group:
$$
\forall x\in G,\ x^{ord(G)}=e
$$
## Lagrange Theorem

$$
H\subseteq G\to ord(H)|ord(G)
$$

Where $|$ means that it divides.

## Discrete Logarithm

If $g$ is a generator of $G$, then for every $a \in G$ there is a unique integer $i \in \mathbb{Z}_{n}$ such that 
$g^{i}=a\mod n$. This $i$ is called the discrete logarithm of $a$ to base $g$, and we denote it 
by $DLog_{G,g}(a)$ 