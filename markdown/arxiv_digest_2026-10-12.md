# arXiv Daily Digest — 2026-10-12

**Mode:** direct
**Categories:** cs.AI, cs.LG, cs.RO, cs.CV
**Keywords:** VLA, RSI, agentic robot, self-improving robot, self-evolving robot, robot harness
**Papers found:** 12

---

## 1. OGPO: Offline Goal-conditioned Policy Optimization for Recoverable Vision-Language-Action Models

**Authors:** Xule Gao, Xi Wang, Zehua Zang, ..., Changwen Zheng, Chuxiong Sun
**arXiv:** [2610.12914](https://arxiv.org/abs/2610.12914)
**Categories:** Artificial Intelligence (cs.AI)

Vision-language-action (VLA) models have shown strong promise in robotic manipulation, yet their post-training still predominantly relies on trajectory-level supervised imitation over robot demonstrations. While effective for learning feasible actions, this paradigm supervises policies to reproduce expert actions at each step, biasing them toward demonstration-specific action paths and providing limited guidance for recovering toward task-progress states once execution deviates from demonstrated trajectories. To address this limitation, we propose OGPO, an Offline Goal-conditioned Policy Optimization framework for recoverable VLA post-training. Instead of treating offline demonstrations merely as step-wise action labels, OGPO adaptively relabels trajectories with semantic key states and constructs goal-conditioned process rewards to optimize the policy for reaching these task-progress states. In this way, OGPO shifts VLA post-training from trajectory-level action imitation to key-state reachability learning, enabling policies to acquire a more robust ability to complete goal states from feasible off-demonstration states without requiring additional online interaction. Experiments on LIBERO and MetaWorld show that OGPO consistently improves VLA policy performance over standard supervised fine-tuning. Moreover, evaluations on LIBERO-Plus and our proposed LIBERO-ReAct, a mid-execution perturbation benchmark, further demonstrate that OGPO achieves stronger robustness and goal-directed recoverability under distribution shifts and recoverable off-demonstration states.

---

## 2. RESCUE: Is This Alarm Worth Acting On? Counterfactual Evaluation of VLA Runtime Monitors

**Authors:** David Ahmedt-Aristizabal, Abdelwahed Khamis, Mohammad Ali Armin, Lars Petersson
**arXiv:** [2610.13516](https://arxiv.org/abs/2610.13516)
**Categories:** Robotics (cs.RO); Artificial Intelligence (cs.AI)

Runtime failure monitors for robot policies are typically evaluated by how accurately they distinguish failed from successful executions. Yet an accurate alarm may arrive too late for recovery, while an unnecessary intervention may disrupt an execution that would otherwise succeed. We introduce RESCUE, a counterfactual framework for evaluating whether a monitor's alarms enable useful interventions. By restoring simulator and policy states at execution checkpoints, RESCUE compares alternative actions, identifies the latest checkpoint satisfying a specified recovery criterion, and evaluates whether acting on alarms reduces expected task-completion cost. We evaluate RESCUE with OpenVLA-OFT and $\pi_{0.5}$ over LIBERO-Spatial and LIBERO-Plus using 128,340 counterfactual branches. Recoverability depends on the state--intervention pair rather than on robot state alone: at $\tau=0.5$, 14 of 66 OpenVLA-OFT/LIBERO-Plus failures contain a recoverable checkpoint under continuation, compared with 34 of 66 under continuation or scripted recovery, while recovery reduces recoverability in other conditions. On the primary strong-policy conditions, favourable detection scores do not establish lower intervention cost. Under the evaluated stop-and-reset model, even an idealised detector can afford only a 2.0--3.3% false-alarm rate before unnecessary resets outweigh the savings from stopping failures early. These results show that monitor value depends jointly on the intervention available and the workload in which it is deployed.

---

## 3. Beyond Actions: Learning Future Operation Targets for Vision-Language-Action Models

**Authors:** Min Lin, Bokai Zhou, Jianqi Lin, ..., Shen Zhao, Xiaodan Liang
**arXiv:** [2610.13212](https://arxiv.org/abs/2610.13212)
**Categories:** Robotics (cs.RO); Artificial Intelligence (cs.AI)

Actions specify what a robot should execute, but do not describe what those commands will achieve. Vision-language-action (VLA) policies nevertheless learn primarily by predicting action chunks from images, language, and state. We introduce Action--Future Coupled Effect Learning (AFCE), which makes a future-grounded physical Effect the policy's primary prediction target. An offline tokenizer constructs temporally ordered Effect tokens from demonstrated actions, realized robot responses, and sparse visual transitions. Reconstruction objectives encourage the representation to retain executable detail and observed physical change. A flow-matching VLA predicts Effects from current images, instruction, and robot state, while a state-conditioned decoder converts them into action chunks. Embodiment-specific interfaces allow single- and dual-arm tasks to share the Effect model. On DexJoCo, AFCE achieves $50.97\%$ overall success, improving over $\pi_{0.5}$ and UVT by 11.82 and 15.21 percentage points, respectively. It leads on all five bimanual tasks, highlighting the value of Effect supervision for coordinated dexterous manipulation. The project page is available at this https URL.

---

## 4. Imagine the Future, Internalize the Gist: Efficient VLA Reasoning via Internalized Spatiotemporal Imagination

**Authors:** Shenglan Li, Zhendong Mi, Hengyi Zhu, ..., Pu Zhao, Shaoyi Huang
**arXiv:** [2610.02626](https://arxiv.org/abs/2610.02626)
**Categories:** Computer Vision and Pattern Recognition (cs.CV); Artificial Intelligence (cs.AI); Machine Learning (cs.LG); Robotics (cs.RO)

Vision-language-action (VLA) models increasingly incorporate intermediate reasoning to improve robotic manipulation, yet existing approaches primarily reason about observed states without explicitly anticipating future scene evolution. Extending such reasoning to explicit future rollouts at every inference step, however, introduces substantial computational overhead. We propose IG-VLA, a VLA reasoning framework that enables models to imagine the future and internalize the gist. Our Latent Spatiotemporal Reasoning learns to imagine task-relevant future scene evolution directly in visual representation space, guiding action prediction without costly pixel-level video generation. To further reduce inference overhead, we introduce Scene Gist Memory, which internalizes reasoning-derived scene-behavior associations into a compact Scene Gist Token, preserving the benefits of future reasoning while bypassing explicit future imagination at inference. Extensive experiments on LIBERO, LIBERO-Plus, and VLABench demonstrate the effectiveness and efficiency of IG-VLA. On the LIBERO-Plus Language suite, both the reasoning and gist policies outperform the strongest baseline by nearly 6% in success rate. The gist policy also achieves up to 6.38x speedup over baselines, reducing inference latency from 1081ms to 169.5ms per action chunk on a single NVIDIA A6000 GPU. These results demonstrate that future spatiotemporal reasoning can be effectively internalized for efficient VLA deployment.

---

## 5. JitterVLA: A Replay Benchmark for Motion Quality in VLA-Driven Human-Robot Manipulation

**Authors:** Faith Ogunwoye, Didar Seyidov, Konstantin Gubernatorov, Dzmitry Tsetserukou
**arXiv:** [2610.13628](https://arxiv.org/abs/2610.13628)
**Categories:** Robotics (cs.RO); Human-Computer Interaction (cs.HC); Machine Learning (cs.LG)

Vision-language-action (VLA) policies issue sparse targets whose arrival at the robot controller is delayed and irregular, so a reasonable predicted action can still produce abrupt motion near people. Remedies are evaluated on different streams, delays and metrics. JitterVLA replays identical commands and arrival traces through alternative controllers, isolating the controller's effect. We apply it to synthetic reaches, hand trajectories from 20 people, three open VLA pipelines (838 episodes) and a physical UR3. Interpolation lowered modeled p99 jerk for every source, by 83% (615 to 106 m/s^3) on human motion with 200 ms delay, at a 2.0 cm tracking cost, and the effect replicated on 598 new episodes; jerk-limited generation lowered jerk further at a larger cost. Entropy-discontinuity associations had opposite, replicated signs in two pipelines, and entropy gating helped in one but not the other. On the UR3, interpolation lowered accelerometer-derived jerk by 3.0-14.0% in all six exploratory pairs, while a position-derived metric did not resolve the contrast. JitterVLA supports screening before human-centred studies; code and data will be released.

---

## 6. Splat2Act: From Captured Scenes to Personalized VLA Manipulation

**Authors:** Xiaomeng Ye, Krishna Jaganathan, Gyubeum Lim, ..., Muhammad Zubair Irshad, Zsolt Kira
**arXiv:** [2610.13945](https://arxiv.org/abs/2610.13945)
**Categories:** Robotics (cs.RO); Computer Vision and Pattern Recognition (cs.CV)

A user who brings a generalist manipulation policy into their home or office wants it to pick up their objects from their shelves, counters, and tables. Yet even a strong generalist like $\pi_{0.5}$ achieves 0% pickup success in our captured deployment scenes without adaptation, and collecting real demonstrations in every user's environment is prohibitively expensive. We present Splat2Act, an automated real-to-sim-to-real pipeline that personalizes a pretrained vision-language-action (VLA) policy to a specific scene and object set using only a handheld phone scan and images of the user's objects. Unlike prior real-to-sim work that reconstructs individual tabletops, Splat2Act operates on building-scale indoor environments: it builds a photorealistic digital twin with 3D Gaussian Splatting and collision geometry, automatically discovers tabletop and non-tabletop receptacles, constructs feasible pickup tasks, and generates successful demonstrations with a privileged simulation oracle, with only scene and object capture required from a human. Applied to 101 scanned campus environments with a median navigable area of 104.87 m$^2$ and 7 receptacles, the pipeline yields 852 receptacles and over 68,000 pickup demonstrations. We fine-tune $\pi_{0.5}$ in two stages: Stage 1 adapts to hundreds of public object assets, drawn either from the deployment scene alone or from all 101 scenes; Stage 2 personalizes to the user's own objects on the deployment scene's receptacles. Our strongest personalized policy reaches 62.5% aggregate pickup success in the target scene. Deployed on a real Stretch 3, the same policy achieves 63.9% success on a 12-task subset, closely tracking its 66.7% simulated success on those tasks. These results suggest that automated real-to-sim-to-real training can personalize VLA manipulation policies using only simulation-oracle data.

---

## 7. Noise Space Learning for VLA Adaptation

**Authors:** Junjie Lu, Chuheng Zhang, Yucen Wang, ..., Min Xu, Li Zhao
**arXiv:** [2610.13943](https://arxiv.org/abs/2610.13943)
**Categories:** Robotics (cs.RO)

Pretrained vision-language-action (VLA) models encode broad manipulation priors, yet adapting them to specific tasks requires balancing limited robot interaction, computational resources, and safety constraints. Noise space learning (NSL) adapts flow-matching-based VLAs by learning a context-conditioned distribution over noise while keeping the pretrained VLA fixed. Building on prior noise-steering methods, we formulate NSL as an interface for VLA adaptation that accommodates different learning algorithms and instantiate it with PPO, SAC, and AWR. Theoretically, we provide an information-theoretic analysis of how NSL enables efficient adaptation. Empirically, we study these NSL algorithms on LIBERO, RoboTwin, and four real-robot manipulation tasks under interaction, computation, and execution constraints. Across these settings, we develop a suite of effective NSL variants and derive practical recommendations for choosing among them under different resource and deployment regimes.

---

## 8. Reflect-VLA: Internalizing Reflective Guidance via Dual-Path On-Policy Self-Distillation for Autonomous Driving

**Authors:** Yuechen Luo, He Chong, Fang Li, ..., Zhi-Xin Yang, Fuxi Wen
**arXiv:** [2610.13453](https://arxiv.org/abs/2610.13453)
**Categories:** Robotics (cs.RO)

Reinforcement Learning (RL) substantially improves planning performance in autonomous-driving Vision-Language-Action (VLA) models. However, existing RL methods rely on scalar trajectory rewards that measure overall quality but fail to identify specific planning errors or provide actionable correction signals. In long-tail scenarios, errors in scene understanding, behavior selection, and trajectory execution are compressed into a single score. We observe that Reflective Guidance turns trajectory evaluation into explicit diagnoses and corrective instructions, substantially improving planning accuracy. Yet such guidance requires an initial prediction and its evaluation results, making it unavailable for direct single-pass inference. We propose Reflect-VLA, which treats Reflective Guidance as training-time privileged information and internalizes its planning benefits through Dual-Path On-Policy Self-Distillation (Dual-OPSD). Unlike scalar-reward optimization, Dual-OPSD uses the driving score only to route student-generated trajectories. It distills dense token-level corrective distributions from the teacher for risky trajectories while applying self-imitation to preserve reliable ones. To provide reliable corrective distributions on student rollouts, the teacher is progressively constructed through Driving-Knowledge Pretraining, Planning-and-Refinement SFT, and Self-Refinement Rejection Sampling. At inference time, Reflect-VLA generates trajectories in a single pass without explicit guidance or iterative refinement. Experiments on NAVSIM v1/v2 and Bench2Drive demonstrate competitive planning performance while reducing training time by over 90% compared with RL.

---

## 9. EndoRSI: Physical-Evidence-Driven Recursive Improvement of Endoscopic Robot Policies

**Authors:** Chi Kit Ng, Yidong Zhang, Tianchun Wu, ..., Huxin Gao, Hongliang Ren
**arXiv:** [2610.13376](https://arxiv.org/abs/2610.13376)
**Categories:** Robotics (cs.RO)

Artificial intelligence is beginning to automate scientific discovery, yet physical robot-policy research still relies on scientists and engineers to interpret experimental failures and decide how controllers should be revised. We present EndoRSI (Endoscopic Recursive Self-Improvement), a human-governed, self-improving robotic research system in which the embedded EndoForge coding agent iteratively develops and refines endoscopic robot policies using evidence from physical experiments. Physical execution remains isolated within a safety-constrained runtime under human authorisation. In motorised endoscopy, validation evidence first caused the agent to reject an initial action representation, while subsequent physical experiments falsified an offline-supported insertion strategy by revealing hazardous closed-loop behaviour absent from the source data. Failed physical rollouts were then incorporated into policy revision; insertion success subsequently increased from 2/21 in the first generation to 17/21 in the fourth. The frozen final policy retained competence across visual and hardware shifts and was the best performing autonomous policy across six independent ex-vivo porcine specimens. These results show that physical robot interaction can serve as experimental evidence for agent-driven robot policy research.

---

## 10. Dual-Stream Memory for Vision-Language-Action Policies

**Authors:** Yang Wang, Ping Liu, Ruiyu Wang, ..., Lingfeng Zhang, Tao Zhang
**arXiv:** [2610.13262](https://arxiv.org/abs/2610.13262)
**Categories:** Robotics (cs.RO); Computer Vision and Pattern Recognition (cs.CV)

Memory-dependent manipulation requires a policy to track execution state and recover visual evidence that is no longer observable. We propose dual-stream memory for vision-language-action policies, assigning these requirements to complementary representations. A task-agnostic Gated DeltaNet compresses history into one temporal token, supervised by progress prediction and action-conditioned feature reconstruction. A task-conditioned retriever retains frames above a fixed relevance threshold; linear multi-scale fusion encodes each frame into sixteen spatial tokens. We then freeze the temporal compressor and jointly optimize retrieval and policy learning. Across sixteen RoboMME tasks, the complete model achieves 49.22% mean success versus 44.51% for the published FrameSamp+Modul reference, improving fourteen tasks and all four suite means. On four real-robot tasks, mean success reaches 62.5% versus 37.5%, with the largest gains on repeated actions requiring execution-stage discrimination. These results support combining execution context with selective visual access, while failures under cup swaps expose persistent identity tracking as an unresolved requirement.

---

## 11. Evo-World: A Lightweight Vision-Language-Action Model with Future Motion Prediction via Optical-Flow Supervision

**Authors:** Zile Zhong, Yuxin Du, Tao Lin, ..., Binhua Zuo, Bo Zhao
**arXiv:** [2610.12936](https://arxiv.org/abs/2610.12936)
**Categories:** Robotics (cs.RO)

Vision-language-action (VLA) models provide a unified framework for visual understanding, language grounding, and robot control, yet anticipating how the scene will evolve beyond the current observation can provide additional information for control. Action supervision alone does not explicitly encourage such anticipation, while future-image prediction entangles task-relevant motion with largely static appearance. To address these limitations, we introduce Evo-World, a lightweight VLA model that augments policy learning with future motion prediction through optical-flow supervision, thereby providing a task-relevant predictive signal focused on motion rather than appearance. We further design the training procedure to preserve these predictive representations during policy learning, regulating representation diversity while decoupling representation learning from action optimization. Across simulation benchmarks, Evo-World demonstrates strong performance, achieving a tier-averaged success rate of 91.1% on Meta-World MT50 , with a 13.0% relative improvement over the non-predictive baseline. On real-world AgileX robots, Evo-World outperforms the evaluated baselines across single-arm and bimanual manipulation tasks while using only 0.87B parameters and delivering lower GPU memory usage and higher inference efficiency. These results demonstrate that future motion prediction through optical-flow supervision provides an effective and lightweight approach to enhancing the predictive capabilities of VLA models.

---

## 12. Spa-Bench: A Real-Robot Benchmark for Spatial Grounding in Vision-Language-Action Models

**Authors:** Justin Tien-Smith, Matthew Pidden, Rolandos Alexandros Potamias
**arXiv:** [2610.12696](https://arxiv.org/abs/2610.12696)
**Categories:** Robotics (cs.RO)

Vision-language-action models (VLAs) offer a promising route toward general-purpose robotics by transferring semantic knowledge from large-scale vision-language pretraining into language-conditioned control. However, most VLA evaluations emphasize aggregate manipulation success under changes in objects, instructions, or environments, leaving unclear how reliably these policies ground spatial descriptions in the physical scenes where they act. We therefore ask a sharper question: how reliably can current VLAs translate spatial descriptions into appropriate real-robot behavior? To investigate this, we introduce Spa-Bench, a real-robot benchmark that evaluates spatial grounding across six tabletop tasks covering Object State, Relative Size, Referential Description, Relational Placement, Ordinal Position, and Counting. Our primary evaluation compares in-distribution (ID) and out-of-distribution (OOD) spatial configurations while retaining training support for the relevant objects, concepts, and actions, reducing object and motor unfamiliarity as alternative explanations for failure. Four diagnostic conditions further probe physical execution, sensitivity to wording, object-task associations, and recognition that no action is required. We release 4,092 episodes collected on the SO-101 robot arm: 1,200 human-teleoperated demonstrations and 2,892 real-robot evaluation rollouts from five state-of-the-art VLA policies. Across the three fully evaluated policies, success falls from 67.5-73.3% on ID spatial configurations to 40.7-52.0% on OOD spatial configurations, while matched direct instructions improve success by 28.3-40.0 percentage points. These results show that the evaluated VLAs can often execute the required manipulations but lack robust spatial grounding. Project materials, including videos, code, and benchmark data, are available at this https URL.

---
