P43
> For prediction purposes linear models can sometimes outperform fancier nonlinear models, especially in situations with small numbers of training cases, low signal-to-noise ratio or sparse data.

P44
> The fitted values at the training inputs are $\hat{\mathbf{y}}=\bm{X}\hat{\beta}=\bm{X}(\bm{X}^T\bm{X})^{-1}\bm{X}^T\bm{y}$, where the matrix $\bm{H}=\bm{X}\hat{\beta}=\bm{X}(\bm{X}^T\bm{X})^{-1}\bm{X}^T$ is sometimes called the "hat" matrix because it puts the hat on $\bm{y}$....the resulting $\hat{\bm{y}}$ is the *orthogonal projection* of $\bm{y}$ onto the column space of $\bm{X}$....If the columns of $\bm{X}$ are not linearly independent, $\bm{X}$ is not of full rank, then $\bm{X}^T\bm{X}$ is singular and the least squares coefficients $\hat{\beta}$ are not uniquely defined....the non-full-rank case occurs most often when one or more qualitative inputs are coded in a redundant fashion.

P47 more results can be found on notes of statistical models
> $(N-p-1)\hat{\sigma}^2 \sim \sigma^2\chi^2_{N-p-1}$.

P48
> To test the hypothesis that a particular coefficient $\beta_j=0$, we use the *Z-score* $z_j=\frac{\hat{\beta}_j}{\hat{\sigma}\sqrt{v}_j}$ where $v_j$ is the $j_{th}$ diagonal element of $\bm{X}^T\bm{X}$. Under the null hypothesis that $\beta_j=0$, $z_j$ is distributed as $t_{N-p-1}$ and a large absolute value of $z_j$ will lead to rejection of null hypothesis. If $\hat{\sigma}$ is replaced by a known value $\sigma$, then $z_j$ would have a standard normal distribution.

P49
> The $F$ statistic measures the change in residual sum-of-squares per additional parameter in the bigger model, and it is normalized by an estimate of $\sigma^2$. Under the Gaussian assumptions, and the null hypothesis that the smaller model is correct, the $F$ statistic will have a $F_{p1-p0, N-p1-1}$ distribution. It can be shown that the $z_j$ are equivalent to the $F$ statistic for dropping the single coefficient $\beta_j$ from the model.

P52
> Gauss-Markov theorem implies that the least squares estimator has the smallest mean squared error of all linear estimators with no bias. However, there may well exist a biased estimator with smaller mean squared error. Such an estimator would trade a little bias for a larger reduction in variance...Any method that shrinks or sets to zero some of the least squares coefficients may result in a biased estimate.

P57
> The least squares estimates often have low bias but large variance.

P61
> Shrinkage methods are more continuous, and don't suffer as much from high variability.

P63 ~64
> When there are many correlated variables in a linear regression model, their coefficients can become poorly determined and exhibit high variance. A wildly large positive coefficient on one variable can be canceled by a similarly large negative coefficient on its correlated cousin...The ridge solutions are not equivariant under scaling of the inputs, and so one normally standardizes the inputs before obtaining the solution. In addition, notice that the intercept $\beta_0$ has been left out of the penalty term. Penalization of the intercept would make the procedure depend on the origin chosen for $Y$; that is, adding a constant $c$ to each of the targets $y_i$ would not simply result in a shift of the predictions by the same amount $c$.

P64
> The ridge regression solution is $\hat{\beta}^{ridge}=(\bm{X}^T\bm{X}+\lambda\bm{I})^{-1}\bm{X}^T\bm{y}$...The solution adds a positive constant to the diagonal of $\bm{X}^T\bm{X}$ before inversion. This makes the problem nonsingular, even if $\bm{X}^T\bm{X}$ is not of full rank, and was the main motivation for ridge regression when it was first introdued in statistics.

> Ridge regression can also be derived as the mean or mode of a posterior distribution, with a suitably chosen prior distribution (normal distribution)...The ridge estimate is the mode of the posterior distribution, since the distribution is Gaussian, it is also the posterior mode.

P66 ~ 67
> $\bm{X}^T\bm{X}=\bm{V}\bm{D}^2\bm{V}^T$ is the *eigen decomposition* of $\bm{X}^T\bm{X}$. The eigenvectors $v_j$ are also called the *principal components* directions of $\bm{X}$. The first principal component direction $v_1$ has the property that $\bm{z}_1=\bm{X}v_1$ has the largest sample variance amongst all normalized linear combinations of the columns of $\bm{X}$....The derived variable $\bm{z}_1=\bm{X}v_1=\bm{u}_1d_1$ is called the first principal component of $\bm{X}$, and hence $\bm{u}_1$ is the normalized first principal component....The small singular values $d_j$ correspond to directions in the column space of $\bm{X}$ having small variance, and ridge regression shrinks these directions the most.

> Ridge regression protects against the potentially high variance of gradients estimated in the short directions. The implicit assumption is that the response will tend to vary most in the directions of high variance of the inputs.

P69
> Lasso does a kind of continuous subset selection.

P72 add later, consider the bayesian info here

P82
> Ridge regression shrinks all directions, but shrinks low-variance directions more. Principal components regression leaves $M$ high-variance directions alone, and discards the rest. Interestingly, it can be shown that partial least squares also tends to shrink the low-variance directions, but can actually inflate some of the higher variance directions.

P93 
> Least squares fitting is usually done via the Cholesky decomposition of the matrix $X^TX$ or a QR decomposition of $X$. With $N$ observations and $p$ features, the Cholesky decomposition requires $p^3+Np^2/2$ operations, while the QR decomposition requires $Np^2$ operations.