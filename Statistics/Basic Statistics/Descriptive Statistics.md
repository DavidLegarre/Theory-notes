reference to: [[Organization of Data]]

Let $x_{1k},\ldots, x_{nk}$ be the $n$ measurements on variable $k$. The the mean of these measurements is defined as:

## Sample Mean

```ad-summary 
title:Defintion 
$$
\bar{x}_{k}=\frac{1}{n}\sum\limits_{j=1}^{n}x_{jk} \quad k=1,2,\ldots,p
$$
```

## Sample Variance

```ad-summary 
title:Defintion 
The variance is the average squared distance from the mean.
$$
s^{2}_{k}=\frac{1}{n}\sum\limits_{j=1}^{n}(x_{jk}-\bar{x}_{k)^{2}}\quad k=1,2,\ldots,p
$$

```

When $n$ is small ( $n<50$, depending on the context ) we shall divide by $\frac{1}{n-1}$ instead.

## Sample Standard Deviation

```ad-summary 
title:Defintion 
The square root of the sample variance, $\sqrt{s^{2}_{k}}$, is known as the sample standard deviation. This measure of variation uses the same units as the observations. 

The standard deviation is useful when considering how far the data are distributed from the mean
```

## Sample Covariance

```ad-summary 
title:Defintion 
A measure of linear association between the measurements of variables $1$ and $2$ is provided by the *sample covariance*:

$$
s_{12}=\frac{1}{n}\sum\limits_{j=1}^{n}(x_{j1}-\bar{x}_{1})(x_{j2}-\bar{x}_{2})
$$

If large values for one variable are observed in conjunction with large values for the other vairable, and the samll values also occur together, $s_{12}$ will be positive. If large values from one variable occur with small values for the other variable, $s_{12}$ will be negative. If there is no particular association between the values for the two variables, $s_{12}$ will be approximately zero.

More generally:
$$
s_{ik}=\frac{1}{n}\Sigma_{j=1}^{n}(x_{ji}-\bar{x}_{i})(x_{jk}-\bar{x}_{k})\quad i=1,2,\ldots,p,\ k=1,2,\ldots,p
$$
```

Note: the sample **covariance** reduces to the sample **variance** when $i=k$. And that, $\forall i,k,\ s_{ik}=s_{ki}$. 

## Sample correlation coefficient

```ad-summary 
title:Defintion 
The sample correlation coefficient is a standardized version of the sample covariance, where the product of the square roots of the sample variances provides the standardization. 
$$
r_{ik}=\frac{s_{ik}}{\sqrt{s_{ii}}\sqrt{s_{kk}}}
$$
```

The sample correlation coefficient has the following properties:
1. The value of $r$ must be $r \in[ -1,+1 ]$ 
2. $r$ measures the strength of the linear association. If $r=0$, this implies no linear 
   association between the components. Otherwise, the sign of $r$ indicates the 
   direction of the association: If $r<0$ then when one value of the pair is larger than 
   the average a value in the other pair is smaller than average, and when $r>0$ they 
   share tendencies, when one value of a pair is larger than average another value in 
   the other pair is too.

We can organize all these descriptive statistics into [[Organization of Data#Arrays|arrays]].
$$
\begin{align*}
\text{Sample means}\quad &\ \  \bar{x}=
\begin{bmatrix}
\bar{x}_{1}\\
\bar{x}_{2}\\
\vdots\\
\bar{x}_{p}
\end{bmatrix}\\
\text{Sample variances and covariances}\quad& \mathbf{S}_{n}=
\begin{bmatrix}
s_{11}& s_{12}&\ldots&s_{1p}\\
s_{21}&s_{22}&\ldots&s_{2p}\\
\vdots&\vdots&\ddots&\vdots\\
s_{p1}&s_{p2}\ldots&s_{pp}
\end{bmatrix}\\
\text{Sample correlations}\quad & \mathbf{R}=
\begin{bmatrix}
1 & r_{12} & \ldots & r_{1p}\\
r_{21}  & 1 & \ldots & r_{2p}\\
\vdots & \vdots & \ddots & \vdots\\
r_{p1} & r_{p2} & \ldots & 1
\end{bmatrix}
\end{align*}
$$

