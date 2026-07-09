# arXiv Daily Digest — 2026-07-08

**Mode:** direct
**Categories:** cs.AI, cs.LG, cs.RO, cs.CV
**Keywords:** VLA, world model, world action model
**Papers found:** 13

---

## 1. A Definition and Roadmap for World Models

**Authors:** Xinyuan Chen, Haoyu Guo, Shi Guo, ..., Bowen Zhou, Ming Zhou
**arXiv:** [2607.06401](https://arxiv.org/abs/2607.06401)
**Categories:** Artificial Intelligence (cs.AI)

World models -- internal simulators that learn the structure and dynamics of an environment -- have become one of the most actively debated concepts in AI. From model-based reinforcement learning and video generation to embodied robotics and ultimately, physical AI, researchers across AI subfields are building systems that they call "world models", yet there is no consensus on what a world model fundamentally is, what it should predict, or how it should be built. This perspective article provides a scientific definition of world models, discussions of their key technical aspects, and a staged roadmap for developing effective world models.

---

## 2. Narrative World Model: Narratology-Grounded Writer Memory for Long-Form Fiction

**Authors:** Mohammad Saifullah, Thomas Kornmaier, Taaha Kazi, ..., Aditya Sanjiv Kanade, Aanand Kumar Yadav
**arXiv:** [2607.05577](https://arxiv.org/abs/2607.05577)
**Categories:** Artificial Intelligence (cs.AI); Computation and Language (cs.CL); Information Retrieval (cs.IR)

Long-form fiction writers need memory that answers multi-hop questions about evolving story state: who knows a secret and when they learned it, whether an event preceded the narration that revealed it, whether a setup paid off, and how a relationship shifted. General-purpose retrieval and agent-memory systems represent entities and facts but not the narratological structure these questions turn on, so they surface the wrong evidence or none at all. We introduce the Narrative World Model (NWM), a writer-memory system that pairs a narratology-grounded typed temporal-state graph with query-conditioned hybrid retrieval. To measure memory rather than the answerer, we read every system through a single held-constant Opus 4.8 reader over only that system's chapter-safe evidence, on a reproducible public corpus and a validated multi-hop benchmark, and we compare against the strongest existing temporal-knowledge-graph agent-memory framework, Graphiti/Zep (Rasmussen et al., 2025). NWM substantially and significantly outperforms this baseline on multi-hop narratological QA across both corpora, and far exceeds GraphRAG and flat retrieval. The advantage is representational rather than an artifact of extraction: it survives rebuilding the baseline with NWM's own extractor, and traces to its narratology-grounded structure and query-conditioned retrieval, not to graph size or extractor quality.

---

## 3. Learning 4D Geometric Priors for Inference-Efficient World Action Models

**Authors:** Jianjun Zhang, Jian Zhu, Taiyi Su, ..., Yi Xu, Hanli Wang
**arXiv:** [2607.05468](https://arxiv.org/abs/2607.05468)
**Categories:** Robotics (cs.RO); Artificial Intelligence (cs.AI)

World Action Models (WAMs) have shown strong potential for robotic manipulation by jointly modeling visual future dynamics and executable action sequences. However, existing video-action co-training methods primarily optimize appearance-oriented video latents, which may insufficiently capture the temporally evolving geometry required for precise manipulation. We propose MECo-WAM, a Multi-Expert Co-Training World Action Model that injects action-relevant 4D geometric priors into video-action representations while preserving the original lightweight inference graph. During training, MECo-WAM combines video and action experts with a lightweight 4D expert supervised by relational targets from a frozen VGGT encoder. Asymmetric expert visibility prevents non-causal shortcuts from auxiliary geometry to action generation. To transfer geometric knowledge into the deployed video-action pathway, we introduce decayed 4D read-mask attention, which provides restricted current-frame geometric guidance early in training and progressively removes this dependency. We further propose action-aware temporal geometric distillation, which aligns within-frame geometric relations and their temporal evolution while emphasizing visual regions most relevant to robot actions. At deployment, all auxiliary 4D components are removed. Experiments on LIBERO (98.2%), RoboTwin 2.0 (92.6%), and challenging real-world manipulation tasks show that MECo-WAM improves manipulation performance without increasing inference cost.

---

## 4. Training-Free Acceleration for Vision-Language-Action Models with Action Caching and Refinement

**Authors:** Ryuji Oi, Hikari Otsuka, Kosuke Matsushima, ..., Tatsuya Kaneko, Daichi Fujiki
**arXiv:** [2607.06370](https://arxiv.org/abs/2607.06370)
**Categories:** Robotics (cs.RO); Computer Vision and Pattern Recognition (cs.CV); Machine Learning (cs.LG)

Vision-Language-Action (VLA) models have emerged as a promising approach for generalizable robotic manipulations. In particular, flow matching-based VLA models have shown remarkable success due to their capability to generate precise and smooth action sequences and capture multimodal distributions. However, the iterative denoising process in the action head acts as a major computational bottleneck, posing a critical challenge for real-time deployment. To address this challenge, we propose ActionCache, a plug-and-play external cache that opportunistically reuses past intermediate actions to warm-start generations from the vicinity of target actions, thereby drastically reducing the inference latency. Specifically, ActionCache stores the intermediate actions with compact multimodal keys, which enables retrieval from similar past contexts across different episodes or even different tasks. Experimental results in simulation and real-world environments demonstrate that ActionCache maintains high task success rates in a low-latency regime, achieving inference acceleration of up to $11.75\times$ and $34.43\times$ for representative flow-based VLA models, $\pi_{0.5}$ and GR00T-N1.6, respectively.

---

## 5. Lift3D-VLA: Lifting VLA Models to 3D Geometry and Dynamics-Aware Manipulation

**Authors:** Jiaming Liu, Qingpo Wuwu, Nuowei Han, ..., Boxin Shi, Shanghang Zhang
**arXiv:** [2607.06564](https://arxiv.org/abs/2607.06564)
**Categories:** Robotics (cs.RO); Computer Vision and Pattern Recognition (cs.CV)

Recently, Vision-Language-Action (VLA) models have demonstrated strong generalization across diverse tasks. However, effective robotic manipulation in physical environments fundamentally requires geometric understanding and spatial reasoning. While some VLA approaches attempt to incorporate 3D information, they are constrained by limited data availability and geometric information loss in current 3D encoding pipelines, and fail to jointly capture 3D geometry and temporally structured actions in dynamic environments. To address these limitations, we introduce Lift3D-VLA, a unified VLA framework that equips models with explicit 3D point cloud reasoning and enables temporally coherent action generation. First, building upon our previous work Lift3D, an enhanced 2D model-lifting strategy is proposed to geometrically align 3D points with pretrained 2D positional embeddings. This design enables direct point-cloud encoding within the VLA vision encoder while minimizing spatial information loss. Based on explicit 3D inputs, we propose Geometry-Centric Masked Autoencoding (GC-MAE), a dual-objective self-supervised framework that reconstructs the current point cloud while predicting its future geometric evolution. This formulation allows the 2D vision encoder to internalize both 3D structure and physical dynamics. To fully exploit 3D representations, we further design layer-wise temporal action modeling, which leverages multiple layers of the LLM to collaboratively predict action chunks, enabling temporally consistent predictions. Across 22 simulated tasks and 8 real-world manipulation tasks, Lift3D-VLA achieves 10.8% and 11.1% higher mean success rates on MetaWorld and RLBench than the best-performing prior VLA methods, and outperforms the strongest real-world baseline by 4 percentage points, while exhibiting stronger generalization to out-of-distribution perturbations.

---

## 6. RynnWorld-4D: 4D Embodied World Models for Robotic Manipulation

**Authors:** Haoyu Zhao, Xingyue Zhao, Siteng Huang, ..., Deli Zhao, Zhongyu Li
**arXiv:** [2607.06559](https://arxiv.org/abs/2607.06559)
**Categories:** Robotics (cs.RO)

Robotic manipulation in the open world requires not only recognizing what a scene looks like, but also anticipating how its 3D structure moves under interaction. We argue that synchronized RGB, depth, and optical flow, namely RGB-DF, provide a physically grounded representation that captures the underlying 4D dynamics of a scene. Compared to 2D pixel videos, this multi-modal synergy aligns visual appearance with geometric structure and temporal motion, creating a representation space significantly closer to the low-level end-effector actions demanded by robotic systems, thereby narrowing the gap between world prediction and policy learning. Building on this insight, we introduce RynnWorld-4D, a generative model that co-produces future RGB frames, depth maps, and optical flow from a single RGB-D image and a language instruction within one unified diffusion process. This 4D world model features a tri-branch architecture that integrates cross-modal attention with frame-wise 3D RoPE, ensuring that appearance, geometry, and motion evolve consistently. To supply training data at scale, we curate Rynn4DDataset 1.0, a massive dataset of over 254.4 million frames across egocentric human and robotic manipulation videos with high-quality pseudo-labels for depth and optical flow. We further propose RynnWorld-4D-Policy, an inverse dynamics head that consumes the internal 4D representations of RynnWorld-4D in a single forward pass, bypassing expensive multi-step denoising, to output robot actions in a closed-loop manner. Experiments show that RynnWorld-4D produces temporally and spatially coherent 4D predictions, and that RynnWorld-4D-Policy achieves state-of-the-art performance on real-world dexterous bimanual manipulation tasks, particularly excelling in tasks demanding spatial precision and temporal coordination.

---

## 7. RynnWorld-Teleop: An Action-Conditioned World Model for Digital Teleoperation

**Authors:** Haoyu Zhao, Xingyue Zhao, Hangyu Li, ..., Deli Zhao, Zhongyu Li
**arXiv:** [2607.06558](https://arxiv.org/abs/2607.06558)
**Categories:** Robotics (cs.RO)

Scaling robot learning requires massive, diverse trajectory data, yet collection is currently bottlenecked by physical teleoperation, where every demonstration binds operator time to specific hardware and workspaces. We introduce digital teleoperation, a paradigm that decouples data collection from physical constraints by replacing the real robot with a generative world model. In this framework, an operator's hand-pose stream drives a robot-centric generative world model to synthesize high-fidelity egocentric videos from a single reference image. The recorded pose stream serves as an embodiment-agnostic action label transferable to any target robot via standard retargeting, yielding complete state-action trajectories for imitation learning independent of physical hardware. We instantiate this paradigm in RynnWorld-Teleop, a system that integrates depth-aware skeletal conditioning, progressive human-to-robot training on a video Diffusion Transformer, and streaming autoregressive distillation. This pipeline compresses the generative process into a single-pass inference, enabling 40+ FPS, real-time interactive generation on a single H100 GPU. Policies trained exclusively on RynnWorld-Teleop-generated data achieve effective zero-shot Sim2Real transfer across dexterous and diverse bimanual tasks. Moreover, augmenting real-world datasets with our digitally teleoperated data consistently improves success rates, demonstrating that RynnWorld-Teleop serves as a high-fidelity, scalable data engine for the next generation of robotic agents.

---

## 8. SIEVE: Structure-Aware Data Selection for Imitation Learning with VLA Models

**Authors:** Changti Wu, Bin Yu, Zhaolong Shen, ..., Lei Zhang, Kai Chen
**arXiv:** [2607.06442](https://arxiv.org/abs/2607.06442)
**Categories:** Robotics (cs.RO)

Vision-Language-Action (VLA) models are typically trained by imitation learning on large-scale robot demonstration datasets, but more data does not necessarily yield better policies due to redundancy, noise, and uneven coverage. Existing data selection methods often assess demonstrations at either the trajectory or state-action level, missing the reusable structures that compose long-horizon behaviors. In this paper, we propose SIEVE, a structure-aware data selection method for VLA imitation learning. SIEVE views demonstrations as compositions of reusable primitives and transition interfaces. It first discovers visuo-motor primitives from segmented trajectories, then allocates selection budgets to composition patterns by maximizing reuse-aware structural exposure under diminishing returns. Finally, it selects medoid trajectories within each composition-pattern bucket to retain central, stable, and imitation-friendly demonstrations. Experiments across multiple datasets, benchmarks, and VLA models show that SIEVE consistently outperforms competitive data selection baselines. Notably, SIEVE can surpass full-data training while using only 50% of demonstrations and 50% of training steps, suggesting that reusable structure, captured through primitives and transitions, is an important signal for efficient VLA imitation learning.

---

## 9. From Foundation to Application: Improving VLA Models in Practice

**Authors:** Wei Wu, Fangjing Wang, Fan Lu, ..., Yujun Shen, Kecheng Zheng
**arXiv:** [2607.06403](https://arxiv.org/abs/2607.06403)
**Categories:** Robotics (cs.RO)

Despite recent progress of VLA foundation models, the disparity between laboratory conditions and real-world applications continues to impede their practical implementation. To bridge this gap, we present LingBot-VLA 2.0, which advances LingBot-VLA through improvements in three functional domains. (1) Generalization across tasks and embodiments. Compared to the previous version, we revamp the data processing pipeline and curate around 60,000 hours of data for pretraining, including 50,000 hours of robot trajectories spanning 20 robot configurations and 10,000 hours of egocentric human videos. (2) Expanded action space in addition to dual-arm hardware platforms. In particular, our system accommodates degrees of freedom for the heads, waists, mobile bases, and dexterous hands, thereby empowering the robots to tackle more complex tasks in practical scenarios. (3) Predictive dynamics modeling for improved temporal reasoning. Specifically, we formulate future prediction as a proxy task, facilitated by a video representation model for semantic priors and a depth estimation model for geometric cues. Evaluations on the GM-100 benchmark, conducted in a generalist setting, validate the beneficial impact of these proposed modifications. Furthermore, benefiting from the expanded pretraining data that covers whole-body degrees of freedom, LingBot-VLA-2.0 demonstrates strong cross-embodiment long-horizon mobile manipulation capability across the two robotic platforms.

---

## 10. Diagnosing Semantic Handoff Failures in Agent-Orchestrated Vision-Language-Action Skill Composition

**Authors:** Ke Rui, Yushen Zuo, Jiawei Wang, ..., Weitao Zhou, Minglei Li
**arXiv:** [2607.06256](https://arxiv.org/abs/2607.06256)
**Categories:** Robotics (cs.RO)

Long-horizon household tasks require robots to compose many language-conditioned skills, yet the boundary between consecutive skills is rarely explicit. A skill may satisfy its own postcondition while leaving the robot, objects, or camera views in a state from which the next skill cannot reliably start. We study this semantic handoff problem in BEHAVIOR-1K through an agent-orchestrated vision-language-action execution harness. The harness invokes $\pi_{0.5}$-based skill checkpoints trained from cleaned BEHAVIOR-1K demonstrations, assigns each skill typed arguments and a step budget, and uses multi-view vision-language model verification to decide whether execution should advance, retry, or replan. To separate isolated skill competence from long-horizon compositional robustness, we evaluate the same checkpoints under two initial-state distributions: clean skill-boundary snapshots and chained terminal states produced by previous skills. Selected navigation, grasping, placement, and door-opening skills achieve 77--100% success from clean snapshots under human-reviewed verification, yet composed rollouts still frequently stall from chained states. Execution traces attribute these failures to next-skill readiness, target grounding, and low-level control execution, revealing a substantial gap between single-skill success and reliable long-horizon task completion. These findings turn near-zero end-to-end task success into actionable diagnostics, showing that future VLA skill libraries must learn robustness to the messy chained-state distribution that clean demonstrations systematically underrepresent.

---

## 11. Imagined Rollouts are Kinematic, Not Dynamic: A Diagnosis of Long-Horizon World-Model Failure

**Authors:** Finn Rasmus Schäfer, Korbinian Moller, Yuan Gao, ..., Sebastian Schmidt, Johannes Betz
**arXiv:** [2607.05966](https://arxiv.org/abs/2607.05966)
**Categories:** Robotics (cs.RO)

Long-horizon failure in world models is conventionally attributed to compounding error, a generic framing that does not distinguish what kind of error compounds. We propose a kinematic-vs-dynamic reframing: world models tend to imagine kinematically rather than dynamically. We operationalize this as the imagined Kinematic-Consistency Error, a per-step diagnostic that measures how far a rollout departs from a closed-form kinematic null, paired with a perturbation protocol that tests whether iKCE responds when physical conditions cross a regime boundary. We instantiate the diagnostic on a released DreamerV3 checkpoint trained on DMC walker-walk, where imagined iKCE runs roughly two orders of magnitude above that of matched real-physics rollouts. Across a friction sweep that crosses the gait-collapse boundary, the model's iKCE stays statistically flat even as the trained policy's reward collapses through the same range, providing the kinematic-not-dynamic signature. The diagnostic distinguishes kinematic from dynamic imagination at horizons longer than the embodiment's gait period.

---

## 12. MoWorld: A Flash World Model

**Authors:** Team Moxin, Deyi Ji, Tianrun Chen, ..., Yunhe Pan, Lingyun Sun
**arXiv:** [2607.06216](https://arxiv.org/abs/2607.06216)
**Categories:** Computer Vision and Pattern Recognition (cs.CV)

The future of World Models depends not only on scaling model capability, but also on scaling practicality and inference efficiency. High-frame-rate inference enables responsive perception, planning, and control in real-world autonomous systems. To this end, we present MoWorld, a cost-effective yet high-performance Flash World Model with an end-to-end framework spanning data generation, pre-training, distillation, and efficient inference, enabling up to 50 FPS real-time interaction with cinematic visual quality without the need of high-end GPUs. To enable large-scale real-world deployment, MoWorld jointly optimizes model capability and cost throughout the entire development pipeline. Specifically, unlike existing approaches that primarily rely on large-scale video corpora, MoWorld is built upon a scalable 3D-native data engine accumulated from our large-scale 3D vision and generative modeling pipeline, enabling the efficient construction of geometrically consistent training data across diverse real-world and synthetic environments. Based on this foundation, a curriculum cross-frame pre-training strategy for stable and scalable World Model learning, an efficient denoising-step distillation algorithm to reduce diffusion training cost, and a mixed-precision parallel inference framework for low-cost real-time deployment. MoWorld is the first real-time interactive World Model built on the Neural Processing Unit (NPU) and can achieves up to 50 FPS in such the devices, enabling practical and efficient deployment at scale. Comprehensive evaluations demonstrate that MoWorld achieves leading performance; notably, its average inference cost is only 30\%-50\% of that of existing World Models, providing a practical foundation for large-scale real-world applications of World Models. We also demonstrate diverse applications of MoWorld.

---

## 13. AlayaWorld: Long-Horizon and Playable Video World Generation

**Authors:** AlayaWorld Team, Kaipeng Zhang, Chuanhao Li, ..., Zian Meng, Zihui Gao
**arXiv:** [2607.06291](https://arxiv.org/abs/2607.06291)
**Categories:** Computer Vision and Pattern Recognition (cs.CV); Human-Computer Interaction (cs.HC)

Game worlds have traditionally been built through labor-intensive production pipelines, making them costly to develop, difficult to customization, and expensive to modify after deployment. Recent advances in video world models offer a fundamentally different paradigm. Rather than explicitly authoring every component of a virtual environment, these models autoregressively synthesize future observations conditioned on the current world state and user interactions, enabling playable worlds to be generated online. Trained on both gameplay recordings and real-world videos, they can capture diverse visual appearances and physical dynamics, opening new opportunities for interactive applications beyond gaming, including embodied intelligence. In this paper, we present \textbf{AlayaWorld}, a full-stack open-source framework for building interactive generative worlds. AlayaWorld enables open-ended real-time interaction, allowing users to freely navigate and perform diverse actions such as combat, spell casting, and monster summoning. The framework unifies the complete development-from data preparation model architecture, model training, inference acceleration, and deployment-within a modular and extensible architecture. Alongside the framework, we release reproducible pipelines, reference implementations, evaluation tools, and comprehensive documentation, establishing a practical foundation for future research and real-time applications of generative world models.

---
