# arXiv Daily Digest — 2026-09-04

**Mode:** direct
**Categories:** cs.AI, cs.LG, cs.RO, cs.CV
**Keywords:** VLA, world model, world action model
**Papers found:** 15

---

## 1. Semantic Bayesian World Models

**Authors:** Tommaso Soru
**arXiv:** [2609.03834](https://arxiv.org/abs/2609.03834)
**Categories:** Artificial Intelligence (cs.AI); Databases (cs.DB); Machine Learning (cs.LG)

Knowledge graphs describe reality in crisp assertions, while the systems now consuming them, foundation models and autonomous agents, reason natively in probabilities. We argue that this mismatch is why the integration of language models and knowledge graphs remains a data-feeding pipeline rather than a unified reasoning architecture. We envision Semantic Bayesian World Models (SBWMs): a Web that describes the world not as a database of facts but as a shared, evolving fabric of beliefs over knowledge graphs, where ontological axioms constrain priors, observations update beliefs by Bayesian conditioning, and actions intervene upon the world. We work through what an agent gains from such a model: a home-security agent deciding whether the figure at the gate is a courier or a burglar, an actuarial estimate aggregated by entailment rather than by string frequency, a planning task that language models reliably fail, and the estimation of quantities that no document has ever stated. We then set out what the community must build to make them possible: belief annotation over RDF~1.2, probabilistic entailment regimes, semantic calibration layers, and protocols by which agents that have never met can exchange, and disagree over, calibrated beliefs.

---

## 2. Rethinking World Models for Safety-Critical Embodied Systems

**Authors:** Kailang Ma, Heye Huang, Inhi Kim, Kitae Jang
**arXiv:** [2609.03774](https://arxiv.org/abs/2609.03774)
**Categories:** Artificial Intelligence (cs.AI); Robotics (cs.RO)

World models have progressed from compact latent dynamics to generative, controllable, and interactive simulators of embodied environments. However, high predictive likelihood and visual fidelity do not necessarily ensure that a model preserves the evidence required for safe decision-making. This perspective identifies three structural mismatches in current world modeling: likelihood versus risk, prediction versus intervention, and finite-horizon prediction versus accumulated consequences. We propose the Risk-Informed World Model (RIWM) as a decision-centric research direction for safety-critical embodied systems. RIWM organizes world modeling around consequences, intervention, epistemic uncertainty, and recoverability, and integrates four interdependent capabilities: decision-relevant representation, counterfactual reasoning, safety-critical episodic memory, and runtime safety assurance. It distinguishes physical, social, and operational consequences while using epistemic uncertainty to qualify the evidence supporting action. We further discuss open challenges in identifying consequential futures, validating counterfactual reasoning, maintaining revisable safety memories, translating learned consequences into executable constraints, and determining when evidence is sufficient to act. This perspective argues that future world models should move beyond predicting likely futures toward identifying which futures matter, revising judgments through experience, and recognizing when to act, revise, sense, defer, or abstain.

---

## 3. FWBC-VLA: Force-Aware Whole-Body Compensation for Contact-Rich Loco-Manipulation

**Authors:** Yutian Zhang, Siyuan Ma, Liwen Yang, ..., Qiaojun Yu, Dibo Hou
**arXiv:** [2609.03889](https://arxiv.org/abs/2609.03889)
**Categories:** Robotics (cs.RO); Artificial Intelligence (cs.AI)

Contact-rich loco-manipulation requires a bridge between semantic action generation and physical interaction control. Existing Vision-language-action (VLA) models generate task-level actions from visual and linguistic observations, but cannot interpret the physical interactions induced by those actions. While the whole-body control (WBC) policy can stabilize the robot, it cannot distinguish task-relevant interaction forces from forces induced by external disturbances during manipulation. Although force/torque sensors provide direct measurements of physical interactions, retrofitting them entails additional hardware costs and substantial integration effort, particularly for platforms not designed with sensor integration in mind. To address this problem, we propose FWBC-VLA, a force-aware framework that bridges task-level VLA action generation and low-level whole-body compensation control for wheeled-legged robots. First, we introduce HSR-Force, a sensorless residual-torque estimator for inferring contact strength and its temporal variation. These contact estimates are then encoded as tokens and injected into the VLA action expert during action decoding, enabling the policy to perceive contact onset, sustained loading, and release. For loco-manipulation tasks, all parameters of the pretrained VLA backbone are fine-tuned on our WL\&Arm Dataset, which comprises more than 5,000 episodes. Moreover, the robot's proprioceptive state, the Jacobian-derived body-frame force estimate, and the estimated contact state are jointly fed into a compensation generator to produce corrective actions. The manipulation-centric actions are subsequently combined with the corrective actions and passed to the WBC policy for execution. Real-world experiments on whiteboard wiping and door opening with a door closer demonstrate the effectiveness of our FWBC-VLA in contact-rich loco-manipulation.

---

## 4. Toward Physically Grounded JEPA World Models for Goal-Conditioned Robotic Planning

**Authors:** Muyuan Liu, Yue Huang, Zheng Liang, Xiang Gao
**arXiv:** [2609.03565](https://arxiv.org/abs/2609.03565)
**Categories:** Robotics (cs.RO); Artificial Intelligence (cs.AI); Machine Learning (cs.LG)

Action-conditioned JEPA world models enable planning toward visually specified goals without reconstructing future pixels, yet latent prediction alone does not explicitly encourage the learned representations to retain information relevant to robotic control. We introduce an end-to-end JEPA world model that augments latent prediction with inverse dynamics (IDM) and state alignment (SA). While inverse dynamics discourages latent collapse and makes latent transitions informative of the actions that produced them, state alignment grounds consecutive representations in their associated physical configuration and motion. Across four benchmark tasks, our model attains the highest success rates on TwoRoom (100%), PushT (98%), and OGBench-Cube (87%), while performing comparably to LeWorldModel on Reacher. Our ablation further shows that adding state alignment consistently improves planning success over IDM alone across all four tasks. Although LeWorldModel, our primary baseline, attains higher average straightening on OGBench-Cube, transition-subspace analysis shows that its transition energy is concentrated in a substantially lower-dimensional subspace. Our state-aligned model exhibits a higher effective transition dimension than LeWorldModel and improves planning over IDM alone, supporting state alignment as an effective complement to inverse dynamics for robotic planning.

---

## 5. Latent Energy Action Planning with World Models

**Authors:** Phu Pham, Aniket Bera
**arXiv:** [2609.03294](https://arxiv.org/abs/2609.03294)
**Categories:** Machine Learning (cs.LG)

Latent world models support efficient model predictive control from high-dimensional observations, yet optimizing a single learned latent objective can favor action sequences whose decoder-predicted terminal descriptor does not match the goal descriptor. We introduce Latent Energy Action Planning (LEAP), which treats the complete action horizon as a differentiable variable and optimizes it through a frozen LeWorldModel (LeWM). LEAP couples terminal latent goal matching with a terminal-window state energy. Low energy requires the predicted terminal latent to agree with the goal latent and the decoder-predicted terminal descriptor to agree with the goal descriptor. A frozen goal-conditioned proposal initializes the search, a quasi-Newton solver refines actions through the autoregressive rollout, and post-optimization projection enforces the admissible action range. Across four control domains using the officially released LeWM checkpoints, the complete LEAP planning system raises mean success from 77.5% for LeWM planned with the cross-entropy method (LeWM+CEM) to 94.8% under a matched protocol, a 17.3-percentage-point improvement, while retaining the frozen LeWM representation and predictor.

---

## 6. Sensing Which Modality Matters: Evidence-Gated Regularization for Robust VLA Policies

**Authors:** Yue Yang, Diego Romeres, Chiori Hori, ..., Daniel Szafir, Siddarth Jain
**arXiv:** [2609.03142](https://arxiv.org/abs/2609.03142)
**Categories:** Robotics (cs.RO); Computer Vision and Pattern Recognition (cs.CV); Machine Learning (cs.LG)

Vision-Language-Action (VLA) policies fuse multimodal sensory inputs, but training on limited and homogeneous robot demonstrations encourages spurious inter-sensor correlations rather than task-relevant signal, a failure we term modality entanglement. Under real-world occlusions and distractors, this manifests as nuisance sensitivity to corruption of uninformative sensors and single-modality insufficiency when only one informative sensor remains intact. We propose Evidence-Gated Regularization (EGR), a modality-agnostic training objective that introduces zero inference-time overhead. EGR derives a per-frame and per-sensor task-relevance signal to gate two state-conditional consistency objectives: invariance on low-evidence sensors, and single-sensor sufficiency on high-evidence ones. We introduce a benchmark based on BEHAVIOR-1K, comprising a fast inference-only diagnostic suite and 47 rollout-based skills targeting modality entanglement. We validate EGR on this benchmark and on two real-robot setups with fundamentally different embodiments: a bi-manual setup with two Kinova arms and three RGB cameras, and a single-arm MELFA ASSISTA setup combining vision and GelSight tactile sensors. EGR improves simulation success rates (SR) from 12.5% to 16.4% under full modalities (+31%), from 9.4% to 16.5% under uninformative-sensor corruption (+75%), and from 2.8% to 6.1% under single-sensor fallback (+120%). Under physical-object distractors, EGR boosts SR from 30% to 85% on the bi-manual setup (+183%) and from 55% to 70% on the tactile setup (+27%).

---

## 7. Toward Unified Robot Learning: Bridging Representation, Vision-Language-Action, and World Models

**Authors:** Shaunak A. Mehta, Ananya Hazarika, Haochen Zhang, ..., Yash Patel, Kanata Suzuki
**arXiv:** [2609.03927](https://arxiv.org/abs/2609.03927)
**Categories:** Robotics (cs.RO)

For robots to operate reliably in real-world environments, they need to perceive their surroundings, act, and reason about the consequences of those actions. Rapid progress in the domains of representation learning, VLA models, and world models has significantly enhanced the capabilities of robot learning systems, enabling robots to work in increasingly complex environments. However, these paradigms are typically developed in isolation, resulting in fragmented systems that struggle with generalization, long-horizon temporal reasoning and planning, and deployment in unstructured environments. In this survey, we present a unified perspective on robot learning by organizing the existing methods along three complementary axes: understanding through representation learning, acting through VLA models, and reasoning through world models. We introduce a structured taxonomy that captures key design choices in environment representation, policy learning, and predictive modeling, and summarize the recent progress in these domains. Beyond classifying the existing works, we analyze how these components interact, discuss common limitations, and highlight emerging trends towards more integrated systems. Through this lens, we identify the challenges in the domain of robot learning, including uncertainty quantification, out-of-distribution generalization, cross-embodiment transfer, long-context understanding, and long-horizon planning. We argue that these challenges arise not only from limitations within individual components but also from the lack of integration across perception, action, and reasoning. Building on this analysis, we outline future directions towards unified, physically grounded, and probabilistic robot learning to develop robust robotic systems that maintain consistent internal representations and support decision making over extended interactions in real-world environments.

---

## 8. WISE: World-model-guided Imagination Scheduling for Efficient Post-training of Vision-Language-Action Models

**Authors:** Chenhao Zhang, Hanyu Zhao, Hang Cheng, Tengfei Pan, Long Zeng
**arXiv:** [2609.03681](https://arxiv.org/abs/2609.03681)
**Categories:** Robotics (cs.RO)

Post-training VLA policies typically rely on supervised fine-tuning with costly expert demonstrations or reinforcement learning with expensive and potentially unstable real-world exploration. World models offer a promising alternative by evaluating candidate behaviors through imagined futures, yet effective post-training requires more than accurate prediction: imagination must be scheduled where it is useful, bounded within reliable horizons, and translated into trustworthy policy supervision. In robotic manipulation, the value of imagination varies substantially across execution stages, while extended rollouts can accumulate prediction errors and introduce unreliable learning signals. We introduce WISE (World-model-guided Imagination Scheduling for Efficient Post-training of Vision-Language-Action Models), a unified framework that coordinates when and how world-model imagination is used during policy refinement. WISE selectively invokes imagination at interaction-relevant states, performs bounded multi-view rollouts, evaluates candidate futures using progress and completion signals, and uses their relative outcomes to refine actions generated from real interaction contexts. Extensive experiments with both $\pi_0$ and $\pi_{0.5}$ demonstrate consistent improvements across diverse manipulation tasks while reducing GPU computation time by approximately 80% compared with full imagination. Real-world evaluations further show substantial gains in robustness and generalization under diverse real-world distribution shifts.

---

## 9. Long-Horizon Consistent and Interaction-Aware World Models for Multi-Style End-to-End Driving

**Authors:** Yuxuan Han, Kunyuan Wu, Liyunong Yang, ..., Yi Xiao, Liang Hu
**arXiv:** [2609.03225](https://arxiv.org/abs/2609.03225)
**Categories:** Robotics (cs.RO)

End-to-end autonomous driving has increasingly adopted world model-based reinforcement learning frameworks to improve learning efficiency through \textit{imagined rollouts}. However, existing world models suffer from three key limitations: temporal inconsistency in long-horizon imagined rollouts, inadequate modeling of ego-environment interactions, and limited adaptability to diverse driving styles. To address these challenges, we propose \textit{StyleDrive}, a world-model-based learning framework that jointly enforces long-horizon consistency, explicitly disentangles interactive traffic states, and supports multi-style policy optimization within a unified learning paradigm. First, we introduce a temporal consistency regularization that integrates historical latent states through gated cross-attention, stabilizing long-horizon imagined rollouts and mitigating error accumulation. Second, we design an explicit state disentanglement module that separates ego-relevant from ego-irrelevant interactive states, enabling more interpretable and efficient decision-making in complex traffic scenarios. Third, we enable multi-style driving behaviors through Group Relative Policy Optimization, which replaces per-step reward optimization with trajectory-wise relative advantages, reducing reward variance and supporting diverse driving styles without retraining. We evaluate StyleDrive on the Bench2Drive closed-loop driving benchmark, achieving a driving score of 88.44 (+17.08 over the previous best world model-based method) and a success rate of 66.82 (+16.58). Furthermore, we deploy StyleDrive on a real automated guided vehicle platform and demonstrate promising sim-to-real transfer capability in dynamic driving scenarios.

---

## 10. GPU-Accelerated Astrodynamics World Models for Spacecraft Rendezvous and Proximity Operations

**Authors:** Duncan Eddy, Isaac R. Ward, Grace Ra Kim, Mykel J. Kochenderfer
**arXiv:** [2609.03067](https://arxiv.org/abs/2609.03067)
**Categories:** Robotics (cs.RO); Systems and Control (eess.SY)

World models are an emerging paradigm in representation learning in which an agent jointly learns state-action dynamics and observation models from offline trajectory data, enabling multi-step planning and trajectory prediction with uncertainty estimates. They have shown strong results in robotics and game environments, but, to the best of our knowledge, have not previously been applied to the space domain. This paper introduces a world model-based approach to cooperative and non-cooperative spacecraft rendezvous and proximity operations. First, we introduce an open-source, JAX-based International Space Station (ISS) docking environment supporting parallel GPU simulation of spacecraft orbit and attitude dynamics, generating the thousands of state-action transitions that world model training requires. Second, we introduce Out-of-this-World-Model, a transformer-based world model that encodes relative kinematic states and body-fixed camera imagery into a latent state and predicts its evolution under commanded thrusts and torques using one-step flow matching. It produces a distribution over future observations, capturing stochastic dynamics and per-timestep uncertainty, and outperforms DreamerV3-style posterior-correction baselines with fewer trainable parameters and hyperparameters. Third, we apply the approach to a capsule autonomously docking with the ISS under keep-out-zone constraints, demonstrating improved sample efficiency and task performance over reinforcement learning baselines (53% versus 29% docking success across ports), better out-of-distribution generalization (on held-out ports the world model more than doubles baseline success, 40% versus 17%), and detection of anomalous objects encountered during approach with 98% classification accuracy. We open-source the simulation environment and model architecture to enable further study of this paradigm.

---

## 11. SV-WAM: An Efficient Surround-View World-Action Model for End-to-End Autonomous Driving

**Authors:** Jinyang Wang, Shiwei Li, Junjian Wang, ..., Ji Tao, Minghao Yang
**arXiv:** [2609.03602](https://arxiv.org/abs/2609.03602)
**Categories:** Computer Vision and Pattern Recognition (cs.CV); Robotics (cs.RO)

World models (WMs) have demonstrated strong potential for end-to-end autonomous driving by learning predictive representations of future scene dynamics. However, generating future videos during inference introduces substantial computational overhead, leading many recent driving WMs to adopt a single front camera as input for efficient deployment. This design restricts spatial coverage in safety-critical maneuvers such as lane changes, merges, and turns. To address this limitation, we propose SV-WAM, a surround-view world-action model (WAM) that preserves full six-camera observations while maintaining efficient inference. SV-WAM leverages future-video prediction as dense training supervision for action learning within a shared generative model, rather than as an inference-time output. At the core of this design is an action-centered causal mask that prevents action tokens from attending to future-video tokens during joint action-video denoising. Consequently, the video branch can be discarded at deployment, enabling efficient action-only planning. Furthermore, we introduce a differentiable drivable-area compliance regularizer that penalizes vehicle-footprint corners approaching or crossing drivable boundaries, improving planning safety and boundary awareness. Extensive experiments on the closed-loop NAVSIMv2 benchmark and the open-loop nuScenes benchmark demonstrate that SV-WAM achieves state-of-the-art planning performance with low inference latency and competitive zero-shot transfer capability.

---

## 12. WorldReward: Reward Modeling for Camera-Conditioned World Models

**Authors:** Yibin Wang, Zehan Wang, Junshu Tang, ..., Jiaqi Wang, Tianyu Pang
**arXiv:** [2609.03952](https://arxiv.org/abs/2609.03952)
**Categories:** Computer Vision and Pattern Recognition (cs.CV)

Camera-conditioned world models generate interactive videos in which commanded actions should induce the expected scene changes while appearance, geometry, and temporal dynamics remain coherent. Existing rewards assess these requirements separately: geometry-based rewards estimate trajectory execution but cannot judge the visual quality of the executed motion, whereas image-based rewards measure frame quality without capturing action execution or temporal dynamics. We posit that a vision-language model (VLM) offers a shared reasoning space for relating actions to their visual outcomes. However, judging a complete long video against its full action sequence creates a lengthy, noisy context in which short-lived local action evidence can be missed or diluted. We present WorldReward, a VLM-based pairwise preference reward model that unifies action-consistency and visual-quality evaluation for camera-conditioned world models. WorldReward decomposes paired videos into action-aligned chunks, organizes each chunk into structured visual evidence, and aggregates chunk-level decisions by voting into separate video-level action and visual-quality preferences. To train it, we construct a large-scale reasoning-augmented preference dataset using structured judgments generated by a frontier VLM and refined through tool-based agent auditing and targeted human review. We further introduce WorldReward-Bench, a human-annotated benchmark measuring reward-model agreement with human preferences across action consistency, appearance quality, and motion quality. WorldReward achieves the highest agreement on all three dimensions, exceeding GPT-5.5 by 3.42, 1.45, and 3.56 percentage points, respectively. When used for RL post-training of HY-WorldPlay 1.5, it consistently improves both action execution and visual quality across short- to long-term horizons.

---

## 13. Drive-HWM: Hierarchical World Models for Dynamic-Latent Guided Autonomous Driving

**Authors:** Zhaoxin Fan, Tianbao Zhang, Wenjun Wu, ..., Zheng Zhu, Shuicheng Yan
**arXiv:** [2609.03572](https://arxiv.org/abs/2609.03572)
**Categories:** Computer Vision and Pattern Recognition (cs.CV)

World models offer a promising paradigm for autonomous driving by predicting how traffic scenes may evolve and using such predictions to support action generation. However, existing approaches either separate future prediction from action generation or jointly predict them at the same temporal scale, making it difficult to simultaneously achieve long-horizon anticipation and responsive, observation-grounded decision making. We present Drive-HWM, a hierarchical slow--fast world modeling framework that organizes future representation prediction and action generation at complementary temporal scales. The slow world model predicts multi-step future representations to capture extended scene evolution. To explicitly model the abundant motion dynamics in driving environments, we introduce Dynamic-Aware Latents learned through optical-flow prediction. Guided by these future representations, the fast model uses a lightweight multimodal backbone and an autoregressive expert to jointly predict the next frame and the immediate action from the latest observation. Next-frame prediction encourages the fast model to capture imminent scene evolution, while one-step action generation allows decisions to be continuously updated as new observations arrive. Extensive experiments on NAVSIM v1 and v2 demonstrate the strong driving performance of Drive-HWM. Comprehensive ablation studies further validate the effectiveness of the hierarchical slow--fast design, dynamics-aware future representations, and joint next-frame and action prediction.

---

## 14. Building Pretraining Data for World Models: An Unreal Engine-Based Pipeline for Action-Conditioned Video Generation

**Authors:** Haoyu Wang, Songchun Zhang, Haoran Li, ..., Zeyue Xue, Nan Duan
**arXiv:** [2609.03557](https://arxiv.org/abs/2609.03557)
**Categories:** Computer Vision and Pattern Recognition (cs.CV); Graphics (cs.GR)

Action-conditioned video models require large-scale visual data paired with control signals that are temporally aligned with the resulting scene transitions. Such supervision is difficult to obtain from ordinary real-world video because the actions that caused each visual change are typically unknown. We present a large-scale synthetic data production pipeline built on Unreal Engine for generating action-conditioned, multi-view video. To accommodate the different execution requirements of real-time physics and high-quality offline rendering, the pipeline executes trajectory generation and final rendering in two stages: Stage I runs real physics in PIE and records per-frame character states, control inputs, and camera states into an intermediate trajectory representation; Stage II replays those trajectories in a new engine process and renders them offline with Movie Render Queue (MRQ). Around this core, we develop a distributed production system with cache-aware task partitioning, node-local slot scheduling, automated scene screening, aesthetic and luminance filtering, partial-output recovery, asynchronous upload, and continuous cluster health monitoring. The production cluster contains 25 servers with eight NVIDIA RTX 5090 GPUs per server. From 2,384 asset packs, 429 levels were retained for production together with a pool of 40 humanoid characters. The pipeline has produced 2,691 hours of 1080p video and 6,076 hours of 720p video. We describe the system architecture, the implementation decisions that emerged from production failures, and the limitations of using perceptual quality proxies for world-model data curation. The pipeline described in this report constitutes the Unreal Engine synthetic-data production component used in EchoWM.

---

## 15. VeriPhy: Agentic Physical Reasoning for World Model Evaluation and Refinement

**Authors:** Wenzhuo Xu, Yuchen Zhu, Chongjian Ge, ..., Noelia Grande Gutiérrez, Jiuxiang Gu
**arXiv:** [2609.03153](https://arxiv.org/abs/2609.03153)
**Categories:** Computer Vision and Pattern Recognition (cs.CV)

Visual fluency in generated video does not imply physical reliability, and a scalar quality score alone is incapable of indicating the obligation a clip violates or the moment it fails. We present VeriPhy, an auditable physical-verification system in which a text-only planner compiles the prompt into typed physical obligations and a statically validated execution plan before any frame is observed. During execution, observations gate and scope only declared calls to frozen low-level experts (e.g., segmentation and tracking, counting, eleven typed physical measurements over the resulting tracks, depth, OCR, and audio-event detection). Each action returns a provenance-carrying evidence record whose payload, when usable, is either a typed measurement or an explicitly tagged learned state. Typed resolvers and fixed composition map usable records to a three-valued state (supported, contradicted, or unknown, surfaced as plausible, implausible, or abstain) with full provenance, so that every verdict is traceable to the evidence that produced it. We anchor evaluation in a 1,500-clip corpus of human-annotated flaw records that localize real generation failures in prompt reference, space, and time. On a 149-clip core carrying 304 such records, VeriPhy accounts for 228, against 164 for a published question-decomposition evaluator given the same clips and the same claims. Recall alone does not separate it from prompting the same backbone monolithically, which reaches 222; what separates them is that each decision retains its evidence record and provenance, making the traces auditable one verdict at a time and usable as the interface through which a critic verdict could be written back into generation.

---
