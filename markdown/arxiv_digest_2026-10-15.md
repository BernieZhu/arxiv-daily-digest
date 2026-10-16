# arXiv Daily Digest — 2026-10-15

**Mode:** direct
**Categories:** cs.AI, cs.LG, cs.RO, cs.CV
**Keywords:** VLA, RSI, agentic robot, self-improving robot, self-evolving robot, robot harness
**Papers found:** 19

---

## 1. SwarmRSI: Recursive Self-Improvement through Evolving Scientific Agent Swarm

**Authors:** Qianru Meng, Xi Zhang, Konstantinos Papakostas, ..., Xiaohui Yan, Yougang Lyu
**arXiv:** [2610.20431](https://arxiv.org/abs/2610.20431)
**Categories:** Artificial Intelligence (cs.AI); Computation and Language (cs.CL)

Recursive self-improvement (RSI) in scientific research aims to improve agents' research capabilities through their own experimental experience. Scientific agent swarms can combine evidence and implementations from different research directions to guide their agents' subsequent experiments. However, poor experimental results can leave unclear whether to revise a hypothesis or its implementation, while overall program scores can hide components useful to other agents. To address these challenges, we introduce SwarmRSI, a framework that evolves scientific agent swarms for recursive self-improvement. We devise Feedback-Guided Swarm Mutation to refine hypotheses and their implementations using experimental feedback from other agents. We also propose Complementary Swarm Recombination to reuse retained hypotheses and complementary program components across agents, allowing partial results to support new research. Recursive Swarm Evolution integrates both mechanisms into a feedback loop, using new experimental evidence to guide subsequent research. Experiments on OpenProblems, NatureBench and MLE-Bench Lite demonstrate SwarmRSI's state-of-the-art (SOTA) performance. Further evaluations show that accumulated research experience improves performance on held-out tasks. Biologists also reproduce its programs for follow-up biological analyses.

---

## 2. VLRLA: Deployment-Time Adaptation of Vision-Language-Action Models through In-Context Reinforcement Learning

**Authors:** Diyuan Shi, Yiqi Tang, Hongyin Zhang, You Wu, Donglin Wang
**arXiv:** [2610.19517](https://arxiv.org/abs/2610.19517)
**Categories:** Artificial Intelligence (cs.AI); Robotics (cs.RO)

Vision-language-action (VLA) models connect visual perception and language understanding with robot control, providing a foundation for instruction-conditioned manipulation. However, conventional pretrained VLA policies lack a mechanism for gradual adaptation through accumulated interaction experience during deployment. We therefore propose VLRLA, a general framework that equips existing VLA models with \textit{in-context reinforcement learning} capabilities for deployment-time adaptation. Our approach augments a VLA model with a reinforcement learning module that learns from historical observations, actions, rewards, and termination signals. During deployment, the policy gradually refines its action generation and progressively improves task success while keeping model parameters fixed. Our approach is also designed for general applicability and compatibility with diverse learning history construction strategies and model training pipelines. Finally, through extensive experiments, we systematically investigate the learning properties of VLRLA in simulation and demonstrate its ability to adapt to unseen scenarios during real-world deployment.

---

## 3. FoveaVLA: Foveation Actions Replace the Wrist Camera in VLAs

**Authors:** Bingao Chen, Lihan Zha, C. Karen Liu, Guy Tevet
**arXiv:** [2610.20064](https://arxiv.org/abs/2610.20064)
**Categories:** Robotics (cs.RO); Artificial Intelligence (cs.AI)

We present FoveaVLA, a Vision-Language-Action (VLA) model that replaces the wrist camera with learned foveation actions. Wrist cameras provide close-up detail but restrict the view to the end-effector's surroundings. External cameras see the whole scene, but the policy receives them at low resolution, so the fine detail needed for manipulation is lost. FoveaVLA recovers this detail by predicting, alongside each action chunk, the interaction region to observe at the next policy query. The policy then receives crops of these regions, taken from the original-resolution images, together with the full views. We build FoveaVLA on $\pi_{0.5}$ in two configurations, Single and Dual, using one or two external stereo cameras with full and foveal RGB and depth inputs, and post-train both on DROID with RoboInter interaction annotations. Across four real-world task suites, FoveaVLA-Single achieves 70.8% success with one external RGB-D view, and FoveaVLA-Dual achieves 77.1%, versus 52.1% for the wrist-equipped $\pi_{0.5}$. Both match the baseline on plain pick-and-place and improve success with distractors, cloth manipulation, and far-away objects.

---

## 4. VideoHarness-SRSI: Structured Recursive Self-Improvement for Video Understanding Harness

**Authors:** Zihao Lin, Haoyu Dong, Haobo Xu, ..., Yang Song, Qifan Wang
**arXiv:** [2610.19424](https://arxiv.org/abs/2610.19424)
**Categories:** Computer Vision and Pattern Recognition (cs.CV); Artificial Intelligence (cs.AI)

LLM system capabilities depend not only on model parameters but also on the executable harnesses that organize information acquisition, tool use, reasoning, and memory. Recursive harness evolution can automate their design, but how it can reliably discover generalizable systems from limited, noisy, and repeatedly reused feedback remains unclear. We study this question in agentic video understanding, where rich multimodal evidence and coupled mechanisms make harness optimization challenging. We first introduce VideoHarness-BRSI, a recursive self-improvement framework that evolves video harnesses around a frozen vision-language model. Analyzing over 4,000 evolved candidates, we find it competitive with hand-engineered systems but identify three interconnected failure modes: validation overfitting, search-budget dilution, and the early-experience trap. We trace all three to a common root: the same imperfect validation evidence drives both harness revisions and the proposer's search strategy. We therefore propose VideoHarness-SRSI, an evidence-governed framework in which every search decision rests on evidence that is transferable, sufficient, and gathered before the search commits. It restricts the proposer to content-free feedback, informs exploration with instrumented warm-up experiments, and develops mechanisms in isolated probe-race branches before factorial composition and joint refinement. Across four video understanding benchmarks, VideoHarness-SRSI improves the equally weighted mean held-out score by 6.2% relative to VideoHarness-BRSI and reduces the mean validation-test gap by 37.9%. Reliable harness evolution thus depends on how search is organized and informed, not only on how well it optimizes validation performance.

---

## 5. TimeRSI: Towards Self-Improved Agentic Deployment for Time-Series Foundation Models

**Authors:** Haoxin Liu, Deqing Fu, Lucheng Fu, ..., Harshavardhan Kamarthi, B. Aditya Prakash
**arXiv:** [2610.19725](https://arxiv.org/abs/2610.19725)
**Categories:** Machine Learning (cs.LG)

Time-series foundation models provide strong zero-shot forecast, but deployment for real-world applications still requires task-specific designs for model inputs and outputs. Direct inference can leave domain knowledge and recurring forecast errors unaddressed, while tailored pipelines require substantial human expertise and effort. We introduce TimeRSI, a self-improving agentic deployment system around frozen forecasting models. A coding agent translates task descriptions into executable pipeline changes. It tests each revision on historical forecasting windows and uses observed errors to guide subsequent revisions. During deployment, an adaptive selector chooses among the resulting pipelines using completed forecasts under similar conditions. Across 198 tasks on TIME and fev-bench, TimeRSI outperforms all submissions on six point and probabilistic forecasting metrics. Controlled comparisons support the value of feedback-guided revision over non-iterative pipeline search. Further experiments verify the generalization with different coding agents and forecasting models. Code is available at this https URL.

---

## 6. MMLA-RSI: Recursive Self-Improvement through RTT and RTMA

**Authors:** Junyi Zou, Avrova Donz
**arXiv:** [2610.20294](https://arxiv.org/abs/2610.20294)
**Categories:** Computation and Language (cs.CL); Machine Learning (cs.LG)

An agent can improve its behavior within an unresolved problem by changing how it acts and which experience it retains. We propose MMLA-RSI, a recursive self-improvement scheme with two implementations in Memory-Mediated Learning Architecture: Reasoning-Time Training (RTT) changes the policy state $\Phi$, while Reasoning-Time Memory Adaptation (RTMA) changes authoritative memory $M$. Each route also makes its adaptation method an object of improvement. A current numerical updater trains the policy proposing its successor; a current memory manager chooses the records available to the process proposing its successor. An independently admitted successor takes over the same role in the next generation. We give bounded executable rule languages, shared task/proposal interfaces, and one algorithm for either route or their composition. The RTT instance changes scalar schedules in a clipped-momentum update. The RTMA instance chooses NULL or a complete-row write with possible eviction. A fixed interpreter, trusted committer, and independent evaluator bound what can change. State versions, read closures, and conditional properties describe causal execution, accepted transitions, and finite work. Existing numerical-component studies motivate the construction. In four-candidate program selection, retaining LARC feedback updates reduces expected error by 24.65 and 36.65 percentage points for two trained initializations. In chronological continuous-integration replay, feedback binding is positive while retention increases loss. Completed SQL studies improve substantially over an unadapted substrate but do not establish the required additional online benefit. These results characterize their declared components. The two recursive routes and their joint realization are specified here; their beneficial recursive chains and discovery efficiency remain to be evaluated.

---

## 7. SafeDriveVLA: Navigation-Conditioned World Model Dreaming for Conflict-Aware End-to-End Autonomous Driving

**Authors:** Shaoyuan Xie, Zihan Zhang, Jingxuan Wang, ..., Henrik I. Christensen, Qi Alfred Chen
**arXiv:** [2610.20609](https://arxiv.org/abs/2610.20609)
**Categories:** Robotics (cs.RO)

Vision-Language-Action (VLA) models are gaining attention in autonomous driving, inheriting commonsense priors from large language models (LLMs) and widening the navigation interface from a fixed command set to free-form natural-language instructions. However, this open-ended interface exposes a new vulnerability surface: an inattentive driver may issue instructions that are unsafe given the current scene, and a malicious user may issue dangerous ones on purpose. We present the first benchmark suite that evaluates navigation following and conflict awareness together, along with adversarial robustness. Existing VLAs fall short on both: SimLingo completes no language-instructed lane change in closed loop, and all models degrade sharply under conflicting signals. We propose SafeDriveVLA, the first driving VLA that (1) explicitly predicts a three-level navigation-compliance mode to decouple conflict reasoning from action generation, and (2) uses navigation-conditioned world model dreaming to inform this prediction. Unlike prior world models that roll out expert or planned actions, ours dreams of strictly following the navigation signal, showing when following is safe. SafeDriveVLA reaches 88.16 Driving Score (DS) and 68.64% Success Rate (SR) on Bench2Drive, lifts closed-loop language following by 49.3% and reduces collisions under unsafe instructions from 60 to 38 compared to the best SimLingo variant. Video demonstrations are available on our project page.

---

## 8. Towards Agentic Robots: Model, Data, Environment, and Harness

**Authors:** Chonghan Qin, Dongming Wu, Kaituo Feng, ..., Yu-Gang Jiang, Xiangyu Yue
**arXiv:** [2610.20442](https://arxiv.org/abs/2610.20442)
**Categories:** Robotics (cs.RO)

Foundation models are driving a paradigm shift in robotic intelligence, moving beyond low-level action prediction to goal-directed orchestration of data collection, model training, task planning, and real-world execution. We characterize this emerging paradigm as an agentic robots, in which agents reason over human instructions, interact with robotic environments, rectify execution errors autonomously, and dynamically adjust operational strategies. Although this field develops fast, current studies are not well connected. Researchers have no consistent view of how to combine different agentic functions into a complete robot system. This paper provides a unified overview of existing research on agentic robots. We first trace the development from robot policies to agentic systems, covering vision-language-action models, world models, and world-action models. We then clarify the definition and scope of agentic robots and organize existing research into seventeen categories across four functional domains: Model, Data, Environment, and Harness. Across these domains, we examine how agents shape model learning and robot decisions, collect and curate robot data, construct worlds, tasks, and tests for learning and evaluation, and organize capabilities for robot use. Finally, we discuss open challenges and outline directions for future research. Looking forward, we hope this work contributes to a clearer understanding of agentic robots and supports new approaches to making them more capable, reliable, and adaptive.

---

## 9. ObjDream: Guiding Vision-Language-Action Models with Object-Level Understanding and Future State Prediction

**Authors:** Huailiang Ma, Yuxuan Li, Ziyi Zhao, ..., Cewu Lu, Jianhua Sun
**arXiv:** [2610.20223](https://arxiv.org/abs/2610.20223)
**Categories:** Robotics (cs.RO)

Vision-language-action (VLA) models have emerged as a powerful paradigm for robotic manipulation, enabling robots to generate actions from visual observations and language instructions. However, most existing VLA models still operate on image-level visual representations inherited from pretrained vision-language backbones, while lacking fine-grained object understanding for manipulation. As a result, their robustness can degrade under out-of-distribution object layouts, clutter, and background variations. To address these limitations, we introduce ObjDream, an object-centric VLA framework centered on object-level understanding and future object state prediction. ObjDream uses a spatio-temporal object encoder to organize visual observations into temporal object slots, where persistent object identity and dynamic object state are represented through separate channels. These structured object representations are inserted into the token sequence of the vision-language model (VLM), where identity-guided routing modulates VLM attention to the corresponding object tokens. In addition, an action-conditioned object dynamics module predicts compact future object states relevant to manipulation during training, explicitly supervising object state evolution under robot actions without requiring future prediction at inference. Experiments on LIBERO, LIBERO-Plus, and RoboTwin 2.0 show that ObjDream improves generalization under diverse distribution shifts and scene perturbations. Real-world robot experiments further demonstrate that ObjDream transfers to physical manipulation settings with novel object arrangements and background changes.

---

## 10. What Matters for World Modeling in Vision-Language-Action Models?

**Authors:** Qisen Ma, Yixiang Chen, Yuan Xu, ..., Yan Huang, Liang Wang
**arXiv:** [2610.19825](https://arxiv.org/abs/2610.19825)
**Categories:** Robotics (cs.RO); Computer Vision and Pattern Recognition (cs.CV)

Integrating world models into Vision-Language-Action models (VLAs) has emerged as a promising direction, enabling policies to anticipate future dynamics beyond reactive observation-to-action mapping. However, existing approaches vary simultaneously in their world representations, integration paradigms, and policy backbones, making it difficult to determine what truly matters for effective world model integration. To disentangle these factors, we categorize existing efforts into four representative paradigms, namely Implicit Future Alignment, Explicit Future Query, MoT Future Expert, and External World Predictor. We instantiate each within a unified framework and systematically evaluate these paradigms with diverse world representations and policy backbones across in-domain, out-of-domain, long-horizon, dynamic, few-shot, and real-world settings. Our study yields four main findings: 1) world representation effectiveness is paradigm-dependent, whereas 2D semantic representations offer robust, cross-paradigm gains; 2) no single paradigm is universally optimal, yet the decoupled MoT Future Expert offers competitive overall performance, particularly in OOD robustness; 3) world modeling consistently benefits policies built on standard VLMs, while decoupled designs exhibit greater compatibility with pretrained VLAs; and 4) world modeling improves performance over action-only baselines across multiple settings, with notable gains on long-horizon and dynamic tasks. Project page and video demonstrations are available at this https URL.

---

## 11. One-shot Human Video-Guided Adaptation for Vision-Language-Action Models

**Authors:** Qi Chen, Yuwei Wu, Quan Chen, ..., Zhi Gao, Yunde Jia
**arXiv:** [2610.19746](https://arxiv.org/abs/2610.19746)
**Categories:** Robotics (cs.RO)

Vision-language-action (VLA) models have recently achieved remarkable progress by leveraging large-scale robot datasets and foundation models for general-purpose robot manipulation. However, their ability to rapidly adapt to novel manipulation tasks beyond the training distribution remains limited. Existing approaches often require task-specific robot demonstrations and additional training, which are labor- and compute-intensive, limiting the scalability of VLA adaptation to open-world scenarios. To reduce this dependence on target-task robot data, we propose CapPro, a framework that enables a VLA policy to adapt to previously unseen manipulation tasks using only a single human demonstration video. CapPro consists of two components. First, a phase-aware human video representation module constructs a compact video representation through learned visual token selection and learns task-relevant query representations under phase-caption supervision. Second, a video-conditioned adaptation module jointly incorporates the compact video and query-derived representations into the action-conditioning context of the pretrained VLA policy. % This design introduces task-specific guidance while largely preserving the original VLA action-generation backbone. In this way, the human demonstration provides task-specific execution guidance rather than an embodiment-aligned trajectory to imitate, without requiring target-task robot demonstrations or target-task fine-tuning. Experiments across source and unseen target tasks show that CapPro improves average performance across unseen target groups while maintaining comparable performance on the source tasks. These results demonstrate the effectiveness of human-video guidance for cross-task VLA adaptation.

---

## 12. Accelerating VLA Inference with Perturbation Informed Execution

**Authors:** Jehun Lee, Hajun Lee, Jimin Ryu, ..., Jonghyun Choi, Jae-Joon Kim
**arXiv:** [2610.19656](https://arxiv.org/abs/2610.19656)
**Categories:** Robotics (cs.RO)

Action-chunking vision-language-action (VLA) models predict sequences of future robot actions. Under fixed-horizon execution, the robot executes a fixedlength prefix of each predicted chunk before invoking the policy again, leaving the remaining predictions unused. For a given number of executed actions, short execution horizons require more policy calls. Extending the execution horizon amortizes policy inference cost over more actions. However, uniformly applying long horizons across episodes can limit opportunities for precise corrections. To address this limitation, we propose PICES (Perturbation-Informed Chunk and Execution Horizon Selection), a training-free method that jointly selects an action chunk and the number of actions executed before the next policy call. Within a single policy call, the action expert generates a batch of action chunks from multiple initial noise samples and their locally perturbed counterparts, using the same conditioning features across all samples. PICES exploits differences between corresponding actions in each nominal chunk and its counterpart to determine candidate-specific execution horizons and select a nominal chunk for execution. Experiments on simulation benchmarks and real-world manipulation tasks demonstrate that PICES achieves speedup by up to 2.3x in wall-clock policy inference time on Jetson Orin and Thor relative to fixed horizon baselines while improving the success rate.

---

## 13. Cracking Mobile Manipulation: From Failure Diagnosis to Agentic Robot System

**Authors:** Zixuan Wang, Jia-Ning Li, Yinzhou Tang, ..., Xin Li, Yiwu Zhong
**arXiv:** [2610.19600](https://arxiv.org/abs/2610.19600)
**Categories:** Robotics (cs.RO)

Recent vision-language-action (VLA) models have shown strong performance on local robot manipulation, yet their success does not readily translate to long-horizon mobile manipulation. In our experiments, a pretrained subtask VLA achieves 80% success rate on atomic manipulation tasks but only 19% when these skills are composed into mobile manipulation. We argue that this gap stems from failures across the execution process rather than from local manipulation capability alone. To uncover these bottlenecks, we systematically diagnose failures in long-horizon mobile manipulation and identify three dominant regimes: task planning, navigation and base positioning, and local manipulation. Based on this diagnosis, we develop failure-guided agentic intervention that augments a fixed subtask VLA with demonstration-based planning guidance, adaptive visual memory, accessibility-aware base adjustment, and local end-effector adjustment. On RoboCasa365, these interventions progressively improve task success from 19% to 47%, with the finalized system reaching 49% on held-out episode seeds, compared with 18% for the baseline. The same design improves performance from 14% to 37% on BEHAVIOR-1K and from 5/20 to 13/20 on real-robot tasks. These results suggest that reliable mobile manipulation can be advanced by diagnosing and intervening on the current bottleneck, rather than uniformly scaling the underlying policy. Our code will be released at this https URL.

---

## 14. Robota-Embed: Unified VLA Embeddings for Robot In-Context Learning and Evolution

**Authors:** Yunze Liu, Jing Wang, Shenrui Wu, ..., Song Han, Han Cai
**arXiv:** [2610.19495](https://arxiv.org/abs/2610.19495)
**Categories:** Robotics (cs.RO); Computer Vision and Pattern Recognition (cs.CV)

Retrieving useful context for a robot requires matching its task, execution stage, and the continuation that should follow. We introduce Robota-Embed, to our knowledge the first vision-language-action (VLA) embedding model to jointly encode all three modalities in both current-state queries and recorded future continuations. Predictive retrieval training aligns these endpoints, enabling historical continuations to serve as context at inference time. We construct a multi-source corpus of 1,695,684 cleaned training anchors and introduce Robota-Embed-Bench, with 4,000 queries and a shared 8,000-entry gallery. Robota-Embed achieves 47.33% clip-level and 81.77% episode-level R@1, exceeding action-free Gemini Embedding 2 by 22.09 and 33.47 percentage points. Controlled retrieval studies show that removing native action degrades retrieval more than removing vision. We study two complementary applications. Embed2ICL uses retrieved experience for training-free and training-based policy conditioning, increasing success from 47.0% to 56.3% in DROID-Sim and from 86.4% to 92.8% on the LIBERO difficult subset, while improving task progress on real robots. Embed2Evolve uses execution feedback to grow task-local memory and refine context use around a frozen GPT-6 Astra policy. Across five ManiSkill tasks, it achieves 68% success, compared with 24% for GPT-6 Astra Direct and 33% for a harness independently evolved with Omni-Embed-Nemotron-3B under the same protocol. Relative to the latter, it uses approximately 79.5% fewer policy tokens per test rollout, counting both successes and failures. These results show that a unified, action-aware retrieval space can support robot in-context learning and task-local context evolution.

---

## 15. Paraphrase Consensus Is Not Self-Consistency: Instruction Reliance and Robustness in VLA Policies

**Authors:** Hanlong Li, Sihan Tan, Takeshi Ashizawa, Benjamin Yen, Kazuhiro Nakadai
**arXiv:** [2610.19438](https://arxiv.org/abs/2610.19438)
**Categories:** Robotics (cs.RO)

Vision-language-action (VLA) policies fine-tuned on LIBERO are trained and evaluated on the same ten instruction strings, and rewording the instruction changes base OpenVLA's success by -38.0 points. Test-time prompt ensembling, which improves language models, does not recover this loss in any setting we ran. Paraphrase consensus (the medoid action over K paraphrases) costs base OpenVLA 16.8 points when the training instruction is a member. Without it, the medoid of the paraphrases scores -32.4 points relative to the training instruction, and confidence-based selection scores -28.0. The same medoid over samples of one paraphrase improves on greedy decoding but stays -27.6 points below the training instruction, consistent with aggregation reducing variance without removing the bias the paraphrases share. A wrong-instruction probe measures how much of a policy's success depends on the instruction. Across three policies and four suites, paraphrases cost a policy only where this share is high, and the stronger policies lose a much smaller fraction of it than base OpenVLA. LoRA post-training on paraphrased instructions reduces the one-paraphrase effect to +2.0 points, against -32.0 for a matched control, reproduces across two seeds and on OpenVLA-OFT, transfers to withheld phrasings, and leaves the policy's reliance on the instruction unchanged.

---

## 16. PACER: Process-Aware VLA Policy Learning from Human Corrections for Robotic Disassembly

**Authors:** Chang Liu, Sibo Tian, Litian Gong, ..., Xiao Liang, Minghui Zheng
**arXiv:** [2610.19248](https://arxiv.org/abs/2610.19248)
**Categories:** Robotics (cs.RO)

Robotic disassembly of end-of-life (EoL) products requires robots to accommodate product variation, follow prerequisite sequences, and approach components precisely for contact-rich manipulation. Supervised fine-tuning (SFT) provides a practical path for adaptation, but limited and costly disassembly data cannot capture the distribution shifts arising from changing environments and product uncertainties. The policy's own rollouts record its approach attempts, and human corrections demonstrate recovery from its errors, but turning these experiences into better policy performance remains challenging. We introduce PACER, a Process-Aware Correction and Evidence Reweighting framework that learns from these experiences through SFT, using progress toward the target and each trace's source and outcome to weight valid action chunks in the native supervised action loss. PACER trains one policy per weighting setting and selects one of the resulting policies through held-out validation. We evaluate PACER on UR5e motherboard disassembly across five component classes, where it achieves 87/100 successful approach-and-handoff trials on the held-out benchmark, compared with 54/100 for vanilla post-SFT.

---

## 17. End-to-End Vision-Language-Action Policies for Autonomous Lunar Rover Docking

**Authors:** Sitan Huang, Grace Gao
**arXiv:** [2610.19224](https://arxiv.org/abs/2610.19224)
**Categories:** Robotics (cs.RO)

Surface navigation on the Moon is subject to extreme illumination contrast and deployment-time perceptual disturbances. While modular navigation pipelines have long supported planetary rover navigation, robustness is compromised by measurement errors that propagate through hand-engineered components. End-to-end learned policies are an alternative approach to navigation, which maps observations directly to control actions without intermediate components. Vision-language-action models, in particular, have driven significant breakthroughs in robotics and autonomous vehicle research. By leveraging internet-scale vision-language pretraining, these models can be exploited for their commonsense reasoning and visual understanding to provide robust generalization with limited task-specific data. However, their applicability and performance have yet to be characterized for lunar surface operations. In this study, we design a vision-language-action policy for autonomous lunar rover docking and characterize its performance relative to a modular navigation pipeline. We develop a scalable training framework that generates safety-aware expert demonstrations in a high-fidelity lunar simulation environment. In closed-loop evaluations, our policy performs competitively relative to the modular baseline under perceptual disturbances unseen during training. To address the tradeoff between compute consumption and closed-loop safety, the policy adapts its execution horizon by determining how far the rover may safely travel in open loop. Adaptive-horizon execution reduces inference frequency while limiting hazard-contact rates relative to fixed horizons in the evaluated scenarios.

---

## 18. AdaRSI: On-Demand Recursive Self-Improvement for Embodied Agents

**Authors:** Peidong Wang, Ying Chang, Zhiming Ma, ..., Jian Su, Daling Wang
**arXiv:** [2610.20474](https://arxiv.org/abs/2610.20474)
**Categories:** Computation and Language (cs.CL); Robotics (cs.RO)

Pretrained vision-language-action models (VLAs) often fail midway through unseen long-horizon tasks. Recursive self-improvement (RSI) offers a remedy, but embodied RSI methods either refine the harness around a frozen executor and so cannot add a missing motion, or train the executor on persistent failures without asking whether a failure lies in how the executor is called or in what it can do. We ask when a self-improving embodied system should change the weights of its executor, and propose AdaRSI, an on-demand RSI framework for embodied agents. A coding agent first improves its skills and harness, then attributes persistent failures by retrying failing sub-steps from saved states, and fine-tunes only the sub-steps that remain unreliable, with demonstrations it collects itself and experience carried over from earlier tasks. On all 50 target tasks of RoboCasa365, with GR00T N1.5 as the executor and no human demonstrations, AdaRSI improves the VLA on all three suites and raises its success on unseen composite tasks from 4.6% to 13.8%. Compared with fine-tuning every sub-step, it reaches slightly higher success while using only 28% of the GPU time and 22% of the self-collected demonstrations, and fine-tuning without a harness trains more yet gains far less.

---

## 19. SPECTRA-VLA: Base-Fine Hyperspectral Token Transfer at Frozen Vision-Language-Action Interfaces

**Authors:** Chih-Chung Hsu
**arXiv:** [2610.19651](https://arxiv.org/abs/2610.19651)
**Categories:** Computer Vision and Pattern Recognition (cs.CV)

Hyperspectral imaging distinguishes RGB-similar objects, but a pretrained vision-language-action model needs a state its frozen decoder can use. SPECTRA-VLA provides a native-width spectral upgrade without retraining the visual encoder or action decoder. A learned continuous residual enriches each target token through its own normalized false-color reference; projection, norm control and validation-calibrated injection regulate the change. Across 86 held-out acquisitions, category balanced accuracy rises from 0.812 to 0.883. With identical residuals and scale, own-token addition improves reuse of an external category-derived probe on frozen decoder logits: 0.701 versus 0.590 with pooled replacement, at similar image-disjoint recognition. Five grouped tests covering the same 86 acquisitions recover within-category spectral shape with $R^2=0.802/0.337$ from continuous and posterior-code states. Category-matched spectral swaps further show that own-token composition approximately doubles the target-specific recovery increment after frozen decoding. Spectral enrichment and receiving-token preservation thus work together at the pretrained interface.

---
