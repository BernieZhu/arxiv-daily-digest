# arXiv Daily Digest — 2026-09-01

**Mode:** direct
**Categories:** cs.AI, cs.LG, cs.RO, cs.CV
**Keywords:** VLA, world model, world action model
**Papers found:** 23

---

## 1. CAER: Causal Action Effect Reweighting for World Model Training

**Authors:** Jianjie Fang, Xvyuan Liu, Ziyou Wang, ..., Xinlei Chen, Yong Li
**arXiv:** [2608.30897](https://arxiv.org/abs/2608.30897)
**Categories:** Artificial Intelligence (cs.AI)

World models are becoming core infrastructure for embodied intelligence, with action-conditioned video generation providing controllable predictions of how scenes evolve after agent interventions. Yet existing models are commonly trained with space-time-uniform mean squared error, allowing abundant background tokens to dominate the gradient while sparse interaction dynamics remain under-optimized; such uniform fitting rewards reconstructing appearance rather than learning how actions change the world. We introduce Causal Action Effect Reweighting (CAER), a general training paradigm that redistributes supervision toward the tokens whose predicted future is causally affected by the action. CAER contrasts the model's own predictions with and without action conditioning to localize these tokens online, then normalizes the resulting effect map into a weight that preserves the total coefficient mass and changes only where it is spent. This online signal requires no external annotations or offline preprocessing, avoids additional data-processing time, and scales naturally with model and dataset size. Experiments across heterogeneous action-conditioned world-model tasks show that CAER converges to better solutions than uniform MSE training, with consistent improvements in the physical consistency, controllability, and visual quality of generated videos.

---

## 2. Motus2: A Self-Evolving General World Model for Dexterous Manipulation

**Authors:** Hongzhe Bi, Zihao Zhou, Yihang Tang, ..., Fan Bao, Jun Zhu
**arXiv:** [2608.30237](https://arxiv.org/abs/2608.30237)
**Categories:** Robotics (cs.RO); Artificial Intelligence (cs.AI); Computer Vision and Pattern Recognition (cs.CV); Machine Learning (cs.LG)

General embodied agents should perceive, predict, act, evaluate, and improve within a unified system. World models have shown great promise in building such agents, yet existing models typically append an action output head to a world simulator, without coupling them into a closed decision-and-learning loop for policy improvement. We present Motus2, a self-evolving general world model for dexterous manipulation. Motus2 advances world modeling through model scaling and data scaling. For model scaling, a single model with shared weights exposes three control interfaces: a policy (world-action model), a simulator (action-conditioned world model), and an evaluator (value model). The policy proposes candidate action chunks, the simulator predicts their visual consequences, and the evaluator assesses the predicted outcomes. Their coupling forms a closed decision-and-learning loop for policy improvement. This formulation uses curated expert demonstrations for action learning, while failed and suboptimal interactions provide valuable evidence for dynamics modeling and value learning. For data scaling, Motus2 progresses from large-scale monocular egocentric data to synchronized stereo egocentric data, followed by robot-domain adaptation with robot trajectories and supplementary human-robot alignment data. Motus2 further studies global-autoregressive and hybrid-memory extensions of its sliding-window context, adds tactile feedback for contact-aware control, and is instantiated on a fully biomimetic platform with stereo vision, dual arms, dual dexterous hands, and tactile sensing. Together, egocentric data scaling and closed-loop general world model scaling provide a general path toward self-evolving dexterous manipulation.

---

## 3. Aligning Multi-Trajectory Supervision with Policy Optimization for VLA Driving

**Authors:** Tian Zhang, Zhuo Huang, Hongrui Ye, ..., Zengmao Wang, Kaixuan Zhou
**arXiv:** [2608.30122](https://arxiv.org/abs/2608.30122)
**Categories:** Computer Vision and Pattern Recognition (cs.CV); Artificial Intelligence (cs.AI); Machine Learning (cs.LG)

Vision-language-action (VLA) driving methods increasingly combine multi-trajectory imitation learning with group-relative policy optimization (GRPO), making trajectory selection critical to final performance. However, some high-scoring trajectories that improve imitation can degrade subsequent GRPO by inducing advantage estimates misaligned with the current policy's feasible behavior distribution, driving updates away from safe and compliant behaviors. To address this, we propose a novel framework that aligns multi-trajectory supervision with policy optimization. To address the policy gradient bias induced by infeasible noisy trajectories outside the feasible region, augmented trajectories are constrained to a neighboring manifold of the ground-truth feasible region, and a Pareto-optimality criterion is adopted in place of the conventional aggregate score, retaining only non-dominated candidates and thereby filtering out conflicting samples at the source. To ensure that expanded trajectory supervision is effectively absorbed during policy optimization, we introduce two complementary mechanisms: feasibility-first advantage assignment and dynamic distillation. The former adapts Pareto credit to the feasibility composition of each rollout group and guides fully infeasible groups toward safe references. The latter updates teacher trajectories across refinement rounds to continually transfer useful supervision. Together, they progressively translate the benefits of expanded supervision into policy improvement. On NAVSIM v1 and v2, our method achieves 91.4 PDMS and 89.1 EPDMS, respectively, under single-trajectory inference, and recovers 440 of 658 initially failed scenes, 11.1\% higher than the original GRPO baseline.

---

## 4. How do World Models and Policies Compose in LLM Agents? A Joint Spectral and Behavioral Account

**Authors:** Ruize Xu, Xiao Yu, Yujin Tang, Chenming Shang, Nikhil Singh
**arXiv:** [2608.30067](https://arxiv.org/abs/2608.30067)
**Categories:** Machine Learning (cs.LG); Artificial Intelligence (cs.AI); Computation and Language (cs.CL)

How do LLM agents come to both understand environments they act in and master tasks set within them? Through controlled experiments combining world-model training (next-state prediction) and policy training (reward maximization), we investigate this question. We dissect the resulting models through their additive parameter updates. Geometrically, we find effective world-model updates are low-rank and share an input-feature subspace with policy updates while writing to nearly orthogonal output directions, whether trained separately or sequentially. However, we find that, in projection interventions, the sequential update induces more robustness than separate policy RL when removing the world model's leading input directions, suggesting that it has learned alternative input pathways. Behaviorally, we find the sequentially trained agent explores a wider range of states and actions. Based on this, we ask: does policy training preserve world knowledge as well as it could? We probe this with training-free merging built on the geometrically motivated input basis plus an online world-model loss during policy RL, and show both improve over the untreated baseline. Our findings suggest world knowledge and task-directed ability can be learned in geometrically complementary forms, and that future post-training pipelines should consider how best to engineer the interface between them.

---

## 5. Training-Free Action Correction for VLA Model Failures via Language Feedback

**Authors:** Owen Kwon, Pablo Ortega-Kral, Arthur Bucker, Jean Oh
**arXiv:** [2608.29967](https://arxiv.org/abs/2608.29967)
**Categories:** Robotics (cs.RO); Artificial Intelligence (cs.AI)

Vision-Language-Action (VLA) models demonstrate strong semantic understanding yet exhibit systematic failures during deployment. The conditions under which these failures occur, and whether they can be corrected without retraining, remain poorly understood. In this paper, we take steps toward addressing this gap. We present CorrectVLA, a framework that translates task-level natural language corrections into additive action magnitude adjustments without modifying policy weights. A human provides a single task-level correction, applied uniformly across all rollouts without per-episode intervention. In simulation, CorrectVLA recovers execution misalignment failures across both in-distribution and OOD tasks. In real-robot experiments on a UFactory xArm7 under environment shift, CorrectVLA restores near-perfect success where the base policy almost entirely breaks down, generalizing across object locations and identities. Through a taxonomy of failure modes on LIBERO-90, we find that execution misalignment failures, where the policy reaches the correct target but miscalibrates action magnitudes, represent the correctable subset, while other failure modes where semantic comprehension itself breaks down are not amenable to this approach. The approach succeeds when policies possess strategic correctness and fails when fundamental comprehension is absent, establishing a practical operational boundary for inference-time correction.

---

## 6. AGM: Achievement-Grounded Memory for Closed-Loop Agents with Frozen VLA Policies

**Authors:** Hongbo Gao, Zeyu Ni, Xin Wen, Siyu Xu, Ruifeng Li
**arXiv:** [2608.29537](https://arxiv.org/abs/2608.29537)
**Categories:** Robotics (cs.RO); Artificial Intelligence (cs.AI)

Frozen vision-language-action (VLA) policies offer broad manipulation skills but execute open-loop action chunks without tracking task progress, so the agent cannot reliably decide whether to continue, retry, or terminate. External memory is a natural remedy, yet it can be harmful when attempted actions are treated as completed progress, turning local execution errors into persistent task-state errors. We propose Achievement-Grounded Memory (AGM), a lightweight closed-loop framework for frozen VLA policies that represents a task as a subgoal sequence with a progress pointer and advances this memory only after the current subgoal is verified by physical evidence. Proprioceptive interaction cues decide when to verify, while coherent point tracking and language-conditioned cross-view comparison, sourced from frozen foundation models through a single 2.43M-parameter verification head, decide what was achieved. AGM thereby converts open-loop execution into a closed loop of execution, verification, and progress, keeping the policy frozen without test-time large-model inference. On the RoboMME Counting benchmark, AGM reaches on PickXTimes and on BinFill, surpassing the strongest memory-augmented baseline by points on average, and the framework yields equally decisive gains on a physical robot. Reliable embodied memory thus depends more on disciplined state updates than on memory capacity.

---

## 7. Does Latent Planning Survive Point Clouds? Action-Conditioned JEPA World Models for Geometric Observations

**Authors:** Fabio F. Oberweger, Michael Schwingshackl
**arXiv:** [2608.29434](https://arxiv.org/abs/2608.29434)
**Categories:** Machine Learning (cs.LG); Artificial Intelligence (cs.AI); Computer Vision and Pattern Recognition (cs.CV)

JEPA world models make latent-space planning a practical route to control, but they are built almost exclusively on images. Whether latent prediction survives geometric observations is unclear: point clouds are sparse, unordered, and self-occluded, and with 0.3-15% of scene points moving, the slow-feature optimum of latent prediction compounds with the geometric shortcut of 3D self-supervision. We lift three canonical JEPA designs to point clouds, frozen-encoder, distribution-prior, and action-sensitive, and re-sense the stable-worldmodel benchmark so that only the observation differs from the image baselines. All three plan without collapse: the distribution-prior model is statistically equivalent to its re-evaluated image counterpart on every benchmark, and the action-sensitive model attains the strongest result in our controlled comparison where the most geometry moves. Probing explains why: object positions are almost perfectly linearly decodable and attention falls on the few moving points. Planning withstands heavy dropout never seen in training, though range noise defeats the thinnest scene. Geometry finally makes a commanded 3D target a natural goal interface: we construct the goal latent from the target and the current latent, at no cost in success rate, without a goal observation.

---

## 8. Flow-JEPA: Flow Matching for Robust Latent Dynamics in JEPA World Models

**Authors:** Yanchen Huo, Ziying Song, Yadan Luo
**arXiv:** [2608.29029](https://arxiv.org/abs/2608.29029)
**Categories:** Machine Learning (cs.LG); Artificial Intelligence (cs.AI)

Joint-Embedding Predictive Architectures (JEPAs) have shown strong potential for learning compact predictive representations, and LeWorldModel (LeWM) extends this paradigm to reconstruction-free latent world modeling from pixels. However, its deterministic autoregressive predictor generates future states through repeated one-step transitions, which can accumulate errors and remain sensitive to task-irrelevant visual perturbations. In this work, we propose Flow-JEPA (F-JEPA), a conditional flow matching dynamics model that jointly generates a sequence of future latent states conditioned on the current observation and actions. A Gaussian distribution serves as the flow source, exposing the vector field to perturbed latent trajectories as it learns to transport them toward clean future representations. This formulation retains the reconstruction-free JEPA framework while replacing point-wise transition regression with stochastic trajectory-level prediction. F-JEPA raises mean success from $86\%$ to $92\%$ under clean observations and from $67\%$ to $86\%$ under noisy conditions, suggesting that conditional flow matching provides a promising alternative to deterministic autoregressive dynamics in JEPA world models.

---

## 9. RoboPhys-3D: A Comprehensive Embodied World Model Evaluation via 3D Reconstruction

**Authors:** Tianyi Wang, Jiazhou Chen, Yiming Xu, ..., Junfeng Jiao, Christian Claudel
**arXiv:** [2608.28718](https://arxiv.org/abs/2608.28718)
**Categories:** Robotics (cs.RO); Artificial Intelligence (cs.AI); Computer Vision and Pattern Recognition (cs.CV); Emerging Technologies (cs.ET); Systems and Control (eess.SY)

Video world models increasingly serve as data engines, action planners, and simulators for embodied AI, but conventional embodied world model (EWM) benchmarks lack a unified 3D-grounded protocol for establishing whether generated rollouts preserve the underlying 3D scene state or translate into executable actions. We introduce RoboPhys-3D, a 3D-grounded EWM benchmark built on RoboTwin 2.0, covering 50 manipulation tasks across four regimes, with 5,000 episodes and 25,000 multi-view ground-truth videos. A defining feature of RoboPhys-3D is that generated and ground-truth videos are processed through the same 3D reconstruction pipeline, enabling reconstruction-induced error to be distinguished from generation-induced error. The RoboPhys-3D benchmark organizes 50 complementary metrics into 18 sub-dimensions across four levels: pixel-level fidelity, 3D geometry consistency, state-level understanding, and task-level completeness. We further introduce Average Full Score, a hierarchical score averaging all 50 metrics for comprehensive evaluation, and RoboPhyscore, a compact task-aligned score averaging the metrics most strongly correlated with task success. Among the four representative video world models, Cosmos 3 achieves the highest RoboPhyscore (0.6330, 92.7% of ground truth), while state- and execution-grounded metrics reveal substantial failures that perceptual and vision-language model-based judgments fail to capture. RoboPhyscore further exhibits strong agreement with human evaluation (Pearson r = 0.9761 and Spearman \r{ho} = 0.8962), demonstrating the importance of grounded, execution-aware evaluation for EWM capability.

---

## 10. The Intervention Gap in Latent World Models

**Authors:** Donna Vakalis
**arXiv:** [2608.29998](https://arxiv.org/abs/2608.29998)
**Categories:** Machine Learning (cs.LG)

Planning-time intervention fidelity is a distinct, measurable property of a learned world model: whether the model's own open-loop transitions move task variables the way matched environment interventions do. In the settings we test, it is neither revealed by reward fit nor ensured by task-anchored training. Across released TD-MPC2 checkpoint sizes, episode return falls as an operator-error diagnostic on task observables grows, while reward-prediction error stays small and nearly flat, and a self-supervised world model trained without task signal preserves the same operator substantially better than a task-anchored model on the shared task. A capture-gated matched-intervention audit then localizes what fails. On Cheetah, three LeWorldModel checkpoints capture the current task query and support decodable real intervention effects; however, their imagined five-step effects are worse than predicting no effect and worse than an environment-endpoint oracle. The failure is task-direction rotation with excess gain, not feature collapse. This severe pattern is conditional: five PreJEPA seeds retain an oracle-relative deficit without it, Finger Spin experiments extend the deficit beyond locomotion with heterogeneous severity across seeds, and shared-bank effect geometry is both candidate- and support-dependent. We also test practice-side questions. In DreamerV3 the posterior distribution, not its sample, carries the current query; ensemble disagreement ranks error only near training support; and a frozen support-aware score degrades held-out error ranking in both tested transfer directions while native disagreement remains informative in both. We conclude that intervention fidelity must be audited directly, capture-first, on the model's native interface.

---

## 11. AdaVLA: Adaptive Step Flow Matching for Training-free Acceleration of Vision-Language-Action Models

**Authors:** Sunghwan Han, Youngtae Han, Youngmin Yi
**arXiv:** [2608.29208](https://arxiv.org/abs/2608.29208)
**Categories:** Robotics (cs.RO); Machine Learning (cs.LG)

Vision-Language-Action (VLA) models, built upon Vision-Language Models (VLMs), have significantly enhanced robotic capabilities by leveraging internet-scale knowledge and multimodal reasoning. However, the intensive computational overhead of VLAs constrains on-device deployment, hindering real-time responses to environmental changes. While various acceleration techniques have been proposed, they often rely on fine-tuning or access to training datasets, which are frequently unavailable due to privacy and proprietary concerns. Moreover, although flow-matching-based VLAs have emerged as efficient alternatives to standard diffusion models, current acceleration efforts largely target VLM inference costs, failing to address the iterative ODE solving process inherent in flow matching inference. To address these limitations, we propose AdaVLA, an online, training-free adaptive framework for fast yet accurate flow-matching-based Vision-Language-Action models. We introduce a novel metric derived from the flow matching trajectory curvature to quantify action generation confidence during inference. This metric enables the dynamic reduction of inference steps and the adaptive adjustment of MLP pruning ratios through an efficiently computed importance evaluation, requiring no access to training data. Experimental results on the LIBERO benchmark using a Jetson AGX Orin device demonstrate that our method achieves $1.87\times$ and $2.24\times$ speedups for $\pi_{0.5}$ and X-VLA, respectively, with negligible degradation in success rates. Furthermore, we validate the robustness of our approach on real-world robotic tasks using SmolVLA.

---

## 12. Temporal Forcing: 4D Representation Alignment for Vision-Language-Action Models

**Authors:** Xingyu Ding, Yuzhong Zhao, Chunhai Zhao, ..., Chaoyang Zhao, Yifan Zhang
**arXiv:** [2608.30643](https://arxiv.org/abs/2608.30643)
**Categories:** Robotics (cs.RO)

Recent vision-language-action (VLA) methods improve manipulation performance by aligning their representations with 3D scene geometry. However, these methods often struggle with long-horizon manipulation and observation aliasing between visually similar states due to a lack of temporal information: the 3D scene geometry captures only the current state, rather than how it has evolved over time. To resolve this, we present Temporal Forcing, a 4D representation alignment method for VLA models. Specifically, we first introduce a history pathway that enables a vanilla VLA model to summarize observation history into temporally aware latent representations. Then, the latent representations are aligned with the geometric features extracted by a pretrained 4D foundation model, which captures the evolving 3D world through temporally consistent geometric representations, enabling a deeper understanding of dynamic environments. Temporal Forcing reaches 98.8% on LIBERO, outperforming its base model by 2.2 points. On a physical hidden-placement task, it raises full-task success from 20.0% to 43.3%. Code will be publicly available.

---

## 13. Behavior-Skill: A Fine-Grained Benchmark for Evaluating Vision-Language-Action Policies in Long-Horizon Tasks

**Authors:** Chunyun Ma, Lun Luo, Xingjian Luo, ..., Huimin Lu, Xieyuanli Chen
**arXiv:** [2608.30536](https://arxiv.org/abs/2608.30536)
**Categories:** Robotics (cs.RO)

Reliable execution of long-horizon mobile manipulation tasks remains challenging because overall task success depends on the successful completion of multiple constituent skills. Existing benchmarks, however, still rely primarily on full-task rollouts and aggregate task-level metrics, making intermediate failures difficult to observe and analyze. We present Behavior-Skill, a benchmark that reformulates the learning and evaluation of long-horizon tasks around executable constituent skills. It contains 235,492 skill instances from 10,000 demonstrations across 50 household tasks and 34 semantic skill categories. Each instance pairs a skill instruction with an aligned observation-action segment, and is further associated with a restorable intermediate state and a skill success condition to enable independent evaluation under valid preconditions. We further introduce trajectory-level and skill-level metrics to characterize policy capability beyond aggregate task success. Extensive experiments across representative VLA policies including pi0.5 and GR00T on the complete 50-task benchmark show that failures are highly non-uniform across skills, with contact-rich manipulation skills forming persistent bottlenecks. These results demonstrate that Behavior-Skill complements full-task evaluation by exposing intermediate capability profiles for analyzing and improving long-horizon VLA policies. Behavior-Skill is publicly available at this https URL.

---

## 14. CometVLA: Co-Training on an Embodied Data Pyramid towards Physical Understanding

**Authors:** Hanwen Wan, Dafeng Chi, Linbo Zhai, ..., Liang Lin, Xiaoqiang Ji
**arXiv:** [2608.30289](https://arxiv.org/abs/2608.30289)
**Categories:** Robotics (cs.RO)

Vision-language-action (VLA) models remain brittle in manipulation tasks that require physical commonsense. Current physical VQA data is typically disembodied and misaligned with robot action domains. Egocentric videos are used only as auxiliary pre-training. It remains unclear whether improved VLM physical understanding actually benefits downstream action generation. Therefore, we present CometVLA to close this gap. We construct CometData and CometBench, an embodied physical VQA corpus and benchmark strictly aligned with the robot's action data and embodiment. We introduce Global Action Prior (GAP) tokens, a compact learnable bottleneck that isolates task-agnostic motion regularities and lets the action head consume physical commonsense without corrupting the pre-trained VLM backbone. We co-train CometVLA across the embodied data pyramid, spanning teleoperation, simulation, egocentric trajectories, and VQA layers. On real-world manipulation tasks and RoboTwin simulation, CometVLA consistently outperforms strong VLA baselines. Correlation analysis shows that stronger VLM performance on CometBench indicates higher VLA success rates. Results demonstrate that physical understanding pre-training genuinely benefits downstream manipulation.

---

## 15. Rethinking Language's Role in Efficient VLA for Autonomous Vehicles: Toward Smarter, Trustworthy Driving

**Authors:** Tongfei Guo, Lili Su
**arXiv:** [2608.30144](https://arxiv.org/abs/2608.30144)
**Categories:** Robotics (cs.RO)

Vision-Language-Action (VLA) models are reshaping autonomous driving (AD) by unifying perception, reasoning, and control through language, enabling semantic grounding, interpretable decisions, and better long-tail generalization. But language is expensive onboard: latency and memory budgets are tight, and autoregressive decoding is inherently sequential. This work reframes the central question as when and where language should act at inference, since inference cost recurs at every deployed frame while training cost is paid once. We introduce the Language Residue taxonomy to organize methods by their inference-time use of language: train-time-only supervision (L1), latent non-textual reasoning (L2), conditional invocation (L3), and full per-frame generation (L4). We review representative methods and tag each across five deployment axes (latency, parameters, memory, FLOPs, tokens), analyzing them on major open- and closed-loop driving benchmarks (e.g., nuScenes, NAVSIM, Bench2Drive). We further trace how efficient methods from NLP/LLM are adapted in AD, identifying the constraints and motivations driving these adaptations. A continuously updated repository will be available at Github.

---

## 16. DriftingVLA: Native One-Step Vision-Language-Action Generation via Per-Dimension Temporal Drifting

**Authors:** Yuxuan Gao, Shiqi Zhang, Yedong Shen, ..., Jiajun Deng, Yanyong Zhang
**arXiv:** [2608.29749](https://arxiv.org/abs/2608.29749)
**Categories:** Robotics (cs.RO)

Conventional flow-based vision-language-action (VLA) models support expressive continuous action generation but rely on multi-step refinement to produce each action chunk, increasing latency in online robot control. To address this issue, we introduce DriftingVLA, a native one-step VLA that generates a complete action chunk with a single action-expert forward pass. Rather than learning a flow field that requires iterative integration at inference, DriftingVLA uses a distribution-drifting objective to learn a direct noise-to-action-chunk mapping for one-step deployment. Since robot action dimensions carry distinct control semantics and distributional characteristics, we further introduce Per-Dimension Temporal Drifting (PDTD). PDTD treats the complete temporal trajectory of each action dimension as a separate drifting unit, enabling finer-grained modeling and shaping of dimension-specific action distributions. This per-dimension decomposition applies only to the training objective; the shared VLA model still generates the complete action chunk jointly, thereby preserving cross-dimensional dependencies. DriftingVLA achieves 98.32% success on LIBERO, 81.09% on RoboTwin 2.0, and 77.67% across six real-world single- and dual-arm tasks, outperforming the evaluated multi-step flow policy and one-step VLA baselines. Native one-step deployment also delivers a 3.36-fold speedup in action-chunk generation, eliminating iterative refinement without sacrificing control performance.

---

## 17. SMILE: Smooth Motion for Improved Long-Horizon VLA Execution

**Authors:** Jongwoo Park, E-Ro Nguyen, Kanchana Ranasinghe, ..., Xiang Li, Michael S Ryoo
**arXiv:** [2608.29432](https://arxiv.org/abs/2608.29432)
**Categories:** Robotics (cs.RO)

Vision-Language-Action (VLA) models reduce inference cost by executing multiple actions per call, but longer horizons often degrade accuracy because raw chunks contain jitter and outliers. We introduce SMILE, an architecture-preserving interface that predicts B-spline coefficients and decodes them into smooth action sequences. SMILE changes only the action representation, enabling longer fixed horizons while retaining each baseline's backbone and model scale. We apply SMILE to SmolVLA, Evo1, VPP, and DAWN, improving accuracy and amortized inference efficiency across LIBERO, CALVIN, and real-world experiments. SMILE-Evo1 reaches 98.0% with a 1.1x speedup on LIBERO, while SMILE-VPP reaches an average length of 4.42 with a 1.5x speedup on CALVIN. At a matched execution horizon of 10, SMILE-SmolVLA reduces non-boundary acceleration by 78.6% and velocity sign-change rate by 42.3%. Real-world xArm tests show higher success, fewer drops, and fewer contacts. These results establish smooth coefficient-space generation as a route to accurate, efficient long-horizon VLA execution. Project page: this http URL

---

## 18. AnyWorld: Factorized Egocentric World Models for Cross-Embodiment Generalization

**Authors:** Cheng Chen, Jerry Bai, Jiacheng Wei, ..., Guosheng Lin, Fayao Liu
**arXiv:** [2608.29242](https://arxiv.org/abs/2608.29242)
**Categories:** Robotics (cs.RO)

Collecting contact-rich robot experiences at scale remains a major bottleneck for generalizable manipulation. Beyond data quantity, robot learning also requires diverse experiences across embodiments, viewpoints, and scenes. Human egocentric videos provide abundant physical interactions, but each video captures only a narrow slice of experience under a single body, camera trajectory, and environment. We propose AnyWorld, a cross-embodiment world modeling framework that expands a single human interaction into diverse robot-native rollouts without paired human-robot demonstrations. Our model factorizes an interaction into action, camera, and embodiment: action controls capture the motion structure, camera controls specify viewpoint evolution, and the target embodiment context defines the acting body and its interaction geometry. This formulation enables independent recomposition of embodiment, viewpoint, and scene factors, allowing a single model to generate many robot-domain experiences while preserving the underlying dynamics and object interactions. We train the model with large-scale human interaction pretraining followed by mixed-embodiment fine-tuning. Experiments show that our model supports controllable recomposition across embodiments, viewpoints, and scenes, and we further demonstrate that the generated data can improve manipulation performance on the RoboCasa GR1 tabletop benchmark and a real IRON humanoid robot. Beyond aggregate gains, we test whether unpaired human experience can be recomposed into robot-native video-action pairs that target a policy gap. Controlled IRON interventions correct a spurious completion prior and establish language-grounded spatial target selection; an action-only counterfactual intervention fails to learn the latter reliably, showing that both action calibration and visual recomposition are necessary.

---

## 19. Hydra: A Navigation World Action Model with Discrete Latent Planning and Continuous Flow-Matching Execution

**Authors:** Mohammad Nazeri, Alexandyr Card, Samira Huber, ..., Sören Pirk, Xuesu Xiao
**arXiv:** [2608.28995](https://arxiv.org/abs/2608.28995)
**Categories:** Robotics (cs.RO); Computer Vision and Pattern Recognition (cs.CV)

World models let robots imagine possible futures, but exploiting this capability for real-time control is bottlenecked by a representation misalignment: the generative model and the planner operate on decoupled manifolds, so the planner has no shared structure to search over and must instead decode every candidate back into high-dimensional pixel space to evaluate it. This decoding step is a major obstacle to real-time control on physical hardware. In this paper, we present Hydra, a discrete World Action Model that closes this gap by moving the planner, both the sampler and the evaluator, inside the model. Hydra establishes a unified latent manifold over visual states, physical poses, and control actions, then compresses this manifold through modality-specific Vector-Quantized bottlenecks into discrete vocabularies of kinodynamic intents and visual states. Because candidates are now drawn directly from this shared manifold, sampling is informed by the model's own understanding of the observation rather than proposed blind, and evaluation happens natively within the discrete space: candidates are ranked by a Kinematic-Perceptual Cost, without ever decoding to pixels. We term this Discrete Latent Planning (DLP). Because planning over discrete intents alone cannot supply the smooth, continuous commands physical actuation requires, Hydra pairs DLP with conditional Flow Matching, which maps each selected intent to a continuous trajectory for execution. Evaluated on two physical robotic platforms, Hydra outperforms state-of-the-art world models in goal-directed planning, while matching or exceeding the closed-loop execution capabilities of leading reactive foundation policies.

---

## 20. RedLight-VLA: Models for traffic-rule grounding and behavioral emphasis in driving policies

**Authors:** Bala Murali Manoghar Sai Sudhakar, Sourab Bapu Sridhar, Sandipan Das, ..., Pratik Likhar, Senthil Yogamani
**arXiv:** [2608.28656](https://arxiv.org/abs/2608.28656)
**Categories:** Robotics (cs.RO); Computer Vision and Pattern Recognition (cs.CV)

Behavior-cloned Vision-Language-Action (VLA) driving policies struggle with rare rule-governed maneuvers at signalized intersections. Braking and launching examples contribute little to averaged trajectory loss, while fused representations lack explicit supervision for the governing traffic-light and stop-line state. We present RedLight-VLA, a training objective that uses expert futures and automatically generated perception targets without additional manual rule annotation. First, trajectory-derived behavioral reweighting (BR) emphasizes rare deceleration and acceleration using rotation-invariant longitudinal dynamics and a scale-preserving reduction that exactly recovers the baseline when disabled. Second, parallel auxiliary (AUX) heads ground traffic-light and stop-line state in continuous post-fusion rule tokens, without autoregressive language generation or changes to the trajectory decoder. We evaluate on a curated set of 20 s sequences with a 5 s prediction horizon. Controlled variants share the same backbone, training data, decoder, and evaluation population. Against an otherwise identical VLA baseline, RedLight-VLA reduces red-light stop-line overshoot from 7.3% to6.8%, reduces stop-line velocity error by 12.7%, and improves 3 s trafficlight-sliced ADE/FDE from 0.274/0.964 m to 0.247/0.897 m. Green-light false stops increase from 3.2% to 3.9%; however, combining BR with AUX supervision mitigates the larger increase observed for AUX alone (4.0%). The combined model also improves non-traffic-light ADE/FDE from 0.268/0.956 m to 0.241/0.876 m and outperforms either mechanism alone on all four sliced displacement measures.

---

## 21. Can Video World Models Track Unobserved World States?

**Authors:** Joonghyuk Shin, Yicong Hong, Jaesik Park, Xun Huang
**arXiv:** [2608.30692](https://arxiv.org/abs/2608.30692)
**Categories:** Computer Vision and Pattern Recognition (cs.CV)

Video world models are increasingly used as simulators, yet visual fidelity alone does not show that a model maintains the hidden state of the world. We examine this gap with an action-conditioned video Shell Game, a visual analog of $S_5$ state tracking that decouples visual rendering from compositing the hidden state underneath. Bidirectional and autoregressive Transformers, Mamba, and linear attention restricted to nonnegative transition eigenvalues all fit the training horizon of 5 swaps and then fall toward chance on longer swap chains (extrapolation) while still rendering plausible video with additional denoising steps providing no benefit. The pixel-based diffusion target never supervises the unseen hidden state, so the generated frames cannot carry it and the state has to live inside the architecture rather than in the tokens. For a Transformer, that architectural state is only an append-only KV cache, so the model has to re-derive the hidden arrangement from the whole history at every chunk. We find two mechanisms that do extrapolate, and both carry a state across chunks and revise it in place. Linear attention succeeds once its transition eigenvalues may be negative, and TTT with a nonlinear fast weight succeeds by updating the feature map through which it reads its own state. We further examine harder cases in dynamic world exploration tasks, and discuss the broader implications for building stateful video world models.

---

## 22. Matrix-Game 3.5: Enhancing Real-Time Streaming Interactive World Models with Patch Memory

**Authors:** Runjia Qian, Zile Wang, Jihai Zhang, ..., Yang Liu, Yangguang Li
**arXiv:** [2608.29910](https://arxiv.org/abs/2608.29910)
**Categories:** Computer Vision and Pattern Recognition (cs.CV)

Interactive world models extend video generation from offline clip synthesis toward persistent simulation of interactive virtual worlds, enabling applications in games, robotics, embodied agents, and XR. Achieving stable long-horizon interactive generation, however, remains challenging, as the model must simultaneously preserve scene geometry, dynamic consistency, and camera control while supporting real-time autoregressive generation. Building upon Matrix-Game 3.0, we present Matrix-Game 3.5, as shown in Figure 1, which advances real-time interactive world generation toward geometry-aware and long-horizon consistent simulation through three key improvements. First, we propose a unified geometry-aware memory framework, whose patch-memory and tiled-PRoPE components introduce no additional learnable parameters, combining explicit 3D patch retrieval with projective camera conditioning to enable geometry-consistent camera control and faithful long-horizon scene recall. Second, we introduce a static-dynamic disentangled world representation that separately models static scene geometry and dynamic subjects, preserving both geometric consistency and subject identity throughout long-horizon generation. Third, we develop a two-stage progressive real-time distillation framework that converts a bidirectional diffusion model into a few-step causal generator through Perceptual Flow Matching and curriculum based Self-Rollout DMD, enabling minute-long real-time interactive generation. Extensive experiments demonstrate that, with a unified training corpus spanning Unreal simulation environments, open-world games, and internet videos, MatrixGame 3.5 achieves strong performance in long-horizon scene recall, precise camera control, subject consistency, prompt-driven world generation, and stable real-time open-world interaction.

---

## 23. Off-Manifold Refinement: Guiding Video Generators with a Frozen World Model

**Authors:** Hai Nguyen-Truong, Tuan-Anh Vu, Dang Huynh
**arXiv:** [2608.29904](https://arxiv.org/abs/2608.29904)
**Categories:** Computer Vision and Pattern Recognition (cs.CV)

Modern video generators routinely fail at physical dynamics: objects float, trajectories violate gravity, contacts vanish. Standard denoising and flow-matching objectives fit visual data distributions but do not explicitly penalize such physical violations. Existing remedies can improve physical consistency, but typically add substantial inference or training cost. Candidate-selection methods generate and score multiple videos, while gradient-based world-model guidance repeatedly decodes and re-encodes intermediate estimates. Generator-internal refinement adds perturbation and re-denoising loops, whereas post-training requires curated data and additional optimization. We propose Off-Manifold Refinement (OMR), an inference-time method that instead injects world-model feedback directly into a single sampling trajectory. During scheduled middle ODE steps, we augment the generator velocity with the gradient of an adapter-space V-JEPA 2.1 surprise energy. This external correction can move the latent away from the uncorrected sampling trajectory and toward regions ranked as more physically plausible by the frozen predictor, after which the generator continues rendering from the corrected state. A small trained latent-to-embedding adapter keeps the gradient tractable at inference, and both the video generator and the world model remain frozen. On our fixed 400-prompt VideoPhy-2 detailed subset, OMR lifts the joint Semantic-Adherence-and-Physical-Commonsense metric from 47.0% to 52.0% (+5.0pp absolute, +10.6% relative) over the base Wan2.2-T2V-A14B sampler. On a separate fixed 50-prompt efficiency subset, it requires $1.71 \times$ the base runtime rather than the multiplicative cost of reward/search alternatives. Project page: this https URL.

---
