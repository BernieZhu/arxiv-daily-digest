# arXiv Daily Digest — 2026-10-27

**Mode:** direct
**Categories:** cs.AI, cs.LG, cs.RO, cs.CV
**Keywords:** VLA, RSI, agentic robot, self-improving robot, self-evolving robot, robot harness
**Papers found:** 20

---

## 1. Skill$^{\infty}$: Recursive Self-Improvement for Agent Skill Optimization

**Authors:** Wangcheng Tao, Zhanglu Yan, Han Wu, Weng-Fai Wong
**arXiv:** [2610.35434](https://arxiv.org/abs/2610.35434)
**Categories:** Artificial Intelligence (cs.AI); Computation and Language (cs.CL)

Recursive self-improvement (RSI), in which a system also improves the way it improves, is a long-standing aspiration on the path to AGI. Language agents increasingly store procedural knowledge in reusable skills. Optimizing skills offers a direct way to achieve RSI, because the optimization procedure itself can be encoded as a skill. Existing skill optimizers, however, follow a hand-designed procedure. Even methods that evolve a meta-skill confine it to a fixed pipeline and relearn it for each task. We present Skill$^{\infty}$, which makes skill optimization recursively self-improving: a meta agent follows a meta-skill to optimize task skills and optimizes the meta-skill itself using the same procedure. The optimization is agent-led. The meta agent diagnoses execution traces, proposes candidates, requests independent reviews, and allocates the search budget. The meta-skill defines these steps, allowing self-improvement to rewrite them. This meta-skill is also decoupled from task skills, refined on multiple skill optimization tasks and then reused to optimize task skills across diverse domains. As in deployment, skills at both levels are standard packages loaded through native skill discovery. On 83 SkillsBench tasks, Skill$^{\infty}$ reaches a pass rate of 60.7%, compared with 56.4% for human-curated skills and 54.5% for SkillEvolver.

---

## 2. RSIV-Harness: A Recursive Self-Improvement Harness Framework for Open-Domain Conversational Text-to-Visualization

**Authors:** Jiawei Lu, Chen Zhang, Jinwei Lu, ..., Yuanfeng Song, Raymond Chi-Wing Wong
**arXiv:** [2610.35316](https://arxiv.org/abs/2610.35316)
**Categories:** Artificial Intelligence (cs.AI)

Users often request charts without knowing which database or table holds the relevant data. Such requests may be ambiguous, and users may ask follow-up questions to deepen their analysis or iteratively refine existing charts. A useful assistant must therefore discover relevant data sources among heterogeneous databases, ask clarifying questions when needed, and track evolving user intent while preserving constraints established in earlier turns. Yet recent text-to-visualization agents typically rely on static agent harnesses that are predefined and remain unchanged despite recurring failures across tasks. To address this limitation, we introduce RSIV-Harness, which keeps the language model weights fixed and applies Recursive Self-Improvement to revise the surrounding harness from the agent's own failure traces. To balance flexible self-improvement with stability, we introduce a four-layer framework that evaluates proposed harness revisions through anchor and memory checks, refining those that pass and restoring the best validated harness otherwise. We further introduce ODAC-Vis, a benchmark with 640 tasks for Open-Domain, Ambiguous, and Conversational text-to-visualization that jointly evaluates open-domain data discovery, ambiguity resolution, multi-turn visualization refinement, and executable chart generation. Experiments show that a single round of RSIV-Harness improves all six evaluation metrics relative to the seed harness, with particularly large gains in executability (+28.02 points) and chart structure (+34.01 points), demonstrating the ability to learn from task-solving experience and turn recurring failures across tasks into substantial performance improvements.

---

## 3. Trustworthy Recursive Self-Improvement in the Era of Large Models: Foundation, Risks, Evaluation and Open Challenges

**Authors:** Jiayue Pu, Ang Gao, Jinyi Bai, ..., Jun Xu, Xiao Zhang
**arXiv:** [2610.35193](https://arxiv.org/abs/2610.35193)
**Categories:** Artificial Intelligence (cs.AI); Cryptography and Security (cs.CR)

AI systems built around large models increasingly use experience and feedback to make persistent changes to models, prompts, memories, tools, and workflows. Recursive self-improvement (RSI) extends this process to inductive biases and to the mechanisms that govern future updates, which can themselves be revised and reused across improvement cycles. Yet self-modification alone does not guarantee trustworthy improvement. Reported gains may reflect flawed evaluations, previously acquired capabilities may deteriorate, and compliance with behavioral constraints may weaken. Compromised artifacts or sensitive information may also persist in successor systems. Changes to improvement mechanisms may invalidate earlier verification results and make human oversight less effective. This survey presents an operational definition and process framework for RSI and organizes the requirements for trustworthy RSI into four interconnected themes: genuine and sustained improvement; behavioral constraints, alignment, and fairness; system security and privacy; and transparency and controllability. We examine these themes from three perspectives: Improvement Validity, Constraint Preservation, and Effective Oversight. This analysis covers improvement diagnosis, proposal generation, proposal evaluation, and update implementation (S1--S4), including the recursive application of these stages to improvement mechanisms (RI). We review risks, safeguards, and evaluation evidence for individual updates, effects inherited by successor systems, and revisions to improvement mechanisms, while distinguishing direct RSI findings from evidence in related systems. Finally, we examine evaluation settings, identify requirements for independent and longitudinal assessment, and discuss applications and open research problems.

---

## 4. Beyond Behaviour: A Stimulus-Response Safety Evaluation of Vision-Language-Action Models

**Authors:** Vy Vo, Dinh Phung
**arXiv:** [2610.34837](https://arxiv.org/abs/2610.34837)
**Categories:** Artificial Intelligence (cs.AI)

Humans exhibit biological sensitivity to safety-critical stimuli that can trigger defensive action. Across three models and two video benchmarks, we investigate whether similar responses emerge in vision-language-action models by examining their internal representations and action tendencies in response to visible hazards and harmful consequences. Our findings suggest that task execution may remain the default response even when danger is internally registered.

---

## 5. Variational Cognitive Memory Abstraction for Long-Horizon Vision-Language-Action Models

**Authors:** Xinyu Liu, Daiying Tian, Chenwei Tang, ..., Liangli Zhen, Jiancheng Lv
**arXiv:** [2610.34251](https://arxiv.org/abs/2610.34251)
**Categories:** Artificial Intelligence (cs.AI)

Vision-Language-Action (VLA) models have shown remarkable success in robotic manipulation, yet their ability to execute long-horizon tasks remains limited by insufficient long- term memory modeling. Existing methods either rely on implicit temporal representations within policy networks, where historical information can be gradually diluted, or maintain explicit memory buffers that suffer from redundancy, noise accumulation, and inefficient retrieval. In this paper, we propose CogMemory, a novel variational cognitive memory framework that enables VLA systems to selectively preserve and reuse task-relevant historical information. Our approach encodes multimodal trajectories into compact latent memory representations through a selective state- space memory encoder, multi-slot temporal abstraction, and variational information compression. During action generation, dynamic cross-attention retrieval with gated fusion adaptively incorporates relevant memories into policy prediction. With merely 3.45M additional parameters, CogMemory stays lightweight and seamlessly fits both early- and intermediate-fusion VLA backbones. Extensive experiments on long-horizon robotic manipulation benchmarks demonstrate consistent improvements across diverse VLA backbones.

---

## 6. Power-of-Two Leaky Integrate-and-Fire Neurons for Event-Driven Vision-Language-Action Inference

**Authors:** Rui Liu, He Lv, Ziyao Zhang, Rui Ma, Rongxiang Nie
**arXiv:** [2610.33658](https://arxiv.org/abs/2610.33658)
**Categories:** Artificial Intelligence (cs.AI)

Vision-language-action (VLA) models have demonstrated strong capabilities in robotic manipulation, yet their reliance on dense, continuous-valued computation presents a fundamental challenge for energy-constrained deployment. Inspired by the sparse, event-driven signaling and temporal integration mechanisms of biological neurons, a promising alternative is to introduce spiking computation into VLA models. However, enabling such computation without restructuring pretrained policies or compromising closed-loop control remains an open challenge. To address this challenge, we introduce the Power-of-Two Leaky Integrate-and-Fire (PoT-LIF) neuron, which emits signed spikes with power-of-two amplitudes. By combining magnitude-coded spike events with residual-preserving membrane dynamics, PoT-LIF enables continuous information to be progressively represented through discrete spikes. The Heartbeat formulation further localizes this process within weighted projections, bridging biologically inspired spiking computation and pretrained VLA architectures without modifying their external inference interfaces. We integrate PoT-LIF into the vision projection, vision-language projection, and action projection of $\pi_{0.5}$ and evaluate both operating modes over 2,000 paired closed-loop LIBERO episodes per configuration. Standard-mode PoT-LIF VLA achieves success rates of 96.90% and 96.35% at $T = 1$ and $T = 2$, respectively, while Heartbeat mode achieves 97.25% and 96.90% at $T = 2$ and $T = 4$, compared with 96.70% for the original continuous-activation $\pi_{0.5}$ baseline. At $T = 1$ with a 60.01% firing rate, PoT-LIF uses approximately 1/7.67 of the dense-reference arithmetic energy, corresponding to a modeled reduction of 86.95%.

---

## 7. TAD: Distilling Vision-Language-Action Policies from Teacher Trajectories Alone

**Authors:** Yun Zhu, Da Wang
**arXiv:** [2610.33650](https://arxiv.org/abs/2610.33650)
**Categories:** Artificial Intelligence (cs.AI)

Online distillation of vision-language-action (VLA) policies commonly relies on teacher action scores that an inference-only interface may not expose. Trajectory-only Adversarial Distillation (\gad{}) instead turns a fixed bank of teacher joint-position features into adaptive feedback: a discriminator compares feature marginals from teacher and student rollouts and supplies rewards for on-policy learning. The student interacts with the environment without online teacher queries or environment task rewards. On ManiSkill \texttt{PutOnPlateInScene25Main}, \gad{} improves OpenVLA-OFT (7B) from $26.2\%$ to $76.6\%$ \successonce{} ($+50.4$ percentage points) and from $20.3\%$ to $58.6\%$ \successend{}. It trails white-box on-policy distillation (OPD) at $81.6\%$ / $59.4\%$ by $5.0$ / $0.8$ percentage points ($n{=}256$ evaluation trajectories per checkpoint). The tested four-epoch continuation achieves the highest \gad{} result without additional teacher data. This best run uses $5\times$ OPD's student interaction budget and $12.5\times$ its complete-rollout batch-passes. The comparison demonstrates online VLA improvement without teacher scoring while quantifying unequal interaction and optimization budgets.

---

## 8. VLA-HWBench: Where the Time Goes When VLA Models Run on Edge Hardware

**Authors:** Borui Xu, Hongshi Tan, Wenqi Jiang, ..., Jason Zeng, Michael Heinrich
**arXiv:** [2610.34717](https://arxiv.org/abs/2610.34717)
**Categories:** Robotics (cs.RO); Artificial Intelligence (cs.AI)

Vision-language-action (VLA) models increasingly run on edge devices aboard robots, where inference latency constrains closed-loop robot control. However, it remains unclear how to design VLA models, their inference software and edge hardware so that robots can run VLA inference in real time. Most VLA models report only task success, while prior studies cover limited action-generation strategies, divide inference into at most three stages, and lack comparisons of inference optimizations on the same models. Therefore, we introduce VLA-HWBench, a benchmark that measures 18 open VLA models on NVIDIA Jetson AGX Thor and AMD Ryzen AI Max+ PRO 395, with a seven-stage inference breakdown. Our study reveals three insights. First, action-generation strategy matters more than model size. It dominates 14 of 19 Jetson configurations, latency varies by $82\times$ on Jetson and $157\times$ on AMD, and parameter count explains at most 15% of latency variance. Models that generate long action chunks in a few flow-matching steps keep up with control, whereas token-by-token decoding does not. Second, kernel fusion with 4-bit weights helps most, running $\pi_{0.5}$ and GR00T N1.7 2.6-2.9$\times$ faster than PyTorch with this http URL, but it exists for only these two models and only on the Jetson. Optimization also moves the time to the stages it shortens least, as CPU preprocessing grows from 12% to 39% of the GR00T N1.7 call. Third, after optimization, memory bandwidth limits only the stages that process few tokens on the Jetson, such as the denoising steps, whereas software limits all other stages, from unfused kernels to serial preprocessing on the host CPU. Overall, low-latency edge VLAs should use few action-generation iterations, inference software should extend kernel fusion and low-bit weights to more models and platforms, and edge hardware needs high memory bandwidth and a fast host CPU.

---

## 9. TRIAGE: Efficient Vision-Language-Action Inference Needs Both Reuse and Pruning

**Authors:** Sooyoung Kwon, Carlee Joe-Wong, Kyunghan Lee
**arXiv:** [2610.34519](https://arxiv.org/abs/2610.34519)
**Categories:** Robotics (cs.RO); Artificial Intelligence (cs.AI); Computer Vision and Pattern Recognition (cs.CV); Machine Learning (cs.LG)

Vision-language-action (VLA) models are increasingly used for robot manipulation because they map camera images and a language instruction directly to actions. Robots that cannot be tethered to a workstation, such as mobile manipulators and humanoids, must run them on onboard embedded boards, where the prefill latency of the language backbone grows with the hundreds of visual tokens processed at every control step. To meet real-time limits, training-free accelerators recompute only a subset of the visual tokens and skip the rest, either by pruning them or by reusing their cached key-value (KV) states. The two options save nearly the same computation, yet existing methods apply only one of them to every skipped token. Through a token-level diagnostic, we show that which option keeps the action closer to full recomputation depends on the token's drift, the change in its shallow-layer value since its cache was computed. On both backbones tested, reusing tokens below a drift threshold was no worse than pruning them, whereas beyond it, reuse yields up to 4.4x the action error of pruning; the same diagnostic calibrates this threshold per backbone. Building on this finding, we propose TRIAGE, which deems a cache valid when its drift is below this threshold and it is not too old. TRIAGE recomputes a fixed budget of tokens, prioritizing important tokens with invalid caches, reuses every other token with a valid cache, and prunes the rest; prune-only and reuse-only methods are the two extremes of this partition. Because the budget fixes the number of recomputed tokens, it directly sets the prefill latency. On LIBERO and SimplerEnv, TRIAGE stays within 3 pp of full recomputation in average success rate while cutting prefill latency on a Jetson AGX Orin by up to 48%, and with only 7% of visual tokens recomputed, it beats the strongest baseline by 24.4 pp on LIBERO-Object.

---

## 10. ParetoRSI-Gym: Can AI Agents Improve Language Models Across Multiple Domains?

**Authors:** Haojin Wang, Yangzhen Wu, Zeyi Chen, ..., Shangding Gu, Dawn Song
**arXiv:** [2610.34386](https://arxiv.org/abs/2610.34386)
**Categories:** Machine Learning (cs.LG); Artificial Intelligence (cs.AI)

Recursive self-improvement (RSI) requires an agentic system to design, train, and evaluate its own successor. Data-driven post-training is a central part of that loop, yet existing evaluations measure it on a single benchmark, where an agent selects from a static pool or distills a stronger model to push one score up in one run. Real post-training is multi-domain, and a gain in one domain has to be weighed against a regression in another. We propose ParetoRSI-Gym, in which an agent searches for data, curates it, trains, reads back per-domain results, and repeats, with everything but the data held fixed: the initial LLM, the five domains (math, code, finance, medicine, science), the toolset, and the SFT pipeline. Generalization benchmarks in each domain separate capability gains from overfitting to the scores the agent optimizes against. Across three agent systems, three base models, five rounds and multiple seeds, the strongest system, Claude Code with Opus-5, raises the generalization scores of its proxy-best checkpoint by 9.2% relative to the starting model (+2.3 absolute points), averaged with equal weight over three base models and five domains, with a single-domain relative gain of up to 63% (medicine on Ministral-3-3B). Further analysis shows that the harness matters as much as the model it drives, and that each agent keeps a unique data selection strategy. We see our work as a step towards evaluation of RSI systems in real-world machine learning engineering.

---

## 11. Continual Learning Exam: Benchmarking Long-Horizon RSI and Experiential Learning in LLM Agents

**Authors:** Haoyu Zhao, Sitian Tu, Yuxuan Huang, ..., Meng Fang, Jun Wang
**arXiv:** [2610.33956](https://arxiv.org/abs/2610.33956)
**Categories:** Machine Learning (cs.LG); Artificial Intelligence (cs.AI); Computation and Language (cs.CL); Computer Vision and Pattern Recognition (cs.CV)

Continual learning is the ability of LLM agents to improve over time by acquiring, refining, and applying knowledge from experience while retaining useful prior knowledge. It is essential for agents learning over long time horizons, yet current evaluations largely assess individual task performance rather than improvement through accumulated experience. We introduce Continual Learning Exam (CLE), a large-scale benchmark developed by 50+ domain experts to measure experience-driven improvement in realistic professional workflows. CLE comprises 120 human-authored tasks, each organised as a five-level ladder, yielding 600 levels spanning 89 professional roles across 12 occupational domains. Agents must pass each level to unlock the next, with later levels building on experience accumulated during earlier assignments. An evaluation agent assesses each submission against human-authored rubrics. We compare a single-submission setting with one that provides diagnostic feedback after failure and allows one revision. Across 17 harness-model configurations using frontier LLMs, feedback and revision yield a median completion gain of 5.3 percentage points. Yet the best-performing system clears only 47.7% of levels and completes all five levels in just 23.3% of tasks, highlighting the difficulty of sustained learning from experience for existing frontier LLMs. As such, the dataset can also be used to post-train LLMs to strengthen their continual learning capabilities.

---

## 12. RSI Arena: Towards Recursive Self-Improvement with Human Feedback

**Authors:** Yue Huang, Yanbo Wang, Lichi Li, ..., Zichen Chen, Zhangchen Xu
**arXiv:** [2610.33624](https://arxiv.org/abs/2610.33624)
**Categories:** Computation and Language (cs.CL); Artificial Intelligence (cs.AI)

Can AI agents autonomously train useful language models and improve them using feedback from users? We introduce RSI Arena, a two-stage study of autonomous post-training as a step toward recursive self-improvement. Ten frontier models act as training agents, each starting from NVIDIA Nemotron 3.5 Lightning 30B-A3B Base. During a six-day first stage, each agent has 1,000 GPU-hours and $300 in API credit on a shared 64-GPU cluster, independently selecting data, implementing training procedures, and choosing checkpoints. We evaluate their models on 20 benchmarks and through blind human evaluations. All ten agents produce working assistants, with the strongest model, trained by GPT-6 Astra, closing a median of 76% of the base-to-Instruct gap across 12 capability benchmarks. Its human-preference rating is also close to NVIDIA Instruct after statistical adjustment for answer length and formatting. In Stage 2, each agent receives the comparison records and votes involving its Stage 1 model and is given three additional days for further training. Using NVIDIA Instruct as a common reference across the two evaluation rounds, we observe an improvement from Stage 1 to Stage 2 in the style-adjusted relative rating of eight of the ten models. We show that benchmark gains were modest, with no clear link to preference gains, while some agents encouraged longer responses and one model showed increased harmful compliance on StrongREJECT. RSI Arena provides an auditable setting for studying how human feedback can guide autonomous model development. It takes a step toward recursive self-improvement with human feedback (RSIHF), in which people help define what improvement means for the AI systems they use.

---

## 13. AGQ: Action-Guided Ultra-Low-Bit Quantization for Vision-Language-Action Models

**Authors:** Xuhong Qiu, Zhuoyu Wu, Qiawei Zheng, ..., Wenqi Fang, Raphaël C.-W. Phan
**arXiv:** [2610.33074](https://arxiv.org/abs/2610.33074)
**Categories:** Computer Vision and Pattern Recognition (cs.CV); Artificial Intelligence (cs.AI)

Vision-language-action (VLA) models enable robots to perform tasks specified through natural-language instructions, but their large weight footprint challenges deployment on memory-constrained onboard platforms. Ultra-low-bit quantization reduces this footprint, yet preserving task performance and controlling weight recovery costs remain challenging. We propose Action-Guided Quantization, which combines action sensitivity with a measured proxy for weight recovery cost to allocate matrix bitwidths under storage budgets. Per-channel calibration compensates for quantization error, while a uniform bitwidth within each matrix preserves regular layouts. Bit-dependent grouped lossless coding reduces resident weight storage, and block-wise recovery limits temporary buffers. On LIBERO, AGQ achieves 92.7% task success at W3, exceeding AWQ and GPTQ by 1.2 and 3.7 percentage points, respectively, and retains 70.5% success at W2.5. An asymmetric configuration, denoted W1.5$^{*}$, uses W4 vision weights and a parameter-weighted average of 1.5 bits for language weights. With lossless coding, it achieves $6.10\times$ complete-model compression relative to BF16 while retaining 25.5% task success. Code and experimental results are available at this https URL

---

## 14. Robot-Aligned 3D Gaussian Splatting for Precise Reaching with Wrist-Camera VLA Policies

**Authors:** Zuoxu Wang, Xiao Liang
**arXiv:** [2610.35626](https://arxiv.org/abs/2610.35626)
**Categories:** Robotics (cs.RO)

Efficient robotic data collection remains a major bottleneck for vision-language-action (VLA) policy learning, especially for tasks requiring accurate end-effector positioning and camera-action alignment. This challenge is particularly severe in electronic-waste disassembly, where robots operate in cluttered assemblies of densely packed, visually similar components. Full digital-twin simulation is difficult because many parts are thin, reflective, or mechanically complex, making accurate object-level meshes and contact models difficult to obtain. In this work, we focus on pre-contact reaching and propose a 3D Gaussian Splatting (3DGS)-based data generation pipeline for wrist-camera VLA adaptation. Our method reconstructs the real workspace with 3DGS and renders diverse wrist-camera observations from robot-aligned poses. These observations are paired with smooth, structured reaching trajectories to provide robot-aligned visual-action supervision for VLA fine-tuning. We further augment the VLA policy with an instruction-conditioned reach verifier that estimates target proximity and provides reliable termination before physical interaction. Experiments in motherboard disassembly demonstrate precise VLA-based reaching using wrist-camera observations alone, without an external side-view camera. With $\pi$0.5, 1,500 generated trajectories achieve 80.0\% precise-reaching success across three targets, compared with 58.7\% using 150 teleoperated demonstrations, while requiring less than 10 minutes of active human capture. Project website: this https URL

---

## 15. RoboDoctor: Training-Free Recursive Self-Improvement for Robot Policies

**Authors:** Heyang Yu, Haomin Li, Sihang Li, ..., Xiaoyu Tian, Yiming Li
**arXiv:** [2610.35604](https://arxiv.org/abs/2610.35604)
**Categories:** Robotics (cs.RO); Computer Vision and Pattern Recognition (cs.CV)

Generalist robot policies and language-model agents provide complementary capabilities, but completing a task also requires adapting their use to the consequences of physical interaction. We study execution as a locus of adaptation: feedback guides the current action and supplies evidence for revising subsequent decisions under fixed model weights. We introduce RoboDoctor, a training-free framework that connects diagnosis, grounded action, and persistent experience across three revision targets. The harness allocates control between policy and agent; intervention determines when to assist while preserving useful policy behavior; and operation refines physical methods through observed effects. Linked experience records retain the reason for a decision, the attempted method, its outcome, and conditions for reuse. On a curated archive of 54 RoboDojo-Sim task entries, RoboDoctor achieves a five-dimension mean score of 57.10, with a native success rate of 49.44%. Recorded interactions illustrate strategy changes, selective correction, and grasp revision. These findings characterize execution-time adaptation in the evaluated system; controlled trials remain necessary to isolate the contribution of cross-episode experience.

---

## 16. JevVLA: Jev-Inspired Energy-Based Adaptation for Vision-Language-Action Policies

**Authors:** Wei Wang, Wenqiao Zhang, Zheqi Lv, ..., Chao Li, Yueting Zhuang
**arXiv:** [2610.35010](https://arxiv.org/abs/2610.35010)
**Categories:** Robotics (cs.RO)

Vision-language-action (VLA) policies can select among discrete candidates for pick-and-place manipulation or generate continuous action chunks for motion control. Improving both forms of decision making through a common mechanism while retaining the capabilities of a pretrained policy is an important adaptation problem. Inspired by Jev's structured, probabilistic decision interface, we propose JevVLA, a lightweight energy-based adaptation framework for VLA policies. JevVLA instantiates this inspiration by modeling the relative quality of action proposals: with the base policy frozen, it learns a differentiable scalar energy conditioned on observations, task context, and actions, using execution feedback, expert corrections, or demonstration-derived preferences. JevVLA uses this single learned action preference function in two ways: its values compare discrete candidates, while its action gradients correct continuous actions or guide their generation. Candidate selection and continuous control thus share one trainable decision core. Each benchmark uses independently trained weights and fixed input/output encodings, while retaining the same core network with approximately 80,000 trainable parameters. On the held-out test sets, JevVLA improves task success over the respective matched base-policy controls by 1.28, 2.31, 1.60, 1.52, and 1.28 percentage points on MetaWorld MT50, VIMA, LanguageTable, LIBERO Plus, and CLIPort, respectively. These results support the feasibility of a lightweight, Jev-inspired energy model for adapting both discrete action selection and continuous action guidance. The JevVLA implementation will be open-sourced at this https URL.

---

## 17. RynnVLA-Latent: Scaling Robotic Manipulation Foundation Models with 3D-Grounded Latent Actions

**Authors:** Haoyu Zhao, Xingyue Zhao, Zhian Su, ..., Deli Zhao, Zhongyu Li
**arXiv:** [2610.34356](https://arxiv.org/abs/2610.34356)
**Categories:** Robotics (cs.RO)

Scaling vision-language-action (VLA) models is constrained by scarce action-labeled demonstrations and incompatible control spaces across robot embodiments. We present RynnVLA-Latent, a framework that turns heterogeneous interaction videos into scalable supervision for robot policy pretraining. At its core, RynnLAM learns continuous, 3D-grounded latent actions from visual transitions without requiring native robot controls. By combining residual future-feature prediction, camera-compensated 3D-flow supervision, and camera-motion decoupling, RynnLAM encourages representations that capture control-relevant motion rather than appearance changes alone. We apply RynnLAM to 30.1K hours of human, robot, and simulation videos, producing 745.52M latent-action descriptors. RynnVLA-Latent then learns to predict latent-action chunks from visual observations and language through flow matching, before adapting its pretrained backbone and action expert to embodiment-specific robot actions. The resulting 4B policy achieves 98.8% success on LIBERO, 84.7% on LIBERO-Plus without benchmark-specific adaptation, 51.9% average success across five VLABench tracks, and 88.6% average success on the RoboTwin 2.0 bimanual benchmark. It also achieves the highest observed success rates among the compared methods on six real-world manipulation tasks across dexterous-hand and mobile-gripper platforms. Together with representation ablations and data-scaling results, these findings demonstrate the potential of latent-action supervision for scaling robot policy learning beyond native action-labeled data.

---

## 18. HuGe: Scaling Humanoid Generalist Vision-Language-Action Models with Egocentric Experience

**Authors:** Yang Liu, Jiacheng Liu, Hengtao Li, ..., Lixin Yang, Donglin Wang
**arXiv:** [2610.34186](https://arxiv.org/abs/2610.34186)
**Categories:** Robotics (cs.RO)

Extending Vision-Language-Action models (VLAs) to humanoid robots requires coordinated whole-body control and diverse demonstrations that are costly to collect in real-world scenarios. Although egocentric human demonstrations provide a complementary source of task experience, differences in visual embodiment and missing robot proprioception complicate transfer to humanoid policies. To address these challenges, we introduce HuGe, a family of Humanoid Generalist VLAs pre-trained on over 2,000 hours of egocentric human and robot data. Specifically, HuGe employs three existing representative VLA architectures to predict latent motion tokens for a pretrained whole-body controller, together with hand-control signals. Based on this, we introduce a three-stage training pipeline that combines egocentric pre-training, humanoid adaptation, and downstream fine-tuning. To facilitate transfer across embodiments, we construct pseudo-proprioceptive states through simulation playback during pre-training and modify arm appearance in egocentric observations through re-rendering during downstream fine-tuning. With this pipeline, HuGe achieves the state-of-the-art on simulation benchmark HumanoidArena. Furthermore, real-world experiments on the Unitree G1 indicate that augmenting robot demonstrations with visually adapted egocentric demonstrations significantly increases success on a pick-and-drop task.

---

## 19. RoboDuo: Attempt, Check and Atomic Recovery through Code for Vision-Language-Action Models

**Authors:** Jie Wang, Bo Zhang, Renzhi Lu, Jianyu Chen
**arXiv:** [2610.34108](https://arxiv.org/abs/2610.34108)
**Categories:** Robotics (cs.RO); Computer Vision and Pattern Recognition (cs.CV)

Vision-Language-Action (VLA) models map a language instruction and the current observation directly to actions, without checking whether the instruction has been completed. For long-horizon tasks, a single failed step therefore goes unnoticed and leaves the whole task unfinished. Such failed episodes, however, often end with the task partially complete. Moreover, the unfinished steps are reusable atomic skills that recur across demonstrations. A failed attempt can thus be recovered by composing with atomic skills. We propose RoboDuo, a closed-loop dual-system framework that uses code as the interface between a coding agent and two VLAs. The agent writes a program that lets a full-task VLA attempt the whole task and checks whether it is complete; on failure, an atomic VLA finishes the remaining steps. Since the agent emits no actions and only decides which VLA for execution, RoboDuo wraps an existing full-task VLA without updating its weights. To train the atomic VLA and the coding agent with the completion-checking ability, we build LIBERO-Atomic, LIBERO-Code, and LIBERO-Judge from a single set of LIBERO demonstrations. RoboDuo consistently improves X-VLA and $\pi_{0.5}$ on LIBERO and LIBERO-PRO, with the largest gains on long-horizon tasks, and recovers failed rollouts of a frozen full-task VLA on a real robot.

---

## 20. EXE: Egocentric Cross-Embodiment Pretraining via Factorized Latent Actions for VLA Models

**Authors:** Qingyuan Cai, Bo Zhang, Yongzhen Huang, Jianyu Chen
**arXiv:** [2610.33685](https://arxiv.org/abs/2610.33685)
**Categories:** Robotics (cs.RO); Computer Vision and Pattern Recognition (cs.CV)

Vision-Language-Action (VLA) models are bottlenecked by the scarcity of robot data. Egocentric human manipulation videos offer an abundant, diverse, and semantically-rich alternative that inherently captures manipulation intent. However, the embodiment gap makes it difficult to extract action-relevant representations from these videos. From the perspective of action execution, human hands and robots share analogous manipulation primitives---reaching, grasping, placing---yet exhibit distinct kinematics tied to their embodiments. This might motivate our key approach: egocentric video pretraining can yield shared action representations capturing transferable manipulation skills, while human-specific motion patterns should be disentangled to avoid interfering with robot policy learning. To this end, we propose EXE, an Egocentric Cross(X)-Embodiment pretraining framework that learns a factorized latent action representation from egocentric human videos, separating shared manipulation priors from embodiment-specific signals. By leveraging the shared action space, the robot policy acquires generalizable manipulation semantics from diverse human demonstrations without being biased by human-specific kinematics. This shared knowledge transfers across embodiments with different kinematic structures, enabling the same pretraining to benefit both parallel grippers and dexterous hands. EXE yields consistent gains over baseline without pretraining on RoboTwin 2.0, RoboCasa GR1, and real-world manipulation tasks.

---
