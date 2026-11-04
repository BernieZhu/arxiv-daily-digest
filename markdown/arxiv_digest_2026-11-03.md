# arXiv Daily Digest — 2026-11-03

**Mode:** direct
**Categories:** cs.AI, cs.LG, cs.RO, cs.CV
**Keywords:** VLA, RSI, agentic robot, self-improving robot, self-evolving robot, robot harness
**Papers found:** 16

---

## 1. CARE: Grounded Recursive Self-Improvement for Production Customer-Service Agents

**Authors:** Yanbei Jiang, Chao Lei, Rena Gao, ..., Ke Xing, Yongjun Yin
**arXiv:** [2611.02839](https://arxiv.org/abs/2611.02839)
**Categories:** Artificial Intelligence (cs.AI)

Recursive self-improvement (RSI) in production agents involves transforming accumulated experience into reliable model updates while adapting to evolving business policies. We present CARE (Customer-service Agent Retrospective and Evolve), a grounded RSI framework that operationalizes this process in customer service. Its goal is to replace a frontier proprietary incumbent with an in-house mid-sized model that continues learning after deployment. After a one-time cold start on governed production traces, the current model serves production traffic alongside the incumbent, and its own failures drive the next update. A 24/7 inspection process establishes failures through evidence-blinded, independently reviewed judgments. Attribution separates model errors from defects in Skills, tools, or the harness, routing component failures to repair. Model-attributable trajectories are truncated at the first erroneous decision and paired with verified repairs. On-policy self-distillation (OPSD) then updates the model using the same model as teacher, with the diagnosis and repair supplied as privileged information unavailable to the student. To support continued evolution as business requirements change, training mixes failures from different Skill/SOP versions, each judged against the policy in force when it occurred. Candidates run an executable simulation test compiled from the latest SOP and then frozen, followed by offline inspection of the resulting traces. Promotion requires a combined simulation-and-inspection score at least at parity with the deployed version, confirmation through an online comparison with the incumbent, and human approval.

---

## 2. Route-Guided CBF-QP Repair for Safe Vision-Language-Action Models

**Authors:** Chan Park, Sunwoo Hong, Kirak Kim, ..., Alexander W. Olson, Ali Pesaranghader
**arXiv:** [2611.01713](https://arxiv.org/abs/2611.01713)
**Categories:** Artificial Intelligence (cs.AI); Robotics (cs.RO)

Vision-language-action (VLA) models can generate task-oriented robot actions, but they do not guarantee safe execution in obstacle-rich manipulation scenes. Although CBF-QP safety filters can locally project unsafe actions into a safe set, such correction may push the robot away from the learned task trajectory and leave the VLA policy without a reliable recovery direction. We propose Route-Guided CBF-QP Repair, a post-hoc repair module that uses the short-horizon action chunk predicted by the VLA to detect blocked nominal trajectories and generate entry-exit-rejoin guidance around obstacles. The selected route is added to the CBF-QP objective as a soft guidance term, while the CBF safety constraint remains hard. On SafeLIBERO, our method improves collision avoidance, task success, and SafeSuccess compared with AEGIS. Our project page is available at GitHub.

---

## 3. Leap-VLA: High-Rate Robot Control from a Low-Rate VLM Backbone

**Authors:** Lin Yang, Yunjie Shen, Zheyu Li, ..., Guofeng Xie, Peigen Fang
**arXiv:** [2611.01011](https://arxiv.org/abs/2611.01011)
**Categories:** Artificial Intelligence (cs.AI)

Vision-language-action (VLA) models re-encode the full observation through a multi-billion-parameter vision-language model (VLM) at every control step, even though scene semantics evolve at roughly 1 Hz while reactive control requires 20-50 Hz. We present a VLA that decouples the two: a VLM runs as a low-frequency semantic anchor whose cached context is reused across control steps, while a flow-matching action expert operates at high frequency, consuming the cached semantics with a fresh, low-latency visual stream from a compact encoder pretrained on robot video with masked reconstruction, optical flow, and depth. The measured age $\tau$ of the cache conditions the expert through adaptive layer normalization. Reusing the cache makes the policy a function of its age, and training covers that function explicitly: cache ages sampled from real episode history, plus an age-ramped pixel corruption that erases the stale snapshot the way deployed staleness corrupts content. On the asynchronous deployment stack, the recipe closes most of the staleness gap: on LIBERO-Spatial, 61.4% to 95.5% at a 2 s semantic refresh (95.9% at 1 s, within 1.6 points of the frequency-matched anchor); averaged over the four LIBERO suites, the deployed policy holds 95.2% at a 1 s refresh and 94.5% at 2 s against a 96.3% matched anchor. A forward-only chunk-boundary correction (soft-nudge), an autograd-free reformulation of real-time-chunking guidance, carries per-control-step re-planning without loss (97.1%) at zero added latency. The same lens exposes a second defect: under an instruction-scene mismatch the policy keeps manipulating the scene, and a chain-of-thought verdict gate trained on zero-cost negative episodes freezes execution exactly on mismatched instructions without hurting feasible success.

---

## 4. CalVLA: Shaping Native Confidence in Vision-Language-Action Policies with Outcome Supervision

**Authors:** Boniface Chukwuemeka Godwin
**arXiv:** [2611.00394](https://arxiv.org/abs/2611.00394)
**Categories:** Artificial Intelligence (cs.AI); Robotics (cs.RO)

Can a vision-language-action (VLA) policy signal likely task failure from its own action probabilities? We introduce CalVLA, which shapes native action-token confidence using successful and failed rollouts and an Action-Confidence Alignment (ACal) squared margin-ranking loss. Low-rank adapters update OpenVLA-7B without an auxiliary failure detector. Observations are paired within tasks at similar normalized elapsed times, not necessarily equivalent physical progress. On a held-out test split from 500 LIBERO-10 configurations, adapted confidence achieves a joint failure-discrimination AUROC of $0.7392\pm0.0480$ over three seeds, averaging scores at 130 and 260 steps. Frozen-policy probes reach 0.6146--0.6436, but superiority over the linear probe is statistically inconclusive. For the same confidence summary, AUROC rises from 0.4485 before adaptation to 0.7327 after adaptation. Mean task success decreases from 58% to 55%. These results show improved failure discrimination, not improved control or established safety benefits.

---

## 5. RecRSI: Mechanism-Guided Discovery of Recommendation Algorithms

**Authors:** Tingran Gan, Zhouziyue Lu, Dian Jin, ..., Weinan Zhang, Yong Yu
**arXiv:** [2611.02487](https://arxiv.org/abs/2611.02487)
**Categories:** Information Retrieval (cs.IR); Artificial Intelligence (cs.AI)

Improving recommendation algorithms for the Web requires coordinating interacting design choices and learning from experiments. We present RecRSI, an LLM-based research framework that uses mechanism hypotheses to organize algorithm discovery. Each hypothesis links a proposed mechanism change to a reference design, a rationale, and an expected observation. MechSpace derives implementable primitives and composition rules from the task source; Research Line uses this space and prior evidence to develop and test hypotheses; Mechanism Feedback carries outcomes and their design context into subsequent research. This organization makes each experiment inform which mechanisms to develop, revise, or combine next. Across four initial recommenders and four datasets, RecRSI yields average relative improvements of 8.48% in NDCG@5 and 6.88% in HR@5 over the initial algorithms, and 2.60% and 2.20%, respectively, over the strongest competing result for each setting and metric. Component and process studies link these gains to coordinated mechanism choices and evidence-guided follow-up. Our code is publicly available at this https URL.

---

## 6. Scene-Adaptive Readout and Decoding in Diffusion Driving VLAs

**Authors:** Seungjun Yu, Jiho Choi, Inha Kang, ..., Seungwook Kim, Hyunjung Shim
**arXiv:** [2611.02076](https://arxiv.org/abs/2611.02076)
**Categories:** Computer Vision and Pattern Recognition (cs.CV); Artificial Intelligence (cs.AI); Robotics (cs.RO)

Diffusion driving vision-language-action models repeatedly execute the backbone at every denoising stage, incurring substantial inference cost, while it remains unclear whether all scenes require the same decoding computation. To distinguish when a trajectory becomes readable from how much further refinement it requires, we analyze trajectory readout across network depth and decoding progress. We identify a depth-decoding dissociation in which late-layer representations already support useful trajectory readout after the first forward sweep, whereas early-layer representations benefit more from continued decoding. We further find that both the preferred readout layer and decoding depth vary across scenes. Based on these observations, we propose a scene-adaptive readout and decoding framework. A scene-conditioned readout MoE adaptively weights and combines trajectory predictions from layer-specific late-layer representations after a single backbone sweep, while an adaptive decoding policy applies additional native refinement only when required by the scene. We evaluate our framework on two diffusion driving VLAs across the Waymo E2E and nuScenes benchmarks. Our method improves validation RFS by up to 0.56 while also improving test performance, and achieves an end-to-end speedup of up to $6.0\times$ on Waymo E2E, while consistently reducing trajectory error on nuScenes. These results demonstrate that scene-level readout and decoding allocation improves planning quality while avoiding unnecessary decoding. Our code is available at this https URL

---

## 7. Same Path, Less Time: Training-Free Fast Execution of Vision-Language-Action Models under Inference Latency

**Authors:** Fuyi Chen
**arXiv:** [2611.01390](https://arxiv.org/abs/2611.01390)
**Categories:** Robotics (cs.RO); Machine Learning (cs.LG)

Vision-language-action (VLA) models predict chunks of future actions, yet deployed robots waste time in two ways that are independent of model capability: they halt while the next chunk is inferred, and they move at the speed of slow, cautious demonstrations. Existing remedies remove one loss each, and stacking them fails, because asynchrony and speed-up each change the correspondence between planned progress and executed motion. We present Path-preserving Time Scaling (PTS), a training-free execution layer for frozen action-chunking policies built on one principle: the robot's motion is a time reparameterization of a reference path, and the path changes only in response to new observations. A path layer decodes every replan deterministically in one step and enters it at the progress consumed during inference. A time layer sums the planned increments, keeps the arm at 1x while the gripper moves, and caps the rate by the actuator's linear range and by chunk feasibility under latency. We show that misaligned entry and stochastic sampling add a bias and a variance to the continuation error, and derive a break-even success rate that states when speeding up pays off. On LIBERO with two frozen VLAs under injected inference latency, PTS raises task throughput over the strongest deployable baseline by 33% for pi0.5 and 104% for SmolVLA while matching or improving the success rate, is best on all six model-suite combinations, and exceeds zero-latency 1x execution. Against asynchronous 1x execution with the same one-step decoder, the time layer alone adds 28% and 38%. On LIBERO-Dynamic it improves on stop-and-wait execution by 38% and is comparable to asynchronous 1x execution.

---

## 8. Behavioral Steering of Vision-Language-Action Models in the Low-Parameter Regime

**Authors:** James Tcheng, Feiyu Gavin Zhu
**arXiv:** [2611.00522](https://arxiv.org/abs/2611.00522)
**Categories:** Robotics (cs.RO); Machine Learning (cs.LG)

Reinforcement learning (RL) is increasingly used to adapt pretrained vision-language-action models (VLAs). We investigate the problem of behavioral steering: adapting a VLA's execution style to preferences such as carrying objects higher. To investigate how little trainable capacity such steering requires and how much pretrained capability can be retained, we freeze an OpenVLA-OFT 7B policy and optimize TinyLoRA adapters with 8 to 384 trainable parameters using either policy-gradient RL (GRPO) or evolutionary search (CMA-ES). With just 256 trainable parameters, we raise carry height by 120 mm on trained tasks at 92% success and by 74 mm on a held-out task at 80% success. By rescaling the learned update, we can tune the trade-off between style gains and capability retention without retraining. Increasing adapter capacity generally improves this trade-off, retaining more pretrained capability at comparable style gains. The choice of optimizer also depends on capacity, with CMA-ES being competitive at low parameter counts, while GRPO offers better trade-offs as capacity grows. These findings show that extremely low-dimensional updates can steer pretrained VLA behavior, with adapter capacity, optimizer choice, and update scaling offering practical control over adaptation and retention.

---

## 9. FineCraft: Enhancing VLA Models for Fine-Grained Manipulation

**Authors:** Shuaike Zhang, Ziheng Quan, Junhao Ran, ..., Shaokun Wang, Jianlong Wu
**arXiv:** [2611.03163](https://arxiv.org/abs/2611.03163)
**Categories:** Robotics (cs.RO)

Fine-grained manipulation couples instruction grounding, local visual precision, and sustained execution. We present FineCraft, a framework that adapts pretrained models for fine-grained manipulation in the MetaFine Challenge. A task-routed mixture of policies selects independently adapted DINOv2-DiT or pretrained $\pi_{0.5}$ policies through a common observation-action interface. Local visual features help identify the instructed object parts, demonstrations and expert continuations teach the required actions, and new observations guide replanning during execution. FineCraft ranks fourth with an overall score of $0.878$, exceeding the published reference on all five tasks. Official results and local diagnostics characterize performance across visual perturbations, instruction changes, and multi-stage manipulation. Code is available at this https URL

---

## 10. VLALagBench: Understanding When and Why VLA Inference Latency Matters

**Authors:** Qi Wen, Borui Xu, Hussein Amro, ..., Christos Kozyrakis, Wenqi Jiang
**arXiv:** [2611.03103](https://arxiv.org/abs/2611.03103)
**Categories:** Robotics (cs.RO)

Vision-language-action (VLA) models offer a promising path toward general-purpose robot manipulation. While inference latency can affect task success in a constantly evolving physical world, the relationship between latency and task success rate remains poorly understood. In this paper, we introduce VLALagBench, a comprehensive benchmark for studying VLA inference latency sensitivity across task types, object speeds, execution modes (synchronous and asynchronous), and VLA policies. Using VLALagBench, we find that even a modest inference latency of 100 ms can nearly halve task success on moving targets, with sensitivity varying substantially across tasks and policies. These differences reflect task-specific requirements for precision and continuous motion. By overlapping inference with action execution, asynchronous execution can recover some of the lost success at the cost of more frequent inference requests. Building on these findings, we develop an empirical model that predicts task success from limited calibration data, achieving root-mean-square prediction errors of only 5.7-7.8% across various VLA policies. Given an inference system's latency and per-robot throughput, these predictions guide the selection of system-specific VLA algorithm configurations to maximize task success. We believe VLALagBench and these findings provide a solid foundation for future robotics algorithm-system co-design.

---

## 11. Beyond Policy Patches: Distilling RL Specialists into Vision-Language-Action Policies

**Authors:** Zhennan Jiang, Tingying Xie, Shilong Ji, ..., Dongbin Zhao, Chao Yu
**arXiv:** [2611.02777](https://arxiv.org/abs/2611.02777)
**Categories:** Robotics (cs.RO)

Vision-language-action (VLA) policies can handle noncritical stages of long-horizon manipulation yet fail during short precision-critical phases. Lightweight reinforcement learning (RL) specialists can address these failures without directly applying RL to the full VLA, but retain auxiliary controllers and switching mechanisms at deployment. We study how to transfer their capabilities into a single flow-matching VLA. Direct imitation of specialist rollouts can reproduce action jitter and leave the VLA unprepared for states encountered during its own execution. We introduce REPAIR, a value-guided distillation framework that combines offline initialization with on-policy refinement. At each critical-phase observation, REPAIR queries the corresponding specialist for multiple action candidates and weights them using its critic to construct a supervision distribution. A shared weighted flow-matching objective trains the VLA first on observations from specialist-assisted rollouts, then on observations collected through its own execution. Specialists provide supervision without taking control during on-policy collection and are removed at deployment. Across six real-robot tasks with 30 evaluation trials per task, REPAIR achieves 100% success on all six tasks, with lower mean end-effector jerk than specialist-assisted execution on every task.

---

## 12. Recursive Self-Improvement of Exoskeleton Assistance Policies through Human-in-the-Loop Feedback

**Authors:** Muyuan Ma, Shuo Jiang, Lijun Han, ..., Houcheng Li, Long Cheng
**arXiv:** [2611.01581](https://arxiv.org/abs/2611.01581)
**Categories:** Robotics (cs.RO)

To reduce reliance on manual design and extensive parameter tuning, a framework for the autonomous evolution of exoskeleton assistance policies through human feedback is proposed. Assistance policies are autonomously generated as executable control code by an intelligent agent and evaluated in experiments with human participants. Subjective user feedback, movement performance, and muscle activation measurements are incorporated into policy assessment. Based on these assessments, policy deficiencies are autonomously identified and the control code is revised by the agent for subsequent trials. A closed loop of policy generation, human feedback, evaluation, and autonomous refinement is thereby established. The framework is evaluated using GPT, DeepSeek, GLM, and Kimi, and initial assistance performance and refinement outcomes are compared across models. Despite differences in initial performance, effective assistance is achieved with all four models after a single autonomous refinement iteration under the tested conditions. Across three tasks, biceps and triceps muscle activation levels are reduced by 29.4% and 35.2%, respectively, compared with those measured without an exoskeleton. However, limited adaptability to unexpected situations is observed, indicating that further improvements in robustness and safety are required.

---

## 13. Serving Agentic Robot Fleets: Workload Characterization, KV-Cache Thrashing, and Admission Control

**Authors:** Sida He
**arXiv:** [2611.01404](https://arxiv.org/abs/2611.01404)
**Categories:** Robotics (cs.RO); Distributed, Parallel, and Cluster Computing (cs.DC)

Agentic robots combine a vision-language brain, a tool-using harness, and a vision-language-action (VLA) policy. Serving a fleet of these agents introduces two coupled resource constraints: the brain repeatedly revisits long, growing key-value (KV) cache states, while the VLA executes action chunks under tight control deadlines. We characterize 80 LIBERO-PRO episodes generated by GPT-6-Astra, RPent, and pi0.5 (1,862 brain turns and 1,582 VLA inference chunks), profile both layers on H800 graphics processing units (GPUs), and replay the resulting agent programs on a vLLM serving engine. Brain contexts reach 215k tokens; the median Astra request takes 7.78 s, while the intervening environment-step gap is only 1.0 s. Under a 0.25 s action-chunk deadline, one VLA GPU meets the 1% starvation target for one robot; under a 1.0 s deadline, its measured capacity reaches at least 32. In sustained brain replay, increasing concurrency from 20 to 32 robots reduces throughput from about 2.4 to 0.6 requests/s as repetitive prefill displaces generation. A static active-episode cap restores 2.24-2.25 requests/s and raises completed trace-program throughput from 1.30 to 5.00-5.55 episodes/min. Our measurements expose the workload-dependent shift between action deadlines and brain KV residency, and establish practical principles for capacity planning and admission in sustained agentic robot fleets.

---

## 14. Verifying Test-State Identity in Paired Evaluation of Vision-Language-Action Models

**Authors:** Rafiqul Islam
**arXiv:** [2611.00896](https://arxiv.org/abs/2611.00896)
**Categories:** Robotics (cs.RO)

Simulation-based VLA evaluation often treats matching task, seed, and episode identifiers as sufficient evidence that two policies faced identical test conditions. Under specific vectorized reset and autoreset conditions, different termination timing can change subsequent initial-state assignment, so the same episode index need not mean the same test state. We present an evaluation-integrity framework for paired comparison - invariants I1-I5, provenance logging, optional scene fingerprints, and an automated checker - and a controlled LeRobot 0.6.1 LIBERO harness study with emulated controllers. Four evidence levels are kept separate: (A) mixed-horizon Sync wave-1 IDs [20, 5, 22, 7] vs [4, 5, 6, 7]; (B) homogeneous separate-job Sync control (16 cells, 0 ID/fingerprint mismatches); (C) Async+Freeze batch-size map differences (12 I3 mismatches; bs=8 incomplete; mechanism unisolated); (D) a synthetic McNemar illustration only. Controllers were emulated and no real-VLA shared-vector experiment was completed. We recommend checking declared/resolved init-state identity and provenance before paired statistics. We do not claim that published VLA leaderboards are generally invalid.

---

## 15. GatedVLA with Camera-Based Emergency Braking: AlpaSim E2E Closed Loop Challenge Technical Report

**Authors:** Kaneyoshi Hiratsuka, Naoki Takada, Makoto Kawano
**arXiv:** [2611.01663](https://arxiv.org/abs/2611.01663)
**Categories:** Computer Vision and Pattern Recognition (cs.CV); Robotics (cs.RO)

This report presents GatedVLA, our entry for the Physical AI AV (PAI-AV) track. Our learned vision-language-action (VLA) policy pairs the driving-pretrained Qwen-Drive-1.0-4B vision-language model with a layer-wise flow-matching action expert that outputs a 2.5 s horizon of acceleration and curvature controls, augmented with a soft visual mask applied to the expert's cross-attention. Compared to an identically trained baseline, the masked policy achieves comparable overall open-loop error while reducing error on left turns. In local closed-loop evaluation across the same 150 scenes (two rollouts per scene), the visual mask increases the mean scene score from 0.479 to 0.517 (paired difference +0.038, 95% bootstrap CI [-0.018, +0.093], wins/losses 37/26, sign test p = 0.21). Incorporating a rule-based automatic emergency braking (AEB) module at deployment further increases the mean score to 0.599 (+0.082, CI [+0.023, +0.143]) and reduces the mean number of scenes with at-fault collisions from 34.0 to 11.0.

---

## 16. RSI-Env: An Open-Ended Environment for Recursive Self-Improvement of Agents

**Authors:** Wanying Qu, Zhiyuan Fan, Jiyao Liu, ..., Yanwei Fu, Dongrui Liu
**arXiv:** [2611.01736](https://arxiv.org/abs/2611.01736)
**Categories:** Computer Vision and Pattern Recognition (cs.CV)

Recursive self-improvement (RSI) envisions agent systems that autonomously improve their own models and harnesses, with each updated system continuing to improve itself. Existing approaches typically restrict optimization objectives, editable components, or evaluation procedures, limiting open-ended exploration and continuity across generations. We introduce RSI-Env, a persistent environment for coordinated model-harness improvement, supporting autonomous training, harness modification, and retention of research state. An independent Host Controller manages services, evaluation, and versioning. Under Self, each accepted model-harness version takes over the next improvement round. We define three settings that vary goal specificity and access to benchmark feedback: Open-General, Capability-Directed, and Benchmark-Guided. Across these three settings, we compare Self with two fixed external Teachers on seven tasks, starting from Qwen3.8-27B with a minimal harness. Without benchmark feedback, Open-General Self raises GPQA Diamond accuracy from 65.2% to 73.2% and AIME 2026 accuracy from 53.3% to 56.7%. All three Capability-Directed Self runs achieve target-aligned gains. Knowledge Self demonstrates continued improvement across system updates, with SimpleQA accuracy rising from 82.0% to 85.0% and then 88.0%. Benchmark guidance and Teacher benefits vary by task. These results demonstrate RSI-Env's support for open-ended exploration and sustained recursive improvement within the studied runs, while highlighting challenges in preserving gains across capabilities.

---
