# Highlights
- The MLE looks for the value of $\mu$ that makes the data as likely as possible.
- For exponential families, they generally have a unique maximum for likelihood functions.
- P119: ordinarily, the MLE is biased - although the bias is small with large samples. They asymptotic variance is also an approximation. Moreover, with small samples, the distribution of the MLE is often far from normal.
- Probit model: $P(Y_i=1|X) = \varphi(X_i\beta)$, where $\varphi$ is the cdf of the standard normal distribution function. Given $X$, the $Y_i$ are independent. They are not identically distirbuted. The model can also be interpreted as havinv a latent variable (similar to error term, but cannot be estimated).
- If $Y = X\beta + \epsilon$, and rank of $X$ is $p-1$, the model is non-identifiable: there will be a $\gamma=0_{p\times 1}$ with $X_{\gamma}=0_{n\times 1}$, so that $Y = X(\beta+n\gamma) + \epsilon=X\beta + \epsilon$, and thus $\beta$ is not identifiable.
- P151: Identification is achieved only by imposing somewhat arbitrary assumptions (indepedence, constant coefficients, etc). That is one of the central tensions in the field. Efforts have been made to model this tension as a bias-variance tradeoff. Truncating the number of parameters introduces bias but reduces variance, and the optimal truncation can be considered.
- P152: Question $12$ points to a weakness in response-reschedule models: if a subject's response depends on treatments given to other subjects, the model does not apply.

### Exercise 7.5.9
People often use observational studies to demonstrate causation, but there's a big problem. What is an observational study, what's the problem, and how do people try to get around it? 

In an experiment, the investigator assigns themselves (or are assigned by some third party). The big problem is confounding. Possible solutions include stratification and modeling.