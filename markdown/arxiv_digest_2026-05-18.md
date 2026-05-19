# arXiv Daily Digest — 2026-05-18

**Mode:** direct
**Categories:** cs.AI, cs.LG, cs.RO, cs.CV
**Keywords:** VLA, world model, world action model
**Papers found:** 19

---

## 1. Learning Bilevel Policies over Symbolic World Models for Long-Horizon Planning

**Authors:** Dillon Z. Chen, Till Hofmann, Toryn Q. Klassen, Sheila A. McIlraith
**arXiv:** [2605.15975](https://arxiv.org/abs/2605.15975)
**Categories:** Artificial Intelligence (cs.AI); Robotics (cs.RO)

We tackle the challenge of building embodied AI agents that can reliably solve long-horizon planning problems. Imitation learning from demonstrations has shown itself to be effective in training robots to solve a diversity of complex tasks requiring fine motor control and manipulation over low-level (LL), continuous environments. Yet, it remains a difficult endeavour to generate long-horizon plans from imitation learning alone. In contrast, high-level (HL), symbolic abstractions facilitate efficient and interpretable long-horizon planning. We propose to combine the strengths of LL imitation learning for manipulation and control, and HL symbolic abstractions for long-horizon planning. We realise this idea via \emph{bilevel policies} of the form $(\pi^{\mathrm{hl}}, \pi^{\mathrm{ll}})$, consisting of a neural policy $\pi^{\mathrm{ll}}$ learned from LL demonstrations, and an HL symbolic policy $\pi^{\mathrm{hl}}$ that is constructed from symbolic abstractions of the LL demonstrations combined with inductive generalisation. We implement these ideas in the BISON system. Experiments on extended MetaWorld benchmarks demonstrate that BISON generalises to long horizons and problems with greater numbers of objects than those solved by VLA and end-to-end methods, and is more time and memory efficient in training and inference. Notably, when ignoring LL execution, BISON's HL policies can solve HL problems with 10,000 relevant objects in under a minute. Project page: this https URL

---

## 2. Deterministic Event-Graph Substrates as World Models for Counterfactual Reasoning

**Authors:** Fabio Rovai
**arXiv:** [2605.15967](https://arxiv.org/abs/2605.15967)
**Categories:** Artificial Intelligence (cs.AI); Computer Vision and Pattern Recognition (cs.CV); Logic in Computer Science (cs.LO)

We study event-graph substrates: a class of world models that represent agent state as an append-only log of typed RDF triples and answer counterfactual queries by forking the log under a structured intervention vocabulary. Substrates are inspectable at the triple level, support exact counterfactuals, and transfer across domains without learned components. We formalize the class, prove a duality between explanatory and counterfactual queries that reduces both to the same causal-ancestor traversal, and evaluate a 1,400-line CLEVRER-DSL interpreter atop a domain-agnostic substrate runtime at full CLEVRER validation scale (n=75,618). The substrate exceeds the NS-DR symbolic oracle on all four per-question categories (by 9.89, 20.26, 17.65, and 0.80 percentage points), and exceeds the parametric ALOE baseline on descriptive and explanatory while lagging on predictive and counterfactual. We also introduce twin-EventLog, a 500-specification Park-canonical Smallville counterfactual benchmark on which the substrate exceeds Llama-3.1-8B with full context by 18.80 points joint accuracy.

---

## 3. Imperfect World Models are Exploitable

**Authors:** Logan Mondal Bhamidipaty, Esmeralda S. Whitammer, David Abel, Mykel J. Kochenderfer, Subramanian Ramamoorthy
**arXiv:** [2605.15960](https://arxiv.org/abs/2605.15960)
**Categories:** Artificial Intelligence (cs.AI); Machine Learning (cs.LG)

We propose a novel definition of model exploitation in reinforcement learning. Informally, a world model is exploitable if it implies that one policy should be strictly preferred over another while the environment's true transition model implies the reverse. We analogize our definition with a prior characterization of reward hacking but show that the associated proof of inevitability does not transfer to exploitation. To overcome this obstruction, we develop a general theory of reward hacking and model exploitation that proves that exploitation is essentially unavoidable on large policy sets and yields the corresponding claim for hacking as a special case. Unfortunately, we also find that the conditions that guarantee unhackability in finite policy sets have no counterpart that precludes exploitation. Consequently, we introduce a relaxed notion of exploitation and derive a safe horizon within which it can be avoided. Taken together, our results establish a formal bridge between reward hacking and model exploitation and elucidate the limits of safe planning in world models.

---

## 4. Offline Semantic Guidance for Efficient Vision-Language-Action Policy Distillation

**Authors:** Jin Shi, Brady Zhang, Yishun Lu
**arXiv:** [2605.16241](https://arxiv.org/abs/2605.16241)
**Categories:** Computer Vision and Pattern Recognition (cs.CV); Artificial Intelligence (cs.AI)

Billion-parameter Vision-Language-Action (VLA) policies have recently shown impressive performance in robotic manipulation, yet their size and inference cost remain major obstacles for real-time closed-loop control. We introduce \textbf{VLA-AD}, a distillation framework that uses a Vision-Language Model as an offline semantic supervisor to transfer large VLA teachers into lightweight student policies. Instead of relying only on low-level action imitation, VLA-AD augments teacher-provided 7-DoF action targets with high-level semantic guidance, including task phase anchors and multi-frame operating-direction descriptions. These auxiliary signals are used only during training: at test time, the student policy runs independently, with neither the VLA teacher nor the VLM required. We evaluate VLA-AD on three LIBERO benchmark suites. Using OpenVLA-7B as the teacher, our method produces a 158M-parameter student, yielding a $44\times$ reduction in model size while matching the teacher with only a $0.27\%$ average relative gap. The resulting policy runs at 12.5 Hz on an RTX 4090, achieving a $3.28\times$ inference speedup over OpenVLA-7B. We further show that the same semantic distillation pipeline generalizes to a different $\pi_{0.5}$-4B teacher, where the student outperforms the teacher on two suites and remains within $0.53\%$ on \texttt{libero\_goal}. Additional analysis indicates that phase-level supervision and multi-frame directional cues make the student less sensitive to noisy teacher actions, such as erroneous high-frequency gripper changes. Overall, VLA-AD demonstrates that offline semantic guidance from VLMs can substantially improve the efficiency, robustness, and deployability of VLA policy distillation.

---

## 5. UAM: A Dual-Stream Perspective on Forgetting in VLA Training

**Authors:** Jianke Zhang, Yuanfei Luo, Yucheng Hu, ..., Tian Lan, Jianyu Chen
**arXiv:** [2605.15735](https://arxiv.org/abs/2605.15735)
**Categories:** Computer Vision and Pattern Recognition (cs.CV); Artificial Intelligence (cs.AI)

Vision--language--action (VLA) models are typically built by fine-tuning a pretrained vision--language model (VLM) on action data. However, we show that this standard recipe systematically erodes the VLM's multimodal competence, a side effect we call the embodiment tax. But do VLAs have to forget? Inspired by the two-stream organization of biological vision, we trace this degradation to a structural bottleneck: current VLAs ask a single encoder to support both language-grounded semantics and control-relevant visual features, whereas biological vision separates recognition and visuomotor control into distinct pathways. Building on this view, we propose the Unified Action Model (UAM), which adds a parallel Dorsal Expert, an analog of the brain's dorsal pathway. To make the Dorsal Expert an effective second pathway and reduce the control-learning burden on the VLM, we initialize it from a pretrained generative model and train it with a mid-level reasoning objective that predicts visual dynamics. This design allows us to train the whole VLA end-to-end on action data alone: with no parameter freezing, no gradient stopping, and no auxiliary VL co-training, UAM retains over $95\%$ of the underlying VLM's multimodal capability and at the same time achieves the highest average success rate among baselines on a variety of manipulation tasks that probe out-of-distribution generalization, including unseen objects, novel object--target compositions, and instruction variation. Together, these results suggest that semantic preservation in VLAs can emerge from architectural separation itself, rather than being enforced by frozen weights or auxiliary data replay, and that this preserved semantic capability can naturally transfer from VLMs to semantic generalization in actions.

---

## 6. Structure Abstraction and Generalization in a Hippocampal-Entorhinal Inspired World Model

**Authors:** Tianqiu Zhang, Muyang Lyu, Xiao Liu, Si Wu
**arXiv:** [2605.15733](https://arxiv.org/abs/2605.15733)
**Categories:** Neural and Evolutionary Computing (cs.NE); Artificial Intelligence (cs.AI); Computer Vision and Pattern Recognition (cs.CV)

Humans abstract experiences into structured representations to facilitate pattern inference and knowledge transfer. While the hippocampal-entorhinal (HPC-MEC) circuit is known to represent both spatial and conceptual spaces, the mechanisms for concurrently extracting abstract structures from continuous, high-dimensional dynamics remain poorly understood. We propose a brain-inspired hierarchical model that simultaneously infers latent transitions and constructs a predictive visual world model. Our architecture employs an inverse model for structural extraction alongside an HPC-MEC coupling model that dissociates relational structures (MEC) from integrated episodic scenes (HPC). Using primitive transformation dynamics as a benchmark, we demonstrate the model's capacity for structural abstraction. By leveraging velocity-driven path integration, the framework enables robust prediction and structural reuse across diverse contexts, thereby achieving structural generalization. This work provides a novel computational framework for understanding how brain-inspired, self-supervised learning of world models facilitates the acquisition of reusable abstract knowledge.

---

## 7. DiLA: Disentangled Latent Action World Models

**Authors:** Tianqiu Zhang, Muyang Lyu, Yufan Zhang, Fang Fang, Si Wu
**arXiv:** [2605.15725](https://arxiv.org/abs/2605.15725)
**Categories:** Computer Vision and Pattern Recognition (cs.CV); Artificial Intelligence (cs.AI); Robotics (cs.RO)

Latent Action Models (LAMs) enable the learning of world models from unlabeled video by inferring abstract actions between consecutive frames. However, LAMs face a fundamental trade-off between action abstraction and generation fidelity. Existing methods typically circumvent this issue by using two-stage training with pre-trained world models or by limiting predictions to optical flow. In this paper, we introduce DiLA, a novel Disentangled Latent Action world model that aims to resolve this trade-off via content-structure disentanglement. Our key insight is that disentanglement and latent action learning are co-evolving: the predictive bottleneck inherent in latent action learning serves as a driving force for disentanglement, compelling the model to distill spatial layouts into the structure pathway while offloading visual details to a separate content pathway for generation. This synergy yields a continuous, semantically structured latent action space without compromising generative quality. DiLA achieves superior results in video generation quality, action transfer, visual planning, and manifold interpretability. These findings establish DiLA as a unified framework that simultaneously achieves high-level action abstraction and high-fidelity generation, advancing the frontier of self-supervised world model learning.

---

## 8. Feedback World Model Enables Precise Guidance of Diffusion Policy

**Authors:** Tuo An, Jindou Jia, Gen Li, ..., Geng Li, Jianfei Yang
**arXiv:** [2605.15705](https://arxiv.org/abs/2605.15705)
**Categories:** Robotics (cs.RO); Artificial Intelligence (cs.AI)

World models aim to improve robotic decision making by predicting the consequences of actions. However, in practice, their predictions often become unreliable once the robot encounters states outside the training distribution, limiting their effectiveness at deployment. We observe that execution itself provides a natural but underutilized signal: after each action, the robot directly observes the true next state, revealing the mismatch between predicted and actual outcomes. Building on this insight, we propose feedback world model, a new paradigm that closes the loop between prediction and observation at inference time. Instead of treating the world model as a static open-loop predictor, our method maintains a lightweight feedback state that is updated online to iteratively correct future predictions, compensating for model errors using real-time observations without additional training data or parameter updates. We show that this process can be interpreted as a latent-space observer and admits convergence guarantees under mild conditions. We further introduce action-aware guidance to better translate corrected predictions into control by emphasizing action-controllable components while suppressing irrelevant variations. Experiments on LIBERO-Plus, Robomimic, and real-world manipulation tasks demonstrate that our method substantially improves both prediction accuracy and policy performance under distribution shift. In particular, it reduces world model prediction error by up to 76.4% and improves out-of-distribution (OOD) success rate by 30%. These results show that incorporating real-time feedback at inference time provides a simple yet powerful alternative to static world modeling.

---

## 9. Latent Video Prediction Learns Better World Models

**Authors:** Ali J Alrasheed, Aryan Yazdan Parast, Basim Azam, James Bailey, Naveed Akhtar
**arXiv:** [2605.15618](https://arxiv.org/abs/2605.15618)
**Categories:** Computer Vision and Pattern Recognition (cs.CV); Artificial Intelligence (cs.AI)

Self-supervised video models are increasingly framed as world models, yet their evaluation remains largely confined to a single top-1 accuracy score on clean benchmarks. This leaves a major gap in comprehending their potential as world models. We present the first systematic study addressing this gap, analyzing four matched-capacity frontier video foundation models, V-JEPA 2.1, V-JEPA 2, VideoPrism, and VideoMAEv2, across five robustness axes relevant to their deployment as video world models: feature discriminability, corruption robustness, fine-grained discrimination, occlusion robustness, and sensitivity to temporal direction. Our evaluations establish that across all five axes, latent-prediction models form a distinct and consistent profile. They degrade more gracefully under pixel corruption, preserve usable class structure rather than mere geometric stability under occlusion, capture fine-grained physical contact cues without reconstructing pixels, and uniquely encode the arrow of time. These advantages can even survive task adaptation: a frozen V-JEPA 2 backbone with a lightweight attentive probe outperforms a fully fine-tuned VideoMAE and a supervised TimeSformer on corruption and occlusion robustness. Our extensive results offer concrete new evidence in favor of latent prediction for robust world modeling.

---

## 10. PanoWorld: Geometry-Consistent Panoramic Video World Modeling

**Authors:** Le Jiang, Xiangyu Bai, Bishoy Galoaa, ..., Yanzhi Wang, Sarah Ostadabbas
**arXiv:** [2605.15391](https://arxiv.org/abs/2605.15391)
**Categories:** Computer Vision and Pattern Recognition (cs.CV); Artificial Intelligence (cs.AI)

We present PanoWorld, a panoramic video world model that generates geometry-consistent 360$\degree$ video from a single image and a caption. Existing panoramic video methods optimize primarily for visual realism and do not explicitly constrain the underlying 3D scene state, producing outputs that appear plausible yet exhibit inconsistent depth, broken correspondences, and implausible motion across the spherical surface. We address this gap by framing panoramic video generation as a geometry- and dynamics-consistent latent state modeling problem rather than pure visual synthesis. Building on a pre-trained perspective video world model, we introduce two lightweight regularizers: a depth consistency loss against pseudo ground-truth panoramic depth, and a trajectory consistency loss that supervises the 3D world-frame positions of tracked points across time. We further apply spherical-geometry-aware adaptation to the conditioning and positional encoding. We additionally introduce PanoGeo, a unified geometry-aware panoramic video dataset with consistent depth, trajectory, and prompt annotations across diverse real and synthetic sources, used for both training and stratified evaluation. Experiments show that PanoWorld improves geometric consistency over prior panoramic generation methods while maintaining competitive visual realism, establishing that panoramic video generation must be treated as a geometric modeling problem to support the holistic spatial understanding requirements of embodied AI applications. Code is available at this https URL.

---

## 11. Learn Where Outcomes Diverge: Efficient VLA RL via Probabilistic Chunk Masking

**Authors:** Vaidehi Bagaria, Nikshep Grampurohit, Pulkit Verma
**arXiv:** [2605.16154](https://arxiv.org/abs/2605.16154)
**Categories:** Machine Learning (cs.LG); Robotics (cs.RO)

Reinforcement learning (RL) allows vision-language-action (VLA) policies to generalize beyond their training distribution by optimizing directly for task success, but post-training is computationally expensive. A natural response has been to speed rollout collection through faster simulators and world models. In GRPO-based VLA RL, we find that the dominant cost lies elsewhere: gradient computation accounts for approximately 78% of wall-clock time per step in our runs, while rollout collection accounts for only 21%. Gradient cost dominates because much of this computation is spent on phases that contribute little to learning. GRPO's learning signal is driven by advantage variance: only phases where successful and failed rollouts diverge produce learning signal. However, GRPO assigns the same advantage to every chunk in a rollout. As a result, actor-update compute is spent uniformly across the trajectory, including phases the policy already handles after pre-training and supervised fine-tuning. This paper presents Probabilistic Chunk Masking (PCM), a drop-in modification to GRPO that allocates gradient computation to a small, probabilistically selected subset of chunks per trajectory. PCM scores semantic phases using success-failure action variance, a rollout-derived proxy for per-phase gradient variance, and samples a fixed chunk budget with online-updated phase-level keep probabilities. We formalize per-phase gradient variance as the quantity determines where gradient computation is useful and show that success-failure action variance provides a measurable proxy for it. PCM requires no reward model or learned critic. On three LIBERO benchmarks, PCM matches the final success rate of standard GRPO while achieving 2.38 times wall-clock speedup, 4.8 times faster gradient updates, and 60% lower peak activation memory, while backpropagating through fewer than 20% of trajectory chunks.

---

## 12. Toward World Modeling of Physiological Signals with Chaos-Theoretic Balancing and Latent Dynamics

**Authors:** Yunfei Luo, Xi Chen, Yuliang Chen, ..., Rakesh Malhotra, Tauhidur Rahman
**arXiv:** [2605.15465](https://arxiv.org/abs/2605.15465)
**Categories:** Machine Learning (cs.LG); Signal Processing (eess.SP)

Physiological time series signals reflect complex, multi-scale dynamical processes of the human body. Existing modeling studies focus on static tasks such as classification, event forecasting, or short-horizon next step prediction, while long-horizon signal-level forecasting and predictive nature of physiological signals remain underexplored. We introduce NormWear-2, a world model that encodes both multivariate physiological signals and clinical intervention variables into a shared latent space and models their joint temporal evolution as a dynamical system. Our approach combines inference from prior pre-trained knowledge (intuition) with instant non-parametric latent state transition adaptation (insight), enabling coherent forecasting across multiple temporal scales, conditioned on heterogeneous clinical interventions. During the pretraining phase, we find that chaos-theoretic balancing of dynamical regime diversity yields more robust representations, with a smaller balanced corpus outperforming one twice its size and capturing bifurcation regimes. We evaluate the world model performance across diverse real-world physiological datasets spanning heterogeneous temporal resolutions and intervention regimes, covering daily life, point-of-care, and clinical settings, including fitness planning, hemodialysis, diabetes management, and surgical monitoring. These evaluation datasets comprise records from 8,026 subjects, spanning study durations from 3.2 hours for high-resolution signal data to 2.3 years for longitudinal clinical biomarker tracking. NormWear-2 achieves the best overall forecasting performance across time, frequency, and latent representation domains, with significant improvements over state-of-the-art time series foundation models, while maintaining competitive downstream representation quality, providing a step toward general-purpose world models for physiological signals.

---

## 13. Health-Conditioned Vision-Language-Action Models for Malfunction-Aware Robot Control

**Authors:** Hüseyin Arslan, Özgür Erkent
**arXiv:** [2605.16056](https://arxiv.org/abs/2605.16056)
**Categories:** Robotics (cs.RO)

Research on Vision Language Action (VLA) models has been increasing rapidly in recent years. Although some of them focus on detecting, preventing, and recovering from task failures, they usually don't deal with adapting to robot's physical failures. In real-life scenarios, most robots face physical degradations in various ways such as joint degradation, actuator failure, or weak gripper. We introduce malfunction-aware (health-conditioned) VLA that takes a health vector as an input that gives information about robots' joints' operation angle and torque capability, and adapts its predictions to complete the tasks with the degraded joints. To achieve this, we inject a Health Projector module to the VLA-Adapter architecture and train it on malfunction robot data we collected on the LIBERO environment [1]. We collect 128 teleoperated episodes on Libero-Spatial tasks. Our results show that, with a very lightweight addition, the model can learn to operate successfully with different configurations of degraded joints which the default pretrained VLA-Adapter's Libero-Spatial-Pro model cannot. The code and dataset will be available soon at this https URL

---

## 14. WorldVLN: Autoregressive World Action Model for Aerial Vision-Language Navigation

**Authors:** Baining Zhao, Jiacheng Xu, Weicheng Feng, ..., Xinlei Chen, Yong Li
**arXiv:** [2605.15964](https://arxiv.org/abs/2605.15964)
**Categories:** Robotics (cs.RO); Computer Vision and Pattern Recognition (cs.CV)

Aerial vision-language navigation (VLN) requires agents to follow natural-language instructions through closed-loop perception and action in 3D environments. We argue that aerial VLN can be formulated as a prediction-driven world-action problem: the agent should anticipate latent world evolution and act according to the predicted consequences. To this end, we propose WorldVLN, the first autoregressive world action model for aerial VLN. Unlike full-sequence video-generation world models that generate an entire visual clip, WorldVLN adapts a latent autoregressive video backbone to predict short-horizon world-state transitions and directly decodes them into executable waypoint actions. After each action segment is executed, newly received observations are encoded back into the autoregressive context, enabling closed-loop world-action prediction. We further introduce a two-stage training framework that first grounds the video prior in instruction-conditioned navigation dynamics and then develops Action-aware GRPO, the first reinforcement learning method tailored to autoregressive WAMs, to optimize waypoint decisions through their downstream rollout consequences. On public outdoor and indoor benchmarks, WorldVLN consistently outperforms existing Vision-Language-Action baselines with 12\%+ success-rate gains and larger advantages on challenging cases. It further transfers zero-shot to real drone deployment, suggesting that the proposed WorldVLN offers a promising route for spatial action tasks. Demos and code are available at this https URL.

---

## 15. EgoExo-WM: Unlocking Exo Video for Ego World Models

**Authors:** Danny Tran, Roberto Martín-Martín, Kristen Grauman
**arXiv:** [2605.15477](https://arxiv.org/abs/2605.15477)
**Categories:** Computer Vision and Pattern Recognition (cs.CV)

Egocentric world models present a promising direction for enabling agents to predict and plan, but their performance is constrained by the limited availability of egocentric training data and its inherent partial observability of humans' physical actions. In contrast, exocentric video is abundant and reveals body poses well, but lacks direct alignment with an agent's action space -- and is not egocentric. We propose a method to bridge this gap by extracting structured body pose from exocentric video as a representation of action and transforming the exocentric video to egocentric video, informed by a human kinematics prior. This process unlocks the integration of in-the-wild exocentric data for egocentric world model training. We show that training whole-body action-conditioned egocentric world models with our converted data significantly improves both prediction quality and downstream planning performance, where we infer the sequence of body poses needed to achieve a visual goal state. Our approach paves the way to enlist arbitrary in-the-wild videos for building powerful egocentric world models, furthering applications in robot planning and augmented-reality guidance.

---

## 16. Entity-Centric World Models: Interaction-Aware Masking for Causal Video Prediction

**Authors:** Santosh Kumar Paidi
**arXiv:** [2605.15466](https://arxiv.org/abs/2605.15466)
**Categories:** Computer Vision and Pattern Recognition (cs.CV)

Learning predictive world models from unlabelled video is a foundational challenge in artificial intelligence. While Joint Embedding Predictive Architectures (JEPA) have set new benchmarks in semantic classification, they often remain physics-blind, failing to capture the causal dynamics necessary for downstream reasoning. We hypothesize that this stems from standard patch-based masking strategies, which prioritize visual texture over rare but informative kinematic events. We propose Interaction-Aware JEPA (IA-JEPA), which utilizes a self-supervised motion-centric masking strategy to prioritize physical interactions. By specifically targeting entities engaged in collisions or momentum transfers, we force the architecture to reconstruct latent trajectories rather than static background features. Evaluated on the CLEVRER benchmark, IA-JEPA achieves 14.26% accuracy on causal reasoning tasks, a significant lead over the 3.22% achieved by standard patch-masked baselines. Crucially, we demonstrate that IA-JEPA breaks the "static bias" of standard self-supervision by inducing a higher-entropy, more discriminative latent space (+10% entropy gain) that linearizes physical energy ($R^2=0.43$). We show that this interaction bias generalizes to real-world human actions (Something-Something V2) and zero-shot physical puzzles (PHYRE-Lite). Our results provide a scalable, fully self-supervised path toward building foundational world models that begin to internalize the causal structure of the physical world.

---

## 17. ReactiveGWM: Steering NPC in Reactive Game World Models

**Authors:** Zeqing Wang, Danze Chen, Zhaohu Xing, ..., Xingyi Yang, Yeying Jin
**arXiv:** [2605.15256](https://arxiv.org/abs/2605.15256)
**Categories:** Computer Vision and Pattern Recognition (cs.CV)

Current game world models simulate environments from a subjective, player-centric perspective. However, by treating the Non-Player Character (NPC) merely as background pixels, these models cannot capture interactions between the player and NPC. In that sense, they act as passive video renderers rather than real simulation engines, lacking the physical understanding needed to model action-induced NPC reactivities. We introduce ReactiveGWM, a reactive game world model that synthesizes dynamic interactions between the player and NPC. Instead of entangling all interaction dynamics, ReactiveGWM explicitly decouples player controls from NPC behaviors. Player actions are injected into the diffusion backbone via a lightweight additive bias, while high-level NPC responses (e.g., Offense, Control, Defense) are grounded through cross-attention modules. Crucially, these modules learn a game-agnostic representation of interactive logic. This enables zero-shot strategy transfer: our learned modules can be plugged directly into off-the-shelf, unannotated world models of different games. This instantly unlocks steerable NPC interactions without any domain-specific retraining. Evaluated on two Street Fighter games, ReactiveGWM maintains fine-grain player controllability while achieving robust, prompt-aligned NPC strategy adherence, paving the way for scalable, strategy-rich interaction with the NPC.

---

## 18. PhysBrain 1.0 Technical Report

**Authors:** Shijie Lian, Bin Yu, Xiaopeng Lin, ..., Cong Huang, Kai Chen
**arXiv:** [2605.15298](https://arxiv.org/abs/2605.15298)
**Categories:** Robotics (cs.RO); Artificial Intelligence (cs.AI); Computation and Language (cs.CL); Computer Vision and Pattern Recognition (cs.CV)

Vision-language-action models have advanced rapidly, but robot trajectories alone provide limited coverage for learning broad physical understanding. PhysBrain 1.0 studies a complementary route: converting large-scale human egocentric video into structured physical commonsense supervision before robot adaptation. Our data engine extracts scene elements, spatial dynamics, action execution, and depth-aware relations, then turns them into question-answer supervision for training PhysBrain VLMs. The resulting physical priors are further transferred to VLA policies through a capability-preserving and language-sensitive adaptation design. Across multimodal QA benchmarks and embodied control benchmarks, including ERQA, PhysBench, SimplerEnv-WidowX, LIBERO, and RoboCasa, PhysBrain 1.0 achieves SOTA results and shows especially strong out-of-domain performance on SimplerEnv. These results suggest that scaling physical commonsense from human interaction video can provide an effective bridge from multimodal understanding to robot action.

---

## 19. Mind Dreamer: Untethering Imagination via Active Latent Intervention on Latent Manifolds

**Authors:** Shaojun Xu, Xiaoling Zhou, Yihan Lin, ..., Luping Shi, Rong Zhao
**arXiv:** [2605.16030](https://arxiv.org/abs/2605.16030)
**Categories:** Machine Learning (cs.LG); Robotics (cs.RO)

Model-Based Reinforcement Learning (MBRL) leverages latent imagination for sample efficiency, yet remains constrained by Historical Tethering: imagination is typically initialized from observed states. This creates a learning asymmetry, where the world model's manifold discovery outpaces the policy's sparse-reward optimization. We propose Mind Dreamer (MD), a framework that operationalizes Active Latent Intervention (ALI) to transcend Markovian continuity. MD reformulates discovery as the minimization of a global Relay Manifold Expected Free Energy (R-EFE); by sampling initial states from a learned generator $s_0 \sim p_{gen}(\cdot)$ rather than the historical buffer, MD utilizes an adversarial generator to synthesize non-continuous latent jumps to epistemic blind spots that are physically plausible yet cognitively challenging. To resolve the credit assignment paradox across these spatial ruptures, we derive the Relay Value Function (RVF) and Relay Uncertainty Function (RUF). These potentials treat synthesized anchors as counterfactual intermediary states, propagating pragmatic and epistemic value through a principled Bellman-style formulation. Notably, we prove that uncertainty propagation across discontinuities necessitates a quadratic discount $\gamma^2$, establishing a formal epistemic horizon. Theoretically, MD approximates a variance-minimizing importance sampler that expands the manifold's spectral gap, reducing the hitting time to critical bottleneck states. Empirically, MD achieves a 1.67$\times$ average speedup over DreamerV3 on DeepMind Control Suite, reaching 8.8$\times$ in sparse-reward tasks.

---
