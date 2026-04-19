## Chapter 1 First order equations
### 1.4
Consider the differential equation $\frac{dy}{dt}=ay+q(t)$ with $y(0)$, the general form of the solution is $y(t)=e^{at}y(0)+e^{at}\int_0^te^{-as}q(s)ds$ (solved by multiplying both sides by $e^{-at}$). When the input source $q(t)$ is 
- constant
- step function at $T$
- delta function at $T$
- exponential
the form can be further simplified.

### 1.5
Consider the differential equation $\frac{dy}{dt}=ay+e^{ct}$ with $y(0)$. When $c$ is an imaginary number, $\frac{dy}{dt}-ay=q(t)=Acoswt+Bsinwt=Rcos(wt-\phi)$, one way is to solve $A,B$ directly, or the following steps are applied: 
1. solve $\frac{dy}{dt}-ay=q(t)=Re^{iwt}$ with the complex solution $y_c=Re^{i(wt-\phi)}/(iw-a)$
2. take the real part of $y_c$

### 1.6
Consider the differential equation $\frac{dy}{dt}=ay+q(t)$ with $y(0)$, the final solution is generalized as $y(t)=G(0,t)y(0)+\int_0^tG(s,t)q(s)ds$ ($y_n+y_p$),
1. when $a$ is constant, one important way to understand the solution is that the input $q(s)$ grows to $e^{a(t-s)}q(s)$ in the time between $s$ and $t$ with the growth factor $G(s,t)=e^{a(t-s)}$, and the integral of this part contributes to the output
2. if $a(t)$ changes with time $t$, the growth factor $G(s,t)=e^{\int_s^ta(T)dT}$

### 1.7
Consider the differential (logistic) equation $\frac{dy}{dt}=ay-by^2$, the solution is $y(t)=frac{a}{de^{-at}+b}$, which can be obtained by partial fractions.

The logistic equation is autonomous, i.e., $\frac{dy}{dt}=f(y)$ that depends only on $y$. The steady states $Y$ are solutions when $f(Y)=0$, and $Y$ are stable if $df/dy<0$ at $y=Y$.

### 1.8
1. separable equations $f(y)dy=g(t)dt$
2. exact equations $dy/dt=g(y,t)/f(y,t)$ when $\frac{\partial f}{\partial t}=-\frac{\partial g}{\partial y}$, the solution steps are
	- integrate $f$ w.r.t. $y$ as $\int f(y,t)dy=F(y,t)+C(t)$
	- choose $C(t) such that $\frac{\partial}{\partial t}(F(y,t) + C(t))=-g(y,t)$ (this is possible when the exactness condition is met)
	- the solution is $F(y,t)+C(t)=constant$

## Chapter 2 Second order equations

