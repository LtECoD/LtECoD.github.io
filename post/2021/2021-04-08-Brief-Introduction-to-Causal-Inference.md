+++
hascode = false
date = Date(2021, 04, 08)
+++
@def tags = ["causalinference"]

# Brief Introduction to Causal Inference

\toc


## What is Causal Inference

Considering the following questions:

* Did the new tax taw cause sales to go up, or was it our advertising campaign.
* Could breakfast bring a lightweight?
* If I had quit smoking, would I still get lung cancer?

All this common questions have a concern with cause-and-effect relationships, recognizable through words such as "cause", "bring" and "get". Yet, until very recently, science gave  us no means even to articulate, let alone answer,them. Causal inference is the science solves this problem in mathematical language[[1]](#R1).

Then, what is causal inference? There is no widely accepted definition of causal inference so far. Here, I cite several unverified definitions from published papers:
>Generally speaking, the task of causal inference is to estimate the **outcome changes** if another treatment had been applied.[[2]](#R2)

>Causal inference refers to an intellectual discipline that considers the assumptions, study designs, and estimation strategies that allow researchers to draw **causal conclusions (effects)** based on data. [[3]](#R3)

>Causal inference is a complex scientific task that relies on triangulating evidence from multiple sources and on the application of a variety of methodological approaches.[[4]](#R4)

The author in [[4]](#R4) also stress no book can possibly provide a comprehensive description of methodologies for causal inference across the sciences and any Causal Inference books will have to choose which aspects of causal inference methodology they want to emphasize.

From the above definitions, we can draw a simple conclusion: the subjects of causal inference is the cause variable(s) and effect variable(s), and it attempts to quantitively estimate the influence of cause variable(s) to effect variable(s).

## Why We Need Causal Inference

A natural question is why we need causal inference, or can't existing scientific methods solve the causal problems? It seems that the above causal problems can be solved using probabilistic methods, such as conditional probability, Bayesian network or any others, as long long they can measure the correlation. But, it has been long declared that **correlation doesn't imply causation**,

### Correlation Doesn't Imply Causation 

Why correlation can not represent causation? What is the difference between these two concepts? Both of them describe relationship between variables, but correlation indicates a more general relation than causation. When we say two variables are correlated, we actually means these two variables display an increasing or decreasing trend. However, such trend can not prove the existence of causation. Compared to correlation, causation involves cause and effect. When we adjust cause variables, effect variables will change also. But the opposite could not hold, i.e., when we change the effect variables, the cause variables may not changes at all. This property does not necessarily hold in correlation. From this view, causation can been seen as a subset of correlation in some degree. Below is a good example to distinct causation and correlation:

>Say you happen upon some data that relates wearing shoes to bed and waking up with a headache, as one does. It turns out that most times that someone wears shoes to bed, that person wakes up with a headache [[5]](#R5). 

Can we say wearing shoes causes waking up with a headache, or, if I wear shoes to bed, I will probably wake up with headache? Anyway, such conclusions doesn't make sense at all since waring shoes has nothing to do with a headache in our mind. Actually, waring shoes and waking up with a headache are related because they have a common cause, i.e., drinking the night before.

~~~
<div align="center">
<img src="/assets/2021/drunksleeping.png" style="width:25%;"/>
</div>
~~~

More real instances indicating "correlation doesn't imply causation" can be found in an interesting website [*Spurious Correlation*](https://www.tylervigen.com/spurious-correlations). For example, number of people who drawn by falling into a pool is correlated with films Nicolas Cage appeared in with correlation ratio 66.6%.

~~~
<img src="/assets/2021/nicholascage.svg" style="width:80%;"/>
~~~

Us spending on science, space and technology is correlated with suicides by hanging, strangulation and suffocation with correlation ratio 99.79%.

~~~
<img src="/assets/2021/usspendinghanging.svg" style="width:80%;"/>
~~~

Divorce rate in Maine is correlated with per capita consumption of margarine with correlation ratio 99.26%.

~~~
<img src="/assets/2021/divorcerate.svg" style="width:80%;"/>
~~~

All these instances illustrate that the correlation between two variables can not imply the existence of causation, no matter how high is the correlation ratio.

## What Problems Does Causal Inference Solve?

The answer of this question can be found in [The Book of Why](#R1). Specifically, Judea Pearl introduces the ladder of causation (see my blog [Summary of *The Book of Why*: Chapter 01](/post/2021/2021-04-09-The-Book-of-Why-Summary-Chapter01/)), and specify some typical questions as well as the task of each rung. But the task description of causal inference in this book is a little obscuring to me. Then I found a more concise task description of causal inference in a survey paper [[2]](#R2):

> For causal inference, our objective is to estimate the treatment effects from the observational data.

**Treatment effect** in this sentence seems unfamiliar. Roughly speaking, it measures the influence amount of one action to the target. It will be introduced in detail in the subsequent blogs. *P.S. So far, I agree more with this description, because it is more intuitive. If I have a deeper understanding to the target fo causal inference in the future, I will update this blog.*


## Applications


### Pearson Paradox





## Causal Inference Frameworks

The potential outcome framework aims to **estimate potential outcomes and then calculate the treatment effect**. Therefore, the treatment effect estimation is one of the central problems in causal inference under the potential outcome framework. The structural model framework describes the causal mechanisms of a system **where a set of variables and the causal relationship among them are modeled by a set of simultaneous structural equations**. This blog will provide a detailed introduction of the potential outcome framework.



## References
~~~
<div><a name="R1"></a>
[1] Pearl J,  Mackenzie D. The book of why : the new science of cause and effect. 2018.
</div>
<div><a name="R2"></a>
[2] Yao, L. , et al. "A Survey on Causal Inference." (2020).
</div>
<div><a name="R3"></a>
[3] Jennifer Hill, Elizabeth A. Stuart. Casual Inference: Overview[M]//International Encyclopedia of the Social & Behavioral Sciences (Second Edition). 2015.
</div>
<div><a name="R4"></a>
[4] Miguel A. Hernán, James M. Robins. Casual Inference: What If. Harvard University. 2020
</div>
<div><a name="R5"></a>
[5] Brady Neal. Introduction to Casual Inference. 2021
</div>
~~~


