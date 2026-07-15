# arXiv Daily Digest — 2026-07-14

**Mode:** direct
**Categories:** cs.AI, cs.LG, cs.RO, cs.CV
**Keywords:** VLA, world model, world action model
**Papers found:** 13

---

## 1. From World Action Models to Embodied Brains: A Roadmap for Open-World Physical Intelligence

**Authors:** Yuanzhi Liang, Xufeng Zhan, Haibin Huang, Chi Zhang, Xuelong Li
**arXiv:** [2607.11689](https://arxiv.org/abs/2607.11689)
**Categories:** Robotics (cs.RO); Artificial Intelligence (cs.AI)

Artificial general intelligence ultimately requires agents that can reason and act in the physical world. Action models, vision-language-action policies, and world models have advanced this goal, while World Action Models (WAMs) are particularly promising because they connect candidate interventions with predicted consequences. However, progress remains fragmented: models use incompatible action spaces and prediction targets, datasets and tasks follow different conventions, and runtime systems expose limited interfaces for reuse and evaluation. We review the evolution toward WAMs and organize these limitations into three coupled gaps: model roles and representations, objectives and standardization, and system composition. Building on this analysis, we propose a co-evolution roadmap for physical intelligence centered on the \emph{embodied brain}, a long-term model target for integrating multimodal context, comparing candidate interventions, and issuing state-transition or capability requests rather than direct actuator commands. WAMs provide promising prototypes for its predictive functions, while a physical harness grounds model outputs through tools, controllers, verification, and trace logging. Shared contracts align heterogeneous models, data, tasks, and embodiments, and closed-loop post-training converts verified interaction into reusable experience. Together, these components define a modular physical-intelligence stack for adaptive and self-improving embodied agents.

---

## 2. See like a Robot: Robot-Centric Pointmaps for Vision-Language-Action Models

**Authors:** Byungkun Lee, Dongyoon Hwang, Dongjin Kim, ..., Minho Park, Jaegul Choo
**arXiv:** [2607.11498](https://arxiv.org/abs/2607.11498)
**Categories:** Robotics (cs.RO); Artificial Intelligence (cs.AI)

Vision-language-action (VLA) models predict robot actions from visual observations and language instructions. These actions are defined in the robot's own 3D coordinate frame, yet most VLAs observe the scene in the camera frame, creating a frame mismatch between where the scene is observed and where actions are defined. The mismatch is benign under a fixed viewpoint, where the policy can memorize a single observation-to-action mapping, but grows harder as large-scale datasets aggregate demonstrations across diverse camera setups and the policy must generalize this mapping across viewpoints. We address this mismatch with robot-centric pointmaps, images whose pixels store the 3D coordinates of scene points in the robot frame. Pointmaps provide robot-frame 3D geometry while preserving the dense H x W grid expected by pretrained 2D VLAs, so they integrate into existing VLAs with minimal architectural change. On RoboCasa, pointmaps improve both pi0.5 and SmolVLA and outperform representative camera-viewpoint and 3D-aware baselines. In real-robot experiments, their advantage over an RGB-only policy widens when the camera is moved to a placement unseen during training.

---

## 3. World Models as Adversaries: Multi-Agent Self-Play Fine-Tuning for Robust Motion Planning

**Authors:** Tong Nie, Yuewen Mei, Junlin He, ..., Jian Sun, Wei Ma
**arXiv:** [2607.10630](https://arxiv.org/abs/2607.10630)
**Categories:** Robotics (cs.RO); Artificial Intelligence (cs.AI)

Robust motion planning in dense traffic requires autonomous vehicles to interact in rare and safety-critical scenarios that are underrepresented in naturalistic driving data. Although adversarial training offers a feasible solution, existing methods often rely on external scenario generators, heuristic perturbations, or simulator-heavy rollouts, which makes them difficult to integrate with modern autoregressive planners. Here, we cast adversarially robust planner learning as a constrained min-max game and propose Adversarial World Modeling (AWM), a theoretically grounded multi-agent self-play fine-tuning framework. Since solving the exact game is intractable, AWM introduces a principled decoupled solver. In the inner minimization, the planner's predictive world model is converted into a role-conditioned adversary that learns sparse, scene-adaptive attack coalitions via counterfactual credit assignment. In the outer maximization, the ego planner optimizes a regret-aware robust best response against the frozen AWM, utilizing tail-risk weighting and reference-anchored trust regions to improve hard-case recovery while preserving nominal driving behavior. Experiments on the nuPlan and InterPlan benchmarks demonstrate that our method generates transferable adversarial interactions and yields a robust planner that achieves competitive closed-loop performance in both nominal and highly interactive long-tail scenarios. Theoretical analysis justifies the decoupled solver and the main optimization components.

---

## 4. Adaptive Compute in Latent World Models: When Depth Helps, Hurts, or Doesn't Matter

**Authors:** Achyuthan Sivasankar
**arXiv:** [2607.10203](https://arxiv.org/abs/2607.10203)
**Categories:** Machine Learning (cs.LG); Artificial Intelligence (cs.AI)

Adaptive-compute world models -- early-exit or mixture-of-depths predictors that spend variable depth per step -- assume depth buys better predictions and can be routed adaptively. In autoregressive rollouts, the first assumption requires depth's per-step precision to survive composition. We test this with a pre-registered instrument, the shallow penalty $\rho=\mathrm{err}(\text{shallowest-exit rollout})/\mathrm{err}(\text{full-depth rollout})$, across nine DeepMind Control tasks under matched single-step ($K=1$) and multi-step ($K=4$) training, three seeds each. We find three regimes: on 6/9 tasks depth helps rollouts (intrinsic, $\rho$ up to $4.7\times$), on 2/9 the shallow exits beat the full stack (inversion, $\rho$ down to $0.85\times$), and one is flat. The robust inversion (cheetah) is not a property of the dynamics but is created by training: an ablation supervising early exits only at the first rollout step erases it ($\rho: 0.87\to1.18$, $n=8$, $\Delta=+0.31$), while an intrinsic-tradeoff task is unaffected -- a double dissociation we call the routability catch-22, since the supervision that makes exits routable is what trains them to out-roll the full stack. The regime is partly predictable a priori: observation/action dimensionality and one-step model error correlate with $\rho$ at $|\text{Spearman}|\approx0.75$ ($n=9$). Inside a CEM planner, $\rho$'s sign predicts whether planning benefits from depth, most sharply on the inversion task, where shallow planning beats deep. Finally, three cautions: a task's regime depends on the metric space, the rollout horizon, and the encoder. All thresholds and gates were fixed before the compute campaign, including a pre-registered negative for the hypothesis that motivated the study.

---

## 5. ActiveFly-Bench: Aligning Embodied Question Answering with Vision-Language-Action for Aerial Embodied Perception

**Authors:** Weichen Zhang, Shiquan Yu, Yinan Zhu, ..., Yong Li, Xinlei Chen
**arXiv:** [2607.10180](https://arxiv.org/abs/2607.10180)
**Categories:** Robotics (cs.RO); Artificial Intelligence (cs.AI)

We introduce ActiveFly-Bench, the first benchmark to bridge cyberspace reasoning and physical-world interaction for UAV embodied perception. The benchmark decomposes active perception into three hierarchical tasks: Aerial Embodied Question Answering (Air-EQA), Observation Behavior Planning (OBP), and Fine-grained Language-guided UAV Control (FLUC), explicitly connecting high-level task understanding, behavior planning, and low-level control. The datasets are collected from both real-world and simulated outdoor environments for training and evaluation. We further develop ActiveFly, a closed-loop UAV agent that integrates visual-language reasoning with fine-grained control, and deploy it on a physical UAV platform. Experiments with representative VLMs and VLA models show that current UAV agents still struggle with behavior planning, viewpoint adjustment, and robust task completion in active perception. These results establish ActiveFly-Bench as a new testbed for embodied aerial intelligence.

---

## 6. TS-Mask VLA: 2D Temporal-Spatial Masking for Vision-Language-Action Model with Effective Bridging

**Authors:** Shengzhuo Yang, Ronghao Yu, Chuanjie Lv, ..., Jiajun Lv, Yong Liu
**arXiv:** [2607.09818](https://arxiv.org/abs/2607.09818)
**Categories:** Robotics (cs.RO); Artificial Intelligence (cs.AI); Computer Vision and Pattern Recognition (cs.CV)

Vision-language-action (VLA) models aim to understand natural-language instructions and visual observations, and to generate and execute corresponding actions as embodied agents. Recently, autoregressive token-based action generation has driven the development of many representative VLA models. However, this paradigm often reduces action generation to next-token prediction, thereby lacking explicit modeling of the spatiotemporal structure of action sequences and the disentanglement between vision-language representations and actions, which can limit performance in long-horizon and complex scenarios. In this paper, we propose TS-Mask VLA, a vision-language-action framework for robot manipulation. TS-Mask VLA is built upon two key designs: (1) a Discrete Diffusion Action Expert equipped with a Bridge Attention conditioning bridge, which enables multi-layer conditioning from the VLM and facilitates more accurate and stable action generation; and (2) a temporal-spatial 2D masking strategy for discrete action tokens that strengthens the model's understanding of cross-time dependencies and inter-dimensional coupling, leading to more structurally consistent action sequences. We conduct extensive experiments on simulation benchmarks and real-world tasks. On LIBERO, TS-Mask VLA achieves a 95.7 percent average success rate with only 0.5B parameters, outperforming significantly larger models. On CALVIN, it attains the best average sequence length of 4.19 and strong long-horizon performance. Comprehensive analyses and ablations further validate the effectiveness of our design.

---

## 7. Maximizing Human Efficiency in Large-Scale Robot Post-Training via VLAC-Cut Guided Pipeline

**Authors:** Shaopeng Zhai, Qi Zhang, Tianyi Zhang, ..., Zhanhui Lin, Zijun Xu
**arXiv:** [2607.09776](https://arxiv.org/abs/2607.09776)
**Categories:** Robotics (cs.RO); Artificial Intelligence (cs.AI)

When adapting Vision Language Action (VLA) models to downstream tasks, multiple rounds of post training are required because a single round of data cannot resolve all issues, making continuous iterations necessary to progressively address the weaknesses exposed in previous rounds. In this report, we aim to maximize human efficiency during post-training, defined as the policy improvement and task throughput achieved per unit of human labor and time.
We propose a human-efficient post-training pipeline that enables a small number of human operators to supervise multiple robots. The pipeline is built around a specialized division of labor: a trained Teleoperator focuses on high-value remote interventions and recovery demonstrations, while a Floor Operator monitors multiple robots, triggers takeovers, and performs physical resets. This role specialization reduces task switching, lowers operator training costs, and allows limited human labor to supervise more robot interaction across a larger fleet. To improve data utilization efficiency, we introduce VLAC-CUT as an automatic rollout curation tool. It segments autonomous robot trajectories into progress-making, idle, failure-inducing, and recovery portions, preserving useful segments while filtering harmful or uninformative ones. The curated rollout data are combined with Human-in-the-Loop data for the next post-training round. We validate the proposed pipeline on four real-world manipulation tasks. Across iterative post-training rounds, the final policies achieve 80\%--95\% success rates and improve task throughput by 1.7$\times$--4.2$\times$ over the base model. Under the same human-intervention budget, VLAC-CUT guided rollout reuse outperforms HITL-only training in both success rate and throughput.

---

## 8. A Control Theory of Predictability in Latent World Models

**Authors:** Hanzhe You, Yonggang Zhang, Maohao Ran, ..., Xinmei Tian, Yike Guo
**arXiv:** [2607.10362](https://arxiv.org/abs/2607.10362)
**Categories:** Machine Learning (cs.LG)

Latent world models are trained to predict future states in a learned representation and are then deployed inside a planner that selects actions by simulating them forward. Current practice adopts the prediction error, the single- or multi-step rollout loss on held-out data, as the training and model-selection objective, on the assumption that a lower prediction error yields better control. We show that this assumption is unreliable for a structural reason: a planner does not query the model on the training distribution but on the states that its candidate actions reach, which generally leave the data manifold, so an error averaged over the data cannot by itself govern control. We therefore reframe the objective as the discrepancy between the predicted and the true plan-cost at the plan the planner commits to, and prove that the planner's suboptimality is bounded by twice this discrepancy, whereas the data-averaged prediction error neither bounds nor tracks it. Under a linear-control premise the discrepancy separates into two terms. The first is a small on-manifold residual, on which the predicted and true dynamics agree and which a spectral tax prices through the non-normality of the latent transition operator. The second is an off-manifold divergence, on which an action carries the state off the manifold and the two dynamics diverge; this divergence is the binding term and is bounded by no data-averaged error. Synthetic operators confirm the pricing formulas, and latent model-predictive control experiments confirm the decoupling: across seeds, the single-step validation error is essentially uncorrelated with control success, whereas a fidelity score on the planner-reachable measure tracks it.

---

## 9. Stateful Worlds, Stateless Elasticity: Exact-State Serving for Interactive World Models

**Authors:** Jin Li, Jiawei Chen
**arXiv:** [2607.10389](https://arxiv.org/abs/2607.10389)
**Categories:** Distributed, Parallel, and Cluster Computing (cs.DC); Machine Learning (cs.LG)

A persistent interactive world model keeps its running state resident on the GPU that serves it: a multi-gigabyte attention cache, almost all of it rewritten at every generation step. That state cannot be recomputed in interactive time or approximated without changing the world, so a live session pins its device. The pin is a scheduling problem. WorldMove moves a live session under one guarantee: the destination is bit-identical to the source, or nothing is installed. It relocates the cache in 18.8 ms same-node, 101x faster than save/load. It holds a checksum-verified 92.1-94.8 Gb/s on a 100 Gb fabric. At that rate the cache fits inside one interactive block. Migrating an actively generating session, it converges at a block boundary and the destination continues the world bit for bit. An admissibility condition decides each move. The move must complete inside the readout horizon, over bandwidth that covers the state plus its dirty rate. Lifted to a fleet schedulability test, it governed a consolidation loop that executed 48 of 48 migrations bit-identical across two providers. Two constraints are structural. Bit-exactness survives only inside a controlled configuration of one GPU architecture, so moving the state is the only way to preserve it exactly in interactive time. Verification cannot hide inside the wire on this fabric. Receive-path checksums stall the transport at protocol timescales under fan-in, and unscheduled incast silently collapses a receiver while every delivered byte stays correct. An incast-aware admission controller holds zero misses to 1.4x offered load and sheds overload as rejects. A lossless GPU codec widens the admission gate to fabrics raw motion cannot use. We exercise the serving loop and the mover separately, each end to end. Their composition on one fabric is unbuilt. Exact-state elasticity is a joint scheduling problem over transport and verification.

---

## 10. On the Efficiency of LoRA Fine-Tuning for Vision-Language-Action Models in Industrial Robotic Manipulation

**Authors:** Finn Ferchau, Daniel Pommer, Cristian Axenie
**arXiv:** [2607.10172](https://arxiv.org/abs/2607.10172)
**Categories:** Robotics (cs.RO); Machine Learning (cs.LG)

Deploying billion-parameter Vision-Language-Action (VLA) models on industrial hardware requires fine-tuning to bridge the embodiment gap. Full Fine-Tuning (FFT) provides maximal plasticity but requires data centre-grade GPUs. We present a systematic study of Low-Rank Adaptation (LoRA) for $\pi_0$, a flow-matching VLA, evaluated on four precision assembly tasks with a UR5e robotic manipulator. Across a sweep of LoRA ranks (r=8 to 256), allocation strategies, and component-freezing ablations, we find no statistically significant advantage of FFT over certain LoRA configurations. Performance saturates at r=32, and uniform allocation across the Vision-Language-Model (VLM) backbone and action expert proves sufficient. Freezing the VLM or restricting the vision encoder to LoRA significantly degrades performance, indicating that embodiment adaptation requires both semantic and visual plasticity. These results suggest that LoRA at r=32 with full vision encoder fine-tuning is a practical approach, reducing static peak VRAM from 36.2 to 10.8 GiB (parameters and optimizer states, activation memory excluded) without detectable performance loss.

---

## 11. Is Energy Guidance All You Need? Training-Free Norm Injection for Driving World Models

**Authors:** Xiyan Su, Frank Diermeyer, Markus Lienkamp
**arXiv:** [2607.10781](https://arxiv.org/abs/2607.10781)
**Categories:** Computer Vision and Pattern Recognition (cs.CV); Robotics (cs.RO)

Driving world models built on large video-diffusion backbones generate realistic scenes but are hard to control: enforcing a traffic norm typically means retraining the backbone or conditioning it on hand-built layouts. We ask whether controllability requires training at all. Our experiment shows that a rectified-flow driving world model, which jointly generates future video and a planned ego trajectory, can have its planned trajectory steered entirely at sampling time by differentiable energy functions that encode driving norms, without knowledge-specific retraining of the diffusion backbone. Concretely, we demonstrate that a world model built on Open-Sora 2.0 MM-DiT backbone can be steered to brake at a counterfactual target by injecting energy guidance at sampling time. However, we find that the generated video does not yet follow the steered trajectory through the backbone's joint self-attention and identify the cross-stream coupling as a crucial requirement for end-to-end-controllable rollouts.

---

## 12. Cycle-World: Mitigating Error Accumulation in Long-term Video World Models via Reverse-Prediction Cycle Consistency

**Authors:** Zihan Su, Teng Hu, Jiangning Zhang, ..., Lizhuang Ma, Dacheng Tao
**arXiv:** [2607.11836](https://arxiv.org/abs/2607.11836)
**Categories:** Computer Vision and Pattern Recognition (cs.CV)

Autoregressive diffusion models have enabled high-quality video generation, yet their sequential nature inherently suffers from error accumulation. In long-horizon video synthesis, minor prediction deviations compound over time, inevitably leading to unconstrained generative drift, structural collapse, and severe visual degradation. To address this, we propose Cycle-World, a novel framework designed for stable and temporally consistent long-video generation. Our approach tackles error drift by enforcing strict temporal reversibility across both the training and inference phases. Theoretically, we demonstrate that forward generative drift can be strictly bottlenecked by a cycle-consistency objective. During training, we integrate an efficient reverse-prediction model to implicitly embed causal constraints into the forward generator, compelling it to produce reversible sequences that tightly adhere to the natural video manifold. At inference time, we repurpose this frozen reverse model as a runtime corrector. Through gradient-based cycle guidance, it iteratively refines the generated latent representations, actively suppressing accumulated errors before they are committed to the historical context. Extensive experiments on the VBench benchmark demonstrate that Cycle-World's dual-phase synergy significantly mitigates error drift, achieving state-of-the-art overall generation quality and long-horizon temporal consistency in 60-second synthesis.

---

## 13. ABot-3DWorld 0: A Universal World Model to Explore Any 3D Space

**Authors:** Mingchao Sun, Luyang Tang, Yu Liu, ..., Mu Xu, Hongyu Pan
**arXiv:** [2607.11673](https://arxiv.org/abs/2607.11673)
**Categories:** Computer Vision and Pattern Recognition (cs.CV)

We present ABot-3DWorld 0, a universal multimodal 3D world model that turns text, image, and video inputs into high-fidelity, explorable 3D worlds. At the heart of our framework is a unified Spatial Generative Primitive (SGP), a compact tuple of a high-quality panorama and a spatial point cloud that delivers an efficient description of any 3D space. Multimodal inputs are first lifted into this primitive; a 3D-consistent panoramic video generator then explores the primitive along a planned trajectory; finally, our panoramic video reconstruction engine converts the generated video into a clean, photorealistic 3D Gaussian Splatting (3DGS) world. This pipeline covers two regimes: rich inputs (multi-view sets, casual video) are lifted into the SGP through a geometry-rigorous recovery that mirrors the observed scene, while a single image or sentence is completed generatively into a creative world. The result is one low-barrier engine for general 3D content creation that further anchors generated worlds to geographic points of interest, enabling map-native spatial exploration at consumer scale. Experiments show that ABot-3DWorld 0 sets the state of the art among open-source methods and demonstrates stronger scene fidelity than Marble under rich multimodal inputs.

---
