# arXiv Daily Digest — 2026-08-31

**Mode:** direct
**Categories:** cs.AI, cs.LG, cs.RO, cs.CV
**Keywords:** VLA, world model, world action model
**Papers found:** 6

---

## 1. AcrossVAM1.0: Particle World Modeling for Text-Assisted Robot Video Prediction

**Authors:** Yafei Zhang, Nan Wu
**arXiv:** [2608.28491](https://arxiv.org/abs/2608.28491)
**Categories:** Artificial Intelligence (cs.AI); Robotics (cs.RO)

Predicting robot videos requires both precise motion reasoning and preservation of high-frequency appearance, yet monolithic pixel models entangle these objectives and often conceal their progress behind a strong last-frame baseline. We present AcrossVAM1.0, a lightweight, text-assisted video action model that factorizes future prediction into object-centric motion and dense appearance. A frozen SAM3-DLP codec decomposes four context frames into semantic particles for the robot, arm, and gripper, together with a background latent. A 0.28M-parameter spatio-temporal Transformer aligns particle identities, rolls their states forward, and is modulated by a frozen OpenCLIP instruction embedding through FiLM. A causal dual-stream decoder combines particle-rendered motion with appearance encoded exclusively from the last observed frame; a residual refiner and learned delivery mask produce five future frames without access to future appearance. On our VRS benchmark constructed from diverse real-robot trajectories, particle dynamics reduce trajectory error by 21.0\% over persistence. Across three delivery-mask seeds, AcrossVAM1.0 improves future-frame PSNR/SSIM from 19.97/0.796 to 20.573/0.8004, while raw particle generation improves motion-region PSNR from 11.89 to 13.23. The delivered model does not yet beat persistence in LPIPS, and correct-versus- shuffled language changes trajectory error by only 2.8--3.1%. We report these limitations alongside oracle, negative-control, multi-seed, and per-robot analyses. The results show that explicit particle dynamics are a promising low-dimensional interface for robot video prediction, while robust language grounding and appearance delivery remain the principal open challenges.

---

## 2. WM-R1: Training GUI Agents to Reason and leverage World Models with Reinforcement Learning

**Authors:** Yu Han, Tianwen Qian
**arXiv:** [2608.27508](https://arxiv.org/abs/2608.27508)
**Categories:** Artificial Intelligence (cs.AI)

GUI agents trained with reinforcement learning (RL) have showcased strong environment learning capabilities on mobile platforms. However, RL typically demands extensive real-environment interactions, leading to high resource costs and instability, especially in GUI scenarios. To address these, we propose WM-R1, the first reinforcement learning framework that trains mobile GUI agents with world models instead of real environments. Specifically, world models serve as the source of state transitions during all rollouts, replacing the real Android environment within the training loop. WM-R1 also embeds world models directly into the thinking process, enabling agents to reason about the consequences of candidate actions before committing to the final action. Crucially, WM-R1 eliminates the need for real-environment interaction, supports massively parallelized and step-level granularized trajectory generation grounded in world models, and introduces a multi-dimensional rule-based reward that jointly optimizes task success, trajectory efficiency, and world model utilization. For efficient training, we curate a high-quality dataset of 2000 challenging tasks. Experiments on Android mobile benchmarks demonstrate that WM-R1-trained agents significantly outperform GRPO-only baselines and inference-time simulation methods. Code is available at this https URL .

---

## 3. An Enclosed Mode Is a Gauge Choice: Topology Relative to Reach in Certified Code World Models

**Authors:** Javier Aguilar Martín
**arXiv:** [2608.28541](https://arxiv.org/abs/2608.28541)
**Categories:** Machine Learning (cs.LG); Artificial Intelligence (cs.AI); Systems and Control (eess.SY)

A code world model accepted by a sampling gate can be exactly right on everything the gate can see and arbitrarily wrong beyond it. We characterize what a certified model can know, and what its errors can cost, when the omission is an annular freeze mode enclosing an unreachable interior. The gate quotient makes the question precise: acceptance-with-certainty determines the model exactly on the reachable query set; beyond reach is gauge. On a minimal ring instrument we prove the extreme case (a wrong-topology filled-disc artifact unfalsifiable by any sampling gate and bitwise harmless at play) and measure, with LLM synthesis across three model families, how one knob (a channel of width gamma) walks the same artifact through three regimes: unfalsifiable-and-harmless, falsifiable-and-costly, and instantly falsified. Three principles organize the empirics. First, danger is topology relative to reach: a channel the planner can use collapses the blind model's exploitation (play cost 1.09 to ~0 over a knee at gamma ~ 0.1), while a hidden channel with the same first Betti number keeps it at full strength (1.12). Second, repair is parameter-bound and sensor-bound: no family recovers the region from outside evidence; from inside, models pose the right topology but cannot pin its parameters, and the posed topology tracks the guiding persistent-homology summary's wrong beta_1 (a sensor with a measured geometric resolution limit), not the truth. Third, mitigation must match the error's dimension and direction: point fences fail against the one-dimensional boundary, a dimension-matched persisted fence collapses exploitation to a two-lesson transient (0.999 to 0.058), and the dual freedom certificate collapses the invented-mode failure symmetrically (1.769 to 0.029). In n dimensions the shell makes misidentification near-certain while the danger stays fully exploitable: the two axes are independent.

---

## 4. PHR-VLA: Planning Horizon Reasoning for Vision-Language-Action Models

**Authors:** Davood Soleymanzadeh, Kaidi Zhang, Zhiyuan Zhang, ..., Yu She, Minghui Zheng
**arXiv:** [2608.27609](https://arxiv.org/abs/2608.27609)
**Categories:** Robotics (cs.RO); Artificial Intelligence (cs.AI)

Vision-language-action models (VLAs) have shown strong promise for general-purpose robotic manipulation by mapping language instructions and vision observations directly to actions. However, most VLAs primarily condition action prediction on current observations and lack an explicit mechanism for reasoning over future task dynamics, which is particularly important for fine-grained, contact-rich manipulation. We present PHR-VLA, a framework that enables planning-horizon reasoning in VLAs through privileged latent representations of future dynamics. PHR-VLA introduces a lightweight auxiliary future head that, during training, aligns the VLA's internal representations with latent dynamics extracted from future observations. Evaluation results demonstrate that local, contact-centric, patch-level latent dynamics supervision from the wrist camera improves success rate on LIBERO from 84.1% to 88.4% and on real-world disassembly tasks from 63.3% to 82.5%. Patch-level supervision from a third-person camera also improves performance on Meta-World from 56.70% to 57.8%. These results demonstrate that privileged latent dynamics alignment provides an effective training signal for improving anticipatory reasoning in VLA policies. Project website: \href{this https URL}{this https URL}

---

## 5. DeicticVLA: Unifying Instruction Modes Based on Language and Deictic Gestures in a Single VLA

**Authors:** Kango Yanagida, Tatsuya Aoki, Yuichiro Yoshikawa, Takato Horii
**arXiv:** [2608.28108](https://arxiv.org/abs/2608.28108)
**Categories:** Robotics (cs.RO); Computer Vision and Pattern Recognition (cs.CV)

Vision-Language-Action models (VLAs) allow users to specify manipulation tasks in natural language, but distinguishing a target or placement goal among objects of the same category or similar appearance requires detailed expressions that VLAs may not use reliably. We propose DeicticVLA, which canonicalizes Language Instruction (LI), Vision-Language Instruction (VLI), and Visual Instruction (VI) into a text prompt and deictic masks through text-prompt completion and deictic gesture grounding, enabling a single pretrained VLA to handle all three instruction modes. With a shared backbone, demonstrations, and matched training steps, we compare two RGB visual prompting methods, two separate-channel mask prompting methods, and three training strategies in simulation. Under two-stage training, the four prompting methods achieve high in-distribution success but differ in their ability to use deictic masks in unseen layouts. Across methods, training-strategy ablations show that two-stage training improves such use, while retaining second-stage LI data mitigates forgetting without reducing VLI and VI performance. In three real-world tasks, one policy supports all modes. VLI and VI outperform LI under unseen expressions, appearance changes, and novel objects. For unseen categories, both achieve 100% success, compared with 16.7% for jointly trained LI. These results demonstrate the unified three-mode interface and guide DeicticVLA design.

---

## 6. Beyond Data Scaling: Representation-Centric Continued Pre-training for Vision-Language-Action Models

**Authors:** Senqiao Yang, Chengyao Wang, Yuxin Chen, ..., Bei Yu, Jiaya Jia
**arXiv:** [2608.27550](https://arxiv.org/abs/2608.27550)
**Categories:** Robotics (cs.RO); Computer Vision and Pattern Recognition (cs.CV)

Scaling robot data is crucial for building generalist Vision-Language-Action (VLA) models, yet robot trajectories are harder to scale than web-scale image-text data because embodied collection is costly and sparsely covers the physical world. This makes representation quality a central bottleneck: under a fixed robot-data budget, continued pre-training must turn limited trajectories into transferable visual-action knowledge rather than merely fit actions. We propose VLAct, a VLA-oriented VLM backbone trained on broad, heterogeneous, multi-embodiment robot data before task-specific fine-tuning. VLAct preserves the broad VLM prior and encourages shared action semantics across embodiments through VLM-prior preservation, multi-head continuous action co-supervision, and a partially unified cross-embodiment action layout, while allowing task-specific action heads during fine-tuning. Across simulation, real-world, and unseen-embodiment transfer, VLAct consistently improves downstream performance under fixed fine-tuning protocols. On LIBERO-Plus and RoboTwin 2.0, VLAct surpasses industrial VLA systems including ABot-M0 and LingBot-VLA, achieving success rates of 82.6% and 92.5%. On RoboDojo, VLAct ranks sixth among all policies by success rate and outperforms all explicitly designated world-action model (WAM) entries on both metrics. Most notably, on RoboCasa-GR1, an unseen humanoid embodiment, VLAct using only 20% of downstream trajectories outperforms the full-data GR00T-N1.6 baseline. These results are obtained using fully open-source data and only a 16-GPU training setup, showing that representation-centric continued pre-training can deliver highly competitive performance under a modest compute budget and is an important independent axis of VLA progress beyond data scaling.

---
