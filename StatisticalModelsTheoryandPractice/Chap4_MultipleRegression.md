# Highlights
- Assumptions of regression models
    - Model: $Y = X\beta + \epsilon$;
    - the data on $Y$ are observed values of $X\beta + \epsilon$;
    - The $\epsilon_i$ are independent and identically distributed, with mean $0$ and variance $\sigma^2$.
- Discern difference between: random erros vs. residuals, parameters vs. estimates.
- The OLS (ordinary least squares) estimator of linear regression parameter $\beta$ is: 
$\hat{\beta} = (X^TX)^{-1}X^TY$. Related properties:
    - $e\perp X, \bar{e}=0$;
    - OLS is conditionally unbiased, i.e., $E(\hat{\beta}|X)=\beta$, when $\hat{\beta}=\beta + (X^TX)^{-1}X^T\epsilon$;
    - $cov(\hat{\beta}|X)=\sigma^2(X^TX)^{-1}$;
    - The conditional unbiased estimator of $\sigma^2$ is $\hat{\sigma^2}=\frac{1}{n-p}\sum_{i=1}^ne_i^2$.
- For a regression equation with intercept, $R^2$ is the square of the correlation between $\hat{Y}$ and $Y$.
- $R^2=var(X\hat{\beta})/var(Y)$ measures goodness of fit, not the validity of any underlying causal model.
- If the variables are orthogonal to each other, dropping one in the model, the estimates of else parameters will remain the same. However, if they are correlated (there is "collinearity"), dropping one varaible will induce the *omitted-variable bias* in estimates, as the disturbance term is now correlated with rest variables, and regression on them picks up the effect of the omitted variable. See Exercises 4B.5,8,10,11,12.

# Discussion on P53
> What happens to OLS if the assumptions break down?
>> If $E(\epsilon|X)\neq 0_{n\times 1}$, the bias in the OLS estimator is $(X^TX)^{-1}X^TE(\epsilon|X)$. If $E(\epsilon|X)= 0_{n\times 1}$ but $cov(\epsilon|X)\neq \sigma^2 I_{n\times n}$, OLS will be unbiased. However, $\hat{\sigma}^2(X^TX)^{-1}$ may be a misleading estimator of $cov(\hat{\beta}|X)$, and significance levels would not be trustworthy, for those are based on standard errors.