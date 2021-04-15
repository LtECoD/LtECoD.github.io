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

\definition{Treatment Effect}{Treatment effect is the gap of potential outcomes between two treatments.}
The treatment effect can be calculated in different levels. To make these definitions clear, we apply the denotations of \citep{survey} and define the treatment as binary, i.e. one unit can only receive treatment ($T=1$) or not ($T=0$). Then the population is divided into two groups, treated group of which units receive treatment, and control group of which units receive no treatment.

At the unit-level, the treatment effect is named as Individual Treatment Effect (ITE), which is defined as:
$$
\text{ITE}_i=Y_i(T=1)-Y_i(T=0)
$$
where $Y_i(T=1)$ and $Y_i(T=0)$ are the potential outcomes of unit $i$ with treatment $t$ being 0 and 1 respectively.

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

🚧

## Assumptions

## Methods


## References

* \biblabel{survey}{Yao, 2020} **Yao L., et al.,**,  A Survey on Causal Inference, 2020.
