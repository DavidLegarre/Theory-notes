# Bayesian Network (BN)
A **Bayesian network** (also known as a **Bayes network**, **Bayes net**, **belief network**, or **decision network**) is a [[Probabilistic Graphical Models|probabilistic graphical model]] that represents a set of variables and their conditional independencies via a [[Graph#Directed Acyclic Graph DAG|directed acyclic graph]] (DAG)

The main advantage of this approach is that there are many efficient algorithms that can perform inference and learning in Bayesian Networks.

The nodes in these DAGs represent variables: they may be observable quantities, unknown parameters or hypotheses. Edges represent conditional dependencies; nodes that are not connected (no paths connects one and another) represent variables that are conditionally independent of each other. Each node is associated with a probability function that takes, as input, a particular set of values for the node's parent variables, and gives (as output) the probability of the variable represented by the node.
