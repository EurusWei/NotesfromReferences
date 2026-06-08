**Conditional independence assumption**: $(Y_0, Y_1)\perp T|X$ 

By CIA, $ATE=\sum_x\{E[Y|T=1,X=x]P(X=x)-E[Y|T=0,X=x]P(X=x)\}$, i.e., the average treatment effect can be identified as the weighted average of in-group differences between treated and control

Confounder: an open backdoor path through which association flows noncausally, e.g., common cause to the treatment and control