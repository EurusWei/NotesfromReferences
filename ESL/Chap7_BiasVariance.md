# Highlights
P219~211
> Choices of measuring errors between $Y$ and $\hat{f}(X)$:
> - *Test error*/generalization error: prediction error over an independent test sample: $Err_{\mathcal{T}}=E[L(Y, \hat{f}(X))|\mathcal{T}]$, where $X$ and $Y$ are drawn randomly from their joint distribution. The training set $\mathcal{T}$ is fixed, and test error refers to the error for this speicifc training set. *This is the goal, but $Err$ is more possible to estimate.
> - Expected prediction error: $Err = E[L(Y, \hat{f}(X))] = E[Err_{\mathcal{T}}]$. This expectation averages over everything that is random, including the randomness in the training dataset that produced $\hat{f}$.
> - Training error: $\bar{err} = \frac{1}{N}\sum_{i=1}^NL(y_i, \hat{f}(x_i))$. With the model gets more complex, it uses the training data more and is able to adapt to more complicated underlying structures. There is a decrease in bias but an increase in variance.

P223
> $Err(x_0) = E[(Y - \hat{f}(x_0))^2|X=x_0]=Irreducible Error + Bias^2 + Variance$ with $x_0$ is fixed. Typically the more complex we make the model $\hat{f}$, the lower the bias but the higher the variance.

P224
> For linear models fit by ordinary least squares, the estimation bias is zero. For restricted fits, such as ridge regression, it is positive, and we trade it off with the benefits of a reduced variance. The model bias can only be reduced by enlarging the class of linear models to a richer collection of models, by including interactions and transformations of the variables in the model.

P226
> The overall point is that the bias-variance tradeoff behaves differently for $0-1$ loss than it does for squared error loss. This in true means that the best choices of tuning parameters may differ substantially in the two settings. One should base the choice of tuning parameter on an estimate of prediction error.

