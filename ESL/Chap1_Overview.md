## Chapter 1
P15 effective number of parameters for KNN
> It appears that $k$-nearest-neighbor fits have a single parameter, the number of neighbors $k$, compared to the $p$ parameters in least-squares fits. Although this is the case, we will see that the effective number of parameters of $k$-nearest-neighbors is $N/k$ and is generally bigger than $p$, and decreases with increasing $k$. To get an idea of why, note that if the neighborhoods were overlapping, there would be $N/k$ neighborhoods and we would fit one parameter (a mean) in each neighborhood.

P16 
> The linear decision boundary from least squares is very smooth, and apparently stable to fit. It does appear to rely heavily on the assumption that a linear decision boundary is appropriate, i.e., low variance and potentially high bias...KNN has high variance and low bias (variance due to sampling variance).

P22 ~ 23 
> Since this corresponds to a fraction $r$ of the unit volume, the expected edge length will be $e_p(r)=r^{1/p}$. In ten dimensions $e_{10}(0.01)=0.63$ and $e_{10}(0.1)=0.80$, while the entire range for each input is only $1.0$. So to capture $1\%$ or $10\%$ of the data to form a local average, we must cover $63\%$ or $80\%$ of the range of each input variable. Such neighborhoods are no longer "local"... Another consequance of the sparse sampling in high dimensions is that all sample points are close to an edge of the sample. Consider $N$ data points uniformly distributed in a $p$-dimensional unit ball centered at the origin. Suppose we consider a nearest-neighbor estimate at the origin. The median distance from the origin to the closest data point is given by the expression $d(p, N)=(1 - (1/2)^{1/N})^{1/p}$...For $N=500,p=10,d(p,N)\approx 0.52$, more than halfway to the boundary. Hence more data points are close to the boundary of the sample space than to any other data point. The reason that this presents a problem is that prediction is much more difficult near the edges of the training sample. One must extrapolate from neighboring sample points rather than interpolate between them....Another manifestation of the curse is that the sampling density is proportional to $N^{1/p}$.

P28
> The additive model assumes that we can capture all those departures from a deterministic relationship with error $\epsilon$.

P31
> The principle of maximum likelihood assumes that the most reasonable values for $\theta$ are those for which the probability of the observed sample is largest.

P33
> And conversely, all methods that overcome the dimensionality problems have an associated-and often implicit or adaptive-metric for measuring neighborhoods, which basically does not allow the neighborhood to be simultaneously small in all directions.

P34 
> Kernal methods and local regression can be thought of as explicitly providing estimates of the regression function or conditional expectation by specifying the nature of the local neighborhood, and of the class of regular functions fitted locally.

P35
> More generally, as the model complexity of our procedure is increased, the variance tends to increase and the squared bias tends to decrease.