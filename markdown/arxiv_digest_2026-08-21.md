# arXiv Daily Digest — 2026-08-21

**Mode:** direct
**Categories:** cs.AI, cs.LG, cs.RO, cs.CV
**Keywords:** VLA, world model, world action model
**Papers found:** 10

---

## 1. DECOWAM: Decoupled Whole-Body World-Action Model for Legged Mobile Manipulation

**Authors:** Siyuan Ma, Boshi Zhang, Yutian Zhang, ..., Dong Wei, Qiaojun Yu
**arXiv:** [2608.20114](https://arxiv.org/abs/2608.20114)
**Categories:** Artificial Intelligence (cs.AI); Robotics (cs.RO)

Mobile manipulation requires a robot to predict how locomotion and arm motion jointly alter future observations and control. Existing world-action models, developed largely for fixed-base platforms, do not explicitly distinguish camera ego-motion from base and arm actions. Here we introduce DECOWAM, a whole-body world-action model that separates these factors through dedicated conditional interfaces. DECOWAM freezes an adapted FastWAM backbone and trains residual adapters, an action-equivalent future bottleneck distilled from privileged observations, adversarially separated base and arm latents, and base-velocity conditioning for video prediction. We further introduce ARMDOG, a real-robot dataset that synchronizes video, whole-body state and action, and language. On a fixed replay protocol, DECOWAM improved both future-video and action prediction over FastWAM, reducing action MSE by 21.7% with 25.95M trainable adaptation parameters. Across 79 closed-loop trials per method, it achieved the highest observed whole-body coordination and base-displacement robustness among the compared systems, while task completion remained comparable to the strongest baseline. These results show that embodiment-aware factorization can support parameter-efficient joint visual prediction and whole-body control under moving viewpoints.

---

## 2. EXIMO: VLM Guided Exploration of VLA Policies

**Authors:** Bhavya Sukhija, Oliver Groth, Mohit Shridhar, ..., Abbas Abdolmaleki, Martin Riedmiller
**arXiv:** [2608.19891](https://arxiv.org/abs/2608.19891)
**Categories:** Artificial Intelligence (cs.AI)

How to efficiently finetune robot policies to learn new tasks on the fly? State of the art robotic manipulation policies are based on behaviour cloning of large vision-language-action (VLA) models with billions of parameters on huge teleoperation datasets. While this simple approach has enabled significant advances for robotic manipulation, finetuning of VLA policies for learning new tasks still remains an open problem. In particular, collecting teleoperation datasets requires hundreds of hours of expensive human labour and the alternative, reinforcement learning (RL), can be notoriously sample-inefficient especially for long-horizon tasks. In addition, RL with VLAs imposes several challenges due to the model's size and architectural design. In this work, we propose EXIMO, an efficient algorithm for finetuning of VLA policies. EXIMO operates in three stages: explore, imitate, and optimize. During the explore phase, EXIMO equips the VLA with a vision language model (VLM) that acts as a planner. The VLM thinks and breaks down challenging long-horizon problems into shorter ones for the VLA. The VLM, together with the VLA, is used to collect an orchestrated dataset on new tasks. During the imitate phase, the VLA is finetuned with the orchestrated data. Finally, during the optimize stage, we use residual off-policy RL to further finetune the policy. In our experiments, we ablate all three stages of EXIMO and show that it outperforms existing approaches significantly in terms of sample-efficiency and final performance.

---

## 3. ADAPT: Physics-Aware Diffusion-based World Models for Adaptive Predictive Transferable HVAC Control

**Authors:** Xu Yang, Kailai Sun, Dianyu Zhong, Qianchuan Zhao
**arXiv:** [2608.19804](https://arxiv.org/abs/2608.19804)
**Categories:** Artificial Intelligence (cs.AI)

Buildings account for roughly one-third of global energy consumption and CO$_2$ emissions. Optimizing indoor climate systems plays a critical role for urban climate mitigation aligned with UN Sustainable Development Goals 11 and 13. However, indoor delayed thermodynamic responses and partial observability severely hinder existing methods, which are primarily limited by implicit thermal inertia, occupancy dynamic prediction, and cumulative prediction errors, especially for out-of-distribution environments. In practice, these challenges are further exacerbated by the high cost and privacy burden of dense indoor sensing, forcing operators to collect only limited data in a single operating regime while expecting controllers to generalize reliably across unseen seasons and climate regions. To address this problem, we propose ADAPT, a physics-aware conditional diffusion indoor environmental world model for HVAC control. The model predicts a short-horizon held-action thermal baseline to capture the latent thermal inertia of the buildings. The diffusion backbone utilizes the robustness of generative models, while a learnable multi-zone heat-balance regularizer constrains generated trajectories to satisfy transferable building thermodynamics without requiring known building geometry or manually calibrated thermal parameters. A credit assignment is then design for the downstream reinforcement learning. Extensive experiments on SemibuildingSim and Sinergym demonstrate that ADAPT reduces HVAC energy consumption by 7.3\% and occupant discomfort by 30.2\% compared with state-of-the-art baselines under IID control. Under OOD control scenarios spanning unseen seasons and climate regions, ADAPT maintains robust performance with only marginal degradation relative to its IID performance, substantially outperforming existing methods in transfer robustness.

---

## 4. An Irreducible Quantum Advantage in Aligning World Models with Reality

**Authors:** Josep Lumbreras, Hailan Ma, Jayne Thompson, Mile Gu
**arXiv:** [2608.19779](https://arxiv.org/abs/2608.19779)
**Categories:** Quantum Physics (quant-ph); Artificial Intelligence (cs.AI); Machine Learning (cs.LG)

World models provide digital simulacra of the true world, allowing agents to be trained and tested before costly real-world deployment. At each time step, they receive an action and generate an observation and reward matching the statistics of the true world. In complex environments where present outcomes depend on events far in the past, this requires memory. One might expect that, by increasing memory, we can always build a model accurately enough to align the optimal agent policies of the real and virtual worlds. We show that this is false for classical world models, even when the true world itself is classical. We construct true worlds for which every finite classical model fails along the same possible trajectory: it either loses the ability to distinguish actions when the true world clearly prefers one, or repeatedly assigns the highest expected reward to suboptimal actions. Its expected-reward estimates also retain a nonvanishing average error. In contrast, each such true world admits a quantum world model using a single qutrit that reproduces it exactly: its reward estimates and preferred actions always match those of the true world, ensuring that the optimal policies of the real and virtual worlds remain perfectly aligned.

---

## 5. Orthogonal JEPA: Factorized Predictive States for Latent World Models

**Authors:** Taoyong Cui, Pheng Ann Heng, Wanli Ouyang
**arXiv:** [2608.20065](https://arxiv.org/abs/2608.20065)
**Categories:** Machine Learning (cs.LG)

World models construct latent states that support prediction, planning, and reasoning about an underlying system. Joint-embedding predictive architectures (JEPAs) offer a direct way to learn such states by predicting targets in representation space instead of reconstructing every detail of the observation. Standard JEPAs, however, organize all predictable content through one target embedding and one prediction pathway. In complex systems, this monolithic state can allocate redundant capacity to dominant signals while providing weak or conflicting gradients to less dominant predictive structure. We introduce \method, a latent world-modeling framework based on orthogonal predictive factorization. Learned basis matrices analyze each target state into multiple components, and a dedicated prediction branch estimates each component from a shared context representation. Predictive regression preserves the factor magnitudes required for state synthesis, an orthogonality objective discourages repeated directions, factor-activity regularization maintains variation in projected targets, and online variance regularization discourages coordinate-wise encoder collapse. Predicted components are synthesized into a complete latent state that can be used by a readout, decoder, planner, or autoregressive rollout. The same predictive-state mechanism applies when the target is temporally future, spatially hidden, or another partial observation of the same system. Experiments on controlled vision, single-cell transcriptomics, longitudinal health records, continuous control, and molecular dynamics evaluate representation quality, forecasting, planning, and long-horizon stability.

---

## 6. Fine-Tuning VLAs with Self-Demonstrated Generative Control for Multi-Task Manipulation

**Authors:** Prachi Garg, Steve Xing, Prahit Yaugand, Saurabh Gupta, Derek Hoiem
**arXiv:** [2608.19490](https://arxiv.org/abs/2608.19490)
**Categories:** Robotics (cs.RO); Computer Vision and Pattern Recognition (cs.CV); Machine Learning (cs.LG)

State-of-the-art vision-language-action (VLA) models such as $\pi_{0.5}$ exhibit strong semantic understanding, instruction following and task behavior. However, when deployed on new robots, even minor mismatches in hardware configuration relative to pretraining can cause severe performance drops. Finetuning the VLA on in-domain expert data from the new embodiment improves performance on the expert task but leads to a loss in its original instruction following and behavioral priors. In this paper, we propose a self-supervised method that generates online interaction rollouts from the zero-shot VLA as additional training data for finetuning. Our experiments show this finetuning scheme yields strong multi-task policies that, on the target robot, (1) inherit prior tasks distilled from the zero-shot model, (2) enable generalist instruction following, while (3) learning new skills from expert data with improved sample efficiency. We demonstrate the success of our approach across test sets probing generalization on a real ALOHA robot and a new simulation benchmark in RoboTwin. Video results are available at this https URL

---

## 7. World-Model-Grounded LLM Planning for AUV and ASV Navigation Near Offshore Wind Farms

**Authors:** Markus Buchholz, Ignacio Carlucho, Yvan R. Petillot
**arXiv:** [2608.19661](https://arxiv.org/abs/2608.19661)
**Categories:** Robotics (cs.RO)

Large language models can turn a natural-language mission into a sequence of robot actions, but they do not have a sense of physics: they cannot judge how long a command should run, or whether it will make the robot drift into an obstacle. We proposed the use of a world model to expand the capabilities of Large Language model-based planners. Our method has three components: a physics-grounded neural world model, a three-phase gradient-based trajectory optimizer, and a Model Predictive Controller (MPC)-style closed-loop replanner with a trust-region guard. The language model decides what to do, and the world model decides how long, whether that means driving eight thrusters through 6 DOF or two differential thrusters through 3 DOF. We evaluate two marine vehicle classes operating near offshore wind infrastructure: a 6-DOF Autonomous Underwater Vehicle (AUV) and a 3-DOF differential-drive Autonomous Surface Vehicle (ASV). In five benchmark missions per platform, both vehicles reach every goal with zero predicted collisions, and both transfer to GazeboSim under ocean current, waves, and thruster dynamics, remaining collision-free and cutting GazeboSim goal-distance error versus the ungrounded baseline by 70-82% (ASV) and roughly 93% (AUV), after a residual fine-tuning pass that separately reduces surrogate rollout Root Mean Square Error (RMSE) by 60% (AUV) and 69% (ASV). For the ASV we further demonstrate a Vision language model (VLM)-assisted semantic-mapping pipeline that extracts obstacles and environmental context from satellite imagery, nautical charts, and forecast Application Programming Interface (API) instead of onboard sensors, reaching 96% navigability accuracy as a drop-in replacement for hand-specified obstacle geometry.

---

## 8. OrthoSkillVLA: Continual Skill Learning via Gradient-Informed Skill Subspace Adaptation

**Authors:** Jiaqi Wang, Zhou Fang, Qiongfeng Shi, Yi Zhou
**arXiv:** [2608.19589](https://arxiv.org/abs/2608.19589)
**Categories:** Robotics (cs.RO); Computer Vision and Pattern Recognition (cs.CV)

Pretrained Vision-Language-Action models provide a strong foundation for robot learning, but sequentially adapting them to diverse skills can perturb the representations and velocity mappings used by previous skills, leading to catastrophic forgetting. Architecture-based approaches improve retention by isolating skills but lead to increased inference footprint. Recent subspace-constrained methods restrict parameter updates in an orthogonal subspace to minimize interference but impose a unified constraint on the entire model. We analyze the distinct roles of internal VLA components and identify two VLA-specific challenges. First, the VLM maintains broad semantic representations, making it vulnerable to capacity exhaustion, whereas the ActionHead refines semantics into localized velocity patterns that are highly sensitive to perturbations. Second, the final velocity decoder serves as a readout layer. Freezing it forms an output-stage expressivity bottleneck, while updating it risks overwriting previous velocity mappings. To this end, we propose OrthoSkillVLA, a parameter-efficient framework for continual skill learning in pretrained VLA models without demonstration replay. Given the representation heterogeneity, we impose separate subspace constraints on the VLM and ActionHead, preserving reusable semantic capacity while protecting localized velocity patterns. For the output layer, we introduce a lightweight feature-aware MoE decoder, where each skill is allocated a compact expert and a training-free router selects the expert according to feature-space affinity. Extensive simulated and real-world evaluations, together with ablations, demonstrate that OrthoSkillVLA better preserves prior skills while acquiring new ones.

---

## 9. HiTac-WAM: A Hierarchical Tactile World Action Model for Contact-Rich Robot Manipulation

**Authors:** Chao Xue, Chaofan Zhang, Wenxuan Ma, ..., Shaowei Cui, Shuo Wang
**arXiv:** [2608.19574](https://arxiv.org/abs/2608.19574)
**Categories:** Robotics (cs.RO)

World action models jointly predict future visual observations and actions, whereas existing tactile-aware variants typically represent future touch as an image or latent stream without modeling the physical dependencies that organize tactile states hierarchically. We present HiTac-WAM, a hierarchical tactile world action model that forecasts a sequence of future tactile states for each candidate action chunk before execution. The forecast factorizes into contact state, a 3D deformation field, and slip risk, organized as a directed hierarchy in which each downstream stage is conditioned on stop-gradient signals from preceding stages. A directed attention mask allows tactile queries to attend to the video-action context of each candidate while preventing video and action queries from attending to tactile tokens. For planning, HiTac-WAM ranks candidate action chunks using tactile forecasts and task-progress estimates. For execution, the selected tactile forecast is retained as a reference; persistent discrepancies between predicted and observed tactile states trigger corrective replanning. HiTac-WAM achieves a mean contact F1 of 0.921; under matched training budgets, the directed hierarchy reduces 3D displacement L2 error by 17.6% relative to the deformation-only predictor and improves slip AUPRC by 60.4% relative to the slip-only predictor. Across chip grasping, blackboard erasing, and USB insertion, selection guided by the hierarchical forecasts increases the average real-robot success rate from 31.1% to 61.1%, while the full system attains 72.2%.

---

## 10. Towards Surgical World-Action Modeling: A Preliminary Joint Visual-Trajectory Forecasting for Surgical Motion Planning

**Authors:** Weiliang Huang, Huanrong Liu, Bob Zhang, ..., Guy Rosman, Qingbiao Li
**arXiv:** [2608.20284](https://arxiv.org/abs/2608.20284)
**Categories:** Computer Vision and Pattern Recognition (cs.CV); Robotics (cs.RO)

Reliable surgical planning requires models to anticipate not only how instruments will move, but also how the operative visual state will evolve together with such motion. Existing approaches typically treat future scene generation and instrument trajectory prediction as two separate tasks. Scene-only models cannot directly evaluate the accuracy of future instrument motion at the trajectory level, while trajectory-only models fail to capture the visual consequences of instrument movement, leaving the consistency between predicted trajectories and future scene evolution unaddressed. Jointly forecasting both provides a more complete account of surgical action-scene dynamics by enabling explicit trajectory-level evaluation while simultaneously modeling the corresponding visual evolution. To bridge this gap, we present a preliminary joint visual-trajectory world-action model that simultaneously forecasts future visual states and instrument trajectories from historical surgical observations. Specifically, we encode historical video frames and tool trajectories into latent representations, which are processed by a temporal-spatial encoder and subsequently decoded through separate visual-state and trajectory prediction heads. Based on this preliminary architecture, a chunked autoregressive rollout is repeatedly applied to predict fifteen future steps. The chunked strategy consistently outperforms direct one-shot prediction across all evaluated horizons, improving first-segment PSNR from 18.86 to 23.11 dB and reducing ADE from 45.77 to 22.22 pixels. These results demonstrate the initial feasibility of joint visual-motion forecasting. However, we observe progressive visual degradation and accumulated trajectory errors over longer prediction horizons, which remain important challenges for future surgical world-action modeling.

---
