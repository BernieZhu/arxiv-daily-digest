# arXiv Daily Digest — 2026-07-07

**Mode:** direct
**Categories:** cs.AI, cs.LG, cs.RO, cs.CV
**Keywords:** VLA, world model, world action model
**Papers found:** 38

---

## 1. MoP-JEPA: Hard-Assigned Predictor Mixtures for Stochastic JEPA World Models

**Authors:** Zhi Song, Ximing Xing, Zhenchao Tang, ..., Lusheng Wang, Jianhua Yao
**arXiv:** [2607.05238](https://arxiv.org/abs/2607.05238)
**Categories:** Artificial Intelligence (cs.AI)

JEPA world models predict the next latent state with a single deterministic predictor trained by latent regression. We show that this fails structurally when the environment is stochastic: at a branching transition, the regression-optimal predictor outputs the conditional mean of the successor embeddings, a point between the true next states that corresponds to no state at all. We prove this collapse for deterministic and gated mixture-of-experts predictors, and prove that MoP-JEPA's hard-assigned predictors converge instead to a quantizer of the transition distribution: one head per successor mode, enumerable in a single forward pass, which is the interface a planner consumes. On official OGBench offline data with leak-free evaluation, planning over single-predictor rollouts performs poorly ($0.02$--$0.09$ success) while planning over our predicted modes reaches up to $0.85$, ahead of deterministic, gated-MoE, and variational predictors on every task. Because multi-prediction evaluation invites coverage freeloading, a verification protocol is part of the method: an input-agnostic codebook control, a shuffled-context test, router-gated readouts, transition-precision guards, and a verified-route criterion in which the model proposes its transition graph blind and ground truth is used only to check the result. Under this criterion our method outperforms the strongest soft alternative on all three mazes ($2$--$5\times$), and the protocol identifies the remaining gap in that baseline's raw scores as routes through predicted transitions that do not exist. The same model executes in the real environment, placing second of seven against the published OGBench baselines on the hardest maze. Multimodal dynamics decide whether a JEPA world model can plan at all; a mixture of predictors with hard assignment is a minimal and verifiable fix.

---

## 2. VLA Grounder: Language-Conditioning Space Optimization for Black-Box VLA Models

**Authors:** Damir Shodiev, Aleksei Staroverov, Nikita Kachaev, Alexey K. Kovalev, Aleksandr I. Panov
**arXiv:** [2607.04517](https://arxiv.org/abs/2607.04517)
**Categories:** Artificial Intelligence (cs.AI)

Vision-Language-Action (VLA) models are commonly treated as end-to-end action policies conditioned on natural-language task descriptions. In practice, however, their behavior often depends sharply on how the instruction is phrased, suggesting that language is not merely a task label but an optimizable conditioning input. We study whether frozen VLA policies can be improved by optimizing language space rather than updating action weights. Our method introduces a language-conditioning space policy that translates a human instruction into a short VLA-grounded command using object appearance, spatial relations, and target-grounding cues. The language-conditioning space policy is initialized with a failure-derived command-space prior and optimized with reinforcement learning from sparse task-completion rewards, while the downstream VLA remains fully frozen. This yields language-conditioning space optimization: RL discovers which VLA-grounded commands best elicit successful behavior from the frozen action policy. Experiments on RL4VLA and VL-Think show that language-conditioning space optimization improves success on instruction-sensitive, symbolic, and multi-object manipulation tasks, demonstrating that language can serve as an optimizable variable for a robot foundation models. Website: this https URL

---

## 3. From Fixed to Free Cameras: Calibration-Free View-Robust Vision-Language-Action Model

**Authors:** Wenhao Li, Xueying Jiang, Quanhao Qian, ..., Gongjie Zhang, Ran Xu
**arXiv:** [2607.05396](https://arxiv.org/abs/2607.05396)
**Categories:** Computer Vision and Pattern Recognition (cs.CV); Artificial Intelligence (cs.AI); Machine Learning (cs.LG); Robotics (cs.RO)

Real-world robot deployment rarely maintains the training-stage camera setup, where cameras often experience repositioning or remounting depending on actual scenarios. Existing view-robust Vision-Language-Action (VLA) policies tolerate such camera variations only when the camera extrinsics are explicitly provided, making them fragile and hard to use especially when view robustness is critical. We argue that the policy should not be told where the camera is, but rather figure it out by itself. To this end, we introduce Camera-Centric VLA (CamVLA), a new VLA model that decouples manipulation controls from camera geometry by predicting (i) a camera-centric end-effector action expressed in the local camera frame, and (ii) a 6-DoF hand-eye matrix relating cameras to the robot base. A deterministic geometric transformation composes the two predictions into a robot base-frame action. This disentangles how I should move in pose-independent camera-centric action generation from where I am looking from in camera-perspective geometric grounding. The resulting policy is calibration-free, depth-free, and single-view, requiring only a single monocular RGB image as the visual observation and task instruction at deployment. Evaluations in both simulation and real-world robot data show that CamVLA consistently improves success rates across diverse unseen viewpoints. Project page: this https URL.

---

## 4. Multiplayer Interactive World Models with Representation Autoencoders

**Authors:** Anthony Hu, Václav Volhejn, Adrien Ramanana Rahary, ..., Michael Black, Patrick Pérez
**arXiv:** [2607.05352](https://arxiv.org/abs/2607.05352)
**Categories:** Computer Vision and Pattern Recognition (cs.CV); Artificial Intelligence (cs.AI); Machine Learning (cs.LG)

We introduce the first multiplayer world model for highly dynamic environments governed by complex physical interactions. Whereas single-player world models treat the other agents as part of the environment, ours conditions on the action streams of multiple agents, learning to attribute changes in the scene to the correct player and to stay coherent under arbitrary combinations of their actions. We study this problem in the game of Rocket League, where players compete and cooperate under fast, tightly coupled dynamics. Trained on 10,000 hours of gameplay collected with publicly available bots, our 5-billion-parameter latent diffusion model generates four-player matches in real time, producing 20 frames per second on a single Nvidia B200 GPU. Although trained only on short clips, its rollouts stay stable far beyond the training horizon: distributional quality holds steady out to five minutes, the longest horizon we measure, and in practice we observe rollouts continuing for hours with no sign of collapse. We systematically investigate the central design choices: the video codec, the generative objective, and the multiplayer conditioning scheme. In addition, we characterize how behavior changes with model and data scale, including the capabilities that emerge and the failure modes that persist. We further develop targeted evaluations that probe the model's physical understanding rather than visual appearance alone. To support continued research on multiplayer world models, we release our dataset, our full training and inference codebase, and a live demo.

---

## 5. Do Vision-Language-Action Models Mean What They Say? On the Role of Faithfulness in Embodied Reasoning

**Authors:** Matthew Foutter, Matteo Cercola, Lena Wild, ..., Daniele Gammelli, Marco Pavone
**arXiv:** [2607.04681](https://arxiv.org/abs/2607.04681)
**Categories:** Robotics (cs.RO); Artificial Intelligence (cs.AI)

Embodied Chain-of-Thought has emerged as a promising mechanism to enhance robot decision-making and interpretability in black-box Vision-Language Action (VLA) models. However, whether this verbalized Chain-of-Thought truthfully reflects the policy's underlying decision process remains poorly understood. We distinguish between functional reasoning, in which reasoning improves task performance, and faithful reasoning, in which reasoning truly reflects the policy's internal decision process. We argue that SoTA alignment strategies offer a necessary but insufficient notion of faithfulness, admitting reasoning whose intermediate steps can mask the causal links in action prediction through confounding factors (e.g., reasoning that is ungrounded in the environment and internally disconnected or inconsistent), restricting policy generalization. We study this gap through a human evaluation of a SoTA reasoning model for autonomous driving, revealing an inconsistent coupling between reasoning quality and downstream trajectory improvement. We then operationalize a behavioral surrogate for embodied faithfulness through a learned critic, Pinocchio, scoring observation grounding and stepwise coherence, and use this critic as a dense reward signal in post-training an embodied policy with reinforcement learning. Across withheld driving benchmarks, our post-trained planner improves faithfulness by 4% and 18% over SoTA alignment and trajectory error post-training baselines, respectively, while maintaining competitive downstream task performance. Finally, on a synthetic out-of-distribution test set, post-training for faithfulness improves policy responsiveness to rare counterfactual scenarios by 1.6x that of a SoTA policy, suggesting that faithful reasoning traces contribute to more robust, generalizable, and interpretable embodied intelligence. Project page: this https URL

---

## 6. Simple-to-Complex Structured Demonstrations for Vision-Language-Action Learning

**Authors:** Xinchuan Qiu, Yi Yu
**arXiv:** [2607.04591](https://arxiv.org/abs/2607.04591)
**Categories:** Robotics (cs.RO); Artificial Intelligence (cs.AI)

Vision-Language-Action (VLA) models have demonstrated strong capabilities in robotic manipulation by integrating visual perception, language understanding, and robot action generation. Existing research has primarily focused on improving model architectures, training strategies, and dataset scale, while little attention has been paid to how demonstrations are collected and organized. We identify demonstration organization as a fundamental yet overlooked aspect of imitation learning, as it directly affects policy learning efficiency, training stability, and policy generalization. To address this gap, we propose a simple-to-complex structured demonstration collection strategy for VLA learning using a dual-arm robotic platform. Our approach systematically organizes data through three general principles: (i) decomposing complex manipulation tasks into progressively learnable sub-skills, (ii) standardizing the interaction environment to reduce unnecessary variability, and (iii) organizing demonstrations according to progressively increasing task complexity. This structured design enables VLA models to first acquire fundamental manipulation skills before learning increasingly complex task compositions, facilitating more effective learning of long-horizon manipulation tasks. We evaluate the proposed strategy on two representative robotic manipulation tasks: block grasping and sorting, and towel folding. Experimental results show consistent improvements in task success rate and training stability compared with the baseline method of directly collecting end-to-end complete task trajectories. These findings highlight demonstration organization as a previously underexplored but important factor in VLA learning and provide practical insights into efficient skill acquisition, scalable dataset construction, and long-horizon robotic manipulation.

---

## 7. Mask2Real-WM: Segmentation Masks as a Sim-to-Real Bridge for Controllable Dexterous World Models

**Authors:** Riccardo O. Feingold, Davide Liconti, Chenyu Yang, Robert K. Katzschmann
**arXiv:** [2607.04546](https://arxiv.org/abs/2607.04546)
**Categories:** Robotics (cs.RO); Artificial Intelligence (cs.AI); Computer Vision and Pattern Recognition (cs.CV); Machine Learning (cs.LG)

Action-conditioned world models allow robots to predict the future consequences of candidate actions without additional physical interaction, supporting policy evaluation, planning, and data augmentation. We present Mask2Real-WM, a two-stage action-conditioned world model for dexterous manipulation that decouples pixel prediction into a dynamics model and a rendering model. The dynamics model predicts future segmentation masks from past masks and 23-DoF action sequences. The rendering model maps the predicted masks to photorealistic RGB using a ControlNet-augmented Stable Video Diffusion backbone. The smaller sim-to-real gap in segmentation space enables the dynamics model to benefit from large-scale pretraining on over 50 h of synthetic simulation data, followed by fine-tuning on fewer than 2.5 h of real demonstrations. Experiments on a dexterous pick-and-place benchmark show that mask conditioning and simulation pretraining are both required for per-DoF action controllability across all 23 degrees of freedom. In contrast, monolithic baselines capture broad hand and end-effector trajectories but do not reliably reflect fine-grained, per-joint action effects.

---

## 8. CRISP: A Spatiotemporal Camera-Radar Backbone for Driving via Forecasting-Based World-Model Pretraining

**Authors:** Jingyu Song, Yi Liu, Katherine A. Skinner
**arXiv:** [2607.04541](https://arxiv.org/abs/2607.04541)
**Categories:** Computer Vision and Pattern Recognition (cs.CV); Artificial Intelligence (cs.AI); Machine Learning (cs.LG); Robotics (cs.RO)

Camera-radar (CR) fusion is a practical sensing configuration for autonomous driving, but existing models are typically trained with task-specific supervision, limiting reusable representation learning. We present CRISP, a spatiotemporal CR backbone pretrained through forecasting-based representation learning. Given historical multi-view images and radar sweeps, CRISP learns a unified bird's-eye-view (BEV) representation by predicting future LiDAR point clouds. LiDAR is used only as privileged supervision during pretraining; the deployed model requires only camera and radar. To make forecasting-based pretraining effective for CR fusion, CRISP introduces an enhanced radar encoder, radar-enhanced temporal self-attention, and multimodal feature rendering with modality innovation gating. These components inject radar range and Doppler cues into BEV temporal propagation and allow BEV tokens to selectively incorporate camera and radar evidence. Experiments on nuScenes show that CRISP improves long-horizon point cloud forecasting and transfers effectively to downstream tasks, including 3D detection, tracking, online mapping, motion forecasting, future occupancy prediction, and planning, suggesting that predictive CR pretraining is a promising path toward scalable driving representations under practical sensor configurations. The project website is this https URL.

---

## 9. Operator-on-F complements value-equivalence: a planning-time diagnostic for latent world models

**Authors:** Donna Vakalis
**arXiv:** [2607.04464](https://arxiv.org/abs/2607.04464)
**Categories:** Machine Learning (cs.LG); Artificial Intelligence (cs.AI)

World-model evaluation for model-based reinforcement learning typically asks whether the learned model predicts reward and value well, which can leave planning-relevant errors in the model's latent rollouts unmeasured. We introduce a complementary diagnostic, operator-on-F, that compares a model's k-step latent pushforward to the environment's on an observable subset F, using the model's own predictor. On a TD-MPC2 size sweep over cheetah-run, reward-prediction error stays within [0.028, 0.091] for every model size - only about 3x variation - so an unnormalized reward-fit check has narrow resolution to distinguish them; the (unnormalized) Bellman residual and reward error themselves have weak relationships with return (Spearman -0.10 and -0.30). Operator error spans 0.28 to 2.62 over the same sizes. At 317M the operator error is 2.62 - an order of magnitude above the 0.28-0.36 cluster - and the planning return collapses to 0.9, while reward-prediction error (0.091) is the highest of the five but stays within the same small [0.028, 0.091] range as the rest of the sweep. The rank correlation between operator error and return loss is -0.90 (anchor-bootstrap 95% CI [-0.90, -0.70] at n=5 sizes; leave-one-out removal of any single size leaves it at -0.80 or stronger). The operator also returns informative, architecture-discriminating estimates in a cross-architecture comparison between TD-MPC2 and a pure-SSL latent world model. The operator diagnostic complements value-equivalence rather than replacing it.

---

## 10. HALO-WA: Hybrid-Attention Latent-Guided Online Reinforcement Learning for World-Action Models

**Authors:** Angen Ye, Weijie Ke, Xiaofeng Wang, ..., Junjie Xie, Dapeng Zhang
**arXiv:** [2607.04265](https://arxiv.org/abs/2607.04265)
**Categories:** Robotics (cs.RO); Artificial Intelligence (cs.AI)

World-action (WA) models can generate long-horizon action chunks for general-purpose robotic manipulation, but they remain vulnerable to calibration, perception, and contact-dynamics errors in real-world precision tasks, often failing in the final few millimeters of alignment or insertion. We propose HALO-WA, a hybrid-attention latent-guided online reinforcement learning (RL) framework for WA models, which leverages latent features and action priors from the WA generation process through a lightweight actor-critic adapter to enable fast online adaptation to real deployment errors. HALO-WA introduces a hybrid-attention structure that preserves the temporal consistency of action chunks while reading task-relevant information from WA latents conditioned on visual context and end-stage correction requirements, thereby producing refined action chunks. We validate HALO-WA on four real-world precision manipulation tasks, where it improves the average success rate from 26.4\% for WA-base to 87.1\%, outperforming the strongest baseline by 19.2 percentage points while requiring only 45--75 minutes of online training per task. To facilitate reproducibility, we further conduct supplementary simulation experiments in RoboTwin and release the code at this https URL.

---

## 11. !Imperio, smolVLA: The Implications of Data Poisoning on Open Source Robotics

**Authors:** Stefan Bühler, Mark Schutera
**arXiv:** [2607.04146](https://arxiv.org/abs/2607.04146)
**Categories:** Robotics (cs.RO); Artificial Intelligence (cs.AI); Computation and Language (cs.CL); Cryptography and Security (cs.CR); Machine Learning (cs.LG)

This work establishes that trigger-word data poisoning of vision language action models is practical, while at the same time the open-source robotics ecosystem holds trust assumptions about community contributions. A few poisoned samples can silently embed a backdoor that disables a robot on command. We evaluate this threat against smolVLA on a real-world pick-and-place task, training on three poison ratios and evaluating across different prompts on the LeRobot platform. Three poisoned episodes in 320 clean episodes suffice for a complete denial of service. Success rate drops to 0.0 plus minus 0.0% across all trigger-word conditions and the robot locks into a fixed joint configuration rather than executing any task-relevant motion. Clean-prompt behaviour holds at approx. 50% success rate across all poison ratios, confirming the attack is stealthy under normal operation. A single poisoned episode already reduces success rate to 6.7 plus minus 6.7%. The robot still moves, but no longer completes the task. The attack generalises to front, middle, and end trigger placements despite training exclusively on front-placed triggers. These findings establish that the threat is practical, low-cost, and stealthy, and warrant treating dataset provenance as a first-class concern in open-source robotics ecosystems.

---

## 12. DynaVieW: Schema-Guided World Modeling for Understanding Hierarchical Visual Dynamics

**Authors:** Silin Gao, Hao Zhao, Zeming Chen, ..., Syrielle Montariol, Antoine Bosselut
**arXiv:** [2607.04112](https://arxiv.org/abs/2607.04112)
**Categories:** Machine Learning (cs.LG); Artificial Intelligence (cs.AI); Computation and Language (cs.CL); Computer Vision and Pattern Recognition (cs.CV)

Multimodal LLMs struggle to systematically model the temporal evolution of visual scenes in videos or multi-image sequences. Such inputs require models to predict or simulate multiple levels of dynamic constituents, such as actions taken in the visual sequence, and the associated changes to the visual environment that result. To address this challenge, we propose a dynamic schema-guided world model, DynaVieW, optimized for visual dynamic prediction and simulation. DynaVieW achieves an in-depth understanding of visual dynamics by learning interleaved state-transition sequences, where states cover broad visual scenes from video keyframes, and transitions capture comprehensive dynamic constituents within a hierarchical schema. DynaVieW jointly models transition prediction and state simulation under a mixture-of-experts architecture, with a cross-expert selective attention and a schema token re-weighted loss, to ensure effective and robust learning. DynaVieW's understanding of visual dynamics boosts its downstream performance in visual narrative creation and world simulation, showing improved consistency, controllability, and instruction-following.

---

## 13. Worldscape-MoE: A Unified Mixture-of-Experts World Model for Scalable Heterogeneous Action Control

**Authors:** Jianjie Fang, Yongyan Xu, Ziyou Wang, ..., Xinlei Chen, Yong Li
**arXiv:** [2607.03964](https://arxiv.org/abs/2607.03964)
**Categories:** Robotics (cs.RO); Artificial Intelligence (cs.AI)

World models are rapidly becoming a core infrastructure for embodied intelligence and interactive agents: they provide controllable simulators in which agents can perceive, act, forecast, and acquire scalable experience. Yet current video generation world models are still organized around isolated control interfaces, such as camera trajectories, robot actions, or hand-joint signals. This fragmentation is increasingly a scaling bottleneck. The central challenge is not the absence of controllable generators, but the lack of a unified and extensible learning framework that can absorb heterogeneous action supervision while preserving a shared model of world dynamics. In this work, we introduce Worldscape-MoE, a Mixture-of-Experts world model built on Diffusion Transformers for scalable heterogeneous action control. Our key observation is that different controls specify different interfaces to the same underlying world: although their representations differ, they constrain shared physical regularities, scene dynamics, and interaction semantics. Worldscape-MoE operationalizes this observation through modality-aware control injection, shared and control-specific experts, and a progressive MoE tuning strategy that supports continual extension to new action modalities. Experiments across locomotion, robotic manipulation, and egocentric hand control show that heterogeneous supervision improves rather than interferes with individual control capabilities. Worldscape-MoE achieves strong results on WorldArena, improves locomotion and hand-control metrics, exhibits robust out-of-distribution generalization, and demonstrates scaling behavior as additional control data and experts are integrated.

---

## 14. Latent Clarity: Bridging World-Model Kinematics to Semantic Manifolds for Video Anomaly Anticipation

**Authors:** Abu Anas Ibn Samad
**arXiv:** [2607.03558](https://arxiv.org/abs/2607.03558)
**Categories:** Computer Vision and Pattern Recognition (cs.CV); Artificial Intelligence (cs.AI); Machine Learning (cs.LG)

Continuous video anomaly detection is dominated by reactive Multiple Instance Learning (MIL) that collapses spatiotemporal features into scalar scores. We introduce PULS (Predictive Unified Latent Space), a continuous semantic world-model pipeline comprising two modules: a 490M-parameter KSD Bridge (Kinematic-to-Semantic Distillation) and a 16.8M-parameter Anticipatory State Predictor (ASP). The KSD Bridge maps V-JEPA 2 physical tensors into the 2048-d Qwen3-VL-Embedding-2B text-aligned hypersphere, trained on a subset of UCF-Crime. This translation alone yields a chunk-level AUROC of 0.8994 for UCF-Crime and 0.8162 for out-of-distribution XD-Violence without MIL or hierarchical fusion.
We introduce and validate the Latent Clarity Hypothesis: because JEPA's temporal predictor discards aleatoric pixel noise while preserving kinematics, anticipated future representations are more semantically separable than observed presents. The ASP sharpens these anticipated future latents, achieving 44.5% mean 14-way zero-shot VQA accuracy (exceeding observation baseline by +9.6 pp). Applying the ASP to Observation Tensors collapses accuracy to 7.3% (random chance), proving Anticipation and Observation occupy distinct sub-manifolds. A Triple-Track Lead-Time protocol with an L1-surprise gate yields a peak +8.9 pp anticipatory advantage at T-0.5s (p < 0.001, N = 1,000 permutation), separating physical anticipation from static scene priors. Zero-shot transfer to XD-Violence confirms that Newtonian-invariant kinematic representations generalize out-of-distribution.

---

## 15. HiMe: Hierarchical Embodied Memory for Long-Horizon Vision-Language-Action Control

**Authors:** Li Ji, Siyin Wang, Pengfang Qian, ..., Jingjing Gong, Xipeng Qiu
**arXiv:** [2607.03449](https://arxiv.org/abs/2607.03449)
**Categories:** Robotics (cs.RO); Artificial Intelligence (cs.AI)

Current Vision-Language-Action (VLA) models excel at robotic manipulation but often struggle with non-Markovian tasks requiring long-term memory and reasoning due to their reliance on immediate observations. Existing solutions face a ''frequency-competence paradox,'' where stronger reasoning models are too slow for real-time control, while faster models lack sufficient reasoning capabilities. To resolve this architectural misalignment, we propose HiMe, a Hierarchical Embodied Memory framework that decouples embodied intelligence into a high-frequency Executor for execution, a Sentry for working memory, and a Planner for long-term strategy. We also introduce a dynamic knowledge system based on cross-modal semantic schemas and active management mechanisms, allowing robots to maintain memory plasticity through ''Add, Update, and Delete'' operations. This hierarchical design effectively balances the conflict between real-time execution and slow thinking planning, significantly improving success rates in long-horizon tasks. Experiments demonstrate that this approach not only outperforms flat memory baselines but also exhibits the novel ability to self-correct its internal knowledge based on human preferences.

---

## 16. AnchorVLA: Bridging Discrete Decisions and Continuous Trajectories for Vision-Language-Action Planning

**Authors:** Qi Liu, Yabei Li, Hongsong Wang, Heng Zhang, Lei He
**arXiv:** [2607.03182](https://arxiv.org/abs/2607.03182)
**Categories:** Robotics (cs.RO); Artificial Intelligence (cs.AI)

Autonomous driving planning requires translating navigation intent, traffic rules, dynamic interactions, and language instructions into executable continuous trajectories. Vision-Language-Action models have been introduced into driving planning to improve long-tail generalization, commonsense reasoning, high-level semantic understanding, and explainability. However, existing VLA planners mainly follow planning-head-based trajectory prediction or full-trajectory autoregressive generation. The former only weakly constrains continuous trajectory generation with VLA reasoning, while the latter relies on long sequences of low-information-density coordinate tokens, making semantic-action alignment difficult and leading to discretization errors and inefficient inference. To address these limitations, we propose AnchorVLA, a hierarchical decision-anchored VLA planning framework that uses trajectory-pattern anchors as an explicit interface between high-level VLA reasoning and continuous trajectory execution. Specifically, Decision-as-Anchor Representation represents behavior-level driving decisions with anchor tokens, each encoding an entire local motion pattern rather than a single coordinate point. Decision-Anchored Residual Flow then generates fine-grained continuous trajectories in the selected anchor-defined residual space, capturing multi-modal execution refinements after high-level decision making. By reasoning over compact and semantically meaningful anchors instead of autoregressively generating waypoint sequences, AnchorVLA preserves LLM-based decision making while improving inference efficiency, semantic-action alignment, and continuous generation flexibility. Experiments on the Bench2Drive closed-loop benchmark show that AnchorVLA achieves a state-of-the-art Success Rate of 77.28 and a competitive Driving Score of 89.92.

---

## 17. Learning Task-Sufficient World Models by Synergizing Agentic Exploration and Structured Modeling

**Authors:** Fan Feng, Yujia Zheng, Minghao Fu, ..., Biwei Huang, Kun Zhang
**arXiv:** [2607.04409](https://arxiv.org/abs/2607.04409)
**Categories:** Machine Learning (cs.LG)

Learning and planning in imagination using world models provides an effective paradigm for training agents for decision-making. However, existing approaches often rely on high-dimensional latent spaces or generic visual embeddings that retain many factors irrelevant to control, limiting efficiency and generalization across tasks. To this end, we study how agents can learn world models with representations that are task-specific, minimal, and sufficient for decision-making. We achieve this via a closed-loop synergy between the agent and the world model, in which structured world-model learning distills task-sufficient representations from informative interaction data. On the agent side, agents actively probe the environment to collect informative trajectories that expose task-relevant latent factors, guided by an adaptive curriculum. On the world-model side, we learn structured representations over observations to distill compact, task-sufficient latent states from the collected interaction data. This synergy enables the empirical recovery of task-sufficient latent representations that capture all control-relevant factors. Leveraging these representations, the resulting policies achieve improved sample efficiency and generalization, including generalization across skills, object-skill compositions, and previously unseen tasks on standard continuous-control and robotic-manipulation benchmarks.

---

## 18. Reduced-Order Models: The Mother of World Models

**Authors:** Rajat Ghosh
**arXiv:** [2607.03198](https://arxiv.org/abs/2607.03198)
**Categories:** Machine Learning (cs.LG); Mathematical Physics (math-ph)

World models -- compressed latent representations of an environment that support action-conditioned prediction and planning -- are typically presented as a product of modern self-supervised learning. This paper argues that the functional anatomy of a world model was independently developed, deployed, and formally analyzed decades earlier in the model-order-reduction (MOR) and control literature, under different names and for a different purpose: the real-time operation of physical systems. We trace the anatomy across three communities. Low-dimensional models of turbulence built on proper orthogonal decomposition (POD) supplied latent dynamics learned from data of a chaotic environment; eigenface methods in early computer vision supplied the encoder-decoder half, including a primitive runtime validity check; and measurement-based POD frameworks for facility thermal control assembled the complete loop -- POD coefficients as latent state, parametric dependence on actuator setpoints as action conditioning, modal reconstruction as decoding, and, critically, a priori analytical error bounds as a verification layer that certified when the model's predictions could be trusted in closed loop. We then examine what each tradition possesses that the other lacks: MOR contributes verification, physical grounding, and extreme data efficiency; learned world models contribute nonlinear representation, transferability, and horizon. We argue that the outstanding obstacle to deploying world models in systems that cannot fail -- power, thermal, process control -- is not predictive fidelity but verifiability, and we outline a research agenda for physics-grounded, verifiable world models that unifies the two lineages.

---

## 19. XS-VLA: Coupling Coarse-grained Spatial Distillation with Latent Flow Matching for Lightweight Robotic Control

**Authors:** Lei Iok Tong, Qingchen Xie, Wei Huang, ..., Xiaolong Liu, Zhidong Deng
**arXiv:** [2607.04171](https://arxiv.org/abs/2607.04171)
**Categories:** Robotics (cs.RO); Machine Learning (cs.LG)

Large Vision-Language Models (LVLMs) have shown strong multimodal understanding and spatial grounding, but their computational cost limits real-time robotic control. In contrast, lightweight models are suitable for edge deployment but often suffer from "spatial blindness", namely weak native spatial prediction ability. Training Vision-Language-Action (VLA) models on mixed human demonstrations can also degrade policy performance due to highly diverse behaviors. To address these limitations, we propose XS-VLA, a two-stage framework for efficient and spatially grounded robotic manipulation. First, we distill spatial semantic knowledge from Qwen3-VL-4B into the SmolVLM2-0.25B backbone by fine-tuning on curated coarse-grained spatial descriptions, turning the lightweight model into a spatially grounded engine. Second, we use this enhanced backbone to condition a Latent Flow Matching policy. Unlike deterministic controllers, our policy combines a Conditional Variational Autoencoder (CVAE) with Flow Matching dynamics to model complex multimodal action distributions. On the LIBERO benchmark, XS-VLA achieves state-of-the-art performance among models with fewer than 0.5B parameters. It improves average success rates by up to 7.2 percent, including a 23 percent gain on LIBERO-Long, over the SmolVLA 0.25B baseline, and outperforms the larger 2.2B vanilla SmolVLA. Ablations show that spatial tuning and generative latent flow control substantially improve lightweight VLA performance, delivering a 3.2 times speedup in mission execution over the previous lightweight flow matching policy.

---

## 20. WorldBagel: Uncovering the Power of Unified Multimodal Models for Vision-Language-Action-World Modeling

**Authors:** Zelin Zhao, Min Shi, Bo Yuan, ..., Humphrey Shi, Yongxin Chen
**arXiv:** [2607.03461](https://arxiv.org/abs/2607.03461)
**Categories:** Computer Vision and Pattern Recognition (cs.CV); Machine Learning (cs.LG)

World models aim to capture environment dynamics in ways that support perception, reasoning, and action, and have recently become a central direction in Vision-Language-Action-World (VLAW) modeling. Meanwhile, unified vision-language models have demonstrated strong multimodal generation capabilities, yet their potential as world models remains underexplored. In this work, we introduce \texttt{WorldBagel}, a unified VLAW framework built on BAGEL, a modern multimodal unified model, and use it to systematically investigate the role of unification in world modeling. Across multi-task robotic manipulation and cross-domain experiments, \texttt{WorldBagel} consistently outperforms task-specific alternatives and learns action representations that are more structured and semantically aligned with visual and linguistic context. Experiments on LIBERO, Language Table, and Franka show that unification is not only an architectural convenience, but also a key factor in learning effective VLAW models, leading to consistent empirical gains and deeper insights into multimodal world modeling. Code and model checkpoints will be released upon acceptance.

---

## 21. Deform360: A Massive Multi-view Visuotactile Dataset for Deformable World Models

**Authors:** Hongyu Li, Wanjia Fu, Xiaoyan Cong, ..., George Konidaris, Yunzhu Li
**arXiv:** [2607.05390](https://arxiv.org/abs/2607.05390)
**Categories:** Robotics (cs.RO); Computer Vision and Pattern Recognition (cs.CV)

Predicting object dynamics (i.e., world modeling) is a fundamental challenge for robotic manipulation, and modeling deformable objects presents a particularly difficult case due to their high-dimensional state spaces and complex material properties. While current world models approach this through two distinct paradigms: learning the dynamics over the 2D pixel space or more explicit 3D geometric space. A systematic understanding of their relative strengths and limitations remains elusive due to the lack of diverse, large-scale real-world data. To address this, we present Deform360, a large-scale visuotactile dataset featuring 198 daily-life objects, 1,980 interaction sequences, and over 215 hours of observations from 41 surround-view cameras and bimanual tactile grippers to capture both global motion and contact-induced local deformations. Leveraging a novel markerless visuotactile 3D tracking pipeline to extract dense geometry and motion, we systematically evaluate current state-of-the-art world models, comparing 2D video models against 3D particle models. Finally, we provide a preliminary demonstration indicating the real-world applicability of our dataset by performing robot planning tasks on deformable objects. Our analysis reveals key insights into the trade-offs between structural priors and scalability, providing a solid benchmark for future research in generalizable deformable object-centric world modeling. Project website: this https URL

---

## 22. InternVLA-A1.5: Unifying Understanding, Latent Foresight, and Action for Compositional Generalization

**Authors:** Haoxiang Ma, Junhao Cai, Xiaoxu Xu, ..., Chunhua Shen, Weinan Zhang
**arXiv:** [2607.04988](https://arxiv.org/abs/2607.04988)
**Categories:** Robotics (cs.RO)

Unified models for robot manipulation aim to equip one policy with both the semantic priors of pretrained VLMs and the physical dynamics learned through future prediction. In practice, existing designs tend to erode the semantics of the pretrained backbone, suffer interference among heterogeneous objectives, and learn future prediction from scratch in pixel space, leaving the dynamics priors of pretrained video generators unexploited. We present InternVLA-A1.5, which builds the policy on a native VLM backbone that keeps training on VQA and subtask prediction, and attaches a lightweight unified expert for continuous action generation. Future prediction is recast as a latent-querying problem, where a small set of learnable foresight tokens condenses the task-relevant future into a compact latent code under the supervision of a frozen pretrained video generation model, so the policy inherits world-model dynamics priors without ever learning pixel-level generation. The video branch is discarded at inference, keeping real-time control. Pretrained on 1.2M robot episodes and 3M multimodal samples, InternVLA-A1.5 achieves the best overall results on all six simulation benchmarks. In the real world, the preserved semantics deliver the strongest compositional generalization on held-out instruction bindings, and the two designs together sustain long-horizon execution.

---

## 23. CAC-VLA: Context-Gated Action Conditioning for Vision-Language-Action Models

**Authors:** Yifu Xiong, Wenhao Yu, Jiaxuan Lin, ..., Yanyong Zhang, Jianmin Ji
**arXiv:** [2607.04816](https://arxiv.org/abs/2607.04816)
**Categories:** Robotics (cs.RO)

Vision-Language-Action (VLA) models have become a promising paradigm for generalist robot manipulation, where visual-language representations are used to condition continuous action generation. However, these representations are not explicitly optimized for action conditioning, leaving the action expert to bridge the gap between multimodal understanding and precise motor control. Recent action-reasoning methods introduce additional modules to generate explicit action plans or action-space reasoning signals, demonstrating the benefit of action-level guidance but often requiring separate action-generation frameworks. We propose CAC-VLA, a Context-Gated Action Conditioning framework that learns a lightweight latent-action interface directly within the VLM. Instead of generating executable trajectories, CAC-VLA trains the VLM to predict coarse-to-fine latent actions, which are structured representations encoded from future action segments, and adaptively leverages them to condition the action expert via a context gate. This enables VLM-native action conditioning while calibrating the influence of latent-action guidance on expert action generation. Experiments on LIBERO and LIBERO-Plus demonstrate the effectiveness of CAC-VLA, achieving 98.3% average success rate on LIBERO and 89.5% LIBERO-Plus, suggesting that context-gated latent-action conditioning is an effective interface for continuous expert control.

---

## 24. KAM-WM: Kinematic Affordance Maps from Latent World Models for Robot Manipulation

**Authors:** Xinyu Shao, Keru Zhou, Guowei Huang, ..., Tongtong Cao, Xiu Li
**arXiv:** [2607.04652](https://arxiv.org/abs/2607.04652)
**Categories:** Robotics (cs.RO)

Learning manipulation from few demonstrations requires visual priors that capture not only where to interact, but also how the interaction should begin; static priors such as segmentation masks encode only the former. We present KAM-WM, a framework that extracts a coarse directional interaction cue from a frozen latent video world model without rollout or world-model fine-tuning. KAM-WM queries a Flow Matching image-to-video backbone once and interprets its single-step latent velocity as a Kinematic Affordance Map (KAM), which provides task-conditioned interaction regions and coarse motion structure. A lightweight Perceiver compresses KAM into tokens that condition a diffusion policy together with RGB observations and proprioception. Across LIBERO and RoboTwin2.0, KAM-WM reaches 90.6% average success on LIBERO and achieves 65.7% and 22.4% success rates in the Easy and Hard settings on RoboTwin2.0, respectively. Controlled comparisons against a zero-order mask prior suggest that part of the gains comes from directional information beyond spatial localization alone. These results indicate that, in the evaluated settings, a frozen video model can provide a useful first-order visual prior for control without the test-time cost of future rollout.

---

## 25. SEAM: Smooth Execution of Action-Chunked Motion for Vision-Language-Action Policies

**Authors:** Dijia Zhan, Xuemiao Xu, Jinyi Li, Jie Tang
**arXiv:** [2607.04609](https://arxiv.org/abs/2607.04609)
**Categories:** Robotics (cs.RO)

Vision-Language-Action (VLA) policies that execute fixed-length action chunks can exhibit multimodal bifurcation: a cross-chunk inconsistency in which adjacent chunks generated from independent Gaussian latents can converge to incompatible trajectory modes, producing abrupt discontinuities at chunk boundaries. Existing remedies either require backpropagation through the policy at each denoising step, rely on rejection sampling, or require retraining, each trading computational cost or task reliability for smoother transitions. We propose SEAM (Smooth Execution of Action-Chunked Motion), a training-free inference-time method for flow matching VLAs. SEAM exploits a simple synchronous-execution insight: after the robot consumes the executed prefix, the previous chunk's unexecuted tail is already available as an analytic consistency reference. Its core mechanism, Velocity-guided Loss Steering (VLS), derives a time-dependent target from this tail and applies a closed-form correction after each Euler step without backpropagating through the policy network. On LIBERO-10 with pi_0.5, SEAM reduces boundary jerk by 28%, reduces chunk transition discontinuity by 27%, preserves baseline-level task success, and keeps denoising-loop cost near the unguided baseline.

---

## 26. Look Before You Leap: Distilling Tree Search into Action Evaluation for Frozen VLA Models

**Authors:** Xinyi Xie, Zican Hu, Zhanyu Liu, ..., Zhi Wang, Pichao Wang
**arXiv:** [2607.03751](https://arxiv.org/abs/2607.03751)
**Categories:** Robotics (cs.RO)

Vision-Language-Action (VLA) models acquire broad embodied capabilities through large-scale pretraining, yet their generalization remains far more fragile than that of LLMs and VLMs. The prevailing remedy, post-training via supervised fine-tuning or reinforcement learning, improves task-specific performance but narrows the generalist capability that makes pretraining valuable. We identify a key bottleneck: VLA failures stem not only from action generation but also from action evaluation. A diagnostic pass@k study confirms that frozen VLAs already contain competent behaviors in their output distribution, with overall success rates rising from 33% at pass@1 to 92% at pass@32. Inspired by this, we propose SVA (Search, Value, and Act), a simple framework that equips frozen VLA policies with long-term consequence awareness. SVA first uses Monte-Carlo tree search in simulation to fully explore the VLA's output distribution and collect diverse trajectories annotated with empirical returns; this knowledge is then distilled into a lightweight Q-value model that predicts the expected consequence of candidate actions; at deployment, the frozen VLA proposes multiple candidates and the evaluator selects the one with the highest uncertainty-regularized Q-value, requiring no simulator access. By decoupling action proposal from consequence evaluation, SVA preserves the generalization capacity of the VLA backbone while substantially improving task success rates. Experiments across embodied benchmarks show that SVA consistently improves generalization on unseen tasks and exhibits strong test-time scaling behavior. Strikingly, SVA enables a 9B VLA to outperform a 27B VLA by 7 points at 27% lower inference latency, suggesting that scaling test-time evaluation is more cost-effective than scaling model size.

---

## 27. CoRE-VLA: Towards Scalable and Robust Vision-Language-Action Modeling via Conditional Routing of Experts

**Authors:** Haozhe Zhang, Sixian Li, Yifei Zhang, ..., Jingjing Gong, Xipeng Qiu
**arXiv:** [2607.03693](https://arxiv.org/abs/2607.03693)
**Categories:** Robotics (cs.RO)

Vision-language-action (VLA) models have advanced generalist robotic manipulation, yet real-world deployment reveals a fundamental challenge: robots are equipped with diverse and heterogeneous sensor configurations, auxiliary sensors can fail unexpectedly during operation, and different robot embodiments often lack certain sensors by design. A unified policy that can exploit auxiliary perceptual inputs when available while remaining reliable under sensor absence, whether incidental or by design, is therefore essential for practical deployment. However, existing VLA policies couple action generation to a fixed sensor set through shared dense computation, making them brittle when sensors are missing and limiting their ability to specialize across diverse tasks and long-horizon behaviors. We propose CoRE-VLA, a scalable and robust VLA framework that formulates action generation as context-conditioned sparse computation. Sensor availability gates modality-specialized experts, enabling graceful degradation under missing sensors without retraining. Task intent further routes action-side representations to task-relevant experts, improving specialization across diverse tasks and long-horizon subgoals. While the framework is designed to accommodate different auxiliary sensors, we focus on depth as a representative and practically important auxiliary modality in our experiments. Experiments on LIBERO, RoboCasa GR1 Tabletop, and real-world dual-arm manipulation show that CoRE-VLA achieves strong results on long-horizon and multi-task benchmarks, and outperforms both a dense-action-generator ablation and a strong pretrained VLA baseline, including in zero-shot generalization to unseen scenarios. Modality analysis shows that CoRE-VLA can exploit auxiliary depth when available while remaining robust when depth is unavailable during deployment.

---

## 28. Feeling the Unexpected: ResTacVLA for Contact-Rich Manipulation via Residual Tactile Representation

**Authors:** Pengwei Zhang, Bin Xie, Ce Hao, ..., Long Cheng, Tiancai Wang
**arXiv:** [2607.03387](https://arxiv.org/abs/2607.03387)
**Categories:** Robotics (cs.RO)

Tactile perception is indispensable for contact-rich manipulation, yet integrating it into Vision-Language-Action (VLA) models often induces modality collapse, where high-bandwidth visual features overshadow sparse tactile cues. Inspired by Predictive Coding, a neural mechanism where the brain attenuates predictable inputs to prioritize surprising stimuli, we propose ResTacVLA. Rather than treating tactile data as raw input, we reformulate it as a Residual Tactile Representation capturing the discrepancy between visual priors and physical sensations. By filtering out visually predictable dynamics, this formulation transforms sparse tactile signals into dense, high-value information gain, thereby inherently resolving the bandwidth mismatch. These residuals are discretized through a Vector Quantized (VQ) bottleneck into Latent Contact Primitives that capture critical events missed by vision. Analogous to the neural surprise signal, we leverage the uncertainty of the visual prior to adaptively gate tactile integration, prioritizing residuals specifically during visually unreliable phases to explicitly prevent visual dominance. Experimental results show that ResTacVLA consistently outperforms all baselines on a diverse set of contact-rich manipulation tasks, while remaining robust to unexpected dynamic disturbances. Project page: this https URL

---

## 29. Exp2VLA: Enabling Vision-Language-Action for Drone Navigation from Expert Demonstrations

**Authors:** Van Huyen Dang, Kabilesh Rajendran, Erdi Sayar, Erdal Kayacan
**arXiv:** [2607.03146](https://arxiv.org/abs/2607.03146)
**Categories:** Robotics (cs.RO)

Vision-language-action (VLA) models open a new path toward intuitive robot control by directly linking perception, language, and action in a single end-to-end framework. Yet for UAVs, practical adoption remains difficult because existing solutions are either computationally heavy or insufficiently capable in complex environments. In this work, we propose a practical expert-distillation pipeline (Exp2VLA) for language-conditioned drone navigation. The core idea is to distill expert behavior, obtained from reinforcement learning, teleoperation, or other controllers, into training data that can be used to fine-tune compact VLA models. This allows existing control strategies to be transferred into a unified language-guided navigation model, reducing manual system integration and lowering the barrier for deploying new robot behaviors. Experiments in both sim-to-sim and simulation-in-the-loop settings across multi-object scenes show that the fine-tuned models can handle varied semantic commands and generalize to unseen target compositions. The proposed framework demonstrates how expert-policy distillation can help mechatronic systems move from specialized control modules toward more flexible and reusable robot intelligence.

---

## 30. DREAMSTEER: Latent World Models Can Steer VLA Policies During Deployment Without Any Finetuning

**Authors:** Hanchen Cui, Sergio Arnaud, Arjun Majumdar, ..., Krishna Murthy Jatavallabhula, Franziska Meier
**arXiv:** [2607.02865](https://arxiv.org/abs/2607.02865)
**Categories:** Robotics (cs.RO)

Pretrained vision-language-action (VLA) policies show promising zero-shot generalization, but often fail under deployment-time distribution shift, leading to decreased robustness and inconsistent instruction following. While prior work commonly tackles this by finetuning on in-distribution data, it assumes demonstrations collected on tasks in the target environment. In this work, we propose DREAMSTEER, a deployment-time steering framework for pretrained VLAs without any finetuning or parameter modifications. The key insight in DREAMSTEER is to leverage a latent world model and a value model to steer pretrained VLA policies. During deployment, DREAMSTEER samples candidate action chunks from a VLA policy and predefined motion primitives, imagines their outcomes using an action-conditioned latent world model, and ranks the imagined trajectories with a language-conditioned value model. Across four real-world manipulation benchmarks with unseen objects, DREAMSTEER improves task success rate from 23.75% to 66.25% and instruction-following accuracy from 38.75% to 56.25% over the base VLA policy.

---

## 31. TACO: TActile World Model as a Self-COrrector forScalable VLA Post-Training

**Authors:** Shengbang Liu, Yueru Jia, Yuyang Yan, ..., Boxin Shi, Shanghang Zhang
**arXiv:** [2607.02840](https://arxiv.org/abs/2607.02840)
**Categories:** Robotics (cs.RO)

Vision-Language-Action (VLA) models have shown promising generalization in robotic manipulation, but they still struggle with contact-rich tasks, where minor contact perturbations can cause unrecoverable failures that are hard to detect from vision alone. Since these failures are localized rather than task-level semantic errors, tactile-aware corrective post-training offers an efficient way to improve recovery. However, scaling such supervision through human intervention is costly. Recent works have explored world models to synthesize imagined rollouts for policy improvement, but vision-only world models may produce visually plausible yet contact-inconsistent trajectories. We therefore introduce TACO, a tactile-aware world-model-driven framework for scalable VLA post-training in contact-rich manipulation. Given real robot rollouts, TACO follows a Recognize-Imagine-Label loop with a tactile-aware world model: a unified progress-action model recognizes failure-adjacent states using progress estimates, a visuo-tactile generation model imagines local correction segments, and the progress-action model labels them with executable corrective actions. To incorporate tactile corrective supervision into VLA post-training, TACO combines knowledge-insulated tactile adaptation with advantage-conditioned training, enabling the policy to learn from imagined corrections without degrading pretrained visual-language priors. These components enable TACO to convert real-world failures into imagined visuo-tactile corrections for iterative VLA post-training. Experiments on real-world contact-rich manipulation tasks show that TACO achieves 44% absolute success rate improvement over the base policy and 32% over the policy without knowledge-insulated tactile adaptation.

---

## 32. GigaWorld-1: A Roadmap to Build World Models for Robot Policy Evaluation

**Authors:** GigaWorld Team, Angyuan Ma, Boyuan Wang, ..., Zhanqian Wu, Zheng Zhu
**arXiv:** [2607.02642](https://arxiv.org/abs/2607.02642)
**Categories:** Robotics (cs.RO)

Evaluating embodied robot foundation models remains a critical bottleneck; unlike large language models efficiently assessed via digital benchmarks, robotic policies require slow, costly real-world rollouts limited by hardware and human supervision, which has driven interest in world models as surrogate policy evaluators, yet the key properties that make a world model reliable for policy assessment remain poorly understood. This work presents a systematic study of world models for robotic policy evaluation and introduces WMBench, a benchmark constructed from real-robot teleoperation data and matched policy rollouts covering diverse manipulation tasks to enable controlled comparisons across model families, action encodings, rollout horizons, and evaluation metrics. Using WMBench, we analyze 7 video world models, 4 action representation schemes, and over 324,000 simulated policy rollouts paired with real robot executions, further enriching our analysis with large-scale community submissions from the CVPR 2026 GigaBrain Challenge, curated synthetic trajectories, and a training videos spanning more than 12,000 hours. Our experiments deliver three core insights: evaluator quality is dominated by long-horizon, action-faithful rollout consistency rather than short-term visual realism; pretraining gains stem not only from data scale but from balancing general world knowledge with robot-specific controllability; and architectural choices including action encoding, memory design, and evaluator-focused post-training strongly determine alignment with real-world robot behavior. Drawing on these results, we derive a practical design roadmap and realize it in \textit{GigaWorld-1}, a world model specially optimized for policy evaluation, and we fully release our code, models, datasets, and toolkits to advance scalable evaluation research for embodied foundation models.

---

## 33. Green for Go, Red for No: Visual Grounding via Semantic Segmentation for VLA Navigation Policies

**Authors:** Adrian Szvoren, Dimitrios Kanoulas, Nilufer Tuptuk
**arXiv:** [2607.05122](https://arxiv.org/abs/2607.05122)
**Categories:** Computer Vision and Pattern Recognition (cs.CV); Robotics (cs.RO)

Vision-language-action (VLA) models enable robot navigation from natural language and visual goals, but remain susceptible to perceptual distractions and ambiguous scene interpretations. This paper presents the first empirical evaluation of visual grounding for VLA navigation policies. We propose a real-time segmentation-based grounding method that highlights traversable areas in green and non-traversable areas in red using SegFormer. Two variants are evaluated: observation-only segmentation and joint observation-goal augmentation. Using OmniVLA on the Grand Tour dataset, we show that visual grounding reduces the mean waypoint error by 27-44% at the farthest waypoint, depending on the instruction length. The benefits are greater for long instructions than for short instructions, and grounding provides little improvement for image goals. Normalized error analysis indicates that grounding primarily acts as a trajectory length regularizer, reducing the predicted path length by 30% without improving per-unit-distance reasoning. Our results indicate that visual grounding offers a simple, computationally inexpensive method to improve VLA navigation without model retraining, although it cannot compensate for missing training signals in out-of-distribution instructions.

---

## 34. DynaWM: A Base-VLA-Guided World Foundation Model for Moving-Object Manipulation

**Authors:** Chongkei Chang, Zhidong Deng
**arXiv:** [2607.02604](https://arxiv.org/abs/2607.02604)
**Categories:** Computer Vision and Pattern Recognition (cs.CV); Robotics (cs.RO)

Although vision-language-action (VLA) models have received widespread attention, many challenges remain in manipulating dynamic moving objects. In most existing approaches, end-to-end forward or inverse dynamics models, i.e., world models, are incorporated into high-performance base VLA architectures, which may degrade the performance of well-pretrained base VLA models due to inappropriate fine-tuning. In this paper, we propose DynaWM, a base-VLA-guided world foundation model that adapts to a wide variety of fine-tuned and coarse-tuned base-VLA checkpoints for moving-object manipulation. DynaWM uses a Mamba-3-based action encoder to encode the base action chunk produced by the base VLA into an action-conditioning representation, a V-JEPA 2.1 vision encoder to extract features from multi-view observation history, and a proprioceptive state encoder to encode robotic-arm proprioceptive states. These feature representations jointly condition a flow-matching DiT to regenerate motion-aware action trajectories for moving-object manipulation. For systematic evaluation, we construct the DynaGrasp-32 benchmark, covering six categories of moving-object manipulation tasks, including velocity variation, trajectory variation, and multi-object manipulation, as well as the DynaGrasp-1600 dataset, which consists of 32 scenarios, 1,600 demonstration trajectories, and approximately 1.53M images. For fine-tuned base-VLA checkpoints, DynaWM achieves percentage improvements of 7.19, 45.31, 1.88, and 10.94 over SmolVLA, X-VLA, {\pi}0, and {\pi}0.5, respectively. For coarse-tuned base-VLA checkpoints, performance increases by 35.13, 44.06, 35.69, and 26.13 percentage, respectively. Ablation experiments show that visual encoding enhances success by 27.50%, while reducing success by 45.44% if action conditioning is removed.

---

## 35. PixelPilot: Scalable Vision-Language-Action Models for End-to-End Autonomous Driving

**Authors:** Pin Tang, Guoqing Wang, Xiangxuan Ren, ..., Bailan, Chao Ma
**arXiv:** [2607.04637](https://arxiv.org/abs/2607.04637)
**Categories:** Computer Vision and Pattern Recognition (cs.CV)

Vision-Language-Action Models (VLAs), which leverage the advanced reasoning capabilities of Vision-Language Models (VLMs), show promising generalization in complex autonomous driving scenarios. Existing VLAs typically predict and optimize 3D trajectories from 2D images. While intuitive, this 2D-to-3D prediction is inherently entangled with camera parameters, leading to limited data scalability across heterogeneous driving datasets. Moreover, directly optimizing in 3D space induces severe convergence to trivial solutions, where VLAs rely on ego-status rather than visual scene understanding. To address these issues, we propose PixelPilot, a novel VLA featuring a decoupled planning and lifting paradigm. In the planning phase, PixelPilot reformulates scene understanding and trajectory prediction as sensor-agnostic 2D-to-2D tasks in the image plane, thereby facilitating scalable training across diverse datasets. The planned 2D trajectories are then deterministically lifted to 3D only during inference, ensuring the full exploitation of visual cues and generalization across different vehicles. To realize this paradigm, we propose a knowledge-instilled policy learning strategy that applies dense, intermediate rewards via Group Relative Policy Optimization (GRPO) to enforce a rigorous causal chain from visual perception to spatial planning. Extensive experiments demonstrate that PixelPilot achieves state-of-the-art performance in both open-loop and closed-loop settings, validating its superior scalability and visual reasoning capabilities.

---

## 36. Geographic Diversity Beats Data Volume for Cross-Domain Generalization in Zero-Label JEPA Driving World Models

**Authors:** Santosh Jaiswal
**arXiv:** [2607.04500](https://arxiv.org/abs/2607.04500)
**Categories:** Computer Vision and Pattern Recognition (cs.CV)

Self-supervised latent world models can assign a surprise score to driving scenarios without any human labels. A natural follow-up question is whether such a model, trained on driving data from one geographic region, can generalize its notion of complexity to unseen cities and sensor configurations. We study this question through a controlled transfer experiment: we train JEPA-based world models on nuPlan data (Pittsburgh, Boston, Singapore) and evaluate zero-shot on held-out Argoverse 2 validation scenarios from Miami and Austin. We find that models trained on geographically diverse data generalize significantly better than models trained on equal amounts of single-geography data. In a matched-scale ablation at 63,000 scenarios per condition (n=3 seeds each), combined training reduces mean surprise score by 16.5% relative to nuPlan-only training (0.228 +/- 0.015 vs 0.273 +/- 0.008). Notably, training on 200,000 AV2-only scenarios (3x more data from one geography) still produces higher surprise (0.264) than the combined 63K model, suggesting that geographic diversity is a stronger predictor of cross-domain generalization than raw data volume.

---

## 37. Present but Not Remembered: Auditing How Frozen VLAs Encode, Deploy, and Steer Visual History

**Authors:** Chih-Ting Liao, Xin Cao
**arXiv:** [2607.03372](https://arxiv.org/abs/2607.03372)
**Categories:** Computer Vision and Pattern Recognition (cs.CV)

A frozen vision-language-action model (VLA) receives recent observations at every decision step, yet prior work has focused on adding memory rather than asking how existing history is represented and used. We study this temporal axis using layer-resolved linear probing and causal interchange interventions across three VLAs from two architecture families. We find a three-part dissociation. First, past-frame content remains linearly decodable throughout the network. Second, information unique to history beyond the current frame is nearly absent, indicating that stored history is largely a redundant copy of the present. Third, history is causally deployed only when the current frame is heavily degraded, while the action readout progressively loses dependence on history through the network. Although all models encode history similarly, their deployment strategies differ: under the same occlusion, one architecture increasingly relies on history as a fallback, whereas the other relies on it less. We further introduce a training-free temporal deployment audit that distinguishes these regimes. In the fallback regime, re-injecting history neither repairs occlusion nor disambiguates actions, confirming the redundancy of the stored representation. In the other regime, the same intervention reliably steers the predicted action toward the donor history. These results show that steerability depends on how history is deployed rather than whether it is encoded. VLAs do not forget the past; they largely fail to represent it as information distinct from the present. Our findings suggest that future memory augmentation should inject information unique to the past rather than simply more history.

---

## 38. UNIVERSE: Unified Video Action Models for Autonomous Driving with Flexible Mask-Modulated Modality Generation

**Authors:** Mengmeng Liu, Diankun Zhang, Jiuming Liu, ..., Hao Cheng, Michael Ying Yang
**arXiv:** [2607.05133](https://arxiv.org/abs/2607.05133)
**Categories:** Computer Vision and Pattern Recognition (cs.CV)

World Action Models (WAMs) have shown strong potential for improving action generalization in autonomous driving by using future video prediction as dense supervision for scene dynamics and temporal causality. However, it remains unclear which architecture better transfers video-modeling benefits to trajectory generation. Existing cascaded or dual-DiT designs separate video imagination from action prediction, weakening the transfer of video-learned world dynamics to the trajectory branch: the action model may still overfit dataset-specific driving priors, while the video model only indirectly regularizes planning. We propose UNIVERSE, a unified video-action model built upon a single mask-modulated Diffusion Transformer. By co-training future video latents and ego-trajectory tokens within shared generative parameters, UNIVERSE allows dense video supervision to directly shape trajectory denoising, leading to stronger cross-domain action generalization. To ensure causal validity and efficient deployment, we introduce a Modality-Decoupling Visibility Mask, which shares historical context across modalities while blocking mutual attention between future video and trajectory tokens. This prevents future-target leakage and enables trajectory-only inference by removing future-video denoising at test time, achieving a $4.3\times$ speedup over joint video-action rollout while maintaining comparable planning accuracy. The same model also supports video-only and joint video-action rollouts. Experiments show that UNIVERSE achieves 91.0 PDMS on NAVSIM (vs. 89.6 for the Two-DiT variant), and demonstrates strong zero-shot transfer to nuScenes and Bench2Drive without fine-tuning, while ablations confirm the importance of single-DiT unification, video co-training, and mask-based modality decoupling.

---
