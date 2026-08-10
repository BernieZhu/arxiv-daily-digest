# arXiv Daily Digest — 2026-05-27

**Mode:** direct
**Categories:** cs.AI, cs.LG, cs.RO, cs.CV
**Keywords:** VLA, world model, world action model
**Papers found:** 3

---

## 1. FineVLA: Fine-Grained Instruction Alignment for Steerable Vision-Language-Action Policies

**Authors:** Xintong Hu, Xuhong Huang, Jinyu Zhang, ..., Shuai Bai, Tao Yu
**arXiv:** [2605.27284](https://arxiv.org/abs/2605.27284)
**Categories:** Robotics (cs.RO); Artificial Intelligence (cs.AI)

Vision-Language-Action (VLA) models are increasingly expected to not only complete robot tasks, but also follow human instructions about how those tasks should be executed. However, existing robot datasets usually pair trajectories with coarse goal-level language, leaving execution-critical details such as active arm, approach direction, and contact region unspecified. This limits steerable policy learning and robotic video understanding. We introduce FineVLA, an open framework for action-aligned fine-grained VLA supervision. The framework includes: (1) a data construction tool that unifies 972,247 trajectories across 85K tasks from 10 open-source robot datasets and builds FineVLA-Data, a human-verified dataset of 47,159 fine-grained trajectories; (2) a held-out benchmark with 500 videos, 10,816 atomic facts, and 1,030 VQA questions; (3) a robotics-specialized VLM annotator for scalable fine-grained annotation; and (4) a steerable VLA policy trained with controlled mixtures of fine-grained and raw goal-level instructions. Our experiments yield three findings. First, fine-grained supervision does not sacrifice goal-level success: FG-only improves over Raw-only by +1.4 to +8.1 success-rate points across settings. Second, fine-grained and raw instructions are complementary, following a consistent inverted-U trend peaking at FG:Raw = 1:2 to 1:1. The best mixed setting reaches 86.8%/82.5% in RoboTwin simulation and 62.7/100 in real-world dual-arm manipulation (vs. 49.9 Raw-only). Third, fine-grained supervision improves steerable control: the largest real-world gains appear on pose (+23), color (+18), and approach direction (+18)--factors where goal-level instructions provide no guidance. Overall, fine-grained language should augment goal-level instructions: specifying how to execute alongside what to achieve. Project page: this https URL

---

## 2. Scaling World-Model Reinforcement Learning Through Diffusion Policy Optimization

**Authors:** Xiaoyuan Cheng, Wenxuan Yuan, Zhancun Mu, ..., Zhuo Sun, Che Liu
**arXiv:** [2605.26282](https://arxiv.org/abs/2605.26282)
**Categories:** Machine Learning (cs.LG)

Model-based reinforcement learning (RL) can be effectively supported at scale through the use of world models. However, in practice, scaling such approaches remains fundamentally limited. A commonly recognized challenge is model bias and error compounding, which degrade long-horizon predictions. Beyond these issues, we identify a more critical yet underexplored bottleneck: a structural misalignment between search and value learning in existing world model approaches. In particular, policy improvement often relies on value functions induced by a separate, non-search policy, resulting in training inconsistency and ultimately suboptimal learning. To address this limitation, we propose Model-Based Diffusion Policy Optimization (MBDPO) in world models, a framework that unifies search and policy optimization through diffusion policy representations, thereby unlocking the potential of world models for scalable policy learning. Instead of constructing an explicit planner over a learned world model, we reformulate policy optimization as a diffusion process over searched trajectories in latent world models. In this view, we extract an implicit energy function from the collected dataset that anchors the policy, enabling MBDPO to refine the score field for policy optimization while mitigating misalignment. We evaluate MBDPO across a wide range of settings, including multi-task offline pretraining, online learning, and offline-to-online fine-tuning. In the offline regime, we further investigate its scaling behavior by pretraining on large-scale datasets, observing consistent and monotonic performance gains with increasing model capacity.

---

## 3. When Does LeJEPA Learn a World Model?

**Authors:** David Klindt, Yann LeCun, Randall Balestriero
**arXiv:** [2605.26379](https://arxiv.org/abs/2605.26379)
**Categories:** Machine Learning (stat.ML); Machine Learning (cs.LG)

A representation that scrambles the true degrees of freedom of the world cannot support reliable planning or compositional generalization. We prove that LeJEPA (alignment plus Gaussian regularization) linearly recovers the world's latent variables from nonlinear observations, a property known as linear identifiability, in a broad class of worlds where latents evolve under stationary, additive-noise transitions. Our main result is that among all such worlds, the Gaussian is the unique latent distribution for which this guarantee holds. The forward direction rests on a spectral decomposition in which each degree of nonlinearity is strictly penalized by alignment, making the linear map the optimum; the converse rules out every non-Gaussian alternative. We further prove an approximate identifiability result where the guarantee degrades gracefully, and show that linear, orthogonal identifiability enables optimal latent-space planning. We validate the theory with experiments ranging from 2D examples to 1024-dimensional latents, including distributional ablations and pixel-based robotic control. Our theory turns an empirically successful recipe into a mathematical guarantee, providing the foundation for building World Models that provably recover the structure of the world.

---
