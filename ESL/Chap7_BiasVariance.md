# Highlights
P219~211
> Choices of measuring errors between $Y$ and $\hat{f}(X)$:
> - *Test error*/generalization error/extra-sample error: prediction error over an independent test sample: $Err_{\mathcal{T}}=E[L(Y, \hat{f}(X))|\mathcal{T}]$, where $X$ and $Y$ are drawn randomly from their joint distribution. The training set $\mathcal{T}$ is fixed, and test error refers to the error for this speicifc training set. *This is the goal, but $Err$ is more possible to estimate.
> - Expected prediction error: $Err = E[L(Y, \hat{f}(X))] = E[Err_{\mathcal{T}}]$. This expectation averages over everything that is random, including the randomness in the training dataset that produced $\hat{f}$.
> - Training error: $\overline{err} = \frac{1}{N}\sum_{i=1}^NL(y_i, \hat{f}(x_i))$. With the model gets more complex, it uses the training data more and is able to adapt to more complicated underlying structures. There is a decrease in bias but an increase in variance. It is an overly optimistic estimate of the generalization error $Err_{\mathcal{T}}$. Part of the discrepancy is due to where the evaluation points occur.
> - *In-sample error*: $Err_{in} = \frac{1}{N}\sum_{i=1}^N E_{Y^0}[L(Y_i^0, \hat{f}(x_i))|\mathcal{T}]$.
> Define the *optimism*: $op\equiv Err_{in}-\overline{err}$. The average of optimism is the expectation of the optimism over training sets: $\omega\equiv E_{y}(op)$ (with predictors fixed).

P223
> $Err(x_0) = E[(Y - \hat{f}(x_0))^2|X=x_0]=Irreducible Error + Bias^2 + Variance$ with $x_0$ is fixed. Typically the more complex we make the model $\hat{f}$, the lower the bias but the higher the variance.

P224
> For linear models fit by ordinary least squares, the estimation bias is zero. For restricted fits, such as ridge regression, it is positive, and we trade it off with the benefits of a reduced variance. The model bias can only be reduced by enlarging the class of linear models to a richer collection of models, by including interactions and transformations of the variables in the model.

P226
> The overall point is that the bias-variance tradeoff behaves differently for $0-1$ loss than it does for squared error loss. This in true means that the best choices of tuning parameters may differ substantially in the two settings. One should base the choice of tuning parameter on an estimate of prediction error.

P229
> For squared error, $0-1$, and other loss functions, one can show quite generally that $\omega\equiv\frac{2}{N}\sum_{i=1}^N Cov(\hat{y}_i, y_i)$. Thus the amount by which $\overline{err} underestimates the true error depends on how strongly $y_i$ affects its own prediction. The harder we fit the data, the greater $Cov(\hat{y}_i, y_i)$ will be, thereby increasing the optimism.

P230
> An obvious way to estimate prediction error is to estimate the optimism and then add it to the training error $\overline{err}$. The methods described in the next section -- $C_p$, $AIC$, $BIC$ and others -- work in this way, for a special class of estimates that are linear in their parameters.

> In contrast, cross-validation and bootstrap methods, described later in the chapter, are direct estimates of the extra-sample error $Err$. These general tools can be used with any loss function, and with nonlinear, adaptive fitting techniques.

> In-sample error is not usually of direct interest since future values of the features are not likely to coincide with their training set values. But for comparison betweenn models, in-sample error is convenient and often lead to effective model selection. The reason is that the relative (rather than absolute) size of the errors is what matters.