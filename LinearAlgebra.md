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

**R**: a good visualization of dimensions of column space and nullspace can be found in: https://homepages.uc.edu/~herronda/linear_algebra/beamers/Chpt6Sect1OC-H.pdf

P138
> Suppose $Ax=0$ has more unknowns than equations ($n > m$, more columns than rows). There must be at least one free column. Then $Ax=0$ has nonzero solutions. 

> The nullspace if a subspace. Its dimension is the number of free variables.

> The rank of $\boldsymbol{A}$ is the nuber of pivots.

### 3.3
- Every matrix $\boldsymbol{A}$ with full column rank ($r=n$) have no free variables, the nullspace $N(\boldsymbol{A})$ contains only the zero vector $\boldsymbol{x}=\boldsymbol{0}$. If $\boldsymbol{Ax}=\boldsymbol{b}$ has a solution, it is the only solution (**R**: too many hyperplanes, and there is a solution iff these hyperplanes intersect to one point)
- For every matrix $\boldsymbol{A}$ with full row rank ($r=m$), the column space is the whole space $\mathbb{R}^m$, and $\boldsymbol{Ax}=\boldsymbol{b}$ has a solution for every $\boldsymbol{b}$ (**R**: too few hyperplanes, which result in another hyperplane with many solutions)

### 4.1
- $N(\boldsymbol{A})$ is orthogonal to $C(\boldsymbol{A}^T)$ in $\mathbb{R}^n$
- $N(\boldsymbol{A}^T)$ is orthogonal to $C(\boldsymbol{A})$ in $\mathbb{R}^m$

### 4.2
- Projection matrix for projecting onto the subspace spanned by $\boldsymbol{A}$ is $\boldsymbol{A}(\boldsymbol{A}^T\boldsymbol{A})^{-1}\boldsymbol{A}^T$, and for projecting onto a line is $\frac{\boldsymbol{a}\boldsymbol{a}^T}{\boldsymbol{a}^T\boldsymbol{a}}$
- The matrix $\boldsymbol{A}^T\boldsymbol{A}$ has the same nullspace as $\boldsymbol{A}$

### 4.4
Gram-Schmidit process factorizes $\boldsymbol{A}=\boldsymbol{QR}$ into an orthonormal matrix and an upper triangular matrix.

### 5.1
- The determinant is not changed by the usual elimination steps from $\boldsymbol{A}$ to $\boldsymbol{U}$
- The determinant of $\boldsymbol{AB}$ is $|\boldsymbol{A}||\boldsymbol{B}|$
- $|\boldsymbol{A}^T|=|\boldsymbol{A}|$

### 5.2
- Cramer's rule solves $\boldsymbol{Ax}=\boldsymbol{b}$ by determinants (when $\boldsymbol{A}$ is not singular): $x_1=|\boldsymbol{B}_1|/|\boldsymbol{A}|$,...,$x_n=|\boldsymbol{B}_j|/|\boldsymbol{A}|$, where the matrix $\boldsymbol{B}_j$ has the $j_{th}$ column of $\boldsymbol{A}$ replaced by the vector $\boldsymbol{b}$
- $\boldsymbol{A}^{-1}=\boldsymbol{C}^T/|\boldsymbol{A}|$

## Chapter 6
- The eigenvectors of $\boldsymbol{A}$ span the nullspace of $\boldsymbol{A}-\lambda\boldsymbol{I}$
- By the property of eigenvalues and eigenvectors, $\boldsymbol{AX}=\boldsymbol{X\Lambda}$, and $\boldsymbol{A}=\boldsymbol{X\Lambda}\boldsymbol{X}^{-1}$. Any matrix that has no repeated eigenvalues can be diagonalized, since eigenvectors that correspond to distinct eigenvalues are linearly independent (TBD if the matrix has repeated eigenvalues)
- Matrices $\boldsymbol{A}=\boldsymbol{BC}\boldsymbol{B}^{-1}$ are similar to $\boldsymbol{C}$, and shall the same eigenvalues. The central idea of similarity is to make $\boldsymbol{A}$ as simple as possible while preserving the essential properties
- Eigenvectors can help to easily find Fibonacci number: portray the problem as $\boldsymbol{u}_{n+1}=\boldsymbol{A}\boldsymbol{u}_n$, and factor $\boldsymbol{u}_0$ as a linear combination of eigenvectors
- A symmetric matrix $\boldsymbol{S}$ has real eigenvalues and orthonormal eigenvectors, and can be diagonalized as $\boldsymbol{S}=\boldsymbol{Q\Lambda}\boldsymbol{Q}^T=\lambda_1\boldsymbol{q}_1\boldsymbol{q}_1^T+...+\lambda_n\boldsymbol{q}_n\boldsymbol{q}_n^T$
- A positive definite matrix $\boldsymbol{S}$ is symmetric and having all positive eigenvalues. If the columns of $\boldsymbol{A}$ are independent, then $\boldsymbol{S}=\boldsymbol{A}^T\boldsymbol{A}$ is positive definite

