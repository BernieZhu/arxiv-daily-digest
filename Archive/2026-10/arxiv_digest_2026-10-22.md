# arXiv Daily Digest — 2026-10-22

**Mode:** direct
**Categories:** cs.AI, cs.LG, cs.RO, cs.CV
**Keywords:** VLA, RSI, agentic robot, self-improving robot, self-evolving robot, robot harness
**Papers found:** 8

---

## 1. From Association to Decision Value: Testing Paired Instruction Dependence for VLA Corpus Selection

**Authors:** Nurmukhambet Serikbayev, Abdul Basit, Muhammad Shafique
**arXiv:** [2610.29646](https://arxiv.org/abs/2610.29646)
**Categories:** Artificial Intelligence (cs.AI)

Choosing among robot demonstration corpora is a ranking problem: an upstream diagnostic must preserve which candidates produce better downstream policies, not merely correlate with average performance. We study paired instruction dependence, the rate at which a demonstrator changes its first decision when only the goal changes. Across 136 independently seeded quadruped-navigation corpora, predictions developed on 56 corpora are evaluated prospectively on 80 held-out corpora. The audit is reliable and associated with downstream paired correctness, and lowers mean absolute prediction error when added to a correctness-aware baseline, but the primary proper-log-score increment is +0.059 nats (95% corpus-bootstrap CI [-0.027, 0.133]) and the prespecified top-20% comparison does not establish an incremental selection gain. An exploratory response decomposition suggests a structural source of this predictive-ranking mismatch: under the tested predictor specification, separating both-correct and both-wrong responses yields larger held-out gains than their unsigned switch statistic. Seed-to-seed agreement indicates that the held-out endpoint retains recoverable rank signal. These results show that counterfactual response structure can be reliable and predictive while providing limited incremental decision value in this setting when compressed into an unsigned statistic, motivating diagnostics that preserve outcome-relevant structure and are validated against the decisions they are intended to support.

---

## 2. Recursive Self-Improvement on a Budget: Scoring Code Edits Before They Run

**Authors:** Erfan Darzi, Sree Bhargavi Balija, Sheng He
**arXiv:** [2610.29121](https://arxiv.org/abs/2610.29121)
**Categories:** Artificial Intelligence (cs.AI); Machine Learning (cs.LG)

A coding agent that rewrites its own scaffold has to choose which proposed edit to expand before that edit has been evaluated, and the search then has to return one agent. Each run fits one linear readout on the parent's steering-split solve rate and eight coordinates of the proposed diff, from 96 scaffold edits labeled by four evaluations of a 16-instance fit split, and then freezes the coefficients. HumanEval+ reserves 48 instances as the steering split and Polyglot reserves 64. That split scores parents and keeps an archive of four nodes. Huxley-Gödel Machine selection draws a parent by Thompson sampling on the steering counts of nodes that have already been evaluated, and it expands the child that parent proposes. Every method then returns the earliest evaluated node whose steering-split solve count is maximal. The tables report the held-out score of that node on the other 100 HumanEval+ instances and the other 145 Polyglot instances, next to the root scaffold and the calibration edit with the highest fit-split label. Twelve runs of GPT-4o return a node at 87.0% on held-out HumanEval+, against 84.2% for the parent-rate ablation. On that split Huxley-Gödel Machine selection returns 85.1%, the root is at 81.2%, and the calibration-best edit is at 82.8%. On the same split Claude Sonnet 4.5 returns 86.6%, beside 86.5% for Huxley-Gödel Machine selection, 85.3% for the parent-rate ablation, and 85.1% for the calibration-best edit.

---

## 3. Toward Recursive Self-Improvement in Physical AI

**Authors:** Meng Luo, Zechen Bai, Shanqing Xu, ..., Wei Chen, Hongzhan Lin
**arXiv:** [2610.29677](https://arxiv.org/abs/2610.29677)
**Categories:** Robotics (cs.RO); Artificial Intelligence (cs.AI)

Recursive self-improvement (RSI) describes a system that improves not only its behavior but also the process by which it improves. Recent digital agents test this idea by rewriting their own code and checking each version with executable tests. Bringing these mechanisms into the physical world requires learning from partial observations through costly trials, while accounting for changing operating conditions and potentially irreversible consequences. We position RSI within robot learning and trace pathways from improving robot capabilities to improving the processes that generate them. We examine how physical experience can strengthen these improvement mechanisms and when the resulting gains can support further self-improvement of the mechanisms themselves. Gains carry forward only when feedback addresses remaining learning needs, the receiving component can use the change, its value survives changes in tasks or hardware, and continued practice remains safe and affordable. Existing studies, concentrated in manipulation, support behavioral improvement, benefits to later learning, and procedure improvement. Some systems also change the improver's knowledge or tools, but the physical studies reviewed here have yet to isolate gains attributable to recursion. We synthesize these findings into evaluation principles and research directions for machines that, trial by trial, safely improve the way they improve.

---

## 4. Post-hoc Epistemic Uncertainty for Vision-Language-Action Policies

**Authors:** Johannes Keller, Albrecht M. Bloße, Adrian Lindenmeyer, Thomas Neumuth, Daniel Schneider
**arXiv:** [2610.29730](https://arxiv.org/abs/2610.29730)
**Categories:** Robotics (cs.RO); Machine Learning (cs.LG); Machine Learning (stat.ML)

Vision-language-action (VLA) policies need to recognize gaps in their training knowledge to request useful demonstrations or assistance in new situations, especially when failures are costly. Disagreement within an ensemble of independently trained policies can guide these decisions, but requires training and running multiple policies. We propose post-hoc kernel-variance heads that estimate epistemic uncertainty from the embeddings of a single policy. Each head computes the conditional variance of a Gaussian process conditioned on embeddings from the training demonstrations. Fitting requires no regression targets or gradient updates and leaves the policy unchanged. In experiments with SmolVLA on LIBERO-10, the kernel variance heads perform competitively with two-policy ensemble scores in task-level correlation with task success, in demonstration acquisition during active learning, and in referral to a stronger supervisor policy as a proxy for human assistance. For SmolVLA, the head on the vision-language backbone reduces uncertainty-scoring time by up to approximately a factor of 50 compared with ensemble scores, while also substantially reducing setup costs. We also show that the established evaluation protocol on LIBERO-10 primarily rewards recognition of coverage differences between tasks, while execution variability weakens assessment of within-task rankings. Thus, controlled perturbations provide a complementary evaluation: modality-specific heads identify unfamiliar camera, instruction, or state inputs, while fused heads can detect unfamiliar combinations of individually familiar inputs. With a supervisor proxy trained on the evaluated perturbation families, the decoder head improves within-task referral over ensemble disagreement. These findings show that useful uncertainty estimates for adaptive robot learning can be obtained from a single policy.

---

## 5. FlowVLA: Learning Flow-Aware Physical Completion for Quantitative Robotic Pouring

**Authors:** Liwen Yang, Yutian Zhang, Jiaqi Zhai, ..., Qiaojun Yu, Dibo Hou
**arXiv:** [2610.29692](https://arxiv.org/abs/2610.29692)
**Categories:** Robotics (cs.RO)

During steady pouring, images and robot pose may remain nearly unchanged while transferred mass accumulates, making the return decision ambiguous for a whole-task vision-language-action (VLA) policy. We present FlowVLA, which separates motor generation from physical-completion estimation. A shared $\pi_{0.5}$ action expert learns approach, pour, and return with boundary-aware supervision. A target-independent estimator fuses visual, joint, wrist-wrench, and recurrent force-belief histories to maintain an estimate of transferred mass. The controller initiates return when this estimate plus predicted residual outflow reaches the requested mass. In coffee-pot/water experiments, FlowVLA achieves 13.1 g goal-balanced mean absolute error (MacroMAE), lower than all tested VLA baselines. Across all attempts, 53.7% both complete the task and finish within +/-10% of the requested mass. The same model interpolates to held-out 150/250-g targets without retraining. Independently trained models further evaluate the formulation in three additional container-fluid settings.

---

## 6. NavBind: Diagnosing Instruction-Action Binding at Route Forks in Navigation VLAs

**Authors:** Josh Qixuan Sun, Xiaoying Xing, Yurun Chen, ..., Wentao Zhu, Mark Crowley
**arXiv:** [2610.29203](https://arxiv.org/abs/2610.29203)
**Categories:** Robotics (cs.RO)

Vision-language-action (VLA) navigation models translate visual observations and instructions into actions. Navigation success assesses whether an agent reaches the goal. However, reaching the goal successfully does not establish whether the model genuinely follows the instructions or relies on visual cues or navigation history. We introduce NavBind to diagnose instruction-action binding: whether changing the instruction influences the probabilistic distribution of the actions, with the navigation context fixed. We construct 3,252 route-fork contexts by recombining route-aligned instruction segments from R2R-CE and RxR-CE. Each context pairs full instructions that share the description of the route already traveled but specify different branches. Both are evaluated under the same agent state and navigation history. We compare generated local action sequences, the likelihoods of fixed reference action sequences under both instructions, and changes in visual attention and attribution. Across the evaluated models, higher reported navigation success does not imply that the model more faithfully follows the instructions.

---

## 7. SimPT: An Automated Simulation Framework for Intervention-Based VLA Post-Training

**Authors:** Caicheng Wang, Zipeng Ye, Zhexuan Zhou, ..., Xi Zhang, Yuchen Xie
**arXiv:** [2610.29161](https://arxiv.org/abs/2610.29161)
**Categories:** Robotics (cs.RO)

Human-in-the-loop (HIL) post-training improves vision-language-action (VLA) policies through expert corrections, but costly human supervision and repeated real-robot evaluation limit algorithm exploration and development. We introduce SimPT (Simulation-based Post-Training), a simulation framework that automates intervention-based VLA post-training by integrating policy rollouts, corrective data collection, policy training, and standalone evaluation. To automatically determine intervention timing and recovery strategies, we develop an Agent-Compiled Progress Graph that tracks task progress using privileged simulator state and retains stable snapshots during policy execution. After a rollout fails, a CuRobo-based expert attempts recovery from these snapshots, starting at more advanced task stages and falling back to earlier ones as needed to generate corrective trajectories. We implement and compare four post-training methods, RECAP, HG-DAgger, DPO+SFT, and FlowPRO, across seven RoboTwin manipulation tasks. Relative to a fixed-interval snapshot baseline, the Progress Graph reduces recovery attempts by 75.0% and increases recovery success from 93.4% to 98.9%. Using SimPT, we develop RECAP-CF-LPF, a refinement of RECAP that combines cross-fitting and low-pass filtering of value predictions. This refinement increases the overall success rate from 76.50% to 79.36% in held-out simulation trials. In real-robot HIL post-training, it increases the success rate from 72% to 96% across 25 scenarios of an Ethernet cable-insertion task. These results demonstrate the utility of SimPT for exploring and developing VLA post-training algorithms.

---

## 8. GeoMem-VLA: Internalizing 3D Scene Understanding into Temporal Memory for Vision-Language-Action Models

**Authors:** Qinfan Zhang, Yifan Luo, Haoyuan Shi, ..., Xiangcong Ren, Xiaozhu Ju
**arXiv:** [2610.29866](https://arxiv.org/abs/2610.29866)
**Categories:** Computer Vision and Pattern Recognition (cs.CV)

Geometric structure is essential for robotic manipulation and understanding the 3D world. Most VLA models rely on 2D representations of current observations, while geometry-aware approaches often require additional 3D information. However, geometry inferred independently from individual observations is often discarded rather than accumulated into a persistent task representation. Our key insight is that action generation needs a compact, task-relevant geometric abstraction that can be continuously updated, rather than a complete, renderable 3D reconstruction at every step. We introduce GeoMem-VLA, a VLA framework that internalizes explicit 3D supervision into dedicated geometric tokens and maintains them as temporal memory for action generation, without directly aligning the VLM's native visual embeddings with the teacher feature space. During training, a frozen geometry foundation model supervises learnable GeoPlan tokens through a geometric flow-matching objective over the current scene point map and future end-effector tracks. These tokens are integrated with the memory of observation representations, where historical information is retrieved, adaptively fused with current observations, and consolidated to retain event frames as the task progresses. At inference, the policy retrieves historical representations and fuses them with the current working representation to predict actions, without invoking the 3D teacher or explicitly reconstructing the scene. After benchmark-specific downstream adaptation, GeoMem-VLA achieves 98.9% average success on LIBERO and 91.10% / 91.24% on RoboTwin's clean/randomized settings. Across five real-world tasks, GeoMem-VLA achieves 78.0% average success. These results suggest that internalizing and remembering 3D scene understanding is a promising approach to robot control.

---
