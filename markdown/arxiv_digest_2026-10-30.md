# arXiv Daily Digest — 2026-10-30

**Mode:** direct
**Categories:** cs.AI, cs.LG, cs.RO, cs.CV
**Keywords:** VLA, RSI, agentic robot, self-improving robot, self-evolving robot, robot harness
**Papers found:** 13

---

## 1. MoLRSI: A Recursive Self-Improving AI agent for Molecular Discovery

**Authors:** Yikun Zhang, Xiwei Cheng, Mingze Yuan, ..., James J. Collins, Wengong Jin
**arXiv:** [2610.39714](https://arxiv.org/abs/2610.39714)
**Categories:** Artificial Intelligence (cs.AI)

Molecular discovery requires navigating vast combinatorial search spaces while balancing competing biological objectives. AI agents can automate expert-defined molecular design protocols, but automation alone does not address how to optimize workflows for new tasks or improve their development through experience. Here we introduce MoLRSI, an AI agent that combines systematic optimization of workflows and model architectures with persistent cross-task memory to recursively improve its search policy for molecular discovery. Workflow performance, refinement outcomes, and execution feedback guide subsequent searches, allowing the agent to improve both its workflows and its strategy for developing them. We evaluate MoLRSI in two challenging molecular discovery settings that require balancing competing properties. In antibiotic discovery, MoLRSI developed a screening workflow balancing antibacterial activity, cytotoxicity and structural novelty, achieving an experimental hit rate of 15.9%, compared with 8.7% for a previous expert-led workflow using the same training data and screening library. In de novo peptide-MHC binder design, MoLRSI developed workflows that jointly consider target binding and specificity, producing eight experimentally validated hits against MART-1 and SARS-CoV-1 pMHCs with preferential binding over tested off-targets while Claude Science completely failed. These findings demonstrate how experience-guided workflow optimization can address competing discovery objectives while improving the search strategies used in subsequent campaigns.

---

## 2. A-RSI: Adaptive Task Refresh for Zero-Data Multimodal Self-Improvement

**Authors:** Yu Liu, Youxing Li, Yuedong Tan, ..., Barnabas Poczos, Jian Luan
**arXiv:** [2610.38568](https://arxiv.org/abs/2610.38568)
**Categories:** Artificial Intelligence (cs.AI)

Recursive self-improvement requires models not only to acquire useful training experience, but also to decide when their current experience has ceased to be useful. Existing methods often focus on what experience to generate next, while paying less attention to when fresh experience should be introduced. Many also construct training targets through self-consistency or majority voting, making supervision depend on the model's own uncertain predictions. We address these two questions separately: training dynamics determine when to acquire new experience, while the answers to new tasks remain independently checkable. A-RSI monitors reward variation and accuracy in training logs to refresh a task pool when its learning signal declines, without consulting validation or test scores. A static library of model-authored programs produces multimodal questions and derives their reference answers; we specify the task-generation contract, automatically verify chosen properties of the reward and refresh rules, and separately audit the generated answers. The training loop uses no external training examples or human-written answer labels. On the primary eleven-benchmark suite, A-RSI raises the performance average from 57.77 to 61.05 with 800 fresh tasks.

---

## 3. SaiVLA-JEPA: Evaluating Future Latent Prediction in JEPA-Conditioned VLA Control

**Authors:** Rufeng Xiao, Ruihao Xiao, Wei Chen, Xinhai Sun
**arXiv:** [2610.38508](https://arxiv.org/abs/2610.38508)
**Categories:** Robotics (cs.RO); Artificial Intelligence (cs.AI)

Joint-embedding predictive architectures (JEPAs) learn to predict representations rather than pixels, offering a compact way to model how visual scenes evolve. We ask whether this predictive objective improves closed-loop control when a vision-language-action (VLA) policy already uses V-JEPA features. We call our JEPA-conditioned flow policy family SaiVLA-JEPA. It combines a vision-language model with a diffusion transformer action expert and receives features from a frozen V-JEPA encoder. Two lightweight auxiliary heads predict future representations during training and are omitted at inference, leaving the action sampler unchanged. We compare policies without JEPA features, with current JEPA conditioning, and with additional future supervision on 10,030 paired LIBERO-Plus episodes. Current JEPA conditioning reaches about 82.5% success versus 71.6% without JEPA, while future supervision provides no detectable aggregate gain at the evaluated training budget. We separately evaluate SaiVLA-JEPA-TCA, which adapts latent context, and SaiVLA-JEPA-TPA, which adapts selected parameters. The context-retry gain is a system-level result under a larger attempt budget; parameter adaptation shows no consistent advantage over the frozen policy and target controls. These results motivate assessing latent-prediction objectives through paired closed-loop rollouts rather than latent loss alone.

---

## 4. How Much Should a VLA Trust Its Reasoning? Step-Level Guidance as a Measured Action-Value Function

**Authors:** Dabin Seo, Eunhyek Joa
**arXiv:** [2610.40002](https://arxiv.org/abs/2610.40002)
**Categories:** Robotics (cs.RO); Computer Vision and Pattern Recognition (cs.CV); Machine Learning (cs.LG)

Reasoning vision-language-action (VLA) policies write a reasoning trace and then decode the action from it. A wrong trace yields a wrong action, and even a correct-looking trace can mislead the plan. Existing remedies ask whether the reasoning is right. We ask how strongly it should steer. CoC-CFG applies classifier-free guidance between the policy's context and the same context without the reasoning span. One weight per Euler step attenuates or amplifies the reasoning, and w=1 recovers the original policy. We treat the choice of this weight as a Markov decision process whose action values are measured, not bootstrapped. With the expert frozen and the noise fixed, applying a weight for one step and finishing the plan under the current controller returns that weight's value exactly. Q-adaptive guidance fits these values with small critics and improves the controller conservatively. In the Alpasim driving simulator it outperforms every fixed weight and online RL (SAC, GRPO) in open loop, and in closed loop it passes 262 of 300 scenes, against 252 for the original policy. On held-out frames of the Waymo end-to-end driving benchmark, its first three stages outperform every fixed weight, four adaptive-guidance methods, SAC and GRPO. On the hidden test set, a frozen Alpamayo 1.5 with rule-based camera and vehicle conversions and Q-adaptive guidance sets a new state of the art among published methods: 8.135159 rater feedback score, against 8.079 for the best published method.

---

## 5. RoboSeed: Multidimensional Evaluation of Vision-Language-Action and World-Action Models: Capability, Resource Affordability, and Research Evidence

**Authors:** Xin Ma, Furong Chen, Xinlong Man, ..., Lap-pui Chau, Chuang Yang
**arXiv:** [2610.40026](https://arxiv.org/abs/2610.40026)
**Categories:** Robotics (cs.RO)

Choosing a robot action model requires evidence about task capability, adaptation cost, deployment requirements, and the reliability of reported conclusions. Success rates alone offer limited guidance to researchers with different computing budgets and goals. We propose RoboSeed, a multidimensional evaluation framework for vision-language-action (VLA) and world-action models (WAM), within a continuing program to train, evaluate, and openly release robot models with verifiable evidence for model selection.
The framework defines five dimensions: capability, downstream training affordability, deployment affordability, locally verified research value, and reproduction evidence. It maps empirical measurements and audit criteria to 0-100 profiles using fixed normalization anchors, with balanced, training-constrained, and deployment-constrained preference settings. Interface and protocol checks establish when comparisons are appropriate. Missing measurements remain explicit, incomplete aggregate scores are withheld, and weighted input coverage identifies evidence gaps.
We apply the framework to representative VLA and WAM models, drawing on local training, released-weight evaluation, task-level audits, and an evaluation-system study. The results reveal budget-dependent backbone choices, sensitivity to adaptation recipes, and differences between language and visual task interfaces. Reproducible scoring code and machine-readable evidence support extension to additional models. The study provides dimension-level assessments and priorities for further measurement, while incomplete serving traces and heterogeneous protocols preclude overall numerical rankings.

---

## 6. From Reasoning to Action: Consequence-Grounded Alignment for Vision-Language-Action Models

**Authors:** Yixue Zhang, Wenke Xia, Kun Wu, ..., Zhengping Che, Chang Liu
**arXiv:** [2610.39543](https://arxiv.org/abs/2610.39543)
**Categories:** Robotics (cs.RO)

Reasoning informs decision-making by connecting intended actions with their expected consequences. Recent vision-language-action (VLA) models incorporate embodied chains of thought (ECoTs) to guide action generation. However, such guidance remains implicit, as actions are conditioned on ECoTs rather than explicitly optimized to align with them.
We introduce CoRAct, a consequence-grounded reasoning-to-action alignment framework that explicitly aligns reasoning and action through reward-guided optimization in action noise space. CoRAct formulates two physically grounded ECoT components as verifiable signals: movement specifies intended motion, while waypoints encode expected spatial consequences. A unified Mixture-of-Transformers jointly models ECoT reasoning, action generation, and action-conditioned future prediction. For candidate actions generated from sampled noise, CoRAct computes alignment rewards based on movement consistency and agreement between predicted outcomes and specified waypoints. These rewards guide group-relative optimization of the initial noise distribution, steering action generation toward consistency with intended actions and expected consequences.
Experiments across RoboCasa, VLABench, and real-world manipulation tasks demonstrate improvements in task success, generalization, and reasoning-execution alignment over strong ECoT-based VLA baselines. CoRAct also grounds externally provided ECoTs in executable behavior, enabling zero-shot adaptation to novel scenarios by leveraging knowledge from powerful vision-language models.
Project page and dataset: this https URL

---

## 7. OpenFlyV2: An onboard vision-language-action model for aerial perception and navigation

**Authors:** Junli Liu, Zhongrui You, Chenhui Li, ..., Zhigang Wang, Bin Zhao
**arXiv:** [2610.39287](https://arxiv.org/abs/2610.39287)
**Categories:** Robotics (cs.RO)

Human cognition flexibly draws on a shared perceptual foundation to understand environments, attend to referenced entities, reason about spatial relationships, and act. Endowing aerial robots with an analogous functional organization remains challenging, as existing systems are often specialized for individual capabilities, dependent on offboard computation, or unable to sustain closed-loop operation on resource-constrained platforms. We present OpenFlyV2, a unified onboard vision-language-action architecture that uses a shared vision-language representation to support semantic understanding, language-grounded perception, spatial reasoning, and continuous aerial control within a single model. A compact action expert converts the shared multimodal context into short-horizon flight waypoints, while motion-aware temporal memory and action priors reduce the computational cost of closed-loop execution. We construct \dataset{}, a simulation-based dataset comprising approximately 70,000 navigation trajectories and 60,000 vision-language instruction--response pairs. OpenFlyV2 generates action chunks, each comprising 12 waypoints, entirely onboard at 10 Hz using an NVIDIA Jetson Orin NX. It transfers zero-shot from simulation to physical quadrotor flight, achieving a 48\% navigation success rate across four real-world environments without real-world aerial training data. Extensive results demonstrate that broad vision-language competence and continuous closed-loop flight can coexist within a single model on a resource-constrained aerial platform. Code will be made publicly available at this https URL.

---

## 8. Quantize by Doing: Task-Guided Mixed-Precision Quantization of Vision-Language-Action Models

**Authors:** Jiuyi Xu, Xiao Hu, Meida Chen, ..., Yang Ye, Yangming Shi
**arXiv:** [2610.38661](https://arxiv.org/abs/2610.38661)
**Categories:** Robotics (cs.RO)

Post-training quantization (PTQ) reduces the memory footprint of vision-language-action (VLA) models, but lowering bit widths while maintaining task performance remains challenging. Existing work has used sensitivity estimates from calibration data to assign bit widths to different model components. However, using task success directly to guide mixed-precision allocation is underexplored because closed-loop evaluations are costly and the effect of quantizing one component depends on the precision of other components. To this end, we propose \textbf{QbD-VLA}, a task-guided mixed-precision quantization method that uses task success from short closed-loop evaluations to assign weight and activation bit widths while accounting for interactions between model components. Experiments covering four VLA models and all four LIBERO suites show strong task performance at average precisions of approximately 4 bits for weights and fewer than 6 bits for activations. On SIMPLER, the gain over uniform quantization is small. On a Franka Research 3 robot arm, simulation-selected allocations show no detected success-rate loss on X-VLA but fail on $\pi_{0.5}$. These findings support using task success to guide mixed-precision VLA quantization, while highlighting the need for real-world evaluation before deployment. Code is available at \href{this https URL}{\texttt{this http URL}}.

---

## 9. Recursive Self-Improvement in Physical AI: Mechanisms, Evidence, and Evaluation

**Authors:** Xiaofeng Han, Kaize Luo, Zenghuang Fu, ..., Weiliang Meng, Xiaopeng Zhang
**arXiv:** [2610.38266](https://arxiv.org/abs/2610.38266)
**Categories:** Robotics (cs.RO)

Embodied systems can update policies, world models, skills, and executable programs from deployment experience, allowing one interaction to benefit later tasks. When a system also revises and reuses its data-acquisition, feedback, or learning procedures, experience changes the process that produces capability, introducing recursive self-improvement. This paper surveys research in physical AI through the connection between persistent capability and its improvement process. We first explain the functional distinction between learner updates and improvers, then compare policy learning, imagined experience, memory and skill accumulation, and executable harnesses. These approaches connect to revisions of curricula, rewards, and research programs in different ways. Contact validity, recovery, retention, and resource costs determine whether the resulting gains accumulate during continued deployment. An L0-L3 rubric distinguishes task-local adaptation, persistent capability gain, inherited process revision, and verified improver gain. Representative benchmarks and within-study contrasts relate these distinctions to existing results. We further propose common-data and interactive comparisons that evaluate reference and revised improvers from shared learner starts, separating the use of experience from its acquisition. This perspective connects the diverse methods, physical operating conditions, and evaluation evidence, underpinning embodied RSI. A comprehensive list of studies in this survey is available at this https URL.

---

## 10. HiFOR: Hierarchical Foresight with Action-Guided World Grounding for Vision-Language-Action Model

**Authors:** Rongxing Ding, Hongyu Qu, Kehong Wu, ..., Xinguang Xiang, Xiangbo Shu
**arXiv:** [2610.40373](https://arxiv.org/abs/2610.40373)
**Categories:** Computer Vision and Pattern Recognition (cs.CV); Robotics (cs.RO)

Vision-Language-Action (VLA) models have demonstrated promising capabilities in robotic manipulation by integrating visual perception, language understanding, and action generation. Recent advances have further incorporated future prediction to enhance the understanding of environmental dynamics and task progression. However, existing methods often model short-term dynamics and long-term task objectives separately, while directly incorporating predicted futures into action policies without sufficiently considering their relevance to current action requirements. To address these limitations, we propose HiFOR, a hierarchical foresight framework with action-guided world retrieval. Specifically, Hierarchical Foresight Prediction jointly predicts short-term state evolution, semantic milestones, and final goal states through a Hierarchical Dependency Mask (HDM), establishing dependencies across temporal horizons. Building upon these predictions, Structure-Aware Latent World Modeling organizes future latent representations along the horizon, view, and spatial dimensions to facilitate fine-grained retrieval. Furthermore, Action-Guided Factorized World Retrieval adaptively retrieves relevant future information from the structured latent world based on evolving action representations during denoising, providing targeted guidance for action generation. Extensive experiments on two simulation benchmarks and six real-world robotic manipulation tasks demonstrate the effectiveness of our approach.

---

## 11. Video Generation Meets Agent Harness: Agentic Video Generation, Agentic World Modeling and Recursive Self-Improvement

**Authors:** Liaoyuan Fan, Yuhao Zheng, Dongxing Mao, ..., Mike Zheng Shou, Wei Liu
**arXiv:** [2610.40191](https://arxiv.org/abs/2610.40191)
**Categories:** Computer Vision and Pattern Recognition (cs.CV)

Video generation is shifting from end-to-end synthesis toward agentic generation, where planning, tool use, and feedback enable coherent, controllable multi-shot videos. In parallel, video world models provide action-conditioned observations and predicted futures, serving as interactive environments for agents. We study their intersection through the agent harness: an executable runtime that constructs context, exposes tools, maintains state, routes feedback, and manages budgets around video models. This report examines three directions. First, agentic video generation, where harnesses coordinate scripting, shot planning, asset management, production, and editing, alongside the evaluation challenges of these systems. Second, agentic world modeling, where harnesses mediate observation, control, execution, and state. We discuss hybrid designs in which game engines or agent-written programs maintain world state while video models render observations, and how agents and world models can mutually evaluate and improve one another. Third, recursive self-improvement (RSI) in video model development, distinguishing output revisions, updates to harness state, generator parameters, and evaluators, and changes to the improvement procedure itself. We identify how these improvements feed back into subsequent development. Across these directions, we analyze essential agent capabilities, including audiovisual perception, long-horizon planning, memory, code-based interaction, feedback-guided control, skill reuse, and multi-agent coordination. We conclude with challenges in autonomous video production, lifelong memory, programmable hybrid control, autonomous model development, provenance, cost accounting, and evaluation linking video quality and task performance to sustained improvements in models and harnesses.

---

## 12. UMI-Live for In-The-Wild Bimanual Robotics Data Collection

**Authors:** Govind Velamoor, Adrian Lin, Sam Jung, ..., Brandon Y. Yang, Amish Sethi
**arXiv:** [2610.39385](https://arxiv.org/abs/2610.39385)
**Categories:** Robotics (cs.RO); Artificial Intelligence (cs.AI)

Universal Manipulation Interface (UMI) devices allow human experts to demonstrate tasks for robot learning without teleoperating physical robots. Using these demonstrations as training data still requires a consistent hardware setup, calibration, and data processing. We present UMI-Live, a full-stack open-source bimanual UMI system for in-the-wild data collection. We design our custom UMI-Live hardware to integrate camera and LiDAR--inertial sensing, onboard compute, and power, without external tracking equipment or calibration within the collection environment. We implement a simple user interface for recording data while an asynchronous pipeline performs parallel SLAM reconstruction and publishes training-ready datasets. We also release software that supports dual-YAM teleoperation and VLA policy training and inference. We validate UMI-Live data quality by fine-tuning $\pi_{0.5}$ and MolmoAct2, achieving success rates of 10/10 and 8/10, respectively on a bimanual pick-and-place task. Furthermore, we release 40 hours of UMI-Live data across three tasks, and complete hardware designs, software, and reproduction guides at our $\href{this https URL}{\text{project website}}$.

---

## 13. LaWAM: Latent World Action Models for Efficient Dynamics-Aware Robot Policies

**Authors:** Jialei Chen, Kai Wang, Kang Chen, ..., Yuanbo Xu, Chao Yu
**arXiv:** [2606.15768](https://arxiv.org/abs/2606.15768)
**Categories:** Robotics (cs.RO); Artificial Intelligence (cs.AI); Computer Vision and Pattern Recognition (cs.CV)

Vision-Language-Action models (VLAs) leverage large-scale vision-language pretraining for semantic robot control, but often lack explicit foresight into how robot actions change the scene. World-Action Models (WAMs) address this limitation by conditioning policies on predicted futures, yet existing approaches typically rely on computationally expensive video generation with substantial pixel-level redundancy. We present LaWAM, a Latent World Action Model that exposes predictive dynamics to robot policies through compact latent visual subgoals instead of reconstructed future video. At the core of LaWAM is a latent-action-conditioned Latent World Model (LaWM). We obtain LaWM by training a latent action model in the latent space of a pretrained vision foundation model and repurposing its forward decoder to predict future observation features for scene evolution. LaWAM then conditions action generation on these predicted latent visual subgoals to enable dynamics-aware robot control. LaWAM achieves state-of-the-art or competitive success rates (SRs) across LIBERO (98.6% SR), RoboTwin (91.22% SR), and real-world manipulation tasks while retaining low-latency inference. LaWAM runs in 187 ms per action-chunk prediction and achieves up to 24x lower wall-clock latency than pixel-space WAMs.

---
