[[Probability]] properties
## Marginal probability
$$
P(x=a_{i})\equiv\sum\limits_{y\in A_y}P(x=a_{i},y)
$$
$$
Pr(y)\equiv\sum\limits_{x\in A_{x}}P(x,y)
$$
## Conditional probability
$$
P(x=a_{i}|y=b_{j})\equiv \frac{P(x=a_{i},y=b_{j})}{P(y=b_{j})}
$$

## Independence
### Marginal independence
$$
P(x,y)=P(x)P(y)
$$
* Denoted as $x\bot y$.

### Conditional independence
$$
P(x,y|z)=P(x|z)P(y|z)
$$
* Denoted as $x\bot y\ |\ z$     

## Product (or chain) rule
$$
P(x,y)=P(x|y)P(y)=P(y|x)P(x)
$$
## Sum rule
$$
P(x)=\sum\limits_{y}P(x,y)=\sum\limits_{y}P(x|y)P(y)
$$

## Bayes Theorem
![[Bayes' Theorem]]
