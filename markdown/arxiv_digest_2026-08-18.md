# arXiv Daily Digest — 2026-08-18

**Mode:** direct
**Categories:** cs.AI, cs.LG, cs.RO, cs.CV
**Keywords:** VLA, world model, world action model
**Papers found:** 24

---

## 1. FabriMAE I Trust Myself? Self-Evaluating VLA Action Generation with Markov Attention Entropy

**Authors:** Aniri, Chen Yilin, Jinhe Bi, ..., Tat-Seng Chua, Yunpu Ma
**arXiv:** [2608.16697](https://arxiv.org/abs/2608.16697)
**Categories:** Artificial Intelligence (cs.AI)

Vision-Language-Action models (VLAs) integrate visual perception, language instruction, and action generation into end-to-end policies across heterogeneous architectures. However, enabling VLAs to self-evaluate their action generation reliability without external supervision remains a major challenge. Existing methods either rely on expert annotations or estimate uncertainty only from output statistics, largely ignoring internal signals. In this work, we observe that internal visual modality entropy exhibits consistent distinctions between successful and failed tasks across heterogeneous VLAs. Although VLAs' architectures differ in their action generation, we show that they share a common latent action generation abstraction evolving under visual perception, language instruction, and state input, which we formulate as a Conditional Generative Markov Chain. Based on this formulation, we propose MAE (Markov Attention Entropy), a self-evaluation framework that directly converts internal attention signals into architecture-aware reliability scores, and introduce LIBERO-Reflect, a 4,000-episode benchmark combining 2,000 standard episodes and 2,000 challenging episodes across four subsets. Extensive experiments across heterogeneous VLA architectures and diverse scenarios show that MAE consistently outperforms state-of-the-art baselines on AUPR, AUROC, and FPR@95. We further instantiate FabriMAE for verifier-free test-time action selection, showing that MAE-guided multiple sampling improves PI-family robustness on LIBERO-Plus with small observed runtime overhead.

---

## 2. DriveCache: Action-Aware Caching for Driving World Model Inference

**Authors:** Jianchun Yang, Jian Liang, Xianda Guo, ..., Wenke Huang, Mang Ye
**arXiv:** [2608.16354](https://arxiv.org/abs/2608.16354)
**Categories:** Artificial Intelligence (cs.AI); Computer Vision and Pattern Recognition (cs.CV)

Driving video generation models support autonomous-driving development by predicting controllable future scenes for simulation, planning evaluation, and offline data generation. Diffusion-based driving generators repeatedly evaluate large backbones across denoising steps, which limits generation throughput. Existing diffusion acceleration methods reduce this cost, but general-purpose designs omit driving signals available before generation, such as ego speed and planned trajectories. Experiments across driving motions show that cache tolerance varies with ego translation and rotation, denoising progress, and consecutive reuse length. We propose DriveCache, a training-free, action-aware controller that uses planned motion to allocate reuse across scenes and dynamic programming to place it across denoising steps under a calibrated response budget. A causal drift check refreshes features and replans the remaining schedule when generation departs from calibration. Across three generator configurations, DriveCache improves the overall fidelity-efficiency trade-off over evaluated cache methods. Our code will be publicly available.

---

## 3. EcoVLA: Energy-Efficient Device-Edge Co-Inference for Vision-Language-Action Models under Real-Time Constraints

**Authors:** Ao Zhou, Bo Dai, Le Yu, ..., Chunming Hu, Jianlei Yang
**arXiv:** [2608.15502](https://arxiv.org/abs/2608.15502)
**Categories:** Artificial Intelligence (cs.AI); Robotics (cs.RO)

Vision-Language-Action (VLA) models have emerged as a promising foundation for Embodied AI, but their high inference cost poses significant challenges for deployment in robotic systems. In practice, on-device inference is constrained by limited compute capacity and energy budgets, struggling to simultaneously satisfy real-time control and energy efficiency requirements. Alternatively, offloading the inference workload to an edge server is susceptible to fluctuations in system conditions, introducing unpredictable latency risks. Device-edge co-inference offers a promising solution, but systematic research tailored to VLA models remains scarce, particularly a unified co-inference framework that jointly addresses real-time constraints and system-level energy efficiency. Thus, we propose EcoVLA, an adaptive device-edge co-inference framework for VLA models that maximizes system energy efficiency under real-time constraints. EcoVLA first introduces a unified stage-level abstraction over different VLA paradigms, establishing an architecture-agnostic co-inference design space. It then formulates a joint device-edge-network latency and energy prediction model to enable rapid runtime evaluation of candidate co-inference schemes. Building on this, EcoVLA continuously selects the energy-optimal scheme satisfying real-time constraints with millisecond-level overhead, adapting to runtime variations in network and system states. Furthermore, EcoVLA incorporates a lightweight transmission mechanism for inter-stage intermediate tensors to reduce the communication overhead incurred by cross-device collaboration. Experimental results across VLA models show that EcoVLA improves system energy efficiency by up to 236% over existing co-inference approaches under a 20 Hz action output frequency constraint, while consistently maintaining SLO satisfaction under dynamic network and edge workload conditions.

---

## 4. Physiological World Models for Human State Transitions

**Authors:** Chongyang Zhang, Rendong Wang, Hao Zheng, ..., Xiaolong Wei, Bin Chong
**arXiv:** [2608.15309](https://arxiv.org/abs/2608.15309)
**Categories:** Artificial Intelligence (cs.AI)

Continuous multimodal sensing now allows human physiology to be observed throughout daily life rather than only during occasional clinical visits. However, most health artificial intelligence systems are designed to recognize current states, estimate risks or analyse individual biomarkers. They do not directly model how physiological states change in response to real-world events, behaviours, contexts and interventions. Here we propose the Physiological World Model (PWM), an event-conditioned framework for learning these changes at the level of the whole person. We introduce the HumanState Transition Token, a structured, quality-scored unit that connects the physiological state before an event with the event or action, relevant context and intervention information, the physiological trajectory after the event, observed outcomes and data quality. We describe four capability levels, from state representation to bounded intervention planning, together with four data acquisition and validation protocols. We also propose six benchmark tasks covering HumanState representation, forecasting across multiple timescales, individualized response prediction, simulation of alternative interventions, bounded planning and reliability under distribution shift. Together, this framework provides a practical path towards personalized health management, behavioural intervention design and clinician-supervised decision support, while clearly separating prediction from causal inference and making uncertainty, safety, governance and limits of use explicit.

---

## 5. SCOPE: Score-Isolated Agentic Optimization for Video World Models

**Authors:** Yuhua Jiang, Jiaming Wang, Qingbin Liu, Feifei Gao
**arXiv:** [2608.15043](https://arxiv.org/abs/2608.15043)
**Categories:** Artificial Intelligence (cs.AI)

Video world models are increasingly used as simulators for planning and embodied decision making, yet improving them at inference time introduces a subtle evaluation problem: prompts, samplers, verifiers, and selectors may evolve together, making it difficult to attribute gains or prevent held-out feedback from shaping the final policy. We introduce \scope (\emph{\scopefullname}), a framework for auditable inference-time adaptation of frozen video world models. \scope represents external controls as a typed state, updates this state only through bounded changes supported by development evidence, and freezes the resulting policy before held-out evaluation. On Physics-IQ benchmark, \scope improves over the exact frozen base by $+14.24$ (95\% CI $[+8.10,+21.23]$). Controlled ablations further identify gains from scene specification, sampling, and learned selection, while the margin over the strongest matched agentic baseline remains unresolved. Cross-backbone and prospective evaluations reveal a complementary result: useful inference-time updates exist, but their benefits do not transfer uniformly across models and settings. Together, these findings suggest that reliable inference-time adaptation requires not only better proposals, but also a principled mechanism for deciding which updates should become part of the deployed system. Code is available at this https URL.

---

## 6. HAF: Adapting Generalist VLAs to Humanoid Whole-Body Loco-manipulation via Hierarchical Action Flow and Spectral Latent RL

**Authors:** Langzhe Gu, Chengkai Hou, Meng Li, ..., Zhengping Che, Shanghang Zhang
**arXiv:** [2608.16837](https://arxiv.org/abs/2608.16837)
**Categories:** Robotics (cs.RO); Artificial Intelligence (cs.AI)

Humanoid robots hold great promise as general-purpose agents in human-centered environments, yet generalist vision-language-action (VLA) foundation models are not readily applicable to humanoid whole-body loco-manipulation. The high dimensionality and interdependence of humanoid motions make it challenging for conventional single-stage VLA architectures to coordinate locomotion, waist posture, and dual-arm manipulation effectively. Moreover, policies trained through offline behavior cloning can remain suboptimal during real-world deployment. Although online reinforcement learning can refine policies through real-world interaction, directly tuning large VLA backbones demands excessive computation and may introduce safety risks during real-robot exploration. To address these bottlenecks, we introduce HAF (Humanoid Adaptation Framework), a two-part framework consisting of HAF-VLA and HAF-Steer that transfers off-the-shelf generalist VLA foundation models to humanoid whole-body loco-manipulation. HAF-VLA is a hierarchical action-flow generator built on a pretrained flow-matching VLA. It splits full-body action denoising into three sequential stages with stage embeddings and cross-stage KV caches that retain kinematic dependencies, avoiding incoherent whole-body actions from one-shot generation. On top of the frozen HAF-VLA, HAF-Steer is a latent offline-to-online RL pipeline that leverages flow-matching invertibility and DCT-based dimensionality reduction to restrict RL optimization to a compact noise subspace and train a regularized SAC policy. This avoids updating the large VLA backbone and enables efficient real-world policy refinement. Evaluated on seven real-world humanoid loco-manipulation tasks, HAF surpasses vanilla single-stage VLA baselines and improves whole-body coordination and task performance. Project website: this https URL .

---

## 7. CaliBench: Are the Stochastic Dynamics of Video World Models Physically Calibrated?

**Authors:** Jonathan Sadeghi, Jenny Seidenschwarz, Jesse Allardice, ..., Benjamin Graham, Jeffrey Hawke
**arXiv:** [2608.16829](https://arxiv.org/abs/2608.16829)
**Categories:** Machine Learning (cs.LG); Artificial Intelligence (cs.AI)

Video world models approximate the stochastic distribution of physical outcomes through generative sampling, but existing benchmarks score individual generations or compare distributions coarsely over a whole dataset, leaving the fine-grained aleatoric uncertainty of specific phenomena untested. We introduce CaliBench, which scores outcomes in a physically interpretable discrete space - a bin index, a die face, a suit, a colour - rather than a learned feature space such as in FID, so the distance from a known reference distribution is measured directly. We curate outcome spaces whose reference is known in closed form (binomial Galton boards, Bernoulli forks, uniform dice/cards/lottery, a skewed European-roulette colour), enabling an exact calibration test. We decompose performance into two orthogonal axes that a single accuracy metric conflates: scorability, the fraction of generations yielding a scoreable outcome, and calibration, the total variation distance from the reference on that sample. A chi-squared test assesses significance; as calibration is its null hypothesis it can evidence only miscalibration, and at N=32 per cell detects only large deviations. We apply it to nine scenes and six image-to-video models (WAN-2.7, SeeDance-2.0, HappyHorse-1.0, Veo 3.1, Runway Gen-4.5, Cosmos3-Super), 32 generations each. Models consistently concentrate probability mass on a few outcomes rather than reproducing the reference. Most scene-model combinations are significantly miscalibrated, in the extreme collapsing to one outcome, as Veo 3.1 does on dice. On roulette, generations often leave the ball ambiguously placed, giving several models low scorability. Performance varies by scene: no model dominates all nine. We release the protocol and a metric (mean normalised total variation, mnTV) for comparing new models against our results.

---

## 8. Orbit-Planner: Towards Latent World Models for On-Orbit Obstacle Avoidance of Satellite Agents

**Authors:** Zhijian Li, Chao Ren, Peijin Wang, Xian Sun
**arXiv:** [2608.16651](https://arxiv.org/abs/2608.16651)
**Categories:** Robotics (cs.RO); Artificial Intelligence (cs.AI)

Satellite agents for on-orbit navigation tasks need to predict collision risks using limited onboard observations. However, conventional planners often rely on predefined maps and fixed environmental assumptions, limiting their adaptability in dynamic on-orbit scenarios. In this paper, we propose Orbit-Planner, a two-stage latent world model for on-orbit obstacle avoidance. Orbit-Planner learns action-conditioned spacecraft dynamics to perform future-state rollouts in latent space, and introduces a Physics Probe to decode physical state changes from imagined latent trajectories. Experiments demonstrate that Orbit-Planner can perform long-horizon latent rollouts and recover physical states from imagined trajectories. In closed-loop obstacle-avoidance navigation in Isaac Sim, it attains a success rate of 91.7%. Code is available at this https URL.

---

## 9. NebulaVLA: A Dual-Frequency Vision-Language-Action Model With Guide Action for Robotic Manipulation

**Authors:** Cong Zhao, Shuai Tian, Xu Zhang, ..., Jin Xu, Ri Yang
**arXiv:** [2608.16503](https://arxiv.org/abs/2608.16503)
**Categories:** Robotics (cs.RO); Artificial Intelligence (cs.AI)

Real-world deployment of Vision-Language-Action (VLA) models is often bottlenecked by efficiency-performance trade-offs, cross-embodiment generalization, and execution smoothness. We present NebulaVLA, an asynchronous dual-frequency architecture that decouples high-level semantic reasoning from low-level action control, optimizing computational resources and modularity. To bridge semantic gaps across heterogeneous robots, we introduce GESTURE-7, a unified language-grounded action representation. Furthermore, our Guide Action algorithm enforces kinematic continuity via mask-based smoothness constraints. Comprehensive evaluations demonstrate that NebulaVLA significantly outperforms synchronous baselines, achieving an 85.5\% average success rate on LIBERO-Plus and accelerating action generation by \textasciitilde 2.7$\times$. This asynchronous design enables highly efficient and responsive control for practical robotics.

---

## 10. Algorithm-Architecture Co-Design for Efficient VLA Inference via Speculative Inference and Verification

**Authors:** Chunyu Qi, Zhuoran Song, Jian Weng, ..., Xiaoyao Liang, Haibing Guan
**arXiv:** [2608.15636](https://arxiv.org/abs/2608.15636)
**Categories:** Robotics (cs.RO); Artificial Intelligence (cs.AI)

Vision-Language-Action (VLA) models have demonstrated remarkable capabilities in the field of embodied AI, but their high computational cost and limited predicted action length hinder real-time deployment. Although Dadu-Corki, a dedicated accelerator for efficient embodied AI, has been introduced, it does not exploit the inherent interaction patterns between the robot and its environment, which results in a relatively short predicted action length. We observe that robotic environments naturally alternate between active states-where precise actions are crucial-and inactive states-where actions have limited impact on task success. This insight enables a new scheduling opportunity: long-action-length speculative prediction in inactive states, paired with selective verification in active states.
We propose SpecVLA, an algorithm-system co-design framework that adaptively balances action length, inference latency, and task reliability. On the algorithm side, SpecVLA introduces a state-aware VLA inference execution paradigm and a hardware-friendly construction of a smaller verification model (sVLA) using differential residuals and block-wise mixed-precision quantization. On the system side, we develop a heterogeneous architecture consisting of a GPU and a robotic-specific hardware module, along with a speculative dataflow that decouples VLA and sVLA through parallel execution. Comprehensive evaluations on OpenVLA and RDT across LIBERO and ManiSkill benchmarks show that SpecVLA reduces end-to-end latency significantly while preserving task success rate. By enabling long-action-length speculative prediction with timely verification, SpecVLA achieves real-time robotic manipulation with both high efficiency and reliability.

---

## 11. Bit-Flip Attacks on Vision-Language-Action Models: Action-Decoding Architecture Shapes the Vulnerability

**Authors:** Yudong Gao, Linghan Chen, Wenhan Wu, ..., Mingyu Guo, Honglong Chen
**arXiv:** [2608.15475](https://arxiv.org/abs/2608.15475)
**Categories:** Cryptography and Security (cs.CR); Artificial Intelligence (cs.AI)

Quantized Vision-Language-Action (VLA) models expose a weight-fault surface: Rowhammer-style faults can corrupt deployed INT8 bits. We present the first bit-flip attack on a VLA: a few gradient-selected flips reduce closed-loop success to $0\%$, while hundreds of random flips are harmless. Across four model variants spanning three action-head families, damaging bits concentrate in a few action-generating layers, but the empirical budget depends sharply on the head: direct regression and token policies fall in $1$--$5$ flips, whereas the evaluated flow-matching policies require ${\sim}100$--$300$. Our fixed-direction manifold-escape loss cuts \pizero{}'s budget from ${\sim}1000$ to ${\sim}100$ flips, and a matched five-direction sweep shows that the attack is not specific to an all-positive direction. On a direct head, protecting $3.1\%$ of weights preserves $60\%$ success at $K{=}100$, and protecting $5.3\%$ moves the open-loop break threshold from 3 to 100 flips. Finally, task-calibrated emulated $K{=}100$ flips yield $0/20$ real-robot successes, versus $14/20$ clean and $16/20$ global-random. Weight integrity is therefore a security boundary for embodied foundation models. Code is included as ancillary material.

---

## 12. PhaseLoRA: Control-Regime-Conditioned Low-Rank Adaptation for Continuous-Action Vision-Language-Action Policies

**Authors:** Yufei Guo, Yinan Wu, Haoran Duan, Guiguang Ding, Jungong Han
**arXiv:** [2608.15285](https://arxiv.org/abs/2608.15285)
**Categories:** Robotics (cs.RO); Artificial Intelligence (cs.AI)

Parameter-efficient fine-tuning (PEFT) is a natural way to adapt pretrained vision-language-action (VLA) policies, but most adapter designs apply temporally static updates throughout a control rollout, overlooking the phase-dependent nature of continuous-action manipulation. Such policies traverse distinct regimes, including approach, contact transition, grasping, transport, and placement, each requiring different adaptation behaviors. We propose \textbf{PhaseLoRA}, a lightweight LoRA parameterization that conditions adaptation at each action-chunk prediction step using two weakly supervised descriptors: fine-control tendency and event/boundary intensity. PhaseLoRA modulates the LoRA left factor in the action expert, allowing the effective low-rank update direction to vary over time while keeping the backbone largely frozen. On LIBERO, PhaseLoRA improves average success rate by 12.2 points over a matched-parameter high-rank LoRA baseline and outperforms stronger LoRA variants. Ablations show that random temporal modulation and scalar gating do not reproduce the performance of the full model, while update-direction analyses reveal structured temporal variation associated with the predicted control descriptors. These results establish within-trajectory conditioning as an effective lightweight PEFT axis for continuous-action VLA policies.

---

## 13. Low-Rank Dynamics-Effective Latent Carriers for Counterfactual Rollout in Learned World Models

**Authors:** Yang Liu, Yuming Chen
**arXiv:** [2608.15156](https://arxiv.org/abs/2608.15156)
**Categories:** Robotics (cs.RO); Artificial Intelligence (cs.AI)

World models may predict the future without making clear which parts of their hidden state actually drive those predictions. We ask whether a small, directly addressable hidden-state change can place a learned world model on the intended counterfactual trajectory and then let the model continue that future on its own. We study a recurrent world model with a 192-dimensional hidden state in a controlled two-object, two-dimensional collision environment. For a bounded family of local velocity edits, we first verify that the model can natively represent and roll out the edited future. We then construct candidate low-rank carriers from training-only factual-to-counterfactual hidden differences and learn a map from the factual state and requested edit to carrier coefficients. On the registered rank grid, rank 4 is the smallest tested rank that satisfies the full development-panel criteria. A single rank-4 patch at the anchor is sufficient to redirect a 12-step autonomous rollout, with no future observations, teacher forcing, or repeated correction. The frozen procedure satisfies the preregistered replication rule across independently trained checkpoints and remains usable across nearby intervention times. Random equal-norm, wrong-object, and wrong-time controls do not explain the effect. A position-edit stress test provides a negative contrast: the intended position patch can pass the raw rollout criteria, but no-patch and random controls can pass the same criteria, and wrong-object specificity is not established. Thus, successful editing alone is not enough. We use dynamics-effective to describe an intervention that changes the model's future computation in a sustained and target-specific way under autonomous rollout. The rank-4 result identifies a compact intervention interface for the tested velocity-edit family, not a closed four-dimensional state or an intrinsic state dimension.

---

## 14. Efficient Block-Layer Parallel Inference for Vision-Language-Action on Hybrid Architectures

**Authors:** Haibo HU, Lianming Huang, Qiao Li, Nan Guan, Chun Jason Xue
**arXiv:** [2608.14586](https://arxiv.org/abs/2608.14586)
**Categories:** Distributed, Parallel, and Cluster Computing (cs.DC); Artificial Intelligence (cs.AI)

Vision-Language-Action (VLA) models are becoming a promising paradigm for autonomous driving, but their deployment on existing vehicle platforms remains difficult because they introduce both high inference latency and strong GPU-side resource pressure. In a full autonomous driving stack, this problem is even more pronounced: legacy vehicle platforms were provisioned for modular pipelines, yet after several planning-related functions are absorbed into a unified VLA model, part of the original CPU budget becomes underutilized, while the visual encoder and the main reasoning path still concentrate most computation and memory demand on the GPU. As a result, directly deploying VLA together with the rest of the onboard system can be hard under realistic GPU memory constraints. To address this issue, we present a hybrid CPU--GPU inference framework with flexible resource scheduling for autonomous driving. Our design partitions the VLA backbone at the block-layer granularity, executes the visual encoder and LLM prefix on the GPU, and offloads the LLM suffix to the CPU through a cross-frame asynchronous pipeline, thereby exposing a schedulable boundary for redistributing compute and memory pressure across heterogeneous processors. We evaluate the proposed framework on two representative driving VLA models, Orion and MindDrive. On Bench2Drive, our method reduces average latency from 521ms to 408.0ms for Orion and from 443ms to 306.2ms for MindDrive, corresponding to 21.7% and 30.9% reduction, respectively. For Orion, the estimated peak GPU memory is further reduced from 45GB to 29GB. In real-vehicle deployment under coexistence with this http URL, native Orion cannot run because the onboard GPU memory budget is insufficient, whereas the hybrid version runs successfully together with the full vehicle stack.

---

## 15. Paired Exact-Reset Evaluation of a Prediction-Derived Medium-to-Full World-Model Cascade

**Authors:** Malo de Pastor
**arXiv:** [2608.14650](https://arxiv.org/abs/2608.14650)
**Categories:** Machine Learning (cs.LG); Robotics (cs.RO)

Existing adaptive-inference and world-action-model systems use cheap-stage outputs or predicted futures to allocate additional computation. We study a narrower question: under paired exact-reset physical outcomes, can a Medium-derived interface predict when switching to a separately frozen Full predictor improves task-specific decision loss enough to justify sequential overhead? Our contribution is a paired evaluation and audit protocol, not a new generic routing rule: all candidate actions are executed from the same reset state, Medium and Full act on the same candidate set and task, and their paired physical-loss difference defines the routing target. On a fresh PushT bank (V106; 1,600 states, 39 tasks, three checkpoint pairs), a frozen prediction-interface router lowers overhead-inclusive decision cost relative to standalone Medium, standalone Full, and a latency-advantaged task-only router. We then prospectively seal a second 1,600-state PushT confirmation (V107) against a stronger current-state control using the task, a dimension-matched projection of current DINO features, and all five candidate actions, with no DINO encoder latency charged. The prediction interface lowers priced physical decision cost by 0.002549 (state-clustered 95% interval [-0.002867, -0.002238]; one-sided 95% upper bound -0.002286), with negative effects for all three checkpoint pairs. A controlled-PyBullet audit independently supports a composite task-prediction-regime router. The sequential router remains slower than fixed policies, and its advantage is restricted to low compute prices. The evidence supports incremental routing information in the tested prediction interface beyond one deliberately favoured current-DINO control, but not causal sufficiency, compute saving, closed-loop value, or cross-family generality.

---

## 16. $τ_0$-VLA: a Hierarchical Robot Foundation Model with World-Model-Guided Test-Time Computation

**Authors:** Xiaowei Cai, Yunuo Cai, Bingao Chen, ..., Pengfei Zhou, Yue Zhou
**arXiv:** [2608.16885](https://arxiv.org/abs/2608.16885)
**Categories:** Robotics (cs.RO)

Long-horizon robot manipulation requires a robot to both execute individual skills reliably and sequence them coherently over extended tasks. Most hierarchical vision-language-action (VLA) models make each such decision with a single forward pass, leaving no mechanism to allocate additional computation to difficult or consequential choices. We introduce $\tau_0$-VLA, a hierarchical robot foundation model that formulates high-level subtask generation as a compute-scalable inference problem through world-model-guided test-time computation. At each inference step, the high-level policy uses execution memory to generate a subtask and, when needed, searches over alternatives before committing to its output. A low-level policy then executes the generated subtask across multiple robot embodiments. The policy is trained on 40,115 hours of heterogeneous real-world data with multimodal co-training. Across in-domain and distribution-shifted settings, allocating additional test-time computation substantially improves next-subtask prediction accuracy, and these gains translate into higher closed-loop success on long-horizon robot manipulation tasks.

---

## 17. SparkVLA: Stop-Aware Hierarchical VLA with Adaptive Action Chunking for Long-Horizon Manipulation

**Authors:** Xunyao Lei, Renjun Wu, Tianlin Huo, Xuesong Li
**arXiv:** [2608.16172](https://arxiv.org/abs/2608.16172)
**Categories:** Robotics (cs.RO)

At every re-observation point in a hierarchical Vision-Language-Action (VLA) system, two interface decisions must be made: when to terminate the current subtask and how far to execute the proposed action chunk. These decisions are mutually dependent---the optimal stopping point depends on what the executor plans to do, while the optimal execution length depends on where the subtask boundary lies---yet existing architectures evaluate them in isolation, an asymmetry neither module can overcome alone. We present SparkVLA, a stop-aware hierarchical VLA that resolves this mutual dependency by formulating both decisions as a single ranking: Stop competes against every action-prefix length in a unified candidate set, and the system selects the highest-scoring option, eliminating threshold tuning and requiring only offline ordinal preferences. An Anchor-Conditioned Context Encoding module caches a history-aware subtask anchor encoding onset-state memory and goal semantics, guiding visual-token pruning toward task-relevant regions; a Stop-Aware Action-Prefix Selection head scores all candidates via full self bnattention at chunk boundaries for efficiency. On RoboCerebra, SparkVLA achieves 47.12% success rate, surpassing the official hierarchical baseline by 30.57% and the strongest reproducible method by 26.83% Real-robot experiments on multi-step tasks further validate these gains on physical hardware.

---

## 18. US-VLA: An Ultrasound Vision-Language-Action Model for Embodied Abdomina

**Authors:** Cheng Zhang, Xingzheng Wu, Guihao Yan, ..., Mei Wu, Qing Cai
**arXiv:** [2608.16074](https://arxiv.org/abs/2608.16074)
**Categories:** Robotics (cs.RO); Computer Vision and Pattern Recognition (cs.CV)

Artificial intelligence-assisted ultrasound scanning enhances diagnostic reliability and efficiency by providing real-time guidance for standardized image acquisition and reducing operator dependence. However, existing reinforcement learning and learning-assisted ultrasound scanning methods typically rely on carefully designed reward functions or extensive interaction data, which limits their generalization ability and stability across different devices, patient populations, and complex clinical scenarios. To address these challenges, we propose an ultrasound vision-language-action model (US-VLA) for automated ultrasound scanning that explicitly encodes clinical semantic goals and generates sequential probe manipulation actions under real-time ultrasound feedback. In particular, we first design an ultrasound-aware expert fusion module to jointly integrate ultrasound observations with auxiliary contextual information, enabling semantic ultrasound feedback to effectively guide the scanning process. Then, we construct US-VLA-Data, a real-world dataset covering liver and kidney examinations, which includes five clinically defined standard planes and comprises 320 expert scanning trajectories with approximately 80,000 synchronized timesteps. Extensive experiments demonstrate that US-VLA achieves competitive performance in ultrasound probe manipulation tasks, indicating its effectiveness and promising generalization within the evaluated abdominal ultrasound setting. The source code is available at this https URL.

---

## 19. ViTaR: Visuo-Tactile Residual Adaptation for Foundation VLA Manipulation

**Authors:** Yi Wang, Renjun Wu, Jinyan Liu, Xuesong Li
**arXiv:** [2608.15816](https://arxiv.org/abs/2608.15816)
**Categories:** Robotics (cs.RO)

As Vision-Language-Action (VLA) models scale toward real-world deployment, contact-rich manipulation exposes a critical blind spot: these policies encode broad visual-semantic priors yet remain unaware of local contact events, producing identical actions whether contact is established, lost, or destabilized. Existing remedies either modify VLA internals, risking catastrophic forgetting, or demand online reinforcement under near-failure contact conditions. Both grant tactile unbounded influence over action generation, conflicting with the priors that make VLAs generalizable. We introduce ViTaR, which reframes tactile feedback from an action-generating perceptual input to an execution modulator that selects and scales bounded residual corrections atop a frozen VLA, preserving pretrained capabilities by construction. ViTaR decomposes adaptation into two stages: Effect-Guided Modeling determines whether and which correction is locally justified via outcome-grounded preference evidence, and Residual Action Modulation converts this evidence into a residual choice with continuously scaled gain from real-time visuotactile observations. On the UniVTAC benchmark spanning seven contact-rich tasks, ViTaR achieves 61.3% average success, a 30.6 percentage-point improvement over its frozen VLA base that also surpasses purpose-built tactile baselines. Physical-robot experiments confirm that bounded tactile modulation transfers to real sensor noise and dynamics.

---

## 20. StructRL: Structured Action-Space Exploration for Flow-Based VLAs

**Authors:** Jiarui Yang, Bin Zhu, Jingjing Chen, ..., Jianggang Zhu, Yu-Gang Jiang
**arXiv:** [2608.15139](https://arxiv.org/abs/2608.15139)
**Categories:** Robotics (cs.RO)

Flow-based Vision-Language-Action (VLA) models are now widely used for continuous robotic manipulation, and online reinforcement learning (RL) is emerging as a key technique for adapting them to new tasks. Existing RL methods typically inject stochasticity inside the denoising chain, often through isotropic or temporally independent noise. However, effective robot exploration calls for structured noise: temporally smooth and scaled differently across action groups. We show that simply switching the in-chain noise to a structured form does not suffice: noise added at an intermediate flow time can be weakened by the remaining denoising steps before execution, a phenomenon we call \emph{Structured Noise Dilution}. We propose \textbf{StructRL}, which avoids dilution by relocating policy stochasticity to the action space via three coupled choices: (i) a deterministic ODE decoder, (ii) structured noise injected directly in the action space, and (iii) last-step replay, where policy-gradient updates avoid assigning likelihoods to intermediate denoising states. This keeps structured exploration tied to the executed action while providing a tractable training signal for the flow decoder. Across three flow-based VLA models on multiple simulated manipulation benchmarks and two real-world tasks, StructRL improves exploration efficiency and OOD performance over prior in-chain baselines, demonstrating the effectiveness of structured action-space exploration for adapting flow-based VLA with RL. \textbf{Project page:} this https URL

---

## 21. ForceU-VLA: A Force-Aware Vision-Language-Action Model for Embodied Ultrasound Scanning

**Authors:** Xingzheng Wu, Cheng Zhang, Guihao Yan, ..., Zhi Liu, Qing Cai
**arXiv:** [2608.15009](https://arxiv.org/abs/2608.15009)
**Categories:** Robotics (cs.RO); Computer Vision and Pattern Recognition (cs.CV)

Embodied intelligent ultrasound scanning enables the automation and standardization of the ultrasound examination process by integrating perception, decision-making, and execution capabilities. However, existing methods suffer from loosely coupled modeling between force and ultrasound modalities and lack awareness of scanning stages, which limits their ability to capture dynamic probe-tissue interactions. To address these issues, we propose ForceU-VLA, a force-aware Vision-Language-Action model for autonomous embodied ultrasound scanning, which leverages force signals and ultrasound image feedback throughout the scanning process to enable accurate and high-quality ultrasound acquisition. Firstly, we propose a Force-Ultrasound Synergistic Fusion Module (FUSFM) that synergistically fuses ultrasound visual and force-feedback information to provide stable, reliable guidance for probe motion. Secondly, a Stage-Adaptive Modulation Mechanism (SAMM) is proposed to accommodate the task requirements across different scanning stages by adaptively modulating multimodal features to enhance their representation quality. Additionally, we introduce ForceU-VLA-Data, a real-world, force-aware embodied ultrasound dataset that integrates visual, force, and action signals, including data from two organs across five representative clinical scanning views, and comprising 450 expert-collected trajectories with approximately 100,000 synchronized multimodal frames. Extensive experimental results demonstrate that ForceU-VLA significantly improves contact stability and probe pressure regulation in embodied ultrasound scanning, thereby effectively enhancing task execution quality and overall system reliability. The source code is available at this https URL.

---

## 22. Evidence of Absence: Cross-Modal Abductive Risk Perception to Sustain World Models When Vision Fails

**Authors:** Cong Xu, Ravi Sankar
**arXiv:** [2608.14952](https://arxiv.org/abs/2608.14952)
**Categories:** Robotics (cs.RO); Computer Vision and Pattern Recognition (cs.CV); Signal Processing (eess.SP)

A structured world-state (entities, relations, context, and predictive cues) is designed to preserve prediction-critical content when perception degrades, but it presumes observations to populate it; when the primary visual modality is occluded or degraded, those observations may be missing. We address how to sustain the world model from a complementary modality by treating the absence of expected co-evidence as evidence of a hidden cause. The abductive framework is modality-agnostic; this article instantiates it acoustically. A microphone-array front-end estimates the bearing of engine and tire sources and extracts approach-rate evidence (Doppler when a stable tone exists, a broadband looming readout otherwise); the event "signature present, visual co-evidence absent" then triggers abductive inference of a hidden road user, emitting a calibrated risk advisory rather than a control command. Recoverability of the hidden state is analyzed as an identifiability question separating shared from modality-unique information, and cueing is cast as Neyman-Pearson detection under an explicit false-alarm budget. On real occluded-approach recordings at blind junctions, the method warns a mean 1.7 seconds before line-of-sight entry, matches the sustained-window variant of the published acoustic baseline's detection rate with 42% fewer false alarms, localizes to 3.4 degrees median once in view, is well calibrated (expected calibration error 0.034), and keeps hazard awareness above 0.87 under staged vision degradation that collapses a vision-only channel to 0.03. We also measure the method's limits: calibration transfers to an unseen junction almost losslessly, the signature classifier does not, and moving-ego noise is the binding deployment constraint.

---

## 23. Imagining Recovery: Inference-Time Counterfactual Realignment for Vision-Language-Action Models

**Authors:** Yanyan Zhang, Disheng Liu, Kai Ye, ..., Yu Yin, Vipin Chaudhary
**arXiv:** [2608.14822](https://arxiv.org/abs/2608.14822)
**Categories:** Robotics (cs.RO); Computer Vision and Pattern Recognition (cs.CV)

Vision-language-action (VLA) models have improved the flexibility and generality of robotic manipulation, yet they remain fragile to online disruptions, such as changes in task goal, scene configuration, or robot state. Existing recovery methods often require failure data, policy retraining, or external corrective agents, introducing additional data requirements and execution risks. We propose Counterfactual Realignment (CoRe), a training-free framework that recovers a frozen VLA at inference time without failure data. Upon detecting a deviation, CoRe imagines how the policy would continue toward the current goal from a recent viable state, using synthesized observations in place of physical execution, and then minimally realigns the robot and scene to rejoin this imagined continuation before returning control to the policy. Recovery is therefore planned without physical trial-and-error, preserves completed task progress, and handles both mid-episode instruction changes and physical perturbations in a unified manner. Extensive experiments across multiple simulators, VLA backbones, and real-world settings show that CoRe improves success rates by up to 85.0 percentage points to near-nominal levels while reducing physical restorations by 42.2%, without policy fine-tuning or failure-specific recovery training.

---

## 24. GaussianDWM++: Language-Grounded 3D Gaussian Driving World Model for Unified Scene Understanding, Editing, and Multi-Modal Generation

**Authors:** Tianchen Deng, Xuefeng Chen, Shuang Wu, ..., Jianfei Yang, Hesheng Wang
**arXiv:** [2608.16234](https://arxiv.org/abs/2608.16234)
**Categories:** Computer Vision and Pattern Recognition (cs.CV)

Driving World Models (DWMs) have recently advanced rapidly with generative models, yet most existing methods mainly focus on conditional scene generation and lack explicit 3D scene understanding, language-grounded reasoning, and controllable 4D editing capabilities. Moreover, commonly used point cloud, occupancy, or BEV representations make it difficult to achieve fine-grained alignment between textual information and the underlying 3D scene structure. To address these limitations, we propose a foundation-feature Gaussian driving world model that unifies scene understanding, language-grounded reasoning, controllable 4D editing, and multi-modal generation within a single framework. Specifically, we introduce a foundation-feature Gaussian tokenizer that directly distills Qwen/SigLIP visual-language features into 3D Gaussian primitives, building a compact open-vocabulary Gaussian semantic field. We further design a geometry-aware Gaussian adapter that combines importance-aware hierarchical selection with text-conditioned Perceiver-style cross-attention to aggregate dense Gaussian primitives into compact world tokens. To improve representation compatibility, we introduce a KL-based Gaussian--image distribution alignment objective that aligns Gaussian world tokens with foundation image tokens. Based on the aligned Gaussian representation, our framework further supports instruction-controllable scene editing, including weather-conditioned generation and dynamic vehicle manipulation. Extensive experiments on broader driving benchmarks demonstrate that our method achieves state-of-the-art performance across scene understanding, visual grounding, planning-oriented reasoning, and controllable 4D generation tasks. We will release the code and datasets publicly on Github.

---
