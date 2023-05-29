# Probability

## Sample Space

```ad-summary 
title:Definition

The set of all possible outcomes of an experiment is known as the sample space of the experiment and is, usually, denoted by $S$.
```

## Event

```ad-summary 
title:Definition

Any subset $E$ of the sample space is known as an event. That is, an event is a set consisting of possible outcomes of the experiment. If the outcome of the experiment is contained in $E$, then we say that $E$ has occured.
```

# Axioms of probability

For each event $E$, we denote $P(E)$ as the probability of event $E$ occuring. By noting $E_{1},\dots, E_{n}$ mutually exclusive events, we have the 3 following axioms:

1. $$
   0\leq P(E)\leq 1
$$
2. $$P(S)=1$$
3. $$P\left(\overset{n}{\underset{i=1}{{\huge \cup}}} E_{i}\right)=\sum\limits_{i=1}^{n}P(E_{i}) $$
# Permutation

A permutation is an arrangement of $r$ objects from a pool of $n$ objects, in a given order. The number of such arrangements is given by $P(n,r)$, defined as:
$$
P(n,r)=\frac{n!}{(n-r)! }
$$
# Combination

A combination is an arrangement of $r$ objects from a pool of $n$, where the order **does not** matter. The number of such arrangements is given by $C(n,r)$, defined as:
$$
C(n,r)=\frac{P(n,r)}{r!}=\frac{n!}{r!(n-r)!}
$$
## Bayes theorem
![[Bayes' Theorem]]

# Independence

```ad-summary 
title:Definition

Two events $A$ and $B$ are independent if and only if we have:
$$
P(A \cap B)=P(A)P(B)
$$

```
