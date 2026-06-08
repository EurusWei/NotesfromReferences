FWL theorem states that a multivariate linear regression model can be estimated all at once or in three separate steps:
1. Debiasing step: $\tilde{T}=T-\hat{T}$
2. Denoising step: $\tilde{Y}=Y-\hat{Y}$
3. Regress $\tilde{Y}$ on $\tilde{T}$ to obtain the causal effect

