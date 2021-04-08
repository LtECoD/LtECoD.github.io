+++
title = "General-Introduction-to-Causal-Inference"
hascode = false
date = Date(2021, 04, 08)

+++
@def tags = ["causalinference", "datascience"]

# General Introduction to Causal Inference

\toc



## Correlation Doesn't Imply Causality

One natural question about causal inference is why we need it? 



There is no doubt **causality** is the core issue of CI. It has been long declared in many writings that **Correlation doesn't imply causality**, then what is the difference between these two concepts. Both of them describe relationship between variables, but correlation indicates a more general relation than causality. When we say two variables are correlated, we actually means these two variables display an increasing or decreasing trend. Compared to correlation, causality involves cause and effect. When we adjust cause variables, effect variables will change also. But the opposite could not hold, i.e., when we change the effect variables, the cause variables may not changes at all. From this view, causality can been seen as a subsect of correlation in some degree. Below is a good example to distinct casuality and correlation:

>A study showed that girls have breakfast normally have lightweight than the girls who don’t, and thus concluded that having breakfast can help to lose weight. But in fact, these two events may just have correlation instead of causality. Maybe the girls who have breakfast everyday have a better lifestyle, such as exercise frequently, sleep regularly, and have a healthy diet, which finally makes them have lightweight. In this case, having a better lifestyle is the common cause of both having breakfast and lightweight, and thus we also can treat it as a confounder of the causality between having breakfast and lightweight.[1]

 Ok, after figuring out the difference between causality and correlation, the following question is what does causal inference do with causality.

## What Problems Does Causal Inference Solve?
 In [the book of why](#R1), Judea Pearl introduces the ladder of causality. The bottom of this ladder is seeing (association). The agent in this level can only learn the association of data to make various prediction, such as classification and regression. Therefore, it only focus on the correlation between variables without caring about the causality, which is the issue of the latter two levels of the ladder. Today artificial intelligence belongs to this level.  A classical example in NLP of agent in this level is the language model that model the text by capturing the occurrence of n-grams or tokens.

~~~
<img src="/assets/2021/ladderofcausal.png" style="scale:10%"/>
~~~

The second level of the ladder is doing (intervention). The author strenthened in the book the agent in this level can predict what will happen if it does something. Agent in the third level of the ladder, which named imagining (counter factual), can even image what will happen if it have done something. Anyway, these two level still seem confused to me. For example, *does the agent in these two level need interact with the real-world to learn the causality or just from the observed data. If it needs interaction with the real-world, then how?* 

Then I found a concise description of the target of causal inference in a [survey paper](#R2):

> For causal inference, our objective is to estimate the treatment effects from the observational data.

**Treatment effect** in this sentence seems unfamilar. Roughly speaking, it measures the influence amount of one action to the target. I will introduce this concept as well as other in detail in the subsequent blogs. 

For now, I agree more with this description, because it is more intuitive. 
~~~
<u>If I have a deeper understanding to the target fo causal inference in the future, I will update this blog.</u>
~~~


## Applications

Another question about



### Pearson Paradox





## Causal Inference Frameworks

The potential outcome framework aims to **estimate potential outcomes and then calculate the treatment effect**. Therefore, the treatment effect estimation is one of the central problems in causal inference under the potential outcome framework. The structural model framework describes the causal mechanisms of a system **where a set of variables and the causal relationship among them are modeled by a set of simultaneous structural equations**. This blog will provide a detailed introduction of the potential outcome framework.



## References
~~~
<div><a name="R1"></a>
[1] Pearl J ,  Mackenzie D . The book of why : the new science of cause and effect. 2018.
</div>
<div><a name="R2"></a>
[2] Yao, L. , et al. "A Survey on Causal Inference." (2020).
</div>
~~~


