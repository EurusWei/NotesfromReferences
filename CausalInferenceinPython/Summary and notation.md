**Fundamental problem of causal inference**: can not observe the same unit with and without treatment

**Difference between $E[Y|T]$ and $E[Y|do(T)]$**: the former measures the quantity on a selected subsample that actually accepts the treatment, the latter forces everyone to receive the treatment and measure the quantity for the entire sample

**Causal identification**: is about finding clever ways of removing bias and making the treated and untreated comparable so that all the difference you see can be attributed to the treatment effect

**Randomization**: ensures that people who get the treatment are comparable to those who don't 

Notation:
- individual treatment effect: $\tau_i=Y_i|do(T=t_1)-Y_i|do(T=t_0)$
- counterfactual: $Y_{ti}=Y_i|do(T_i=t)$
- average treatment effect (ATE): $E[\tau_i]=E[Y_{1i}-Y_{0i}]=E[Y|do(T=1)]-E[Y|do(T=0)]$
- average treatment effect on the treated (ATT): $E[Y_{1i}-Y_{0i}|T=1]$
- conditional average treatment effect (CATE): $E[Y_{1i}-Y_{0i}|X=x]$
- association between the treatment and outcome: $E[Y|T=1]-E[Y|T=0]$ 
	- causation is measured by $E[Y_1-Y_0]=E[Y|do(t=1)]-E[Y|do(t=0)]$
	- breakdown of association: $E[Y|T=1]-E[Y|T=0]=E[Y_1-Y_0|T=1]+\{E[Y_0|T=0]-E[Y_0|T=1]\}$, the first is ATT, the second is bias (how the treated and control group differ regardless of the treatment). If bias is zero, then association gives ATT
