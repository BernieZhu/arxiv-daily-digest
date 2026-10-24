# arXiv Daily Digest — 2026-10-23

**Mode:** direct
**Categories:** cs.AI, cs.LG, cs.RO, cs.CV
**Keywords:** VLA, RSI, agentic robot, self-improving robot, self-evolving robot, robot harness
**Papers found:** 7

---

## 1. Measuring the Reasoning-Action Coupling in Driving Vision-Language-Action Models through Counterfactuals

**Authors:** Gabriel Manalu, Saad Wazir, Thao Do, ..., Tolcha Yalew Kidane, Daeyoung Kim
**arXiv:** [2610.30953](https://arxiv.org/abs/2610.30953)
**Categories:** Artificial Intelligence (cs.AI)

Driving vision-language-action (VLA) models bring an appealing form of explainability to a safety-critical domain, since a system that can state the reasons for its maneuvers offers the transparency that deployment and public trust in autonomous driving demand. These models read the world into language before they act on it, describing the scene and reasoning over it in text that ranges from chain-of-thought to multi-stage question answering on the way to a trajectory. That framing quietly assumes two separable properties, namely that the trajectory follows the generated reasoning and that the generated reasoning tracks the causes that actually produce the trajectory. To thoroughly investigate these properties, we apply causal, counterfactual interventions to four driving VLAs across different benchmarks. First, we perturb the models' own reasoning and show that altering its meaning produces small trajectory changes relative to blanking the same models' camera inputs, a pattern that persists across benchmarks and model architectures. We then construct scene-level counterfactuals through photorealistic removal of key objects named in the models' reasoning and analyze whether the generated reasoning and trajectories track these changes. Overall, our findings indicate that the reasoning these models present to account for their resulting driving behavior is weakly coupled to that behavior itself, pointing to limits on the explainability these systems are intended to provide.

---

## 2. FocusVLA: Future-Intent Guided Dynamic View Routing for Vision-Language-Action Models

**Authors:** Huixin Xu, Ziya Yu, Peng Li
**arXiv:** [2610.31423](https://arxiv.org/abs/2610.31423)
**Categories:** Robotics (cs.RO); Artificial Intelligence (cs.AI)

Vision-language-action (VLA) models have become an important paradigm for robotic manipulation by unifying visual perception, language understanding, and action generation. Since reliable manipulation requires sufficient observation of objects, end-effectors, and their spatial relationships, multi-view inputs are widely used to provide complementary spatial information. However, our experiments show that existing VLA models do not fully exploit such multi-view complementarity. The policy tends to persistently rely on the wrist view, lacking the ability to dynamically adjust global-local view dependency across manipulation stages, which limits stage adaptability and robustness. To address this issue, we propose FocusVLA, a stage-aware multi-view routing framework. FocusVLA predicts future interaction intent from historical actions and uses it to guide dynamic view routing during action generation. By adaptively coordinating global and local observations across different task stages, FocusVLA improves multi-view utilization. On RoboTwin 2.0, FocusVLA improves the average success rate over the strongest baseline $\pi_{0.5}$ by 10.10 pp. In real-world evaluation, FocusVLA improves the success rate from 71.7\% to 85.0\%, achieving a 13.3\% gain over $\pi_{0.5}$. Moreover, the intent prediction and dynamic routing modules of FocusVLA can be integrated into existing VLA frameworks without modifying their core architectures.

---

## 3. Progress Probes $P^2$: Lightweight Runtime Monitoring for Vision-Language-Action Models

**Authors:** Atiksh Bhardwaj, Edward W. Duan, Junwon Seo, ..., Andrea Bajscy, Preston Culbertson
**arXiv:** [2610.31613](https://arxiv.org/abs/2610.31613)
**Categories:** Robotics (cs.RO)

Vision-Language-Action (VLA) models can perform diverse manipulation tasks directly from visual observations and natural language instructions, but they remain prone to mistakes and unpredictable failures. Deploying these policies without continuous human supervision will require robust runtime monitors that detect when the policy has gone off-course. Existing monitors use external foundation models, such as vision-language models (VLMs) to supervise the policy, introducing significant complexity and computational cost for monitoring at runtime. In this work, we investigate an alternate approach: \textit{can a VLA's own internal activations provide the information needed to monitor its execution?} Our method trains linear probes on policy activations from demonstrations to estimate progress, then flags executions that deviate from expected progress. In experiments with the open-source VLA $\pi_{0.5}$ and across simulated and real-world manipulation tasks, this approach is competitive with or outperforms VLM-based monitors in task failure detection, as well as methods which require failure data for training. These findings suggest that simple probes of VLA internals can be used to develop reliable runtime monitors, opening a path toward building policies that can act reliably and monitor their execution without external foundation models.

---

## 4. Echo: Coupled Action and Task Status Signal Denoising for Vision Language Action Models

**Authors:** Yufeng Liu, Bohao Fan, Juntu Zhao, ..., Yang Gao, Cheng Ma
**arXiv:** [2610.31569](https://arxiv.org/abs/2610.31569)
**Categories:** Robotics (cs.RO)

Recognizing task completion and failure enables robots to stop upon success and initiate recovery or replanning after failure. Existing methods augment Vision Language Action (VLA) policies with task status signal prediction to support these execution decisions. However, learning and integrating these signals can require fine-grained supervision, external monitoring models, or complex architectural designs. Moreover, the potential of task status signals to directly guide action generation remains underexplored. We present Echo, a framework that combines task status signal learning without frame-level progress annotations with a compact design for status prediction and action generation within a single VLA. Specifically, Echo represents task status with stop and failure signals, added as two dimensions of each action chunk and denoised together with robot actions. Their combination distinguishes ongoing execution, successful completion, and failure. To learn these signals without fine-grained progress annotations, Echo constructs successful, failed, and recovery trajectories with complementary supervision properties. To enable status signal-guided action generation, Echo controls interactions between the signals and actions and denoises the signals faster than the actions. These allow later action denoising steps to condition on cleaner status estimates while preserving accurate signal prediction. Extensive real-world manipulation experiments show that Echo accurately predicts task status and consistently improves policy performance.

---

## 5. FastHarness: Experience-Driven Review Scheduling for Vision-Language-Action Policies

**Authors:** Tao Lin, Yuxin Du, Haoxiao Wang, Zile Zhong, Bo Zhao
**arXiv:** [2610.31427](https://arxiv.org/abs/2610.31427)
**Categories:** Robotics (cs.RO)

Agentic robot systems combine language-model reasoning with robot policies to monitor execution and recover from failures. However, reviewing every action chunk incurs substantial overhead, even in familiar situations. We introduce FastHarness, an experience-driven execution harness that adaptively schedules GPT-6 Astra supervision of a {\pi}0.5 policy. A fast path uses stage memory and reviewed outcomes to reduce review frequency as experience accumulates, while a complementary recovery path focuses supervision on correcting errors. Once recovery is verified, routine execution resumes, with failure experience retained to guide future interventions. The policy remains frozen and generates fresh actions from current observations. Across four simulated manipulation tasks, reviewer token use decreases by an average of 57.2% per task from the first evaluated episode to the mean of the final five episodes. Mean episode time decreases from 85.5 to 52.0 minutes over the same interval. On the same tasks, mean success increases from 80% for GPT-as-Policy ({\pi}0.5 + GPT-6 Astra) to 97.19% with FastHarness. These results highlight adaptive supervision as a practical route to more efficient agentic robotics without additional model training.

---

## 6. HiSTEVE 1.0: Harnessing Human-Interface VLA Agents for Open-World Games

**Authors:** Zecong Tang, Zian Guan, Yuncheng Guo, ..., Yiwen Guo, Bo Dai
**arXiv:** [2610.31162](https://arxiv.org/abs/2610.31162)
**Categories:** Computer Vision and Pattern Recognition (cs.CV)

Building virtual embodied agents that operate in open-ended games like human players is a long-standing goal requiring both long-horizon autonomy and reliable native-interface control. As a procedurally generated open world, Minecraft provides a natural testbed for studying the integration of these capabilities. Existing agents typically provide either native visuomotor control without long-horizon autonomy or high-level planning executed through environment APIs or predefined skills. To bridge this gap, we propose HiSTEVE, a hierarchical VLA agent with a capability-aware agent harness. At the orchestration level, we equip the harness with structured memory for tracking progress and a VLM planner for selecting subtasks within the VLA's capabilities. To reliably determine subtask completion, we further introduce a policy-coupled task completion state detector that conditions on VLA policy context to signal candidate completion. At the control level, a single VLA executes all subtasks with vision-only perception and native keyboard-and-mouse actions. To mitigate interference between heterogeneous GUI and non-GUI interactions, we introduce regime-specific RMSNorm branches and separate mouse-movement token embeddings. We also train the VLA through world knowledge injection, imitation learning, and reinforcement learning with environment feedback to improve reliability and recovery. HiSTEVE achieves state-of-the-art atomic-task performance, scoring 85.0% on MineStudio Bench and a 37.4% average success rate on OpenHA, while also completing long-horizon tasks such as crafting an iron pickaxe from scratch like human players.

---

## 7. SmolVLA-MoE: Sparse Mixture-of-Experts for Efficient Multi-Task Robotic Manipulation

**Authors:** Shiyang Zhang, Miao Yang, Zhengda Li, ..., Hui Peng, Peng Song
**arXiv:** [2610.30732](https://arxiv.org/abs/2610.30732)
**Categories:** Computer Vision and Pattern Recognition (cs.CV)

Vision-Language-Action (VLA) models have shown promising results in multi-task robotic manipulation by leveraging visual and language understanding for action generation. However, existing lightweight VLA models employ a single dense action expert to handle all tasks, which limits their multi-task capability under constrained computational budgets. To address this issue, we propose SmolVLA-MoE, a novel framework that introduces sparse Mixture-of-Experts (MoE) into the FFN layers of the action expert in VLA models. SmolVLA-MoE replaces dense FFN layers with multiple parallel expert FFNs and a token-level router, enabling each token to adaptively select the most suitable expert for action generation. We further introduce a shared expert with a tunable weight parameter to balance the inheritance of pre-trained capabilities and task-specific expert specialization. Through sparse activation, SmolVLA-MoE activates only a single expert FFN during inference, with a total activated parameter count of approximately 500M including the frozen VLM backbone, while benefiting from approximately 800M total stored parameters. We evaluate our method on four task suites of the LIBERO benchmark. SmolVLA-MoE achieves an average success rate of 84.25%, outperforming SmolVLA (82.75%) and OpenVLA-7B (76.5%), while maintaining comparable inference efficiency. Our code is publicly available at this https URL.

---
