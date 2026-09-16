# arXiv Daily Digest — 2026-09-15

**Mode:** direct
**Categories:** cs.AI, cs.LG, cs.RO, cs.CV
**Keywords:** VLA, agentic robot, robot harness
**Papers found:** 11

---

## 1. Planning in the Backbone: DiffAdapterVLA for Native Continuous Trajectory Generation with Driving VLMs

**Authors:** Changxin Lu, Xiaoliang Meng, Yu Wu, ..., Kaixuan Zhou, Yadong Shao
**arXiv:** [2609.15322](https://arxiv.org/abs/2609.15322)
**Categories:** Robotics (cs.RO); Artificial Intelligence (cs.AI)

Pretrained driving vision-language models (VLMs) integrate visual, route, language, and driving context into rich driving priors, yet their representation objectives remain separated from continuous driving planning. Existing methods typically begin trajectory generation only after the VLM has formed a final condition, leaving depth-wise condition computation outside the stepwise formation of trajectory state. We introduce DiffAdapterVLA, which realizes Planning in the Backbone: it injects explicit trajectory tokens into selected VLM late layers, bringing trajectory state into backbone forward computation, where it co-evolves with driving conditions at different depths. Lightweight layer-wise DiffAdapters organize this computation into recursive trajectory refinement, while asymmetric joint attention preserves directed guidance from the condition stream to trajectory planning. By placing planning within existing backbone computation rather than relying on an independent trajectory planner, DiffAdapterVLA adapts only lightweight trajectory modules to turn existing driving priors into efficient continuous planning capability. NAVSIM results show that it achieves high-quality closed-loop planning with low end-to-end latency using few trainable parameters, and demonstrate that jointly evolving trajectory state and depth-wise driving conditions in VLM late-layer computation effectively realizes continuous trajectory planning.

---

## 2. IMPACT-VLA: Interaction-aware Multimodal Propagation Attribution via Counterfactual Trajectories for Vision-Language-Action Policies

**Authors:** Jinwoong Kim, Sangjin Park
**arXiv:** [2609.15005](https://arxiv.org/abs/2609.15005)
**Categories:** Robotics (cs.RO); Artificial Intelligence (cs.AI)

Vision-Language-Action (VLA) policies perform robot manipulation tasks using multimodal inputs such as visual observations, proprioceptive states, and language instructions. However, it remains unclear at which execution stages each modality contributes to final task success and how input interventions propagate through subsequent states, observations, and actions. Existing attribution approaches primarily measure local sensitivity or temporally aggregated importance, limiting their ability to capture phase-dependent contributions and cross-phase dependencies. We propose Interaction-aware Multimodal Propagation Attribution via Counterfactual Trajectories for Vision-Language-Action Policies (IMPACT-VLA). IMPACT-VLA constructs behavioral phases from action transitions in a successful reference rollout, aligns them with policy query boundaries, and defines phase-modality blocks as attribution units. It then performs closed-loop counterfactual re-execution to quantify each block's contribution to final task success. We further analyze cross-phase non-additive interactions and trajectory propagation while distinguishing behavioral from functional recovery. Across 30 LIBERO robot manipulation tasks using OpenVLA-OFT, dominant-modality transitions occurred in 25 tasks (83.3%), and closed-loop attribution identified task-critical information more faithfully than Static Action Perturbation. Later-block marginal gains for negatively interacting pairs increased by approximately 3.3x under early-phase input replacement, while functional recovery could occur without behavioral recovery. These results reveal when multimodal inputs support task success and how their contributions become conditionally coupled during closed-loop execution.

---

## 3. Task-Specified Active Metrological Inspection with Measurement-Steered VLA Manipulation and Deterministic Evidence Gating

**Authors:** Zhiling Chen, Jingzhan Ge, Ruimin Chen, ..., David Gorsich, Farhad Imani
**arXiv:** [2609.14219](https://arxiv.org/abs/2609.14219)
**Categories:** Robotics (cs.RO); Artificial Intelligence (cs.AI); Computer Vision and Pattern Recognition (cs.CV)

High-mix low-volume (HMLV) manufacturing requires inspection systems to adapt to changing parts, specifications, and work orders without repeated task-specific programming. Existing inspection automation typically assumes predefined sensing sequences, while general purpose robot agents optimize task completion rather than the completeness and validity of metrological evidence. We formulate task-specified active metrological inspection and propose From Requirements to Admissible Metrological Evidence (FRAME), a hierarchical dual-arm framework that converts an inspection instruction and structured specification into traceable conformance evidence. FRAME coordinates learned manipulation with calibrated laser profilometry: a task manager grounds and schedules requirements, active surface correspondence verifies physical-to-specification localization, and evidence memory tracks measurement provenance, admissibility, and coverage. Learned components may propose inspection targets and physical access actions, but deterministic datum-grounded measurement, admissibility checks, coverage auditing, and conformance evaluation prevent incomplete or unverified evidence from authorizing PASS. A series of physical experiments shows that FRAME achieves higher end-to-end inspection reliability, fewer false accepts, and shorter task completion time.

---

## 4. ReWeight: Leveraging Human Data for VLA Post-Training via Demonstration Retrieval and Sample Weighting

**Authors:** Chenwei Wang, Dianye Huang, Match W.L. Ko, Chenjia Bai, Zhongliang Jiang
**arXiv:** [2609.13851](https://arxiv.org/abs/2609.13851)
**Categories:** Robotics (cs.RO); Artificial Intelligence (cs.AI)

Post-training vision-language-action (VLA) models for specific robots and tasks requires in-domain demonstrations, yet collecting diverse robot data is costly. Egocentric human demonstrations provide a scalable alternative, but directly mixing human and robot data can introduce cross-embodiment discrepancies and degrade policy performance. To address this challenge, we introduce ReWeight, a framework that incorporates human data into VLA post-training through demonstration-level retrieval and sample-level weighting. ReWeight learns a cross-embodiment visuomotor representation that combines visual observations with future actions to measure behavioral similarity between human and robot demonstrations. Based on optimal transport, it retrieves human demonstrations relevant to the target robot data and assigns larger weights to samples with smaller cross-embodiment discrepancies. We evaluate ReWeight using $\pi_{0.5}$ across eight simulation tasks and four real-world tasks under both clean and randomized settings. In simulation, ReWeight improves the average success rate of post-trained $\pi_{0.5}$ from 39% with only robot data and 44% with randomly mixed human-robot data to 57%. In the physical experimental setting, it achieves an average success rate of 68.8%, outperforming the baselines by 28.8% and 13.8%, respectively. Overall, ReWeight provides an effective paradigm for transforming abundant egocentric human experience into transferable supervision for robot learning. (Project webpage: this https URL)

---

## 5. ShieldVLA: Feasibility-Aware Safety Alignment for Vision-Language-Action Models

**Authors:** Manan Tayal, Akshay Nambi
**arXiv:** [2609.13231](https://arxiv.org/abs/2609.13231)
**Categories:** Robotics (cs.RO); Artificial Intelligence (cs.AI)

Vision-Language-Action (VLA) models demonstrate strong generalization in robotic manipulation and navigation, but existing fine-tuning methods provide limited safety guarantees. Current approaches primarily rely on Lagrangian optimization that enforces safety through soft penalties on expected cumulative cost, often resulting in residual constraint violations or overly conservative behavior. Moreover, learning safety in visual domains is challenging due to the absence of dense per-step safety annotations. We propose ShieldVLA, a safety-aligned fine-tuning framework for VLA models based on Hamilton-Jacobi (HJ) reachability. ShieldVLA learns a model-free approximation of the HJ reachability value function directly from visual observations to estimate the safe operating region. The learned safety critic gates policy optimization by separating reward maximization within feasible regions from recovery near unsafe states, avoiding persistent reward-cost trade-offs. To enable scalable supervision in visual environments, we introduce rubric-based VLM safety scores that convert semantic safety feedback into structured critic targets without requiring manual cost labels. Across five navigation and manipulation benchmarks spanning multiple VLA backbones, ShieldVLA reduces cumulative safety cost by 57% on average and improves task success rate by +0.13 over SafeVLA.

---

## 6. When Faster VLA Deployment Changes Closed-Loop Behavior: Task Success-Latency Analysis of SmolVLA Across PyTorch and ONNX Variants

**Authors:** Rafiqul Islam
**arXiv:** [2609.14146](https://arxiv.org/abs/2609.14146)
**Categories:** Robotics (cs.RO); Machine Learning (cs.LG)

Vision-language-action (VLA) deployment can reduce inference latency while changing closed-loop task behavior. We evaluate HuggingFaceVLA/smolvla_libero on an RTX 2060 (6 GB) in LIBERO Spatial and Object (MuJoCo 3.3.2, LeRobot 0.6.1, seed 42), comparing PyTorch+AMP with ONNX Runtime CUDA Execution Provider (CUDA EP). The main evaluation uses 100 episodes/suite; a paired rollout uses 300 episodes/suite. PyTorch+AMP reaches 70.0%/88.0% Spatial/Object success at 1181 ms p99. Requested-FP16 and requested-INT8 ONNX reduce tether-inspect p99 to 601 ms and 532 ms, while Spatial success falls to 41.0% and 40.0% and Object remains at 89.0%. A graph audit shows those artifacts are byte-identical FP32 graphs, so the requested-INT8 row is not operator-level INT8 quantization. A static language-width ablation (16/24/32 tokens) yields Spatial success of 41.0%, 75.0%, and 71.0%; widths 24 and 32 recover much of the Spatial drop while Object success and uniform-bench latency stay approximately stable. Width-24 ONNX Spatial success is comparable to the PyTorch+AMP baseline at roughly half the latency (Wilson intervals overlap; two-proportion chi-squared p=0.53). Context width is an important contributor in this stack; it does not account for every PyTorch-vs-ONNX difference. Deployment evaluation should jointly report latency, artifact inspection, interface constraints, and closed-loop success. Code: this https URL.

---

## 7. Beyond Single-Axis Testing: Paired Evaluation of Compound Robustness in Vision-Language-Action Policies

**Authors:** Hiroki Sawada, Shunichi Kasahara
**arXiv:** [2609.15940](https://arxiv.org/abs/2609.15940)
**Categories:** Robotics (cs.RO)

Vision-language-action policies are typically evaluated one perturbation at a time, providing a useful diagnosis of their sensitivity to individual distribution shifts. Real-world deployment, however, may involve several shifts simultaneously, and it remains unclear how these individual robustness measurements compose. We ask whether compound robustness can be inferred from single-axis evaluations. We introduce LIBERO-CTRL, a six-axis benchmark that pairs each initial state across single-axis conditions and a matched simultaneous condition. This design reveals two opposing outcome changes that aggregate success rates cannot distinguish: emergent failures, where all single-axis rollouts succeed but the simultaneous rollout fails, and compensated successes, where at least one single-axis rollout fails but the simultaneous rollout succeeds. Because one transition decreases compound success while the other increases it, they can cancel, making aggregate compound performance appear consistent with single-axis measurements even when individual outcomes differ substantially. These opposing transitions can largely cancel in aggregate: even when the difference between the two transition rates is not statistically distinguishable from zero, as many as 29.0% of matched initial states still change outcome. Across six policies and three severity levels, such outcome changes reach 34.5% in the most affected condition. The relative prevalence of the two transitions varies across policies and severities, while the transition rates remain similar under independent re-evaluation of stochastic policies. Compound robustness therefore cannot be characterized from aggregate single-axis success rates alone; matched per-instance evaluation is needed to reveal how joint perturbations alter behavior.

---

## 8. What Makes an Efficient VLA? Navigating Action-Head Design, Scaling, and Latency

**Authors:** Luoyang Sun, Guoyang Xia, Fengfa Li, ..., Jun Wang, Cheng Deng
**arXiv:** [2609.13984](https://arxiv.org/abs/2609.13984)
**Categories:** Robotics (cs.RO); Computer Vision and Pattern Recognition (cs.CV)

Vision-Language-Action (VLA) models combine a pretrained vision encoder, a language backbone, and an action head, but their relative contribution has not been established under controlled, latency-paired conditions. We fix the backbone families (SigLIP2 and Qwen2.5) and the training pipeline, sweep action-head design and module scale, and pair each configuration with measured on-device latency. The study yields three findings. First, action-head performance is governed primarily by initialization rather than decoder architecture, loss, or inference budget: copying the last transformer layers of the language backbone into the head is the single largest lever, at no latency cost, and the only axis that helps at every module scale. Alignment also explains the other axes: flow matching and a heavier decoder pay off only while the head is misaligned and reverse once it is aligned, and extra inference passes give no measurable benefit; expressiveness appears to substitute for missing alignment. We read this as representation transfer: the aligned head keeps attending to the instruction's object nouns and stays close to the backbone in weight space rather than relearning to act from scratch. Because we reach alignment only through initialization, we offer this as the account that best organizes the measurements, not a demonstrated cause, and name the control that would settle it. Second, capacity pays only after alignment: the aligned action head is the highest-return module to scale. Third, those returns diminish sharply near the size today's $\pi$-series VLAs already use, so further growth buys little in-domain accuracy for its latency. These specify EffVLA, a compact model matching the strongest open-source VLAs on standard LIBERO, leading on most LIBERO-Plus perturbation axes at lower latency, and transferring to a real SO-ARM101 arm with the recipe unchanged.

---

## 9. GeomVLA: Unifying Scene, Motion, and Action in 3D

**Authors:** Ziyin Xiong, Nikos Gkanatsios, Moritz Reuss, Katerina Fragkiadaki
**arXiv:** [2609.13812](https://arxiv.org/abs/2609.13812)
**Categories:** Robotics (cs.RO)

We present GeomVLA, a Vision-Language-Action (VLA) model that unifies perception, latent scene motion prediction, and action generation within a shared robot-centric 3D coordinate frame. Our approach lifts pretrained VLM features into spatially grounded 3D scene tokens using depth and camera calibration, while retaining the semantic representations learned during VLM pretraining. We further introduce a 3D Scene Trajectory Denoiser, a task-conditioned module that learns a latent representation of how scene points are expected to move in 3D. Rather than executing the predicted trajectory as an open-loop plan, GeomVLA extracts intermediate motion tokens from the trajectory denoiser and uses them to condition a 3D flow-based action denoiser through geometry-aware attention. GeomVLA achieves state-of-the-art performance on CALVIN, competitive performance on LIBERO and RoboTwin2.0, and outperforms strong baselines in real-world manipulation settings without robot-action pretraining. Extensive ablations show that future-motion reasoning alone is insufficient: the primary gains are associated with maintaining geometric consistency among scene representation, motion prediction, and robot actions throughout the perception-to-action pipeline.

---

## 10. GROOVE: Geometry-Guided Reduction of Operational-Space Jerk in VLA Execution

**Authors:** Sangho Yun, Minsoo Kim, Minwoo Cho, Hwanjo Yu
**arXiv:** [2609.13695](https://arxiv.org/abs/2609.13695)
**Categories:** Robotics (cs.RO)

Chunked vision language action (VLA) policies execute several commands per query, but jerk within chunks and across replanning boundaries can induce oscillatory motion and sharp actuator transients. We present GROOVE, an online regulator that searches directional correction regions around the raw three dimensional end effector (EEF) path, without retraining or additional VLA inference. It optimizes the new chunk using delivered commands as boundary conditions, reducing boundary and within chunk jerk while bounding cumulative translation and local axis angle deviation from the raw plan after every command. Using quadratic programs (QPs), GROOVE generates a cube reference and thirteen directional candidates, then selects the one with the lowest command space jerk under a reference relative deviation cap. On a held out LIBERO benchmark, GROOVE achieves the largest reductions among the evaluated methods, reducing translational and rotational EEF jerk by 33.02% and 43.42%, respectively, with task success of 95.75% versus 93.75% for raw execution. Across 50 matched UR5e pairs with measured execution timing, it reduces translational and rotational tool center point (TCP) jerk by 16.39% and 19.49% and joint current slew by 29.09%.

---

## 11. How to Better Train VLAs: Lessons Learned From the REAL-I Challenge at ICRA 2026

**Authors:** Jiaming Wang, Jizhuo Chen, Diwen Liu, ..., Yongping Pan, Harold Soh
**arXiv:** [2609.13679](https://arxiv.org/abs/2609.13679)
**Categories:** Robotics (cs.RO)

How can robot policies learn more effectively from a fixed demonstration budget? The first Real-world Embodied AI Learning (REAL-I) Challenge at ICRA 2026 examined this question through simulation, real-robot evaluation, and an on-site final on a shared dual-arm humanoid platform. We describe the challenge tasks, data and deployment interfaces, and competition results, then compare the approaches contributed by NUS-CLEAR, RCL-Lab, and this http URL. Their systems combined pretrained vision-language-action models and task-specific imitation policies with different strategies for data curation, staged adaptation, checkpoint selection, and action-space design. The team reports highlight the importance of adapting to the deployment environment while retaining prior capabilities, treating demonstration quality at an appropriate temporal scale, and suppressing errors in inactive robot components. They also expose the limitations of offline action-prediction metrics for forecasting closed-loop success. These observations motivate a view of fixed-data robot learning that integrates data, adaptation, evaluation, and deployment.

---
