# arXiv Daily Digest — 2026-10-06

**Mode:** direct
**Categories:** cs.AI, cs.LG, cs.RO, cs.CV
**Keywords:** VLA, RSI, agentic robot, self-improving robot, self-evolving robot, robot harness
**Papers found:** 26

---

## 1. Second-Order Problem Solving for Recursive Self-Improvement in Formal Verification

**Authors:** Yuxuan Jiang, Aditya Vempaty, Ashish Jagmohan
**arXiv:** [2610.05701](https://arxiv.org/abs/2610.05701)
**Categories:** Artificial Intelligence (cs.AI)

Recursive self-improvement (RSI) enables agents to iteratively optimize their workflows via execution feedback. However, standard RSI typically operates as a first-order optimizer: it repeatedly patches surface-level parameters in response to immediate failure symptoms, often leading to trial-and-error thrashing without resolving underlying mechanisms. To address this limitation, we introduce SO-RSI, a framework that elevates workflow optimization to a second-order diagnostic inquiry, investigating why failures occur before committing to structural interventions. SO-RSI passively monitors execution traces for three structural anomalies (recurrence, opposing edits, and expectation mismatch) to trigger targeted mechanism investigations. By executing lightweight diagnostic probes and maintaining persistent inquiry memory across RSI rounds, SO-RSI accumulates causal evidence to guide systematic workflow edits rather than parameter patches. Across Lean 4 proof generation and Verus-based verifiable code generation, SO-RSI improves final held-out pass rates over Naive RSI by 21.8 and 25.8 percentage points under matched 24-hour search budgets. Behavioral analyses further confirm that SO-RSI substantially suppresses failure recurrence and eliminates unproductive zero-progress optimization loops.

---

## 2. A Safe Action Is Not Enough: Feasible-Future Decoding for Vision-Language-Action Policies

**Authors:** Tu Nguyen, Matthieu Zimmer, Vu Anh Vu, ..., Xuebing Zhou, Haitham Bou Ammar
**arXiv:** [2610.05166](https://arxiv.org/abs/2610.05166)
**Categories:** Artificial Intelligence (cs.AI); Robotics (cs.RO)

A safe action is not necessarily a viable one. A frozen vision-language-action (VLA) policy can favor a locally admissible move that leaves no policy-supported route to safe task completion. We call this the feasibility-likelihood gap: likelihood ranks the next move, while feasibility depends on the futures it leaves open.
To bring those futures into the decision, we derive the exact next-block marginal of the history-conditioned policy-environment trajectory law restricted to safe task completion. The derivation reveals a candidate-dependent feasible-future mass: its support records whether safe completion remains possible under the frozen continuation process, while its magnitude measures how much weighted safe-completion mass remains. Since exact evaluation is impractical online, we develop a selective finite-candidate approximation and establish conditions for recovering the best retained viable candidate.
Our alarm-triggered, training-free reranker VICS-G lowers mean cumulative safety cost by 1.9%-57.5% across six Safety-CHORES settings while remaining within 2.5 percentage points of policy sampling in success and 0.82 steps in mean episode length. Our approach offers a promising and practical path toward safer task completion, grounded in an exact policy-relative target yet requiring neither policy retraining nor online rollouts.

---

## 3. PermVLA: Factorization Order as a Regularizer for VLA Learning

**Authors:** Yanqiao Chen, Yuhan Rui, Dongsheng Hou, ..., Yutong Wan, Qi Hao
**arXiv:** [2610.04659](https://arxiv.org/abs/2610.04659)
**Categories:** Artificial Intelligence (cs.AI); Robotics (cs.RO)

Vision-language-action (VLA) policies commonly learn action chunks through a fixed left-to-right (LTR) factorization, although the same expert trajectory distribution admits many valid chain-rule factorizations. We identify factorization order as an overlooked regularization choice and introduce causally anchored permutation (CAP), which samples action reveal orders with a tunable chronological prefix. Its auxiliary objective trains one shared policy to predict actions from different known subsets of the same expert chunk, while deployment retains deterministic LTR control. We call this conditional-set augmentation: it creates multiple conditional prediction problems from one expert chunk without adding demonstrations. This discourages reliance on the single chronological prefix used by ordinary teacher forcing. Controlled experiments show that CAP consistently outperforms standard LTR training on LIBERO and LIBERO-Plus, with the same advantage appearing in cross-dataset CALVIN evaluation. A diagnostic that measures the expected squared difference between a chunk's joint log likelihood under two reveal orders verifies that CAP training internalizes agreement across reveal orders. These findings position sampled subset-conditioned auxiliary objectives as a general recipe for constructing VLA regularizers, illustrated by an extension to diffusion action generators.

---

## 4. Recursive Video In-Context Learning for Agentic Robot

**Authors:** Wenrui Bao, Xinxin Liu, Bingxin Xu, Yuzhang Shang
**arXiv:** [2610.06843](https://arxiv.org/abs/2610.06843)
**Categories:** Robotics (cs.RO); Artificial Intelligence (cs.AI); Computation and Language (cs.CL); Multiagent Systems (cs.MA)

LLM agents that orchestrate frozen vision-language-action (VLA) policies improve across episodes through text memory, which records what the agent did but not how the task is done. A demonstration video shows it, but fits poorly into an agent's context. The full video slows every turn, fixed keyframes lose the contact detail that decides whether a grasp holds, and what the agent needs shifts from the task's structure while planning to the frames around each contact. We introduce Recursive Video In-Context Learning (RV-ICL), a training-free method that turns a demonstration into a hierarchy the agent navigates rather than a prompt it receives. The hierarchy is built from the sub-events of the demonstration, such as grasps and releases. Its levels grow finer, from keyframes of the whole task to phases, moments and short clips, and are exposed through read-only tools. The agent reads the coarse levels before planning. During execution it re-enters the hierarchy whenever a step needs more detail and loads only the clip of its current sub-goal. One demonstration per task is enough. Built on RPent, RV-ICL raises success from 92.6% to 96.5% on LIBERO-PRO and from 86.7% to 95.8% on LIBERO-Plus.

---

## 5. Wiring Matters: Injection Topology and Initialization of Affordance Heads in Vision-Language-Action Policies

**Authors:** Zijian An, Linhan Wang, Jiayan Wang, ..., Yiming Feng, Lifeng Zhou
**arXiv:** [2610.06318](https://arxiv.org/abs/2610.06318)
**Categories:** Computer Vision and Pattern Recognition (cs.CV); Artificial Intelligence (cs.AI)

Dense affordance supervision is an appealing auxiliary signal for vision-language-action (VLA) policies, yet naively co-training an affordance head can severely damage instruction following. We present a controlled study of how to wire such a head into a modern VLA on the LIBERO benchmark. Our recipe reads the backbone through a stop-gradient and re-injects an intermediate head feature into the action expert via a learned bridge. The stop-gradient is a precondition: letting affordance gradients reach the backbone drops the policy below the headless base (85.5% vs. 93.1%). With the backbone protected, a same-budget 2*2 ablation over injection topology (concatenation vs. residual) and bridge initialization (zero vs. random) shows initialization is the dominant lever. The best wiring, an actively initialized residual bridge, reaches 96.2%, matching the far more elaborate three-expert AffordanceVLA (95.8%) with under 1% extra parameters. Two probes explain the mechanism: ground-truth affordances fed as an input hurt, and inference-time zeroing shows a lazy bridge acts only as a training-time regularizer while an active bridge becomes load-bearing.

---

## 6. VLA-ZO: Fast Zeroth-Order Adaptation for Vision-Language-Action Models

**Authors:** Jaemin Kim, Jiahn Kim, Taesik Gong
**arXiv:** [2610.06271](https://arxiv.org/abs/2610.06271)
**Categories:** Robotics (cs.RO); Artificial Intelligence (cs.AI)

Adapting vision-language-action (VLA) models to deployment-time distribution shifts is important for reliable robotic operation, but conventional first-order adaptation can exceed the memory budget of inference-oriented deployment platforms. Zeroth-order (ZO) optimization offers a forward-only alternative with inference-level memory, but accurate gradient estimation requires many perturbation queries, making naive ZO prohibitively slow for large VLA models. We present VLA-ZO, a framework for fast ZO adaptation that exploits the structure of VLA computation. By confining adaptation to the action side, VLA-ZO keeps the expensive vision-language prefix frozen and reuses its conditioning states across perturbation queries and optimizer steps, while schedule-aware prefetching hides state-transfer overhead. On LIBERO camera-viewpoint shifts, VLA-ZO reduces end-to-end adaptation time by 25.59$\times$ at $q=16$ and 32.54$\times$ at $q=64$ relative to baseline ZO, while improving average task success from 48.27% without adaptation to 58.17% and 63.58%, respectively. These results show that making ZO faster can make larger query budgets practical, providing a promising path toward resource-efficient VLA adaptation on deployment platforms.

---

## 7. Do VLAs Understand and Adapt to the Objects They Handle, or Simply Replay Learned Behaviors?

**Authors:** Xinnuo Xu
**arXiv:** [2610.06078](https://arxiv.org/abs/2610.06078)
**Categories:** Robotics (cs.RO); Artificial Intelligence (cs.AI)

This paper asks whether VLA generalization is grounded in a global understanding of objects' physical properties that enables policies to adapt their motion to unseen setups, or if policies simply replay the motions they've learnt that happen to succeed in new setups. The former reflects genuine generalization; the latter reflects incidental robustness. We first examine awareness of physical properties in seven VLAs by applying linear probing and representational similarity analysis (RSA) to their activations. We find that physical properties, including mass, fragility, deformability, friction and size are less decodable than non-physical properties such as semantic category, material, sound and price in nearly every modality stream. Compared with their base VLMs, robot pre-training weakens the linear encoding of physical properties in the language stream. Neither pre-training nor downstream fine-tuning strengthens the alignment between physical-property differences and activation distances. We then ask whether the weak physical information present in these activations shapes the actions a VLA generates. In a controlled LIBERO case study, we increase the mass of an in-domain object and signal the change through language or vision. Most VLAs use similar lifting behaviour for the heavier and original-mass objects, leading to task success declines. The few exceptions change their behaviour in response to lexical or visual cues rather than to mass itself. These results suggest that VLAs encode physical properties weakly and do not reliably use them to adapt their motion.

---

## 8. OGAM: Connecting Systematic Testing to Runtime Assurance through Object-Grounded Attention Monitoring for VLA Policies

**Authors:** Haki Darwish, Xiangyu Yin, Changwen Li, ..., Francisco Gomes de Oliveira Neto, Chih-Hong Cheng
**arXiv:** [2610.05878](https://arxiv.org/abs/2610.05878)
**Categories:** Machine Learning (cs.LG); Artificial Intelligence (cs.AI); Robotics (cs.RO)

Benchmarks expose vision-language-action (VLA) policies to few canonical instructions, while exhaustive deployment testing is impossible. We introduce Object-Grounded Attention Monitoring (OGAM), connecting systematic testing to runtime assurance: testing reveals attention divergence between successful and failed executions, and OGAM uses this signal to stop failures beyond the finite suite. We generate scene-grounded instructions through pairwise combinations of action templates and objects, and separately test meaning-preserving paraphrases. All 87 out-of-benchmark cases reveal problematic behavior across OpenVLA, OpenVLA-OFT, UniVLA, and $\pi_{0.5}$: none completes any of the 24 feasible instructions, while infeasible or hazardous requests also trigger behavior substitution. At each action query, we project gradient-weighted visual attention through object masks and group it by instruction role for comparison across tasks and policies. Dynamic time warping aligns this course with a successful reference despite speed differences; conformal calibration on successful episodes sets the early-stopping threshold for sustained deviations, with a nominal false-stop target of $\alpha=0.05$. Across four policies, OGAM stops 87-100% of failed episodes at median times of 5-12s within a 20s budget, with observed false-stop rates of 3-5%, without failure-labeled training. Finite testing thus identifies attention patterns that support online intervention before failure fully unfolds.

---

## 9. Vela: Scaling Vision-Language-Action Models with Adaptive Action Curve Parametrization

**Authors:** Yifan Li, Jiaxu Wang, Dongming Wu, ..., Xiangyu Yue, Yanwei Fu
**arXiv:** [2610.05230](https://arxiv.org/abs/2610.05230)
**Categories:** Robotics (cs.RO); Artificial Intelligence (cs.AI)

Most vision-language-action models represent future motion as fixed-rate action chunks, tying temporal resolution and prediction horizon to a fixed output budget. This pointwise representation wastes capacity on highly correlated neighboring actions, leaves temporal continuity and smoothness to be learned implicitly, and forces a tradeoff between long-horizon coverage and the local precision required for contact-rich manipulation. To address these limitations, we introduce Vela, a vision-language-action foundation model that represents future robot behavior as continuous trajectories. Vela combines a compact spline-based action representation with motion-dependent temporal support and a shared action interface for heterogeneous embodiments, allowing a fixed output budget to adapt its temporal resolution across motions. We pretrain Vela on large-scale multi-embodiment robot data and evaluate it on LIBERO-X, EBench, and two real-world long-horizon tasks, egg-cake cooking and potato shredding, obtaining promising results across simulation and physical manipulation. These results highlight the potential of continuous action representations as a foundation for future embodied foundation models. Project page and more results: this https URL .

---

## 10. DiVeR: Decision-Critical Verifier Learning for VLA Test-Time Scaling

**Authors:** Seongheon Park, Heecheol Kim, Shulin Tian, ..., Sharon Li, Yasuyuki Matsushita
**arXiv:** [2610.04933](https://arxiv.org/abs/2610.04933)
**Categories:** Robotics (cs.RO); Artificial Intelligence (cs.AI); Machine Learning (cs.LG)

Scaling robot data and model capacity has improved Vision-Language-Action (VLA) policies, but further progress is constrained by the high cost of robotic data. Verifier-guided test-time scaling offers an efficient alternative by sampling multiple action candidates and selecting the one most likely to lead to task success at inference time. Existing classification-based verifiers learn from trajectory-level outcomes but treat all visited states equally, even though their value for candidate discrimination can vary across a trajectory. At many states, plausible actions are similar and provide limited discrimination signal, while only a sparse set of decision-critical states admits meaningfully different actions that can substantially affect downstream outcomes. To address this, we propose DiVeR, which estimates decision criticality from the dispersion of sampled action representations. DiVeR then uses this signal to reweight verifier learning toward states where action selection is most consequential, without requiring step-level annotations or additional environment interaction. Across LIBERO, RoboCasa, and real-world experiments on a Franka Research 3 robot, DiVeR consistently improves task success through more effective verifier-guided action selection, while adding negligible verifier inference overhead.

---

## 11. Beyond In-Distribution Preservation: Recovering Generalization in Quantized VLAs via Vulnerability-Oriented Tuning

**Authors:** Shen Ruan, Wenchang Gao, Jin Wang, ..., Dongchun Ren, Xin Zheng
**arXiv:** [2610.05745](https://arxiv.org/abs/2610.05745)
**Categories:** Machine Learning (cs.LG); Robotics (cs.RO)

Post-training quantization has been shown to preserve VLA performance under standard evaluation conditions, but whether it preserves the full-precision model's robustness and generalization remains underexplored. In this study, we systematically study the robustness and generalization of post-quantized VLA policies under environmental disturbances. Empirical results show that quantized policies can become fragile to subtle environmental variations despite retaining comparable in-distribution performance. We further observe that action discrepancies are concentrated in a small subset of rollout states, while teacher guidance has opposite effects depending on discrepancy: it improves generalization at high-discrepancy states but can degrade it at low-discrepancy states. These findings reveal that effective post-quantization recovery requires selectively intervening on vulnerable states rather than globally distilling the student. We therefore propose Policy-Induced Vulnerability-Oriented Tuning (PIVOT-Q), a vulnerability-aware On-Policy Distillation (OPD) framework that selectively corrects vulnerable states encountered during quantized-student rollouts using the frozen full-precision policy as a teacher. PIVOT-Q identifies vulnerable states using discounted accumulated discrepancies over a short horizon, applies phase-balanced sparse supervision, and uses a Behavioral Anchor to prevent unnecessary changes. Experiments under seven LIBERO-Plus environmental variations demonstrate consistent recovery across multiple VLA backbones and quantization methods. Notably, PIVOT-Q consistently outperforms full-state distillation across all settings while using only 7.4% of its state-level distillation budget. Our code is available at this https URL.

---

## 12. When Does Retrieval Help? A Study of In-Context Adaptation in Vision-Language-Action Models

**Authors:** Zixuan Liu, Joris Köster, Zizhan Zheng, Siavash Khajavi
**arXiv:** [2610.05492](https://arxiv.org/abs/2610.05492)
**Categories:** Machine Learning (cs.LG)

Vision-language-action (VLA) models have shown strong potential as generalist robot policies, but adapting them to unseen tasks often requires costly parameter updates. Recent work such as RICL introduces in-context adaptability by retrieving expert demonstrations based on the current VLA observation and providing them as additional context at test time. The effectiveness of this adaptation therefore depends critically on the retrieval mechanism. In this work, we systematically study how different retrieval methods affect both retrieval quality and task performance within the RICL framework. Specifically, we compare four different methods: image-based retrieval, retrieval augmented with VLA's state, retrieval using features from the VLA backbone, and random retrieval. Our experiments yield three main findings. First, no retrieval method consistently dominates the others in task success, while surprisingly, random retrieval achieves a non-trivial success rate. Second, standard retrieval-quality diagnostics do not reliably reflect downstream VLA performance. Third, demonstrations from different but related tasks can provide useful transferable information. Together, these results provide an initial step toward understanding how retrieval mechanisms shape the in-context learning capability of VLA models and their downstream task performance, while highlighting the need for more careful design and evaluation of retrieval mechanisms for reliable test-time adaptation.

---

## 13. How (and How Not) to Use Data Augmentation in VLA Post-Training

**Authors:** Bram Grooten, Joaquin Vanschoren
**arXiv:** [2610.05994](https://arxiv.org/abs/2610.05994)
**Categories:** Robotics (cs.RO); Machine Learning (cs.LG)

Vision-language-action (VLA) models currently demonstrate strong performance in a wide range of real-world robotics tasks. However, they often still lack the generalization ability to handle large visual out-of-distribution shifts. Post-training of VLAs with reinforcement learning (RL) has been shown to benefit robustness, but significant room for improvement remains. In this work, we systematically study the effect of image augmentation on VLA post-training. We find that it is crucial to augment only the critic module during RL updates, while leaving the actor's input clean during both rollouts and updates. For $\pi_{0.5}$ and GR00T N1.5 this raises out-of-distribution success on LIBERO-Plus by $7.8$ and $10.0$ points respectively, while augmenting the actor collapses training entirely. We investigate a range of augmentation types and strengths, and provide practical recommendations for improving generalization in VLA post-training.

---

## 14. Arm-wise Compositional Generalization in Dual-Arm Vision-Language-Action Models

**Authors:** Zaibin Zhang, Binghao Ran, Yuhan Wu, ..., Lijun Wang, Huchuan Lu
**arXiv:** [2610.06184](https://arxiv.org/abs/2610.06184)
**Categories:** Robotics (cs.RO)

Generalization in multi-arm collaboration can be studied as composing familiar atomic skills in new ways across arms. However, existing evaluations offer limited insight into which training and architectural choices support this ability under different coordination requirements. We introduce \textbf{ACG-Bench}, a benchmark for \emph{Arm-wise Compositional Generalization} that provides a common testbed for studying skill recomposition in dual-arm policies. It contains 23 task--condition pairs across 8 task families, with 6 in-domain conditions and 17 unseen compositions covering reordering, synchronization, their combination, and cross-task composition. All methods receive the same per-arm atomic prompts, and success requires achieving the task goal while satisfying physical milestones and specified order or timing constraints. Using $\pi_{0.5}$ as a common vision-language-action backbone, we compare representative data-augmentation and architectural strategies with shared source data and a common evaluation protocol. Our architectural study examines arm-token grouping, skill-specific LoRA adapters (SkillLoRA), and arm-wise attention (AWA), highlighting the complementarity of skill-conditioned parameters and attention structure. Combining these choices yields \textbf{AE-VLA}, which achieves 21.53\% generalization success in simulation, compared with 2.94\% for Single $\pi_{0.5}$, 3.06\% for MA-VLA, and 5.53\% for two independently controlled $\pi_{0.5}$ policies. On physical SO101 robots, AE-VLA reaches 39.00\% mean success across five unseen conditions, compared with 10.00\% for the strongest baseline. These findings provide empirical guidance for designing dual-arm policies that generalize beyond fixed training routines.

---

## 15. What the Guard Misses, the Robot Executes: Implied Harm in VLA Instructions

**Authors:** Sripad Karne, Arjun Balaji
**arXiv:** [2610.05818](https://arxiv.org/abs/2610.05818)
**Categories:** Robotics (cs.RO)

Vision-language-action models (VLAs) act on instructions without being able to refuse, so screening harmful requests falls to monitors. We test whether these monitors catch ordinary robot tasks requested for harmful reasons, holding the task fixed while varying only how explicitly the intent is stated. $\pi_{0.5}$ completes the task at every level of explicitness, as often as for harmless controls. Text guards flag nearly every blunt request but few implied ones: up to 95% of implied-harm runs end with the task done and no flag raised, and up to 90% even after recalibrating on robot instructions. Monitoring the model's activations does not close this gap. Linear probes separate harmful from harmless instructions almost perfectly in the base language and vision-language models, but this separation weakens after robot training in two model families, most for implied harm.

---

## 16. When to Switch: Reliable Action-Chunk Extension for Vision-Language-Action Models

**Authors:** Seonghoon Yu, Dongwon Kim, HyungRok Jung, ..., Suha Kwak, Jeany Son
**arXiv:** [2610.05719](https://arxiv.org/abs/2610.05719)
**Categories:** Robotics (cs.RO)

Vision-Language-Action (VLA) models serve as unified policies for robotic manipulation, yet their expensive inference forces robots to pause between policy calls, resulting in stop-and-go execution that interrupts smooth motion and prolongs task completion. Extending the action chunk reduces policy calls and hence these pauses, but predicting farther into the future makes long-chunk execution unreliable. To understand where this unreliability arises, we analyze action errors within long chunks and find that they concentrate around transitions between manipulation subskills, growing sharply with chunk length. This suggests the importance of transition timing, i.e., when to switch subskills within a chunk. Motivated by this observation, we introduce RACE (Reliable Action-Chunk Extension), a framework that predicts the transition timing from an auxiliary one-step denoising pass and conditions action generation on it. By learning and conditioning on transition timing, RACE reduces errors at subskill transitions and enables reliable execution of longer action chunks. Across simulation benchmarks, RACE outperforms fine-tuning at the same chunk length; with 2x longer chunks, it surpasses recent state-of-the-art and efficient VLAs in success rate, and with 4x longer chunks, it remains competitive. On a real robot, RACE uses 4x longer chunks, which reduces the idle time caused by stop-and-go execution by about 5x, while achieving a higher success rate than fine-tuning with the same chunk length. Code and a real-robot demo are available at this https URL

---

## 17. EvoMem-VLA: State-Evolution Memory for Long-Horizon Robot Manipulation

**Authors:** Yuheng Na, Zhide Zhong, Junjie He, ..., Tianyu Huang, Haoang Li
**arXiv:** [2610.05418](https://arxiv.org/abs/2610.05418)
**Categories:** Robotics (cs.RO); Computer Vision and Pattern Recognition (cs.CV)

Most vision-language-action (VLA) models rely on current observations and lose task-relevant evidence once it leaves view, limiting performance on long-horizon, memory-dependent tasks. Existing efforts incorporate compressed historical features or sparse visual keyframes. However, isolated snapshots can leave the policy uncertain about what changed during past interactions and which action should follow. To overcome this limitation, we propose EvoMem-VLA, which constructs state-evolution memory by explicitly encoding and retaining observed changes between historical states. These change representations preserve evidence of interaction outcomes, allowing the policy to track task progress beyond isolated snapshots. Specifically, we introduce conditional delta tokenization to encode ordered frame pairs into directional, source-conditioned delta tokens, each associated with its corresponding state evidence. A shared VLM backbone supports task-adaptive routing: normal long-horizon tasks follow a direct action route, whereas multi-stage tasks use a subtask route that generates an executable subtask as an additional input for action generation. With a single jointly trained policy for each simulation benchmark, EvoMem-VLA achieves success rates of 80.7\% on RMBench, 82.0\% on RoboMME and 83.8\% across four real-world tasks spanning two robot embodiments. These results represent substantial improvements over the previous state of the art in all three evaluation settings.

---

## 18. Recursive Self-Improvement of Visuomotor Policies through Local Recovery Supervision

**Authors:** Yuzhi Zhang, Xinyu Liu, Yu Zhang
**arXiv:** [2610.05151](https://arxiv.org/abs/2610.05151)
**Categories:** Robotics (cs.RO)

Visuomotor policies can execute familiar tasks yet lack the corrective behavior needed after their own mistakes. We present a framework for recursive self-improvement through local recovery supervision. Each round audits the current policy, generates corrective demonstrations at supported failure states, and uses them to update the policy that drives the next round of collection. An offline auditor locates unresolved failures using coarse and dense temporal evidence and specifies observable repair goals. A fixed multimodal agent acts as a tool-using teacher, generating recovery actions through observation, computation, execution, and feedback. The frozen student tests whether each teacher endpoint supports further progress. If continuation fails, the system restores that endpoint and extends the demonstration. Action-level quality assessment then defines continuous training windows with aligned observations, quality weights, and validity masks. Only the student is deployed. In a preliminary LIBERO-Goal study, recovery-augmented post-training achieves 88 successful episodes out of 100 validation scenes, compared with 78 for original-data continuation from the same $\pi_0$ checkpoint. An earlier BC-RNN study on robomimic Can improves success from 102/130 to 112/130 using 26 local recovery segments. Both comparisons match 2,000 additional optimization steps.

---

## 19. ExStereo: Lifting 2D Vision-Language-Action Models to 3D with Explicit Stereo Representations

**Authors:** I-Chun Arthur Liu, Jason Chen, Gaurav S. Sukhatme, Daniel Seita
**arXiv:** [2610.04805](https://arxiv.org/abs/2610.04805)
**Categories:** Robotics (cs.RO); Computer Vision and Pattern Recognition (cs.CV)

Three-dimensional perception is critical for robotic manipulation, particularly for high-precision tasks, as recovering metric depth and precise 3D object positions from monocular RGB observations is inherently ill-posed. However, many Vision-Language-Action (VLA) models rely solely on RGB observations for perception. Leveraging recent advances in foundation models for stereo matching, we introduce ExStereo, a stereo module that augments pre-trained 2D VLAs with 3D perception. ExStereo reconstructs scene geometry from stereo image pairs and renders multi-view observations as an explicit stereo representation for stereo feature extraction. The action tokens from the action expert selectively attend to the resulting stereo tokens through our proposed action-stereo cross-attention mechanism, enabling the policy to generate robot actions conditioned on 3D scene information. To learn robust 3D representations, we introduce a mid-training stage before task-specific post-training, using a self-supervised learning objective on large-scale stereo data. We validate our approach by fine-tuning two publicly available VLAs, $\pi_{0.5}$ and SmolVLA, and evaluate them in simulation and on a real-world bimanual PiPER platform. Across both settings, VLAs fine-tuned with ExStereo consistently outperform baselines, demonstrating the effectiveness of stereo perception for robotic manipulation. Our project website is at: this https URL.

---

## 20. PerturBot: Breaking Shortcut Priors in Vision-Language-Action Models with Perturbative Training

**Authors:** Mingyu Liu, Chonghao Sima, Tianjian Feng, ..., Hao Chen, Chunhua Shen
**arXiv:** [2610.04616](https://arxiv.org/abs/2610.04616)
**Categories:** Robotics (cs.RO); Computer Vision and Pattern Recognition (cs.CV)

A vision--language--action (VLA) policy can complete complex tasks while ignoring the evidence that should determine its actions. An object held near the wrist camera can displace the instructed target. Language and action show the same pattern: a familiar noun can trigger the operation it was paired with in training even after the verb changes, and a gripper that closed on nothing may lift anyway. We call these dependencies modality shortcuts: regularities in successful demonstrations make visual, lexical, or motor cues sufficient to predict expert actions without the task evidence needed for the underlying decision. More demonstrations of the same kind can raise task success while leaving these shortcuts intact. We propose Perturbot which makes task-relevant evidence easier to use and shortcuts insufficient on their own: it applies task-preserving wrist-view perturbations, enriches instructions with decision-relevant captions, and adds random and failed trajectory segments relabeled with the behavior they contain. It complements scaling by changing what is scaled, and leaves inference unchanged. Moreover, we propose GroundingFscore, an offline score that diagnoses how severely a policy relies on modality shortcuts. Task success rate shows whether a policy improves, while GroundingFscore reveals whether the policy scales healthily, relying on task evidence rather than shortcuts. Together, Perturbot and GroundingFscore provide a training-and-evaluation framework for disentangling VLA decisions from shortcut priors while preserving responsiveness to task-relevant evidence.

---

## 21. ForeAct3D: Policy-Grounded Future World Modeling for VLA Policies

**Authors:** Zhe Tao, Feiran Wang, Gaowen Liu, Ramana Rao Kompella$, Yan Yan
**arXiv:** [2610.04607](https://arxiv.org/abs/2610.04607)
**Categories:** Robotics (cs.RO); Computer Vision and Pattern Recognition (cs.CV)

Robots need to anticipate how their actions will change the world, since manipulation success hinges on the resulting contacts and object motions. However, existing Vision-Language-Action (VLA) policies that predict future observations from shared features leave the forecast decoupled from the actions the policy will actually execute, and impose no physical constraints on how the scene may evolve. We introduce ForeAct3D, a framework for policy-grounded future world modeling within VLA policies. Learnable geometric queries decode depth, semantic segmentation, and camera pose from the policy representation into current and future semantic 3D scene states, and the future queries are conditioned on the policy-generated action chunk to ground the forecast in the planned interaction. A physical-consistency closure relates the two states through background staticity and instance-level rigidity, and anchors the wrist-camera pose to end-effector kinematics. These objectives shape the shared representation used for action generation during training, and no future prediction is required at inference. Without robot pretraining, ForeAct3D achieves 98.3\% average success on LIBERO and an average task length of 3.73 on CALVIN, outperforming its base policy on every suite. Ablations show that semantic 3D supervision, physical consistency, and action conditioning each improve manipulation performance, and that action conditioning substantially improves future object localization. Real-world experiments on spatial placement, object insertion, and sequential manipulation further raise average success from 6.7\% to 37.8\% over the base policy. The project page and code are available at this https URL.

---

## 22. AgenticTactileVLA: Contact-Guided Execution-Time Supervision for Generalizable Dexterous Manipulation without VLA Retraining

**Authors:** Elizaveta Semenyakina, Ivan Snegirev, Mikhail Kiselev, ..., Hajira Amjad, Dzmitry Tsetserukou
**arXiv:** [2610.04391](https://arxiv.org/abs/2610.04391)
**Categories:** Robotics (cs.RO)

Vision-language-action policies may predict a transferable manipulation strategy yet fail to realize it reliably on the encountered object: objects compatible with the same grasp differ in geometry and compliance, and visual feedback degrades under closure occlusion. AgenticTactileVLA is presented as an execution-time supervisor that shifts part of object-specific adaptation from prediction to physical interaction. A fixed VLA provides the approach and hand targets; the supervisor decides whether to remain transparent, refine finger flexion, retain or release the corrected configuration, return control to the VLA for retry, or select a compliant hand-control regime. It uses finger-position and motor-effort feedback as proprioceptive contact evidence and requires neither tactile sensors nor VLA retraining. On a Unitree G1 with a BrainCo Revo2 hand, a randomized matched-block evaluation on five objects held out from VLA training yields 61.3% completion for the base VLA, 72.0% for unconditional close-to-stall control, and 84.0% for the supervisor under a shared budget; the gain is positive on every object and persists under moderate pose perturbations. Ablations show the gain is not explained by extended closure alone, and that selective triggering reduces correction episodes by 65.7% with no detected change in completion. A retention audit shows acceptance predicts retention in 88.9% of held-out cases, while compliant objects expose conservative false rejection. A thin-walled-cup study demonstrates contextual routing to compliant control, matching an always-compliant reference. These results suggest that contact-guided execution-time adaptation can improve the object-level generalization of a fixed VLA to held-out objects by adapting physical realization without object-specific retraining.

---

## 23. When and What to Prune? Stage-Aware Visual Token Pruning for Efficient VLA

**Authors:** Tianjun Shi, Haotian Xiong, Ziyu Gong, Qi Lu, Li Li
**arXiv:** [2610.05273](https://arxiv.org/abs/2610.05273)
**Categories:** Computer Vision and Pattern Recognition (cs.CV); Robotics (cs.RO)

Visual token pruning is an effective way to accelerate vision-language models and is especially useful for vision-language-action (VLA) inference, where many visual tokens must be processed before predicting robot actions. Existing pruning methods usually estimate which tokens can be pruned based on attention scores or feature diversity, retaining tokens that are either highly attended or visually different from others. However, most of them use fixed pruning schedules, such as pruning once at a preset layer or pruning at uniformly spaced layers. Such schedules can be risky for VLA models, because the model may not know which visual regions matter for the action in early layers. Tokens that look unimportant at first may become useful after the model combines visual observations with the language instruction. In this work, we propose SAPrune, a training-free visual token pruning framework for efficient VLA inference. Instead of pruning at fixed layers, SAPrune uses a small calibration set to observe how action-to-visual attention changes across layers, and chooses pruning layers only after the attention pattern becomes more reliable. At each selected layer, SAPrune applies a dual-path pruning rule: one path protects strongly attended visual tokens from pruning, while the other prevents useful surrounding context from being discarded. Experiments on LIBERO, SIMPLER, and real-world robotic tasks show that SAPrune prunes 87.5% of visual tokens and achieves up to 1.718x inference speedup while maintaining competitive task success rates.

---

## 24. Beyond LLM Serving: Characterizing Vision-Language-Action Workloads for Embodied AI System Design

**Authors:** Seonghun Jung, Sieun Moon, Jiyoung Jeong, Jimin Lee, Jaehyuk Huh
**arXiv:** [2610.05062](https://arxiv.org/abs/2610.05062)
**Categories:** Hardware Architecture (cs.AR); Robotics (cs.RO)

Vision-language-action (VLA) models translate multimodal observations into low-level robot actions. During robot operation, each control period sets an inference deadline, and overruns leave the robot acting on stale observations, reducing task success. Meeting this deadline motivates on-device or nearby edge execution, where a single robot requires batch-1 inference outside the design point of LLM serving systems. Although VLA architectures combine familiar vision-language, autoregressive, and diffusion-style components, their runtime behavior in this batch-1 control setting remains uncharacterized. We characterize four representative VLA models on an edge GPU server and two onboard SoCs, using single-inference profiling and 43,200 closed-loop episodes. Action tensor dimensionality determines whether a stage is memory- or compute-bound, platform balance can shift that bottleneck, and GPU frequency scaling yields a platform-dependent energy-latency sweet spot. In closed-loop operation, overlapping inference with action execution creates an accuracy-speed-energy tradeoff, and no configuration is Pareto-dominant across deployment SLOs. These results guide joint design of VLA model architectures, hardware, and runtime policies.

---

## 25. GeoBridge-VLA: Geometry-Aware Residual Adaptation for Vision-Language-Action Models

**Authors:** Hyun Song, Kangmin Kim, Loren Jinsoo Um, ..., Taewan Cho, Andrew Jaeyong Choi
**arXiv:** [2610.05026](https://arxiv.org/abs/2610.05026)
**Categories:** Computer Vision and Pattern Recognition (cs.CV); Robotics (cs.RO)

Vision-language-action (VLA) models encode semantic information from vision-language pretraining, but manipulation also requires precise spatial reasoning. We present GeoBridge-VLA, a two-stage method for learning geometric features from a pretrained VLA's frozen visual encoder and using them for action prediction. Stage I trains a feature bridge and geometry decoder with depth supervision. Stage II freezes these modules and trains a gated residual interface together with the action-side projections and action expert. The residual augments the existing visual tokens without adding a second image encoder or increasing the token count. Deployment requires RGB, robot state, and language, but no depth observations. Under matched evaluation conditions, GeoBridge-VLA achieves 70.9% success on LIBERO, compared with 60.0% for SmolVLA. Disabling the residual in the same trained checkpoint reduces success from 70.90% to 69.85%, with mixed effects across suites. On a physical ROBOTIS OMY robot, GeoBridge-VLA succeeds in 148 of 200 trials (74.0%) across four tasks, compared with 108 of 200 (54.0%) for SmolVLA.

---

## 26. Triggering Generalist Reasoning via Predictive Uncertainty for Dual-System VLA

**Authors:** Hyemin Yang, Wooseong Jeong, Giwon Lee, Kuk-Jin Yoon
**arXiv:** [2610.05025](https://arxiv.org/abs/2610.05025)
**Categories:** Computer Vision and Pattern Recognition (cs.CV)

Dual-system Vision-Language-Action (VLA) models improve real-time robotic control by pairing a slow, reasoning-capable generalist with a fast specialist action expert. However, existing methods invoke the generalist at a fixed frequency, ignoring the fact that decision-making complexity varies throughout a rollout. This static strategy wastes computation in easy phases and can delay renewed reasoning when the scene changes unexpectedly. We propose TUD (Triggering generalist reasoning via predictive Uncertainty for Dual-system VLA), an adaptive inference framework that selectively skips unnecessary generalist calls. TUD measures the cross-step dispersion of action re-predictions at the upcoming chunk slot under the cached generalist context, as a predictive uncertainty signal. This signal captures how much the future action plan shifts as new observations arrive and is computed from forwards the architecture already runs, requiring neither manual phase labels nor an auxiliary uncertainty model. On VLA-Arena, it achieves a higher success rate at matched call budgets than alternative uncertainty baselines while maintaining low wall-clock overhead, and more consistently separates successful from failed rollouts. Also, TUD finds a more favorable cost-success trade-off than non-adaptive baselines, tracing an entire operating curve as a single threshold is varied, and substantially reduces VLM calls at matched success rate. The same trade-off appears in our real-robot experiments, where TUD cuts generalist calls by 75% relative to the strongest fixed-interval baseline while achieving an even higher success rate. Our results suggest that predictive uncertainty provides a practical criterion for adaptive reasoning in efficient VLA control.

---
