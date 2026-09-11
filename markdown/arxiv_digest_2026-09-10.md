# arXiv Daily Digest — 2026-09-10

**Mode:** direct
**Categories:** cs.AI, cs.LG, cs.RO, cs.CV
**Keywords:** VLA, world model, world action model
**Papers found:** 11

---

## 1. Time-Frequency Geometric Cross-Attention for Chunked Vision-Language-Action Models

**Authors:** Shengye Dong, Haochen Niu, Hao Liu, ..., Chuang Wang, Shanmin Pang
**arXiv:** [2609.09925](https://arxiv.org/abs/2609.09925)
**Categories:** Artificial Intelligence (cs.AI); Robotics (cs.RO)

Modern vision-language-action (VLA) policies predict a whole chunk of actions: one to two seconds of coordinated motion emitted in a single forward pass. Yet an action chunk is essentially a short multivariate trajectory, but inside these models it is a sequence of generic per-timestep hidden tokens decoded by a linear head. This under-serves two motion structures. First, frequency: a chunk superimposes a smooth global trend and fine corrective motion across time scales, and a single token entangles them. Second, cross-phase geometry: motions of different phases (reach, contact, grasp adjustment, settling) unfold along very different, near-orthogonal directions in representation space, yet are tightly related for the task and arise across the time axis. Dot-product attention scores alignment by an inner product, so it favors aligned tokens and is least sensitive near orthogonality, leaving such relationships for the network to recover through a detour.
We introduce Time-Frequency Geometric Cross-Attention (TFGCA), a drop-in module repairing both blind spots. TFGCA uses a per-dimension learnable stationary wavelet transform to decompose the action chunk into time-frequency tokens, and each time token retrieves information from them via a cross-attention that fuses the dot product (similarity) with the wedge-product magnitude (sensitive to near-orthogonality) through a learnable weight. A zero-initialized residual reproduces the base behavior at initialization, so it can be dropped onto a pretrained VLA and fine-tuned jointly. Relative to the same-source base, TFGCA improves in-distribution LIBERO by +1.5 on average, the OOD LIBERO-Plus by +6.3, the randomized average under RoboTwin domain randomization by +28.5, and the overall success rate on three real-robot AgiBot A2 tasks by +11.67 points, with larger gains out of distribution.

---

## 2. Valerant: An Automatic Navigable Game Map Generator via Action-Conditioned World Model Exploration

**Authors:** Yiran Qiao, Feng Wang, Jing Ma
**arXiv:** [2609.09418](https://arxiv.org/abs/2609.09418)
**Categories:** Artificial Intelligence (cs.AI)

World Action Models (WAMs) couple predictive world modeling with action generation, allowing anticipated future states to guide agent behavior. Although WAMs are rapidly advancing embodied AI, general-purpose counterparts remain largely unexplored in games. Existing game-oriented approaches often combine action-conditioned world models with external policies and reward functions to realize WAM-like decision-making, yet they operate mainly in 2D visual observation space and do not instantiate persistent 3D geometry. Extending this paradigm to 3D games introduces a distinct challenge. In autonomous driving and robotics, the physical environment exists independently of the model, providing a persistent 3D world in which selected actions can be executed. Games have no such external substrate; the virtual world itself must be instantiated. Most playable games require a persistent and navigable space, while 3D games additionally require explicit geometry that supports movement and interaction. Action-conditioned video rollouts provide visual observations but not this spatial representation. We present \textsc{Valerant}, a training-free framework that transforms a pretrained action-conditioned world model into a WAM for exploring and constructing 3D game maps. By coupling predictive visual rollouts with SLAM-based spatial reconstruction and exploration-driven action selection, \textsc{Valerant} progressively transforms a single image into a persistent 3D game map. This framework extends WAM-based interaction beyond 2D visual simulation and offers a new approach to reducing manual effort in 3D game-map creation.

---

## 3. Compact Visuotactile World Models for Lifting: Prediction, Reward Alignment, and Force Constraints

**Authors:** Qinzhen Ma
**arXiv:** [2609.09597](https://arxiv.org/abs/2609.09597)
**Categories:** Robotics (cs.RO); Artificial Intelligence (cs.AI)

Accurate tactile forecasts need not improve force-constrained control. We study a 652,157-parameter action-conditioned visuotactile world model with matched behavior cloning, policy learning in imagination, independent reactive implicit Q-learning, and model-assisted force feedback. A fixed protocol executes 34 policies on 120 fresh MuJoCo environments spanning geometry and physical-parameter shifts, plus 324 independently replayed action branches on 12 additional ID environments. Visuotactile dynamics reduce force action-effect MAE from 0.413 N for persistence to 0.338 N. Model-assisted feedback raises ID force-budgeted success from 73.3% to 93.3%, with paired difference +20.0 [+6.7,+33.4] percentage points (95% CI), with the difference occurring during scripted lowering. Its pooled difference is +3.9 [-4.5,+11.7] points. Imagined RL achieves 11.9% pooled joint success versus 25.0% for reactive IQL. An empirical tactile-residual stress test adds 330 executions. The evidence concerns rigid-box lifting after a common approach, without physical-robot transfer or a closed-loop safety guarantee.

---

## 4. World-Time Compute with Verified Code World Models

**Authors:** James Schwoebel, Ingrida Semenec, Jenia Rousseva, ..., Jessica Tsai, Martin G. Frasch
**arXiv:** [2609.09163](https://arxiv.org/abs/2609.09163)
**Categories:** Machine Learning (cs.LG)

LLMs generalize across a domain only after seeing many real, labeled examples, which most domains lack. We study a way to manufacture it cheaply. When a domain's dynamics can be written as code, one template instantiates into many world models: executable, verifiable programs over symbolic state, each an inexhaustible source of exactly-labeled trajectories. Fine-tuning an LLM on trajectories through many such worlds, which we call world-time compute, a training-time analogue of test-time compute, lifts generalization to held-out worlds it never trained on (synthesized world families). Gains are largest where capability is scarcest: +29 points at 0.5B; the largest model's lift is within noise, consistent with saturation. Labels can be trusted because the worlds are verified code: synthesized-then-checked dynamics are exact over 20-step rollouts and answer 10x out-of-distribution probes exactly (100%), whereas per-step LLM and MLP predictors compound error and collapse. Unlike domain randomization, each world is independently authored and verified; a corrupted-label control shows label exactness, not task variety, drives the gains. On real benchmarks (ARC-AGI grids, List Functions, CLRS) the same lever holds as per-world test-time training. On List Functions the harder cross-world form holds: one adapter trained on 128 disjoint worlds reaches 40% on held-out worlds versus 6% for a corrupted-label control (+34 points, CI [29, 39]). The gain is a saturating regularity, not a law: largest for few-step reasoning and small/weak models, fading for long chains, perception-induced tasks, and saturated tasks; cross-task transfer is weak without shared skill. Worlds are authored and served by OpenWorld, a zero-dependency framework (companion paper). Scope: symbolic state; pixel-native domains remain territory of learned models. All code, recipes, and this manuscript regenerate from one repository.

---

## 5. DUET-DINO: Simultaneous Cross-View World Modeling for Latent Planning in Robot Manipulation

**Authors:** Nisarga Nilavadi, Ralf Römer, Moritz Reuss, ..., Rudolf Lioutikov, Wolfram Burgard
**arXiv:** [2609.10506](https://arxiv.org/abs/2609.10506)
**Categories:** Robotics (cs.RO); Computer Vision and Pattern Recognition (cs.CV)

Action-conditioned latent world models predict future visual representations, enabling zero-shot goal-conditioned robot planning and control. However, their predictions for fine-grained spatial and rotational actions are unreliable for full 7-DoF end-effector control. To address this gap, we introduce DUET-DINO, a simultaneous cross-view latent world model that jointly learns action-conditioned predictions from static side- and wrist-camera observations through cross-view conditioning. By exploiting complementary global scene and gripper-centric information, DUET-DINO enables latent planning over the full 7-DoF action space. Across spatially diverse reach, orientation-intensive angled-reach, and multi-goal grasp-and-lift tasks, DUET-DINO consistently outperforms single-view and independent dual-view baselines, achieving 92% success on reach, 72.5% on angled-reach, and 60.0% on lift tasks. DUET-DINO is trained from scratch on DROID and RoboArena datasets and generalizes robustly under visual distribution shifts. We further show that while V-JEPA 2 wrist-view predictions underestimate visual dynamics induced by fine-grained actions, DINOv3 predictions better capture action-conditioned scene changes, leading to stronger downstream planning. The code and model checkpoints will be open-sourced. Project page: this https URL

---

## 6. Frequency-Conditioned Flow Matching for Vision-Language-Action Models

**Authors:** Haochen Niu, Shengye Dong, Hao Liu, Peiwen Lin, Wang Chuang
**arXiv:** [2609.10405](https://arxiv.org/abs/2609.10405)
**Categories:** Robotics (cs.RO)

Robot actions are temporally correlated trajectories whose frequency components encode motion at different scales with highly non-uniform energy distributions. Yet Flow Matching--based vision-language-action (VLA) models typically generate actions in temporal coordinates, without explicitly modeling or systematically leveraging this frequency heterogeneity. We introduce \emph{FreqFM}, a frequency-conditioned Flow Matching framework for VLA models. It raises action frequency from an implicit trajectory property to an explicit conditioning dimension that spans the entire generation pipeline. Concretely, in DCT frequency coordinates, FreqFM constructs a spectrum-matched source distribution, adaptively balances the objective across frequencies, and constrains per-frequency guidance residuals using the corresponding reference transport scales. FreqFM integrates into existing Flow Matching action experts without changing the VLA backbone. Across LIBERO, LIBERO-Plus, and VLA-Arena, FreqFM consistently improves performance, including a 9.3-point gain on LIBERO-Plus, and further demonstrates its effectiveness on six real-robot tasks.

---

## 7. RoboDrop: Curating VLA Post-Training Data via Local Gradient Compatibility

**Authors:** Runze Xu, Yuanfan Xu, Cuijie Xu, ..., Yu Wang, Jincheng Yu
**arXiv:** [2609.10021](https://arxiv.org/abs/2609.10021)
**Categories:** Robotics (cs.RO)

Vision--language--action (VLA) models acquire broad generalization through large-scale pretraining, yet adapting them to a new task and robot embodiment still requires post-training on newly collected data. Unlike pretraining, post-training targets task- and embodiment-specific adaptation, making it particularly sensitive to data quality. In practice, collected robot datasets often contain heterogeneous errors, including execution mistakes, sensor drift, and timestamp misalignment, which can impair post-training and policy performance. Manual inspection is costly, while existing data-cleaning methods are typically tailored to particular corruption types. To address these challenges, we introduce \textsc{RoboDrop}, a data-curation framework that audits supervision using local gradient compatibility measured along the training trajectory as a proxy for its effect on post-training performance. During a one-epoch warm-up run, RoboDrop scores each candidate sample online by comparing its gradient with those of task-semantic and visually matched validation samples. The resulting sample scores are aggregated at the episode level, and a simple automatic post-processing rule converts them into filtering decisions. We evaluate RoboDrop on controlled observation--action corruptions, naturally suboptimal demonstrations in simulation, and real-robot datasets containing non-expert collection errors. Across these settings, RoboDrop more accurately distinguishes unreliable demonstrations than prior methods, while post-training on the curated data consistently yields stronger downstream policies, with average real-robot rollout success rising from $35.0\%$ to $67.5\%$. These results establish training-trajectory-aware, context-conditioned supervision auditing as an effective approach to robust VLA post-training.

---

## 8. HaWMPO: Hallucination-Aware World Model-based Policy Optimization for Generalist Robot Policy

**Authors:** Zengjue Chen, Peidong Liu, Jiawei Li, Qi Wang
**arXiv:** [2609.09941](https://arxiv.org/abs/2609.09941)
**Categories:** Robotics (cs.RO)

Generalist robot policies have demonstrated strong generalization across robotic manipulation tasks, yet their success rates remain limited in com- plex long-horizon scenarios. Recent methods improve Visual-Language-Action (VLA) policies through online reinforcement learning on real robots, but such training relies on costly physical interactions, suffers from low sample efficiency, and may introduce hardware and safety risks. World models offer a promising alternative by enabling policy optimization with imagined rollouts. However, long-horizon rollouts generated by world models often suffer from prediction hal- lucinations, producing biased state transitions that can mislead policy learning. To address this issue, we propose Hallucination-aware World Model-based Pol- icy Optimization (HaWMPO), a closed-loop reinforcement learning pipeline for VLA policy post-training with world models. Specifically, HaWMPO introduces an action-conditioned hallucination-aware model to estimate the reliability of gen- erated image sequences, and incorporates hallucination scores into group relative policy optimization through a Reward-Soft mechanism, suppressing unreliable ac- tion chunks during training. On the LIBERO benchmark, HaWMPO achieves the best average success rate, with gains of 15.0% over the base model and 2.8% over the strongest baseline; real-world experiments on a G1 robot further validate its effectiveness, raising the average success rate on two manipulation tasks from 67.5% to 80.0%.

---

## 9. Identifying Habit, Physics, and Nuisance in Robot World Models

**Authors:** Jinting Hang, Zhenhui Cai
**arXiv:** [2609.09210](https://arxiv.org/abs/2609.09210)
**Categories:** Robotics (cs.RO); Computer Vision and Pattern Recognition (cs.CV)

Teleoperated demonstrations are often multimodal even when the underlying dynamics are nearly deterministic given the executed action. We argue that this multimodality typically mixes three factors--operator habit in action selection, shared physics, and observation nuisance--and that entangled next-observation predictors absorb all three. We formalize the split with a structural causal model a=g(h,z,u), z'=f(z,a), o=r(z,c), and test it with complementary interventions: replacing or shuffling actions at fixed state sharply increases next-state error, whereas appearance and camera changes should not; habit-aware reverse scoring improves ranking of feasible pasts without rewriting the dynamics. The associated adaptation rule is to freeze a shared physics readout and update only a thin interface. On StackCube, DROID, and RH20T this rule improves low-shot transfer relative to training from scratch, retains cleaner dynamics under corrupted adaptation data, and extends from proprioception to pixel observations with multi-view and multi-step checks. We do not equate latent actions with operator habit, and we do not target large-scale video generation benchmarks.

---

## 10. Programmable World Model

**Authors:** Zheng-Hui Huang, Guixu Lin, Jiacheng Lin, ..., Kaipeng Zhang, Zhixiang Wang
**arXiv:** [2609.10540](https://arxiv.org/abs/2609.10540)
**Categories:** Computer Vision and Pattern Recognition (cs.CV)

Recent video world models generate increasingly realistic and interactive visual experiences, yet lack reliable mechanisms for maintaining persistent world state and enforcing programmable rules over extended interactions. We introduce Programmable World Model, a framework that decouples world-state evolution from visual observation generation. An agent translates natural-language instructions into executable programs that specify entity states and state-transition rules, enabling direct control over individual entities and their interactions. A lightweight engine executes these programs to update and maintain an explicit, persistent global world state, including off-screen entities and non-visual attributes. To connect world state with visual generation, we introduce state-augmented 3D oriented bounding boxes (OBBs) as an intermediate representation. This representation, together with the target camera trajectory, is deterministically compiled into pixel-aligned spatiotemporal conditioning signals for a pretrained video model serving as the generative renderer. This design allows users to create playable games with predefined mechanics, direct control over individual entities, and persistent world state throughout gameplay. We further introduce CombatStateBench, a benchmark for evaluating programmable world models. On CombatStateBench, our method achieves 94% Count Accuracy and 98% State Accuracy, substantially outperforming existing interactive video world models while supporting coherent long-horizon generation. These results demonstrate the effectiveness of separating explicit state evolution from generative rendering for building persistent, programmable worlds.

---

## 11. Arti-JEPA: Adapting Video World Model to Real-Time MRI of the Vocal Tract for Speech-Production Analysis

**Authors:** Hong Nguyen, Sean Foley, Christina Hagedorn, ..., Dani Byrd, Shrikanth Narayanan
**arXiv:** [2609.09757](https://arxiv.org/abs/2609.09757)
**Categories:** Sound (cs.SD); Computer Vision and Pattern Recognition (cs.CV)

Real-time MRI (rtMRI) captures the dynamics of the entire vocal tract during speech, but labeled data are scarce and the modality - single-slice, grayscale, low-resolution - differs substantially from the natural videos that video foundation models are trained on. We introduce Arti-JEPA, a joint embedding predictive architecture to model vocal tract rtMRI by continuing its self-supervised objective on about 62h of unlabelled vocal-tract videos, and evaluate the frozen representation on three tasks: cross-domain phoneme prediction (on typical speakers), fluent-vs-disfluent classification (a corpus containing stuttered speech), and characterizing pre/post-operative transfer (after partial glossectomy). Three key findings emerge. (1) A temporal video prior decisively outperforms per-frame image encoders, and latent prediction (V-JEPA) is at least as strong as pixel reconstruction (VideoMAE), with the edge on fine-grained phonemes. (2) Domain adaptation is \emph{task-dependent}: it roughly doubles cross-domain phoneme prediction $\kappa$ (to 0.352) but does not help binary stuttering classification. (3) Arti-JEPA was able to recover phoneme signal from pre/post glossectomy speech --- an in-domain probe decodes patients at least as well as a typical speaker, indicating that the residual transfer gap is cross-speaker/domain misalignment, not surgical signal loss, and post-operative decoding does not fall below performance on pre-operative speech. Together, these position a frozen, domain-adapted rtMRI encoder as a reusable measurement tool for articulatory and clinical speech science.

---
