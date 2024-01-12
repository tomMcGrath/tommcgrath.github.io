# Safety as a Scientific Pursuit

“Wir müssen wissen – wir werden wissen” - David Hilbert


## Here be dragons?

When humanity was still exploring the Earth, it was common to mark uncharted territories or places from where few travellers had returned with fantastic and dangerous beasts[^1]. Although we were born too late to explore the Earth, and are probably too soon to explore the stars, there is now one clear, vast frontier: intelligence. Just as before, rumours of strange creatures beyond the settled frontier reach those of us behind it (what did Ilya see?) and we are warned of strange scaly creatures beyond the borders of what is known. And, just as before, as the frontier moves forward we must replace these crude sketches with detailed maps if we are to safely make use of what we have found.

What I’ve just said probably sounds quite harsh to early pioneers in AI, and to those in AI safety in particular. This isn’t my intention. Although early maps were often crude and distorted, they also contained a lot of truth. Many of the strange creatures in the far reaches of the Hereford Mappa Mundi (to give an example I’m familiar with) actually have some relation to reality, and when travellers failed to return there was often a good reason. Sea monsters might not be quite real, but the ocean was a dangerous frontier, and AI may be as well. There’s something badly wrong with this analogy, however. The unknown territory of the past was guarded by the realities of distance and danger, but today’s frontiers in AI are largely barred by artificial walls.

In this essay I outline the possibility for an empirical revolution in AI safety research, contrast this with the current dominant approach, and make concrete suggestions for how we might move towards the goal of empirical safety research. One of the core values I suggest we revisit is openness, which I believe has been prematurely rejected.


## The two cultures of safety research: rationalism and empiricism

