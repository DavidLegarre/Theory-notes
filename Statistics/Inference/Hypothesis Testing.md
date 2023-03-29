```ad-summary 
title:Defintion 
A Hypothesis is an **educated guess** about something in the world around us. It should be testable, either by experiment or observation. 

A hypothesis is often defined of the form

"If I (do this to an independent variable) then (this will happen to the dependent variable)"
```

## Null Hypothesis

```ad-summary 
title:Defintion 
The **null hypothesis ($H_{0}$)** often represents a skeptical perspective or a claim to be tested.
The **alternative hypothesis ($H_{1}$)** represents an alternative claim under consideration and is often represented by a range of possible parameter values.
```

In many statistical explanations, we use double negatives. For instance, we might say that the
null hypothesis *is not implausible* or we *failed to reject* the null hypothesis. Double negatives
are used to communicate that while we are not rejecting a position, we are also not saying it is
correct

### Example

A researcher thinks that if knee surgery patients go to physical therapy twice a week (instead of 3 times), their recovery period will be longer. Average recovery times for knee surgery patients is 8.2 weeks.

In this example, the **Null hypothesis would be**:
$$
H_{0}:\mu\leq8.2
$$
and the Hypothesis ( The alternative Hypothesis ) that we want to prove is:
$$
H_{1}: \mu>8.2 
$$

## Decision errors

![[Pasted image 20230329192249.png]]

* **Type 1 error**: When we **reject** the null hypothesis when in reality it is **true**.
* **Type 2 error**: When we **accept** the null hypothesis when in reality it is **false**.

## P-Value

```ad-summary 
title:Defintion 
The **p-value** is the **probability of observing data at least as favorable to the 
alternative hypothesis as our current data set**, if the null hypothesis were true. 
We typically use a summary statistic of the data, in this section the sample 
proportion, to help compute the p-value and evaluate the hypotheses.
```

### Hypothesis testing using P-Value

$$
\begin{align*}
p&<\alpha,\ \text{Reject }H_{0}\\
p&>\alpha,\ \text{Do not reject }H_{0}
\end{align*}
$$

## Hypothesis Testing methods

Main note: [[Confidence Interval]]

### Numerical Data

* [[One Sample Z-test]]
* [[One-sample means with the t-distribution]]

### Categorical Data

### General methods

* [[Bayesian Hypothesis Testing]]



