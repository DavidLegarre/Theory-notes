# Markov Networks
## Factors
We define factors as:
$$
\phi: Val(x_{1},\ldots,x_{k})\to\mathbb{R}
$$
Joint probability distributions are (normalized) factors

![[Pasted image 20220703195736.png]]


The problem when trying to ***factorize*** in markov networks is that it is not unique. The joint probability distribution can be expressed without loss of generality as a product over factors defined on the **maximal** cliques on the graph

$$
p(x)=\frac{1}{Z}
\prod_C\phi_{C}(x_{C})
$$

Where $C$ is a [[Graph#Cliques|clique]] in the graph