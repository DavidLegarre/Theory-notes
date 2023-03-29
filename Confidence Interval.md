```ad-summary 
title:Defintion 
A **confidence interval** represents the range of plausible values where we are likely to find the population parameter. 
If we report a point estimate $\hat{p}$, we probably will not hit the exact population proportion. On the other hand, if we report a range of plausible values, representing a confidence interval, we have a good shot at capturing the parameter
```

## Constructing a 95% confidence interval

Our sample proportion $\hat{p}$ is the most plausible value of the population proportion, so it makes sense to build a confidence interval around this point estimate. The standard error provides a guide for how large we should make the confidence interval.  **The standard error represents the standard deviation of the point estimate**, and when the [[Central Limit Theorem]] conditions are satisfied, the point estimate closely follows a normal distribution. 

$$
\text{Standard Error (SE)}: \sqrt{\frac{p(1-p)}{n}}
$$
Then to build a confidence interval of $95\%$:

$$
\hat{p}\pm\mathbb{Z}_{95\%}·SE
$$
$$
\hat{p}\pm 1.96·SE
$$

![[Pasted image 20230329191540.png]]


In a confidence interval $\mathbb{Z}_{\alpha}·SE$ is called the **margin of error**.