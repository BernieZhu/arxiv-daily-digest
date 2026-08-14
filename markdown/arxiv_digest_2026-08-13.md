# arXiv Daily Digest — 2026-08-13

**Mode:** direct
**Categories:** cs.AI, cs.LG, cs.RO, cs.CV
**Keywords:** VLA, world model, world action model
**Papers found:** 8

---

## 1. Foresight Without Seeing: Latent Futures for World Action Models

**Authors:** Jiakai Huang, Zhongbo Wu, Zheng Zhang, ..., Shan You, Tao Huang
**arXiv:** [2608.11605](https://arxiv.org/abs/2608.11605)
**Categories:** Artificial Intelligence (cs.AI)

World Action Models (WAMs) couple future visual prediction with robot action generation, enabling policies to model how the physical world evolves during interaction. Existing WAMs differ in how predictive dynamics are exposed to the action pathway. Explicit-future WAMs provide direct access to predicted scene evolution, but incur substantial inference costs from iterative video denoising. In contrast, direct-policy WAMs efficiently predict actions from the current observation but lack an explicit inference-time interface for exposing predictive dynamics to the Action DiT. To bridge this gap, we propose ForeWAM, a dynamics-conditioned direct-policy WAM that provides predictive context for action generation without decoding future videos. At its core, Future-KV performs a single Video DiT prefill over the current visual latent and stochastic future slots, and reuses the resulting layer-wise key-value states throughout action denoising. We further introduce dynamics registers supervised by a frozen latent action teacher, encouraging the implicit future states to capture interaction-induced transitions such as object motion, contact changes, and task progress. Ground-truth future observations and the teacher are used only during training; deployment requires neither and performs no future video generation. Without embodied robot data pretraining, the standard and accelerated variants of ForeWAM achieve average success rates of 96.7% and 96.9% on LIBERO, respectively. The standard variant further achieves 61.6% success on LIBERO-Plus. These results demonstrate that direct-policy WAMs can retain efficient action prediction while exposing predictive dynamics to the action pathway without explicitly generating future observations.

---

## 2. AutoWorldModel-Bench: A State-Centric Benchmark for Automated World-Model Research

**Authors:** Marjan Moodi, Xuankang Zhu, Fernando De Mesentier Silva, Harold Chaput, Mohammad Reza Taesiri
**arXiv:** [2608.11216](https://arxiv.org/abs/2608.11216)
**Categories:** Artificial Intelligence (cs.AI)

World modeling is an unsettled field: architectures, training objectives, and state representations interact in complex ways, and no single recipe dominates across environments. This makes it an ideal testbed for AI coding agents acting as autonomous researchers--a setting in which the improvement direction is not specified in advance, unlike the engineering-to-spec tasks that dominate current agent benchmarks. We introduce AutoWorldModel-Bench, a closed-loop benchmark in which frontier coding agents autonomously improve a provided world-model starter under a fixed compute budget. The benchmark spans eight game environments under a unified structured-state representation--ground-truth entity state extracted from each game and consumed through a shared tensor format--which isolates dynamics modeling from perception and enables minutes-per-run iteration. Across 64 sessions, Codex-5.4 and Claude Opus 4.6 improve their starter on 63; in 91% of sessions the winning edit is a non-trivial research-style modification--a new objective, representation, rollout procedure, or architectural change--rather than a hyperparameter tweak. Our benchmark offers a setting in which frontier coding agents can be evaluated on open-ended research rather than engineering-to-spec problems.

---

## 3. Better Slots, Better Worlds: Representation Quality & Robustness in Object-Centric World Models

**Authors:** Shukrullo Nazirjonov, Sai Prasanna, Anna Manasyan, Georg Martius
**arXiv:** [2608.12078](https://arxiv.org/abs/2608.12078)
**Categories:** Computer Vision and Pattern Recognition (cs.CV); Artificial Intelligence (cs.AI); Machine Learning (cs.LG)

Learning world models from offline trajectories enables agents to accomplish different tasks through planning. Object-centric (OC) representations, which decompose a scene into a set of slots that bind to its objects, have been proposed as an inductive bias for world models that are more sample-efficient and generalize better. Yet prior object-centric world models (OCWMs) take the slot encoder as given and evaluate only in-distribution, leaving open whether the object-centric bias actually delivers for planning and what within the OCWM drives it. We conduct a controlled study of OCWMs for visual model-predictive control along two axes: object-centric representation quality and generalization under distribution shift relative to scene-centric models. We find that (i) planning success correlates positively with unsupervised slot-quality metrics (FG-ARI, mBO), though the gains saturate at high slot quality; (ii) with well-bound slots, the auxiliary proprioception inputs and masking inductive bias that prior methods relied on become unnecessary; and (iii) under unseen distribution shifts, the OCWM with well-bound slots is more robust overall than the end-to-end trained scene-centric LeWM, while DINO-WM, built on similar frozen pretrained features, remains competitive -- pointing to pretrained features as a key contributor to robustness.

---

## 4. Keep the Future, Drop the Rollout: RIFT for World Action Models

**Authors:** Chushan Zhang, Jinguang Tong, Xuesong Li, Yikai Wang, Hongdong Li
**arXiv:** [2608.11521](https://arxiv.org/abs/2608.11521)
**Categories:** Robotics (cs.RO); Artificial Intelligence (cs.AI)

World action models (WAMs) condition robot actions on predicted futures, but iterative video rollout increases deployment latency. We ask whether action generation requires the evolving rollout trajectory or only its future representation. Across four WAMs on all 40 LIBERO tasks, paired closed-loop interventions show that masking or reassigning future-cache values changes execution and reduces success, indicating sensitivity to future values and their assigned positions. For Joint and Cosmos-2, however, replaying one fixed final-clean key/value (K/V) cache nearly preserves unmodified execution, with $1.7$ to $1.9$~cm end-effector average displacement error and $97.9\%$ to $98.2\%$ success. This separates cache consumption from production: these models can reuse a fixed cache but still require iterative rollout to construct it. We therefore propose RIFT (\emph{Rollout-free Imagination via Future Tokens}), which uses learned anticipation tokens to construct a complete future K/V cache in one backbone pass while retaining the original future-read interface. On LIBERO, RIFT achieves $98.8\%$ success, close to rollout-based Joint, IDM, and LingBot-VA at $98.4\%$ to $98.6\%$, while reducing action-chunk latency by $68.2\%$ to $89.1\%$. On RoboTwin~2.0, RIFT reaches $92.9/92.6\%$ on clean/randomized scenes, the highest observed among the evaluated methods. These results support rollout-free future conditioning without iterative video generation at deployment.

---

## 5. StellaVLA: In-Context Structured Demonstration for Generalizable Vision-Language-Action Models

**Authors:** Siyu Xu, Yunke Wang, Zijian Wang, ..., Tao Huang, Chang Xu
**arXiv:** [2608.11671](https://arxiv.org/abs/2608.11671)
**Categories:** Robotics (cs.RO)

Vision-Language-Action (VLA) models can follow instructions and manipulate objects, but their performance often collapses out of distribution (OOD), when the scene, viewpoint, or object differs from training. Adapting to each new situation typically requires collecting more data and fine-tuning. We present StellaVLA, a framework that instead adapts at test time by conditioning on a single retrieved demonstration. The key idea is to move beyond imitating what an expert did and instead convey why: an automated offline pipeline converts each raw trajectory into a structured demonstration, e.g., a task plan, sub-goal descriptions, and verbalized 3D motion, at zero human-annotation cost. Provided as in-context guidance, this structured demonstration lets the policy reason about the task rather than mimic a pixel trajectory, which also makes it transferable across embodiments (real-robot, human-hand, or XR demonstrations). A parallel dual-training design internalizes this reasoning during training through a joint action-and-language objective, while inference uses the action expert alone, preserving real-time, high-frequency control with no added latency. On the VLA-Arena leaderboard(Aug 1, 2026), StellaVLA ranks first with an overall score of 0.63, versus 0.44 and 0.22 for the strong prior models ($\pi_{0.5}$ and LingBot-VLA), and it further leads on LIBERO with 98.8% average success rate and LIBERO-Plus with 85.1% success rate. Our real-robot benchmark demonstrates that StellaVLA can use both human/robot demos and human-to-robot (XR) demos as in-context structured demonstration to help VLA model adapt to OOD tasks.

---

## 6. World Tokens: Enhancing Embodied Policies with Training-Time World Modeling

**Authors:** Qu Tang, Benhui Zhuang, Bo Yuan, ..., Longteng Guo, Junlan Feng
**arXiv:** [2608.09730](https://arxiv.org/abs/2608.09730)
**Categories:** Computer Vision and Pattern Recognition (cs.CV); Robotics (cs.RO)

Vision-language-action (VLA) models are a widely adopted paradigm for embodied policies. They excel at efficient closed-loop control but do not explicitly model how physical scenes evolve as a task unfolds. Recently emerging world-action models (WAMs) leverage pretrained video world models to capture spatiotemporal evolution, yet retaining future generation or a large video backbone in the control loop substantially increases inference cost. We introduce World Tokens, an embodied policy architecture built around a World Adapter that bridges visual-language understanding, world-dynamics modeling, and action generation. It uses world modeling during training to enhance the action policy while preserving efficient deployment. Specifically, the World Adapter transforms VLM features into a fixed set of world tokens, which condition a jointly fine-tuned future-video denoiser and simultaneously serve as the action expert's sole visual-language context. This shared conditioning allows gradients from future-video denoising to directly shape the representation used for action prediction, while exclusive routing prevents the policy from bypassing that representation. At deployment, the world-model branch is removed, leaving only the VLM, World Adapter, and action expert, with no online video-model inference. With a 2B backbone and no embodied action pretraining, World Tokens is highly competitive on LIBERO, attains the best reported averages on SIMPLER, substantially improves real-world R1 Pro success over a matched action-only baseline, and generates each action chunk at VLA-level latency.

---

## 7. Early Warning Signals for OpenVLA Failure under Visual Distribution Shift

**Authors:** Dipesh Tharu Mahato, Rachel Ren
**arXiv:** [2606.29699](https://arxiv.org/abs/2606.29699)
**Categories:** Computer Vision and Pattern Recognition (cs.CV); Artificial Intelligence (cs.AI); Robotics (cs.RO)

Visual shifts can cause a vision-language-action policy to fail after initially plausible behavior. We ask whether OpenVLA's internal activations contain signals associated with the steps before failure. We freeze the policy, record one MLP activation per LIBERO-10 step, and fit two linear monitors. Occlusion reduces task success from $57\%$ to $17\%$. Within failed matched-reset trajectories, a layer-16 logistic probe attains AUROC $0.972$ and AUPRC $0.352$, whereas action disagreement attains AUROC $0.496$. Without refitting, the occlusion-trained probe reaches AUROC $0.689$ on failed camera-jitter episodes. In a calibration check, however, the same layer-16 monitor averages 3.32 warning onsets per clean episode. This contrast shows that strong retrospective discrimination does not imply operationally quiet warning behavior. Because fitting and evaluation share tasks, resets, and seed, these results establish retrospective separability rather than prediction on independent episodes.

---

## 8. How Can Driving World Models Do Counterfactual Prediction?

**Authors:** Jiaru Zhang, Can Cui, Yi Xu, ..., Ruqi Zhang, Ziran Wang
**arXiv:** [2608.11601](https://arxiv.org/abs/2608.11601)
**Categories:** Computer Vision and Pattern Recognition (cs.CV)

Driving world models are often interpreted as counterfactual simulators for observed driving episodes: given a factual driving log, they are asked what would have happened under an alternative ego action. In this paper, we identify a fundamental mismatch between this goal and direct action-conditioned prediction. The direct prediction uses the shared history and the alternative action but not the factual continuation observed after that history. It can therefore generate a plausible future without preserving what actually happened in this episode. We formalize this gap using the causal recipe of abduction, action, and prediction and study it in a setting with a short time horizon, where the alternative ego action does not alter how surrounding agents evolve. To make the gap measurable, we construct a controlled simulation benchmark with factual outcomes and matched counterfactual outcomes. Across two representative world models, direct predictions fail to match the counterfactual ground truth, supporting our analysis. As a constructive check of this analysis, we introduce a deliberately simple, training-free pipeline that moves observed evidence into the counterfactual view and lets the frozen model complete what remains unknown. Even this simple construction raises the overall recovered fraction substantially and reduces perceptual distance to the matched counterfactual on both models. We hope this work draws attention to this gap and motivates better counterfactual prediction methods for driving world models.

---
