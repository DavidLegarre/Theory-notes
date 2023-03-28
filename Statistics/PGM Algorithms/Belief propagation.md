relates to: [[Graph]]
# Belief Propagation

Basic idea:
* Associate a message (factor) to each edge in both directions
* Iteratively propagate information via message update equations
* Once converged, the marginals can be computed at each node from the messages
This method will always converge, if the graph is a tree.

The algorithm works by passing real valued functions called *messages* along the edges between the hidden nodes. More precisely, if $v$ is a variable node and $a$ is a factor node connected to $v$ in the factor graph, then the messages $\mu_{v\to a}$  (from $v$ to $a$) and the messages $\mu_{a\to v}$ (from $a$ to $v$) are real-valued functions.
These messages contain the **influence** that one variable exerts on another. The messages are computed differently depending on whether the node receiving the message is a variable or a factor:

**Message** $\mu_{v\to a}$ Variable to Factor:
$$
\mu_{i\to a}(x_i)=
\prod_{
a^{*}\in N(i)\setminus\{a\}
}
\mu_{a^{*}\to i}(x_i)
$$
Where: $N(i)$ is the set of neighboring factor nodes of $i$.
![[Pasted image 20220708204809.png]]


**Message** $\mu_{a\to i}$ Factor to variable
$$
\mu_{a\to i}(x_{i})=
\sum\limits_{x_{a}\setminus\{i\}}
f_a(x_a)
\prod_{j\in N(a)\setminus\{i\}}
\mu_{j\to a}(x_j)
$$
![[Pasted image 20220708205349.png]]


Once all the messages have been updated, **any** marginal can be computed by taking the product of the incoming messages and renormalizing.

## Belief propagation Clamping evidence
Evidence can be incorporated in the factor graph by adding a new factor which evaluates to $1$ for $E=e$, and $0$ otherwise.
![[Pasted image 20220709163144.png]]

The probability of evidence $P(E)$ can be computed by chosing an arbitrary variable *after* running BP and summing the product of incoming messages over all values of the variable

![[Pasted image 20220709163515.png]]

## Marginal over a subset
Marginal probabilities that involve more than one single variable can be computed easily from a common factor if all variables are directly connected.

![[Pasted image 20220709170248.png]]