## Chapter 7
The SVD decomposes a matrix as $\boldsymbol{A}=\boldsymbol{UD}\boldsymbol{V}^T=\sigma_1\boldsymbol{u}_1\boldsymbol{v}_1^T+...+\sigma_r\boldsymbol{u}_r\boldsymbol{v}_r^T$. Here $\boldsymbol{A}$ is a rectangular matrix with dimension $m\times n$.
- $\boldsymbol{U}=(\boldsymbol{u}_1,...,\boldsymbol{u}_r,\boldsymbol{u}_{r+1},\boldsymbol{u}_m)$, where the first $r$ vectors is an orthonormal basis for $C(\boldsymbol{A})$, the rest spans $N(\boldsymbol{A}^T)$. The first eigenvectors $\boldsymbol{u}_1$ points in the most significant direction of the data, and accounts for a fraction $\sigma_1^2/T$ of the total variance
- $\boldsymbol{D}=(\sigma_1,...,\sigma_r,0,...,0)$, each $\sigma_i^2$ is an eigenvalue of $\boldsymbol{A}\boldsymbol{A}^T$ and $\boldsymbol{A}^T\boldsymbol{A}$. $\sigma_1$ is the norm of matrix $\boldsymbol{A}$
- $\boldsymbol{V}=(\boldsymbol{v}_1,...,\boldsymbol{v}_r,\boldsymbol{v}_{r+1},\boldsymbol{u}_n)$, where the first $r$ vectors is an orthonormal basis for $C(\boldsymbol{A}^T)$, the rest spans $N(\boldsymbol{A})$
Note that singular values are more stable than eigenvalues. Let $\boldsymbol{S}=\boldsymbol{A}^T\boldsymbol{A}$, then singular values are ordered ratios of the Rayleign quotient $\frac{\boldsymbol{x}^T\boldsymbol{Sx}}{\boldsymbol{x}^T\boldsymbol{x}}$.
- Every real square matrix can be factored into $\boldsymbol{A}=\boldsymbol{UV}^T\boldsymbol{V\Sigma V}^T=\boldsymbol{QS}$, where $\boldsymbol{Q}$ is orthogonal and $\boldsymbol{S}$ is symmetric positive semidefinite
- In general, the pseudoinverse of $\boldsymbol{A}$ is $\boldsymbol{A}^{+}=\boldsymbol{V\Sigma}^{+}\boldsymbol{U}^T$, where the component matrices have dimensions $n\times n, n\times m, m\times m$, respectively
- If $\boldsymbol{A}$ is singular, geometrically, $\boldsymbol{Ax}=\boldsymbol{b}$ has infinitely many solutions. The pseydoinverse gives the shortest solution as $\boldsymbol{x}^{+}=\boldsymbol{A}^{+}\boldsymbol{b}$

## Chapter 8
- For a transformation $T:\mathbb{R}^n\rightarrow\mathbb{R}^n$, its matrix $\boldsymbol{A}$, which is in general not diagonal when using the standard basis. If choosing the $n$ independent eigenvectors (if exist) as the input and the output basis, then the matrix for $T$ is the diagonal eigenvalue matrix $\Lambda$
- $\boldsymbol{C}=\boldsymbol{Q}_1^{-1}\boldsymbol{AQ}_2$ is isometric to $\boldsymbol{A}$ if $\boldsymbol{Q}_1$ and $\boldsymbol{Q}_2$ are orthogonal, and gives the transformation matrix in new bases. When $\boldsymbol{Q}_1,\boldsymbol{Q}_2$ have different choices, $\boldsymbol{C}$ has different meanings:

|              $\boldsymbol{Q}_1$              |              $\boldsymbol{Q}_2$              |       $\boldsymbol{C}$       |
| :------------------------------------------: | :------------------------------------------: | :--------------------------: |
|               $\boldsymbol{X}$               |               $\boldsymbol{X}$               |    $\boldsymbol{\Lambda}$    |
|               $\boldsymbol{U}$               |               $\boldsymbol{V}$               |    $\boldsymbol{\Sigma}$     |
| generalized eigenvectors of $\boldsymbol{A}$ | generalized eigenvectors of $\boldsymbol{A}$ | Jordan form $\boldsymbol{J}$ |
- 