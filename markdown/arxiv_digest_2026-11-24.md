# arXiv Daily Digest — 2026-11-24

**Mode:** direct
**Categories:** cs.AI, cs.LG, cs.RO, cs.CV
**Keywords:** VLA, RSI, RUA, agentic robot, self-improving robot, self-evolving robot, robot harness
**Papers found:** 34

---

## 1. Fin-RSI: A Unified Library of Financial Skills, Checks, and Self-Improvement for LLM Agents

**Authors:** Wanghao Ye, Shwai He, Sihan Chen, ..., Qiong Wang, Ang Li
**arXiv:** [2611.29716](https://arxiv.org/abs/2611.29716)
**Categories:** Artificial Intelligence (cs.AI)

As large language models (LLMs) become more capable, financial agents need tools they can readily discover and use. Yet financial software is fragmented across libraries with different interfaces and conventions, making it difficult to build reliable agent workflows. We present Fin-RSI, a unified Python library of financial skills, checks, and self-improvement designed for LLM agents. It brings together tools for market analysis, forecasting, portfolio construction, and trading research through shared interfaces across models and agent frameworks. Agents can find suitable tools from natural-language requests, reuse tested implementations, and improve generated programs through checking and feedback. Developers can extend the library with new tools without rebuilding integrations for each model. Across 20 open-weight models on six trading-position tasks, tool discovery increased the proportion of episodes producing valid programs from 9.7% to 29.2%; for models with at least 14 billion parameters, it rose from 23.6% to 64.6%. We release the library and benchmark as a shared resource for the community and plan to expand its tools and task coverage as financial agents evolve.

---

## 2. Diversity over Scale: Recursive Self-Improvement with Ensembles of Small Open-Weight Models

**Authors:** Navapat Nananukul, Mayank Kejriwal
**arXiv:** [2611.28420](https://arxiv.org/abs/2611.28420)
**Categories:** Artificial Intelligence (cs.AI)

The advancement of large language models (LLMs) has significantly enhanced the capabilities of agents across various tasks. Recursive self-improvement (RSI) loops, in which a language model repeatedly rewrites a program and builds on its previous version, now perform well in machine-learning tasks, but they rely on frontier models and hundreds of calls per run. Small open-weight models are far cheaper, yet when used alone, their programs often crash and their improvements stall. We propose DiVE (diverse models evolve), an ensemble method for RSI that aims to improve creativity and diversity of generated solutions. DiVE uses three components: a shared memory, a failure log, and best-idea-wins rounds. This allows models to write candidate solutions from the same context and retain the best idea at each iteration. On 22 MLE-bench Lite competitions, an ensemble of five 8-12B open-weight models has 25.4% less test error than its average member and 16.7% less than Llama 3.3 70B, and comes within 7.1% of Qwen 3.5 122B-A10B at 75% of its cost. Diversity among small models can thus stand in for part of the scale that RSI relies on.

---

## 3. FinEvo: Recursive Self-Improvement for Long-Horizon Financial Modeling

**Authors:** Chengjun Pan, Shichun Liu, Zekai Zhou, ..., Dingwei Zhu, Tao Gui
**arXiv:** [2611.28239](https://arxiv.org/abs/2611.28239)
**Categories:** Artificial Intelligence (cs.AI)

Advances in large language models (LLMs) have expanded their role in high-value productivity tasks, including financial analysis and modeling, while enabling models to play an increasingly active role in their own improvement. This motivates two complementary lines of inquiry: can financial modeling capabilities provide a foundation for model self-evolution, and can self-evolution, in turn, advance financial capabilities? We introduce FinEvo, a self-evolution framework that integrates autonomous experience construction with financial capability improvement. FinEvo prepares financial models, iteratively evolves challenges through self-play, and learns from the resulting interactions using executable rewards, relying on the same model throughout. An end-to-end execution with Qwen3.6-27B shows that solving feedback supports both increasing reasoning demands and identifying specification issues that executable checks can miss. Learning from these experiences raises whole-task success from 22.73 to 29.09 on held-out within-source tasks and from 13.13 to 19.19 on SpreadsheetBench 2 Financial. Comparable gains across task sources and evaluation settings, together with improvement on a task category absent from training, suggest that FinEvo strengthens underlying financial modeling capabilities shared across tasks. These findings support self-evolution as a path toward broader financial competence, advancing the empirical exploration of recursive self-improvement (RSI) in professional domains. Code is available at this https URL.

---

## 4. Beyond Self-Consistency: Recursive Self-Improvement at Test Time

**Authors:** Jianyu Wu, Yizhou Wang, Encheng Su, ..., Wanli Ouyang, Shixiang Tang
**arXiv:** [2611.30965](https://arxiv.org/abs/2611.30965)
**Categories:** Computation and Language (cs.CL); Artificial Intelligence (cs.AI); Machine Learning (cs.LG)

Large language models (LLMs) that continue improving after deployment (e.g., recursive self-improvement) offer a promising path toward general intelligence. Current test-time methods pursue this goal on unlabeled questions, primarily relying on self-consistency: they generate independent solutions and use majority voting to select an answer or construct training targets. This leaves earlier reasoning unused at inference and can reinforce an incorrect majority during training. Humans instead build on earlier attempts to preserve useful reasoning, correct mistakes and improve their problem-solving strategies. Following this principle, we propose Test-Time Recursive Self-Improvement (TT-RSI), a label-free framework for improving LLMs at test time through two mutually reinforcing components: (1) In-Context RSI repeatedly re-solves each question using the full previous solution as a reference, letting the model decide whether and how to use it so that inference compute builds on earlier reasoning. (2) In-Weight RSI distills successive refinements into the model's weights, enabling progress beyond an initially wrong majority and theoretically bringing the first attempt toward the model's infinite-step refinement limit. The updated model answers better and refines more effectively, generating stronger references for subsequent training. Extensive experiments show that TT-RSI improves average accuracy by +13.89% over the base model and outperforms the strongest self-consistency-based method by +4.79% under the same test-time scaling budget.

---

## 5. GeoMerge-OPD: Balanced Skill Integration in Vision-Language-Action Models

**Authors:** Le Yang, Haoyang Lyu, Honglei Jin, ..., Yutao Yue, Xiaochun Cao
**arXiv:** [2611.30632](https://arxiv.org/abs/2611.30632)
**Categories:** Robotics (cs.RO); Artificial Intelligence (cs.AI)

Vision-language-action (VLA) models excel at individual robotic skills, yet integrating heterogeneous skills into a single policy remains a key challenge for general-purpose robotic control, especially in whole-body tasks with differing manipulation and locomotion requirements. Common multi-skill integration strategies, such as joint fine-tuning and parameter merging, can induce unintended actions during closed-loop execution, severely degrading individual skills. Task-conditioned analysis of expert updates reveals response energy concentrated in a few dominant directions and opposing expert responses along high-energy directions within a shared, task-relevant response subspace. This structure co-occurs with unintended action shifts after merging. We propose GeoMerge-OPD, combining response-space regularization, parameter merging, and on-policy distillation. During independent expert fine-tuning, G-isometry constrains update-response gains within task-activation subspaces; the expert parameters are then statically merged into a student with preliminary multitask capabilities. Fine-tuned task experts serve as teachers, providing velocity-field supervision at the environment observations and intermediate action-flow states visited by the student to calibrate residual behavioral deviations. Experiments with two VLA backbones show strong, balanced humanoid skill integration on SIMPLE and consistent performance on LIBERO and LIBERO-PRO, outperforming joint fine-tuning and multitask reinforcement-learning baselines while maintaining robustness under perturbations.

---

## 6. OVOGO: Offline Value-Guided On-Policy Generative Optimization for Flow-Based Vision-Language-Action Models

**Authors:** Rongzheng Yang, Jiaming Guo, Yuxuan Guo, ..., Xing Hu, Yunji Chen
**arXiv:** [2611.30477](https://arxiv.org/abs/2611.30477)
**Categories:** Robotics (cs.RO); Artificial Intelligence (cs.AI)

Flow-based vision-language-action models can benefit from robot experience collected during deployment, but repeatedly acquiring new physical interactions for policy improvement is costly. Offline reinforcement learning provides a natural way to reuse collected experience, while flow-based policies offer an additional opportunity because fresh generation trajectories can be cheaply resampled from the current policy at replay observations. This motivates separating offline value learning from on-policy optimization of the generative process. We propose OVOGO, an offline reinforcement learning framework that realizes this separation for flow-based VLAs. A central challenge in this formulation is to learn a critic that remains grounded in logged robot experience while providing useful value signals for newly generated actions. OVOGO introduces a Return-Anchored Ranking Critic that combines in-sample distributional value learning with guarded local ranking, improving discrimination among generated actions without assigning them artificial return targets. The frozen critic then provides group-relative value signals for selected-transition optimization of fresh action candidates sampled from the current flow policy. Experiments on RoboTwin 2.0, DexJoCo, and LIBERO, as well as a real-robot dexterous manipulation task, show that OVOGO improves the initial VLA across all four settings and achieves higher success rates than the evaluated offline adaptation and value-guided baselines. These results suggest that offline robot experience can be repeatedly reused for value learning while inexpensive generative sampling supports policy optimization, providing an effective approach to experience-based post-training of flow-based VLAs.

---

## 7. LeadVLA: Learning Follower-Aware Route Execution for Robot Leading

**Authors:** Tianle Zeng, Hanjing Ye, Bingyi Xia, ..., Yonggen Ling, Hong Zhang
**arXiv:** [2611.30149](https://arxiv.org/abs/2611.30149)
**Categories:** Robotics (cs.RO); Artificial Intelligence (cs.AI); Computer Vision and Pattern Recognition (cs.CV)

Robot leading requires executing a route while continuously adapting to a designated follower. Existing robot-leading systems often mediate follower understanding and physical route execution through explicit states, planners, or modular interfaces; directly learning this coupling through end-to-end trajectory prediction can instead entangle route execution with follower response. We introduce LeadVLA, a structured multimodal policy that preserves the route as an explicit Path reference while learning a Pace for route progress and a Residual for local follower- and scene-conditioned adaptation. To make this problem trainable and measurable, we develop LeadInfra, a configurable Unreal Engine-based closed-loop data-generation infrastructure from which we instantiate an approximately 4M-sample training corpus, and LeadBench, a standardized benchmark with 108 fully held-out closed-loop episodes. LeadVLA achieves the highest task success (39.6%) among evaluated robot policies on LeadBench while maintaining strong route fidelity and follower responsiveness, and transfers to unseen real-world environments without real-world policy fine-tuning. Project Page: this https URL

---

## 8. Detecting Is Not Choosing: What a World Model Needs to Keep a VLA Policy Safe

**Authors:** Thanish Bolla
**arXiv:** [2611.29553](https://arxiv.org/abs/2611.29553)
**Categories:** Robotics (cs.RO); Artificial Intelligence (cs.AI); Machine Learning (cs.LG)

Vision-language-action (VLA) policies complete most benchmark tasks but often violate safety constraints. Since they are stochastic, one remedy is to sample several candidate action chunks and execute one that a world model predicts is safe. We ask what such a model must do. In simulation, a lookahead safety filter with the simulator as an exact world model raises the safety rate of three VLA policies on LIBERO and of pi0.5 on LIBERO-Plus by 11.5 to 25.7 points. It also helps pi0.5 on three RoboCasa tasks. Learned critics trained on one policy's data detect dangerous states (pooled AUROC up to 0.864) but rank candidates at one state close to chance (within-decision AUROC 0.551-0.560), and the learned dynamics and video models we test do no better. When the simulator's state is perturbed, selection degrades long before detection. In the loop, a median position error of 3.18 mm removes 70% of the gain on LIBERO-Spatial, partly because the error also corrupts the displacement check. On LIBERO-10 the loss is smaller, and the intervals overlap. The median does not predict the cost: a pixel reader with a 0.56 mm median error keeps 6.5 points less of the gain than Gaussian error of a similar median. A world model for safety should thus be judged by within-state ranking, and its state must be accurate in the tail and on handled objects, not only in the median.

---

## 9. From Vanishing Gradients to Recursive Self-Improvement: Evaluating the Most Influential Papers in Large Language Model Evolution (1997-2026)

**Authors:** Saadh Jawwadh
**arXiv:** [2611.29303](https://arxiv.org/abs/2611.29303)
**Categories:** Computation and Language (cs.CL); Artificial Intelligence (cs.AI)

The rapid proliferation of Large Language Model (LLM) research makes it increasingly difficult to distinguish incremental refinements from true paradigm shifts. This review evaluates 22 of the most influential publications spanning nearly three decades (1997-2026), organized through a causal, chronologically anchored taxonomy centered on the author's birth year (1999). Beginning "before 1999" with how recurrent neural networks (RNNs) forgot earlier context (much like forgetting Chapter 1 by the time a reader reaches Chapter 9), we trace how Long Short-Term Memory (LSTM) networks introduced a "bouncer" mechanism of forget, input, and output gates to selectively preserve long-term memory. We then examine how Word2Vec turned language into vector mathematics (king - male + female ~ queen), why sequential RNNs hit a parallelization wall, and how the Transformer's all-to-all attention weights launched the modern LLM era alongside a quadratic bottleneck. Next, we analyze why scaling parameters alone leaves capacity under-trained unless data scales equally (Chinchilla), how Reinforcement Learning from Human Feedback (RLHF) left alignment superficial, and how that gap compounded into adversarial jailbreaks and single-direction refusal subspaces (J-space), where instructing a model not to think of a restricted concept surfaces it much like the human "red ball" paradox. Finally, we synthesize the current state of AI (2024-2026), encompassing recursive model collapse, autonomous reasoning-model jailbreak agents, machine-speed agentic intrusions, and closed-loop recursive self-improvement (AIDE^2).

---

## 10. JEPA-Tuner: From Predictive Fine-Tuning to Asynchronous Execution of Vision-Language-Action Models

**Authors:** Jingxiang Qu, Tian Xie, Youngjin Hong, ..., Yang Katie Zhao, Yi Liu
**arXiv:** [2611.29096](https://arxiv.org/abs/2611.29096)
**Categories:** Robotics (cs.RO); Artificial Intelligence (cs.AI)

Vision-Language-Action (VLA) models generate sequences of actions from visual observations, proprioceptive states, and language instructions. In embodied interaction, executing these actions influences subsequent observations and robot states, providing a natural predictive signal for policy learning. However, standard action-supervised fine-tuning does not explicitly capture these action-conditioned temporal dependencies in the guidance consumed by the action predictor. We introduce JEPA-Tuner, a predictive fine-tuning framework that regularizes the VLA's native policy guidance through action-conditioned future prediction. During fine-tuning, a predictor in JEPA-Tuner learns to match guidance encoded from a future observation given the current guidance and committed actions. This objective encourages a cross-modal guidance adapter to capture how the scene and robot state evolve under those actions, while jointly training the action expert on both observed and predicted guidance keeps the representation informative for control. In addition, when deploying the VLA model with asynchronous action-chunk inference, the pre-trained predictor will anticipate the guidance needed at the next chunk boundary. The policy can thus generate the next chunk in advance and execute it from its first action without overlap correction or additional predictor training, enabling efficient and high-quality asynchronous execution. Experiments on LIBERO and Meta-World show that JEPA-Tuner improves task success under synchronous inference with better multi-modal guidance embeddings. For asynchronous control, JEPA-Tuner improves performance and smoothness across different latency settings on both LIBERO simulator and multi-size real robot demonstrations. The project website with video demos is at this https URL.

---

## 11. AsyncMixVLA: Runtime Asynchronous Robot Policy Switching for Adaptation to Dynamic Environments

**Authors:** Tamoghno Das, Keyon Jazayeri, Yerin Cho, ..., Arshia Aravinthan, Nikil Dutt
**arXiv:** [2611.28585](https://arxiv.org/abs/2611.28585)
**Categories:** Robotics (cs.RO); Artificial Intelligence (cs.AI); Systems and Control (eess.SY)

Vision-language-action (VLA) models translate visual observations and language instructions into robot actions, enabling general-purpose robotic control. However, environmental perturbations, such as objects moving during execution, can undermine their reliability. Different policies exhibit complementary failures under mid-rollout perturbations, motivating selective switching between policies for recovery. Such switching can stall the robot during inference of the newly invoked policy or, if performed asynchronously, act on stale observations. We present AsyncMixVLA, an adaptive inference framework for proactive, asynchronous switching across heterogeneous VLA policies. A learned trigger balances recovery potential against intervention harm to selectively escalate to a higher-compute policy. AsyncMixVLA overlaps its inference with committed outgoing actions and aligns its context to the anticipated takeover state. On LIBERO-Long with mid-rollout perturbations, AsyncMixVLA improves perturbed task success from 69.5% to 77.1% over the lightweight policy. It achieves 84.9% overall success, comparable to 84.5% for synchronous switching, while reducing median exposed handoff latency from 226.5 ms to 0.1 ms. Without retraining or recalibration, it achieves 75.1% success across three unseen perturbation families, compared with 71.3% for the stronger constituent policy in aggregate.

---

## 12. Pruning Autonomous Driving VLAs: What to Preserve for Reasoning and Action

**Authors:** Seongchan Kim, Soowon Son, Sangoh Kim, ..., Woongchan Nam, Seungryong Kim
**arXiv:** [2611.31240](https://arxiv.org/abs/2611.31240)
**Categories:** Computer Vision and Pattern Recognition (cs.CV); Machine Learning (cs.LG); Robotics (cs.RO)

Reasoning vision-language-action (VLA) models for autonomous driving use chain-of-thought (CoT) reasoning to guide action generation, but incur substantial memory and computational costs. We study structured pruning for these models, focusing on preserving both scene understanding and trajectory prediction. Our analysis of Taylor importance in Alpamayo-1.5-10B shows that reasoning and trajectory objectives assign different importance to the same vision-language model (VLM) structures. In the action expert, MLP channels exhibit more stable importance rankings across denoising steps than query heads, and a small fraction of channels accounts for most of the measured importance. Based on these findings, we propose MoOP, which combines importance ranks from both objectives for VLM pruning and aggregates stepwise importance to select a fixed subset of expert MLP channels. At 24.0% total parameter reduction, VLM-only pruning with MoOP performs comparably to or slightly better than the strongest baselines in driving, while retaining 94.0% of the dense model's LingoQA score, far above all other methods. At a higher reduction of 30.0%, MoOP degrades much less than every other method, as it is the only one whose reasoning does not collapse. Removing 93.75% of expert MLP channels increases total parameter reduction to 39.4%, with nearly unchanged open-loop errors relative to VLM-only pruning and competitive closed-loop performance. The resulting model achieves a 1.37x end-to-end inference speedup and 36.6% lower peak memory than the dense model, without post-pruning fine-tuning.

---

## 13. NoveltyGate: Novelty, Not Error, Decides Which VLA Prefix Tokens to Compute Exactly

**Authors:** Lemeng Qi
**arXiv:** [2611.31099](https://arxiv.org/abs/2611.31099)
**Categories:** Robotics (cs.RO); Machine Learning (cs.LG)

Flow-matching vision-language-action (VLA) models such as $\pi_{0.5}$ re-encode the camera images and the instruction with a 2B-parameter backbone at every control step, and the feed-forward layers of this prefix account for most of its compute. A natural way to save this compute is to send most tokens through a low-rank MLP and compute exactly only the tokens whose approximation error is large. We find that this intuition is wrong. Even a verifier that knows every token's exact error picks the wrong tokens, producing 1.3--1.7$\times$ larger action deviation than a simple test of whether a token's input is novel, that is, whether it falls outside the subspace seen during calibration. Large errors concentrate in tokens the policy relies on little, such as the third-person camera, while the novelty test favors the wrist camera, a view the action depends on heavily. We call this the error--reliance gap. Building on it, we propose NoveltyGate, a training-free method that routes each prefix token, once per layer and before any multiplication, to either a low-rank or the original MLP. Deciding once per layer instead of once per matrix product avoids moving wide intermediate tensors and keeps every shape static, so the whole prefix runs as a single CUDA graph. On LIBERO, NoveltyGate accelerates the $\pi_{0.5}$ prefix by up to 1.61$\times$, stays 2.7--2.9$\times$ closer to the original policy than channel pruning and low-rank compression at equal compute, and preserves closed-loop task success.

---

## 14. Hierarchical Reasoning Action Head for Tiny Vision-Language-Action Models

**Authors:** Aditya Makineni, Amitesh Sahoo, Qing Tian
**arXiv:** [2611.29813](https://arxiv.org/abs/2611.29813)
**Categories:** Computer Vision and Pattern Recognition (cs.CV); Machine Learning (cs.LG); Robotics (cs.RO)

Real-time onboard robot control calls for a lightweight vision-language-action (VLA) model, yet shrinking the backbone leaves less capacity for deliberation at inference time. Chain-of-thought decoding, dual-system architectures, and larger backbones can restore deliberation but reintroduce the latency and memory costs that motivated going small. Recurrent action heads offer a lighter alternative by iterating in latent space before committing to an action, but existing designs refine a single undifferentiated state that must simultaneously encode slowly evolving task context and rapidly changing motor commands. We propose the Hierarchical Reasoning Action Head (HR-AH), which maintains two latent states updated at different frequencies: a low-level state that updates fast, grounded in action tokens and proprioception, and a high-level state that updates slowly, grounded in visual understanding and the instruction-informed low-level state. The two states exchange information through nested reasoning cycles. Because all iteration occurs in the compact head after a single backbone pass, HR-AH adds hierarchical reasoning without increasing the backbone size. With a 22.5M-parameter head, 3-4.3x smaller than those of RD-VLA and VLA-Adapter on the same backbone, HR-AH reaches 97.0% success rate on LIBERO and a 4.40 average chain length on CALVIN ABC->D, at the lowest latency among compared methods. We show that this hierarchy improves performance over a parameter-matched single-state head, and that routing distinct modalities to each level yields further gains in both accuracy and inference cost.

---

## 15. JKO-GRPO: Augmenting GRPO with Wasserstein Proximal Steps for Flow-Matching VLAs

**Authors:** Jiyong Kwon, Yikun Bai, Amirhossein Mollaali, Guang Lin
**arXiv:** [2611.29646](https://arxiv.org/abs/2611.29646)
**Categories:** Robotics (cs.RO); Machine Learning (cs.LG)

Flow-based vision-language-action (VLA) models such as $\pi_0,\pi_{0.5}$ generate continuous action chunks by flow matching, and online reinforcement learning (RL) can improve them beyond supervised fine-tuning. Existing methods, such as Flow-GRPO and $\pi_{\mathrm{RL}}$, optimize likelihood ratios of stochastic denoising transitions, which reweight the sampled actions by their advantages but do not use the distances between them. We propose JKO-GRPO, which augments Flow-GRPO with Wasserstein proximal steps, with two contributions: (1) At each state, we treat the group of sampled actions as an empirical distribution and formulate policy improvement as a Jordan-Kinderlehrer-Otto (JKO) step. We use a soft discrete $c$-transform to construct transport targets from group-relative advantages and combine shared-noise regression of the deterministic flow sampler onto these targets and combined with the clipped Flow-GRPO objective without Kullback-Leibler (KL) regularization. (2) We extend this approach to sequential VLA control through random-time branching: we select one or multiple action-chunk indices along old-policy trajectories and independently apply group-level JKO updates using candidate continuations from the corresponding states.

---

## 16. Intervention-Robust VLA: Diverse Demonstrations for Robot Deployment with Safety Filters

**Authors:** Tzu-Yuan Huang, Shao-Hsuan Chang, Dai-Jie Wu, ..., Kenneth Marino, Sandra Hirche
**arXiv:** [2611.28289](https://arxiv.org/abs/2611.28289)
**Categories:** Robotics (cs.RO); Machine Learning (cs.LG); Systems and Control (eess.SY)

Vision-Language-Action models (VLAs) have shown strong potential for learning complex robotic behaviors from demonstrations. However, learning safe behavior directly from data requires extensive coverage of safety-critical situations, which is often impractical in real-world settings. Test-time safety filters provide an alternative by correcting unsafe actions during deployment, but these interventions can drive the robot into states poorly covered by the training data, thereby degrading task performance. We introduce InteR-VLA, an intervention-robust framework for VLAs that leverages diverse task-completing demonstrations to broaden task-relevant state coverage and maintain competence under safety interventions. By better aligning the training distribution with safety-filtered deployment under the same data budget, our approach mitigates intervention-induced distribution shift while preserving task performance. Real-world experiments across in-distribution and out-of-distribution settings show that InteR-VLA maintains safety, increases Safe Success Rate up to 90% from 0% for nominal policies, and consistently outperforms nominal-data training on both evaluated VLAs.

---

## 17. WeaveVLA: 3D Relational Grounding for Vision-Language-Action Models

**Authors:** Zien Wang, Yuhao Pan, Yunfeng Fan, ..., Xin Xia, Wenchao Xu
**arXiv:** [2611.31126](https://arxiv.org/abs/2611.31126)
**Categories:** Robotics (cs.RO); Computer Vision and Pattern Recognition (cs.CV)

Vision-language-action (VLA) models leverage pretrained vision-language representations for instruction-conditioned robot control, yet their understanding of task-relevant 3D relations and how these relations evolve during manipulation remains largely implicit. To address this challenge, we introduce WeaveVLA, a framework that enhances VLA action generation by explicitly modeling task-relevant relative 3D relations and maintaining relational context across observations. WeaveVLA employs a task-conditioned sparse graph neural network to encode relative 3D relations among objects, the gripper, and nearby references. Pair-specific recurrent edge states integrate geometric evidence across observations to maintain evolving spatial context. A learned-query readout summarizes the updated graph representations into compact relational tokens, which condition the action expert alongside the original vision-language context. An auxiliary geometry reconstruction objective further encourages spatial structure preservation. We instantiate WeaveVLA on StarVLA-GR00T and $\pi_{0.5}$, achieving over 98% average success on LIBERO with both backbones. On LIBERO-Plus, WeaveVLA improves success from 74.9% to 82.0% and from 85.7% to 87.8%, respectively, with additional improvements on CALVIN D$\rightarrow$D. On three real-world tasks, the StarVLA-GR00T-based variant improves average success from 55.6% to 70.0% under standard conditions and from 33.3% to 53.3% under OOD perturbations, surpassing the $\pi_{0.5}$ baseline in both settings.

---

## 18. RoboUniverse-10K: Toward the Scaling Era of Agentic Robotics via Real-to-Sim Environments

**Authors:** Jinkun Liu, Yingze Wang, Situ Wang, ..., Tiga Altman, Huan-ang Gao
**arXiv:** [2611.31002](https://arxiv.org/abs/2611.31002)
**Categories:** Robotics (cs.RO); Computation and Language (cs.CL)

Agentic Robotics, in which foundation models act as coding agents to control robots through executable programs, has emerged as a compelling paradigm for embodied intelligence. Yet unlike software engineering, where massive executable environments power post-training, robotics remains constrained by small, manual benchmarks and in-distribution evaluation. To bridge this gap, we introduce RoboUniverse-10K, 10,807 interactive, resettable, and verifiable physics environments built from real-world videos via an automated Real2Sim and quality assurance pipeline. Each runs in an isolated, Harbor-compatible harness that hides privileged states and grading logic to mirror real-world sensing. From the same pipeline, we hold out 500 unseen tasks to establish RoboUniverse-Verified, an expert-verified zero-shot benchmark. Evaluating 11 closed- and open-source models reveals a huge gap: frontier models reach 85.8\% success, while open-source baselines lag at 2.6\% to 10.0\%, bottlenecked by low-level grasping, deformable-object manipulation, and post-contact physical control. Finally, we collect about 17K multi-turn trajectories totaling 0.79B tokens with GPT-6 Astra and perform full-parameter supervised fine-tuning on Qwen3.6-35B-A3B, yielding RoboUniverse-35B-A3B. Our model achieves substantial zero-shot gains on RoboUniverse-Verified, lifting the success rate from 0.8\% to 21.2\%, while achieving zero-shot task completions across LIBERO-MAX, RoboCasa, RoboTwin 2.0, and a real Franka arm. We open-source the RL-ready environments and model to lay the foundation for large-scale reinforcement learning in Agentic Robotics.

---

## 19. Generalizing Agentic Robotics via Multi-Teacher On-Policy Distillation

**Authors:** Xinxin Liu, Anh Dao, Wenrui Bao, ..., Chen Chen, Yuzhang Shang
**arXiv:** [2611.30997](https://arxiv.org/abs/2611.30997)
**Categories:** Robotics (cs.RO)

Building general-purpose robots is a central goal in robotics. Agentic robotics pursues this goal with planners that control robots through tool calls. However, existing methods either rely on proprietary models accessed through APIs, which incur high costs and latency, or post-train a planner with reinforcement learning (RL) in a single domain, requiring a separate specialist for each domain with incompatible tools. In large language model (LLM) post-training, multi-teacher on-policy distillation (MOPD) has been used to consolidate domain specialists into a single generalist. Yet whether MOPD can build a generalist planner for agentic robotics, how well it performs, and how it compares with other consolidation methods remain unexplored. In this paper, we systematically study these questions: we introduce Robo-MOPD, which trains a single student on closed-loop rollouts in simulation under token-level supervision from matching frozen specialists, and compare it with weight merging, off-policy specialist supervised fine-tuning (SFT), and multi-domain online RL. Experiments on LIBERO-PRO and RoboCasa365 show that a single 9B Robo-MOPD planner reaches 72.9% and 44.8% success (58.9% average), surpassing all consolidated baselines in average success and both 9B specialists on their respective benchmarks. Robo-MOPD excels on long-horizon tasks, outperforming multi-domain online RL by 13.0 percentage points on LIBERO-10.

---

## 20. EgoStudy: How Does Scaling Egocentric Data Affect VLA and WAM Pretraining?

**Authors:** Puzhen Yuan, Yanjiang Guo, Yichen Liu, ..., Zhide Zhong, Jianyu Chen
**arXiv:** [2611.30490](https://arxiv.org/abs/2611.30490)
**Categories:** Robotics (cs.RO); Computer Vision and Pattern Recognition (cs.CV)

Egocentric human manipulation data offer a scalable resource for training dexterous robot policies. However, how effectively robots can learn and benefit from these data remains unclear due to the embodiment gap between humans and robots. We present EgoStudy, a systematic, controlled study of egocentric data for robot learning. Holding the robot dataset fixed, we vary the scale and diversity of egocentric data, data processing strategies, and co-training configurations. We investigate three questions: (1) Which data processing and pretraining choices most effectively exploit egocentric data? (2) Which components of robot action prediction benefit most from scaling these data? (3) How do scaling effects differ between vision-language-action models (VLAs) and world-action models (WAMs)? Our experiments yield three main findings. First, data diversity, alignment between trajectories, and detailed language annotations are key factors in effective transfer. Second, scaling egocentric data yields larger gains in predicting end-effector translation than in predicting fine-grained finger movements. Third, WAMs perform better when egocentric data are limited, whereas VLAs exhibit greater gains as the amount of egocentric data increases. Together, these findings provide practical guidance on processing and using egocentric data to train VLAs and WAMs, while clarifying the benefits and limitations of scaling these data.

---

## 21. ConsisX: Cross-View Consistency Thinking in 3D for Vision-Language-Action Models

**Authors:** Yunhe Zhang, Long Gao, Yuedong Fu, ..., Yuqi Zhu, Pengyu Li
**arXiv:** [2611.30308](https://arxiv.org/abs/2611.30308)
**Categories:** Robotics (cs.RO)

Vision-language-action (VLA) models integrate visual perception and language understanding from vision-language models (VLMs) with action prediction for robotic manipulation. Although multi-view observations provide complementary scene information, VLMs model cross-view interactions based on 2D feature similarity, which can lead to physical inconsistency in the form of cross-view incorrect association between distinct entities and cross-view information fragmentation about the same entity. To address these challenges, we propose ConsisX, a novel VLA framework that integrates cross-view association and entity coherence to enable cross-view consistency thinking in 3D for physically consistent robotic manipulation. Specifically, Cross-View Association Modeling (CAM) is proposed to introduce cross-view spatial proximity constraints in a shared 3D space to reduce cross-view incorrect association. Entity Coherence Organization (ECO) is designed to organize cross-view local information into coherent 3D entity evidence, thereby addressing cross-view information fragmentation. Consistent Action Conditioning (CAC) is introduced to condition action prediction on task-relevant 3D entity evidence for cross-view consistent action execution. Experiments on 3 real-world manipulation tasks and 4 simulation benchmarks establish ConsisX as an effective and competitive framework for robotic manipulation.

---

## 22. Beyond Which: Where, How, and When in Vision-Language-Action Models

**Authors:** Yunhe Zhang, Long Gao, Yuedong Fu, ..., Chang Wu, Songyuheng Gao
**arXiv:** [2611.30291](https://arxiv.org/abs/2611.30291)
**Categories:** Robotics (cs.RO)

Vision-language-action (VLA) models typically rely on vision-language model (VLM) features as the primary perceptual source for action prediction, showing strong generalization across diverse robotic manipulation tasks. Although VLM features can identify which entities are relevant to action prediction, precise manipulation also requires understanding where task-relevant entities are located within the spatial layout, how their geometric structure constrains physical interaction, and when spatial or geometric information should make a greater contribution to action prediction. To this end, we introduce {\mathcal{W}^{3}\mathcal{H}}-VLA to organize VLA perception and action prediction around which, where, how, and when. Specifically, {\mathcal{W}^{3}\mathcal{H}}-VLA retains VLM-based semantic entity perception which and further introduces spatial distance perception where and geometric structure perception how with adaptive spatial-geometric guidance when to enrich the perceptual information available for action prediction. Experiments across real-world settings and simulation benchmarks demonstrate the effectiveness and superior performance of {\mathcal{W}^{3}\mathcal{H}}-VLA.

---

## 23. Quantizing in the Loop: Drift-Aware Ultra-Low-Bit Vision-Language-Action Models

**Authors:** Yanlong Chen, Thongthornpatch Chamadol, Yichen Guo, ..., Addison Lin Wang, Yawei Li
**arXiv:** [2611.30178](https://arxiv.org/abs/2611.30178)
**Categories:** Robotics (cs.RO)

Deploying large vision-language-action (VLA) models on resource-constrained robots demands extreme compression, yet existing post-training quantization (PTQ) methods frequently collapse at ultra-low bit-widths ($\le$ 2 bits). We trace this failure to two mismatches in standard pipelines. First, calibrating on static offline demonstrations induces distribution shift: minor quantization perturbations drive the policy into unseen states where uncalibrated errors compound. Second, minimizing the layer-wise weight reconstruction error is a flawed proxy, as action generation depends only on the representations consumed by the action head. We present LoopQ, an on-policy ultra-low-bit quantization framework. LoopQ closes the loop by calibrating on states from the quantized policy's own rollouts. It then adds readout-aligned fine-tuning, which freezes the trellis codes and optimizes only lightweight lookup tables and scaling factors to align the backbone readout with the full-precision teacher. With all linear layers at 2 bits, LoopQ achieves a 60.4% success rate on LIBERO-Plus with GR00T N1.7, close to the 61.8% of full precision. Even at 1 bit per weight, $\pi_{0.5}$ still completes 80.0% of LIBERO tasks. With 8-bit activations, the 2-bit $\pi_{0.5}$ runs on integer kernels on an embedded NVIDIA Jetson AGX Thor, with 4.1$\times$ smaller weights and 44% less memory. On a real AgileX Piper arm, it stays within one success of full precision on each of three tasks. Code and checkpoints are available at this https URL

---

## 24. Self-Refining VLA Sampling

**Authors:** Jeff Duan, Arjun Sharma, Jennifer Cruden, Vansh Tibrewal
**arXiv:** [2611.29383](https://arxiv.org/abs/2611.29383)
**Categories:** Robotics (cs.RO)

Vision-Language-Action (VLA) models typically use flow-based generative modeling to learn a rich, often multimodal, distribution of robot actions. Generating samples from flow-based methods involves iteratively updating random noise, and distinct noise samples from the same state can result in distinct trajectories and task outcomes. Existing test-time scaling methods improve action chunk generation via selection, aggregation, or correction, but commonly require the generation of large ensembles of candidates or the training of an external corrector. We adapt Predict-and-Perturb (P&P), a self-refinement procedure for flow-based models originally used for mode-seeking in video generation, to the robotics domain. We find that applying P&P to VLA models requires modifications to the refinement process used in video generation due to differences in the underlying structure of the data. Across 400 episodes of LIBERO evaluated using SmolVLA, P&P improves upon the stock baseline by 5.3 percentage points. Further, episode-level P\&P uncertainty correlates strongly with task failure (AUC 0.851).

---

## 25. A2I-VLA: A Two-Stage Vision-Language-Action model with Semantic-Physical Alignment and Integration

**Authors:** Kun Dai, Tianqi Wang, Haibo Lei, ..., Tao Xie, Wenming Tan
**arXiv:** [2611.29279](https://arxiv.org/abs/2611.29279)
**Categories:** Robotics (cs.RO)

Force and tactile feedback provide essential information about physical interactions in contact-rich manipulation that visual observations alone cannot reliably this http URL, integrating these signals into vision-language-action (VLA) models remains challenging owing to the representational gap between visual-language semantics and physical this http URL address this challenge, we propose A2I-VLA, a two-stage VLA framework that first learns semantically Aligned force-tactile representations and then Integrates them into a VLA this http URL Stage I, a cross-modal alignment loss is introduced to promote correspondence between semantic and physical representations. The tactile and force feature streams are then integrated through a hierarchical multimodal fusion network, and the resulting representations are jointly supervised by future wrench and action prediction losses. The former encourages the model to anticipate physical responses, while the latter associates force-tactile observations with task-relevant manipulation this http URL Stage II, a gated cross-attention bridge module adaptively integrates the hierarchical physical features learned in Stage I into the VLA model to guide action this http URL-world experiments demonstrate that the proposed A2I-VLA significantly outperforms the baseline PI05 across three contact-rich manipulation tasks, improving the success rate from 70% to 95%.

---

## 26. LIBERO-MOR: A Multimodal Robustness Benchmark Across the Vision-Language-Action Pipeline

**Authors:** Qihang Chen, Tengjie Li, Hongwei Lu, ..., Shikui Tu, Lei Xu
**arXiv:** [2611.28867](https://arxiv.org/abs/2611.28867)
**Categories:** Robotics (cs.RO)

Vision-language-action (VLA) models have achieved strong performance on robot manipulation benchmarks. Translating this progress into reliable deployment calls for systematic evaluation of how policies respond to variations throughout the robot interaction loop. We introduce LIBERO-MOR, a multimodal robustness benchmark across the vision-language-action pipeline. Built on standard LIBERO, it covers five deployment-facing domains: vision, language, proprioception, action execution, and environment. The benchmark comprises 22 deployment-inspired perturbations, each evaluated at three severity levels across 40 tasks under a paired clean-perturbed protocol, enabling controlled and reproducible comparisons. We evaluate seven representative VLA models spanning diverse action-generation mechanisms. Our experiments reveal substantial robustness gaps behind high clean-task success, together with shared vulnerabilities and distinct model-specific failure patterns across domains. Severity analysis further distinguishes progressive degradation, collapse at stronger interventions, and failures triggered at the mildest tested level. By connecting aggregate performance to pipeline domains, individual perturbations, and intervention strength, LIBERO-MOR provides a systematic framework for diagnosing VLA robustness and guiding the development of more reliable robot policies.

---

## 27. AlpaSafe: Risk-Aware Trajectory Selection for Vision-Language-Action Models in Autonomous Driving

**Authors:** Qiren Wang, Mingyu Guo, Weisong Shi
**arXiv:** [2611.28509](https://arxiv.org/abs/2611.28509)
**Categories:** Robotics (cs.RO); Computer Vision and Pattern Recognition (cs.CV)

Reasoning-based driving vision-language-action (VLA) models propose multiple candidate trajectories at each decision, yet only one is executed. Standard evaluation scores the best candidate, assuming an oracle selector that deployment lacks, and leaves the risk of the executed candidate unexamined. Existing online evaluators typically close this gap with a purpose-trained scene or world model, often rolling out each candidate through it at inference time. We introduce AlpaSafe, a risk-aware trajectory selector that reuses the scene representation a frozen driving VLA computes while proposing its candidates. AlpaSafe reads the last hidden token of the VLA's prompt prefill. A lightweight head, trained on the closed-loop simulation outcomes of the candidates, fuses this token with each candidate trajectory and predicts a relative score and collision/offroad logits. A fixed rule removes candidates dominated on the two risk logits and selects the highest-scoring candidate among those remaining, adding neither rollouts nor VLA training. Experiments on 525 AlpaSim scenes show that AlpaSafe outperforms Alpamayo's default first-sample rule and uniform random selection in selected regret and top-1 agreement, and reduces the collision-at-fault or offroad rate from 6.41% and 6.10% to 4.93%. The selector has 1.7M parameters and takes 0.75 ms per decision.

---

## 28. Defending Vision-Language-Action Models against Transferable Attacks via Visual-Proprioceptive Consistency

**Authors:** Jiahao Wang, Ming F. Li, Han Xu
**arXiv:** [2611.28346](https://arxiv.org/abs/2611.28346)
**Categories:** Robotics (cs.RO); Computer Vision and Pattern Recognition (cs.CV)

Vision-Language-Action (VLA) models have demonstrated strong capabilities in a wide range of robotic tasks. However, adversarial attacks in VLA models have shown strong transferability across robotic tasks, posing significant threats to robotic systems. Despite their different attack strategies, we observe that these transferable attacks share a common consequence: they disrupt the VLA model's perception towards the robot itself. Motivated by this observation, we propose a proprioception-grounded defense framework that leverages trusted proprioceptive information to detect and mitigate transferable adversarial attacks. Specifically, we utilize the robot's proprioceptive states to establish a trusted spatial reference, and compare it with the robot's perceived location inferred from visual features. Discrepancies between these two sources provide a reliable signal for detecting adversarial attacks. Extensive experiments demonstrate effective detection of transferable adversarial patches and improved closed-loop performance. Real-robot experiments further demonstrate the effectiveness of our defense on real-world robotic tasks.

---

## 29. FlowPAC: Flow-Guided Visual Pruning and Action Caching for Efficient VLA Inference

**Authors:** Jintao Cheng, Yipu Zhang, Haozhe Wang, ..., Jiang Xu, Wei Zhang
**arXiv:** [2611.28256](https://arxiv.org/abs/2611.28256)
**Categories:** Robotics (cs.RO); Computer Vision and Pattern Recognition (cs.CV)

Vision-Language-Action (VLA) models have emerged as a powerful paradigm for embodied AI, yet their high inference latency and memory footprint remain major barriers to edge deployment. Existing training-free acceleration techniques, such as visual token pruning and action caching, typically rely on static resource allocation. This mismatch with dynamic robotic interactions not only degrades control performance but also causes severe hardware inefficiencies, including fragmented KV-cache layouts and wasted compute on non-critical regions. To address this, we propose FlowPAC, a locality-aware framework that leverages task-aware optical flow as a shared physical signal to jointly optimize visual and action computation. Specifically, we introduce Direction-Aware Trajectory Propagation (DATP) and Locality-Aware Contiguous Token Selection (LACT) to jointly handle visual token dynamics and enforce spatial locality, reducing memory fragmentation and enabling efficient KV-cache compression. This is complemented by Flow-Conditioned Action-Block Refresh (FCAR) for adaptive action computation based on motion dynamics. Extensive closed-loop evaluations on LIBERO demonstrate that FlowPAC achieves a 2.13$\times$ end-to-end speedup over the dense baseline while essentially maintaining the success rate with 30% visual-token retention. These results validate that aligning computation allocation with both physical dynamics and hardware constraints is essential for efficient VLA deployment on edge systems.

---

## 30. RMR-VLA: Recurrent Memory Reasoning for Vision-Language-Action Models

**Authors:** Yiheng Du, Jingqi Tian, Xu Jiang, ..., Zecheng Tang, Jian Zhang
**arXiv:** [2611.30145](https://arxiv.org/abs/2611.30145)
**Categories:** Computer Vision and Pattern Recognition (cs.CV); Robotics (cs.RO)

Long-horizon, history-dependent robotic manipulation often requires acting on visual cues that have disappeared, such as an object indicated earlier or a target hidden under a moving cup. The key challenge is to maintain what past evidence means for the next action as the scene changes. We introduce Recurrent Memory Reasoning (RMR), an explicit reasoning step that connects memory to action inside a vision-language-action model (VLA), with no external reasoning model. At each update, the VLA first infers an event from visual evidence, then revises the task state and grounds a subgoal in the current scene to guide action generation. Carrying the state and subgoal across updates lets remembered identities and task progress determine the current target, doubling RoboMME success over an otherwise identical model without recurrence. Joint training lets one VLA both reason and act; because its memory decisions are text tokens with exact likelihoods, GRPO refines them from rollout rewards without making action generation stochastic. Among the compared methods, RMR-VLA achieves the best results on RoboMME (66.46% overall, 79.83% on the Reference category) and LIBERO-Mem (90.08%).

---

## 31. Spatially Grounded Latent Lookahead for Vision-Language-Action Models

**Authors:** Qihang Chen, Tengjie Li, Hongwei Lu, ..., Shikui Tu, Lei Xu
**arXiv:** [2611.28839](https://arxiv.org/abs/2611.28839)
**Categories:** Computer Vision and Pattern Recognition (cs.CV); Robotics (cs.RO)

Vision-language-action (VLA) models benefit from strong semantic representations that support object recognition and instruction understanding. However, precise manipulation also depends on resolving object locations and workspace relations, and on selecting actions with an estimate of how the scene will evolve. Existing geometry-aware methods make the current scene more explicit, while predictive methods model future observations or representations. Yet future information is often neither grounded in a control-relevant spatial state nor directly used to guide action generation. We introduce Spatially Grounded Latent Lookahead (SG-LL), which uses the grounded present as the reference for predicting an actionable near-future representation. A frozen spatial teacher first distills geometric priors into policy-connected spatial tokens. A current-conditioned bottleneck then learns a compact latent that captures future information relative to the present scene. This latent is predicted from the current policy context and initial Action Expert features, without access to future observations or the spatial teacher. Finally, zero-initialized residual fusion incorporates the predicted latent into the Action Expert to refine action generation. Experiments on LIBERO-Plus, CALVIN, and three real-world manipulation tasks demonstrate improvements over
in both simulation and real-robot settings.

---

## 32. DriveDreamer-RSI: Recursive Self-Improvement of Driving Perception and Agentic Data Generation

**Authors:** Dingyi Yao, Tingdong Yu, Guosheng Zhao, ..., Lihui Peng, Zheng Zhu
**arXiv:** [2611.30671](https://arxiv.org/abs/2611.30671)
**Categories:** Computer Vision and Pattern Recognition (cs.CV)

Controllable generation can expand training data for driving perception, but visual realism alone does not ensure learning gains. Effective generation must adapt both what data to generate and how to construct them as the perception model evolves. In this paper, we present DriveDreamer-RSI, a framework for recursive self-improvement of driving perception and agentic data generation through feedback between perception learning and data construction. Its outer loop implements Gap-Guided Target Adaptation, generating labeled videos from current perception gaps and updating targets after training. Its inner loop uses a vision-language agent to iteratively edit scenes through observation and execution feedback. Across rounds, Learning-Feedback-Driven Strategy Refinement derives reusable construction advice from execution experience and downstream learning outcomes. On the nuScenes validation set, DriveDreamer-RSI surpasses the dataset-replay baseline by 4.09 mAP and 4.13 NDS points using approximately half the synthetic frames.

---

## 33. MM-DataLoop: Closing the Data-Side Loop for Recursive Self-Improvement in MLLM Post-Training

**Authors:** Likang Peng, Chen Ju, Xu Chen, ..., Haihong Tang, Ying Chen
**arXiv:** [2611.29254](https://arxiv.org/abs/2611.29254)
**Categories:** Computer Vision and Pattern Recognition (cs.CV)

Recursive self-improvement (RSI) offers a path toward improving models through repeated evaluation and revision. We study its data side in multimodal language model (MLLM) post-training, where heterogeneous operations and cross-round evidence must be coordinated. MMDataLoop organizes data interventions into five operation families and connects them through an Observe-Diagnose-Plan-Execute-Verify-Reflect cycle with shared rule memory. Across 34 candidate rounds on Qwen3.5-0.8B and five benchmarks, we hold the base initialization, shared training schedule and evaluation protocol fixed while varying data recipes. The five-benchmark mean reaches 63.04 at R33, up 5.32 points from the zero-shot baseline; R29, R32, and R33 form a close top cluster within 0.09 points. In eightcandidate comparisons, guided search reaches the preselected target in six candidates and identifies the top observed candidate, while random arms show higher means and lower dispersion. The selected R29 recipe also scores above two full-pool baselines under the same epoch schedule. Together, these findings establish MM-DataLoop as a traceable workflow and provide an empirical basis for studying how data-side decisions shape outcomes across MLLM post-training recipes.

---

## 34. GenPA: Image Generators as Efficient Robot Policies

**Authors:** Zian Deng, Tianyi Zhang, Zilong Zheng, ..., Yao Lyu, Shengbo Eben Li
**arXiv:** [2611.27446](https://arxiv.org/abs/2611.27446)
**Categories:** Robotics (cs.RO); Computer Vision and Pattern Recognition (cs.CV)

Pretrained visual generation models have shown great promise in robotic manipulation. However, a representative line of work still treats future visual prediction as the central link between visual generative pretraining and action learning, retaining it as a training objective even when future scenes are no longer generated at inference time. We argue that the instruction-following, spatial understanding, and visual imagination capabilities acquired through image generation pretraining can support control without future visual prediction: image generation models themselves can be directly adapted into powerful action learners. Building on this perspective, we propose GenPA, which fine-tunes an image generation backbone with a lightweight 19M-parameter action regression adapter and reuses its native generative objective for perception co-training. The native image-editing interface accommodates different visual targets without task-specific perception heads, enabling comparisons of current-scene perception, future prediction, and their combinations within a common policy architecture. At deployment, GenPA requires only a single backbone forward pass and action regression, without visual generation or iterative action denoising. Without additional large-scale robot-data pretraining, GenPA demonstrates strong control performance and robustness to perturbations across simulation benchmarks (99.10% success on LIBERO and 83.79% on LIBERO-Plus) and real-world manipulation tasks. Under compiled inference, GenPA takes 20.9 ms per action chunk on a single H100 GPU, achieving 1.7-3.4x speedups over strong VLA and WAM baselines. Our latency analysis further highlights architectural advantages of visual generation backbones for efficient robot control. Ablations across visual tasks and their combinations identify current-depth supervision as a simple, effective training recipe.

---
