# Bayesian Network (BN)
A **Bayesian network** (also known as a **Bayes network**, **Bayes net**, **belief network**, or **decision network**) is a [[Probabilistic Graphical Models|probabilistic graphical model]] that represents a set of variables and their conditional independencies via a [[Graph#Directed Acyclic Graph DAG|directed acyclic graph]] (DAG)

The main advantage of this approach is that there are many efficient algorithms that can perform inference and learning in Bayesian Networks.

The nodes in these DAGs represent variables: they may be observable quantities, unknown parameters or hypotheses. Edges represent conditional dependencies; nodes that are not connected (no paths connects one and another) represent variables that are conditionally independent of each other. Each node is associated with a probability function that takes, as input, a particular set of values for the node's parent variables, and gives (as output) the probability of the variable represented by the node.

### Example
![[Pasted image 20220625121014.png]]

There's two events that can cause the grass to be wet: an active sprinkler or rain. Rain has a direct effect on the use of a sprinkler (when it rains, the sprinkler is not usually active). This situation can be modeled with a Bayesian Network. Each variable has two possible values $T:$ true and $F:$ false.

The joint probability function of the model is:

$$
Pr(G,S,R)=Pr(G|S,R)Pr(S|R)Pr(R)
$$

## Joint probability distribution
The joint probability distribution of a Bayesian network is defined as 
$$
P(X_{1},\ldots,X_{n})=\prod_{i=1}^{n}P(X_{i}|\text{parents}_{i})
$$
This factorization represents a probability distribution $\to$ all values are positive and add up to $1$.

Each variable is conditionally independent of all its non-descendants in the graph given the value of all of its parents

# D-separation algorithm
Is an [[Computer Science/Algorithms/Algorithms|algorithm]] that given an evidence set $E$ and two non-overlapping subsets of variables $A$ and $B$, it returns us whether $A\perp B|C$ holds or not.

We know a path is blocked if:

![[Pasted image 20220703185417.png]]


If all paths from $A$ and $B$ are blocked then, $A$ is d-separated from $B$ by $C$ and
$$
A\perp B\ |\ C
$$
# Models as Bayesian Networks
## Naïve bayes
In classification problems: features are pairwise independent given the class.
![[Pasted image 20220703190355.png]]

The ratio of probabilities in a binary classification problem would be:
$$
\frac{P(label=l_{1}|f_{1},\ldots,f_{n})}{P(label=l_{2}|f_{1},\ldots,f_{n})}
=
\frac{P(label=l_1)}{P(label=l_{2})}
\prod_{i=1}^{n}
\frac{P(f_{i}|label=l_{1})}{P(f_{i}|label=l_{2})} 
$$
## Noisy-OR 
Given multiple causes, we will have one effect.

![[Pasted image 20220703191650.png]]

While adding a *Leakage probability* $p_{0}$. This model only requires $M+1$ instead of $2^M$. $f$ is a deterministic OR function

$$P(I_{k}=0|C_{k})=(1-p_{k})^{C_{k}}$$

We define that the causes are independent of the other causes.

We then have that:
$$
P(E=0|C)=
\prod_{k=1}^{n}(1-p_{k})^{C_{k}}
$$
When trying to predict the effect of 2 causes:
$$
P(E=1|C_{1}=1, C_{2}=1)=p_{1}+p_{2}-p_{1}p_{2}
$$

## Hidden Markov model
A temporal model consisting of: 
* A state variable and observation
* A Markov process defined on the state variable (transition model)
* An observation model that maps states with observations
