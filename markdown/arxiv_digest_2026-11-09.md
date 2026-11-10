# arXiv Daily Digest — 2026-11-09

**Mode:** direct
**Categories:** cs.AI, cs.LG, cs.RO, cs.CV
**Keywords:** VLA, RSI, agentic robot, self-improving robot, self-evolving robot, robot harness
**Papers found:** 11

---

## 1. Flex-RSI: Benchmarking Recursive Self-Improvement of Frontier Agents

**Authors:** Jingdong Zhang, Jionghao Wang, Zhengming Yu, ..., Zhengzhong Tu, Wenping Wang
**arXiv:** [2611.08946](https://arxiv.org/abs/2611.08946)
**Categories:** Artificial Intelligence (cs.AI); Computer Vision and Pattern Recognition (cs.CV); Robotics (cs.RO)

Frontier language models are increasingly deployed as agents, and how well an agent performs depends not only on its model but also on its harness: the prompts, tools, memory, and control loop through which the model acts. When an agent is applied to a new problem, a natural question is whether it can use the feedback of the task to improve the way it works, and not merely its answer. Most existing benchmarks keep the agent's harness fixed and score the solution it produces, or target large-scale model training. We introduce Flex-RSI, a benchmark for the recursive self-improvement of agents on vision and robotics tasks under a fixed budget. In each round, an executor improves the task solution, which is kept only if it scores higher on held-out validation data, and an improver then revises the harness, including the executor and itself. Every run starts from the same general-purpose harness, and the final solution is scored on hidden test data. Evaluating closed-source and open-weight models on tasks spanning perception, reasoning, robot action, 3D reconstruction, visual creation, and infrastructure, we find that self-improvement helps most when the agent builds its own solution, that feedback recording only success or failure holds back open-weight models, and that open-weight models fall furthest behind where outputs must pass strict checks of physical stability or exact correctness. Paired runs further show that editing the harness itself contributes to the gains.

---

## 2. SURE:Spatiotemporal Uncertainty Representation for Efficient Vision-Language-Action Learning

**Authors:** Jingye Zhang, Choo Sin Wai, Dake Zhong, ..., Peng Jiao, Haoqian Wang
**arXiv:** [2611.09684](https://arxiv.org/abs/2611.09684)
**Categories:** Robotics (cs.RO); Artificial Intelligence (cs.AI)

Vision-language-action (VLA) policies have become a promising paradigm for end-to-end robot control, but their effectiveness still depends heavily on large volumes of demonstration data. In manipulation tasks, this dependence is compounded by structured spatiotemporal uncertainty in the action space: multiple nearby actions or trajectories may successfully solve the same task, while semantically equivalent demonstrations often unfold at different speeds. Standard pointwise supervision treats each demonstrated action as an exact target, imposing an unnecessary learning burden under such uncertainty. We present SURE, a data-efficient VLA training framework that explicitly models both spatial and temporal uncertainty. SURE augments a VLA backbone with a lightweight transposed-convolutional probabilistic action decoder that captures spatial uncertainty through local correlations among neighboring action bins. It further introduces Soft-DTW alignment supervision to accommodate local timing variations between predicted and demonstrated action chunks. Together, these two components reduce sensitivity to demonstrator-specific poses and execution timing, enabling more data-efficient action learning. We evaluate SURE on LIBERO, RoboTwin 2.0, and real-world manipulation tasks. Even with only 10% of the demonstration data or 20% of the training steps, SURE achieves manipulation success rates that match or surpass baseline VLAs.

---

## 3. HiMEM: Hippocampus-Inspired Memory Consolidation, Pruning, and Composition for Vision-Language-Action Models in 3D Scenes

**Authors:** Boran Zhao, Yanbin Hu, Jun Ye, ..., Jin Cui, Pengju Ren
**arXiv:** [2611.09355](https://arxiv.org/abs/2611.09355)
**Categories:** Computer Vision and Pattern Recognition (cs.CV); Artificial Intelligence (cs.AI)

Memory plays a crucial role in long-horizon task execution and cross-task generalization for Vision-Language-Action (VLA) models operating in complex 3D scenes. However, existing VLA memory mechanisms suffer from memory noise, particularly in complex 3D scenes, as stored episodic memories contain extensive redundant details about scene layouts, object configurations, and robot-specific states, which obscure generalizable manipulation principles and hinder cross-task transfer. To address this challenge, we first introduce a hippocampus-inspired memory consolidation mechanism that synthesizes extensive episodic experiences into a compact set of essential semantic memories, enabling VLA models to derive generalizable principles from practical experience. Second, we propose an episodic memory pruning mechanism that removes redundant episodic memories whose contents are captured by consolidated semantic memories, thereby increasing effective memory capacity and improving long-horizon task execution. Finally, to handle complex task scenarios, we develop a flexible memory composition mechanism that jointly leverages multiple episodic and semantic memories to enhance cross-scenario generalization. Experiments on LIBERO, LIBERO-Plus demonstrate the effectiveness of HiMEM across different VLA backbones, improving the average success rate of pi_0 from 91.88% to 98.20% on LIBERO.

---

## 4. A Controlled Study of Models, Skills, Feedback, and Curriculum in Agentic Robotics

**Authors:** Kaiyuan Chen, Xinyue Zhu, Shuangyu Xie, ..., Spencer Huang, Ken Goldberg
**arXiv:** [2611.09030](https://arxiv.org/abs/2611.09030)
**Categories:** Robotics (cs.RO); Artificial Intelligence (cs.AI); Machine Learning (cs.LG)

Agentic robotics asks coding agents to implement and iteratively improve robot policies from simulated and real-world physical interactions. We study the self-learning loop of agentic robotics through a controlled simulation study spanning nine manipulation tasks, 631 different experiment configurations, and 28K coding agent rollouts, systematically varying model capability, skill priors, feedback structure, and curriculum. The experiment data suggests that the bottleneck is often not the access to sufficient information, but interpreting it into the right policy update. Across these factors, a successful self-learning loop depends on how effectively agents attribute failures, reason task-relevant spatial and geometric structure, and selectively restructure code to improve policies.

---

## 5. VLA Handover: Failure-Prediction-Based Switching from On-Robot to Server VLA Models

**Authors:** Takayuki Nishio
**arXiv:** [2611.08987](https://arxiv.org/abs/2611.08987)
**Categories:** Robotics (cs.RO); Machine Learning (cs.LG); Networking and Internet Architecture (cs.NI)

Large vision-language-action (VLA) models generalize well but are difficult to run in real time on a robot, and small VLAs that run there fail more often. Remote inference over beyond-5G and 6G networks lets a robot use a large VLA on a server, but querying the server for every action chunk limits the number of robots per server. We propose VLA handover: the robot runs a small VLA (S-VLA) and switches to a large VLA (L-VLA) on a server only when the S-VLA is likely to fail. We formulate the switching as minimizing the request cost under a required success probability and, since this problem cannot be solved directly, propose a heuristic framework that retrains neither VLA. In simulation with SmolVLA and $\pi_{0.5}$ on three of the four LIBERO suites, VLA handover raised the success rate by 11-22 percentage points over the S-VLA alone and sent 49-77% fewer requests than server-only control at a 2-4 percentage-point lower success rate, and its completion time grew less with the network latency.

---

## 6. DobotTrack: Target-Grounded Vision-Language-Action Learning for Embodied Person Tracking

**Authors:** Shengjun Deng, Yinghan Zhang, Chengrui Wei, ..., Xi Li, Teng Wang
**arXiv:** [2611.09041](https://arxiv.org/abs/2611.09041)
**Categories:** Robotics (cs.RO); Computer Vision and Pattern Recognition (cs.CV)

Language-guided embodied person tracking requires a mobile agent to identify a target from a referring description and consistently follow the target under egocentric observations. We present DobotTrack, a target-grounded vision-language-action (VLA) framework that integrates auxiliary grounding supervision with efficient temporal modeling. We systematically investigate five auxiliary tasks---person segmentation, bounding-box grounding, visual-spatial classification (VSC), future DINO feature prediction, and future-frame prediction---and adopt complementary mask and bounding-box supervision to enhance target delineation and localization. We introduce Q-identity, a target-conditioned historical visual compression module that leverages target-grounding predictions to selectively preserve identity-discriminative appearance features and spatial cues in compact historical tokens. On EVT-Bench, our 0.8B-parameter model achieves an average success rate of 77.9%, exceeding OmTrackVLA by 16.9 percentage points across the three tasks. We further construct a real-world person-tracking dataset collected using a quadruped robot, comprising 126 episodes and 596,323 mask-annotated frames. The target masks enable automatic derivation of bounding boxes and visual-spatial labels encoding horizontal position and apparent image scale, providing additional grounding supervision without separate manual annotation of these labels. Together, our framework and annotation pipeline support learning target-grounded tracking policies from simulated and real-world data. Code is available at this https URL.

---

## 7. PRISM: Primitive Routing via In-context Skill Mixing for Retentive VLA Adaptation

**Authors:** Jiachen Tao, Gengyu Zhang, Haoxuan Wang, Bing Liu, Yan Yan
**arXiv:** [2611.08917](https://arxiv.org/abs/2611.08917)
**Categories:** Robotics (cs.RO)

Vision-Language-Action (VLA) models promise a single language-conditioned policy adaptable to many manipulation behaviors, yet deployment additionally requires skill retention and long-horizon composition: a policy must retain previously acquired skills and reuse them inside composite tasks whose behavior changes across phases. The standard recipe absorbs every new task into one shared update, which provides neither a parameter-level locus for reusable skills nor a mechanism for invoking each skill along the trajectory. We observe that this missing structure is latent rather than absent: per-skill low-rank updates of a pretrained VLA occupy a robustly distinguishable, low-dimensional subspace, and a single composite-task LoRA concentrates roughly half of its Frobenius energy in this subspace, against a near-zero matched random-rotation control. Building on this geometry, we introduce PRISM, which represents reusable skills as parameter-level primitives: each skill family is stored as a dedicated low-rank action-expert adapter in a primitive bank, primitives are augmented with skill-specific low-rank residuals and composed at inference by a per-chunk VLM-conditioned router that reads the prefix representation to track task progress, and the router is supervised by per-chunk labels from a deterministic, task-conditioned, action-derived oracle. During composite training, the vision encoder, the language LoRA, the skill residuals, the router, and the shared action projections and time MLP are updated; every primitive is held frozen, so the base per-skill action-expert adapters are preserved by construction. On RoboCasa365, PRISM achieves 56.43% atomic-skill success and reaches 20.00% on long-horizon composite tasks, while a standard $\pi_{0.5}$-LoRA two-stage fine-tune reaches 17.86% atomic and 17.50% composite success. We additionally validate PRISM on an AgileX PIPER real-robot setup.

---

## 8. Localizing and Editing the Goal Representation of a Vision-Language-Action Model

**Authors:** Sudhanshu Srivastava, Faisal Aqlan
**arXiv:** [2611.08895](https://arxiv.org/abs/2611.08895)
**Categories:** Robotics (cs.RO)

Operators can state safety constraints for robots as prohibitions such as "do not put the bowl on the stove". We study whether OpenVLA follows such prohibitions and where it represents the goal it executes. The 10 tasks of LIBEROGoal share one scene, so we can label the goal that each rollout executes. We combine closed-loop rollouts with activation patching, linear probes, activation steering and runtime monitors. On LIBERO-Goal, negation had no detectable effect on which task OpenVLA executed. The model executed the forbidden task in 79% of negated rollouts and completed 78% of plain tasks. A goal probe gives similar read-outs under "not X" and "X". Activation patching shows that the first action depends mostly on the instruction tokens before layer 12 and on the last prompt token from layer 16 onward. A fixed steering vector at the instruction tokens at layer 8 redirected 12 of 18 rollouts. Fixed vectors and prefill patches at layers 12 to 20 redirected none of 158. From layer 16, only patches at every decoded action token redirected the robot (15 of 18 rollouts at layer 24). When the instruction changes during a rollout, the layer-32 goal read-out detects non-compliance better than failure detectors, and an external probe on image and instruction features performs comparably. These results support enforcing prohibitions outside the instruction and monitoring goal read-outs against the specification. Goal edits in OpenVLA should act before layer 12 or patch every action token.

---

## 9. ActPrune: Action-Grounded Visual Token Pruning for Efficient Vision-Language-Action Models

**Authors:** Sungwon Moon, Minji Kim, Hyemin Boo, Daeun Song, Jiyoung Lee
**arXiv:** [2611.08827](https://arxiv.org/abs/2611.08827)
**Categories:** Robotics (cs.RO)

Vision-language-action (VLA) models perform versatile manipulation tasks from language instructions, but their inference cost limits how fast a robot can respond in closed-loop control. Visual token pruning reduces this cost; however, prior methods estimate token redundancy from encoded visual embeddings or attention, only after the visual encoder has processed the entire observation. We propose \ours, a training-free token pruning method that moves the pruning decision ahead of the vision encoder by grounding it in a geometric prior derived from the robot's own action. The action chunk predicted at the previous control step is already available before the current observation is encoded, and it specifies the end-effector and camera motion between consecutive observations. The same action affects the two standard camera views asymmetrically: in the fixed third-person view, \ours retains patches along the projected end-effector trajectory together with semantic anchors, while in the wrist view, it prunes patches that remain unchanged after compensating for the action-induced camera motion. Extensive experiments on two simulation environments (LIBERO and VLABench) and four real-robot tasks demonstrate that \ours achieves up to 1.61 $\times$ speedup and 59.5\% FLOPs reduction with negligible degradation in success rates.

---

## 10. VICTR: Value-Informed In-Context Learning for Vision-Language-Action Models

**Authors:** Luca Macesanu, Tianluo Zhang, Aditya Patil, ..., Chen Feng, Juexiao Zhang
**arXiv:** [2611.08698](https://arxiv.org/abs/2611.08698)
**Categories:** Robotics (cs.RO)

Recent advances in robot foundation models have highlighted the potential of in-context learning (ICL) for adapting robot behavior from demonstrations without further fine-tuning. Previous work has used retrieval-based post-training to equip pretrained vision-language-action (VLA) models with the capability for ICL by teaching them to condition action predictions on retrieved visually-relevant demonstration chunks. However, the effectiveness of retrieval hinges on selecting context relevant to the current execution stage, which visual similarity alone may not capture. We introduce VICTR, a framework enabling in-context learning in VLAs via progress-informed context retrieval built around an In-Context Value Function Estimator (IC-VFE). IC-VFE conditions on a reference demonstration video, a language instruction and the current observation to estimate task-relative progress. By conditioning progress estimation on a reference demonstration, IC-VFE can align the current state with a demonstrated execution even for tasks unseen during training. VICTR uses the estimated progress to select demonstration chunks at corresponding stages of execution and supplies them to a $\pi_{0.5}$ policy post-trained for in-context action generation. On unseen out-of-domain real-world manipulation tasks, VICTR raises the success rate from 6.2% for a fine-tuned $\pi_{0.5}$ baseline to 23.8% and more than doubles the task progress rate, from 28.9% to 55.5%. Project page with code, data and videos: this https URL

---

## 11. Meituan-Robotics-0: A Vision-Language-Action Foundation Model for Desktop Manipulation

**Authors:** Meituan Robotics Team, Caicheng Wang, Chen Zhao, ..., Ziyuan Qin, Ziqin Wang
**arXiv:** [2611.08577](https://arxiv.org/abs/2611.08577)
**Categories:** Robotics (cs.RO); Computer Vision and Pattern Recognition (cs.CV)

We present Meituan-Robotics-0 (MR0), a vision-language-action foundation model and embodied-agent system for stationary-base desktop manipulation. MR0 combines 147 million vision-language samples with 15,060 hours of curated robot trajectories spanning 12 embodiments. A three-stage training recipe aligns multimodal representations with robot behavior through discrete action-token pre-training, transfers these priors to continuous cross-embodiment control through flow-matching mid-training, and adapts the policy through real-world post-training. We introduce Rollback, which pairs replaced policy segments with human corrections to provide positive and negative supervision for CFG-DAgger without value learning or advantage labeling. A unified end-effector interface supports heterogeneous embodiments, while asynchronous action-chunk merging maintains smooth execution under variable inference latency. An event-driven agent maintains persistent task events and reassesses plans when progress or feasibility changes, enabling cross-task retrieval and conditional task resumption. MR0 achieves 93.6% success on RoboTwin 2.0 and ranks fifth in the RoboDojo VLA track. Under matched HG-DAgger post-training, MR0 achieves higher average success rate and progress score than $\pi_{0.5}$ across three real-robot tasks. On Ethernet insertion, CFG-DAgger trained with Rollback data reaches 70% success and a progress score of 0.90. Qualitative agent deployments demonstrate cross-task event retrieval and recovery from temporarily unsatisfied task conditions.

---
