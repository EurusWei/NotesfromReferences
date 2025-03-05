P261
> Bootstrap provides a direct computational way of assessing uncertainty, by sampling from the training data.

P267
> In essence the bootstrap is a computer implementation of nonparametric or parametric maximum likelihood. The advantage of the bootstrap over the maximum likelihood formula is that it allows us to compute maximum likelihood estimates of standard errors and other quantities in settings where no formulas are available.

P268
> The Bayesian approach differs from the standard ("frequentist") method for inference in its use of a prior distribution to express teh uncertainty present before seeing the data, and to allow the uncertainty remaining after seeing the data to be expressed in the form of a posterior distribution...We assume that the observed features $x_1, x_2,..., x_N$ are fixed, so that the randomness in the data comes solely from $y$ varying around its mean $\mu(x)$.

P270
> In Gaussian models, maximum likelihood and parametric bootstrap analysis tend to agree with Bayesian analysis that use a noninformative prior for the free parameters. These tend to agree, because with a constant prior, the posterior distribution is proportional to the likelihood. 

P272
> In this sense (in case of Gaussian and multinomial distribution), the bootstrap distribution represents an (approximate) nonparametric, noninformative posterior distribution for our parameter...Hence we might think of the bootstrap distribution as a "poor man's" Bayes posterior. By perturbing the data, the bootstrap approximates the Bayesian effect of perturbing the parameters, and is typically much simpler to carry out.

P276
> EM algorithm: are ones for which maximization of the likelihood is difficult, but made easier by enlarging the sample with latent (unobserved data).

P277
> The EM iteration never decreases the likelihood. 

P278
> The E step is equivalent to maximizing the log-likelihood over the parameters of the latent data distribution. The M step maximizes it over the parameters of the log-likelihood. 

P279
> Gibbs sampling, an MCMC procedure, is closely related to the EM algorithm: the main difference is that it samples from teh conditional distribution rather than maximizing over them...More formally, Gibbs sampling produces a Markov chain whose stationary distribution is the true joint distribution.

P282
> The bagged estiamte will differ from the original estimate $\hat{f}(x)$ only when the latter is a nonlinear or adaptive function of the data. 

P283
> Bagging can dramatically reduce the variance of unstable procedures like trees, leading to improved prediction...because averaging reduces variance and leaves bias unchanged.

P285
> True population aggregation never increases mean squared error. This suggests that bagging-drawing samples from the training data - will often decrease mean squared error.

P286
> Unfortunately, the unstable models most helped by bagging are unstable because of the emphasis on interpretability, and this is lost in the bagging process.

P288
> In the same way that bootstrap values of an estimator is viewed as approximate posterior values of a corresponding parameter, the bagged estimate is an approximate posterior Bayesian mean. In contrast, the training sample estimate $\hat{f}(x)$ corresponds to the mode of the posterior. Since the posterior mean (not mode) minimizes squared-error loss, it is not surprising that bagging can often reduce mean squared-error.