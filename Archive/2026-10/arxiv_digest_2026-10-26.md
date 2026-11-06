# arXiv Daily Digest — 2026-10-26

**Mode:** direct
**Categories:** cs.AI, cs.LG, cs.RO, cs.CV
**Keywords:** VLA, RSI, agentic robot, self-improving robot, self-evolving robot, robot harness
**Papers found:** 13

---

## 1. HarnessMM: Recursive Self-Improvement for Harness Token Efficiency

**Authors:** Yuhua Jiang, Chang Xu, Feifei Gao, Li Zhao
**arXiv:** [2610.32813](https://arxiv.org/abs/2610.32813)
**Categories:** Artificial Intelligence (cs.AI)

Agent harnesses repeatedly invoke reasoning after tool feedback, even when an earlier call has already fixed the next action. We introduce HarnessMM (Harness Minus Minus), a method for improving harness token efficiency through guarded decision reuse and recursive self-improvement (RSI). RSI iteratively refines companion harness configurations from training feedback, with validation selecting the configuration for deployment. A controller at the model-tool boundary reuses resolved decisions to replace later reasoning callbacks while actor weights remain fixed. Executable Decision Graphs store exact actions, literal arguments, causal dependencies, and public guards. Guarded Decision Reuse activates these persistent decisions from observed receipts; Certified Callback Substitution executes them through the native interface and records removal of the registered slow callback. New semantic decisions, unsupported evidence, and selector abstention invoke the original actor again. The representation restricts what feedback may change, while complete-task measurements establish quality and cost. On HumanEval, HarnessMM preserves Codex success at 90.82\% while reducing Tokens/task (k) from 66.72 to 47.02 (29.54\% saving). For DeepSeek Harness, success rises from 71.43\% to 85.71\% while Tokens/task (k) fall from 96.28 to 11.62 (87.93\% saving). A separate MBPP ablation measures 26.91\% lower cost than single-use graphs and 19.52\% lower cost than retained callbacks. These results establish guarded decision reuse as a practical way to reduce repeated reasoning in existing harnesses.

---

## 2. When to Stop Penalizing Actions? Martingale GRPO for VLA Reinforcement Learning

**Authors:** Zongyao Zhao, Cheng-Jie Zhao, Ruihang Jiang, ..., Zhaolin Wang, Yuanwei Liu
**arXiv:** [2610.32431](https://arxiv.org/abs/2610.32431)
**Categories:** Artificial Intelligence (cs.AI)

A failed vision-language-action (VLA) rollout does not imply that every action contributed to failure. Yet in group-relative policy optimization (GRPO), a single trajectory-level advantage is assigned to all actions in a rollout. Potentially useful recovery attempts can thus be penalized alongside the errors they aim to correct. Ideal stopping conditions for failure feedback are characterized using success-probability and policy-score martingales. At these stops, the removed gradient contribution has zero conditional expectation given the retained information. Truncation therefore preserves the expectation of a reference GRPO group-gradient estimator and can reduce its covariance. One such stop occurs when the conditional probability of success is zero, motivating error and recovery cues for selecting candidate feedback boundaries. Martingale GRPO (MART-GRPO) is introduced with a vision-language model (VLM) for event-guided truncation. The VLM is fine-tuned on our annotated training set using low-rank adaptation (LoRA). The last visible error without observed recovery is localized by the frozen VLM in complete rollout videos. Failure feedback is retained through the selected error interval and removed afterward, while successful-rollout loss terms and original loss normalization are preserved. For retrospective boundaries, changes in expectation and variance are analyzed to assess departures from ideal stopping. Experiments with OpenVLA-OFT on RoboTwin 2.0 show that MART-GRPO improves success rates over full-trajectory GRPO across multiple tasks.

---

## 3. RSIHub: A Composable Framework for Agent-Evolution Methods

**Authors:** Zimu Wang, Xiaobo Wang, Siyu Ye, ..., Xiaodong Gu, Zilong Zheng
**arXiv:** [2610.32253](https://arxiv.org/abs/2610.32253)
**Categories:** Artificial Intelligence (cs.AI)

Agent-evolution methods use execution feedback to improve prompts, skills, tools, and orchestration, but their implementations often rebuild the same experimental machinery. We present RSIHub, an open-source framework for building, comparing, and extending these methods on shared infrastructure. Recipes compose reusable operators and declare mutable resources; RSIHub supplies execution, evaluation, recovery, and lineage. Researchers can focus on evolution policy while evaluation stays outside the mutable surface and results remain tied to candidates and evaluation conditions. We instantiate AHE, Hyperagents, A-Evolve, and GEPA without modifying the framework core, keeping method-specific logic in recipes and operators. We evaluate them with MiniSWE and Codex on Terminal Bench 2 and $\tau^3$ Banking under fixed model and evaluator configurations. The largest observed overall pass@1 gain is 13.5 percentage points, while method rankings vary across settings and optimization gains do not always transfer to held-out tasks. RSIHub provides a common protocol for comparing evolution policies, inspectable candidate histories, and reusable components for developing new methods.

---

## 4. RSI-Opt: Recursive Self-Improvement Optimizer Agents For Model Training

**Authors:** Binghang Lu, Yige Sun, Guang Lin
**arXiv:** [2610.32026](https://arxiv.org/abs/2610.32026)
**Categories:** Artificial Intelligence (cs.AI)

Conventional neural-network training typically follows a predefined optimization recipe, motivating a LLM agent that monitors training dynamics and adjusts optimizer settings as training progresses, but a fixed agent policy does not accumulate experience across runs. We introduce RSI-Opt, a plug-and-play Recursive Self-Improvement Optimizer Agents which evolves the knowledge that guides this process: a prompt, a playbook of procedures, a library of tested optimizer code, and a decision cadence. A meta-agent rewrites this policy using evidence from earlier runs, and an archive retains evaluated policies for further evolution. Across 5 generations on three training tasks, the meta-agents develop reusable procedures and code and conduct their own CPU proxy experiments. RSI-Opt substantially improves optimizer-agent performance, with representative raw-space summary $z$-scores increasing from $+10.48$ to $+14.33$ on the evolution suite with Opus 5.5 and from $-0.36$ to $+3.11$ on held-out tasks with GPT-5.5 through cross-model policy transfer. On the Burgers PDE, it reduces mean relative $L_2$ error by approximately 2.7-fold with Opus 5.5 and 8.8-fold with GPT-6.1 over the fixed-prompt agent baseline, although PDE transfer varies across LLMs and tasks. Controlled comparisons show that the evolved policy combines reusable optimization knowledge with adaptation to each task: initial decisions capture most observed gains on seen tasks, while continued adaptation improves outcomes on unseen tasks. These findings demonstrate how procedures and executable tools accumulated across training runs can improve optimizer-agent performance and support transfer to scientific machine learning.

---

## 5. Do VLAs Know They Will Fail? Interpretable Success and Failure Patterns in Physical AI Systems

**Authors:** Christian A. Rogers, Qian Lin, Daniel S. Brown
**arXiv:** [2610.32208](https://arxiv.org/abs/2610.32208)
**Categories:** Robotics (cs.RO); Artificial Intelligence (cs.AI); Machine Learning (cs.LG)

Vision-Language-Action (VLA) models have emerged as powerful general-purpose robot policies, but their successes and failures remain difficult to diagnose and understand. In this work, we show that sparse autoencoder (SAE) representations of OpenVLA activations contain outcome-predictive information and can be used to predict task failure before the robot reaches an unrecoverable state. Moreover, to provide insights into what common behaviors may contribute to these outcomes, we identify individual SAE features whose strong activations are associated with specific stages of success or failure, and uncover recurring behavioral patterns by localizing temporal intervals where these features exhibit significant activation changes. We further develop a VLM-based interpretation pipeline to generate behavioral descriptions of these patterns and validate their correspondence to feature activations on held-out intervals.

---

## 6. ImageRSI: Verification-Driven Recursive Self-Improvement for Agentic Image Generation

**Authors:** Shuo Han, Zhilin Wang, Peng Ling, ..., Yukun Cao, Xike Xie
**arXiv:** [2610.32120](https://arxiv.org/abs/2610.32120)
**Categories:** Computer Vision and Pattern Recognition (cs.CV); Artificial Intelligence (cs.AI)

Complex text-to-image requests remain difficult to satisfy reliably. Verifying and repairing an image can fix an individual output, but a successful repair does not necessarily carry over to other requests. We present ImageRSI, a framework that keeps the image generator frozen and combines three components: five-dimensional verification and repair within each task, an experience library shared across tasks, and offline updating of the judge. Candidate experiences enter the library only after paired A/B validation, and the judge is updated with supervised fine-tuning and GRPO on accumulated image-judgment records and evaluated before reuse. We also introduce ImageReq-Bench, a benchmark of 961 requests built around hard cases in real-world image-generation requests, each paired with an evaluation checklist. ImageRSI achieves a Checklist Strict Accuracy (CSA) of 52.6% on MindBench (with Nano Banana Pro as the generator) and 65.66% on ImageReq-Bench, and we compare system outcomes across judge-training configurations.

---

## 7. TTT in VLA Models: Exploring Training with Human Demonstrations

**Authors:** Qiangong Zhou, Jiafeng Liang, Yimin Dong, Yang He, Hongxiang Li
**arXiv:** [2610.32094](https://arxiv.org/abs/2610.32094)
**Categories:** Robotics (cs.RO); Artificial Intelligence (cs.AI); Computer Vision and Pattern Recognition (cs.CV)

Long-horizon robot tasks require retaining and using past information. We integrate Test-Time Training (TTT), which stores context in fast weights, into InternVLA-A1 and Pi0.5 to study action generation conditioned on human demonstrations through training on paired demonstrations and robot trajectories. We implement memory transfer between the two phases and truncated backpropagation, and examine training objectives, gradient coverage, and contrastive regularization across video, short-video, and single-frame cue tasks. In our experiments, adding TTT and training on paired data at the current scale did not lead to consistent target selection based on demonstrations. Under the tested settings, shorter sequences, full trajectory gradient connectivity, and contrastive regularization did not clearly improve responsiveness to demonstrations. When demonstrations were reduced to single-frame cues, real-robot execution still showed a preference for cups at fixed positions. We document the implementation, training configurations, and observations to support further inspection and replication.

---

## 8. If at First You Don't Succeed, Backtrack: Lightweight Recovery for Frozen VLAs

**Authors:** Thomas Landeg, Thierry Tambe
**arXiv:** [2610.32941](https://arxiv.org/abs/2610.32941)
**Categories:** Robotics (cs.RO); Machine Learning (cs.LG)

Vision-Language-Action (VLA) models perform well on robotic manipulation, yet remain brittle once their own actions carry them into states their training data barely covers. Recovering from such failures usually requires recovery demonstrations, policy retraining, or a separate model at inference time. We introduce Backtrack, a lightweight failure detection and recovery mechanism for frozen VLAs that needs none of these. A small failure prediction head, trained only on outcome-labeled rollouts of the frozen policy, reads the VLA's existing internal representations to estimate whether the current episode will fail. When the predicted failure probability exceeds a threshold, a controller pauses the policy, retraces the arm's recently achieved motion, and hands control back to the unchanged policy so it can retry from an earlier configuration. The head adds only 0.48-0.88% to the policy's parameter count. We evaluate Backtrack on LIBERO with three VLAs spanning two action-generation families: SmolVLA and $\pi$0.5, which use flow-matching action experts, and the autoregressive $\pi$0-FAST. On LIBERO-Long, the suite of long-horizon multi-step tasks and the one on which all three policies fail most often, Backtrack reduces each policy's failure rate by 19-48%, raising success by up to 7.4 percentage points; on the three shorter suites, where control success is already 85-99%, its effect is smaller. On MetaWorld, all twelve controller configurations tested with SmolVLA improve on the unassisted policy.

---

## 9. When Human Corrections Travel: Safety in Federated VLA Adaptation

**Authors:** Vigneshwaran Subbaraju, Obaidullah Zaland, Monowar Bhuyan
**arXiv:** [2610.32888](https://arxiv.org/abs/2610.32888)
**Categories:** Robotics (cs.RO); Machine Learning (cs.LG)

Vision-language-action (VLA) policies can adapt to local human intervention, while federated learning can combine distributed robot experience without pooling raw records. We examine their prospective intersection: sharing adaptations derived from diverse human corrections across tasks, environments, people, and robot embodiments. Corrections differ in modality, safety semantics(urgency, behavioral scope, etc.), and privacy sensitivity. A shared update that improves mean task success may suppress a rare safety intervention or produce an unsafe response on another robot. We argue for three requirements: preserve the context and uncertainty of multimodal corrections when deciding what to share; assess candidate updates in each receiving robot's closed loop before deployment; and evaluate leakage alongside retention of safety-critical evidence. Immediate, legible defensive behavior remains necessary during human interaction. We offer counterexamples and a falsifiable evaluation agenda, not experimental results.

---

## 10. MAST-VLA: Skill-Conditioned Adaptation with Trajectory-Affordance Priors for Multi-Skill Robot Manipulation

**Authors:** Jiachi Yang, Zhiyi Xu, Hongquan Zhang, ..., Jingyu Gong, Yuan Xie
**arXiv:** [2610.32312](https://arxiv.org/abs/2610.32312)
**Categories:** Robotics (cs.RO)

Generalist robot manipulation requires a single vision-language-action (VLA) policy to execute diverse skills across scenes and instructions. However, current multi-skill VLA policies often leave two aspects of an instruction insufficiently modeled: which primitive skill to execute and where/how to contact and move objects. We propose MAST-VLA (Multi-skill Adaptation with Skill-conditioned experts and Trajectory-affordance priors), a dual-conditioning framework for robot manipulation. MAST-VLA introduces skill-conditioned LoRA Mixture-of-Experts (LoRA-MoE) adapters in the LLM backbone, where skill-query tokens and routing biases guide low-rank expert specialization, and converts a predicted affordance heatmap into a patch-level trajectory-affordance spatial prior for the action head. On the CALVIN ABC$\rightarrow$D long-horizon multi-skill cross-scene generalization setting, MAST-VLA achieves state-of-the-art performance, reaching an Avg. Len of 4.65 over five-subtask evaluation sequences. Real-robot multi-skill sequence experiments further validate its deployability under real perception and control noise.

---

## 11. From Tabletop to Walking Bot: Deploying a VLA Model on a Legged Manipulator Robot

**Authors:** Giovanni Minelli, Antonio Langella, Giovanni B. Dessy, ..., Victor Barasuol, Claudio Semini
**arXiv:** [2610.32271](https://arxiv.org/abs/2610.32271)
**Categories:** Robotics (cs.RO)

Vision-language-action (VLA) models are typically pretrained on broad, diverse datasets and subsequently fine-tuned on a comparatively small dataset tailored to a specific target robot. Such adaptation recipe is now widely established, achieving its most mature results on fixed-base arms due to their static base dynamics and consistent reference frame. Mounting the same arm on a quadruped extends the workspace to the entire floor, but fundamentally changes the embodiment: rather than controlling the arm in isolation, the policy must jointly coordinate base navigation, body posture, and end-effector motion. In this work, we study the practical demands of this embodiment change across data collection, model adaptation, and inference design to achieve closed-loop loco-manipulation on a Unitree Go2 with an AgileX Piper arm. We report the choices that made this real-robot deployment feasible, namely model variant, action horizon, and demonstration conventions, together with a study tailored to a pick-and-place task, separating data coverage from model capacity. We show that expanding demonstration coverage reduces held-out end-effector error by 30%, and incorporating secondary skills (such as pushing rather than grasping) introduces new behavioral modes without degrading baseline performance. Finally, closed-loop real-world experiments show how dataset composition shapes success and failure, validating the pipeline for more complex loco-manipulation.

---

## 12. Coupling Execution Horizon and Sampling Depth in Flow-Matching VLA Policies

**Authors:** Jiabing Yang, Yuan Xu, Yixiang Chen, ..., Yan Huang, Liang Wang
**arXiv:** [2610.32102](https://arxiv.org/abs/2610.32102)
**Categories:** Robotics (cs.RO)

Flow-matching Vision-Language-Action (VLA) models generate expressive continuous trajectories for robotic manipulation, yet balancing real-time responsiveness with execution stability remains a persistent challenge. Standard deployment workflows typically treat numerical solver depth and execution horizon as decoupled choices. The horizon amortizes inference latency, while solver depth is kept high to preserve integration fidelity. In this paper, we reveal a fundamental compute-execution coupling in flow-matching VLAs governed by a systematic sign reversal. While coarse numerical integration degrades precision under rapid replanning, it markedly improves task performance under extended open-loop commitment. Geometrically, numerical truncation contracts lateral action dispersion around an invariant trajectory centroid, serving as an implicit regularizer that suppresses compounding open-loop drift. Across LIBERO, RoboTwin 2.0, and real-world Franka manipulation on representative VLA backbones including $\pi_0$, $\pi_{0.5}$, and GR00T, exploiting this joint coupling consistently achieves superior task success while drastically lowering inference latency, entirely training-free and without architectural modifications. These findings establish numerical sampling depth as an operational variance regulator, shifting its role from a static precision budget to an active deployment knob in robot learning. Project page: this https URL

---

## 13. Full-Weight VLA Fine-Tuning Without an fp32 Master Copy Silently Erases Most Updates

**Authors:** Shubham Singh
**arXiv:** [2610.31859](https://arxiv.org/abs/2610.31859)
**Categories:** Robotics (cs.RO)

When a vision-language-action (VLA) model is fine-tuned with its trainable weights in bfloat16 (bf16) and no fp32 master copy, AdamW writes each update straight into bf16, silently rounding away any update smaller than 1/512 of a weight. In 9 of 12 open VLA codebases a default or documented recipe trains this way, 4 on full weight matrices, including LeRobot's SmolVLA default and its $\pi_0$/$\pi_{0.5}$ guides. In our LIBERO runs without the copy, a probe every 100 steps finds at least 79% of updates to bf16 weights erased. On the Hugging Face Hub, 99% of sampled full-weight SmolVLA fine-tunes store the action expert in bf16, and 84% of recent $\pi_{0.5}$ fine-tunes with a training configuration set the bf16 flag. On LIBERO-Object, with rules fixed in advance, an fp32 copy raises success over LeRobot's storage from 4.3% to 49.3% for SmolVLA and from 5.1% to 80.9% for $\pi_{0.5}$ at a ten-times lower learning rate, where both models are undertrained, and from 89.0% to 97.7% for $\pi_{0.5}$ at its default rate. For SmolVLA at its default rate it adds 10.2 points with open-loop 50-action chunks but only 4.2 when re-planning every 10 actions. In these five comparisons and two more against SmolVLA with every trainable weight in bf16, every run with the copy beats every run without it (p < 0.05); all gaps but the 8.7- and 4.2-point ones clear our 10-point threshold. The fix is to keep the trainable weights in fp32 during training, a one-line change for SmolVLA in LeRobot.

---
