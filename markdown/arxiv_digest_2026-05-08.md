# arXiv Daily Digest — 2026-05-08

**Mode:** direct
**Categories:** cs.AI, cs.LG, cs.RO, cs.CV
**Keywords:** VLA, world model, world action model
**Papers found:** 11

---

## 1. HaM-World: Soft-Hamiltonian World Models with Selective Memory for Planning

**Authors:** Haoyun Tang, Haodong Cui, Keyao Xu, Kun Wang, Zhandong Mei
**arXiv:** [2605.05951](https://arxiv.org/abs/2605.05951)
**Categories:** Artificial Intelligence (cs.AI)

World models enable model-based planning through learned latent dynamics, but imagined rollouts become unstable as the planning horizon grows or the dynamics distribution shifts. We argue that this instability reflects two missing structures in planner-facing latents: history-conditioned memory for approximate Markov completeness, and geometric organization that separates configuration, momentum, and task semantics. We propose HaM-World (HMW), a structured world model that decomposes the latent state into a canonical (q, p) subspace and a context subspace c, while using Mamba selective state-space memory as the history-conditioned input to the same latent dynamics. Within this interface, (q, p) evolves through an energy-derived Hamiltonian vector field plus learnable residual/control dynamics, while c captures semantic, dissipative, and non-conservative factors. This gives the planner a single latent state shared by dynamics prediction, reward/value estimation, imagined rollouts, and CEM action search. On four DeepMind Control Suite tasks, HaM-World reaches the highest Avg. AUC (117.9, +9.5%), reduces long-horizon rollout error to 45% of a strong baseline model, and wins 11/12 k in {3,5,7} MSE cells. Under 12 OOD perturbations spanning dynamics shifts, action delay, and observation masking, HaM-World achieves the highest return in every condition, with average OOD-return gains of 10.2% on Finger Spin and 13.6% on Reacher Easy. Mechanism diagnostics further show bounded action-free Hamiltonian-energy drift, structured energy variation under policy rollouts, and coherent control-induced energy transfer, supporting the intended Soft-Hamiltonian dynamics design.

---

## 2. Render, Don't Decode: Weight-Space World Models with Latent Structural Disentanglement

**Authors:** Roussel Desmond Nzoyem, Mauro Comi
**arXiv:** [2605.06298](https://arxiv.org/abs/2605.06298)
**Categories:** Computer Vision and Pattern Recognition (cs.CV); Artificial Intelligence (cs.AI)

Training world models on vast quantities of unlabelled videos is a critical step toward fully autonomous intelligence. However, the prevailing paradigm of encoding raw pixels into opaque latent spaces and relying on heavy decoders for reconstruction leaves these models computationally expensive and uninterpretable. We address this problem by introducing NOVA, a world modelling framework that represents the system state as the weights and biases of an auxiliary coordinate-based implicit neural representation (INR). This structured representation is analytically rendered, which eliminates the decoder bottleneck while conferring compactness, portability, and zero-shot super-resolution. Furthermore, like most latent action models, NOVA can be distilled into a context-dependent video generator via an action-matching objective. Surprisingly, without resorting to auxiliary losses or adversarial objectives, NOVA can disentangle structural scene components such as background, foreground, and inter-frame motion, enabling users to edit either content or dynamics without compromising the other. We validate our framework on several challenging datasets, achieving strong controllable forecasting while operating on a single consumer GPU at $\sim$40M parameters. Ultimately, structured representations like INRs not only enhance our understanding of latent dynamics but also pave the way for immersive and customisable virtual experiences.

---

## 3. When to Trust Imagination: Adaptive Action Execution for World Action Models

**Authors:** Rui Wang, Yue Zhang, Jiehong Lin, ..., Zhongrui Wang, Xiaojuan Qi
**arXiv:** [2605.06222](https://arxiv.org/abs/2605.06222)
**Categories:** Robotics (cs.RO); Artificial Intelligence (cs.AI)

World Action Models (WAMs) have recently emerged as a promising paradigm for robotic manipulation by jointly predicting future visual observations and future actions. However, current WAMs typically execute a fixed number of predicted actions after each model inference, leaving the robot blind to whether the imagined future remains consistent with the actual physical rollout. In this work, we formulate adaptive WAM execution as a future-reality verification problem: the robot should execute longer when the WAM-predicted future remains reliable, and replan earlier when reality deviates from imagination. To this end, we propose Future Forward Dynamics Causal Attention (FFDC), a lightweight verifier that jointly reasons over predicted future actions, predicted visual dynamics, real observations, and language instructions to estimate whether the remaining action rollout can still be trusted. FFDC enables adaptive action chunk sizes as an emergent consequence of prediction-observation consistency, preserving the efficiency of long-horizon execution while restoring responsiveness in contact-rich or difficult phases. We further introduce Mixture-of-Horizon Training to improve long-horizon trajectory coverage for adaptive execution. Experiments on the RoboTwin benchmark and in the real world demonstrate that our method achieves a strong robustness-efficiency trade-off: on RoboTwin, it reduces WAM forward passes by 69.10% and execution time by 34.02%, while improving success rate by 2.54% over the short-chunk baseline; in real-world experiments, it improves success rate by 35%.

---

## 4. EA-WM: Event-Aware Generative World Model with Structured Kinematic-to-Visual Action Fields

**Authors:** Zhaoyang Yang, Yurun Jin, Lizhe Qi, Cong Huang, Kai Chen
**arXiv:** [2605.06192](https://arxiv.org/abs/2605.06192)
**Categories:** Computer Vision and Pattern Recognition (cs.CV); Artificial Intelligence (cs.AI); Robotics (cs.RO)

Pretrained video diffusion models provide powerful spatiotemporal generative priors, making them a natural foundation for robotic world models. While recent world-action models jointly optimize future videos and actions, they predominantly treat video generation as an auxiliary representation for policy learning. Consequently, they insufficiently explore the inverse problem: leveraging action signals to guide video synthesis, thereby often failing to preserve precise robot spatial geometry and fine-grained robot-object interaction dynamics in the generated rollouts. To bridge this gap, we present EA-WM, an Event-Aware Generative World Model that effectively closes the loop between kinematic control and visual perception. Rather than injecting joint or end-effector actions as abstract, low-dimensional tokens, EA-WM projects actions and kinematic states directly into the target camera view as Structured Kinematic-to-Visual Action Fields. To fully exploit this geometrically grounded representation, we introduce event-aware bidirectional fusion blocks that modulate cross-branch attention, capturing object state changes and interaction dynamics. Evaluated on the comprehensive WorldArena benchmark, EA-WM achieves state-of-the-art performance, outperforming existing baselines by a significant margin.

---

## 5. Reconstruction or Semantics? What Makes a Latent Space Useful for Robotic World Models

**Authors:** Nilaksh, Saurav Jha, Artem Zholus, Sarath Chandar
**arXiv:** [2605.06388](https://arxiv.org/abs/2605.06388)
**Categories:** Computer Vision and Pattern Recognition (cs.CV); Machine Learning (cs.LG); Robotics (cs.RO)

World model-based policy evaluation is a practical proxy for testing real-world robot control by rolling out candidate actions in action-conditioned video diffusion models. As these models increasingly adopt latent diffusion modeling (LDM), choosing the right latent space becomes critical. While the status quo uses autoencoding latent spaces like VAEs that are primarily trained for pixel reconstruction, recent work suggests benefits from pretrained encoders with representation-aligned semantic latent spaces. We systematically evaluate these latent spaces for action-conditioned LDM by comparing six reconstruction and semantic encoders to train world model variants under a fixed protocol on BridgeV2 dataset, and show effective world model training in high-dimensional representation spaces with and without dimension compression. We then propose three axes to assess robotic world model performance: visual fidelity, planning and downstream policy performance, and latent representation quality. Our results show visual fidelity alone is insufficient for world model selection. While reconstruction encoders like VAE and Cosmos achieve strong pixel-level scores, semantic encoders such as V-JEPA 2.1 (strongest overall on policy), Web-DINO, and SigLIP 2 generally excel across the other two axes at all model scales. Our study advocates semantic latent space as stronger foundation for policy-relevant robotics diffusion world models.

---

## 6. OA-WAM: Object-Addressable World Action Model for Robust Robot Manipulation

**Authors:** Yushan Liu, Peibo Sun, Shoujie Li, ..., Xiao-Ping Zhang, Wenbo Ding
**arXiv:** [2605.06481](https://arxiv.org/abs/2605.06481)
**Categories:** Robotics (cs.RO)

World Action Models (WAMs) enhance Vision-Language-Action policies by jointly predicting scene evolution and robot actions, but existing methods usually represent the predicted world as holistic images, video tokens, or global latents. These representations are difficult for an action decoder to address when an instruction refers to a particular object, especially under scene shifts where object identity is entangled with context. We propose OA-WAM, an Object-Addressable World Action Model for robust robot manipulation. OA-WAM decomposes each frame into N+1 slot states, with one robot slot and N object slots. Each slot contains a persistent address vector and a time-varying content vector, and is fused with text, image, proprioception, and past-action tokens in a block-causal sequence. A world head predicts next-frame slot states, while a flow-matching action head decodes a 16-step continuous action chunk in the same forward pass. Addressability is enforced by routing cross-slot attention through address-only keys and resetting the address slice at every transformer layer, separating which object to act on from what that object currently is without adding extra tokens. OA-WAM matches strong VLA and WAM baselines on LIBERO (97.8%) and SimplerEnv (79.3%), reaches state-of-the-art performance on the most relevant LIBERO-Plus geometric axes, and remains competitive on the seven-axis aggregate. A causal slot-intervention test yields a swap-binding cosine of 0.87, versus at most 0.09 for holistic baselines. These results suggest that addressable object states provide an effective interface for robust world-action modeling under scene perturbations.

---

## 7. CKT-WAM: Parameter-Efficient Context Knowledge Transfer Between World Action Models

**Authors:** Yuhua Jiang, Yijun Guo, Hongbing Yang, ..., Feifei Gao, Biqing Qi
**arXiv:** [2605.06247](https://arxiv.org/abs/2605.06247)
**Categories:** Robotics (cs.RO)

World action models (WAMs) provide a powerful generative framework for embodied control, yet transferring knowledge across heterogeneous WAMs remains challenging due to mismatched latent interfaces, high adaptation cost, and the rigidity of conventional distillation objectives. We propose \textbf{CKT-WAM}, a parameter-efficient \textbf{C}ontext \textbf{K}nowledge \textbf{T}ransfer framework that transfers teacher WAM's knowledge into a student WAM through a compact context in the text embedding space, rather than output imitation or dense hidden-state matching. Specifically, CKT-WAM extracts intermediate teacher hidden states, reduces the number of tokens via compressors' learnable-query cross attention (LQCA), and transforms them through an always-on generalized adapter, a lightweight router, and sparsely activated specialized adapters. The resulting context is then appended to the student's conditioning textual embeddings, thereby injecting the transferred knowledge into the student with minimal architectural modification. Experiments show that CKT-WAM consistently improves zero-shot generalization and achieves the best overall performance on LIBERO-Plus, reaching 86.1\% total success rate with only 1.17\% trainable parameters, while approaching full fine-tuning performance. Beyond simulation, CKT-WAM also demonstrates strong real-world long-horizon manipulation ability, achieving the best average success rate of 83.3\% across four multi-step and long-horizon tasks. Code is available at this https URL.

---

## 8. VLA-GSE: Boosting Parameter-Efficient Fine-Tuning in VLA with Generalized and Specialized Experts

**Authors:** Yuhua Jiang, Junjie Lu, Xinyao Qin, ..., Feifei Gao, Li Zhao
**arXiv:** [2605.06175](https://arxiv.org/abs/2605.06175)
**Categories:** Robotics (cs.RO)

Vision-language-action (VLA) models inherit rich visual-semantic priors from pre-trained vision-language backbones, but adapting them to robotic control remains challenging. Full fine-tuning (FFT) is prone to overfitting on downstream robotic data and catastrophic forgetting of pretrained vision-language capabilities. Parameter-efficient fine-tuning (PEFT) better preserves pre-trained knowledge, yet existing PEFT methods still struggle to adapt effectively to robot control tasks. To address this gap, we propose VLA-GSE, a parameter-efficient VLA fine-tuning framework that improves control adaptation while retaining PEFT's knowledge preservation advantage. Specifically, VLA-GSE (Generalized and Specialized Experts) is initialized by spectrally decomposing the frozen backbone, assigning leading singular components to generalized experts (shared experts) and disjoint residual components to specialized experts (routed experts). This decomposition improves adaptation capacity under a fixed trainable-parameter budget. Under a comparable parameter budget, VLA-GSE updates only 2.51% of the full model parameters and consistently outperforms strong FFT and PEFT baselines. It achieves 81.2% average zero-shot success on LIBERO-Plus, preserves pre-trained VLM capability comparably to LoRA on multimodal understanding benchmarks, and improves real-world manipulation success under multiple distribution shifts. Code is available at: this https URL

---

## 9. TriRelVLA: Triadic Relational Structure for Generalizable Embodied Manipulation

**Authors:** Hanyu Zhou, Chuanhao Ma, Gim Hee Lee
**arXiv:** [2605.05714](https://arxiv.org/abs/2605.05714)
**Categories:** Computer Vision and Pattern Recognition (cs.CV); Robotics (cs.RO)

Vision-language-action (VLA) models perform well on training-seen robotic tasks but struggle to generalize to unseen scenes and objects. A key limitation lies in their implicit visual representations, which entangle object appearance, background, and scene layout. This makes policies sensitive to visual variations. Prior work improves transferability through structured intermediate representations that objectify visual content. However, these representations mainly capture scene semantics instead of action-relevant relations. As a result, action prediction remains tied to appearance statistics. We observe that manipulation actions depend on the object-hand-task relational structure, which governs interactions among task requirements, robot states, and object properties. Based on this observation, we propose TriRelVLA, a triadic relational VLA framework for generalizable embodied manipulation. Our approach consists of three components: 1) We construct explicit object-hand-task triadic representations from multimodal inputs as relational primitives. 2) We build a task-grounded relational graph. Task-guided cross-attention forms nodes, and a relation-aware graph transformer models interactions among them. 3) We perform relation-conditioned action generation. The relational structure is compressed into a bottleneck space and projected into the LLM for action prediction. This triadic relational bottleneck reduces reliance on appearance statistics and enables transfer across scenes, objects, and task compositions. We further introduce a real-world robotic dataset for fine-tuning. Experiments show strong performance on fine-tuned tasks and clear gains in cross-scene, cross-object, and cross-task generalization.

---

## 10. Earth-o1: A Grid-free Observation-native Atmospheric World Model

**Authors:** Junchao Gong, Kaiyi Xu, Wangxu Wei, ..., Ben Fei, Lei Bai
**arXiv:** [2605.06337](https://arxiv.org/abs/2605.06337)
**Categories:** Computer Vision and Pattern Recognition (cs.CV)

Despite the unprecedented volume of multimodal data provided by modern Earth observation systems, our ability to model atmospheric dynamics remains constrained. Traditional modeling frameworks force heterogeneous measurements into predefined spatial grids, inherently limiting the full exploitation of raw sensor data and creating severe computational bottlenecks. Here we present Earth-o1, an observation-native atmospheric world model that overcomes these structural limitations. Rather than relying on conventional atmospheric dynamical modeling systems or traditional data assimilation, Earth-o1 directly learns the continuous, three-dimensional physical evolution of the Earth system from ungridded observational data. By integrating diverse sensor inputs into a unified, grid-free dynamical field, the model autonomously advances the atmospheric state in space and time. We show that this fundamentally distinct paradigm enables direct, real-time forecasting and cross-sensor inference without the overhead of explicit numerical solvers. In hindcast evaluations, Earth-o1 achieves surface forecast skill comparable to the operational Integrated Forecasting System (IFS). These results establish that continuous, observation-driven world models -- a new class of fully observation-native geophysical simulators -- can match the fidelity of established physical frameworks, providing a scalable data-driven foundation for a digital twin of the Earth.

---

## 11. Toward Visually Realistic Simulation: A Benchmark for Evaluating Robot Manipulation in Simulation

**Authors:** Yixin Zhu, Zixiong Wang, Jian Yang, ..., Jiayuan Gu, Beibei Wang
**arXiv:** [2605.06311](https://arxiv.org/abs/2605.06311)
**Categories:** Robotics (cs.RO)

Reliable simulation evaluation of robot manipulation policies serves as a high-fidelity proxy for real-world performance. Although existing benchmarks cover a wide range of task categories, they lack visual realism, creating a large domain gap between simulation and reality. This undermines the reliability of simulation-based evaluation in predicting real-world performance. To mitigate the sim-to-real visual gap, we conduct a systematic analysis to isolate the effects of lighting and material. Our results show that these factors play a critical role in geometric reasoning and spatial grounding, yet are largely overlooked in existing benchmarks. Motivated by the analysis, we propose VISER, a visually realistic benchmark for evaluating robot manipulation in simulation. VISER features a high-fidelity dataset of over 1,000 3D assets with physically-based rendering (PBR) materials, along with 3D scenes created from these assets through curated layouts or generation. To this end, we propose an automated pipeline leveraging Multi-modal Large Language Models (MLLMs) for material-aware part segmentation and material retrieval, enabling scalable generation of physically plausible assets. Building on the high-fidelity 3D asset dataset, we construct diverse evaluation tasks, such as grasping, placing, and long-horizon tasks, enabling scalable and reproducible assessment of Vision-Language-Action (VLA) models. Our benchmark shows a strong correlation between simulation and real-world performance, achieving an average Pearson correlation coefficient of 0.92 across different policies.

---
