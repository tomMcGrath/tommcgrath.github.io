# Research interests
My research covers two main themes: inference of patterns that drive behaviour, and physical constraints on inference. I study both of these through a combination of statistical physics, Bayesian inference, and information theory. 

I'm currently studying feeding behaviour as a prototype for more complex motivated behaviours - it's a fundamental behaviour which is shared across species, but is rich enough to include aspects of reward, learning, and planning. With mice we also have good _in vivo_ access to measure and control the neural populations underlying feeding ([review](http://www.cell.com/cell-metabolism/abstract/S1550-4131(15)00617-8)), so we can expect a better back-and-forth between experimental and theoretical studies than is possible with complex human behaviours we might eventually want to understand.

Longer-term I'm interested in AI safety, particularly on how uncertainty can be factored into decision-making. A good example of this is [Bayesian defence against adversarial examples](https://arxiv.org/abs/1703.00410) - uncertainty over classification is a good way to detect adversarial attacks. Uncertainty can be a useful tool for learning as well; Bayesian optimisation can tell us what agents need to know. For these reasons, I'm interested in exploring uses of [distributional approaches to reinforcement learning](https://arxiv.org/abs/1707.06887) in AI safety.

I'm also interested in practical applications of inverse reinforcement learning (see below) - this seems likely to play an important role in value alignment in the long term, but right now we have few case studies to discover practical issues or subtleties that might be of interest.

# Contact me
[Email](mailto:thomas.m.mcgrath@gmail.com) is probably best, but you can reach me on [LinkedIn](https://www.linkedin.com/in/tom-mcgrath-7337bb151/) as well.

# Current research
## Inverse reinforcement learning for animal preferences
Feeding behaviour has the potential to become an experimental testbed for comparing current reinforcement learning techniques with biological systems that might implement them. The first step along this path is to try to learn the reward values of physiological states from behaviour. 

By reusing data sources from my previous work (below) in conjunction with [maximum entropy inverse reinforcement learning](https://www.aaai.org/Papers/AAAI/2008/AAAI08-227.pdf) I intend to find out if this is possible, and to infer the effects of drugs and nutritional state on reward if so. This will create a model that could be run alongside _in vivo_ measurement of neural activity in order to determine whether 'normative' reward values have any connection to neural activity.

# Finished projects
## Stochastic modelling of rat feeding behaviour
With Nick Jones, Kevin Murphy, and other researchers from Medicine we came up with a stochastic process model of rat feeding in order to understand how drugs, fasting and time of day affected patterns of feeding behaviour. By using a Bayesian hierarchical model we were able to study inter-individual variation in a data-efficient way and do accurate inference even with relatively small datasets for each animal.

We were able to identify exactly what effect each drug had on behaviour, as well as do _in silico_ testing to try out optimised therapies and behavioural changes. It turns out that inter-individual variation in behaviour is pronounced, even for genetically identical animals in the same conditions, which has implications for the structure of models that attempt to infer reward functions from behaviour (see above).

### Publications
_Interpretable forecasting and control of feeding behaviour at the micro and mesoscale_; T. McGrath, E. Spreckley, A.F. Rodriguez, A. Alamshah, E. Akalestou, K.G. Murphy, N. S. Jones; In preparation

_Quantitative approaches to energy and glucose homeostasis: machine learning and modelling for precision understanding and prediction_; T. McGrath, K.G. Murphy, N.S. Jones; Under review

## Biochemical machines for interconversion of information and work
With [Tom Ouldridge](https://www.imperial.ac.uk/people/t.ouldridge) and [Pieter Rein ten Wolde](https://amolf.nl/research-groups/biochemical-networks) I worked out the properties of what could be described as a 'biochemical Maxwell's Demon': a machine made of biologically-available parts designed to allow the conversion between mutual information and energy. 

We found and explained a number of interesting results, including the existence of an 'information catalyst' regime, where although the mutual information is left unchanged (or even increases) during the machine's operation, its efficiency is improved.

### Publications:
_[Biochemical Machines for the Interconversion of Mutual Information and Work](https://arxiv.org/abs/1604.05474)_; T. McGrath, N.S. Jones, P.R. ten Wolde, T.E. Ouldridge; Physical Review Letters, 2017

# Non-research projects
## Maths Helpdesk
I am part of the team that runs Imperial College's [Maths Helpdesk](http://mathshelpdesk.ma.ic.ac.uk/). The aim of the helpdesk is to put researchers who have a mathematical problem in touch with people across the maths and statistics department who could help them. We've just got funded for another year, and plan to run a lot of events in 2017/18 including dropin sessions, hackathons, and courses in useful techniques.

## Deep Learning study group
I started this because I saw that a lot of people were interested in learning to use deep learning techniques, but that following a MOOC online was slower and less successful for many people than working in a group. We met weekly to work through the exercises for [fast.ai](course.fast.ai). This was a success and I plan to run this again in 2018, and may start a Deep RL study group if there's enough interest.

## AI Safety research accelerator
I'm currently co-organising a 'research accelerator' for AI safety, to be held sometime in 2018. Safety research is widely considered to be both [important](https://www.openphilanthropy.org/focus/global-catastrophic-risks/potential-risks-advanced-artificial-intelligence) and [talent-limited](https://80000hours.org/career-reviews/artificial-intelligence-risk-research/). The aim of this event is to try and mitigate this to some extent; we intend to take people with research experience and an interest in AI safety, and to give them a space to work intensely on collaborative group projects in order to make it easier for people to transition into working on this problem.

We're currently looking for participants, as well as experienced researchers who might be willing to advise teams. If you're interested, please let us know [here](https://docs.google.com/forms/d/e/1FAIpQLSfqnmz3WVPPahSp-qCcZ-jbMLbwtfVqt2feHaufxou8jv_vrg/viewform).