### 2.1
Consider the fundamental equation of mechanics $m\frac{d^2y}{dt^2}+ky=0$, the unforced oscillation is $y(t)=y(0)coswt+\frac{y'(0)}{w}sinwt$ with $w=\sqrt{k/m}$.

The frequency response for $m\frac{d^2y}{dt^2}+ky=coswt$ is $y_p(t)=\frac{1}{k-mw^2}coswt=\frac{1}{m(w_n^2-w^2)}coswt$. 

The impulse response (fundamental solution) for $m\frac{d^2g}{dt^2}+kg=\delta(t)$ with zero initial conditions is $g=e^{at}$, which is also the null solution when $g(0)=0$ and $g'(0)=\frac{1}{m}$.

$g(t)$ solves the equation for any forcing equation $f(t)$, i.e., $m\frac{d^2y}{dt^2}+ky=f(t)$ has $y_p(t)=\int_0^tg(t-s)f(s)ds$.

### 2.3
Consider the differential equation $A\frac{d^2y}{dt^2}+B\frac{dy}{dt}+Cy=0$ starting from $y(0)$ and $y'(0)$, it has the characteristic equation $As^2+Bs+C=0$. $B^2>,=,<4AC$ correspond to overdamping, critical damping, underdamping. If $B=0$, the system has no damping.

The impulse response (fundamental solution) for $A\frac{d^2g}{dt^2}+B\frac{dg}{dt}+Cg=\delta(t)$ is $g=\frac{e^{s_1t}-e^{s_2t}}{A(s_1-s_2)}$, which is also the null solution when $g(0)=0$ and $g'(0)=\frac{1}{A}$. Similarly, $g$ gives all other solutions: $y_p(t)=\int_0^tg(t-s)f(s)ds$.

### 2.4
For the differential equation $A\frac{d^2y}{dt^2}+B\frac{dy}{dt}+Cy=e^{st}$, first obtain the null solutions, then $y_p=\frac{1}{As^2+Bs+C}e^{st}$, the complete solutions is $y_n+y_p$. 

For the differential equation $A\frac{d^2y}{dt^2}+B\frac{dy}{dt}+Cy=e^{iwt}$, first obtain the null solutions, then $y_p=\frac{1}{A(iw)^2+B(iw)+C}e^{iwt}=Ge^{-i\alpha}$, the complete solutions is $y_n+y_p$. 

When the differential equation has higher orders, use the similar logic to find the particular solution. If resonance exists, then $y_p=\frac{t e^{ct}}{P'(c)}$, when $P(c)$ is the characteristic function.

### 2.7
The Laplace transform of $f(t)$ is $F(s)=\int_0^{\infty}f(t)e^{-st}dt$. One way to solve the differential equation, is to transform left and right side of the equation and obtain $Y(s)$, and then back engineering (such as using partial fractions) to find $y(t)$ with the Laplace transform $Y(s)$.

The correspondence between functions and their Laplace transforms are listed below:

| functions                  | Laplace transform                                   |
| -------------------------- | --------------------------------------------------- |
| $dy/dt$                    | $sY(s)-y(0)$                                        |
| $dy^2/d^2t$                | $s^2Y(s)-sy(0)-y'(0)$                               |
| $1,t,t^2$                  | $1/s,1/s^2,2/s^3$                                   |
| $e^{at},te^{at},t^2e^{at}$ | $\frac{1}{s-a},\frac{1}{(s-a)^2},\frac{1}{(s-a)^3}$ |
| $coswt,sinwt$              | $\frac{s}{s^2+w^2},\frac{w}{s^2+w^2}$               |
| $e^{at}coswt,e^{at}sinwt$  | $\frac{s-a}{(s-a)^2+w^2},\frac{w}{(s-a)^2+w^2}$     |

## Chapter 3

### 3.2
This chapter discusses about the visualization of differential equation solutions. The correspondence between roots order and solution types are listed as below:

| order of roots                                   | types                   |
| ------------------------------------------------ | ----------------------- |
| $s_1>s_2>0$                                      | source: unstable        |
| $s_1<s_2<0$                                      | sink: stable            |
| $s_2<0<s_2$                                      | saddle: unstable        |
| $a=Res>0$ (this and below are for complex roots) | spiral source: unstable |
| $a=Res<0$                                        | spiral sink: stable     |
| $a=Res=0$                                        | center: neurally stable |
### 3.3
To get the linearization and stability in 2D and 3D, similarly, consider the equations $(y,z)'=(f,g)$, the steady state is $(Y,Z)$ when $f(Y,Z)=g(Y,Z)=0$. Then near the steady state, $f(y,z)\approx(\partial f/\partial y)(y-Y)+(\partial f/\partial z)(z-Z)$, and $g$ has a similar approximation. These derivatives of $f,g$ go in a $2\times 2$ matrix $\boldsymbol{A}$. The system $(y,z)'=(f,g)$ is stable at $Y,Z$ when $(y-Y,z-Z)'=\boldsymbol{A}(y-Y,z-Z)$ are stable, i.e., $\lambda_1,\lambda_2$ have real parts $<0$.

### 3.4-3.5
Some numerical methods:

| methods                                | details                                                                                                                                                                                       | error                  |
| -------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------- |
| Euler's method                         | $y_{n+1}^E=y_n+\Delta t f_n$                                                                                                                                                                  | $\sim \Delta t$        |
| Backward Eular                         | $\frac{y^B_{n+1}-y_n}{\Delta t}=f(t_{n+1},y^B_{n+1})$                                                                                                                                         | more stable but slower |
| Improved Eular, simplified Runge-Kutta | $\frac{y^S_{n+1}-y_n}{\Delta t}=f(t_n,y_n)/2+f(t_{n+1},y^E_{n+1})/2$                                                                                                                          |                        |
| Fourth order Runge-Kutta               | $k_1=f(t_n,y_n)/2$, $k_2=f(t_{n+1/2},y_n+\Delta k_1)/2$, $k_3=f(t_{n+1/2},y_n+\Delta k_2)/2$, $k_4=f(t_{n+1/2},y_n+2\Delta k_3)/2$, $\frac{y^{RK}_{n+1}-y_n}{\Delta t}=(k_1+2k_2+2k_3+k_4)/3$ | $\sim(\Delta t)^4$     |

## Chapter 6
### 6.3
Consider a first order linear system $d\boldsymbol{y}/dt=\boldsymbol{A}\boldsymbol{y}+\boldsymbol{q}$. If $\boldsymbol{A}$ is a constant matrix, then
- find out eigenvalues $\lambda_1,...,\lambda_n$, eigenvectors $\boldsymbol{x}_1,...,\boldsymbol{x}_n$ of $\boldsymbol{A}$, express the initial condition as a linear combination of eigenvectors, i.e., $\boldsymbol{y}(0)=c_1\boldsymbol{x}_1+...+c_n\boldsymbol{x}_n$
- the output is $\boldsymbol{y}(t)=c_1e^{\lambda_1 t}\boldsymbol{x}_1+...+c_ne^{\lambda_n t}\boldsymbol{x}_n$
Higher order equations can also be expressed in the matrix form.

### 6.4
Matrix exponential: $e^{\boldsymbol{At}}=\boldsymbol{I}+\boldsymbol{At}+(\boldsymbol{At})^2/2+...=\sum_{n=0}^{\infty}((\boldsymbol{At})^n)/n!=\boldsymbol{V}e^{\boldsymbol{\Lambda t}}\boldsymbol{V}^{-1}$. The solution to $d\boldsymbol{y}/dt=\boldsymbol{A}\boldsymbol{y}$ is $\boldsymbol{y}=e^{\boldsymbol{At}}\boldsymbol{y}(0)$. The solution to $d\boldsymbol{y}/dt=\boldsymbol{A}\boldsymbol{y}+\boldsymbol{q}$ is $\boldsymbol{y}=e^{\boldsymbol{At}}\boldsymbol{y}(0)+\int_0^te^{\boldsymbol{A}(t-s)}\boldsymbol{q}(s)ds$.

Every matrix $\boldsymbol{B}=\boldsymbol{V}^{-1}\boldsymbol{A}\boldsymbol{V}$ is similar to $\boldsymbol{A}$. They have the same eigenvalues. The eigenvectors change to $\boldsymbol{u}=\boldsymbol{V}^{-1}\boldsymbol{x}$.

## Chapters 7-8
- Heat equation: $\boldsymbol{u}_t=\boldsymbol{u}_{xx}$
- Laplace equation: $\frac{\partial^2\boldsymbol{u}}{\partial\boldsymbol{x}^2}+\frac{\partial^2\boldsymbol{u}}{\partial\boldsymbol{y}^2}=0$
- Poisson's equation: $\frac{\partial^2\boldsymbol{u}}{\partial\boldsymbol{x}^2}+\frac{\partial^2\boldsymbol{u}}{\partial\boldsymbol{y}^2}=f(\boldsymbol{x},\boldsymbol{y})$
- The Fourier functions $e^{ikx}$ are eigenfunctions for $d/dx$
- The discrete Fourier transform (DFT) replaces each continuous function by a vector of sampled points, i.e., $\boldsymbol{f}=\boldsymbol{Fc}$. The fast Fourier transform (FFT) factors $\boldsymbol{F}$ into sparse matrices, and reduces the number of computations from $N^2$ to $NL/2$ when $N=2^L$, $L$ is the number of levels.