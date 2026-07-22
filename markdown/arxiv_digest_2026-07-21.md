# arXiv Daily Digest — 2026-07-21

**Mode:** direct
**Categories:** cs.AI, cs.LG, cs.RO, cs.CV
**Keywords:** VLA, world model, world action model
**Papers found:** 15

---

## 1. SAGE: Subgoal-Conditioned Action Generation for Latent World Model Planning

**Authors:** Letian Cheng, Qi Zhang, Yisen Wang
**arXiv:** [2607.17973](https://arxiv.org/abs/2607.17973)
**Categories:** Artificial Intelligence (cs.AI)

Latent world models have emerged as a powerful planning paradigm by learning action-conditioned predictive dynamics and using them as internal simulators to imagine and evaluate candidate action sequences. However, as the planning horizon grows, performance becomes increasingly constrained by proposal quality: a fixed candidate budget must search an exponentially larger action space, making it difficult to expose the world model to high-quality candidate futures for evaluation. In this paper, we introduce a prior-conditioned planner that replaces random proposal initialization with structured guidance. At each planning stage, a goal-conditioned generator predicts the next reachable latent subgoal for a specified duration, which is then used to condition the generation of candidate action sequences. To capture semantic information across temporal scales, we use subgoals of varying durations as priors, balancing fine-grained local control with higher-level long-horizon progress. Then the frozen world model evaluates and refines these subgoal-conditioned proposals before execution. Experiments on PushT and OGBench Cube show that coupling latent subgoal decomposition with prior-conditioned action generation substantially improves long-horizon planning while preserving strong short-horizon performance. To be specific, when the target offset is $150$, it raises PushT success from $12.7\%$ to $64.7\%$ and OGBench Cube success from $26.7\%$ to $67.3\%$.

---

## 2. An Explicit World Model Based on Data-First Ontology: DaoQL Multimodal Storage Validation and Counterfactual Reasoning Evaluation

**Authors:** Zhanbo Li, Shifeng Wu, Xiangjin Meng, Wenjie Cai
**arXiv:** [2607.17269](https://arxiv.org/abs/2607.17269)
**Categories:** Artificial Intelligence (cs.AI); Databases (cs.DB)

Large language models encode world models implicitly in neural weights, which exposes four structural risks in high-precision domains such as medicine and finance: hallucination, frozen knowledge, poor explainability, and poor modifiability. This paper proposes data-first ontology: LLMs are treated as reasoning and language engines, while deterministic knowledge is moved into an explicit multimodal database, DaoQL. We formalize an explicit world model and show that, under rule independence, deterministic evaluation, and fixed conflict resolution, explicit models provide a sufficient condition for composable counterfactual decomposability; implicit models lack atomic read/delta semantics and therefore provide no comparable architectural guarantee. The implemented system focuses on DaoQL's verified storage layer and explicit Eval path, integrating graph, column, vector, and full-text engines within one process. KVCache graph nodes, expert hot updates, and the DaoQL-Agent runtime remain future work. On an embedded same-machine setup, DaoQL reports graph BFS at 1.20 ms, HNSW at 83.1 us, and a Fluent hybrid query at 105.8 us; these results indicate engineering potential but must be interpreted with deployment-shape differences from client-server systems. Exploratory measurements on LDBC SNB SF1 and ANN-Benchmarks further show 34/34 query coverage with interactive-class queries mostly in the sub-millisecond to millisecond range, but only 1.8 QPS overall due to long-tail BI/IC queries; ANN-Benchmarks reaches Recall@10 >= 99% at thousand-level QPS after a bridge-edge protection fix. In a five-domain counterfactual experiment (n = 1250), DaoQL+GPT-4o achieves 94% composable counterfactual decomposability, 49 percentage points above GPT-4o alone. The paper explicitly separates provable structure, preliminary empirical evidence, and architectural roadmap claims.

---

## 3. Masked Diffusion Language Models are Strong and Steerable Text-Based World Models for Agentic RL

**Authors:** Darshan Deshpande
**arXiv:** [2607.16204](https://arxiv.org/abs/2607.16204)
**Categories:** Artificial Intelligence (cs.AI); Machine Learning (cs.LG)

Recent growth in reinforcement learning (RL) has surfaced a need for diverse, specialized training environments. Hand-curated environments with fixed task and reward difficulties become ineffective signals as model performance improves, and sparse rewards over long horizons induce mode collapse on specific workflows or tool structures. World models that simulate environment states have matched pure rollout performance, making them promising for scaling diversity on-demand. However, autoregressive (AR) world models suffer from a left-to-right bias preventing conditioning on globally interdependent state anchors such as tool schemas, prior turns, and expected outcomes. We (i) formalize text-based world modeling as a steerable transition-dynamics problem decomposed into initial state, task context, tool schemas, domain rules, and steering directives, and (ii) curate 239,403 grounded state-action trajectories spanning nine open-source environments and twelve frontier model families. We compare AR LMs and masked diffusion language models (MDLMs), showing MDLMs, via bidirectional anchor-aware denoising, achieve better coherence, groundedness, and empirically validated rollout diversity than LLMs over 4x their parameter size, at comparable inference latency. We introduce a plug-and-play GRPO training framework with deterministic state checks, and perform zero-shot transfer ablations on three OOD environments (ScienceWorld, ALFWorld, AppWorld) across three 1.2B-7B agent backbones (LFM2.5, Qwen3, Mistral), achieving up to 47% absolute gains over baselines without environment-specific fine-tuning. We further conduct behavioral analysis of failure modes under adversarial scenarios and human evaluation on realism, outcome correctness, and training utility. We open-source our work to encourage research in this direction.

---

## 4. Reasoning as a Double-Edged Sword: Architecture and Cross-Stage Robustness in Vision-Language-Action Models

**Authors:** Tuan Duong Trinh, Naveed Akhtar, Basim Azam
**arXiv:** [2607.17786](https://arxiv.org/abs/2607.17786)
**Categories:** Robotics (cs.RO); Artificial Intelligence (cs.AI); Cryptography and Security (cs.CR); Machine Learning (cs.LG)

Does adding a reasoning step make a Vision-Language-Action (VLA) model more robust to perturbation? Intuitively, a policy that reasons before acting should absorb a perturbed input better than one that maps observations directly to actions. We test this premise head-on across three models that span the reasoning spectrum (no reasoning, a text chain-of-thought, and a latent iterative loop), perturbing each at the vision, reasoning, and action stages on LIBERO and SimplerEnv. Two questions organize the study: does the reasoning design shift robustness, and can the reasoning be read back at runtime as a safety signal? We find that the latent-iterative model is by far the least robust: under both stochastic noise and white-box perturbation its task success collapses, while the other two hold. This fragility is structural rather than cumulative: varying the reasoning depth at inference barely moves it. Reasoning outputs can in principle be monitored, but the monitors fail under fair tests. A plan--action consistency probe that looks near-perfect under naive evaluation falls to chance under adaptive attack. Under matched-FPR calibration, fusing it with an action-anomaly probe never lifts defended success above undefended. Scoped to these output-level behavioral probes under white-box vision-stage attack, this ceiling is a precondition that any viable defense must first satisfy.

---

## 5. Mobile Network Control with a World Model

**Authors:** Maxime Bouton, Ioanna Mitsioni, Simon Lindståhl, Jaeseong Jeong
**arXiv:** [2607.17747](https://arxiv.org/abs/2607.17747)
**Categories:** Networking and Internet Architecture (cs.NI); Artificial Intelligence (cs.AI)

The increasing complexity of mobile networks necessitates intelligent and dynamic control strategies for efficient, energy-conserving management. We propose a world model-based approach for network control that enables adaptive configuration of crucial parameters. The world model is trained from historical data and predicts the impact of its actions on future network states. Our controller leverages the model's uncertainty estimate to robustly find optimal network configuration changes. Furthermore, the optimization objective can be changed dynamically without model retraining. We demonstrate the effectiveness of the approach in simulated closed-loop control of a mobile network energy-saving feature. Our results show improved performance in balancing energy savings with quality of service, compared to traditional methods and reinforcement learning approaches. Finally, we show the world model performance on real network data from, and evaluate counterfactual actions proposed by the controller under various throughput constraints.

---

## 6. VLA-ReID: Video-Level Association for Re-Identification in Multi-Object Tracking with Highly Similar Objects

**Authors:** Yanrong Qin, Xiaoyan Cao, Yao Yao
**arXiv:** [2607.17157](https://arxiv.org/abs/2607.17157)
**Categories:** Computer Vision and Pattern Recognition (cs.CV); Artificial Intelligence (cs.AI)

Multi-object tracking (MOT) aims to localize multiple objects in videos while preserving their identities over time. Long-term identity preservation remains difficult when objects are small, densely distributed, and highly similar in appearance, as in bee swarm scenes. Existing trackers rely on re-identification (re-ID) models trained through single-instance assignment (instance-level querying). At inference, however, MOT requires global assignment between multiple trajectories and detections, corresponding to video-level querying. This training-inference mismatch can cause identity switches among visually similar objects. Existing approaches also often require substantial additional annotations to enhance appearance discrimination. We propose Video-Level Association re-ID (VLA-ReID), which reformulates re-ID as video-level association modeling. It uses aggregated historical trajectory features as queries and all current-frame detections as candidates, enabling direct optimization of their global association at each frame. In addition, Frame-Common Appearance Estimation (FCAE) estimates a common appearance direction from current-frame detections, while Common-Appearance Suppression (CAS) removes the corresponding component along this direction from trajectory and detection features. This amplifies discriminative differences among highly similar objects without additional annotations. Experiments on BEE24 show that VLA-ReID improves HOTA by 1.1, MOTA by 0.3, AssR by 2.6, AssA by 0.7, and IDF1 by 0.8 over state-of-the-art trackers, while reducing identity switches by 28%. These results demonstrate the effectiveness of video-level re-ID modeling for appearance-based association in MOT.

---

## 7. What Do They See? Interpreting Complex Road Scenarios Through the Eyes of Vision-Language-Action Models for Safe and Trustworthy Autonomous Vehicle Learning

**Authors:** Kalpana Panda, Wesley Maia, Vinti Agarwal, Ross Greer
**arXiv:** [2607.16938](https://arxiv.org/abs/2607.16938)
**Categories:** Computer Vision and Pattern Recognition (cs.CV); Artificial Intelligence (cs.AI); Machine Learning (cs.LG); Robotics (cs.RO)

End-to-end autonomous driving models are now able to navigate complex road scenarios, mapping raw sensor observations directly to observed paths for open-loop evaluation and often effective driving in closed-loop evaluation. Yet the internal logic of these safety-critical systems remains largely opaque, due to the complexity of traffic scenes. We propose a counterfactual ablation framework called Counterfactual Vision Action Analysis (CVAA) that systematically removes individual detected objects from front-camera images using photorealistic generative inpainting to prepare counterfactual sets to evaluate the difference in the model's response. This isolates the causal effect of each object's presence on the model's planning behaviour. Applied to the Alpamayo 1 trajectory predictor across 210 nuScenes driving scenes, we create a dataset Counter -nuScenes, using which we see that vehicles and pedestrians within the model's 'path' dominate causal influence as expected, while traffic lights, as expected, exert disproportionate effect relative to their image footprint. However, we also find cases where the model responds strongly to objects a human driver would consider irrelevant. This brings forth a deeper question: does the model itself view the scene as a sum of individual objects influencing the outcome, or does it encode an entirely different set of internal features that do not correspond to human-legible scene elements? To further understand this, we compare intermediate representations of original and inpainted image pairs using mechanistic interpretability techniques and examine the effect of the removal through the various model layers. Together, these two stages offer a path from behavioral auditing to representational understanding, creating explainable driving systems and solidifying human-AI trust.

---

## 8. Foresight Residual RL for Long-Horizon Robot Manipulation with Vision-Language-Action Models

**Authors:** Yuhan Liu, Xinyu Zhang, Litao Liu, Abdeslam Boularias
**arXiv:** [2607.16506](https://arxiv.org/abs/2607.16506)
**Categories:** Robotics (cs.RO); Machine Learning (cs.LG)

Vision-Language-Action (VLA) policies offer strong general-purpose manipulation priors, but often fail on tight-tolerance, contact-rich assembly due to long-horizon credit assignment and subtask coupling: a state that is geometrically successful for the current skill can be brittle for downstream skills. We show this failure mode in residual reinforcement learning (RL) over a frozen VLA base policy: constant sparse success rewards improve each subtask in isolation yet yield little or no gain when skills are chained, because terminal state quality is uncontrolled. We propose Foresight Residual RL, which optimizes handoff quality by augmenting each subtask's sparse success reward with an offline-estimated foresight value -- the probability of future subtask success conditioned on the terminal state of the current subtask. Concretely, we (i) train a visual foresight predictor from images of terminal states of the base policy, labeled using downstream rollout statistics, and (ii) train residual policies via backward foresight induction, using the predictor output as a reward multiplier. On a three-phase wrench-based nut-tightening assembly task in Isaac Gym (grasp, move-insert, rotate), our method achieves 85.6% full-task success, outperforming standard subtask residual RL (54.5%) and VLA baselines, while leaving per-subtask success unchanged. These results highlight that improving long-horizon performance requires shaping which successful states are produced at each sub-task, not only whether success occurs.

---

## 9. Depth-Regularized JEPA World Models Learn More Transferable Representations from Real Outdoor Robot Data

**Authors:** Usman M. Khan
**arXiv:** [2607.16314](https://arxiv.org/abs/2607.16314)
**Categories:** Computer Vision and Pattern Recognition (cs.CV); Machine Learning (cs.LG); Robotics (cs.RO)

World models, especially based on JEPA architectures, have been shown to learn robust dynamics of various environments. However, learning from visually complex real-world data remains a challenge, especially in unpredictable outdoor environments. We introduce depth as a geometric prior during training in learning more robust latent dynamics directly from robot video data and handling visual complexity. This combines depth supervision with an isotropy-inducing latent regularizer (SIGReg), maximizing task-agnostic latent diversity while constraining how that diversity is organized, with the combined objective targeting the highest-entropy representation consistent with scene geometry. To satisfy this greater complexity without increasing inference time, we also add training-only overparameterization. Training an 18M-parameter model on video from a real agricultural robot, we evaluate with frozen-representation visual odometry probes, predictor-based surprise detection, and multi-step latent rollout fidelity. Compared to the baseline LeWM, our method lowers visual odometry probe error by 33%, substantially increases surprise-score separation both in-domain and on the out-of-domain TartanGround benchmark, and improves multi-step rollout fidelity under domain shift, with gains that grow with rollout horizon. Notably, we also see improvements in surprise-score separation on physics understanding that is not directly tied to 3D geometry, such as lighting and shadows. These results show that a lightweight training-time geometric prior makes a compact JEPA world model more useful and more transferable on real outdoor data with strong underlying representations, without adding inference overhead. Our work suggests that depth as a physically grounded prior can enhance world model generalization on a variety of tasks.

---

## 10. FM-VLA: Force-based Memory for Vision-Language-Action Models in Contact-Rich Manipulation

**Authors:** Ruicheng Li, Qixiu Li, Ruichun Ma, ..., Jiaolong Yang, Baining Guo
**arXiv:** [2607.18231](https://arxiv.org/abs/2607.18231)
**Categories:** Robotics (cs.RO)

Vision-language-action (VLA) models have achieved impressive generalization in robotic manipulation, and recent memory-augmented VLAs have relaxed the Markovian assumption by conditioning on past images or language summaries. Vision-based memory approaches address this by conditioning on sampled past image frames, but they are computationally expensive and fundamentally limited when temporal events are visually ambiguous, e.g., pushing a button multiple times with small movements. We propose FM-VLA, a VLA model with force-based memory, enabling temporal context reasoning for non-Markovian, contact-rich manipulation. We encode force histories into compact force memory tokens with a variational autoencoder (VAE) pretrained with force time series reconstruction. By projecting force latent representations and short state history as additional conditioning tokens to the action expert module, we enable VLAs to leverage accumulated contact event history to guide manipulation. We evaluate FM-VLA on three memory-dependent tasks, including finding a hidden block, pressing a button, and wiping a dish for a specific number of times. Our lightweight force memory achieves over 80% success rate with minimal inference overhead, significantly outperforming baseline approaches. Project page: this https URL

---

## 11. Closing the Loop in Humanoid VLA: Persistent 3D Object Tokens for Verifiable Loco-Manipulation

**Authors:** Peng Ren, Haoyang Ge, Jiang Zhao, ..., Pei Chi, Kai Chen
**arXiv:** [2607.18016](https://arxiv.org/abs/2607.18016)
**Categories:** Robotics (cs.RO)

Vision-language-action policies are a promising foundation for general robot control, but long-horizon humanoid loco-manipulation requires the robot to treat task objects as persistent physical entities across movement, contact, occlusion, and recovery. We study this problem as object-state divergence: the object state used to condition a whole-body action can differ from the state used to decide whether the action achieved the intended physical relation. We propose \emph{Persistent Object Tokenization} (POT), which maintains role-indexed 3D object records from RGB-D observations and converts them into object tokens for a whole-body action expert. Instantiated as \emph{POT-VLA}, the same object records condition action generation and support geometric predicate checks, yielding a closed-loop execution system in which object state is both actionable and verifiable. On a Unitree G1, POT-VLA improves a matched direct GR00T-N1.7 baseline from 39/80 to 71/80 successes over eight real-world task families. In an external Being-0-aligned reference, POT-VLA achieves 44/50 successes on aligned service tasks, compared with the 37/50 success reported by the Being-0 paper. The largest gains occur on tasks requiring maintained 3D relations, suggesting that persistent object-centered state is a useful abstraction for verifiable humanoid VLA execution.

---

## 12. GeoWorldAD: Geometry World Action Model for Autonomous Driving

**Authors:** Songyan Zhang, Jinyuan Tian, Hanbing Li, ..., Kuiyuan Yang, Chen Lv
**arXiv:** [2607.17521](https://arxiv.org/abs/2607.17521)
**Categories:** Robotics (cs.RO)

Autonomous driving requires both safe and efficient planning decisions in dynamic 3D environments. Although recent Vision/Video-Action models learn policies directly from visual observations and scale well with advances in vision transformers and large-scale training data, they often lack explicit geometric grounding and future-aware spatial guidance, limiting their ability to balance collision avoidance and driving progress. In this work, we propose GeoWorldAD, a geometry world action model that grounds trajectory planning in ego-aligned 3D space and anticipates short-horizon scene evolution with latent future geometry tokens. Present geometry provides essential spatial constraints for safe planning, while future geometry reveals how surrounding agents and ego-centric free space may evolve, reducing overly conservative decisions without sacrificing safety. To efficiently exploit these geometric cues, GeoWorldAD progressively aggregates multi-scale present geometry and latent future geometry through iterative trajectory refinement. Experiments on NAVSIM v1 and v2 demonstrate state-of-the-art performance, highlighting the effectiveness of explicit 3D geometry grounding and future geometry world modeling for safe and efficient autonomous driving.

---

## 13. Test-Time Scaling for World Action Models via Zero-Shot Geometric Evaluation

**Authors:** Zesen Zhao, Minkyoung Cho, Hui shen, ..., Yulong Cao, Z.Morley Mao
**arXiv:** [2607.17454](https://arxiv.org/abs/2607.17454)
**Categories:** Robotics (cs.RO)

Test-time scaling improves foundation-model inference by spending additional computation, but robot control requires deciding whether extra compute is useful before executing an action. World Action Models (WAMs) make this decision natural: each rollout exposes both an action chunk and predicted future observations. We propose \methodgated, a training-free selective test-time scaling framework for WAMs. We first instantiate \method, a fixed-budget Best-of-$N$ selector that ranks sampled rollouts by cross-view depth reprojection consistency of their predicted futures, computed with a frozen geometry foundation model. \methodgated\ adds a lightweight action--future consistency gate that invokes \method\ only when the initial rollout appears internally inconsistent. Across five benchmark--backbone settings on RoboCasa, LIBERO Long, and RoboTwin~2.0, fixed-budget \method\ improves $N{=}8$ task success in every setting, e.g., raising the RoboCasa group average from $66.3\%$ to $68.4\%$ with Cosmos Policy and from $80.8\%$ to $82.5\%$ with X-WAM. With gating enabled, \methodgated\ recovers on average $74.8\%$ of the always-on success gain while triggering additional sampling on only $26.2\%$ of decision points. Offline diagnostics show that cross-view reprojection is a strong task-label-free selector, and we identify false low-score selections as a failure mode that helps explain why performance can saturate or degrade as $N$ increases.

---

## 14. PAVXploreRL: Physical-Action-Visual World Model Reinforcement Learning with Action Exploration

**Authors:** Han Wang, Zijun Wang, Shuoshuo Xue, ..., Xiaodan Liang, Roy Ka-Wei Lee
**arXiv:** [2607.16602](https://arxiv.org/abs/2607.16602)
**Categories:** Computer Vision and Pattern Recognition (cs.CV)

Action-conditioned world models are a key component of embodied AI, serving as scalable policy evaluators that reduce reliance on expensive real-world rollouts. To accurately capture diverse action-induced dynamics, such models should satisfy three key objectives-Physical Plausibility (P), Action Adherence (A), and Visual Fidelity (V), collectively referred to as PAV-while remaining robust to both in-distribution (ID) expert demonstrations and out-of-distribution (OOD) actions. However, existing methods primarily rely on ID action-video pairs and pixel-level reconstruction losses, which do not explicitly optimize PAV objectives and generalize poorly beyond expert data. To address this, we propose PAVXploreRL, a reinforcement learning framework built on a pretrained latent world model that explicitly optimizes PAV objectives through reward-driven training. To improve action generalization, our method jointly leverages ID trajectories and noise-driven OOD action exploration, without paired video supervision. Experiments show that PAVXploreRL consistently outperforms pretrained baselines, achieving a 5.6% average gain across benchmarks and producing higher-quality PAV properties. As a policy evaluator, it also yields more reliable performance estimates and reduces the overestimation bias of prior expert-only world models such as Ctrl-World. Code: this https URL

---

## 15. Patch Policy: Efficient Embodied Control via Dense Visual Representations

**Authors:** Gaoyue Zhou, Zichen Jeff Cui, Ada Langford, ..., Yann LeCun, Lerrel Pinto
**arXiv:** [2607.18236](https://arxiv.org/abs/2607.18236)
**Categories:** Robotics (cs.RO); Machine Learning (cs.LG)

Pretrained dense visual features from Vision Transformers (ViTs) are powerful yet have been underutilized in robot learning. Modern robot policies either compress each observation into a single global token, or rely on visual backbones trained from scratch, sacrificing both fine-grained spatial detail and the benefits of large-scale visual pre-training. While there exist policies that do operate on dense patch features like large vision-language-action models (VLAs), they tend to be heavy and slow, inheriting the full cost of a billion-parameter vision-language model (VLM) backbone. We close this gap with Patch Policy, a minimal architectural extension that enables transformer-based policies to consume dense pre-trained patch tokens directly without the computational overhead of a full VLM. At its core is a block-causal attention mask that preserves the temporal causality of standard policies while letting the model attend over many patch tokens per observation, alongside other state information. Patch Policy is lightweight, fast, and highly effective. Across four simulated and three real-world environment suites, our method achieves a 40% relative improvement over policies using state-of-the-art global-pooled representations. Furthermore, it surpasses fine-tuned OpenVLA-OFT by 18% while using roughly 0.7% of the parameters. We believe Patch Policy provides a pipeline for the robotics community to readily leverage continuing progress in visual representation learning, without sacrificing the training efficiency or inference speed required for high-frequency, reactive control. Videos can be viewed at this https URL

---
