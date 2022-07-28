# Statistical learning

Suppose that we observe a quantitative response $Y$ and $p$ different predictors, 
$X_{1}, X_{2}, \ldots, X_{p}$. We assume that there is some relationship between $Y$ and $X$ which can be written in the very general form:
$$
Y=f(X)+\epsilon
$$

Here $f$ is some fixed but unknown [[Functions|function]] of $X$, and $\epsilon$ is a random *error term*, which is independent of $X$ and has mean $0$. 
In this formulation, $f$ represents the systematic information that $X$ provides about $Y$.

```ad-note 
title:Defintion 
In essence, statistical learning refers to a set of approaches for estimating $f$.
```

## Prediction
In many situations, a set of inputs $X$ are readily available, but the output $Y$ cannot be easily obtained. In this setting, since the error term averages to zero, we can predict $Y$ using:
$$
\hat{Y}=\hat{f}(X)
$$
Where $\hat{f}$ represents our estimate of $f$, and $\hat{Y}$ represents the resulting prediction of $Y$. In this setting, $\hat{f}$ is often treated as a *black box*, in the sense that one is not typically concerned with the exact form of $\hat{f}$, provided that it yields accurate predictions of $Y$. 

The accuracy of $\hat{Y}$ as a predictor for $Y$ depends on two quantities, called the *reducible* 
and the *irreducible* error. In general, $\hat{f}$ will not be a perfect estimate of $f$, and this 
inaccuracy will introduce some error. 

This error is *reducible* because we can potentially improve the accuracy of $\hat{f}$ by using the 
most appropriate statistical learning technique to estimate $f$. 
However, even if it were possible to form a perfect estimate for $f$, so that our estimated response took the form $\hat{Y}=f(X)$, our prediction would still be inaccurate, since $Y$ is also a function of $\epsilon$, which, by definition, cannot be predicted using $X$. 
Therefore, variability associated with $\epsilon$ also affects the accuracy of our predictions. This is 
known as the *irreducible* error, because no matter how well we estimate $f$, we cannot reduce the error introduced by $\epsilon$. 

$$
\begin{align*}
E(Y-\hat{Y})^{2}
&=E[\, f( \,X) \, +\epsilon-\hat{f}(X) ] \,^{2}\\
&=\underset{\text{Reducible}}{[f(X)-\hat{f}(X)]^{2}}
+\underset{\text{Irreducible}}{Var(\epsilon)}
\end{align*}
$$
Where $E(Y-\hat{Y})^{2}$ represents the average, or [[expected value]], of the squared difference 
between the predicted and actual value of $Y$, and $Var(\epsilon)$ represents the [[variance]] 
associated with the error form $\epsilon$.