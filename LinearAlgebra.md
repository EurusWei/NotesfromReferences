P87
> 1. Gauss-Jordan: Multiply $[\boldsymbol{A} \boldsymbol{I}]$ by $\boldsymbol{A}^{-1}$ to get $[\boldsymbol{I} \boldsymbol{A}^{-1}]$.
> 2. The inverse of a band matrix is generally a dense matrix.

P89
> 1. $\boldsymbol{A}^{-1}$ exists exactly when  $\boldsymbol{A}$ has $n$ pivots. (A triangular matrix is invertible if and only if no diagonal entries are zero.)
> 2. Diagonally dominant matrices are invertible, i.e., $|a_{ii}|>\sum_{i\neq j}|a_{ij}|$, because for any non-zeros $\boldsymbol{x}$, $\boldsymbol{Ax}=0$ is impossible (think about the row with largest $|x_i|$). 

P97
> $\boldsymbol{A}=\boldsymbol{LU}=(lower triangular)(upper triangular).$
> Elimination on $\boldsymbol{Ax}=\boldsymbol{b}$ reaches $\boldsymbol{Ux}=\boldsymbol{c}$. The back-substitution solves $\boldsymbol{Ux}=\boldsymbol{c}$.

P98
> In the decomposition $\boldsymbol{A}=\boldsymbol{LU}$, there is no row exchanges, the upper triangular $\boldsymbol{U}$ has the pivots on its diagonal, the lower triangular $\boldsymbol{L}$ has all $1$'s on its diagonal.
> A further breakdown is $\boldsymbol{A}=\boldsymbol{LDU}$, where $\boldsymbol{D}$ is a diagonal matrix that contains the pivots.

P101 -- go back to review the cost computation

P108
> The inverse of a lower triangular matrix is still lower triangular.

P109 
> $\boldsymbol{Ax}$ combines the columns of $\boldsymbol{A}$ while $\boldsymbol{x}^T\boldsymbol{A}^T$ combines the rows of $\boldsymbol{A}^T$.

P111
> Even if $m=n$, it is very likely that $\boldsymbol{A}^T\boldsymbol{A}\neq\boldsymbol{A}\boldsymbol{A}^T$. Equality can happen, but it is abnormal.

P112
> If $\boldsymbol{S}=\boldsymbol{S}^T$ is factored into LDU with no row changes, then $\boldsymbol{U}$ is exactly $\boldsymbol{L}$.

> A single row exchange is its own inverse. More import: $\boldsymbol{P}^{-1}$ is always the same as $\boldsymbol{P}^T$.

P126
> The system $Ax=b$ is solvable if and only if $b$ is in the column space of $A$.

> Suppose $A$ is an $m$ by $n$ matrix. If columns have $m$ components (not $n$). So the columns belong $\mathbb{R}^m$ (not $\mathbb{R}^n$).



https://homepages.uc.edu/~herronda/linear_algebra/beamers/Chpt6Sect1OC-H.pdf

