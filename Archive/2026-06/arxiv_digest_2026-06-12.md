# arXiv Daily Digest — 2026-06-12

**Mode:** direct
**Categories:** cs.AI, cs.LG, cs.RO, cs.CV
**Keywords:** VLA, world model, world action model
**Papers found:** 24

---

## 1. A Tutorial on World Models and Physical AI

**Authors:** Il-Seok Oh
**arXiv:** [2606.12783](https://arxiv.org/abs/2606.12783)
**Categories:** Artificial Intelligence (cs.AI)

World modeling is emerging as a central principle for building intelligent systems capable of prediction, reasoning, and decision making. A central distinction can be drawn between explicit world models, which learn structured dynamics for rollout-based reasoning and planning, and implicit world models, which encode predictive structure within scalable learned representations. These complementary paradigms provide a foundation for physical AI in domains such as robotics and autonomous driving, enabling intelligence beyond reactive control under real-world constraints. Recent foundation models further suggest a pathway toward unified systems integrating perception, prediction, and action. Despite rapid progress, major challenges remain in hierarchical reasoning, long-horizon planning, and autonomous goal formation, which are critical for advancing toward artificial general intelligence. This tutorial presents a coherent framework in which diverse world modeling approaches are unified through shared predictive structure and differentiated by how such structure is represented and exploited.

---

## 2. PersonaDrive: Human-Style Retrieval-Augmented VLA Agents for Closed-Loop Driving Simulation

**Authors:** Mahmoud Srewa, Praneetsai Iddamsetty, Mohammad Abdullah Al Faruque, Salma Elmalaki
**arXiv:** [2606.12616](https://arxiv.org/abs/2606.12616)
**Categories:** Artificial Intelligence (cs.AI); Computation and Language (cs.CL)

Closed-loop driving simulators typically populate their environments with non-ego traffic agents that behave largely the same way, produced either by rule-based traffic managers or by learned models trained toward a single behavioral mode. Recent work introduces style variation through post-hoc labels on observational data or LLM-inferred reward weights, but these signals act as proxies for what a style should reward rather than demonstrations of humans explicitly asked to drive in that style. We introduce PersonaDrive, a pipeline that conditions a vision-language-action (VLA) driving agent on retrieved demonstrations from a style-instructed human driving dataset, in which participants drive CARLA leaderboard routes under aggressive, neutral, and conservative instructions on a driver-in-the-loop rig. The pipeline has three stages: (i) offline triplet mining over per-style human driving data using a combined image-text similarity score; (ii) training a lightweight retrieval head that fuses frozen visual features with a small control encoder over per-style databases; and (iii) fine-tuning a single VLA backbone to treat retrieved context points as in-context behavioral demonstrations during waypoint prediction. At inference, the same backbone is conditioned on any style by swapping which per-style database the retrieval head queries, so selecting a style requires no per-style retraining while enabling human-style, style-diverse non-ego agents for closed-loop simulation. On Bench2Drive, PersonaDrive (no style) improves the driving score by 4.6% over SimLingo and 2.5% over HiP-AD, and under style conditioning attains the highest driving score in every style within a roughly 2% band (its weakest style surpassing the strongest baseline, DMW, by 5.4%), while average speed and acceleration rise by 18% and 25% from the conservative to the aggressive instruction.

---

## 3. LabVLA: Grounding Vision-Language-Action Models in Scientific Laboratories

**Authors:** Baochang Ren, Xinjie Liu, Xi Chen, ..., Ningyu Zhang, Huajun Chen
**arXiv:** [2606.13578](https://arxiv.org/abs/2606.13578)
**Categories:** Computation and Language (cs.CL); Artificial Intelligence (cs.AI); Machine Learning (cs.LG); Multimedia (cs.MM); Robotics (cs.RO)

Scientific laboratories increasingly rely on AI systems to reason about experiments, but the physical act of doing science remains largely outside their reach. AI can help read literature, generate hypotheses, and plan protocols, yet the execution of those protocols at the bench still requires a human operator. Vision-Language-Action (VLA) models provide one possible interface between written protocols and robot execution, but existing policies are trained mostly on household and tabletop demonstrations and rarely encounter the instruments, transparent liquids, or fixed protocol workflows found in scientific laboratories. Closing this gap requires both laboratory-specific supervision and a unified learning framework that can accommodate the diverse robot embodiments used to execute experimental protocols. We therefore identify data and embodiment as central bottlenecks alongside model design. To address the data side, we build RoboGenesis, a simulation-based workflow and data engine that composes configured laboratory workflows from atomic skills, validates and filters rollouts, and exports structured demonstrations across supported robot profiles. On the policy side, we present LabVLA, trained with a two-stage recipe: FAST action token pretraining first makes the Qwen3-VL-4B-Instruct backbone action aware before any continuous control is learned, and flow matching posttraining then attaches a DiT action expert under knowledge insulation. On the LabUtopia benchmark, LabVLA achieves the highest average success rate among all evaluated baselines under both in-distribution and out-of-distribution settings.

---

## 4. EA-WM: Event-Aware World Models with Task-Specification Grounding for Long-Horizon Manipulation

**Authors:** Kailin Wang, Haoxiang Jie, Yaoyuan Yan, Jiacheng Zhou, Zhiyou Heng
**arXiv:** [2606.13053](https://arxiv.org/abs/2606.13053)
**Categories:** Robotics (cs.RO); Artificial Intelligence (cs.AI)

Pretrained-feature world models provide a useful substrate for robot imagination, but visual or latent prediction alone does not determine whether an imagined future satisfies task-relevant events. Long-horizon manipulation requires progress signals that are relational, predicate-level, and physically grounded: whether an object has moved, whether a drawer or contact state has changed, whether a placement predicate is satisfied, and whether a candidate future is reliable enough for execution. We introduce EA-WM, an event-aware world-model framework that augments frozen visual-feature dynamics with task-specification-grounded event prediction and verification. EA-WM rolls out candidate futures in pretrained visual-feature space, decodes them into structured event states, and scores them using task-progress, semantic-consistency, physical-feasibility, and uncertainty terms. The verifier guides sampling-based planning, gates candidate actions, and, in the contact-sensitive LIBERO wine-rack setting, selects among PPOgenerated proposals. Across navigation, deformable-object, wall-constrained, and languagedescribed manipulation studies, EA-WM shows that event-aware verification can make featurespace world models more interpretable and better aligned with task progress.

---

## 5. Diffusion Transformer World-Action Model for AV Scene Prediction

**Authors:** Ruslan Sharifullin, Benjamin Jiang, Kai Xi Chew
**arXiv:** [2606.12987](https://arxiv.org/abs/2606.12987)
**Categories:** Computer Vision and Pattern Recognition (cs.CV); Artificial Intelligence (cs.AI); Machine Learning (cs.LG); Robotics (cs.RO)

Action-conditioned world models let an autonomous vehicle predict future camera scenes from its own planned controls, enabling planning and simulation without real-world rollouts, but at compact, trainable scale the futures are ambiguous and the field's standard distortion metrics actively mislead: they reward a blurry regression mean over a realistic prediction. We confront this with a compact latent world model that, given the present front-camera latent and a sequence of ego-actions, predicts future scene latents a frozen decoder renders to $256 \times 256$ frames up to 8 seconds ahead, evaluated on 150 held-out nuScenes scenes. We first benchmark where to predict: across six frozen encoders spanning four representation families, V-JEPA2 with temporal context reduces steering RMSE by 40% over the best single-frame encoder. We then train a latent Diffusion Transformer (DiT) and, through a controlled diagnosis, identify the four ingredients it needs: spatial tokens, the $x_0$ objective, residual anchoring, and sampling matched to target uncertainty. In a Stable-Diffusion-VAE encode-predict-decode pipeline we expose the central tension: distortion metrics (cosine similarity, SSIM) favor the blurry mean, masking that the diffusion model is far closer to the real frame distribution. Inception-based FID and KID reveal a clean perception-distortion frontier: diffusion attains KID 0.078 versus 0.375 for regression ($4.8\times$ better), and a deployable train-derived calibration makes this practical without test-time ground truth. The model is genuinely action-controllable (steering drives scene displacement, Spearman $\rho = 0.81$, vs $-0.18$ for regression). We trace limited single-pass motion to a shared-present anchor and engineer a compact 1.7M-parameter "jump" model that recovers full ground-truth motion magnitude ($1.02\times$ GT), where single-pass models capture less than half.

---

## 6. EWAM: An Enhanced World Action Model for Closed-Loop Online Adaptation in Embodied Intelligence

**Authors:** Xin Zhou, Cong Miao
**arXiv:** [2606.12690](https://arxiv.org/abs/2606.12690)
**Categories:** Robotics (cs.RO); Artificial Intelligence (cs.AI)

In this paper, we propose the Enhanced World Action Model (EWAM), a closed-loop online adaptation architecture built upon a pretrained and fully frozen Cosmos3 backbone network. Evaluated entirely under a zero-shot task protocol, EWAM is centrally focused on reducing the amount of additional deployment data required to adapt to new task layouts. Notably, no extra task-specific demonstration sets were introduced in any of the evaluations, and no fine-tuning was performed on the backbone network. Its performance gains stem entirely from an inference-time co-reasoning mechanism composed of four inserted lightweight neural layers: the Neural Experience Memory Layer located in the intermediate layers of the Diffusion Transformer (DiT) provides task-relevant execution context; the Neural Anomaly Detection Layer after the state prediction head monitors the divergence between predicted and actual states in real time; the Neural Policy Routing Layer dynamically selects direct execution, conservative replanning, or rollback recovery based on the anomaly severity; and the Neural Action Correction Layer refines the generated action chunks using execution diagnostics. Unlike naive feature fusion, the memory, anomaly detection, and correction modules are deeply integrated into the Cosmos3 forward path in a differentiable manner, with only the final routing decision being a discrete supervised one.

---

## 7. Scale Buys Interpolation, Structure Buys a Horizon: Certified Predictability for Equivariant World Models

**Authors:** Hongbo Wang
**arXiv:** [2606.13092](https://arxiv.org/abs/2606.13092)
**Categories:** Machine Learning (cs.LG); Robotics (cs.RO); Dynamical Systems (math.DS)

Scale buys interpolation; structure buys a certified horizon. A world model's average error says nothing about whether a particular prediction can be trusted, or for how long. For equivariant latent world models we give a computable, multi-step certificate of the predictable horizon: $T$-step rollout error is provably constant over each symmetry orbit (Theorem A) and stratified channel-by-channel by the predictor's Lyapunov spectrum, $T_j(\epsilon)\sim\log(1/\epsilon)/\lambda_j$. The horizon is two-sided -- a matching lower bound makes approximate equivariance provably horizon-limited -- and the certificate is exclusive to structure: orbit-constant error characterizes equivariance, so no non-equivariant model has it at any scale. Empirically, on 40-D Lorenz-96 only a $\mathbb{Z}_N$-equivariant network recovers the full Lyapunov spectrum ($R^2{=}0.98$); dense and recurrent baselines fail.
Because the spectrum is faithful, the certificate acts, a priori: under a fixed sensing budget a $c\times$-inflated certificate provably needs $c\times$ the budget, and the equivariant certificate meets a budget its inflated dense counterpart cannot -- with zero calibration data. The same read-out, unchanged, audits public pretrained world models training-free: TD-MPC2 checkpoints land on the certificate's own scope taxonomy -- calibrated where strongly expansive (ratio 0.94-1.02), optimistic where weakly expansive, correctly abstaining where contracting -- a map a deployed monitor replicates cell-by-cell, out-of-sample. Across the official 1M-317M multitask ladder, calibration does not improve with parameters. On V-JEPA 2-AC (1B, real robot data) the measured cross-check correctly overrides an over-promising tangent spectrum -- the cross-validated audit, not the raw number, is the deployable object. Scale buys interpolation, not a calibrated horizon.

---

## 8. EPM-JEPA: Operator-Side Experience Modulation in JEPA-Family World Models

**Authors:** Vedant Pandya
**arXiv:** [2606.12979](https://arxiv.org/abs/2606.12979)
**Categories:** Machine Learning (cs.LG)

JEPA-family world models use a static predictor whose weights do not adapt when test-time dynamics diverge from training. We compare two mechanisms for incorporating accumulated experience into a JEPA predictor under distribution shift: operand-side injection, where a compressed experience representation is added as a residual to the predictor's hidden state (EI-JEPA), and operator-side modulation, where the same representation generates low-rank weight deltas via LoRA applied to the predictor's weights (EPM-JEPA). On a pre-registered comparison (Moving MNIST, gravity shift), EPM-JEPA (D_shift^{n=50} = 0.7848 +/- 0.0078, three seeds) differs from EI-JEPA (0.8238) by delta = 4.74% - Outcome C: a null result - by our stated criterion, a valid outcome. As a secondary, non-pre-registered observation, EPM-JEPA improves 1.90% over a no-memory baseline (0.8000), consistently across seeds, while EI-JEPA underperforms the baseline, indicating the benefit is specific to weight-level modulation. Our primary contribution is a mechanism analysis: the D_shift^{n=50} trajectory reflects three independent dynamical processes - buffer cycling, EMA target drift, and an intrinsic LoRA settling transient of +0.021 - rather than convergence to equilibrium. These findings motivate PEM-JEPA, a physics-grounded successor addressing this dynamical-peak limitation.

---

## 9. ProPlay: Procedural World Models for Self-Evolving LLM Agents

**Authors:** Yijun Ma, Zehong Wang, Yiyang Li, ..., Chuxu Zhang, Yanfang Ye
**arXiv:** [2606.12780](https://arxiv.org/abs/2606.12780)
**Categories:** Machine Learning (cs.LG); Computation and Language (cs.CL)

Self-evolving agents are expected to improve through interaction without external supervision, but this remains difficult in partially observable environments where agents must explore actively, learn from limited feedback, and decide when to trust prior experience. Existing LLM-agent methods often rely on memory or planning modules, yet they rarely close the loop between them to continually refine an internal understanding of environment dynamics. We introduce ProPlay, a procedural world model that supports procedure-level preplay, where agents can rehearse future procedural paths using the learned world knowledge. Rather than representing experience as isolated rules or low-level action constraints, ProPlay abstracts successful trajectories into procedures and organizes them in a procedure graph that captures causal transitions among task stages. Each transition is associated with a reliability record embedding to estimate its task-specific contribution from past outcomes. Before each episode, ProPlay simulates future procedural trajectories over known graph structures as structured soft guidance; after execution, it refines the graph using environment feedback. Experiments on public benchmarks show that ProPlay consistently improves environment understanding and self-evolution capability over strong baselines. Our code has been released in this https URL.

---

## 10. $μ$VLA: On Recurrent Memory for Partially Observable Manipulation in VLA Models

**Authors:** Egor Cherepanov, Nikita Kachaev, Daniil Zelezetsky, ..., Aleksandr I. Panov, Alexey K. Kovalev
**arXiv:** [2606.12497](https://arxiv.org/abs/2606.12497)
**Categories:** Machine Learning (cs.LG); Robotics (cs.RO)

Vision-language-action (VLA) models predict chunks of future actions from the current observation, an assumption that fails under partial observability, where decisions depend on information no longer visible. Existing memory-augmented VLAs simultaneously introduce recurrence, retrieval, compression modules, auxiliary objectives, hierarchical memory, or task-specific architectural changes, so the contribution of recurrence itself remains entangled with surrounding machinery. We present a controlled isolation study of recurrence in a strong pretrained VLA backbone. Our formulation augments the transformer with a small set of learnable memory tokens carried across timesteps and updated through self-attention, trained end to end with truncated backpropagation through time, with no auxiliary losses and no architectural changes. We instantiate this as $\mu$VLA, a family of OpenVLA-OFT variants parameterized by memory width m, TBPTT length K, and the memory update rule (cross-step gradients or a detached EMA), so that recurrence is the only varying factor. On MIKASA-Robo, $\mu$VLA improves average success rate on five training tasks from 0.42 to 0.84 at the strongest setting and reaches 0.23 on held-out tasks with the same memory structure versus 0.07 for the memoryless baseline. On tasks requiring different memory structure, performance remains near baseline. On LIBERO, the strongest recurrent variant achieves 96.2% average success, indicating no regression under full observability. We interpret these results as a calibration of the capability envelope of minimal in-backbone recurrence, identifying the regime in which it is sufficient and the regime where additional memory structure is required. Demos and videos can be found in this https URL.

---

## 11. MaskWAM: Unifying Mask Prompting and Prediction for World-Action Models

**Authors:** Hanyang Yu, Haitao Lin, Jingbo Zhang, ..., Heng Li, Ping Tan
**arXiv:** [2606.13515](https://arxiv.org/abs/2606.13515)
**Categories:** Computer Vision and Pattern Recognition (cs.CV); Machine Learning (cs.LG); Robotics (cs.RO)

World Action Models (WAMs) present a promising paradigm for robotic control via video prediction. However, current WAMs suffer from fundamental spatial bottlenecks: standard text inputs introduce referential ambiguity in cluttered scenes, while unstructured RGB predictions lack semantic grounding and remain biased by task-irrelevant backgrounds. To overcome these limitations, we introduce MaskWAM, an object-centric world-action model. By jointly integrating masks as both explicit inputs and predictions via a unified Mixture of Transformers (MoT), MaskWAM unlocks robust policy generalization. This design provides two key benefits: (1) predicting future masks yields object-centric semantic supervision that suppresses visual noise, significantly enhancing even standard text-conditioned WAMs; and (2) coupling this predictive supervision with first-frame visual prompts, such as target object masks, establishes a precise spatial anchor that substantially reduces language ambiguity. Crucially, as WAMs are inherently vision-driven architectures, direct mask conditioning yields substantially stronger guidance than text alone, establishing a precise and robust paradigm for manipulating unseen objects. Evaluations on LIBERO, RoboTwin, and real-world tasks demonstrate that MaskWAM significantly outperforms baselines in both language-clear and language-ambiguous tasks.

---

## 12. Identifiability Without Gaussianity: Symbolic World Models and Near-Infinite Temporal Consistency

**Authors:** Seth Dobrin, Łukasz Chmiel
**arXiv:** [2606.12471](https://arxiv.org/abs/2606.12471)
**Categories:** Machine Learning (stat.ML); Computation and Language (cs.CL); Emerging Technologies (cs.ET); Machine Learning (cs.LG)

Klindt, LeCun, and Balestriero (arXiv:2605.26379) proved that Joint-Embedding Predictive Architectures (JEPAs) achieve linear identifiability, the linear recovery of the world's true latent variables, if and only if the world's latent dynamics follow a Gaussian, stationary process. This Gaussian boundary implies a fundamental limit on temporal consistency: for any non-Gaussian physical system, the representation error of a statistical World Model grows monotonically with time. We prove that this limit is an artifact of the statistical alignment mechanism, not a property of World Models in general. We introduce the Physics-Grounded Symbolic Architecture (PGSA) and prove three results: (1) a PGSA achieves exact linear identifiability for all physical regimes, regardless of the latent distribution; (2) the per-step error of a PGSA is bounded by numerical precision alone; and (3) as a direct consequence, a PGSA maintains temporal consistency for an unbounded number of transitions, a property we term near-infinite temporal consistency. We further prove that statistical World Models cannot achieve this property for any non-Gaussian system, regardless of model capacity or the volume of training data. The algebraic cores of four of the theorems are formalized in Lean 4 with Mathlib4 v4.31.0 (zero sorry placeholders); the Klindt et al. converse is taken as an external premise. The contrast establishes that symbolic grounding in the causal generator of the world's dynamics is the sufficient condition and, in non-Gaussian regimes, the only condition for near-infinite temporal consistency.

---

## 13. $\texttt{WEAVER}$, Better, Faster, Longer: An Effective World Model for Robotic Manipulation

**Authors:** Arnav Kumar Jain, Yilin Wu, Jesse Farebrother, Gokul Swamy, Andrea Bajcsy
**arXiv:** [2606.13672](https://arxiv.org/abs/2606.13672)
**Categories:** Robotics (cs.RO)

The potential impacts of world models (WMs, i.e., learned simulators) on robotics are far-reaching -- policy evaluation, policy improvement, and test-time planning -- all with limited real-world interaction. To unlock these downstream capabilities, a WM needs to jointly satisfy three desiderata: $\textit{(i)}$ fidelity (i.e., producing simulated trajectories that correlate with reality), $\textit{(ii)}$ consistency (i.e., producing simulated trajectories that are coherent over long horizons), and $\textit{(iii)}$ efficiency (i.e., producing simulated trajectories quickly). We propose $\texttt{WEAVER}$ (World Estimation Across Views for Embodied Reasoning): a WM architecture that simultaneously achieves all three desiderata, providing state-of-the-art results on robotic manipulation tasks. $\texttt{WEAVER}$ is a multi-view WM trained to predict future latents and reward values via a flow-matching loss. We distill the key design decisions across model architecture, memory, and prediction objectives required to unlock the kinds of long-horizon dynamic manipulation tasks that have confounded prior world modeling approaches. We apply $\texttt{WEAVER}$ in robotic hardware, demonstrating its effectiveness at policy evaluation ($\rho$=0.870 correlation with real-world success rate), policy improvement (real-world success rate improvement of $38\%$ on top of the $\pi_{0.5}$ robot foundation model), and test-time planning (real-world success rate improvement of $14\%$ with a $5-10\times$ speedup over prior WMs). $\texttt{WEAVER}$ also demonstrates better performance than prior WMs when evaluated on out-of-distribution scenarios. Code, models, and videos at: this https URL .

---

## 14. NavWAM: A Navigation World Action Model for Goal-Conditioned Visual Navigation

**Authors:** Daichi Azuma, Taiki Miyanishi, Koya Sakamoto, ..., Yusuke Iwasawa, Yutaka Matsuo
**arXiv:** [2606.13494](https://arxiv.org/abs/2606.13494)
**Categories:** Robotics (cs.RO); Computer Vision and Pattern Recognition (cs.CV)

Goal-conditioned visual navigation requires a robot to act under partial observability by anticipating how its motion will change the future egocentric view and whether that change brings it closer to the goal. Navigation world models provide such visual foresight, but they remain prediction modules that require an external planner to convert predicted futures into closed-loop control. We propose Navigation World Action Model (NavWAM), a diffusion-transformer policy that turns navigation world-model prediction into executable action by representing future observations, goal-progress values, and action chunks in a shared latent sequence. By learning future prediction jointly with the action and value targets that determine closed-loop behavior, NavWAM makes visual foresight directly usable for robot control. We build NavWAM through simulation pretraining and real-robot adaptation, and evaluate it on image-goal navigation against planning-based world models and a representative direct navigation policy. Across offline benchmarks and closed-loop real-robot deployment, NavWAM improves over planning-based world-model baselines in our evaluations while using the default policy mode without CEM-style action search. Project page: this https URL

---

## 15. GIVE: Grounding Human Gestures in Vision-Language-Action Models

**Authors:** Pengfei Liu, Gen Li, Junqiao Fan, ..., Yang Xiao, Jianfei Yang
**arXiv:** [2606.13435](https://arxiv.org/abs/2606.13435)
**Categories:** Robotics (cs.RO)

Human communication is inherently multimodal, where language is often accompanied by non-verbal cues such as gestures to convey intentions. However, current Vision-Language-Action (VLA) models treat robotic manipulation as a pure text-driven task, overlooking the important role of gestures in Human-Robot Interaction (HRI). This often leads to inaccurate intent grounding and unreliable manipulation when language instructions are ambiguous or underspecified. To address this challenge, we propose GIVE (Gesture Intent via Visual-Semantic Enhancement), an effective approach that enhances pre-trained VLA models with human gesture understanding without architectural modifications. Specifically, GIVE incorporates gesture information through two complementary pathways: a visual pathway that overlays hand skeletons and fingertip rays onto robot observations for explicit object grounding, and a semantic pathway that generates high-level descriptions of human gestures and task instructions for robust intent grounding. By jointly leveraging visual and semantic guidance, GIVE enables VLA policies to better associate gestures with manipulation behaviors and adapt to dynamic interaction intents. In real-world HRI experiments, GIVE substantially outperforms the baseline, improving target object recognition accuracy by 40% and overall task success rate by 80%, while demonstrating strong robustness and generalization to unseen spatial layouts and diverse participants.

---

## 16. Trajectory-Level Redirection Attacks on Vision-Language-Action Models

**Authors:** Gokul Puthumanaillam, Vardhan Dongre, Pranay Thangeda, ..., Dilek Hakkani-Tür, Melkior Ornik
**arXiv:** [2606.12978](https://arxiv.org/abs/2606.12978)
**Categories:** Robotics (cs.RO); Computer Vision and Pattern Recognition (cs.CV); Systems and Control (eess.SY)

Vision-language-action (VLA) policies bring natural language into closed-loop robot control, enabling robots to execute manipulation tasks directly from text instructions. The same interface gives text a recurring role in control because the prompt is reused at every replanning step, and each prompt-conditioned action changes the future observations on which the policy acts. Existing VLA attacks study adversarial prompts that elicit targeted low-level actions or make such actions persist across changing images. We identify a stronger trajectory-level failure mode: a prompt that still $\textit{appears}$ to specify the intended task but redirects the final physical outcome. We mathematically formalize this setting as $\textit{command-preserving trajectory redirection}$, a prompt-only threat model in which the attacker chooses one prompt before the episode, all policy and environment components remain fixed, and the prompt must stay close to the benign instruction while omitting target words and correction language. To find such prompts, we introduce an on-policy prompt search method that uses rollouts to discover perturbations whose closed-loop behavior tracks a target task while satisfying the command-preserving constraints. Experiments in simulation and on hardware show that near-benign prompt perturbations can redirect VLA rollouts to attacker-specified targets. These results expose a trajectory-level vulnerability in VLA instruction grounding: text that appears to preserve the intended command can still give an adversary control over the robot's final physical outcome. Project website: this https URL

---

## 17. AIR-VLA+: Decoupling Movement and Manipulation via Cascaded Dual-Action Decoders with Asymmetric MoE for Aerial Robots

**Authors:** Jianli Sun, Bin Tian, Qiyao Zhang, ..., Yisheng Lv, Yonglin Tian
**arXiv:** [2606.12859](https://arxiv.org/abs/2606.12859)
**Categories:** Robotics (cs.RO)

Aerial manipulation systems have long suffered from representation coupling in end-to-end control, as platform-level Unmanned Aerial Vehicle (UAV) movement and end-effector-level arm manipulation differ substantially in action scale, dynamics, and control objectives. In this paper, we propose AIR-VLA+, a flow matching action generation architecture specifically designed for aerial manipulation, featuring cascaded dual-action decoders and an asymmetric feature-level Mixture of Experts (MoE). We construct cascaded manipulation and movement decoders, allowing the UAV to unidirectionally observe the manipulator's intent during movement to achieve workflow coordination, while isolating the impact of UAV movement information backpropagation on arm manipulation stability. Addressing the characteristic that UAV movement is highly dependent on high-level semantics and responsible for task state transitions in aerial manipulation, we design an input feature enhancement module for the UAV movement decoder. This module introduces an implicit visual grasp projector to perceive the interaction state between the gripper and the object, and injects compressed global semantic features. Within the UAV movement decoder, we deploy an implicit MoE architecture, enabling different movement experts to spontaneously exhibit capacity inclinations for various task stages during training. Through dense soft blending computation on the feature manifold, the UAV movement is endowed with stronger task-stage adaptability. Experiments on the standardized AIR-VLA benchmark demonstrate that our method comprehensively surpasses all baselines with an overall average score of 48.0. The overall task completion score improves by 80.2\% compared to the single-head $\pi_{0.5}$ policy, effectively mitigating the heterogeneous coordinated control conflicts of composite robots.

---

## 18. Learning to Assist: Collaborative VLAs for Implicit Human-Robot Collaboration

**Authors:** Leo Xu, Letian Li, Alex Cuellar, Michael Hagenow
**arXiv:** [2606.12475](https://arxiv.org/abs/2606.12475)
**Categories:** Robotics (cs.RO)

Human-robot collaboration (HRC) combines the complementary strengths of humans and robots to improve task efficiency. However, many existing collaborative systems rely on hand-engineered pipelines, limiting their scalability and flexibility for new tasks. In this work, we show that models trained end-to-end with imitation learning, specifically vision-language-action (VLA) models, can support collaborative manipulation, and characterize the key factors affecting their real-world performance. We evaluate two state-of-the-art models and identify a failure mode of action-chunking policies in implicit HRC, where demonstration action leakage (i.e., action chunks crossing latent task transitions) can cause premature assistive behavior. We find that this issue increases with longer execution horizons and occurs in real-world collaborative VLA systems, such as when a robot attempts to hand over a tool before the person is ready. We propose an inference-time steering method to mitigate these erroneous assistive actions while preserving policy performance. Finally, through a 16-participant user study on a long-horizon collaborative assembly task, we show that steering enables a longer execution horizon while mitigating premature assistance, leading to faster collaboration and fewer failures compared to a shorter-horizon policy.

---

## 19. RepWAM: World Action Modeling with Representation Visual-Action Tokenizers

**Authors:** Junke Wang, Qihang Zhang, Shuai Yang, ..., Yu-Gang Jiang, Yinghao Xu
**arXiv:** [2606.13674](https://arxiv.org/abs/2606.13674)
**Categories:** Computer Vision and Pattern Recognition (cs.CV)

This work presents RepWAM, a representation-centric world action model (WAM) built on representation visual-action tokenizers. Existing WAMs typically inherit reconstruction-oriented video tokenizers from pretrained video generation models. Although these tokenizers preserve visual fidelity, pixel reconstruction alone provides limited guidance for learning instruction-following dynamics that connect future prediction with robot control. To address this, we explore a semantic visual-action latent space for representation-centric world action modeling. Specifically, we train a representation visual-action tokenizer that maps visual inputs into aligned visual and latent action tokens. We then pretrain our WAM to jointly model future visual states and the latent actions that connect them under language instructions, followed by adaptation to real robot trajectories for closed-loop manipulation. Experiments on real-world manipulation tasks and simulation benchmarks show that RepWAM delivers strong performance across diverse manipulation settings, while ablations highlight the value of semantic visual-action tokenization over reconstruction-oriented alternatives. These results establish representation visual-action tokenization as a promising foundation for world action models and a step toward generalist robot policies. Code and weights will be available at this https URL.

---

## 20. VISA: VLM-Guided Instance Semantic Auditing for 3D Occupancy World Models

**Authors:** Ruiqi Xian, Yuehan Xian, Jing Liang, Xuewei Qi, Dinesh Manocha
**arXiv:** [2606.13460](https://arxiv.org/abs/2606.13460)
**Categories:** Computer Vision and Pattern Recognition (cs.CV)

Semantic 3D occupancy provides a voxelized world state for autonomous driving and robot decision making, but object and rare-class errors can affect free-space interpretation, collision checking, and temporal state propagation. We show that a common VLM strategy, aligning 3D voxel or object features with crop-caption embeddings, improves text-space similarity without reliably improving closed-set occupancy mIoU. Motivated by this mismatch, we propose VISA, a training-time semantic auditing approach for existing occupancy world models. VISA queries an offline VLM on a representative crop of each physical object instance, obtains a structured audit with class hypotheses, plausible confusions, reliability, attributes, and evidence, and propagates it along the object track. The audit is grounded to matched 3D object voxels and distilled into semantic logits through reliability-weighted taxonomy, attribute-factor, and scene-level audit graph losses, while inference remains unchanged and requires no VLM. On nuScenes, averaged across three runs, VISA improves OccWorld from 19.06 to 20.05 mIoU and GaussianWorld from 21.36 to 21.91 mIoU; on GaussianWorld, object mIoU improves from 18.18 to 19.16 and rare-class mIoU from 15.60 to 16.79. These results suggest that VLMs are better suited to closed-set occupancy as reliability-aware semantic auditors than as generic caption-embedding targets.

---

## 21. MoVerse: Real-Time Video World Modeling with Panoramic Gaussian Scaffold

**Authors:** Yang Zhou, Ziheng Wang, Yuqin Lu, ..., Shengfeng He, Jing Li
**arXiv:** [2606.13376](https://arxiv.org/abs/2606.13376)
**Categories:** Computer Vision and Pattern Recognition (cs.CV)

We present MoVerse, a real-time video world model that creates an interactively navigable scene from a single narrow-field-of-view image. This setting is challenging because the input observes only a small fraction of the environment, while interactive roaming requires a complete surrounding world, persistent geometry, controllable camera motion, and temporally coherent high-fidelity observations. MoVerse addresses this problem by separating world construction from observation rendering. It first expands the input into a gravity-aligned 360$^\circ$ panorama with topology-aware diffusion, closing the missing field of view before 3D reasoning. It then lifts the panorama into a persistent 3D Gaussian scaffold using panoramic geometry-aware residual prediction, yielding a dense and directly renderable spatial memory. Finally, a Gaussian-conditioned video renderer translates scaffold renderings along user-specified camera trajectories into photorealistic video. To make this renderer practical for interaction, we train a bidirectional diffusion teacher for high-quality conditional rendering and distill it into a causal autoregressive student for bounded-latency streaming. This design combines the controllability and long-range consistency of explicit 3D representations with the perceptual quality of generative video models. MoVerse supports real-time scene roaming at 8~FPS on a single NVIDIA RTX~4090 GPU, demonstrating a practical path toward single-image world creation with interactive video output.

---

## 22. VLADriveBench: Evaluating CoT-Action Relationship in VLA for Autonomous Driving

**Authors:** Thach Nguyen, Danhua Guo, Tom Lampo, Fei Wu, Burhan Yaman
**arXiv:** [2606.12706](https://arxiv.org/abs/2606.12706)
**Categories:** Computer Vision and Pattern Recognition (cs.CV)

Vision-language-action (VLA) models generate chain-of-thought (CoT) reasoning alongside driving trajectories, but existing benchmarks evaluate only trajectory quality and do not assess whether the CoT is relevant, consistent, or causally connected to the driving action. We introduce VLADriveBench, a framework that combines observational metrics (mentioning, hallucination, contradiction, action alignment) with a CoT intervention protocol to provide complementary views of the CoT-action relationship. Applying VLADriveBench to three models across two architectures, we find that the two analyses can diverge sharply: ORION scores highest on observational alignment yet its CoT is epiphenomenal, while Alpamayo v1.5 scores lower yet its CoT is strongly causal, with visual salience gating the extent of CoT influence.

---

## 23. Real-Time Execution with Autoregressive Policies

**Authors:** Sangkyu Lee, Seohyeon Park, Tackgeun You, ..., Hwasup Lim, Youngjae Yu
**arXiv:** [2606.13355](https://arxiv.org/abs/2606.13355)
**Categories:** Robotics (cs.RO); Artificial Intelligence (cs.AI)

Real-time execution, enabled by asynchronous inference that ensures both smooth action trajectories and fast reactivity, is critical for realistic deployments of large-scale Vision-Language-Action models. However, recent work on real-time execution primarily focuses on variants of diffusion policies, even though it is more critical for autoregressive policies given their slower rollout speed in synchronous inference. In contrast, we demonstrate that autoregressive policies can achieve real-time execution by adjusting the tokenization horizon and applying constrained decoding, thereby guaranteeing strict latency bounds that enable multi-trajectory decoding to maximize performance. Across simulated and real-world environments, we find that the autoregressive policy consistently outperforms its equivalent-level flow-matching policy counterpart while achieving significantly improved task completion speeds from synchronous inference. Coupled with the inherent advantages of autoregressive policies, such as faster convergence and better generalizability in instruction-following, these results confirm that autoregressive policies can remain a competitive policy type supporting real-time execution.

---

## 24. An Embodied Simulation Platform, Benchmark, and Data-Efficient Augmentation Framework for Wet-Lab Robotics

**Authors:** Zhe Liu, Huanbo Jin, Zhaohui Du, ..., Bin Ji, Ting Xiao
**arXiv:** [2606.12936](https://arxiv.org/abs/2606.12936)
**Categories:** Robotics (cs.RO); Artificial Intelligence (cs.AI)

Wet-lab robots can improve the reproducibility, throughput, and safety of biomedical experiments, but scaling their learning requires customizable simulators for safe and reproducible task generation, open editable laboratory assets, and efficient pipelines that turn limited demonstrations into usable training data. We present Pipette, an embodied simulation platform, benchmark, and data-efficient augmentation framework for wet-lab robot learning. Pipette releases over 43 open-source and re-editable wet-lab assets, together with an extensible asset-building pipeline. A key component of Pipette is its simulation-based data augmentation pipeline, replaying human demonstrations in simulation, applies lighting, camera, speed, and action perturbations, and filters generated episodes with automatic task success checks, rapidly expanding usable training data from limited manual demonstrations. We further introduce an 11-task wet-lab embodied benchmark covering sample handling, culture-ware manipulation, device operation, and precision placement. With only 30 demonstrations per task, ACT achieves 65.5% average success rate, while simulation augmentation improves SmolVLA from 44.1% to 74.7% and {\pi}0 from 40.4% to 46.5%, validating the effectiveness of Pipette for data-efficient VLA training and evaluation. Pipette also supports natural-language-driven scene construction and task registration, lowering the barrier for non-expert users to define new wet-lab robotic tasks.

---
