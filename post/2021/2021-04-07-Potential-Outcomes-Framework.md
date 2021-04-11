+++
hascode = false
date = Date(2021, 04, 07)
+++
@def tags = ["causalinference"]

# Potential Outcomes Framework

\toc

🚧


## Definitions

The potential outcome framework aims to **estimate potential outcomes and then calculate the treatment effect**. Therefore, the treatment effect estimation is one of the central problems in causal inference under the potential outcome framework. The structural model framework describes the causal mechanisms of a system **where a set of variables and the causal relationship among them are modeled by a set of simultaneous structural equations**. This blog will provide a detailed introduction of the potential outcome framework.

As mentioned above, the potential out framework is to estimate potential outcomes and calculate the treatment effect. There are several key concepts in the potential outcome framework.

1. `Unit` is the atomic research object in the treatment effect study. For example, when we want to calculate the treatment effect of smoking on lung cancer, a unit is a *person*.

2. `Treatment` refers to an action applied to a unit. Still taking smoking as an example, the treatment is smoking or not smoking. Note that treatment is not always discrete. It can also be continuous.

3. `Potential outcome` is the outcome of a treatment that was applied to a unit.

4. `Treatment effect` is the gap of potential outcomes between two treatments. The treatment effect can be calculated in different levels, for example in the unit-level (named *Individual Treatment Effect, ITE*) and in the population-level(named *Average Treatment Effect, ATE*).

To better illustrate the above definitions, we use symbolics to represent them. Specifically, 







## References

[1] Yao, L. , et al. "A Survey on Causal Inference." (2020).