# arXiv Daily Digest — 2026-05-04

**Mode:** direct
**Categories:** cs.AI, cs.LG, cs.RO, cs.CV
**Keywords:** VLA, world model, world action model
**Papers found:** 6

---

## 1. Physically Native World Models: A Hamiltonian Perspective on Generative World Modeling

**Authors:** Sen Cui, Jingheng Ma
**arXiv:** [2605.00412](https://arxiv.org/abs/2605.00412)
**Categories:** Artificial Intelligence (cs.AI); Robotics (cs.RO)

World models have recently re-emerged as a central paradigm for embodied intelligence, robotics, autonomous driving, and model-based reinforcement learning. However, current world model research is often dominated by three partially separated routes: 2D video-generative models that emphasize visual future synthesis, 3D scene-centric models that emphasize spatial reconstruction, and JEPA-like latent models that emphasize abstract predictive representations. While each route has made important progress, they still struggle to provide physically reliable, action-controllable, and long-horizon stable predictions for embodied decision making. In this paper, we argue that the bottleneck of world models is no longer only whether they can generate realistic futures, but whether those futures are physically meaningful and useful for action. We propose \emph{Hamiltonian World Models} as a physically grounded perspective on world modeling. The key idea is to encode observations into a structured latent phase space, evolve the latent state through Hamiltonian-inspired dynamics with control, dissipation, and residual terms, decode the predicted trajectory into future observations, and use the resulting rollouts for planning. We discuss how Hamiltonian structure may improve interpretability, data efficiency, and long-horizon stability, while also noting practical challenges in real-world robotic scenes involving friction, contact, non-conservative forces, and deformable objects.

---

## 2. Being-H0.7: A Latent World-Action Model from Egocentric Videos

**Authors:** Hao Luo, Wanpeng Zhang, Yicheng Feng, ..., Yuhui Fu, Zongqing Lu
**arXiv:** [2605.00078](https://arxiv.org/abs/2605.00078)
**Categories:** Robotics (cs.RO); Computer Vision and Pattern Recognition (cs.CV); Machine Learning (cs.LG)

Visual-Language-Action models (VLAs) have advanced generalist robot control by mapping multimodal observations and language instructions directly to actions, but sparse action supervision often encourages shortcut mappings rather than representations of dynamics, contact, and task progress. Recent world-action models introduce future prediction through video rollouts, yet pixel-space prediction is a costly and indirect substrate for control, as it may model visual details irrelevant to action generation and introduces substantial training or inference overhead. We present Being-H0.7, a latent world-action model that brings future-aware reasoning into VLA-style policies without generating future frames. Being-H0.7 inserts learnable latent queries between perception and action as a compact reasoning interface, and trains them with a future-informed dual-branch design: a deployable prior branch infers latent states from the current context, while a training-only posterior branch replaces the queries with embeddings from future observations. Jointly aligning the two branches at the latent reasoning space leads the prior branch to reason future-aware, action-useful structure from current observations alone. At inference, Being-H0.7 discards the posterior branch and performs no visual rollout. Experiments across six simulation benchmarks and diverse real-world tasks show that Being-H0.7 achieves state-of-the-art or comparable performance, combining the predictive benefits of world models with the efficiency and deployability of direct VLA policies.

---

## 3. MiniVLA-Nav v1: A Multi-Scene Simulation Dataset for Language-Conditioned Robot Navigation

**Authors:** Ali Al-Bustami, Jaerock Kwon
**arXiv:** [2605.00397](https://arxiv.org/abs/2605.00397)
**Categories:** Robotics (cs.RO)

We present MiniVLA-Nav v1, a simulation dataset for Language-Conditioned Object Approach (LCOA) navigation: given a short natural-language instruction, an NVIDIA Nova Carter differential-drive robot must navigate to the named object and stop within 1 m across four photorealistic Isaac Sim environments (Office, Hospital, Full Warehouse, and Warehouse with Multiple Shelves). Each of the 1,174 episodes pairs an instruction with synchronized 640x640 RGB images, metric depth maps (float32, metres), and instance segmentation masks, together with continuous (v,omega) and 7x7 tokenized expert action labels recorded at 60 Hz from a vision-based proportional controller. Trajectory diversity is ensured through three spawn-distance tiers (near: 1.5-3.5 m, mid: 3.5-7.0 m, far: global curated points; Pearson r=0.94 between spawn distance and trajectory length), 12 object categories, 18 training templates, and 12 paraphrase-OOD templates. Five evaluation splits support in-distribution accuracy, template-paraphrase robustness, and OOD object-category benchmarking. The dataset is publicly available at this https URL

---

## 4. Embodied Interpretability: Linking Causal Understanding to Generalization in Vision-Language-Action Models

**Authors:** Hanxin Zhang, Mingshuo Xu, Abdulqader Dhafer, ..., Hongbiao Dong, Zhou Daniel Hao
**arXiv:** [2605.00321](https://arxiv.org/abs/2605.00321)
**Categories:** Robotics (cs.RO)

Vision-Language-Action (VLA) policies often fail under distribution shift, suggesting that decisions may depend on spurious visual correlations rather than task-relevant causes. We formulate visual-action attribution as an interventional estimation problem. Accordingly, we introduce the Interventional Significance Score (ISS), an interventional masking procedure for estimating the causal influence of visual regions on action predictions, and the Nuisance Mass Ratio (NMR), a scalar measure of attribution to task-irrelevant features. We analyze the statistical properties of ISS and show that it admits unbiased estimation, and we characterize conditions under which action prediction error provides a valid proxy for causal influence. Experiments across diverse manipulation tasks indicate that NMR predicts generalization behavior and that ISS yields more faithful explanations than existing interpretability methods. These results suggest that interventional attribution provides a simple diagnostic approach for identifying causal misalignment in embodied policies.

---

## 5. World Model for Robot Learning: A Comprehensive Survey

**Authors:** Bohan Hou, Gen Li, Jindou Jia, ..., Yilun Du, Jianfei Yang
**arXiv:** [2605.00080](https://arxiv.org/abs/2605.00080)
**Categories:** Robotics (cs.RO); Computer Vision and Pattern Recognition (cs.CV)

World models, which are predictive representations of how environments evolve under actions, have become a central component of robot learning. They support policy learning, planning, simulation, evaluation, data generation, and have advanced rapidly with the rise of foundation models and large-scale video generation. However, the literature remains fragmented across architectures, functional roles, and embodied application domains. To address this gap, we present a comprehensive review of world models from a robot-learning perspective. We examine how world models are coupled with robot policies, how they serve as learned simulators for reinforcement learning and evaluation, and how robotic video world models have progressed from imagination-based generation to controllable, structured, and foundation-scale formulations. We further connect these ideas to navigation and autonomous driving, and summarize representative datasets, benchmarks, and evaluation protocols. Overall, this survey systematically reviews the rapidly growing literature on world models for robot learning, clarifies key paradigms and applications, and highlights major challenges and future directions for predictive modeling in embodied agents. To facilitate continued access to newly emerging works, benchmarks, and resources, we will maintain and regularly update the accompanying GitHub repository alongside this survey.

---

## 6. Thinking in Text and Images: Interleaved Vision--Language Reasoning Traces for Long-Horizon Robot Manipulation

**Authors:** Jinkun Liu, Haohan Chi, Lingfeng Zhang, ..., Xiaoshuai Hao, Wenbo Ding
**arXiv:** [2605.00438](https://arxiv.org/abs/2605.00438)
**Categories:** Artificial Intelligence (cs.AI); Robotics (cs.RO)

Long-horizon robotic manipulation requires plans that are both logically coherent and geometrically grounded. Existing Vision-Language-Action policies usually hide planning in latent states or expose only one modality: text-only chain-of-thought encodes causal order but misses spatial constraints, while visual prediction provides geometric cues but often remains local and semantically underconstrained. We introduce Interleaved Vision--Language Reasoning (IVLR), a policy framework built around \trace{}, an explicit intermediate representation that alternates textual subgoals with visual keyframes over the full task horizon. At test time, a single native multimodal transformer self-generates this global semantic-geometric trace from the initial observation and instruction, caches it, and conditions a closed-loop action decoder on the trace, original instruction, and current observation. Because standard robot datasets lack such traces, we construct pseudo-supervision by temporally segmenting demonstrations and captioning each stage with a vision-language model. Across simulated benchmarks for long-horizon manipulation and visual distribution shift, \method{} reaches 95.5\% average success on LIBERO, including 92.4\% on LIBERO-Long, and 59.4\% overall success on SimplerEnv-WidowX. Ablations show that both modalities are necessary: without traces, LIBERO-Long success drops to 37.7\%; text-only and vision-only traces reach 62.0\% and 68.4\%, while the full interleaved trace reaches 92.4\%. Stress tests with execution perturbations and masked trace content show moderate degradation, suggesting that the trace can tolerate local corruption and moderate execution drift, but remains limited under stale or incorrect global plans.

---
