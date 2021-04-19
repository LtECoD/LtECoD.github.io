+++
hascode = false
date = Date(2021, 04, 07)
+++
@def tags = ["causalinference"]

# Potential Outcomes Framework

\toc

## Definitions

The potential outcome framework aims to **estimate potential outcomes and then calculate the treatment effect**. The treatment effect estimation is one of the central problems in causal inference under the potential outcome framework. Compared with structural causal model framework, which emphasize conceptualizing, expressing and reasoning about the effects of possible causal relationships among variables, the potential outcomes framework tent to emphasize estimating the size or strength of casual effects.

There are several key concepts in the potential outcome framework.

\definition{Unit}{Unit is the atomic research object in the treatment effect study.}
For example, when we want to calculate the treatment effect of smoking on lung cancer, a unit is a *person*.

\definition{Treatment}{Treatment refers to an action applied to a unit.}
Still taking smoking as an example, the treatment is smoking or not smoking. Note that treatment is not always discrete. It can also be continuous.

\definition{Potential Outcome}{Potential outcome is the outcome of a treatment that was applied to a unit.}

An example is shown here to better illustrate the above three definitions:
\example{Consider the scenario where you are unhappy. And you are considering whether or not to get a dog to help make you happy. In this scenario, you is one of the unit, the treatment is whether or not to get a dog, and the potential outcome is happiness.}

If you become happy after you get the dog, does this mean the dog caused you to be happy? Well, what if you would have also become happy had you not gotten the dog? Okey, answering these causal questions requires an important concept: treatment effect.

\definition{Treatment Effect}{Treatment effect is the gap of potential outcomes between two treatments.}
The treatment effect can be calculated in different levels. To make these definitions clear, we define the treatment as binary, i.e. one unit can only receive treatment ($T=1$) or not ($T=0$). Then the population is divided into two groups, treated group of which units receive treatment, and control group of which units receive no treatment.

At the unit-level, the treatment effect is named as Individual Treatment Effect (ITE), which is defined as:
$$
\text{ITE}_i=Y_i(T=1)-Y_i(T=0)
$$
where $Y_i(T=1)$ and $Y_i(T=0)$ are the potential outcomes of unit $i$ receiving treatment $T$ being 0 and 1 respectively. Considering the above example, $T=1$ represents getting a dog, while $T=0$ represents not. And $Y=1$ represents being happy, while $Y=0$ represents not.

At the population-level, the treatment effect is named as Average Treatment Effect (ATE), which is defined as:
$$
\text{ATE}=\mathbb{E}\left[ Y(T=1)-Y(T=0) \right]
$$
where $Y(T=1)$ and $Y(T=0)$ are the potential treated and control outcome of the whole population respectively.

At the subgroup level, the treatment effect is called Conditional Average Treatment Effect (CATE), which is defined as:
$$
\text{CATE}=\mathbb{E}\left[Y(T=1) | x \right]-\mathbb{E}\left[Y(T=0) | x \right]
$$

\bluebox{The objective of potential outcomes framework is to estimate the treatment defined on different levels.}

In additional there are two definitions for variable, namely the pre-treatment variables and the post-treatment variables.

\definition{Pre-treatment Variables}{Pre-treatment variables are the variables that will not be affected by the treatment.}
\definition{Post-treatment Variables}{The post-treatment variables are the variables that are affected by the treatment.}
Note that, pre-treatment variables are also called *background variables*. For example, in the follow figure, variable $X$ and $Z$ are both background variables, while the intermediate variable $U$ is a post-treatment variable.

~~~
<div align=center>
<img src="/assets/2021/pretreatmentvar.svg", style="width:30%;"/>
</div>
~~~

## Assumptions

In order to estimate the treatment effect, the following assumption are commonly used in the causal inference literature.

### Assumption 1: No Interference

The assumption emphasizes the independence of each unit, that is, there are no interactions between units. In the context of the above illustrative example, your happiness will not affect others' outcomes, and vice versa. Specifically, it is formulated as:
$$
Y_i(T_1,\cdots,T_{i-1},T_i,T_{i+1},\cdots,T_n)=Y_i(T_i)
$$

### Assumption 2: Ignorability

When we want to compute the treatment effects, like ATE, a natural quantity that comes to mind is association difference: $\mathbb{E}[Y|T=1]-\mathbb{E}[Y|T=0]$. Unfortunately, this is not true in general due to confounding or background variables. However, aforementioned treatment effects are impossible to compute directly because we can't observe all potential outcomes in the same time. Assumption *ignorability* would make it so that the treatment effect is simply the associational difference.

Ignorability indicates that treatment is independent with potential outcomes:
$$
(Y(1),Y(0)) \bot T
$$
Ignorability is critical because it allows us to reduce avereage treatment effect to the association difference::
$$
\begin{aligned}
    \mathbb{E}[Y(1)]-\mathbb{E}[Y(0)] &=\mathbb{E}[Y(1)|T=1]-\mathbb{E}[Y(0)|T=0] \\
    &=\mathbb{E}[Y|T=1]-\mathbb{E}[Y|T=0]
\end{aligned}
$$
Ignorability is called *exchangeability* as well, which means that if the treated group and the control group are swapped, we can also get the same result. More specifically, if we take the old treated group as the new control group and take the old control group as the new treated group, the new potential outcomes would keep the same as the old.

Actually, ignorability assumes all the units share the same background variables. Therefore, the changing of treamt



### Assumption 3: Postivity

🚧

## Methods


## Acknowledgement

This blog refers mainly \cite{survey} and \cite{introduction}.

* \biblabel{survey}{Yao, 2020} **Yao L., et al.**,  A Survey on Causal Inference, 2020.
* \biblabel{introduction}{Brady, 2021} **Brady Neal**, Introduction to Casual Inference, 2021.