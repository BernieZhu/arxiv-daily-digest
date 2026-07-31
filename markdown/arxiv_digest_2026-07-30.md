# arXiv Daily Digest — 2026-07-30

**Mode:** direct
**Categories:** cs.AI, cs.LG, cs.RO, cs.CV
**Keywords:** VLA, world model, world action model
**Papers found:** 12

---

## 1. CG-World: A Large-Scale World-State Dataset and Protocol for World Models

**Authors:** Yiming Cai, Fangjie Yu, Meiqing Yu, ..., Pengfei Yuan, Yong Guo
**arXiv:** [2607.26452](https://arxiv.org/abs/2607.26452)
**Categories:** Artificial Intelligence (cs.AI); Computer Vision and Pattern Recognition (cs.CV); Graphics (cs.GR)

World models must learn the joint dynamics of states, actions, events, and observations, yet existing video, robotics, and simulation datasets usually capture only part of this structure. We introduce CG-World, a large-scale world-state dataset and protocol derived from industrial computer graphics production pipelines. CG-World explicitly records intermediate states, including multimodal semantics, spatial structure, skeletal and controller states, motion curves, camera and lighting parameters, physics caches, contact events, and multi-pass renderings. CG-World v1 contains approximately 850,000 temporally aligned segments of 1-5 seconds. It separates latent states, observations, relations, events, and branch metadata, and organizes them into unified spatiotemporal samples. To support intervention learning and counterfactual reasoning, CG-World defines a branch lineage covering factual trajectories, observation interventions, action interventions, mechanism interventions, and strict counterfactual branches, with intervention targets, invariants, and alternative outcomes explicitly recorded. We evaluate the dataset on geometry-conditioned video generation, action prediction, and closed-loop vision-language-action policy transfer. Results show that CG-World provides reusable structured supervision for controlled generation, action modeling, and embodied policy transfer. We plan to expand CG-World through continued data collection and community collaboration toward a shared data infrastructure for world models, Physical AI, and embodied intelligence.

---

## 2. What Can Latent World Models Know? Physical Parameter Identifiability in Multimodal Predictive Representations

**Authors:** Kaizhen Tan, Xin Xu, Siru Tao, ..., Yang Feng, Heqing Du
**arXiv:** [2607.27017](https://arxiv.org/abs/2607.27017)
**Categories:** Machine Learning (cs.LG); Robotics (cs.RO)

A central premise of latent world models is that predicting the future forces a representation to internalize the physics of its environment. Which physical quantities does a trained latent actually contain, and what decides this? We answer with controlled interventions in POKEWORLD, an interactive environment whose visually identical objects hide mass, drag, and contact stiffness. A certificate-gated protocol first certifies each parameter as recoverable from raw observations, then measures whether it enters the latent, so a null result can be attributed to the objective rather than to the environment. The resulting identifiability map has two organizing mechanisms and one frontier. Inputs limit what can be known, while prediction targets decide what is retained. Stiffness enters the latent only when touch is forecast ($R^2=0.50$, compared with $-0.02$ when the same signal is merely fused into the input), and under single-step prediction a vision-only latent discards even perfectly visible object state. Drag marks the frontier. It carries a recoverability certificate of 0.89 yet plateaus near 0.13 under every deterministic prediction objective we test, while a supervised head on the same trunk reaches 0.45. Parameters whose readout is slow and ratio-type under the sensed coordinates fall outside what these objectives acquire. On RH20T, an input-target factorial across scaling curves reproduces both mechanisms across two robots and 4,258 episodes. Every arm missing information or prediction pressure stays flat over a fivefold data range, and only the full multimodal objective forecasts force beyond a persistence baseline, with held-out gains that grow with scale. Objective structure determines which physical parameters a latent acquires, and additional data improves only the parameters it already acquires.

---

## 3. Temporally Centered SIGReg Improves Multi-Task LeWorldModel Learning: From Analysis to Method

**Authors:** Chang Liu, Fei Suo, Yanzhou Jin, ..., Yutaka Matsuo, Yaonan Zhu
**arXiv:** [2607.26924](https://arxiv.org/abs/2607.26924)
**Categories:** Machine Learning (cs.LG); Robotics (cs.RO)

Recent work on LeWorldModel (LeWM) has shown that the Sketched Isotropic Gaussian Regularizer (SIGReg) enables stable end-to-end world-model learning from pixels by regularizing the latent marginal distribution toward an isotropic Gaussian, thereby preventing representation collapse. While effective and elegant in single-task settings, this recipe does not extend reliably to multi-task training, leading to substantially worse downstream behavior-cloning performance. In this paper, we show that marginal Gaussianization compresses the separation between task-dependent latent clusters relative to within-cluster variation. This compression introduces representation aliasing across tasks and states, and makes the learned representations highly sensitive to small visual perturbations. To address this problem, we apply SIGReg to temporally centered residuals rather than to the latent marginal distribution. This surrogate target places no direct regularization pressure on the separation among cluster centers, removes the requirement that the full latent follow a single isotropic Gaussian, and retains the anti-collapse effect of SIGReg. On the LIBERO benchmark, our method improves downstream success on the long-horizon suite by 1.7x and raises the average success rate across four suites from 53.2% to 73.6%. Without external pretraining, it slightly outperforms Diffusion Policy trained from scratch and approaches the performance of large-scale pretrained policy baselines. These results reveal a structural incompatibility between marginal Gaussian priors and multi-task latent structure, and provide a simple route toward stable and scalable end-to-end multi-task world-model learning.

---

## 4. CalTwin: Towards Calibrated, Shift-Robust Medical World Models via Fisher-Information Regularisation

**Authors:** Behraj Khan, Shabir Ahmad, Syed Ahmad Chan Bukhari, Tahir Qasim Syed
**arXiv:** [2607.26752](https://arxiv.org/abs/2607.26752)
**Categories:** Machine Learning (cs.LG)

Medical world models aim to learn a latent state of patient or organ physiology and a transition function that forecasts how that state evolves under interventions, supporting downstream tasks from imaging-based diagnosis to digital-twin treatment planning. Two failure modes threaten the reliability of such models in clinical deployment: (i)~\emph{covariate shift}, because training data are fragmented across hospitals, scanners, and time, so the feature distribution seen by the latent-dynamics predictor differs across fragments and from the distribution at deployment; and (ii)~\emph{confidence misalignment}, because multi-step forecasts are often overconfident exactly where clinical risk is highest. We argue that both problems admit a unified treatment via a single lightweight regularisation objective, \textbf{CalTwin}, which combines a Fisher-Information-based shift penalty adapted from our prior work on fragmented covariate-shift remediation~\cite{khan2025mitigating,khan2025causal} with a Confidence Misalignment Penalty adapted from our prior work on calibrated vision-language classification~\cite{khan2025confidence}, applied here to a GRU-based medical world model's latent transition predictor. We derive the combined objective, establish which proof steps transfer from the classification setting without modification and which require adaptation, and evaluate it on the PhysioNet 2019 Sepsis Challenge, treating the two hospital systems as sequential training fragments and the unseen system as an out-of-distribution test. CalTwin reduces OOD next-step latent-state MSE by 9.1\% relative to the no-penalty baseline (FIM penalty alone accounts for 7.0\%); the ECE reduction from the Confidence Misalignment Penalty is real but small (0.7\% for CalTwin, 1.3\% for CMP alone).

---

## 5. Learning Implicit Causal World Models from Multi-Agent Demonstrations

**Authors:** Jasorsi Ghosh
**arXiv:** [2607.26336](https://arxiv.org/abs/2607.26336)
**Categories:** Machine Learning (cs.LG); Multiagent Systems (cs.MA); Robotics (cs.RO)

In model-based reinforcement learning, world models exist as internal simulators, but their training often conflates statistical correlations with causal mechanisms. This problem is exacerbated in multi-agent systems where physical transitions are intertwined with strategic agent intents, causing world models to fail under distribution shift. We introduce Implicit Causal World Models to recover environmental dynamics from offline demonstrations without requiring pre-defined causal graphs. By incorporating policy variance, we render world models discoverable via the sequential backdoor condition. Evaluations across coordination tasks (Two-Door, Navigation, and Giveway) demonstrate that these models provide interpretable causal representations under both full and partial observability, with model accuracy scaling directly with interventional strength.

---

## 6. RL$^2$-VLA: Adaptive RL Latent Compositional Steering with Test-Time Scaling for Vision-Language-Action Models

**Authors:** Derek Ming Siang Tan, Shailesh Shailesh, Srikrishna Iyer, ..., Qiao Gu, Guillaume Sartoretti
**arXiv:** [2607.26991](https://arxiv.org/abs/2607.26991)
**Categories:** Robotics (cs.RO)

Despite the impressive visuomotor capabilities enabled by Vision-Language-Action (VLA) models, their performance often degrades on challenging and out-of-domain tasks. Recent test-time steering and scaling methods improve performance without extensive data collection and retraining, but action samples often remain concentrated around similar behaviors and therefore inherit correlated failure modes. Moreover, existing methods apply the same intervention strategy at every timestep, regardless of whether the base policy is already likely to succeed. To address these limitations, we introduce $RL^2$, an adaptive inference-time steering framework that leverages Reinforcement Learning on VLA Latents. First, we train a lightweight offline RL policy conditioned on expressive latents extracted from the VLA action expert and compose its flow velocity with that of the frozen VLA during inference. This compositional steering strategy combines the behavioral priors of large-scale imitation learning with the action diversity induced by offline RL beyond dominant demonstration modes. We further discover that inference-time steering follows fundamentally different scaling laws under success and failure states, revealing that action diversity is most beneficial when the base VLA is likely to fail, but can unnecessarily perturb already-accurate actions when success is likely. Building on this insight, $RL^2$ activates compositional steering only when failure is predicted. Across the SIMPLER and PolaRiS benchmarks, $RL^2$ improves success rates by up to +17.3% in out-of-domain settings, while ablations and scaling studies demonstrate the importance of latent representations and RL training. Finally, real-world experiments demonstrate that these gains transfer beyond simulation, establishing $RL^2$ as a practical and modular steering framework for VLA deployment.

---

## 7. Route by Kinematics, Act by Observation: Kinematics-Supervised Expert Routing in MoE-Augmented VLA

**Authors:** Tianhang Yang, Yanze Zheng, Junjie Wang, ..., Ruotong Li, Yujiu Yang
**arXiv:** [2607.26807](https://arxiv.org/abs/2607.26807)
**Categories:** Robotics (cs.RO)

While MoE augments VLA via expert specialization, router suffers from ineffective expert routing owing to the kinematic heterogeneity of actions across manipulation tasks and, even worse, the unavailability of the kinematic signals at inference time. In this work, we first observe that most semantically distinct manipulation tasks reduce to multiple kinematic archetypes. Motivated by this finding, we propose Kinematics-supervised explicit routing (KinRT), a new paradigm that shifts from implicit, observation-driven expert routing to explicit, kinematics-guided expert dispatching. Specifically, we perform kinematic clustering on action trajectories into multiple kinematically coherent groups, whose IDs serve as ground truth to supervise the training of the router; at inference time, the router dispatches experts only using visual-language observations, without any reliance on action kinematics. KinRT actually introduces an asymmetric bridging mechanism that distills the task kinematics from the action space in training into the observation space at inference. In addition, to assess KinRT's cross-platform generalization, we build an economical, Do-It-Yourself robot (DIYRobot) platform from scratch using 3D-print technology ($<$ 2,000USD). Extensive experiments demonstrate KinRT's superiority over both dense and MoE-featured VLAs by more than 23.26% on RoboTwin benchmark and 20.27% on our introduced DIYRobot platform. Our code and DIYRobot platform will be open-sourced.

---

## 8. CheckVLA: Execution-Time Verification with Action-Conditioned World Model for Long-Horizon Mobile Manipulation

**Authors:** Yushan Liu, Peibo Sun, Xintao Chao, ..., Xiao-Ping Zhang, Wenbo Ding
**arXiv:** [2607.26789](https://arxiv.org/abs/2607.26789)
**Categories:** Robotics (cs.RO)

Vision-language-action (VLA) policies commonly execute long-horizon mobile manipulation through open-loop action chunks, issuing multiple actions without receiving new high-level visual input. A committed chunk therefore implies how observations should evolve, but accidental deviations can violate this expectation while the remaining actions continue to propagate the error: commit-time policy confidence cannot react to a deviation that occurs after dispatch, and observation-only anomaly scores lack an action-conditioned reference for separating expected effects from unexplained changes. We propose CheckVLA, which verifies execution with a separately trained, frozen action-conditioned world model. A conformally calibrated risk threshold bounds the episode-level probability of an unnecessary first intervention and determines when to intervene, its exceedance controls how strongly the rewritten suffix retains the superseded chunk, latency-aware hard prefixing restricts replacement to actions that remain deployable, and an event-driven keyframe bank preserves evidence of prior progress across repairs. On RoboCasa365, under a common training recipe and a matched invocation budget, CheckVLA attains a 36.1% average success rate against 27.6% for periodic replanning (+8.5 points). At a matched 5% episode-level false-alarm target, action conditioning raises timely recall to 77.9%, against 48.6% for an observation-only control and 37.9% for an action-shuffled control. These simulation results support action-conditioned verification as a way to restore feedback during chunked execution while keeping the repair consistent with inference latency.

---

## 9. ActSWM: Action-Sensitive World Models for Long-Horizon Planning in Open-World Games

**Authors:** Zhenfeng Gan, ZiTong Zeng, Jiajun Cheng, ..., Yongyi Tang, Xueqian Wang
**arXiv:** [2607.26712](https://arxiv.org/abs/2607.26712)
**Categories:** Robotics (cs.RO)

Latent world models support efficient model-predictive control by optimizing future control sequences in latent space and replanning in a receding-horizon manner. However, existing latent predictors often lack stable long-horizon rollout ability, and prediction accuracy alone does not ensure that rollouts remain responsive to the actions being planned. We identify Context Collapse, a failure mode in which autoregressive latent predictors maintain high similarity to future states while producing nearly indistinguishable futures under different action sequences. To address this issue, we propose ActSWM, an action-sensitive latent world model grounded in a transition-separation principle: a planning-useful latent dynamics model should keep alternative-action futures distinguishable and make the action associated with each local transition recoverable. Under this principle, action sensitivity is enforced as a constraint on latent rollouts rather than treated only as an auxiliary prediction target, encouraging predicted futures to preserve action-dependent differences over long horizons. Across step-drift analysis, closed-loop Minecraft planning, and cross-game local action recovery, ActSWM preserves larger action-dependent rollout gaps than existing baselines, improves task success in long-horizon interactive settings, and enables world-model-based action recovery from offline gameplay videos.

---

## 10. Explicit Kinematic Guidance from Analytic Concepts for Vision-Language-Action Models

**Authors:** Mingyang Sun, Jiude Wei, Xiujian Liang, ..., Cewu Lu, Jianhua Sun
**arXiv:** [2607.26513](https://arxiv.org/abs/2607.26513)
**Categories:** Robotics (cs.RO)

Current Vision-Language-Action (VLA) models rely mainly on 2D inputs, neglecting the rich object structural information and commonsense knowledge inherent in the 3D physical world. This deficiency restricts their spatial awareness and adaptability for complex, high-precision manipulation. To bridge this crucial gap, we construct a Concept Expert module for VLA to build executable Analytic Concepts that represent objects as explicit, programmatic blueprints. Our mechanism operates in two synergistic phases: First, prior to VLA inference, the Concept Expert leverages 3D information from Vision Foundation Models (VFMs) to estimate the initial kinematic and structural parameters. Second, throughout the manipulation process, the VLA model utilizes its inherent capability to dynamically track the dynamic concept parameters, continuously aligning them with observational changes to ensure persistent accuracy. Once established, the Analytic Concepts provide explicit, high-quality guidance for VLA fine-tuning through (1) dense, programmatic manipulation rewards and (2) precise spatial guidance.
This formulation allows VLA models to learn physically grounded interaction behaviors while maintaining end-to-end learning flexibility.
Our experimental results show consistent improvements in success rate and learning efficiency across supervised and reinforcement learning settings, demonstrating the effectiveness of structured, concept-based guidance for VLA post-training.

---

## 11. TurboVLA: Real-Time Vision-Language-Action Model at 32 Hz on an RTX 4090 with <1 GB VRAM

**Authors:** Hengyi Xie, Chenfei Yao, Xianjin Wu, ..., Xiang Bai, Han Ding
**arXiv:** [2607.27205](https://arxiv.org/abs/2607.27205)
**Categories:** Computer Vision and Pattern Recognition (cs.CV); Robotics (cs.RO)

Vision-language-action (VLA) models commonly adopt an LLM-centric $V \to L \to A$ pathway, where visual observations are projected into the representation space of a large language model before being decoded into robot actions. Although effective, this design incurs substantial computation and memory overhead at every policy invocation. In this work, we introduce TurboVLA, a new VLA paradigm that reformulates the conventional $V \to L \to A$ pathway as a direct $V + L \to A$ mapping. Instead of using a large language model as the central interface between perception and action, TurboVLA independently encodes visual observations and language instructions, directly exchanges information between them through lightweight bidirectional vision-language interaction, and predicts continuous action chunks with a compact decoder. This simple design constructs task-conditioned representations directly from visual and linguistic features, significantly reducing the computational and memory costs of VLA inference. On LIBERO, TurboVLA achieves 97.7% average success with only 0.2B parameters, 31.2 ms inference latency, and 0.9 GB inference VRAM on a consumer-grade RTX 4090, matching or outperforming substantially larger VLA policies. These results establish TurboVLA as a simple and effective alternative to the prevailing LLM-centric VLA paradigm, offering a new perspective on how vision, language, and action can be connected for efficient robotic manipulation. Code is available at this https URL.

---

## 12. StatePlay: State-Aware Game World Models for Mechanics-Consistent Generation

**Authors:** Zijun Lin, Zeqing Wang, Cheston Tan, Bihan Wen, Yeying Jin
**arXiv:** [2607.26754](https://arxiv.org/abs/2607.26754)
**Categories:** Computer Vision and Pattern Recognition (cs.CV)

Recent game world models can generate visually realistic and interactive environments conditioned on player actions. However, games are not defined by pixels alone; they are governed by explicit mechanics, namely state-dependent rules that control health reduction, skill activation, and game termination. These mechanics depend on precise internal states, such as health points, skill meters, and timers, which are tightly coupled with visual observations and determine how gameplay evolves. Without modeling these state dynamics, existing game world models may generate visually plausible rollouts but violate the underlying game rules. In this paper, we propose StatePlay, a novel state-aware game world model that jointly predicts visual content and game states to promote mechanics-consistent generation. StatePlay adopts a mixture-of-transformers (MoT)-style architecture that preserves specialized visual and state representations while enabling cross-modal interaction, allowing predicted states to guide frame generation. Each branch is further optimized with a distinct objective suited to its modality. Experiments show that StatePlay achieves an average normalized L1 distance below 0.06 for state prediction. Furthermore, compared with models without explicit state modeling, our method improves mechanics fidelity in generated game rollouts by 18.6%. Overall, our work highlights the importance of state-aware game world modeling and advances beyond pixel-level realism toward complete and mechanically faithful game generation.

---
