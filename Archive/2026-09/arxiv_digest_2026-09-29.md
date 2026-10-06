# arXiv Daily Digest — 2026-09-29

**Mode:** direct
**Categories:** cs.AI, cs.LG, cs.RO, cs.CV
**Keywords:** VLA, RSI, agentic robot, self-improving robot, self-evolving robot, robot harness
**Papers found:** 54

---

## 1. RSI-Master: Structuring Experiments to Guide Autonomous Model Improvement

**Authors:** Yaxin Du, Xiyuan Yang, Zhifan Zhou, ..., Zixing Lei, Siheng Chen
**arXiv:** [2609.35561](https://arxiv.org/abs/2609.35561)
**Categories:** Artificial Intelligence (cs.AI)

Recursive self-improvement (RSI) seeks to enable AI systems to participate in improving their own capabilities. A concrete pathway is autonomous model development, where agents iteratively explore post-training strategies to improve a base model. This setting faces two challenges: agents may exploit open-ended experimental actions through hacking, and repeated experimentation may lead to strategy lock-in, where an early direction is refined rather than reconsidered. We introduce RSI-Master, which addresses the two challenges at two levels: regularize step-wise actions, avoiding hacking behaviors, and promote well-structured exploration of research directions, avoiding strategy lock-in. RSI-Master consists of an Experiment OS, which enables regularized experimental actions and maintains persistent, traceable experimental records, and Reviewer-Guided Research Orchestration, which organizes Workers and Reviewers in a dynamically growing research DAG. Workers explore diverse research directions and Reviewers compare evidence across related experiments for subsequent explorations. On PostTrainBench with Qwen3-4B-Base, it averages 54.49 versus 46.53 for the strongest agent baseline, with a 0.0\% hacking rate. Scaling to 35B model, RSI-Master surpasses the human-developed Instruct model on LiveCodeBench-v6 (41.21 vs. 37.36) and SciCode, and reaches a nonzero score on HorizonMath, a benchmark of unsolved research problems on which most frontier models score near zero.

---

## 2. Sol-H3: Recursive Self-Improvement for MiniMax-H3 Inference Acceleration on Sol-Engine across Cloud and Edge

**Authors:** Yitong Li, Jincheng Yu, Junsong Chen, ..., Song Han, Enze Xie
**arXiv:** [2609.35110](https://arxiv.org/abs/2609.35110)
**Categories:** Artificial Intelligence (cs.AI); Computer Vision and Pattern Recognition (cs.CV); Machine Learning (cs.LG)

Video diffusion models are rapidly scaling and exhibiting enhanced generation capabilities. Among these recent advancements, MiniMax-H3 stands out as a highly capable, production-level open-source model. However, its 33-billion parameters and multi-step iterative denoising process introduce substantial computational overhead. Consequently, their practical production is hindered by generation latency in the cloud deployment like NVIDIA-GB200, alongside strict memory limits that pose further challenges at the edge device like DGX-Spark. To address these diverse hardware bottlenecks from cloud to edge device, we present a full-stack inference pipeline that integrates efficient algorithmic design with optimized operator implementations. Algorithmically, we introduce a cross-resolution two-stage generation scheduler that exploits the step-wise nature of diffusion: early low-resolution steps rapidly establish the global layout, while later high-resolution steps focus refinements of local and perceptual details. These stages are connected by a learned latent-to-latent mapping module, completely eliminating the computationally expensive VAE decode-reencode cycle for resolution transferring cross different resolutions. For operator implementation, we deploy a Recursive Self-Improvement (RSI) loop that searches kernel fusions and memory layouts, evaluating latency together with numerical agreement. Together, these optimizations deliver up to 30x end-to-end speedup and 20% lower memory: a 5-second 1344x768 video with audio is generated 3.5x faster than real time on an 8xGB200 node, and in under a minute fully memory-resident on a single DGX Spark.

---

## 3. RSI-Router: Evolving Subtask-Level LLM Routing and Skills for Cost-Efficient Agents

**Authors:** Hao Li, Hangfan Zhang, Zhiyao Cui, ..., Danyang Jia, Shuyue Hu
**arXiv:** [2609.34712](https://arxiv.org/abs/2609.34712)
**Categories:** Artificial Intelligence (cs.AI)

Practical deployment of large language model (LLM) agents requires strong task performance at affordable inference cost. For long-horizon agentic tasks, this performance-cost trade-off can be improved through within-task large-small model collaboration, as smaller models can handle some stages even when they cannot solve the full task. In this paper, we introduce RSI-router, a routing framework that constructs subtask-level model assignments and model-specific skills through recursive self-improvement over accumulated experience. Each iteration consists of four stages: Subtask Mining derives subtask definitions and identification rules from training trajectories; Routing Strategy Evolution proposes and evaluates diverse model assignments; Model-Specific Skill Evolution compares routed and large-model-only trajectories to diagnose failures and develop reusable execution skills; and Pareto-Optimal Router Selection updates the Pareto population using historical and newly generated routers while retaining dominated routers as experience for subsequent evolution. Routing between DeepSeek-V4.1-Flash and Qwen3.5-9B, RSI-router consistently surpasses the DeepSeek-only baseline at roughly half the inference cost (48.3%) across five agentic benchmarks. In particular, on ALFWorld, ScienceWorld, and WebShop, it cuts inference cost by 74.7-82.2% while simultaneously improving performance; on Terminal-Bench 2.0, it achieves a 16.7% relative performance gain at 18.0% lower cost. Moreover, RSI-router establishes a stronger performance--cost Pareto frontier than 9 routing methods.

---

## 4. R$^2$ Flow: Recursive Self-Improvement via Recursive Skill Evolution

**Authors:** Mingda Zhang, Qiang Huang, Yanjin Li, ..., Xiaoying Tang, Tiesunlong Shen
**arXiv:** [2609.33867](https://arxiv.org/abs/2609.33867)
**Categories:** Artificial Intelligence (cs.AI)

LLM-based agents can improve themselves across tasks by reusing and revising the skills they orchestrate into executable procedures. Flow-based training fits this loop: it samples procedures in proportion to reward, and the flow through each skill credits it for the next library revision. Three obstacles stand in the way of making this self-improvement reliable: flow training suffers strategy collapse over tree-structured histories; nonnegative flow-based credit rewards frequent use as if it were benefit; and library edits rest on the task reward the policy optimizes. We introduce R$^2$ Flow, a recursive self-improvement framework that alternates policy learning, independent verification, and versioned skill-library updates on a shared-state orchestration graph. The graph merges histories that differ only in the order of independent steps, allowing flow training to pool evidence across equivalent executions. A flow-share readout of the trained flow, invariant to the backward policy, and a separate signed utility rank which skills to change, verifier evidence decides whether an edit is warranted, and a residual-variance plateau sets when to update. Committed edits reshape the graph the next policy learns on, realizing recursive skill evolution. Across question answering, mathematical reasoning, interactive decision making, and code generation, R$^2$ Flow improves task accuracy and library-edit precision over heuristic orchestration, reinforcement learning, and skill-evolution baselines, and transfers across executors. Code is available at this https URL.

---

## 5. Does Adversarial Training Improve Generalization in Multi-View VLAs? Revealing and Mitigating View Collapse

**Authors:** Futa Waseda, Shuhei Kurita, Isao Echizen
**arXiv:** [2609.33707](https://arxiv.org/abs/2609.33707)
**Categories:** Artificial Intelligence (cs.AI); Robotics (cs.RO)

Vision-language-action (VLA) models adapt pretrained vision-language models (VLMs) for closed-loop robot control, transferring their perceptual and semantic capabilities to action prediction. Despite strong in-distribution performance, however, VLAs often degrade under deployment shifts. Adversarial training (AT) offers a model-adaptive approach to robustness without explicitly anticipating individual shifts, but its effect on natural distribution-shift generalization in multi-view VLAs remains unclear. We study this question using a multi-view VLA directly adapted from a pretrained VLM and evaluate generalization across seven LIBERO-Plus shift axes. Direct AT substantially improves Camera Viewpoint and Sensor Noise, the two shifts affecting only the third-person view, yet produces mixed or negative effects on other shifts. Controlled view interventions reveal a surprising failure mode that we term view collapse: Direct AT can shift cross-view reliance so strongly that the policy becomes dominated by the wrist view. This exposes a \textit{robustness shortcut}: apparent robustness to a shifted view can arise from reduced use of that view rather than more robust perception of it. This motivates a distinction between robust perception, extracting reliable information under within-view shifts, and robust fusion, adapting reliance across views according to their reliability. To reduce fixed view reliance, we use a simple View Swap intervention and then re-evaluate AT. With View Swap, AT further improves Camera Viewpoint, Sensor Noise, and Robot Initial State, while its effects remain mixed on other shifts. Our results show that multi-view robustness requires separating improved perception from changes in cross-view reliance, and that AT provides selective rather than generic distribution-shift benefits.

---

## 6. COEVO: Co-Evolving Context and Parameters for Recursive Self-Improvement

**Authors:** Siwei Chen, Xinping Bao, Xinyu Cai, ..., Wan Jiang, Shaohong Chen
**arXiv:** [2609.33398](https://arxiv.org/abs/2609.33398)
**Categories:** Artificial Intelligence (cs.AI)

Recursive self-improvement (RSI) seeks to move large language models beyond static training pipelines toward systems that can participate in improving their own future behavior. Existing approaches largely follow two directions: updating model parameters through online learning, or improving the external context through search, reflection, and prompt optimization. Although both mechanisms can support continued improvement, they are typically studied independently. This separation overlooks an important interaction: the context shapes the experience from which a model learns, while an evolving model may interpret and utilize the same context differently over time. We therefore formulate RSI as a problem of parameter--context co-evolution, where model parameters and the learning context adapt within a shared feedback loop. We introduce COEVO, a framework that updates model parameters from on-policy experience while adapting contextual guidance according to the state of the evolving policy. Policy entropy and prompt-conditioned attention are used as complementary signals to guide this adaptation. Experiments show that COEVO consistently improves task performance over fixed-context reinforcement learning and produces policies that are more robust to changes in system prompts. More broadly, our results suggest that external context should be viewed not merely as a fixed interface to a large language model, but as an adaptive component of recursive self-improvement.

---

## 7. Are Vision-Language-Action Models Robust to One-Step Observation Perturbations?

**Authors:** Shojiro Yamabe, Jun Sakuma
**arXiv:** [2609.32550](https://arxiv.org/abs/2609.32550)
**Categories:** Artificial Intelligence (cs.AI); Machine Learning (cs.LG); Robotics (cs.RO)

Understanding the safety risks of vision-language-action (VLA) models is essential for their deployment in the physical world. Existing safety research has mainly considered persistent perturbations that are applied continuously to observations throughout an episode. However, momentary observation corruption, in which observations are severely perturbed only briefly within an episode, remains an underexplored safety threat. To address this gap, this work investigates robustness to one-step perturbations applied at a single time step per episode. Our experiments reveal that these perturbations substantially degrade VLA performance and that their impact depends on the action chunk execution length. Based on them, we propose CARE, which dynamically selects the execution length based on consistency with the previously predicted action chunk. CARE improves robustness with low computational overhead while preserving clean performance by selecting shorter execution lengths only under perturbations.

---

## 8. PluginRSI: Recursive Improvement of Agent Harnesses with Reusable Plugins

**Authors:** Yaorui Shi, Yuchun Miao, Yuxin Chen, ..., Xiang Wang, An Zhang
**arXiv:** [2609.32423](https://arxiv.org/abs/2609.32423)
**Categories:** Artificial Intelligence (cs.AI)

The harness surrounding a language model is a central determinant of agent performance. Recent methods optimize harnesses by searching over complete programs, where individual mechanisms are difficult to isolate and reuse. We introduce PluginRSI, which represents a harness as a composition of atomized plugins and organizes harness evolution around these plugins. Individual plugins are improved independently and accumulated in a shared library, then recombined into new harnesses at each iteration. PluginRSI improves over existing harness optimization methods across software engineering, command-line interaction, and question-answering tasks. The resulting harnesses retain their advantage when transferred to other solver models without further optimization. The evolved plugin library accelerates subsequent optimization from the initial harness, which helps faster and higher convergence on unseen tasks. These results show that accumulating reusable mechanisms provides an effective basis for continued harness improvement.

---

## 9. ConflictVLA-Bench: Benchmarking Behavioral Responses of Vision-Language-Action Models to Premise Conflicts

**Authors:** Liyu Hou, Yuan Wu, Yi Chang
**arXiv:** [2609.31792](https://arxiv.org/abs/2609.31792)
**Categories:** Artificial Intelligence (cs.AI); Robotics (cs.RO)

While Vision-Language-Action (VLA) models perform strongly on manipulation tasks, their responses to invalid task premises remain underexplored. Existing evaluations of premise conflicts often focus on terminal task outcomes, yet task failure alone cannot distinguish behavioral disengagement from continued pursuit followed by an execution error. We call the latter pattern Failed Persistence. To study this phenomenon, we introduce ConflictVLA-Bench, which pairs conflict rollouts with premise-consistent reference rollouts and evaluates both outcomes and execution processes. Built on LIBERO, the benchmark contains 2,826 prompt-conditioned conflict tasks spanning four conflict families, four structural configurations, and two prompt conditions. Across all eight VLAs, invalid premises reduce original goal completion by at least 17.3 percentage points, with the reduction reaching 56.2 percentage points for OpenVLA. Crucially, even when models succeed on premise-consistent tasks and fail on their matched conflict tasks, they often continue to approach the original targets, retain early trajectory structure, and show limited action magnitude suppression. Failed Persistence therefore recurs across the evaluated models. Explicit premise checking does not consistently produce selective and coordinated behavioral changes. These findings show that terminal failure alone establishes neither behavioral disengagement nor refusal and that outcomes alone are insufficient for VLA evaluation. Experimental data and additional details are available on the project page: this https URL

---

## 10. Learning to Act under Visual Interruptions with Vision-Language-Action Models

**Authors:** Mingle Jiang, Rui Xu, Yunke Wang, Chang Xu
**arXiv:** [2609.35003](https://arxiv.org/abs/2609.35003)
**Categories:** Robotics (cs.RO); Artificial Intelligence (cs.AI)

Vision-language-action (VLA) models have demonstrated strong capabilities in robotic manipulation, but they are typically developed and evaluated with all camera streams available throughout task execution. When a camera stops delivering frames during task execution, the policy must continue acting without access to subsequent observations from the missing view. Despite its practical importance, how such interruptions affect closed-loop manipulation remains insufficiently understood. To investigate this problem, we introduce MAIL-Bench, a benchmark that evaluates visual interruptions with VLA models. By interrupting different cameras at multiple stages of each policy's successful reference trajectory, MAIL-Bench measures how well policies retain their capabilities when visual inputs become unavailable. Building on this benchmark, we propose MINT, which first trains VLA policies to remain functional under missing visual inputs. At inference time, MINT selectively supplements missing observations using optical-flow extrapolation or an action-conditioned world model, and withdraws predicted views when they become unreliable. Experiments on $\pi_{0.5}$ and GR00T N1.5 show that MINT significantly improves task success under camera loss over the original models. Experiments on AgiBot G2 further demonstrate the real-robot deployment under camera loss. The benchmark is available at this https URL

---

## 11. Audit the Scaffold, Not the Checkpoint: A Stationarity Dichotomy for Recursive Self-Improvement in Agentic Coding

**Authors:** Sebastian Bobadilla-Suarez, Bob Suh, Ryan Fortin
**arXiv:** [2609.34924](https://arxiv.org/abs/2609.34924)
**Categories:** Machine Learning (cs.LG); Artificial Intelligence (cs.AI); Software Engineering (cs.SE)

An auditor who checks whether a system's weights are frozen is checking the wrong thing. Our stationarity dichotomy says that iterative self-modification hits strict diminishing returns whenever the agent's reachable set of edits stays fixed, and can escape only if that set expands. Rewriting scaffolding (tools, verifiers, decomposition) expands what an agent reaches without touching a weight, so frozen weights buy an eventual ceiling but no stationarity along the way. The criterion also separates three regimes usually merged: search within a fixed class, test-time training that raises the ceiling itself, and scaffold rewriting between them. Audit the scaffold, not the checkpoint.
The same ceiling binds sideways. Best-of-$k$ orchestration realizes the best worker's ceiling exactly: width buys rate, not budget. Re-consulting a fixed pool has a horizon computable in advance, decided by the pool alone, and the one arrangement that would beat it, a weighted vote, needs diversity real workers lack: on 30 same-family workers the failure overlap sits at its maximum, and a majority fails 23/55 (42%) of tasks.
We obtain the criterion by reading refinement as gradient boosting on the residual error between draft and target, a patch or git diff, and then measuring where that reading breaks: patches compose instead of standing beside each other to be voted on, and failures overlap. What we measure is saturation. Per-round improvement decays toward zero on SWE-bench, and churn decays geometrically across 401 production sessions, a shape shared with a pre-AI human baseline that establishes the regime without identifying its cause. Both breaks are engineering choices rather than laws about code, so together they specify a harness worth building.

---

## 12. Resolving State-Representation Mismatch: State-Space Visual Reasoning for Open-Loop VLA Planning

**Authors:** Junhao Xiao, Haoxiang Zhao, Menghao Fang, ..., Youjun Bao, Zhiyuan Ma
**arXiv:** [2609.33412](https://arxiv.org/abs/2609.33412)
**Categories:** Computer Vision and Pattern Recognition (cs.CV); Artificial Intelligence (cs.AI)

Despite rapid progress in vision-language-action (VLA) models, existing reasoning paradigms still face a fundamental \emph{state-representation mismatch} in open-loop planning. Given only an initial observation, models must internally simulate action-conditioned state transitions, whereas text-, pixel-, and latent-space reasoning can suffer from lossy spatial compression, error-accumulating visual generation, and bypass of intermediate latent tokens, respectively, undermining reliable long-horizon planning. We propose \textbf{State-Space Visual Reasoning} (SSVR), which decouples static visual context, language constraints, and a recurrent latent state. SSVR encodes the initial image and instruction once, then conditions each action prediction on the latent state and updates it with an action-conditioned GRU. Using Qwen2.5-VL as the backbone, SSVR achieves 99.5/99.6, 96.3/98.0, and 83.9/90.6 EM/PR on FrozenLake, Maze, and MiniBehavior, substantially outperforming prior methods. Extensive experiments support the effectiveness of recurrent state modeling for VLA open-loop planning across input transformations and transfer settings. By reusing static visual-textual context and updating a compact recurrent state, SSVR supports efficient multi-step inference, achieving up to $98.58\times$ faster Maze decoding rollouts than the evaluated baselines with the prefix cache prebuilt.

---

## 13. TAO-DA: Towards Autonomous Operation--A Dual-Arm Vision-Language-Action Model for Coordinated Manipulation

**Authors:** Yongsheng Zhao, Han Gao, Baoping Cheng, ..., Lei Zhao, Ye Wang
**arXiv:** [2609.33197](https://arxiv.org/abs/2609.33197)
**Categories:** Robotics (cs.RO); Artificial Intelligence (cs.AI)

Vision-Language-Action (VLA) models provide a unified framework for grounding high-level semantic information into low-level robot actions, enabling scalable robotic manipulation across diverse tasks. However, existing VLA models lack explicit mechanisms to disentangle the states and intents of the two arms, leading to unintended cross-arm interference that degrades task execution success. To address this issue, we propose a symmetric Dual-Arm Expert (DAE) architecture built upon a shared Vision-Language Model (VLM) backbone with decoupled, arm-specific expert towers. Expert selection is carried out through a two-stage dual-arm intent routing scheme, in which experts are routed either by explicit language instructions in the first stage or by implicit visual semantics in the second stage. Moreover, we introduce a lightweight task progress prediction module that leverages cross-attention between the pre-chunk temporal features and semantic representations of proprioceptive and visual observations to accurately estimate frame-wise task completion progress. This module facilitates task progress synchronization to support coordinated scheduling for collaborative multi-robot tasks. Experimental results demonstrate the effectiveness of our model in dual-arm intent routing and the disentanglement of cross-arm interference, and further provide preliminary evidence of emergent skill generalization from single- to dual-arm tasks (as well as the reverse), together with cross-arm motion-domain skill transfer.

---

## 14. DS-VLA: A Dendritic-inspired Vision-Language-Action Model for Robust Action Control

**Authors:** Yaxing Lyu, Jingyi Li, Mingkun Xu, Yujie Wu
**arXiv:** [2609.32253](https://arxiv.org/abs/2609.32253)
**Categories:** Robotics (cs.RO); Artificial Intelligence (cs.AI); Neural and Evolutionary Computing (cs.NE)

Vision-language-action (VLA) models have achieved strong performance in language-conditioned manipulation, yet success under nominal evaluation does not necessarily translate into robust closed-loop behavior when executed actions are transiently corrupted. We introduce DS-VLA, a dendritic-inspired action architecture that incorporates dendritic spiking dynamics into VLA control to address this limitation. Specifically, to enable modularized feature processing and temporal information integration, DS-VLA equips action neurons with multiple sparsely connected dendritic branches, each featuring heterogeneous, learned decay factors. Furthermore, to suppress unreliable state updates while preserving task-relevant historical information, we introduce a neuron-wise inhibitory gate that adaptively regulates the admission of new multimodal evidence into dendritic states prior to somatic dynamics. We evaluate DS-VLA on all four LIBERO suites under both nominal rollouts and a unified closed-loop action-perturbation protocol. DS-VLA achieves a 91.6\% average nominal success rate and an 87.35\% average perturbed success rate, retaining 95.4\% of its nominal performance. Under the same reported perturbation setting, OpenVLA-OFT, FAST, $\pi_0$, and GR00T achieve 39.45\%, 23.90\%, 28.55\%, and 30.75\%, respectively. A controlled ablation isolates the contribution of neuron-wise shared inhibition, while analyses of neural dynamics and post-perturbation trajectories associate robust performance with selective evidence suppression and effective behavioral recovery. Together, these results demonstrate that integrating brain-inspired computational mechanisms offers a promising architectural prior for robust embodied intelligence beyond merely scaling vision-language backbones or generative action decoders.

---

## 15. What Stops Recursive Self-Improvement in Robotics? Lessons from 123 Rounds of Agentic Skill Discovery

**Authors:** Jiaming Wang
**arXiv:** [2609.31760](https://arxiv.org/abs/2609.31760)
**Categories:** Robotics (cs.RO); Artificial Intelligence (cs.AI); Machine Learning (cs.LG)

Can a robot improve itself the way coding agents now improve software? We built an agentic system to find out. It watches a robot fail, works out which capability is missing, writes new skills or finds and installs external models, tests every change in simulation, and repeats, with no human writing robot code. We ran it for 123 improvement rounds on household manipulation tasks. This report describes what we learned. The good news is that the agent can discover capabilities on its own: noticing that its targets were out of view, it asked for an active-viewing model, debugged it, and deployed a working search skill. The bad news is that its improvements did not add up. Changes kept passing their tests, yet the target task, putting condiments on the top shelf of a fridge, never succeeded. We found that the agent was rarely the bottleneck. Three things around it were. First, chained perception modules do not understand relations. Segmenters such as SAM 3 find shelves but not "the top shelf", so the agent filled the gap with ever more geometric rules that never converged, when what it needed was a different kind of model. Second, skill chains lock learning onto the first step. Long tasks mostly fail early, so evidence and fixes pile up there, and later skills are rarely reached, tested, or improved. Third, what the agent learns is decided by the harness. The agent optimized exactly what the evaluator measured, including where it was wrong, and weak tests and misleading memory turned activity into a standstill. We distill these lessons into concrete recommendations for building robot systems that improve themselves, each paired with an experiment that could prove it wrong.

---

## 16. Energy Vision--Language--Action: A Controlled Multimodal Benchmark for Intent-Conditioned Residential Energy Management

**Authors:** Lyes Saad Saoud, Oualid Doukhi, Ehsan Reihani, ..., Moussa Ayyash, Reza Ghorbani
**arXiv:** [2609.31648](https://arxiv.org/abs/2609.31648)
**Categories:** Machine Learning (cs.LG); Artificial Intelligence (cs.AI); Systems and Control (eess.SY)

Vision-Language-Action (VLA) models are studied mainly in robotics, where visual observations and language instructions are mapped to physical actions. This paper introduces Energy Vision-Language-Action (EVLA), a controlled multimodal benchmark for intent-conditioned residential energy management. EVLA frames battery scheduling as a multimodal trajectory-prediction problem in which an RGB energy-field representation, a numerical operating state, and a natural-language objective are mapped to a 16-step battery-action trajectory generated by a finite-horizon sampling-based reference generator. Source windows are derived from public residential electrical-load data, while electricity price, battery state of charge, indoor temperature, and time of day are generated benchmark metadata. A hidden operating regime is encoded only through energy-field texture, enabling paired visual changes while the explicit numerical state is fixed. Crossing 439,203 retained base windows with three hidden regimes and five language objectives yields 6,588,045 multimodal instances. An initial study evaluates 36 configurations over three training seeds using fixed subsets of 5,000 training, 500 validation, and 500 test instances. In the MobileNet-family comparison, removing processed language increases trajectory mean-squared error from 0.3856 +/- 0.0039 to 0.8628 +/- 0.0001, whereas removing vision yields 0.3843 +/- 0.0013, comparable to the full model. The results show strong asymmetry in modality use: the processed-language pathway is strongly associated with prediction quality, while the current RGB pathway provides no aggregate error advantage. These results characterize the fixed pilot subset and executed protocol rather than full-benchmark training. EVLA provides a controlled setting for studying how semantic intent and latent context influence residential energy-action prediction.

---

## 17. Adjoint Guidance Flow: Amortized Critic Guidance for VLA Policies

**Authors:** Jeongsol Kim, Youngjun Jun, Kyumin Choi, ..., Kwanyoung Kim, Jong Chul Ye
**arXiv:** [2609.34944](https://arxiv.org/abs/2609.34944)
**Categories:** Machine Learning (cs.LG); Computer Vision and Pattern Recognition (cs.CV); Robotics (cs.RO)

Flow-based Vision-Language-Action (VLA) policies are typically trained by behavior cloning and thus do not explicitly optimize long-term task return. Critic guidance steers generation toward higher-value actions, but existing methods differentiate the critic through a one-step surrogate of the sampler and back-propagate a critic ensemble at every flow step. In contrast, here we propose Adjoint Guidance Flow (AGF), which amortizes trajectory-aware critic guidance into a lightweight guidance network while preserving the pretrained VLA policy. Specifically, we formulate critic-guided flow generation as a deterministic optimal control problem, whose optimal guidance is a costate that carries the terminal critic gradient back through the remaining flow, and regress the guidance network onto this costate while keeping both the VLA and critic frozen. This design provides favorable memory and throughput scaling during training, and inference needs one guidance-network forward pass per step, without the critic ensemble, back-propagation, or adjoint computation. Across LIBERO, RoboCasa, and LIBERO-Pro, AGF consistently improves pretrained VLAs, remains competitive with critic-guidance and policy-fine-tuning baselines, and is the most robust method when a single guidance strength is deployed across tasks. Compared with QGF, AGF runs $3.6\times$ faster per guidance step with $7.0\times$ fewer parameters, with comparable and even better performance, showing that critic guidance can be trajectory-aware and lightweight.

---

## 18. The Low-Rank Structure of VLA Reinforcement Learning

**Authors:** Minjae Oh, Yoonah Park, Jongwon Lim, Yohan Jo
**arXiv:** [2609.34599](https://arxiv.org/abs/2609.34599)
**Categories:** Machine Learning (cs.LG)

Reinforcement learning (RL) is increasingly used to post-train vision-language-action (VLA) models, yet how RL reshapes these policies remains poorly understood. We find that RL across widely used flow-based VLA models, including $\pi_{0.5}$ and GR00T~N1.5/N1.6, on LIBERO, ManiSkill, MetaWorld, and CALVIN induces substantially lower-rank parameter updates that are highly concentrated in the action expert's Timestep Modules, a small and previously overlooked component. Through systematic module-replacement experiments, we further show that these modules capture a disproportionate share of the performance gains from RL. We then characterize what is encoded in these Timestep Modules. First, we show that RL specializes them to the discrete denoising timesteps used during rollouts, and that this discrete-timestep training underlies the low-rank updates. Second, we find that among their outputs, the shift vector changes most distinctly under RL, and through probing, we show that shift update directions strongly predict task success (ROC-AUC up to $99.6\%$). Third, we find that the geometry of shift updates reflects task relationships, as their pairwise similarity correlates with cross-task transfer patterns. Building on these findings, we show that steering along shift update directions further improves RL-trained policies without additional RL training. Overall, we provide a systematic understanding of how RL reshapes VLA policies by studying how learned signals are encoded in parameter space, offering insights into more efficient and interpretable VLA post-training.

---

## 19. Alignment-Guided Flow Transformer for Efficient Vision-Language-Action Policy Learning

**Authors:** Shengchao Hu, Peng Wang, Qiyang Zhou, ..., Ya Zhang, Dacheng Tao
**arXiv:** [2609.34467](https://arxiv.org/abs/2609.34467)
**Categories:** Machine Learning (cs.LG)

Recent advances in Vision-Language-Action (VLA) models point toward general-purpose robotic intelligence by unifying perception, instruction, and control. Despite impressive progress, existing VLA models often adapt poorly due to \emph{tri-modal misalignment} among vision, language, and action, which weakens action grounding and hurts generalization and fine-tuning efficiency. In this work, we present Alignment-Guided Flow Transformer (AGFT), a novel framework that explicitly enforces tri-modal alignment through a dedicated alignment loss, bridging the representational gap across modalities and enhancing task adaptation. While prior research has predominantly emphasized bi-modal vision--language alignment, we systematically formalize and study tri-modal alignment in VLA models, and provide both ablations and analysis to isolate its role in improving adaptation and robustness. To further accelerate deployment, we adopt a flow-matching objective, enabling substantially fewer inference steps than diffusion-based policies while maintaining accuracy. Theoretically, we establish a quantitative connection between the tri-modal alignment gap and the optimization tightness of flow matching; empirically, experiments on the extensive benchmark show that AGFT achieves superior success rates and lower inference latency compared to SOTA baselines, underscoring tri-modal alignment as a key ingredient for scaling robust VLA manipulation.

---

## 20. SAMBAR: Selective Anchoring via Method of Multipliers for Balanced Knowledge Acquisition and Retention in Vision-Language-Action Models

**Authors:** Aayushi Shrivastava, Xunlan Zhou, Hongrui Zhao, Ziyu Chen, Negar Mehr
**arXiv:** [2609.32108](https://arxiv.org/abs/2609.32108)
**Categories:** Machine Learning (cs.LG); Robotics (cs.RO)

Vision-Language-Action (VLA) models leverage large-scale pretraining to ultimately achieve generalist manipulation. Deployed VLA policies must support continual learning to acquire new tasks over time. Teaching a VLA a new task generally requires finetuning it on demonstrations of that task. However, naively finetuning on downstream tasks causes the policy to forget earlier tasks and degrades generalist capabilities. This failure is known as catastrophic forgetting. Most continual learning methods counter it by replaying data from earlier tasks. However, the old task demonstrations are not always readily available. In this paper, we introduce SAMBAR, a continual learning algorithm that prevents catastrophic forgetting during VLA finetuning without requiring access to the demonstrations of any previously learned task. We propose to cast continual learning as a constrained optimization problem and solve it with the method of multipliers. In our approach, the method of multipliers drives the policy to learn the new task without the model parameters drifting far away from their previous values. In contrast to a standard regularization penalty, the method of multipliers raises the penalty as the constraint violation accumulates by using a dual variable. We also selectively anchor the parameters critical to previous tasks to preserve past knowledge, leaving other parameters free for new task acquisition. The combination of dual variable and selective anchoring, therefore, balances knowledge acquisition with knowledge retention. We evaluate our method, SAMBAR, on the LIBERO simulation benchmark and on hardware. When sequentially finetuning on a VLA, every replay-free baseline we compare against completely forgets the first task it learned, whereas SAMBAR retains every task it has learned.

---

## 21. Natural State-Prediction Accuracy can Hide Weak Controlled Responsiveness in VLA Readouts

**Authors:** Hyungjoon Kim, Wonbin Son, Mi Young Lee, Jun Young Lee, Seungmin Rho
**arXiv:** [2609.34684](https://arxiv.org/abs/2609.34684)
**Categories:** Robotics (cs.RO); Computer Vision and Pattern Recognition (cs.CV); Machine Learning (cs.LG)

Accurately decoding object states from the internal representations of vision-language-action (VLA) models does not establish that the predictions respond faithfully to changes in the target physical state. In natural observations, object state, robot configuration, occlusion, and task progress vary together, allowing contextual cues to contribute to prediction. In this paper, we introduce an evaluation framework that separates prediction accuracy, target-state responsiveness, and context stability using physically validated observations that cross target coordinates with robot contexts. We demonstrate that high natural-trajectory accuracy can coexist with weak controlled target-state responsiveness in fixed representation-readout pairs. Comparisons and interventions involving representations, readouts, and training data show that the three properties provide distinct diagnostic information. Furthermore, adding responsiveness and context sensitivity to a failure predictor based on initial state error and physical variables reduces policy-failure prediction error on new initializations relative to the specified baseline while same-observation controlled MAE is also informative. These findings motivate evaluating target-state responsiveness and context stability alongside natural prediction accuracy, and examining their relationship to actual policy behavior and task outcomes.

---

## 22. Federated Subspace Guided Vision-Language-Action Policy Distillation for Non-IID Multi-Robot Manipulation

**Authors:** Biprodip Pal, Kaushik Roy, Yanming Zhu, ..., Alan Wee-Chung Liew, Peyman Moghadam
**arXiv:** [2609.32239](https://arxiv.org/abs/2609.32239)
**Categories:** Robotics (cs.RO); Computer Vision and Pattern Recognition (cs.CV); Distributed, Parallel, and Cluster Computing (cs.DC); Machine Learning (cs.LG)

Federated learning offers a natural way for multiple robots to jointly improve manipulation policies without requiring centralized access to training demonstrations. However, non-IID task and environment distributions can induce representation drift and mutually incompatible robot-policy updates, making naive parameter aggregation destructive. We present FedDRMan, a federated subspace-guided distillation framework for heterogeneous robot manipulation. At each communication round, the server model provides a frozen teacher for local behavior cloning, while low-rank multimodal subspace and action-distribution distillation preserve globally useful representation geometry and policy behavior. To address heterogeneous aggregation, FedDRMan groups clients by update compatibility and maintains a persistent model for each cluster. The server then spectrally rebalances each compatible aggregate to mitigate attenuation of weaker task-relevant robot-policy update directions. Extensive experiments on LIBERO across diverse non-IID settings, heterogeneity levels, client participation variation, together with ablations and aggregation analyses, show that FedDRMan substantially improves knowledge transfer and consistently outperforms strong federated baselines achieving a peak mean success rate of 80.7%, 11.6 percentage points above the strongest evaluated federated baseline.

---

## 23. GT-VLA: Target-Conditioned Trace Guidance for Generalizable Robotic Manipulation

**Authors:** Ninghan Zhong, Jing-Chen Peng, Sriram Vishwanath
**arXiv:** [2609.31904](https://arxiv.org/abs/2609.31904)
**Categories:** Robotics (cs.RO); Machine Learning (cs.LG)

Vision-Language-Action (VLA) models have shown strong performance on robotic manipulation, but they often struggle to generalize to unseen tasks, configurations, and long-horizon settings. A key challenge is that VLAs overfit to training scenes and fail to follow novel language instructions. Off-the-shelf vision-language models (VLMs) often provide stronger generalization, but cannot directly control robot actions. To combine the common sense of VLMs with VLA control, we propose Guided Trace VLA (GT-VLA), a steerable framework that accepts guidance from an external generalist VLM through trace-conditioned action generation. GT-VLA uses a generalist model to identify semantic guidance for the current skill, converts this guidance into a 2D visual trace, and conditions its action policy on the resulting trace-rendered observation. This design separates semantic target acquisition, trace generation, and low-level action execution, allowing high-level guidance to propagate to robot actions. GT-VLA uses a Mixture-of-Experts architecture with skill-specific trace and action modules for robust execution. We evaluate GT-VLA on LIBERO and a physical robot platform, showing improved generalization over recent VLA baselines in both settings. The code and additional supplemental materials are available on our project website at this https URL.

---

## 24. Humanoid Loco-Manipulation With Discrete VLA Model

**Authors:** Wenxin Shao, Siqi Chai, Kun Li, ..., Wei Xu, Qiang Liu
**arXiv:** [2609.35709](https://arxiv.org/abs/2609.35709)
**Categories:** Robotics (cs.RO)

Vision-language-action (VLA) models using discrete action tokens have proven effective for controling robotic arms on manipulation tasks. For a humanoid, however, the whole-body action space -- legs, torso, arms, and hands -- is far higher-dimensional and heterogeneous, raising tokenization, training, and real-time inference challenges that the previous VLA models do not address. We present Holo-M, to our knowledge the first discrete VLA model for humanoid loco-manipulation that intrinsically exploits the language model by extending its vocabulary with action tokens. In this model, we devise a unified action tokenizer that decomposes the humanoid action space into four body-part-specific tokenizers -- end-effector, body, hand, and kinematics -- enabling training across drastically different embodiments and data sources, including humanoid teleoperation, ego-centric human video, and simulation. By extending the language model's vocabulary with these action tokens, we avoid the knowledge-insulation problem inherent to the models that use separate continuous action experts. To meet real-time control requirements, we decode each body part's action tokens through grouped discrete diffusion decoding, rather than using autoregression on the action tokens. We have conducted extensive experiments on the SIMPLE humanoid loco-manipulation benchmark, in which Holo-M achieves the highest success rates in both the generalist and specialist evaluations, leading the second best by significant margins. We will release all the code and model weights.

---

## 25. Uni-VLaT: Whole-Body Tactile Adaptation of VLA Policies for Humanoid Loco-Manipulation

**Authors:** Zihao Wang, Shutong Liu, Siqi Zheng, ..., Yanchao Yang, Mengdi Xu
**arXiv:** [2609.35450](https://arxiv.org/abs/2609.35450)
**Categories:** Robotics (cs.RO)

Physical contact often determines how a humanoid should respond during loco-manipulation, yet vision and proprioception alone are often insufficient to characterize physical interaction, especially when the contact region is occluded. Unlike sparse force or torque measurements at predefined regions, distributed tactile sensing preserves spatially resolved contact patterns across the robot body. We therefore study how to integrate such whole-body tactile information into vision-language-action (VLA) policies for contact-rich control. Our approach, Uni-VLaT, introduces a tactile pathway whose latent state is trained not only for action generation, but also to predict future tactile, proprioceptive, and visual representations. This predictive objective builds a tactile-anchored multimodal context, encouraging a more structured understanding of the physical world. We evaluate Uni-VLaT on five real-robot tasks covering tactile-triggered locomotion, sustained physical interaction, human-robot contact, and loco-manipulation. Uni-VLaT achieves a 75% average success rate, outperforming a baseline without tactile input by 43 points and a tactile-input baseline without predictive supervision by 7 points. Across two pretrained VLA backbones, our method improves Table Sweeping by 30 points on both backbones and Back-Tap Walking by 85-90 points. Ablations further show that contextualized tactile prediction and absolute future targets are critical to performance. These results indicate that predictive tactile learning provides an effective route for extending pretrained VLA policies to whole-body physical interaction.

---

## 26. Do Not Cut When Uncertain: Rejectable and Calibrated Decision Heads for VLA Policies in Robotic Harvesting

**Authors:** Heng Zhang
**arXiv:** [2609.35039](https://arxiv.org/abs/2609.35039)
**Categories:** Robotics (cs.RO)

Vision-Language-Action (VLA) policies trained with behavior cloning or flow matching are optimized to output an action trajectory, but they cannot express "I don't know" or "I should not act." In robotic harvesting, occlusion makes single-frame decisions fundamentally ambiguous: identical pixels can correspond either to a cuttable stem or to no stem at all. Existing VLAs are forced to commit, leading to high-confidence errors with irreversible consequences. We argue that the failure mode of a VLA is determined not by backbone scale but by its output interface. We propose Rejectable and Calibrated Decision Heads (RCDH), a typed, rejectable, and calibrated output interface that can be attached to a frozen VLA backbone without retraining or new features. RCDH introduces (i) a decision schema with explicit rejection and ordered, conditional decomposition, and (ii) a calibration procedure for risk-aware abstention. We evaluate RCDH on a robotic harvesting platform with controllable leaf occlusion, comparing generative, enumerated, calibrated, and rejectable interfaces. We show that replacing only the output head restores out-of-distribution usability under occlusion while preserving in-distribution performance. We further test whether the ordering of the rejection space is critical. Our results suggest that the right to refuse, rather than a larger model, is the missing interface for reliable manipulation under uncertainty.

---

## 27. AGRO-SUVIDE: Agentic Robotics for Surgical Viscoelastic Debridement

**Authors:** Shutong Jin, Ziyang Chen, Preethi Satish, ..., Florian T. Pokorny, Ken Goldberg
**arXiv:** [2609.34823](https://arxiv.org/abs/2609.34823)
**Categories:** Robotics (cs.RO)

Augmented dexterity has the potential to reduce the fatigue experienced by surgeons during repetitive surgical tasks. In this paper, we propose the first AGentic RObotics framework for SUrgical VIscoelastic DEbridement (AGRO-SUVIDE), the repeated removal of small fragments attached to a viscoelastic substrate. Leveraging the self-improving and coding capability of agents, AGRO-SUVIDE adopts a modular framework. Specifically, the demonstration analysis module automatically identifies recurring skills from a single expert demonstration, using both visual and kinematic information. The construction module then builds each skill, either as a procedural model-based skill the agent codes against a scaffolded library or as a model-free policy-based skill. At runtime, the monitoring module composes the skills into a loop-style graph sized to the number of fragments it observes, then verifies pre- and post-conditions of each skill to decide whether to advance or retry. We evaluate AGRO-SUVIDE through 340 physical trials on the da Vinci Research Kit (dVRK). AGRO-SUVIDE achieves an average single-fragment removal success rate of 85%, completing consecutive three-fragment removal at 60% and at 95% with one human intervention. It further generalizes to unseen five-fragment scenarios with an average success rate of 80% for single-fragment removal. Project page: this https URL

---

## 28. Where Memory Belongs: Ledger, an Object Ledger for Memory-Augmented VLAs

**Authors:** Tanguy Dieudonné, Jack B. Jedlicki, Heng Yang
**arXiv:** [2609.34554](https://arxiv.org/abs/2609.34554)
**Categories:** Robotics (cs.RO)

Memory is essential for long-horizon, partially observed robotic manipulation: a robot must remember which object was placed in a drawer, whose cup it moved, or how many action cycles have elapsed. Recent vision-language-action (VLA) models embed memory directly inside the policy, but benchmarks show no single in-policy mechanism covers all spatio-temporal dimensions, trailing oracle methods by a wide margin. We argue that memory type dictates where memory should reside: short-term perceptual memory (repetition, timing, retracing) belongs inside the policy, while long-term object memory (persistent spatial state, containment, event history) belongs outside as an explicit, readable record. We present Ledger, a harness that realizes this split over a single fine-tuned $\pi_{0.5}$ policy by pairing an in-policy frame-sampling memory with an external spatio-temporal object memory, the ledger, built from a SAM3 tracker and a VLM captioner of the demonstration and read by an LLM planner that decides at step boundaries. On RoboMME, Ledger reaches the highest four-suite average among the evaluated methods, 64.3% (vs. 45.9% for the strongest prior method under identical evaluation), leading object reference (60.7% vs. 40.3%) and object permanence (86.7% vs. 56.2%) using a single set of weights. Choosing the memory source at runtime, from the instruction and the record, removes the need for a task-level router.

---

## 29. Gaze Prompts: Temporally Dense Human Attention for Vision-Language-Action Fine-Tuning

**Authors:** Yihan Zhou, Rui Yan, Mingcong Li, ..., Xueyang Guo, Yilin Mo
**arXiv:** [2609.34550](https://arxiv.org/abs/2609.34550)
**Categories:** Robotics (cs.RO)

Vision-Language-Action (VLA) fine-tuning pairs images with actions at every step, yet typically provides only a task-level language instruction, leaving moment-to-moment visual relevance implicit. We introduce \emph{eye-tracker-supervised gaze prompting}, which uses gaze recorded during VR teleoperation to provide frame-level visual guidance for VLA fine-tuning. During training, recorded gaze locations are rendered as crosshairs on the robot's head-camera images. At deployment, a lightweight predictor estimates gaze locations from recent images and the instruction, supplying the same type of visual prompt without an eye tracker or changes to the policy architecture. Instantiated with $\pi_0$, gaze prompting increases mean success from $26.3\%$ to $56.0\%$ across six real-world bimanual manipulation tasks, with gains also observed when a single policy is trained on all six tasks. We release \textsc{GazeMani}, a dataset of $1{,}200$ teleoperated trajectories with synchronized gaze.

---

## 30. RoboIRGBench: Benchmarking Implicit Referential Grounding in Vision-Language-Action Models

**Authors:** Aernaer Akelijiang, Jiannan Li, Zhineng Chen, Jingjing Chen, Bin Zhu
**arXiv:** [2609.34384](https://arxiv.org/abs/2609.34384)
**Categories:** Robotics (cs.RO); Computer Vision and Pattern Recognition (cs.CV)

Vision-Language-Action (VLA) models have shown strong capabilities in robotic manipulation, yet existing benchmarks typically assume that task-relevant information is explicitly specified in the instruction. In practice, however, humans frequently refer to objects, quantities, and relations implicitly, requiring robots to recover the intended target from linguistic and perceptual context. We study this capability as Implicit Referential Grounding (IRG) and introduce RoboIRG-Bench, a manipulation benchmark designed to systematically evaluate it. Built upon RoboMME, RoboIRG-Bench contains 40 variants derived from 11 tasks and covers four challenges, including direct, reasoning-mediated, spatial, and contextual referential grounding. As IRG often requires retaining and retrieving previously established context, we evaluate representative VLAs spanning different memory mechanisms. Our evaluation reveals a noticeable referential robustness gap. Models that perform well under explicit instructions can degrade sharply when the same task-relevant information must be recovered from context. Reasoning-mediated and spatial references are particularly challenging, while models using external VLMs show greater robustness but still exhibit significant failures. Moreover, replacing the external VLM with a stronger model does not eliminate these gaps. We further validate these findings on a Franka Research 3 robot arm, where the gap persists under real-world manipulation and manifests as both incorrect referent grounding and downstream execution failures. These results establish IRG as a distinct and underexplored capability for reliable robotic instruction following and highlight the need for VLAs that can robustly integrate language, perception, reasoning, and action.

---

## 31. FailPatch: Failure Residual Patching for Vision-Language-Action Models

**Authors:** Peng Yu, Jiacheng Wang, Ziheng Zhang, ..., Tiancai Wang, Hongbin Sun
**arXiv:** [2609.34175](https://arxiv.org/abs/2609.34175)
**Categories:** Robotics (cs.RO)

Vision-Language-Action (VLA) policies are typically adapted using successful demonstrations, which provide direct action supervision but rarely cover failure-prone states. Deployment failures expose these states, yet lack the corrective actions needed for conventional supervised learning. We propose FailPatch, a failure-driven residual patching framework that decouples action supervision from execution-reliability supervision. Successful demonstrations ground how the policy should act, while deployment trajectories indicate when its behavior becomes unreliable. We further observe that action hidden representations exhibit clear linear separability between reliable and failure-associated states while directly conditioning action generation. Building on these insights, FailPatch introduces a Null-gated Residual Expert Bank into the action hidden space of a frozen VLA policy. A unified Preserve--Redirect--Trust objective retains the original policy in reliable states, selects residual experts in failure-associated states and redirects representations from failure regions toward success-associated regions under bounded intervention. With only 0.52% trainable parameters, FailPatch improves success rates by 11.0 percentage points on four long-horizon RoboTwin tasks under clean evaluation, 9.5 percentage points under clean-to-random generalization, and 16.7 percentage points over the baseline across three real-world tasks. Project and code: this https URL.

---

## 32. RAVEL: Asynchronous Rolling Inference for Flow-Based Vision-Language-Action Models

**Authors:** Yuhan Chen, Ke Yu, Pengfei Liu, ..., Yi Yang, Linchao Zhu
**arXiv:** [2609.34170](https://arxiv.org/abs/2609.34170)
**Categories:** Robotics (cs.RO)

Flow-based vision-language-action (VLA) models are highly effective for generalist robot manipulation, yet their reliance on computationally expensive VLM encoding and multi-step iterative action generation imposes a significant latency bottleneck. The resulting inference latency makes it difficult for robots to respond quickly, especially in dynamic environments. We address this limitation with RAVEL (Rolling Asynchronous VLA Enabling Low-Latency Control), an asynchronous inference framework that addresses the computational bottlenecks of both the VLM backbone and the action expert. To reduce the delay from multi-step action denoising, RAVEL allows near-term actions to be executed after a single denoising step by carrying partially denoised future actions forward in a rolling buffer. To avoid blocking on slow VLM encoding, RAVEL decouples VLM encoding from rolling action generation, allowing the action expert to operate continuously using the latest available VLM context, while a lightweight Fast Observation Pathway (FOP) directly conditions the action expert on current observations. Across simulated and real-world manipulation tasks, RAVEL consistently achieves substantially lower response latency while maintaining the task capability of the underlying VLA, enabling high-frequency and responsive closed-loop control.

---

## 33. Quantile Head for Vision-Language-Action Models

**Authors:** Xuan Wang, Yinan Wu, Haoran Duan, Jungong Han
**arXiv:** [2609.34061](https://arxiv.org/abs/2609.34061)
**Categories:** Robotics (cs.RO); Computer Vision and Pattern Recognition (cs.CV)

Vision-Language-Action (VLA) models integrate pretrained Vision-Language Models (VLMs) with action heads for robot control. Common action heads have distinct limitations: point regression provides only a point estimate of the action distribution, while standard flow-matching samplers require costly iterative sampling. To address these limitations, we unify regression and flow matching under a shared objective and extend it to derive a quantile objective. This quantile objective guides the design of our Quantile Head, which predicts a median and positive gaps to form ordered marginal action quantiles in one forward pass. These quantiles support multiple sampling strategies without retraining and are jointly supervised to train the default median policy. Our local analysis of this joint supervision shows that, with calibrated nearby quantiles, fixed gaps, and matched correction speed, direct median updates have lower variance than under median-only supervision. Experiments show that this jointly supervised median policy achieves the highest average success rates among the compared methods on LIBERO, LIBERO-Plus, LIBERO-Pro, and two real-robot tasks, together with the shortest mean episode time among matched LIBERO baselines; code is available at this https URL.

---

## 34. InfraVLA: Extending Vision-Language-Action Navigation with Infrastructure Cameras

**Authors:** Lukas Vierling, Benjamin Ramtoula, Luke Robinson, Ronald Clark, Daniele De Martini
**arXiv:** [2609.33647](https://arxiv.org/abs/2609.33647)
**Categories:** Robotics (cs.RO)

Many indoor environments in which robots operate, such as warehouses, offices, and hospitals, already have cameras installed. They observe parts of the building that the robot cannot see from where it stands, yet navigation policies, including recent vision-language-action (VLA) models, do not use them. We propose InfraVLA, an end-to-end method that adapts a pretrained navigation VLA to such static infrastructure views: a closed-circuit television (CCTV) encoder turns each external view into tokens of the input sequence. Because the views matter only at rare decision points, fine-tuning alone did not make the policy use them in our experiments; we therefore train in two stages, on demonstrations with upsampled counterfactual data and then on recovery data. We evaluate on two simulated warehouse tasks, finding an object named in the instruction and rerouting around blocked aisles, where the deciding information is often visible only to the infrastructure cameras. Tested in distribution, InfraVLA reached a success rate of 100% on both, against 34.0% and 73.6% for a baseline without CCTV input. On out-of-distribution test sets it reached 88.2% and 88.9%. On a real quadruped fine-tuned with under 10 minutes of demonstrations, the policy reached 83.3% against 29.2% for the on-board-only baseline.

---

## 35. SLIP-VLA: Single-Step Latent Imagination for Policy Learning in Vision-Language-Action Models

**Authors:** Tianfu Li, Haoxuan Xu, Wenbo Chen, ..., Lujia Wang, Haoang Li
**arXiv:** [2609.33575](https://arxiv.org/abs/2609.33575)
**Categories:** Robotics (cs.RO)

Vision-Language-Action models are increasingly effective for robotic manipulation, yet most predict actions directly from current observations without explicitly modeling future scene evolution. Recent methods introduce future prediction to improve action generation, but dense future modeling often requires expensive iterative denoising, while one-step alternatives can underperform their multi-step counterparts. To reconcile efficient future modeling with strong action performance, we present SLIP-VLA, a policy learning framework that equips VLA models with a Single-Step Latent Imagination for future-aware action prediction. SLIP-VLA obtains temporally dense future latent representations with a single denoising update, and we improve the perceptual sufficiency of these representations by aligning intermediate latents with future geometric and semantic features. We further improve their control sufficiency through action-conditioned latent world modeling and inverse dynamics modeling, explicitly coupling latent transitions with robot actions. SLIP-VLA achieves state-of-the-art performance across diverse simulation benchmarks and real-world manipulation tasks, while its single-step latent imagination takes only 12 ms.

---

## 36. ActionGround: Training-Free Runtime Refinement of Frozen VLA Policies

**Authors:** Namai Chandra, Madhur Thareja, Shriram Damodaran, Addison Lin Wang
**arXiv:** [2609.33256](https://arxiv.org/abs/2609.33256)
**Categories:** Robotics (cs.RO)

Vision-Language-Action (VLA) models map visual observations and language instructions directly to robot actions, but they do not explicitly represent the phase structure of manipulation tasks or the rigid-body dynamics governing execution. We present ActionGround, a neuro-symbolic, training-free runtime layer that wraps a frozen VLA policy without retraining, fine-tuning, or weight access, adding less than 1 ms of overhead per control step. A symbolic phase-aware finite-state machine identifies the manipulation phase (approach, grasp, transport, or place) and applies a phase-specific rule-based correction. In parallel, an always-on, inertia-weighted Euler-Lagrange term incorporates the robot's equations of motion into each control step, while its dynamics residual is logged as a consistency diagnostic rather than used as a gate.
We evaluate ActionGround across OpenVLA, OpenVLA-OFT, Force-VLA, and Generalist-VLA on ten LIBERO-Spatial pick-and-place tasks using a 7-DoF Franka Panda. With fixed parameters across tasks and backbones, ActionGround improves success rate by up to 6 percentage points and stability by up to 19.3 percentage points, while improving trajectory efficiency by up to 15%. In a separate Robosuite noise sweep, ActionGround provides approximately a 10x improvement in trajectory-jerk robustness under injected action noise. In a matched-seed Robosuite simulation companion to a real Agilex Piper trial, simulated baseline success increases from 35% to 95%. The physical-hardware experiment is presented as a qualitative deployment demonstration; quantitative per-trial success on the real arm is left for future work. Our evaluation is limited to rigid-object pick-and-place manipulation.

---

## 37. TimelyDAgger: Timing-Aware Expert Querying for VLA Policy Improvement

**Authors:** Zhixuan Zhao, Peiyan Li, Enhao Zhang, ..., Yu Luo, Huaping Liu
**arXiv:** [2609.33157](https://arxiv.org/abs/2609.33157)
**Categories:** Robotics (cs.RO)

DAgger improves robot policies by aggregating expert supervision from states visited during policy execution. Robot-gated DAgger automates expert queries, allowing the robot to decide when to request expert takeover. While existing gates emphasize detecting the need for assistance, takeover timing also shapes the content of these demonstrations and their value for policy learning. We propose TimelyDAgger, combining Bridge-PCA monitoring of internal vision-language-action (VLA) features with Feedback-guided Threshold Adaptation based on expert behavior to improve takeover timing. We introduce an evaluation framework linking failure detection, takeover timing, and policy improvement, including Target-Aligned Supervision Ratio (TASR) for assessing supervision quality without retraining. Experiments show that takeover timing affects policy learning, with TimelyDAgger achieving competitive failure detection and higher post-training success in most evaluated settings under matched expert-action budgets.

---

## 38. SEES: A Self-Evolving Embodied System via Failure-Guided VLA Policy Adaptation

**Authors:** Ziwen Li, Hanlue Zhang, Zhenyang Ren, ..., Chris Russell, Mingming Gong
**arXiv:** [2609.32698](https://arxiv.org/abs/2609.32698)
**Categories:** Robotics (cs.RO)

Recent vision-language-action (VLA) policies demonstrate promising generalization across diverse short-horizon tasks. However, they remain unreliable on long-horizon tasks, partly because the large-scale training data is biased toward single-stage manipulation tasks that are cheaper to demonstrate. A single weak atomic skill can cause failures across multiple multi-stage tasks. To address such failures, existing methods often require experts to identify the bottleneck and provide additional demonstrations, making the improvement costly and potentially impractical after deployment. To this end, we present a Self-Evolving Embodied System (SEES) that learns from failures and improves the VLA policy without additional expert demonstrations. SEES decomposes long-horizon tasks into atomic tasks and routes them to corresponding family policies. Each family consists of related atomic skills that share one VLA adapter. During execution, the system automatically monitors atomic-task outcomes to identify the most frequently failing atomic skills as the current bottlenecks. To overcome these bottlenecks, SEES constructs tailored RL tasks in simulation by restoring previously encountered states and generating task-specific success criteria with an LLM. Online RL updates the shared family adapters to promote positive transfer among related atomic skills and cumulative improvement across evolution rounds. Extensive experiments show that SEES can be integrated with different VLA backbones to progressively improve their long-horizon performance. We also observe continued improvement on unseen tasks, providing evidence of transfer beyond the evolution settings.

---

## 39. PF-RL: Progress Field Reinforcement Learning via Goal-Conditioned Value Geometry for Vision-Language-Action Models

**Authors:** Yunpeng Qing, Yilun Kong, Sixu Lin, ..., Zhi Hou, Changqing Zou
**arXiv:** [2609.32634](https://arxiv.org/abs/2609.32634)
**Categories:** Robotics (cs.RO)

Reinforcement Fine-Tuning~(RFT) has emerged as a promising paradigm for improving Vision-Language-Action~(VLA) policies, yet sparse task-level outcomes provide limited credit for intermediate transitions, especially in long-horizon manipulation. A natural approach is to model intermediate task progress and use it as dense feedback for policy improvement. Despite their architectural differences, existing progress-aware methods commonly formulate task progress as an explicit scalar prediction, providing limited structure for modeling how intermediate observations relate to the task goal, which may hinder effective transition-level credit assignment. We introduce Progress Field Reinforcement Learning (PF-RL), which learns a structured goal-conditioned progress representation over pretrained VLA features and converts it into dense credit for policy optimization. A lightweight shared Progress Field head maps current and goal representations into a compact progress space, where geometric distance induces goal-conditioned value, while complementary temporal and goal-structure objectives shape the learned geometry. Transition-level value changes naturally yield dense progress advantages, enabling fine-grained credit assignment for both offline policy improvement and online reinforcement fine-tuning. Extensive experiments on LIBERO, RoboTwin2.0, and real-world bimanual manipulation tasks show that PF-RL consistently improves policy performance over strong supervised fine-tuning, reinforcement fine-tuning, and progress-aware baselines.

---

## 40. RecastVLA: From Past Interaction to Future Control with Adaptive Policy States

**Authors:** Wenbo Li, Jun Yang, Yiteng Chen, Wei Zhang, Qingyao Wu
**arXiv:** [2609.32155](https://arxiv.org/abs/2609.32155)
**Categories:** Robotics (cs.RO)

Sequential manipulation requires a robot to track what has already happened, even when the current scene no longer reveals it. Policies with explicit history representations make past interactions available as context for current decisions. We ask how action generation itself can form a persistent state for subsequent control. Building on action-side test-time training, RecastVLA maintains an adaptive policy state within a flow-matching vision-language-action policy. The state is represented by shared fast weights and remains fixed throughout action generation. Depth-specific interfaces read the same state, while features across depths and flow evaluations jointly define one update for the next policy call. Subsequent action losses train the initialization, interfaces, and update rule by differentiating through earlier state transitions. At deployment, updates use the policy's own action-generation features without expert action labels. Across LIBERO, RoboTwin, RoboDojo, and twelve real-robot tasks, RecastVLA improves mean success over a matched policy trained without test-time training, including 10.68 percentage points on RoboTwin Clean-to-Clean. In controlled RoboTwin comparisons, retaining state improves success, and the shared design exceeds independently trained layer-local TTT by 2.58 points.

---

## 41. Find Something You Can't Do: Agentic Real-World Reinforcement Learning for Self-Improving VLA Models

**Authors:** Yuan Fang, Zechu Li, Haolei Tong, Puze Liu, Georgia Chalvatzaki
**arXiv:** [2609.32069](https://arxiv.org/abs/2609.32069)
**Categories:** Robotics (cs.RO)

Vision--language--action (VLA) models provide strong priors for robotic manipulation but are typically deployed as frozen policies, unable to improve from their own failures. Real-world reinforcement learning (RL) offers a path to continued improvement, yet manual environment resets and task-success supervision hinder autonomous learning. We introduce \textbf{FIND}, an agentic real-world RL framework that closes the loop between scene understanding, weakness-aware practice, self-evaluation, and policy improvement in a persistent workspace. FIND reframes autonomous practice as a scene-conditioned, performance-aware task-selection problem: instead of restoring a predefined scene after each rollout, it uses the resulting scene to determine what to practice next. A vision--language agent identifies feasible tasks from a predefined library, prioritizes those with lower recent success rates, and evaluates outcomes using paired pre- and post-execution observations. We instantiate FIND with a frozen $\pi_{0.5}$ VLA and residual off-policy RL. Across eight real-world manipulation tasks, the independent human-assessed success rate improves from $55\%$ to $71.9\%$. A representative run completes 456 autonomous episodes within 6 hours of interaction, requiring 30 scene-recovery interventions and no human-provided reward labels during online learning. Ablations and systematic evaluations further examine key design choices, agent evaluation accuracy, and human intervention requirements. Our website is made publicly available at: this http URL.

---

## 42. ActionUNet: Improving Robustness of VLA Models with Efficient Multi-scale Fine-tuning

**Authors:** Di Zhu, Ziheng Yan, Fang Wan
**arXiv:** [2609.34982](https://arxiv.org/abs/2609.34982)
**Categories:** Computer Vision and Pattern Recognition (cs.CV); Robotics (cs.RO)

Vision-Language-Action (VLA) models have shown great promise for robotic manipulation by mapping multi-modal semantics to physical actions. However, this mapping inherently struggles to align these coarse-grained semantics with fine-grained temporal execution. It leaves VLA models with limited generalization and insufficient robustness in cluttered environments. To overcome this issue, we propose ActionUNet, an efficient multi-scale fine-tuning framework that enhances pre-trained VLA models with minimal computational cost. ActionUNet first constructs a lightweight temporal U-Net within the temporal-aligned action feature space to fuse hierarchical structural priors, effectively bridging the scale gap between semantics and temporal executions. Recognizing that multi-scale modeling can disrupt microscopic temporal continuity and cause mechanical oscillations, ActionUNet then employs a conditional SIREN as a continuous action decoder. Equipped with explicit second-order smoothness constraints, this decoder guarantees temporal continuity and reduces high-frequency motion jitter. By smoothing temporal discontinuities from multi-scale fusion, this continuous formulation reduces mechanical execution failures while preserving the base VLA model's generalization and manipulation robustness. Extensive experiments on RoboTwin 2.0 and LIBERO-Plus benchmarks, together with real-world hard evaluations, demonstrate that ActionUNet significantly improves {\pi}0.5 success rates by absolute 9.8%, 6.1%, and 11.4%, respectively, while also generalizing to the regression-based OpenVLA-OFT backbone, highlighting its effectiveness and efficiency as a fine-tuning strategy. Code and implementation details are available at this https URL.

---

## 43. Text-Vision Synergistic Token Caching: A Training-Free Framework for Efficient Vision-Language-Action Inference

**Authors:** Qianer Li, Chengjie Zhang, Jingwen Chen, ..., Jiyuan Zhang, Hong Zhang
**arXiv:** [2609.34319](https://arxiv.org/abs/2609.34319)
**Categories:** Computer Vision and Pattern Recognition (cs.CV); Robotics (cs.RO)

Vision-Language-Action (VLA) models enable generalizable robotic control but remain computationally expensive. Token caching provides a training-free, plug-and-play acceleration alternative. However, existing VLA caching does not fully exploit a key inductive bias of VLA models: text-vision synergy, wherein textual semantics guide the precise visual grounding of task-relevant regions. In particular, existing designs insufficiently account for head-wise reliability in attention aggregation and layer-wise stability in cache reuse. To address this, we propose Text-Vision Synergistic Token Caching (TVCache), a training-free framework for efficient VLA inference. TVCache filters attention heads based on text-vision information focus to improve task-relevant and physically consistent visual grounding. Concurrently, we introduce a reuse-layer selection mechanism guided by text-vision entropy differences to avoid caching unstable representations and improve cache resource allocation. Extensive experiments across four representative VLA models, two simulation benchmarks, and real-world robotic tasks demonstrate the effectiveness and generality of TVCache. At matched token-retention ratios, TVCache consistently improves task success over existing VLA caching with comparable computational cost. On OpenVLA-OFT, it improves average success by up to 14.5 percentage points over VLA-Cache at 12.5% retention while reducing FLOPs by 2.45x relative to full-token inference.

---

## 44. Train Together or Merge Later? Unifying VLA Experts via a Shared Action Interface

**Authors:** Zhizhen Zhang, Yuxia Fu, Zijian Wang, Helen Huang, Yadan Luo
**arXiv:** [2609.33125](https://arxiv.org/abs/2609.33125)
**Categories:** Computer Vision and Pattern Recognition (cs.CV); Robotics (cs.RO)

Co-training offers a straightforward way to build a multi-task vision-language-action (VLA) policy, but can fall short of the performance achieved by training each task independently. The challenge is to retain these task-specific gains in a multi-task policy without joint post-training. Combining independently trained experts through model merging is a natural approach, yet strong individual experts do not necessarily yield a strong merged policy. We identify one source of this incompatibility: task-specific changes to the action interface, comprising action normalization and the action encoder and decoder. We propose PolicyWeave, combining merge-compatible post-training with context-guided sparse merging. During post-training, all experts retain the common base policy's action interface, while task adaptation is restricted to LoRA updates in the hidden layers of the action model. This makes the experts more compatible with existing model merging methods. However, merging all experts can still introduce interference from unrelated tasks at deployment. PolicyWeave scores each expert's LoRA updates using the initial visual-language context, determines the expert set through leave-one-layer-out ranking stability, and forms a sparse weighted merge of the selected updates that remains fixed for current task. We evaluate PolicyWeave with GR00T N1.5 on 18 RoboCasa365 tasks, using only 10% of the target-task demonstrations for supervised fine-tuning (SFT). Preserving the shared action interface raises the average success rate across four static merging methods from 17.0% to 52.8%. PolicyWeave achieves 64.7% success with these SFT experts and 74.1% after task-specific reinforcement learning (RL), compared with 60.7% for joint RL. Further evaluations on LIBERO-10 and an AgileX Piper arm support the deployment of independently learned skills in long-horizon and real-world manipulation.

---

## 45. CausalDriveBench: Evaluating Causal Reasoning in Vision-Language-Action Models for Autonomous Driving

**Authors:** Narendiran Chembu, Navvrat Rao, Shreedhar Shreeshail Kodate, ..., Kaustubh Beedkar, Arjun Jain
**arXiv:** [2609.32157](https://arxiv.org/abs/2609.32157)
**Categories:** Computer Vision and Pattern Recognition (cs.CV); Robotics (cs.RO)

Vision-Language-Action (VLA) models for autonomous driving produce natural-language reasoning alongside predicted trajectories, but whether this reasoning reflects the causal structure of the scene remains untested. We introduce CausalDriveBench, an evaluation framework grounded in Pearl's Causal Hierarchy (PCH) that tests causal reasoning in driving-specific VLAs through structured visual question answering (QA) and alternative-trajectory prediction. To this end, we construct causal scene graphs over nuScenes that distinguish causally active, dormant, and distractor entities, separating perceptual salience from causal relevance. The benchmark spans all four rungs of PCH (association, intervention, and counterfactual along with causal discovery) for QA generation. For the higher rungs, we additionally provide reference trajectories under specified scene modifications, enabling action-level verification that complements reasoning-level evaluation. In total, the benchmark contains 7,285 verified causal QA pairs and 1,000 counterfactual trajectories derived from nuScenes. We evaluate 10 driving-specific VLAs and 3 general-purpose VLMs, and report three findings. First, the best model reaches only 70.6% QA accuracy, and 4 of 13 models score below random chance. Second, comparing each driving VLA to the general-purpose VLM that shares its language backbone, the cost of driving fine-tuning ranges from 2 to 34 percentage points on causal QA, with post-training design explaining the spread. Third, causal QA and trajectory accuracy are statistically uncorrelated across models: under counterfactual prompts, predicted trajectories either over-react or collapse onto the observed-scene baseline. Taken together, these results show that neither fluent rationales nor accurate observed-scene trajectories constitute evidence of causal understanding.

---

## 46. PanoFuse: Panorama-Enhanced Vision-Language-Action Learning with Decoupled Semantic-Geometric Routing

**Authors:** Peng Xu, Haoran Lin, Wanjun Jia, ..., Zhiyong Li, Kailun Yang
**arXiv:** [2609.31717](https://arxiv.org/abs/2609.31717)
**Categories:** Computer Vision and Pattern Recognition (cs.CV); Robotics (cs.RO); Image and Video Processing (eess.IV)

Vision-Language-Action (VLA) policies have shown promising performance in language-conditioned robotic manipulation. However, most existing VLA systems rely on conventional perspective cameras with limited fields of view, often missing global scene context and leading to unreliable manipulation under visual occlusions, distractors, and unseen environments. In this work, we propose PanoFuse, a panorama-enhanced VLA framework that complements local manipulation observations with global panoramic perception. PanoFuse introduces a dedicated panoramic branch that leverages a pretrained panoramic foundation model to extract complementary semantic and geometric representations from omnidirectional observations. Rather than directly mixing these heterogeneous features, we introduce Decoupled Semantic-Geometric Routing (DSGR), which maintains semantic and geometric representations as separate context streams and selectively routes both to downstream state and action representations through structured block-wise attention. This design provides the action expert with global spatial context while preserving task-relevant semantic information from the pretrained VLA backbone. We further develop a synchronized data collection pipeline and construct a new real-world manipulation dataset containing panoramic RGB observations, wrist-view images, language instructions, robot states, and actions. Across seven evaluation settings, PanoFuse achieves an average success rate of 52.9%, outperforming the evaluated baselines and achieving consistent gains under novel-object, unseen-background, and distractor-rich settings. Code and data will be released publicly at this https URL.

---

## 47. RefineDrive: Reliable Failure-Guided Learning for Vision-Language-Action Driving

**Authors:** Zhe Sun, Ziyi Luo, Yehao Lu, Lei Zhou, Xi Li
**arXiv:** [2609.35078](https://arxiv.org/abs/2609.35078)
**Categories:** Computer Vision and Pattern Recognition (cs.CV)

Vision-Language-Action (VLA) models for autonomous driving rely heavily on successful expert demonstrations, leaving model-specific failures underexploited. Learning from these failures is hindered by unreliable diagnoses, poorly matched correction targets, and coarse rewards. We propose RefineDrive, a failure-guided post-training framework that learns from self-generated failures through targeted supervision and safety-aware reinforcement learning. Reliable Diagnosis derives structured, verifiable feedback on collisions and drivable-area violations directly from simulator states. Minimum-Correction Target Retrieval searches a clustered human trajectory bank for nearby corrections that satisfy hard-safety constraints in the current scene, prioritizing preservation of the failed prediction's motion pattern. Conditioned on the driving context and failed trajectory, Correction SFT learns to generate the diagnosis followed by the retrieved correction as a training-only auxiliary task. We then apply GRPO with a Safety-Layered Reward that strictly prioritizes hard-safe trajectories, retains continuous safety feedback for both unsafe and hard-safe trajectories, and rewards driving progress only after hard safety is satisfied. At inference, the policy directly predicts trajectories from the driving context without an explicit diagnosis or repair stage. On NAVSIM v1, RefineDrive improves the 4B base SFT policy from 87.7 to 91.7 PDMS. Using the same checkpoint without additional training, RefineDrive achieves 89.4 EPDMS on the original NAVTEST scenes evaluated with NAVSIM v2 extended metrics. Controlled ablations support the benefits of structured diagnosis supervision, retrieved corrections, and safety-layered optimization for direct planning.

---

## 48. D$^2$-VLA: Dual-Memory Dual-Frequency Vision-Language-Action Model For Long Dynamic Manipulation

**Authors:** Zijian Ye, Chengqi Wei, Wei Huang, ..., Zhongrui Wang, Xiaojuan Qi
**arXiv:** [2609.34792](https://arxiv.org/abs/2609.34792)
**Categories:** Computer Vision and Pattern Recognition (cs.CV)

Long-horizon manipulation requires robots to remember cues that are no longer in view while responding to moving objects. Yet vision-language-action (VLA) policies often rely on the latest observation, and refreshing their visual context typically requires another costly vision-language model (VLM) pass. We present D$^2$-VLA, which combines dual memory and dual-frequency control at the KV-cache interface of a pretrained VLA. D$^2$-VLA uses block-wise causal KV caching to encode observations incrementally and, guided by distinct temporal attention patterns, constructs separate historical KV read views for the VLM and action expert. Between periodic VLM updates, a gated adapter incorporates fresh visual features into the latest history-conditioned KV block, while a short fast-memory queue supports action replanning. We introduce DOMINO-Long, a ten-task benchmark requiring robots to use earlier visual cues when manipulating moving objects. D$^2$-VLA achieves complete-task success rates of 29.3\% on DOMINO, compared with 9.6\% for $\pi_{0.5}$ and 17.2\% for PUMA, and 60.0\% on DOMINO-Long, compared with 35.4\% and 20.6\%, respectively. It improves success rates on eight real-robot tasks and reaches 97.5\% on LIBERO-Long and 74.3\% on RoboTwin 2.0.

---

## 49. Unified Trajectory Matching Policy Optimization: Diverse T2I Generation and VLA Generalization

**Authors:** Zhiyuan Ma, Jiaming Li, Lingzhen Li, ..., Bowen Zhou, Xiang Bai
**arXiv:** [2609.34688](https://arxiv.org/abs/2609.34688)
**Categories:** Computer Vision and Pattern Recognition (cs.CV)

Reward-maximizing reinforcement learning (RL) is widely used to post-train stochastic diffusion and flow policies for text-to-image (T2I) generation. However, reward-maximizing RL causes policy mode collapse even under reference KL or entropy regularization, reducing the policy to a single high-reward mode. In T2I, this produces similar images and reward hacking. When extended to vision-language-action (VLA) models, the same collapse removes alternative successful strategies and weakens task and scene generalization. To address this limitation, we introduce Unified Trajectory Matching Policy Optimization (Uni-TMPO), a unified RL post-training framework for diffusion and flow policies. First, Uni-TMPO converts standardized rewards into a target distribution within each trajectory group and derives the policy distribution from trajectory log probabilities. Then, forward Kullback-Leibler optimization matches the two distributions instead of maximizing expected reward. A progress-conditioned coarse-to-fine scheduler efficiently constructs T2I trajectories. Within the unified framework, feedback-conditioned sampling uses updated observations to construct VLA trajectories. Extensive experiments show that Uni-TMPO achieves higher T2I rewards and VLA ID success rates than the strongest baselines. More importantly, it achieves the best T2I reward-diversity-efficiency trade-off and VLA generalization to held-out tasks and scenes, while real-robot evaluation demonstrates the value of multiple action strategies when the higher-reward target is blocked.

---

## 50. CAR-VLA: Complexity-Aware and Risk-Adaptive Reasoning for Autonomous Driving

**Authors:** Xiaolei Chen, Zhuolin He, Yuxuan Liang, ..., Bin Li, Xiangyang Xue
**arXiv:** [2609.34387](https://arxiv.org/abs/2609.34387)
**Categories:** Computer Vision and Pattern Recognition (cs.CV)

Existing adaptive reasoning methods for driving Vision-Language-Action (VLA) models primarily focus on whether to reason, overlooking how reasoning should differ across driving situations. Our key insight is that while scene complexity informs reasoning depth, dynamic risk is equally critical for deciding how to reason in time-critical situations. We therefore propose CAR-VLA, a unified driving VLA model that jointly considers scene complexity and dynamic risk to guide reasoning depth, urgency, and focus. CAR-VLA maps four complexity--risk categories to three reasoning modes: \textit{Fast Intuition} for direct trajectory generation in simple low-risk scenes, \textit{Slow Thinking} for deliberate reasoning in complex low-risk scenes, and \textit{Reflex Response} for compact, hazard-focused reasoning in high-risk scenes regardless of complexity. Rather than merely shortening deliberation, Reflex Response centers reasoning on the most critical hazard and the immediate safe response. We train CAR-VLA through progressive supervised learning that links scene assessment, reasoning-mode selection, and trajectory generation, followed by reasoning-augmented reinforcement learning to improve driving quality and reasoning behavior. Experiments on NAVSIM v1(91.1 PDMS), NAVSIM v2(90.3 EPDMS), and Navhard(35.0 EPDMS) demonstrate competitive driving performance. Qualitative comparisons on navtest and in-house high-risk scenarios further illustrate risk-aware reasoning and hazard-responsive trajectory generation. The code for this paper will be released publicly at: this https URL

---

## 51. WorldGuide: Learning Success-Failure Boundaries in Latent World Models for Vision-Language-Action Policies

**Authors:** Lin Liu, Lu Zhang, Ziying Song, ..., Wulong Liu, Huchuan Lu
**arXiv:** [2609.34206](https://arxiv.org/abs/2609.34206)
**Categories:** Computer Vision and Pattern Recognition (cs.CV)

Latent world models offer a promising way to improve Vision-Language-Action policies by capturing the consequences of actions. However, models trained primarily on expert demonstrations have limited exposure to failure outcomes and may struggle to distinguish visually similar successful and failed interactions. We propose \textbf{WorldGuide}, a framework that learns these distinctions in latent space and uses them to guide policy training. WorldGuide combines predictive pretraining on successful and failed trajectories with contrastive learning on matched success--failure pairs. The learned predictor then provides a differentiable reward to guide joint optimization of the policy and visual encoder. The predictor is discarded after training, so deployment requires no additional world-model inference. Extensive experiments show that WorldGuide substantially improves VLA reliability and achieves state of the art performance on LIBERO 100 and SimplerEnv, reaching \textbf{96.8\%} and \textbf{72.0\%}, respectively. Code will be publicly available.

---

## 52. ReVision3D: Attribution-Guided Recursive Self-Improvement for 3D Medical Perception

**Authors:** Ho Hin Lee, Yuyin Zhou, Yannan Yu, Shi Gu, Yifan Wu
**arXiv:** [2609.32984](https://arxiv.org/abs/2609.32984)
**Categories:** Computer Vision and Pattern Recognition (cs.CV)

Recursive self-improvement (RSI) offers a promising path for overcoming the limited visual capability of current medical imaging agents. Yet applying RSI to volumetric imaging remains difficult: failures can arise from acquisition, perception, training recipe, or downstream inference, while self-generated feedback and logged trajectories provide little guidance on which component should change. We introduce ReVision3D, an RSI system that leverages 3D volumes with spatially grounded annotations to determine where visual evidence is lost and recursively improve the corresponding visual capability. A frozen language-model designer proposes revisions to acquisition, perception, training, or inference, while the verifier and system-level objective remain fixed. Our key insight is that an annotated volume forms an exact replay world for view rendering and spatial verification: unvisited views can be rendered on demand, and localized predictions can be checked directly against reference masks. This grounded feedback directs targeted revision, while only changes that improve beyond measured seed noise are retained. Each accepted change triggers renewed attribution, allowing the dominant bottleneck to shift across rounds. On abdominal CT, attribution identifies perception as the dominant remaining limitation. Revising that level enables ReVision3D to achieve 79% liver recall and 83% kidney recall at under 0.4 false positives per patient, outperforming the evaluated frozen multimodal foundation models, with the largest gains on small lesions.

---

## 53. RCVLA: 4D Radar-Grounded Semantic Reasoning and Trajectory Arbitration for Autonomous Driving

**Authors:** Lianqing Zheng, Xiaokai Bai, Yixuan Luo, ..., Xichan Zhu, Zhixiong Ma
**arXiv:** [2609.32681](https://arxiv.org/abs/2609.32681)
**Categories:** Computer Vision and Pattern Recognition (cs.CV)

4D radar provides geometric and motion cues that complement visual semantics, but integrating it into vision-language-action (VLA) models requires both radar--language alignment for semantic reasoning and explicit use of radar measurements for trajectory refinement and selection. To support these capabilities, we construct Cap4DR with 86,016 radar-image-text samples for alignment pretraining and OmniHD-QA with 520,161 question-answer pairs for instruction tuning across scene description, key-object reasoning, occupancy understanding, and trajectory planning. Building on these datasets, we propose RCVLA, a radar-camera VLA framework consisting of a radar-grounded semantic reasoning stage (RCVLA-Sem) and a trajectory arbitration stage (RCVLA-Phys). RCVLA-Sem performs gated bidirectional interaction between camera and radar tokens for driving question answering and reference trajectory generation, while auxiliary heads provide object and occupancy queries. RCVLA-Phys refines reference-guided trajectory candidates through truncated diffusion conditioned on these queries and cluster-level radar measurements, then calibrates candidate scores using radar-derived time-to-collision risk. On OmniHD-QA, RCVLA-Sem improves CIDEr by 9.92 points and reduces key-object velocity error by $21.9\%$ relative to OmniDrive. RCVLA-Phys further reduces average L2 error from $0.348$ to $0.259\,\mathrm{m}$ and average open-loop collision rate from $0.576\%$ to $0.175\%$ relative to RCVLA-Sem. Ablation studies further show that language-aligned radar tokens improve semantic reasoning, while cluster-level radar measurements and risk calibration improve trajectory arbitration. Code will be released.

---

## 54. Devol-ONE: One Autoregressive Mixture of Transformers to Unify Vision-Language-Action and Latent World Modeling

**Authors:** Hongyi Cai, Yi Herng Ong, Tingshiuan C. Wu, ..., Kehong Guo, Sze Yuan Cheong
**arXiv:** [2609.32193](https://arxiv.org/abs/2609.32193)
**Categories:** Computer Vision and Pattern Recognition (cs.CV)

Vision Language Action (VLA) models condition actions directly on current visual and language context, without an explicit account of how the scene evolves under candidate actions. World Action Models (WAM) attempt to address this limitation by predicting future states, but existing designs keep prediction and policy learning architecturally separate, connecting them only through the predicted output, whether through pixel space video generation or a latent forecasting module trained independently of the policy. We present Devol-ONE, a Mixture of Transformers architecture that unifies vision language understanding, latent world dynamics prediction, and action generation within a single autoregressive framework. Instead of encoding vision language tokens once and feeding them to the action expert, Devol-ONE runs autoregressive prediction jointly across a vision language stream and a V-JEPA pretrained dynamics stream, attending to the vision language key-value cache at every layer to forecast future latent states under language guidance. The action expert is in turn shaped continuously by semantic reasoning and predicted physical dynamics rather than by a fixed representation computed in advance. Extensive experiments are conducted on LIBERO, LIBERO-PLUS, RoboTwin2.0 along with real-world evaluation on Flexiv single-arm and dual-arm setups. Ablation studies show the effectiveness of dynamic stream prediction and layer-wise unified attention to validate our model architectural coherency.

---
