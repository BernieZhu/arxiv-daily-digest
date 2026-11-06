# arXiv Daily Digest — 2026-11-05

**Mode:** direct
**Categories:** cs.AI, cs.LG, cs.RO, cs.CV
**Keywords:** VLA, RSI, agentic robot, self-improving robot, self-evolving robot, robot harness
**Papers found:** 8

---

## 1. EnzymeRSI: A dual-loop recursive self-improvement system for enzyme design

**Authors:** Genoria AI Team, Yuejie Hou, Lixiang Yang, ..., Yueyuxiao Yang, Meng Yang
**arXiv:** [2611.06321](https://arxiv.org/abs/2611.06321)
**Categories:** Artificial Intelligence (cs.AI)

Improvement in enzyme engineering is usually pursued by optimising which candidates to assay within a fixed model and workflow; when the bottleneck arises from a mismatched method or a failing workflow, that route is difficult to escape. We present EnzymeRSI, a dual-loop system for recursive self-improvement (RSI). The outer loop evolves harness assets without changing model weights, the inner loop develops prediction and selection algorithms under controlled conditions, and a cloud laboratory system is specified to close the physical loop with quality-controlled feedback. By updating its prediction strategy through iterative comparison, the outer loop raised the mean development-set Spearman correlation on ProteinGym by 0.044 across five assays, reaching 0.335 on CD19 and 0.683 on OPSD (rhodopsin); of the two first places, only CD19 was produced by the outer loop itself. In the self-improvement of the ThermoMPNN algorithm the inner loop reached a PCC of 0.849, and on TadA-Bench it reached a Spearman correlation of 0.307 in 1.13 h. In three prospective wet-lab tests of the system's experimental decision-making, 10 of the 32 candidates that had not been pre-specified for the luciferase RLuc showed at least twice the wild-type activity; a recommended variant of the cytidine deaminase A3A raised 5mC conversion to 90.2%; and path selection in evolution raised the catalytic efficiency of the DNA polymerase KOD-E on a modified substrate to 31.1 times that of the parent. By treating the organisation of the research workflow and the development of algorithms as a single falsifiable dry-to-wet loop, this work offers an evolutionary paradigm for moving beyond the blind spots of a fixed method and for autonomous enzyme engineering.

---

## 2. Reglos: A Self-Evolving Personal Memory Agent with Recursive Self-Improvement

**Authors:** Sen Yang, Jiaduo Lin, Zehong Huang, Wen Liu
**arXiv:** [2611.06049](https://arxiv.org/abs/2611.06049)
**Categories:** Artificial Intelligence (cs.AI)

Personal agents draw on past conversations to tailor their responses to each user. Their memory systems store and update what each user says, and coding agents now also rewrite the harness that turns this memory into the model's context. Such patches risk overfitting, because one tested only on the failures it targets can fix those cases and help nowhere else. We present Reglos, a training-free personal memory agent that tests whether harness changes help beyond the failures they were written to fix. Its self-evolving memory adds to each user's append-only record with every conversation, as new preferences supersede old ones and facts can be forgotten. Its harness improves through recursive self-improvement, in which a coding agent proposes patches from failure traces and a critic from a second model family screens each one for benchmark gaming. After the harness is frozen, a fixed evaluator decides which further patches to accept. With the same backbone behind every system, Reglos outperforms state-of-the-art memory systems such as Mem0, MemOS and EverOS, reaching 61.3% and 84.0% on PersonaMem-v2 and LongMemEval-S with Qwen3.8-27B, and 57.5% and 87.2% with GPT-5.6 Luna.

---

## 3. VABAR: A Variational Automation Benchmark for Agentic Robotics

**Authors:** Shuangyu Xie, Kaiyuan Chen, Uksang Yoo, ..., Spencer Huang, Ken Goldberg
**arXiv:** [2611.06881](https://arxiv.org/abs/2611.06881)
**Categories:** Robotics (cs.RO)

For robots to operate reliably in commercial and industrial applications, they must persistently perform specific tasks with known variations in object shape and pose. We call this Variational Automation (VA) to differentiate these settings from fixed automation. Inspired by recent papers on Agentic Robotics, where pretrained LLM and VLM coding agents combine interpretable robot programming with the open-world adaptability of model free policies, we propose a general set of agentic robotics benchmark design criteria that includes accessibility, repeatability, diversity, relevance to agentic robotics and practical applications, physical realizability, resistance to benchmark saturation, and computational efficiency. We instantiate these principles in six manipulation task classes spanning industrial, medical, and infrastructure applications: tool sorting, tool hanging, gear meshing, syringe packing, cable insertion, and cable routing. We introduce the Variational Automation Benchmark for Agentic Robotics (VABAR), an open, easily replicable, simulation-based manipulation benchmark to systematically evaluating agentic robotics systems. Built fully on open-source tools, VABAR features detailed implementations using the Newton physics engine, standardized task variations, difficulty tiers, success metrics, and a library of 33 generalizable skills with human-authored programmatic reference solutions. We provide initial baseline evaluations using an open agentic manipulation harness, Graph-as-Policy (GaP), and Isaac Lab Arena.

---

## 4. PyRUA-REAL: Robot Exploration and Adaptive Learning through RSI in the Real World

**Authors:** Qiang Wang, Jianxin Bi, Shulong Jiang, ..., Xuanyi Li, Daquan Zhou
**arXiv:** [2611.06768](https://arxiv.org/abs/2611.06768)
**Categories:** Robotics (cs.RO)

Coding agents powered by models such as GPT-6-Astra connect spatial reasoning with executable robot behavior, raising the question of how such agents can produce lasting improvements in robot capabilities from physical interaction. In this work, we study embodied recursive self-improvement (RSI) through real-world exploration, code refinement, and deployment using PyRUA-REAL, a framework in which coding agents retain interaction experience as persistent memory and reusable executable skills that inform subsequent exploration and improvement. Our empirical study places physical manipulation at the center of the improvement process, examining how agents collaborate, what kinds of execution feedback support effective code refinement, and how task specifications and previously acquired skills influence robustness and task transfer. We further investigate the efficiency and capability of the resulting programs when deployed without involving an online agent for decision-making. Across eight real-world tasks, PyRUA-REAL achieves an average success rate of 91.1%. In complementary evaluation on 42 tasks from the RoboDojo benchmark, it achieves an average success rate of 84.4%. This study provides empirical guidance for turning physical exploration into reusable robot skills that support continued improvement and robust, efficient deployment.

---

## 5. Where Is VLA Inference Time Spent? Bottlenecks and Optimization Interactions Across GPUs

**Authors:** Muhammad Danish Waseem, Ahmed Ali-Eldin Hassan
**arXiv:** [2611.06710](https://arxiv.org/abs/2611.06710)
**Categories:** Robotics (cs.RO)

Vision-language-action (VLA) models map camera observations and language instructions to robot actions. However, their large backbones and repeated action generation can make inference take longer than the robot's real-time requirements for its next action. To reduce the load of VLA computations, researchers have proposed multiple optimization approaches, including quantization and pruning. These optimizations can be combined with other general optimizations such as better kernel compilation or using CUDA graphs instead of the eager mode. However, most of these optimization results are usually reported on a single GPU type, typically for a few VLA models, with no analysis of what the real bottlenecks are for a model on a particular hardware or how these optimizations would generalize beyond the reported results. In this paper, we provide a comprehensive measurement study of seven families of inference optimization methods, from CUDA graphs and compilation to token pruning and quantization, on seven state-of-the-art VLAs evaluated on four GPU families ranging from a datacenter H100 to an embedded Jetson Thor. We analyse how CPU launch overhead, memory bandwidth, and kernel efficiency jointly shape optimization gains, and how applying one method changes the benefit of another. From this analysis, we derive VLA-Triage, guidelines for stacking optimizations under latency budgets. The guidelines identify which stages can provide the required savings and which combinations need testing in the deployed execution mode.

---

## 6. Compounding Physical RSI: Turning Execution Failure into Inherited Capability

**Authors:** Yixuan Yang, Qiang Chen, Run Shao, ..., Yichao Cao, Xiu Su
**arXiv:** [2611.06654](https://arxiv.org/abs/2611.06654)
**Categories:** Robotics (cs.RO)

Generalist robot policies are trained on static offline datasets, yet physical manipulation unfolds sequentially across stages. Because a weakness in a downstream stage remains unobservable until the policy passes earlier ones, each resolved bottleneck exposes the next hidden failure mode. This staged structure calls for Recursive Self-Improvement (RSI), in which a policy iteratively executes, diagnoses failures, and updates itself. Moreover, because task completion behaves like a product of stage-level pass rates, recursive gains can multiply across generations. In physical environments, three bottlenecks obstruct compounding: terminal execution feedback rarely localizes the stage that caused a failure, failed trajectories do not supply the corrective action, and updating shared parameters can degrade previously mastered skills.
We propose Compounding Physical RSI, a self-evolving policy framework that turns execution failures into heritable capability. First, automated capability-gap assessment traces failed rollouts to the task stage where progression breaks down and formulates a structured improvement objective. Second, conditioned on this objective, our remedy stage curates validated, stage-relevant experience and refines the policy via behavior-regularized offline reinforcement learning, without requiring costly online rollouts at each optimization step. Third, to safeguard existing skills, our retention stage constructs weight-space candidates between the inherited reference policy and the refined policy, evaluates them across the task suite, and promotes the best candidate as the reference state for the next generation.
Evaluated across all 42 tasks of the RoboDojo-Sim benchmark, CSU-AI-07 ranks first on the leaderboard with a three-seed mean Overall Score of 26.15 and Success Rate of 20.70%, outperforming the next-best entry by 5.92 points and 5.82 percentage points.

---

## 7. $A^3$-VLA: Automatic Perception-Guided Attention Alignment for Robot Manipulation

**Authors:** Shengzhe Zhang, Qi Zhang, Dazhong Shen, ..., Shaopeng Zhai, Hui Xiong
**arXiv:** [2611.06447](https://arxiv.org/abs/2611.06447)
**Categories:** Robotics (cs.RO)

Vision-Language-Action Models (VLAs) enable robots to perform manipulation tasks by leveraging Vision-Language Models (VLMs) to process visual observations and language instructions. However, the action prediction objective itself lacks fine-grained task-specific perceptual supervision, making it prone to relying on task-irrelevant visual shortcuts, leading attention away from target objects and key interaction areas, thereby limiting its operational performance and generalization ability. To address this, we propose Automatic Perception-Guided Attention Alignment for Robot Manipulation ($A^3$-VLA), a framework that derives task-specific visual guidance from the manipulation process itself. Specifically, $A^3$-VLA first generates heuristic candidate regions for target objects and the robot from interaction-induced visual changes, and refines them with a visual segmentation model offline. These regions serve as explicit perceptual guidance through two complementary objectives: an attention allocation loss that encourages sufficient focus on task-critical regions when language or robot state tokens query the visual input, and a contrastive learning loss that aligns the representations of candidate target regions with language instructions while separating them from task-irrelevant regions. Extensive experiments on simulated and real-world manipulation tasks demonstrate that $A^3$-VLA consistently improves multiple VLA backbones, with an average success rate gain of 6.5% - 25.2% across benchmarks.

---

## 8. From Pixels to Actions - Towards Native Vision-Language-Action Policies

**Authors:** Weichen Fan, Haiwen Diao, Penghao Wu, ..., Dahua Lin, Ziwei Liu
**arXiv:** [2611.06918](https://arxiv.org/abs/2611.06918)
**Categories:** Computer Vision and Pattern Recognition (cs.CV)

Vision-language-action models are typically built on a simple premise: perception is first compressed by visual encoders, and action reasoning begins only afterwards. Yet manipulation often hinges on precisely the visual signals most vulnerable to this abstraction, e.g., local geometry, boundaries, depth, and subtle state changes. This raises a fundamental question: should action policies inherit a fixed visual endpoint, or directly access evolving visual computation? We introduce NEO-VLA, a structurally encoder-free vision-language-action framework. Images are tokenized by lightweight patch convolutional layers and evolve jointly with language throughout the backbone, allowing a flow-matching action expert to draw from instruction-conditioned visual representations at different depths. This simple change reveals a consistent pattern. Native architectures outperform encoder-based counterparts under controlled comparisons; full fine-tuning reduces but does not erase the gap, and additional scale alone cannot recover it. More strikingly, layer-wise probing shows that the action-critical signals often peak well before the final visual representation. Across diverse manipulation settings and distribution shifts, NEO-VLA consequently achieves stronger and more robust control. Together, these results suggest that embodied control benefits from access to visual representations across the computational hierarchy, rather than a fixed encoder output.

---
