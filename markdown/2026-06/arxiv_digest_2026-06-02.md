# arXiv Daily Digest — 2026-06-02

**Mode:** direct
**Categories:** cs.AI, cs.LG, cs.RO, cs.CV
**Keywords:** VLA, world model, world action model
**Papers found:** 41

---

## 1. COMAP: Co-Evolving World Models and Agent Policies for LLM Agents

**Authors:** Youwei Liu, Jian Wang, Hanlin Wang, Wenjie Li
**arXiv:** [2606.02372](https://arxiv.org/abs/2606.02372)
**Categories:** Artificial Intelligence (cs.AI); Computation and Language (cs.CL)

Equipping language agents with world models enables them to anticipate environment dynamics and evaluate candidate actions before execution. However, existing textual world models are typically fixed after training, preventing them from adapting to the on-policy state-action distributions induced by an evolving agent. Meanwhile, agent-improvement methods often rely on external rewards or verifiers, limiting their applicability in realistic interactive environments. In this paper, we propose COMAP, a novel framework that co-evolves textual world models and agent policies through closed-loop interaction. At each decision step, the world model predicts future state feedback for candidate actions, and the agent performs future-aware reflection by estimating the reliability of this feedback and refining its action accordingly. The resulting on-policy trajectories are then used to update the world model via self-distillation, allowing it to better match the agent's evolving interaction distribution. Across embodied task planning, Web navigation, and tool-use benchmarks, COMAP consistently outperforms competitive baselines, e.g., +16.75% relative improvement with Qwen3-4B. Further analyses show that the co-evolutionary loop improves the world model's prediction accuracy over time and leads to more effective long-horizon decision-making. Our code is available at: this https URL.

---

## 2. Closed-Loop Neural Activation Control in Vision-Language-Action Models

**Authors:** Abhijith Babu, Ramneet Kaur, Nathaniel D. Bastian, ..., Sumit Kumar Jha, Anirban Roy
**arXiv:** [2606.00269](https://arxiv.org/abs/2606.00269)
**Categories:** Artificial Intelligence (cs.AI)

Vision-Language-Action (VLA) models can be steered at test time by intervening on semantically meaningful internal directions, but existing methods use a fixed steering coefficient, effectively operating in open loop. This is poorly suited to embodied control, where task state and concept error evolve over time, often causing overcorrection, oscillation, and reduced task success, especially for temporal behaviors such as speed and smoothness. We propose CTRL-STEER, a closed-loop framework that replaces static intervention strength with adaptive, time-varying control signals. The key idea is to decouple representation from regulation: rather than assuming temporal concepts are directly controlled by individual neurons, we steer along motion-aligned residual directions while a feedback controller adjusts intervention magnitude online. We instantiate this framework with both PID and reinforcement learning based controllers. Experiments with a fine-tuned OpenVLA policy on four LIBERO task suites show that CTRL-STEER achieves more stable concept regulation and a better steering-task success trade-off than fixed-coefficient baselines, without modifying or retraining the base model.

---

## 3. Policy and World Modeling Co-Training for Language Agents

**Authors:** Ning Lu, Baijiong Lin, Shengcai Liu, ..., Qi Wang, Ke Tang
**arXiv:** [2606.02388](https://arxiv.org/abs/2606.02388)
**Categories:** Machine Learning (cs.LG); Artificial Intelligence (cs.AI)

Reinforcement learning (RL) improves large language model (LLM) agents by teaching them which actions lead to high rewards, but provides little supervision on what those actions do to the environment. World modeling (WM) can fill this gap, yet existing approaches often require separate simulators, extra training stages, or additional inference-time computation. We observe that on-policy RL rollouts already contain the needed signal: each transition pairs an action with its resulting next observation. Based on this observation, we propose PaW, a Policy and World modeling co-training framework that adds auxiliary WM supervision to the same policy during RL, without changing the inference paradigm. To make auxiliary WM supervision informative and stable, PaW introduces three components: action-entropy-based WM data selection, noise-tolerant WM loss, and reward-adaptive loss balancing. Experiments on three agentic task benchmarks show consistent improvements over strong RL baselines across models and RL algorithms. These results suggest that standard RL rollouts are a practical source of WM supervision for language-agent training.

---

## 4. Beyond Task Success: Behavioral and Representational Diagnostics for WAM and VLA

**Authors:** Hung Mai, Bin Zhu, Tuan Do
**arXiv:** [2606.01095](https://arxiv.org/abs/2606.01095)
**Categories:** Robotics (cs.RO); Artificial Intelligence (cs.AI)

Vision-language-action (VLA) policies and World-Action Models (WAM) represent two increasingly important paradigms for robotic manipulation. However, it remains unclear whether future prediction in WAMs leads to behaviorally meaningful improvements beyond final task success. In this paper, we ask whether WAMs merely add future prediction, or whether they change robot behavior and internal representations in ways that are actionable for control. We introduce a model-agnostic diagnostic framework that compares WAMs and VLAs through two complementary lenses: behavioral rollout analysis and sparse-autoencoder-based feature analysis. The behavioral protocol measures action dynamics consistency, target-object progress, distractor disturbance, and runtime cost. The feature-space protocol characterizes internal representations as memorized, reactive, or predictive, revealing whether models encode future-oriented structure. Across LIBERO and RoboTwin2.0, we evaluate 7 policies spanning direct VLAs and joint, sequential, and auxiliary WAMs. Our results show that success alone hides key differences: WAMs often improve object-level behavior and target selectivity, but their gains depend on architecture and incur higher inference cost. Sequential WAMs show the clearest predictive structure, while auxiliary and joint WAMs respectively compress or entangle future information. These findings suggest future directions for WAMs design to preserve behaviorally actionable future representations for efficient manipulation.

---

## 5. Behavior-Invariant Task Representation Learning with Transformer-based World Models for Offline Meta-Reinforcement Learning

**Authors:** Fuyuan Qian, Menglong Zhang, Song Wang, Quanying Liu
**arXiv:** [2606.00780](https://arxiv.org/abs/2606.00780)
**Categories:** Machine Learning (cs.LG); Artificial Intelligence (cs.AI)

Offline meta-reinforcement learning leverages static datasets to enable agents to generalize to unseen environments by combining offline efficiency with meta-learning adaptability, yet it faces key challenges from context and policy distribution shifts. These issues hinder agents from adapting to online environments, and are further exacerbated under sparse-reward settings. As a result, agents often become trapped in an inherent pattern dilemma, failing to achieve robust generalization. In this work, we propose a novel framework that integrates information-theoretic task representation learning with a Transformer-based stochastic world model. Our approach extracts task-defining latent variables that are invariant to behavior policy, thereby effectively mitigating the context distribution shift. To further handle policy shift and model exploitation, we apply a conservative value penalty to imagination-based rollouts, preventing the policy from exploiting model inaccuracies while maintaining robust adaptation. Extensive evaluations demonstrate that our method outperforms state-of-the-art approaches, with superior stability and generalization under out-of-distribution and sparse-reward settings.

---

## 6. PaCo-VLA: Passivity-Shielded Compliance Prior for Contact-Rich Vision-Language-Action Manipulation

**Authors:** Haofan Cao, Zhaoyang Li, Zhichao You, Liang Guo, Tianrui Li
**arXiv:** [2606.00515](https://arxiv.org/abs/2606.00515)
**Categories:** Robotics (cs.RO); Artificial Intelligence (cs.AI); Systems and Control (eess.SY)

Contact-rich manipulation demands both high-level semantic reasoning and the safe regulation of high-frequency contact dynamics. While Vision-Language-Action (VLA) models provide unprecedented semantic generalization, their low-rate outputs lack the reliability required for direct plant authority in force-sensitive tasks. To bridge this semantic-to-control gap, we introduce PaCo-VLA, a passivity-shielded compliance prior that recasts the VLA interface. Rather than trusting VLAs with direct motor commands, PaCo-VLA treats network outputs as task-level compliance proposals: semantic bindings, task stages, and admittance schedules. A high-frequency, proposal-independent passivity shield governs these proposals through energy-tank accounting and boundary checks, preventing invalid, stale, or unverified model predictions from bypassing low-level contact physics. This decoupled architecture also enables causal evaluation, isolating semantic contributions from geometric shortcuts. Extensive simulated and real-world connector-insertion experiments demonstrate that PaCo-VLA achieves superior precision over unshielded VLA baselines, sustaining zero passivity violations even under adversarial compliance shifts. This framework establishes a provably sampled-passive runtime contract at the admittance port and provides a runtime interface for deploying foundation models in contact-rich domains.

---

## 7. StressDream: Steering Video World Models for Robust Policy Evaluation and Improvement

**Authors:** Junwon Seo, Sushant Veer, Ran Tian, ..., Marco Pavone, Andrea Bajcsy
**arXiv:** [2606.00267](https://arxiv.org/abs/2606.00267)
**Categories:** Computer Vision and Pattern Recognition (cs.CV); Artificial Intelligence (cs.AI); Machine Learning (cs.LG); Robotics (cs.RO)

Video world models (WMs) have shown promise for policy evaluation and improvement by imagining realistic future observations conditioned on ego-robot actions. While WMs can model distributions over futures, policy evaluation and improvement typically rely on nominal imaginations, which can miss high-impact outcomes of robot actions unless prohibitively many samples are drawn. To enable robust policy evaluation and improvement over WM imaginations, we propose StressDream, which steers imaginations toward high-impact yet plausible outcomes specified at inference time by optimizing the initial noise of diffusion-based WMs. However, optimizing high-dimensional noise is challenging: the optimization must reason about nuanced, scene-dependent target events in generated videos while avoiding out-of-distribution (OOD) noise that yields implausible imaginations. We address this with two complementary objectives: a semantic objective with a Vision-Language Model that provides informative gradients by reasoning about the generated video, and a plausibility objective that prevents the optimized noise from drifting OOD. With state-of-the-art video world models for autonomous driving and robotic manipulation, we show that StressDream effectively steers imaginations toward high-impact yet plausible outcomes specified by text at inference time, such as task failures, enabling robust policy evaluation and improvement by identifying actions whose plausible futures include undesirable outcomes. Video results are available at this https URL.

---

## 8. Continuous Reasoning for Vision-Language-Action

**Authors:** Yueh-Hua Wu, Tatsuya Matsushima, Kei Ota
**arXiv:** [2606.00229](https://arxiv.org/abs/2606.00229)
**Categories:** Robotics (cs.RO); Artificial Intelligence (cs.AI); Machine Learning (cs.LG)

Natural language is a powerful reasoning medium for language and vision-language models, but it is mismatched to the granularity of continuous control. Text and explicit subgoals operate at task-level granularity, whereas vision-language-action (VLA) policies must choose actions at a much finer temporal scale; a single reasoning step can therefore span many action chunks while remaining only weakly coupled to the action needed now. This suggests a different question for VLA: what should play the role of language? We argue that a useful VLA reasoning medium must be shareable across model instances, verifiable through downstream action improvement, and aligned with temporally extended control structure.
Based on this view, we propose Continuous Reasoning for Vision-Language-Action. Our model first predicts continuous reasoning in the form of a structured set of continuous thoughts, then reuses them as shared context for chunk-structured action generation. Better action prediction alone does not certify good reasoning: if the same internal medium cannot be shared across model instances and independently verified through improved downstream control, the added latent may simply become a model-private shortcut that helps on seen behaviors without supporting generalizable control. We therefore instantiate continuous reasoning as a shared Gaussian latent interface and train it with a self-verification objective in which an exponential-moving-average teacher must successfully consume the student's reasoning when predicting target actions.
Empirically, Continuous Reasoning improves LIBERO-PRO robustness and performs strongly on real robots, raising mean subtask success over {\pi}0.5 by 40.4% on TX-G2, an AgiBot G2-compatible variant, and 26.3% on HSR. This suggests that reasoning in VLA is less about extra tokens than about a shareable, verifiable internal language for action.

---

## 9. From Human Videos to Robot Manipulation: A Survey on Scalable Vision-Language-Action Learning with Human-Centric Data

**Authors:** Zhiyuan Feng, Qixiu Li, Huizhi Liang, ..., Jiaolong Yang, Baining Guo
**arXiv:** [2606.00054](https://arxiv.org/abs/2606.00054)
**Categories:** Robotics (cs.RO); Artificial Intelligence (cs.AI); Computer Vision and Pattern Recognition (cs.CV)

Recent progress in generalizable embodied control has been driven by large-scale pretraining of Vision-Language-Action (VLA) models. However, most existing approaches rely on large collections of robot demonstrations, which are costly to obtain and tightly coupled to specific embodiments. Human videos, by contrast, are abundant and capture rich interactions, providing diverse semantic and physical cues for real-world manipulation. Yet, embodiment differences and the frequent absence of task-aligned annotations make their direct use in VLA models challenging. This survey provides a unified view of how human videos are transformed into effective knowledge for VLA models. We categorize existing approaches into four classes based on the action-related information they derive: (i) latent action representations that encode inter-frame changes; (ii) predictive world models that forecast future frames; (iii) explicit 2D supervision that extracts image-plane cues; and (iv) explicit 3D reconstruction that recovers geometry or motion. Beyond this taxonomy, we highlight three key open challenges in this area: structuring unstructured videos into training-ready episodes, grounding video-derived supervision into robot-executable actions under embodiment and viewpoint heterogeneity, and designing evaluation protocols that better predict real-world deployment performance and transfer efficiency, thereby informing future research directions. A curated list of papers and resources is available at this https URL.

---

## 10. IMWM: Intuition Models Complement World Models for Latent Planning

**Authors:** Baoqi Gao, Ruize Han, Miao Wang, Song Wang
**arXiv:** [2606.01626](https://arxiv.org/abs/2606.01626)
**Categories:** Machine Learning (cs.LG)

Planning with a learned latent world model is a promising route to control from raw pixels, but a strong world model alone is not enough. We show this experimentally: even with a perfect world model (operationalized by replacing the learned forward predictor with an idealized rollout of the true environment dynamics), a finite-budget sample-based planner still fails on some tasks, indicating that the bottleneck can lie in search rather than in world-model accuracy. Motivated by this gap, we propose IMWM (Intuition Model + World Model), which pairs the world model with an intuition model trained from demonstrations to recognize promising actions. The two models collaborate through three lightweight components: (i) Retrieval Initialization, which initializes the planner's action proposal from a retrieved demonstration; (ii) Hybrid Cost, which combines the intuition score with the world-model rollout cost; and (iii) a Reliability Gate, which adjusts how much the planner trusts intuition in each setting. Across four pixel-based goal-reaching tasks (Two-Room, Reacher, Push-T, and OGBench-Cube), IMWM has higher mean success than the world-model-only planner on all four, with the largest gains on Two-Room (99.2%, +11.5 percentage points) and OGBench-Cube (94.7%, +28.5 percentage points).

---

## 11. World Models: A Comprehensive Survey of Architectures, Methodologies, Reasoning Paradigms, and Applications

**Authors:** Arif Hassan Zidan, Yi Pan, Hanqi Jiang, ..., Tianming Liu, Wei Zhang
**arXiv:** [2606.00133](https://arxiv.org/abs/2606.00133)
**Categories:** Machine Learning (cs.LG); Emerging Technologies (cs.ET)

World models, internal simulators that learn the structure and dynamics of an environment, have emerged as a central paradigm in the pursuit of artificial general intelligence, enabling agents to predict, plan, and reason within learned representations. Despite rapid progress across reinforcement learning, robotics, autonomous driving, and video generation, the field lacks a unified framework integrating its diverse architectural choices, training methods, reasoning mechanisms, and application settings. This survey addresses that gap with a multi-axis taxonomy organized along four dimensions: (i) architecture, encompassing representation format, dynamics formulation, input modality, learning paradigm, and downstream application; (ii) methodological family, including state-space and recurrent approaches, transformer-based models, diffusion-based generators, physics-informed networks, and language-augmented multimodal systems; (iii) reasoning strategy, covering imagination-based planning, latent policy learning, counterfactual reasoning, and planning under uncertainty; and (iv) application domain, spanning robotics, autonomous driving, video prediction, multimodal agents, reinforcement learning, scientific modeling, medical imaging, educational measurement, and business and finance. Tracing the field from early cognitive-science foundations to milestone systems such as PlaNet, the Dreamer family, MuZero, Sora, Cosmos, and Genie, we examine how these dimensions interact and highlight the recent convergence of chain-of-thought reasoning with world-model imagination. We review evaluation protocols and benchmarks, identify persistent challenges such as compounding prediction errors, sim-to-real transfer, and fragmented evaluation, and outline future directions toward unified multimodal world models, foundation-scale interactive simulators, and safe deployment in safety-critical domains.

---

## 12. Learning Action-Conditional and Object-Centric Gaussian Splatting World Models for Rigid Objects

**Authors:** Jens U. Kreber, Lukas Mack, Joerg Stueckler
**arXiv:** [2606.01950](https://arxiv.org/abs/2606.01950)
**Categories:** Robotics (cs.RO); Computer Vision and Pattern Recognition (cs.CV); Machine Learning (cs.LG)

World models enable intelligent agents to predict the consequences of their actions on the environment. In this paper, we propose Multi Rigid Object Gaussian World Model (MRO-GWM), a novel model that learns action-conditional dynamics of rigid objects in 3D. By representing the scene by object-centric Gaussians, we can represent arbitrary object shapes and multi-object scenes. We develop a novel spatio-temporal transformer architecture that predicts future rigid body motion from a history of object Gaussians and future actions. Objects are represented by their Gaussians in a canonical frame, which allows for describing object motion as rigid body transformation. Our model is trained on reconstructions from multiple viewpoints, which requires the model to handle partial observations of objects due to occlusions. We analyze prediction performance of our approach on synthetic datasets composed of typical household objects with multi-object dynamics and interactions by a robot end effector. We also evaluate our model in model-predictive control for non-prehensile manipulation in simulation.

---

## 13. The Lie We Tell: Correcting the Euclidean Fallacy in Vision Language Action Policies via Score Matching on Tangent Space

**Authors:** Bing-Cheng Chuang, I-Hsuan Chu, Bor-Jiun Lin, ..., Min Sun, Chun-Yi Lee
**arXiv:** [2606.01847](https://arxiv.org/abs/2606.01847)
**Categories:** Robotics (cs.RO); Machine Learning (cs.LG)

Diffusion-based Vision-Language-Action policies achieve remarkable success in robotic manipulation, yet commit a fundamental geometric error we term the $\textbf{Euclidean Fallacy}$: representing SE(3) poses as flat $\mathbb{R}^{12}$ vectors. This approximation induces (1) manifold drift violating SO(3) constraints, (2) broken equivariance under coordinate transformations, and (3) non-geodesic trajectories with excessive kinematic cost. We introduce $\textbf{Lie Diffuser Actor (LDA)}$, a diffusion framework operating intrinsically on SE(3). Our method injects noise through left-invariant SDEs, predicts scores in the tangent space, and retracts samples via the exponential map. This formulation eliminates manifold drift by construction while guaranteeing coordinate-frame equivariance and geodesic optimality. On CALVIN ABC$\rightarrow$D, LDA improves average task length from $3.27$ to $3.51$ ($+7.3\%$). We further validate our method on real robot and the results show that our methodology outperforms the baseline on majority tasks.

---

## 14. Per-Group Error, Not Total MSE: Fine-Tuning Vision-Language-Action Models for 11-DoF Mobile Manipulation

**Authors:** Pau Montagut Bofi, Mario García Blasco, Tessa Pulli, Markus Vincze
**arXiv:** [2606.00253](https://arxiv.org/abs/2606.00253)
**Categories:** Robotics (cs.RO); Machine Learning (cs.LG)

Fine-tuning Vision-Language-Action (VLA) models for mobile manipulators with heterogeneous joint spaces can produce a counterintuitive result: the checkpoint with the lowest aggregate MSE is not the one that performs best on the real robot. We argue this is a predictable consequence of collapsing heterogeneous joint groups (arm, gripper, head, wheeled base) into a single metric, where easy-to-predict joints can mask joints that still fail.
We fine-tune SmolVLA (450M, action-expert only) on the 11-DoF Toyota HSR and compare it against $\pi_{0.5}$ (3.3B), a stronger pretrained baseline. Per-group analysis exposes two patterns: in SmolVLA, the mobile base converges slowest and limits overall performance. In expert-only fine-tuning of $\pi_{0.5}$ (training only the action head, backbone frozen), total MSE drops below the baseline but arm accuracy degrades. On 60 real-robot trials (20 per model), $\pi_{0.5}$ 80k (4.0/4) significantly outperforms both fine-tuned variants (expert-only 3k: 3.75/4; HSR-SmolVLA: 3.5/4; Mann-Whitney $p \leq 0.010$), despite expert-only 3k having the lowest total MSE. This separation is most consistent with the offline arm-group error, not total MSE or base-group error. We conclude that per-group error is a more reliable signal than total MSE for checkpoint selection on robots with heterogeneous action spaces. Code: this https URL

---

## 15. RoboDream: Compositional World Models for Scalable Robot Data Synthesis

**Authors:** Junjie Ye, Rong Xue, Basile Van Hoorick, ..., Vitor Guizilini, Yue Wang
**arXiv:** [2606.02577](https://arxiv.org/abs/2606.02577)
**Categories:** Robotics (cs.RO); Computer Vision and Pattern Recognition (cs.CV)

Scaling robot learning requires large-scale, diverse demonstrations, yet real-world data collection via teleoperation remains prohibitively expensive and time-consuming. While video diffusion models offer a promising avenue for data scaling, existing generative approaches are often limited to superficial visual augmentation, or suffer from embodiment hallucinations that yield physically infeasible motions. We present a generalizable embodiment-centric world model that achieves scalable data generation by synthesizing photorealistic demonstrations with novel objects, in novel scenes, and from novel viewpoints. Our approach anchors generation to rendered robot motion while conditioning on explicit scene and object priors, effectively decoupling trajectory execution from environment synthesis. This formulation has the potential to unlock two powerful data scaling capabilities: (1) retrieval and rebirth, which repurposes existing trajectories into entirely new contexts without new motion data; and (2) prop-free teleoperation, where operators manipulate empty air and the model hallucinates the target objects and scene afterwards, eliminating reset time. We demonstrate with real-world experiments that our generated data consistently improves downstream policy performance and significantly reduces real-world data requirements across diverse manipulation tasks.

---

## 16. Intercepting the Future: Latent-Space Predictive World Model for Dynamic VLA Manipulation

**Authors:** Shahram Najam Syed, Arthur Jakobsson, Haoran Hao, Jeffrey Ichnowski
**arXiv:** [2606.02486](https://arxiv.org/abs/2606.02486)
**Categories:** Robotics (cs.RO)

Vision-Language-Action (VLA) models generalize across static manipulation but fail when objects move during task execution. They map the current observation to an action and assume the scene is stationary between observation and execution, so at any non-trivial object speed the resulting latency exceeds the time available to grasp. We close this gap with AHEAD (Anticipatory Horizon Extrapolation with Adaptive Dynamics), a predict-then-act wrapper that augments a frozen VLA with a motion-aware latent world model. A small world model trained on manipulation video forecasts future patch tokens in the VLA's feature space, conditioned on per-token velocity and acceleration from optical flow. A language-and-motion saliency mask concentrates prediction on task-relevant patches, and the model rolls forward for an adaptive horizon, halting when prediction uncertainty crosses a threshold. The frozen action decoder then receives the predicted future tokens in place of the current ones. AHEAD adds 4.9M parameters to a frozen 7B OpenVLA and reaches 79 to 97% success across 20 dynamic simulation scenarios where the strongest baseline reaches 31 to 58%. On a physical UFactory xArm 7, AHEAD succeeds on 29/30 to 30/30 on three conveyor and rolling-ball tasks, 23/30 on paddle interception, and 19/30 on projectile catching where every baseline scores 0/30.

---

## 17. Towards Precise Intent-Aligned VLA Aerial Navigation via Expert-Guided GRPO

**Authors:** Tianyang Chen, Wenjun Li, Xin zhou, Yuze Wu, Fei Gao
**arXiv:** [2606.02313](https://arxiv.org/abs/2606.02313)
**Categories:** Robotics (cs.RO)

Vision-Language-Action (VLA) models offer a promising end-to-end paradigm for unmanned aerial vehicles (UAVs) to accomplish complex tasks specified by fine-grained instructions. However, standard supervised fine-tuning (SFT) suffers from data scarcity, limited generalization, and weak supervision for nuanced and complicated human intents. Reinforcement fine-tuning offers a natural way to mitigate these challenges and align policy behaviors with human intents through designable feedback, but applying it to aerial navigation remains challenging due to inefficient exploration in expansive continuous spaces. To address these challenges, we introduce an efficient reinforcement learning (RL) framework for VLA-based aerial navigation. At its core, we propose EG-GRPO (Expert-Guided Group Relative Policy Optimization) to augment online rollouts with few-shot expert data. Additionally, we design a heterogeneous pipeline enabling parallel simulation and inference, which reduces rollout time by 43.5%. Across multiple tasks specified by complex human intents, EG-GRPO improves the success rate to 2.13x that of the SFT baseline, while improving intent alignment performance by 60.9%. These results demonstrate that our framework can move aerial navigation toward precise intent-aligned flight.

---

## 18. FATE-VLA:Failue-aware test generation for vision-language-action models

**Authors:** Arusa Kanwal, Pablo Valle, Shaukat Ali, Aitor Arrieta
**arXiv:** [2606.02307](https://arxiv.org/abs/2606.02307)
**Categories:** Robotics (cs.RO)

Vision-Language-Action (VLA) models are increasingly used as generalist robot policies, yet their evaluation still relies largely on static benchmarks that randomly sample task scenes. In high-dimensional embodied spaces, failures are sparse and clustered, so static benchmarking can underestimate robustness risks. We reframe VLA evaluation as an active failure-discovery problem and propose a failure-aware test-generation approach that combines diversity-driven exploration with surrogate models learned from observed executions. The method steers testing toward high-risk yet diverse scene regions. Across four state-of-the-art VLA models, it uncovers substantially more failures (up to +29.7 % over selected baselines) while revealing more diverse failure modes. This mean that, for instance, in the case of GR00T-N1.6, success rate dropped from 64.4% to 34.7%. More broadly, our findings call for a shift in VLA evaluation: from passive measurement on fixed task suites to adaptive, failure-seeking test generation that exposes the structure of model weaknesses before deployment.

---

## 19. RoboSemanticBench: Diagnosing Semantic Grounding in Action Prediction for VLA Models

**Authors:** Bin Yu, Yao Zhang, Haishan Liu, ..., Cong Huang, Kai Chen
**arXiv:** [2606.02277](https://arxiv.org/abs/2606.02277)
**Categories:** Robotics (cs.RO)

Vision-language-action (VLA) models are built on the premise that semantic understanding from pretrained language or vision-language backbones should guide robot action prediction. Yet robot fine-tuning is optimized as imitation over task-specific action distributions, and many evaluations can be solved through visual or instruction-action shortcuts. We introduce RoboSemanticBench (RSB), an embodied benchmark for diagnosing semantic grounding in action prediction: whether post-trained VLA models can use complex instruction semantics to select and manipulate the correct physical target. In each episode, a robot receives a multiple-choice math or general-knowledge question, observes candidate answer blocks, and must grasp the block corresponding to the correct answer. RSB covers controlled arithmetic, grade-school mathematical understanding, and commonsense or factual understanding under four-choice and ten-choice suites. Across representative VLA models, we find that many policies learn to grasp candidate blocks but select the semantically correct block at near-random or below-random rates after controlling for grasp success, revealing a persistent gap between backbone-level semantic competence and action prediction.

---

## 20. WALL-WM: Carving World Action Modeling at the Event Joints

**Authors:** Shalfun Li, Victor Yao, Charles Yang, ..., Hao Wang, Qian Wang
**arXiv:** [2606.01955](https://arxiv.org/abs/2606.01955)
**Categories:** Robotics (cs.RO); Computer Vision and Pattern Recognition (cs.CV)

WALL-WM is a World Action Model that shifts video-action learning from chunk-centric optimization to event-grounded Vision-Language-Action pretraining, using semantically coherent action events as the atomic unit of learning. Existing WAMs commonly initialize from multimodal or video foundation models and then optimize fixed-length action chunks conditioned directly on the current observation and instruction. Although convenient, this chunk-centric formulation creates a fundamental granularity mismatch. Language describes semantic goals and events, vision evolves through continuous scene dynamics, and actions operate at control-level timescales; forcing all three into the same fixed-length prediction window turns VLA training into short-horizon correlation fitting. WALL-WM addresses this mismatch by organizing both supervision and data around semantic events. Specifically, it pairs event-grounded VLA pretraining with a data ecosystem built from event-level captions and cluster-balanced sampling, enabling scalable learning over diverse behaviors, scenes, and task structures. From the same event-pretrained backbone, WALL-WM supports two complementary inference modes. The event mode consumes next-event descriptions and enables variable-length execution chunks, while the unified mode uses a VLM with Staircase Decoding to condition conventional fixed-length chunk inference while preserving a gradient-continuous VLA path. Together with Muon-optimizer-based large-scale pretraining infrastructure, WALL-WM provides a practical scale-up recipe for general-purpose WAMs. Experiments show that WALL-WM generalizes broadly across language, scenes, and tasks, achieving state-of-the-art performance in large-scale real-world generalization evaluation.

---

## 21. LEGS: Fine-Tuning Teleop-Free VLAs for Humanoid Loco-manipulation in an Embodied Gaussian Splatting World

**Authors:** Hojune Kim, Timothy Chen, Jiankai Sun, ..., Ke Wang, Mac Schwager
**arXiv:** [2606.01458](https://arxiv.org/abs/2606.01458)
**Categories:** Robotics (cs.RO)

Training vision-language-action (VLA) policies for humanoid loco-manipulation is constrained by the high cost and complexity of collecting human teleoperation demonstrations. VLA policies fine-tuned in simulators have, until now, failed to transfer effectively in humanoid loco-manipulation tasks. We present LEGS (Loco-manipulation via Embodied Gaussian Splatting), a hybrid simulator that composites a mesh foreground (robot, objects, props) over a photorealistic 3D Gaussian Splatting (3DGS) background reconstructed from a handheld scene capture. LEGS uses a procedural motion-primitive generator to synthesize labeled demonstrations at scale without human teleoperation, and a deterministic two-stage color calibration to align the rendered 3DGS image to the robot's deployment camera. On a Unitree G1 humanoid robot, across three pick-and-place tasks of increasing whole-body difficulty and three VLA backbones (psi_0, pi_0.5, GR00T N1.6), a policy trained purely on LEGS data matches or exceeds one trained on human teleoperation demos on every experiment. It also outperforms a mesh-only simulation baseline that ablates the effect of the 3DGS background, showing that photorealistic rendering is a key enabler for synthetic data transfer. Humanoid motion is recorded independently of scene appearance in LEGS, allowing the same auto-generated demonstrations to be re-rendered under new backgrounds and object meshes--covering a new scene at more than 15x lower cost than teleoperation--to augment training data for robustness to scene variations. Under combined object-and-scene appearance shift, the policy trained on re-rendered LEGS-AUG data maintains task success while the baseline trained on teleoperation data fails entirely. Our project page is located at this https URL.

---

## 22. OneVLA: A Unified Framework for Embodied Tasks

**Authors:** Lingfeng Zhang, Xiaoshuai Hao, Yingbo Tang, ..., Long Chen, Wenbo Ding
**arXiv:** [2606.01241](https://arxiv.org/abs/2606.01241)
**Categories:** Robotics (cs.RO)

Navigation and manipulation are fundamental capabilities of embodied intelligence, enabling robots to interpret natural language commands and interact physically with their surroundings. However, current Vision-Language-Action (VLA) models remain constrained by task-specific architectures, specializing in either navigation or manipulation, which hinders the development of general-purpose robotic agents. To bridge this gap, we introduce OneVLA, a unified architecture that integrates these distinct tasks into a single, cohesive framework. Specifically, we design a unified action head capable of generating both navigation and manipulation actions without requiring task-specific variants. Furthermore, we propose a multi stage progressive training strategy-incorporating curated data construction and Chain-of-Thought (CoT) fine-tuning that facilitates strong positive transfer and mutual reinforcement between the two domains. Extensive experiments in both simulated and real-world environments demonstrate that OneVLA achieves state-of-the-art performance, significantly outperforming both specialized single-task and existing cross-task models. By unifying these core capabilities, OneVLA paves the way for truly general-purpose robotic systems. The model and source code will be publicly released.

---

## 23. ImagineUAV: Aerial Vision-Language Navigation via World-Action Modeling and Kinodynamic Planning

**Authors:** Xuchen Liu, Jiawei Huang, Shihao Xia, ..., Jinqiang Cui, Jiankun Yang
**arXiv:** [2606.01205](https://arxiv.org/abs/2606.01205)
**Categories:** Robotics (cs.RO)

Vision-language navigation (VLN) for UAVs demands grounding free-form instructions into 6-DoF flight under partial observability. While Vision-Language-Action (VLA) models excel at semantic reasoning, they suffer from brittleness due to geometric inconsistency and dynamics mismatch. To address this, we propose ImagineUAV, an imagination-driven framework leveraging cascaded world-action modeling. Instead of direct regression, ImagineUAV employs a latent video diffusion model to generate instruction-conditioned future observations, explicitly imagining environmental evolution, from which 6-DoF motions are inferred via an action extractor. A kinodynamic planner then refines these estimates into collision-free trajectories. Additionally, a step-distilled inference pipeline ensures real-time execution. With only 1.3B parameters, ImagineUAV outperforms prior VLN and VLA baselines on benchmarks and real-world flights, validating the practicality of imagination-driven aerial navigation.

---

## 24. $τ_0$-WM: A Unified Video-Action World Model for Robotic Manipulation

**Authors:** Pengfei Zhou, Shengcong Chen, Di Chen, ..., Zhi Chen, Jianlan Luo
**arXiv:** [2606.01027](https://arxiv.org/abs/2606.01027)
**Categories:** Robotics (cs.RO)

Robotic manipulation requires models that generate executable actions while anticipating and evaluating their future consequences before physical execution. We present $\tau_0$-World Model ($\tau_0$-WM), a unified video-action world model that integrates policy learning, video prediction, and action evaluation within a single future-predictive framework. Built on a shared video diffusion backbone, $\tau_0$-WM provides two complementary interfaces. First, a video action model jointly predicts future visual latents and continuous action chunks from multi-view observations, language instructions, and robot state. Second, an action-conditioned video simulator rolls out candidate action chunks into multi-view futures and predicts dense task-progress scores. The model is trained on approximately $27{,}300$ hours of real-robot teleoperation, UMI-style interaction, egocentric human videos, and rollout or failure trajectories using modality-specific supervision masks. At inference time, $\tau_0$-WM uses test-time computation to sample action candidates, rank them with re-denoising consistency, and invoke simulator-based rectification for low-quality candidates. On challenging long-horizon and fine-grained robotic manipulation tasks, $\tau_0$-WM shows superior performance over other relevant baselines.

---

## 25. Make Your VLA More Robust Without More Data By Interleaving Motion Planning

**Authors:** Dan BW Choe, Sundhar Vinodh Sangeetha, Samuel Coogan, Shreyas Kousik
**arXiv:** [2606.00985](https://arxiv.org/abs/2606.00985)
**Categories:** Robotics (cs.RO)

Vision-Language-Action (VLA) models have shown remarkable progress for mobile manipulation, but their performance on long-horizon tasks remains poor. These tasks are especially challenging because (1) progress toward high-level goals must be maintained across extended sequences of spatially distributed subtasks, and (2) early execution errors compound rapidly over the task horizon. These challenges persist despite finetuning on large human teleoperated mobile manipulation data, indicating that more data alone may not resolve the problem. To address these challenges, we propose MPVI: Motion Planner / VLA Interleaving, a framework that integrates model-based motion planning with VLAs to improve robustness without further training. The proposed integration enables localization and navigation to distant or occluded target objects through cluttered scenes using open-vocabulary object detection, frontier exploration and motion planning. However, such integration is non-trivial, requiring reliable switching between modules; we show one way forward via VLM-based completion checking with proprioceptive triggers. We evaluate our approach on the BEHAVIOR-1K benchmark and demonstrate 113% improvement in task progress over a top end-to-end VLA baseline. Additional details are available at the project page: this https URL.

---

## 26. Threading Optimization for Vision-Language-Action Model Inference in Low-Cost Smart Agricultural Manipulation

**Authors:** Keith Truongcao, Christopher Nhu, Zijian An, ..., Siwei Cai, Lifeng Zhou
**arXiv:** [2606.00966](https://arxiv.org/abs/2606.00966)
**Categories:** Robotics (cs.RO)

Vision-Language Action (VLA) models continue to face challenges such as slow inference speed and difficulty performing fine-grained motion adjustments, limiting their widespread adoption in industry. While the Real-Time Action Chunking (RTAC) algorithm has been proposed to address these bottlenecks, bridging the gap between the algorithm provided in pseudocode to a stable, real-world deployment on a low-cost robotic arm remains a challenge. In this work, we present a complete system-level implementation of RTAC tailored for a low-cost robotic manipulation system. We advance beyond the original high-level pseudocode by optimizing the threading implementation for the policy inference and control pipeline, reducing end-to-end latency and improving responsiveness without modifying the underlying policy. We evaluate this system on tasks involving the manipulation of agricultural produce, specifically garlic bulbs and walnuts. Experimental results demonstrate that our custom threading implementation significantly improves control stability and speed compared to the base implementation of RTAC.

---

## 27. SafeVLA-Bench: A Benchmark for the Success-Safety Gap in Vision-Language-Action Models

**Authors:** Jialiang Fan, Weizhe Xu, Oleg Sokolsky, Insup Lee, Fanxin Kong
**arXiv:** [2606.00773](https://arxiv.org/abs/2606.00773)
**Categories:** Robotics (cs.RO)

Vision-language-action (VLA) benchmarks measure whether a policy completes a requested manipulation task, but binary success can hide safety-relevant trajectory behavior: reaching the goal while applying excessive contact, disturbing bystander objects, destabilizing the held object, or entering robot self-contact. We present SafeVLA-Bench, a post-hoc safety-evaluation framework for existing simulator-based VLA benchmarks. It formalizes task-aware safety requirements as Signal Temporal Logic (STL) specifications and reports native success with two unsafe-success metrics: Succ-But-Unsafe (SBU), the fraction of rollouts that both succeed and violate safety, and Violation Severity Index (VSI), a bounded worst-violation depth score. We instantiate SafeVLA-Bench on LIBERO and RoboCasa-365, evaluating nine policy-benchmark entries across tabletop and kitchen manipulation tasks. High task success does not imply safe execution: high-SR tabletop baselines still leave 13 to 15 percent unsafe-episode rates,and 36 to 56 percent of successful RoboCasa-365 rollouts violate at least one active safety clause. Project page: this https URL.

---

## 28. SKIP: Sparse Keyframe Interpolation Paradigm for Efficient Embodied World Models

**Authors:** Ziheng He, Yixiang Chen, Ning Yang, ..., Nianfeng Liu, Yan Huang
**arXiv:** [2606.00664](https://arxiv.org/abs/2606.00664)
**Categories:** Robotics (cs.RO); Computer Vision and Pattern Recognition (cs.CV)

Embodied world models have emerged as a promising paradigm in robotics by predicting how robot actions affect the surrounding scene. However, the rollout inference remains computationally expensive in pixel space, as long-horizon manipulation videos typically have to be generated frame by frame. This cost cannot be easily reduced by indiscriminately dropping frames, since downstream policies rely on complete preservation of sparse task-relevant events such as approach, contact, grasp, and release. To address this challenge, we propose Sparse Keyframe Interpolation Paradigm (SKIP), an event-preserving sparse-to-dense framework that avoids dense frame-by-frame generation. SKIP first identifies task-relevant keyframes by leveraging robot-aware multimodal features. It then synthesizes only these keyframes with a sparse video diffusion model. A learned gap predictor and an action-conditioned interpolator subsequently reconstruct the missing intervals according to the robot actions. On LIBERO, SKIP generates dense rollouts $4.16\times$ faster than a dense baseline while improving visual fidelity and reducing aggregate FVD by $89.0\%$. Importantly, SKIP-generated videos are effective policy-training data. Even when they fully replace real demonstrations, $\pi_{0.5}$ success drops only $1.3$ pp in LIBERO simulation and $6.7$ pp on the real robot, whereas fully dense frame-by-frame generation collapses by $48$ to $58$ pp.

---

## 29. World Models for Robotic Manipulation: A Survey

**Authors:** Fangyuan Wang, Ziyuan Wang, Guorui Pei, ..., Sichao Liu, Peng Zhou
**arXiv:** [2606.00113](https://arxiv.org/abs/2606.00113)
**Categories:** Robotics (cs.RO)

Robotic manipulation depends on the ability to anticipate how actions reshape objects, contacts, and scene geometry before execution. Learned world models provide this capability by predicting task-relevant future evolution under robot intervention, yet the term now spans latent dynamics models, action-conditioned video generators, three- and four-dimensional scene predictors, physics-informed simulators, and predictive modules inside vision-language-action systems. This breadth has fragmented the literature and obscured the design choices that matter for manipulation. We survey world models for robotic manipulation through three questions: what future representation is predicted, how prediction is connected to action, and when prediction is used in the robot-learning pipeline. We operationally define a world model as an action-conditioned predictive system and distinguish it from perception modules, inverse models, policies, rewards, and value functions. We then organize existing work into five representation families, develop a functional taxonomy that separates integrated prediction-action models from explicit predictive planners, and characterize infrastructure roles including synthetic experience generation, candidate filtering, search-based evaluation, learned environments, and outcome verification. We further map these roles across pretraining, post-training, and inference adaptation, review 34 manipulation datasets, and synthesize evaluation protocols for predictive fidelity, task performance, and simulator reliability. This survey shows that world models are evolving from task-specific dynamics predictors into predictive infrastructure for robot learning, while exposing open challenges in contact modeling, hallucination control, action alignment, and benchmarking under closed-loop use.

---

## 30. VLAMotor: Test-Guided Enhancement of Vision-Language-Action Models via Agent-BasedData Synthesis

**Authors:** Zeqin Liao, Peifan Ren, Zixu Gao, ..., Zibin Zheng, Yang Liu
**arXiv:** [2606.00053](https://arxiv.org/abs/2606.00053)
**Categories:** Robotics (cs.RO)

Vision-Language-Action (VLA) models follow a data-driven paradigm and are constrained by the coverage of training data, making them prone to failure on edge-case configurations after deployment. To mitigate such risks, it is essential to expose high-quality failure modes and convert the resulting failures into supervisory data for model enhancement. Existing studies largely stop at failure detection and lack a mechanism for leveraging discovered failures for model repair.
We propose VLAMotor, the first analysis framework for VLA enhancement, which integrates distance-aware model testing for failure exposure and agent-based data synthesis for model finetunning. First, VLAMotor estimates input uncertainty based on the distance to training samples, and combines uncertainty ranking with redundancy elimination to build compact test sets that expose diverse failures. Then, VLAMotor abstracts failure trajectories into structured semantic representations, and plans parameterized repair-skill sequences, which are then realized as executable trajectories through inverse kinematics and motion execution. The resulting successful trajectories are automatically labeled and used to fine-tune the original VLA model, yielding an enhanced VLA model. Evaluation on four representative robotic manipulation tasks shows that 92.33% of the in-simulation test cases generated by VLAMotor trigger VLA failures, and VLAMotor improves test coverage over the state-of-the-art tool by 18.93%. By fine-tuning VLA models with synthetic data derived from failed test cases, VLAMotor further enhances the overall success rate of VLA models by 49.25%. When deployed on real hardware, the simulation-enhanced models improve the success rate over the original VLA models by 57.50%, demonstrating an effective and low-cost direction for VLA enhancement.

---

## 31. RoboTrustBench: Benchmarking the Trustworthiness of Video World Models for Robotic Manipulation

**Authors:** Huiqiong Li, Jiayu Wang, Zhiting Mei, ..., Jingjing Chen, Bin Zhu
**arXiv:** [2606.01600](https://arxiv.org/abs/2606.01600)
**Categories:** Computer Vision and Pattern Recognition (cs.CV); Computation and Language (cs.CL); Robotics (cs.RO)

Video world models are increasingly used in robotic manipulation, yet existing benchmarks mostly evaluate them under valid, feasible, and safe instructions. We introduce RoboTrustBench, a benchmark for evaluating the trustworthiness of video world models under four scenarios: Normal, Constraint-Sensitive, Counterfactual, and Adversarial. Built from real-world DROID episodes, RoboTrustBench contains 1,207 expert-validated instruction-image pairs and a six-dimensional evaluation protocol with 13 fine-grained criteria. Evaluating seven representative video world models with human and MLLM assessment, we find that current models often generate visually coherent videos, but struggle with constraint reasoning, counterfactual grounding, physical interaction, and unsafe-instruction suppression. These results show that visual quality and surface-level instruction following are insufficient for trustworthy robotic video world modeling.

---

## 32. From Zero to Hero: Training-Free Custom Concept Spawning in World Models

**Authors:** Kiymet Akdemir, Pinar Yanardag
**arXiv:** [2606.02575](https://arxiv.org/abs/2606.02575)
**Categories:** Computer Vision and Pattern Recognition (cs.CV)

Autoregressive world models have emerged as a powerful paradigm for interactive video generation, allowing users to navigate dynamically generated environments through actions. These models are typically conditioned on a text prompt and/or a single reference frame, from which the entire world is generated. Yet the moment the user navigates beyond what is visible in that frame, the unseen regions are populated by the base model's priors, with no mechanism for the user to specify what should appear and where. This is a fundamental limitation for applications such as gaming, interactive storytelling, and simulation, where controllable scene composition is essential. We refer to this missing capability as concept spawning; introducing a user-specified visual concept into a world model, analogous to spawning in a game engine. We introduce SPAWN (Swapping Pinned Anchor with Windowed iNjection), a training-free method for concept spawning. SPAWN exploits a structural property of image-to-video backbones: the first slot of the context memory is pinned to the reference frame and acts as a foundational anchor for every generated chunk. By swapping this anchor with an external concept latent over a short injection window and letting the original anchor return, we cause the concept to propagate naturally through the rollout via the model's own memory. SPAWN supports concepts from fine-grained entities such as characters and props to large-scale elements such as buildings and landmarks, and accepts either a concept image or a text description as input. Experiments show that SPAWN integrates concepts with consistent lighting, scale, and perspective while preserving identity and temporal coherence, demonstrating that controllable concept spawning is achievable in existing autoregressive world models without any training.

---

## 33. Geometry-Aware Implicit Memory for Video World Models

**Authors:** Zhengxuan Wei, Xu Guo, Xinghui Li, ..., Xiangwang Hou, Qi Fan
**arXiv:** [2606.02436](https://arxiv.org/abs/2606.02436)
**Categories:** Computer Vision and Pattern Recognition (cs.CV)

Video world models aim to simulate controllable visual environments, but long-horizon rollouts depend on what the model remembers after observations leave its native context window. Explicit memories retain frames or online 3D reconstructions, which can suffer from heuristic retrieval errors, redundant appearance storage, or reconstruction artifacts. Implicit memories compress history into a compact state, but existing designs are not explicitly constrained to encode cross-view scene geometry. We propose GIM-World, a geometry-aware implicit memory framework for video world models. A lightweight transformer encoder compresses variable-length history into fixed-size memory tokens, a camera-queryable geometry head distills 3D scene structure from a frozen foundation model into the memory during training, and an information-guided pruning rule keeps encoding cost bounded as history grows. The geometry teacher is discarded at inference, leaving a lightweight memory module. Experiments on MIND show that GIM-World better preserves long-horizon geometric and visual consistency than both explicit- and implicit-memory baselines.

---

## 34. Unified Driving Tokens: Representation- and Geometry-Guided Discrete Tokenizer for Driving World Models and Planning

**Authors:** Ziyang Yao, Zeyu Zhu, YunCheng Jiang, Zibin Guo, Huijing Zhao
**arXiv:** [2606.01935](https://arxiv.org/abs/2606.01935)
**Categories:** Computer Vision and Pattern Recognition (cs.CV)

Discrete visual tokens should provide a compact representation for both token-based world modeling and planning in autonomous driving. However, most tokenizers are inherited from image generation and are optimized mainly for pixel reconstruction, which may leave a gap between what is easy to generate and what is useful to decode for driving decisions. We present a representation-guided and geometry-enhanced tokenizer that learns discrete tokens under joint supervision. The tokenizer aligns its discrete bottleneck with a frozen DINO feature space through feature decoding, while preserving appearance via RGB reconstruction with perceptual and adversarial losses. To inject geometric state-related cues, we add adjacent-frame depth and relative-pose supervision during training and stabilize joint objectives with multi-codebook quantization. We evaluate the same learned tokens with a lightweight planning readout and a GPT-style next-token world model. Experiments on NAVSIM show improved reconstruction fidelity and representation consistency, competitive planning performance under a fixed decoder, and better generative quality under matched settings.

---

## 35. Towards Interactive Video World Modeling: Frontiers, Challenges, Benchmarks, and Future Trends

**Authors:** Jiuming Liu, Chaojun Ni, Mengmeng Liu, ..., Ayush Tewari, Per Ola Kristensson
**arXiv:** [2606.01164](https://arxiv.org/abs/2606.01164)
**Categories:** Computer Vision and Pattern Recognition (cs.CV)

With rapid development of large language models and diffusion-based content generation, world modeling has attracted increasing research attention, benefiting various downstream domains such as game engines, embodied AI, autonomous driving, etc. Through explicitly incorporating user actions into world state transition, recent literature empowers world modeling with interactivity in an action-conditioned video or 3D generation paradigm, further enhancing controllability over world evolutions and facilitating users to freely traverse, manipulate, navigate, and personalize the state evolution. In this paper, we aim to systematically review recent research trends, technical developments, evaluation benchmarks, and also propose future potential directions in interactive world modeling. Specifically, we first summarize recent efforts and trends in terms of application scenarios, world state evolution, and scene modality. Afterwards, we delve into three crucial technical challenges, including action-conditioned controllability, long-horizon interactions and memory, and action-following responsiveness for real-time interactivity. Furthermore, we also thoroughly compare existing benchmarks and metrics in four specific application fields: open-world exploration, game engine, autonomous driving, and robotics. Finally, we discuss several promising future directions in achieving next-generation interactive world modeling. The corresponding repository is publicly available at: this https URL.

---

## 36. MBench: A Comprehensive Benchmark on Memory Capability for Video World Models

**Authors:** Shengjun Zhang, Zhang Zhang, Simin Huang, ..., Chen Li, Yueqi Duan
**arXiv:** [2606.00793](https://arxiv.org/abs/2606.00793)
**Categories:** Computer Vision and Pattern Recognition (cs.CV)

Recent advancements in video-based world models have demonstrated an unprecedented ability to synthesize high-fidelity visual sequences. However, a fundamental gap persists between visually plausible video generation and the functional requirements of a world model, particularly in maintaining a stable and reasonable internal state over extended temporal horizons. While existing benchmarks primarily emphasize visual quality, motion coherence, and text-video alignment, they largely overlook memory, the core capability of a world model to preserve consistency across long-term horizons and complex interactions. To address this gap, we present \textbf{MBench}, a comprehensive benchmark dedicated to quantifying and evaluating the memory capability of video world models. We systematically decompose the memory capability of video world models into three hierarchical and complementary core dimensions: entity consistency, environment consistency, and causal consistency, which are further refined into 12 quantifiable sub-dimensions for comprehensive characterization of long-term memory. Our benchmark is built upon rigorously curated real-captured long videos, and evaluated by rule-based quantitative matrices and VLM to enable objective and comprehensive consistency assessment. Extensive evaluations of mainstream state-of-the-art video world models reveal critical systemic limitations of existing methods in long-term state retention, providing a standardized benchmark and clear research direction to advance the field.

---

## 37. Physical Object Understanding with a Physically Controllable World Model

**Authors:** Rahul Venkatesh, Klemen Kotar, Lilian Naing Chen, ..., Stefan Stojanov, Daniel LK Yamins
**arXiv:** [2606.00439](https://arxiv.org/abs/2606.00439)
**Categories:** Computer Vision and Pattern Recognition (cs.CV)

A central challenge in visual intelligence is learning the physical structure of scenes from raw videos: how regions form objects and the laws that govern their interactions. Solving these tasks requires world models capable of inferring distributional states of the world from partial observations - capabilities that current architectures do not provide. We introduce a new class of probabilistic world models that support estimation of the probability of any visual variable, such as appearance and dynamics, conditioned on any other variables. Here, we identify that these models can be trained efficiently with autoregressive sequence modeling, yielding world models from which rich object understanding emerges. First, we demonstrate that our model captures the physical laws governing how objects move by generating multiple plausible future states of the world through sequential inference. Then, by analyzing motion correlations across these futures, we extract objects and articulated object subparts. Having discovered these objects, we show that our world model can manipulate them in 3D. Finally, we demonstrate how physical relationships between objects can be computed from the world model, enabling applications such as Visual Jenga.

---

## 38. World-Task Factorization for Robot Learning

**Authors:** Eduardo Sebastián, Adrian Pfisterer, Vito Mengers, Oliver Brock, Amanda Prorok
**arXiv:** [2606.02027](https://arxiv.org/abs/2606.02027)
**Categories:** Robotics (cs.RO); Machine Learning (cs.LG); Multiagent Systems (cs.MA)

Robot learning must produce policies that generalize to new combinations of constraints, teammates, and environments. To achieve this, we must structurally factor the policy, which is a choice that dictates what generalizes, what requires retraining, and what remains entangled. Existing methods span a wide spectrum, from expecting structure to emerge from data scaling, to hand-designing it via hierarchies, skill libraries or learned specializations. In this paper, we study what we argue is the most fundamental factorization in robotics: separating the world from the task. We investigate the conditions under which this factorization is principled. World factors are properties of the embodied system and the environment; they exist independently of intent. Task factors are defined by the task's logic over what the world admits. We formalize this asymmetry through Bayesian model evidence: it aligns with the data-generating process, maintains high likelihood through an analytical world model, and reduces the Occam razor's penalty on task parameters. We instantiate this factorization by pairing AICON, a differentiable graph of recursive estimators and interconnections that is compositional, operates without task-specific data, and propagates cost gradients to actuators, with a compact, learned policy that modulates gradient paths. Gradients serve as the interface between the two factors: they carry world structure through the graph and task structure through costs, enabling low-dimensional learning while preserving structural generalization. We test the world/task factorization across three problems that encompass heterogeneous robots, environments, task logic and sensorimotor modalities. Our framework outperforms end-to-end baselines and analytical heuristics in all settings, generalizes zero-shot to out-of-distribution configurations, and transfers to real hardware without retraining.

---

## 39. HOIST: Humanoid Optimization with Imitation and Sample-efficient Tuning for Manipulating Suspended Loads

**Authors:** Songyang Liu, Shunyu Yao, Dingyuan Huang, Shuai Li
**arXiv:** [2606.00252](https://arxiv.org/abs/2606.00252)
**Categories:** Robotics (cs.RO); Machine Learning (cs.LG)

Manipulating suspended payloads with humanoid robots is challenging because the robot can only influence an underactuated, oscillatory load through whole-body motion and intermittent contact. Imitation learning provides safe initial behavior but does not directly optimize final placement, while reinforcement learning from scratch is unsafe and sample-inefficient on real humanoids. We present HOIST-Humanoid Optimized with Imitation and Sample-efficient Tuning for manipulating suspended loads. HOIST first finetunes a high-level vision-language-action (VLA) policy from virtual-reality (VR) teleoperation demonstrations and executes its commands through a whole-body controller. It then uses VLA rollouts and iterative batched RL to improve placement accuracy and stopping behavior. Experiments in simulation and on a real humanoid show that HOIST improves over imitation-only and additional-demonstration baselines; compared with pure VLA rollouts, HOIST reduces translational placement error by 19.9 cm and raw angular error by 3.56 degrees, demonstrating the potential of humanoids for underactuated material-handling tasks.

---

## 40. Co-training with Ego-centric Video and Demonstration for Robot Navigation Task

**Authors:** Shoya Kuno, Yumo Ouchi, Kanata Suzuki
**arXiv:** [2606.01951](https://arxiv.org/abs/2606.01951)
**Categories:** Robotics (cs.RO)

Vision-language-action (VLA) models are promising for diverse robotic tasks, but their performance heavily depends on large-scale high-quality training data, whose collection on real robots is costly and time-consuming. While prior work has explored augmenting manipulation datasets with egocentric human videos, applying such approaches to mobile robot navigation remains challenging due to viewpoint changes during locomotion. In this paper, we propose a framework that converts egocentric walking videos into datasets for mobile robot imitation learning. The proposed method estimates camera motion from human videos and transforms it into action representations compatible with ground mobile robots. By jointly training a VLA model on human-derived and robot-collected datasets, the model achieves improved language understanding and more robust action generation than training with either data source alone. Experiments on a fruit-search navigation task demonstrate that human egocentric videos provide an effective and scalable data source for mobile robot learning.

---

## 41. OptiWorld: Optimal Control for Video World Generation under Physical Constraints

**Authors:** Yu Yuan, Jianhao Yuan, Xijun Wang, ..., Lu Ling, Stanley H. Chan
**arXiv:** [2606.00499](https://arxiv.org/abs/2606.00499)
**Categories:** Computer Vision and Pattern Recognition (cs.CV)

Video generation models are becoming a scalable form of world models, but they mainly generate plausible motion rather than proactively control or optimize the underlying dynamics. As a result, an object in the generated video may follow trajectories that are unsafe, not smooth, inefficient, or physically inconsistent. In this work, we propose \textbf{OptiWorld}, a framework that brings classical optimal control into video generation at inference time. OptiWorld first extracts a compact, task-relevant world state, then plans an optimal trajectory under physical constraints, and finally renders the video conditioned on this trajectory. We formulate planning as a geometric problem on a continuous manifold, which converts 3D geometry and task-dependent physical constraints into a unified planning geometry. By adding this optimal-control layer, OptiWorld generates videos with preferable dynamics, demonstrating strong potential in multiple tasks including goal-conditioned image-to-video generation, video dynamics editing, and counterfactual generation.

---
