# arXiv Daily Digest — 2026-09-02

**Mode:** direct
**Categories:** cs.AI, cs.LG, cs.RO, cs.CV
**Keywords:** VLA, world model, world action model
**Papers found:** 11

---

## 1. Towards a Belief-Based World Model for LLM Agents

**Authors:** Shubham Kumar, Harshit Kumar, Narendra Ahuja, Saurabh Jha
**arXiv:** [2609.00455](https://arxiv.org/abs/2609.00455)
**Categories:** Artificial Intelligence (cs.AI)

Large language models (LLMs) are being used as policies for autonomous decision-making and planning in many domains. Despite their strong reasoning capabilities, LLMs struggle with long-horizon tasks, especially under partial observability. World models are a promising way to enhance policy performance, both during training and inference. During inference, agents currently use world models to simulate the consequences of candidate actions before committing to an action, which can improve decision-making. However, we argue that simulation alone is an incomplete interface for decision-making under partial observability: simulation doesn't adequately capture uncertainty about the current state, which agents may need for accurate decision-making. We address this limitation with Belief-Based World Models (BB-WMs), which model and maintain a belief that LLMs can query to access information on what is known and uncertain about the current state. Before developing methods to learn accurate BB-WMs, we first ask a more fundamental question: does exposing a world model's belief directly to an LLM policy improve decision-making? Our results show that giving LLM agents access to world model beliefs improves task performance under partial observability, while remaining complementary to existing simulation-based world models. Code is released at this https URL.

---

## 2. IMPACT: Attention Is the Interaction Map for Scalable Interaction-Aware World Model Training

**Authors:** Rongze Tang, Jianjie Fang, Zhaolu Wang, ..., Yong Li, Zhibo Chen
**arXiv:** [2609.00161](https://arxiv.org/abs/2609.00161)
**Categories:** Artificial Intelligence (cs.AI); Robotics (cs.RO)

World models have made remarkable progress in action-conditioned future prediction for embodied agents, yet still struggle to model physically plausible interactions. Existing approaches address this limitation by constraining the generation process with external representations encoding motion, geometry, or semantics. Obtaining these spatiotemporally dense representations typically requires auxiliary estimators or manual annotations, limiting training scalability. We instead revisit the training objective and identify a supervision-allocation mismatch under the globally averaged mean squared error (MSE) denoising objective: prevalent static content dominates the optimization signal, leaving sparse dynamic-object regions critical to interaction generation disproportionately under-supervised. Motivated by this observation, we introduce IMPACT, a scalable Interaction-aware Model training framework with Prior-guided Attention Calibration and Targeting. IMPACT uses cross-attention associated with manipulated-object tokens as an internal spatiotemporal prior for action-conditioned changes. It samples candidate regions from this prior, calibrates them with detached local prediction errors to construct an interaction map, and uses the map to reweight denoising supervision, requiring neither external representations nor inference-time modifications. Extensive experiments on robot-arm and human-hand manipulation, spanning diverse control modalities and DiT backbones, show that IMPACT consistently outperforms the corresponding MSE-trained baselines, improving interaction fidelity, physical plausibility, and visual quality.

---

## 3. HyperWorld: Hypergraph-Structured State Serialization Improves Learned Textual World Models

**Authors:** Yun-Jian Zhang, Chen-Wei Liang, Tian-Yi Zhang, ..., Hong-Yu An, Mu-Jiang-Shan Wang
**arXiv:** [2609.00002](https://arxiv.org/abs/2609.00002)
**Categories:** Artificial Intelligence (cs.AI)

World models enable language-model agents to predict environment dynamics and plan before acting. In text environments, the model must learn symbolic action effects from serialized state descriptions, but the role of serialization structure remains underexplored. We present HyperWorld, a controlled study of state serialization for learned textual world models. We compare raw observations with three symbolic serializations of the same ground-truth state: independent sentences, pairwise triples, and entity-centered hyperedge units that group multiple related facts around entities and relations. All variants use the same training objective: given a state and an action, predict symbolic effects or judge the action infeasible. Across model scales, data budgets, and in-distribution and out-of-distribution test worlds, hyperedge serialization gives the clearest gains for 0.5B--1.5B models and under distribution shift. Larger models reduce the gap, and pairwise triples can match or slightly exceed hyperedges on in-distribution exact match, but hyperedges achieve the strongest out-of-distribution fact F1 and the best small-to-medium scale trade-off between feasibility detection and effect prediction. In downstream greedy planning, the hyperedge world model also attains the highest success rate among the tested representations. These results show that higher-order state organization is a simple but effective inductive bias for learned symbolic world models, especially when model capacity is limited or test environments differ from training.

---

## 4. Evaluating Multimodal LLMs as Generalist Vision-Language-Action Agents for Drone Control: Commanding, Approaching, Tracking and Searching

**Authors:** Jaewoo Park, Minyoung Lee, Sukmin Seo, ..., Bado Lee, Geewook Kim
**arXiv:** [2609.01404](https://arxiv.org/abs/2609.01404)
**Categories:** Robotics (cs.RO); Artificial Intelligence (cs.AI)

Multimodal Large Language Models (MLLMs) are strong perceivers of images and video. We ask how far that reach extends into acting: dropping an MLLM directly into a drone's control loop, with its entire action space declared solely in the prompt. Recent systems approach this setting but increasingly narrow the model's decision-making. We widen it back. We introduce DroneCATS-Agent, an architecture where the MLLM is a swappable component, and DroneCATS, a benchmark treating the model as the independent variable. Beyond merely flying toward a pixel, our agent entrusts the model to yaw and search, deliberate when unsure, and self-declare arrival---all without fine-tuning or function-calling schemas. Evaluating frontier and open models across four core capabilities---approaching a visible target, tracking a moving one, searching outside the initial view, and commanding a multi-drone fleet---reveals that even the simplest embodied settings are far from solved. Crucially, to identify what breaks first at the edge, our roster scales down to 2B parameters. The findings expose a stark paradox: it is not the flying that fails. Small open models often navigate into the success radius more reliably than frontier models, yet lose the episode by declaring arrival prematurely or not at all. Multi-drone commanding amplifies this divide, with small models failing by blindly copying a single coordinate across distinct views. Viewed as vision-language-action agents, the models' spatial perception holds up, but their action protocol does not. What separates a deployable edge model from a frontier model is not navigation, but the discipline to sustain a declared protocol and emit the correct terminating action. The open problem is closing this gap at onboard compute costs---yielding a fast model that plans persistently and knows exactly when it is done---and DroneCATS is built to measure that distance.

---

## 5. EmbodiedSkills: A Unified Framework for Orchestrating, Training, and Deploying VLA Agents

**Authors:** Wei Wang, Wenqiao Zhang, Yutong Lin, ..., Chao Li, Yueting Zhuang
**arXiv:** [2609.01281](https://arxiv.org/abs/2609.01281)
**Categories:** Robotics (cs.RO); Artificial Intelligence (cs.AI)

Vision-language-action (VLA) models map visual observations and language instructions directly to robot actions, but long-horizon tasks require more than action prediction. An agent must coordinate perception, planning, execution, progress verification, and recovery as the physical state evolves. An action prediction or a model-generated skill decision does not, by itself, guarantee that the proposed operation is valid in the current state or that its outcome will be verified. We propose EmbodiedSkills, a unified framework that treats each skill decision as an execution proposal: the runtime checks its prerequisites before execution and verifies the outcome afterward. A shared executable-skill interface connects high-level skill selection, bounded low-level VLA execution, and post-action verification within a single agent loop. Because this interface remains fixed, low-level VLA policies can be replaced or adapted without changing the agent loop. The interface also records planning, execution, verification, and recovery events as structured trajectories, which provide supervision for individual components and can support optional online adaptation when interactive feedback is available. We instantiate EmbodiedSkills with Qwen3-VL and OpenPI/pi0.5 on RoboTwin 2.0 and LIBERO. Task-adapted low-level VLA policies achieve an average success rate of 86.20% across 50 RoboTwin 2.0 tasks and 97.40% across the four LIBERO suites. These results establish the execution performance of the task-adapted low-level VLA policies used in EmbodiedSkills. On four memory-dependent RMBench tasks, the same task-adapted execution approach achieves 12.5% average success. The framework provides a trainable and inspectable agent layer for turning these policies into closed-loop embodied systems.

---

## 6. REFACTOR-VLA: Unsupervised Library Learning of Typed Motor Programs

**Authors:** Riyaaz Shaik, Chandru Venkataraman
**arXiv:** [2609.01215](https://arxiv.org/abs/2609.01215)
**Categories:** Machine Learning (cs.LG); Artificial Intelligence (cs.AI); Robotics (cs.RO)

Most vision-language-action (VLA) models -- OpenVLA, $\pi_0$, RT-2, RDT-1B -- are monolithic: they emit raw motor commands or short action chunks without organizing behavior into reusable abstractions, so they degrade on long-horizon tasks and resist interpretation. Existing skill-discovery methods sidestep the core question of when two action sequences are behaviorally equivalent, either clustering contrastive embeddings or delegating the judgment to a language model uncalibrated to the robot's dynamics. We introduce REFACTOR-VLA, a wake/sleep system for learning reusable skills. Its sleep phase clusters motor-program fragments under a Behavioral-Equivalence Kernel (BEK) computed from rollouts of a learned latent world model $M_\phi$; its wake phase emits typed lambda terms over a Hindley--Milner-inspired vocabulary, consumed by a library-conditioned rectified-flow action decoder. Abstractions are admitted only if they pass Minimum Description Length and return-preservation gates. On LIBERO we report two findings. First, enlarging the world model from 188M to 430M parameters worsened performance on 4 of 4 suites, so capacity alone does not help. Second, the training objective matters far more: adding an auxiliary supervised contrastive (InfoNCE) loss during world-model warmup substantially improves sleep-phase clustering, giving Normalized Mutual Information at $n=3$ seeds of $0.462 \pm 0.021$ (object), $0.867 \pm 0.025$ (spatial), $0.915 \pm 0.013$ (goal) and $0.754 \pm 0.010$ (LIBERO-10), and beating the strongest published baseline on all 4 suites by a mean $\Delta = +0.184$. Across providers ($n=12$) the 95% bootstrap confidence interval for mean pairwise NMI is $[0.683, 0.729]$ (mean $0.705$). The sleep phase also yields the first real-LIBERO task-language library: the decoder uses 2 of 3 admitted abstractions and rewrites all 256 sampled demonstrations.

---

## 7. Risk-Aware Decision-Making for Autonomous Overtaking: A World Model-Based Mixture-of-Experts Framework

**Authors:** Yongzhi Liu, Sunan Zhang, Jinchang Xu, ..., Chen Lv, Weichao Zhuang
**arXiv:** [2609.00385](https://arxiv.org/abs/2609.00385)
**Categories:** Robotics (cs.RO); Artificial Intelligence (cs.AI); Machine Learning (cs.LG)

Autonomous highway overtaking demands foresighted decision-making to handle complex interactions, stochastic traffic evolution, and temporal risk accumulation. However, standard safe reinforcement learning approaches typically rely on implicit value-based risk estimations rather than explicit dynamics modeling, thereby struggling to accurately capture complex risk propagation over multi-step horizons. This limitation frequently results in behaviors that are locally safe but induce substantial latent risks in the long term. To address this, a World Model-based Risk-aware Mixture-of-Experts (WM-RMoE) framework is proposed. First, a learned latent dynamics model facilitates parallel multi-step rollouts, elevating safety assessment from the action level to the trajectory level via cumulative risk evaluation. Second, to enhance robustness under varying interaction intensities, a hierarchical gating mechanism dynamically coordinates experts across long-horizon, short-horizon, and rule-based safety modules. Furthermore, a Gaussian Mixture Model is integrated to preserve multimodal maneuvering branches, thereby mitigating the issue of behavioral mode averaging. Experimental results demonstrate that WM-RMoE significantly outperforms representative baselines in terms of safety compliance, decision stability, and generalization capability. Furthermore, benefiting from the risk-aware formulation, the proposed framework uniquely exhibits the ability to generate foresighted and semantically distinct overtaking maneuvers across diverse traffic densities.

---

## 8. GUI-CC: Benchmarking Contextual Consistency of GUI World Models as Agent Environments

**Authors:** Lin Fu, Zheyuan Yang, Tianhui Zhang, ..., Yilun Zhao, Yu Rong
**arXiv:** [2609.00048](https://arxiv.org/abs/2609.00048)
**Categories:** Computation and Language (cs.CL); Artificial Intelligence (cs.AI)

GUI world models are increasingly evaluated as one-step next-screen predictors, yet their intended use is often as multi-step environments for GUI agents. This mismatch leaves a key requirement under-tested: generated states must remain contextually consistent when they are repeatedly reused for future interaction. We introduce GUI-CC, a benchmark that evaluates contextual consistency of GUI world models as agent environments rather than isolated next-screen predictors. GUI-CC contains two complementary tracks: an offline reference-action track that rolls models along real mobile GUI trajectories, and an online agent-loop track that lets fixed probing agents interact with model-generated UIs. We construct 500 offline trajectory tasks from GUIOdyssey and 200 emulator-verified online tasks across 30 mobile apps. GUI-CC evaluates transition fidelity, transition plausibility, contextual consistency, and task progress. Experiments show that plausible single-step generation does not guarantee reliable environment simulation: current models often produce usable-looking screens while failing to preserve task-relevant context or support executable multi-step rollouts.

---

## 9. Knowing When to Stop: Adaptive Action Chunking via Internal Cross-Attention Dynamics in VLAs

**Authors:** Runze Xu, Xiaolong Shan, Shuang Dai, Yu Wang, Jincheng Yu
**arXiv:** [2609.00908](https://arxiv.org/abs/2609.00908)
**Categories:** Robotics (cs.RO)

Action chunking is a standard execution strategy in modern Vision-Language-Action (VLA) frameworks, but fixed execution horizons impose a trade-off between efficiency and accuracy. Short chunks require frequent inference and may cause oscillatory behavior, whereas long chunks can become misaligned with newly observed states. We address this limitation with an adaptive action chunking approach based on internal cross-attention dynamics in the action expert. We observe that, as the prediction horizon extends, action-to-observation cross-attention becomes increasingly dispersed and its entropy rises toward a plateau. This pattern is associated with higher action prediction error and provides an online signal that the current observation offers limited grounding for further open-loop execution. Based on this observation, we introduce a training-free truncation mechanism that detects sustained high-entropy plateaus and dynamically selects the execution horizon during inference. The method uses attention weights already computed by the policy and introduces negligible additional overhead. Evaluations on $\pi_{0.5}$ and X-VLA across RoboTwin 2.0, LIBERO, and three real-world manipulation tasks show improved average task success over fixed-horizon and adaptive chunking baselines, while preserving efficient closed-loop control. These results show that cross-attention dynamics can provide a practical internal signal for adaptive action execution in VLAs.

---

## 10. Streaming4D: Accelerate 4D World Models via Block-wise Video Generation and Incremental Reconstruction

**Authors:** Xiaoyan Liu, Jiaxin Liu, Kangrui Li, Sifan Zhou
**arXiv:** [2609.00610](https://arxiv.org/abs/2609.00610)
**Categories:** Computer Vision and Pattern Recognition (cs.CV)

Current 4D generation paradigms are often bottlenecked by a sequential decoupling design: video is generated first, followed by 3D reconstruction, leading to high interaction latency. This limits applications in interactive real-time scenarios. To this end, we propose \textbf{Streaming4D}, a tightly coupled synchronous pipeline that integrates block-wise autoregressive video generation with incremental 3D reconstruction. Unlike traditional frame-by-frame emission and delayed geometry recovery, Streaming4D generates temporal video blocks and immediately triggers reconstruction for each completed block, enabling parallel execution between synthesis and geometric updates. This approach allows the world representation to evolve online with the video stream, reducing feedback latency while preserving geometric fidelity. We instantiate \textbf{Streaming4D} using a Self-Forcing-style autoregressive generator and an incremental reconstruction backend. Experiments show consistent runtime improvements across resolutions on a single RTX 4090 (1.24$\times$ speedup), while maintaining high-quality 4D geometry and multi-view consistency.

---

## 11. ZimaBlue: Evolving Generalizable World Action Models through Scalable Video Pre-training

**Authors:** Xionghao Wu, Yijun Yang, Shiyang Zhou, ..., Haoyang Huang, Nan Duan
**arXiv:** [2609.00188](https://arxiv.org/abs/2609.00188)
**Categories:** Computer Vision and Pattern Recognition (cs.CV)

Robotic manipulation faces a fundamental scaling challenge: robust generalization demands broad physical experience, yet action-labeled robot trajectories are expensive to collect and inherently limited in diversity. Egocentric videos offer a far more scalable source of embodied experience, capturing object interactions, contact dynamics, tool use, and long-horizon behaviors across diverse environments. The central challenge is how to convert this abundant but action-free experience into effective robot control. We introduce ZimaBlue, a scalable framework for learning generalizable World Action Models (WAMs) from large-scale video. ZimaBlue follows a three-stage training curriculum: it first performs causal embodied video pre-training on large-scale human and robot egocentric videos, then grounds the learned visual dynamics in heterogeneous robot trajectories through video-action mid-training with a unified action representation, and finally specializes the model to a target robot for deployment. To make generative WAMs practical for real-time control, ZimaBluefurther adopts an asynchronous Slow-Fast dual-system architecture, where a high-capacity Slow world model provides generalizable spatiotemporal representations and a lightweight Fast branch enables 30 Hz action prediction on NVIDIA RTX 4090. On real-robot zero-shot evaluations, scaling from target-robot data alone to over 120,000 hours of embodied video improves success from 36.1% to 77.8%. ZimaBlue further delivers strong performance across multiple benchmarks, with particularly pronounced gains on unseen tasks.

---
