```toc
style: number
min_depth: 1
```
# Sample Space

```ad-summary 
title:Sample space
A set $S$ that consists of all possible outcomes of a random experiment is called a *sample space*, and each outcome is called a *sample point*. Often there will be more than one sample space that can describe the outcomes of an experiment, but there is usually only one that will provide the most information.
```

## Events

```ad-summary 
title:Events
An *event* is a subset $A$ of the sample space $S$, i.e., it is a set of possible outcomes. If the outcome of an experiment is an element of $A$, we say that the event $A$ *has occured*. An event consisting of a single point of $S$ is often called a *simple* or *elementary event*.
```

By using [[Theory of Sets#Set Operations|set operations]] on $\forall A \in S$, we can obtain other events in $S$. For example, let $A$ and $B$ be events, then:

1. $A \cup B$ is the event "either $A$ or $B$ or both" 
2. $A \cap B$ is the event "both $A$ and $B$" 
3. $A'$ is the event "not $A$". 
4. $A-B=A \cap B'$ is the event "$A$ but not $B$"

If the sets corresponding to events $A$ and $B$ are disjoint, i.e. $A \cap B =\emptyset$, we often say that these events are *mutually exclusive*. This means that they cannot both occur. 

# Probability

There are two important procedures by means of which we can estimate the probability of an event. 

* **Classical approach**: If an event can occur in $h$ different ways out of a total number of $n$ possible ways, all of which are equally likely, then the probability of the event is $\frac{h}{n}$. 
* **Frequency approach**: If after $n$ repetitions of an experiment, where $n$ is very large, an event is observed to occur in $h$ of these, then the probability of the event is $\frac{h}{n}$. This is also called the *empirical probability* of an event. 


Both the classical and frequency approaches have serious drawbacks, the first because the words “equally likely” are vague and the second because the “large number” involved is vague. Because of these difficulties, mathematicians have been led to an axiomatic approach to probability.

## Axioms of Probability

```ad-summary 
title:Axioms

Suppose we have a sample space $S$. If $S$ is discrete, all subsets correspond to events and conversely, but if $S$ is nondiscrete, only special subsets (called *measurable*) correspond to events. To each event $A$ in class $C$ of events, we associate a real number $P(A)$. Then $P$ is called a *probability function*, and $P(A)$ the probability of the event $A$, if the following axioms are satisfied:

* **Axiom 1**:
$$
	\forall A \in C, P(A)\geq 0  
$$

* **Axiom 2**: For the sure event $S$:
$$
\exists S \in C, P(S)=1
$$

* **Axiom 3**: For any number of mutually exclusive events in $C$:
$$
P(A_{1}\cup A_{2}\cup \dots)=P(A_{1})+P(A_{2})+\dots
$$

```
