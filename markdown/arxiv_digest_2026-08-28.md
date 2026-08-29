# arXiv Daily Digest — 2026-08-28

**Mode:** direct
**Categories:** cs.AI, cs.LG, cs.RO, cs.CV
**Keywords:** VLA, world model, world action model
**Papers found:** 15

---

## 1. GameWAM: A World Action Model for Video Games

**Authors:** Yuncheng Guo, Zhanqiu Zhang, Yiwen Guo, Weijia Li
**arXiv:** [2608.26200](https://arxiv.org/abs/2608.26200)
**Categories:** Artificial Intelligence (cs.AI); Computer Vision and Pattern Recognition (cs.CV); Machine Learning (cs.LG)

Modern video games combine first-person perception, rapid visual changes, persistent world state, and heterogeneous native controls. Existing game agents map visual and task context directly to actions but lack explicit world dynamics modeling, whereas interactive game world models predict visual futures from supplied actions but do not serve as task policies. World-Action Models (WAMs) unify these objectives, but remain largely unexplored under the dynamics and open-ended interaction of video games. We introduce GameWAM, to our knowledge the first WAM for native closed-loop gameplay and GUI control. GameWAM jointly generates future visual observations and executable keyboard-mouse trajectories through parallel visual and action generative processes with block-causal conditioning and flow matching. To support joint world-action learning, we construct synchronized gameplay and GUI trajectories. To handle heterogeneous native control, GameWAM predicts a gameplay/GUI mode at each action step and generates actions with mode-specific prediction distributions and continuous-action normalization. For long-horizon interaction, block-cycle control predicts beyond the committed horizon, executes only a short action prefix, and replans from new observations, while fine-grained within-cycle context and hierarchical cross-cycle history preserve temporal continuity. Experiments demonstrate competitive task success with fewer executed native actions than the compared agents. We further uncover Low-Frequency Action Source Imprinting (LASI), in which low-frequency components of the sampled action source systematically steer coarse generated camera motion under fixed conditioning, revealing a source-sensitivity failure mode in generative control. Project page is available at this https URL.

---

## 2. Predicting Consequences and Reinforcing Navigation Policies with Latent World Models

**Authors:** Zengmao Wang, Wei Gao, Shuhan Shen
**arXiv:** [2608.26190](https://arxiv.org/abs/2608.26190)
**Categories:** Artificial Intelligence (cs.AI)

World models enable agents to reason about future outcomes and learn policies from their knowledge of state transition, but existing approaches primarily focus on reconstructing future observations or features, which introduces unnecessary complexity and limits their effectiveness for decision making. In this work, we propose a compatibility prediction Latent World Model (LWM) for robot navigation that predicts action-conditioned latent feature compatibility rather than reconstructing observations. Our key insight is that spatial proximity correlates with latent feature similarity, enabling action consequences to be evaluated directly in latent space. To support counterfactual training, our model leverages action sequences sampled across trajectories and learns to predict which sequences lead closer to the goal. Furthermore, we demonstrate how the learned world model can supervise policy learning from unlabeled video data and further improve policies through reinforcement learning entirely within the world model. This imagination-driven framework eliminates the need for action annotations and additional environment interaction. Extensive experiments on multiple real-world robot navigation datasets show that our approach significantly outperforms prior world model and imitation learning methods in prediction accuracy, policy learning, and real-world navigation performance. The code, pretrained models, and additional materials are available at this https URL.

---

## 3. CLAP: Cross-Embodiment Video World Models are Zero-Shot Physical Simulators

**Authors:** Kechen Liu, Ola Shorinwa
**arXiv:** [2608.27406](https://arxiv.org/abs/2608.27406)
**Categories:** Robotics (cs.RO); Artificial Intelligence (cs.AI); Computer Vision and Pattern Recognition (cs.CV)

State-of-the-art action-conditioned video models are typically restricted to a single robot embodiment, preventing them from leveraging the vast corpus of heterogeneous video data that contains rich signals for learning generalizable physics. To bridge this gap, we introduce CLAP, a framework for cross-embodiment action-conditioned video generation capable of being trained on diverse, internet-scale videos across human and robotic agents. CLAP is grounded in the insight that universal physical laws govern spatiotemporal dynamics regardless of the actor. However, cross-embodiment learning is non-trivial because action representations vary sharply across robot platforms and are typically absent in human videos. CLAP addresses this fundamental challenge through the following core contributions. First, CLAP reconciles disparate action spaces using end-effector poses, language instructions, and latent actions. Second, to resolve their individual limitations, CLAP introduces a curriculum-based cross-embodiment learning recipe that first learns foundational physical priors across unlabeled video data using latent actions and subsequently grounds them in end-effector action spaces for zero-shot deployment to real-world tasks. Crucially, CLAP approaches or surpasses state-of-the-art single-embodiment video models in challenging environments like DROID. These performance advantages compound via few-shot adaptation to establish a novel paradigm for training single-embodiment video world models. Ultimately, CLAP delivers the most comprehensive suite of action-conditioned video world models to date - spanning diverse action-conditioning spaces (end-effector, language, and latent) and robot morphologies (including cross-embodiment, DROID, Bridge, bimanual YAM robots, and G1 humanoids). We open-source all code and models. Project Website at this https URL .

---

## 4. Successive Capacity Growth: Task-Complexity-Driven Width and Depth Expansion for Vision Transformer Encoders in JEPA World Models

**Authors:** Frederik Berenz
**arXiv:** [2608.27367](https://arxiv.org/abs/2608.27367)
**Categories:** Computer Vision and Pattern Recognition (cs.CV); Artificial Intelligence (cs.AI)

Joint-Embedding Predictive Architectures (JEPAs) for world modeling typically employ fixed-size Vision Transformer encoders that are over-provisioned for simple tasks and under-provisioned for complex ones, with significant redundancy across attention heads. We propose Successive Capacity Growth (SCG), a method that starts from a minimal encoder (1 head, 2 layers, 283K parameters) and grows incrementally in width (adding attention heads for low-level semantic capacity) or depth (adding transformer blocks for higher-order semantic abstraction), driven by a task-agnostic test-and-verify mechanism that exploits function-preserving expansion to safely trial architectural changes and roll back if they do not improve prediction loss. The Sketched Isotropic Gaussian Regularizer (SIGReg) ensures that all learned semantic dimensions remain statistically independent and aligned with the predictive objective, preventing collapse even as the architecture grows. On a 60-dimensional multi-object dynamics task, SCG naturally triggers depth expansion, improving prediction loss by 20.3% over the fixed small baseline with 56 times greater parameter efficiency than scaling to the fixed large model; on a 2D navigation task, a single width expansion yields even an 23% improvement over the fixed large model. Across all three tested environments of increasing complexity, the adaptive encoder matches or exceeds the fixed small baseline, with zero false-positive expansions and bit-exact function preservation (ratio = 1.0, absolute difference = 0.0). The take-away is that JEPA world model encoders need not be pre-allocated at maximum capacity - they can grow successively as the task demands, achieving significant compute and data efficiency while maintaining representation quality.

---

## 5. PAWBench: How Far Are We from Probabilistically Aligned World Modeling?

**Authors:** Yuandong Pu, Le Zhuo, Sayak Paul, ..., Jingbo Xing, Xi Chen
**arXiv:** [2608.27345](https://arxiv.org/abs/2608.27345)
**Categories:** Computer Vision and Pattern Recognition (cs.CV); Artificial Intelligence (cs.AI)

Recent video generation models are increasingly framed as world models. Many physical processes can unfold in more than one valid way. Therefore, a world model should reproduce not only a plausible trajectory, but also the distribution of possible behaviors under the same initial observation and action. We call this distribution-level requirement probabilistic alignment. However, existing evaluations largely assess individual-video plausibility and do not test whether repeated generations recover the correct distribution. This raises a central question: how far are current video generators from probabilistically aligned world modeling? To answer it, we formalize probabilistic alignment as a distributional criterion for world models and introduce PAWBench, a benchmark for evaluating video generators as stochastic samplers of world dynamics. We further introduce PAWEval, an outcome-level protocol that converts repeated video rollouts into empirical distributions over possible physical behaviors. Across 50 scenarios and eleven current systems, no model consistently matches the reference probabilities while recovering the range of valid behaviors. Having established this gap, we test whether language prompts, initial noise sampling, or model training can reshape the model's predictive distribution. We believe our work can serve as a foundation for future efforts to move towards probabilistically aligned world modeling.

---

## 6. Making Latent Evolution Explicit: Operator-Structured Transitions for World Action Models

**Authors:** Xiaoxiao Lu, Yunlong Dong, Jiahao Shi, Ye Yuan
**arXiv:** [2608.27259](https://arxiv.org/abs/2608.27259)
**Categories:** Machine Learning (cs.LG)

World Action Models (WAMs) augment robot policies by predicting how task-relevant scene states may evolve under interaction. Recent WAMs increasingly perform such prediction in latent representation spaces, avoiding full appearance-level generation while preserving control-relevant information. Yet latent transitions are commonly realized with Transformer-based predictors whose inductive structure is centered on token interaction rather than temporal evolution. We study transition realization as an architectural choice distinct from predictive representation and prediction-policy coupling. We introduce the Latent Evolution Operator Network (LEON), which models latent evolution in a learned observable space through context-modulated operator-based propagation and additive forcing. Grounded in the controlled Koopman generator view of evolution, LEON organizes context-dependent transition variation around a shared evolution-operator structure while retaining a complementary path for additive change. Controlled dynamical systems verify the resulting evolution-specific inductive bias and the complementary roles of operator propagation and forcing. Across two WAM formulations that integrate latent prediction into the policy differently, LEON improves closed-loop performance and robustness while remaining effective under full transition replacement. These results establish transition realization as a consequential architectural choice in latent WAMs.

---

## 7. FlashVLA: Streaming Action Decoding for Fast and Asynchronous VLA Inference

**Authors:** Zekai Li, Jiaming Tang, Zhijian Liu
**arXiv:** [2608.27384](https://arxiv.org/abs/2608.27384)
**Categories:** Robotics (cs.RO)

Vision-Language-Action (VLA) models are increasingly promising for robotic manipulation, yet their real-world deployment remains bottlenecked by high inference latency and unstable asynchronous execution. This challenge is particularly pronounced in flow-matching-based VLA models, where action decoding requires multiple iterative steps conditioned on the VLM context. While efficient inference methods improve control frequency and asynchronous methods reduce execution idle time, existing approaches often fail to jointly achieve low-latency inference and accurate, temporally consistent asynchronous execution. We introduce \textbf{FlashVLA}, a streaming action decoding framework that addresses both challenges in a unified formulation. FlashVLA maintains a streaming action buffer with multiple chunks at different noise levels and decodes them using chunk-wise causal attention. This design allows FlashVLA to produce one executable action chunk per inference step. Moreover, its chunk-wise autoregressive formulation implicitly preserves action continuity, enabling smooth asynchronous execution without extra future-state conditioning. Across extensive simulated and real-world experiments, FlashVLA substantially improves inference speed while maintaining strong task performance. It can achieve $\geq$30\,Hz control frequency on a single GPU with smooth asynchronous inference in real-world deployment.

---

## 8. Riemann-1.0: An Embodied World Action Model for Physical AI

**Authors:** Haofeng Sun, Jiangbo Pei, Fei Kang, ..., Yang Liu, Yangguang Li
**arXiv:** [2608.27033](https://arxiv.org/abs/2608.27033)
**Categories:** Robotics (cs.RO)

We introduce Riemann-1.0, a fully causal autoregressive World Action Model for embodied intelligence. Riemann-1.0 jointly models multi-view visual observations, robot states, and embodiment-specific actions within a unified causal autoregressive sequence, representing robot actions and world evolution as causal state transitions. Unlike existing WAMs based on joint generation, video-first prediction, or decoupled modeling paradigms, Riemann-1.0 unifies online robot policy execution and action-conditioned world simulation within a single model, enabling it to function as both an executable robot policy and a multi-embodiment visual world simulator. To scale embodied experience across heterogeneous data sources, we further develop a progressive embodied pretraining framework that unifies learning from egocentric human videos, handheld-gripper demonstrations, and heterogeneous robot trajectories under a shared World Action Modeling objective. Built upon 200K+ hours of interaction data, Riemann-1.0 progressively transfers large-scale embodied experience into executable robot manipulation capabilities. Riemann-1.0 achieves state-of-the-art performance across both simulation benchmarks and real-world manipulation tasks. It achieves success rates of 94.3% on RoboTwin2.0, 99.0% on LIBERO, and 62.6% on the long-horizon compositional benchmark RoboCasa-365, outperforming the previous best method by 8.4% On long-horizon real-world manipulation tasks, Riemann-1.0 achieves a Success Rate (SR) of 85.0% and a Progress Success Rate (PSR) of 94.4%, exceeding the strongest open-source baseline by 15% in SR. These results demonstrate that unified World Action Modeling together with progressive embodied pretraining effectively transforms large-scale embodied experience into generalizable robot manipulation capabilities.

---

## 9. TemporalFlow-VLA: Learning Physically Grounded Execution History for Long-Horizon Robot Manipulation

**Authors:** Jiarui Yang, Yehao Lu, Yuning Su, ..., Junwei Liang, Enyu Li
**arXiv:** [2608.26821](https://arxiv.org/abs/2608.26821)
**Categories:** Robotics (cs.RO)

Vision-language-action (VLA) models leverage pretrained vision-language representations for robot control, yet simply adding historical frames does not reliably capture recent physical change. This is especially problematic in multi-stage manipulation, where visually similar states may require different actions depending on prior execution. To address this challenge, we present TemporalFlow-VLA, which learns compact execution history through physically grounded temporal supervision. Using recorded robot states, robot geometry, and calibrated cameras, we construct robot-surface temporal flow as a training-only target and supervise two execution-aligned temporal queries that provide structured history to the action expert. The geometric supervision path is not evaluated at deployment. TemporalFlow-VLA achieves 97.63 +/- 0.26% average success on LIBERO, including 96.60 +/- 0.87% on LIBERO Long, and 85.5%/84.2% Clean/Randomized success across 12 RoboTwin tasks. It shows its clearest advantage over prior methods on longer-horizon, multi-stage manipulation. Controlled history interventions show that action prediction depends on both historical content and temporal order. With asynchronous feature caching, temporal conditioning maintains single-frame-level server-side sampling latency without additional historical-encoding overhead. Overall, TemporalFlow-VLA provides a compact, physically grounded interface for exploiting ordered execution history without explicit motion estimation or geometric processing at deployment.

---

## 10. PredVLA: A Sub-Million-Parameter Predictive-Coding Policy for Robot Manipulation

**Authors:** Hiroki Sawada, Shunichi Kasahara
**arXiv:** [2608.26673](https://arxiv.org/abs/2608.26673)
**Categories:** Robotics (cs.RO)

Large pretrained vision-language-action models dominate modern robot-manipulation benchmarks, but it remains unclear how much model scale is necessary for strong language-conditioned control, or whether fundamentally different control architectures can remain competitive at much smaller parameter budgets. We present PredVLA, a language-conditioned predictive-coding policy with only 0.68 million trainable network parameters and no robot-data pretraining, whose hierarchical generative recurrent dynamics predict visual features and proprioception while observations influence latent state only through online inference from the resulting sensory prediction errors. On LIBERO, PredVLA achieves an 86.9% mean success rate across the three short-horizon suites and 75.4% when the long-horizon suite is included. Under a controlled comparison using the same frozen front end, demonstrations, action decoder, and evaluation protocol, PredVLA achieves 3.7x and 7.4x mean success rates of parameter-matched Transformer and LSTM policies, respectively. The predictive-coding formulation also makes the contribution of observation-driven correction directly measurable: because observations influence the recurrent state only through prediction-error-based latent inference, disabling this inference yields an exact open-loop control condition. Together, these results show that a sub-million-parameter recurrent generative policy can achieve strong performance on modern language-conditioned manipulation benchmarks while providing an explicit mechanism for prediction-error-driven online state correction.

---

## 11. TrapVLA: Trapping Vision-Language-Action Models in Configured Failure Modes

**Authors:** Jun-Hui Liu, Kun-Yu Lin, Yi-Lin Wei, ..., Yan Li, Wei-Shi Zheng
**arXiv:** [2608.26578](https://arxiv.org/abs/2608.26578)
**Categories:** Robotics (cs.RO); Computer Vision and Pattern Recognition (cs.CV)

This work introduces Configured Failure Trapping, a novel backdoor attack task against Vision-Language-Action (VLA) models, which aims to activate attacks through stealthy textual triggers and induce configured failure modes. Unlike prior backdoor attacks that treat any task failure as a successful attack, Configured Failure Trapping requires the attacker to control how the robot fails (e.g., causing the robot to grasp with a specified positional offset), making it substantially more challenging and hard to detect. To support the new task, we propose an effective data engine for synthesizing high-quality target trajectories and an automated suite for measuring configured-failure fidelity. Then, based on this foundation, we construct two new benchmarks, namely Trap-LIBERO and Trap-RoboTwin, that instantiate Configured Failure Trapping across four representative failure modes. To address this task, we identify sparse action deviation as a critical challenge and accordingly propose a novel method named TrapVLA, which explicitly learns trigger-induced action residuals to steer the policy toward the configured failure behavior. Extensive experiments across simulation benchmarks and real-world robotic settings show that TrapVLA effectively injects configured failure modes into VLA models while largely preserving performance on clean data. Project page: this https URL

---

## 12. WALL-SS: Scaling Long-horizon World Models via Next-Scale Autoregression

**Authors:** Maeve Zhang, Rain Sun, Xiang Wang, ..., Hao Wang, Qian Wang
**arXiv:** [2608.26239](https://arxiv.org/abs/2608.26239)
**Categories:** Robotics (cs.RO)

Generative world models provide robots with predictive models of how the world evolves under interaction, with growing potential for simulation, planning, policy evaluation, and robot learning. Beyond clip-level future prediction, a unified generative formulation should relate actions to consequences, support flexible horizons and continuous interaction, and enable reward-driven optimization. We introduce WALL-SS, a world model that generates visual futures through Scale-wise autoregressive Scaling, enabling action-controllable and long-horizon robotic simulation. WALL-SS represents embodied trajectories as causal sequences of temporally interleaved observations and actions, making action-dependent state transitions explicit while naturally supporting variable-length generation, streaming extension through reusable causal states, and direct optimization through sequence probabilities. To make this formulation effective over long horizons, we generate each future observation in a coarse-to-fine manner and develop three complementary components within the same hierarchy. Action-conditioned next-scale prediction injects scale-aligned action representations to improve action-future coupling and model both successful and failed behaviors. Scale-compressed long-horizon memory retains recent interactions at fine resolution while compressing distant observations and actions, with scale-wise dream forcing enhancing robustness to self-generated context. Finally, on-policy alignment optimizes autoregressive visual dynamics with action-following and long-term consistency rewards while preserving the pretrained visual distribution. Experiments show that WALL-SS improves action following and trajectory accuracy, supports coherent minute-long streaming rollout under bounded memory, and consistently benefits from on-policy alignment in reducing action drift and long-horizon inconsistency.

---

## 13. SpatialCrafter: Single Image World Modeling with Generative 3D Proxies

**Authors:** Chuan Fang, Lingteng Qiu, Yixun Liang, ..., Zihan Zhou, Ping Tan
**arXiv:** [2608.27073](https://arxiv.org/abs/2608.27073)
**Categories:** Computer Vision and Pattern Recognition (cs.CV); Robotics (cs.RO)

Explorable image-to-scene generation is essential for applications in gaming, robotics, and virtual reality. Existing methods based on video diffusion model (VDM) commonly rely on incomplete conditioning signals such as sparse point clouds or 2D panoramas, leading to stochastic hallucinations, long-term drifts and suboptimal 3D consistency. We present SpatialCrafter, a novel two-stage framework that addresses these issues by introducing a global 3D proxy for high-fidelity image-to-scene generation. Specifically, we decompose the generation process into global proxy generation and appearance refinement. For proxy generation, we propose a Point-anchored Sparse Structure~(PaSS) Flow module that predicts a spatially aligned and geometrically consistent 3D proxy. For appearance refinement, we re-frame the VDM as a Generative Deferred Refiner which synthesizes high-frequency photorealistic details upon proxy-defined scene geometry. To better integrate the proxy with the pre-trained VDM, we introduce Parallel Geometry Injection and Proxy-Aware Corruption training strategies, which improve robustness to proxy artifacts without disrupting the pretrained generative manifold. Furthermore, as no suitable dataset exists for this explorable scene generation task, we construct a new large-scale dataset of 115K scenes. To the best of our knowledge, it is the first hybrid dataset for image-to-scene generation. Extensive experiments on both synthetic and real-world datasets show that SpatialCrafter outperforms state-of-the-art methods, mitigates long-term drift, and remains robust and consistent under rapid camera motion and extreme viewpoint changes. Code, models, and the newly constructed dataset will be publicly released. See more at this https URL.

---

## 14. R2M-Bench: Evaluating Revisit Memory via Relative Consistency in Interactive Video World Models

**Authors:** Qiwen Gu, Bingjie Gao, Rui Chen, ..., Xiangxiang Chu, Junqiao Zhao
**arXiv:** [2608.27328](https://arxiv.org/abs/2608.27328)
**Categories:** Computer Vision and Pattern Recognition (cs.CV)

High similarity between first-visit and return frames does not necessarily show that a video world model remembered the scene; the intervening rollout may simply have changed very little. This ambiguity makes absolute revisit scores sensitive to rendering stability, repetitive content, and failed motion. We introduce \emph{R2M-Bench} (\textbf{R}elative \textbf{R}evisit \textbf{M}emory Benchmark), a benchmark of observable revisit-selective consistency. For every detected return, R2M-Bench compares the revisit pair with two controls from the same rollout: a gap-matched non-revisit pair that measures generic temporal stability and a short-range pair that estimates short-horizon consistency. These comparisons produce \emph{MemoryGain} (MG), the revisit advantage over the temporal baseline, and the \emph{Normalized Memory Ratio} (NMR), which normalizes this advantage by the short-to-baseline dynamic range. R2M-Bench combines 100 reference scenes with three leave-and-return trajectories to form 300 instances and evaluates appearance fidelity, scene and object identity, local geometry, and persistent state. Across seven action-conditioned video world models, Overall NMR correlates with human consistency judgments at Spearman's $\rho=0.547$ (95\% CI $[0.45,0.63]$). Its within-model correlation magnitude with generated motion is $0.072$, compared with $0.207$ for raw revisit similarity, indicating that relative calibration substantially reduces the slow-motion shortcut. DreamX-World-Memo achieves the highest Overall NMR among the evaluated video models. Together, these results support same-rollout relative calibration as a practical way to distinguish revisit-specific consistency from generic temporal stability.

---

## 15. Surgical Video Generation From Diffusion to World Models: A Survey

**Authors:** Fuxiang Huang, Chenxu Zhang, Liang Han, Lei Zhang
**arXiv:** [2608.26214](https://arxiv.org/abs/2608.26214)
**Categories:** Computer Vision and Pattern Recognition (cs.CV)

Surgical video data provides the primary training resource for models of intraoperative perception, surgical workflow understanding, and robotic decision-making. However, clinical data acquisition remains constrained by privacy, cost, and class imbalance. Surgical video generation has emerged as a transformative approach to addressing data scarcity and as a foundation for surgical simulation, training, and robotic policy learning. The field has developed rapidly without a clear conceptual framework. This survey organizes the 2024-2026 literature into three categories: unconditional generation, conditional generation, and world modeling generation, revealing a fundamental shift in how the task is defined from synthesizing visually plausible frames to modeling the causal dynamics of surgical scenes. We examine the persistent gap between pixel-level fidelity and clinical plausibility, and identify generalization, physical realism, controllability, and interpretability as bottlenecks. We further summarize experimental results of representative methods on public datasets to provide a quantitative reference for the field. This survey provides a structured overview of the current state and open challenges, offering a reference for researchers working at the intersection of intelligent perception, multi-modal fusion, generative AI, and surgical data science.

---
