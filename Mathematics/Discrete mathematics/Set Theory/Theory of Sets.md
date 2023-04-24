relates to: [[Topology]]

# Sets

* If an object **A** belongs to a set **S** we shall write $A \in S$ (read, "$A$ in $S$"), and if $A$ does not belong to $S$ it is written as $A \not \in S$.

* If $A_{1},\ldots,A_{n}$ are objects, the set consisting of precisely these objects will be written $\{A_{1},\ldots, A_{n}\}$
   
* $A \in\{A\}$ is true but $A=\{A\}$ is not. 
  
* The empty set is noted as $\emptyset$   

## Subsets

```ad-summary 
title:Defintion 
Let $A$ and $B$ be sets. If for each object $x \in A$, it is true that $x \in B$, we say that $A$ is a *subset* of $B$. In this event, we shall also say that $A$ *is contained in* $B$, which we write $A\subset B$, or that $B$ *contains* $A$, which we write $B\supset A$.
$$
A\subset B = \{\forall x \in A \land x \in B\}
$$
```

$$
A=B\iff (A\subset B \land B\subset A)
$$
Sets may themselves be objects *belonging to other sets*. Ex:
$$
\{\{1,3,5,7\},\{2,4,6\}\}
$$

## Power set

```ad-summary 
title:Defintion 
$$
\forall A, \exists 2^{A}\ \forall B \in 2^{A}\iff B\subset A
$$
The set $2^{A}$ is the power set of $A$ that contains all the of A.
```

# Set Operations

## Union

```ad-summary 
title:Defintion 
The union of the sets $A$ and $B$ is the set whose members are those objects $x$ that:
$$
A\cup B = \{\forall x, x \in A \lor x \in B\}
$$
```
![[Pasted image 20230408202201.png]]

## Intersection

```ad-summary 
title:Defintion 
The intersection of $A$ and $B$ is the set whose members are those objects $x$ that:

$$
A\cap B=\{\forall x, x \in A \land x \in B\}
$$
```
![[Pasted image 20230408202434.png]]

## Complement

```ad-summary 
title:Defintion 
Let $A \subset S$. The *complement* of $A$ in $S$ is the set of elements that belong to $S$ but not to $A$. 
$$
S\setminus A = \{\forall x, x \in S \land x \not \in A\}
$$

The complement can also be noted as:
$$
A^{c}, C(A)
$$
And relative complement as:
$$
C_{s}(A), S - A
$$
```
![[Pasted image 20230408202756.png]]
Then we can see that:
$$
(S\setminus A)\setminus A = A
$$
## De Morgan's laws

```ad-summary 
title:Defintion 
Let $A \subset S, B\subset S$. Then:
$$
\begin{align*}
C(A\cup B) &= C(A)\cap C(B)\\
C(A\cap B) &= C(A)\cup C(B)
\end{align*}
$$
```

### Proof

Suppose $x \in C(A\cup B)$. Then $x \in S$ and $x \not \in A\cup B$. Thus, $x\not \in A$ and $x\not \in B$, or $x \in C(A)$ and $x\in C(B)$. Therefore $x \in C(A) \cap C(B)$ and, consequently:
$$
C(A\cup B)\subset C(A)\cap C(B)
$$
Conversely, suppose $x \in C(A)\cap C(B)$. Then $x \in S$ and $x \in C(A)$ and $x \in C(B)$. Thus, $x\not \in A$ and $x\not \in B$, and therefore $x\not \in A\cup B$. It follows that $x \in C(A\cup B)$ and, consequently,
$$
C(A)\cap C(B)\subset C(A\cup B)
$$

We then have that:
$$
C(A)\cap C(B) = C(A\cup B)
$$

