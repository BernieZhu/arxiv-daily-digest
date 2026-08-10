# arXiv Daily Digest — 2026-07-23

**Mode:** direct
**Categories:** cs.AI, cs.LG, cs.RO, cs.CV
**Keywords:** VLA, world model, world action model
**Papers found:** 7

---

## 1. Closing the Lab-to-Store Gap: A Data-Efficient Post-Training and Experience-Driven Learning VLA Framework for Retail Humanoids

**Authors:** Roger Sala Sisó, Tiago Silvério, Jakob Sand, Tran Nguyen Le
**arXiv:** [2607.20345](https://arxiv.org/abs/2607.20345)
**Categories:** Robotics (cs.RO); Artificial Intelligence (cs.AI)

Closing the gap between benchmark performance and reliable real-world operation remains a central challenge for Vision-Language-Action (VLA) humanoid robots, which must handle execution errors, distribution shifts, and environmental variability. This paper presents DEED (Data-Efficient Post-Training and Experience-Driven Learning), a systems-level approach evaluated on a supermarket chip-restocking task using a Unitree G1-Edu humanoid robot and the GR00T N1.6 foundation model. DEED comprises three key components: (1) a data-efficient post-training pipeline with control-frequency alignment, data curation, task-relevant visual highlighting, and reduced VLA dependence; (2) a real-world study of experience-driven refinement, adapted from RECAP via a text-based advantage prefix and a vision-language value function; and (3) a latent-space analysis tool for studying in- and out-of-distribution behavior. Our results suggest that bridging the lab-to-store gap is primarily a systems integration challenge rather than an architectural one: careful data design and targeted post-training can transform a policy that fails under naive fine-tuning into a competent real-world system using only a single GPU.

---

## 2. The World Model Remembers, the Actor Forgets: Dream Rehearsal for Continual Model-Based RL

**Authors:** Gurp Nijjer
**arXiv:** [2607.19749](https://arxiv.org/abs/2607.19749)
**Categories:** Machine Learning (cs.LG); Artificial Intelligence (cs.AI)

Model-based reinforcement-learning agents of the DreamerV3 family forget catastrophically when trained on task sequences, even when an unbounded replay buffer preserves every earlier experience. We ask a question the continual-RL literature has assumed an answer to but never measured: which component forgets? Under never-clear replay, pre-registered component-level probes (n=3 seeds throughout) show that the world model retains essentially everything measurable about old tasks -- reward discrimination (retention ratio ~1.0), value estimates, and termination structure -- while the actor's behavior collapses. Forgetting in this regime is a channel problem, not a memory problem. We demonstrate this by intervention: with the world model frozen and identical imagined rollouts, reinforcement learning in imagination fails to recover a lost skill (0/3 seeds), while supervised self-imitation on the world model's own graded dreams recovers it on 3/3 seeds with zero environment interaction. Interleaved during training, this graded dream rehearsal yields a task-label-free, parameter-constant continual learner: 3/3 four-task chains retained where plain replay passes 0/3, 3/3 eight-task chains, and consistent gains over matched real-episode cloning (paired difference +0.13, bootstrap 95% CI [0.07, 0.24], complete seed separation). The dream-grading step is load-bearing: we characterize two scoring failure modes, provide an offline selection gauge that caught both before they contaminated results, and give a realized-first grading rule that closes them. All experiments were pre-registered with committed protocols; every refuted hypothesis is reported.

---

## 3. Leveraging Offline Supervision for Efficient and Generalizable Reinforcement Learning in Large-Scale Vision-Language-Action Models

**Authors:** Dmitriy Poyarkov, Aleksei Staroverov, Aleksandr I. Panov
**arXiv:** [2607.19399](https://arxiv.org/abs/2607.19399)
**Categories:** Machine Learning (cs.LG); Artificial Intelligence (cs.AI); Computer Vision and Pattern Recognition (cs.CV)

It is commonly observed that online reinforcement learning (RL) produces better-performing strategies than offline methods across a broad range of performance measures. In particular, RL-trained policies exhibit stronger out-of-distribution (OOD) behavior, where models trained only with imitation learning approaches often struggle. A recent study introduced an OOD-focused benchmark and reported that RL-trained vision-language-action (VLA) policies achieve noticeably better OOD performance and slightly better in-distribution (IND) performance than their counterparts trained with supervised fine-tuning (SFT). In this work, we investigate whether hybrid offline-online training can combine the advantages of both approaches. Specifically, we study RL methods regularized by offline supervision via either offline data or an offline-trained reference policy. We evaluate these approaches on the OOD benchmark and compare them with both offline-only training and standard RL. Our results show that although offline training achieves limited OOD performance by itself, incorporating offline supervision into RL preserves strong OOD capability while substantially improving training efficiency. In particular, the guided methods reach performance close to that of standard RL while requiring roughly half of the training budget. Rather than producing a trade-off between speed and OOD performance, the hybrid approach retains strong OOD capability while achieving this efficiency gain. Project page: this https URL

---

## 4. Koopman Dreamer: Spectrally Constrained Latent Dynamics for Stable World-Model Imagination

**Authors:** Jiaqi Li, Xinglong Zhang, Haibin Xie, ..., Wei Pan, Xin Xu
**arXiv:** [2607.19719](https://arxiv.org/abs/2607.19719)
**Categories:** Machine Learning (cs.LG); Robotics (cs.RO)

Latent world models improve sample efficiency in continuous control by optimizing policies over imagined latent trajectories, but common neural transitions offer limited direct control over modal persistence and error accumulation in long rollouts. We propose Koopman Dreamer, a Dreamer-style world model with a spectrally constrained deterministic latent dynamics core. Its Koopman-inspired backbone uses two-dimensional rotation--scaling blocks with bounded radii to represent damping, rotation, and near-periodic modes. Linear and low-rank bilinear action terms capture global and state-dependent control effects, while stochastic-state modulation supplies local correction information. To reduce the mismatch between posterior-conditioned training and prior-only imagination, the model combines posterior-conditioned EMA teacher targets with one-step consistency, multi-step rollout, and open-loop observation-prediction objectives. We further derive a multi-step rollout-error bound that separates amplification by the spectral backbone and bilinear interaction from the additive effects of stochastic-state mismatch and modeling residuals, clarifying the trade-off between error attenuation and long-term information retention. Experimental results on proprioceptive continuous-control tasks from the DeepMind Control Suite and UAV-LiDAR autonomous navigation demonstrate that Koopman Dreamer improves the stability of long-horizon latent rollouts and achieves stronger closed-loop control performance on tasks that rely on high-quality multi-step imagination.

---

## 5. Dreamer-CPC: Message Learning with World Models for Decentralized Multi-agent Reinforcement Learning

**Authors:** Taisuke Takayama, Naoto Yoshida, Tadahiro Taniguchi
**arXiv:** [2607.19809](https://arxiv.org/abs/2607.19809)
**Categories:** Multiagent Systems (cs.MA); Machine Learning (cs.LG)

In multi-agent reinforcement learning (MARL), inter-agent communication is effective for improving performance under partial observability. Representation learning-based approaches enable decentralized agents to learn messages grounded in their own observations, but they rely only on current observations and cannot convey information accumulated over time. We propose Dreamer-CPC, a decentralized model-based MARL method that integrates message learning based on Collective Predictive Coding (CPC) into the world model of DreamerV3. Each agent independently maintains a world model and a message module, and infers and exchanges messages from the latent states of the world model that reflect the history of past observations and actions. We evaluated Dreamer-CPC in two environments: Observer, a non-cooperative information-sharing task, and CatchApple, a newly introduced task in which task-relevant observations are temporarily missing. In both environments, Dreamer-CPC outperformed IPPO-CPC, an existing CPC-based method that generates messages from current observations, as well as no-communication baselines. In particular, in CatchApple, Dreamer-CPC achieved 4 to 5 times the episode return of IPPO-CPC, demonstrating effective coordination where other methods fail due to missing observations. These results suggest that communication grounded in the latent dynamics of world models can support decentralized decision-making when current observations alone are insufficient.

---

## 6. KineBench: Benchmarking Embodied World Models via IDM-Free Kinematic Grounding

**Authors:** Zeyu Liu, Zhangzhe Zhu, Yang Zhang, ..., Chenjia Bai, Xuelong Li
**arXiv:** [2607.19876](https://arxiv.org/abs/2607.19876)
**Categories:** Robotics (cs.RO); Computer Vision and Pattern Recognition (cs.CV)

Evaluating the physical consistency of embodied world models(EWMs) is a critical open challenge. While closed-loop evaluation via simulator rollouts offers a more faithful assessment of physical plausibility than open-loop alternatives, existing frameworks almost exclusively rely on Inverse Dynamics Models(IDMs) for action extraction. Due to the intricate mapping from 2D pixel space to 3D kinematic space, the learned IDMs can be brittle to data outside their training distribution, resulting in unreliable action extraction from the generated videos with novel objects and scenarios. This creates an unavoidable attribution ambiguity between world model inaccuracies and extractor errors. To reduce this ambiguity, we present KineBench, an IDM-free closed-loop benchmark for EWMs, built upon an explicit kinematic grounding pipeline. Given a generated video, KineBench employs cascaded visual foundation models to directly extract 6D end-effector poses from individual frames, which are then executed in a physics simulator for closed-loop validation. Beyond execution-based task success, KineBench incorporates two classical 3D kinematic metrics--Spectral Arc Length (SPARC) and the Maruyama Manipulability Index--to characterize trajectory smoothness and kinematic feasibility from a robot-centric perspective. Built on 20 diverse manipulation tasks in ManiSkill3, KineBench evaluates EWMs across four progressive suites: basic execution, task transfer, visual out-of-distribution generalization, and complexity-conditioned scaling. Evaluation across frontier models reveals task-complexity-bounded nonlinear scaling in embodied video generation, providing empirical guidance for future data-scaling strategies.

---

## 7. PerceptDrive: Perception Prior World-Action Modeling with Adaptive Expert Routing for End-to-End Autonomous Driving

**Authors:** Yushan Liu, Tianxiong Lv, Bohua Wang, ..., Xiao-Ping Zhang, Wenbo Ding
**arXiv:** [2607.20175](https://arxiv.org/abs/2607.20175)
**Categories:** Computer Vision and Pattern Recognition (cs.CV)

Frozen perception foundation models encode rich geometric, semantic, and dynamic knowledge. Yet narrow conditioning interfaces may attenuate task-relevant cues, while static fusion cannot adjust expert contributions to each scene. We cast this challenge as the prior-to-plan transfer problem and introduce PerceptDrive, a perception prior world-action modeling framework with adaptive expert routing. PerceptDrive feeds teacher-distilled priors from a frozen, driving-adapted provider and dense observation latents from a frozen self-supervised video encoder into a trainable expert-routed world-action model. Expert-specific query branches process these signals, while a prior-retention objective anchors each branch to its prior. A router predicts soft gates from a shared scene representation and combines the expert conditions before trajectory generation. During training, privileged rule-based sub-metric estimates for branch-specific trajectory drafts provide soft-gate distillation targets. The predicted action-free future latent conditions a flow-matching actor. At inference, privileged components are absent; with one front-facing camera, PerceptDrive generates one trajectory per planning step without test-time scoring, reranking, or search. Experiments show that PerceptDrive achieves state-of-the-art performance with 90.4 PDMS on NAVSIM v1 and 90.2 EPDMS on NAVSIM v2, outperforming existing methods. Ablations confirm complementary gains from prior retention and scene-conditioned routing, alongside differential reliance on the three priors. These results demonstrate that preserving and adaptively routing perception priors improves direct planning without test-time candidate selection.

---
