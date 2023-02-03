# Awesome Skill Learning
Collection of resources on skill learning methods

## What is Skill Learning

[Blogpost on Skill Learning (WIP)](https://daniel-ch-tan.github.io/blog/2022/skill-learning/)
Tl;dr Learning reusable skills for downstream tasks.  

## Benchmarks

Challenging control environments in which skill learning would be useful
- MuJoCo: Multi-agent soccer environment [code](https://github.com/deepmind/dm_control/tree/main/dm_control/locomotion/soccer)
- MuJoCo: CMU motion-capture imitation environment [code](https://github.com/deepmind/dm_control/tree/main/dm_control/locomotion/mocap)
- IsaacGym: Humanoid adversarial motion prior [code](https://github.com/NVIDIA-Omniverse/IsaacGymEnvs/blob/main/isaacgymenvs/tasks/humanoid_amp.py)
- IsaacGym: Humanoid adversarial skill embedding [code](https://github.com/nv-tlabs/ASE)

## Theory
Foundational theory on abstracting the action space
- [AAAI 1999] Between MDPs and semi-MDPs: A framework for temporal abstraction in reinforcement learning: [paper](https://people.cs.umass.edu/~barto/courses/cs687/Sutton-Precup-Singh-AIJ99.pdf)
- Latent-variable methods

## Methods

### Skill Learning 
Learning to execute known skills. 

Complex motor skills for high-DoF robots, e.g. through imitation of motion-capture data. 
- [RSS 2020] Learning Agile Robotic Locomotion Skills by Imitating Animals [paper](https://arxiv.org/abs/2004.00784), [github](https://github.com/erwincoumans/motion_imitation)
- [PMLR 2020] CoMic: Complementary Task Learning & Mimicry for Reusable Skills [paper](https://proceedings.mlr.press/v119/hasenclever20a.html)
- [Arxiv 2022] Learning Agile Skills via Adversarial Imitation of Rough Partial Demonstrations [paper](https://arxiv.org/abs/2206.11693), [video](https://www.youtube.com/playlist?list=PLhqs0Oka9VRFrKb9djmEBU-NyewCKHfGP)

Other methods
- [ICRA 2021] Model Predictive Actor-Critic: Accelerating Robot Skill Acquisition with Deep Reinforcement Learning [paper](https://ieeexplore.ieee.org/stamp/stamp.jsp?tp=&arnumber=9561298), [code](https://github.com/dnandha/mopac)

### Skill Discovery
Learning to discover unknown skills. 

General methods based on e.g unsupervised RL objectives
- Quality-Diversity [website](https://quality-diversity.github.io/)
- [Arxiv 2018] Diversity is All You Need: Learning Skills without a Reward Function: [paper](https://arxiv.org/abs/1802.06070), [website](https://sites.google.com/view/diayn/), [code](https://github.com/ben-eysenbach/sac)
- [Arxiv 2020] Dynamics-Aware Unsupervised Discovery of Skills: [paper](https://arxiv.org/abs/1907.01657), [code](https://github.com/google-research/dads)
- [ICLR 2023] Efficient Planning in a Compact Latent Action Space: [paper](https://arxiv.org/abs/2208.10291), [code](https://github.com/ZhengyaoJiang/latentplan)

Methods focusing on motor skills for robots
- [CASE 2021] Building Skill Learning Systems for Robotics [paper](https://ieeexplore.ieee.org/stamp/stamp.jsp?tp=&arnumber=9551562)

### Transferring Skills to Tasks
Enabling transfer of pre-trained skills to downstream tasks. 

Policy distillation 
- [ICLR 2019] Neural probabilistic motor primitives for humanoid control [paper](https://arxiv.org/abs/1811.11711), [video](https://www.youtube.com/watch?v=CaDEf-QcKwA)

Hierarchical control (e.g. options)
- [Arxiv 2021] From Motor Control to Team Play in Simulated Humanoid Football [paper](https://arxiv.org/abs/2105.12196), [video](https://youtu.be/KHMwq9pv7mg)
- [ACM SIGGRAPH 2022] ASE: Large-Scale Reusable Adversarial Skill Embeddings for Physically Simulated Characters: [paper](https://arxiv.org/abs/2205.01906), [website](https://xbpeng.github.io/projects/ASE/index.html), [code](https://github.com/nv-tlabs/ASE)
- [Arxiv 2022] Leveraging Approximate Symbolic Models for Reinforcement Learning via Skill Diversity [paper](https://arxiv.org/abs/2202.02886)
- A Deep Hierarchical Approach to Lifelong Learning in Minecraft [paper](https://arxiv.org/abs/1604.07255)

Compositional policies
- [RSS 2020] Composable Energy Policies for Reactive Motion Generation and Reinforcement Learning [paper](http://www.roboticsproceedings.org/rss17/p052.pdf)

Program synthesis
- [Arxiv 2021] Learning to Synthesize Programs as Interpretable and Generalizable Policies [paper](https://arxiv.org/abs/2108.13643), [website](https://clvrai.github.io/leaps/)
- [Arxiv 2023] Hierarchical Programmatic Reinforcement Learning via Learning to Compose Programs [paper](https://arxiv.org/abs/2301.12950)

### Classical Robotics
Classical robotics heuristics for implementing high-quality 'skills'.

DMPs.
- [IEEETrans 2013] Dynamical Movement Primitives: Learning Attractor Models for Motor Behaviors [paper](https://ieeexplore.ieee.org/document/6797340)
- [Arxiv 2021] Dynamic Movement Primitives in Robotics: A Tutorial Survey: [paper](https://arxiv.org/pdf/2102.03861.pdf)

Hybrid zero dynamics
- [IEEETrans 2015] Hybrid Zero Dynamics of Planar Bipedal Walking [paper](https://web.eecs.umich.edu/~grizzle/papers/Grizzle_Westervelt_HZD_IsidoriFest.pdf)
- [IJRR 2019] Combining trajectory optimization, supervised machine learning, and model structure for mitigating the curse of dimensionality in the control of bipedal robots: [paper](https://journals.sagepub.com/doi/pdf/10.1177/0278364919859425)
  - This paper introduces generalized HZD which uses ML to interpolate HZD trajectories to obtain a control manifold. 

Other concepts: Locomotion gaits, Raibert heuristic. 