The AI community runs along an ancient major philosophical faultline, with much of the safety community on one side and much of the ‘builder’ community on the other. This faultline is the divide between rationalism and empiricism. This division has similarities with [Jacob Steinhardt’s distinction between Philosophers and Engineers](https://bounded-regret.ghost.io/more-is-different-for-ai/). The philosophical idea of rationalism also has some overlaps with the modern Rationalist community - although the Rationality movement has historically [emphasised the importance of empiricism](https://slatestarcodex.com/2014/11/27/why-i-am-not-rene-descartes/) this is in my view (at least in AI) now practiced much less than it’s preached. I’d like to draw on all of these proposed distinctions to contrast what I’m going to call the rationalist and empiricist worldviews as they relate to AI safety.

A key practical distinction between the rationalist and empiricist worldviews is what to do in the presence of uncertainty: empiricists seek to reduce uncertainty and then act, whereas rationalists marginalise over the possibilities (weighted by utility). Although for ideal reasoners there’s no difference between these points of view, for humans the differences can be substantial. The second part of this essay outlines some of the most relevant differences by suggesting what an empirical revolution in safety research would look like. The third part outlines what an ecosystem designed to maximise progress in empirical safety research would be like, and the effects this could have on the rest of the AI ecosystem.


### Rationalism

A reasonable summary of the typical rationalist viewpoint on AI safety might be: "It's logically possible (and perhaps even likely for arbitrarily powerful predictors) that LLMs could become deceptively aligned/have inner misalignment/exhibit a sharp left turn. It might even be happening now! Because this outcome is so bad, and has some nontrivial (maybe even large) weight in our probability distribution of possibilities, we should stop building AI until we know how to make this situation logically impossible."

The rationalist worldview focuses on trying to predict outcomes _a priori_ and forestall them. This leads to a natural emphasis on focusing on worst-case problems. It's primarily a philosophical, mathematical, and computer science-based mindset. This approach primarily focuses on definitions (e.g. deconfusion research) and unfolding them into their implications. It's largely self-referential, based on logical entailment, rewards brilliance over diligence, and could be relatively easy to carry out in secret (assuming you don't regularly make logical errors).

I want to be sympathetic to rationalism here - empiricism is only possible when you have something to be empirical about! So it’s unsurprising that so much early work (pre-GPT for example) has been done by rationalists, as a lot of the relevant empirical work was impossible without real systems to study[^2]. To some extent all visionary work has a substantial element of abstract thought in it and is often a leap of faith unsupported by evidence.


### Empiricism

I would summarise the empiricist worldview as roughly: "It's certainly possible that AI could be dangerous, even catastrophic. How would we know? What relevant properties do current AI systems have? What do we need to know about them to reduce possible dangers? How can we maximise the rate at which we collectively learn important true things about the systems we're building? What decisions do we need to make soon, and what do we need to learn to make them?"

Each of the questions posed by our imaginary empiricist opens out into other questions, which all have implications for how we might keep building or know when to stop. Empiricism is naturally outward-looking and rewards experimental hard work (although brilliance has a role to play, as in all sciences). Because there's always some experimental detail you might have failed to consider, follow-on experiment or alternative interpretation of the data, this approach works best in the open (more on this later).

The idealised empiricist worldview focuses on being able to learn new, relevant information and rapidly change direction based on that information. It's primarily a natural science and engineering mindset. The key questions to an empiricist are what we think we know, why we think we know them, and how we can learn more.


### How rationalism and empiricism come into conflict

**Intellectual conflicts**

These differing worldviews tend to shade into other differences of opinion, not least on the degree to which current approaches will easily scale past human-level (an empiricist might ask where the data to do so will come from, for example), or the degree to which a disembodied AI would be able to take over the world in a single shot but I'll leave exploring that for another day. For now I'll have to accept that if you believe that (a) current approaches to AI will easily scale to superhuman levels and (b) this will render everything we can learn about current systems irrelevant then we have very little common ground and from your perspective you might reasonably dismiss empiricism as an approach[^3]. Regardless, you might benefit from a better understanding of where many of those you see as your opponents are coming from, and how you might persuade them better in order to achieve our shared goal of having AI go well.

**Practical conflicts**

I believe that the current fractious state of AI is at least in part because the primarily abstract-thought-based safety community has largely failed to convince more empirically-minded engineers of the risks they believe current or potential next-generation systems pose. Because more empirically-minded people remain unconvinced of potential risks, or are unconvinced that these risks pose a currently-binding constraint they keep pushing forward (correctly, by their lights) on AI research they view as beneficial. This gets interpreted by the safety community as “not caring about safety.”[^4]

Having failed to stop AI progress, the main approaches of the safety community have been to repeat their arguments more loudly and to seek political and corporate veto power such as the recent Pause AI movement (and perhaps to some extent the recent OpenAI board shenanigans). I think that a more productive approach over the long term would be to engage deeply with empiricism in a way that I’ll outline shortly.

**How empiricism can avoid or de-escalate conflicts**

_“Scientists try to eliminate their false theories, they try to let them die in their stead.”_ - Popper

Beliefs in conjunction with values typically lead to actions, and when differing beliefs lead to differing actions then that leads to conflicts - as we’re currently seeing in AI. If we can resolve the differences in beliefs, then if our values are more-or-less similar we’ll probably arrive at similar actions and the conflict is removed. If we can’t resolve differences in beliefs then we’re left in conflict about actions, or worse end up concluding that the difference actually lies in our values, and our intellectual opponents are actually amoral monsters hell-bent on destroying everything we care about. What’s really going on is that we’re simply not convinced by the evidence we see, and are acting accordingly. So how can we resolve these disagreements? \


I have essentially never seen a major disagreement in AI resolved by rationalist methods (e.g. the double crux) - for some examples see [the MIRI dialogues](https://www.lesswrong.com/s/n945eovrA3oDueqtq) or the [XRisk Persuasion Tournament](https://www.astralcodexten.com/p/the-extinction-tournament), and for some positive effects of introducing evidence see [The Great Air Conditioner Debate Of 2022](https://www.lesswrong.com/tag/air-conditioning). Although in principle the discussion would proceed until it hits some tractable point of disagreement, or a surprising conclusion is derived from some shared set of definitions that settles the argument, all that appears to happen is that the discussion expands down endless rabbit holes, never to return. I think that this is because when we’re playing ‘duelling intuitions’ then there’s nothing to arbitrate between the clashing intuitions at play; doing so is the role of empiricism and we’re suffering from its absence.

Disagreements are resolved all the time by empirical means; that’s more or less what science entails[^5]. A relevant example that is playing out right now is the question of whether neural network representations are human-understandable. The science of mechanistic interpretability appears to be answering that question in the affirmative, much to the surprise of a huge number of neural network researchers. Simply working on the assumption that [one cannot scrute the matrices](https://www.lesswrong.com/posts/uMQ3cqWDPHhjtiesc/agi-ruin-a-list-of-lethalities#sufficiently_good_and_useful) based on one’s priors would have left the potential for enormously powerful tools on the table.

The questions we’re trying to answer are important, urgent, and decision-relevant, so we have to do better. Although doing good empirical work might seem harder and slower than having another discussion about our intuitions, in relatively little time it will make far more progress[^6], and in a way that minimises division in the community - we should strive to test our theories so they may die instead of us.


## An empirical revolution in safety research


### What would an empirical revolution in safety research consist of?

The first and obvious change would be to demand evidence for claims about the dangers of particular systems. This could be for claims of current harms, or potential harms that could occur from changing policies on current systems (e.g. open-sourcing). These experiments should be constructed in a way that puts the central hypothesis at risk, rather than ones where the outcome is known in advance and essentially baked into the setup. This kind of policy-based evidence-making seems ubiquitous in [work on AI-aided biorisk](https://1a3orn.com/sub/essays-propaganda-or-science.html) and massively harms the credibility of this research. Safety researchers have tended to treat those who disagree with them as ideological enemies or idiots to be routed around, rather than as a source of helpful sharpening of their ideas. 

The second change would be to push as hard as possible to find empirical evidence that bears on core safety questions that have remained hypothetical until now. This will almost inevitably involve an imperfect match between the experiments available to us and the safety issues of interest, but this match is likely to gradually improve as systems improve over time. Key questions include the degree to which AI systems naturally learn human-understandable representations, the nature of the learning process (particularly the types of functions preferred by SGD) and the ways in which networks generalise (and fail to do so). In many cases considerable empirical work will already have been done outside of the safety community and an easy way to start would be by collating it and considering its implications - [this work by Nora Belrose and Quintin Pope](https://docs.google.com/document/d/18tF9z3OhmKsyQCj93NkrcDwGBquat8BTMma-f3kW7sM/edit?usp=sharing\) is a good example. Although others might disagree about what conclusions to draw from the evidence, these disagreements would most likely be much more specific and open to resolution by further empirical work.

A third change would be to support open, reproducible research. This is the only way that our work can reach the kind of rigour necessary to be relied upon. A natural but very important corollary of this is to support open-source AI as vital to many of the most important areas of safety research: without access to training data we can’t understand learning dynamics or generalisation, without access to weights we can’t do interpretability research, and without access to full transcripts and data analysis we can’t rely on the results of evaluations. There are hypothetical situations in which open-sourcing models would be wrong and would generate unacceptable risks, and I can certainly imagine eval results that would lead me to agree that a model should remain closed, but there’s no evidence we’re currently in this situation.

Finally, doing an experiment and reporting the results isn't the end of the process. Often there are methodological issues that need to be settled to be clear about what a series of experiments really means - science is an iterative process and things are always open to revision. This is unsatisfying if what you want is absolute once-and-for-all certainty, but I think that that is a mirage when dealing with the real world. What we find will typically be complex and not simply a safe/unsafe finding. We should expect pushback and back-and-forth about experimental results: this is simply the way that an empirically-minded community arrives at consensus regarding what an experiment ‘really shows’.


### Openness is essential to good empiricism

Openness is a central pillar of effective science: there’s a reason that the Royal Society’s motto is _“Nullus in verba.”_ Openness means that your data, as well as the way you’ve obtained it and your subsequent analyses are open to scrutiny, and can be reproduced, explored, and extended by other researchers - you’re not reliant on [simply integrating the opinions of others](https://twitter.com/geoffreyhinton/status/1728178632508780919). To do good open research in many areas of AI we need open models, and the safety community’s push to prevent open-sourcing will be counterproductive within months or years. The [Pythia model suite](https://arxiv.org/abs/2304.01373) is an example of the kind of resource we should be prioritising - [this thread](https://twitter.com/BlancheMinerva/status/1722954269194629580) by one of the authors lists some papers but I’d also like to highlight Eric Michaud’s highly safety-relevant work on [a model of learning that explains scaling laws](https://arxiv.org/abs/2303.13506) and [recent work on sparse autoencoders for lifting superposition](https://arxiv.org/abs/2309.08600), both of which relied on the Pythia model suite.

A further good example of the value of openness is the [recent work by Apollo research on deception](https://static1.squarespace.com/static/6461e2a5c6399341bcfc84a5/t/65526a1a9c7e431db74a6ff6/1699899932357/deception_under_pressure.pdf). I found the initial release ‘trailer’ almost completely unconvincing ([as did others](https://twitter.com/norabelrose/status/1720301015868797011)) - there were too many researcher degrees of freedom that could easily be tweaked to get the results to come out ‘right’. When the full paper and GitHub repo with transcripts and analysis code came out I was able to look into the raw data and found this considerably more compelling as it didn’t seem finely tuned to produce the desired result. There’s still some things I want to check to be more confident in their findings, but because of the high standard of openness I can do this. I find Apollo’s work substantially more persuasive than any other evals result I've seen so far, not because of the openness in some ideological sense, but because of what the openness enables. Apollo’s work here is the standard to which other evaluation work should be held[^7], and if I were building LLM systems I’d take the possibility of the kind of deception they demonstrate seriously.

To give an example of lack of openness and its consequences: Anthropic’s [recent results on sycophancy](https://cdn2.assets-servd.host/anthropic-website/production/files/model-written-evals.pdf) in base models [fail to replicate on OpenAI models](https://www.lesswrong.com/posts/3ou8DayvDXxufkjHD/openai-api-base-models-are-not-sycophantic-at-any-size). The original finding was very surprising safety-relevant research, so finding that it doesn’t replicate is a bit troubling. Given that the finding fails to replicate, how should we change our minds? It’s hard to know, because we don’t know what’s different between OpenAI’s models and Anthropic’s, and given trends towards internal siloing at major labs, perhaps the researchers on the original paper don’t know either! Perhaps the base model Anthropic used was non-standard in some important way? Perhaps there’s some important training data subset that leads to this behaviour? All we can do is speculate. The research community has learnt essentially nothing from this paper now, but if both labs had been more open we would have an important piece of information on the causes of sycophancy.

One of the main reasons put forward to not open-source models is that doing so would enable ‘bad actors’ to harm people. A central example in this category, and the one that’s been most heavily used to push to prevent open-sourcing, is bioterrorism risk. The core concern here is that LLMs might contain information that could help a terrorist carry out a biological attack - a perfectly reasonable concern and one that should be relatively easy to test. I remain open to strong evidence of potential harms - the Apollo paper on deception shows that well-executed empirical research can be done on these topics - but the evidence we have for current LLMs being able to cause significant harms is paper-thin at best.


### Adversarial collaborations: a way forward when openness is impossible

Everyone but the most ardent advocates for openness must realise that there are times when it’s safest for research to not be fully open. This is already the case in some particularly risky domains and it might become true of AI in future. In this case, what can be done? I think that adversarial collaborations are probably the best way forward: find two researchers that have contradictory views on the research question (e.g. “Can this system meaningfully help with hacking? Should it be open-sourced?”) and have them work together towards a conclusion. Ideally all evals would be conducted this way if they can’t be done in the open, and certainly I would like to see a norm of only making decisions on evals that have come out of an adversarial collaboration. If you can’t find potential ‘adversaries’ to collaborate with, consider that you might be in something of an intellectual bubble[^8]. For more on adversarial collaborations see [this in-depth article](https://www.researchgate.net/profile/Cory-Clark-2/publication/356944598_Keep_your_enemies_close_Adversarial_collaborations_will_improve_behavioral_science/links/6205332b634ff774f4c0b076/Keep-Your-Enemies-Close-Adversarial-Collaborations-Will-Improve-Behavioral-Science.pdf). [This article by Andrew Gelman](https://statmodeling.stat.columbia.edu/2023/10/16/a-successful-example-of-adversarial-collaboration-when-does-this-approach-work-and-when-does-it-not/) gives an example of adversarial collaborations working in practice - although note that he’s had them fail too.

An important advantage of adversarial collaborations is that even if the full results can’t be released, we know that someone has had their mind changed. This isn’t generally the case with research publications: when an OpenPhil-funded study finds that an AI system is dangerous and shouldn’t be released, who is surprised? Although I generally dislike this kind of Aumannian approach, and think it’s relied on far too extensively, in some occasional cases it may actually be the best we can do. A potential disadvantage of adversarial collaborations is that they will almost certainly take more time than a single paper where the authors are all in agreement. I think that this is the wrong comparison class, and the correct comparison would be to a back-and-forth in the literature spanning multiple papers.

A final aspect of adversarial collaborations that I find promising is that they involve _collaboration_. At a time when AI safety is generating far more heat than light, and frontier AI research is rapidly splitting into ideologically-opposed factions, projects that generate understanding across factional lines have the potential to defuse some of this tension.


## An open research ecosystem


### Build and support open models to enable open research

The first major change would be to put open models at the core of AI research, and to release their training data (as EleutherAI did with Pythia) to enable better-informed evaluations, as well as other research for which knowledge of training data is essential. Currently we don’t have the tools to really understand the link between training data and the resulting model, but [progress is being made](https://arxiv.org/abs/2308.03296) and even ad-hoc analyses can have surprising value (I’ve certainly seen this myself).

At a minimum I think that the safety community should reconsider the costs and benefits of open models. I believe (for the reasons given above, as well as arguments [very well put by Beren Millidge](https://www.beren.io/2023-11-05-Open-source-AI-has-been-vital-for-alignment/)) that this will come down strongly in favour of much more openness on the current margin, and so the safety community should stop opposing open model releases, such as Llama 2, and stop pushing for anti-open-source legislation. A far larger and more impactful move would be to actively create new open research-grade models that can easily be studied and be even more safely open-sourced, even at the frontier. The best way to do this is not yet clear but I believe there are multiple good options - that’s for another post.

A final strand of work would be to do work that reduces the potential downsides of open models. A commonly-cited reason to keep models behind an API is so that if undesirable model behaviours are found then the model can be updated or access filtered in some way. Finding and deploying practical ways to update a model (as [suggested by Colin Raffel](https://colinraffel.com/blog/a-call-to-build-models-like-we-build-open-source-software.html)) quickly in response to issues is a priority for open models, as is research into [machine unlearning](https://blog.research.google/2023/06/announcing-first-machine-unlearning.html).


### Build the capacity to learn and react fast

Although we might want to anticipate and forestall every issue, in practice this will be impossible - problems and opportunities that never even occurred to us happen all the time. In addition, although dangerous AI capabilities may well exist in the future, we have no real idea how close many of them are. A strong, scientifically rigorous evaluation framework that enables us to learn and react as fast as possible is the only realistic way to counter potential emergent issues. [Responsible scaling policies](https://www.anthropic.com/index/anthropics-responsible-scaling-policy) and [OpenAI’s preparedness framework](https://cdn.openai.com/openai-preparedness-framework-beta.pdf) are a good example of empirically-grounded safety work that builds in the kind of deep uncertainty we should have about the future course of AI, and [Open Philanthropy’s two new proposals](https://www.openphilanthropy.org/research/rfps-on-llm-impacts/) also have some promise - but the quality of the science they produce will determine their impact. Without openness on their results and methods, however, their ability to influence those external to the lab doing the testing will also be limited.

All of the above relies on some deep assumptions about the way AI systems will develop with scale, particularly an assumption of gradualism: AI systems of one scale will largely resemble AI systems of another scale. These foundational assumptions need checking, and fundamental empirical and theoretical work should be done here. The problem of induction still applies - how will we know that these properties hold at yet larger scale? - but unless you’ve got a solution to that problem this is the best we can do[^9].


## In defence of rationality


### When is rationality a better choice?

Up to now I’ve been advocating for much more empiricism on the current margin. Nevertheless, it’s worth acknowledging that not only does rationalism have its place, but that there are things you might believe that would imply more rationalism is still the correct way forward. The most obvious limitation of empiricism is that you can only use empiricism to learn about models that actually exist or models that are related to those that currently exist in some way that you think you understand (e.g. scaled-up versions of current networks). If you believe that there’s some important sharp discontinuity, and that all relevant risks are on the other side of that discontinuity, then empiricism will probably look like a waste of time. Examples of this might be fast takeoff or the [sharp left turn](https://www.alignmentforum.org/tag/sharp-left-turn). We don’t see these in current systems, of course, but the natural empiricist move is to ask what relevant analogues these might have in current systems, and what we might learn that transfers. For example, we could study discontinuities and emergent properties in current networks and learn all we can about them, or we could investigate how physically plausible fast takeoff is. Still, the fact that we think about them at all is something we can attribute to rationalist-style thinking.

Another time it would seem worth switching over to primarily rationalist-style approaches is if you believe that: 



1. dangerous systems are just around the corner,
2. you know what the relevant problems are, and 
3. you have no idea of how to solve them 

(though you’ll clearly be better at convincing others if you can produce solid evidence of this). In this case it’s probably worth allocating more time and effort to rationalist-style methods. I think that [Eliciting Latent Knowledge](https://www.lesswrong.com/tag/eliciting-latent-knowledge-elk) is a good example of working within this paradigm, and offers some chance of progress.

Finally, rationalist methods can offer the possibility of completely new approaches (although empirical work can also turn up many beneficial surprises). A good example of this is the work on [debate](https://arxiv.org/abs/1805.00899), which is an example of an elegant and compelling new approach. Debate is also a great example of the power of alternating between empiricism and rationalism: coming up with the approach was a conceptual leap, driven largely by abstract thought about arbitrarily powerful systems, but the question of whether it works in practice (and what causes it to succeed and fail) has been the subject of substantial empirical work. I expect success stories to often look a lot like this.


## An invitation to empirical research, and a final concern


### What if empiricism/rationalism preferences are far deeper than I’ve assumed?

Before closing with a list of proposals, I feel the need to air a concern that’s been troubling me since my friend Zhengdong Wang aired it: perhaps the distinction between empirical and rational research is far more than a difference in intellectual toolsets that we can switch out at will. It may be something far more fundamental; a deep disposition that is a core part of our identity as individual scientists and people. Maybe I favour empirical work out of a lack of imagination, or as a crutch for a lack of theoretical brilliance? Conversely, rationalist preferences may play some similarly deep psychological role for some that hold them - I am loath to psychoanalyse here, however. Even if the empiricism/rationalism divide is deeper than I hope, at least we can facilitate dialogue between these two cultures. Moreover, this is much less of a binary distinction than I have drawn so far, and those in the middle can bridge the gap to produce what neither culture could have achieved alone.


### An invitation to empirical research

If the ideas in this essay are appealing, or you think there might be something to be gained from doing more empirical research relevant to the safety of AI systems, then I have some concrete projects to suggest in the appendix. These are, of course, only a starting point, and there’s an enormous amount of other work we could do.


## Acknowledgements

Many thanks to Zhengdong Wang, Matthew Rahtz, Gavin Leech, Misha Yagudin, Ziming Liu, Eric Michaud, Jade Leung, and Beren Millidge for many helpful comments on earlier drafts.


## Appendix: Examples of empirical safety research


### Tools for understanding training data

Nothing in machine learning makes sense except in light of the training data. I suspect that in many cases there is some surprising data in LLM corpora that would affect our interpretation of many of their capabilities, but our ability to retrieve this training data is pretty limited (e.g. simple textual search). 

Implementing more sophisticated methods such as embedding-based lookup or [influence functions](https://www.anthropic.com/index/influence-functions) on a fully open model from the [LLM360](https://www.llm360.ai/) or Pythia families would allow better contextualisation of responses, as well as assessing possible contamination of test sets. I expect this would be somewhat deflationary about LLM’s generalisation abilities, but I could be very surprised.


### What do we currently understand about neural networks and what does this imply?

This project is a survey of what’s known empirically and theoretically about neural networks and what it might imply for safety. A selection of useful further questions should come out of this. Possible topics include inductive biases of SGD, what properties of data make it easily learnable/induce structure in network representations, whether the [linear representation hypothesis](https://arxiv.org/abs/2311.03658) is true and what impacts this has on representational engineering, to what extent the quantisation hypothesis is true and what impact this would have on scaling, among many others. This project would probably be best done as a large collaboration.


### Adversarial collaborations on LLM biorisk

This would aim to provide the definitive evaluation of whether current language models pose a meaningful risk of assisting with bioterrorism. To the maximum extent compatible with safety the results would be openly readable. This could also test whether adversarial collaborations can provide strong, reliable evaluation results and could set best practice for future evaluations.


### Learning new scientific knowledge from AlphaFold 2

This is a very ambitious project and reflects a strategy that I learned at DeepMind: to push state of the art in a given area, choose a particular problem as a ‘forcing function’ that will require you to develop new techniques in order to achieve it. This project is intended to push the state of the art in interpretability techniques for domains where humans don’t have an intuitive understanding and provide some useful data for thinking about ELK along the way.

The aim of this project would be to take the [open-sourced AlphaFold 2 model](https://github.com/google-deepmind/alphafold) and (presumably by collaborating with structural biologists) learn something new about protein folding. It seems very likely that AlphaFold 2 has all sorts of knowledge about protein folding that humans don’t yet know, and being able to extract some of this would be a good signal that we’re making progress in interpretability tools that can scale to complicated domains.


### Can neural networks learn ‘steganographic representations’?

A common concern about using interpretability tools is that models will learn to circumvent them by altering their internal representations. This project aims to study how plausible this is, and the effect that doing so has on the learning process. A strong simple proxy for this process is to train a model on a task which has multiple sufficient statistics and include the results of linear probe for one or more of those sufficient statistics in the loss, for example



$$
L = -\log p(y | x) +  (S(x)-S(x))^2,
$$

where y is the output, x the input, $S(x) one of the sufficient statistics for y and $\hat{S}$ the output of a linear probe for S.

My expectation is that neural networks would be able to evade the linear probe, but at a substantial cost in training time and/or generalisation ability (I’d expect a grokking phase diagram to change, for example).


### How does scaling behave beyond human level?

A key component of most models for why LLMs could achieve superhuman performance is the idea that we will be able to generate new, superhuman data to learn from (for instance by self-play of some form) and/or that [generalisation will work surprisingly well](https://evjang.com/2021/10/23/generalization.html). I currently believe that LLMs are exhibiting catch-up growth with respect to human knowledge, and that obtaining new superhuman data will at minimum be dramatically more costly, even discounting costs of experimentation and hard time limits this implies.

One way to model this process is to use a domain with a natural ‘transition point’, for example a board game dataset capped at a certain ELO. By doing (possibly ELO-conditioned) supervised learning on this data we could obtain a compute-ELO scaling law like those obtained in [Scaling Scaling Laws with Board Games](https://arxiv.org/abs/2104.03113) and [Multi-Game Decision Transformers](https://proceedings.neurips.cc/paper_files/paper/2022/file/b2cac94f82928a85055987d9fd44753f-Paper-Conference.pdf). We could then switch to MCTS-based training at the ELO cap and observe whether the compute-ELO scaling law alters substantially. This proxy clearly neglects recursive self-improvement, but should otherwise give a lot of information on what to expect when trying to extend current methods beyond human-level.


### Does pretraining with preference data bake in safeguards?

Finetuning is one of the main safety mechanisms used in language models but it’s easy to undo, whether deliberately or accidentally. It’s widely believed that this is because finetuning creates ‘wrappers’ around capabilities without substantially altering those capabilities, and some [mechanistic interpretability analysis](https://arxiv.org/abs/2311.12786) supports this. It would be great to make these safeguards more robust - maybe if we include preference data in pretraining (either by pretraining with human feedback or DPO) then the safeguards will be more deeply integrated into the network and so harder to remove.


<!-- Footnotes themselves at the bottom. -->
## Notes

[^1]:
    Although the dragons are apparently [largely a modern invention](https://en.wikipedia.org/wiki/Here_be_dragons), with real medieval mapmakers preferring lions.

[^2]:
    Although this is true I think that it’s often overemphasised: a lot of basic understanding work could have been done much earlier - e.g. toy models of superposition, mechanistic interpretability, grokking, and deep double descent could all have been studied in the 90s (and often were to some extent, only for this work to be rediscovered or reinvented now). From an empirical perspective this is essential foundational science that’s needed to engineer safer systems.

[^3]:
    I acknowledge that although (a) and (b) seem uncomfortable bedfellows to me - how can you be confident that the current approach will both scale successfully and retain none of their important attributes while doing so? - they can certainly be made compatible.

[^4]:
     An alternative explanation is that the safety community believes that their opponents are primarily ultra-short-term individualists (e.g. the guy quoted in the first paragraph of [this essay by Michael Nielsen](https://michaelnotebook.com/oppenheimer/index.html)), idiots, or essentially eschatologically motivated like Rich Sutton and common ground is basically impossible to find. If this is the case then I'd appreciate having it confirmed! I don't think most people in AI who disagree with the safety community and/or don't support a pause fall into any of these camps - [even most self-professed e/accs don’t](https://twitter.com/daniel_271828/status/1728746552666030391).

[^5]:
    Although individuals often don’t change their mind in response to evidence (see Pauli’s famous comment about how science advances) the consensus of the field as a whole typically shifts.

[^6]:
     Empirical work doesn’t even necessarily have to be some huge heavy-duty effort. [This blog post](https://sohl-dickstein.github.io/2023/03/09/coherence.html) by Jascha Sohl-Dickstein is a neat example of doing some quick experimental work aimed directly at safety-relevant questions.

[^7]:
     Obviously there are some concerns on specific issues in biorisk but I think these are considerably overblown: if the information is already available by Googling then I think that it’s often not necessary to redact it from a paper.

[^8]:
     It’s certainly possible that in the long run this could lead to a sort of ‘controlled opposition’, or adversaries-for-hire designed to give the appearance of an adversarial collaboration without actually doing so. I’m not currently sure what to do about this, but at the moment I think you would find no shortage of good-faith, intelligent adversarial collaborators for basically every important question in safety.

[^9]:
     There’s also the possibility that some theoretical framework will provide an understanding of the effects of scaling that we can draw on for insight beyond current models, but this framework will almost certainly only come from careful theorising based on empirical results.
