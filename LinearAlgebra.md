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

P134
> The nullspace $N(A)$ consists of all solutions to $Ax=0$. These vectors $\boldsymbol{x}$ are in $\mathbb{R}^n$.

P135
> Every matrix with $m<n$ has nonzero solutions to $Ax=0$ in its nullspace.

> The free components correspond to columns with no pivots. The special choice(one or zero) is only for the free variables in the special solutions. (RMK: from this we can see the dimension of $N(A)$ is $n-r$.)

P136
> When we add extra equations (giving extra rows), the nullspace certainly cannot become larger. The extra rows impose more conditions on the vectors $\boldsymbol{x}$ in the nullspace.

> Update pivot rows and divide the pivot row by its pivot don't change the zero vector on the RHS of the equation, so the nullspace stays the same: $N(A)=N(U)=N(R)$.

RMK: a good visualization of dimensions of column space and nullspace can be found in: https://homepages.uc.edu/~herronda/linear_algebra/beamers/Chpt6Sect1OC-H.pdf

P138
> Suppose $Ax=0$ has more unknowns than equations ($n > m$, more columns than rows). There must be at least one free column. Then $Ax=0$ has nonzero solutions. 

> The nullspace if a subspace. Its dimension is the number of free variables.

> The rank of $\boldsymbol{A}$ is the nuber of pivots.




