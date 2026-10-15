# arXiv Daily Digest — 2026-10-14

**Mode:** direct
**Categories:** cs.AI, cs.LG, cs.RO, cs.CV
**Keywords:** VLA, RSI, agentic robot, self-improving robot, self-evolving robot, robot harness
**Papers found:** 42

---

## 1. Who Improves the Robot? Toward Physical Recursive Self-Improvement

**Authors:** Hai Zhou, Fan Yang, Zeyi Chen, ..., Qian Feng, Shangding Gu
**arXiv:** [2610.18842](https://arxiv.org/abs/2610.18842)
**Categories:** Artificial Intelligence (cs.AI); Machine Learning (cs.LG); Robotics (cs.RO)

Robots are increasingly autonomous in task execution, yet their improvement remains largely human-driven. This study investigates Physical Recursive Self-Improvement (Physical RSI), in which physical experience guides lasting updates to both a robot's capabilities and its improvement procedure, making subsequent improvement more effective across tasks. Physical RSI faces challenges from noisy observations, continuous dynamics, costly trials, and irreversible consequences. We present an L0-L5 framework that differentiates capability-level from meta-level updates and within-task from across-task gains, reserving L5 for independently verified recursive gain. We study existing methods around harness adaptation and model training, alongside safety and control mechanisms that govern execution and successive updates. Our analysis reveals that, despite substantial progress in self-improvement, the surveyed literature does not yet demonstrate Physical RSI as defined by our framework. We identify research priorities in reliable feedback, causal attribution, safety preservation, and benchmarking, outlining a path toward robots that autonomously improve how they learn while ensuring safety. The GitHub repository for Physical RSI is available at this https URL.

---

## 2. AReaL-RSI: Adaptive Scaling and Coordination of Recursive Self-Improvement

**Authors:** Wenhao Zhou, Jiajun Song, Haitao Wang, ..., Yi Gao, Binhang Yuan
**arXiv:** [2610.18083](https://arxiv.org/abs/2610.18083)
**Categories:** Artificial Intelligence (cs.AI)

Scaling recursive self-improvement requires additional computation to produce useful research progress in reaching persistent objectives. Intuitively, more researcher agents can explore more hypotheses, but early evaluation scores might misrepresent their promise, shared findings could lose their applicability conditions, and useful procedures could remain confined to completed investigations. In this paper, we present AReaL-RSI, a framework for organizing a persistent research team of agents without updating backbone LLM weights. We formulate the scaling problem in terms of evaluated outcomes and whole-system resource expenditure. Concretely, a leader agent selects task-appropriate research orientations and guides ongoing investigations; conditional memory sharing distinguishes unresolved problems from supported findings and enables recipient adaptation. During recursive evolution, after each campaign, evidence-based review revises researcher orientation, knowledge, and skills for later campaigns. Experiments compare AReaL-RSI with Codex-Goal on downstream harness optimization, GPU kernel optimization, and AI research tasks using two backbones. Under the reported resource allocations, AReaL-RSI improves Terminal Bench performance by 2.2 percentage points for each backbone and increases mean KernelBench speedup by 32.2-36.8%; further scalability comparisons favor the design of AReaL-RSI over native scaling: combining experience sharing with specialized researcher roles yields 1.9-27.5% lower kernel latency than independent exploration and 1.3-33.9% lower latency than sharing alone across all seven comparable task-backbone pairs.

---

## 3. ECG-RSI: Recursive Self-Improvement through Targeted Electrocardiogram Waveform Evolution

**Authors:** Xiaoliang Wang, Zhuo Chen, Chuanyang Zheng, ..., Jian Wang, Lijun Wu
**arXiv:** [2610.17718](https://arxiv.org/abs/2610.17718)
**Categories:** Artificial Intelligence (cs.AI); Machine Learning (cs.LG); Signal Processing (eess.SP); Quantitative Methods (q-bio.QM)

Electrocardiogram (ECG) models need supervision that targets evolving weaknesses and remains faithful to waveform evidence. We introduce ECG-RSI, a recursive self-improvement framework combining verified waveform synthesis with feedback-guided intervention search. Signal remeasurement verifies waveform edits; construction errors guide generator repair, while learner errors motivate interventions compared on a separate selection set. Across seven benchmarks, three rounds raise Qwen3.5-35B-A3B's mean question-answering accuracy from 34.57% to 56.04% and mean classification F1 from 24.27 to 34.03. Across the retained trajectory, the preferred supervision shifts from direct reinforcement to confusion-focused contrasts. Continued feedback correction yields diminishing external gains. These results motivate separating error diagnosis from intervention selection and checking whether gains on the feedback set transfer to independent benchmarks.

---

## 4. TacitVLA: Reasoning Vision-Language-Action Models Without Reasoning Latency

**Authors:** Jack Lu, Yurong You, Boyi Li, ..., Marco Pavone, Yan Wang
**arXiv:** [2610.17540](https://arxiv.org/abs/2610.17540)
**Categories:** Artificial Intelligence (cs.AI); Robotics (cs.RO)

Textual reasoning before acting has improved vision-language-action (VLA) models, but at the cost of latency: every action conditioned on the reasoning text must wait for autoregressive decoding. We show that actions do not need to wait for or condition on the generated reasoning to benefit from it, because the reasoning supervision already improves the backbone representation. We introduce TacitVLA, a reasoning VLA whose action expert never attends to the reasoning it generates for the current call. On long-horizon tasks where the reasoning text also serves as episodic memory, it can generate each entry during action execution rather than before acting. We evaluate it in a controlled study on four benchmarks spanning manipulation and autonomous driving, memory and non-memory tasks: RoboMME, RMBench, LIBERO, and PhysicalAI-AV. On all four, TacitVLA matches the performance of its explicit-reasoning counterpart at up to 3.4x lower latency, and matches the latency of the same architecture trained without reasoning at up to +17.1% success. In absolute terms, it surpasses the best previously published results on the RoboMME Counting suite (82.7% vs. 66.8%) and RMBench (77.5% vs. 56.5%), and reaches 72.9% on LIBERO-Plus and a 52.5% scene score on the public split of the PhysicalAI-AV closed-loop driving challenge. Project page: this https URL.

---

## 5. SpecForge: Recursive Self-Improvement for Coding Agents via Behavioral Specifications

**Authors:** Yutong Cheng, Haifeng Chen, Peng Gao, Wei Cheng
**arXiv:** [2610.15708](https://arxiv.org/abs/2610.15708)
**Categories:** Artificial Intelligence (cs.AI); Software Engineering (cs.SE)

Coding agents based on frozen language models can improve their performance by refining the external context they rely on, without updating model weights. We study recursive self-improvement through behavioral specifications: natural-language code documentation that describes the behavior of program entities and guides agents in generating correct code. We formulate a self-improvement loop in which an agent generates code from its current specifications, evaluates it with execution-verified tests, and refines the specifications based on observed failures. The improved specifications then guide subsequent generation, progressively improving the agent's understanding of the codebase. However, recursive refinement is challenging because program entities are interdependent. Improving the specification of one entity can inadvertently degrade the correctness of others, a phenomenon we call output coupling. This creates a whack-a-mole effect in which local improvements cause regressions elsewhere, preventing consistent progress. We introduce SpecForge, a multi-frontier tree search framework that addresses this challenge with three mechanisms: (i) Pareto-guided state selection preserves complementary specification states and prevents premature commitment; (ii) dependency-constrained entity selection prioritizes callee-before-caller refinement; and (iii) error-diversified expansion explores multiple refinements using different subsets of test failures. On DevEval+, SpecForge achieves the best performance across five backbone models, including a 94.9% solve rate with Claude-4.5-Sonnet and a 5.7-percentage-point average improvement over the strongest baseline. The improved specifications also make the agent better at tasks outside the loop: they transfer to cross-language translation and to new-feature implementation, where they outperform the benchmark-provided requirement documents.

---

## 6. Pre-Registered Genesis Accounting for Recursive Self-Improvement: First Audited Operator-Genesis Events in a Physics-Discovery Runtime

**Authors:** Wenbin Mao, Pei Zou
**arXiv:** [2610.14843](https://arxiv.org/abs/2610.14843)
**Categories:** Artificial Intelligence (cs.AI)

Claims of recursive self-improvement are easy to make and hard to falsify: did improvement come from re-using designer-provided mechanisms, or from mechanisms the system authored itself? We introduce a pre-registered, two-tier accounting: M1 counts machine-generated content instances within a designer-provided vocabulary, while M2 counts machine-authored mechanism types (new operators registered into the runtime's own vocabulary, with a held-out-validation certificate). We report the first audited M2 genesis events. In the primary event, depth-limited compositional search over elementary operators, judged by held-out R^2 on real NIST hydrogen Balmer measurements, produced the operator sq(inv(n)) = 1/n^2 -- the Rydberg-level form -- which no standard-library transform could express (held-out R^2: -0.546 best standard transform vs. 1.0000000 composed). A protocol flaw (independent variable built by inverting the very law under test) was caught in audit and repaired via an independent-label protocol; extrapolation to unseen levels (n=8,9 trained on n<=7) attains relative error ~10^-6, four to six orders beyond the best standard operator. A second event independently recovered sqrt(inv(a)) -- Kepler's velocity law -- from JPL ephemeris vectors. Also incorporated: an audited compounding channel (first domain-level measurement: 1.109x accuracy ratio on a real held-out domain) and blind, decurated genesis exams whose honest tally is zero. The Kepler event passes line audit; the hydrogen gap reproduces on He II; the certificate is threshold-stable. Against eleven prior systems, the contribution is the measurement and governance of machine-authored mechanisms, not the search algorithm or rediscovered physics. Limitations: exams were curated by agents who knew the textbook answer, triggers manual, grammar observer-injected; both events demonstrate capability to author, not yet autonomous genesis.

---

## 7. From Existing Methods to New Research Ideas: Two Perspectives on Recursive Self-Improvement

**Authors:** Leijun Zhou, Yanke Yu, Zhihao Liu, ..., Yaowei Zheng, Junhao Hu
**arXiv:** [2610.14625](https://arxiv.org/abs/2610.14625)
**Categories:** Artificial Intelligence (cs.AI)

Recursive self-improvement (RSI) offers a route to AI systems that participate in their own continued development. Recent methods allow language agents to retain changes to their parameters, memory, skills, and code for subsequent execution and improvement. We examine how these methods can inform new research ideas through two complementary perspectives. First, we introduce a unified taxonomy with nine design dimensions organized into four groups: update targets, update organization, update schedule and scope, feedback and selection. This taxonomy places existing methods in a shared design space, where examining individual dimensions and their interactions can inspire new research ideas. Second, we examine how existing RSI methods draw on traditional deep learning, for example through optimization, regularization, data augmentation, continual learning, and adversarial learning. We develop further ideas by examining more specific learning mechanisms and drawing on evolutionary computation. We also review how existing benchmarks assess self-improvement under online, offline, and offline-to-online settings. Together, these perspectives help researchers develop new RSI research ideas from existing designs and learning mechanisms. RSI papers and resources are available at this https URL.

---

## 8. Reels-RSI: Program-Level Self-Improvement for Code-Rendered Explainer Videos

**Authors:** Wei Lin
**arXiv:** [2610.14495](https://arxiv.org/abs/2610.14495)
**Categories:** Artificial Intelligence (cs.AI); Graphics (cs.GR); Multimedia (cs.MM); Software Engineering (cs.SE)

Explainer videos -- a worked geometry problem, why the sky is blue, how a dynasty fell -- are usually one more target for pixel video generation. We argue they are a different kind of artifact: a program (script, storyboard and per-frame animation code) that a deterministic renderer turns into frames. A program can be read, diffed, tested and audited; pixels can only be watched. Reels-RSI is an open-source reel director for any agent harness; its self-improvement happens at the program level rather than in weights or prompts. Every revision pass is logged with a code snapshot; a retrospective pairs each check finding with the diff that fixed it and proposes lessons; a lesson that a static check can catch is compiled into a rule with a must-fail and a must-pass example, so the memory is unit-tested; and a rule learned today runs over everything made before it. A bounded, benchmark-gated step lets an agent rewrite the director's playbook, kept only when blind pairwise judgments on held-out topics prefer it; nothing enters memory without a human decision. Across 111 reels -- a field study, two playbook evolutions, a 2x2 memory ablation, a weaker director, a 48-reel learning curve and a judge-reliability study -- we find that the rule learned in the field caught four latent defects in frames authored before it existed and none after; that rules are an audit for a strong director (eight unguarded reels, no violation) and a guard for a weaker one (thirty violations unguarded versus five); that lessons shorten revision loops but do not compound or move the judge; and that the first rewrite's 11--1 verdict was a position bias in our vote design (judges pick the second-shown reel 62--81% of the time), masking scripts that traded thirteen facts for craft. We document four failure modes of the preference signal, which check caught each, and the fixes. Code, rules, lessons and data are public.

---

## 9. ChunkAct: Action Chunking for Agentic Robotics

**Authors:** Bingxin Xu, Wenrui Bao, Xinxin Liu, ..., Yuzhang Shang, Emilio Ferrara
**arXiv:** [2610.18874](https://arxiv.org/abs/2610.18874)
**Categories:** Robotics (cs.RO); Artificial Intelligence (cs.AI); Computation and Language (cs.CL); Computer Vision and Pattern Recognition (cs.CV)

Agentic robotics places a large language model (LLM) agent in the robot control loop, where it composes perception, motion, and vision-language-action (VLA) tools under the guidance of a memory and thereby generalizes to new tasks without retraining. This generality comes at a steep price in efficiency. Every primitive requires a round of LLM reasoning over the full interaction history, so the cost of an episode grows with the number of primitives. We find this reasoning largely redundant: once a sub-goal is chosen, its primitives follow a routine already prescribed by memory. We present ChunkAct, which introduces action chunking to agentic robotics. Online, a single call launches a chunk of chained primitives, which executes autonomously and returns control only upon failure. Offline, ChunkAct compiles the memory into these chunks, so execution is memory-free at test time and the planner is reserved for decisions that require reasoning. LLM computation therefore scales with the number of decisions rather than the number of primitives. On LIBERO-Pro, ChunkAct improves task success by 5.0 points over the state of the art in agentic robotics while requiring 2.9x fewer LLM calls, 4.4x fewer input tokens, and 2.3x fewer output tokens.

---

## 10. What Matters in Quality-Aware VLA Pretraining: A Benchmark and Empirical Study

**Authors:** Mingxuan Yan, Litian Gong, Dihong Huang, ..., Jianfei Yang, Jiachen Li
**arXiv:** [2610.18869](https://arxiv.org/abs/2610.18869)
**Categories:** Robotics (cs.RO); Artificial Intelligence (cs.AI); Machine Learning (cs.LG)

How should demonstration quality be used during vision-language-action (VLA) pretraining to improve performance after target-task fine-tuning? We compare weighting, filtering, and conditioning across reward definitions and label granularities using 5,000 naturally suboptimal human demonstrations and 24 target tasks. Within each VLA, we match demonstrations and training budgets. Additional comparisons examine pretraining data size and the roles of quality tags during fine-tuning and inference. Across three VLAs, we find that approach-aware episode conditioning improves mean success over plain behavioral cloning; conditioning and filtering favor episode and chunk labels, respectively, on average, with model-dependent reversals; and constant-tag fine-tuning improves mean success after conditioned pretraining with either tagged or untagged inference. We introduce AXIS-Bench to support these controlled comparisons. Built on crowdsourced simulation demonstrations, it provides recorded object and contact states for recomputing quality labels on shared trajectories. Replayable trajectories support workspace-aligned rendering and user-defined real-world target tasks. In our real-world experiment, simulation pretraining raises success from 9.6\% to 31.7\%. Project page: this https URL.

---

## 11. LIBERO-RIG: A Hardware-Setup Robustness Benchmark for Vision-Language-Action Models

**Authors:** Andrea Yaoyun Cui, Hanyu Wang, Xinyi Wang, ..., Dejia Xu, Matthew Tancik
**arXiv:** [2610.18843](https://arxiv.org/abs/2610.18843)
**Categories:** Robotics (cs.RO); Artificial Intelligence (cs.AI)

Robot policies are expected to generalize across deployment environments, including variations in the robot itself: cameras are bumped and remounted, calibrations drift, controllers run at different rates, and end-effector pads wear down. We present LIBERO-RIG, a benchmark that perturbs only the robot's hardware and setup while holding every LIBERO task fixed. The benchmark spans eleven perturbation axes, including camera mounting and optics, camera-to-arm calibration, actuation gain, control rate, proprioceptive noise, base pose, table height, and gripper pads. Each axis has five severity levels, yielding 210 conditions across the four LIBERO suites. We evaluate nine recent vision-language-action models using 500 episodes per condition and substantiate each finding with rigorous statistical tests. Pooled success falls from 0.932 to 0.767 at the middle severity and 0.509 at the highest severity. Performance degradation varies substantially across perturbation axes and action interfaces, and training on visual perturbations does not mitigate faults that leave camera images unchanged. We release the benchmark together with manifests specifying the fixed perturbation parameters for each episode.

---

## 12. SEAR: Self-Evolving Agentic Robotics

**Authors:** Xinyi Wang, Bangzheng Li, Hanyu Wang, ..., Shyamal Buch, Dejia Xu
**arXiv:** [2610.18792](https://arxiv.org/abs/2610.18792)
**Categories:** Robotics (cs.RO); Artificial Intelligence (cs.AI); Computation and Language (cs.CL)

Frontier language-model agents can now improve robots on their own: they write control code, test it, and keep what works as skills and memories for the next task. We introduce SEAR (Self-Evolving Agentic Robotics), a framework and benchmark built around two questions. Is the agent really learning, or just trying more often? And does what it learns still help on new tasks, in a new simulator, and on a real robot? The framework runs an agent in three modes: it writes code that becomes the policy (code-as-policy), acts live in the control loop (agent-as-policy), or works as a researcher that fine-tunes a vision-language-action model (auto-research). The benchmark adds controls that separate retained experience from repeated attempts, familiar tasks, privileged simulator state, larger budgets, and luck. Across seven frontier language models, 330 simulated and five physical tasks, and over four years of agent runtime, we highlight three findings. First, the learning curve of a robotic agent depends both on the overall time budget and the task difficulty relative to model capability. Harder tasks make longer sessions worthwhile; on easier tasks, re-rolling short attempts does just as well. Second, control code and shared routines transfer across tasks and simulators, while task-specific solutions do not. On a real robot, we observe a performance gap between agent-designed practice and novel human-designed scenes. Third, different models evolve more effectively in different ways. Some do best acting live, others writing code first. And a text-only model keeps pace with a comparable multimodal one: perception helps with error assessment, but agentic reasoning and tool use can matter more. We release the benchmark and codebase to support future research.

---

## 13. D-World: An Explicit World-Language-Action Model with Recursive Self-Improvement under Dual Control

**Authors:** Xuan Wen, Baichao Wang
**arXiv:** [2610.17114](https://arxiv.org/abs/2610.17114)
**Categories:** Robotics (cs.RO); Artificial Intelligence (cs.AI)

Frontier large language models (LLMs) now reason about space well enough to program robots, yet the world models behind robot policies are implicit, held in network weights or predicted video, and cannot be inspected or corrected directly. We present D-World, an explicit world-language-action model built on the Sense, Plan and Act decomposition. A perception agent writes the scene as an executable digital twin using generated vision and geometry code. A planning agent searches for actions in simulation and, after each executed action chunk, revises the twin's object states and named physical parameters against what the robot measured. A parameter revision is accepted only if replaying the latest chunk does not increase any measured residual beyond its tolerance, and every chunk is checked in the updated twin before it runs. Structural mismatches return to perception for reconstruction. We call this measurement-grounded cycle of correction and revision recursive self-improvement (RSI), in which the LLM stays frozen while the world it acts in improves. We model the choice of actions that both advance the task and expose model error as a dual control problem and show that the cost of incorporating evidence into the twin sets the threshold at which probing pays, so cheap local revision counteracts the turn-off of cautious controllers. Each episode runs a real-to-sim-to-real loop, and its recorded twins can be refitted and re-rendered offline into higher-fidelity environments for post-training. Because perception and planning communicate only through the twin and language, either can be replaced by a learned model, and since inference dominates the loop, the loop speeds up with faster models. On a dual-arm robot, towel and toaster tasks show local revisions, such as one reducing the bread's rendered-depth residual from 22.4 to 1.5 mm, that let execution continue without reconstruction.

---

## 14. AUGUstus: Autonomous Driving VLA Model with Unified Generation and Understanding

**Authors:** Yuqi Ye, Caigao Jiang, Zhuonan Wang, ..., Honggou Yang, Wei Gao
**arXiv:** [2610.16985](https://arxiv.org/abs/2610.16985)
**Categories:** Computer Vision and Pattern Recognition (cs.CV); Artificial Intelligence (cs.AI)

Vision-language-action (VLA) models show strong potential for end-to-end autonomous driving by leveraging world knowledge and understanding to excel in long-tail scenarios. However, current VLAs have two limitations: 1) Degeneration into vision-action (VA) models. For low latency, regression/flow-based methods directly generate actions but underuse VLM understanding, causing unsafe, unexplainable actions. 2) Autoregressive high latency. Autoregressive methods sequentially generate chain-of-thought (CoT) and action tokens, fully leveraging VLM understanding, but high latency hinders deployment. To enable low-latency deployment while using CoT to assist action generation, we propose AUGUstus, an Autonomous-driving VLA model with Unified Generation and Understanding. We unify diffusion-based action generation and autoregressive CoT understanding in one model, where understanding only serves generation. Joint CoT supervision preserves VLM spatial understanding in shared representation for safer, more accurate trajectories. AUGUstus-mode orders action generation before CoT, so CoT supervises reliable actions during training while inference needs only action output, enabling low latency. AUGUstus-GRPO, a unified GRPO algorithm, jointly optimizes action and CoT, improving action performance. Experiments show AUGUstus achieves 94.6 PDMS on NAVSIMv1 and 90.7 EPDMS on NAVSIMv2, SOTA planning without scorer module. On nuScenes, it achieves average L2 error 0.27 m and average collision rate 0.05%, best among compared methods. To validate AUGUstus practicality, we train on in-house data with 512 NVIDIA H800 GPUs for ~2 days, evaluate on an internal 1,000 km dataset, and preliminarily deploy on a real vehicle, achieving 12 Hz operation. Project page: this https URL

---

## 15. VLA-GAUGE: Systematically Evaluating Generalization and Robustness in Vision-Language-Action Models

**Authors:** Jun Xiao, Rui Ye, Dong Cao, ..., Ying Wang, Zhiliang Zhu
**arXiv:** [2610.16567](https://arxiv.org/abs/2610.16567)
**Categories:** Computer Vision and Pattern Recognition (cs.CV); Artificial Intelligence (cs.AI); Robotics (cs.RO)

Vision-Language-Action models (VLAs) have achieved high success rates on familiar manipulation tasks, yet it remains unclear whether such scores reflect genuine zero-shot generalization and perturbation robustness. Existing evaluation frameworks provide limited capability-level diagnosis and combinatorial perturbation coverage, often without connecting diagnosis to targeted model refinement. We introduce VLA-GAUGE, a diagnostic framework that unifies both evaluations under a shared executable task representation. It combines (1) paired in-distribution and out-of-distribution tasks across six capability suites, (2) single-factor sensitivity analysis with combinatorial perturbation screening and evaluation, and (3) diagnosis-driven refinement through targeted data augmentation and model fine-tuning. We evaluate 12 VLAs spanning different model sizes and action-modeling paradigms under a unified protocol. We find that (1) The mean Zero-Shot Score on VLA-GAUGE is only 22.3%, with SimpleVLA-RL scoring 8.0% and ranking second to last among the evaluated models. (2) Under three representative combinatorial perturbation configurations, the mean R-Score is 9.3. (3) Diagnosis-driven fine-tuning improves $\pi_{0.5}$'s zero-shot generalization and robustness under a selected perturbation combination on held-out scenarios by 72.4 and 31.8 scoring points, respectively; the latter exceeds the 10.9-point gain from LIBERO-Plus single-factor fine-tuning despite fewer successful training trajectories. These results show that high reported success rates on familiar manipulation tasks do not guarantee strong zero-shot generalization to unseen tasks or robustness to combinatorial perturbations, while diagnostic evaluation provides actionable signals for targeted model improvement.

---

## 16. Drafting Agents, Not Just Tokens: Speculative Recursive Self-Improvement for Agentic Systems

**Authors:** Xin Xu, Ke Cheng, Hao Wang, ..., Jie Jiang, Zhouchen Lin
**arXiv:** [2610.16491](https://arxiv.org/abs/2610.16491)
**Categories:** Machine Learning (cs.LG); Artificial Intelligence (cs.AI)

Improving an agent through successive revisions requires balancing exploration and evaluation under a limited budget. A narrow search can miss useful sequences of edits, while fully evaluating every intermediate version can exhaust the budget before those sequences yield a verified improvement. We introduce Speculative Recursive Self-Improvement (SpecRSI), which drafts executable successor agents before their predecessors are fully evaluated, while requiring complete verification before adoption. Verification-Aware Tree Search (VATS) allocates the budget between further edits and outstanding checks using the predicted verified return of a continuation. Group Verification Optimization (GVO) learns the improver from completed searches while keeping the real evaluator fixed. In the main scientific comparison, terminal gains exceed Janus by 33.3%--40.0%. Additional evaluations show that SpecRSI outperforms Janus in all 50 scientific backbone--task pairs and exceeds MetaRSI-v1 by 1.85%--2.38% in macro-average system score across twenty backbones. Coding-validation success reaches 69.4% versus HGM's 64.3% at a 20.8% lower target-cost index.

---

## 17. RoboHarness: A Simple Harness Outperforms VLA and World Actions Models

**Authors:** Bince Qu, Wei Chen, Bo Zhang
**arXiv:** [2610.14018](https://arxiv.org/abs/2610.14018)
**Categories:** Robotics (cs.RO); Artificial Intelligence (cs.AI)

The rise of large language models (LLMs) has opened a path toward generalist embodied AI, raising the question of how LLMs can act in the physical world. One straightforward approach is training the model to generate actions: collect robot-action data and video demonstration, refine LLM architecture with an action head, and train a vision-language-action (VLA) model at scale. However, we argue that coding agents have the potential to realize generalist embodied manipulation. All they need is a simple yet effective robot harness. We present RoboHarness: a robotic harness that gives LLM agents a visual-geometric control panel so that they can directly understand and invoke embodied tasks. With RoboHarness, Qwen3.8-Flash-Next outperforms state-of-the-art VLA models on BEHAVIOR Challenge 2025 tasks. The implementation will be released as open source.

---

## 18. Trust-Calibrated VLA Policy Post-Training with Evolving Imagination

**Authors:** Wenzhan Li, Yiran Qin, Heng Zhou, ..., Yulan Guo, Ruimao Zhang
**arXiv:** [2610.16517](https://arxiv.org/abs/2610.16517)
**Categories:** Robotics (cs.RO); Machine Learning (cs.LG)

Vision-Language-Action (VLA) models are often pretrained via imitation learning, making reinforcement learning (RL) post-training important when deployment moves beyond demonstration coverage. Existing refinement paradigms expose a reliability--efficiency tension: model-free refinement avoids simulator bias but is interaction-intensive, whereas model-based refinement can exploit unreliable imagination even as its simulator adapts. We propose Model-Evolving Reinforcement Learning (MERL), a trust-calibrated framework that couples policy optimization with an online-updated simulator comprising a world model and a reward proxy head. Across stages, simulator reliability controls the imagined-data ratio and rollout horizon; within rollouts, chunk-level trust controls replay selection and optimization weight. For recursive imagination without exact grounded continuations, a residual predictor estimates trust without querying future ground truth. On perturbed LIBERO-PRO tasks, MERL reaches 79.7% average success, improves high-threshold learning speed by 10.9% over the matched model-free control, and outperforms same-protocol external baselines across three training seeds. Fixed-data adaptation from 50 demonstrations per task achieves 80.0% average success on two physical-robot tasks.

---

## 19. CoLA: Multi-VLA Coordination via Learned Adapters

**Authors:** Ahaskar Kashyap, Jiawen Zong, Boyu Ma, ..., Stefano V. Albrecht, Jianfei Yang
**arXiv:** [2610.15337](https://arxiv.org/abs/2610.15337)
**Categories:** Robotics (cs.RO); Machine Learning (cs.LG); Multiagent Systems (cs.MA)

Vision-Language-Action (VLA) models are typically deployed as isolated single-agent policies. When several such agents share a workspace, they can coordinate implicitly, by observing one another, or explicitly, by exchanging messages, but it remains unclear when explicit communication becomes necessary. We introduce CoLA (Coordination via Learned Adapters), which keeps each agent's VLA backbone frozen and trains a lightweight message channel and a per-arm diffusion action head on top, with fully decentralised execution. Across three tasks that differ in how much each agent can observe, the channel matters only when information is private. On an occluded tray handover, where the box's colour marker is visible to one agent only, CoLA reaches 76.0% success versus 1.3% with messages zeroed throughout training. On two-arm and three-arm handover tasks, removing messages has no measurable effect with a shared overhead camera (90.6% vs. 88.3% at two arms; 63.5% vs. 60.0% at three), but lowers success on the two-arm task's wrist-only variant (74.8% vs. 64.3%). This architecture generalises across different VLA backbones as well. With a frozen $\pi_{0.5}$ backbone on the same occluded tray task, CoLA matches the overall success rate of a LoRA-fine-tuned baseline (37.3% vs. 34.7%) using a fraction of the trainable parameters. When CoLA places the box, it selects the correct tray 71.8% of the time, whereas the independently fine-tuned baseline, whose placing arm never sees the marker, selects it at chance level (34.7% against 33.3%).

---

## 20. ForkCast: Predictive Recovery for Vision-Language-Action Policies via Counterfactual Futures

**Authors:** Chenru Wen, Huajian Zeng, Haokai Ding, ..., Dezhen Song, Xingxing Zuo
**arXiv:** [2610.18650](https://arxiv.org/abs/2610.18650)
**Categories:** Robotics (cs.RO)

Vision-language-action (VLA) policies perform manipulation tasks using camera images and language instructions, but object slip or visual occlusion can disrupt execution. Recovery is typically learned during policy training or delegated to a monitor that triggers a scripted repair after detecting a failure. We introduce ForkCast, a predictive recovery framework that compares counterfactual futures to determine whether and how to intervene in a frozen VLA policy. At each decision point, ForkCast evaluates three candidates: executing the policy's nominal action chunk (Commit), adjusting the camera viewpoint (Reobserve), and replanning the arm trajectory (Replan). A candidate-conditioned world model forecasts the latent outcome of each candidate at a common future horizon, and a shared task-progress head scores the predicted outcomes. By evaluating the policy's own continuation alongside the repair candidates, a single comparison based on task progress determines both whether and how to intervene, without a failure detector, an intervention threshold, or updates to the VLA backbone. On five simulated RoboTwin 2.0 tasks with injected occlusion and object slip, ForkCast increases pooled success from 13.3% for the frozen $\pi_{0.5}$ policy to 30.0% and transfers to two additional VLA backbones without updating ForkCast. After adaptation on real-robot candidate rollouts, ForkCast also improves success over the base policy under both clean and visibility-limited conditions. Code will be released to benefit the research community.

---

## 21. WAVE-0: Bridging VLA Policies and WAMs with Lightweight Latent Future Prediction

**Authors:** Haomin Wang, Anqiong Ji, Ke Wang, ..., Ran Zheng, Zhipeng Zhang
**arXiv:** [2610.18568](https://arxiv.org/abs/2610.18568)
**Categories:** Robotics (cs.RO)

Vision-language-action (VLA) policies excel at generalist robotic manipulation but generate actions without explicitly modeling their environmental consequences. World action models (WAMs) incorporate future prediction, yet most rely on costly video generation, while latent alternatives either use predicted futures only as auxiliary targets or infer latent actions from suboptimal visual transitions through costly large-scale video pretraining. We introduce WAVE-0 (World-model-Augmented VLA Execution), a framework that bridges VLAs and WAMs through a lightweight latent world model. By connecting the semantic understanding of pretrained VLAs with explicit future prediction, WAVE-0 allows anticipated action consequences to directly guide action generation. Built on a pretrained VLA, its 257M world model translates VLM-generated latent action plans into predicted future representations that condition the action expert, unifying latent planning, future prediction, and action generation. The world model is trained directly on ground-truth robot actions with a counterfactual ranking objective, requiring neither pixel reconstruction nor large-scale video pretraining. WAVE-0 achieves success rates of 91.47% on RoboTwin 2.0 and 98.7% on LIBERO, along with 88.0%, 61.4%, and 75.0% on LIBERO-Plus, LIBERO-Pro, and LIBERO-Para, respectively. On real-world tasks, it improves the success rate of $\pi_{0.5}$ from 38.3% to 73.3%. These results demonstrate strong manipulation performance and generalization across diverse distribution shifts.

---

## 22. DR-VLA: Learning Human-Like Quadruped Navigation from Egocentric Web Videos via Domain-Invariant Scene Representations

**Authors:** Jun Tian, Yingjie Niu, Ruo Chen, Hongyi Lin, Chao Li
**arXiv:** [2610.18373](https://arxiv.org/abs/2610.18373)
**Categories:** Robotics (cs.RO)

Quadruped robots performing outdoor deliveries must interpret complex scenes, anticipate changes, and navigate in socially compliant ways. Robot demonstrations are costly to collect at the scale needed for generalization. Egocentric web videos offer abundant human navigation experience, but differences in viewpoint and motion make this experience difficult to transfer to robots. We introduce DR-VLA, a Mixture-of-Transformers framework that transfers human navigation experience through a domain-invariant scene representation (DISR). The framework combines vision-language understanding and latent world modeling with a flow-matching action expert. We introduce EgoLynx, comprising 10,000 hours of curated egocentric web video (EgoLynx-Web) and 2,000 clips of teleoperated robot navigation collected during real-world deliveries (EgoLynx-Robot). We pretrain the understanding and world experts on EgoLynx-Web without action labels, then adapt the model to robot observations and train the action expert on EgoLynx-Robot to predict executable trajectories. We also propose the Quadruped Navigation Score (QNS), a pseudo-closed-loop metric combining safety, instruction compliance, comfort, and progress. On the held-out EgoLynx-Robot test split, DR-VLA improves QNS by approximately 5% and reduces open-loop final heading error (FHE) by 14.6%, each relative to the best competing result for that metric. Ablations show that web-video pretraining improves generalization and that the model's key components contribute to performance. As a future-prediction target, DISR outperforms five generic visual representations and yields performance close to task-specific 3D perception without dedicated geometric labels or point clouds for target construction. Trained separately on NAVSIM v1 without web pretraining, DR-VLA achieves 92.1 PDMS, suggesting that the framework also applies to autonomous driving.

---

## 23. WoVR+: World Model as Reliable Simulator for Versatile VLA Policy Optimization with RL

**Authors:** Shangqing Zhou, Zhennan Jiang, Ning Ma, ..., Haoran Li, Dongbin Zhao
**arXiv:** [2610.17922](https://arxiv.org/abs/2610.17922)
**Categories:** Robotics (cs.RO)

Action-conditioned world models can reduce costly real-robot interaction in reinforcement learning for Vision-Language-Action models (VLA-RL), but hallucinations can mislead policy optimization. Extending them to richer VLA interfaces and long-horizon tasks raises challenges in spatiotemporal and cross-modal consistency, exploration-reliability balance in RL, and compounding rollout errors. We present WoVR+, extending WoVR's hallucination-aware WM-RL framework by redesigning the learned environment and imagined interaction protocol: A VLA-interface-aligned world model provides multi-view prediction and proprioceptive updates while mitigating hallucinations. Chunk-wise noise preserves flow-based policy exploration while limiting prediction-degrading action jitter. For long-horizon tasks, stage-local imagined training combines stage-entry resets, stage-specific rewards, local horizons, and controllable sampling to shorten generated prefixes and balance training across stages. WoVR+ improves success over SFT by 21.09% and 16.7% on RoboTwin and 6 real-robot tasks. Long-horizon phone-packaging success rises from 30% to 75%. Videos are available at this https URL.

---

## 24. Agentic Robot Creation through Generation, Verification, and Revision

**Authors:** Xuebing Li, Yibo He, Sitong Liu, Ran Ji, Jiayuan Gu
**arXiv:** [2610.17881](https://arxiv.org/abs/2610.17881)
**Categories:** Robotics (cs.RO)

Can an AI agent turn high-level user intent into a functioning robot and teach it how to behave? We study this question from two complementary aspects: embodiment and behavior creation. For embodiment creation, we investigate how well current multimodal models capture mechanical requirements, and introduce computational metrics for evaluating generated designs before fabrication. For behavior creation, we present Roboforge, an agentic framework that turns task specifications into executable policies through motion generation, policy learning, and execution-grounded revision. Given a robot embodiment and task, the agent generates a reference motion, configures the learning objective, and trains a policy. Crucially, motion remains in the loop: rollout feedback can revise the reference motion, reward, or both. We evaluate a generated embodiment across multiple MLLMs and behavior creation across four diverse robots against reward-refinement and one-shot motion baselines. Our computational metrics expose recurring mechanical failures in generated designs, while behavior experiments show that execution-grounded refinement improves task-level behavior and execution quality. Finally, we fabricate an agent-generated Gorilla and directly deploy learned behaviors on the physical robot.

---

## 25. The Human--VLA Communication Gap: What Humans Leave Implicit and What Policies Cannot Recover

**Authors:** Yiqing Xu, Jiajun Wu
**arXiv:** [2610.17746](https://arxiv.org/abs/2610.17746)
**Categories:** Robotics (cs.RO)

A robot may know how to perform a task yet fail when a human asks for it naturally. We study this human--VLA communication gap by separating an \emph{information gap}, where task semantics, grounding, or event structure remain unresolved, from a residual \emph{execution gap}, where even a fully specified task depends on how it is organized and invoked. To do this, we characterize how people naturally express demonstrated objectives and evaluate controlled variants of the same physical tasks, with detailed analysis on $\pi_{0.5}$ and consistent trends on $\pi_0$-FAST and Cosmos3-Edge. Our study reveals that humans increasingly compress instructions as tasks grow, relying more on contextual grounding and implicit execution structure. Current policies are misaligned with this behavior: they tolerate grounding dependence relatively well, but struggle when task semantics or event structure must be reconstructed. Even after the information gap is resolved, execution remains sensitive to command granularity and invocation state. These findings identify concrete targets for human-centered policy learning and interfaces that better bridge natural human objectives to robot behavior. Project website: this https URL.

---

## 26. Language2Drive: Do Vision-Language-Action Models Really Follow the Instructions in Autonomous Driving?

**Authors:** Zihan You, Zehua Fan, Wenqi Lyu, ..., Haoang Li, Yan Wang
**arXiv:** [2610.16634](https://arxiv.org/abs/2610.16634)
**Categories:** Robotics (cs.RO); Computer Vision and Pattern Recognition (cs.CV)

Recent Vision-Language-Action (VLA) models increasingly use natural-language instructions to condition autonomous driving behavior. Yet existing closed-loop benchmarks primarily measure route completion, safety, and rule compliance, leaving a fundamental question unresolved: does language actually determine which feasible behavior the vehicle executes? A trajectory may be safe and successful while still violating or even ignoring the passenger's instruction. To address this, we introduce \ltd, a benchmark designed to directly test this capability. Its key evaluation unit, the paired counterfactual unit (PCU), holds the initial driving scene fixed while changing only the instruction. This design enables us to distinguish isolated instruction success from counterfactual paired success across four instruction-following scopes. To test whether this distinction persists across evaluation regimes, we instantiate Language2Drive in complementary closed-loop CARLA simulation, reconstructed real-world scenes, and open-loop driving benchmarks, including our released CARLA-Language2Drive simulator with purpose-built maps. Evaluating representative driving VLAs across these settings reveals a striking mismatch between strong driving competence and weak language control: 93.2% of successful rollouts do not have a successful counterpart under the alternative feasible instruction. This failure is dominated by one-sided completion, where a model repeatedly executes one preferred behavior but fails when the same scene requires the counterfactual alternative. These results expose two fundamental limitations of current evaluation: isolated success and driving scores, which are widely used by conventional driving benchmarks, can substantially overstate language-following capability, while current driving VLAs themselves lack reliable instruction following under matched counterfactual tests.

---

## 27. Listen Before Act: Audio-Conditioned Robot Manipulation with ListenVLA

**Authors:** Jiaqi Fan, Rui Xu, Jiakun Xia, ..., Yili Fu, Xu Li
**arXiv:** [2610.16313](https://arxiv.org/abs/2610.16313)
**Categories:** Robotics (cs.RO)

Vision-language-action (VLA) models have advanced robotic manipulation by connecting visual perception and language instructions to action generation. However, many manipulation tasks depend on auditory cues that cannot be reliably inferred from visual observations and may need to be elicited through physical interaction. To address this gap, we present ListenVLA, an audio-conditioned VLA policy built on GR00T N1.7 for sound-guided manipulation. ListenVLA combines semantic audio embeddings with waveform-derived acoustic cues over a causal audio history and conditions continuous action generation through audio tokens and feature modulation. Moreover, we introduce an audio-action binding objective that uses context-matched demonstrations to link auditory differences to demonstrated action differences. The objective supervises short-horizon differences between flow-velocity predictions under different audio conditions, with shared pure-noise action inputs and fixed non-audio observations, alongside full-chunk action supervision. Furthermore, we develop LIBERO-Audio, an eight-task benchmark covering sound-based target selection, responses to auditory events, and physical interactions that reveal acoustic evidence. Experiments on LIBERO-Audio and three real-world manipulation tasks show excellent performance. Ablation studies support the contributions of binding supervision and audio modulation, while audio swap tests show that sound influences action predictions. Our code and videos are available at this https URL

---

## 28. FlowVLA: Enabling World Dynamics Understanding through Pluggable 3D Flow Learning

**Authors:** Junhyeong Go, Mingyu Jung, Woobin Im, Jongbin Ryu
**arXiv:** [2610.16160](https://arxiv.org/abs/2610.16160)
**Categories:** Robotics (cs.RO)

Recent advances in 3D reconstruction enable the extraction of temporally consistent 3D motion from RGB observations; however, current Vision-Language-Action (VLA) models still predominantly rely on 2D image-text priors. Therefore, they do not accurately represent the fundamental dynamics of the 3D world associated with physical actions. This over-reliance on static 2D visual cues limits the capacity of VLA models in achieving robust robot manipulation. To address these limitations, we introduce FlowVLA, a reconstruction-guided, pluggable 3D flow learning framework aimed at empowering VLA models with an inherent understanding of action-relevant dynamics. Instead of requiring explicit 3D sensor inputs or altering the inference-time architecture, our method is designed to utilize temporally aligned 3D flow only during training. This allows the model to learn the dynamic evolution of the physical scene while preserving the computational efficiency of conventional 2D VLA backbones. To bridge scene-level dynamics with robotic manipulation, we propose a modular 3D flow learning framework with dual-level flow supervision. Specifically, point-level flow guides the model to forecast the future displacements of task-critical 3D points, while TCP-level flow aggregates these motions to align with the robot's TCP trajectories. This dual-level flow supervision encourages the model to focus on semantically meaningful dynamic regions, effectively coupling scene-level motion with precise control signals. Extensive evaluations across simulation and real-world experiments demonstrate that FlowVLA consistently improves manipulation performance, zero-shot robustness, and optimizes data efficiency. FlowVLA adds only lightweight auxiliary heads during training and discards them at inference. Therefore, FlowVLA introduces no additional 3D sensor inputs, architectural modifications, or inference-time computation.

---

## 29. ReTrace: Cross-Stage Failure Attribution for Self-Improving Robotic Manipulation

**Authors:** Yue Yu, Bin Zhu, Junhui Li, ..., Shijie Zhou, Jingjing Chen
**arXiv:** [2610.15814](https://arxiv.org/abs/2610.15814)
**Categories:** Robotics (cs.RO)

General-purpose multimodal foundation models are increasingly capable of directly controlling robots, yet improving their manipulation capabilities through autonomous interaction remains challenging. A key challenge to such self-improvement is learning from failures in complex manipulation tasks involving cross-stage dependencies, where an action may succeed locally but cause a later stage to fail. To address this challenge, we introduce ReTrace, a self-improvement framework for robotic manipulation through autonomous physical interaction and retrospective reasoning, without provided demonstrations or model-parameter updates. ReTrace retrospectively traces downstream failures to earlier decisions, proposes targeted corrections, and evaluates them through subsequent interactions. Across attempts, ReTrace progressively consolidates validated corrections into a reusable manipulation skill that guide subsequent execution. We evaluate ReTrace on four real-world manipulation tasks using a Franka Research 3 robot. On the two tasks with strong cross-stage dependencies, GPT-6 Astra-low improves from 0% to 80% success on plug insertion and from 0% to 100% on ball pouring, while GPT-6 Sol-xhigh improves from 0% to 10% and 0% to 90%, respectively. The learned skills also transfer across model and reasoning configurations and reduce inference-time decision cost in most evaluated settings.

---

## 30. Recovering Low-Bit Failures in Vision-Language-Action Policies via Quantization-Conditioned Reinforcement Learning

**Authors:** Seongmin Park, Jaewon Lee, Yujun Heo, ..., Hyoung-rock Kim, Jungwook Choi
**arXiv:** [2610.15675](https://arxiv.org/abs/2610.15675)
**Categories:** Robotics (cs.RO); Computer Vision and Pattern Recognition (cs.CV)

Quantization lowers deployment costs of vision-language-action (VLA) policies but can compromise task completion. Across five VLA models and 4,050 real-world trials, we systematically reveal that quantization-aware training (QAT) generally improves on post-training quantization (PTQ) but leaves substantial gaps to full precision (FP) on long-horizon tasks and under visual and semantic shifts, while its imitation-based objective does not explicitly use rollout success or partial completion. To exploit these outcome signals, we introduce Quantization-Conditioned Reinforcement Learning (QCRL), an offline RL method coupling progress-based advantage estimation with quantization-aware source conditioning. FP rollouts supply reference experience beyond action-level distillation, progress-scaled terminal penalty distinguishes partial completion, and quantization-aware conditioning selects advantageous reference behavior within the quantized policy. We evaluate weight-only INT4 W4A16 on $\pi_{0.5}$ and GR00T N1.5 and joint weight-activation NVFP4 W4A4 on $\pi_{0.5}$. Using only in-distribution data, QCRL reaches 99.3% of FP's mean score across three visual-shift conditions for $\pi_{0.5}$ with INT4 W4A16, alongside 42.9% model-memory savings. With NVFP4 W4A4, it reaches 100.7% of the same FP baseline, alongside a $1.73\times$ speedup using NVFP4/FP8 deployment. Hardware gains are relative to FP16 on Jetson Thor.

---

## 31. Barrier-Constrained Guidance For Real-time Asynchronous VLA Execution

**Authors:** Wenbo Yu, Jifan Li, Wenke Xia, ..., Zhengping Che, Di hu
**arXiv:** [2610.14997](https://arxiv.org/abs/2610.14997)
**Categories:** Robotics (cs.RO)

While asynchronous execution enables VLA models to operate in real-time environments by predicting the next chunk during execution, it inevitably introduces boundary misalignment with the committed action stream. Existing delay-aware solutions address this at the prohibitive cost of extensive retraining, architectural modifications, or fixed-prefix inpainting that inflates computation when low latency is vital. To address these problems, we propose FreeBar, a training-free real-time inference plugin that enables robust asynchronous execution with only marginal additional inference cost by casting chunk alignment in flow-based VLAs as barrier-guided action-space constraint. Specifically, FreeBar introduces a lightweight Control Barrier Function (CBF)-inspired consistency constraint between consecutive action chunks and solves the resulting correction in closed form, avoiding costly backpropagation through the VLA action head. By progressively tightening the consistency bound during generation, FreeBar aligns generated chunks with the committed execution stream while preserving early-stage generative and within-chunk future action flexibility,. Across Kinetix, RoboCasa, and diverse real-world robotic platforms with multiple VLA backbones, FreeBar improves success rates over naive asynchronous execution by 10%--15% on average, with larger gains in highly dynamic scenarios. It also preserves real-time computational efficiency, decreasing inference latency per action chunk over 45% than RTC. Additionally, as a universal plugin, FreeBar remains robust across distinct latency environments, base policies, and hyperparameter settings.

---

## 32. Verify, Act, Distill: Turning Test-Time Compute into Test-Time Adaptation for Vision-Language-Action Models

**Authors:** Kaneyoshi Hiratsuka, Satoshi Yamamori, Jun Morimoto
**arXiv:** [2610.14885](https://arxiv.org/abs/2610.14885)
**Categories:** Robotics (cs.RO)

Test-time compute (TTC), which scores multiple candidate actions at inference time, is a powerful way to improve the execution performance of vision-language-action (VLA) models, but existing methods keep the policy frozen, so the gain must be recomputed at every execution. We propose Verify, Act, Distill, a framework that consolidates the gains of TTC into the VLA itself. A fixed verifier scores candidates generated by a flow-matching VLA, the weighted aggregate is executed, and the observations and aggregated chunks from successful adaptation episodes are distilled directly into LoRA parameters with the standard flow-matching loss. This reuses supervision that TTC has already produced during execution, without additional reinforcement learning or rollouts dedicated to teacher generation. On the 40 LIBERO tasks with a SmolVLA 5k checkpoint, distilling from only 10 episodes per task raises the mean success rate of verifier-free single-candidate generation from 54.1% to 70.6%, retaining about 74% of the improvement obtained by aggregating eight candidates. Applying the same aggregation to the distilled policy further raises the success rate from 76.4% to 82.3%, with a particularly large gain on LIBERO-Long (44.0% to 57.8%), and the single-candidate policy also improves on LIBERO-plus, which contains distribution shifts. These results show that using verification as a learning signal, rather than only as an execution-time selector, both retains the improvements of TTC and re-amplifies the effect of subsequent TTC.

---

## 33. DEFT-VLA: Stage-Localized Force Specialization for Contact-Rich Robotic Manipulation

**Authors:** Zan Huang, Yibo Qiu, Kan Ding, ..., Ronald X Xu, Mingzhai Sun
**arXiv:** [2610.14854](https://arxiv.org/abs/2610.14854)
**Categories:** Robotics (cs.RO)

Contact-rich manipulation poses a stage-dependent sensory conflict: vision and proprioception are essential for localization and approach, when force is largely uninformative and potentially distracting, whereas force becomes critical after contact, when irrelevant visual details and correlated robot states may become shortcuts. We propose DEFT-VLA (Dual-Expert Force-specialized Training for Vision-Language-Action Manipulation), which retains the task-adapted base expert for vision-dominated non-contact behavior and introduces a force-aware contact expert for critical contact stages, localizing force-conditioned adaptation to where it is needed. We further introduce a contact-localized force-attending curriculum that applies force-attending post-training only to the contact expert, progressively restoring vision and masking state tokens to suppress shortcuts. Real-robot experiments on pipette tip attachment, bimanual pipette aspiration, and whiteboard wiping show that DEFT-VLA effectively exploits force feedback to improve contact-stage performance while maintaining strong non-contact behavior and robustness to held-out grasp heights. It improves overall task success by 20-40 percentage points over the strongest baseline on each task.

---

## 34. PRISM: Precision Forcing for Generalist Vision-Language-Action Policies

**Authors:** Chenghao Yue, Peiyan Li, Hao Wang, ..., Yu Luo, Yuanlong Zhang
**arXiv:** [2610.14704](https://arxiv.org/abs/2610.14704)
**Categories:** Robotics (cs.RO)

Coupling a pretrained vision-language model (VLM) with a diffusion or flow-matching action expert has become the mainstream vision-language-action (VLA) paradigm for embodied policies, yet they remain unreliable once a task demands precise manipulation, e.g., submillimeter cable insertion. We attribute this weakness to a training objective that averages flow-matching errors across contexts and flow times, allocating little supervision to the few decisive moments determining task success. Along the generative path, inference integrates a locally supervised velocity field, so equally penalized errors at different flow times can affect the executed action unequally. Consequently, precision-task performance deteriorates as physical tolerance tightens by orders of magnitude. We call this supervision imbalance across contexts and flow times Flow-Time Starvation. The remedy is to jointly align supervision allocation and representation learning with context-dependent precision demand, enabling the policy to recognize when greater precision is needed. We instantiate this precision-forcing strategy as Precision-aware Reweighting and Internalization for Skilled Manipulation (PRISM), which scores precision demand offline, strengthens flow supervision where errors are consequential and action signals are visible, and internalizes that demand in the VLM condition representation. Simulation and real-robot experiments show that PRISM preserves or improves general-task performance while raising mean end-to-end success from 38.3% to 86.7% across drive connector insertion, bimanual connector mating, and screw tightening, substantially extending the precision boundary of existing embodied policies without new sensors or observation modalities.

---

## 35. Flow-Support-Weighted Proposals for Test-Time Verified VLA Policies

**Authors:** Chen Zhao, Zipeng Ye, Haitao Shen, ..., Yuchen Xie, Jing Zhang
**arXiv:** [2610.14588](https://arxiv.org/abs/2610.14588)
**Categories:** Robotics (cs.RO); Computer Vision and Pattern Recognition (cs.CV)

Test-time sampling promises to turn one action prediction into a set of distinct executable candidates that a verifier can choose among. Downstream fine-tuning works against that promise. A vision-language-action model trained to solve one task distribution concentrates its flow-matching decoder around the dominant demonstrated action, so repeated samples differ only marginally and the verifier receives many copies of one decision. We call this proposal contraction and identify it as a key constraint on test-time scaling: repeated samples can remain highly redundant as the candidate budget grows. Action Dynamic Sampling (ADS) alleviates the constraint on the proposal side, during training. At each training step, ADS integrates $K$ additional trajectories from the current policy under fresh base noise, scores each by the flow support along its path with a Hutchinson trace estimator, and corrects the policy's local action distribution toward this weighted set through a detached finite-set KL term. Training cost rises; deployment cost is unchanged. Across simulation and four physical-robot tasks, ADS raises proposal spread without the success penalty that Gaussian perturbation incurs, lifts oracle best-of-8 success on RoboCasa from 57.6% to 63.0%, improves fixed verifiers by 2.4 to 4.9 points in simulation, and raises TokenPB by up to 13.0 points on real-world manipulation.

---

## 36. Red-Teaming of Vision-Language-Action Models via Quality Diversity Environment Generation

**Authors:** Shihan Zhao, Henry Chen, Ya-Chuan Hsu, ..., Stefanos Nikolaidis, Daniel Seita
**arXiv:** [2610.14415](https://arxiv.org/abs/2610.14415)
**Categories:** Robotics (cs.RO)

A long-standing goal in robotics is to develop generalist robots that can perform tasks across a wide range of settings, flexibly specified with images and text. Vision-Language-Action (VLA) models offer a promising path toward this goal by training on large collections of robot demonstrations. However, while VLAs perform well in-distribution, they often fail under minor test-time shifts, such as changes in object positions, lighting, textures, and camera poses. To address this, we propose Quality Diversity for Diverse Environment Generation (Q-DEG), a method for improving VLA robustness by generating adversarial environments and fine-tuning the VLA on its own successful rollouts. Q-DEG uses Quality Diversity (QD) optimization to find a set of high-failure environments, while promoting diversity using policy embeddings extracted from the VLA. These environments expose vulnerabilities that can be mitigated through self-imitation fine-tuning, thereby improving the VLA's robustness. In simulation, we conduct experiments across three representative VLA models, and our results indicate that Q-DEG improves robustness to out-of-distribution (OOD) adversarial environments compared to the base VLA and VLAs fine-tuned using data collected from two red-teaming baselines. Furthermore, we demonstrate that improving VLA robustness through Q-DEG facilitates sim-to-real transfer. Our anonymous project website is at: this https URL.

---

## 37. Axiom-0: Hierarchical Self-Refinement for Vision-Language-Action Policies

**Authors:** Renbin Shu, Jing Yang, Xiangyuan You, ..., Feng Wu, Keke Tang
**arXiv:** [2610.14155](https://arxiv.org/abs/2610.14155)
**Categories:** Robotics (cs.RO); Computer Vision and Pattern Recognition (cs.CV)

Reliable manipulation requires policies that generalize across tasks, layouts, and object interactions. Vision-language-action (VLA) models combine pretrained multimodal understanding with learned control, but their performance remains limited on unfamiliar task compositions. We present Axiom-0, a VLA policy that addresses both the quality of its representations and their use in action generation through hierarchical self-refinement. Intra-VLM Representation Refinement (IVRR) strengthens selected intermediate features through consistency supervision with learned feature projections during training. VLM-Action Interface Refinement (VAIR) recursively updates the resulting conditioning before action generation. Joint optimization of the supervised VLM layers, VAIR, and the action generator connects the two components. On RoboCasa365, Axiom-0 achieves 62.32% overall success in our evaluation, exceeding the highest published leaderboard score (Paimon-0, 58.1%) by 4.22 percentage points and the Xiaomi-Robotics-1 reference by 4.92 points. Under the evaluated profiling setup, mean action-chunk generation latency increases by 1.7% over Xiaomi-Robotics-1. These results demonstrate improved task completion with modest inference overhead.

---

## 38. The Last Remote Sensing Model Built by Humans? Casting Any Earth Observation Task as Recursive Self-Improvement

**Authors:** Sijie Zhao, Zeqi Zhou, Heli Qi, ..., Weihao Xuan, Naoto Yokoya
**arXiv:** [2610.18845](https://arxiv.org/abs/2610.18845)
**Categories:** Computer Vision and Pattern Recognition (cs.CV); Computation and Language (cs.CL)

Earth observation (EO) models are still built by hand. For each new task, experts design a training recipe and tune it against a benchmark. We show that this loop can be handed to an agent. Any verifiable task can be cast as a harness and a verifier, where the harness defines what the agent may use and the verifier defines what counts as success. Every EO task can be made verifiable, through labeled benchmarks, independent sensors, physical models or the repeated observation of the same place. Given only these two components, a general-purpose coding agent builds the EO model and improves it recursively on its own outputs. Settings long treated as separate research problems, from learning with a handful of labels to adapting across domains, become choices of harness and verifier. On four EO benchmarks spanning optical, SAR and multispectral time-series imagery, agent-built models surpass the state of the art and keep most of that accuracy from about 1% of the training labels. This establishes a new paradigm for EO, in which people design harnesses and verifiers and agents build the models, so EO models improve as agents do.

---

## 39. RSIgen: Reciprocal Self-Improvement for Agentic Visual Generation

**Authors:** Yidi Liu, Haozhe Wang, Jie Xiao, ..., Xueyang Fu, Zheng-Jun Zha
**arXiv:** [2610.18688](https://arxiv.org/abs/2610.18688)
**Categories:** Computer Vision and Pattern Recognition (cs.CV)

Agentic visual generation produces experience that can improve the native understanding (agent) and generation roles of a unified multimodal backbone, but task success alone does not determine which role should learn. Generator updates can also make the agent's action supervision stale. We introduce RSIgen, a task-centric reciprocal self-improvement framework linking learning allocation, supervision refresh, and recursive curriculum construction. Dynamic Responsibility Routing (DRR) uses matched interventions on evidence, inputs, and supported actions to select learning recipients and construct compatible training targets. After generator learning, RSIgen re-evaluates the relative utility of tested actions with branch inputs held fixed to refresh agent supervision; the retained roles then construct the next curriculum. Across BAGEL, Qwen-Image, and Wan-Image-7B, RSIgen improves AgentGen-Bench Full Overall9 by 3.2--3.3 points over a three-cycle SearchGen adaptation with action costs. Wan controls support allocation gains at matched role-level training exposure, refresh gains at a matched adaptation budget, and benefits from updated curriculum sources while recipients continue learning. In blind evaluation on 200 real-user requests, pooled tie-adjusted preference scores against the same baseline reach 70.0% for task completion and 64.9% for visual quality.

---

## 40. Data-Centric Recursive Self-Improvement for Navigation via Policy-Synchronized Language-Action Dual Bootstrapping

**Authors:** Songze Li, Haoming Gu, Ziyang Gong, ..., Wenwei Zhang, Yi Wang
**arXiv:** [2610.15782](https://arxiv.org/abs/2610.15782)
**Categories:** Computer Vision and Pattern Recognition (cs.CV)

Vision-language navigation requires agents to follow natural-language instructions to reach target locations, making high-quality language supervision essential. Since human annotation is costly, prior work has explored scalable data synthesis methods. However, existing methods typically either use separate models for navigation and instruction generation or couple the two tasks through task-specific components; most also annotate the full trajectory corpus with a fixed model before updating, which can cause generated supervision to lag behind the evolving policy. Therefore, we introduce RSI-Nav, a data-centric recursive self-improvement framework for navigation via policy-synchronized language-action dual bootstrapping, which unifies vision-language-to-action instruction following and vision-action-to-language instruction generation within a shared model. Specifically, after supervised fine-tuning establishes fundamental capabilities, RSI-Nav progressively processes unlabeled trajectories in small shards. The current model generates instructions for these trajectories, executes them to evaluate goal completion and path efficiency, retains qualified samples, and immediately updates itself before processing the next shard. This shard-wise update keeps newly generated supervision aligned with the evolving policy. We also incorporate spatial understanding data, since stronger spatial reasoning benefits navigation. Extensive experiments show that RSI-Nav reaches 68.6% SR on R2R-CE and 72.4% SR on RxR-CE, while providing stronger instruction-generation utility and modestly improved spatial understanding after recursive evolution.

---

## 41. A Persian Vision-Language-Action Dataset and Benchmark for Ambiguity- and Infeasibility-Aware Instruction-to-Plan Grounding

**Authors:** Abdollah Pourasghari, Saeedeh Sadat Sadidpour, Mohammad Roustaei
**arXiv:** [2610.15666](https://arxiv.org/abs/2610.15666)
**Categories:** Computer Vision and Pattern Recognition (cs.CV); Computation and Language (cs.CL)

Converting natural-language instructions into executable action plans conditioned on a scene image is a core capability for embodied human-robot interaction, but existing benchmarks target English, simulated or video-grounded environments, and largely assume instructions are clear and executable. We introduce the first Persian vision-language-action dataset for this task: 258 instances over 230 real household/office photographs, annotated with reference plans, deliberate ambiguity and infeasibility labels, disambiguating question-answer pairs, and an auto-generated chain-of-thought rationale for training. Using this resource, we ablate retrieval-augmentation, chain-of-thought prompting, and an agentic disambiguation step, evaluated with an LLM-as-judge protocol and a new metric, PGOS-FA, extending prior work (PG2S) with step-order sensitivity, an over-generation penalty, and Persian-adapted embeddings. Paired statistical testing across 36 comparisons shows retrieval-augmentation is a large, robustly significant effect, while finer-grained additions are directionally consistent but not statistically distinguishable from noise at this scale, and the LLM-judge metric has near-zero power where PGOS-FA succeeds. A blind human-correlation study on 79 real outputs shows PGOS-FA tracks human judgment at least as closely as the LLM-judge. Testing generalization beyond the ablation's single backbone, we find that most of the gap between an open-weight and a substantially stronger closed planner is attributable to open-weight model generation rather than to the closed model's capability specifically, and that our best configuration significantly outperforms an independently reproduced external baseline despite a weaker backbone. The dataset, PGOS-FA implementation, and evaluation code will be made available upon reasonable request.

---

## 42. OmniRSI: Taming Latent Diffusion for Unified Multimodal Remote Sensing Image Generation

**Authors:** Hebaixu Wang, Jing Zhang, Haonan Guo, ..., Jiayi Ma, Bo Du
**arXiv:** [2610.15414](https://arxiv.org/abs/2610.15414)
**Categories:** Computer Vision and Pattern Recognition (cs.CV)

Multimodal remote sensing image generation emerges as a promising paradigm for recovering complete and complementary observations from heterogeneous and partially observed remote sensing data. However, existing methods predominantly depend on sensor-specific fine-tuning of natural image generation models, limiting unified multimodal generation capacity due to the absence of shared representations and robust conditioning mechanisms. To address these challenges, we propose OmniRSI, a unified multimodal remote sensing image generation model. Specifically, we develop a remote sensing-specific variational autoencoder that captures multimodal priors and promotes a locally smooth latent space for unified representation and robust reconstruction across diverse observed data. Building upon that, we fully adapt Stable Diffusion 3.5 with a ControlNet branch to support unified multimodal generation and translation conditioned on textual and visual cues. Besides, we devise a training-free cyclic latent alignment mechanism that iteratively enriches incomplete visual conditions with generated multimodal information, progressively improving guidance reliability while preserving observed measurements. We also construct RSI-MM, a large-scale dataset comprising 11.5M multi-resolution images with text annotations and partially paired data for training and evaluation. Extensive experiments verify that OmniRSI achieves superior performance in multimodal reconstruction, generation and translation.

---
