FWL theorem states that a multivariate linear regression model can be estimated all at once or in three separate steps:
1. Debiasing step (regress on confounders): $\tilde{T}=T-\hat{T}$
2. Denoising step (regress on confounders): $\tilde{Y}=Y-\hat{Y}$ 
3. Regress $\tilde{Y}$ on $\tilde{T}$ to obtain the causal effect

Plots from P107-114 are helpful.