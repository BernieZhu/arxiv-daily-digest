# arXiv Daily Digest — 2026-10-07

**Mode:** direct
**Categories:** cs.AI, cs.LG, cs.RO, cs.CV
**Keywords:** VLA, RSI, agentic robot, self-improving robot, self-evolving robot, robot harness
**Papers found:** 14

---

## 1. PERSIST: Who-What-When Memory Across Sessions for Full-Duplex Spoken Dialogue

**Authors:** Achira Lin, Siyuan Hou, Wenyi Yu, ..., Mangsuo Zhao, Chao Zhang
**arXiv:** [2610.07725](https://arxiv.org/abs/2610.07725)
**Categories:** Artificial Intelligence (cs.AI)

Modern voice assistants may be shared by multiple users and should be able to answer questions about earlier conversations such as "When did I originally plan to leave?" or adapt their behavior to individual users based on past interactions. This requires more than retrieving a topically similar passage: the assistant must identify the current speaker, recover the relevant past state, and distinguish it from later revisions. We present PERSIST, a persistent memory system for multi-session, multi-speaker spoken dialogue that explicitly models Who, What, and When. PERSIST structures cross-session histories into readable event records and retrieves them with a 3W joint scoring mechanism that combines semantic content, acoustic speaker identity, and temporal state. For real-time full-duplex interaction, PERSIST further reuses intermediate representations from the dialogue backbone, avoiding query-audio re-encoding and reducing retrieval latency from 578.42 ms to 7.03 ms. We also introduce SpokenTrace, a diagnostic benchmark that factorizes evaluation along memory tasks and speaker-query types, exposing failures in recall, speaker attribution, and temporal-state tracking. On SpokenTrace, PERSIST achieves 85.08% end-to-end task accuracy and improves all-support EM@3 from 49.01% with BGE-large to 82.10%.

---

## 2. Adapting Vision-Language-Action Models to Unknown Visual Disruptions During Execution

**Authors:** Ahin Lee, Jinwoo Seo, Youngsoo Jang, Taesik Gong
**arXiv:** [2610.07946](https://arxiv.org/abs/2610.07946)
**Categories:** Robotics (cs.RO); Artificial Intelligence (cs.AI)

Visual disruptions can arise while a robot is executing a task, leaving a vision-language-action (VLA) policy to respond without knowing the disruption type or timing. We introduce Self-supervised Adaptation from Leftover Trajectories (SALT), which uses the leftover trajectory, the unexecuted part of the previous action chunk, as self-supervision for test-time adaptation. Because consecutive chunks overlap in time, the leftover provides a temporally aligned target for the current prediction over the same future control interval. At the onset of a visual shift, the leftover can retain a plan formed before the corruption, so updating the policy toward it anchors the adaptation across the shift (Transition Anchoring). SALT keeps the adapted policy and regenerates the current chunk, whose leftover becomes the target at the next replan, carrying the correction forward along the execution trajectory (Sequential Correction Propagation). Supervision comes entirely from the policy's own predictions, requiring no disruption annotations, expert actions, or target-domain demonstrations, and a lightweight adaptation gate calibrated only on nominal trajectories decides when updates begin. On LIBERO-10, SALT increases average success across five persistent visual corruptions from 43.9% to 53.2% with SmolVLA and from 58.7% to 66.0% with GR00T N1.7, while largely preserving nominal performance. On a real robot, it raises task progress averaged over digital and physical disruptions from 0.49 to 0.61.

---

## 3. Seeing the Invisible: Physics-Guided Visual Prompting for Temperature- and Radiation-Aware VLA Navigation

**Authors:** Hojoon Son, Fan Zhang
**arXiv:** [2610.07558](https://arxiv.org/abs/2610.07558)
**Categories:** Robotics (cs.RO); Artificial Intelligence (cs.AI); Machine Learning (cs.LG)

Vision-Language-Action (VLA) models have become a major paradigm for Vision-and-Language Navigation (VLN). However, in safety-critical facilities, invisible risks such as radiation or temperature spikes cannot be detected by an RGB camera, and handling each risk is expensive, requiring a new encoder, new data, and model retraining. We propose Physics-Guided Visual Prompting (PG-VP), a plug-and-play multimodal perception module that instead reuses what a frozen VLA model already does well: avoiding visible obstacles. Given a proximal radiation or thermal source, PG-VP performs a physics-guided risk assessment to determine the avoidance direction and overlays a corresponding virtual obstacle that moves across consecutive frames (Dynamic Visual Prompting). The navigation policy then naturally detours around this invisible hazard. The identical virtual obstacle is used regardless of hazard type, so the visual prompting pattern remains fixed as sensors are added. When no hazard is detected, nothing is rendered, and the policy behaves exactly as it would without PG-VP. We evaluate PG-VP on OmniNav using the val-unseen splits of R2R-CE and RxR-CE, where it guides the policy toward intended low-risk actions in 84.9% and 83.2% of cases, at a cost of 6.8 and 7.9 percentage points in navigation success rate. We further test it with distinct scenarios on a real robot in the presence of actual thermal and radiation sources, all without any retraining. The real test shows that PG-VP effectively avoids these invisible hazards, improving worst-10% average trajectory safety by 63.45% and 32.59% against thermal and radiation sources, respectively.

---

## 4. Beyond Successor Accuracy: State Retention for Recursive Self-Improvement in Recommendation

**Authors:** Jinfeng Xu, Zheyu Chen, Ziyue Peng, ..., Shujie Li, Edith Ngai
**arXiv:** [2610.07105](https://arxiv.org/abs/2610.07105)
**Categories:** Information Retrieval (cs.IR); Artificial Intelligence (cs.AI)

Recommendation recursive self-improvement (Rec-RSI) feeds recommender outputs into subsequent training. Evaluating each round solely through its latest model assumes that the successor consolidates the update, although pre- and post-update models may retain complementary ranking decisions. We term this \emph{distributed progress} and quantify it using cross-generation advantage (CGA), a marginally matched contrast between cross- and within-generation model pairs. A rank-separation statistic, label-free at selection time, predicts which family to retain. Across four datasets and three sequential recommendation encoders, the preferred retention regime varies by architecture: cross-generation pairing benefits GRU4Rec and SASRec, whereas FMLP initially favors within-generation pairing and shifts toward cross-generation pairing after a second update. Rank separation selects the stronger family in 12/12 first-update and 5/6 second-update dataset-encoder settings; on held-out tests, the selected family outperforms the direct successor in 34/36 trajectories. Five transfer mechanisms do not consistently reproduce these gains in one model. These findings establish state retention as a distinct Rec-RSI problem: progress may reside in relations between generations as well as in the latest model. Code is available at \href{this https URL}{this https URL}.

---

## 5. WareFly-VLA: A Vision-Language-Action Framework for UAV Navigation and Human Tracking in Smart Warehouses

**Authors:** Thinh D. Le, Son T. Nguyen, Duong Q. Nguyen, ..., Ngo Anh Vien, H. Nguyen-Xuan
**arXiv:** [2610.08526](https://arxiv.org/abs/2610.08526)
**Categories:** Robotics (cs.RO); Computer Vision and Pattern Recognition (cs.CV)

Vision-Language-Action (VLA) models have achieved impressive results in robotic manipulation and ground-mobile navigation, yet language-conditioned control of unmanned aerial vehicles (UAVs) in smart warehouses remains largely unexplored, hindered by the lack of benchmarks that jointly provide continuous low-level flight actions, fine-grained natural-language target descriptions, and realistic industrial environments. This paper introduces WareFly-VLA, a photorealistic UAV VLA framework and dataset for language-guided human search, localization, and tracking in warehouse environments. It contains 507 human-teleoperated flight episodes and 8,504 high-resolution RGB transitions collected in NVIDIA Isaac Sim, each paired with a human-written appearance description of the target worker and a synchronized four-degree-of-freedom control command. Two aerial tasks are covered: target approach and person following, under occlusion, long-range search, altitude variation, and clutter. A unified benchmark of four open-source VLA architectures (SmolVLA, GR00T N1.7, pi_0 and OpenVLA) is established under a leakage-free episode-level protocol at two control rates. The results show that language-conditioned aerial control in warehouses is far from solved: performance drops substantially under strict generalization settings, continuous action modeling consistently outperforms discrete action tokenization, only the forward channel is reliably learnable from a single frame, and current foundation-model interfaces transfer poorly from ground and humanoid embodiments to aerial platforms. The synchronized video, language, action, pose, and difficulty annotations further support world-model research. The dataset, baselines, and evaluation protocol are released to support language-grounded aerial autonomy in smart warehouses.

---

## 6. ActTune: Action-Aware Precision and GPU Operating-Point Adaptation for Energy-Efficient Vision-Language-Action Inference

**Authors:** Zou Qingyun, Bin Gao, Wenju Zhao, ..., Bingsheng He, Tulika Mitra
**arXiv:** [2610.08444](https://arxiv.org/abs/2610.08444)
**Categories:** Robotics (cs.RO); Hardware Architecture (cs.AR)

Vision-language-action (VLA) policies repeatedly invoke inference to control robots, making graphics processing unit (GPU) energy a recurring cost of task execution. Reducing energy per inference call, however, may not reduce energy per successful task if numerical errors increase failures or slower inference prolongs execution. We therefore target GPU energy per successful task while preserving task success and keeping the inference-latency increase within 10\%. Our approach builds on two observations: quantization sensitivity varies across action classes, model layers, and weights versus activations; and numerical precision changes the workload, shifting favorable GPU operating points. We introduce ActTune, an action-aware framework that connects layer-wise precision allocation with workload-dependent GPU operating-point selection over requested frequency--power-cap pairs. A lightweight decision tree learns its splits and leaf precision configurations directly from configuration action errors, then selects precision before each policy call. The controller forecasts the next workload and applies the selected GPU operating point asynchronously using a lookup table calibrated under a latency budget. A shared resident quantized weight bank enables configuration switching without weight reconstruction or additional policy evaluations. On LIBERO, a benchmark for lifelong robot learning, ActTune improves mean task success by up to 2.3\% relative to state of the art. Relative to the original BF16 implementations, it delivers up to $2.02\times$ faster inference and, with GPU operating-point adaptation, reduces energy per successful task by up to 76.8\%.

---

## 7. MIM-VLA: Learning Physical Interaction Representations from Gripper Motor Feedback

**Authors:** Jaeyoung Lee, Jiyeon Koo, Taehwa Kim, Yerin Cha, Andrew Jaeyong Choi
**arXiv:** [2610.08425](https://arxiv.org/abs/2610.08425)
**Categories:** Robotics (cs.RO)

Vision-language-action (VLA) policies infer grasp actions primarily from visual observations and robot state, but do not explicitly represent the physical response observed after contact. We present MIM-VLA, a motor-feedback-based architecture that encodes recent gripper current, position, velocity, and signal validity as a 128-dimensional interaction token. A motor-only Motor Interaction Module (MIM) is pretrained with human-reviewed contact and interaction-phase labels and then conditions only the gripper-action pathway of SmolVLA; arm actions and the position-control interface remain unchanged. The same token supports the MEM selector VLM that compares candidate interactions and produces evidence-conditioned selections and explanations. We evaluate MIM-VLA in three real-world settings: comparing the interaction resistance of visually different objects, disambiguating visually similar real and replica objects through active probing, and gently grasping fragile objects, including held-out instances. Across 13 object pairs, MIM-VLA selects the higher-resistance object in 75.0% of trials, compared with 48.8% for the SmolVLA baseline. For the evaluated tasks, the approach uses motor feedback already available from the gripper and does not require an additional tactile array, force-torque sensor, calibrated force estimate, or direct current control.

---

## 8. ViDAL: A Visual Dynamics-Grounded Action Latent Space for Vision-Language-Action Models

**Authors:** Yuan Xu, Yixiang Chen, Qisen Ma, ..., Yan Huang, Liang Wang
**arXiv:** [2610.08150](https://arxiv.org/abs/2610.08150)
**Categories:** Robotics (cs.RO)

Vision-Language-Action (VLA) models have become a central paradigm for robot policy learning, which predict actions in three forms: raw action chunks, discrete action tokens, or continuous action latents. However, existing action representations primarily model action trajectories, with limited consideration of the visual dynamics induced by these actions. We introduce ViDAL, a Visual Dynamics-grounded Action Latent Space that anchors continuous action latents in the future visual dynamics of the scene. Specifically, ViDAL learns action latent space by training an Action Variational Autoencoder (Action VAE) to reconstruct action chunks while aligning its latent with future scene dynamics. When integrated into downstream robot policies, the proposed Action VAE serves as a plug-in action interface compatible with multiple VLA architectures and enables optional future-video prediction as an additional capability. Empirically, ViDAL outperforms competitive baselines on LIBERO with 98.1% average success, improves a multi-task $\pi_{0.5}$ policy on RoboTwin 2.0 from 54.3% to 65.5% (Clean) and from 33.2% to 43.1% (Random) success rates over 50 dual-arm tasks, and yields 20.0% and 23.4% absolute success-rate gains on real-world single-arm Franka and dual-arm ARX robot platforms.

---

## 9. VLA-ACL: Action-Consistent Visual Token Pruning for Efficient Vision-Language-Action Models

**Authors:** Owen Du, Yang Yue, Jie Zhang, ..., Chi Bene Chen, Gao Huang
**arXiv:** [2610.08133](https://arxiv.org/abs/2610.08133)
**Categories:** Robotics (cs.RO); Computer Vision and Pattern Recognition (cs.CV)

Vision-Language-Action (VLA) models achieve strong robotic manipulation performance but incur high computational costs from processing long token sequences at every control step, limiting real-time deployment. Visual token pruning offers a direct solution, as visual patches dominate the input sequence and contain considerable redundancy. Existing approaches, however, either rely on indirect training-free heuristics, such as attention scores and motion thresholds, or require costly fine-tuning of the base VLA model. We introduce VLA-ACL (Action Consistency Learning), which learns a lightweight visual token pruning policy through action-level supervision while keeping the base VLA model entirely frozen. The training objective encourages actions produced from pruned visual contexts to remain consistent with the full-context teacher, with ground-truth actions as auxiliary supervision. This directly ties token selection to its effect on the downstream control output. Experiments on LIBERO and real-world manipulation tasks show that VLA-ACL prunes up to 87.5% of visual tokens while retaining competitive performance, reduces computation by up to 75%, and achieves a 1.5x inference speedup. These results establish a stronger performance-efficiency trade-off than existing frozen-VLA pruning methods and demonstrate the value of action-level supervision for visual token selection. Code is available at this https URL.

---

## 10. StairVLA: Stage-Aware Hierarchical Action Generation for Vision-Language-Action Models

**Authors:** Shangyuan Yuan, Xinda Qi, Yujiang Pu, Wenliang Guo, Xiaobo Tan
**arXiv:** [2610.07756](https://arxiv.org/abs/2610.07756)
**Categories:** Robotics (cs.RO)

Vision-language-action (VLA) models increasingly rely on diffusion- or flow-matching-based action heads to generate continuous robot actions. These action heads typically process the denoising trajectory in a largely uniform manner. However, we observe that the conditioning focus naturally shifts across denoising stages: early stages combine language instructions and visual observations to establish a coarse action trajectory, whereas later stages place greater emphasis on current visual observations for action alignment. Based on this insight, we introduce StairVLA, a stage-aware hierarchical action generation framework that uses partially denoised actions as a natural interface between coarse long-horizon action generation and local refinement. A high-level VLA performs early denoising to produce a reusable long-horizon partially denoised action trajectory, while a lightweight refiner operates at a higher frequency to refine local action chunks using the latest observations. This design amortizes expensive high-level VLA computation while preserving frequent closed-loop correction. On LIBERO, our GR00T-style instantiation improves average success from 96.5% to 97.8% while reducing amortized inference latency from 115.0 ms to 44.2 ms per action chunk. More broadly, across two VLA backbones, simulation benchmarks, and real-robot tasks, StairVLA consistently reduces inference cost while maintaining strong task performance.

---

## 11. ProactiveVLA: Augmenting Embodied Memory through Proactive Environment Exploration

**Authors:** Shizuo Tian, Haodong Luo, Yutong Li, ..., Yunxin Liu, Yuanchun Li
**arXiv:** [2610.06999](https://arxiv.org/abs/2610.06999)
**Categories:** Robotics (cs.RO)

Rapid adaptation to a new environment requires a robot to acquire useful knowledge about local objects, states, and interactions from limited experience. Systems that combine a reasoning agent with a frozen vision-language-action model (VLA) can adapt through execution feedback and memory, making the choice of experience central to their effectiveness. Repeated practice of a target task may refine a familiar solution while leaving other interactions relevant to changed conditions untested. We introduce ProactiveVLA, which uses proactive environment exploration to acquire reusable knowledge for deployment-time adaptation. After completing an initial task, the agent allocates the remaining interaction budget to self-proposed goals covering object affordances, state-changing interactions, and compositions of interactions. It verifies execution outcomes and consolidates both task-directed and exploratory experience into memory that guides subsequent planning and control. ProactiveVLA outperforms the baselines under the same turn budget on LIBERO-Pro and RoboCasa365 Composite-Seen. On LIBERO-Pro Goal-T, with at most one VLA primitive invocation allowed during evaluation, ProactiveVLA completes 48% of instances, compared with 19% for the state-of-the-art task-refinement baseline.

---

## 12. SWAP: Stepwise Action Policy Routing for Vision-Language-Action Models

**Authors:** Mousumi Das, Aditeya Prajapati, Abrar Anwar, Jesse Thomason
**arXiv:** [2610.06926](https://arxiv.org/abs/2610.06926)
**Categories:** Robotics (cs.RO)

Robot manipulation systems using Vision-Language-Action (VLA) model backbones typically use just one VLA for task execution. However, individual VLAs do not perform well across different task states and environments. We introduce a framework for dynamically composing multiple VLA policies during execution: StepWise Action Policy Routing (SWAP). SWAP formulates policy routing as an offline reinforcement learning problem, learning a routing critic that selects the most appropriate policy at each decision step given the current observation. SWAP enables robots to select new policies to execute online rather than committing to a single policy for the duration of an episode. We evaluate SWAP on both real-world DROID manipulation tasks and LIBERO simulation experiments. SWAP improves over fixed-policy execution and routing baselines, giving absolute improvements in real-world task success up to 33% while reducing successful trajectory robot action step length by 28.3%.

---

## 13. Does a Learned Corrector Beat a Simple Retreat? Evidence from a Frozen VLA

**Authors:** Chenchao Sheng, Zhuang Jiang, Liuhaichen Yang, Ningwei Bai, Zezhi Tang
**arXiv:** [2610.06921](https://arxiv.org/abs/2610.06921)
**Categories:** Robotics (cs.RO)

Before deploying runtime recovery for a frozen vision-language-action (VLA) policy, one must establish that an intervention improves success beyond ordinary run-to-run variation and that its complexity adds value over a simple action. We evaluate these questions on frozen $\pi_{0.5}$ across four RoboTwin tasks. For each test seed, we pair rollouts with and without correction and include a same-seed base-policy re-run as a placebo. Seed-cluster intervals and prespecified comparison rules assess net gains against stochastic outcome changes. Across 3,888 paired episodes, the full pipeline raises success on beat_allowbreak block_allowbreak hammer by $+13.5$\,pp (95\% interval $[+9.4,+17.7]$), with no detectable gain on the other three tasks at the deployed weight. Among failed base episodes on the responsive task, $43.2\%$ succeed on a plain re-run, compared with $63.5\%$ after correction; many nominal rescues therefore reflect the base policy's own variability. A fixed-time trigger and scripted return to an earlier joint configuration produce a net gain with no detected difference from the learned pipeline across two rounds, although our prespecified equivalence criterion is not met consistently. Pausing and a constant-action control do not yield comparable gains. On this benchmark, the decision to intervene depends strongly on the task, and a paired placebo plus a simple retreat baseline are needed to establish what learned correction contributes.

---

## 14. EmbodiedSmith: Scaling Embodied Data through Recursive Self-Improvement Flywheel in Simulation

**Authors:** Yikai Qin, Yifei Deng, Mingjian Liang, ..., Pengwei Wang, Haoang Li
**arXiv:** [2610.07969](https://arxiv.org/abs/2610.07969)
**Categories:** Computer Vision and Pattern Recognition (cs.CV); Robotics (cs.RO)

Scaling robotic foundation models requires diverse training data and reliable evaluation environments. Simulation offers a scalable solution, yet existing generation pipelines remain constrained by predefined assets and skills, a disconnect between scene generation and task generation, and limited support for complex embodiments and physics. We introduce EmbodiedSmith, a framework for scalable embodied data generation through recursive self-improvement (RSI). EmbodiedSmith unifies asset, scene, and task generation in a pipeline that supports autonomous creation and language-driven customization. Its core is an agentic refinement loop: scene generation anticipates downstream task requirements, while task generation guides targeted scene edits, allowing scenes and tasks to iteratively improve one another. This joint refinement improves task generation success, including for long-horizon tasks. The framework further supports mobile manipulators, humanoids, and dexterous hands, as well as interactions involving deformable objects and fluids, broadening the range of behaviors and physical phenomena represented in generated data. Together, these capabilities provide a flexible simulation engine for both robot pretraining and evaluation. Extensive experiments validate the quality, diversity, and generation efficiency of the resulting data, while downstream policy experiments demonstrate that increased data diversity improves generalization.

---
