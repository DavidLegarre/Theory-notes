# Variable Elimination (VE)

Example of on a chain
![[Pasted image 20220708202119.png]]
![[Pasted image 20220708202128.png]]

# The induced Graph
Steps:
1. If the original graph is a [[Bayesian Network|BN]], moralize (join the parents of each node) it.
2. Eliminate variables according to the given ordering
	1. Eg: $P(J)\ ?$  with ordering $C,D,I,H,G,S,L$
3. Once a variable is eliminated, connect all neighbors ($I_{K,\alpha}$)

Original graph:
![[Pasted image 20220709172720.png]]

Induced graph:
![[Pasted image 20220709172737.png]]

The **maximal clique in** $I_{K,\alpha}$ determines the complexity.

* **Width of an induced graph**: The number of nodes in the largest clique minus $1$ 
* **Tree-width (Minimal induced width)**: The minimal width of the induced graph