# Group Theory
## Group definition

A group is a set of elements associated to an operation $(G, \circ)$. It must fulfill 3 **properties**:

1. **Associative law**: 
	   $(x\circ y)\circ z=x\circ(y\circ z)\ \forall x,y,z\in\mathbb{G}$  
1. **Existence of identity**: 
$$\exists\ e\in\mathbb{G}\ :\forall x\in\mathbb{G},\  e\circ x =x\circ e=x
   $$
1.  **Existence of inverse**: 
$$\forall g\in G : \exists g^{-1}\ g\circ g^{-1}=g^{-1}\circ g=e$$

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
