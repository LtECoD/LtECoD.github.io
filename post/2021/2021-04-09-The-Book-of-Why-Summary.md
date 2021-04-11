+++
hascode = false
date = Date(2021, 04, 09)
+++
@def tags = ["causalinference"]

# The Book of Why

\toc

## Chapter 1: The ladder of causation

This chapter introduces mainly the ladder of causation proposed by the author. The ladder includes three levels, including association, intervention, and counterfactuals from bottom to top. The three levels have progressively more powerful causal queries.

~~~
<img src="/assets/2021/ladderofcausal.png"/>
~~~

### Association

The first rung calls for prediction based on passive observations, of which one typical question is "*what if I see ... ?*". The author placed existing artificial intelligent machines on this rung because machines are disappointingly far from humanlike cognization. The author also quoted two precise statements about artificial intelligence: 

> The field of intelligence is bursting with micro discoveries.

> Human-level intelligence or animal-level abilities?

Machine learning programs operate almost entirely in the association mode. They are driven by a stream of observations to which they attempt to fit a function. Lacking flexibility and adaptability is inevitable in systems works on the first level.

### Intervention

Intervention ranks higher than association because it involves not just seeing but changing what is. The typical question of intervention is "*what if I do ... ?*". Observation can never cover all possible situations. Then we need to intervene the world and observe what will happen. A very direct way to predict the result of an intervention is to experiment with it under carefully controlled conditions. Successful predictions of the effects of interventions can sometimes be made even just with causal models instead of experiments. The problem of intervention lies that we can not intervene the world in two ways. It means when we intervened the world in one way, we have lossed observations of other interventions. We step up to the top level of the causation ladder when we begin to seek possibilities contrary to the facts, i.e., counterfactuals.

### Counterfactuals

Counterfactuals have a particularly problematic relationship with data because data are, by definition, facts. This rung aims to compare the real world to a fictitious world. The typical question of counterfactuals is "*what if i had done ... ?*" or "*why ... ?*". I don't think I can fully digest the significance of counterfactuals now. So I quote the book directly:

> While rung one deals with the seen world, and rung two deals with a brave new world that is seeable, rung three deals with a world that cannot be seen (because it contradicts what is seen). To bridge the gap, we need a model of the underlying causal process, sometimes called a "theory" or even (in cases where we are extraordinarily confident) a "law of nature." In short, we need understanding. This is, of course, a holy grail of any branch of science—the development of a theory that will enable us to predict what will happen in situations we have not even envisioned yet. But it goes even further: having such laws permits us to violate them selectively so as to create worlds that contradict ours. Our next section features such violations in action.


There are still several questions confusing me:

1. The author mentioned that no machine could derive explanations from raw data. It needs a push. But how to push?

2. Only learning from observed data makes current intelligent machines stay on the first rung. However, the potential outcome framework bases on observed data as well. Is this framework competent for causal inference?


## Chapter 2: the genesis of causal inference

:construction:

