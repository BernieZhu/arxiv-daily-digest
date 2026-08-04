# arXiv Daily Digest — 2026-08-03

**Mode:** direct
**Categories:** cs.AI, cs.LG, cs.RO, cs.CV
**Keywords:** VLA, world model, world action model
**Papers found:** 8

---

## 1. DreamQAS: Learning a Decision-Useful World Model for VQE-Efficient Quantum Architecture Search

**Authors:** Jiayang Niu, Yan Wang, Jie Li, ..., Muhammad Usman, Yongli Ren
**arXiv:** [2607.29491](https://arxiv.org/abs/2607.29491)
**Categories:** Machine Learning (cs.LG); Artificial Intelligence (cs.AI)

Reinforcement-learning-based quantum architecture search (RL-QAS) repeatedly optimizes a variational quantum eigensolver (VQE) after extending a circuit, although circuit construction and action legality are deterministic and known. We introduce DreamQAS, a model-based RL framework that preserves these exact circuit dynamics and learns only the expensive post-VQE feedback. A recurrent randomized-prior ensemble predicts an oracle-free score relative to an empirical energy frontier and supports multi-step imagined policy learning over explicit legal circuits. Ranking-based activation, uncertainty-aware pessimism and truncation, and selective real-VQE verification form a reliability-controlled learning loop. Under a common 15,000-episode budget and frozen evaluation for the RL methods, DreamQAS has the lowest mean frozen-policy energy error on four of five molecular tasks and the second-lowest on one. At fine-error targets reached by all seeds of both methods, it uses 1.6x to 2.0x fewer real VQE calls on four tasks and 10.6x fewer on BeH2-8q. Counterfactual action-ranking utility increases across all five tasks, with a mean increase of 0.346 and a 95 percent confidence interval of [0.185, 0.507], while direct greedy and beam use of the same model does not recover the gains of imagined policy learning. Ensemble disagreement also improves risk-coverage over random rejection on all three probed tasks. These results establish a world-model design for QAS whose value lies in decision-useful feedback rather than exact energy prediction.

---

## 2. FBFM: A Training-Free Asynchronous Feedback Mechanism for Flow-Matching in World-Action Models Execution

**Authors:** Peize Li, Ruimeng Zhang, Ru Zhang, ..., Kai Chen, Shanghang Zhang
**arXiv:** [2607.29235](https://arxiv.org/abs/2607.29235)
**Categories:** Robotics (cs.RO); Artificial Intelligence (cs.AI); Systems and Control (eess.SY)

Although world-action models (WAMs) enhance long-horizon robot control by predicting visual evolution before acting, long-horizon reliability demands repeated re-grounding in real observations--not recursive rollout. Existing WAMs address this by refreshing history or KV cache with ground-truth data between chunks. However, such chunk-wise feedback operates at a coarse temporal granularity and thus fails to correct prediction errors at the individual time-step level. To address this, we propose Feedback Flow Matching (FBFM), a training-free inference mechanism that pushes re-grounding inside the actively generated chunk. During flow matching, FBFM applies a masked pseudoinverse correction to the conditional velocity field: it leverages the preceding action chunk to guide generation of the next action chunk, and uses the image observed after executing that preceding chunk to guide the next frame prediction. This cross-chunk pairing--where feedback from one chunk arrives in time to shape the next--creates an asynchronous loop that corrects errors without waiting for chunk boundaries. Being training-free, the mechanism improves responsiveness to unexpected events and suppresses drift in long-horizon tasks. We evaluate FBFM on both a joint-generation WAM (DreamZero) and a stage-wise WAM (LingBot-VA). On selected LIBERO and RoboTwin2.0 tasks, it improves success rates by over 5% in favorable settings, and real-world robot observation-prediction diagnostics show notably better tracking. We argue that FBFM offers a new paradigm for fine-grained online correction, bridging open-loop flow generation with closed-loop real-world dynamics.

---

## 3. ActFovea: Runtime Safeguarding for VLA Policies via Spatiotemporal Visual-Action Consistency

**Authors:** Wenda Yu, Tianshi Wang, Fengling Li, ..., Jingjing Li, Lei Zhu
**arXiv:** [2607.29169](https://arxiv.org/abs/2607.29169)
**Categories:** Robotics (cs.RO); Artificial Intelligence (cs.AI)

Vision-language-action (VLA) policies achieve strong performance in robotic manipulation but remain vulnerable to runtime disturbances that break the temporal alignment among visual observations, robot states, and executed actions. We introduce ActFovea, a plug-and-play safeguarding framework that detects and mitigates such failures without retraining or modifying the underlying VLA policy. ActFovea uses robot kinematics, proprioceptive states, and recent actions to construct action-conditioned foveated regions that retain contact-relevant areas and predicted motion corridors while suppressing task-irrelevant visual content. It detects runtime risks by evaluating whether visual motion and observation freshness remain consistent with geometric, proprioceptive, and action transitions. For recoverable disturbances, ActFovea constructs disturbance-specific candidate observations and accepts a recovery only after verifying the resulting action chunk. When stale or replayed observations make reliable recovery impossible, it invokes a bounded safe-failure procedure. In closed-loop evaluations of $\pi_0$ across multiple LIBERO suites, ActFovea increases success under localized visual overlays from 49.3\% to 90.3\%, closing 93.7\% of the gap to clean performance. It further improves success under action drift and visual delay by 7.0 and 9.8 percentage points, respectively, while preserving clean-task performance. Under frozen-observation replay, ActFovea triggers timely safe failure in all trials, with no unprotected failures. These results demonstrate that spatiotemporal visual-action consistency provides an effective basis for runtime safeguarding of VLA policies.

---

## 4. Auto-JEPA: A Latent World Model of Continuous Intent for End-to-End Autonomous Driving

**Authors:** Jiwei Yang, Zhengxian Chen, Chaosheng Huang, Jun Li
**arXiv:** [2607.29031](https://arxiv.org/abs/2607.29031)
**Categories:** Robotics (cs.RO); Artificial Intelligence (cs.AI)

Existing autonomous-driving world models typically perform dense prediction of future videos, occupancy states, BEV representations, or agent motion. We argue that planning need not reconstruct the complete future world, but only focus on scene features that affect future ego action. Based on this perspective, we propose Auto-JEPA, an action-oriented latent world model that learns continuous future driving intent through joint-embedding prediction. Given visual observations, egomotion history, and navigation commands, Auto-JEPA predicts an intent embedding aligned with the latent representation of the future ego trajectory. The predicted intent retrieves executable trajectories from a fixed trajectory memory, which are then ranked by a scene-conditioned candidate selection module. Auto-JEPA keeps the visual encoder frozen, requires no explicit perception annotations, and uses no learned trajectory generator. By optimizing only task-specific modules for trajectory representation, intent prediction, and candidate selection, Auto-JEPA achieves 91.3 PDMS on NAVSIM v1 and 89.1 EPDMS on NAVSIM v2. Semantic occlusion experiments show that masking dynamic-agent regions induces an average intent change 2.97x that of equal-area random masking. Moreover, occluding vehicles that affect future driving substantially changes the predicted intent and selected trajectory, whereas both remain essentially unchanged when non-influential vehicles are occluded. These results show that future-intent prediction encourages the model to focus on planning-relevant visual features and supports high-quality planning without dense future-world modeling.

---

## 5. WCM: A World Critic Model for Vision-Language-Action Reinforcement Learning

**Authors:** Senyu Fei, Xiaopeng Yu, Siyin Wang, ..., Jingjing Gong, Xipeng Qiu
**arXiv:** [2607.29613](https://arxiv.org/abs/2607.29613)
**Categories:** Robotics (cs.RO); Computation and Language (cs.CL); Computer Vision and Pattern Recognition (cs.CV)

Reinforcement learning (RL) post-training of Vision-Language-Action (VLA) models has shown strong promise for robotic manipulation. Among RL methods, critic-based approaches rely on a value estimator that predominantly operates on single-frame observations or single-frame VLM backbone latents, which is a fundamental mismatch with the partially observable nature of robot control. A naive approach to incorporate observation history into the critic incurs exponential complexity with high-dimensional visual space, and still fails because pure scalar-return regression provides insufficient supervision for learning cross-temporal dynamics. We identify the root cause as a state approximation problem: without an explicit world modeling objective, the critic's representation cannot capture the temporal structure needed for accurate value estimation. To address this, we propose the World Critic Model (WCM), built on a lightweight LeJEPA architecture; WCM jointly predicts future latent state and estimates values, such that the critic's representation is explicitly trained to capture temporal dynamics rather than merely regress scalar returns. WCM integrates seamlessly into both on-policy and off-policy training pipelines and is compatible with state-of-the-art VLA backbones including Pi0, Pi0.5, and OpenVLA-OFT. Extensive experiments on 149 tasks across four benchmarks demonstrate that WCM consistently achieves state-of-the-art performance in both in-distribution and out-of-distribution settings, with particularly strong generalization gains. We further validate WCM on seven real-world manipulation tasks using OpenVLA-OFT and Pi0.5 with off-policy RL, confirming stable deployment across diverse settings.

---

## 6. FibVLA: An Efficient Temporal Vision-Language-Action Model with Fibonacci Sampling

**Authors:** Li Lin, Wujun Xu, Weiwei Meng, ..., Kang Hao Cheong, Shuai Wang
**arXiv:** [2607.29596](https://arxiv.org/abs/2607.29596)
**Categories:** Robotics (cs.RO); Computer Vision and Pattern Recognition (cs.CV)

Vision-language-action models (VLAs), which leverage the cognition of multimodal information to infer physical-world actions, provide a generalized solution for embodied AI applications. Conventional VLAs usually concentrate on current digital cognition. While some efforts are made to enhance VLAs' reasoning capabilities by capturing temporal information, encoding the long-context history causes an efficiency-decreasing issue. To reconcile the conflict between capturing temporal information and maintaining inference efficiency in VLAs, this paper introduces FibVLA, an efficient framework featuring temporal perception of long-context history. Specifically, we leverage logarithmic hindsight sampling to both proprioceptive states and visual frames to capture long-term temporal dependencies with minimal redundancy. For the action expert, we introduce the flow matching to produce action distributions, and the Fibonacci recurrent inference strategy to generate long-range planning steps based on real-time closed-loop feedback. Experiments demonstrate that FibVLA significantly improves action smoothness and success rates without retraining large-scale visual encoders. Efficiency analysis demonstrates superior real-time responsiveness compared to video-based baselines in real-world evaluations.

---

## 7. Safe Vision Language Action Models via Barrier Enhanced Flow Matching

**Authors:** Kasra Sinaei, Hung-Chieh Wu, Donald Ebeigbe
**arXiv:** [2607.29569](https://arxiv.org/abs/2607.29569)
**Categories:** Robotics (cs.RO); Systems and Control (eess.SY)

This article presents a modular inference framework that integrates Flow Matching generative models with formal Control Barrier Function (CBF) safety guarantees. Unlike existing methods that apply external safety filters to a model's final output, our approach modifies the Flow Matching denoising process within the model to inherently generate safe trajectories. By employing a smooth Log-Sum-Exponential aggregate barrier, we enforce safety over entire action chunks. This aggregate barrier ensures a minimal increase in computational overhead and does not alter the semantic intent of the model. We show that, within the proposed framework, the 2-Wasserstein distance between the generated distribution and the target distribution remains bounded. Our method eliminates the need for safety-specific datasets or costly model retraining, providing a versatile solution for safe inference. We validate the approach on two robotic manipulation platforms and a 2D navigation benchmark, verifying that our framework achieves reliable safety without degrading the success rate of the model.

---

## 8. ST-WAM: Semantic-Temporal World Action Model for Robust Manipulation under Visual Distribution Shifts

**Authors:** Mingxin Wang, Bin Hu, Bin Qian, ..., Houde Liu, Tianlun Li
**arXiv:** [2607.28993](https://arxiv.org/abs/2607.28993)
**Categories:** Robotics (cs.RO); Computer Vision and Pattern Recognition (cs.CV)

World Action Models (WAMs) have emerged as a promising paradigm by jointly modeling robot actions and future visual dynamics. However, their reliance on pixel-generative future supervision can entangle action-relevant state transitions with task-irrelevant visual content, limiting robustness under visual distribution shifts. We identify Training-Distribution Hallucination, a recurring phenomenon in which futures conditioned on visually shifted observations hallucinate training-domain content rather than remain faithful to the current scene. A controlled frame-triplet diagnosis further shows that DINOv3 features remain more stable across visual shifts while better preserving task-state distinctions than Wan-VAE latents. Rather than correcting the predicted futures, we propose Semantic-Temporal WAM (ST-WAM) to improve action robustness by using DINOv3 as a shared semantic representation for future prediction and history retrieval while retaining fine-grained VAE dynamics. Its Dual-Space Future Experts (DSFE) jointly predict future VAE latents and DINO features, while Current-Anchored Intent Retrieval (CAIR) retrieves task-relevant evidence from recent DINO history under the current visual-language context. ST-WAM is trained end-to-end without additional embodied pretraining or task-specific annotations, and requires no explicit future generation at inference. It achieves 98.7% on LIBERO and 92.8% on RoboTwin 2.0; more importantly, compared with Fast-WAM, it improves zero-shot LIBERO-Plus performance by 21.3 percentage points and more than doubles real-world success under visual shifts from 25.8% to 61.5%. These results demonstrate that semantic-temporal modeling effectively complements pixel-generative dynamics for robust manipulation.

---
