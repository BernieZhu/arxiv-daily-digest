# arXiv Daily Digest — 2026-10-08

**Mode:** direct
**Categories:** cs.AI, cs.LG, cs.RO, cs.CV
**Keywords:** VLA, RSI, agentic robot, self-improving robot, self-evolving robot, robot harness
**Papers found:** 15

---

## 1. EmbodiedRSI: Active Continual Robot Learning Through Hypothesis-Guided Co-Evolution

**Authors:** Python Song, Zhixuan Liang, Kelsey Fu, ..., Junfeng Yang, Shilong Liu
**arXiv:** [2610.10498](https://arxiv.org/abs/2610.10498)
**Categories:** Artificial Intelligence (cs.AI)

Robot foundation models provide strong visuomotor control, yet their performance can degrade when object positions or task instructions change. Further improvements often require post-training on substantial robot data, which can be costly to collect through methods such as teleoperation. Agentic harnesses can adapt around the model, but current self-evolving harnesses use robot trials inefficiently when deciding which code and skill changes to pursue. We introduce EmbodiedRSI, a self-evolving agentic harness that autonomously decides where to explore next and turns the resulting physical interaction into improved code and skills. EmbodiedRSI realizes this through a Fast-Slow Dual-System Architecture, in which competing code and skill hypotheses are maintained in a Hypothesis Graph. Value-of-Information Experiment Selection chooses physical experiments that can distinguish these hypotheses. Their outcomes guide Code-Skill Co-Evolution. The Slow System builds Hierarchical Memory, and Reward-Grounded Memory Learning selects effective memory according to their value for later Fast-System improvement. On RoboCasa365, EmbodiedRSI reaches 77.0% overall success and 71.3% on Composite-Unseen, compared with 40.1% for the best baseline. EmbodiedRSI also reaches 86.8% overall success on LIBERO-Pro. Beyond benchmark performance, EmbodiedRSI transfers zero-shot to real-world robot, achieving 71.3% overall success across multiple challenging tasks.

---

## 2. RSI-Forge: From Research Papers to Environments for Recursive Self-Improvement

**Authors:** Renxiong Wang, Darvin Yi, Abril Herrlein, ..., Tong Zhao, Yunzhong He
**arXiv:** [2610.09426](https://arxiv.org/abs/2610.09426)
**Categories:** Artificial Intelligence (cs.AI)

Environments are the foundation of recursive self-improvement: they provide the problems agents work on and the feedback used to evaluate progress. Yet constructing challenging research environments with reliable evaluation still depends on domain experts, limiting their scale and disciplinary coverage. We introduce RSI-Forge, a multi-agent pipeline that turns published papers into executable environments for self-improvement. Three agents coordinate construction, reproduction, and review to produce tasks with automated evaluators; each paper's method is independently reimplemented to establish a baseline score. We present 210 environments across 18 fields, including 90 reviewed by independent human domain experts. Both experts and agent judges give high ratings to the potential for improving the provided starting solutions and the evaluators' ability to distinguish solution quality, whereas experts are more critical of shortcut resistance, faithfulness to the source paper, and whether a single idea can exhaust a task. To validate their use for repeated improvement, we evaluate four models over 3 successive attempts on 120 environments, with each attempt inheriting prior code and notes while model weights remain fixed. At least one model improves after the first attempt in 84% of environments. Models also outperform the reproduced paper methods in 68 of the 120 environments, demonstrating room for gains beyond these baselines. Transcript analysis identifies work beyond parameter tuning in 95% of these successful attempts. Analysis of the resulting trajectories shows that models scoring lower on these tasks explore less, more often accept gains smaller than the reported standard error, and rely more heavily on tuning to the development set. RSI-Forge provides a scalable approach to constructing research environments for training and evaluating self-improving agents.

---

## 3. DIVA: Dual-Space Intent-Aware Visual Attenuation for Vision-Language-Action Policies

**Authors:** Kaixi Feng, Guoheng Sun, Ziyao Wang, ..., Zheyu Shen, Ang Li
**arXiv:** [2610.09144](https://arxiv.org/abs/2610.09144)
**Categories:** Artificial Intelligence (cs.AI)

Vision-language-action (VLA) policies typically feed dense visual patch tokens into a language-action backbone, preserving scene context but offering no explicit mechanism to regulate how strongly different visual tokens influence policy computation. We introduce DIVA, a Dual-Space Intent-Aware Visual Attenuation module with an anchor-then-attenuate design. DIVA combines high-level task intent with low-level visual evidence to estimate patch-wise relevance anchors, then applies them in two complementary spaces: it reweights projected visual tokens before backbone entry and persistently attenuates low-relevance visual states within the backbone. DIVA preserves the full visual token sequence and requires no external grounding supervision. On LIBERO, DIVA improves OpenVLA-OFT from 96.6% to 98.0% average success and raises its zero-shot LIBERO-Plus score from 69.6 to 72.6. Real-world experiments further show consistent gains under task-irrelevant visual perturbations, supporting the robustness of intent-aware visual attenuation beyond simulation.

---

## 4. PAIR: Bridging Perception and Action in Vision-Language-Action Models

**Authors:** Kaixi Feng, Guoheng Sun, Ang li
**arXiv:** [2610.09016](https://arxiv.org/abs/2610.09016)
**Categories:** Artificial Intelligence (cs.AI)

Vision-language-action (VLA) models map visual observations and language instructions to continuous robot actions. This task requires a transition from representations that describe the scene and instruction to representations that support action generation. Many continuous-action VLAs leave this transition implicit and supervise it mainly through the final action-prediction loss. We introduce PAIR, a framework that learns a shared perception-action representation between these two spaces. During training, a Masked Action Autoencoder encodes expert action chunks into horizon-aligned Action Latent Tokens. A Bridge Module extracts task-relevant features from the current visual-language representations. PAIR aligns these features with the Action Latent Tokens to form Bridge Tokens that preserve task information and capture the structure of expert actions. The Bridge Tokens are then projected into the action-token space and injected into the initial Action Tokens, providing an action-ready starting point for Action Expert refinement. At inference, the autoencoder is removed, and the Bridge Tokens are generated only from the current observation and instruction. Experiments on LIBERO, LIBERO-Plus, and CALVIN ABC-D show gains for the evaluated OpenVLA-OFT and VLA-Adapter models. On LIBERO-Plus, PAIR raises VLA-Adapter's success rate from 59.1% to 64.2%. On CALVIN, it increases VLA-Adapter's average completed sequence length from 4.42 to 4.53. Across seven real-world tasks, PAIR raises OpenVLA-OFT's success rate from 51.4% to 65.0%. Representation analyses show that Bridge Tokens retain task information while making continuous-action information accessible before Action Expert refinement. These results support a shared intermediate representation as a useful interface between perception and action in continuous-action VLAs.

---

## 5. Sparse Feature Policy Unlearning Mitigates State Hallucination in Vision-Language-Action Models

**Authors:** Jiho Lee, Jeongeun Park, Heayoun Choi, Taekyung Kim, Eunwoo Kim
**arXiv:** [2610.09496](https://arxiv.org/abs/2610.09496)
**Categories:** Robotics (cs.RO); Artificial Intelligence (cs.AI); Machine Learning (cs.LG)

Vision-Language-Action (VLA) models have shown strong generalization in robotic manipulation by leveraging rich representations from pretrained vision-language models. However, their deployment in real-world environments remains limited by recurring unreliable behaviors. In this work, we study state hallucination, a recurring failure pattern in which a VLA continues acting as if an unrealized robot-object state had been achieved. Our analyses find that state hallucination coincides with weakened attention to task-relevant visual regions, and a mechanistic interpretation via sparse autoencoders reveals that hallucination-associated sparse features are activated when these failures occur. Based on this analysis, we propose SOUL (Sparse feature pOlicy UnLearning), which selectively unlearns policy knowledge associated with state hallucination behaviors, where sparse features identified from hallucination failures and successful behaviors serve as explicit forgetting and retention targets, respectively. Experiments across VLA architectures in simulated and real-world environments show that our method substantially reduces hallucinated failures and improves task success without substantially compromising the existing manipulation capabilities. These results suggest that interpretable feature analysis provides a practical basis for selectively modifying undesirable knowledge in robot policies.

---

## 6. RSIGym: A Flexible Environment for Recursive Self-Improvement

**Authors:** Fanqing Meng, Lingxiao Du, Haocheng Lu, ..., Mengkang Hu, Michael Qizhe Shieh
**arXiv:** [2610.10310](https://arxiv.org/abs/2610.10310)
**Categories:** Machine Learning (cs.LG)

Recursive self-improvement requires carrying accepted changes into later improvement cycles, while studying agent-proposed changes also requires substantial research infrastructure. Existing settings often leave agents to rebuild routine infrastructure or restrict exploration to individual components. We introduce RSIGym, an agent-native research environment based on Everything as a Service (EaaS). RSIGym exposes training, inference, rollout, evaluation, and sandbox execution through reusable services, with shared budget and permission controls supporting Data, Harness, and Joint improvement tracks. This design enables agents to investigate individual interventions and jointly optimize data, training settings, and execution harnesses within the same environment. We define RSI-Index as the mean fraction of the remaining performance gap closed across five benchmarks covering software engineering, terminal interaction, mathematics, scientific reasoning, and skill-based tasks. Comparing six frontier research models in independent Joint runs, Opus 5 achieves the highest RSI-Index of 0.4809 under a $500 platform-service budget per benchmark run. Its selected systems improve all five benchmarks, raising SWE-bench Verified from 17.67% to 50.33% and AIME from 31.67% to 97.78%. Additional experiments examine DSH-harness refinement, budget variation, and restricted network access, while recorded trajectories reveal how agents diagnose failures and select candidates. We open-source the full RSIGym codebase and results to support reproducibility and further research.

---

## 7. Rephrase Before You Act: Characterizing and Mitigating Language Sensitivity in Vision-Language-Action Models

**Authors:** Mikey Watts, Yuchen Cui
**arXiv:** [2610.10526](https://arxiv.org/abs/2610.10526)
**Categories:** Robotics (cs.RO); Computation and Language (cs.CL); Machine Learning (cs.LG)

Vision-language-action models (VLAs) are strikingly sensitive to instruction phrasing and do not inherit the language robustness of the vision-language models they are built on. A one-word edit can move success by tens of points: $\pi_{0.5}$ turns on a LIBERO stove 100% of the time for "switch on the stove" and 2% for "switch on the hot plate", and a $\pi_0$ checkpoint finetuned with rephrase augmentation still shows swings of up to 61 points. We characterize this sensitivity with statistically tested single-edit swings and an oracle phrase search, which shows that phrasing alone nearly closes the 21-point gap between in-distribution and out-of-distribution tasks. We then reduce it without modifying the policy. Because the sensitivity is systematic, it can be expressed as explicit rules: we score many phrasings of a few training tasks, have a large language model distill the evidence into ten to twenty rephrasing rules, and at deployment rewrite each incoming instruction once under these rules. The rules improve the frozen $\pi_0$ by 16 to 27% relative on twelve held-out tasks across adversarial, VLM-generated, and human-generated phrasings, with gains concentrated on out-of-distribution tasks. The pipeline replicates on $\pi_{0.5}$ and LIBERO, lifting in-finetune success from 93.6% to 97.8%. The method requires no retraining and no per-step verification, and applies zero-shot to unseen tasks and instructions. Project website: this https URL

---

## 8. Many Ways to Succeed: Diversity-Driven RL Fine-Tuning for VLA Generalization

**Authors:** Haoru Li, Jinmei Liu, Zhiyong Wang, ..., Chunlin Chen, Zhi Wang
**arXiv:** [2610.09943](https://arxiv.org/abs/2610.09943)
**Categories:** Robotics (cs.RO); Machine Learning (cs.LG)

Reinforcement learning (RL) fine-tuning improves vision-language-action (VLA) policies through closed-loop experience, yet generalization beyond the fine-tuning distribution remains limited. Our analysis reveals a selective reshaping of exploration: RL contracts behavior globally, yet diversifies successful trajectories, elicits success with fewer rollouts, and covers more of the latent task-valid solution space than supervised fine-tuning. Broader successful-mode coverage may provide alternative strategies under distribution shifts. Inspired by this, we introduce DRIVE (Diversity-driven RL fIne-tuning for VLA gEneralization), which turns successful-behavior diversity into an explicit RL objective. DRIVE groups rollouts under matched task conditions, compares their trajectories with temporal alignment, and derives a success-conditioned intrinsic reward from relative behavioral diversity. This design encourages broader coverage of feasible solutions without rewarding diverse failures or superficial timing differences. Across LIBERO-Plus, ManiSkill3, and RoboTwin 2.0, DRIVE improves the average out-of-domain (OOD) performance over vanilla RL fine-tuning by 5.3 points on $\pi_0$ and 2.0 points on $\pi_{0.5}$. On a dual-arm AgileX PiPER-X platform, DRIVE further increases average OOD success from 64.1% to 73.3% (+9.2 points), demonstrating gains that persist under physical deployment.

---

## 9. CARE: Certifying Acceleration for Vision-Language-Action Inference

**Authors:** Rui Liu, Tong Zheng, Jindong Gu, Zhipeng Wang
**arXiv:** [2610.08917](https://arxiv.org/abs/2610.08917)
**Categories:** Computation and Language (cs.CL); Machine Learning (cs.LG)

While vision-language-action (VLA) models have advanced rapidly, running them at every control step remains expensive. Prior work accelerates VLA inference using techniques like action chunking and visual-token pruning, typically evaluating based on latency and average task success. However, acceleration may discard information and break tasks the original policy would solve, a risk hidden by average metrics. Measuring these failures is challenging because action deviations compound over closed-loop trajectories, meaning task failure is only observable across full episodes. We therefore define an acceleration-induced failure via paired rollouts from identical initial conditions, tracking when the reference succeeds but the accelerated policy fails. To manage this, we introduce CARE, an approach for certified accelerator selection. CARE uses paired rollouts on a calibration set to provide finite-sample guarantees that acceleration-induced failure risk stays below a user-specified budget. It deploys the fastest certified candidate, falling back to the reference if none qualify. By relying only on terminal outcomes and measured compute, CARE applies unchanged across diverse acceleration mechanisms, while sequential testing and failure-triggered reference rollouts keep certification affordable. On four LIBERO suites with OpenVLA-OFT, CARE certifies $9.0$--$10.8\times$ speedups while guaranteeing (at $95\%$ confidence) that at least $85.8\%$ of reference-solved episodes are preserved. Under tight budgets, selectors without guarantees exceed the budget in up to $75\%$ of trials, whereas CARE stays within budget and its sequential form uses $78.9\%$ fewer rollouts than exhaustive evaluation. CARE further generalizes to flow-step reduction for $\pi_{0.5}$, and to Qwen3.5-9B and Llama-3.1-8B agents in Crafter.

---

## 10. Do Vision-Language-Action Models Understand Instructions? A Mechanistic Interpretability Study on Language Grounding

**Authors:** Theodor Wulff, Angelo Cangelosi
**arXiv:** [2610.10178](https://arxiv.org/abs/2610.10178)
**Categories:** Robotics (cs.RO)

Vision-Language-Action models are designed to generalise across environments and task descriptions, raising the question of whether their action generation actually depends on the language instruction, or whether they largely rely on visual cues and superficial correlations. Robustness to variance in the visual and linguistic observation space is critical for real-world deployment, yet VLAs lack explicit grounding modules and instead rely on the intrinsic language grounding capabilities of their Vision-Language model backbones. For this reason, we conduct a controlled mechanistic interpretability study on the language grounding capabilities of two state-of-the-art Vision-Language-Action models, $\pi_{0.5}$ and GR00T N1.7, by applying activation and attribution patching to the residual stream of the action generation modules. We systematically corrupt the task instruction of input samples of the LIBERO benchmark following five strategies: synonym replacement, semantic scaling, directional corruption, random object substitution, and empty string. Our experiments find that both models are comparatively insensitive to abstract rephrasing and to referencing non-existent objects, but react strongly to empty task descriptions and, especially, to directional language. During action generation, this sensitivity is concentrated in different loci for each model: mainly in the early, periodic cross-attention layers for GR00T N1.7, versus distributed across the earliest and selected later layers for $\pi_{0.5}$. For GR00T N1.7, directional perturbations drive some of the largest causal effects while leaving the internal representational geometry comparatively unchanged, a dissociation we do not observe clearly for $\pi_{0.5}$. Finally, the reliability of attribution patching is model-dependent: it closely tracks activation patching for GR00T N1.7 but not for $\pi_{0.5}$.

---

## 11. Juno: Taming Predictive Latents for Vision-Language-Action Models

**Authors:** Yuchen Zhu, Chenyi Xu, Yulin Zhang, Gang Xu, Wentao Zhu
**arXiv:** [2610.09940](https://arxiv.org/abs/2610.09940)
**Categories:** Robotics (cs.RO); Computer Vision and Pattern Recognition (cs.CV)

Joint-embedding predictive architectures (JEPAs) predict masked or future observations in representation space, offering a natural source of predictive latents for vision-language-action (VLA) models. Yet making these latents useful across pretraining, policy learning, and deployment requires addressing three failures: mismatch with embodiment-specific control, interference with action learning, and teacher miscalibration under distribution shifts. We introduce Juno, a unified framework built around one action-conditioned JEPA that serves as a control-aligned representation backbone, a predictive teacher, and an adaptable dynamics model. During pretraining, we train it on embodiment-matched trajectories and use a dynamic CLS loss to transfer motion-weighted patch dynamics to a compact global state. During policy learning, we fuse current-frame JEPA patches into VLA perception and use a decoupled reasoning branch with separate transformation parameters to distill future latent states for action generation. During deployment, we adapt the world model on all observed transitions, including failed rollouts, freeze the adapted teacher, and re-align the policy on verified executions using LoRA adapters and a trainable action head, without expert corrections or task rewards. On SimplerEnv, Juno raises average success from $60.9\%$ to $68.5\%$ over Qwen3GR00T, the strongest baseline, and test-time adaptation further reaches $72.7\%$; on a real robot, it retains $70\%$--$75\%$ success under background, height, and object shifts where the base policy collapses to $0\%$.

---

## 12. YUBI-STAG: Contact and Semantic-Rich Alignment for VLAs via Automated Video-Language Grounding

**Authors:** Masatoshi Tateno, Takehiko Ohkawa, Yueh-Hua Wu, ..., Yoichi Sato, Kei Ota
**arXiv:** [2610.09718](https://arxiv.org/abs/2610.09718)
**Categories:** Robotics (cs.RO); Computer Vision and Pattern Recognition (cs.CV)

Vision-Language-Action (VLA) models acquire broad manipulation capabilities via large-scale pretraining, yet eliciting them through language requires fine-grained alignment between instructions and physical interactions. Existing robot demonstrations typically provide only coarse task descriptions, omitting how actions are executed, including which gripper acts, which object is contacted, and how it is grasped and moved. We introduce YUBI-STAG, a framework for Spatio-Temporal Annotation and Grounding that automatically enriches manipulation demonstrations with interaction-rich semantics to align pretrained VLAs with fine-grained manipulation language. Combining contact-object segmentation with vision-language models, YUBI-STAG annotates object identities, attributes and states, per-gripper actions, bimanual coordination, and spatially grounded interactions. To address YUBI-STAG's reliance on localized sequences and multi-stage VLM inference, we distill it into YUBI-VLM. YUBI-VLM directly recovers action structure and annotations from raw, unsegmented video in few inference calls and operates from wrist views alone. We evaluate both frameworks on YUBI-STAG-Bench across temporal, semantic, and spatial grounding tasks. YUBI-VLM retains much of YUBI-STAG's annotation accuracy with fewer inference calls and shorter runtime while generalizing to unseen manipulations. Finally, post-training VLA policies on these annotations aligns them with fine-grained language and contact-aware structure. Bimanual experiments demonstrate improved performance and instruction following, including control over object identity, acting gripper, target location, and spatial relations absent from original labels.

---

## 13. TMT: Runtime Backdoor Detection for Vision-Language-Action Policies on Unseen Tasks

**Authors:** Zirun Zhou, Jingfeng Zhang, HaoChuan Xu, ..., Jing Sun, Hong Jia
**arXiv:** [2610.09462](https://arxiv.org/abs/2610.09462)
**Categories:** Robotics (cs.RO)

Backdoored vision-language-action (VLA) policies can preserve benign task performance while producing malicious actions when a trigger appears. Detecting such activation is difficult because malicious behavior can comprise individually plausible actions, while unfamiliar tasks introduce legitimate changes in observations and behavior. We introduce TMT, a runtime backdoor detector based on Token Manifold and latent Transition modeling. Trained on benign rollouts, its two branches assess input-token structure and prediction errors in adjacent-layer latent dynamics. A suspicious rollout identified by the token manifold branch, once confirmed through latent deviations, guides transition selection for subsequent monitoring. We further explore policy purification through self-distillation: a frozen copy of the backdoored policy provides benign-input actions to supervise a student on paired benign and triggered observations, without requiring a separate clean reference policy. For evaluation, we adapt traditional backdoor detectors and repurpose anomaly and failure detection methods as VLA backdoor detectors. In a post-hoc comparison with ten baselines, TMT achieves state-of-the-art backdoor detection performance on unseen tasks across three VLA backdoor attacks. Our project page is available at this https URL.

---

## 14. TempoBridge: Language-Guided Tempo Control for Vision-Language-Action Policies

**Authors:** Yeonseo Lee, Hyosup Shin, Guebin Hwang, Sungho Jo
**arXiv:** [2610.09451](https://arxiv.org/abs/2610.09451)
**Categories:** Robotics (cs.RO)

Vision-Language-Action (VLA) models are effective at understanding what task to perform, but provide limited control over how it should be executed, such as moving quickly or slowly. We introduce TempoBridge, a lightweight framework that uses frozen VLA representations to modulate actions according to tempo cues in the instruction at each task phase, without additional tempo-conditioned robot demonstrations or tempo-specific base-policy fine-tuning. TempoBridge extracts tempo cues from contextual VLM representations, aligns them with task progress through a causal phase router, and modulates nominal motion commands during execution. Across LIBERO tasks, TempoBridge improves Tempo Success Rate from 52.6% to 89.7% under canonical tempo instructions while retaining high task success. It also preserves near-baseline performance when no tempo cue is present and generalizes to unseen tempo expressions without additional training. Experiments on a physical robot further demonstrate language-conditioned tempo modulation in real-world manipulation.

---

## 15. Explicit Geometric Chain-of-Thought for Vision-Language-Action in Autonomous Driving

**Authors:** Xingtai Gui, Yucheng Zhou, Dongqian Guo, ..., Feiyang Tan, Jianbing Shen
**arXiv:** [2610.10390](https://arxiv.org/abs/2610.10390)
**Categories:** Computer Vision and Pattern Recognition (cs.CV)

Vision-language-action~(VLA) models have emerged as a promising paradigm for autonomous driving. However, existing VLA models still suffer from a fundamental mismatch: driving actions require precise 3D geometric cues, while visual-language understanding and reasoning are largely conducted in a 2D semantic space. In this paper, we propose GeoCoTDrive, an explicit geometric chain-of-thought framework that grounds geometry in a planning-oriented manner. GeoCoTDrive follows a think with 2D first, drive with dedicated 3D priors paradigm. It first grounds 2D regions corresponding to decision-critical cues, and then retrieves localized 3D priors by sampling features from a geometric foundation model within the grounded regions. These localized geometric features are interleaved into the autoregressive context to support the trajectory generation. To supervise this process, we introduce planning-relevant grounding, a new region-level grounding task that focuses on local spatial cues directly affecting ego planning decisions, and construct the PlanningGrounding dataset to endow VLAs with planning-oriented grounding capability. Experiments across multiple end-to-end autonomous driving benchmarks show that GeoCoTDrive consistently improves safety-critical planning performance, demonstrating the effectiveness of the explicit geometric chain-of-thought process for VLA-based planning.

---
