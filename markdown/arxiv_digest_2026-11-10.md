# arXiv Daily Digest — 2026-11-10

**Mode:** direct
**Categories:** cs.AI, cs.LG, cs.RO, cs.CV
**Keywords:** VLA, RSI, agentic robot, self-improving robot, self-evolving robot, robot harness
**Papers found:** 21

---

## 1. SciMARS: Multi-Agent Recursive Self-Improvement for Closed-Loop Scientific Discovery

**Authors:** Weimin Wu, Han Liu
**arXiv:** [2611.12552](https://arxiv.org/abs/2611.12552)
**Categories:** Artificial Intelligence (cs.AI)

We propose SciMARS, a framework for recursive task-local adaptation of multi-agent harnesses in closed-loop scientific discovery. Multi-agent systems coordinate analysis, experimental design, and verification as scientific evidence evolves. However, two problems limit their effectiveness: (i) without shared memory, agents lose observations and repeat work; (ii) fixed role procedures, handoffs, and memory policies perpetuate mistakes despite retained evidence. We address these problems with a shared evidence graph and separate component editors. SciMARS adapts roles and coordination; SciMARS + Memory adds a third editor for how agents record, retrieve, and receive evidence. Candidate probes guide composition and selection of the next harness. We evaluate scientific discovery through experimental-data replay and a digital twin. SciMARS + Memory resolves 12/18 GPT-6-Astra and 2/18 GLM-5.3 attempts on Autonomous Science Bench, compared with 8/18 and 1/18 for the base multi-agent team. On ScienceAgentBench and AppWorld, it solves 14/38 and 11/20 tasks, compared with 11/38 and 5/20 for the base team. These results support combining shared memory with harness adaptation across scientific and interactive tasks.

---

## 2. InfraRSI: Harnessing Recursive Self-Improvement for Training Infrastructure

**Authors:** InfraRSI Team, Yuchuan Tian, Haocheng Mei, ..., Yunhe Wang, Yu Wang
**arXiv:** [2611.11558](https://arxiv.org/abs/2611.11558)
**Categories:** Artificial Intelligence (cs.AI)

While Recursive Self-Improvement (RSI) accelerates isolated algorithm and kernel synthesis, distributed LLM training depends on tightly coupled launch settings, operator kernels, and communication schedules, where single edits often hit out-of-memory (OOM) boundaries, compiler conflicts, measurement jitter, or silent numerical drift. We present InfraRSI, the agentic harness that turns open-ended human commands into verified training optimizations via a five-stage workflow: init locks editable scope and a fixed task contract over workload, loss, and timing invariants to prevent reward hacking, doctor profiles baseline phases and calibrates cluster noise, run co-optimizes launch knobs and code patches before re-verifying top candidates against the baseline and logging findings to a cross-hardware experience bank, and report and apply audit source paths, track failed-trial costs, and commit promoted changes. Rather than stepping greedily from a single incumbent, InfraRSI initializes from diverse experience-seeded configurations and fits global execution-time and censored peak-memory models across all trials, including OOMs. Using these models, it prices per-setting memory costs, revises miscalibrated LLM priors from live runs, and pairs memory-hungry optimizations with memory savers and verified code patches. Across four single- and multi-node dense and Mixture-of-Experts (MoE) LLM workloads, InfraRSI achieves a speedup of up to $2.75\times$ and lifts mean Model FLOPs Utilization (MFU) from $17.4\%$ to $30.0\%$, outperforming existing tuners and coding agents while transferring experience across GPUs. As it improves training infrastructure efficiency, InfraRSI forms a two-level Recursive Self-Improvement loop---revising priors online within runs and distilling experience across clusters---to push foundation model scaling.

---

## 3. No Second Run: Does RSI Stop at Frontier Pre-training?

**Authors:** Xiaojie Cai, Jiayi Chen, Junwei Chen, ..., Yumin Zhuang, Haoyang Zou
**arXiv:** [2611.10719](https://arxiv.org/abs/2611.10719)
**Categories:** Artificial Intelligence (cs.AI)

Pre-training is where every foundation model begins; bringing recursive self-improvement (RSI) there would let AI improve the process that creates AI. Yet public RSI work has so far targeted only post-training, which starts from an existing base model, runs trials costing GPU-hours, and returns verifiable scores. Pre-training breaks all three conditions at orders-of-magnitude higher cost: a run consumes hundreds of thousands of GPU-hours over months and cannot be repeated; its objective, post-training headroom, cannot be read off any single score; and what must improve is not a model but the whole production system, from data pipelines and training infrastructure to the teams that run them. To our knowledge, we are the first to apply RSI to an entire frontier pre-training run from scratch and to report it in detail. RSI does not stop at frontier pre-training, but it changes form: since no end-to-end loop can close over a single unrepeatable run, we decompose it into smaller loops that can, each repairing a step the full run breaks. The result is 801-30B-A3B-Base, a 30B-A3B MoE trained from scratch on 11.8T tokens in three months by a newly formed team. We release it as a base model; the lightweight SFT reported here (6B tokens, no RL) only probes post-training headroom. As a base model, 801-30B-A3B outperforms Qwen3-30B-A3B and Nemotron-3.5-Lightning-30B-A3B, trailing only the larger Qwen3.5-35B-A3B, and keeps this position under identical SFT; with lightweight SFT alone, it achieves the highest average on four agentic benchmarks against fully post-trained models, including Qwen3.6-35B-A3B. Since post-training RSI presupposes a strong base model, bringing RSI into pre-training acts on the foundation every later stage builds on. We open-source 801-30B-A3B-Base and the lightweight SFT data at this https URL .

---

## 4. Is Recursive Self-Improvement Safe?

**Authors:** Vincent Conitzer
**arXiv:** [2611.10261](https://arxiv.org/abs/2611.10261)
**Categories:** Artificial Intelligence (cs.AI); Computer Science and Game Theory (cs.GT); Machine Learning (cs.LG)

The phrase recursive self-improvement (RSI) refers to the idea of an AI system designing and creating another, better AI system, which in turn designs and creates an even better one, and so on. While the idea has a long history, it has always been an abstract, futuristic idea -- until recently. Today's frontier AI has attained a set of abilities, including in programming, mathematics, research, tool use, and working coherently over extended periods of time, that make RSI seem plausible. AI companies are starting to pursue it, but many of the involved people are also expressing concerns, asking whether humanity should really set this in motion and under what conditions. I will discuss the situation, argue that we do not even have clear frameworks for thinking about the likely outcomes of RSI, and do a quick game-theoretic analysis of how to choose whether to initiate RSI when another party is making the same choice.

---

## 5. Thermo-VLA: A Thermal-Aware Vision-Language-Action Model with Gated Residual Modulation for Robotic Manipulation

**Authors:** Jingxuan Chen, Junshi Luo, Chencheng Dong, ..., Tongge Huang, Qiang Huang
**arXiv:** [2611.11981](https://arxiv.org/abs/2611.11981)
**Categories:** Robotics (cs.RO); Artificial Intelligence (cs.AI)

Recent Vision-Language-Action (VLA) models have begun incorporating thermal sensing, but existing approaches typically treat thermal images as ordinary visual inputs, providing limited support for temperature-aware relational reasoning in manipulation. To address this limitation, we propose Thermo-VLA with a ThermoRes Encoder, which decomposes thermal images into cold and hot attribute representations and injects them into the RGB token through language-conditioned residual modulation, enabling temperature-driven target selection and continuous manipulation. We further construct six real-world robotic tasks on a dual-arm Unitree G1 platform, spanning basic grounding to relational reasoning. Experiments show that Thermo-VLA achieves an average success rate of 0.86 across four thermal-dependent tasks, outperforming a pi_0.5 baseline that directly incorporates RGB-thermal observations by 18 percentage points. Under unseen-object and scene variations, Thermo-VLA maintains an average success rate of 0.78, achieving the best generalisation performance among the compared methods. Beyond thermal sensing, we transfer the same residual modulation mechanism to colour attributes and observe consistent improvements in both simulation and real-robot experiments, indicating its potential to generalise beyond thermal attributes. Project website: this https URL

---

## 6. Decoupled Asynchronous System for Humanoids (DASH): Latency-Agnostic Scaling of Vision-Language-Action Models for Humanoid Manipulation

**Authors:** Bingzhang Wang, Nathan Zhao, Jialeng Ni, ..., Kehua Chen, Jian Yao
**arXiv:** [2611.11854](https://arxiv.org/abs/2611.11854)
**Categories:** Robotics (cs.RO); Artificial Intelligence (cs.AI)

Vision-language-action (VLA) models pair a vision-language backbone with an action head, but in closed-loop control the backbone sits on the control-critical path: while it computes, the robot keeps moving, so each executed action is conditioned on an increasingly stale observation. A larger backbone therefore directly blocks reactivity, especially in humanoid dexterous manipulation. We present DASH, a Decoupled Asynchronous System for Humanoids that removes this coupling. DASH splits the policy into a slow vision-language model (System 2) and a fast flow-matching action head (System 1) that run as concurrent processes over the LCM communication protocol, so the control rate is set by the action head alone, independent of backbone size. The action head fuses stale semantics from a frozen backbone with fresh vision from its own ResNet encoder, desynchronized training exposes it to the staleness it meets at deployment, and an adaptive temporal aggregator aligns overlapping action chunks under variable inference latency. On an asynchronous RoboTwin benchmark that charges inference latency in simulated time, DASH holds 20 Hz control rate from 0.8B to 8B backbones while the synchronous rate falls from 9.7 to 4.1 Hz, with higher success at every size. On a real humanoid with dexterous hands, DASH achieves clearly higher pick-and-place success than the synchronous pipeline.

---

## 7. Zero-Shot VLA Adaptation with Retrieved Guidance

**Authors:** Subin Kim, Anh-Quan Pham, Dinesh Jayaraman
**arXiv:** [2611.10894](https://arxiv.org/abs/2611.10894)
**Categories:** Robotics (cs.RO); Artificial Intelligence (cs.AI); Machine Learning (cs.LG)

Pre-training large parametric "Vision-Language-Action" (VLA) models on large demonstration datasets has recently yielded promising results for general-purpose manipulation. However, these models still struggle under even small domain shifts relative to the training data, such as changes in camera viewpoint, background, object identity, or robot morphology. Motivated by the success of Retrieval-Augmented Generation (RAG) in language models, we pursue retrieval to boost VLA performance. Specifically, we seek to leverage retrieval from domain-mismatched, "in-the-wild" demonstration datasets like DROID to guide a VLA's behavior in a new target domain. To achieve this, we introduce RAGu, which overcomes robotics-specific challenges for RAG: (1) It incorporates simple geometric calibration to transform source demonstrations into the target setup and reduce cross-domain differences. (2) It uses a coarse-to-fine retrieval strategy that selects, from a large pool of pre-warped candidates, the trajectory most compatible with the base VLA. (3) It guides the VLA's flow-matching inference procedure rather than seeking to retrain the base model or expand its limited context window. We evaluate RAGu across real-world, simulation, sim-to-real transfer, and cross-embodiment humanoid manipulation. We find it improves real-world VLA success rates from 20% to 80% and outperforms the closest-related baselines in sim. Project website: this http URL

---

## 8. Trustworthy Recursive Self-Improvement with Statistical Guarantees

**Authors:** Zihe Gao, Zhengling Qi, Yifan Cui
**arXiv:** [2611.10787](https://arxiv.org/abs/2611.10787)
**Categories:** Machine Learning (stat.ML); Artificial Intelligence (cs.AI); Machine Learning (cs.LG); Methodology (stat.ME)

Recursive self-improvement offers a promising path toward AI agents that improve through experience by refining their own harnesses without retraining their underlying large language models (LLMs). Making this self-improvement process reliable, however, requires more than generating new updates: agents must decide which changes are worth keeping. A greedy gate that accepts updates based solely on higher validation scores can mistake an observed gain for genuine progress and lead to performance degeneration, whereas overly conservative statistical gates may reject beneficial updates and hinder performance improvement. We introduce Trustworthy Recursive Updates with Statistical Testing (TRUST), a framework that adapts an online multiple hypothesis testing procedure to control the rate of false evolution across rounds, with an LLM analyzing historical context to help determine how much evidence is required to update the incumbent. Under interpretable assumptions, we prove that TRUST limits the proportion of accepted updates that result in unacceptable performance loss. We further derive a lower bound on the final performance gain. Across the benchmarks HotpotQA, DROP, and APPS with the models DeepSeek-V4-Flash and Qwen-3.8-Flash, TRUST reduces the average ratio of accepted inferior updates from the greedy gate's 45.59% to 2.78%, while achieving higher final scores than the state-of-the-art statistical gate baselines for recursive self-improvement. These findings demonstrate that TRUST strikes a balance between statistical reliability and performance gain in recursive self-improvement.

---

## 9. DeltaForge: A Post-hoc Mixture-of-Experts VLA for Multi-Domain Autonomous Driving

**Authors:** Bingzhang Wang, Mo Poorsartep, Yasaman Esfandiari
**arXiv:** [2611.11856](https://arxiv.org/abs/2611.11856)
**Categories:** Machine Learning (cs.LG); Robotics (cs.RO)

Fleets of driving vision-language-action (VLA) models are developed one domain at a time: each operator finetunes a shared base model on private data, producing specialized experts that are costly to consolidate into a single model. Weight merging loses accuracy as heterogeneous domains accumulate, and dense mixture-of-experts routing is prohibitively expensive to combine them. We present DeltaForge, to our knowledge the first post-hoc mixture-of-experts VLA for driving, which consolidates N independently finetuned per-domain models into a single multi-domain model from their weights and a small proxy set alone. When different operators finetune the same base model, their weight updates end up sharing a lot of structure. We exploit this by decomposing all the updates together using singular value decomposition (SVD), splitting each one into a shared part (the same across all domains) and a tiny domain-specific part. The router then only needs to work with those tiny domain-specific pieces, not the full expert weights, which is what keeps the approach efficient. Then two cooperating clip-level blind routers, one over the VLM reasoning experts and one over the flow-matching dynamics experts, are trained from soft labels on the proxy dataset. Across six diverse domains spanning urban, off-road, and highway driving on cars, trucks, and all-terrain vehicles (ATVs), DeltaForge approaches the accuracy of the per-domain experts and surpasses every merging, routing, centralized, and federated baseline at close to single-model parameter and compute cost. Adding a new domain requires only projecting its weight update onto the shared basis with no end-to-end retraining needed. The resulting model also generalizes to domain combinations it was never explicitly trained on.

---

## 10. VLA Adaptation with Real and Simulated Data: A Case Study on Robotic Chess

**Authors:** Matěj Kripner, Milan Straka
**arXiv:** [2611.12676](https://arxiv.org/abs/2611.12676)
**Categories:** Robotics (cs.RO); Machine Learning (cs.LG)

Vision-language-action (VLA) models are trained as general-purpose foundation models for robot learning, and require fine-tuning for each downstream task and robot. This raises practical questions such as how much data and training updates are needed, how checkpoints should be selected, and whether simulation can be leveraged to alleviate the cost of real data collection. We study these questions on a task that requires both precise manipulation and spatial understanding of the scene. In this task, an SO-101 arm moves a chess king between two squares that are given only by their names, such as e4 and a5. We fine-tune $\pi_{0.5}$ with various dataset sizes and update budgets, using teleoperated demonstrations as well as simulated demonstrations from a randomized scripted expert that imitates the variability of human demonstrations. In simulation, the success rate scales with both data and updates. Importantly, we find that a short learning-rate cool-down adds up to 31 points and is necessary for comparing checkpoints, and that validation loss and action error are unreliable for model selection. On the real arm, we fine-tune on up to 256 teleoperated demonstrations and evaluate ten policies in 25 trials each. Partial results indicate that pretraining on the simulated demonstrations helps substantially, most clearly when real data is scarce. We also present a negative result, in which training on the policy's own rollouts with filtered behavior cloning, RECAP-style advantage conditioning, corrections from an automatic coach, or residual reinforcement learning did not yield a measurable improvement over plain behavior cloning in our setting. We release the simulator, the expert and the real demonstrations.

---

## 11. Streaming Failure Forecasting: VLA Failure Monitors That Keep Learning After Deployment

**Authors:** Amit Jadhav, Shaurya Beriwala, David Q. Liu, Yanfei Liu
**arXiv:** [2611.11688](https://arxiv.org/abs/2611.11688)
**Categories:** Robotics (cs.RO); Machine Learning (cs.LG)

Failure monitors for vision-language-action (VLA) policies are trained offline and then frozen. After deployment, lighting, objects and cameras drift, and the policy itself is updated or moved to new tasks. On recorded real-robot runs, after a switch of task or policy version, a frozen monitor fit on the old task ranks failures little better than chance. We present Streaming Failure Forecasting (SFF), a monitor that keeps learning from the one label every episode provides: whether it succeeded. SFF keeps the offline monitor's network fixed and refits only its last linear layer after each episode, at 2.18 ms per policy call on a Jetson CPU core. Its alarm threshold moves only after successes, which in simulation kept false alarms near target except when two drifts came at once. With every setting locked before testing, SFF ranks failures better than the same monitor kept frozen on 4 of 5 simulated test suites under unannounced drift, and above resetting on detected drift on every suite. Carried with its locked learner settings to 434 recorded runs of four VLAs on real SO-101 arms, replayed across unannounced switches of task or policy version, it ranks failures better than the frozen monitor for every VLA and, in an exploratory comparison, above a full reset at the true switch. A deployed failure monitor need not stay frozen: refitting its readout from outcomes is cheap and helps after the changes we tested.

---

## 12. AutoVLA-D: Learn a Trajectory-Geometric Condition from Reasoning for Autonomous Driving VLA

**Authors:** Yuguang Yang, Zhewen Tan, Canyu Chen, ..., Yan Wang, Xianbin Cao
**arXiv:** [2611.12382](https://arxiv.org/abs/2611.12382)
**Categories:** Robotics (cs.RO); Computer Vision and Pattern Recognition (cs.CV)

Autoregressive VLA planning usually predicts continuous trajectories as the final output, but driving instructions often describe actions rather than ego states, which weakens direct conditioning on the final continuous trajectory. We address this gap with TrajCond, which introduces a discrete trajectory-geometric condition for VLA planning. Specifically, we represent TrajCond as a 1D-Brohan differential action trajectory and learn it with a two-stage training framework before final continuous trajectory prediction. With the simultaneous autoregressive generation of discrete and numeric trajectories, we name our method AutoVLA-D (Double). Experiments on NAVSIM navtest, nuScenes, and NeuroNCAP show that discrete trajectories are weaker as direct outputs but more effective as TrajCond, consistently improving final continuous trajectory prediction across closed-loop and open-loop driving benchmarks. Code is available at this https URL.

---

## 13. VLA-MOPD: On-Policy Distillation for Multi-Task VLA Policy Consolidation

**Authors:** Yongxuan Lv, Zhen Fang, Lichen Man, ..., Fei Wang, Feng Zhao
**arXiv:** [2611.12286](https://arxiv.org/abs/2611.12286)
**Categories:** Robotics (cs.RO); Computer Vision and Pattern Recognition (cs.CV)

Physical intelligence requires embodied agents to ground language in observations and execute actions while retaining useful skills. Vision-language-action (VLA) policies offer a shared interface, but task-specific post-training often produces separate specialists. Consolidation is difficult: mixed-task reinforcement learning provides sparse trajectory-level credit, while offline distillation may miss student-visited observations and endpoint distillation does not supervise intermediate action-generation states. We introduce VLA Multi-teacher On-Policy Distillation (VLA-MOPD), a protocol for consolidating flow-matching VLA specialists. After acquiring task or suite experts, a shared student collects robot rollouts and queries the instruction-routed frozen teacher at each visited observation and intermediate ordinary differential equation (ODE) state. Detached per-flow-step transition targets supervise valid action chunks through a masked local matching loss; an optional reference-policy term supports retention on other tasks. Starting from one trajectory per LIBERO task, VLA-MOPD raises mean success-once from 75.4% to 98.9%, compared with 98.15% for endpoint action distillation. It improves mean RoboTwin 2.0 success from 73.0% to 89.3%; on a Piper robot, two consolidation rounds improve average success from 70.0% to 90.0%. In a near-matched Spatial-adaptation study, reference matching limits the Object suite decrease to 3.0 points, versus 13.2 without the reference term.

---

## 14. Flip Anything with Agentic Robotics Self-Learning

**Authors:** Shuangyu Xie, Kaiyuan Chen, Ken Goldberg
**arXiv:** [2611.11941](https://arxiv.org/abs/2611.11941)
**Categories:** Robotics (cs.RO)

Flipping is a fundamental robotic manipulation skill that requires reorienting a target object in a stable pose on a planar support surface by rotating it 180$^\circ$ about an axis parallel to the support surface -- think of flipping a coin from heads to tails. Although flipping is a common objective in industrial tasks such as parts inspection, mechanical assembly, and tool use, coding a bimanual robot with grippers to flip diverse objects is a significant challenge. In this paper, we show that a coding agent can autonomously develop and refine object-flipping strategies through iterative learning in physics simulations across diverse object geometries. Progressive skill acquisition, from basic handover to toppling and pushing, robust grasping and sensing, and thin-object manipulation with recovery, improves task success from 24.7% to 95.0%. The resulting graph-based code integrates high-level strategy selection with reactive control, enabling multi-stage flipping on physical robots.

---

## 15. DreamVLA: From Generated Human Motions to Humanoid Vision-Language-Action Policies

**Authors:** Kevin Park, Izat Rasyad, Dvij Kalaria, Shankar Sastry
**arXiv:** [2611.10872](https://arxiv.org/abs/2611.10872)
**Categories:** Robotics (cs.RO)

Training vision-language-action (VLA) policies typically depends on substantial robot demonstration data, making human teleoperation a costly and cumbersome bottleneck, particularly for whole-body humanoid interaction. Reinforcement learning in simulation offers an alternative for scaling this data, but designing task-specific rewards remains challenging. To address this, we propose DreamVLA, which uses generated motion trajectories to guide reinforcement learning (RL) in simulation, converting them into reliable task execution trajectories. These trajectories train VLA models in simulation without new task-specific teleoperation data. Our central contribution is a reference-conditioned DAgger distillation procedure: after a failed learner rollout, we restart the RL expert from a sampled learner state with the same reference suffix and aggregate successful corrective trajectories, addressing the distribution shift left by offline imitation. We evaluate picking from a platform, opening a drawer, pressing a button, and walking and picking from a platform, with ablations of DAgger iterations, residual RL, and generated dataset scale. Project website: this http URL.

---

## 16. Spatial Representation Distillation and Knowledge Routing for Vision-Language-Action Models

**Authors:** Jungin Park, Chaoran Zhu, Changjae Oh, Kwanghoon Sohn
**arXiv:** [2611.10443](https://arxiv.org/abs/2611.10443)
**Categories:** Robotics (cs.RO)

Understanding three-dimensional physical structure has become essential for vision-language-action models (VLAs). However, existing approaches either rely on explicit geometric inputs at inference time or adopt a single visual pathway, potentially compromising the visual-semantic knowledge inherited from pre-trained models. We present SPARK-VLA, Spatial Representation distillation and Knowledge routing for VLAs, a preserve-specialize-route framework for spatially adapting VLAs without requiring external 3D inputs or experts at inference. SPARK-VLA consists of two key components: (1) spatial representation distillation, which transfers 3D understanding from a frozen 3D expert to a LoRA-adapted visual branch by aligning attention responses while preserving the original visual pathway, and (2) a lightweight knowledge router, which selectively forwards action-relevant visual tokens to the language model using routing supervision derived from action-loss gradients. Across LIBERO, LIBERO-Plus, CALVIN, and real-world manipulation, SPARK-VLA achieves strong performance with only a 0.5B language backbone and approximately 53M trainable parameters, providing an effective and parameter-efficient approach to 3D-aware VLA learning. Code is available at this https URL.

---

## 17. World In-Context Learning for Agentic Robot Manipulation

**Authors:** Heng Fang, Zehui Guo, Yuehan Zhang, ..., Dingkang Liang, Xiang Bai
**arXiv:** [2611.12885](https://arxiv.org/abs/2611.12885)
**Categories:** Computer Vision and Pattern Recognition (cs.CV); Robotics (cs.RO)

Trained action policies write manipulation skill into network weights, tying what is learned to the distribution it is learned from. In-context learning (ICL) avoids this coupling but has not matched trained policies, because a demonstration recorded in another scene carries no feedback from the world the robot currently faces. We observe that what an agent learns in context is semantic, recording task steps and object roles rather than visual appearance, so experience gathered in one world transfers to another. Based on this insight, we propose World In-Context Learning (WICL), a paradigm in which a frozen model starts from a demonstration, rehearses the task in a world such as a simulator, and writes the feedback into its context rather than its weights. We build RoboScript, a modular infrastructure that implements WICL for agentic manipulation. From a single demonstration, RoboScript learns each task through rehearsal in simulation, freezes the learned knowledge as a Task Memory, and deploys the frozen memory on new scenes with data isolation that ensures every deployment input is available on a real robot. On all 50 tasks of RoboTwin 2.0, RoboScript reaches 83.4% mean success across clean and randomized settings with one demonstration per task and no gradient updates, exceeding the strongest trained action policy by over 20 points. The method generalizes across visual distributions, improves through reflection, scales with the foundation model, and transfers to a physical dual-arm robot through cross-embodiment memory adaptation. With a world in the loop, a robot can learn a manipulation task in its context as well as it learns one in its weights. All code is available at this https URL

---

## 18. Efficient VLA Inference via Retrieval-Based Speculation and Hardware Acceleration

**Authors:** Zhengyang Cheng, He Zhu, Zeyu Guo, ..., Yu Feng, Minyi Guo
**arXiv:** [2611.11098](https://arxiv.org/abs/2611.11098)
**Categories:** Hardware Architecture (cs.AR); Robotics (cs.RO)

Vision-language-action (VLA) models enable robots to understand and execute complex instructions, but their autoregressive (AR) action generation introduces significant latency on resource-constrained robotic platforms. Speculative decoding can accelerate AR-based inference by parallelizing action generation and verification; however, existing approaches rely on costly draft models, which are inefficient on edge platforms.
In this paper, we propose Zora, a hardware-software co-design framework for accelerating AR-based VLA inference. Specifically, Zora introduces a lightweight retrieval-augmented generation (RAG)-based draft model that exploits robotic dynamics without additional neural draft models. We further reduce batch verification overhead through a kinematics-guided action-acceptance strategy and a KV-cache-sharing attention mechanism. To address the retrieval overhead introduced by RAG-based drafting, we co-design dedicated hardware support, Zora core, to address the memory irregularity in RAG-based drafting. We evaluate Zora on four VLA models with the LIBERO benchmark. Zora retains comparable accuracy while achieving up to 3.4$\times$ speedup with software-only optimization and up to 7.6$\times$ speedup with hardware support over GPUs.

---

## 19. How Many Demonstrations Does a VLA Need? On the Sample Efficiency of VLA Finetuning

**Authors:** Rahul Chand, Miguel Villa Floran
**arXiv:** [2611.09964](https://arxiv.org/abs/2611.09964)
**Categories:** Computer Vision and Pattern Recognition (cs.CV); Robotics (cs.RO)

Pretrained vision language action (VLA) models show strong zero-shot performance but they are rarely deployed directly and are often first post-trained on demonstrations from the target setting. Yet VLAs are typically compared by zero-shot or full-data fine-tuned success which reveals little about the data and compute required for downstream adaptation. We study adaptation efficiency for six VLAs ($\pi_0$, $\pi_{0.5}$, and GR00T N1-N1.7) on four LIBERO suites, varying both demonstrations and training steps. This reveals differences hidden by full-data fine-tuning: models which are within two points on the full LIBERO-Spatial dataset differ by up to 3$\times$ in success with 50 demonstrations. $\pi_{0.5}$ needs 2-5$\times$ fewer demonstrations than $\pi_0$ and is the most sample-efficient model at every budget, with the largest gap on the long-horizon suite. Within GR00T, N1.5 adapts more efficiently than N1.6 and N1.7 on three of four suites, despite their stronger zero-shot performance. We also study one pretraining factor behind these differences by freezing the VLM during finetuning: this severely degrades the $\pi$ models whose VLM is jointly trained with the action expert during pretraining, but barely affects GR00T models.

---

## 20. From Game Generation to Game Playing: Fully Automated Ability Training for Vision-Language-Action Models

**Authors:** Changran Liu, Qi Wu, Wenchao Ma, Sharon X. Huang, Haomiao Jiang
**arXiv:** [2611.11136](https://arxiv.org/abs/2611.11136)
**Categories:** Computer Vision and Pattern Recognition (cs.CV)

Training vision-language-action (VLA) models to follow gameplay instructions across diverse games is limited by the cost of collecting demonstrations. We introduce a framework that automatically generates game environments and expert demonstrations. An LLM-powered agent uses game-building tools to construct executable environments and tasks targeting specified skills. Programmatic experts then use privileged simulator state to generate aligned instructions, rendered observations, and keyboard and mouse actions. We train our game policy, Script2Play, by post-training a 4B vision-language model with behavior cloning on 150.3 hours of synthetic Minecraft and Roblox gameplay, without human gameplay demonstrations or reinforcement learning. Evaluation on multiple public game benchmarks demonstrates that Script2Play follows gameplay instructions effectively and generalizes across game engines, highlighting the effectiveness of targeted synthetic supervision.

---

## 21. QCC-WM: Linking Macro-State Dynamics and Visual Generation via Quotient Causal Construction

**Authors:** Zhizhong Fu, Wei Zhou, Zhaoyang Jiang, ..., Xiaorong Ding, Yifan Chen
**arXiv:** [2611.12353](https://arxiv.org/abs/2611.12353)
**Categories:** Computer Vision and Pattern Recognition (cs.CV)

A key challenge in action-conditioned world modeling is to construct macro-states from high-dimensional observations that support recursive prediction under actions, while keeping their predicted evolution consistent with visual changes in generated observations. We propose QCC-WM, a visual world model based on Quotient-based Causal Construction. QCC-WM uses action responses to guide macro-variable construction for recursive action-conditioned prediction. A shared reference quotient measurement constrains the consistency between predicted states and observed changes, allowing macro-level predictions to provide structured constraints for future visual generation.
Using translational and rotational actions and their predicted responses, the model aggregates local visual features into macro-nodes with spatial correspondence through causal abstraction, and recursively predicts node content and motion under a shared reference measurement. Macro-level predictions guide future observation generation, while predicted motion transports historical appearance information. Node-level errors between generated observations and macro-level targets are then mapped back to the corresponding spatial regions for correction, improving consistency between visual generation and macro-level predictions.
On the US-VLA dataset, QCC-WM achieves an ROI-MSE of 0.01861 for four-step prediction. Compared with the best baseline at each prediction horizon, it reduces LPIPS by 48.59%, 41.68%, and 30.23% for four-step prediction and eight- and sixteen-step recursive extrapolation, respectively. Ablation studies and mechanism analyses show that motion-guided reference transport mainly improves pixel reconstruction, while node-level error feedback further improves perceptual quality and consistency between generated observations and macro-level predictions.

---
