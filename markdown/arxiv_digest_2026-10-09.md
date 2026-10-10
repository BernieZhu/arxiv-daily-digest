# arXiv Daily Digest — 2026-10-09

**Mode:** direct
**Categories:** cs.AI, cs.LG, cs.RO, cs.CV
**Keywords:** VLA, RSI, agentic robot, self-improving robot, self-evolving robot, robot harness
**Papers found:** 16

---

## 1. Recursive Self-Improvement through Multi-Agent Self-Supervision

**Authors:** Hyunin Lee, Jinglue Xu, Jeffrey Seely, ..., Matei Zaharia, Yujin Tang
**arXiv:** [2610.12176](https://arxiv.org/abs/2610.12176)
**Categories:** Artificial Intelligence (cs.AI)

Recursive self-improvement (RSI) of a model on non-verifiable tasks, such as open-ended research, faces a supervision bottleneck when its outputs exceed what even human experts can reliably assess, leaving the model itself (optimizee) as the best available optimizer and evaluator. However, a single model instance struggles to critique and improve its own complex reasoning under this homogeneous loop. To address this, we propose Multi-Agent Self-Supervision (MASS), an RSI method that alternates between evolutionary workflow optimization and supervised fine-tuning on self-generated trajectories. Guided by early findings that multi-agent topologies excel at complex reasoning, MASS prompts a single base model to iteratively propose, execute, and self-evaluate multi-agent workflows. Through an evolutionary search constrained by structural guardrails, the model optimizes these computational-graph-like orchestrations, discovering the most effective distinct roles and information routing for a given task. Over two MASS cycles with Qwen3.6-27B, the model achieves 1.2-1.6x higher performance per output tokens on four open-ended public benchmarks. Because the improved model subsequently acts as a better optimizer and evaluator, this alternating framework enables a continuous, recursive bootstrapping of the model's capabilities. Moreover, multi-agent traces are also more training-efficient: a student trained on them outperforms a single-agent student trained on 1.4x more training tokens. These findings suggest that jointly learning orchestration and bounded subagent execution from multi-agent trajectories can provide an effective signal for RSI.

---

## 2. Recompose and Refine Latent Reasoning Flows for Vision-Language-Action Models

**Authors:** Hongyu Shi, Sen Zhao, Zuyu Zhang, ..., Xu Zhang, Qinghua Zhang
**arXiv:** [2610.12090](https://arxiv.org/abs/2610.12090)
**Categories:** Artificial Intelligence (cs.AI)

Latent reasoning enables vision-language-action (VLA) models to transform multimodal observations into task-relevant internal states before generating continuous robot actions. While existing methods learn to generate or refine such states for each policy query, they discard successful reasoning after execution and therefore reconstruct similar computation from scratch. We present Reasoning and Flow Memory (FLOWMEM), a unified VLA model that turns successful latent computation into reusable reasoning experience. Rather than appending a fixed retrieved context, FLOWMEM dynamically retrieves and recomposes compatible latent fragments as the embodied context evolves, forming a reasoning route that follows the temporal structure and progress of successful computation. The route is then refined using current visual and proprioceptive evidence before it conditions action generation. Experiments on RoboMME and LIBERO-Plus show that FLOWMEM attains 48.0% and 77.3% success, outperforming memory-free policies by 1.7 and 4.1 percentage points, respectively. These results demonstrate the value of reusing successful latent computation for closed-loop VLA control.

---

## 3. Memento 3: Model-Based Recursive Self-Improvement through Reflective Rulebooks

**Authors:** Haoyu Zhao, Zhengxu Yu, Zhiyuan He, ..., Weilin Luo, Jun Wang
**arXiv:** [2610.11794](https://arxiv.org/abs/2610.11794)
**Categories:** Artificial Intelligence (cs.AI); Computation and Language (cs.CL); Computer Vision and Pattern Recognition (cs.CV); Machine Learning (cs.LG)

Learning to act in unfamiliar environments requires agents to infer how the world works and revise that understanding as new evidence arrives. Yet limited observations can support multiple world models that explain past interactions but predict different outcomes in unseen states. We introduce Memento 3, building on the Memento series to enable frozen LLM agents to continually learn explicit world models through external memory. The agent maintains a natural-language rulebook as persistent semantic memory, recording revisable hypotheses about environment dynamics while leaving unknown aspects underspecified. It compiles this rulebook into executable code for prediction and planning. Through a continual loop of observation, reflection, rule revision, compilation, and verification, the agent uses prediction errors to refine both the rulebook and its code. Updated code is accepted only when the LLM judges it faithful to the rulebook and cell-exact replay reproduces the observed transitions. We investigate this process as a model-based route to recursive self-improvement (RSI): the agent autonomously explores the environment, revises its world model, and uses verified updates to guide subsequent interaction and learning, while the underlying LLM remains fixed. A population extension maintains multiple world models in parallel, sharing interaction evidence and using their predictions to guide exploration. On ARC-AGI-3, the single-model agent clears every level of all 25 public games, achieves a mean Relative Human Action Efficiency (RHAE) of 100.0, and uses 44% of the human action count. In an Atari Pong case study, a learned feedback controller wins 21:0 in each of three evaluated episodes with different openings, without further LLM calls.

---

## 4. DuplexAgent-RSI: Recursive Harness Improvement for Full-Duplex Voice Agent Collaboration

**Authors:** Yingda Shen, Yuxiang Wang, Kunyu Feng, ..., Yutong Bian, Zhizheng Wu
**arXiv:** [2610.11299](https://arxiv.org/abs/2610.11299)
**Categories:** Artificial Intelligence (cs.AI); Sound (cs.SD)

Voice agents are converging on a collaboration pattern: a full-duplex interaction model stays on the live channel as the entry to the conversation, while search, reasoning, and coding are handled through asynchronous delegation. A duplex model supports continuous listening and speaking, but complex reasoning and tool use may exceed its capabilities. A coding agent can plan and execute extended tasks, but its sequential interface is a poor fit for live conversation. Combining them requires a harness that coordinates task acceptance, progress, cancellation, replacement, and result delivery while keeping the conversation responsive. Existing harnesses often rely on coupled heuristics, making them difficult to improve systematically from evidence. We present DuplexAgent, a full-duplex collaboration system whose harness expresses this workflow as six editable modules, and Duplex-Harness-RSI, a closed loop that revises them from interaction traces. A simulator automatically generates timed test conversations, runs the system, and produces failure traces that identify the collaboration modules requiring repair. Reasoning LLMs and coding agents in the delegation pool also serve the improvement loop: the Exam Planner selects the next tests from observed weaknesses and the repair archive, and the Harness Editor proposes targeted module changes. The capabilities that serve the user thus also improve the system's coordination. Experiments on intelligence, agentic, and duplex benchmarks show that DuplexAgent combines continuous interaction with difficult reasoning and complex task execution, achieving stronger spoken-knowledge and executable-tool scores than the compared delegated systems while maintaining strong interruption response. A harness ablation further shows that this modular, verifiable loop outperforms the initial harness and repeated editing that lacks its diagnosis and repair archive.

---

## 5. RoboRSI: Stable, efficient, and reusable robot self-evolution in complex real-world environments

**Authors:** Zimo Wen, Yijin Chen, Yuxuan Cao, ..., Chuan Wen, Cewu Lu
**arXiv:** [2610.12424](https://arxiv.org/abs/2610.12424)
**Categories:** Robotics (cs.RO); Artificial Intelligence (cs.AI)

A generalist robot should not only perform diverse tasks but also improve through experience, turning what it learns during execution into capabilities that later tasks can reuse. Robot agents that act through code can already repair programs from execution feedback, yet it remains a central challenge to organize this experience around the task structure that gives it meaning, so that each repair is attributed to the responsible capability, supported by execution evidence, and validated before it is reused. We introduce RoboRSI, a robot self-improvement system built on Top-Down Skill Refinement (TSR). TSR decomposes tasks into compound, atomic, and base skills with scoped responsibilities and explicit input--output contracts, attributes each execution outcome to the responsible branch, and confines revision to that branch. Building upon this structure, a Manager, Planner, Engineer, and Reviewer coordinate planning, execution, diagnosis, and the validated release of new skills, while people steer the process through objectives and corrections; stable skill sequences are further consolidated into reusable compound skills. On a mobile manipulator, RoboRSI develops multi-object household cleanup over 104 rounds. In simulation, it achieves the highest success rate on LIBERO, LIBERO-PRO, LIBERO-Plus, and RoboTwin, exceeding the strongest baseline by 2.7 to 11.0 percentage points.

---

## 6. REACT: Rolling Denoising and Dual Decoupling for Reactive Robot Control with VLA Models

**Authors:** Houlong Xiong, Zhenqi Qiu, Zechen Wang, ..., Ran Cheng, Qian Zhu
**arXiv:** [2610.12007](https://arxiv.org/abs/2610.12007)
**Categories:** Robotics (cs.RO); Artificial Intelligence (cs.AI)

Flow-based vision-language-action (VLA) models generate action chunks for temporally coherent robot motion, but chunked control creates a fundamental closed-loop trade-off: long chunks provide smooth execution, whereas frequent replanning improves reactivity at the cost of action discontinuities. We introduce REACT, a rolling-denoising framework that makes flow-based VLAs more reactive while preserving long-horizon context. Instead of regenerating entire action chunks from scratch, REACT maintains a persistent action buffer with staggered flow timesteps. At each control step, the full horizon is denoised using the latest observation, the cleanest action block is executed, partially refined future blocks are shifted forward, and fresh noise is appended to the tail. As a result, each executed action block is refined across multiple recent observations before deployment. To support real-time control, we further introduce dual decoupling, which separates sensing, VLM encoding, DiT denoising, and action execution, enabling high-frequency observation updates and action streaming under practical compute constraints. Across the RoboTwin 2.0 simulation benchmark and real-world tasks spanning bimanual manipulation and dynamic control on multiple robot platforms, REACT improves task success and reduces reaction latency while producing smoother trajectories than frequent-replanning and asynchronous baselines.

---

## 7. DVLA-RL++: Dual-Level Vision-Language Alignment with Reinforcement Learning Gating for Few-Shot Learning

**Authors:** Wenhao Li, Xianjing Meng, Qiangchang Wang, ..., Yilong Yin, Liqiang Nie
**arXiv:** [2610.12095](https://arxiv.org/abs/2610.12095)
**Categories:** Computer Vision and Pattern Recognition (cs.CV); Machine Learning (cs.LG)

Few-shot learning aims to recognize novel categories from limited labeled examples. Recent studies incorporate textual semantics to compensate for limited visual observations and improve class representations. However, high image-text agreement may reflect both intrinsic object properties and incidental context, making support prototypes susceptible to contextual contamination. To address this problem, we propose DVLA-RL++, which extends DVLA-RL with complementary semantic purification (CSP) and counterfactual reinforcement-learning gating (CRG). Specifically, CSP generates intrinsic and nuisance descriptions from labeled supports and compares their agreement with each support token. An ambiguity-dependent rejection margin guides sparse evidence allocation, while an intrinsic semantic anchor fills the unassigned mass to provide a fallback when visual evidence is unreliable. CRG learns layer-wise semantic fusion strengths using a reward that balances recognition performance and nuisance exposure. An independently executed reference trajectory on the same episode provides a paired learning signal. Theoretical analysis relates retained evidence and anchor quality to prototype stability and establishes conditions for unbiased on-policy gradient estimation. Experiments on standard, fine-grained, and cross-domain benchmarks show state-of-the-art accuracy, with an average gain of 1.4% over DVLA-RL. The project page is available at this https URL.

---

## 8. When Listening Becomes Easier: Scrubbing Visual Cues for Shortcut-Free VLAs

**Authors:** Jasper Gerigk, Kenzo Aspuru-Takata, Chin-Hsuan Wu, ..., Shuhong Zheng, Igor Gilitschenski
**arXiv:** [2610.10912](https://arxiv.org/abs/2610.10912)
**Categories:** Robotics (cs.RO); Computer Vision and Pattern Recognition (cs.CV); Machine Learning (cs.LG)

Shortcut learning is a prevalent issue in robot learning. The limited diversity of robot demonstration datasets can mislead policies into exploiting spurious correlations between tasks and irrelevant features, such as viewpoint or background. Collecting sufficiently diverse robot demonstrations is costly and inefficient, motivating algorithmic alternatives. We focus on vision-language-action (VLA) models and discover that different vision-language model backbones exhibit substantially different levels of susceptibility to visual shortcut learning. We find that model behavior correlates with our proposed representation-level metric, action margin, which requires no policy rollouts. Visual shortcuts consistently enter action representations in early layers, with models differing in the extent to which later layers correct them by incorporating language information. To boost models' attention to language, we introduce task scrubbing, a new domain-adversarial training method that decreases models' likelihood of using visual shortcuts and improves VLAs' generalization. Experiments in both simulation and the real world across multiple VLAs and visual cues show that task scrubbing improves out-of-distribution robustness and often eliminates visual shortcut learning.

---

## 9. Embodied Turing Machines: Stateful Code for Robot Recursive Self-Improvement

**Authors:** Kairui Hu, Siyuan Hu, Fangzhou Hong, Zhaoxi Chen, Ziwei Liu
**arXiv:** [2610.12369](https://arxiv.org/abs/2610.12369)
**Categories:** Robotics (cs.RO); Computer Vision and Pattern Recognition (cs.CV)

Most robot policies keep a model in the control loop: a VLA maps observations to actions, and an Agent Harness, such as Agent-as-Policy or Harness VLA queries a VLM for decision making at run time. We propose a different view: the embodied world is an Embodied Turing Machine, whose tape is the robot and environment state and rules are the policy. If this state can be represented accurately, the decision making can be written entirely in code. We therefore propose Code-Only-as-Policy (COAP): code measures and tracks the robot, environment, and task state from camera images and proprioception, and makes every decision from it. The same code applies across episodes, and different tasks share one library without a VLM or VLA in the loop. Compared with VLAs and Agent Harnesses, we analyze three advantages of COAP: (i) Explicit State: the state can be stored in code; (ii) Execution: code makes decision making controllable, recovers from failures flexibly, and runs fast and cheaply online; (iii) Extensibility: new tasks reuse, inherit, or extend the shared library, so capabilities can accumulate over tasks. These advantages make COAP a suitable medium for recursive self-improvement (RSI): coding agents develop the library in a closed loop, and each change is explicit and controllable. On RoboDojo's 42 bimanual tasks, the resulting library reaches a success rate of 70.24% without a model at test time. The upper bound of COAP lies in how accurately the state is represented for decision making and how robust the code logic is. We thus propose COAP as a new paradigm for embodied tasks; since it applies across episodes, it can also serve as an efficient data engine for VLAs and Agent Harnesses.

---

## 10. PLaW-VLA: Predictive Latent World Modeling for Vision-Language-Action Policies

**Authors:** Yu Liu, Hetian Guo, Tianlv Huang, ..., Zhiyuan Zha, Xuan Song
**arXiv:** [2610.12285](https://arxiv.org/abs/2610.12285)
**Categories:** Robotics (cs.RO)

Learning to predict how the world evolves can provide vision-language-action (VLA) policies with predictive context for long-horizon control, but its effectiveness depends on what future representation is modeled and how it conditions action generation. We introduce PLaW-VLA, which models task-relevant future states in a pretrained prediction-oriented representation space, reducing the need to predict control-irrelevant visual details. Built on a Mixture-of-Transformers architecture, PLaW-VLA conditions action generation on observation history, current task semantics, and predicted future states through structured causal attention. Experiments show a +11.8 percentage-point (pp) gain over reactive policies on RoboTwin Hard Horizon III and a +1.77 pp gain over reconstruction-oriented latent prediction on zero-shot LIBERO-Plus, supporting improved long-horizon control and generalization under distribution shift, respectively. By avoiding low-level visual reconstruction, PLaW-VLA lowers the burden of future prediction, enabling a lightweight latent world model with parallel future prediction and about 1/19 the inference latency of generative world-action modeling at comparable policy performance.

---

## 11. PathTime-VLA: Path-Time Decoupling for Factorized Post-Training of Vision-Language-Action Policies

**Authors:** Qing Huang, Yifei Yang, Ziqing Zou, ..., Rong Xiong, Yue Wang
**arXiv:** [2610.11771](https://arxiv.org/abs/2610.11771)
**Categories:** Robotics (cs.RO)

Vision-Language-Action (VLA) policies typically predict actions at fixed time intervals, coupling the route a robot follows with its execution pace. This coupling complicates adaptation from teleoperation: useful geometric guidance comes with timing shaped by interface delays and operator behavior. Our key insight is to bring the path-time parameterization of classical motion planning into the learned action representation of a VLA. We introduce PathTime-VLA, which represents motion as a progress-indexed interaction path $X(s)$ and a positive interval-time profile. The latter defines a monotone time law $t(s)$, yielding controller commands $X(s(t))$. For a given path, alternative executions are expressed through the time profile, allowing chunk-wise speed choices without changing the geometric prediction target. This representation supports a staged post-training procedure: demonstrations and DAgger interventions establish a target-domain prior, Speed-DQN learns execution multipliers from robot interaction, and Path-AWR uses rollout outcomes to refine the diffusion path generator. A path-conditioned action expert realizes the resulting motions while maintaining distinct learning interfaces for path generation and execution timing. Across three tasks, the complete method achieves $58/60$ successes versus $57/60$ for PathTime-VLA under BC + DAgger at fixed $1\times$, with approximately $39$-$52\%$ shorter mean completion times over successful trials.

---

## 12. WARP-VLA: Wrist-Camera Adaptation for View-Robust Policy Execution in Vision-Language-Action Models

**Authors:** Junmyeong Lee, Dongmin Shin, Min-Gyu Park, ..., Inho Chang, Hae-Gon Jeon
**arXiv:** [2610.11508](https://arxiv.org/abs/2610.11508)
**Categories:** Robotics (cs.RO); Computer Vision and Pattern Recognition (cs.CV)

Despite recent advances in Vision-Language-Action models (VLAs) for robotic manipulation, their performance remains sensitive to changes in camera configuration. The problem becomes more evident in cross-setup deployment, as reproducing the exact camera pose used for training is nearly impossible. Unlike fixed external views, wrist views are more challenging because the camera moves with the robot, causing even small mounting variations to alter fine-grained geometric cues. To address this, we propose WARP-VLA, a camera-view robust VLA for diverse wrist camera configurations. WARP-VLA adopts a Mixture-of-Experts (MoE) architecture where individual experts learn view-specific feature transformations, and a router combines them based on implicit view information. This allows the policy to be deployed without requiring camera extrinsic parameters as additional input. Through experiments on the LIBERO benchmark, WARP-VLA improves the average success rate of pi-0.5 from 39.2% to 78.3% under wrist-view perturbations. The real-robot experiments further show that the feature-level adaptation learned in simulation successfully transfers to diverse deployment settings. To facilitate reproducibility and future research, we release our wrist viewpoint robustness benchmark and a plug-and-play implementation.

---

## 13. SimVLA: Zero-Shot Sim-to-Real VLA Learning for Mobile Manipulation

**Authors:** Kyoungin Baik, Youngwoon Lee
**arXiv:** [2610.11248](https://arxiv.org/abs/2610.11248)
**Categories:** Robotics (cs.RO)

Large-scale, diverse datasets have driven the success of LLMs and VLMs. But VLAs for robotics remain limited by the cost and complexity of real-world data collection. While simulation offers a scalable alternative, its potential for sim-to-real VLA learning in mobile manipulation remains largely underexplored. We introduce SimVLA, an end-to-end framework that trains VLAs entirely on synthetic simulation data without teleoperation for mobile manipulation. SimVLA is first pre-trained on two complementary simulation-derived datasets: SimAction, a large-scale robot action dataset spanning 35 diverse mobile manipulation tasks, generated by composing atomic skills, and SimVQA, which leverages privileged simulator state to provide spatial, geometric, and subtask-level visual-language supervision. We further post-train SimVLA on a mixture of SimAction and SimDeploy, a dataset collected from policy rollouts across diverse simulated environments. We evaluate SimVLA on tasks including restocking, pouring, and cleaning, and show zero-shot transfer to real-world mobile manipulation, including real home environments. SimVLA outperforms policies trained on 50 in-domain real-world demonstrations, suggesting that simulation can enable scalable sim-to-real mobile manipulation. We further demonstrate the value of multiple complementary forms of supervision for effectively leveraging simulation in VLA training.

---

## 14. VersaCamVLA: Camera-Configurable VLA Policies for Robotic Manipulation

**Authors:** Boyao Han, Chen Shi, Jingjing Qian, ZhuoTan Tian, Li Jiang
**arXiv:** [2610.12451](https://arxiv.org/abs/2610.12451)
**Categories:** Computer Vision and Pattern Recognition (cs.CV); Robotics (cs.RO)

Vision-Language-Action (VLA) models have emerged as powerful foundations for robotic manipulation, but their reliance on fixed camera configurations during training makes them brittle to changes in camera count or pose during deployment. To overcome these limitations, we propose VersaCamVLA, a camera-configurable framework that decouples camera-set representation from action learning. VersaCamVLA learns a unified scene-token interface that maps an arbitrary, variable set of posed RGB views into fixed-size latent scene tokens. This is achieved via multi-signal target-view prediction and Wrist-Augmented Pose Sampling (WAPS), which leverages natural wrist-camera motion for free pose diversity. At deployment, a lightweight spatial encoder injects these compact scene tokens into a pretrained base VLA as a supplementary visual condition, requiring no explicit 3D sensing or novel-view rendering. Experiments on RoboTwin, LIBERO, and a real-robot platform demonstrate that VersaCamVLA consistently outperforms prior VLA methods and direct multi-view baselines, maintaining robust performance across varying camera counts and unseen camera poses.

---

## 15. VGGTWorld-VLA: Intent-Conditioned 3D World Evolution for Autonomous Driving

**Authors:** Zhaoyang Liu, Kun Jiang, Ziying Song, Diange Yang
**arXiv:** [2610.11161](https://arxiv.org/abs/2610.11161)
**Categories:** Computer Vision and Pattern Recognition (cs.CV); Robotics (cs.RO)

VGGT provides a strong foundation for geometry-centric world models by recovering unified 3D scene geometry from visual observations. Although recent extensions enable temporal 3D prediction, their future evolution remains weakly conditioned on driving intentions and actions, limiting their ability to model alternative action-dependent futures. We propose VGGTWorld-VLA, an intention-conditioned extension of VGGT-World for controllable 3D world evolution in autonomous driving. First, we introduce an action--semantic conditioning mechanism that injects complementary driving semantics and ego-motion representations into the future-token stream, enabling different future geometry predictions for the same observed scene under alternative ego actions. Second, we develop a geometry--language--action bridge that adapts historical geometry, VLA semantic features, and maneuver and trajectory representations for joint conditioning of future geometry prediction. We evaluate future geometry prediction on NAVSIM, while conditioning ablations further examine the contributions of semantic and action information. Compared with the baseline, our method demonstrates competitive geometry prediction performance. Ablation studies further support the effectiveness of semantic and action conditioning. These results demonstrate the potential of semantic and action conditioning for controllable VGGT-based world prediction in autonomous driving.

---

## 16. ContourVLA: A Closed-Loop Perception-Action Contour Policy for Generalized Referring Expression Segmentation

**Authors:** Ruicheng Zhang, Kaiwen Shen, Jiaqi Hou, ..., Li Jiang, Shen Zhao
**arXiv:** [2610.12107](https://arxiv.org/abs/2610.12107)
**Categories:** Computer Vision and Pattern Recognition (cs.CV)

Generalized referring expression segmentation (GRES) requires dynamically balancing high-level semantics for identifying a variable number of language-specified referents with fine-grained visual evidence for precise boundary delineation. This requirement challenges existing cascaded vision-language architectures, which typically rely on static feature interfaces and single-pass mask prediction, limiting adaptive perception and geometric correction. We introduce ContourVLA, a vision-language-action policy that recasts GRES as a closed-loop visuomotor process, in which editable contours serve as explicit policy states that condition multimodal perception and are updated by geometric action chunks. Evolution-Aware Semantic Scheduling (EASS) couples contour-guided bidirectional boundary sampling with state-conditioned routing of multilevel multimodal features, adapting perception to each contour state. Following supervised initialization, Dustbin-Augmented Entropic Credit Transport GRPO (DECT-GRPO) jointly optimizes discrete grounding and continuous contour actions with instance-level credits. Its rollout rewards and credits are derived from soft prediction-target correspondences that account for false positives and missed targets. ContourVLA improves gIoU over the strongest evaluated baselines by 8.7, 2.8, and 2.7 points on gRefCOCO val, testA, and testB, respectively, and achieves the highest mIoU across all eight RefCOCO, RefCOCO+, and RefCOCOg splits.

---
