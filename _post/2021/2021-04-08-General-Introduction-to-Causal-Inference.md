+++
title = "General-Introduction-to-Causal-Inference"
hascode = false
date = Date(2021, 04, 08)
+++
@def tags = ["causalinference", "datascience"]

# General Introduction to Causal Inference

\toc



## What Problems Does Causal Inference Solve?
In my opinion, the preliminary of studying someone theory or technology is to understand what problems does it aims to solve. So, I want to summarize the targets of Casual Inference (CI) firstly.

There is no doubt `causality` is the core issue of CI. It has been long declared that **Causality doesn't mean correlation**, but what is the difference between these two concepts. Actually, correlation indicates a more general relation than causality, and when we say two variables are correlated, we actually means that these two variables display an increasing or decreasing trend. Compared to correlation, causality involves cause and effect. When we adjust cause variables, effect variables will change also. But the opposite doesn't hold, i.e., when we change the effect variables, the cause variables may not changes at all. From this view, causality can been seen as a subsect of correlation in some degree. Below is a good example to distinct casuality and correlation:

>A study showed that girls have breakfast normally have lightweight than the girls who don’t, and thus concluded that having breakfast can help to lose weight. But in fact, these two events may just have correlation instead of causality. Maybe the girls who have breakfast everyday have a better lifestyle, such as exercise frequently, sleep regularly, and have a healthy diet, which finally makes them have lightweight. In this case, having a better lifestyle is the common cause of both having breakfast and lightweight, and thus we also can treat it as a confounder of the causality between having breakfast and lightweight.[1]

Ok, after figuring out the difference between causality and correlation, the following question is what can causal inference do?



## Definitions

The potential outcome framework aims to **estimate potential outcomes and then calculate the treatment effect**. Therefore, the treatment effect estimation is one of the central problems in causal inference under the potential outcome framework. The structural model framework describes the causal mechanisms of a system **where a set of variables and the causal relationship among them are modeled by a set of simultaneous structural equations**. This blog will provide a detailed introduction of the potential outcome framework.



## References

[1] Yao, L. , et al. "A Survey on Causal Inference." (2020).