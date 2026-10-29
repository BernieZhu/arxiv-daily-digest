# arXiv Daily Digest — 2026-10-28

**Mode:** direct
**Categories:** cs.AI, cs.LG, cs.RO, cs.CV
**Keywords:** VLA, RSI, agentic robot, self-improving robot, self-evolving robot, robot harness
**Papers found:** 8

---

## 1. The Trinity:Capability-Driven Recursive Self-Improvement for Multimodal Agents

**Authors:** Weidong Tang, Ruiheng Wang, Jingxuan Zhang, ..., Odin Zhang, Yang You
**arXiv:** [2610.36077](https://arxiv.org/abs/2610.36077)
**Categories:** Artificial Intelligence (cs.AI); Computer Vision and Pattern Recognition (cs.CV)

Multimodal intelligence can be viewed as human-guided co-evolution between worlds and agents through interaction. However, scaling this process faces two bottlenecks: constructing heterogeneous, verifiable environments is costly, and manual Harness iteration cannot keep pace with growing task diversity and complexity. A key insight is that tasks with different modalities and surface forms can share the same underlying capability requirements. We therefore introduce The Trinity, a recursive self-improvement framework coupling world generation with Harness evolution through three roles: Creator, Explorer, and Evolver. Drawing on verified execution trajectories, Evolver shifts the basis of task organization from surface categories to shared requirements, reorganizing the original task tree into a hierarchical capability tree. We introduce Capability-Driven Real2Sim2Real: for heterogeneous tasks at the same node, Creator abstracts their common requirements into simplified, verifiable simulated worlds for capability learning, while evaluation on original tasks measures transfer. Along this capability tree, Explorer progressively evolves reusable capability modules through selective inheritance, forming a Harness tree whose validated updates accumulate across iterations within a fixed topology. The resulting Harnesses specialize in different capabilities, motivating a Capability-Aware Harness Router that uses public task information to select compatible module configurations from the tree. Our evolved Harnesses improve mean performance by 34 points across 28 training benchmarks and 26 points across 18 unseen benchmarks, including two real-world embodied tasks.

---

## 2. Retrieve to Act: Motion Primitive Graph Retrieval for Robust VLA Execution

**Authors:** Pham Tri Quang, Bao-Ngoc Dao, Minh Duc Nguyen, ..., Duy M. H. Nguyen, Vien Anh Ngo
**arXiv:** [2610.37215](https://arxiv.org/abs/2610.37215)
**Categories:** Robotics (cs.RO); Artificial Intelligence (cs.AI)

Vision-Language-Action (VLA) policies demonstrate remarkable semantic generalization, yet remain highly vulnerable to out-of-distribution (OOD) visual shifts during execution. While existing test-time methods attempt to suppress spurious visual cues, they fundamentally overlook the rich, uncorrupted kinematic priors embedded in the policy's own training experience. We introduce Retrieve to Act (R2A), a test-time scaling framework that formulates OOD robustness purely as a geometric motion primitive retrieval problem. R2A bypasses fragile visual features by structuring successful training demonstrations into an offline spatiotemporal motion primitive graph. During inference, a query-dependent Graph Neural Network dynamically localizes the robot's ongoing execution within this graph, retrieving structurally compatible future motion primitives. These retrieved geometric priors are then seamlessly harmonized with the frozen VLA's predicted actions via a learned, dimension-wise gating mechanism, adaptively rectifying erroneous spatial trajectories while preserving the policy's local reactivity. Extensive experiments across three state-of-the-art VLA architectures, GR00T N1.7, $\pi_{0.5}$, and StableVLA, demonstrate that R2A consistently and significantly enhances robustness against diverse contextual perturbations. R2A achieves absolute success rate improvements of up to +12% in simulation benchmarks (LIBERO-Plus, RoboTwin2.0-Plus) and +40% in real-world deployments, without requiring any finetuning of the base policies. Project page: this https URL

---

## 3. PDRVLA: A Vision-Language-Action Model with Physical Dynamics Representations

**Authors:** Hanqing Wang, Zhaotian Cai, Ruichuan An, ..., Zenan Zhou, Youzheng Wu
**arXiv:** [2610.37381](https://arxiv.org/abs/2610.37381)
**Categories:** Robotics (cs.RO); Computer Vision and Pattern Recognition (cs.CV); Machine Learning (cs.LG)

Vision--Language--Action (VLA) models generate robot actions from visual observations and language instructions, but their understanding of physical dynamics remains limited. Video world models can capture scene dynamics, yet generating future videos introduces high latency into the control loop. We introduce PDRVLA, whose lightweight Physical Dynamics Module extracts physical tokens from vision--language features to condition action generation without online video generation. The module learns through direct prediction of future RGB, depth, and optical-flow features, with auxiliary supervision through a frozen pretrained video world model. Training relies entirely on publicly available data, expanded through human-to-robot synthesis, subtask annotation, and embodied chain-of-thought (ECoT) annotation. Across four simulation benchmarks, PDRVLA achieves success rates of 99.3% on LIBERO, 89.9% on LIBERO-Plus, 93.6% on RoboTwin~2.0, and 81.5% on SimplerEnv. Ablations show improved future prediction with world-model supervision and evaluate how subtask conditioning, future object-pose supervision, and ECoT training affect action success.

---

## 4. VLA-Stem: A Lightweight Safety Mechanism for Vision-Language-Action Models via Reinforcement Learning

**Authors:** Bojun Zou, Wenhao Yu, Jiaohao Li, ..., Yanyong Zhang, Jianmin Ji
**arXiv:** [2610.37378](https://arxiv.org/abs/2610.37378)
**Categories:** Robotics (cs.RO)

Vision-Language-Action (VLA) models integrate high-level reasoning with low-level action execution for end-to-end robotic control. However, most VLA models target static manipulation in unconstrained environments, overlooking spatial constraints and dynamic obstacles. Fine-tuning VLAs on obstacle-avoidance data is a straightforward solution, but collecting such data is costly, especially for dynamic scenarios, and may degrade their original task capabilities. To address these limitations, we propose VLA-Stem, a lightweight, reinforcement-learning-based safety mechanism for VLA systems. Without fine-tuning the underlying VLA policy, VLA-Stem converts its action chunks into motion references and uses trajectory-level guidance to preserve their spatial intent while allowing flexible motion and timing adjustments. Conditioned on these references, robot proprioception, and local obstacle information, the Stem policy adaptively modifies execution at inference time, preserving the original task intent while enabling responsive adaptation to spatial constraints and dynamic obstacles. For robust and sample-efficient training, we combine teacher-student distillation with curriculum learning. We evaluate VLA-Stem on reference following, static spatial constraints, and dynamic obstacle avoidance. Across six constrained simulation settings, VLA-Stem achieves 52.8% average collision-free task success versus 23.7% for the strongest safety baseline, while preserving base-policy performance in obstacle-free settings; real-world experiments further show consistent collision reductions under static and dynamic obstacles. These results demonstrate that VLA-Stem couples high-level VLA task intent with rapid, reflex-like responses to immediate physical risks, providing a brainstem-inspired mechanism for robust robot execution.

---

## 5. From 12 to 200 Demonstrations: How ACT, Diffusion Policy, SmolVLA and $π_{0.5}$ Scale on a Low-Cost Arm

**Authors:** Simon Cowling
**arXiv:** [2610.37170](https://arxiv.org/abs/2610.37170)
**Categories:** Robotics (cs.RO)

We trained four widely used imitation-learning policies, ACT, Diffusion Policy, SmolVLA and $\pi_{0.5}$, on nested subsets of 12, 25, 50, 100 and 200 teleoperated demonstrations of one pick-and-place task with distractor objects, using one fixed training recipe per policy. Every trained model was then run on a physical SO-101 arm on a fixed set of object placements: 1,340 scored episodes in 126 blocks.
ACT, trained from scratch, rose from 1 success in 40 episodes at 12 demonstrations to 37 in 40 at 100. $\pi_{0.5}$ with its action expert fine-tuned was the best policy when data was scarce (16 of 40 at 12 demonstrations, 28 of 40 at 25) and then stayed near 70%; from 100 demonstrations ACT was ahead, by a margin this study does not fully resolve. SmolVLA and Diffusion Policy peaked near 50%, and both were affected by a failure to start: SmolVLA's arm never started moving in 47% of episodes, and Diffusion Policy hardly ever started until an idle lead-in was trimmed from the demonstrations. For $\pi_{0.5}$ the fine-tuning recipe mattered more than the amount of data: low-rank adaptation succeeded in 4 of 110 episodes, against 130 of 200 for action-expert fine-tuning.
From the joint and camera recordings we place every episode on a four-stage ladder (started, reached the ball, carried it, delivered it) and show that for ACT more data moves failures from reaching, to grasping, to none, while the failures $\pi_{0.5}$ retains are in grasping. We also measure how weak a ten-episode block is as a measurement (the same checkpoint tested twice differs by 2 successes in 10 on average), separate seed-to-seed variation from that noise, and audit the human scoring against the recordings. Training length was fixed within each recipe, so the amount of data and the number of times it was seen change together; we state which conclusions survive that confound and which do not.

---

## 6. ASPEN: Adaptive Semantic Reasoning via Command Persistence Prediction for Efficient Navigation VLAs

**Authors:** Vieri N. Akustia, Bin Hu
**arXiv:** [2610.36285](https://arxiv.org/abs/2610.36285)
**Categories:** Robotics (cs.RO)

Navigation vision-language-action (VLA) policies repeatedly invoke costly semantic reasoning even when the next command remains unchanged. Command reuse can reduce computation but risks missing instruction-dependent turns or stops. We introduce ASPEN, an event-triggered scheduler based on command persistence prediction: estimating whether the frozen base policy would reissue its previous command. A lightweight multimodal predictor combines temporal observations, language instructions, execution history, and cached VLA confidence. At eligible command boundaries, sufficient predicted persistence permits command reuse. Otherwise, ASPEN triggers fresh semantic reasoning from the VLA. Evaluated with frozen NaVILA on cross-dataset RxR-CE val-unseen, ASPEN reduces VLA calls by 9.5% and estimated inference time by 8.1%, including scheduling overhead. It maintains comparable navigation performance and preserves identical baseline action sequences on 92.1% of episodes.

---

## 7. Vision-Language-Action or World-Action? Just Action Models

**Authors:** Yonghao Yu, Lang Huang, Runyi Li, Toshihiko Yamasaki
**arXiv:** [2610.37219](https://arxiv.org/abs/2610.37219)
**Categories:** Computer Vision and Pattern Recognition (cs.CV); Robotics (cs.RO)

The vision-language-action (VLA) and world-action model (WAM) communities debate whether control policies should inherit pretrained knowledge from vision-language models or from visual generators. The debate, however, bundles three separable choices: backbone initialization, the objective applied to future observations, and whether the machinery for that future loss is kept at inference. A gap between a VLA and a WAM therefore cannot simply be attributed to any one of them. We show that decoupling these choices yields a common framework for both families, which we term Just Action Model (JAM): a pretrained visual backbone with an action expert, trained with an action loss and a foresight loss. The foresight loss trains current-observation features to predict frozen encodings of the recorded future through a prediction head discarded after training, so no visual generation is involved in either training or inference, and the backbone can be chosen freely. We first compare objectives within fixed policy architectures, then evaluate the foresight recipe across backbone families. The resulting JAM policies outperform their matched FastWAM and ImageWAM counterparts on LIBERO and LIBERO-Plus, and achieve similar or slightly higher success rates on RoboTwin. Compared with FastWAM, JAM improves the success rates from 97.0%/55.3%/91.2% to 98.2%/64.5%/91.4%, respectively. With cached foresight targets, JAM reduces estimated online training FLOPs per sample per update by 73% relative to FastWAM. Our results show that future supervision improves control without visual generation or additional inference machinery, and strong foresight performance is attainable with either generator-initialized or vision-language backbones. Project Page: this https URL

---

## 8. Evaluation-Guided Demonstration Refinement for Vision-Language-Action Policies: The Winning Entry in the MetaFine Open Competition

**Authors:** Lifan Zheng, Guotao Chen, Zhenyang Li, ..., Qiang Huang, Fan Liu
**arXiv:** [2610.36765](https://arxiv.org/abs/2610.36765)
**Categories:** Computer Vision and Pattern Recognition (cs.CV)

We fine-tuned a separate $\pi_{0.5}$ policy for each of the five tasks in the MetaFine Open Competition, with a task-specific training mixture and number of actions executed per prediction. Training started from the official demonstrations and expert procedures. Local evaluation exposed recurring grasping, pushing, and insertion failures. We addressed them by revising the demonstrated motions and by adding expert continuations from states the policy reached, while keeping nominal demonstrations in training. Checkpoints were compared on every instruction, so that a gain on one instruction could not hide a loss on another. Our submission, MAI, ranked first overall with a score of 96.66.

---
