```ad-summary 
title:Defintion 
Linear regression is the statistical method for fitting a line to data where the relationships between two variables, x and y, can be modeled by a straight line with some error

$$
y=\beta_{0}+\beta_{1}x+\epsilon
$$
```

In the definition, the term $\hat{\beta_{0}}$ is the *intercept*, also known as the *bias* in [[Machine Learning]]. 
Then, we write the linear model in vector form as an inner product:
$$
\hat{Y}=X^{T}\hat{\beta}  
$$
Here we are modeling a single output, so $\hat{Y}$ is a scalar; in general $\hat{Y}$ can be a $K$-vector, in which case $\beta$ would be a $p\times K$ matrix of coefficients. In the $(p+1)$-dimensional input-output space, $(X, \hat{Y})$ represents a hyperplane. 
Viewed as a function over the $p$-dimensional input space, $f(X)=X^{T}\beta$ is linear, and the gradient $f'(X)=\beta$ is a vector in input space that points in the steepest uphill direction.

# Fitting the model

How do we fit the linear model to a set of training data? The most popular method is the method of *least squares*. In this approach, we pick the coefficients $\beta$ to minimize the residual sum of squares:
$$
RSS(\beta)=\sum_{i=1}^{n}(y_{i}-x_{i}^{T}\beta)^{2}
$$
$RSS(\beta)$ is a quadratic function of the parameters, and hence its minimum always exists. but may not be unique. The solution is easiest to characterize in matrix notation. 
$$
RSS(\beta)=(y-X \beta )^{T}(y-X \beta)
$$
where $X$ is an $N\times p$ matrix with each row an input vector, and $y$ is an $N$-vector of the outputs in the training set. Differentiating w.r.t. $\beta$ we get the normal equations:
$$
X^{T}(y-X \beta)=0
$$
If $X^{T}X$ is nonsingular (*square matrix invertible*), then the unique solution is given by:
$$
\hat{\beta}=(X^{T}X)^{-1}X^{T}y
$$




