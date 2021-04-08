+++
title = "Potential Outcomes Framework"
hascode = false
date = Date(2021, 04, 07)
+++
@def tags = ["causalinference", "datascience"]

# Potential Outcomes Framework

\toc

## What Problems Does Causal Inference Solve?
Potential outcome framework is one of two frameworks in Causal Inference (another is the structural model).

In my opinion, the preliminary of studying someone theory or technology is to understand what problems does it aims to solve. So, I want to summarize the targets of Casual Inference (CI) firstly.

There is no doubt `causality` is the core issue of CI. It has been long declared that **Causality doesn't mean correlation**, but what is the difference between these two concepts. Actually, correlation indicates a more general relation than causality, and when we say two variables are correlated, we actually means that these two variables display an increasing or decreasing trend. Compared to correlation, causality involves cause and effect. When we adjust cause variables, effect variables will change also. But the opposite doesn't hold, i.e., when we change the effect variables, the cause variables may not changes at all. From this view, causality can been seen as a subsect of correlation in some degree. Below is a good example to distinct casuality and correlation:

>A study showed that girls have breakfast normally have lightweight than the girls who don’t, and thus concluded that having breakfast can help to lose weight. But in fact, these two events may just have correlation instead of causality. Maybe the girls who have breakfast everyday have a better lifestyle, such as exercise frequently, sleep regularly, and have a healthy diet, which finally makes them have lightweight. In this case, having a better lifestyle is the common cause of both having breakfast and lightweight, and thus we also can treat it as a confounder of the causality between having breakfast and lightweight.[1]

Ok, after figuring out the difference between causality and correlation, the following question is what can causal inference do?



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