# arXiv Daily Digest — 2026-11-25

**Mode:** direct
**Categories:** cs.AI, cs.LG, cs.RO, cs.CV
**Keywords:** VLA, RSI, RUA, agentic robot, self-improving robot, self-evolving robot, robot harness
**Papers found:** 15

---

## 1. RecurSciBench: Benchmarking Recursive Self-Improvement in Data-Driven Scientific Research

**Authors:** Wenxi Xu, Chuan Qin, Zihan Wang, ..., Yuanchun Zhou, Hengshu Zhu
**arXiv:** [2611.32508](https://arxiv.org/abs/2611.32508)
**Categories:** Artificial Intelligence (cs.AI)

Large language model (LLM)-based agents are advancing the automation of data-driven scientific research. Recent advances in recursive self-improvement (RSI) offer the potential for these agents to continuously improve through experience, but evaluating transfer across scientific tasks requires executable, scientifically verifiable tasks and independent assessment of self-improvement gains. We introduce RecurSciBench, a scalable benchmark for evaluating RSI in data-driven scientific research. Its RecurSciPipe framework automatically constructs scientific modeling and data analysis tasks from raw datasets, with execution-based verification and scientific validity checks. RecurSciBench spans four scientific domains, multiple data modalities, and varied scientific objectives. We evaluate four RSI systems by comparing their initial and evolved states on independent tasks after evolution on source tasks, covering within-type, cross-type, and cross-domain transfer. Experiments show that the benefits of self-improvement vary across agent systems and scientific domains. Positive overall gains can coexist with regressions on individual tasks. Experience can transfer across task types and benefit other domains even without measurable gains in the source domain.

---

## 2. Sparse Poison, Strong Hijack: Efficient Trajectory-Level Backdoors in Vision-Language-Action Models with Only 1\% Poisoning

**Authors:** Simin Huang, Jiawei Chen, Shaolong Zhu, Qiwei Liang, Zhaoxia Yin
**arXiv:** [2611.32304](https://arxiv.org/abs/2611.32304)
**Categories:** Artificial Intelligence (cs.AI)

Vision-Language-Action (VLA) models advance robotic manipulation, but their reliance on demonstrations exposes them to backdoor threats. Among these threats, trajectory-level targeted backdoors are particularly challenging and may pose greater safety risks than behavior-disrupting attacks: rather than merely causing task failures or local action deviations, they must sustain closed-loop redirection to complete an attacker-specified multi-step task. To reliably induce such behaviors, existing methods typically rely on high poisoning rates to obtain sufficient target-trajectory supervision. However, high poisoning rates may compromise clean-task performance, whereas low rates leave target-trajectory supervision scarce and backdoor learning vulnerable to interference from dominant clean-task updates. To resolve this trade-off at low poisoning rates, we propose a two-stage co-optimization framework guided by vision, language, and action. Stage I freezes the policy and uses differentiable rendering and multimodal supervision to optimize a 3D trigger's texture, translation, and scale, strengthening trigger-target associations from limited poisoned demonstrations. Building on the optimized trigger, Stage II applies source-selective dual-LoRA adaptation to decouple clean and backdoor updates and mitigate their interference, followed by learned column-wise calibration and analytic fusion into a unified policy. Experiments on OpenVLA, OpenVLA-OFT, $\pi_0$, and $\pi_{0.5}$ across four LIBERO suites show consistent gains over all evaluated attack baselines. With only 1% poisoned data, our method achieves 86.4% target success and 95.2% clean-task success on OpenVLA-OFT in LIBERO-Spatial. Real-robot trials also demonstrate trajectory-level hijacking.

---

## 3. Perception Is Enough, at the Right Scale: Scale-Adaptive Token Pruning for Vision-Language-Action Models

**Authors:** Yifeng Lin, Liuxiang Qiu, Yunfeng Chen, Tiesong Zhao
**arXiv:** [2611.31954](https://arxiv.org/abs/2611.31954)
**Categories:** Artificial Intelligence (cs.AI); Robotics (cs.RO)

Vision-language-action (VLA) models must process continuous streams of visual observations, and the resulting computational cost limits real-time robotic control. Token pruning reduces this cost, but a fixed semantic scale of perceptual representation can overlook information needed at different stages of manipulation. We show that perceptual semantics can guide effective token selection without relying on internal attention when the selection scale adapts to the scene's evolving semantic structure. Based on this observation, we introduce TauPrune-VLA, a training-free method that controls the scale of the retained perceptual representation through a single perception temperature $\tau$. To adapt this scale as manipulation proceeds, TauPrune-VLA updates $\tau$ online using trends in perceptual semantics, with robot-state changes and action magnitude regulating the adjustment strength. While these semantics evolve over the course of manipulation, they remain relatively stable between consecutive frames. This continuity allows retention indices computed from the current observation to be applied at the next policy invocation, enabling token selection to run asynchronously with inference and reducing pruning overhead. Evaluated across diverse VLA models and simulation benchmarks, TauPrune-VLA achieves up to a $1.86\times$ inference speedup while maintaining near-baseline task success rates. We further validate its effectiveness on two real-world robotic platforms.

---

## 4. A recursive self-improvement framework for electron microscopy analysis

**Authors:** Yaotian Yang, Sijia Tao, Yuping Zhang, ..., Xiao Chen, Fei Wei
**arXiv:** [2611.32325](https://arxiv.org/abs/2611.32325)
**Categories:** Computer Vision and Pattern Recognition (cs.CV); Materials Science (cond-mat.mtrl-sci); Artificial Intelligence (cs.AI)

Resolving local atomic structures such as defects and interfaces from electron microscopy contrast relies heavily on researcher judgement, leading to low efficiency and subjective standards. Here we present PhyEvo-Mic-RSI, a physics-guided and expert-informed recursive self-improvement framework that turns one-off human corrections into reusable, verifiable capabilities by updating executable operators, parameters and routing rules with versioned inheritance. Given researcher-defined tasks, the system selects analysis paths from image features without expert labels, while testing and inheriting code updates under fixed budgets. Combining physical priors with expert feedback improves atomic point-defect detection over larger models and raises cross-material interface coverage from 5.13% to 72.11% within a 10% area budget. Adapting the framework to micrographs from unseen studies further separates touching nanoparticles by aligning optimization with particle-level measurements. This work moves computational microscopy beyond standalone models and static scripts towards self-evolving platforms that accumulate human scientific expertise

---

## 5. Near-Zero Forgetting Is Not Enough: Out-of-Distribution Robustness in Continual Learning of Pretrained VLAs

**Authors:** Adrià Ruiz, Bartłomiej Twardowski, Tinne Tuytelaars, Sergi Masip
**arXiv:** [2611.31511](https://arxiv.org/abs/2611.31511)
**Categories:** Machine Learning (cs.LG); Robotics (cs.RO)

Recent work shows that pretrained Vision-Language-Action (VLA) models exhibit near-zero forgetting in specific continual learning settings with experience replay. However, robustness to domain shift of learned tasks remains unexplored. In this work, we study the robustness of Pi0 fine-tuned with experience replay under out-of-distribution (OOD) data using the LIBERO and LIBERO-Plus benchmarks. While the in-domain (ID) setup achieves near-zero catastrophic forgetting, OOD performance on previous tasks quickly collapses. Specifically, we show that during the continual learning process, the OOD capabilities of the model degrade, following a shared representational pattern across domain shifts, which is also visible behaviorally in the two simpler suites. Representational analysis shows that drift concentrates in the multimodal and action features. Linear probes indicate that OOD features still retain task-relevant information, but appear unreadable, consistent with representation misalignment. These findings suggest that even when ID stability remains intact, severe OOD forgetting can still occur, accompanied by representational drift during continual learning.

---

## 6. PyRUA-Dex: Learning Programmatic Policies for Dexterous Bimanual Manipulation with Coding Agents

**Authors:** Feixiang Ruan, Guodong Lv, Kewei Zhang, ..., Enze Xie, Daquan Zhou
**arXiv:** [2611.33144](https://arxiv.org/abs/2611.33144)
**Categories:** Robotics (cs.RO)

Learning for dexterous manipulation is limited by the scarcity of high-quality demonstrations: retargeting from human video is imprecise, teleoperation gives no force feedback to the operator, and exoskeleton-based collection is hard to scale up. We present PyRUA-Dex, a framework that enables coding agents to develop dexterous manipulation through programmatic policy, without the need of demonstrations. The programmatic policy is developed in two stages: during exploration, multiple agents explore in parallel for task skills and ways to compose them, and a distilling agent condenses the successful attempts into a task library and one program. During refinement, this program is improved through randomized layouts for enhanced robustness and execution efficiency. In simulated environments, PyRUA-Dex achieves SOTA on Bench2Dex with a score of 72.9 and reaches 81.0% success on DexJoCo under full randomization, ahead of every trained policy on both benchmarks. In real world experiments on a bimanual platform with two 22-DoF hands, PyRUA-Dex learns to play piano, write calligraphy, and other tasks efficiently: learning a new piece from sheet music takes as little as 30 minutes. These results suggest that PyRUA-Dex is an effective framework for developing dexterous manipulation policies with coding agents in the absence of high quality dexterous manipulation demonstrations.

---

## 7. DiffGR00T: Execution-Aware Differentiable Training for Humanoid Whole-Body Vision-Language-Action Models

**Authors:** Sichen Wu, Qian Sun, Mengfan Liu, ..., Bike Zhu, Hesheng Wang
**arXiv:** [2611.32665](https://arxiv.org/abs/2611.32665)
**Categories:** Robotics (cs.RO)

Vision-language-action (VLA) models have achieved strong results in arm-centric manipulation, yet humanoid whole-body control (WBC) requires dynamic balance and tightly coupled full-body coordination. Existing hierarchical humanoid VLAs typically decouple motion generation from physical execution, leaving tracking and balance errors unable to directly optimize the VLA generator. We propose DiffGR00T, an end-to-end differentiable training framework that couples GR00T N1.7 with SONIC, a pretrained whole-body behavior foundation model. To enable execution-aware differentiable training, we replace the non-differentiable simulator with a learned, action-conditioned world model, allowing multi-step body-execution losses to backpropagate through the frozen whole-body controller and the flow-matching sampler directly into the VLA action head. On four HumanoidArena simulation tasks, DiffGR00T improves average task success by 12.5 percentage points over the supervised base VLA (59.2% to 71.7%), demonstrating that execution-aware gradients effectively align high-level motion generation with closed-loop whole-body dynamics.

---

## 8. VLAs Execute, Code Recovers: 3D Skill Envelopes Bridge the Compositional Gap in Agentic Manipulation

**Authors:** Jiajie Zhang, Yankai Xiang, Changhao Chen
**arXiv:** [2611.32245](https://arxiv.org/abs/2611.32245)
**Categories:** Robotics (cs.RO)

Composing frozen Vision-Language-Action (VLA) skills under an agentic planner promises scalable long-horizon manipulation without long-horizon demonstrations, yet strong atomic skills routinely fail at seams even under a correct plan. Standard remedies reset the robot's pose or draft entry conditions in language, missing the physical cause we uncover via causal interventions: even after re-homing, a frozen VLA rigidly retraces its habitual trajectory and collides with displaced scene residue, whether or not it can see it. We propose the Skill Envelope, a policy-measured 3D geometric precondition capturing the volume a frozen skill sweeps during successful executions. Exploiting the insight that the rigidity making a frozen skill fragile at seams also makes its trajectory predictable in advance, we expose each envelope as two classical 3D tools (CHECK to detect blocking residue and FREE to locate safe placement regions), establishing a division of labor where VLAs execute in-distribution manipulation and code repairs out-of-distribution states. On LIBERO-Goal with frozen $\pi_{0.5}$, our zero-failure envelope predicts collisions at 0.946 AUROC (0.944 from one RGB-D view) and beats frontier VLMs on seam readiness (0.902 vs. 0.793); using it for skill ordering and code repair lifts success from 82.8% to 92.3% on two-step seams and from 29.7% to 93.8% on drawer-bearing 3-4 step chains, matching privileged world reset. Together, these results show that reliable VLA composition hinges on measuring a policy's physical workspace rather than guessing preconditions in language. Ongoing work closes the loop with autonomous LLM orchestration, synthesized free-object recovery, and cross-policy evaluation on cluttered benchmarks and real hardware.

---

## 9. KeyMemVLA: Subtask-Guided Key Memory for Long-Horizon Robotic Manipulation

**Authors:** Yongwei Zhang, Tao Chen, Sicheng Ma, ..., Zhikun She, Ce Hao
**arXiv:** [2611.32081](https://arxiv.org/abs/2611.32081)
**Categories:** Robotics (cs.RO)

Memory-dependent long-horizon manipulation requires vision-language-action (VLA) policies to infer task progress and recall evidence absent from current observations. Under a limited memory budget, the challenge is to retain history that resolves stage ambiguity and supports subsequent decisions. We present KeyMemVLA, a subtask-guided key memory framework based on progress indication and decision-evidence retention. A two-level annotation process selects subtasks satisfying either criterion and labels their final frames as keyframes to supervise online memory writes. A shared vision-language backbone jointly learns subtask, action, and keyframe prediction. At inference, the policy first predicts the current subtask from the instruction, visual context, and memory, then uses this semantic condition to predict actions and future memory-write positions. Actual observations are retained at the selected times during execution. We introduce KMBench to evaluate active memory retention for decisions across subtasks. Evaluations on RMBench-$M(n)$, RoboTwin-MeM, KMBench, and real-world manipulation tasks show higher average success rates than the compared baselines. Ablation studies and representation analysis support the roles of key memory and explicit task-progress semantics. These results highlight the value of coupling sparse key memory with online progress inference for history-dependent control.

---

## 10. Hi3R-VLA: Grounding Semantics and Actions in 3D

**Authors:** Shizhe Chen, Paul Pacaud, Cordelia Schmid
**arXiv:** [2611.31535](https://arxiv.org/abs/2611.31535)
**Categories:** Robotics (cs.RO); Computer Vision and Pattern Recognition (cs.CV)

While recent vision-language-action (VLA) models increasingly incorporate 3D geometry, how to effectively exploit it for precise and generalizable action prediction remains a central challenge. We introduce Hi3R-VLA, a 3D policy that grounds heterogeneous modalities - vision, language, and action - in explicit 3D geometry for robotic manipulation. Our model integrates spatially-aligned visual features and language conditioning into point cloud representations, enriching scene geometry with fine-grained, task-relevant semantics. It then anchors low-level control commands in the same 3D coordinate frame and uses 3D-RoPE enhanced action-to-point attention over coarse-to-fine point features to model geometric relationships between action targets and observed points. Our analysis demonstrates the importance of semantic fusion within 3D and spatial alignment between observations and actions. With fewer than 250M trainable parameters, Hi3R-VLA achieves state-of-the-art performance on RoboCasa, RLBench, RoboTwin2, DexJoCo and DexSuite across diverse manipulation tasks and embodiments, from single-arm and dual-arm grippers to dexterous hands. Real-robot evaluations further demonstrate its effectiveness in the physical world. The model, code and dataset are publicly released at this https URL.

---

## 11. Seeing Is Not Reaching: Instruction Shortcuts Override Visual Grounding in Vision-Language-Action Models

**Authors:** Qing Zhang, Xuesong Li, Zhaoyuan Yang, ..., Xinyu Tian, Jing Zhang
**arXiv:** [2611.32206](https://arxiv.org/abs/2611.32206)
**Categories:** Computer Vision and Pattern Recognition (cs.CV); Robotics (cs.RO)

Vision-language-action models (VLAs) are expected to inherit visual grounding from vision-language models, yet often reach for an object's training location after it has been moved. Across six VLAs, we identify two shortcuts: a scene shortcut, where the arm follows the scene's original task despite a new instruction, and an instruction shortcut, where the instruction retrieves the requested object's training location. In $\pi_{0.5}$, the instruction shortcut persists even though object-name attention follows the moved target. We call this Seeing Is Not Reaching. To determine whether this grounding is unused or overridden, we separately mask an image-mediated grounding pathway and a direct instruction-to-action pathway. Masking the grounding pathway eliminates reaches to moved targets, whereas masking the direct pathway increases them. Thus, grounding already guides action but is often overridden by the instruction shortcut, which acts through the direct pathway. We introduce Pathway-Separated Guidance (PSG), which amplifies grounding and suppresses the shortcut without training or external target locations. On LIBERO-PRO Object under Position perturbations, PSG raises the target-reaching rate from 22.0% to 52.6% and task success from 16.6% to 40.8%, while largely preserving performance on the original tasks.

---

## 12. Beyond Expert Replay: Cross-Instruction Anchoring for Continual Vision-Language-Action Learning

**Authors:** Ziyang Chen, Dehua Chen, Shaoguang Wang, ..., Hao Huang, Tao Chen
**arXiv:** [2611.31903](https://arxiv.org/abs/2611.31903)
**Categories:** Computer Vision and Pattern Recognition (cs.CV); Robotics (cs.RO)

Vision-language-action (VLA) models need to continually acquire new manipulation skills while retaining the ability to follow previously learned instructions. Experience replay (ER) can mitigate catastrophic forgetting, but retaining only a small number of historical expert frames per task leaves many old-instruction responses without direct supervision. Under limited replay, we observe a structured failure mode in which an earlier instruction can trigger a subsequently learned, competing goal. To address this gap, we propose Cross-Instruction Anchoring (XIA), which supplements expert replay with instruction-conditioned response preservation. At each task boundary, XIA freezes the previous policy as a teacher and matches its responses to old instructions paired with current observations. This extends supervision beyond stored historical examples without requiring additional expert replay data. Experiments across multiple VLA architectures and three LIBERO suites demonstrate improved success rates and reduced forgetting compared with ER under identical historical expert-data budgets. Additional RoboCasa and real-world experiments further support the effectiveness of XIA.

---

## 13. OmniHarness-RSI: Modality-Aware Harness Evolution for Omnimodal Understanding

**Authors:** Shilin Ma, Xingming Shui, Jinglin Chen, ..., Deyi Zhu, Yansong Tang
**arXiv:** [2611.32951](https://arxiv.org/abs/2611.32951)
**Categories:** Computer Vision and Pattern Recognition (cs.CV)

Recent advances in harness-based recursive self-improvement (RSI) have improved video understanding by evolving executable agent workflows without updating foundation model parameters. However, extending this paradigm to omnimodal understanding remains challenging, as the heterogeneous and interdependent nature of multimodal perception and reasoning creates a complex evolution space, making targeted harness optimization difficult. To address these challenges, we propose OmniHarness-RSI, a modality-aware framework for evolving agent harnesses. Specifically, we factorize the evolution space into three capability dimensions: modality routing and collaboration, modality-aware evidence localization, and modality-specific perception. Based on this factorization, we construct a Factorized-Harness Agent integrating specialized perception experts and audio-video retrieval tools. We further introduce modality-guided harness evolution, which identifies deficiencies through structured modality-capability attribution and refines corresponding harness strategies through interactive code revisions and execution feedback. Validation-guided selection and held-out evaluation assess generalization within and across datasets. Experiments on WorldSense, Daily-Omni, and OmniVideoBench demonstrate test accuracy improvements of 8.86, 8.13, and 6.23 percentage points, respectively, consistently outperforming modality-agnostic RSI. The evolved harnesses also demonstrate cross-dataset transfer without adaptation, while reducing planner calls and viewed frames.

---

## 14. Knocked Off Course: Tracing Uncommanded Motion from Perception to Action in Embodied VLAs

**Authors:** Dan Zlotnikov, Nadav Alali, Ohad Ben-Shahar
**arXiv:** [2611.32705](https://arxiv.org/abs/2611.32705)
**Categories:** Computer Vision and Pattern Recognition (cs.CV)

Vision-Language-Action models (VLAs) enable simultaneous processing of egocentric video and textual target descriptions to produce action commands for embodied tracking platforms. However, these platforms rarely move exactly as commanded, in part due to unexpected environmental disturbances such as wind, unleveled terrain, and road bumps. Here we study how such models handle uncommanded egomotion. First, we explore performance across diverse disturbances by benchmarking three tracking VLAs on three datasets. We find that models differ in which environmental disturbances hurt them most, but all are sensitive to sudden target loss. Tracing egomotion from pixels to emitted actions, we identify two gaps. In representation, motion is reliably recovered through explicit relations between frames, but aggressive compression of past frames weakens small-motion readouts. In action, large rotations do reach the decision state, yet the decoded direction carries only a few percent of a mirrored rotation's effect on the turn. Targeting both gaps, we fine-tune one model, Uni-NaVid, on data amounting to just 1.7% of its original training set in a ladder of analysis-motivated variants. These gain 5-22 points after target-loss without degrading clean success; after a smooth loss, the best one improves success by 72% (relative), recovering 76% of its gap to clean. We also show that targeted fine-tuning improves recovery partly via a text-mediated action dependency, without new architecture, large-scale data collection or training from scratch.

---

## 15. Ground, Guide, Act: Improving VLA Spatial Generalization with Multimodal Foundation Models

**Authors:** Guangting Zheng, Shaoxuan Wang, Yu Yuan, ..., Jiajun Deng, Yanyong Zhang
**arXiv:** [2611.31452](https://arxiv.org/abs/2611.31452)
**Categories:** Computer Vision and Pattern Recognition (cs.CV)

Vision-Language-Action (VLA) models effectively learn action policies from robot demonstrations, but struggle to generalize to changes in object positions and task goals. General multimodal foundation models (MFMs) offer complementary scene understanding and spatial reasoning, but remain slow and unreliable for direct fine-grained control. To understand how MFMs can improve VLA spatial generalization, we conduct a systematic capability analysis across multiple VLA architectures using atomic-stage interventions, revealing that many failures stem from poor target grounding and global spatial routing, while local manipulation skills remain largely usable. Based on these findings, we propose MFM-VLA, a selective collaboration framework in which an MFM provides target grounding and spatial guidance, controllers execute free-space motion, and the VLA retains control over fine-grained manipulation. We fine-tune the VLA with action-chunk-level dense geometric captions and perturbed-state recovery data to improve local guidance following and recovery from unfamiliar handoff states. A development-calibrated capability router selects between direct VLA execution and MFM-assisted execution to avoid unnecessary intervention. Across LIBERO-PRO, ALOHA-Sim-PRO, RoboCasa365, and real-world chemistry tasks, MFM-VLA improves success rates by 14.9, 74.0, 3.6, and 30.9 percentage points, respectively, over the corresponding base VLA. The project page is available at this https URL

---
