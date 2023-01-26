# Awesome Skill Learning
Collection of resources on skill learning methods

## What is Skill Learning

As humans, we have learned certain patterns of whole-body actuation as high-level “skills” (walking, running, jumping, etc.) In planning our bodily actions, we do not consciously control each and every actuator (muscle) in our body.Rather,we largely constrain ourselves to these general and re-usable patterns, adapting and composing them on the fly to fit the situation. Why not do the same for robots?

I believe that learning of reusable, composable, and adaptable skills is essential to deploying agents in the lifelong learning setting.  

## Blog posts

- [Skill Learning (conflict-of-interest disclaimer: blogpost written by this repo's author)](https://daniel-ch-tan.github.io/blog/2022/skill-learning/)

## Papers

### Theory
Foundaational theory on abstracting the action space
- [AAAI 1999] Between MDPs and semi-MDPs: A framework for temporal abstraction in reinforcement learning: [paper](https://people.cs.umass.edu/~barto/courses/cs687/Sutton-Precup-Singh-AIJ99.pdf)

### Skill Discovery
Methods of skill discovery based on unsupervised RL objectives
- [Arxiv 2018] Diversity is All You Need: Learning Skills without a Reward Function: [paper](https://arxiv.org/abs/1802.06070), [website](https://sites.google.com/view/diayn/), [code](https://github.com/ben-eysenbach/sac)
- [Arxiv 2020] Dynamics-Aware Unsupervised Discovery of Skills: [paper](https://arxiv.org/abs/1907.01657), [code](https://github.com/google-research/dads)
- [ICLR 2023] Efficient Planning in a Compact Latent Action Space: [paper](https://arxiv.org/abs/2208.10291), [code](https://github.com/ZhengyaoJiang/latentplan)
- [ACM SIGGRAPH 2022] ASE: Large-Scale Reusable Adversarial Skill Embeddings for Physically Simulated Characters: [paper](https://arxiv.org/abs/2205.01906), [website](https://xbpeng.github.io/projects/ASE/index.html), [code](https://github.com/nv-tlabs/ASE)

### Classical Methods
Classical robotics methods has many methods of abstracting the action space, usually by employing some heuristics. This has the benefit of reducing the search space in e.g. online planning settings. We briefly mention some of these. 

DMPs.
- [IEEETrans 2013] Dynamical Movement Primitives: Learning Attractor Models for Motor Behaviors [paper](https://ieeexplore.ieee.org/document/6797340)
- [Arxiv 2021] Dynamic Movement Primitives in Robotics: A Tutorial Survey: [paper](https://arxiv.org/pdf/2102.03861.pdf)

Hybrid zero dynamics
- [IEEETrans 2015] Hybrid Zero Dynamics of Planar Bipedal Walking [paper](https://web.eecs.umich.edu/~grizzle/papers/Grizzle_Westervelt_HZD_IsidoriFest.pdf)
- [IJRR 2019] Combining trajectory optimization, supervised machine learning, and model structure for mitigating the curse of dimensionality in the control of bipedal robots: [paper](https://journals.sagepub.com/doi/pdf/10.1177/0278364919859425)
  - This paper introduces generalized HZD which uses ML to interpolate HZD trajectories to obtain a control manifold. 

Other concepts: Locomotion gaits, Raibert heuristic. 