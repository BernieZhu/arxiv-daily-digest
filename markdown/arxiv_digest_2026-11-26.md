# arXiv Daily Digest — 2026-11-26

**Mode:** direct
**Categories:** cs.AI, cs.LG, cs.RO, cs.CV
**Keywords:** VLA, RSI, RUA, agentic robot, self-improving robot, self-evolving robot, robot harness
**Papers found:** 20

---

## 1. A Failure-Driven Data Flywheel for Post-Training Vision-Language-Action Models

**Authors:** Yuhao Luo, Zihao Sheng, Zilin Huang, ..., Shuai Wang, Sikai Chen
**arXiv:** [2611.34698](https://arxiv.org/abs/2611.34698)
**Categories:** Artificial Intelligence (cs.AI)

Pretrained vision-language-action (VLA) models rarely satisfy all behavioral requirements of a new platform, and teams without a large deployed fleet lack the data to address the resulting failures. We propose a failure-driven data flywheel for post-training such models. It constructs target scenarios absent from the available data by inserting task-relevant entities into reconstructed real-world scenes, and evaluates the model against each behavioral requirement of the target task. Failure rates form a failure map across task conditions and difficulty levels, which is re-evaluated after each round and assigns larger data generation quotas to conditions where the model still fails. We instantiate the framework in autonomous driving for occluded-pedestrian emergence and yielding at stop-sign-controlled intersections, and evaluate it on two VLA models and one non-VLA planner in simulation and on a real vehicle. For occluded-pedestrian emergence, five rounds of post-training improve the critical-phase collision-free rate on the sealed test set from 0.261 to 0.579 for AutoVLA and from 0.390 to 0.765 for ReCogDrive, while the unnecessary braking rate in paired control scenarios never exceeds 0.013. On a full-scale vehicle without real-world training, post-trained ReCogDrive achieves 4 of 5 safe passages, versus 1 of 5 for the base model. Fine-grained evaluation reveals a pattern obscured by the collision-free rate alone: both VLA models learn anticipatory deceleration before reaching the occluding vehicle, while braking after pedestrian emergence remains limited. For stop-sign yielding, the stop-before-line rate rises from 0.100 to 0.897 for AutoVLA and from 0.000 to 0.667 for ReCogDrive. With sequential training from the pedestrian-capability models, it reaches 0.599 and 0.358, respectively, while the pedestrian collision-free rate decreases by at most 0.032.

---

## 2. Keep or Roll Back? Out-of-Loop Judges for Self-Improving VLA and End-to-End Embodied Policies

**Authors:** Zilin Huang, Zhengyang Wan, Kangan Qian, Zihao Sheng, Sikai Chen
**arXiv:** [2611.33794](https://arxiv.org/abs/2611.33794)
**Categories:** Artificial Intelligence (cs.AI); Computer Vision and Pattern Recognition (cs.CV); Robotics (cs.RO)

Self-improvement is now a practical recipe for embodied policies: a policy collects experience, is retrained, and is kept when a judge rates it higher. However, the judge is usually trained or chosen inside the same loop, so its evidence is not independent of the policy. We introduce SealedLoop, an evaluation framework that adds a sealed judge: an evaluator outside the loop that the improver cannot see or optimize against. A new policy is kept only when a sequential test on the sealed judge confirms the gain, with a bounded probability of keeping a worse one. Running the same loop under each judge, we separate two sources of a false gain, which we call judge error (the loop's judge is wrong on its own data) and transfer gap (a real gain there does not carry over to unseen conditions). We evaluate on LIBERO manipulation, NAVSIM driving, and a full-scale real vehicle. In manipulation, a success classifier accepted 65 of 196 failures in one generation. In driving, policies that gain on the loop's own frames lose in an unseen city, so even an exact in-loop judge would keep 8/15 of them. When the sealed test decides, a driving loop built to improve ends with a better policy than under its own critic (0.674 against 0.649 PDMS, from 0.638), and on driving pairs with known sealed gain the test accepted 11 of 12 real gains and none of 59 losses. In a real-world field experiment on a published improvement step, the reinforced version drove further into a curve than the version it started from in all 6 blind pairs, though neither completed it. These results show that evidence from inside the loop, however accurate, is not enough to decide whether a policy has improved. SealedLoop offers a foundation for trustworthy self-improvement of embodied policies, in which progress is judged by evidence the improving system cannot influence.

---

## 3. RePace: Reasoning about Demonstration Speedup for Faster Vision-Language-Action Policies

**Authors:** Insup Lee, Hojin Jeon, Sunguk Shin, ..., Jinwoo Shin, Dongsu Han
**arXiv:** [2611.34864](https://arxiv.org/abs/2611.34864)
**Categories:** Robotics (cs.RO); Artificial Intelligence (cs.AI)

Since vision-language-action (VLA) policies can inherit the slow pace of human demonstrations, accelerating these demonstrations before fine-tuning can lead to faster VLA policies without an additional speed-selection module at deployment. Several offline speedup methods have focused on identifying segments that require less precision and assigning predefined speedup factors to the segments. However, even within a single segment, a speedup factor suitable for steady motion may be too high when precise alignment is required. To this end, this paper presents RePace, an offline reasoning framework that determines how much to accelerate each part of a demonstration. For the same recorded movement, RePace measures how much each candidate speedup factor shortens the sequence and compares the resulting observation-action pairs used for training. Given the task instruction, a pretrained language model uses the visual context and original motion of successive windows to interpret these candidate retiming effects and select a speedup profile for the complete episode. Experimental results demonstrate that RePace outperforms the baselines in overall task execution efficiency on both LIBERO and RoboCasa-Kitchen. On all three tasks with a gripper-equipped Franka Research 3 arm, RePace matches or exceeds the acceleration baselines in success rate and completes successful trials faster.

---

## 4. Aegis-VLA: Reliability-Gated Action Refinement via a Trajectory World Model for Dynamic Object Manipulation

**Authors:** Lennox Wei, Jiaqi Yao, Shixin Sun, ..., Shaohui Liu, Wangmeng Zuo
**arXiv:** [2611.33993](https://arxiv.org/abs/2611.33993)
**Categories:** Robotics (cs.RO); Artificial Intelligence (cs.AI)

Dynamic object manipulation requires maintaining spatial and temporal alignment with targets that continue to move during inference and execution. Although future prediction can inform action correction, an accurate forecast does not establish whether modifying an existing action would be beneficial. We present Aegis-VLA, a world-model-guided vision-language-action (VLA) framework that generates predictive action corrections and separately determines whether and how strongly to apply them. A Trajectory World Model combines kinematic extrapolation with learned residual dynamics to predict object motion and estimate positional uncertainty. Discrepancy-Guided Action Refinement uses differences between history-only and base-action-conditioned end-effector forecasts to propose bounded arm corrections. A Reliability Gate learns when to admit corrections based on demonstration-relative improvements over base actions, and regulates their application during inference using predictive uncertainty and anticipated object--end-effector proximity. Rejected corrections preserve the corresponding base actions. Aegis-VLA introduces only approximately 2.45M trainable parameters. On the simulated Dynamic Object Manipulation (DOM) benchmark, Aegis-VLA achieves 56.72\% success over 1,800 evaluation trials, exceeding our reproduced DynamicVLA baseline of 45.44\% by 11.28 percentage points.

---

## 5. Best-of-$N$ Test-Time Steering Can Lead to Reward Hacking in Vision-Language-Action Models

**Authors:** Vanshaj Khattar, Jing Liu, Toshiaki Koike-Akino, Ming Jin, Ye Wang
**arXiv:** [2611.33398](https://arxiv.org/abs/2611.33398)
**Categories:** Robotics (cs.RO); Artificial Intelligence (cs.AI); Machine Learning (cs.LG)

Vision-language-action (VLA) models have shown promise for general-purpose robotic manipulation, but adapting to changing environmental conditions still remains challenging. Recent test-time steering methods have shown promise in enabling adaptive VLA policies by utilizing additional computation during deployment. In this paper, we consider best-of-$N$ test-time steering for VLA models, where multiple action candidates are sampled from a fixed policy and a verifier is used to select the best one during deployment. We show that increasing $N$ does not always improve performance when the verifier is inaccurate, and can favor candidates whose scores exploit prediction errors, a form of reward hacking. We study this effect on 60 LIBERO-Safety task-level cases using a $\pi_{0.5}$ policy, with ten repetitions per case. We introduce controlled errors in a MuJoCo trajectory verifier and show that as $N$ increases, selected candidate rewards diverge from the accurate verifier rewards, leading to reward hacking. We also show that verifier calibration and softmax-based candidate selection can mitigate reward hacking in some settings.

---

## 6. Cairn: Object-Centric 3D Trajectory Priors for Steering Frozen VLAs

**Authors:** Agelos Kratimenos, Kostas Daniilidis, Evangelos Chatzipantazis
**arXiv:** [2611.34914](https://arxiv.org/abs/2611.34914)
**Categories:** Robotics (cs.RO); Computer Vision and Pattern Recognition (cs.CV)

Vision-language-action models (VLAs) are capable low-level controllers, but they tie where objects go to the layouts they were trained on: when objects are moved or obstacles block the way, they carry them to the wrong place or into collisions. Fine-tuning on new layouts needs robot data for each one and erodes skills the model already has. We introduce Cairn, which keeps the VLA frozen and steers it at test time along learned 3D trajectories of the object in its gripper. A small prior reads point clouds of the scene and the held object, along with its pose when grasped and the instruction, and samples SE(3) trajectories up to its release that lead it around obstacles and turn it to fit through gaps. The prior and the VLA form the two levels of a hierarchical planner in which feedback runs both ways: the VLA's intended motion chooses and reshapes the trajectories, and the chosen one guides the VLA's denoising. Its predicted actions, mapped to the held object's poses through the grasp, are pulled toward the next waypoint, while the VLA's weights stay untouched. Across 1,941 held-out LIBERO scenes with displaced objects and obstacles, Cairn raises the success rate of a frozen {\pi}0.5 from 24.5% to 95.1%, above that of a {\pi}0.5 fine-tuned on our training layouts, without hurting standard LIBERO. On the third-party LIBERO-PRO benchmark, it raises success from 27.3% to 38.0%, and from 54.4% to 81.1% on the episodes it steers. On a real Franka, with a prior trained purely in simulation, it guides the frozen DROID {\pi}0.5 around an obstacle and to a placement at the limit of the arm's reach, where it otherwise fails. All code, models and data will be made public.

---

## 7. Toward Agentic Robotics: A Large-Scale Study of Harness Design for Robot-Use Agents

**Authors:** Yuxiang Lai, Jike Zhong, Yu-Jhe Li, ..., Zheda Mai, Ruixi Fan
**arXiv:** [2611.34778](https://arxiv.org/abs/2611.34778)
**Categories:** Robotics (cs.RO)

Recent vision-language models (VLMs) can act as robot-use agents that understand diverse scenes and control robots through policy code and tools. However, they predict 3D gripper poses poorly even with extended reasoning, struggling with precise manipulation. Vision-language-action (VLA) and world-action (WAM) models are the opposite: they execute fast, smooth control on trained tasks, yet fail under domain shifts or when tasks require long-horizon memory and reasoning. Agentic robots therefore combine VLM reasoning and perception with precise VLA/WAM control through a policy harness. Yet harness design spans thousands of configurations, shifting success by tens of points with the same models. Moreover, testing even one design takes thousands of rollouts at high API and GPU cost, so prior works often commit to a single design chosen from few alternatives. To guide harness design, we evaluate over 470,000 rollouts across eight simulation benchmarks, six VLMs, and 15 VLA/WAM checkpoints. Seven controlled studies show effective harnesses must adapt to both VLM and VLA/WAM capabilities. Our findings specify what structure the VLM's policy code needs, where VLA manipulation needs help from tools and policy code, and when to involve the VLM at test time. The reference recipe X-Harness shows that these findings compose without weight updates, lifting base policies up to $+42.8$ points across memory, reasoning, and domain shifts.

---

## 8. M$^{2}$AdaptVLA: Multimodal Memory-Augmented Vision-Language-Action Model with Predictive Test-Time Adaptation

**Authors:** Liufan Tan, Tong Wang, Yuehao Yin, ..., Ruyi Gan, Hao Wang
**arXiv:** [2611.34560](https://arxiv.org/abs/2611.34560)
**Categories:** Robotics (cs.RO); Computer Vision and Pattern Recognition (cs.CV)

Effective robotic manipulation calls for multimodal memory and rapid adaptation to shifts in contact dynamics. However, many existing policies, which retain either visual or wrench history, may miss key cues from the other modality. Moreover, even with wrench memory, fixed policies can struggle when contact conditions shift at deployment. To this end, we introduce M$^{2}$AdaptVLA, a vision-language-action model that integrates visual and wrench memories with predictive test-time adaptation. For visual memory, the model uses test-time training (TTT) to encode observation history in fast weights. Each entry in the bounded TTT bank combines the corresponding frame's features with a readout from these weights, preserving cues that predate the oldest retained frame. For wrench memory, a context gate controls how much the action expert draws on wrench history as it jointly denoises future actions and wrenches. For predictive test-time adaptation, the auxiliary wrench prediction loss also provides online self-supervision. Using measured wrenches as targets, we update low-rank policy adapters by backpropagating only through the final denoising step. Real-world experiments show that the TTT bank outperforms visual memory baselines on progress tracking, scene recall, and demonstration following. On contact-sensitive tasks, the context gate yields higher success rates than direct injection or gated cross-attention. Predictive test-time adaptation improves robustness to shifts in contact dynamics. On eight tasks requiring visual and wrench memory, M$^{2}$AdaptVLA achieves a mean success rate of 82.71%, a 31.46% absolute gain over the strongest baseline. The project page is available at this https URL.

---

## 9. Beyond Natural-Language Instructions: Temporal Logic as a Task Language for VLA Models with Visual-Logical Fusion

**Authors:** Zezhi Liu, Jingwen Sun, Hongjin Chen, ..., Xin Jin, Zhibo Chen
**arXiv:** [2611.34352](https://arxiv.org/abs/2611.34352)
**Categories:** Robotics (cs.RO)

Robotic tasks combine object relations, logical dependencies, and temporal requirements, which robot planning and industrial control commonly specify in temporal logic (TL). We introduce TL-VLA, a vision--language--action framework that replaces natural-language task instructions with temporal logic, making this spatiotemporal structure explicit. A typed graph encoder and visual--logical fusion condition continuous actions on the task specification and the current observations. To prepare a general vision--language backbone for this interface, we develop TL-aware robot pretraining with separate semantic and structural readouts: a frozen language teacher aligns task semantics, the structural readout encodes TL syntax to support complex, long-horizon tasks, and autoregressive action prediction connects the graph representation to robot behavior. Downstream policies inherit the pretrained backbone and TL encoder and learn new fusion and action modules. On CALVIN ABC$\rightarrow$D, our TL-aware initializer reaches \textbf{3.800} average chain length and \textbf{62.3\%} five-task success, compared with 3.578 and 54.5\% for a FAST initializer pretrained on the same data and 3.485 average chain length for a Qwen+NL baseline. On LIBERO-10, TL-aware initialization improves success from \textbf{91.2\% to 95.8\%}. On LIBERO-Mem, our policy reaches \textbf{65.0\%} success without observation history, compared with 45.0\% for a Qwen+NL reference. On held-out Panda planning specifications, it reaches \textbf{59.6\%} at Success@256 over three generation seeds, versus 48.4\% for Qwen+TL and 37.0\% for Qwen+NL. These results support explicit logical task conditioning and transferable TL-aware representations for robot action learning.

---

## 10. DataForgeVLA: Fully Synthetic Manipulation Demonstrations for Vision-Language-Action Training

**Authors:** Sergei Kurchev, Iaroslav Kolomiets, Filipp Maksimov, ..., Artem Lykov, Dzmitry Tsetserukou
**arXiv:** [2611.34287](https://arxiv.org/abs/2611.34287)
**Categories:** Robotics (cs.RO)

We present a dataset of 340 fully synthetic manipulation demonstrations generated from real seed data for Vision-Language-Action (VLA) training. The corpus contains 32,340 frames with synchronized RGB and actions across eight object categories, represented as LeRobot v2.1 episodes with H.264 video, per-frame robot states and pose-valued action labels, language task annotations, summary statistics and quality decisions. Each synthetic demonstration is produced without additional teleoperation: a LoRA-fine-tuned Cosmos-3 model generates a manipulation video, and RoboHaMeR recovers the corresponding robot trajectory from RGB. Quality screening accepted 300 of 340 episodes for policy fine-tuning. As preliminary evidence of feasibility, a pretrained GR00T N1.6 policy fine-tuned exclusively on the 300 accepted episodes reaches 16/20 (80%) real-world pick-and-place success on the Oreo-package task. A policy fine-tuned on 105 real teleoperated episodes achieved 18/20 (90%) under the same protocol. These results are based on one object and 20 trials per policy and are therefore reported as preliminary evidence rather than a general performance claim.

---

## 11. Escapingthe instruction blackhole of vision-language-action policies via optimal-transport wormholes

**Authors:** Xuetao Li, Chen Liu, Jing Wu, Sheng Liu, Miao Li
**arXiv:** [2611.34280](https://arxiv.org/abs/2611.34280)
**Categories:** Robotics (cs.RO)

Vision-language-action (VLA) policies are trained to follow a fixed instruction, yet people change their minds while the robot acts. We identify the instruction black hole: once a VLA policy commits to a task, new instructions are absorbed and the robot completes the old task or freezes. We quantify it with a transmission ratio and an event horizon and prove it is a blind spot of static imitation, which cannot distinguish a policy that listens from a deaf one once the execution state reveals the task. We propose Wormhole, a training-free plug-in that relocates the robot instead of re-instructing it: optimal transport selects an approach-phase state of the new task, a rate-limited traversal carries the robot there, and the unmodified policy takes over. On LIBERO,Wormhole raises committed-switch success of pi to and pi0.5 from at most 1.2% to 93.1%, matching or exceeding scripted retreat-and-restart with one fifth of its action discontinuity.

---

## 12. SEEK: Self-Evolution through Execution Knowledge for Agentic Robot Manipulation

**Authors:** Zeyang Guan, Qihao Zhao, Rui Gong, ..., Scarlett Li, Kim-Hui Yap
**arXiv:** [2611.33915](https://arxiv.org/abs/2611.33915)
**Categories:** Robotics (cs.RO); Computer Vision and Pattern Recognition (cs.CV)

General-purpose multimodal foundation models enable robots to adapt during deployment from observations and execution feedback, without task-specific demonstrations or training. However, the robot retains what it learns only in the model's working context. Once the task ends, it loses this execution knowledge, such as how to carry a bowl between two grippers. On the next attempt at the task, the robot may take just as long and repeat the same mistakes. To avoid this repetition, robots must retain execution knowledge across attempts. Yet replaying past actions is insufficient, because their effects depend on the current conditions. Procedures that determine actions from the current scene address this, but when they meet conditions that earlier attempts did not cover, revising them requires the measured effects of earlier actions. We therefore propose SEEK, an agentic framework that retains both, enabling robots to improve across attempts while keeping the underlying model fixed. To adapt retained knowledge to the current scene, SEEK adopts a Self-Evolving Programmatic Policy (SEPP) that encodes manipulation as executable procedures and determines each action from current observations. As the robot executes these procedures, SEEK records the measured effects of its actions, including those from failed attempts, in a Persistent Action-Effect Bank (PAEB). Where a retained procedure applies, it acts without a model request; where it meets a condition it does not cover, this evidence guides its revision. On RoboDojo, knowledge retained over ten attempts raises SEEK's average task score from 27.0 to 54.4 and its success rate from 19.7% to 48.0% across all 42 tasks. On 34 of these tasks with GPT-6.2 Astra, SEEK reaches 80.1 after five attempts, against 49.6 for the same model acting directly, and uses 77.6% fewer model requests. this https URL

---

## 13. Integration of Vision-Language-Action Control for Autonomous Forklift Unloading with Limited Real-World Data

**Authors:** Koshi Oishi, Seigo Ito
**arXiv:** [2611.33880](https://arxiv.org/abs/2611.33880)
**Categories:** Robotics (cs.RO)

Forklifts play a critical role in warehousing and distribution, but existing automation systems remain limited in handling complex tasks that require sequential decision-making. Recently, vision--language--action (VLA) models have emerged as a promising approach for multi-step decision-making by directly generating control actions from visual observations and language prompts. Although VLA-based control has been extensively researched for manipulators, to the best of our knowledge, its application to forklifts remains unexplored. Therefore, this study demonstrates the integration of VLA control for an autonomous forklift unloading task with limited real-world data. Moreover, training VLA models typically requires large-scale datasets. As there is currently no public dataset for forklift operations, we use a VLA model pretrained primarily on robotic manipulator data and construct a training dataset via simulation, which can be scaled up at low cost. We then adapt the pretrained VLA model to forklift control using 9.38 h of simulation data and 0.8 h of real-world demonstrations, with the latter accounting for approximately 8% of the collected forklift data by duration. The integrated system was validated through 72 real-world trials across four model variants. The results show that the proposed system can accomplish an unloading task even with limited real-world data.

---

## 14. $\widetilde{\varepsilon}$: Does Initial Noise Induce Directional Bias in Vision-Language-Action Models?

**Authors:** Junmyeong Lee, Dongmin Shin, Wooseok Jeon, ..., Seunghyun Shin, Hae-Gon Jeon
**arXiv:** [2611.33816](https://arxiv.org/abs/2611.33816)
**Categories:** Robotics (cs.RO)

Vision-language-action models (VLAs) have widely adopted diffusion-based action generation for continuous robot motions, enabling fine-grained control across diverse tasks. However, recent studies have shown that their performance is highly sensitive to initial noise, with resulting action errors that make recovery difficult during execution. Existing approaches search for favorable noise initializations to improve performance, yet the action expert itself remains sensitive to noise. In this work, we reveal that initial noise induces a consistent directional bias in action space that closely aligns with the noise's temporal mean. We thus introduce a simple yet effective framework that improves robustness to initial noise through interventions during both training and inference. During training, we enforce consistent action predictions from antithetic noise pairs $(\epsilon, -\epsilon)$ and, at inference, remove the noise's temporal mean. Our method substantially reduces action deviation and improves task performance across simulation benchmarks. In real-robot experiments, our method increases the average task success rate of $\pi_{0.5}$ from 40% to 68%, with more stable and consistent execution.

---

## 15. FailPoint-X: A Policy-Matched, Failure-Anchored Benchmark for Offline VLA Post-Training from Human Takeovers

**Authors:** Zirui Li, Yujie Yan, Jingxuan Qian, ..., Haoran Xu, Chen Lv
**arXiv:** [2611.33769](https://arxiv.org/abs/2611.33769)
**Categories:** Robotics (cs.RO)

Human takeovers offer corrective supervision for vision-language-action (VLA) policies, but their contribution to offline post-training must be separated from that of continued optimization. We introduce FailPoint-X, a benchmark for offline VLA post-training with human takeovers. To represent uncertainty in failure onset, an annotator marks an interval for each failure, and training takeovers start at seeded frames sampled within it. From one fixed $\pi_{0.5}$ checkpoint, which also initializes post-training, we assemble 629 natural failures across 10 LIBERO-X task families at up to five difficulty levels. All 2,823 takeover attempts are logged; 2,400 are accepted recoveries, of which 2,320 are used for post-training. Evaluation restarts every method from the fixed midpoints of 384 held-out failure intervals. Under matched actor-update counts, we compare behavior cloning of recoveries, value-based offline learning on recoveries and failed rollouts, and continued training on existing demonstrations. Within 1,200 steps on the 240 L1-L3 held-out failures, cloning improves recovery by 29.4 percentage points (pp) over the demonstration-only control; the value-based learner does not establish a further gain (1.5 pp). In exploratory evaluation from L1-L5 nominal starts at the same horizon, cloning loses 30.0 pp of success relative to the base policy; mixing in demonstrations reduces the loss to 16.5 pp, a reduction that shrinks under a stricter, pre-specified horizon. Restorable failure states and a shared evaluator let all methods be compared from identical starts.

---

## 16. FreshVLA: Frequency-Regularized Time Scale Hierarchical Latent Actions for Vision-Language-Action Models

**Authors:** Jiaming Liang, Yifeng Zhan, Rongyi He, ..., Xingjian Jing, Qiang Nie
**arXiv:** [2611.33635](https://arxiv.org/abs/2611.33635)
**Categories:** Robotics (cs.RO)

Learning reusable latent actions from action-free videos offers an effective route to improving Vision-Language-Action (VLA) policies. However, reconstruction-oriented latent actions do not necessarily benefit policy learning: as they may encode task-irrelevant static appearance with scene identity, or entangle slowly varying task progress with fine-grained execution dynamics in limited discrete code. We propose FreshVLA, a VLA framework built on a frequency-guided, dynamics-sensitive learning paradigm for acquiring temporally hierarchical continuous latent actions. FreshVLA uses a high-pass prior to guide visual transition encoding toward dynamical regions, thereby reducing reliance on static appearance cues. It further organizes latent actions into coarse-grained task progress and fine-grained execution dynamics through cross-timescale sampling and frequency-domain regularization, enhancing their capacity to represent long-horizon behaviors. During policy training, we freeze the pretrained latent action encoder and transfer its representations to robot control through joint flow-matching of latent and robot actions. FreshVLA achieves 98.2% average success on LIBERO and 98.0% on LIBERO-Long, exceeding GR00T-N1.6 on the latter by 3.6%. It also reaches an average sequence length of 4.52 on CALVIN and strong overall success rate of 80.4% in the zero-shot LIBERO-PLUS evaluation. Furthermore, FreshVLA exhibits greater robustness to visual perturbations and a more distinct division of roles between two branches in modeling low- and high-frequency motion, respectively. In 35-step action regression, it achieves a 51.3-percentage-point higher relative error reduction than its hierarchical discrete counterpart. Real-world experiments demonstrate that FreshVLA improves the average success rate over $\pi_{0.5}$ by 7.5%. The FreshVLA project page is available at this https URL.

---

## 17. Commit2Drive: Perception-Grounded Language Decisions as Commitments for Trajectory Planning in Vision-Language-Action Driving Models

**Authors:** Zikai Zhang, Hubert P. Shum, Toby Breckon
**arXiv:** [2611.34614](https://arxiv.org/abs/2611.34614)
**Categories:** Computer Vision and Pattern Recognition (cs.CV)

Vision-Language-Action (VLA) models introduce language reasoning into end-to-end autonomous driving. They output a language decision together with a trajectory, which makes the planner more interpretable. However, in existing methods the language decision is either an independent output or an index that selects among similar candidate trajectories, and its annotations are not verified against the trajectory. As a result, the language decision and the trajectory are often inconsistent in closed-loop driving. To address this, we propose Commit2Drive, a framework that imposes the language decision as a consistency constraint on trajectory planning. The decision is a commitment, a maneuver class with a continuous parameter that one deterministic rule reads from any trajectory, and it is grounded in facts reported by the perception of the model itself. A Maneuver Bank maps the commitment to a code with a kinematic meaning, and consistency losses train the planner to execute every admissible decision of a scene, so that the trajectory follows the decision. An automatic data pipeline supplies the supervision. Decisions are labeled from the future motion of the expert, counterfactual executions train the decision and the trajectory together, and rule-based functions with a Vision-Language Model (VLM) generate, review and refine the language annotations. The code is a lookup that involves no hidden state of the language model, so Commit2Drive is extensible to rule-based decisions, which the same planner executes without retraining. Commit2Drive uses a 0.5B language model and runs closed-loop inference online on a single consumer graphics card. On Bench2Drive, Commit2Drive reaches a Driving Score (DS) of 78.50 and a Success Rate (SR) of 55.91% with a lightweight model, which is competitive with the state of the art, and greatly reduces the language-action inconsistency. Code will be released soon.

---

## 18. Off the Driven Path: Transferable Road Understanding in Driving VLAs

**Authors:** Lena Wild, Christian Helten, Katie Z Luo, ..., Patric Jensfelt, Marco Pavone
**arXiv:** [2611.33878](https://arxiv.org/abs/2611.33878)
**Categories:** Computer Vision and Pattern Recognition (cs.CV)

End-to-end driving policies increasingly operate without explicit HD maps at inference, raising the question of what road knowledge they actually internalize. To probe this knowledge through model outputs, we introduce Road-KSU, a framework that automatically converts HD maps and actor annotations into a road-centric scene graph. From this, we derive road-focused question answering and reasoning targets, complemented by map-based trajectory compliance metrics. Pairing Road-KSU with geographically disjoint splits yields a $2 \times 2$ evaluation crossing output modality (language vs. action) with place familiarity (seen vs. unseen roads). On NAVSIM, 95% of test samples lie within 10m of a training sample, and scores of 13 published planners on turns rise steeply with the number of training drives through the test location, pointing to memorized road geometry. Retraining on geographically disjoint splits and probing with Road-KSU confirm that action-space performance degrades most on unfamiliar turns, with failures dominated by geometric compliance. Language accuracy, however, drops on road-centric VQA on straight and curved roads alike, and remains stable on dynamic scene content. Scaling the training data further reveals a double dissociation: more drives through the same places improve driving on unseen roads but leave road question answering unchanged, whereas spreading a fixed data budget over more places increases road question answering with little change in driving performance. These findings show that improved driving scores need not imply broader road understanding on unseen roads, and identify geographic diversity as key to transferable road knowledge.

---

## 19. FlipVLA: Backdoor Attacks on Vision-Language-Action(VLA) Models Only Through Bit Flips

**Authors:** Zexi Zhao, Zizhen Liu, Jing Justin Ye, Huawei Li
**arXiv:** [2611.33810](https://arxiv.org/abs/2611.33810)
**Categories:** Computer Vision and Pattern Recognition (cs.CV); Cryptography and Security (cs.CR)

Vision-language-action (VLA) models generate robot actions from visual observations and language instructions in real-world environments, making malicious model tampering a potential threat to physical safety. We study whether object-triggered backdoors can be implanted through a small, fixed set of parameter bit flips without retraining. The central challenge is to make persistent weight modifications disrupt trigger-present behavior while preserving performance on non-trigger inputs. We propose FlipVLA, a two-stage selector-amplifier method that exploits existing visual features within an FC-GELU-FC structure. The selector constructs a trigger-dependent response in a selected channel, using GELU to attenuate background activity. The amplifier modifies a connected downstream weight to convert this response into an action-relevant perturbation. Channel screening and discrete bit search construct both components under a limited modification budget. Experiments on OpenVLA-OFT and GR00T N1.7 across four LIBERO suites achieve attack success rates of 90.22% to 100%, with task success decreasing by at most 1.5 percentage points on clean scenes.

---

## 20. RoboARC: Physical Puzzles for Robotic Manipulation under Spatial Constraints

**Authors:** Qineng Wang, Jianwen Lyu, Pingyue Zhang, ..., Ruohan Zhang, Manling Li
**arXiv:** [2611.33390](https://arxiv.org/abs/2611.33390)
**Categories:** Robotics (cs.RO); Artificial Intelligence (cs.AI)

Many hard manipulation tasks come down to a spatial constraint that only a few motions satisfy, such as passing a part through a gap barely wider than itself or separating two interlocked parts. These motions depend on the exact geometry of each scene, so demonstrations and skills recorded elsewhere rarely transfer. We therefore ask: when manipulation hinges on spatial constraints, can robots reason out the right motions? We introduce RoboARC, a benchmark of 90 tasks in six constraint types over rigid and soft materials, on three robots in MuJoCo. Every task is a frozen scene with a physics-based grader and a verified reference solution that replays bit-identically. Each task comes in a Privileged regime, with the full simulator state and resets, and a Standard regime with real-sensor inputs (camera images and proprioception) and a single attempt without resets. We evaluate seven coding agents and four VLA policies, none trained on these tasks. The strongest agent, GPT-6 Astra in Codex, solves 86% of the tasks in the Privileged regime and 43% in the Standard regime, and the four VLA policies, run zero-shot, solve none of their 18 one-arm puzzles. On 15 puzzles that GPT-6 Astra solved in the Privileged regime and failed in the Standard regime, object poses add 4 points and part geometry 13, but both together add 36, from 24% to 60%. Only 7% of the coding agents' failed runs pass more than half of a task, and 53% of the failed runs in the Standard regime are stuck on a single step. Frontier coding agents already reason out the right motions for many of these tasks once they know where the parts are and what shape they have. From their own sensors, in a single attempt, the strongest solves fewer than half of the tasks. The website can be found at this https URL

---
