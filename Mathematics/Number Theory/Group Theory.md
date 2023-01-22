# Group Theory
## Group definition
A group is a set of elements associated to an operation $(G, \circ)$. It must fulfill 3 **properties**:
1. **Associative law**: $(x\circ y)\circ z=x\circ(y\circ z)\ \forall x,y,z\in\mathbb{G}$  
2. **Existence of identity**: $\exists\ e\in\mathbb{G}\ s.t.\ e\circ x=x\circ e=x\ \forall x\in\mathbb{G}$ 
3.  **Existence of inverse**: $\forall x\in G,\ \exists y\in G\ s.t.\ x\circ y=y\circ x=e$. This $y$ is called the inverse element

### Examples of groups

**Additive groups**:
1. $(\mathbb{Z}, +)$
2. $(\mathbb{Z}_{n}, +)$

**Multiplicative groups**:
1. $(\mathbb{Z}_{n}^{*}, ·)$

## Order of a group
The order of a group is the number of elements in $G$:
$$
\begin{align*}
ord(G)&=|G|\\
ord(\mathbb{Z}_{5}^{*})&=4=\phi(5)
\end{align*}
$$
## Subgroups
Defined as:
$$
H\subseteq G
$$
$H$ has the same properties of $G$.

## Generators
A subgroup $x$ is a generator if: $|x|=|G|$

### Cyclic groups
$G$ is a cyclic group if it's finite and has a generator:
$$
<g>=\{g^{k}\}=G
$$
If $G$ is a cyclic group, then $|<g>|=\phi(|G|)$ 

## Euler's Theorem
Let $G$ be a group:
$$
x^{ord(G)}=e
$$
## Lagrange Theorem
$$
H\subseteq G\to ord(H)|ord(G)
$$
Where $|$ means that it divides.
