# arXiv Daily Digest — 2026-06-15

**Mode:** direct
**Categories:** cs.AI, cs.LG, cs.RO, cs.CV
**Keywords:** VLA, world model, world action model
**Papers found:** 17

---

## 1. SIMMER: Benchmarking Latent Failures in LLM Executable Planning with a World Model

**Authors:** Xiaoxin Lu, Ranran Haoran Zhang, Rui Zhang
**arXiv:** [2606.14574](https://arxiv.org/abs/2606.14574)
**Categories:** Computation and Language (cs.CL); Artificial Intelligence (cs.AI)

Large language models (LLMs) are increasingly deployed as planners for autonomous agents in household environments. While existing benchmarks evaluate whether LLM-generated plans execute successfully, they overlook a critical type of failure: latent failures. Unlike immediate failures that trigger instant feedback at execution time and enable timely correction, latent failures do not immediately halt plan execution but silently compromise goal achievement. In severe cases, they cause irreversible harm. To address this gap, we introduce SIMMER, a benchmark for evaluating latent failures in LLM planning through a human-curated symbolic world model grounded in the kitchen domain. SIMMER defines a world model comprising 77 actions, 262 unique objects, and approximately 46,800 possible interactions that are semantically realistic, derived from real-world cooking scripts. It then leverages a state machine executor that validates plans against the world model and detects immediate precondition violations, latent hazards, and irreversible failures. Experiments across six LLMs show that even frontier models achieve at most 17% error-free plans. Moreover, up to 56% of plans contain latent failures, the majority of which lead to irreversible consequences. We further demonstrate that explicit state reasoning via counterfactual foresight simulation can reduce latent failures by up to 72% and irreversible cases by up to 75%, suggesting a promising direction for more robust LLM planners.

---

## 2. Hy-Embodied-0.5-VLA: From Vision-Language-Action Models to a Real-World Robot Learning Stack

**Authors:** He Zhang, Lingzhu Xiang, Haitao Lin, ..., Han Hu, Zhengyou Zhang
**arXiv:** [2606.14409](https://arxiv.org/abs/2606.14409)
**Categories:** Robotics (cs.RO); Artificial Intelligence (cs.AI)

In this report, we present Hy-Embodied-0.5-VLA, abbreviated as HyVLA-0.5, an end-to-end system that spans the full robot learning stack: data collection, model design, continued pre-training and supervised fine-tuning, RL post-training, and real-world deployment. Each component serves a distinct role in this stack.

---

## 3. Elastic Queries Reinforcement Learning: Self-Aware Policy Execution for VLA Models

**Authors:** Ge Wang, Xinyu Tan, Xiang Li, ..., Yatong Han, Zhen Li
**arXiv:** [2606.14375](https://arxiv.org/abs/2606.14375)
**Categories:** Robotics (cs.RO); Artificial Intelligence (cs.AI)

Vision-language-action (VLA) models are powerful action generators for robot manipulation, but they are typically executed with fixed inference and replanning schedules. This rigidity ignores the uneven difficulty of robot control: contact-rich or uncertain states may need more computation and fresher feedback, while easier states can often be handled with fewer inference steps and longer open-loop execution. We propose Elastic Queries Reinforcement Learning (EQRL), a framework that makes each VLA policy query elastic. A lightweight latent-schedule adaptor jointly selects the latent input, denoising budget, and action chunk length, without fine-tuning the underlying VLA model. To make scheduling difficulty-aware, EQRL trains a critic over the joint latent-schedule action and derives a state difficulty signal from critic ensemble disagreement. This signal guides compute toward difficult states, while a learned residual allows task-driven correction. We formulate variable chunk execution as query-level macro-action RL with chunk-dependent discounting and an amortized number-of-function-evaluations (NFE) budget. Across simulation and real-robot manipulation, EQRL reduces amortized inference cost while preserving or improving task success.

---

## 4. When and How Severely: Scenario-Specific Safety Envelopes for Driving VLAs

**Authors:** Abhinaw Priyadershi, Jelena Frtunikj
**arXiv:** [2606.14238](https://arxiv.org/abs/2606.14238)
**Categories:** Robotics (cs.RO); Artificial Intelligence (cs.AI)

Safety certification of Vision-Language-Action (VLA) driving planners under ISO 21448 (SOTIF) rests on an Operational Design Domain (ODD) specification that answers two complementary questions: when does the planner start to fail, and how severely does it fail once it does? We evaluate Alpamayo R1, a 10B-parameter open-weight driving VLA, on 15,968 (clip, attack) pairs. We find a conservative-aggregate gap: an aggregate safe threshold of $\sigma \leq 50$ under a 15% average displacement error (ADE) budget masks well-sampled scenarios that tolerate the top of the tested grid ($\sigma = 70$). A Gaussian Mixture Model (GMM) on the changed-explanation subset identifies six discrete severity bands (BIC-optimal $k{=}6$), so two perturbation conditions with the same mean error can differ materially in their share of high-severity (C4/C5) failures. Joining the two analyses on the same corpus surfaces a finding neither yields in isolation: the scenarios with the loosest noise thresholds are not those with the lowest high-severity rate: STOP_SIGNAL concentrates roughly $4\times$ the C4/C5 share of LANE_KEEPING despite tolerating a larger $\sigma$. A deployable SOTIF ODD specification for driving VLAs therefore requires a two-dimensional safety envelope, not a single aggregate value per hazard.

---

## 5. RT-VLA: Real-Time Vision-Language-Action Models via Knowledge Distillation

**Authors:** Xiangyu Huang, Zhenlin Hua, Han Zhou, Shounak Sural, Ragunathan Rajkumar
**arXiv:** [2606.14010](https://arxiv.org/abs/2606.14010)
**Categories:** Computer Vision and Pattern Recognition (cs.CV); Machine Learning (cs.LG); Robotics (cs.RO)

Vision-Language-Action (VLA) models have shown strong potential for end-to-end autonomous driving by jointly modeling visual perception, language reasoning, explainability and action prediction. However, their large vision-language backbones and reasoning modules introduce substantial inference latency and thereby prevent their deployment in the unforgiving reality of the road networks. We propose RT-VLA, a lightweight, distilled VLA model that transfers the driving and reasoning capabilities of the state-of-the-art SimLingo model into a compact student through multi-level supervised distillation. RT-VLA preserves language-based reasoning and supports post-hoc explanation through offline language analysis of safety-critical driving moments without adding latency to real-time control. Compared to the SimLingo teacher, RT-VLA maintains competitive closed-loop driving and language reasoning performance while reducing inference time by 44.8X in vision-only mode and 7.9X in vision+language mode. These results suggest that supervised distillation is a practical approach for building real-time, explainable VLA-style autonomous driving models.

---

## 6. PhysVLA: Towards Physically-Grounded VLA for Embodied Robotic Manipulation

**Authors:** Namai Chandra, Shriram Damodaran, Lin Wang
**arXiv:** [2606.13886](https://arxiv.org/abs/2606.13886)
**Categories:** Robotics (cs.RO); Computer Vision and Pattern Recognition (cs.CV); Machine Learning (cs.LG)

Vision-Language-Action (VLA) models excel at mapping visual inputs and natural language instructions directly to robotic control policies. However, because they are trained primarily to fit behavioural demonstration data, they do not explicitly enforce fundamental physical principles such as rigid-body dynamics or contact constraints. This exposes a critical physics gap: standard temporal smoothing applied on top of single-step or chunked VLAs trades trajectory quality for added failures that short-term memory cannot resolve. To bridge this gap, we introduce PhysVLA (Physics-VLA), a plug-and-play, inference-time framework designed to wrap any frozen VLA backbone without retraining, fine-tuning, or weight access, with less than 1 ms of overhead per control step. PhysVLA intercepts the predicted control action, captures only the simulator or system state, and applies a dual-layered correction: (i) a phase-aware finite-state machine that structures discrete task segments (approach, grasp, transport, and place), and (ii) a selective Euler-Lagrange gate that activates only when a dynamics oracle detects kinodynamic inconsistency. Evaluated across OpenVLA, OpenVLA-OFT, Force-VLA, and Generalist-VLA on LIBERO-Spatial with a 7-DoF Franka Panda, the framework delivers absolute success rate increases of up to 17% and stability increases of up to 19% with no per-task regressions, improves trajectory efficiency by up to 15% across all four backbones, and shows up to a 10x improvement in trajectory jerk robustness on a Robosuite Lift cross-simulator sweep. We further validate the framework on a real Agilex Piper arm with a pick-and-place task, confirming that PhysVLA transfers to physical hardware without retraining, with success-rate improvements of up to 50%, establishing physical awareness as a composable, backbone-agnostic runtime module.

---

## 7. FlowMo-WM: A World Model with Object Momentum and Hidden Ambient Drift

**Authors:** Yitao Jiang, Luyang Zhao, Muhao Chen, Devin Balkcom
**arXiv:** [2606.13817](https://arxiv.org/abs/2606.13817)
**Categories:** Robotics (cs.RO); Machine Learning (cs.LG)

World models in robot learning predict future states from visual observations and actions, enabling agents to reason about the consequences of their controls. However, many action-conditioned models are evaluated in settings where motion is dominated by immediate control, whereas aquatic surface vehicles and other real-world objects continue moving under inertia and are displaced by hidden ambient drift, such as water currents or wind. We propose FlowMo-WM, an end-to-end trainable visual world model that infers object-centric motion state and a predictive long-history context associated with hidden drift from image-action histories without direct supervision of flow fields. FlowMo-WM factorizes image-action history into a short-history latent state, trained to summarize object-centric motion, and a longer-history context, trained to summarize slowly varying exogenous influences. A zero-context residual transition separates action-conditioned base dynamics from context-dependent drift effects during latent rollout. In simulated aquatic surface-vehicle environments with diverse hidden flows, disturbances, and randomized vehicle dynamics, FlowMo-WM improves long-horizon rollout accuracy over representative action-conditioned latent world models. Prediction-time context ablations, in which the inferred context is zeroed or shuffled during rollout, show that the ambient context is important for stable prediction under hidden drift, while frozen linear probes characterize information encoded in the learned factors.

---

## 8. $μ_0$: A Scalable 3D Interaction-Trace World Model

**Authors:** Seungjae Lee, Yoonkyo Jung, Jusuk Lee, ..., Jia-Bin Huang, Furong Huang
**arXiv:** [2606.13769](https://arxiv.org/abs/2606.13769)
**Categories:** Robotics (cs.RO); Computer Vision and Pattern Recognition (cs.CV); Machine Learning (cs.LG)

World models that capture how actions induce physical change enable scalable robot learning without reliance on embodiment-specific action labels. Pixel-space video models provide broad visual priors but expend model capacity on dense appearance reconstruction, while direct action models require embodiment-specific labels that hinder scalability. We present $\mu_0$, a scalable world model based on 3D traces. Rather than predicting dense pixels or directly modeling actions, $\mu_0$ forecasts smooth 3D trajectories for salient interaction points such as objects, tools, hands, and contact regions, yielding a compact, embodiment-agnostic motion interface. To enable training from diverse video sources, our TraceExtract system automatically extracts 3D supervision by selecting keypoints, constructing globally aligned traces, and associating motion segments with hierarchical language captions. This TraceExtract supervision pretrains $\mu_0$ by combining a pretrained vision-language backbone with a modular trace expert, which represents each query via B-spline control points and predicts future traces. Experiments show that $\mu_0$ outperforms baselines in both 2D and 3D trace prediction, including trace prediction models and tokenized VLM methods. Because $\mu_0$ is frozen and reusable, it can be paired with action experts for downstream robot embodiments. Despite action-free pretraining, the resulting trace-conditioned policies achieve performance competitive with VLA models pretrained with action supervision, such as $\pi_0$. These results establish 3D traces as a scalable and transferable representation for cross-embodiment manipulation.

---

## 9. ReactVLA: Fast and Lightweight Reactive Robot Manipulation via Improved Mean Flow Action Generation

**Authors:** Yanzhao Guo, Wenkai Chen, Jianwei Zhang
**arXiv:** [2606.14255](https://arxiv.org/abs/2606.14255)
**Categories:** Robotics (cs.RO)

Diffusion-based Vision-Language-Action (VLA) policies have demonstrated strong capability in modeling expressive and multimodal action distributions. However, their reliance on iterative sampling introduces substantial inference latency, which limits their applicability to reactive closed-loop robot manipulation. To address this limitation, we propose \texttt{ReactVLA}, a lightweight and low-latency VLA framework for real-time robotic manipulation. \texttt{ReactVLA} combines two complementary designs: (1) an improved Mean Flow (iMF) action generator that reduces expensive multi-step diffusion sampling to one-to-few-step action generation, and (2) Attention Residuals (AttnRes), a dynamic depth-wise feature routing mechanism that replaces uniform residual accumulation to better preserve task-relevant multimodal representations. We evaluate \texttt{ReactVLA} on large-scale simulation benchmarks, including LIBERO and RoboIMI, as well as real-world robotic manipulation tasks. Experimental results show that \texttt{ReactVLA} consistently outperforms similarly sized VLA baselines, including SmolVLA and $\pi_0$. On challenging precision manipulation tasks, \texttt{ReactVLA} achieves up to a 1.65$\times$ improvement in task performance while providing more than a 4$\times$ increase in inference speed compared with leading VLA models. Finally, it reduces real-world policy latency to below 38.6 ms, enabling fast reactive control on physical robot platforms. Please check out our project website at: this https URL.

---

## 10. Self-Improving VLA Policies: Selected Diffusion Noise for Spurious-Robust Action Smoothing

**Authors:** Duc Minh Nguyen, Bao-Ngoc Dao, Tung M. Luu, ..., Duy M. H. Nguyen, Vien Anh Ngo
**arXiv:** [2606.14084](https://arxiv.org/abs/2606.14084)
**Categories:** Robotics (cs.RO)

Diffusion-based Vision-Language-Action (VLA) policies enable strong generalization in robotic manipulation, but remain sensitive to spurious visual correlations and noisy action generation, leading to brittle behavior under perturbations. We introduce Selected Diffusion Noise (SDN), a simple, training-free test-time method that improves both robustness and success rate by leveraging the diffusion noise space as a controllable degree of freedom. SDN dynamically samples noise vectors that are maximally separated from a reference set to mitigate reliance on spurious cues, while selecting candidates that yield more coherent action trajectories. This dual objective encourages stable behavior even under object-masked observations and reduces action jitter without modifying model parameters. We evaluate SDN on two simulation benchmarks (Google Robot, Widow-X) and two real-world robotic datasets across multiple VLA policies, including pi_0, Groot-N1.5, and Groot-N1.6. SDN consistently improves success rates by +8% in simulation and +10% in real-world settings, while producing smoother and more stable actions. Our results highlight that diffusion noise selection can serve as an effective and general mechanism for enhancing VLA policies at test time.

---

## 11. ReactSim-Bench: Benchmarking Reactive Behavior World Model Simulation in Autonomous Driving

**Authors:** Zhiyuan Zhang, Yanlun Peng, Jianing Zhang, ..., Xiaosong Jia, Junchi Yan
**arXiv:** [2606.14058](https://arxiv.org/abs/2606.14058)
**Categories:** Robotics (cs.RO)

Reactive capability is a key property of data-driven behavior world model simulators for autonomous driving simulation systems. With this capability, simulated world agents can respond feasibly to autonomous vehicle (AV) behaviors that differ from the log. However, existing behavior simulation benchmarks do not directly measure reactive capability. They often let the simulator jointly control the AV and surrounding agents and evaluate realism through log similarity or open-loop prediction metrics. In this work, we introduce ReactSim-Bench for evaluating the reactive capability of behavior world model simulation in autonomous driving. We decouple the control of agents and the AV, using AV behaviors that differ from the log and require agents to respond as independent AV inputs. To obtain these AV behaviors, we construct a pipeline that uses an AV planner model to generate candidate behaviors and filters the data using rules and manual verification. Collision metrics, map-based metrics, and kinematic feasibility metrics are used to evaluate the safety and rule compliance of reactive responses. We construct 2,636 test scenarios with three categories and conduct a systematic evaluation of state-of-the-art models across multiple architectures, including Transformer-based, diffusion-based, and next-token-prediction-based models. We further analyze how replan frequency affects performance and provide insights for future studies.

---

## 12. ContactWorld: What Matters in Vision-Tactile World Models for Contact-Rich Manipulation

**Authors:** Zhiyuan Zhang, Pokuang Zhou, Kaidi Zhang, ..., Minghui Zheng, Yu She
**arXiv:** [2606.13877](https://arxiv.org/abs/2606.13877)
**Categories:** Robotics (cs.RO)

Contact-rich manipulation requires world models to reason over complex contact dynamics from multimodal sensory observations. However, it remains unclear which representation properties fundamentally support stable long-horizon planning in contact-rich settings. In this paper, we present ContactWorld, a benchmark and systematic empirical study of vision-tactile world models spanning 12 contact-rich manipulation tasks, including insertion, disassembly, screwing, and exploratory interaction. Across extensive experiments, we find that representations that are both spatially structured and temporally continuous consistently achieve the strongest planning performance. In particular, point-cloud observations improve average planning success rates from 20.7% with wrist-view observations and 22.0% with front-view observations to 32.1%. We further find that the effectiveness of tactile sensing depends critically on cross-modal representation compatibility rather than modality scaling alone. Combining point-cloud observations with tactile force-field representations, which preserve richer spatial structure and interaction dynamics, further improves performance to 36.1%, yielding the strongest overall planning performance across all evaluated tasks. Moreover, tactile sensing becomes increasingly important under long-horizon planning objectives, where compounding prediction errors and contact uncertainty accumulate over time. Together, these findings highlight the importance of representation structure, multimodal compatibility, and long-horizon robustness in vision-tactile world models for contact-rich robotic manipulation.

---

## 13. Output-Level Regularization Eliminates the Seed Lottery in Single-GPU VLA Fine-Tuning

**Authors:** Jeffrin Sam, Dzmitry Tsetserukou
**arXiv:** [2606.13856](https://arxiv.org/abs/2606.13856)
**Categories:** Robotics (cs.RO)

Fine-tuning a vision-language-action model (VLA-JEPA) on a single GPU should be simple: load a pretrained checkpoint, run training, deploy. There is a hidden danger. Run the same fine-tuning code thirteen times -- same data, same architecture, different random seed -- and twelve runs produce a robot succeeding 91--94% of the time, while one run silently degrades to 65.2%: a 29 pp gap with no error message, no warning, and no way to predict which seed will fail. We call this the seed lottery. We trace the cause to output collapse: the action predictor quietly learns to produce nearly identical outputs regardless of what the robot sees. Existing weight-level methods (L2, EWC) are structurally blind to this collapse -- they penalize weight changes, but collapse occurs in directions weights can move freely without affecting outputs, a gap we formalize via the Jacobian null-space. Across 7 methods x up to 13 seeds x 3 LIBERO benchmarks, three output-level regularizers -- VICReg (n=12 seeds), Dropout (n=4), and a halved learning rate (n=5) -- each eliminate every catastrophic seed (0/21 combined collapses vs. 1/13 Baseline; F(12,11)=28.7, p<0.001), while weight-level methods (L2, EWC) preserve the lottery. The simplest fix is changing one number in your optimizer config.

---

## 14. Multi-Agent Embodied Autonomous Driving: From V2X Information Exchange to Shared World Models

**Authors:** Senkang Hu, Zhengru Fang, Yihang Tao, ..., Sam Tak Wu Kwong, Yuguang Fang
**arXiv:** [2606.13840](https://arxiv.org/abs/2606.13840)
**Categories:** Robotics (cs.RO); Computer Vision and Pattern Recognition (cs.CV)

Autonomous driving is shifting from isolated vehicle intelligence toward multi-agent embodied systems that share perception, infer intent, and coordinate action under uncertainty. This survey examines this transition through the lens of Shared World Models (SWMs): predictive cross-agent representations maintained across vehicles, infrastructure, and other traffic participants. We review more than 380 publications spanning vehicle-to-everything (V2X) communication, collaborative perception, inter-agent cognition, cooperative planning, end-to-end cooperative driving, and simulation and data engines for closed-loop validation. The organizing question is how exchanged observations become aligned state, intent-aware interaction, and coordinated downstream action. Across the surveyed literature, evaluation remains concentrated in simulation, curated benchmarks, and offline protocols. Foundation-model-based coordination also lacks verified real-time safety guarantees in open traffic. These gaps motivate key research priorities for multi-agent embodied autonomous driving (MAEAD): verifiable shared-state maintenance, robust intent and plan alignment, and safe coordinated action under communication, latency, and deployment constraints.

---

## 15. Encoder Winners Do Not Reliably Transfer Across VLA Backbone Scale: A Frozen-Backbone Grafting Diagnostic

**Authors:** Qingping Zeng, Fei She
**arXiv:** [2606.14153](https://arxiv.org/abs/2606.14153)
**Categories:** Computer Vision and Pattern Recognition (cs.CV); Robotics (cs.RO)

Vision-language-action (VLA) policies typically inherit their vision encoder from upstream VLM releases, but it is unclear whether an encoder choice validated on a small VLA transfers to a larger backbone. We introduce a frozen-backbone grafting diagnostic: the vision tower of a released VLA is replaced by a candidate encoder under a fixed protocol (adaptive average pooling, LayerNorm, and a single trainable linear projector), with the language model and action expert frozen. Across four encoders, two LIBERO suites, two backbones (SmolVLA-450M and $\pi_{0.5}$-3.3B), and two-to-three seeds per cell (40 main grafting runs plus native, LoRA, pooling, and zero-/shuffled-image controls, all scored by offline action MSE), the small-backbone winner does not reliably select the large-backbone top tier: SigLIP is best on SmolVLA across both suites, while on $\pi_{0.5}$ DINOv2-small leads the spatial suite and the object suite is a seed-sensitive near-tie band; three of the four backbone-suite comparisons (and 11 of 12 seed-level cells) support backbone-dependent rankings. The grafting wrapper is itself non-neutral with opposite sign across backbones (+45-56% MSE on the SmolVLA native tower, -50-52% on $\pi_{0.5}$), so all conclusions are conditional on the fixed grafting protocol. We position frozen grafting as a cheap target-backbone diagnostic to run before committing to an encoder at scale, not as a closed-loop deployment claim.

---

## 16. WAM4D: Fast 4D World Action Model via Spatial Register Tokens

**Authors:** Ying Li, Xiaobao Wei, Jiajun Cao, ..., Sirui Han, Shanghang Zhang
**arXiv:** [2606.14048](https://arxiv.org/abs/2606.14048)
**Categories:** Computer Vision and Pattern Recognition (cs.CV); Robotics (cs.RO)

World action models (WAMs) have recently shown promise in jointly modeling future observations and executable robot actions. However, most existing WAMs still operate in 2D video or latent spaces, where visually plausible rollouts miss the 3D spatial constraints and occluded contact geometry required for precise manipulation. While geometric foundation models offer strong priors for recovering dense 3D structure and motion from visual observations, forcing WAMs to predict the dense 4D representation introduces costly geometric decoding and slows down causal action generation. To address the trade-off, we present WAM4D, a fast 4D world action model that uses lightweight spatial register tokens as training-time future-depth readouts to transfer pretrained geometric priors into a causal video-action transformer, then removes the register branch for lightweight action inference. To prevent non-causal shortcuts, we further design causal mixture attention for the Mixture-of-Transformers (MoT) WAM backbone, defining modality-specific visibility among video, action, and geometry tokens. Comprehensive experiments on RoboTwin 2.0 and challenging real-world manipulation tasks show that WAM4D improves spatial consistency and achieves competitive action prediction while maintaining efficient inference.

---

## 17. Causal Object-Centric Models for Planning with Monte Carlo Tree Search

**Authors:** Rodion Vakhitov, Leonid Ugadiarov, Alexey Skrynnik, Aleksandr Panov
**arXiv:** [2606.14418](https://arxiv.org/abs/2606.14418)
**Categories:** Artificial Intelligence (cs.AI); Machine Learning (cs.LG); Robotics (cs.RO)

We introduce COMET (Causal Object-centric Model for Efficient Tree search), a model-based reinforcement learning algorithm that performs Monte Carlo Tree Search in a slot-structured latent space. COMET pairs a frozen unsupervised object-centric encoder with a transformer-based world model, in which actions are bound to objects through a novel action-slot fusion mechanism that is used in slot transition prediction. Policy and value heads use object-causal attention, modulating token interactions by learned per-slot relevance scores so that decision-making concentrates on task-relevant entities. COMET adds an explicit object-level inductive bias to MuZero-style latent planning. Across eight visually and dynamically diverse tasks from the Object-Centric Visual RL benchmark, ManiSkill, Robosuite, and VizDoom, COMET achieves a higher mean normalized score during the early stages of training compared to object-centric and monolithic baselines.

---
