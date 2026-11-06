# arXiv Daily Digest — 2026-10-21

**Mode:** direct
**Categories:** cs.AI, cs.LG, cs.RO, cs.CV
**Keywords:** VLA, RSI, agentic robot, self-improving robot, self-evolving robot, robot harness
**Papers found:** 12

---

## 1. MaD-RSI: Model-as-Data for Recursive Self-Improvement of Agent Harnesses

**Authors:** Yu Cui, Hong He, Ruiqing Yue, ..., Haibin Zhang, Cong Zuo
**arXiv:** [2610.28201](https://arxiv.org/abs/2610.28201)
**Categories:** Artificial Intelligence (cs.AI)

Recursive self-improvement (RSI) of agent harnesses has emerged as an effective approach to enhancing the capabilities of large language model (LLM) agents. By searching the harness space for a specific LLM on a given dataset, RSI can discover a harness tailored to the capabilities and behavioral characteristics of that model. However, such optimization often creates a strong coupling between the learned harness and its target LLM, limiting generalization across models and requiring substantial computational resources to adapt to new LLMs. Moreover, existing RSI methods typically optimize a harness using feedback from a single model and evaluate its generalization to other models only after training. This paradigm treats model differences primarily as a criterion for evaluating generalization rather than as valuable evidence for optimization. In this paper, we introduce a new perspective that treats models as data and places the harness at the center of optimization. Building on this perspective, we propose \textsc{MaD-RSI}, a framework that directly optimizes a shared harness across multiple heterogeneous LLMs by incorporating their diverse failure trajectories into the training process. Rather than assessing model differences only after optimization, \textsc{MaD-RSI} leverages these differences as training evidence to guide the self-improvement of a shared harness. Furthermore, we introduce a new evaluation framework with two complementary metrics designed to assess the effectiveness of harness optimization across models. Experiments across multiple datasets and LLMs demonstrate that \textsc{MaD-RSI} improves generalization over existing approaches while reducing training costs.

---

## 2. RSI Control: Can AI Models Perform Covert Sabotage in the Self-Improvement Process?

**Authors:** Kaiwen Zhou, Udari Madhushani Sehwag
**arXiv:** [2610.27735](https://arxiv.org/abs/2610.27735)
**Categories:** Artificial Intelligence (cs.AI)

Recursive self-improvement, in which frontier AI models work on training the next generation, is quickly becoming a reality. However, the safety of this process has received far less attention than it should. A misaligned model training its successor can shape what that successor knows, how it behaves, and what it wants, and the harm carries forward into the next generation. We study this risk through the lens of AI control. We introduce RSI Control Arena, a testbed in which a frontier model, acting as an autonomous R\&D agent, is given a benign main task from a stage of a successor model's training pipeline together with a covert side task to install a misaligned property in the successor. The testbed contains 16 side tasks in three classes, forming 22 task pairs with main tasks that span the pipeline from data curation to reinforcement learning. We evaluate six frontier models as agents against LLM monitors that read the transcript of the run and the agent's reasoning. We observe that every model completes a substantial share of the side tasks without degrading the main-task performance, including side tasks that make the successor itself a better saboteur. Under minimal instructions to stay covert, models already produce successful attacks that monitors fail to detect, and providing a short list of evasion tactics further reduces the detection rate. Monitors with access to agent's reasoning detects most attacks, but not all. Our results indicate that recursive self-improvement raises significant safety concerns, and that strong safety effort should be in place before models are trusted with greater responsibility of training their successors.

---

## 3. Perceives but Doesn't Brake: A Perception-Action Binding Gap in Reasoning Driving VLAs

**Authors:** Matteo Cercola, Katie Z Luo, Simone Formentin, Marco Pavone
**arXiv:** [2610.28184](https://arxiv.org/abs/2610.28184)
**Categories:** Robotics (cs.RO); Artificial Intelligence (cs.AI)

Reasoning-augmented vision-language-action (VLA) driving models can perceive and reason about safety-critical hazards yet fail to translate that evidence into safe actions. We characterize this failure as a perception-action binding gap: hazard information is available inside the model but exerts insufficient control over trajectory generation. Using matched simulated counterfactuals and logged driving replay, we show that in-path hazards are actually encoded in the visual representation, but longitudinal plans are dominated by ego-speed history and respond only weakly to hazard proximity or the model's own reasoning trace. Further analysis shows that the trajectory generator is capable of braking but sometimes fails to do so due to the perception-action binding gap. Without retraining or modifying any weights, we inject a hazard-conditioned energy into the frozen flow-matching sampler of Alpamayo-1.5, restoring the missing coupling at generation time. With exact obstacle geometry, guidance cuts footprint intrusion from 58.1% to 14.5% and recovers safe braking whenever sufficient stopping distance remains, eliminating collisions entirely in our braking-relevant closed-loop battery. It also reverses the diagnosed dependence of the plan, from tracking ego speed to responding to obstacle range. These results separate hazard perception from hazard control in driving VLAs, show that unsafe behavior can arise even when the model has both the evidence and the ability to act on it, and propose a simple fix for bridging this binding gap.

---

## 4. VLA-Retain: Benchmarking Cross-Dimension Effects of Vision Tuning in VLAs

**Authors:** Borui Xu, Han Chen, Bingsheng He, ..., Jason Zeng, Michael Heinrich
**arXiv:** [2610.27698](https://arxiv.org/abs/2610.27698)
**Categories:** Computer Vision and Pattern Recognition (cs.CV); Artificial Intelligence (cs.AI)

Vision-language-action (VLA) models transfer knowledge from large-scale pretraining into robot control, but their manipulation performance remains sensitive to changes in observation conditions, which recent work addresses by fine-tuning the visual module on target-domain data. However, it remains unclear how such adaptation affects robustness beyond the target condition, as existing robustness benchmarks only evaluate models without fine-tuning and adaptation studies only report the target gain. Measuring this cross-dimension effect requires separating target gains from off-target changes, isolating adaptation effects from architectural differences, ruling out generic forgetting, and comparing tuning choices. Therefore, we introduce VLA-Retain, a benchmark that compares five open VLA models, tuned on Camera-view or Sensor-noise data, with their own base checkpoints on LIBERO-Plus dataset spanning seven perturbation dimensions. Our study reveals four findings. First, targeted vision tuning is not local, and its target gain does not predict retention. Mean off-target gain is negative in 8 of 10 model--domain configurations. Under Camera-view tuning, X-VLA gains $69.4$ percentage points on the target but loses $4.6$ points on average elsewhere, whereas OpenVLA-OFT gains $39.3$ and $1.4$ points, respectively. Second, these regressions are not explained only by performance loss on the same tasks without perturbations. Third, broader training coverage raises overall gain over target-specific training but does not eliminate dimension-level regressions. Fourth, tuning strategies are model-dependent, as DELTA-style feature preservation raises X-VLA's mean off-target gain to $+1.2$ points but lowers OpenVLA-OFT's to $-23.1$. Overall, these findings show that target-domain success alone is insufficient and highlight cross-dimensional retention as a key criterion for targeted VLA adaptation.

---

## 5. Auditing the Product, Not the Recursion: The Evaluation Evidence Behind Recursive Self-Improvement Claims

**Authors:** Zihan Chen, Di Zhu, Lei Nico Zheng
**arXiv:** [2610.27610](https://arxiv.org/abs/2610.27610)
**Categories:** Machine Learning (cs.LG); Artificial Intelligence (cs.AI); Computation and Language (cs.CL); Software Engineering (cs.SE)

Recursive self-improvement (RSI) promises AI systems, such as self-evolving LLM agents, that become better at producing further improvements. Evaluating this promise requires separating product claims about the final system from process claims about the improvement process itself. Existing surveys specify the evidence these claims require, but how often studies report that evidence remains unmeasured. We examine this question through full-text coding of 114 eligible studies in a reproducible arXiv search frame frozen in October 2026, including 90 that describe their own systems as RSI. The codebook links claims to evaluation designs. Independent human coding, third-reader adjudication, and a separate blind coding of improver comparisons assess coding reliability. Among the 90 RSI studies, 90% report product evaluation beyond development tasks under a broad criterion that includes partial or unstated separation, while 60% report evaluation on tasks unused for selection. Only 22% audit two or more reruns of the full loop. In a human-coded random sample, the RSI studies show the same contrast: 45% evaluate on tasks unused for selection and 14% audit two or more reruns. Of the 26 studies claiming a better improvement procedure, 23 report a related comparison, but only 4 compare earlier and later procedures from identical starting artifacts at a matched budget. Across these results and a comparison set of established works, evidence for repeatability and improved procedures remains less developed than product evaluation. Three propositions explain how selection effects, shared evaluator errors, and changes in system state limit what product evaluations can establish. Together, the findings support a claim-indexed reporting standard that connects each claim to the evaluation design needed to test it.

---

## 6. What Would Removing This Corruption Change? Failure Attribution for Vision-Language-Action Models

**Authors:** Carson Sobolewski, Anjali Parashar, Fei Chen, Yingke Li, Chuchu Fan
**arXiv:** [2610.27277](https://arxiv.org/abs/2610.27277)
**Categories:** Robotics (cs.RO); Machine Learning (cs.LG)

Vision-language-action (VLA) models are sensitive to visual corruptions, but knowing that a corruption is typically harmful does not establish whether removing it would benefit the current episode. Furthermore, when several corruptions co-occur, deciding what to correct requires understanding which ones contribute to failure risk and how much their removal would help. We define this problem as failure attribution. Detecting corruption presence alone cannot answer this question, as corruptions can be present but relatively harmless, while directly measuring removal benefits requires costly paired policy rollouts with and without the corruption present. To address this, we introduce a factorized risk model that learns separate representations of the scene and corruptions, allowing us to estimate removal benefits through latent intervention from the current image and task instruction, without paired clean images or additional counterfactual rollouts. We evaluate our approach on OpenVLA and $\pi_{0.5}$ in simulation and $\pi_{0.5}$-DROID on a Franka robot. Our method outperforms monolithic and vision-language-model (VLM) baselines, including achieving approximately 3x lower attribution error than frontier VLMs. We also demonstrate our method adapts to execution context and corruption intensity, and can be used for online failure monitoring on hardware.

---

## 7. AgenticRoboRL: Bringing Coding-Agent Post-Training to Agentic Robotics

**Authors:** Xinxin Liu, Bingxin Xu, Wenrui Bao, ..., Chen Chen, Yuzhang Shang
**arXiv:** [2610.28589](https://arxiv.org/abs/2610.28589)
**Categories:** Robotics (cs.RO)

Agentic robotics systems combine planners with robot harnesses to perform complex manipulation tasks. Recent work improves these systems through better harnesses and external memory, but relies on powerful closed-source models as planners and does not improve the planners' own capabilities. In contrast, coding agents have improved substantially by post-training the model itself. We therefore investigate whether post-training can also improve robot planners. However, applying it across robot harnesses requires accommodating different execution mechanisms, including VLA skill invocation and control-code generation. To this end, we introduce AgenticRoboRL, a framework for post-training robot planners across different harnesses. The training recipe combines supervised fine-tuning with multi-turn reinforcement learning. To accommodate different execution mechanisms, harness-specific adapters connect recorded planner interactions with task outcomes, enabling a common RL training pipeline while keeping execution components fixed. On LIBERO-PRO, AgenticRoboRL raises the success rate of a 9B-parameter planner from 18.1% to 71.0% without external memory, approaching the 72.1% achieved by Codex (GPT-5.5) with external memory. These results demonstrate post-training as an effective approach for improving robot planners. We will release the framework and trained planner checkpoints.

---

## 8. Reasoning as a Distribution: Generative Plan Latents for Vision-Language-Action Models

**Authors:** Matteo Cercola, Katie Z Luo, Milan Ganai, ..., Simone Formentin, Marco Pavone
**arXiv:** [2610.28166](https://arxiv.org/abs/2610.28166)
**Categories:** Robotics (cs.RO)

Vision-Language-Action (VLA) policies increasingly reason before acting, but existing reasoning models compress this intermediate decision into a single representation. When several plans are valid, this commitment hides alternatives that could otherwise be selected or revised. We introduce the Generative Plan Latent (GPL), which represents the reasoning state as a low-dimensional conditional distribution over plans, such as which object, grasp, or route to use. This makes the reasoning state addressable: without retraining the VLA, plans can be sampled (coverage), selected on request (steering), and reweighted by deployment outcomes (outcome adaptation). We test all three on SimplerEnv manipulation with $\pi_0$, and extend the analysis to RoboCasa, LIBERO, and a maze domain. Steering the plan raises the fraction of executions that follow the request from 0.48 to 0.94, while the same guidance on the native action distribution shows no reliable gain. Finally, we show that an explicit plan is most useful when it carries decision information not already determined by the observation.

---

## 9. FIT-MAC: A Closed-Loop Multi-Agent Framework for Robust Vision-Language-Action Models

**Authors:** Jiatong Li, Jisheng Dang, Qiangqiang Ma, ..., Hong Peng, Bin Hu
**arXiv:** [2610.28109](https://arxiv.org/abs/2610.28109)
**Categories:** Robotics (cs.RO)

Vision-language-action (VLA) models have achieved strong performance on standard robotic manipulation benchmarks. However, their reliability can degrade substantially when task conditions deviate from the nominal setting. Perturbations in object positions and task instructions may lead to complete task failure. Existing VLA policies generally lack an explicit runtime mechanism for distinguishing these failure modes and selecting an appropriate recovery strategy. To systematically mitigate this issue, we propose FIT-MAC, a failure-aware, closed-loop multi-agent control framework for improving the robustness of VLA policies at inference time. FIT-MAC augments a VLA policy with an inference-time control layer. First, the Planner Agent parses the language instruction into a structured task specification that captures the manipulation goal and spatial constraints, and the Grounder Agent resolves each instruction-level reference to a visual target. Next, the Verifier Agent tracks phase-specific execution progress, distinguishes target-binding errors from local execution failures, and determines whether intervention is warranted. The Correction Agent then routes permitted interventions to target rebinding or bounded grasping or placement recovery, depending on the failure type. When no intervention is required, the pretrained VLA remains the default action generator. Extensive experiments on LIBERO-PRO demonstrate that FIT-MAC improves robustness across multiple VLA backbones, consistently increasing success rates and achieving state-of-the-art performance under diverse perturbations.

---

## 10. PACT-VLA: Speculative Action-Chunk Verification with Pre-Commit Observations

**Authors:** Yixiang Zhu, Ruilong Wu, Yonghao Chen, ..., Yusong Hu, Xinyu Chen
**arXiv:** [2610.28019](https://arxiv.org/abs/2610.28019)
**Categories:** Robotics (cs.RO)

Vision-language-action (VLA) policies are commonly deployed with asynchronous inference in real-world settings, where the next action chunk is generated while the robot is still executing the previous one. By the time the new chunk is committed, the robot and scene have changed, so the chunk is conditioned on a stale observation and task success drops sharply as this inference delay grows. Generating multiple candidate chunks could let newer observations inform the final choice, but existing multi-candidate methods either rank candidates with the stale inference-start observation or repeatedly switch between candidates during execution, which can make the executed action sequence discontinuous. Our key insight is that inference delay can be used as decision time. While candidate generation is still underway, candidate selection can reuse the VLA itself to choose the complete action chunk that best fits a later observation. We propose PACT-VLA, a training-free framework that generates candidates from the inference-start observation and selects one using this pre-commit observation. Its scoring function, FlowRes, measures the residual between each candidate's implied flow direction and the velocity predicted by the frozen policy under the pre-commit observation, requiring no separate verifier. A pipelined implementation overlaps observation processing with candidate generation and batches scoring, so selection adds no control-step delay on the evaluated hardware. At a four-step delay, PACT-VLA improves average success by 15.0 percentage points over RTC on Kinetix and by 5.2 points over single-candidate asynchronous execution with GR00T N1.7 on LIBERO, and it further improves existing delay-robust methods. On three real-robot tasks, it raises average success from 60% to 82% over naive asynchronous execution with the same frozen $\pi_{0.5}$ checkpoint.

---

## 11. RoboCasa-Shift: Stage-Aware Robustness Evaluation of Vision-Language-Action Policies in Long-Horizon Household Manipulation

**Authors:** Haocheng Wang, Youquan Liu, Weiyu Guo, ..., Weidong Yang, Ben Fei
**arXiv:** [2610.27861](https://arxiv.org/abs/2610.27861)
**Categories:** Robotics (cs.RO)

Vision-language-action (VLA) robustness is commonly summarized by aggregate task success, which obscures how individual executions change under distribution shifts and where failures emerge in long-horizon tasks. We introduce \textbf{RoboCasa-Shift}, a diagnostic robustness benchmark built on RoboCasa365 that combines controlled single-factor shifts, matched clean-perturbed rollouts in which each pair shares the same underlying settings and differs only in the target shift, and simulator-grounded stage-aware diagnostics. We evaluate GR00T N1.5 on four long-horizon tasks that pass a predefined clean-performance gate under four perturbation factors and three calibrated severity levels, including conditions that drive the evaluated policy to complete task failure, totaling 1,040 formal rollouts. Robustness responses vary substantially across factors and tasks, and increasing severity does not always produce monotonic degradation. For example, one camera condition yields $\Delta\mathrm{SR}=0$ despite 8 of 80 matched episodes changing outcome. Stage-aware analysis further shows that the same end-to-end degradation can correspond to different execution-depth profiles. Camera $L_2$ and Gaussian blur $L_1$ both yield $\Delta\mathrm{SR}=0.188$, yet their first-stage failure rates are 19.0\% and 36.4\%, respectively. Our findings suggest that VLA robustness should be viewed as a multi-dimensional property of execution rather than a single end-to-end performance measure, motivating evaluation protocols that jointly capture outcome degradation, paired outcome sensitivity, and failure progression. The code is publicly available at this https URL.

---

## 12. Embodied Playground: A Long-Horizon Agentic Robotics Benchmark for Physical, Strategic, and Spatial Reasoning

**Authors:** Feng Chen, Pei Zhou, Lixuan He, ..., Kaichen Zhou, Yi Ma
**arXiv:** [2610.27039](https://arxiv.org/abs/2610.27039)
**Categories:** Robotics (cs.RO)

Foundation models offer a promising basis for robotic agents, but long-horizon tasks require them to sustain coherent reasoning and reliable physical execution across interdependent stages. We introduce Embodied Playground, a benchmark for evaluating how foundation-model agents coordinate physical, strategic, and spatial reasoning throughout such tasks. Agents must track task progress, satisfy intermediate constraints, and revise their plans using execution feedback as earlier actions shape subsequent decisions. The playground comprises 410 task environments spanning basic manipulation, sequential puzzles, and multi-stage household activities, with variations in planning depth, geometric constraints, and physical execution demands. We curate EP-100, a representative selection of 100 tasks across five suites and 16 task types, together with the EP-Easy and EP-Hard difficulty splits and the compact EP-20 selection. A shared protocol specifies observation and tool access, resource budgets, repeated trials, and independent checks of goal completion, task-rule compliance, and physical validity. Embodied Playground provides a unified framework for studying whether foundation-model agents can sustain effective reasoning and action over extended task horizons. this https URL

---
