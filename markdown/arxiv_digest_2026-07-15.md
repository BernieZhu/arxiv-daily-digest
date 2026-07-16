# arXiv Daily Digest — 2026-07-15

**Mode:** direct
**Categories:** cs.AI, cs.LG, cs.RO, cs.CV
**Keywords:** VLA, world model, world action model
**Papers found:** 7

---

## 1. From Observation to Insight: Mechanistic World Models and the Quest for Autonomous Discovery

**Authors:** Ingmar Posner, Anson Lei, Bernhard Schölkopf
**arXiv:** [2607.12474](https://arxiv.org/abs/2607.12474)
**Categories:** Artificial Intelligence (cs.AI)

Recent advances in foundation models have transformed AI for Science, enabling remarkably accurate predictive performance across domains ranging from protein folding to weather forecasting. Yet prediction alone does not constitute scientific discovery. Scientific understanding depends on uncovering the reusable explanatory mechanisms that generate observations, whereas contemporary machine learning remains fundamentally organised around predictive mappings rather than explanatory structure. In this paper, we argue that scientific discovery is fundamentally a problem of knowledge organisation. To this end, we introduce Mechanistic World Models, a new design paradigm that places reusable mechanisms at the centre of representation, computation and learning. Drawing on insights from the philosophy of science, we derive the computational capabilities required for discovery, identify the design principles and inductive pressures that encourage explanatory knowledge to emerge, and formalise the anatomy of a mechanism-centric world model. Finally, we show how diverse research directions including mechanistic interpretability, causal representation learning, equation discovery and modular architectures capture complementary ingredients of this paradigm while lacking a unified framework. We propose Mechanistic World Models as a conceptual foundation and computational blueprint for moving AI beyond predictive forecasting towards autonomous scientific discovery.

---

## 2. Mind the Gap: Promises and Pitfalls of Hierarchical Planning in LeWorldModel

**Authors:** Niccolò Caselli, Francesco Massafra, Samuele Punzo, ..., Ippokratis Pantelidis, Sathya Kamesh Bhethanabhotla
**arXiv:** [2607.12547](https://arxiv.org/abs/2607.12547)
**Categories:** Robotics (cs.RO); Artificial Intelligence (cs.AI); Machine Learning (cs.LG)

We investigate whether temporal hierarchy can improve LeWorldModel on long-horizon goal-conditioned control. We introduce Hi-LeWM, an extension that freezes the pretrained low-level LeWM and adds high-level planning over latent subgoals. We evaluate Hi-LeWM on PushT and Cube across increasing goal offsets. Hierarchy does not automatically improve performance: at short horizons, the best configuration uses a one-step high-level horizon, while longer horizons reveal a mismatch between the learned high-level action space and the inference-time search distribution. Experiments with true future latent subgoals show that the frozen low-level controller can execute well-aligned intermediate targets, indicating that high-level subgoal generation is the main bottleneck. Unconstrained search can select latent macro-actions that appear favorable under the learned model but produce poor control targets. Constraining search around macro-actions encoded from training trajectories, with appropriate subgoal execution timing, recovers useful hierarchical regimes, improving over flat LeWM by +11.3 percentage points at medium-range horizons and +14.7 percentage points at the longest PushT horizon. Overall, temporal abstraction can benefit compact frozen LeWM, but only when high-level search remains compatible with the low-level controller

---

## 3. FlowWAM: Optical Flow as a Unified Action Representation for World Action Models

**Authors:** Yixiang Chen, Peiyan Li, Yuan Xu, ..., Yan Huang, Liang Wang
**arXiv:** [2607.13017](https://arxiv.org/abs/2607.13017)
**Categories:** Robotics (cs.RO); Computer Vision and Pattern Recognition (cs.CV)

World Action Models (WAMs) are able to leverage pretrained video generators for both world modeling and action prediction. However, directly leveraging such video generators for control raises a new challenge: how to represent actions in a suitable form that aligns with pretrained video generators while carrying enough motion cues for accurate control. Existing numerical actions fail to satisfy the former, and prior visual action representations overlook the temporal motion structure across frames. We address this issue with FlowWAM, a dual-stream diffusion framework that adopts optical flow as a unified, video-native action representation. Flow videos share the same format as RGB videos and encode rich per-pixel displacement. By jointly modeling them within a shared pretrained video generator, FlowWAM can naturally implement two modes of WAMs. In policy mode, FlowWAM generates flow for action prediction, while in world-model mode, it uses target flow sequences to guide future video generation. Moreover, since flow can be easily extracted from raw videos without action labels, FlowWAM can leverage large-scale action-unlabeled video datasets for pretraining. We empirically find that our flow-based action representation delivers gains across both modes. On RoboTwin manipulation, FlowWAM raises the success rate to 92.94% on the Clean setting and 92.14% on Random, outperforming both VLA and WAM baselines. On WorldArena world modeling, it achieves the best overall EWMScore (63.71) with an 18.4% relative improvement in trajectory accuracy. More results can be found on our project website: this https URL .

---

## 4. ExToken: Structured Exploration for Efficient Vision-Language-Action Reinforcement Fine-tuning

**Authors:** Yilun Kong, Yunpeng Qing, Guozheng Ma, ..., Zhi Hou, Dacheng Tao
**arXiv:** [2607.12931](https://arxiv.org/abs/2607.12931)
**Categories:** Robotics (cs.RO)

Reinforcement Learning (RL) has demonstrated significant potential for improving Vision-Language-Action (VLA) models on complex manipulation tasks. However, its practical scalability remains severely limited by the substantial cost of environmental interactions. In this work, we first investigate the exploration stagnation bottleneck in current VLA-RL frameworks and reveal that trajectory diversity is fundamentally more important to sample efficiency than the sheer quantity of collected rollouts. Motivated by these insights, we introduce RL Exploration Token (ExToken), a simple yet general framework that condition VLA policies on discrete behavioral priors derived from offline demonstrations for structured exploration. By conditioning the policy on different tokens during rollout collection, ExToken encourages the agent to explore diverse behavioral modes, substantially improving state-action coverage and exploration efficiency. To bridge exploration during training with deterministic inference at deployment, ExToken further incorporates a state-conditioned token selector that adaptively predicts effective behavioral modes for unseen scenarios. Extensive experiments across simulated and real-world robotic manipulation tasks demonstrate that ExToken consistently accelerates convergence, improves task performance, and exhibits strong robustness under highly constrained interaction budgets.

---

## 5. TrustVLA: Mechanism-Guided Inference-Time Defense Against Vision-Language-Action Backdoors

**Authors:** Pinhan Fu, Xianda Guo, Xuetao Li, ..., Wei Sui, Mang Ye
**arXiv:** [2607.12571](https://arxiv.org/abs/2607.12571)
**Categories:** Robotics (cs.RO)

Vision-Language-Action (VLA) models are deployed through pipelines that end users cannot audit, and a poisoned VLA can behave normally on clean observations while a small visual trigger redirects a long-horizon robot policy before any failure becomes observable. Existing vision or language defenses rarely explain what a triggered VLA representation looks like or how to recover behavior without retraining. We study this gap through two independently proposed VLA attacks from groups with distinct injection strategies, BadVLA and INFUSE; the latter persists after downstream clean adaptation. Across the evaluated poisoned models, we identify a recurring internal mechanism: a \emph{compact causal footprint}, namely a small visual support that is attention-seeded, spatially compact, and \emph{causal} in a precise sense -- masking it returns a clean-calibrated evidence-evolution score to the normal operating region. This footprint motivates TrustVLA, a mechanism-guided inference-time defense that adapts the Dirichlet evidence framework from trusted classification to monitor per-token, per-layer epistemic uncertainty in VLA policies. With only a small clean calibration set, TrustVLA (i)~detects abnormal evidence evolution, (ii)~localizes the compact support by counterfactual mechanism-score drop, and (iii)~recovers the observation by localized inpainting. Across OpenVLA/LIBERO and $\pi_{0.5}$ transfer evaluations, TrustVLA reduces attack success while preserving clean-task performance, providing a retraining-free, mechanism-guided defense for visual-triggered VLA backdoors.

---

## 6. VistaVLA: Geometry- and Semantic-Aware 3D Gaussian-Grounded VLA for Robotic Manipulation

**Authors:** Mohan Liu, Zhihao Gu, Xuanyu Chen, ..., Wei-Yun Yau, Lin Wang
**arXiv:** [2607.12356](https://arxiv.org/abs/2607.12356)
**Categories:** Robotics (cs.RO)

Vision-Language-Action (VLA) models have emerged as a powerful end-to-end paradigm for robotic manipulation by mapping language instructions and 2D visual inputs directly to actions. However, these models lack an explicit, scene-level 3D representation, limiting their ability to reason over spatial layouts and geometric constraints. While recent efforts incorporate explicit 3D cues, such as depth maps or point clouds, to improve geometric awareness, they primarily capture low-level structures and lack high-level semantic grounding in 3D space. In human cognition, interaction with the physical world relies on a 3D semantic cognitive map - an internal mental model that integrates spatial layouts with semantic context to enable persistent, viewpoint-invariant reasoning. In light of this, we present VistaVLA, a novel two-stage framework that constructs a geometry- and semantics-aware 3D cognitive representation from 3D Gaussian primitives and grounds it as compact context tokens for VLA policy learning. Specifically, VistaVLA lifts multi-view vision-language features into 3D Gaussian primitives, forming geometry-anchored semantic tokens that align view-consistent spatial grounding with 2D visual feature spaces. To make this 3D representation computationally tractable for effective VLA control, we introduce Merge-then-Query (MtQ), a token summarization mechanism. MtQ compresses dense Gaussian primitives into a highly compact set of spatially informative tokens, achieving a 99% token reduction while preserving action-relevant 3D layouts and semantic context. Extensive evaluations in both simulated and real-world environments demonstrate the effectiveness of VistaVLA. Notably, in real-world scenarios, VistaVLA improves success rates by 22.8% across seven real-world tasks and by 30.0% over the VLA-Adapter baseline on challenging out-of-distribution tasks.

---

## 7. Reducing Temporal Redundancy for Efficient Vision-Language-Action Inference

**Authors:** Yuzhou Wu, Yuxin Zheng, Muchun Niu, ..., Linfeng Zhang, Chuan Wen
**arXiv:** [2607.12287](https://arxiv.org/abs/2607.12287)
**Categories:** Robotics (cs.RO)

Vision-Language-Action (VLA) models exhibit strong generalization for robotic manipulation, yet their high inference latency limits real time deployment. We identify two primary sources of temporal redundancy in existing VLA pipelines: repeated visual encoding of highly similar consecutive frames and multi step iterative sampling in diffusion based policies. To address this, we propose a system level acceleration strategy that reduces computation in both perception and action generation. On the perception side, we incrementally update only tokens corresponding to dynamic scene regions instead of re-encoding entire frames. On the policy side, we compress diffusion sampling into a compact 2-step schedule through efficiency oriented training while preserving action precision. Experiments on Libero, RobotWin, and Real Robot Platforms demonstrate over 2 times speedup while maintaining high performance, achieving up to 98% success rate on general manipulation benchmarks. Our codes will be released on Github.

---
