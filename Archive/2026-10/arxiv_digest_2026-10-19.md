# arXiv Daily Digest — 2026-10-19

**Mode:** direct
**Categories:** cs.AI, cs.LG, cs.RO, cs.CV
**Keywords:** VLA, RSI, agentic robot, self-improving robot, self-evolving robot, robot harness
**Papers found:** 13

---

## 1. R$^2$Orch: Recursive Self-Improvement for Agent Orchestration via Self-Play within a Skill-Internalization Loop

**Authors:** Mingda Zhang, Yun Huang, Qiang Huang, ..., Jian Wang, Xiaoying Tang
**arXiv:** [2610.22740](https://arxiv.org/abs/2610.22740)
**Categories:** Artificial Intelligence (cs.AI)

In recent years, agentic orchestration has been widely applied to solve complex human tasks. However, existing orchestration learning still faces key challenges, including hand-designed curricula, advantage collapse when a task's rollouts all reach the same outcome, and unreliable evaluation signals that judge each skill by one noisy score. To address these challenges, we propose R$^2$Orch, a new paradigm of Recursive Self-Play Orchestration: an inner loop of self-play that improves the orchestrator on self-chosen tasks, and an outer loop that improves how the inner loop improves. To support this paradigm, we introduce Recursive Learnability, a training objective that rewards a Proposer for choosing tasks whose rollouts keep reaching different outcomes as skills are withdrawn. Built on this objective, we further propose Skill Withdrawal, in which the outer loop withdraws each skill once a controlled evaluation within self-play shows that the orchestrator performs as well without it. Moreover, the two loops form one cycle: failures are distilled into skills, skills into parameters, and withdrawals lead the Proposer to new failures, so the orchestrator moves toward zero-skill deployment. Experimental results on twelve datasets show that R$^2$Orch consistently outperforms baselines across question answering, math, code, and interactive tasks.

---

## 2. Beyond Success Rate: Interventional Evaluation of Memory in Vision-Language-Action Systems

**Authors:** Keyuan Luo, Yi Xie, Wanyun Ling, ..., Ziyue Li, Zhuoqi Zeng
**arXiv:** [2610.23372](https://arxiv.org/abs/2610.23372)
**Categories:** Robotics (cs.RO); Machine Learning (cs.LG)

When we say that a robot uses memory, does that memory actually play a role? Success-rate ablations alone cannot establish the use of task-relevant facts: they change information and computation together, while aggregate rates can hide offsetting gains and losses. We propose an Interventional Memory Evaluation Protocol (IMEP) for vision-language-action (VLA) systems to address four questions: (1) Does memory provide a net benefit? (2) Under what conditions does memory help? (3) Do changes to memory alter task outcomes? (4) Are these effects specific to task-relevant facts? At the retrieval interface, we compare target-fact substitutions with fact-preserving replacements, minimal numerical perturbations, and exact replicas, while assessing decision correctness separately from motor execution success. We evaluate within-episode, cross-episode, and agentic memory. In cross-episode learned-bank experiments, a one-unit-in-the-last-place (ULP) intervention, including its installation procedure, changes 11.9% of seed-paired outcomes, while changing key facts produces no clear additional effect over fact-preserving replacements. To examine when memory helps, we introduce ChainBench, where correct decisions require historical information unavailable in current observations. The full memory configuration raises task success from 39.1% to 74.3%, matching the oracle-decision condition under shared recorded executions. These results show that correct history can support robot decisions, but establishing whether a memory system realizes this benefit requires fact-specific evidence beyond aggregate success rates.

---

## 3. NestedVLA: Learning to Consolidate and Generate Skills for Vision-Language-Action Models

**Authors:** Guodong Du, Wanyu Lin
**arXiv:** [2610.23271](https://arxiv.org/abs/2610.23271)
**Categories:** Robotics (cs.RO); Machine Learning (cs.LG)

Vision--Language--Action (VLA) models promise generalist robotic agents, yet consolidating skills learned across heterogeneous tasks and environments remains difficult: training data is fragmented across platforms, joint multi-task training suffers from interference, and model merging tends to introduce parameter conflicts or require architectural changes. We instead advocate a paradigm in which skills are first learned independently and then consolidated post hoc. To this end, we propose NestedVLA, which replaces parameter aggregation with parameter generation: a nested hypernetwork, conditioned on the target task, synthesizes task-adaptive action-expert parameters that compose with a frozen base VLA. Task-specific compressed VLM residuals are retained separately. This formulation enables flexible task-conditioned skill reuse while mitigating interference. Across three RL benchmarks (MetaWorld, ManiSkill, CALVIN), NestedVLA outperforms the strongest model-merging baseline by 41 pp on average, matches per-task fine-tuning within 1 pp on ManiSkill, and substantially closes the gap on CALVIN, pointing toward a storage-efficient route to skill consolidation. Code is available at this https URL.

---

## 4. Embodiment-Classifier Guidance: Transferring Frozen VLAs Across Robot Dynamics without Demonstrations

**Authors:** Devin Han, Hershraj Niranjani
**arXiv:** [2610.22576](https://arxiv.org/abs/2610.22576)
**Categories:** Robotics (cs.RO); Machine Learning (cs.LG)

Flow-based policies such as $\pi_0$ are trained on a fixed set of embodiments, and transferring them to new ones is an open problem. To adapt a frozen $\pi_0$ to a new embodiment without additional demonstrations or parameter updates, we train a lightweight embodiment classifier to distinguish successful action chunks on the source body from those on the target body, using a few calibration tasks. On transfer tasks that $\pi_0$ saw on its source body but the classifier was never trained on, we nudge each denoising step of $\pi_0$ with the classifier's gradient, which estimates the direction from the distribution of successful actions on the source body toward that on the target body. On the LIBERO simulation benchmark with four modified controllers, embodiment-classifier guidance raises $\pi_0$'s average success on the target bodies from 72% to 80% across 12 suite-controller pairs, with a 31% relative reduction in failures (11 of 12 gain; 5 significant after Holm correction). In simulation, guidance is data-efficient, needing few target-body rollouts per task, which makes it promising for sim-to-real transfer, where rollouts are costly. Guidance is mixed on weak wrists and harmful on a locked wrist, when the classifier lacks data or favors infeasible motions. Collecting more target-body data with guided $\pi_0$ can fill such gaps: on one weak-wrist arm, guided $\pi_0$ solved a task on which unguided $\pi_0$ had zero successes in the original data, and retraining the classifier on the guided successes raised success from 52.5% to 70.7%.

---

## 5. When Plans Change, Remember: Replanning-Guided Visual Memory for Vision-Language-Action Models

**Authors:** Victoria Smelova, Daniil Kazachkov, Georgiy Kazantsev, ..., Aleksandr I. Panov, Alexey K. Kovalev
**arXiv:** [2610.22556](https://arxiv.org/abs/2610.22556)
**Categories:** Robotics (cs.RO); Machine Learning (cs.LG)

Long-horizon, multi-stage Vision-Language-Action (VLA) policies often require visual information that is no longer present in the current observation. Retaining the complete observation history is computationally expensive and highly redundant, motivating selective visual memory. We introduce RePlanMem-VLA (Replanning-Guided Keyframe Memory for VLA), which turns a policy's own plan revisions into an online memory-write signal. Under receding-horizon execution, consecutive action chunks predict some of the same future actions. RePlanMem-VLA treats unusually large disagreement between these temporally aligned predictions as evidence of a task-relevant event. We first compare 35 disagreement measures across single-task autoregressive decoder-only and Flow-Matching Transformers trained from scratch, then validate the selected signals on pretrained OpenVLA-OFT and $\pi_{0.5}$ policies over MIKASA-Robo-VLA tasks. The resulting detectors achieve ROC-AUC of 0.981-0.997. We then use the selected signals in RePlanMem-VLA to trigger updates to a bounded visual memory, with a robot-masked write filter suppressing redundant frames. In the evaluated memory-retention experiments, RePlanMem-VLA preserves task-relevant observations until the later decision point in 100% of episodes. Real-robot replay data further show that event selection and redundancy suppression extend beyond simulation. These results establish plan revision as a policy-internal signal for controlling what a VLA remembers. Website: this https URL.

---

## 6. Enhancing Visual Task-Redirection Attacks on Vision-Language-Action Models via Closed-Loop Optimization

**Authors:** Chunjin Ye, Guanying Chen, Jianjie Huang, ..., Tieyun Qian, Xiaochun Cao
**arXiv:** [2610.23566](https://arxiv.org/abs/2610.23566)
**Categories:** Robotics (cs.RO)

Vision-language-action (VLA) models enable language-guided robot manipulation, but remain vulnerable to visual attacks that undermine user control over robot behavior. Prior studies optimize visual perturbations using fixed target supervision. However, the perturbation can change earlier actions and, in turn, the physical states reached later. As the attacked trajectory evolves, this supervision may no longer match the behavior needed at the states actually reached. Accurately matching these targets can therefore fail to advance the attacker-specified task. Even with suitable supervision, reducing average matching error does not ensure sustained task progress. The robot may still fail at a critical stage, and further updates can disrupt previously successful behavior. To address these limitations, we propose TRACO, a framework that enhances existing targeted visual attacks through closed-loop optimization. Its Execution-Driven Supervision rebuilds supervision for the states reached under attack to guide subsequent updates. Within this framework, Progress-Guided Selection focuses updates where progress stalls while maintaining supervision on the earlier behavior needed to reach that point. Experiments across VLA models and simulation environments show improved task-redirection success with TRACO, highlighting the security implications of closed-loop attack optimization.

---

## 7. Look Before You Act: Bridging Active Perception and Vision-Language-Action Models via Observation-Aligned Data Adaptation

**Authors:** Jiawei Geng, Zhenyang Liu, Yuzheng Wu, Yongchong Gu, Yanwei Fu
**arXiv:** [2610.23378](https://arxiv.org/abs/2610.23378)
**Categories:** Robotics (cs.RO)

Robots manipulating objects in clutter must decide not only how to act, but also where to look. Although active camera motion can expose an occluded target, it may move the robot into an initial observation-state distribution that differs from the manipulation policy's training distribution. We identify this problem as first-frame distribution sensitivity: under perturbed starts in LIBERO, naively prepending camera repositioning to pi_0.5 reduces success from 46.3% to 11.5%. We introduce ActiveAlign, a data-adaptation framework that trains a Vision-Language-Action (VLA) policy from the states at which active perception terminates. A learned viewpoint module first generates a camera trajectory. Offline, ActiveAlign uses closed-loop alignment to connect the trajectory endpoint to an existing demonstration, replays the remaining manipulation trajectory, and retains successful continuations for fine-tuning. At deployment, the same viewpoint module precedes the adapted VLA without modifying its architecture. Across 40 LIBERO tasks, ActiveAlign achieves 70.7% success with pi_0 and 72.7% with pi_0.5, outperforming their standard-training baselines by 40.0% and 26.4% respectively. Matched-state and data-matched controls support gains beyond prefix shortening and generic viewpoint augmentation; OpenVLA and GR00T N1 also show the same trend. Success rate under physical occlusion in real world increases from 35/90 to 83/90. These results show that active perception benefits manipulation when policy training is aligned with the observation and robot-state distribution induced by viewpoint selection.

---

## 8. From Sliding Windows to Self-evolving Lifelong Memory: A Dual-perspective Survey of Memory Paradigms for Long-Horizon Robotics VLA Models

**Authors:** Yong Wang, Boyu Shen, Xinwei Zhang, Yizheng Li, Keyuan Luo
**arXiv:** [2610.23319](https://arxiv.org/abs/2610.23319)
**Categories:** Robotics (cs.RO)

Long-horizon robotic tasks expose a fundamental limitation of current Vision-Language-Action (VLA) models because their restricted temporal context pre-vents effective accumulation and reuse of past experiences. As a result, memory has become a fundamental component for enabling embodied agents to perform long-horizon reasoning and adaptive decision-making. This survey presents a systematic taxonomy of VLA memory mechanisms based on memory scope and persistence, categorizing existing approaches into five representative paradigms and one emerging frontier. Based on this taxonomy, we compare representative VLA memory systems in terms of memory characteristics, architectural com-plexity, and open-source maturity, revealing a clear trade-off in which increasing architectural complexity is generally accompanied by decreasing open-source ma-turity. Finally, we discuss the key challenges in building full-lifecycle memory systems, including efficient memory management and lifelong knowledge evolu-tion. Overall, this survey provides a unified perspective on memory architectures for VLA agents and offers insights into the development of lifelong embodied in-telligence.

---

## 9. VLA-Fabric: Learning Interaction for Composable Multi-Arm VLA Agents

**Authors:** Chenglong Zhang, Shuaijun Liu, Feiyang You, ..., Chengyu Wu, Ningxin Su
**arXiv:** [2610.23018](https://arxiv.org/abs/2610.23018)
**Categories:** Robotics (cs.RO)

Vision-language-action (VLA) models are rapidly expanding what individual robots can accomplish, yet many real-world manipulation settings require multiple arms to operate as a coordinated system. Existing approaches organize multi-arm coordination in different ways, including centralized joint policies, high-level task or role assignment, and locally executed policies that react to teammates. However, how complete action-producing VLAs should explicitly interact with one another during action generation remains largely unexplored. We introduce VLA-Fabric, which organizes one complete VLA per arm while preserving local perception and action ownership, and enables coordination through learned interaction across policy boundaries. We first systematically study where such interaction should occur, how peer information should be aggregated, and how the interaction should be learned, revealing complementary coordination functions spanning shared context, peer-specific latent information, and action-stage interaction. We then re-instantiate these functions in a structurally different VLA architecture, showing that the coordination principle is not tied to a particular tensor layout or backbone implementation. Finally, we compose teams of three and four arms and evaluate them in simulation and physical experiments. On all four physical tasks, Full interaction improves success over independently trained local policies by 16--40 percentage points. Together, these results suggest that explicit interaction among complete VLA policies offers a scalable path toward networked embodied intelligence.

---

## 10. MambaAct: Efficient Mamba Action Experts for Flow-Matching Vision-Language-Action Models

**Authors:** Khuyen Pham, Tran Nguyen Le, Edoardo Fazzari, Cesare Stefanini
**arXiv:** [2610.22951](https://arxiv.org/abs/2610.22951)
**Categories:** Robotics (cs.RO); Computer Vision and Pattern Recognition (cs.CV)

Vision-language-action (VLA) models have shown strong promise for generalist robotic manipulation, but their inference cost remains a major bottleneck for real-time control. This limitation is especially pronounced in flow-matching VLAs such as $\pi_{0.5}$, where the action expert is evaluated repeatedly during iterative denoising. We introduce MambaAct, an efficient Mamba action expert for flow-matching VLA policies. MambaAct retains the pretrained visual-language prefix encoder of $\pi_{0.5}$, while replacing its transformer-based action expert with a compact Mamba-based action expert. Within this expert, Mamba serves as the action mixer that models dependencies across the noisy continuous-action sequence. To preserve visual-language conditioning without repeated token-level cross-attention, MambaAct uses a lightweight Context Compressor to map Vision-language model (VLM) prefix tokens into a compact conditioning signal that gates and modulates each Mamba action block. MambaAct uses a $10\times$ smaller action expert and reduces flow-matching denoising latency by $64.8\%$ on LIBERO and $58.8\%$ in real-world deployment, while improving mean LIBERO success by $1.08$ percentage points across three independent fine-tuning seeds and maintaining gains on LIBERO-Plus and real-world benchmarks. Our code and model weights are publicly available at this https URL.

---

## 11. EmbodiedMidtrain: Bridging the Gap between Vision-Language Models and Vision-Language-Action Models via Mid-training

**Authors:** Yiyang Du, Zhanqiu Guo, Haochen Zhang, ..., Yonatan Bisk, Chenyan Xiong
**arXiv:** [2604.20012](https://arxiv.org/abs/2604.20012)
**Categories:** Computer Vision and Pattern Recognition (cs.CV); Artificial Intelligence (cs.AI); Computation and Language (cs.CL); Robotics (cs.RO)

Vision-Language-Action Models (VLAs) inherit their visual and linguistic capabilities from Vision-Language Models (VLMs), yet most VLAs are built from off-the-shelf VLMs that are not adapted to the embodied domain, limiting their downstream performance. In this work, we propose EmbodiedMidtrain to bridge the gap between VLMs and VLAs. We first characterize the data distribution gap between them, showing that VLA data occupy compact regions that are largely separated from the broader VLM distribution, while the degree of alignment varies substantially both across and within VLM data sources. Then, we build a mid-training data engine that leverages a lightweight learnable proximity estimator to select the most VLA-aligned candidates from a large VLM pool, and produce EmbodiedMidtrain-1M, a VLM dataset that we further use to mid-train the VLM before downstream VLA fine-tuning. Experiments on both simulated robot manipulation benchmarks and real-world tasks show consistent VLA performance gains over off-the-shelf checkpoints across VLM backbones and VLA action heads. These gains extend to downstream tasks not used to guide data selection. Further analysis reveals that mid-training provides a stronger initialization for VLA fine-tuning, with gains emerging from the earliest steps and widening throughout training. Moreover, the data engine captures both dataset-level and sample-level alignment signals, favoring spatial reasoning over text-centric tasks while preserving the diversity of the VLM data. We will release all code, data and models for future research.

---

## 12. Language Models Learn to Improve Language Models

**Authors:** Minhua Lin, Zijun Wang, Zewen Liu, ..., Suhang Wang, Hanqing Lu
**arXiv:** [2610.23344](https://arxiv.org/abs/2610.23344)
**Categories:** Computation and Language (cs.CL); Artificial Intelligence (cs.AI)

Large language models (LLMs) are increasingly used to automate AI research, including language-model (LM) development, offering a potential path toward recursive self-improvement. However, turning experimental feedback into a learned ability to propose effective improvements across models faces two challenges. First, training such an ability with real feedback is expensive: reinforcement learning (RL) requires evaluating tens of thousands of proposals, each potentially requiring a full model-training run. Even at ten GPU-hours per run, reward collection alone would consume hundreds of thousands of GPU-hours, motivating a cheaper surrogate. Second, surrogate feedback can become unreliable as policy optimization favors overestimated proposals when the proposal distribution shifts. To address these challenges, we propose LM2LM, which trains LLMs with RL to generate effective LM improvement proposals. To provide scalable feedback, we use a research world model (RWM), a frozen LLM that predicts proposal gains from real experimental records provided in context, as the reward model for RL. To maintain feedback reliability, we periodically execute current-policy proposals ranked highly by the RWM and add their measured outcomes to its context. Across eight autoregressive and diffusion LM development environments, real-execution evaluations on held-out tasks show that LM2LM enables Qwen3.8-27B to outperform GPT-6-sol, even when GPT-6-sol is given 300 real experimental records in context, while requiring 33% lower data-generation cost. LM2LM also generalizes to a model family unseen during training.

---

## 13. Unifying Embodied Foundation Models via a Model-to-Policy Formulation

**Authors:** Xinyi Hong, Mingyang Ren
**arXiv:** [2610.23053](https://arxiv.org/abs/2610.23053)
**Categories:** Robotics (cs.RO); Artificial Intelligence (cs.AI); Machine Learning (cs.LG)

Vision-language-action (VLA) models and world-action models (WAMs) have emerged as promising approaches to robot learning and control. These models integrate multimodal perception and action generation, but differ in their architectures, output representations, and learning objectives. In this paper, we present a unified, architecture-agnostic probabilistic formulation for embodied foundation models based on stochastic kernels. Our formulation has two key components: (i) we characterize embodied foundation models through conditional output distributions and action-realization kernels, which together induce task-conditioned robot policies; and (ii) we connect pretraining and post-training to policy deployment, accommodating model-specific pretraining objectives and offline or online post-training strategies. We instantiate the formulation for OpenVLA and DreamZero, covering autoregressive action-token prediction and joint video-action generation.

---
