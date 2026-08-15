# arXiv Daily Digest — 2026-08-14

**Mode:** direct
**Categories:** cs.AI, cs.LG, cs.RO, cs.CV
**Keywords:** VLA, world model, world action model
**Papers found:** 17

---

## 1. AlayaWorld: Interactive Long-Horizon World Modeling - Full Technical Report (v1.1)

**Authors:** AlayaWorld Team, Kaipeng Zhang, Chuanhao Li, ..., Zian Meng, Zihui Gao
**arXiv:** [2608.13492](https://arxiv.org/abs/2608.13492)
**Categories:** Artificial Intelligence (cs.AI)

This report presents an improved version of AlayaWorld. While the backbone architecture, chunk-wise autoregressive generation scheme, and training data remain unchanged from the previous release, we substantially revise how conditioning signals are represented and integrated into the model. The new design is guided by a simple principle: conditioning signals should match the generated content as closely as possible in both latent representation and temporal structure. To this end, we make two major changes. First, we replace the previous depth-warping-based spatial memory with a streaming 3D point-cache renderer. Second, we redesign the conditioning pipeline so that visual conditions are encoded in the same causal-VAE latent space, with temporal statistics consistent with those of the generated video. Concretely, the new version introduces six modifications: (1) replacing static-frame image conditioning with motion-aware latent conditioning; (2) causally encoding re-rendered spatial memory as a continuous sequence; (3) aligning the temporal-memory window in pixel space; (4) adopting hard memory dropout that removes memory tokens rather than zeroing them; (5) unifying the VAE encoding and decoding protocol across training and inference; and (6) removing the camera AdaLN branch, such that viewpoint control is provided entirely through the re-rendered spatial condition.

---

## 2. A Unifying Perspective on Causal World Models: From Observations to Representations to Structure

**Authors:** Avinash Kori, Fabrizio Russo
**arXiv:** [2608.13456](https://arxiv.org/abs/2608.13456)
**Categories:** Artificial Intelligence (cs.AI); Computer Vision and Pattern Recognition (cs.CV)

World Models (WM) are increasingly seen as a foundation for intelligent agents that can predict, plan, and act beyond their training distribution. In this paper, we study WMs from a causal perspective across multiple levels of abstraction, ranging from perceptual observations to building a conceptual representation of the structure governing the environment dynamics. We argue that useful WMs must go beyond generative capabilities alone: they should also capture entity properties, entity-to-entity interactions, and entity-to-environment interactions that determine and explain the dynamics of a system. We provide a formal definition of Causal WMs (CWMs) grounded in the tasks they are intended to support, connecting world modelling with existing work in causal representation learning, object-centric learning, causal discovery, structural causal models, and model-based decision-making. Finally, we relate CWMs to the literature on identifiability, clarifying when the components of a WM can be recovered from data and up to which equivalence. With this, we ground WMs in representations and structures that support causal reasoning and informed decision-making.

---

## 3. FlashDrive: Flash Vision-Language-Action Inference for Autonomous Driving

**Authors:** Zekai Li, Yihao Liang, Hongfei Zhang, ..., Yesheng Liang, Zhijian Liu
**arXiv:** [2608.12932](https://arxiv.org/abs/2608.12932)
**Categories:** Artificial Intelligence (cs.AI)

Vision-Language-Action (VLA) models promise to bring end-to-end reasoning to autonomous driving, but their computational cost remains far too high for real-time control. The core challenge is structural: VLA inference is not a single bottleneck but a cascade of four. Visual encoding wastes compute on overlapping video frames; language-model prefill recomputes context that could be carried over from the previous timestep; reasoning tokens are generated serially despite low entropy; and flow-matching denoising applies uniform compute to a non-uniform velocity field. Addressing any one stage in isolation leaves the others untouched. We propose FlashDrive, an algorithm-system co-design framework that targets all four stages simultaneously. Our key insight is that each bottleneck admits a distinct, lightweight algorithmic shortcut: temporal overlap enables streaming KV-cache reuse across frames; the low per-token entropy and strong intra-block correlations of driving-domain reasoning make a non-autoregressive diffusion drafter highly effective for speculative decoding; and the velocity field's structure---sharp at the endpoints, flat in the middle---permits adaptive step caching that concentrates compute where it matters. Layered on system-level CUDA Graph compilation and kernel fusion, these techniques compound. Applied to Alpamayo 1.5-10B with W4A8 quantization, FlashDrive reduces end-to-end latency from 717ms to 151ms (4.7x) while leaving accuracy essentially unchanged: minADE6@6.4s shifts by only 0.08m, minADE1 improves, and closed-loop collision and off-road rates improve in simulation. By raising a 10B-parameter reasoning VLA from 1.4~Hz to 6.6~Hz on a single GPU, FlashDrive moves end-to-end autonomous driving substantially closer to real-time deployment.

---

## 4. UniTexture: Cross-Task Universal Adversarial Textures for Vision-Language-Action Models

**Authors:** Yukun Dai, Mingzhe Dai, Tianshi Wang, ..., Jingjing Li, Lei Zhu
**arXiv:** [2608.13453](https://arxiv.org/abs/2608.13453)
**Categories:** Computer Vision and Pattern Recognition (cs.CV); Artificial Intelligence (cs.AI)

Vision-Language-Action (VLA) models have emerged as generalist robotic policies capable of following diverse language instructions and performing a wide range of manipulation tasks. However, their direct control over embodied agents also exposes them to adversarial interference that may cause unsafe physical behaviors. Existing attacks on robotic policies are typically optimized for a single task or instruction, leaving the cross-task vulnerabilities of multitask VLAs largely unexplored. We introduce UniTexture, a cross-task universal adversarial texture attack that uses a single textured 3D object to induce targeted deviations in VLA action predictions across multiple tasks. UniTexture backpropagates gradients from the policy's action outputs to surface texture parameters through a differentiable renderer. It jointly optimizes the shared texture over a distribution of tasks, instructions, states, and viewpoints using a targeted action-space objective, steering predicted actions toward attacker-defined targets without optimizing a separate texture for each task. We evaluate UniTexture on OpenVLA and $\pi_{0.5}$ across diverse manipulation tasks and multiple evaluation settings. UniTexture reduces the mean task success rate from 90.0% under benign conditions to 48.4% under attack, induces target-aligned action shifts, and further exhibits cross-suite and cross-model transfer without re-optimization. Together, these findings reveal shared cross-task vulnerabilities in multitask VLAs that can be systematically exploited through a single adversarial surface texture.

---

## 5. ContactGuard: Pre-Contact Execution Monitoring with Action-Conditioned Latent World Models

**Authors:** Gehan Zheng, Matthew Johnson-Roberson, Weiming Zhi
**arXiv:** [2608.13438](https://arxiv.org/abs/2608.13438)
**Categories:** Robotics (cs.RO); Artificial Intelligence (cs.AI); Computer Vision and Pattern Recognition (cs.CV)

Contact-rich manipulation failures are often detected only after the robot has committed to contact. This is especially limiting in wrist-camera setups: close gripper--object views help observe contact, but a poor approach may already push, miss, slip, or disturb the object before conventional detectors react. We introduce \emph{ContactGuard}, a pre-contact execution monitor for chunked visuomotor policies. Given the policy's planned action chunk, ContactGuard predicts its short-horizon consequence in latent visual space and aborts if the predicted future latent indicates likely failure. Its latent world model is trained from unlabelled robot trajectories to predict compact multi-view visual embeddings under planned actions, avoiding pixel-level video prediction. A lightweight failure probe is then trained from a small labelled set of pre-contact clips. At deployment, ContactGuard anchors prediction before an imminent contact event, rolls the model forward under the policy's own actions, and verifies the predicted post-contact latent. Across real-world contact-rich manipulation tasks, ContactGuard predicts failure more accurately than direct and corrupted-action ablations, and transfers to live robot as a pre-contact abort signal without modifying the underlying policy.

---

## 6. The Objective Is the Bottleneck: Latent World Models Encode What Their Planners Cannot Use

**Authors:** Joyjeet Singh
**arXiv:** [2608.12959](https://arxiv.org/abs/2608.12959)
**Categories:** Machine Learning (cs.LG); Artificial Intelligence (cs.AI)

Latent world models are judged by how well they predict, so when planning fails at long horizons the natural reading is that the predictor degrades. On a reproduction of LeWorldModel on TwoRoom we show the binding constraint is the planner's objective instead.
The predictor is not the limit: its imagined state seventy-five environment steps ahead is still only 0.189 as wrong as assuming the world froze, while the planner never imagines beyond twenty-five. The objective is. Cross-entropy-method planning minimises squared latent distance, which tracks true distance at r = 0.426, saturates by about eighty arena units and decreases beyond a hundred and twenty, so moving away from the goal can lower the cost. The information is present throughout: a ridge probe recovers position from the frozen embedding at R^2 0.9922.
The pathology is the method's, not one reimplementation's. It is present in the authors' released weights, and across four checkpoints long-horizon success rank-orders exactly with metric quality and inversely with prediction accuracy.
Replacing only the objective, with nothing retrained and no GPU, lifts goals reached at offset 100 from 26.0% to 98.0%, equals the 98.0% at offset 25, and reaches 92.0% under a third of the budget: planning stops depending on the horizon. The best cost is not the most accurate. A head learned from frame separation alone predicts spatial distance worse than a position probe (r = 0.819 against 0.9897) yet plans better, charging 24% more to cross the environment's dividing wall where squared latent distance charges 4% less. It has learned reachability, not proximity.

---

## 7. Intervention-Aware Clinical World Model for Post-Op Outcome Forecasting in Cardiology

**Authors:** Yunsung Chung, Yingshuo Liu, Abboud F. Hassan, ..., Nassir Marrouche, Jihun Hamm
**arXiv:** [2608.13518](https://arxiv.org/abs/2608.13518)
**Categories:** Machine Learning (cs.LG); Computer Vision and Pattern Recognition (cs.CV)

Many clinical prediction models treat post-intervention outcomes as a one-step mapping from baseline measurements to a future endpoint. However, recovery after a procedure often unfolds as an irregular trajectory: clinical observations, medication changes, repeat interventions, and physiological measurements are recorded asynchronously and can change risk assessment over time. We propose an intervention-aware clinical world model that represents each patient with a structured latent state and evolves it through time-ordered post-intervention events. The model first encodes baseline imaging into a 3D spatial latent state. It then updates this state using procedural context, static covariates, elapsed time, and peri-event physiological embeddings. Follow-up imaging provides training-only supervision through a latent forecasting objective. We apply the framework to atrial fibrillation ablation. During the 90-day recovery window, irregular post-procedure records provide clinically meaningful evidence for long-term recurrence risk. In repeated internal cross-validation on DECAAF-II, our model achieves AUROC 0.756 and AUPRC 0.777 for recurrence prediction. It also achieves a scar-extent MAE of 2.971 percentage points without requiring follow-up MRI intensities at inference. The learned state supports recurrence-risk queries at different horizons and retrospective input editing of blanking-period records.

---

## 8. Diagnosing JEPA World Models with Action-Conditioned Predictive Consistency

**Authors:** Guo An, Zijing Wu, Honghua Dong, ..., Yurong Ling, Qi Tian
**arXiv:** [2608.12939](https://arxiv.org/abs/2608.12939)
**Categories:** Machine Learning (cs.LG)

Joint-embedding predictive architectures (JEPAs) learn world models that predict in a compact latent space rather than in pixels, reducing the pressure to model nuisance appearance. Yet this provides no guarantee against visual perturbations: they can still alter the encoded representation and affect subsequent action-conditioned predictions. Bisimulation captures this requirement precisely: two observations should be treated as the same state only when their action-conditioned consequences agree. Guided by this criterion, we introduce Action-Conditioned Predictive Consistency (ACPC), a diagnostic that measures how far a clean history and a visually perturbed view of it diverge after being rolled forward under the same action sequence. We prove that this divergence bounds the perturbation-induced change in multi-step prediction error and planner cost. Building on pairwise ACPC, we define two complementary measures: the Invariance Radius (IR) summarizes clean-perturbed rollout spread, while the Separation Rate (SR) checks whether different states remain distinguishable after rollout. Experiments on four visual control tasks show that pairwise ACPC predicts perturbation-induced prediction and cost changes. On LeWM, the IR-SR screen transfers across tasks, and the joint diagnostic remains informative under blur and resize. PLDM exhibits similar diagnostic trends under a different architecture.

---

## 9. Scaling Automatic Research Agents via World Models

**Authors:** Xiyuan Yang, Sheikh Sarwar, Jingru Cheng, ..., Jingrui He, Zhenyu Liao
**arXiv:** [2608.12564](https://arxiv.org/abs/2608.12564)
**Categories:** Machine Learning (cs.LG)

Automating empirical research is a long-standing direction of AI. Recent automatic research (AutoResearch) agents bring this goal within reach, as modern LLMs show the capability to independently implement solutions and learn from the execution outcomes. Behind these gains, post-training (especially RL) plays a central role. In this paper, we identify a fundamental tension when scaling RL for these agents: the two components of every AutoResearch trajectory (agent generation and environment execution) scale in very different manners, since all generation shares compute through batching, while each execution occupies its exclusive sandbox and real machine time. As a result, the environment execution dominates the training cost and becomes the bottleneck as trajectories grow. To resolve this tension, we propose World Model RL (WMRL), which replaces environment execution with a world model to remove this bottleneck. Additionally, the world model can be imperfect, as its rewards are corrupted by bias and noise. Therefore, we further equip WMRL with two mitigations, Online Debiasing and Inverse-Variance Denoising, which offset the bias and suppress the noise respectively. Theoretically, we prove that both mitigations of WMRL strictly improve the convergence guarantee. Empirically, WMRL accelerates training by 3-4x on various tasks at different agent scales, while exceeding the performance of standard RL baselines. Moreover, our post-trained 4B and 9B agents outperform much larger open-weight agents of 48B and 120B on held-out benchmarks. Beyond AutoResearch, WMRL also transfers to post-training embodied VLA policies, which demonstrates the generalizability of our method.

---

## 10. Decoding Task Progress from VLA Representations

**Authors:** Atiksh Bhardwaj, Edward Weiyi Duan, Prithwish Dan, Wei-Chiu Ma, Preston Culbertson
**arXiv:** [2608.13474](https://arxiv.org/abs/2608.13474)
**Categories:** Robotics (cs.RO)

Vision-language-action models (VLAs) are moving rapidly towards deployment as general-purpose manipulation policies, but we currently lack basic tools for understanding what these models represent internally or for monitoring them at runtime. Leveraging ideas from mechanistic interpretability, we probe the residual stream of $\pi_{0.5}$ and find that task progress, the normalized time remaining in a trajectory, is linearly readable from the activations. We find that this signal is present in the pretrained PaliGemma backbone prior to training on any robot-specific data. A single linear probe generalizes to unseen tasks and varies under language counterfactuals when trained on multi-prompt data, but does not enable meaningful steering of the policy. These properties make the signal directly useful for instrumenting deployed VLAs. We use the probe as a simple label-free OOD detector, which detects stalled task progress, and find it competitive with state-of-the-art methods. Our results suggest that VLAs have rich, linearly readable internal representations of semantic quantities like task progress, and that learning to read these signals offers a lightweight, interpretable path toward monitoring deployed visuomotor policies.

---

## 11. FIRE-VLA: Failure-Informed Self-Evolution for Vision-Language-Action Models in Autonomous Driving

**Authors:** Hao Dou
**arXiv:** [2608.13395](https://arxiv.org/abs/2608.13395)
**Categories:** Robotics (cs.RO)

Reinforcement learning improves autonomous-driving vision-language-action (VLA) models by evaluating trajectories sampled from the current policy. Group relative policy optimization (GRPO) learns from reward differences within each rollout group. When all sampled trajectories are poor, this relative signal can rank failures without identifying behavior outside the failed region. We introduce FIRE-VLA, a failure-informed self-evolution framework that converts such unresolved failures into privileged supervision for the next policy. Low-reward, low-diversity groups trigger self-distillation from a frozen round-start copy of the same model. Teacher and student have the same parameter scale, but only the teacher observes the hidden future trajectory. Supervision follows the student's generated prefix and is restricted to answer tokens, while GRPO remains active for every group. The updated policy supplies the teacher for the next round, allowing the routed failure distribution to change with the policy without requiring a larger external teacher. Starting from the same Qwen2.5-VL-3B SFT checkpoint, the comparison matches student rollout and policy-update counts. On 6,019 examples from 150 held-out nuScenes scenes, FIRE-VLA retains comparable single-sample planning, reduces G=4 mean L2 from 1.848 to 1.500 m, and lowers evaluation-persistent failure prevalence from 13.03% to 11.20%. The reduction in mean error arises mainly from rare severe rollouts rather than uniform improvement across ordinary trajectories.

---

## 12. S2-HWM: Sparse Event-Structured Hierarchical World Model for Long-Horizon Surgical Robot Manipulation

**Authors:** Shuzhe Zhang, Xin Zhu, Yinling Qian, Qiong Wang
**arXiv:** [2608.13103](https://arxiv.org/abs/2608.13103)
**Categories:** Robotics (cs.RO); Systems and Control (eess.SY)

Long-horizon surgical robot manipulation is challenging because task rewards are sparse, while meaningful interaction changes occur at irregular intervals. Existing world-model agents typically imagine at primitive-step resolution, leaving variable-duration task progress implicit. Manually specified stages can provide intermediate structure, but their task specific boundaries are difficult to align with state-dependent interaction transitions. We propose S2-HWM, a Sparse Event-Structured Hierarchical World Model that learns sparse event evidence from primitive latent trajectories to coordinate an event-level manager and a primitive-step worker. The event evidence schedules manager goal updates, and each selected latent goal conditions the worker's primitive actions until the next update. The learned event evidence also forms variable-duration segments for an Event Transition Model (ETM), which predicts the next?boundary stochastic state, segment duration, and accumulated segment reward. Chaining these event-level predictions provides a variable-duration continuation beyond the primitive imagination horizon for manager learning, while the worker retains primitive-step actor-critic learning. On a SurRoL-based PegTransfer task, S2-HWM achieves a success rate of 98.7%, outperforming the flat GAS DreamerV3 baseline by 22.7 percentage points.

---

## 13. H2R-Bench: Benchmarking Human-to-Robot Manipulation Video Generation in World Models

**Authors:** Dingyi Rong, Yue Shi, Chaofan Ma, ..., Guangtao Zhai, Ning Liu
**arXiv:** [2608.13049](https://arxiv.org/abs/2608.13049)
**Categories:** Robotics (cs.RO); Computer Vision and Pattern Recognition (cs.CV)

Large-scale manipulation data is essential for robot learning, yet collecting robot demonstrations remains expensive and difficult to scale. Meanwhile, abundant egocentric human manipulation videos provide rich behavioral experiences, but transferring them across embodiments remains challenging due to differences between human hands and robotic end-effectors. Recent advances in video world models offer a promising pathway to synthesize robot-centric manipulation videos from human observations, while their cross-embodiment transfer capability remains largely unexplored. Therefore, we introduce H2R-Bench, a benchmark for evaluating cross-embodiment human-to-robot manipulation video generation, where models transform egocentric human demonstrations into robot manipulation videos under specified embodiments. Each benchmark instance contains a human demonstration video, target embodiment constraints, and source-grounded annotations covering task goals, action events, functional contacts, and object responses. H2R-Bench evaluates generated videos through five dimensions, including goal-state completion, action-event completion, functional contact transfer, embodiment correctness, and general video quality. We benchmark eleven state-of-the-art video generation models across six manipulation families and two robot embodiments. Our evaluation reveals that current video world models remain limited in human-to-robot manipulation transfer: even leading models often fail in embodiment consistency, functional interaction, and task execution. H2R-Bench provides a systematic diagnostic framework for evaluating whether video world models can bridge the human-to-robot embodiment gap and convert human manipulation observations into robot-centric training resources.

---

## 14. Temporal GRPO: Beyond Trajectory-Level Credit in Vision-Language-Action Reinforcement Learning

**Authors:** Yao Zhou, Hang Gao, Fengge Wu, Changwen Zheng, Wenwen Qiang
**arXiv:** [2608.13026](https://arxiv.org/abs/2608.13026)
**Categories:** Robotics (cs.RO)

Outcome-driven reinforcement learning offers a scalable way to post-train vision-language-action (VLA) policies from sparse task-success feedback. In common GRPO-based VLA post-training, one rollout-level advantage is applied to every action in the trajectory. A rollout that completes several valid stages but fails later can therefore penalize the actions that produced its earlier progress. We call this trajectory-level credit aliasing. Temporal GRPO addresses this problem by constructing detectable task stages, aligning each rollout with stage-specific action intervals, and comparing only rollouts that have entered the same stage. The resulting stage advantages are applied to their corresponding intervals in a single policy update. On RoboTwin 2.0, Temporal GRPO improves task success and sample efficiency, with consistent gains across task horizons. Controlled updates on LIBERO-Long preserve shared prerequisite stages and concentrate improvement at the first stage where rollout outcomes diverge.

---

## 15. DreamX-Phi 1.0: Action-Conditioned Video World Model for Robotic Manipulation

**Authors:** DreamX Team, Rui Chen, Xiangxiang Chu, ..., Jun Wang, Pengfei Zhang
**arXiv:** [2608.13489](https://arxiv.org/abs/2608.13489)
**Categories:** Computer Vision and Pattern Recognition (cs.CV); Robotics (cs.RO)

We present \textbf{DreamX-Phi 1.0}, an action-conditioned video world model for robotic manipulation that, given an observed frame, a language instruction, and a prescribed action sequence comprising end-effector poses and gripper states, predicts the resulting future observations. Yet realism alone does not guarantee faithfulness: a convincing rollout can still move the wrong arm or lose the manipulated object. To ensure the prediction respects each arm's commanded path, we inject per-arm $\mathrm{SE}(3)$ transformations into attention via \textbf{PRoPE-style geometric encoding}, preserving arm identity and rigid-motion structure. Action control alone does not fully constrain scene geometry or the evolution of small manipulated objects. We therefore add a lightweight \textbf{depth branch} for scene-level geometry and use \textbf{SAM3 masks} with a frozen \textbf{V-JEPA teacher} to maintain object consistency throughout grasping. We further distill the multi-step generator into a few-step student via distribution-matching distillation for efficient deployment. At the time of writing, \model{} achieves first place on Track~1 and second place on Track~2 of the WorldArena~2.0 Challenge. Our model and code will be publicly available.

---

## 16. PlayWorld: Benchmarking World Models with Agent Players over Long-Horizon Objectives

**Authors:** Kaixin Ding, Xi Chen, Minghong Cai, ..., Pengfei Wan, Hengshuang Zhao
**arXiv:** [2608.13552](https://arxiv.org/abs/2608.13552)
**Categories:** Computer Vision and Pattern Recognition (cs.CV)

Video world models simulate future states conditioned on current observations and user actions. Recent systems have demonstrated impressive video consistency and action controllability over long sequences. However, fairly comparing these interactive models remains challenging. In practice, a human player typically evaluates a world model by pursuing long-horizon objectives through interaction. For example, a user may turn around 360 degrees to see whether the environment remains consistent, or walk into the water and inspect whether realistic water ripples are generated. The action sequence required to achieve the same objective may vary substantially between models, making fixed action-conditioned evaluation unsuitable for cross-model comparison. To address this, we employ multi-modal Agent Players to interact with world models toward specified long-horizon objectives. Building on this paradigm, we introduce PlayWorld, a benchmark providing 171 scenarios, each with a specified objective. To evaluate performance thoroughly, we assess models along four core dimensions: geometry consistency, interaction fidelity, out-of-sight evolution, and insight evolution. In addition, we incorporate basic ability metrics for video quality and controllability. Experiments across nine state-of-the-art world models reveal that current models remain unreliable on long-horizon interactive objectives, particularly in maintaining spatial consistency and persistent state evolution. Code and data are available at this https URL.

---

## 17. HounsWorld: A Multimodal World Model for Hidden Patient-State Readout, Reconstruction, and Simulation

**Authors:** Yunhao Bai, Zhongwei Qiu, Guangyu Guo, ..., Ling Zhang, Yan Wang
**arXiv:** [2608.12904](https://arxiv.org/abs/2608.12904)
**Categories:** Computer Vision and Pattern Recognition (cs.CV)

Clinical intelligence requires estimating a patient's underlying condition from incomplete observations rather than learning isolated mappings from scans to answers. Volumetric medical images provide dense observations of anatomy, attenuation, and lesions, whereas clinical language provides sparse but complementary semantic observations. We formulate CT-centered intelligence as inference over a shared latent patient state, under which readout, reconstruction, and simulation all become state-dependent prediction problems. To operationalize this view, we introduce HounsBench, a computed tomography (CT) centric patient-state benchmark that unifies these three task families with patient-disjoint splits and per-family metrics, and HounsWorld, a 3B multimodal world model that treats volumetric scans and language as observations of the shared state through Joint Understanding-Generation Learning. A shared transformer forms an implicit patient-state estimate and supports three outputs: query-conditioned answers that read out the state, reports and captions that reconstruct it in language, and condition-specific CT volumes for low-dose denoising, virtual contrast enhancement, and anatomy-constrained text-and-mask-to-volume generation. Zero-initialized CT adapters preserve pretrained multimodal mappings, while condition-explicit Hounsfield-unit window sampling exposes clinically meaningful density observations. HounsWorld shows strong performance across all three task families while consistently improving CT understanding through clinically structured completion. Our project is available at this https URL

---
