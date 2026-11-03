# arXiv Daily Digest — 2026-11-02

**Mode:** direct
**Categories:** cs.AI, cs.LG, cs.RO, cs.CV
**Keywords:** VLA, RSI, agentic robot, self-improving robot, self-evolving robot, robot harness
**Papers found:** 4

---

## 1. VLA Policies Do Not Know When Not to Act: Unintended Task Execution and Start Suppression

**Authors:** Minsu Jang, Jae-Woo Choi, Youngwoo Yoon, Dohyung Kim
**arXiv:** [2610.41609](https://arxiv.org/abs/2610.41609)
**Categories:** Robotics (cs.RO); Artificial Intelligence (cs.AI)

A robot should act only on an instruction from a person or on an intent that the robot explicitly represents and generates. Unintended actions taken without such an instruction can cause risk or inconvenience to people and the environment. We examine how recent vision-language-action (VLA) policies respond when the instruction is missing or meaningless. We apply a paired protocol with empty, neutral, nonsense, infeasible, and wrong-task instructions to six model checkpoints in LIBERO-Goal simulation. Holding the initial state fixed and varying only the instruction, we ask three questions: whether the robot starts to move, which task it completes, and what the instruction determines. Even when the instruction was empty, the robot started moving in every episode with all six checkpoints, and with five of them it often completed a task that the instruction had not specified. On two GR00T checkpoints, the instruction determined which task was executed but not whether the robot started moving; the robot moved even on infeasible instructions. We then tested three methods for suppressing the start: prepending "if no task is given do not move" to the instruction; a gate that holds the robot when the first action chunk for the given instruction nearly equals that for an empty instruction; and fine-tuning the policy to hold still on non-task inputs. The prefix stopped the robot in none of the six checkpoints, and the gate held it on non-task inputs in five of the six checkpoints. The fine-tuned policy never completed a task on non-task inputs, but it did not reliably keep the robot still, and it failed to suppress the start on infeasible instructions.

---

## 2. SACQ: Structure-Aware Codebook Quantization for Ultra-Low-Bit Vision-Language-Action Models

**Authors:** Haesung Lee, Insu Han
**arXiv:** [2610.41408](https://arxiv.org/abs/2610.41408)
**Categories:** Computer Vision and Pattern Recognition (cs.CV); Machine Learning (cs.LG); Robotics (cs.RO)

Vision-Language-Action (VLA) models enable capable robot behavior, but their large memory footprint limits deployment on resource-constrained robotic platforms. Weight quantization is a natural remedy, yet post-training quantization (PTQ) recipes inherited from large language models degrade when applied to VLAs at ultra-low precision. Existing low-bit PTQ methods often fail to explicitly account for the structure of downstream operations and allocate precision without considering its effect on the policy actions. We introduce SACQ, an ultra- low-bit weight-only vector-codebook quantization framework for VLAs. SACQ combines (1) structure-aware codebook fitting with role-specific quadratic metrics that reflect input statistics and downstream sensitivity; (2) action-aware mixed-bit allocation based on the increase in final-action error as individual layers are compressed; and (3) two-stage post-quantization refinement that reassigns codeword indices with second-order error compensation and calibrates codebooks and row-group scales against the decoded action. Using GR00T N1.7, SACQ achieves 93.85% average success across four LIBERO suites at 1.5 bits per language/action weight while reducing model memory by 4.83x. With INT8 activation quantization and low-precision attention, it retains 93.55% success while running 1.51x faster than BF16. On SimplER, SACQ further achieves 63.76% and 52.27% success under Visual Matching and Variant Aggregation at 2 bits per language/action weight, compared to 58.90% and 53.45% for BF16, respectively.

---

## 3. Nexus-VLA: Bridging Human and Robot Experiences via a Shared Hierarchical Semantic Latent Space

**Authors:** Biaoliang Guan, Tingyu Yuan, Wen Ye, ..., Jihua Zhu, Chaoyang Zhao
**arXiv:** [2610.42021](https://arxiv.org/abs/2610.42021)
**Categories:** Robotics (cs.RO)

Large-scale egocentric human videos provide rich and scalable manipulation experience for robot policy learning, yet substantial embodiment gaps in visual appearance, kinematic structure, and action spaces hinder effective knowledge transfer. Existing methods often decouple cross-embodiment knowledge alignment from robot policy learning, making it difficult for human manipulation knowledge to directly and fully contribute to robot action learning. To address this issue, we propose Nexus-VLA, a hybrid policy learning framework that enables cross-embodiment knowledge transfer through end-to-end human-robot joint training, allowing human manipulation experience to directly contribute to robot policy learning. We first introduce a hierarchical cross-embodiment semantic alignment paradigm that progressively establishes shared manipulation semantics from task intent to fine-grained interactions, enabling more complete use of the manipulation knowledge contained in human videos. Building on this hierarchy, we design a shared manipulation latent representation that jointly encodes multi-level shared knowledge into an internal representation directly used for continuous action generation, improving policy learning efficiency while effectively leveraging human knowledge. Across RoboCasa-GR1, OOD settings, and real-world robot experiments, Nexus-VLA achieves an 80.5% task success rate on RoboCasa-GR1 and demonstrates strong advantages in human-data utilization, learning efficiency, and cross-scenario generalization.

---

## 4. META-Robot: Self-Cognition and Capability Scaling in Agentic Robots

**Authors:** Xuanzhi Feng, Zeyu Liu, Weiheng Gao, ..., Jie Zhang, Song Guo
**arXiv:** [2610.41868](https://arxiv.org/abs/2610.41868)
**Categories:** Robotics (cs.RO)

LLM-based robotic agent systems can generate programs for robot control, yet their generalization to new tasks often depends on elaborate scaffolding. Expanding their skill repertoires alone offers limited guidance on how to assess new capabilities or identify what remains beyond their reach. We introduce META-Robot, a framework that couples self cognition with capability scaling by expanding the criteria through which an agent evaluates and develops its skills. At its core, action-level predicates make execution outcomes explicit and available for LLM reasoning. The agent uses these assessments to identify its own limitations, extend relevant evaluation criteria, and guide the structured expansion of its skills. Proprioceptive feedback further grounds this process in the robot's physical state, enriching the evidence available for self-cognition. Experiments in simulation and on real robots demonstrate stronger overall task performance, generalization to new tasks, continued expansion of skills and evaluation criteria, and effective use of non-visual proprioceptive signals.

---
