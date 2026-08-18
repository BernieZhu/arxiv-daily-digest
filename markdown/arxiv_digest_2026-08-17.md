# arXiv Daily Digest — 2026-08-17

**Mode:** direct
**Categories:** cs.AI, cs.LG, cs.RO, cs.CV
**Keywords:** VLA, world model, world action model
**Papers found:** 8

---

## 1. Traj-LeWM: Path-Aware World-Model Planning via Latent Trajectory Cost

**Authors:** Xiaodi Huang, Ziyi Ding, Jingtian Wan, ..., Zhang Zhang, Tao Huang
**arXiv:** [2608.14125](https://arxiv.org/abs/2608.14125)
**Categories:** Artificial Intelligence (cs.AI)

LeWM is a lightweight visual world model that learns latent dynamics end-to-end from pixels and ranks candidate action sequences by the distance between their predicted endpoints and the goal. However, LeWM has two limitations. First, during training, it learns local next-step transitions without evaluating complete trajectories relative to the task goal. Second, during planning, it ranks candidates solely by predicted endpoint distance. Because model predictions may differ from actual execution outcomes, the candidate whose predicted endpoint is closest to the goal may not perform best when executed in the environment. The evolution of the complete predicted trajectory can therefore provide complementary information beyond endpoint distance. To address these limitations, we propose Traj-LeWM, which retains LeWM's local-dynamics objective and endpoint score while introducing a goal-conditioned latent trajectory cost (LTC) that aggregates trajectory-level information as a complementary signal. During training, LTC-based trajectory-preference supervision complements next-step prediction in shaping the shared representation. During planning, LTC is combined with endpoint distance to incorporate intermediate-path information into candidate ranking. With joint endpoint-plus-LTC scoring, Traj-LeWM outperforms LeWM on Push-T, OGBench-Cube, Reacher, and Two-Room by $3$, $14$, $7$, and $7$ percentage points, respectively. Controlled experiments and ablations further verify the complementary roles of trajectory-level representation shaping and path-aware candidate ranking.

---

## 2. Reflex: Enabling Fast and Predictive Vision-Language-Action Models for Reaction-Critical Manipulation

**Authors:** Yuxuan Chen, Wanruo Zhang, Xiao Li
**arXiv:** [2608.14379](https://arxiv.org/abs/2608.14379)
**Categories:** Robotics (cs.RO); Artificial Intelligence (cs.AI)

Vision-Language-Action (VLA) models have recently achieved promising performance in robotic manipulation. However, existing benchmarks mainly evaluate generalization on static manipulation tasks and largely overlook dynamic interaction scenarios. To address this gap, we present ReflexBench, a benchmark for reaction-critical manipulation. ReflexBench contains six dynamic tasks and introduces an evaluation framework that decouples simulator stepping from robot control while supporting configurable latency under synchronous and asynchronous inference. Building upon ReflexBench, we propose ReflexVLA, an efficient VLA model designed for reaction-critical manipulation without large-scale robot-data pretraining. ReflexVLA enhances temporal reasoning through latent future prediction and multi-frame temporal fusion within the vision backbone, while reducing deployment latency through batched visual encoding and CUDA Graph replay. Experiments show that ReflexVLA consistently improves dynamic manipulation performance while maintaining competitive accuracy on standard static manipulation benchmarks, and real-world experiments further demonstrate its effectiveness under practical deployment conditions. Project website: this https URL

---

## 3. Evolve Vision-Language-Action Model into an Agent with On-the-fly Tool-use

**Authors:** Yi Ding, Yanzhao Yu, Xili Dai, ..., Xiangyu Yue, Jianan Wang
**arXiv:** [2608.14047](https://arxiv.org/abs/2608.14047)
**Categories:** Robotics (cs.RO); Artificial Intelligence (cs.AI); Computer Vision and Pattern Recognition (cs.CV)

This paper integrates end-to-end Visual-Language-Action (VLA) models with agentic tool-use to propose Agentic Robot with Tool-use (ART). ART is a tool-injection framework that tunes any VLA model to leverage off-the-shelf tool modules for low-level vision, high-level affordance, and embodiment enhancement. Compared to vanilla VLA models with a whole continuous action solution space, ART reduces the complexity of the action solution space through tool-use, which not only improves generalizability across different tasks but also reduces data dependency. To demonstrate the advantages (high generalizability and low data dependency) of this framework, we first built a dataset of 30K tool-use trajectories and action demonstrations, which is much smaller than those used by baseline methods. We then designed a training regimen for long-trajectory tool-use reasoning in challenging environments. Experiments show that ART achieves a 20% higher success rate than mainstream baselines on simulation and real-world tasks, such as pick-and-place in the dark at novel viewpoints. Empirical results highlight the benefits of an agent-based approach: modular tool utilization enables more efficient training, lightweight deployment, and scalable integration of new tools. This design fosters robustness, adaptability, and extensibility, paving the way for the practical deployment of VLA systems in complex real-world scenarios.

---

## 4. ForgeWM: Progressive Causal Training for Few-Step Action-Conditioned Video World Models

**Authors:** Xinye Li, Lingshuai Lin, Lei Wang, ..., Jiang Bian, Wai Lam
**arXiv:** [2608.14022](https://arxiv.org/abs/2608.14022)
**Categories:** Computer Vision and Pattern Recognition (cs.CV); Artificial Intelligence (cs.AI)

Action-conditioned video world models require low-latency causal generation and reliable responses to game-native controls. Although causal distillation enables one- or few-step video synthesis, extending it to interactive world models remains challenging, as discrete keyboard states and continuous mouse motion must remain aligned with temporally compressed latent chunks during causal training and autoregressive rollout. We introduce ForgeWM, a progressive framework that transforms a bidirectional action-conditioned video generator into efficient few-step world models through domain adaptation, teacher-forced causal training, causal consistency distillation, and on-policy distribution matching with a bidirectional teacher. The resulting budget-specialized students operate at steady-state denoising budgets of 1, 2, and 4 steps. ForgeWM further supports a dual-path deployment protocol combining latency-critical interaction with optional replay-time refinement, where the one-step student re-noises and refines its saved draft. On paired Minecraft trajectories, ForgeWM leads the evaluated systems in Imaging Quality, reference-aligned motion-profile agreement, action-sign accuracy, and mouse-control accuracy, while achieving the lowest reference LPIPS; the same four-stage recipe transfers to gamepad-controlled FPS gameplay. Replay-time refinement matches four-step reference quality while remaining roughly three times closer to the experienced trajectory than regeneration from noise. These results demonstrate ForgeWM's effectiveness for controllable few-step video generation.

---

## 5. hint$^2$: Hierarchical World Models for Inference-Time Temporal Logic Guidance

**Authors:** Moritz Zoellner, Anastasios Manganaris, Ahmed H. Qureshi, Rohan Paleja
**arXiv:** [2608.13678](https://arxiv.org/abs/2608.13678)
**Categories:** Robotics (cs.RO); Machine Learning (cs.LG)

A central goal of robot learning is to enable robots to execute rich instructions specified at runtime. Large-scale language-conditioned policies have made substantial progress toward this goal, yet still struggle with temporal structure and safety constraints. Linear Temporal Logic (LTL) provides a powerful language to express complex, non-Markovian instructions. However, guiding learned manipulation policies toward LTL satisfaction remains challenging because modern policies generate short-horizon action chunks and replan in closed loop, while almost all LTL specifications are evaluated over long-horizon trajectories. In this paper, we introduce hint$^2$, a method for guiding short-horizon policies toward satisfying complex LTL specifications at inference time using hierarchical world models. Our key idea is to derive two separate guidance objectives using each world model's abstraction level. A high-level model predicts future action-induced transitions in task-relevant atomic propositions to guide progress through the LTL automaton, while a low-level dynamics model predicts immediate state evolution for accurate local safety guidance. Our results show that hint$^2$ overcomes the limitations of current LTL-guided diffusion methods, outperforms existing inference-time steering methods in CALVIN, and successfully completes instructions with complex liveness and safety constraints more elegantly than language-conditioned alternatives. Finally, we demonstrate that hint$^2$ can handle complex instructions on a real UR5e manipulator.

---

## 6. BICPO-VLA: Behavior-Identified Continuation Preference Optimization for Smooth Asynchronous Vision-Language-Action Control

**Authors:** Ming Shang, Yuchen Huang, Jiaoyang Chen, ..., Xinzhou Wang, Fuchun Sun
**arXiv:** [2608.13924](https://arxiv.org/abs/2608.13924)
**Categories:** Robotics (cs.RO)

The request-to-handoff gap has three coupled sources: ambiguity about the behavior intended at request time, physical-state drift accumulated during action generation, and residual incompatibility when the new action finally assumes control. BICPO-VLA addresses them in sequence. First, an instruction-aware causal history encoder identifies the behavior supported by the command and current task progress. Second, sequential Haar subspace generation decomposes each action chunk into complementary pairwise scaffold and residual coefficients, enabling two specialized generation stages followed by exact reconstruction. By reducing iterative refinement in the original action space, it shortens the interval over which the robot continues moving before the new chunk becomes available. Finally, BICPO rolls the known outgoing actions to the actual handoff state and applies reference-relative Flow-DPO among behaviorally matched candidates, adapting the generated chunk to the remaining request-to-handoff mismatch without changing its intended behavior.

---

## 7. Ontology-Grounded World Models for Failure Diagnosis and Closed-Loop Repair in Physical AI Systems

**Authors:** Kailin Wang, Haoxiang Jie, Yaoyuan Yan, Jiacheng Zhou, Zhiyou Heng
**arXiv:** [2608.13901](https://arxiv.org/abs/2608.13901)
**Categories:** Robotics (cs.RO)

EV-WM represents candidate quality with feature and event scores, but these scores do not explicitly record an unmet task predicate, a route label for an available correction mechanism, or a post-correction acceptance result. We present Onto-EV-WM, an ontology-grounded diagnosis and verification-gated correction interface layered above EV-WM rather than a replacement world-model architecture. The implemented task-local TBox defines entity types, predicate signatures, and constraints; source-specific grounding maps predicted or simulator-observed states to task ABoxes; and deterministic rules retain each missing predicate and its arguments when assigning a route label. Learned or heuristic proposers remain separate from this symbolic interface; native task predicates determine acceptance, and the bounded protocol determines whether a failed verification is retried. In the aligned PointMaze evaluation, EV-WM and Onto-EV-WM both report 94% success, with mean final-state distances of 0.90573 and 0.61177, respectively; the separately budgeted search reaches 100% success. On LIBERO-Goal, the ontology represents failed task conditions as typed records, retains their predicate arguments, and associates them with the declared source/joint correction route and predicate-gated acceptance; the complete configuration reports 93.8% corrected-window success on seed 0 and 94.05 +- 0.30% across four evaluation-sampling seeds. On the fixed 10,030-task LIBERO-Plus registry, Onto-EV-WM succeeds on 8,526 tasks (85.00%), with suite-level success rates of 65.98% for LIBERO-10, 91.39% for LIBERO-Goal, and 91.38% for both LIBERO-Object and LIBERO-Spatial. These numbers report the performance of the complete ontology-grounded configurations under the tested simulator protocols; an ontology-only causal share is not measured separately, and real-robot recovery is not evaluated.

---

## 8. SSP: An Event-Matched Syn2Sim2Phy Cross-Domain Evaluation Framework for Autonomous Driving VLA Models

**Authors:** Haojie Feng, Peizhi Zhang, Xinrui Zhang, ..., Junfan Zhu, Lu Xiong
**arXiv:** [2608.14024](https://arxiv.org/abs/2608.14024)
**Categories:** Computer Vision and Pattern Recognition (cs.CV)

Vision-language-action (VLA) models for autonomous driving jointly produce scene interpretation, language-based reasoning, and driving trajectories. Existing evaluations often use independently selected synthetic, simulated, and physical data, so measured performance gaps can be confounded by changes in scenario content rather than genuine domain sensitivity. We propose SSP (Synthetic-Simulation-Physical), an event-matched Syn2Sim2Phy evaluation framework that anchors cross-domain comparison to the same safety-critical interaction. Starting from a synthetic long-tail video, SSP builds a validated event specification that preserves road topology, participant roles, relative motion, conflict evolution, passing order, response constraints, and event phases. Platform-specific realizations are then constructed in CARLA and on a closed proving ground and are evaluated only after transfer audits confirm preservation of mandatory event properties. SSP maps heterogeneous outputs from OpenEMMA, LLaViDA, and Alpamayo-R1 into common semantic slots and a 1 s trajectory window to assess output validity, semantic accuracy, critical-interaction recognition, trajectory quality, and risk response. Across Cut-in and vulnerable-road-user crossing cases, the macro-averaged Integrated VLA Capability Scores are 0.259, 0.291, and 0.325 in the Synthetic, Simulation, and Physical domains, respectively, while the best domain varies by scenario. Alpamayo-R1, OpenEMMA, and LLaViDA obtain scores of 0.405, 0.338, and 0.131. SSP provides a reproducible scene-transfer chain and an evidence-qualified evaluation of VLA behavior without assuming that the Physical domain is universally superior.

---
