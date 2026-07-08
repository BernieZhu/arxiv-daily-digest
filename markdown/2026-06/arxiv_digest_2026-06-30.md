# arXiv Daily Digest — 2026-06-30

**Mode:** direct
**Categories:** cs.AI, cs.LG, cs.RO, cs.CV
**Keywords:** VLA, world model, world action model
**Papers found:** 32

---

## 1. Self-Evolving World Models for LLM Agent Planning

**Authors:** Xuan Zhang, Wenxuan Zhang, See-Kiong Ng, Yang Deng
**arXiv:** [2606.30639](https://arxiv.org/abs/2606.30639)
**Categories:** Artificial Intelligence (cs.AI); Computation and Language (cs.CL)

World models offer a principled way to equip long-horizon LLM agents with foresight: predictions of action consequences before execution. However, unreliable foresight can be ignored, misused, or even degrade downstream decision-making. In this paper, we introduce WorldEvolver, a self-evolving world model framework that revises its deployment-time context while keeping the downstream agent and all model parameters frozen. WorldEvolver integrates three modules: (i) Episodic Memory, which exploits real action transitions through retrieval-based simulation; (ii) Semantic Memory, which extracts persistent heuristic rules from prediction-observation mismatches; and (iii) Selective Foresight, which filters low-confidence predictions before integrating them into agent reasoning context. We evaluate WorldEvolver on ALFWorld and ScienceWorld, measuring world model prediction accuracy on Word2World and downstream agent success rate on AgentBoard. Extensive experiments show that WorldEvolver achieves the highest prediction accuracy across three backbones and leads other world model baselines on downstream agent success rate, demonstrating that test-time memory revision enhances both predictive fidelity and planning performance.

---

## 2. The CRISTAL Method: Neurosymbolic analysis from AI-synthesized world models

**Authors:** Rafael Kaufmann, Felix Neubürger, Michael Walters, Thomas Kopinski, Dimitrije Marković
**arXiv:** [2606.29799](https://arxiv.org/abs/2606.29799)
**Categories:** Artificial Intelligence (cs.AI)

This project introduces the CRISTAL Method (Coherent Reliable Intentional Synthesis of Truthful Analysis Logic), a neurosymbolic framework for automating complex analysis workflows, with fundamental investment analysis as a primary use case. This domain poses major challenges: high structural uncertainty, noisy and subjective data, tight attention budgets, and the need for justified, reproducible decisions. Human analysts often struggle in this domain due to cognitive biases and limitations, suggesting significant value in automation. But while LLM-based agents have been proposed as analytical aids, their limitations -- poor numerical reasoning, unawareness of uncertainty, and lack of reproducibility -- hinder their effectiveness in this context. CRISTAL addresses these gaps through a principled blend of statistical model synthesis, continuous learning, and active learning. Starting from a natural-language prior knowledge curriculum, CRISTAL builds a dynamic, interpretable probabilistic program that enables full Bayesian inference, including uncertainty quantification and budget-aware data acquisition. CRISTAL continually refines its world model during analysis, leveraging LLMs for code synthesis and learning. We validate CRISTAL on a novel benchmark of synthetic equities with rich financial and textual data. On a company classification task, CRISTAL achieves Bayes-optimal accuracy with just 5 examples and a 5-second budget, outperforming state-of-the-art LLMs that plateau around 40\% accuracy even with order-of-magnitude more input data and compute.

---

## 3. Cognitive World Models for Process-Level Social Influence Evaluation

**Authors:** Minghui Ma, Bin Guo, Han Wang, ..., Yan Liu, Zhiwen Yu
**arXiv:** [2606.29495](https://arxiv.org/abs/2606.29495)
**Categories:** Artificial Intelligence (cs.AI)

Social influence dialogue changes user behavior by altering internal cognitive states. The central evaluation question is whether the user's beliefs, desires, intentions, and emotions measurably change over the course of conversation, a process-oriented criterion that neither surface-level text metrics (BLEU/ROUGE) nor single-score LLM judgments can capture. We propose the \textbf{Cog}nitive \textbf{W}orld \textbf{M}odel \textbf{(CogWM)}, an LLM-based user model that reframes multi-turn dialogue evaluation from ``what did the user say'' to ``how did the user's internal cognitive state evolves.'' CogWM jointly predicts BDI/E cognitive states and user utterances and serves as both a user simulator and an evaluation platform, using a three-tier evaluation framework that covers turn-level fidelity, trajectory-level state dynamics, and task-level composite scoring. Trained via our \textbf{S}ummarize-\textbf{a}nd-\textbf{A}llocate \textbf{(SaA)} annotation pipeline on 150,454 user-turn samples across four social influence scenarios, CogWM achieves 77.6\% emotion accuracy (2.1$\times$ over GPT-5.5). In 3600 multi-agent discrimination trials, it distinguishes six commercial agents by their cognitive influence, with Llama-4-Scout ranking first (CTS +0.233). CogWM moves social influence dialogue evaluation from terminal judgment to process tracking. We have released our code\footnote{\scriptsize Code: this https URL} and models\footnote{Model: this https URL}.

---

## 4. SurgVLA-Bench: Towards Evaluating Vision-Language-Action Models for Laparoscopic Surgical Robotics

**Authors:** Jiashuo Sun, Yue He, Wenxuan Liu, ..., Xiang Chen, Min Liu
**arXiv:** [2606.29247](https://arxiv.org/abs/2606.29247)
**Categories:** Artificial Intelligence (cs.AI)

Vision-Language-Action (VLA) models represent a promising direction for embodied intelligence in surgical robotics. Despite the prevalence of VLA benchmarks for general robotics, standardized evaluation platforms specifically designed for surgical contexts remain absent. To address this limitation, we present SurgVLA-Bench, the first comprehensive benchmark for evaluating VLA models in laparoscopic surgical robotics. Leveraging the SurRoL simulation platform, we construct a hierarchical task taxonomy ranging from atomic actions to complete surgical procedures, complemented by a multi-dimensional evaluation framework assessing action accuracy and semantic consistency. We then systematically evaluate two representative paradigms, including autoregressive models such as OpenVLA, and flow matching models such as $\pi_{0}$, $\pi_{0.5}$, and SmolVLA. Our experiments show that autoregressive models tend to excel in semantic understanding, while flow matching models often achieve higher task precision but may face generalization trade-offs. However, even the best-performing models remain far from satisfactory, as the constrained endoscopic field of view, restricted viewing angles, and frequent occlusions persist as fundamental physical bottlenecks. The code and data are available at this https URL

---

## 5. SA-VLA: State-aware tokenizer for improving Vision-Language-Action Models' performance

**Authors:** Tengyue Jiang, Chunpu Xu, Jiayue Kang, Yao Mu
**arXiv:** [2606.30113](https://arxiv.org/abs/2606.30113)
**Categories:** Robotics (cs.RO); Artificial Intelligence (cs.AI)

Discrete action tokenization provides a compact interface for autoregressive VLA policies, but accurately recovering continuous robot actions from discrete codes remains challenging. Existing tokenizers typically map each discrete code to a fixed continuous action prototype, ignoring the robot's current proprioceptive state. This limitation is particularly pronounced in manipulation, where the same action token may require different continuous controls under different joint configurations, object poses, and contact conditions. We therefore propose SA-VLA, a state-aware action tokenizer that conditions action decoding on robot state. We study two state-injection mechanisms for VQ-based action tokenization: cross-attention between state and action features, and a lightweight state adapter that predicts action-wise modulation factors for state-conditioned action modulation and reconstruction. The adapter formulation expands the effective support of a finite codebook by allowing each discrete token to represent a family of state-dependent continuous actions, while preserving the efficiency and compatibility of discrete action modeling. Integrated into an LLM-based VLA policy, SA-VLA supports both autoregressive and parallel action-token decoding with minimal changes to the model interface. On 12 RoboTwin manipulation tasks, SA-VLA improves the average success rate from 0.29 to 0.56 over the strongest tokenizer baseline. In zero-shot sim-to-real experiments on three real-world tasks, it further improves average success from 0.15 to 0.33 over the strongest tokenizer baseline. These results demonstrate that state-conditioned action decoding is a simple and effective mechanism for reducing the compression gap in discrete VLA policies.

---

## 6. Pondering the Way: Spatial-perceiving World Action Model for Embodied Navigation

**Authors:** Hong Chen, Daqi Liu, Zehan Zhang, ..., Hangjun Ye, Yihua Tan
**arXiv:** [2606.29908](https://arxiv.org/abs/2606.29908)
**Categories:** Robotics (cs.RO); Artificial Intelligence (cs.AI)

Existing world model-based planners for visual navigation typically follow a verification-centric paradigm, decoupling goal intent from trajectory synthesis. This approach suffers from candidate dependence, heavy computational overhead, and inconsistencies between sampled actions and predicted visuals. To address these issues, we propose SWAM (Spatial-perceiving World Action Model), a task-centric joint observation-action generation framework. Given start and goal RGB observations, SWAM performs single-pass inference to simultaneously generate intermediate RGB-D sequences and corresponding action trajectories, promoting goal-consistent trajectory generation and improved spatial feasibility. While SWAM leverages depth pseudo-labels during training to internalize spatial priors, it requires only monocular RGB input at inference time. We further introduce a visual-guided action refinement module and a trajectory-scale regularization loss to enforce fine-grained alignment between motion and visual cues while stabilizing predictions across varying distances. Extensive experiments show that SWAM significantly outperforms state-of-the-art two-stage planners in success rate, trajectory accuracy, and inference efficiency, while demonstrating robust zero-shot generalization to unseen environments.

---

## 7. Trust Your Instincts: Confidence-Driven Test-Time RL for Vision-Language-Action Models

**Authors:** Siyao Chen, Jiakang Yuan, Jiaxin Wang, Tao Chen
**arXiv:** [2606.29892](https://arxiv.org/abs/2606.29892)
**Categories:** Robotics (cs.RO); Artificial Intelligence (cs.AI)

Reinforcement learning (RL) has become indispensable for pushing Vision-Language-Action Models (VLAs) beyond static imitation learning. However, existing RL methods typically require external environmental feedback, relying on predefined success signals to guide policy updates. In this work, we show that VLA models possess useful internal evaluative capabilities: in discrete-action VLAs, trajectories with higher generation confidence are significantly more likely to succeed. Based on this observation, we introduce T^2VLA (Test-time VLA), an architecture-agnostic test-time RL framework that enables VLA models to achieve self-bootstrapping policy improvement. Instead of relying on external rewards, T^2VLA leverages trajectory-level similarity to high-confidence expert demonstrations as an intrinsic reward signal. In addition, we propose a Confidence-Driven Dual Expert Bootstrapping mechanism, which dynamically balances a Local Pseudo-Expert for exploration and a Global Expert Pool for training stability. Extensive experiments on the LIBERO and RoboTwin benchmarks show that T^2VLA consistently outperforms supervised baselines and approaches oracle RL performance with ground-truth rewards, achieving effective improvement without external reward feedback. Furthermore, T^2VLA adapts to distinct VLA paradigms, including both OpenVLA-OFT and the pi series.

---

## 8. LWDrive: Layer-Wise World-Model-Guided Vision-Language Model Planning for Autonomous Driving

**Authors:** Chen Yang, Yuhao Wei, Ze Xu, ..., Jie Li, Guofa Li
**arXiv:** [2606.29879](https://arxiv.org/abs/2606.29879)
**Categories:** Computer Vision and Pattern Recognition (cs.CV); Artificial Intelligence (cs.AI)

Vision-Language Models (VLMs) provide powerful semantic understanding and commonsense reasoning for End-to-End Autonomous Driving (E2E-AD) planning. However, trajectories directly generated by VLMs often encode only coarse driving intentions and remain insufficient for geometrically accurate, future-aware, and multi-view-grounded planning. To address these limitations, we develop the Layer-Wise World-Model-Guided Driving framework (LWDrive). LWDrive is a VLM planning framework that refines coarse trajectories through layer-wise world-model guidance. Instead of treating the VLM output as the final trajectory, LWDrive uses it as an intent-aware coarse plan, expands a diverse candidate space around it, and progressively refines the candidates through a Foresight Cascade Planner (FCP). Specifically, we introduce future-frame generation supervision to encourage the VLM to learn forward-looking scene representations, thereby injecting planning-relevant predictive dynamics into its internal hidden states. Built upon these world-model-supervised representations, FCP exploits VLM features across multiple layers and integrates historical temporal states, Action-Query representations, and current-frame multi-view Bird's-Eye-View (BEV) features to refine candidate trajectories in a coarse-to-fine manner. This design enables progressive correction of spatial positions and motion trends while grounding trajectory refinement with multi-view scene cues and preserving the high-level driving intention produced by the large model. Finally, a score head evaluates the refined candidates and selects the best trajectory as the final planning output. Experiments show that LWDrive achieves a score of 92.0 on the NAVSIM benchmark and 89.6 on NAVSIM-v2. Code and models will be made publicly available.

---

## 9. Early Warning Signals for OpenVLA Failure under Visual Distribution Shift

**Authors:** Dipesh Tharu Mahato, Rachel Ren
**arXiv:** [2606.29699](https://arxiv.org/abs/2606.29699)
**Categories:** Computer Vision and Pattern Recognition (cs.CV); Artificial Intelligence (cs.AI)

Vision Language Action models combine perception, language grounding, and control in a single policy, but their failures are hard to diagnose once visual conditions shift. We test whether OpenVLA feedforward activations contain linearly decodable information about near term task failure in LIBERO manipulation rollouts. The policy is fixed throughout. We log internal activations during execution and fit lightweight monitors after the rollouts are collected. Occlusion is the main controlled stress test. It reduces OpenVLA success from $57\%$ to $17\%$ over $100$ episodes per condition. Under this shift, a logistic probe at layer 16 reaches AUROC $0.972$ and AUPRC $0.352$ for predicting failure within a $15$ step horizon. It outperforms both a mean difference direction and an action disagreement baseline. A sparse layer sweep finds uneven decodability across depth: layer 16 is strongest among the tested layers, layer 8 remains informative, and layer 10 is weaker. To check whether the monitor is just an occlusion detector, we also evaluate color shift and camera jitter without refitting. Color shift produces no failures in this setting, so it is a benign control rather than a failure benchmark. Camera jitter does induce failures, and the occlusion trained monitor remains above random. The result is deliberately limited: OpenVLA internal states contain failure relevant structure under controlled perceptual shift, but these experiments do not establish a causal mechanism, task held out generalization, or a deployable recovery system.

---

## 10. Fast Enough to Act: Spatio-Temporal Visual Token Merging for Low-Latency Robotic VLMs and VLAs

**Authors:** Junzhou Chen, Jindong Wang, Gang Zhou
**arXiv:** [2606.29350](https://arxiv.org/abs/2606.29350)
**Categories:** Computer Vision and Pattern Recognition (cs.CV); Artificial Intelligence (cs.AI)

Vision-language models and vision-language action models endow the robot with unprecedented capabilities. However, the input of video and high-resolution images yields a massive number of visual tokens, leading to extremely high inference latency and severely hindering the robot's real-time control. To break through this computational bottleneck, we propose ST-Merge, a plug-and-play, training-free framework that efficiently fuses redundant tokens directly during the visual encoding phase. By explicitly constructing 3D spatiotemporal coordinates, it employs a multi-queue parallel matching and weighted aggregation mechanism to achieve efficient and geometrically consistent fusion of redundant tokens across frames. In addition, we introduce a post-merge positional correction mechanism that effectively eliminates spatial deviation caused by merging by dynamically re-evaluating the rotational position code of the weighted centroid of the vision token, thereby ensuring the high-precision spatial awareness required for dexterous operation. In the Video Question Answering task on the mainstream VLM, Qwen2.5-VL, ST-Merge achieves a 2$\times$ inference speedup with only a tiny 1\% loss in precision. When deployed on the $\pi_{0.5}$ VLA policy, ST-Merge achieves an 8.3$\times$ speedup at 1024 $\times$ 1024 resolution and matches the baseline success rate at this high-resolution setting. At lower resolutions, it introduces a small drop in accuracy.

---

## 11. Flow Matching in Feature Space for Stochastic World Modeling

**Authors:** Francois Porcher, Nicolas Carion, Karteek Alahari, Shizhe Chen
**arXiv:** [2606.29059](https://arxiv.org/abs/2606.29059)
**Categories:** Computer Vision and Pattern Recognition (cs.CV); Artificial Intelligence (cs.AI)

World modeling requires forecasting uncertain futures while preserving information useful for
downstream perception. Existing visual world models often struggle to satisfy both goals:
VAE-based stochastic models operate in low-dimensional reconstruction latents, which can
limit perception performance, while deterministic predictors using strong pretrained features
collapse multimodal futures into a single blurry mean. In this work, we propose FlowWM, a
stochastic world model that performs flow matching directly within pretrained feature space
(e.g., DINOv3). This is challenging because pretrained features are substantially
high-dimensional, making standard diffusion recipes suboptimal. To address this, we
investigate the design choices needed for feature-space flow matching and introduce a
differentiable one-step projection mechanism that enables efficient training with temporal
consistency and task-driven objectives. We evaluate FlowWM on two benchmarks: a synthetic
benchmark for systematic evaluation of accuracy and diversity, and a real-world benchmark
FuturePerception. FlowWM improves perception performance, mode coverage, and horizon
robustness, validating our proposed design for stochastic world modeling in high-dimensional
feature spaces.

---

## 12. X-Mind: Efficient Visual Chain-of-Thought via Predictive World Model for End-to-End Driving

**Authors:** Bohao Zhao, Chengrui Wei, Guangfeng Jiang, ..., Hang Zhang, Xianming Liu
**arXiv:** [2606.28758](https://arxiv.org/abs/2606.28758)
**Categories:** Computer Vision and Pattern Recognition (cs.CV); Artificial Intelligence (cs.AI)

Predicting future states is essential for autonomous agents, yet current Vision-Language-Action (VLA) models fundamentally lack this capability, relying instead on reactive perception-action mapping. While integrating Predictive World Models (PWMs) addresses this gap, existing approaches either incur prohibitive cascaded latency or act as shallow terminal tasks that fail to deeply embed forward-looking reasoning. To endow VLA models with this reasoning capability, we propose X-Mind. Rather than treating PWMs as an external auxiliary module, this framework internalizes them as the Visual Chain-of-Thought (Visual CoT). By enforcing a world rollout prior to action, the model is constrained to imagine future evolution first, yielding a driving policy that is robustly grounded in environmental dynamics and aware of the future consequences its actions will unfold. The challenge here is efficiency, and we tackle it on two fronts. First, we introduce a compact representation of visual thinking: an abstract sketch that fuses a Bird's-Eye-View (BEV) layout with abstract driving priors (e.g., navigation intents and traffic rules). Rather than rolling out dense future frames, the model reasons over this sketch as a mental canvas; aided by a Deep Compression Autoencoder (DC-AE), a 12-frame future rollout is reduced to merely 96 tokens, alleviating the long-context computational bottleneck. Second, to accelerate generation further, we propose a recurrent block diffusion scheme that unrolls the denoising steps across the layers of the large drive model, folding iterative refinement into the backbone's one forward pass. Trained and validated on large-scale real-world data, X-Mind achieves competitive end-to-end driving performance, which makes it a highly practical, low-latency solution that successfully deploys large-scale cognitive reasoning directly onto resource-constrained vehicle platforms.

---

## 13. Event-Conditioned Diagnostics of Kinematic, Contact, and Object-Permanence Fields in Passive Object-State World Models

**Authors:** Yang Liu, Yuming Chen
**arXiv:** [2606.28455](https://arxiv.org/abs/2606.28455)
**Categories:** Robotics (cs.RO); Artificial Intelligence (cs.AI); Machine Learning (cs.LG)

World models can predict future physical states, but prediction accuracy alone does not explain how physical information is organized and used inside their latent dynamics. We introduce a controlled diagnostic protocol for studying event-conditioned latent physical structure in passive object-state world models. The protocol tests whether hidden representations encode event-regime information, whether event contexts reweight non-exclusive physical field readouts, and whether field-aligned representational components have functional consequences for prediction. Using a balanced controlled-generator dataset with free-motion, collision, and occlusion events, we evaluate recurrent, attention-based, and latent state-space transition models under a fixed-horizon forecasting setup. The models learn useful predictive dynamics and their hidden states support reliable event-regime readout. Event contexts systematically reweight kinematic, contact, and object-permanence field readouts: free motion is kinematic-dominant, collision combines kinematic and contact structure, and occlusion combines motion-related and object-permanence structure. Time-aligned and directional-consistency analyses further show phase-related shifts in field emphasis. Finally, fixed-horizon projection causal field effect (CFE) shows that suppressing field-aligned directions can degrade event-relevant prediction, with strongest evidence for contact-aligned structure in collision-contact windows and more qualified evidence for object-permanence-aligned structure in hard-occlusion hidden windows. These results support event-conditioned organization and fixed-horizon functional sensitivity of latent physical fields, while not implying explicit physical modules, isolated causal circuits, or context-invariant sliding-window generalization.

---

## 14. RoboGaze: Evaluating Robot World Models via Structured Vision-Language Analysis

**Authors:** Minh-Loi Nguyen, Nghiem Tuong Diep, Hung Khang Nguyen, ..., Vien Anh Ngo, Tran Van Nhiem
**arXiv:** [2606.28385](https://arxiv.org/abs/2606.28385)
**Categories:** Robotics (cs.RO); Artificial Intelligence (cs.AI)

Recent advances in robot world models enable synthetic video generation for embodied prediction and planning. However, evaluating these videos is challenging: visually realistic outputs often violate physical laws, temporal consistency, or task logic, while conventional metrics and monolithic Vision-Language Model (VLM) judges fail to generalize or provide precise diagnostic value. We present RoboGaze, a training-free, multi-agent VLM framework that provides structured, interpretable evaluation for generated robot-manipulation videos. Given a task instruction and video, RoboGaze operates via a three-stage pipeline: task-scene grounding, dimension-specific specialist routing, and critic-based verification. It outputs temporally localized glitch reports categorized under a novel 6-dimension, 30-type robotics-specific taxonomy. To benchmark RoboGaze, we introduce a human-validated dataset of 382 clips spanning simulated and real-world multi-view manipulation. Evaluating eight open-source and proprietary VLM backbones, RoboGaze dramatically outperforms zero-shot baselines, improving description-F1 by up to +43 points and temporal alignment (F1 x IoU) by up to +37 points, closing approximately 85% of the gap to the human ceiling. Furthermore, its critic verifier mitigates the "cry-wolf" false-positive flaw of standard VLMs, lifting clean-clip accuracy from under 25% to over 80%. RoboGaze offers a scalable, highly interpretable diagnostic tool for the rigorous evaluation of robot world models.

---

## 15. DreamForge-World 0.1 Preview: A Low-Compute Real-Time Controllable World Model

**Authors:** Daniyel Ayupov, Artur Markov-Tsoy
**arXiv:** [2606.30292](https://arxiv.org/abs/2606.30292)
**Categories:** Machine Learning (cs.LG); Computer Vision and Pattern Recognition (cs.CV)

We present DreamForge-World 0.1 Preview, a preview foundational world model for real-time interactive world simulation. The system adapts the LongLive 1 autoregressive video stack, itself derived from Wan2.1-T2V-1.3B, with a residual action pathway inspired by the Matrix-Game family. DreamForge-World 0.1 Preview focuses on a complementary axis to frontier-scale world simulators: low-compute adaptation, consumer-GPU runtime, and broad interactive capability coverage. It supports live keyboard and mouse control, multimodal initialization, mid-stream reprompting, dual-view operation, and minute-scale interactive rollouts at native 480p resolution, reaching up to 14 to 15 FPS FPS on a single RTX 4090 with a low memory footprint. By leveraging open video backbones and applying targeted adaptation runs, we build the preview system with high cost-efficiency. DF-World 0.1 Preview is not yet a memory-complete or frontier-quality world simulator, but demonstrates a practical low-compute route toward real-time controllable world-model previews on consumer GPUs.

---

## 16. Prototype Latent World Model Replay for Class-Incremental Learning

**Authors:** Weizhi Nie, Hui Wang, Weijie Wang, Yuting Su
**arXiv:** [2606.29465](https://arxiv.org/abs/2606.29465)
**Categories:** Machine Learning (cs.LG)

Class-incremental learning requires a model to learn new classes while preserving decision regions for old ones. This is difficult when raw old samples are no longer available. We propose Prototype Latent World Model Replay, a memory-free framework that stores old classes as distributions over stable hidden states rather than as images. A frozen ImageNet-pretrained encoder maps each image into a latent state space. In this space, each class is summarized by several prototype-centered distributions with class-specific variances. When new classes arrive, the model samples old latent states from this prototype world model. It then trains a lightweight adapter and classifier using both sampled old states and real new-class features. We also add a supervised contrastive term in the adapter space to promote intra-class compactness and old-new class separation. On Split CIFAR-100, our method improves over fine-tuning under Inc5, Inc10, and Inc20 without storing raw exemplars. The full Ours-LWM+Con model raises LastAcc from 4.55% to 31.64%, from 9.06% to 37.06%, and from 16.96% to 43.10% in Inc5, Inc10, and Inc20, respectively. It also achieves AvgAcc of 45.86%, 52.19%, and 56.18%. Ablation and retention analyses show that stable latent-state replay is the main source of the gain. Contrastive separation further refines the old-new geometry. These results suggest that prototype latent memory preserves reusable class-state distributions, rather than only fitting the current classifier.

---

## 17. A Path-Space Formulation of Prediction in World Models: From a Single Action to Prediction, Planning, and Irreversibility

**Authors:** Gunn Kim
**arXiv:** [2606.28751](https://arxiv.org/abs/2606.28751)
**Categories:** Machine Learning (cs.LG); Statistical Mechanics (cond-mat.stat-mech)

We propose a path-space formulation of prediction in AI world models. Rather than sequences of one-step conditional distributions, we argue that a world model implicitly defines a probability measure over future trajectories. In the local regime where latent dynamics admit an effective Markovian description, this path measure takes the Onsager-Machlup form. Within this framework, prediction (most probable trajectory), planning (constrained optimization), and uncertainty (fluctuations) emerge as operations on a single action functional. We decompose the latent dynamics into reversible and irreversible components and introduce operational measures of entropy production from model rollouts. In controlled small-scale attention-based models, we find that attention asymmetry is acquired during training in proportion to the irreversibility of the data. Symmetrizing the learned attention suppresses entropy production and selectively degrades long-horizon prediction of irreversible dynamics while preserving relaxational prediction. These results suggest that irreversibility may serve as a computational resource for predictive world models. More generally, the fundamental predictive object is a distribution over future paths rather than states.

---

## 18. J-LAW: Joint Localization and Actionable World Modeling via Coupled Latent Factor Graphs

**Authors:** Guanqun Cao, Liang Chen
**arXiv:** [2606.28712](https://arxiv.org/abs/2606.28712)
**Categories:** Robotics (cs.RO); Machine Learning (cs.LG)

Classical SLAM estimates metric poses and a geometric map but produces no actionable predictive model for planning. Action-conditioned world models learn compact latent dynamics for planning but ignore global metric consistency and accumulate drift under open-loop rollout. We argue these are two views of the same estimation problem and propose J-LAW (Joint Localization and Actionable World Modeling) in this letter: a coupled factor graph that jointly optimizes metric object poses, latent world states, and latent landmark embeddings. The bridge is a pose-conditioned latent encoder and a learned pose--latent coupling factor, so that better localization improves the world model and vice versa. We cast observation, action-conditioned prediction, metric odometry, pose--latent coupling, latent loop closure, and latent landmark observation as probabilistic factors in a single MAP objective. Real-data experiments on PushT and WildGS show that coupled graph correction substantially reduces latent prediction RMSE and endpoint drift relative to open-loop rollout, while latent loop closure improves global trajectory consistency. J-LAW yields a map that is simultaneously metric (poses) and actionable (latent landmarks for planning).

---

## 19. Training Vision-Language-Action Models with Dense Embodied Chain-of-Thought Supervision

**Authors:** Haoyang Li, Guanlin Li, Youhe Feng, ..., Tong Yang, Jing Zhang
**arXiv:** [2606.30552](https://arxiv.org/abs/2606.30552)
**Categories:** Robotics (cs.RO); Computer Vision and Pattern Recognition (cs.CV)

Cross-embodiment transfer in vision-language-action (VLA) models remains challenging because low-level state and action spaces differ fundamentally across robot platforms. We observe that the high-level cognitive process underlying manipulation, including scene perception, object identification, task planning, and sub-task decomposition, is largely shared across embodiments. Based on this observation, we present ZR-0, a 2.6 billion parameter end-to-end VLA model that uses dense Embodied Chain-of-Thought (ECoT) supervision to align cross-embodiment representations within the vision-language model (VLM). ZR-0 adopts a dual-stream architecture: a pre-trained VLM (System 2) generates structured ECoT reasoning during training, while a Diffusion Transformer-based action expert (System 1) produces continuous action chunks via flow matching. The two components are coupled through cross-attention, with an attention mask that restricts the action expert to input prompt features only, enabling ECoT generation to be entirely skipped at inference without any performance loss. ZR-0 is pre-trained on ProcCorpus-60M, a large-scale dataset comprising approximately 60 million frames (approximately 1,000 hours) from over 400K trajectories, with dense ECoT annotations covering 96.8% of all frames. We evaluate ZR-0 on three simulation benchmarks spanning single-arm (LIBERO), bimanual (RoboTwin 2.0), and humanoid (RoboCasa GR-1 Tabletop) embodiments, as well as real-world experiments on the xArm platform, demonstrating strong performance across all settings. Code and model checkpoints are available at this https URL.

---

## 20. Vision-Language-Action Models: Experimental Insights from a Real-World UR5 Platform

**Authors:** Mathilde Hochedel, Marc Lalonde
**arXiv:** [2606.30456](https://arxiv.org/abs/2606.30456)
**Categories:** Robotics (cs.RO); Computer Vision and Pattern Recognition (cs.CV)

This project investigates whether recent Vision-Language-Action (VLA) models can be transferred from controlled research benchmarks to a real-world robotic platform, specifically a UR5e manipulator, in a reproducible and operationally meaningful manner. The work integrates real-robot data acquisition, dataset engineering (compatible with the RLDS format), and the fine-tuning and deployment of OpenVLA and OpenVLA-OFT models, with systematic validation of action representations and control interfaces. The project resulted in several foundational assets: (i) a complete real-robot data acquisition pipeline, (ii) a dataset conversion workflow aligned with RLDS standards, (iii) an initial fine-tuning and inference infrastructure for VLA models, and (iv) a structured set of experimental observations grounded in real-robot trials. These elements collectively establish a reproducible framework for evaluating learning-based manipulation systems beyond simulation. Empirically, the experiments reveal a consistent gap between promising offline indicators and unstable closed-loop behavior on the physical system: this gap cannot be attributed solely to model limitations, it is strongly influenced by action semantics, coordinate frame conventions, temporal alignment between modalities, image preprocessing consistency, and dataset coverage and quality. These observations lead to a key interpretation: the successful deployment of VLA systems in real-world settings depends less on incremental improvements in model capacity and more on precise control of the entire data-model-control pipeline. The project reframes VLA-based robotics from a primarily model-centric challenge to a system-level problem; it highlights the difficulty of running robust task execution on the real robot and provides a clear, experimentally grounded understanding of the conditions required for reliable deployment.

---

## 21. FutureNav: Unified World-Action Modeling for Vision-and-Language Navigation

**Authors:** Lingfeng Zhang, Zeying Gong, Xiaoshuai Hao, ..., Junwei Liang, Wenbo Ding
**arXiv:** [2606.30367](https://arxiv.org/abs/2606.30367)
**Categories:** Robotics (cs.RO)

Vision-and-language navigation (VLN) in continuous environments requires an agent to ground instructions in egocentric observations while maintaining spatial understanding across long action sequences. Recent navigation foundation models have shown strong progress by scaling vision-language models, but they often learn navigation primarily as direct action generation, without explicitly modeling world states or predicting their future evolution. We introduce FutureNav, a VLM-based unified world-action modeling framework for vision-and-language navigation. Specifically, FutureNav jointly encodes text, visual, and spatial features and feeds them into the LLM, and optimizes four objectives for simultaneous world and action modeling: an action policy objective for navigation action prediction, inverse and forward dynamics objectives for modeling state transitions, and a future generation objective for predicting future spatial states. This unified architecture strengthens action prediction while explicitly modeling the world, without sacrificing inference speed. Extensive experiments show that, with only a 4B-scale backbone, FutureNav achieves state-of-the-art performance on multiple VLN benchmarks and substantially outperforms prior VLN methods, paving the way toward future world-action models for VLN. We will release the code and models to support future research.

---

## 22. Learning Transferable Dynamics Priors from Action to World Modeling

**Authors:** Ze Huang, Jiahui Zhang, Hairuo Liu, ..., Ran Cheng, Li Zhang
**arXiv:** [2606.29501](https://arxiv.org/abs/2606.29501)
**Categories:** Robotics (cs.RO)

We study action-conditioned world modeling as a scalable way to learn transferable dynamics priors for robot learning. By pretraining a model to predict how actions drive visual scene evolution, the resulting world model captures reusable interaction dynamics beyond appearance-level video generation. Concretely, we pretrain a multi-view interactive base diffusion world model, A2World, on large-scale robot manipulation data with real action annotations. We validate the learned dynamics priors from two complementary perspectives. First, we adapt A2World into a task- or scene-specialized real-world simulator, A2World-sim, whose long-horizon rollouts support simulator-based policy evaluation and scalable what-if analysis by replacing real-robot rollouts with world model rollouts. Second, starting from the same pretrained weights, we adapt A2World into a video-action joint prediction model, A2World-policy, that predicts actions under visual and instruction conditioning. Experiments across simulation benchmarks and real-robot settings demonstrate that action-conditioned world model pretraining yields transferable dynamics priors that benefit both simulator-centric and policy-centric robot learning.

---

## 23. TAP-VLA: Tactile Annotation Prompting for Vision Language Action Models

**Authors:** Mark Van der Merwe, Mohamad Louai Shehab, Jayjun Lee, ..., Dmitry Berenson, Nima Fazeli
**arXiv:** [2606.29089](https://arxiv.org/abs/2606.29089)
**Categories:** Robotics (cs.RO)

Vision-Language-Action (VLA) models demonstrate impressive reasoning over visual, semantic, and spatial task variations by leveraging large-scale vision and language pre-training. They remain, however, largely blind to contact forces, which seldom manifest clearly in visual feedback but are central to contact-rich manipulation. Tactile sensing measures these forces directly, but integrating it into VLAs is difficult: tactile data is absent from the large-scale corpora used to pre-train VLAs, so adding it as a new input modality induces a distribution shift that erodes the very pre-training that makes VLAs effective. We propose Tactile Annotation Prompting for Vision-Language-Action models (TAP-VLA), a simple framework that supplies tactile feedback through visual augmentation rather than architectural change. TAP-VLA extracts shear fields from visuo-tactile sensors and overlays them as spatially-grounded vectors onto the multi-view RGB images the policy already consumes, yielding a clear, interpretable tactile cue in the VLA's native observation space. Because the architecture is untouched, the approach requires no tactile pre-training, adds negligible compute, and stays close to the pre-training distribution. Across four contact-rich tasks, TAP-VLA succeeds on 78% of trials, compared to under 50% for vision-only fine-tuning and alternative tactile-fusion baselines -- including tasks where the baselines perform no better than chance.

---

## 24. Event-VLA: Action-Conditioned Event Fusion for Robust Vision-Language-Action Model

**Authors:** Jiaxin Liu, Xun Xu, Zhenhao Zhang, ..., Weiyu Guo, Laurent Kneip
**arXiv:** [2606.29384](https://arxiv.org/abs/2606.29384)
**Categories:** Computer Vision and Pattern Recognition (cs.CV); Robotics (cs.RO)

Vision-Language-Action (VLA) models have become an important paradigm of embodied AI. However, existing VLA models typically assume well-lit and stable indoor settings, while real-world embodied manipulation may involve degraded RGB observations caused by illumination shifts, posing critical challenges for robust robotic manipulation. To address this gap, we propose \textbf{Event-VLA}, an event-enhanced VLA framework for generalizable manipulation across varying illumination conditions. We formulate VLA-based manipulation under degraded visibility as a practical robustness problem for RGB-centric policies, and introduce event streams as an illumination-robust, motion-sensitive complementary observation to improve robustness across visibility levels. Specifically, unlike conventional multimodal fusion that directly merges event features into the global semantic token space, Event-VLA injects event information through an action-query routing pathway. It uses learnable action queries to extract task-relevant semantics from the VLA reasoning process, and selectively aggregates event tokens via gated cross-attention to construct event-aware action representations. This design preserves the pretrained RGB-language semantic priors while effectively leveraging event information for robust action prediction. Experiments in simulation and real-world deployment show that Event-VLA maintains strong manipulation performance under normal lighting and improves success rates under low-light degradation and near-dark real-world settings.

---

## 25. ViPSim: Collaborating Visual and Parameter Spaces for Consistent Long-Horizon Embodied World Models

**Authors:** Longyu Chen, Heng Li, Wei Yang, Manqi Zhao, Dongsheng Jiang
**arXiv:** [2606.28804](https://arxiv.org/abs/2606.28804)
**Categories:** Computer Vision and Pattern Recognition (cs.CV); Robotics (cs.RO)

Embodied World Models (EWMs) have emerged as a scalable and risk-free paradigm for advancing embodied intelligence, enabling the safety-critical evaluation of Vision-Language-Action systems. However, their reliability as evaluation benchmarks and foundational simulators is often hindered by the representation gap between low-dimensional actions and high-dimensional video synthesis. This gap results in a lack of geometric correspondence, manifesting as accumulated trajectory drift and inconsistent robot-object interactions during long-horizon rollouts. To bridge this gap, we propose ViPSim, a framework that achieves consistent long-horizon generation through the synergistic collaboration of Visual and Parameter Spaces. We define the Visual Space as a domain of explicit spatial priors, integrating pixel-aligned projections of end-effector pose, camera perspectives, depth-informed scene geometry, and robotic morphological masks to provide dense structural grounding. Concurrently, the Parameter Space serves as a domain of numerical drivers, injecting raw action sequences and camera matrices to provide precise motion guidance. By unifying these two spaces, ViPSim ensures that the generated states are simultaneously anchored by geometric boundaries and steered by numerical commands. Extensive experiments demonstrate that ViPSim is backbone-agnostic and significantly enhances trajectory consistency. Notably, our approach exhibits emergent capabilities in generating complex interactions with deformable objects (e.g., cloth folding) and maintains robust performance in out-of-distribution and cross-embodiment scenarios, providing a high-fidelity foundation for the automated evaluation and predictive control of embodied agents.

---

## 26. A Physics-Grounded Benchmark for Multi-Agent Dynamics in World Models

**Authors:** Nuo Chen, Lulin Liu, Zihao Li, ..., Yang Zhou, Zhiwen Fan
**arXiv:** [2606.28757](https://arxiv.org/abs/2606.28757)
**Categories:** Computer Vision and Pattern Recognition (cs.CV); Robotics (cs.RO)

Generative world models hold immense promise as scalable simulators for autonomous systems, particularly for synthesizing rare but safety-critical multi-agent interactions, such as vehicle collisions. However, current evaluation paradigms index heavily on visual fidelity and semantic alignment, leaving a critical blind spot: they cannot reliably quantify whether generated dynamics actually obey the fundamental physical laws required for reliable simulation. Assessing this physical plausibility is inherently difficult due to a lack of physical metrics and the challenge of extracting metric-scale kinematics from uncalibrated video rollouts. To bridge this gap, we introduce CrashTwin, a physics-grounded evaluation framework designed to stress-test the physical trustworthiness of world models. CrashTwin couples a diverse dataset of multi-agent collision scenarios, comprising 25K controllable synthetic and 12K in-the-wild real-world collision sequences with a novel calibration-free reconstruction pipeline, enabling the recovery of 3D physical attributes directly from world model rollouts. We propose a diagnostic suite that systematically evaluates three dimensions: spatio-temporal consistency, momentum and kinetic energy conservation, and world-dynamics integrity. Extensive benchmarking of state-of-the-art models reveals a crucial insight: high perceptual quality frequently masks severe physical violations during complex interactions. By quantitatively exposing these failure modes, CrashTwin provides a vital diagnostic tool for developing physically grounded world models capable of reliable real-world simulation.

---

## 27. OWMDrive: Causality-Aware End-to-End Autonomous Driving via 4D Occupancy World Model

**Authors:** Junjie Cheng, Ruiqi Song, Ye Wu, ..., Ximiao Li, Yunfeng Ai
**arXiv:** [2606.30421](https://arxiv.org/abs/2606.30421)
**Categories:** Computer Vision and Pattern Recognition (cs.CV)

Autonomous driving systems are steadily moving toward end-to-end paradigms to mitigate the limited adaptability of rule-based pipelines in complex traffic environments. However, most existing learning-based methods still make decisions from static representations of the current scene, without explicit future rollouts or modeling of the temporal causal dynamics in traffic interactions. This limitation often results in unstable or overly conservative planning under high-uncertainty conditions, such as occlusions and unexpected events. To overcome these challenges, we introduce OWMDrive, a generative end-to-end driving framework built upon an Occupancy World Model for multi-step 3D occupancy forecasting, which serves as a conditional prior to guide diffusion-based planning. Conditioned on both current observations and predicted future states, the planner iteratively refines trajectory candidates to generate a reinforced driving trajectory. By explicitly modeling scene evolution over future horizons, OWMDrive captures key spatiotemporal causal dependencies, which leads to more foresighted and robust trajectory generation. Extensive experiments demonstrate that OWMDrive significantly improves planning reliability and safety, especially in challenging and partially observable driving scenarios.

---

## 28. Behavior Uncloning: Distilling Mode Redirection into Policy Weights without Inference-Time Steering

**Authors:** Hao Wang, Jiuzhou Lei, Dayou Li, ..., Ruohan Zhang, Zhiwen Fan
**arXiv:** [2606.29201](https://arxiv.org/abs/2606.29201)
**Categories:** Robotics (cs.RO); Artificial Intelligence (cs.AI)

Behavior-cloned policies often learn multiple behavior modes from demonstration datasets, including modes that are unsafe or otherwise undesired at deployment. For example, a policy trained on diverse handover demonstrations may learn to pass a knife blade-first. Standard remedies such as data curation and inference-time steering either require access to the original demonstrations for full retraining or add substantial inference-time overhead. To address this gap, we propose MoRE(Mode Redirection), which redirects policy rollouts toward desired behavior modes through a short "uncloning" step. Specifically, MoRE distills the redirection signal from a temporary mode classifier into the policy weights to steer behavior. A retain loss balances this edit by preserving desired-mode competence, allowing the standalone policy to suppress unwanted modes with zero inference-time overhead. Across eight simulated and real-world tasks, MoRE improves the average deployment success rate (SR) by 44 percentage points over the original mixed-mode policy. Among all compared adaptation and steering baselines, MoRE achieves the strongest SR and approaches the filtered-data retraining reference, while preserving task competence and inference speed. MoRE also generalizes across robot policy backbones, including Diffusion Policy and the Pi0.5 VLA, diverse task categories, and real-world deployments.

---

## 29. Zero-Label Driving Scenario Complexity Detection via Joint Embedding Predictive Architecture

**Authors:** Santosh Jaiswal
**arXiv:** [2606.28383](https://arxiv.org/abs/2606.28383)
**Categories:** Computer Vision and Pattern Recognition (cs.CV); Machine Learning (cs.LG)

Identifying complex and safety-critical driving scenarios in large unlabelled datasets is an important but expensive problem. Existing approaches rely on human annotators, supervised classifiers, or carefully engineered rule sets, all of which require substantial prior knowledge about what constitutes a difficult scenario. We ask whether a model can discover scenario complexity on its own, with no labels at any stage. We train a minimal Joint Embedding Predictive Architecture (JEPA) on structured agent state data from the nuPlan mini dataset and use the temporal prediction error as a zero-shot complexity score. Without access to any ground-truth labels during training or evaluation setup, the model assigns significantly higher scores to scenarios involving unprotected turns, crosswalk interactions, and pedestrian proximity, and significantly lower scores to lane-following and stationary-traffic scenarios. We validate this finding through four ablation experiments that isolate the source of the signal, and through a downstream anomaly detection evaluation that achieves Average Precision of 0.512 against a 0.436 chance baseline. The results show that temporal prediction error in a self-supervised latent world model is a practical proxy for driving scenario complexity.

---

## 30. Sequential Planning via Anchored Robotic Keypoints

**Authors:** Bryce Grant, Aryeh Rothenberg, Logan Senning, ..., Zach Patterson, Peng Wang
**arXiv:** [2606.30613](https://arxiv.org/abs/2606.30613)
**Categories:** Robotics (cs.RO)

We present Sequential Planning via Anchored Robotic Keypoints, SPARK, a training-free neurosymbolic manipulation system that reaches 43.7% on six LIBERO-PRO position \& task cells, more than doubling CaP-Agent0 and Vision-Language-Action (VLA) baselines. CaP-Agent0, a multi-turn code-generation agent, achieves 18.2% by re-querying an LLM at every turn, but its restart-from-scratch solution proves costly against minor policy failures. Perception is the layer that fails most under position and task changes so SPARK spends its computation there. A single Gemini call composes the plan as a typed behavior tree (BT) of composable primitives, each already containing the low-level control (motion, grasping, depth geometry) a code-generation agent would otherwise regenerate on every trial. The rest of the budget goes to perception: a second Gemini call proposes three alternative text prompts per object, SAM3 evaluates each, and we keep the prompt$\to$label pair with the most confident detection and a recovery loop then retries a failed primitive against freshly detected objects, with no new LLM call. The alternative prompts add +27.7 points on the spatial suite and +10.0 on the object suite, with the recovery loop adding +5.0 overall. SPARK runs the same primitives on three robot families (UR10e, Franka FR3, bimanual Franka) across nine unique tasks at twenty trials each, averaging 68%. Since the detector, planner, and controller modules sit behind the typed plan, they swap independently without training, and each primitive's checkable post-condition traces a failure to the corresponding module or a kinematic limit. Every trial logs a verified, labeled trajectory, so a training-free planner that already beats VLAs can supply the data those policies need without teleoperation. Project page: this https URL

---

## 31. Chronos: A Physics-Informed Full-History Framework for Non-Markovian Long-Horizon Manipulation

**Authors:** Yulin Zhou, Yimeng Wang, Nengyu Wang, ..., Xiangrui Zeng, Zhouping Yin
**arXiv:** [2606.30318](https://arxiv.org/abs/2606.30318)
**Categories:** Robotics (cs.RO)

General-purpose robot policies should be modeled as dynamical systems, yet many VLA and generative imitation policies still rely on present observations or short windows. This Markovian shortcut fails in memory-dependent manipulation: identical observations can demand different actions after different histories. We present Chronos, a physics-informed full-history framework for non-Markovian long-horizon manipulation. The key idea is to elevate observation history from auxiliary context to the latent state of the policy dynamics. At each physical control step, Chronos forms one state-representative token by fusing observation and proprioception, so the token sequence is aligned one-to-one with physical time. A selective state space model propagates this causal historical state, which conditions a multimodal coarse action prior through implicit maximum likelihood estimation (IMLE). This prior is then refined by a second-order Schrodinger-inspired bridge that predicts acceleration fields, yielding smoother and more physically grounded robot motion. Across 16 simulated tasks and 4 real-world experiments, Chronos is evaluated on precision insertion, general manipulation, and memory-dependent long-horizon control. On RMBench, where success requires remembering task phase, Chronos achieves 73.6% average success, outperforming Markovian VLA baseline pi0.5 by +62.4 percentage points, a 6.6x relative gain, while using 10x fewer parameters. It also surpasses the memory VLA Mem-0 by 22.8 points while using over 30x fewer parameters. In real-world dual-arm experiments using a single RGB camera, Chronos achieves 78% average success over four tasks, including 72% on the three memory-dependent tasks, whereas pi0.5 achieves 7% overall and 0% on the memory-dependent subset. These results suggest that history should not be treated as auxiliary context, but as the latent state of the manipulation policy.

---

## 32. OpenSPM: An Environment-Transferable Robotic Key Spatial Pose Memory and Closed-Loop High-Frequency Flow-Matching Action Generation Model

**Authors:** Iok Tong Lei, Qingchen Xie, Yifan Wang, Yap Ying Jie, Zhidong Deng
**arXiv:** [2606.29936](https://arxiv.org/abs/2606.29936)
**Categories:** Robotics (cs.RO)

Open-environment tabletop robotic manipulation requires systems to possess semantic understanding, precise geometric pose estimation, and high-frequency action generation. While end-to-end vision-language-action (VLA) models excel at semantic generalization, they often lack explicit geometric constraints for fine-grained tasks and require costly training. To bridge the gap between high-level semantics and low-level physical execution, we propose OpenSPM, an open environment spatial persistent memory framework consisting of spatial pose memory and flow-matching action generation model. OpenSPM first leverages semantically conditioned 3D perception and Kalman filtering to track continuous 6D poses. It then extracts key spatial poses from human demonstrations, keeping them as transferable, object-centric spatial persistent memory entries. During inference, OpenSPM retrieves relevant memory entries in terms of natural language instructions, transfers the spatial poses to new scenes using SE(3) transformations, and generates high-frequency action chunks via a lightweight conditional flow-matching model. Combined with real-time proprioceptive state feedback and terminal residual correction, the system effectively suppresses trajectory error accumulation. Evaluated on ten LIBERO-GOAL tasks, OpenSPM achieves an 85.6% success rate and an equivalent control frequency of 1033.3 Hz, while requiring minimal inference AI computing power. Extensive ablations illustrate that structured spatial persistent memory and closed-loop residual correction play a crucial role in reliable, high-frequency robotic manipulation.

---
