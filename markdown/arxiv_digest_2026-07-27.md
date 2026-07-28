# arXiv Daily Digest — 2026-07-27

**Mode:** direct
**Categories:** cs.AI, cs.LG, cs.RO, cs.CV
**Keywords:** VLA, world model, world action model
**Papers found:** 6

---

## 1. TRW: TRACE-RealWorld---An Auditable Consistency Contract for World Models as Materialized Views

**Authors:** Edward Y. Chang
**arXiv:** [2607.21910](https://arxiv.org/abs/2607.21910)
**Categories:** Artificial Intelligence (cs.AI); Databases (cs.DB)

TRACE-RealWorld addresses a core data-management problem: maintaining an actionable materialized view over a continuously changing physical world when reads of the base state are priced, delayed, heterogeneous, and fallible. Its data-management contributions are a commitment-level validity abstraction for materialized predictions; consequence-conditioned adaptive view maintenance; transaction-style, dependency-scoped compensation for commitments invalidated after authorization; and append-only provenance supporting exact replay. The work builds directly on materialized-view maintenance, adaptive stream synchronization, transaction recovery, sagas, data freshness, and provenance. The end-to-end Flood-SAR evaluation treats sensing as physical data acquisition and measures freshness, verification cost, stale reads, recovery scope, restoration failure, and replayability through six pre-registered questions with held-out seeds. The contribution is therefore not a new predictive model, but a consistency, recovery, and accountability contract for deploying learned world representations as operational data systems.

---

## 2. Persistent Computational State: A Session-Centric Runtime for Generative World Models

**Authors:** Zhen Lin
**arXiv:** [2607.21686](https://arxiv.org/abs/2607.21686)
**Categories:** Artificial Intelligence (cs.AI)

Generative world models are increasingly driven as simulators: a planner forks a state, rolls out futures, backtracks, and returns to a visited viewpoint. Recent benchmarks establish that current video world models fail this usage, and attribute it to the model, prescribing new architectures and training objectives. We show this attribution is incomplete, and for an important class of models simply wrong. Snapshotting the state the runtime already holds -- an observation plus RNG state, a memory bank, or a windowed KV context, by architecture -- and restoring it after a genuine excursion reproduces the never-left continuation byte-identically on all three; corrupting only the RNG degrades it. The capability was never missing: request-centric serving discarded it, inheriting from language-model serving the assumption that runtime state is recomputable -- but world-model state carries a non-recomputable kernel. We define Persistent Computational State (PCS), the minimal non-recomputable state that must survive across requests, show it can be discovered by measurement, and build a session-centric runtime over it. Checkpoint and restore cost 0.012 ms against a 1.85 s generation step; resident sessions become host- rather than device-bounded (measured to 1,024); and world memory must be evicted by relevance to the return, not recency -- the inverse of LLM practice.

---

## 3. On the Identifiability of Controlled World Models

**Authors:** Xiangteng Zhang, Yang Guan, Bo Zhang, ..., Ya-Qin Zhang, Shengbo Eben Li
**arXiv:** [2607.22430](https://arxiv.org/abs/2607.22430)
**Categories:** Machine Learning (cs.LG)

World model serves as a promising tool to infer environment dynamics under high-dimensional observations and candidate actions. Recently, LeCun's JEPA provides a compelling framework for learning such models in representation space. Its action-conditioned extension plays a central role in visual control and latent-space planning, but leaves a fundamental question: can it recover the controlled dynamics from nonlinear observations? This paper presents a joint identifiability condition for controlled world models with Gaussian latent states, which consists of two coupled components: (1) representation identifiability and (2) transition identifiability. The former depends on the spectral separation property while the latter is related to non-degenerate variation of conditional action. We prove that when this condition holds, minimizing the LeJEPA-style predictive objective can recover both latent states and controlled dynamics in the sense of orthogonal transformation. We further prove that the upper bound of transition prediction error is inversely proportional to the spectral separation margin. We also characterize an attainable amplification of counterfactual prediction error that scales inversely with the weakest conditional action-excitation margin. The theoretical predictions are empirically supported across four nonlinear observation settings.

---

## 4. Robot-Factored World Models via Robot Rendering

**Authors:** Byungjun Kim, Taeksoo Kim, Hyunsoo Cha, Hanbyul Joo
**arXiv:** [2607.22535](https://arxiv.org/abs/2607.22535)
**Categories:** Robotics (cs.RO); Computer Vision and Pattern Recognition (cs.CV)

Action-conditioned video world models predict future observations from an initial observation and an action signal. In robotics, actions influence future observations through two distinct processes: they are first realized into robot motion by the robot body and controller, and the scene then responds through contact and object motion. Conditioning directly on action commands asks the world model to learn the realization process itself, while conditioning on logged future states leaks the interaction outcomes it is meant to predict. We propose robot-factored world models, which move two robot-specific factors outside the world model. First, action realization: each command is rolled through the robot's own controller and kinematics into a deployment-available nominal trajectory, a middle signal that avoids both action-realization learning and future-state leakage. Second, robot rendering: this nominal trajectory is rendered through the robot URDF, factoring the robot's geometry, kinematics, and appearance out of the model and into explicit rendered robot geometry. To resolve depth ambiguity, we pair end-effector depth with scene depth, giving geometric cues for contact and occlusion beyond image-plane overlap. Together, camera-aware static RGB/depth context and rendered robot geometry form a shared visual world-model interface that stays consistent across viewpoints and robot embodiments, so the model sees the action only as visible robot geometry and learns how objects respond to it. Our experiments show that the rendered interface outperforms vector-conditioned baselines and generalizes to unseen robot embodiments at inference. We further demonstrate that our model generates robot manipulation videos from human demonstrations by retargeting and rendering the hand motion as robot geometry.

---

## 5. ViTacWorld: Scaling Visuo-Tactile World Models for Contact-Rich Robot Manipulation

**Authors:** Yunao Huang, Shiyu Sang, Haotao Lu, ..., Ye Shi, Jingya Wang
**arXiv:** [2607.22530](https://arxiv.org/abs/2607.22530)
**Categories:** Robotics (cs.RO)

Contact-rich robot manipulation requires physical interaction cues that are often invisible to cameras, making tactile sensing essential for robust control. However, scaling visuo-tactile robot learning remains difficult because real tactile interaction data are expensive to collect, hardware-dependent, and limited in task and scene diversity. We present ViTacWorld, an action-conditioned visuo-tactile world model for scalable contact-rich robot manipulation. ViTacWorld leverages public real tactile datasets and a constructed simulation environment to scale visuo-tactile-action data, exploiting the fact that tactile signals are directly grounded in physical contact and can exhibit a smaller simulation-to-real gap than purely visual observations. The model is first pretrained with large-scale real and simulated visuo-tactile trajectories, and then finetuned with real-world policy rollouts to better match downstream manipulation behaviors. Given robot actions, ViTacWorld predicts temporally aligned visual observations and tactile feedback, enabling visuo-tactile-action rollout generation. To the best of our knowledge, ViTacWorld is the first framework that uses a world model for robot visuo-tactile-action trajectory generation and policy evaluation. It serves two roles: synthesizing rollouts to improve downstream tactile policies, and evaluating policies by predicting action-conditioned visuo-tactile outcomes under controlled action sequences. Experiments on contact-rich manipulation tasks show that ViTacWorld generates physically meaningful rollouts, improves policy performance through scalable data augmentation, and enables action-conditioned policy evaluation. Project page: this https URL

---

## 6. Action-Conditioned World Model for Goal Plane Probe Guidance in Robotic Ultrasound

**Authors:** Siqi Fan, Mingcong Chen, Ran Liu, ..., Yunhui Liu, Hongbin Liu
**arXiv:** [2607.21918](https://arxiv.org/abs/2607.21918)
**Categories:** Robotics (cs.RO)

We present an action-conditioned world model framework for goal plane probe guidance in robotic ultrasound, with a focus on neck ultrasound scanning. Autonomous ultrasound tasks often require large numbers of probe-motion trajectories for training, but collecting high-quality demonstrations is labor-intensive and explicit simulators are difficult to build because ultrasound appearance depends on contact, tissue deformation, and view-dependent acoustic artifacts. We address this problem with a two-stage model-based learning pipeline. First, a latent conditional diffusion world model predicts future ultrasound observations from recent context frames, probe motions and temporal offset. Second, a goal-conditioned temporal transformer predicts ordered probe motions and is fine-tuned using rewards from the frozen world model. Experiments on the self-collected dataset show that the world model preserves action-dependent anatomical structure on target-directed scans. In real-world closed loop experiments, the framework achieves success rates of 70.0\% for carotid guidance and 65.0\% for thyroid guidance. These results demonstrate the potential of learned ultrasound dynamics for training goal-directed robotic probe navigation.

---
