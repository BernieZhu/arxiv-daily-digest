# arXiv Daily Digest — 2026-11-11

**Mode:** direct
**Categories:** cs.AI, cs.LG, cs.RO, cs.CV
**Keywords:** VLA, RSI, agentic robot, self-improving robot, self-evolving robot, robot harness
**Papers found:** 6

---

## 1. APS-VLA: Action-Guided and Future-Aware Token Pruning for Efficient Vision-Language-Action Models

**Authors:** Xiaoyang Xing, Chun-Mei Feng, Anthony Cohn, Xiaoliang Gong, Asoke Nandi
**arXiv:** [2611.13030](https://arxiv.org/abs/2611.13030)
**Categories:** Artificial Intelligence (cs.AI)

Vision-language-action (VLA) policies have demonstrated strong generalization in robotic manipulation, yet processing dense visual tokens often incurs high inference latency. Visual token pruning offers a practical way to reduce this cost, but identifying a compact set of tokens that preserves reliable action generation remains challenging. Existing methods largely rely on static or immediate heuristic cues to estimate token importance. We introduce APS-VLA, a framework that learns visual token selection from robot demonstrations while keeping the pretrained VLA backbone frozen. A lightweight Decision Influence Estimator scores tokens conditioned on current visual observations, language instructions, and robot proprioception. Its training combines two complementary signals: action supervision matches both the full-input policy predictions and demonstrated actions, while an auxiliary visual transition objective uses demonstrated actions to predict subsequent visual features from the selected representation. At deployment, the estimator performs a single hard selection and packing step before the policy's native action-generation procedure; the auxiliary predictor is removed. Experiments with OpenVLA-OFT on LIBERO and with $\pi_{0.5}$ and XR-1 on RoboCasa365 demonstrate inference acceleration with modest changes in task success. Across five real-world tasks on two dual-arm platforms, APS-VLA reduces mean policy inference latency from 137.25 to 93.25 ms, achieving a $1.47\times$ speedup with an average success rate of 61%, compared with 60% for the unpruned baseline. Together, these results support APS-VLA as a modular, plug-in framework for efficient robotic control across VLA architectures, preserving the underlying policy parameters and native action-generation procedure.

---

## 2. How Much of Your VLA Is kNN

**Authors:** Denis Grachev, Damien LaRocque, Omar Moured
**arXiv:** [2611.13160](https://arxiv.org/abs/2611.13160)
**Categories:** Robotics (cs.RO); Artificial Intelligence (cs.AI); Machine Learning (cs.LG)

Vision-language-action (VLA) models now exceed 95% success on the LIBERO simulation benchmark, yet it remains unclear how much of this performance requires generalization beyond the training demonstrations. In this work, we show that retrieving nearby demonstrations and reusing their action chunks achieves a success rate of 91.7 % on LIBERO without policy training. Under LIBERO-Plus perturbations, retrieval shows the smallest drop of all evaluated policies. Across nine publicly available VLAs, fine-tuning mostly makes the vision-language backbone a better retrieval key, and the actions of the VLAs remain close to the demonstrations. In addition, we introduce Local Action Consistency (LAC), an offline metric that measures whether nearby observations in representation space are also associated with similar future actions. We show that LAC tracks the success rate of retrieval and can guide the training of a retrieval key. Our evaluation and source code are available at this https URL.

---

## 3. Third Eye: Beyond Immediate Gains in Recursive Self-Improvement

**Authors:** Sujato Dutta, Padala Indira Sneha, Kypu Mahitha, Shashank Vanga, Neeraj Choudhary
**arXiv:** [2611.12988](https://arxiv.org/abs/2611.12988)
**Categories:** Machine Learning (cs.LG); Artificial Intelligence (cs.AI)

Does a useful self-update remain useful after the model updates again? Third Eye separates immediate performance from the outcome of a further native update. We evaluate five 3-8B backbones on math and code: 64 fresh runs, three candidates per run, and three continuations per candidate. Selection and final scoring use disjoint items. In the balanced Qwen3-4B/Llama-3.2-3B comparison, immediate-selected utility is near zero, but continuation reduces it by 1.78 percentage points (simultaneous 95% interval [0.68, 2.88]). Candidate-averaged immediate utility is already negative: selection partly accounts for the apparently neutral first step. Continuation also lowers utility for SmolLM3-3B and Llama-3.1-8B; Qwen3-8B remains inconclusive. Target and out-of-distribution losses dominate retention changes. Matched recipe and recipient-donor controls identify neither a reliable mitigation nor a single mechanism. The results support evaluating persistent self-updates as adaptation transitions, with independent scoring and a no-update baseline, rather than interpreting immediate performance as their full value.

---

## 4. The RSI Tax: When Recursive Self-Improvement Is Not Worth the Cost

**Authors:** Yitong Zhang, Ang Li, Yisen Wang
**arXiv:** [2611.13524](https://arxiv.org/abs/2611.13524)
**Categories:** Machine Learning (cs.LG)

Recursive self-improvement (RSI) seeks to improve an agent using its own task experience. Its practical value depends on whether performance gains justify the full cost of self-improvement and task execution. We evaluate this trade-off on continual task streams, scoring each task before its feedback is used for subsequent updates. We define the \emph{RSI Tax} as the token cost of the self-improvement process and include it alongside task-execution costs in end-to-end evaluation. Across six methods and two language models, a bounded-note baseline matches or exceeds the observed accuracy of Meta-Harness, EvoSkill, and RRSI, with mean total-token savings of 65.6-71.0\%. We decompose the RSI Tax into verification, exploration, and writing costs, and track subsequent use of the associated state or artifact. For these three RSI methods, verification accounts for 74.8--93.6% of the aggregate RSI Tax. A substantial share of the RSI Tax is also associated with states or artifacts that are not used later in the evaluated streams. These results expose a practical limitation of costly RSI procedures: improvements in the deployed agent need not justify the expense of the improvement process. They motivate RSI objectives that jointly optimize the RSI Tax and expected task-execution cost while ensuring continued growth in agent capabilities across the task stream.

---

## 5. Is Your Robot's Memory Just a Clock? Temporal Shortcuts in Memory-Augmented VLA Policies

**Authors:** Chubin Zhang, Bo An
**arXiv:** [2611.14488](https://arxiv.org/abs/2611.14488)
**Categories:** Robotics (cs.RO)

Memory-augmented vision-language-action (VLA) policies are meant to remember what happened. Many of them, however, fill memory by time: they sample frames uniformly across the episode and stamp each frame with its time step. Because time passes even when nothing happens, such a memory may not tell waiting from working. We show that it does not. On the counting tasks of RoboMME, we make the robot briefly pause or fidget its wrist. Such a null event changes nothing the task depends on, yet a released memory VLA counts the interval as work done and stops early. We call this failure phantom progress. It cuts success from 47 to 16 of 50 on one task and from 44 to 10 on the other. When the same frames are withheld from memory, success returns, so the cause lies in memory rather than in the interruption itself. We trace the failure to a temporal shortcut: because demonstrations proceed at a steady pace, elapsed time predicts progress. Indeed, rescaling the time stamps alone makes the policy stop early when the clock runs fast and repeat when it runs slow. Surprisingly, removing the time encoding does not cure the failure, because the frames of a null event still occupy slots of the time-sampled memory. Across RoboMME's released designs, vulnerability follows how memory is indexed. Of the fixes the diagnosis suggests, training with injected pauses does not remove the failure and impairs counting, whereas indexing memory by events recovers half or more of the loss without retraining. A memory meant to remember what happened should count events rather than clock ticks.

---

## 6. LEASH: Stay Safe in Agentic Robotics

**Authors:** Qinfeng Zhu, Weiguang Zhao, Ke Sun, ..., Lei Fan, Kaizhu Huang
**arXiv:** [2611.14115](https://arxiv.org/abs/2611.14115)
**Categories:** Robotics (cs.RO)

Foundation models such as GPT and Claude have shown strong capabilities in spatial understanding and embodied intelligence. These advances make agentic robotics a promising path toward artificial general intelligence in robotics. However, we find that using foundation models to control robots poses serious safety risks, and comprehensive safety evaluation is still lacking. We introduce RoboRisk, a comprehensive benchmark for evaluating safety in agentic robotics. Its 92 simulated tasks and 13 physical-robot tasks fall into five categories: Task-level Refusal (T), Plan Repair (P), Execution-time Hazard (E), Injection (I), and Sequential Memory (S). Prior benchmarks cover at most two of these categories, and several evaluate only text outputs. In contrast, RoboRisk covers all five and executes every task in closed loop. We evaluate six state-of-the-art foundation models on RoboRisk: GPT-6 Astra, GPT-6.1 Sol, GPT-6 Luna, Claude Opus 5.5, Gemini 4 Argon, and Grok 4.7. These models generally show high harm rates. We also evaluate two robot-specific APIs: the Dream API and PokeBot's RoboAPI. We further propose the Lease-Enforced Agentic Safety Harness (LEASH), which offers essential safety infrastructure for agentic robotics and can be integrated into nearly any agentic architecture. LEASH leverages a decision model (Jev or OpenAI's Decisions API) to implement task, action, and commit gates, which review the task, each action, and each irreversible operation in their visual context. The planner and all three gates share a common safety policy. Experiments on RoboRisk in simulation and on physical robots show that LEASH effectively reduces harm across all six foundation models. It largely preserves their task completion performance and adds little time and token overhead.

---
