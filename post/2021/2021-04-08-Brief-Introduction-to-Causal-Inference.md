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

All these common questions have a concern with cause-and-effect relationships, recognizable through words such as "cause", "bring" and "get". Until very recently, science gave us no means to even articulate, let alone answer, them. Causal inference is the science that solves this problem in mathematical language[[1]](#R1).

Then, what is causal inference? There is no widely accepted definition of causal inference so far. Here, I cite several unverified definitions from published papers:
>Generally speaking, the task of causal inference is to estimate the **outcome changes** if another treatment had been applied.[[2]](#R2)

>Causal inference refers to an intellectual discipline that considers the assumptions, study designs, and estimation strategies that allow researchers to draw **causal conclusions (effects)** based on data. [[3]](#R3)

>Causal inference is a complex scientific task that relies on triangulating evidence from multiple sources and on the application of a variety of methodological approaches.[[4]](#R4)

The author in [[4]](#R4) also stresses no book can provide a comprehensive description of methodologies for causal inference across the sciences, and any Causal Inference books will have to choose which aspects of causal inference methodology they want to emphasize.

From the above definitions, we can draw a simple conclusion: the subjects of causal inference are the cause variable(s) and effect variable(s), and it attempts to quantitively estimate the influence of cause variable(s) to effect variable(s).

## Why We Need Causal Inference

A natural question is why we need causal inference, or can't existing scientific methods solve the causal problems? It seems that the above causal problems can be solved using probabilistic methods, such as conditional probability, Bayesian network, or any others, as long they can measure the Correlation. But, it has been long declared that ** Correlation does not imply causation**,

### Correlation Does Not Imply Causation 

Why correlation can not represent causation? What is the difference between these two concepts? Both of them describe the relationship between variables, but Correlation indicates a more general relation than Causation. When we say two variables are correlated, we actually mean these two variables display an increasing or decreasing trend. However, such a trend can not prove the existence of causation. Compared to Correlation, Causation involves cause and effect. When we adjust cause variables, effect variables will change also. However, the opposite could not hold, i.e., when we change the effect variables, the cause variables may not changes at all. This property does not necessarily hold in correlation. From this view, causation can been seen as a subset of correlation in some degree. Below is an excellent example to distinct Causation and Correlation:

>Say you happen upon some data that relates wearing shoes to bed and waking up with a headache, as one does. It turns out that most times that someone wears shoes to bed, that person wakes up with a headache [[5]](#R5). 

Can we say wearing shoes causes waking up with a headache, or, if I wear shoes to bed, I will probably wake up with a headache? Anyway, such conclusions do not make sense since wearing shoes has nothing to do with a headache in our mind. Waring shoes and waking up with a headache are related because they have a common cause, i.e., drinking the night before.

~~~
<div align="center">
<img src="/assets/2021/drunksleeping.png" style="width:25%;"/>
</div>
~~~

More real instances indicating "correlation doesn't imply causation" can be found in an interesting website [*Spurious Correlation*](https://www.tylervigen.com/spurious-correlations). For example, the number of people drawn by falling into a pool is correlated with films Nicolas Cage appeared in with a correlation ratio of 66.6%.
~~~
<img src="/assets/2021/nicholascage.svg" style="width:80%;"/>
~~~
US spending on science, space, and technology is correlated with suicides by hanging, strangulation, and suffocation with a correlation ratio of 99.79%.
~~~
<img src="/assets/2021/usspendinghanging.svg" style="width:80%;"/>
~~~
Divorce rate in Maine is correlated with the per capita consumption of margarine with a correlation ratio of 99.26%.
~~~
<img src="/assets/2021/divorcerate.svg" style="width:80%;"/>
~~~

All these instances illustrate that the correlation between two variables can not imply causation, no matter how high the correlation ratio.

## What Problems Does Causal Inference Solve?

This question's answer can be found in [The Book of Why](#R1). Specifically, Judea Pearl introduces the ladder of causation (see my blog [Summary of *The Book of Why*: Chapter 01](/post/2021/2021-04-09-The-Book-of-Why-Summary-Chapter01/)) and list some typical questions as well as the task of each rung. However, the task description of causal inference in this book is a little obscuring to me. Then I found a more concise task description of causal inference in a survey paper [[2]](#R2):

> For causal inference, our objective is to estimate the treatment effects from the observational data.

**Treatment effect** in this sentence seems unfamiliar. Roughly speaking, it measures the influence amount of one action on the target. It will be introduced in detail in the subsequent blogs. *P.S. So far, I agree more with this description because it is more intuitive. If I have a deeper understanding of the target of causal inference in the future, I will update this blog.*

## Applications

Causal inference is commonly used in many scientific fields. For example, if we are choosing treatments for a disease, we want to choose the treatment that causes the most people to be cured, without causing too many bad side effects. If we want a reinforcement learning algorithm to maximize reward, we want it to take actions that cause it to achieve the maximum reward. If we are studying the effect of social media on mental health, we are trying to understand what the main causes of a given mental health outcome are and order these causes by the percentage of the outcome that can be attributed to each cause. A classical application of causal inference is to solve Simpson's Paradox, as shown in [[5]](#R5). 

There are also casual inference methodology for language, including methodology for causal inference with observed data, in which text is a treatment, outcome or others. Also natural language processing can be applied in causal inference. I intend to introduce those works in future blogs.

## Causal Inference Frameworks

There are two main frameworks for causal inference: the potential outcomes framework and the structural model framework. The potential outcomes framework aims to **estimate potential outcomes and then calculate the treatment effect**. Therefore, the treatment effect estimation is one of the central problems in causal inference under the potential outcomes framework. The structural model framework describes the causal mechanisms of a system **where a set of variables and the causal relationship among them are modeled by a set of simultaneous structural equations**. The two frameworks are described in detail in my blog [potential outcomes framework](/post/2021/2021-04-07-Potential-Outcomes-Framework/) and [the structural model framework](/post/2021/2021-04-13-Structural-Model-Framework/).

## References

~~~
<div><a name="R1"></a>
[1] Pearl J, Mackenzie D. The book of why : the new science of cause and effect. 2018.
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


