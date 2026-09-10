# arXiv Daily Digest — 2026-09-09

**Mode:** direct
**Categories:** cs.AI, cs.LG, cs.RO, cs.CV
**Keywords:** VLA, world model, world action model
**Papers found:** 33

---

## 1. WorldAgen: Unified State-Action Prediction with Test-Time World Model Training

**Authors:** Chi Wan, Kangrui Wang, Yuan Si, Pingyue Zhang, Manling Li
**arXiv:** [2609.08162](https://arxiv.org/abs/2609.08162)
**Categories:** Artificial Intelligence (cs.AI)

How can vision-language-action (VLA) models adapt to new environments where world dynamics shift? While recent research has combined world modeling and action prediction to improve VLA performance, existing methods largely rely on pretraining on static datasets, without mechanisms for active adaptation at deployment time. As a result, these models often fail to generalize when deployed in unseen scenarios with novel object configurations or dynamics. We present WorldAgen, a unified framework that jointly learns world modeling and action prediction while enabling Test-Time Training (TTT) to adapt to new environments. WorldAgen employs a shared Transformer backbone with two heads: (1) a world model head that predicts future states from past state-action trajectories, and (2) an agent model head that predicts actions conditioned on task instructions. We design a Mixed Unidirectional Attention Mask to separate these two models. During test time, WorldAgen samples exploratory actions, collects ground-truth state transitions, and performs lightweight TTT updates to refine its world model. This adaptation improves the model's understanding of the environment and leads to more accurate action predictions. Experiments on the CALVIN and LIBERO benchmarks demonstrate that our baseline model achieves comparable, and in some cases superior, performance to current state-of-the-art approaches. Moreover, with TTT on a small number of samples, our method surpasses existing state-of-the-art models, highlighting the effectiveness of adapting world models at inference time.

---

## 2. A radiographic world model for clinical reasoning and evidence generation

**Authors:** Suyang Xi, Songtao Hu, Shansong Wang, ..., Ralph R. Weichselbaum, Xiaofeng Yang
**arXiv:** [2609.07719](https://arxiv.org/abs/2609.07719)
**Categories:** Artificial Intelligence (cs.AI)

Medical imaging artificial intelligence (AI) is commonly developed as separate mappings from radiographs to diagnostic outputs or from clinical descriptions to generated images, although both arise from the same underlying radiographic state. A world-model formulation instead seeks to learn an internal representation of this state that can support both clinical readout and conditional simulation of radiographic observations. Here we introduce MedDream, a radiographic world model that learns a shared continuous latent state from paired chest radiograph-text observations for diagnostic reasoning and report-conditioned evidence generation. MedDream was pretrained on 2.65 million leakage-controlled chest radiograph-text pairs curated from 4.40 million candidates. Across eight clinical datasets and two independent reader cohorts, MedDream outperformed leading diagnostic and generative comparators. For diagnostic reasoning, MedDream showed strong generalization across disease recognition, label-scarce adaptation, severity assessment, and localization, while MedDream-supported review increased mean resident concordance with independent radiologist consensus from 56.3% to 63.0%. For evidence generation, MedDream produced radiographs that preserved clinically relevant pathology and improved downstream performance on held-out real data, with synthetic augmentation increasing external VinDr-CXR macro-AUROC from 76.4% to 81.4%. More importantly, conditioning generation on prespecified subgroup performance gaps enabled targeted evidence construction, increasing weighted F1 by 3.1 percentage points in Asian patients, whereas matched-volume unguided augmentation decreased it by 2.3 points. These findings establish radiographic world models as a path toward medical AI that learns clinically meaningful internal states for interpreting, simulating, and constructing evidence for clinical use.

---

## 3. World Models Under Asynchronous Sensor Observations

**Authors:** Akash Anand, Abhay Anand, Yash Vishe
**arXiv:** [2609.07299](https://arxiv.org/abs/2609.07299)
**Categories:** Artificial Intelligence (cs.AI)

Learned world models typically assume that observations arrive synchronously, an abstraction inherited from simulators that return a complete state vector at each environment step. Physical sensing instead operates at heterogeneous rates, leaving most observation channels stale at any given instant. Interpolating stale channels introduces measurements that were never observed, while downsampling to the slowest sensor discards valid measurements. A natural alternative is to zero-order-hold the most recent reading and provide the known sampling schedule to the model through two features, staleness and time-to-refresh. We test this prediction using transformer world models across three regimes of increasing causal coupling: open-loop rollouts in continuous-control locomotion, closed-loop model-predictive planning in which each learned model serves as the planner dynamics, and a linear latched-actuator system in which refresh events apply a zero-order-held command to the plant. Our findings show that the effectiveness of time-to-refresh depends on the causal role of the sampling schedule, specifically when refresh events affect the system rather than merely report its state. These results establish when sampling schedules provide useful information for predictive world models operating under asynchronous physical observations.

---

## 4. LayerRoute: Action-Conditioned Mixture-of-Layers Routing for Vision-Language-Action Policies

**Authors:** Zheng Lu, Haoran Liao, Wanqi Zhong, ..., Zirui Song, Yiming Li
**arXiv:** [2609.06079](https://arxiv.org/abs/2609.06079)
**Categories:** Artificial Intelligence (cs.AI); Machine Learning (cs.LG)

Vision-Language-Action (VLA) policies leverage pretrained vision-language models (VLMs) to guide action generation for robot control. VLMs provide hierarchical visual-semantic representations that evolve across layers, from local visual geometry to abstract, language-aligned semantics; different manipulation tasks may therefore require different mixtures of layer representations. Meanwhile, the action module maintains intermediate representations that evolve throughout action computation and may provide useful information for subsequent decisions. However, existing VLA interfaces offer limited flexibility in representation access: VLM information is exposed through fixed layer assignments for each action layer, while intermediate action states are only propagated implicitly through residual streams without explicit reuse. We introduce LayerRoute, an action-conditioned representation routing interface that enables adaptive access to VLM layers and action representations. The Layer Mixture Router dynamically forms mixtures of cached VLM representations, while Action-State Reread reuses earlier action representations. Across diverse simulation and real-world benchmarks, LayerRoute consistently improves StarVLA-$\pi$ and $\pi_{0.5}$, achieving up to 7.2 gains on LIBERO Long with only 0.31% / 3.87% additional parameters. Ablation studies validate the benefit of action-conditioned layer routing, while routing analyses reveal structured allocation patterns across action layers and task settings.

---

## 5. Learning Counterfactual World Models for Embodied Reasoning under Partial Observability

**Authors:** Todd Y. Zhou, Daniel Zhang
**arXiv:** [2609.05834](https://arxiv.org/abs/2609.05834)
**Categories:** Artificial Intelligence (cs.AI)

World models promise a general route to embodied intelligence: learn predictive dynamics once, then reason, plan, and act with them. Increasingly, the representations beneath such models are pretrained on large-scale video, interaction, and multimodal corpora, which raises a question prediction quality alone cannot answer: when is a learned representation actually actionable? We identify a failure mode we call counterfactual collapse: a model predicts visually plausible futures while failing to distinguish interventions with different behavioral consequences. This arises whenever a representation is optimized for perceptual similarity rather than intervention structure, which is precisely the objective under which most large-scale pretrained encoders are learned. We introduce Counterfactual Latent World Models (CLWM), which combine a recurrent belief-state encoder, action-conditioned latent dynamics, and a contrastive counterfactual objective that separates futures induced by distinct interventions even when their observations look alike. Across occluded manipulation, aliased navigation, and long-horizon manipulation, CLWM improves planning success over the strongest baseline (65.1% $\to$ 74.6% on Occluded Push and 67.3% $\to$ 78.9% on Aliased Maze) and reduces exploitative planning failures (18.4% $\to$ 9.7% on Deferred Kitchen), with ablations attributing the gains to hard counterfactual negatives, especially perceptual-alias negatives. Finally, our counterfactual separability metric, which tracks planning success across the five baseline model classes ($r \ge 0.94$), is representation-agnostic: given intervention-outcome labels, it can audit any encoder, pretrained or trained from scratch, before a planner trusts it. We do not yet measure it on large-scale pretrained encoders. Here we establish the metric and its relationship to planning success for world models trained from scratch.

---

## 6. ARC-Bench: Closed-Loop Replanning Masks Broken Action Ranking in Frozen JEPA World Models

**Authors:** Zhengshu Zhang, Zhiyuan Li
**arXiv:** [2609.05461](https://arxiv.org/abs/2609.05461)
**Categories:** Artificial Intelligence (cs.AI); Machine Learning (cs.LG); Robotics (cs.RO)

Reward-free latent world models plan by scoring candidate actions with distances in a frozen latent space: an action is preferred if its predicted future embedding lands closer to the goal embedding. This silently assumes that latent closeness is action-rankable, i.e., that ordering candidates by latent distance agrees with ordering them by true cost. We audit this assumption directly. We introduce ARC-Bench, a no-leak, fixed-candidate protocol that measures whether frozen JEPA-style objectives rank candidate actions correctly, and apply it to official released JEPA-WM checkpoints across navigation and manipulation-style control. The assumption fails, severely and structurally: on the official manipulation audits the top-scored candidate is almost always suboptimal, and the same inversion appears in the maze domains. A controlled visual-backbone extension shows that the defect persists when DINOv2 is replaced by video-pretrained V-JEPA 1 and V-JEPA 2 encoders at ViT-L/ViT-G scale. Provenance, undertraining, matched-budget backbone controls, and metric-circularity controls rule out trivial explanations. We then explain why this defect has stayed invisible: closed-loop replanning masks it. When we reduce the planner's replanning frequency, success collapses in both a navigation and a manipulation domain, and the episodes rescued by frequent replanning are enriched for severe first-plan ranking failures in the PointMaze first-plan diagnostic. Closed-loop success rates therefore systematically overstate the rankability of frozen latent representations. ARC-Bench supplies the measurement, and the masking mechanism the explanation, for methods that adapt, amortize, or replan around latent-space planners without directly auditing released JEPA-WM action rankability.

---

## 7. TANGO: Humanoid Navigation in Cluttered Environments with a Whole-Body Vision-Language-Action Model

**Authors:** Anqi Li, Yuxin Chen, Zhaobo Li, ..., Masayoshi Tomizuka, Dhruv Shah
**arXiv:** [2609.09158](https://arxiv.org/abs/2609.09158)
**Categories:** Robotics (cs.RO); Artificial Intelligence (cs.AI)

We study the problem of navigating cluttered indoor environments with a humanoid robot. Unlike conventional methods that model navigation as a 2D path planning problem, humanoid traversal in cluttered environments requires continuous geometry-aware whole-body adaptation, including coordinated arm placement, torso adjustment, and gait modulation for collision-free movement through complex 3D spaces. We introduce TANGO, the first whole-body vision-language navigation framework for language-conditioned humanoid traversal in cluttered environments. Given a natural-language instruction and egocentric RGB observations, TANGO directly predicts 29-DoF joint-space actions for downstream whole-body control. We train TANGO entirely in simulation by synthesizing diverse collision-free traversal behaviors via global path planning, kinematic whole-body motion generation, obstacle-aware motion editing, and RL-based tracking. This pipeline provides dynamically feasible action supervision for learning language-conditioned whole-body policies. In extensive simulation experiments, TANGO demonstrates state-of-the-art performance in vision-language navigation, while outperforming strong modular baselines in navigating challenging scenes requiring obstacle negotiation. Lastly, we deploy TANGO zero-shot on a Unitree G1 humanoid robot, and observe robust language-guided traversal in cluttered real-world scenes without training on any real-world navigation data.

---

## 8. DeCAL: Towards Physically-Grounded Dexterous Vision-Language-Action Models via Contact-Aware Latent Co-Imagination

**Authors:** Yankai Fu, Ning Chen, Junkai Zhao, ..., Zhongyuan Wang, Shanghang Zhang
**arXiv:** [2609.09119](https://arxiv.org/abs/2609.09119)
**Categories:** Robotics (cs.RO); Artificial Intelligence (cs.AI)

Dexterous manipulation involves contact-rich and fine-grained interactions with the physical world, posing significant challenges for existing vision-language-action (VLA) models due to severe visual occlusions and complex contact dynamics. While recent works have incorporated tactile sensing into robotic manipulation, most approaches still rely on homogeneous multimodal fusion, lacking adaptive tactile integration and explicit modeling of physical dynamics. In this work, we present DeCAL, a physically-grounded dexterous vision-language-action model that unifies understanding, imagination and action generation for contact-rich dexterous manipulation. Built upon a Mixture-of-Transformers (MoT) architecture, DeCAL leverages specialized experts for each capability while enabling efficient information flow among them. To effectively leverage tactile information, we introduce Adaptive Visuo-Tactile Fusion that dynamically regulates tactile interactions via a contact-aware gating strategy. Furthermore, we propose Visuo-Tactile Latent Co-Imagination to jointly model visual and tactile dynamics, equipping the policy with implicit physical world knowledge. Experimental results show that DeCAL consistently achieves state-of-the-art performance across all tasks, attaining a 71% average success rate and an 83.4% progress success rate, while also demonstrating strong generalization to unseen scenarios. The website is available at this https URL.

---

## 9. Earth System World Model for What-If Simulations: A Case Study for Terrestrial Ecosystems

**Authors:** Zhihao Wang, Ruichen Wang, Ruohan Li, ..., Shaowen Wang, Yiqun Xie
**arXiv:** [2609.08855](https://arxiv.org/abs/2609.08855)
**Categories:** Machine Learning (cs.LG); Artificial Intelligence (cs.AI)

Machine learning emulators have become essential for accelerating expensive Earth-system simulations, but most existing approaches remain passive forecasters: they reproduce simulator trajectories under prescribed forcings without an explicit interaction mechanism for user-specified interventions. This limits their use in interactive scientific workflows and Earth-system digital twins, where users often need to explore how a system would respond if selected state components were changed. We propose an action-conditioned world-modeling framework for Earth-system emulation that reformulates simulator trajectories as supervision for controllable state-transition learning. The key idea is transition-action pretraining: naturally observed state changes are treated as label-free action supervision, allowing the model to learn both prescribed dynamics and action-conditioned responses without manually annotated interventions. We further introduce masked response learning to infer unobserved variables under partial state edits and learn coupled system dependencies. We test this framework on ecosystem dynamics across six global regions and multiple stand ages. Experiments show that the model preserves competitive long-horizon emulation accuracy while enabling controllable structural interventions and coherent responses in coupled ecosystem-cycle variables. These results suggest a practical route from passive Earth-system emulators toward interactive, intervention-aware scientific surrogates.

---

## 10. Hi-FLoop: Hierarchical State-Feedback Loops for Multi-Timescale World Modeling

**Authors:** Rx Fan, Z Han
**arXiv:** [2609.08796](https://arxiv.org/abs/2609.08796)
**Categories:** Computer Vision and Pattern Recognition (cs.CV); Artificial Intelligence (cs.AI)

Multi-agent traffic simulation seeks diverse, coordinated, and physically realistic futures from maps and observed history. Long-horizon closed-loop generation must reconcile multiple decision time scales while its context evolves with generated states. Existing methods often unfold long futures from an initial scene and resolve intent, interaction, and motion monolithically, weakening cross-scale consistency and adaptation. Multimodal rollout poses a further consistency problem: independently reselecting modes across agents or commits can stitch together incompatible futures instead of preserving a coherent joint branch. We present Hi-FLoop, a branch-consistent multi-timescale state-feedback framework. Eight scene-level Worlds represent joint hypotheses; all agents share one selected World identity throughout all 16 commits of an 8-second rollout, while Goal, Preview, and Control states adapt within that branch. An 8-second Goal anchors intent, a 2-second Preview coordinates interactions, and 1-second Control produces physical motion. Every 0.5-second commit feeds back only its executed prefix as new facts, while unexecuted hypotheses never enter factual memory. Joint Preview Interaction induces a sparse directed future graph and uses conflict probabilities and signed arrival-time differences to refine interaction-aware motion. For generated-state recovery, a prefix-frozen A-to-B cascade transfers typed physical state and the branch index--but no latent state--from a frozen prefix model to an independently parameterized recovery model. On the full H-D public-validation split of 955 scenarios, the S2.1 cascade obtains an 8-second scene-joint ADE-at-joint-minFDE@8/joint-minFDE@8 of 2.048/6.384 m when one World must explain all evaluated agents. Agent-centric oracle-minADE@8 is 0.526 m at 6 seconds and 0.875 m at 8 seconds.

---

## 11. Measuring Language Transfer in Robot Policies: Adding Greek to a Cosmos3 Vision-Language-Action Policy

**Authors:** Ayoub Kirouane, Georgios Giaples, Christos Petrocheilos
**arXiv:** [2609.07470](https://arxiv.org/abs/2609.07470)
**Categories:** Robotics (cs.RO); Artificial Intelligence (cs.AI)

Robot foundation models are trained and evaluated predominantly in English, and robot demonstration corpora do not exist for most languages. We study the addition of Greek to an open vision-language-action stack using only machine-rephrased instructions and no architecture changes. The main challenge is measurement rather than translation. Several plausible instruments produce false conclusions: a color-histogram metric rewards noise, a single-goal benchmark scores 84.6% under correct Greek and 82.6% under deliberately wrong instructions, training loss fails to predict Greek success, and single-run comparisons are dominated by seed variation. On a discriminative ninety-task suite with three seeds per arm, a multilingual text tower without Greek demonstrations remains at its wrong-instruction floor, while Greek-only training exceeds its control by at most 2.7 points. Bilingual training yields a consistent 6.7-7.1 point margin over its control and reaches about two fifths of English performance. The policy also overfits the translator's phrasing; training on seven phrasings per task approximately halves this penalty. Warm-starting from a language-adapted world model and unfreezing the text tower both degrade performance. The results support two practical requirements for low-resource robot-policy localization: build a guaranteed null before trusting a metric, and replicate low-resource-language results across seeds.

---

## 12. PV-WM: A Heterogeneous Micro-Macro World Model for Articulated Pedestrian-Vehicle Co-Rollout

**Authors:** Haozhuang Chi, Jingsong Liang, Ziying Song, ..., Haoruo Zhang, Chen Lv
**arXiv:** [2609.07328](https://arxiv.org/abs/2609.07328)
**Categories:** Robotics (cs.RO); Artificial Intelligence (cs.AI); Multiagent Systems (cs.MA)

Local pedestrian-vehicle forecasting spans heterogeneous physical scales: pedestrians combine root locomotion with articulated motion, whereas vehicles are rigid bodies described by kinematic state and oriented extent. Existing road-agent forecasters typically omit pedestrian articulation, while pose forecasters leave vehicle futures outside the learned rollout. We introduce PV-WM, a history-only world model over structured post-perception tracks. It recurrently advances pedestrian root motion, 15-joint articulation, and learned vehicle states within a synchronized heterogeneous state. The generated pedestrian and vehicle chunks supply the next recurrent boundary; vehicle boxes are reconstructed from predicted center and heading with observed extent, and P-V geometry is recomputed after every transition. Relative to a matched one-shot complete-state predictor, recurrent execution reduces Root ADE by 12.7% and MPJPE by 14.8%. Feedback interventions show that later predictions depend on the content, temporal order, and pedestrian identity of generated articulation. Across 824 aligned Waymo contexts, with 797 providing valid future vehicle support, PV-WM reduces Root ADE by 5.2%, MPJPE by 7.6%, P-V distance error by 11.9%, and oriented-box closest-approach error by 5.8% relative to a validation-selected Modular Specialist. The single-network model uses 57.1% fewer parameters, 96.5% lower average FLOPs per local scene, and 25.5% lower measured p95 latency. PV-WM unifies this heterogeneous future state while preserving type-specific pedestrian and vehicle dynamics.

---

## 13. InfluenceField: A Differentiable Field with Interventionally Identifiable Causal Structure for Multimodal World Modeling

**Authors:** Zihao Yang, Zijia Wang, Zhiqiu Huang
**arXiv:** [2609.07874](https://arxiv.org/abs/2609.07874)
**Categories:** Machine Learning (cs.LG); Machine Learning (stat.ML)

Multimodal large language models often capture visual-linguistic correlations but struggle to predict how local visual interventions propagate and affect downstream answers. We introduce InfluenceField, an intervention-aware latent field inserted between the visual encoder and language decoder. It lifts patch features into a continuous spatial representation, propagates directed influence over multiple steps, and predicts local intervention effects through a shared transition operator. Training jointly optimizes language modeling, cross-environment invariance, counterfactual rollout supervision, and structural regularization. For a nonlinear finite-basis population model, we show that target-aligned interventional supervision, together with a one-step separation condition on the transition, restricts admissible representations to within-location reparameterizations, so that the directed dependency graph of the full transition is recovered exactly. A linear specialization gives an exact partial-coverage characterization and a finite-loss stability bound, and the field analysis derives the spatial profile of coefficient interventions together with a shared-channel calibration result. On CausalVQA, InfluenceField improves overall accuracy over its backbone by 13.1 percentage points, with the largest gains on the planning and hypothetical categories. Capacity-matched baselines and structural controls attribute the gains in robustness and factual-counterfactual consistency to the causal objectives rather than to added capacity.

---

## 14. TrojanWorld: Backdooring World-Model Agents via Imagination Steering

**Authors:** Wenkai Huang, Siyuan Liang, Gaolei Li, ..., Jianhua Li, Dacheng Tao
**arXiv:** [2609.07051](https://arxiv.org/abs/2609.07051)
**Categories:** Machine Learning (cs.LG); Cryptography and Security (cs.CR)

World models increasingly serve as the predictive core of model-based reinforcement learning agents, enabling them to simulate future dynamics and reason over imagined trajectories before acting. Their substantial training demands make pretrained world models attractive for distribution and reuse, exposing downstream systems to model supply chain threats. Backdoor attacks offer a targeted and stealthy means of exploiting such supply chains, yet their threat to interactive world-model agents remains largely unexplored. To fill this gap, we present TrojanWorld, a backdoor framework for world-model agents that induces attacker-specified behavior by steering internal imagination. A physical object placed in the scene acts as the trigger, enabling deployment-time activation through the agent's native observation pipeline without digitally manipulating the observation stream. To achieve effective, stealthy, and persistent control, TrojanWorld combines Decision-Reflective Induction to steer trigger-conditioned imagination toward attacker-specified actions using decision feedback, Clean Behavior Anchoring to preserve trigger-free predictive and behavioral fidelity, and Causal Propagation to sustain the induced preference along subsequent trajectories after the trigger disappears. Together, these mechanisms establish an end-to-end attack chain from physical perception through corrupted imagination to malicious action selection. Experiments with the TD-MPC2, DreamerV3, and R2-Dreamer systems across the DeepMind Control, MetaWorld, MyoSuite, and RoboDesk benchmarks show that under trigger activation, TrojanWorld achieves a target-action deviation as low as 0.026 while retaining at least 98.8% of the corresponding clean performance. Even after trigger removal, the compromised agent can remain trapped in the induced behavioral trajectory, continuing to execute attacker-specified actions.

---

## 15. ActionSplice: In-Flight Action Editing for Interactive World Models

**Authors:** Pardis Taghavi, Tingyu Guo, Jonas Lossner, Gaurav Pandey, Reza Langari
**arXiv:** [2609.08230](https://arxiv.org/abs/2609.08230)
**Categories:** Computer Vision and Pattern Recognition (cs.CV); Machine Learning (cs.LG)

Chunk-autoregressive video world models typically condition each generated chunk on one action. An action received during sampling must therefore wait for the next chunk, condition future solver evaluations on a state produced under the previous action, or trigger rollback that repeats completed evaluations. We introduce ActionSplice, an inference framework that formulates this problem as Counterfactual State Transport (CST). A lightweight corrector transports the interrupted backbone-native representation toward the matched state induced by the revised action at the same solver step. The world model and sampler remain frozen, and sampling resumes without replaying completed evaluations. The retargeting variant $\mathrm{CST}*{R}$ updates the entire active chunk, while the temporal-splicing variant $\mathrm{CST}*{T}$ preserves a temporal prefix and updates only the suffix. Across minWM-Wan Action2V and HY-WM1.5, $\mathrm{CST}*{R}$ reduces rollback-relative LPIPS by 61.5% and 75.9% relative to direct condition swapping. $\mathrm{CST}*{T}$ reduces suffix LPIPS by 56.1% and 77.5%, respectively, while providing $2.73\times$ and $1.69\times$ pixel-ready speedups over waiting. Under the HY-WorldPlay protocol, $\mathrm{CST}_{R}$ obtains a PSNR of 25.66 dB, an SSIM of 0.6902, and an LPIPS of 0.1337 against the original rollout.

---

## 16. Beyond Task Success: Stage-Wise Reliability of World Model Planning under Sensing Degradation

**Authors:** Geonmyeong Lee, Byoung-Tak Zhang
**arXiv:** [2609.07126](https://arxiv.org/abs/2609.07126)
**Categories:** Robotics (cs.RO); Machine Learning (cs.LG)

In world model planning, sensing inputs pass through an encoder and predictor before affecting planner decisions, so final task success alone cannot reveal where sensing disturbances attenuate or persist in the pipeline. We apply 10 visual and temporal sensing degradations to a world model planner and track their effects across representation, future prediction, planner preference, and physical outcome using paired evaluation on the same 50 tasks. The relative impact of degradations was not preserved across stages: large representation shifts could attenuate downstream, while smaller initial shifts could persist to the outcome, and internal-response ordering did not directly match physical-outcome ordering. Temporal degradations also showed distinct patterns: even with similar overall changes in observation history, responses differed substantially with the location of corrupted information and the planner's actual exposure. This non-uniform stage-wise response was also observed in secondary evaluations with another manipulation task and a different world model. Stage-wise diagnosis can therefore identify where sensing disturbances attenuate or persist and help prioritize subsequent model verification and sensing mitigation.

---

## 17. BinauralVAE: Spatial Audio Reconstruction For World Models

**Authors:** Luis Vitor Zerkowski, Luiz Velho
**arXiv:** [2609.06837](https://arxiv.org/abs/2609.06837)
**Categories:** Sound (cs.SD); Machine Learning (cs.LG)

Embodied artificial intelligence has historically very much relied on visual perception, leading to a proliferation of multiple vision-centric world models. However, this reliance fails to capture spatial understanding in its entirety and can even present vulnerabilities in environments with visual occlusions, low-light conditions, or blackouts-scenarios, where acoustic information becomes a critical alternative for spatial awareness and navigation. Despite its potential, research into realistic spatial audio and particularly the development of audio-centric world models remains sparse. In this technical report, we introduce BinauralVAE: a flexible, open-source pipeline (this https URL) that explores multiple models for spatialized audio reconstruction, progressing from fundamental baselines to advanced, mathematically grounded architectures. Our approach evaluates various Variational Autoencoder architectures -- including complex-valued variants -- to learn robust latent representations of binaural signals. Developed alongside AudioWorldSim, our methodology leverages realistic acoustic data captured as a simulated robot navigates an environment. This pipeline establishes a foundation for state representation in a future audio-based world model, designed to map the direct causal connection between navigational actions and their resulting acoustic consequences, and helping to enable sound as an essential complementary modality for spatial knowledge acquisition.

---

## 18. SimpleMemVLA: A Simple but Effective Native-Video Memory for Vision-Language-Action Models

**Authors:** Cheng Yin, Wang Xu, Junpeng Yang, ..., Zhouping Yin, Yankai Lin
**arXiv:** [2609.05533](https://arxiv.org/abs/2609.05533)
**Categories:** Computer Vision and Pattern Recognition (cs.CV); Machine Learning (cs.LG); Robotics (cs.RO)

Long-horizon manipulation is partially observable: the information needed to choose the next action may appear only in observations from minutes earlier. Existing memory mechanisms: retrieval banks, learned compressors, recurrent states must decide what to keep from the past before knowing what a future decision will require. This was motivated by the assumption that minute-scale history is too large to process directly, which modern VLM backbones no longer make true. In this work, we introduce SimpleMemVLA, a VLA without a dedicated memory module. It keeps the sampled history intact and passes it to the backbone in the timestamped video format the backbone was pretrained to process; the hidden states of a generated sub-task then form the only channel from history to a standard flow-matching action head. Since consecutive decisions share most of their history, prefilling the shared prefix during action execution keeps latency close to a single-frame VLA. SimpleMemVLA sets a new state of the art on four memory benchmarks without cost on general-purpose control. Holding the backbone and training setup fixed, it outperforms retrieval, compression and recurrent-state mechanisms by a wide margin, and causal interventions confirm that the policy genuinely reads its history. Code available at this https URL

---

## 19. ComVLA: Communication-Aware Split Inference for VLA Models in 6G-Connected Robotics

**Authors:** Boliang Liu, Wint Yi Poe, Jingyun Di, Riccardo Trivisonno, Giuseppe Caire
**arXiv:** [2609.07838](https://arxiv.org/abs/2609.07838)
**Categories:** Robotics (cs.RO)

Connected robotics is an emerging 6G application where mobile robots follow natural-language instructions to manipulate physical objects. The Vision-Language-Action (VLA) models that enable this are too large to run on the robot; a common trend is to offload inference to the cloud. The wireless link, however, limits how much sensing data the edge can transmit per control step. Two recent lines address this constraint: semantic communication codecs compress sensor data but require channel-specific retraining, and VLA token pruners select tokens from image but ignore the channel. Our insight is that the dense semantic information contained in the language already indicates which visual tokens matter. We propose ComVLA, a framework that uses this language guidance to adapt the VLA token budget to the channel capacity. Transmitting 32 tokens instead of 512 on the LIBERO benchmark, ComVLA cuts inference compute by 74% and inference latency by 22% versus the original OpenVLA-OFT baseline, at a cost of 1.5 pp in average task success (95.4% vs. 96.9%), and it stays within the capacity budget under Rayleigh and Rician fading. These results demonstrate that co-designing VLA inference and wireless communication is a practical direction for 6G-connected robotics.

---

## 20. ICI-VLA: In-Context Imitation with Spatiotemporally Aligned Demonstrations for Vision-Language-Action Models

**Authors:** Songhua Yang, Ziyu Liu, Xuetao Li, ..., Kangxin Zhu, Miao Li
**arXiv:** [2609.07581](https://arxiv.org/abs/2609.07581)
**Categories:** Robotics (cs.RO)

Vision-Language-Action (VLA) policies are commonly adapted to new manipulation settings through additional gradient updates, which limits rapid deployment when task-specific data or compute is scarce. We present ICI-VLA, a training and retrieval framework that equips a text-action VLM with few-shot test-time adaptation through in-context demonstrations. Unlike mainstream VLA designs based on action-specific multimodal fusion, ICI-VLA retains the native text-generation interface. ICI-VLA updates its parameters only during offline training; at inference, the policy remains fixed and conditions action generation on retrieved micro-demonstrations. The framework decomposes long trajectories into short, semantically labeled examples and trains an RD-Encoder with positives mined by Dynamic Time Warping (DTW), aligning the retrieved context with the phase and geometry of the current subtask. We further introduce Target Action Masking, a context-corruption objective designed to reduce direct action copying and increase reliance on the current observation. ICI-VLA reaches average success rates of 97.7% on LIBERO and 60.4% on RoboTwin 2.0, exceeding the highest reported baseline average on RoboTwin 2.0 by 19.3 percentage points. It also achieves 83.2% across four physical tasks. These results indicate that a fixed VLA policy can benefit from conditioning on spatiotemporally aligned demonstrations at test time.

---

## 21. OpenWAM: An Open, Modular Exploration Towards Systematic World-Action Model Pretraining

**Authors:** Yuran Wang, Siqiao Huang, Mingleyang Li, ..., Lin Shao, Hang Zhao
**arXiv:** [2609.07398](https://arxiv.org/abs/2609.07398)
**Categories:** Robotics (cs.RO)

World-Action Models inherit world knowledge from video-generative priors, and channel it into executable control signals through embodied experience. Existing systems, however, are monolithic: the generative backbone, visual representation, architecture, information flow, inference procedure, and training data are tightly coupled, obscuring which design choices matter and why. We introduce OpenWAM, an open research stack that turns world-action pretraining into a controlled experimental program. OpenWAM-Infra factorizes the WAM design space into composable modules with unified training, inference, deployment, and evaluation. On this substrate, OpenWAM-Study examines three questions through controlled experiments: what to inherit, how world and action learning interact, and how their synergy scales; and distills three principles: upstream knowledge transfers through a sufficiently capable generative backbone and a compact, information-rich latent space; world-action synergy requires dedicated action capacity, explicit world-to-action information flow, and synchronized joint denoising; and embodied pretraining principally improves out-of-domain generalization, with one-stage co-training over egocentric and robot data integrating world coverage and action grounding. Composing these principles, we build OpenWAM-{\alpha}, an open WAM pretrained on roughly 6,400 hours of egocentric human and robot data and evaluated across simulation and real-world benchmarks. Across the eight simulation benchmarks and the real-robot experiments, which together span embodiments from single-arm and bimanual manipulation to dexterous hands, OpenWAM-{\alpha} delivers consistently excellent performance, sustaining its top-tier standing from simulation to the physical world. We release the full stack, including infrastructure, evaluation protocols, pretrained models, and data recipes, to facilitate future research.

---

## 22. Diagnosing and Dynamically Filtering Occupancy World Models for Active Mapping

**Authors:** Jiahui Zhang, Gongbo Liang, Yu Zhang
**arXiv:** [2609.06820](https://arxiv.org/abs/2609.06820)
**Categories:** Robotics (cs.RO); Computer Vision and Pattern Recognition (cs.CV)

Active mapping requires a robot to select camera viewpoints that efficiently reconstruct an unknown 3D scene. To reason about unobserved regions, recent systems use pretrained occupancy networks as world models that complete missing geometry. The predicted structure contributes to expected coverage gain and constrains feasible robot motion. Consequently, occupancy errors can change both what the robot chooses to explore and where it is able to move. We diagnose these effects by holding the planner fixed and varying only the occupancy representation provided to it. We consider planning without completion, with learned occupancy, with false positives removed by a ground truth oracle, with false negatives restored by an oracle, and with ground truth occupancy. Our experiments show that correcting false positives or false negatives alone does not consistently improve final coverage. This finding reveals a gap between occupancy accuracy and downstream planning performance. Ground truth occupancy provides a much larger improvement in coverage efficiency than in endpoint coverage, suggesting that planning and reachability remain important bottlenecks even when the geometric world model is accurate. Based on these findings, we introduce a dynamic filtering strategy that preserves predictions in unexplored space while suppressing repeatedly unsupported occupancy using online observations. Preliminary examples show that this strategy can redirect viewpoint selection toward reachable surfaces that would otherwise remain unobserved.

---

## 23. VLA-Corrector: Stage-Aware Observable State Understanding for Prompt-Based Closed-Loop Recovery of Vision-Language-Action Policies

**Authors:** Chang Song, Bin Qian, Yan Feng, Zhijie Song
**arXiv:** [2609.06508](https://arxiv.org/abs/2609.06508)
**Categories:** Robotics (cs.RO)

Long-horizon robot manipulation with Vision-Language-Action (VLA) policies remains vulnerable to execution-time deviations, as final task success provides little information for diagnosing and correcting failures caused by action noise, object displacement, or goal misalignment. We introduce a stage-aware failure verification and Prompt Recovery framework that enables closed-loop correction of a fixed VLA policy without parameter updates or privileged simulator states. The framework introduces an observable-history-based Learned Verifier that jointly estimates manipulation progress and execution risk by temporally modeling multi-view visual observations, proprioceptive states, and executed actions. To provide interpretable task understanding, we represent manipulation execution through semantic progress stages, including approach, alignment, grasp, transport, and placement, and identify stage-specific failure patterns. Upon detecting abnormal execution, the framework preserves the original instruction and generates a stage-conditioned recovery prompt, allowing the same frozen VLA policy to produce corrective actions. Extensive multi-round evaluations on LIBERO and LIBERO Plus demonstrate that the proposed approach substantially improves closed-loop reliability under diverse perturbations. Without access to privileged object or goal coordinates, the Learned Verifier achieves recovery performance close to that of the privileged rule-based verifier in the evaluated settings. These results show that observable visual-proprioceptive-action history is sufficient to infer latent task states and enable practical failure recovery for existing VLA policies.

---

## 24. GloVLA: Let Geometry Move and Local VLA Interact for Robust Object-Centric Manipulation in Unstructured Environments

**Authors:** Truong Thanh Nguyen, Huy Hoang Nguyen, Ha Anh Nguyen, ..., Minh Nhat Vu, Ngan Le
**arXiv:** [2609.06256](https://arxiv.org/abs/2609.06256)
**Categories:** Robotics (cs.RO)

Vision-language-action (VLA) models have shown promising generalization for language-conditioned robot manipulation, but deploying them in unstructured environments remains challenging. A single end-to-end VLA policy must simultaneously solve long-range transport of the end effector to task-relevant regions and short-horizon, contact-rich interaction upon arrival. This formulation is inefficient and brittle: small visual shifts, distractors, clutter, occlusions, or unfavorable initial gripper poses can push the policy outside the local state distribution in which it was trained, leading to task failure. We introduce GloVLA, a hybrid framework that explicitly separates object-centric manipulation into two complementary regimes: a geometric transport controller moves the end-effector into interaction-centric handoff regions, and local VLA policies handle only the short-horizon interaction phases. GloVLA is model-agnostic and can be integrated with different VLA backbones with no additional demonstrations and no changes to the action space or success predicate. Experiments on standard LIBERO and LIBERO-Plus Object tasks together with a newly introduced LIBERO-Challenge benchmark ettings with clutter, distractors,illumination changes, visual shifts, and obstruction show that GloVLA improves task success and substantially lowers VLA inference cost compared with full end-to-Challenge, full-trajectory GR00T N1.6execution degrades to 20.9% average success while GloVLA retains 88.5%; on a physical UR10e, overall success improves from 35.6% to 90.0% while mean inference time is more than halved. Videos and additional results are available at this https URL

---

## 25. Where Success Breaks: Failure-Boundary Learning for Robust Vision-Language-Action Models

**Authors:** Yanzhe Chen, Zhijun Cao, Mike Zheng Shou
**arXiv:** [2609.06114](https://arxiv.org/abs/2609.06114)
**Categories:** Robotics (cs.RO)

Vision-language-action (VLA) models adapted through supervised fine-tuning (SFT) inherit a structural asymmetry: expert demonstrations teach the policy where success behavior lies, but provide no signal about where it ceases to be reliable. We argue that robust VLA adaptation should therefore be viewed not as further demonstration fitting, but as **Failure-Boundary Learning**---the problem of *Discovering*, *Localizing*, and *Shaping* the boundary between recoverable deviations and task failure. To instantiate this view, we propose **DLS**: built on a **real-grounded behavioral prior** from few real demonstrations and simulated co-training, DLS *discovers* failure boundaries at scale through on-policy digital twin rollouts. Rather than reducing each rollout to a binary label, **semantic progress localization** uses privileged simulator states to assign progress-aware signals that capture *where* the failure boundary is crossed, not merely *whether*. These signals drive **directional boundary shaping** in the flow dynamics---reinforcing success-producing denoising directions and suppressing failure-producing ones, without action likelihoods or auxiliary critics. Across real-robot manipulation tasks, DLS improves robustness over SFT and online RL baselines, especially under randomized initial states and unseen visual conditions.

---

## 26. How to Learn from What a Human Would Avoid? Intervention-Aware World Models with Real-World RL for Dexterous Manipulation

**Authors:** Jiaju Yin, Zhenhui Zhang, Lixin Xu, ..., Arash Ajoudani, Renjing Xu
**arXiv:** [2609.06009](https://arxiv.org/abs/2609.06009)
**Categories:** Robotics (cs.RO)

Multi-fingered dexterous manipulation remains a frontier for real-world reinforcement learning (RL) due to the high-dimensional action space and the prohibitive cost of hardware failures. While human-in-the-loop (HIL) RL allows operators to intervene before failures occur, current pipelines often treat these interventions as reactive corrections, discarding the rich safety signal inherent in the operator's decision to take control. In this paper, we ask: How can we learn from what a human would avoid? We present WHIRL, a safety-aware RL framework that transforms binary human interventions into forward-predictive signals for proactive risk avoidance. Our approach centers on an intervention-aware latent world model with four prediction heads: dynamics, reward, termination, and a novel per-state intervention-probability head that learns to predict the likelihood of a human takeover at future states. This head provides an actor-side risk-shaping term that discourages the policy from entering "intervention-prone" regions, modeling the operator's internal safety threshold. We evaluate our framework on a 16-DoF LEAP Hand across tasks spanning convex and irregular object grasping, prismatic manipulation, and long-horizon multi-stage tasks. Our results show that predictive risk-shaping enables the system to achieve a 96.7 percent success rate on complex grasping tasks while reducing the operator intervention burden by up to 84 percent in step-weighted terms. By closing the loop between human intuition and predictive world modeling, this work provides a practical safety-aware recipe for training complex dexterous agents in the real world while reducing operator fatigue and hardware-risk exposure.

---

## 27. CR-VLA-Force: Learning Control-aware Compliance VLA Model for Robust Contact-rich Robotic Manipulation

**Authors:** Zhaohong Mai, Chao Wang, Chao Zeng, ..., Shunbo Zhou, Chenguang Yang
**arXiv:** [2609.05832](https://arxiv.org/abs/2609.05832)
**Categories:** Robotics (cs.RO)

Integrating visuomotor policies or Vision-Language-Action (VLA) models with force/torque (F/T) perception has demonstrated significant progress in imitation learning for robotic manipulation. However, existing force-aware VLA models frequently exhibit limited capability in precise force tracking and rapid successive adjustments. This deficiency stems from the limitations of action-chunk execution strategies and the substantial latency between perception and real-time control. Such limitations can lead to task failures and safety risks, particularly when the execution of an action chunk exerts excessive interaction forces without timely adjustment. To overcome this challenge, we propose the Control-aware Compliance VLA (CC-VLA) framework for reactive control. The CC-VLA model employs a multimodal mixture-of-experts (MoE) to encode force signal sequences and vision-language fused feature. Furthermore, it utilizes a multi-stage training strategy to ensure robust perception within the visual-semantic space and effective force perception under sparse sampling conditions. Additionally, a VLA-guided adaptive compliance controller is designed to facilitate precise position tracking during contact-free motion and optimal force-position tracking for contact-rich tasks. To facilitate high-precision F/T data acquisition, we also implement an adversaria shared teleoperation strategy for contact-rich demonstrations that bolsters system safety and interactivity. Extensive real-world experiments demonstrate that CC-VLA significantly improves success rates in challenging force-perception tasks and enhances force-control precision, while providing multi-level safety and robustness under the tested partial-OOD pose-shift settings.

---

## 28. GE-Act 2.0: Pretraining and Scaling a World-Action Model for Robotic Manipulation

**Authors:** AgiBot Research Team, Renhang Liu, Wenzhi Zhao, ..., Sanping Zhou, Maoqing Yao
**arXiv:** [2609.05588](https://arxiv.org/abs/2609.05588)
**Categories:** Robotics (cs.RO); Computer Vision and Pattern Recognition (cs.CV)

World-action models (WAM) predict future states to guide robot actions, enabling learning from both action-free video and action-labeled interaction. Most inherit pretrained video generators, leaving WAM pretraining and scaling underexplored. We introduce Genie Envisioner Act 2.0 (GE-Act 2.0), a world-action model whose trainable generative and action components are all initialized from scratch on manipulation data. It combines a control-oriented autoencoder (CoAE), a single-step visual planner (SVP), and an inverse dynamics model (IDM). CoAE retains action- and instruction-relevant information under aggressive compression, while SVP produces a complete future state in one differentiable pass, so visual planning and inverse dynamics can be pretrained separately on complementary data. The components are then jointly trained with knowledge-aligned selective optimization (KASO), which reduces mismatched supervision by selecting only predicted futures judged behaviorally compatible with the recorded action. We evaluate pretrained checkpoints directly, without per-task fine-tuning, on 100 tasks across 20 manipulation skill groups with held-out scenes, backgrounds, lighting, and object instances. Scaling co-training data from 300 to 30,000 hours raises success from 17.1% to 44.1% on G1-OP and from 13.4% to 31.1% on G2-90D; despite comprising less than 2% of the co-training data, G2-90D improves by 17.7 points, suggesting cross-embodiment transfer. Gains span 19/20 and 18/20 skill groups, and skill-specific coverage strongly correlates with zero-shot out-of-distribution (OOD) success (Pearson r=0.80; Spearman rho=0.85). Under the same protocol, the model grounds object, color, shape, and position references in at least 90% of trials and follows explicit instructions even when they conflict with an already-committed behavior or a conventional scene association.

---

## 29. CST-WM: A Causally Structured World Model for Embodied Visual Tracking

**Authors:** Junyi Hu, Shuaihang Yuan, Yi Fang
**arXiv:** [2609.06302](https://arxiv.org/abs/2609.06302)
**Categories:** Computer Vision and Pattern Recognition (cs.CV); Robotics (cs.RO)

Embodied visual tracking requires a robot not only to react to the current view, but to choose actions that preserve or recover future evidence of a moving target under ego-motion, occlusion, and distractors. It is therefore a predictive decision problem over future target observability and apparent scale. A central difficulty is a task-specific form of causal hallucination: in action-conditioned prediction, a model can exploit the strong correlation between robot control and target-related observations by hallucinating a direct causal effect from the current action to target evidence, rather than letting action influence that evidence only through robot motion and the resulting observation change. The shortcut yields plausible futures with the wrong semantics for tracking-oriented planning and re-acquisition. We propose CST-WM, a causally structured world model that decomposes the latent state into target-evidence, robot, and observation branches and factorizes the transition so that direct action injection into the target-evidence branch is blocked, while action remains available to robot motion and observation updates. Combined with rollout-based model-predictive control, CST-WM supports both stable following and temporary target re-acquisition in one planning framework. On EVT-Bench and Habitat 3.0, covering standard tracking, target-loss recovery, and cross-dataset transfer, it improves following quality, distance-range control, safety, and re-acquisition over reactive and world-model baselines; offline diagnostics show better multi-step rollout fidelity, stronger planning-value consistency, and substantially reduced direct action leakage. For embodied visual tracking, future prediction alone is not enough: the predictive structure itself must align with how target evidence enters planning.

---

## 30. MobileVLA-R1 2.0: RL-Enhanced Reasoning for Mobile Robot Control

**Authors:** Ting Huang, Yue Huang, Zeyu Zhang, Shuicheng Yan, Hao Tang
**arXiv:** [2609.06251](https://arxiv.org/abs/2609.06251)
**Categories:** Computer Vision and Pattern Recognition (cs.CV); Robotics (cs.RO)

Grounding natural-language instructions into reliable and executable actions remains a fundamental challenge for vision-language-action (VLA) systems on mobile robots, due to the persistent gap between high-level semantic reasoning and low-level locomotion and manipulation control. Existing approaches often rely on implicit reasoning or monolithic action prediction, making it difficult to maintain coherent long-horizon decision making while producing precise and adaptable robot actions. To address this challenge, we propose MobileVLA-R1 2.0, an RL-enhanced VLA framework that explicitly couples structured embodied reasoning with executable mobile robot control. The framework learns multi-granularity reasoning over embodied trajectories through supervised Chain-of-Thought (CoT) alignment and reinforcement learning, improving reasoning-to-action consistency beyond purely behavioral supervision. To support both locomotion and manipulation, we further introduce a reasoning-conditioned action decoder that maps multimodal reasoning representations to task-level action targets, which are subsequently translated into embodiment-specific commands by robot controllers. This design provides a unified perception-reasoning-action interface while decoupling high-level action generation from robot-specific actuation. We conduct extensive evaluations on language-guided navigation, quadruped control, and humanoid mobile manipulation, covering VLN-CE, QUARD, and real-world deployments on Unitree Go2 and G1 robots. MobileVLA-R1 2.0 consistently outperforms strong VLA baselines, achieving an average 1.6 point improvement in SR on VLN-CE and a 10.0 point improvement in full-task success on real-world G1 mobile manipulation tasks over MobileVLA-R1, while demonstrating robust long-horizon instruction following and closed-loop execution across different robotic platforms.

---

## 31. SyncWorld: Visual Calibration Enables World Models as Zero-Shot Simulators

**Authors:** Yuncong Yang, Zhengtao Han, Furkan Ozyurt, ..., Yilun Du, Chuang Gan
**arXiv:** [2609.09155](https://arxiv.org/abs/2609.09155)
**Categories:** Computer Vision and Pattern Recognition (cs.CV)

World models are increasingly used as policy-in-the-loop imagination environments, where reliable rollouts require fine-grained controllability with respect to low-level robot actions. A key obstacle to scaling such models in robotics is that actions are not a universal language in pixel space: changes in visual environment, camera view, robot placement, or embodiment alter how the same numerical action manifests visually, leading to conflicting supervision under mixed training and brittle generalization at deployment. We introduce SyncWorld, an action-conditioned world model that serves as a zero-shot simulator across unseen environments without any additional training. SyncWorld leverages a visual calibration episode---paired frames and actions that showcase all the controllable degrees of freedom---to specify the setup-specific Action--Visual Mapping in context. Training with visual calibration contexts teaches the model to interpret actions through visual evidence and to leverage interaction history when explicit calibration is unavailable. Experiments show that SyncWorld can accurately simulate action outcomes in previously unseen settings, and that its capability of simulating rollouts enables test-time policy improvement without training.

---

## 32. VeriScene: Reconstructing Crime Scenes from Legal Evidence via World-Model Agent

**Authors:** Kevin Chuanpu Fu, Yongsen Zheng, Zee Kin Yeong, Kwok-Yan Lam
**arXiv:** [2609.08342](https://arxiv.org/abs/2609.08342)
**Categories:** Computer Vision and Pattern Recognition (cs.CV); Cryptography and Security (cs.CR)

World models take multimodal inputs like text, photos, and diagrams to generate dynamic scenes in accordance with the laws of physics, thus opening a compelling application: fusing multimodal legal evidence to re-create a crime scene and re-enact how an offence could have been committed. However, feeding the raw, unorganized evidence into a world model fails in forensic use: it silently drops evidence, glosses over contradictory testimony, and produces motion that violates the evidentiary record. This paper presents VeriScene, an agent that orchestrates the world model: it reconstructs crime scenes from forensic photographs and witness statements of varying reliability, keeping every claim traceable to evidence and every motion physically plausible. VeriScene iteratively fuses the evidence into a cited narrative under an auditing loop, verifies the hypothesized dynamics via probe rollouts in the world model with corrective constraint injection, and renders the offence as a re-enactment video from a fused keyframe. On a benchmark of 25 crime scenarios across 7 physically-driven case types (139 forensic-style photographs and 65 statements with planted unreliability), VeriScene attains 0.9014 evidence coverage and 0.7217 factual consistency (0-1 scale) on the 20 test scenes, outperforming an end-to-end multimodal-LLM baseline by 20.35% in factual consistency and 34.88% in temporal coherence, while generalizing across four LLM orchestration backends at USD 1.82 per scene.

---

## 33. Learning to Use Imagination: Progress-Conditioned Future Utilization for World Action Models

**Authors:** Yijie Zhu, Zitong Yu, Wei Li, ..., Rui Shao, Liqiang Nie
**arXiv:** [2609.06578](https://arxiv.org/abs/2609.06578)
**Categories:** Computer Vision and Pattern Recognition (cs.CV)

World Action Models (WAMs) extend Vision-Language-Action (VLA) models by incorporating future visual dynamics into action generation. However, existing WAMs often utilize imagined futures with limited adaptation to evolving execution progress, potentially introducing distracting or unreliable predictive cues. This limitation arises from two empirically identified forms of non-uniformity in future utility: (i) at the inter-progress level, the utility of imagined futures varies across execution stages as control demands change; and (ii) at the intra-progress level, individual future latents exhibit heterogeneous relevance within the same progress state. To address these limitations, we propose ProWAM, a Progress-Conditioned World Action Model that introduces execution progress as an explicit intermediate representation for adaptive imagination utilization. ProWAM comprises two tightly coupled components: (1) To obtain a reliable representation of execution progress, we propose the Self-Supervised Dual-Temporal Progress Encoder (SS-DTPE). SS-DTPE couples short-term action-observation interaction modeling with long-term recurrent progress aggregation to capture recent execution feedback and accumulated task history. (2) Conditioned on the progress representation from SS-DTPE, we propose the Hierarchical Progress-Conditioned Imagination Modulation (HPIM) to adapt imagination utilization to execution progress. HPIM operates at two complementary levels: an inter-progress global modulation mechanism adapts future utilization across execution stages, while an intra-progress relevance mechanism differentiates individual future latents within each progress state. Extensive experiments demonstrate consistent gains over strong VLA and WAM baselines.

---
