# arXiv Daily Digest — 2026-08-07

**Mode:** direct
**Categories:** cs.AI, cs.LG, cs.RO, cs.CV
**Keywords:** VLA, world model, world action model
**Papers found:** 17

---

## 1. From Economic Agents to Agentic Economies: A Systems Blueprint for Economic World Models

**Authors:** Jiale Han, Xiang Li, Jing Qian, ..., Benyou Wang, Lin William Cong
**arXiv:** [2608.06020](https://arxiv.org/abs/2608.06020)
**Categories:** Artificial Intelligence (cs.AI); Machine Learning (cs.LG)

Economic World Models (EWMs) are generative economic models that simulate how economies evolve from within by modeling heterogeneous agents, their beliefs and actions, and the market and institutional mechanisms through which their interactions produce aggregate outcomes. This paper develops an implementation roadmap for building economic world models as generative engines in which heterogeneous agents act, interact, adapt, and co-evolve with markets and institutions, thereby producing economic dynamics from the inside. We organize EWM systems into a six-level capability ladder, from fixed rule-based agent worlds to adaptive and LLM-based agent worlds, self-evolving agents, evolving institutional worlds, and sim-to-real economic twins aligned with real observations. A systematic literature survey across these levels reveals that existing work remains concentrated in lower-level agent and simulation environments, while systems with self-evolving agents, endogenous institutions, persistent empirical alignment, and validated economic mechanisms remain rare. By translating the EWM agenda into an implementation blueprint, this paper aims to accelerate the development of the next generation of economic simulation environments that can serve as high-fidelity sandboxes for human decision-makers and as training, planning, evaluation, and safety substrates for AI agents. We release a curated paper list and related resources to support future research.

---

## 2. GAUGE: A Measurement-Grounded Benchmark for Physical Fidelity in Simulation Engines and Video World Models

**Authors:** Shuai Wang, Yaxin Feng, Xuekun Jiang, ..., Chunhua Shen, Weinan Zhang
**arXiv:** [2608.05948](https://arxiv.org/abs/2608.05948)
**Categories:** Artificial Intelligence (cs.AI); Computer Vision and Pattern Recognition (cs.CV); Robotics (cs.RO)

Physics engines facilitate large-scale training and evaluation for embodied intelligence, while generative video world models are emerging as implicit simulators of future states and interactions. However, existing evaluations of physical fidelity are often conducted in isolation and rely heavily on perceptual similarity or human judgments, providing limited insight into which physical principles or parameters are violated. We introduce GAUGE, a real-world-grounded diagnostic benchmark for jointly evaluating how numerical simulators and generative video world models reproduce or deviate from real-world physics. It comprises 22 controlled task families covering rigid bodies, flexible cables, textiles, and volumetric deformable objects. Grounded in real-world trajectories and paired with calibrated physical metadata, uncertainty annotations, and task-specific observables, these tasks cover fundamental physical processes including collision, friction, momentum transfer, oscillation, self-contact, and deformation across diverse materials and conditions. We benchmark Isaac Sim, Genesis, and Newton on 14 task families using generalized trajectory errors, and evaluate 6 image-to-video models on 5 rigid-body tasks by testing physical-law consistency and the temporal stability of inferred parameters. Our results reveal no uniformly faithful physics engine, with the largest discrepancies arising in impulsive contact, rapid textile motion, and volumetric deformation. We further find that video world models can produce trajectories with the expected equation form while recovering incorrect accelerations, momentum transfer, and oscillation timing. GAUGE lays the groundwork for developing more physically faithful simulators and world models for embodied intelligence.

---

## 3. AppDeltaWorld: Transition-Grounded Delta Code World Model for Mobile GUI Agents

**Authors:** Weikai Xu, Yunren Feng, Haoxiang Lei, ..., Shuo Shang, Bo An
**arXiv:** [2608.05891](https://arxiv.org/abs/2608.05891)
**Categories:** Artificial Intelligence (cs.AI); Computation and Language (cs.CL)

Mobile GUI agents can operate apps through pixel perception and touch actions, making them a promising interface for collecting and improving long-horizon mobile interaction policies. However, real trajectories are difficult to obtain for sensitive apps and privacy-critical operations. At the same time, existing simulated environments are costly to scale up, and GUI world models still suffer from unstable generation, limited modality coverage, and inconsistent action-transition logic. To address these limitations, we propose AppDeltaWorld, a transition-grounded delta code world model that predicts the next GUI as a reachable code update rather than as an unconstrained image or text description. AppDeltaWorld retrieves app-specific Level-1 HTML references under an action-transition constraint, generates Level-2 executable HTML conditioned on the current screen, action, predicted next-screen text, and retrieved structure, and inserts generated visual assets into image slots before browser rendering. As a world model, AppDeltaWorld achieves the highest fidelity on CMGUIBench-500 under Code2World evaluation, with clear gains in structural layout and UI element reconstruction over image-only and code-only baselines. As a training environment, AppDeltaWorld supports filtered closed-loop SFT data construction that, when combined with public supervision, enables AppDeltaAgent to achieve state-of-the-art performance on AndroidLens and consistent gains on MobileGym and MobileWorld. Moreover, world-model-based test-time reinforcement learning enables policy adaptation and shows further improvements without additional interaction with real apps.

---

## 4. DreamGuard: Efficient Runtime Guardrail for LLM Agents via Risk-Aware World Model

**Authors:** Wenhao Lin, Chenyu Yu, Xingwei Lin, ..., Letian Sha, Chunming Wu
**arXiv:** [2608.05695](https://arxiv.org/abs/2608.05695)
**Categories:** Artificial Intelligence (cs.AI); Computation and Language (cs.CL); Cryptography and Security (cs.CR)

As large language model (LLM) agents increasingly invoke external tools and interact with real-world systems, unsafe actions may cause irreversible consequences on external states, user data, and downstream services. Recent runtime guardrails mitigate such risks by checking proposed actions before execution, but many remain reactive: they primarily assess the apparent safety of the current action, lacking an explicit model of how risk evolves across the trajectory. This limitation creates a critical blind spot for long-horizon risks, where individually benign-looking actions can gradually drift the agent toward hazardous states. In response, we propose DreamGuard, a proactive guardrail for LLM agents built around a risk-aware world model. The world model maintains a compact recurrent latent state over the trajectory and predicts future latent states from which DreamGuard derives immediate-hazard and prefix-risk evidence. It then fuses these multi-horizon signals into intervention decisions before execution. Experiments across four benchmarks and an online guardrail evaluation show that DreamGuard outperforms generic, reactive, and proactive guardrail baselines, achieves the best safety-utility trade-off among evaluated guardrails, and maintains an average end-to-end latency of 25 ms per call.

---

## 5. Quantum-Structured World Models (QSWMs) for Predictive Latent Dynamics

**Authors:** Hailong Jiang, Emran Hossain, Feng Yu, ..., Guilin Zhang, Wulan Guo
**arXiv:** [2608.05371](https://arxiv.org/abs/2608.05371)
**Categories:** Machine Learning (cs.LG)

World models learn latent states that summarize interaction histories, evolve over time, and support prediction, simulation, or planning. Most existing world models represent these states using classical vectors, probability distributions, recurrent hidden states, or transformer activations. In this paper, we introduce Quantum-Structured World Models (QSWMs), a quantum-inspired framework for predictive world modeling with structured latent states, latent transition operators, and measurement-inspired decoding maps. We study whether mathematical structures inspired by quantum theory, such as complex-valued representations and density-matrix-like latents, provide useful inductive biases for world modeling. We establish three foundational properties: classical inclusion, predictive sufficiency, and structured compactness. We then instantiate complex-valued and density-matrix-like QSWM variants and evaluate them on elementary cellular automata against strong classical baselines. Results show promising local predictive potential for complex-valued QSWMs, while also revealing limitations in long-horizon rollout, density-matrix variants

---

## 6. $ω$-0: A Latent Predictive World Action Model for Concurrent Humanoid Loco-Manipulation

**Authors:** Zhe Li, Zhenzhe Zhang, Yangyang Wei, ..., Jianfei Yang, Shanghang Zhang
**arXiv:** [2608.06375](https://arxiv.org/abs/2608.06375)
**Categories:** Robotics (cs.RO)

Humanoid household tasks often require concurrent loco-manipulation, where the robot must move, adjust posture, maintain balance, and manipulate objects as a single coordinated behavior. Yet existing humanoid policies typically decompose locomotion and manipulation, while recent world-action models remain either arm-centric or video-centered. We present $\omega$-0, a latent predictive whole-body world-action model for real-world humanoid concurrent loco-manipulation. Given a language instruction, current visual observation, and robot proprioceptive state, $\omega$-0 directly predicts controller-compatible whole-body action latents for real-robot execution. Rather than reconstructing future videos, $\omega$-0 learns compact future observation embeddings as a lightweight predictive objective, coupling latent visual foresight with diffusion-based whole-body action generation. The model supports egocentric RGB, exocentric RGB, and exocentric depth inputs, and leverages controller-based simulation replay to ground human/public visual-motion priors into robot-executable action latents. We further collect $\omega$-HOME, a 40+ hour real-world household humanoid dataset with synchronized multi-view observations, whole-body SMPL motions, robot states, and action latents. Real-world experiments on 11 household tasks demonstrate that a single $\omega$-0 model can produce smooth manipulate-while-moving behaviors and consistently outperform representative imitation learning, VLA, humanoid, and WAM baselines.

---

## 7. DyPES-VLA: Learning Shared Dynamics Priors and Embodiment-Specific Control for Cross-Embodiment Manipulation

**Authors:** Junfeng Li, Junjie He, Zhide Zhong, ..., Yuxiang Gao, Haoang Li
**arXiv:** [2608.06374](https://arxiv.org/abs/2608.06374)
**Categories:** Robotics (cs.RO)

Vision-Language-Action (VLA) models have become a powerful paradigm for robot manipulation, but training a single generalist policy for heterogeneous robot embodiments remains an open problem. Existing methods have two main limitations. First, they underuse dynamics priors shared across diverse visual and interaction data, limiting cross-embodiment transfer. Second, they require extensive manual preprocessing to convert embodiment-specific actions into a common format. To overcome these limitations, we propose DyPES-VLA, a cross-embodiment VLA that learns shared Dynamics Priors and Embodiment-Specific control. First, we learn shared dynamics priors by training the vision-language model (VLM) with a future-prediction objective on cross-embodiment data, driving the shared query representation to capture object motion, contact, and interaction-induced scene changes. Second, an embodiment-specific Mixture-of-Experts (MoE) action head translates these shared dynamics priors into executable controls directly in each embodiment's native action space, without manually pre-aligning heterogeneous actions into a common format. This head shares attention layers to capture common temporal action structures, while its embodiment-specific feed-forward experts resolve the unique kinematic constraints and control semantics of distinct embodiments. As a generalist policy, our \ourmethod achieves state-of-the-art performance across simulation and real-world evaluations, reaching 98.0% success on LIBERO, 59.25% on RoboCasa-GR1, and 89.02% on RoboTwin~2.0.

---

## 8. GeniWorld: A Generalizable Interactive World Model for Robotic Manipulation via Visual Actions

**Authors:** Chenghao Gu, Hanyang Yu, Jingbo Zhang, ..., Jingyan Jiang, Zhi Wang
**arXiv:** [2608.06332](https://arxiv.org/abs/2608.06332)
**Categories:** Robotics (cs.RO)

Generalist robot policies exhibit strong capabilities, but their robustness in complex and unseen environments remains limited. Scaling robot learning and evaluation in diverse real-world environments remains costly and challenging. Action-conditioned world models offer a promising alternative, but they often suffer from limited action controllability and poor generalization to out-of-distribution (OOD) scenarios. To this end, we present GeniWorld, an interactive world model for robots that generalizes robustly across unseen scenarios. Building on pretrained video generative models, we use URDF-based rendering to transform numerical actions into visual action representations, enabling spatially grounded action control. By explicitly decoupling embodiment kinematics from environmental dynamics, our model mitigates scene overfitting and facilitates modeling of robot-environment interactions. To achieve closed-loop control, we construct an autoregressive video prediction model integrated with high-frequency robot kinematic control, enabling interaction with both robot policies and human teleoperators. In our experiments, even when trained solely on limited fixed-scene data, our model achieves superior in-domain performance and robust zero-shot generalization to highly randomized, unseen environments. For downstream applications, GeniWorld serves as a scalable policy evaluator that remains reliable under environmental perturbations. Furthermore, even with limited real-world demonstrations, GeniWorld generates diverse manipulation trajectories within the world model, improving downstream policy performance and robustness in complex environments.

---

## 9. XEWorld: Can Action-Conditioned World Models Generalize to Unseen Robot Embodiments?

**Authors:** Yixiang Chen, Jiabing Yang, Yuan Xu, ..., Yan Huang, Liang Wang
**arXiv:** [2608.05799](https://arxiv.org/abs/2608.05799)
**Categories:** Robotics (cs.RO); Computer Vision and Pattern Recognition (cs.CV)

Action-conditioned world models are promising learned simulators for robotic manipulation, yet evaluating them exclusively on training robots fails to reveal whether they capture physical dynamics or merely memorize visual patterns. To answer whether a model can faithfully render a robot it has never seen, we introduce XEWorld, a controlled cross-embodiment testbed for world models that isolates embodiments by evaluating held-out robots within physically identical scenes. Our systematic analysis uncovers a shared architectural bottleneck: current models act primarily as 2D visual pattern matchers whose generalization is governed by visual similarity rather than physical kinematic similarity. Driven by this limitation, they struggle to translate abstract numeric joint actions into coherent visual trajectories, and fail to predict dynamic visual changes from static initial observations. Consequently, successfully rendering an unseen embodiment zero-shot strictly requires heavily grounded cues, specifically pixel-space actions and explicit spatial-temporal alignment. Even when bypassing this zero-shot barrier via few-shot adaptation, the forced appearance recovery triggers catastrophic forgetting of seen embodiments. Together, these failures expose a critical inability to apply learned physical dynamics to novel visual appearances, highlighting that achieving true cross-embodiment generalization requires architectural innovations that decouple visual appearance from underlying physical dynamics.

---

## 10. In-Context VLA: Endowing Vision-Language-Action Models with Language via In-Context Post-Training and Agentic Tool Use

**Authors:** Jiarui Yang, Wen Huang, Jiale Zhang, Maowei Hu, Hang Guo
**arXiv:** [2608.05738](https://arxiv.org/abs/2608.05738)
**Categories:** Robotics (cs.RO)

Vision-Language-Action (VLA) models have become the dominant recipe for generalist manipulation, yet they are almost universally trained by behavior cloning: a policy imitates expert action chunks conditioned on a static image and a fixed instruction. A natural remedy is to inject explicit reasoning through textual chain-of-thought (CoT). We show, both empirically and analytically, that free-form textual CoT degrades low-level control: the reasoning it produces is ungrounded, its latency breaks closed-loop timing, and, crucially, the reasoning and action tokens are optimized against conflicting objectives so that the policy learns to narrate rather than to act. We argue that what a VLA needs is not the ability to generate language, but the ability to consume grounded language. To this end we introduce \textbf{\ourmethod{}}, a framework that endows a VLA with language competence through (i) in-context post-training, in which perceptual evidence is injected as structured context and the model is supervised only on actions, and (ii) an agentic tool-use interface, in which the policy queries open-vocabulary detectors, monocular depth, and a vision--language model to actively acquire task-relevant information. Rather than emitting a single templated caption, our data engine produces diverse, paraphrased, and evidence-conditioned spatial descriptions, so that the policy learns to interpret language it has never seen verbatim. Across the RoboCasa-GR1, SimplerEnv, and LIBERO simulation benchmarks, together with 8 real-world robot manipulation tasks, our method consistently achieves SOTA results in both performance and efficiency when compared with CoT-based approaches under matched configurations.

---

## 11. VLAff: Vision-Language-Affordance Model for Unified Actionable Affordances

**Authors:** Jihoon Oh, Kento Kawaharazuka, Kei Okada
**arXiv:** [2608.05215](https://arxiv.org/abs/2608.05215)
**Categories:** Robotics (cs.RO); Computer Vision and Pattern Recognition (cs.CV)

Learning manipulation skills from human videos is promising for scalable robot learning. However, the embodiment mismatch between humans and robots makes this challenging. One promising solution is to learn object-centric actionable affordances that are embodiment-agnostic. In this work, we propose a framework that leverages egocentric human videos with state-of-the-art 3D Structure-from-Motion and hand mesh reconstruction to extract actionable affordances such as visual, grasp, and trajectory affordances that explicitly encode where to interact, how to grasp, and how to move. We construct EgoAffordance, a large-scale dataset comprising 204K episodes with 5.6M visual affordances and 11.6M grasp and trajectory affordances. Building on this, we introduce VLAff, a large vision-language model-based unified foundation model that learns cross-modal correlations across all actionable affordances. Given a visual observation and instruction, VLAff generates visual affordance heatmaps, grasp poses, and trajectories, which are then converted into directly executable actions by utilizing 3D scene information. Through extensive experiments, we demonstrate that VLAff not only achieves state-of-the-art performance on visual affordance prediction, but can also be effectively applied to real robot applications such as zero-shot manipulation and affordance-guided robot learning.

---

## 12. Robust-WAM: Bridging Generative Pretraining and Semantic Foresight in World-Action Models

**Authors:** Haodong Yan, Junfeng Li, Junjie He, ..., Bingbing Liu, Haoang Li
**arXiv:** [2608.05903](https://arxiv.org/abs/2608.05903)
**Categories:** Computer Vision and Pattern Recognition (cs.CV); Robotics (cs.RO)

Mainstream World-Action Models (WAMs) adapt pretrained video generation models (VGMs) for robot control, transferring their learned dynamics prior for action prediction. These VGMs are typically trained in a variational autoencoder (VAE) latent space. However, the VAE latent space is optimized for pixel reconstruction, which rewards fine appearance detail and leaves the action prediction fragile under visual shifts. Recent works build WAMs in semantic latent space, which are more robust to appearance shifts. However, these models cannot leverage the large-scale VGM pretraining that exists only in VAE space. To overcome this dilemma, we propose Robust-WAM, a general post-training method for video-generation-based WAMs that preserves the VAE-based generative path and adds a lightweight semantic foresight alignment objective on the action stream. This retains the large-scale VGM pretraining while grounding actions in appearance-invariant dynamics that stay reliable under illumination shifts and other visual out-of-distribution conditions. Specifically, we employ learnable query tokens to bring future-scene semantics into the action stream by aligning their output hidden states with the semantic foresight of future ground-truth frames. To establish the temporal correspondence between each query and the future step it describes, we give it the positional encoding of the matching action tokens. Experiments on out-of-distribution generalization simulation benchmarks and a real-robot setup show that our Robust-WAM consistently improves the success rates of multiple WAM baselines without sacrificing in-distribution performance.

---

## 13. MASS: Multiplayer World Models with Authoritative Shared State

**Authors:** Ziqi Cai, Siqi Yang, Yimu Wang, ..., Kaipeng Zhang, Boxin Shi
**arXiv:** [2608.06257](https://arxiv.org/abs/2608.06257)
**Categories:** Computer Vision and Pattern Recognition (cs.CV); Human-Computer Interaction (cs.HC)

Current video world models struggle in multiplayer environments because they entangle world state with view-dependent visual latents, leading to redundant compute, view inconsistencies, and poor scalability. We propose MAS (Multiplayer world models with Authoritative Shared State) to resolve this limitation. Inspired by multiplayer game architectures, MAS disentangles world dynamics and view rendering. A learned Logic Engine advances a global, authoritative typed state from joint actions without any hand-written transition function, acting as the sole recurrent memory and synchronization reference. From this shared state, a learned Rendering Engine generates independent and consistent views for any requested camera on demand. This explicit disentangling allows MAS to achieve superior state accuracy and lower cross-view inconsistency compared to state-of-the-art multi-view baselines on a matched multiplayer Snake benchmark. It advances predicted worlds with 1,024 concurrent players for 10,000 recurrent steps. Our results show that explicit, authoritative state modeling provides a practical foundation for scalable and consistent multi-agent world simulation.

---

## 14. PhyLatent: Learning Dynamics-Relevant Representations for JEPA World Models

**Authors:** Xi Zeng, Haojie Ren, Ziying Song
**arXiv:** [2608.05720](https://arxiv.org/abs/2608.05720)
**Categories:** Computer Vision and Pattern Recognition (cs.CV)

We propose PhyLatent, a dynamics-relevant training objective for JointEmbedding Predictive Architecture (JEPA) world models. Our key observation is that preventing global latent collapse does not ensure that a representation preserves physical states and action consequences. We identify three failure modes in JEPA world models: physical invariance collapse, physical identifiability collapse, and counterfactual dynamics collapse. PhyLatent addresses them through three training pathways: physical invariance, physical identifiability, and counterfactual dynamics, implemented with physical state grounding, future representation alignment, static visual invariance, counterfactual branch separation, and latent denoising. On OGBench-Cube, PhyLatent reduces the three failure rates from 15.60%, 6.71%, and 8.41% to 7.53%, 0.95%, and 4.62%, respectively, and improves model predictive control (MPC) success from 70.0% to 78.1%. With the same architecture and planner, it further improves success from 81.0% to 98.0% on TwoRooms and remains competitive on Reacher and PushT. These results show that global non-collapse alone is insufficient for learning a reliable JEPA worldmodel state space.

---

## 15. LAWM-3D: Learning 3D-Aware Latent Actions from Human Videos for Generalizable Robot World Models

**Authors:** Jiarui Yang, Jiale Zhange, Jiawei Li, ..., Peidong Liu, Shu-Tao Xia
**arXiv:** [2608.05706](https://arxiv.org/abs/2608.05706)
**Categories:** Computer Vision and Pattern Recognition (cs.CV)

World models enable agents to perform forward rollout and planning without real-world interaction. However, their application in open-world embodied intelligence remains limited by the high cost of action annotations and the heterogeneity of action spaces across platforms. Recently, latent action models (LAMs) have alleviated this bottleneck by learning action representations directly from unlabeled human videos in a self-supervised manner. Nevertheless, most existing LAMs rely on single-view inputs and operate primarily in 2D pixel space, raising a fundamental question: can simply incorporating multi-view videos into LAM training endow the learned latent actions with 3D-aware perception? Our study shows that the answer is negative. The primary reasons lie in future-frame appearance leakage as well as inter-camera appearance discrepancies and viewpoint variations. To address these issues, we propose LAWM-3D, which introduces three tightly coupled key designs: (1) a multi-view invariant unified action tokenization scheme for learning 3D-aware latent actions; (2) a geometric alignment constraint that anchors intermediate encoder features to a pretrained 3D foundation model, thereby explicitly providing cross-view geometric correspondences; and (3) a non-injective RGB-D joint reconstruction objective that prevents shortcut learning from future-frame appearance information, forcing the LAM to focus supervision on motion cues with geometric significance. Importantly, these components are not simply stacked but are tightly coupled through a unified motivation. Built upon a two-stage paradigm of large-scale human video pretraining followed by robot fine-tuning, extensive experiments demonstrate that the proposed 3D-aware latent actions significantly improve world model performance, achieving SOTA results in generation quality, physical consistency, and generalization ability.

---

## 16. Uncertainty-Aware World Model for Aerial Image-Goal Navigation

**Authors:** Deyi Zhu, Haoyu Fan, Yinan Zhu, ..., Xinlei Chen, Yansong Tang
**arXiv:** [2608.05597](https://arxiv.org/abs/2608.05597)
**Categories:** Computer Vision and Pattern Recognition (cs.CV)

Aerial image-goal navigation requires an unmanned aerial vehicle (UAV) to reach a target location specified by a goal image. Existing world-model-based methods rank candidate trajectories using predicted futures, but typically rely on only one or a few point predictions, which is inadequate for large-scale outdoor environments with substantial future-state uncertainty. To address this limitation, we propose the Uncertainty-Aware Navigation World Model (UA-NWM), an efficient latent world model for aerial image-goal navigation, which formulates trajectory scoring as conditional out-of-distribution detection. UA-NWM represents plausible futures with an uncertainty subspace and decomposes the prediction--goal discrepancy into uncertainty-explainable and unexplainable components. Only the unexplainable residual is used for scoring, enabling robust selection without multiple future samples. Extensive experiments demonstrate that UA-NWM consistently outperforms existing navigation world models while maintaining low inference latency. Real-world UAV experiments further validate its practical applicability. Project page: this https URL

---

## 17. HERA: Historical Evidence Routing Adapter for Physical Prediction in Latent World Models

**Authors:** Yuanruyi, Yue Cao, Haojia Gao, ..., Zhuo Zou, Xueqian Wang
**arXiv:** [2608.05523](https://arxiv.org/abs/2608.05523)
**Categories:** Computer Vision and Pattern Recognition (cs.CV)

Predictive video models have emerged as promising world models by learning latent visual dynamics from large-scale video. Yet these models remain challenged by physical events under occlusion, where later predictions may depend on object evidence that is no longer available in the current view. Addressing this challenge requires historical evidence not only to be preserved but also to remain accessible when it becomes relevant to a subsequent prediction. Existing approaches mainly enlarge the temporal context, cache generic video features, or impose explicit object-centric states, thereby improving the capacity or structure of retained history. However, they do not directly address how relevant historical evidence can be selectively retrieved and integrated into a pretrained predictor without interfering with its native latent workspace. Accordingly, we introduce HERA (Historical Evidence Routing Adapter), a framework for routing retained historical evidence into a frozen latent predictor, and instantiate it with Register-Routed Patch Memory (RRPM), a lightweight adapter comprising a Structured Memory Bank, Memory Registers, and Workspace Registers. On the IntPhys2 Main split, HERA with RRPM improves the pairwise AvgSurprise accuracy of V-JEPA 2-G from 52.57% to 54.35%. Subgroup analysis shows particularly strong improvements on fixed-camera continuity, from 46.15% to 57.69%, and fixed-camera immutability, from 46.15% to 63.46%. These results support historical evidence routing as a practical adaptation strategy for physical prediction in latent world models.

---
