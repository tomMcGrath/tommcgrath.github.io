# Research projects I'm interested in
This was originally an appendix to ["Safety as a Scientific Pursuit"](https://tommcgrath.github.io/safety_as_science) but it seems useful to break it out as a separate page so I can easily link to it and keep it up to date as I have new ideas or finish projects.


## Tools for understanding training data

Nothing in machine learning makes sense except in light of the training data. I suspect that in many cases there is some surprising data in LLM corpora that would affect our interpretation of many of their capabilities, but our ability to retrieve this training data is pretty limited (e.g. simple textual search). 

Implementing more sophisticated methods such as embedding-based lookup or [influence functions](https://www.anthropic.com/index/influence-functions) on a fully open model from the [LLM360](https://www.llm360.ai/) or Pythia families would allow better contextualisation of responses, as well as assessing possible contamination of test sets. I expect this would be somewhat deflationary about LLM’s generalisation abilities, but I could be very surprised.


## What do we currently understand about neural networks and what does this imply?

This project is a survey of what’s known empirically and theoretically about neural networks and what it might imply for safety. A selection of useful further questions should come out of this. Possible topics include inductive biases of SGD, what properties of data make it easily learnable/induce structure in network representations, whether the [linear representation hypothesis](https://arxiv.org/abs/2311.03658) is true and what impacts this has on representational engineering, to what extent the quantisation hypothesis is true and what impact this would have on scaling, among many others. This project would probably be best done as a large collaboration.


## Adversarial collaborations on LLM biorisk

This would aim to provide the definitive evaluation of whether current language models pose a meaningful risk of assisting with bioterrorism. To the maximum extent compatible with safety the results would be openly readable. This could also test whether adversarial collaborations can provide strong, reliable evaluation results and could set best practice for future evaluations.


## Learning new scientific knowledge from AlphaFold 2

This is a very ambitious project and reflects a strategy that I learned at DeepMind: to push state of the art in a given area, choose a particular problem as a ‘forcing function’ that will require you to develop new techniques in order to achieve it. This project is intended to push the state of the art in interpretability techniques for domains where humans don’t have an intuitive understanding and provide some useful data for thinking about ELK along the way.

The aim of this project would be to take the [open-sourced AlphaFold 2 model](https://github.com/google-deepmind/alphafold) and (presumably by collaborating with structural biologists) learn something new about protein folding. It seems very likely that AlphaFold 2 has all sorts of knowledge about protein folding that humans don’t yet know, and being able to extract some of this would be a good signal that we’re making progress in interpretability tools that can scale to complicated domains.


## Can neural networks learn ‘steganographic representations’?

A common concern about using interpretability tools is that models will learn to circumvent them by altering their internal representations. This project aims to study how plausible this is, and the effect that doing so has on the learning process. A strong simple proxy for this process is to train a model on a task which has multiple sufficient statistics and include the results of linear probe for one or more of those sufficient statistics in the loss, for example

$$
L = -\log p(y | x) +  (S(x)-S(x))^2,
$$

where y is the output, x the input, $S(x)$ one of the sufficient statistics for y and $\hat{S}$ the output of a linear probe for S.

My expectation is that neural networks would be able to evade the linear probe, but at a substantial cost in training time and/or generalisation ability (I’d expect a grokking phase diagram to change, for example).


## How does scaling behave beyond human level?

A key component of most models for why LLMs could achieve superhuman performance is the idea that we will be able to generate new, superhuman data to learn from (for instance by self-play of some form) and/or that [generalisation will work surprisingly well](https://evjang.com/2021/10/23/generalization.html). I currently believe that LLMs are exhibiting catch-up growth with respect to human knowledge, and that obtaining new superhuman data will at minimum be dramatically more costly, even discounting costs of experimentation and hard time limits this implies.

One way to model this process is to use a domain with a natural ‘transition point’, for example a board game dataset capped at a certain ELO. By doing (possibly ELO-conditioned) supervised learning on this data we could obtain a compute-ELO scaling law like those obtained in [Scaling Scaling Laws with Board Games](https://arxiv.org/abs/2104.03113) and [Multi-Game Decision Transformers](https://proceedings.neurips.cc/paper_files/paper/2022/file/b2cac94f82928a85055987d9fd44753f-Paper-Conference.pdf). We could then switch to MCTS-based training at the ELO cap and observe whether the compute-ELO scaling law alters substantially. This proxy clearly neglects recursive self-improvement, but should otherwise give a lot of information on what to expect when trying to extend current methods beyond human-level.


## Does pretraining with preference data bake in safeguards?

Finetuning is one of the main safety mechanisms used in language models but it’s easy to undo, whether deliberately or accidentally. It’s widely believed that this is because finetuning creates ‘wrappers’ around capabilities without substantially altering those capabilities, and some [mechanistic interpretability analysis](https://arxiv.org/abs/2311.12786) supports this. It would be great to make these safeguards more robust - maybe if we include preference data in pretraining (either by pretraining with human feedback or DPO) then the safeguards will be more deeply integrated into the network and so harder to remove.
