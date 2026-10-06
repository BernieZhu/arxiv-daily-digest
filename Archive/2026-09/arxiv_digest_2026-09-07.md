# arXiv Daily Digest — 2026-09-07

**Mode:** direct
**Categories:** cs.AI, cs.LG, cs.RO, cs.CV
**Keywords:** VLA, world model, world action model
**Papers found:** 9

---

## 1. RoboSPA: Can VLA Models Go Beyond Simple Scenes and Short-Horizon Tasks?

**Authors:** Zhenxuan Fan, Bo Zhang, Yutong Lin, ..., Jun Xiao, Yueting Zhuang
**arXiv:** [2609.05324](https://arxiv.org/abs/2609.05324)
**Categories:** Robotics (cs.RO); Artificial Intelligence (cs.AI); Computer Vision and Pattern Recognition (cs.CV)

Vision-Language-Action (VLA) models have shown promising progress in language-conditioned robotic manipulation. However, existing datasets and benchmarks mainly evaluate task completion under predefined settings, offering limited insight into model reasoning under increasing spatial and procedural complexity. We introduce \textbf{RoboSPA} (\textbf{Robo}t \textbf{S}patial-\textbf{P}rocedural \textbf{A}ssessment), a large-scale robotic manipulation dataset and benchmark for diagnosing embodied reasoning in VLA models. \texttt{RoboSPA} focuses on two core dimensions, Fine-Grained Spatial Reasoning and Long-Horizon Procedural Planning, covering 10 task categories and 56 base tasks. Each task is instantiated across five difficulty levels, yielding 280 variants with increasing spatial ambiguity and procedural complexity. We collect 527K trajectories across multiple embodiments and diverse scenes. Beyond binary success rate, \texttt{RoboSPA} introduces diagnostic metrics for more detailed evaluation. Experiments on representative VLA models show that current systems still struggle with complex spatial relations, precise low-level execution, and memory-intensive planning. These results establish \texttt{RoboSPA} as a challenging diagnostic benchmark for developing more capable, reliable, and generalizable embodied agents. Our data and code are available at this https URL.

---

## 2. VLA-Precision: Asymmetric Co-Bootstrapping for Efficient Real-World Online RL of Vision-Language-Action Models

**Authors:** Chenyu Su, Zhaolong Shen, Yuan Qian, ..., Shuang Cong, Weiwei Shang
**arXiv:** [2609.04355](https://arxiv.org/abs/2609.04355)
**Categories:** Robotics (cs.RO); Artificial Intelligence (cs.AI); Human-Computer Interaction (cs.HC); Machine Learning (cs.LG)

Pretrained vision-language-action (VLA) models enable broad manipulation but remain unreliable in tasks demanding precision and repeatability. Applying real-world online reinforcement learning (RL) to VLA post-training enables autonomous trial-and-error improvement beyond demonstrations alone, but exposes two bottlenecks: 1) unreliable value signals can induce policy drift; 2) large-VLA overhead constrains throughput and sample efficiency. To address these challenges, we present VLA-Precision, an efficient real-world online RL framework featuring the Asymmetric Co-Bootstrapping (ACoB) algorithm and the ACoB-Stream architecture. Specifically, ACoB establishes asymmetric co-bootstrapping across timescales: early intervention-guided behavioral learning rapidly improves policy performance while enhancing online experience quality. As autonomous experience accumulates, global return propagation and local preference ranking progressively calibrate value estimates, yielding relative action advantages for reference-regularized policy improvement while suppressing drift. To enable ACoB on large VLAs, we develop ACoB-Stream, a closed-loop experience--policy architecture that establishes invariant-state decoupling and on-demand streaming as design principles, delivering up to 10.9$\times$ improvements in throughput and computational efficiency. Extensive evaluations on nine high-precision chemistry tasks across four categories and four robot embodiments show that VLA-Precision achieves 98.3\% mean success rate in 45.8 min/task, with 27.6 s episodes running at 1.2$\times$ and 1.8$\times$ the speeds of VLA and RL baselines. Resources are available at this https URL.

---

## 3. Spectral-Target Physical Latent Structuring for JEPA-Style World Models

**Authors:** Penghao Zhu, Salvatore Penachio, Kaustav Mukherjee, Aneesh Jonelagadda
**arXiv:** [2609.04264](https://arxiv.org/abs/2609.04264)
**Categories:** Machine Learning (cs.LG)

Latent world models have become increasingly popular as a method to predict and plan in latent space rather than pixel space. Recent architectures, such as LeWorldModel (LeWM), jointly train the encoder and predictor using regularization techniques like SIGReg to prevent representation collapse. Even with such regularization preventing representation collapse, we identify a new world model failure mode of \textit{physical representation laziness}, particularly noted in highly dynamic environments. For these lazy cases, the learned latent states do not collapse but nonetheless fail to represent key physical properties, causing ubiquitous downstream planning failure. To resolve this issue, we propose training-time auxiliary supervision with a lightweight "Fourier auxiliary head", which enforces physically-informed structuring of the latent space with no additional inference-time cost and can be generalized to any environment. Experimentally, we show that the auxiliary head substantially improves planning success rates in dynamic environments where the baseline LeWM exhibits physical representation laziness. It also leads to modest improvements in other environments, even when the baseline does not exhibit physical representation laziness. We further observe superior planning performance being accompanied by higher latent space correlations with key physical properties, indicating both the ability of our method to physically structure latent states and the potential planning-side benefit to the learned representation being physically structured. We also see in low-data regimes, auxiliary supervision is particularly impactful in increasing success rate. These findings support the use of our Fourier auxiliary head method to improve both overall success rate and data efficiency, while avoiding representation laziness in latent world models.

---

## 4. Coupled Control and Wireless World Models for Resilient Remote Robotic Control

**Authors:** H.P. Madushanka, Sumudu Samarakoon, Mehdi Bennis
**arXiv:** [2609.04851](https://arxiv.org/abs/2609.04851)
**Categories:** Robotics (cs.RO); Machine Learning (cs.LG)

Remote robotic systems operating over wireless networks must maintain reliable control despite limited communication resources, changing channel conditions, and environmental this http URL, continuously transmitting high-dimensional sensory observations, such as camera images, increases communication overhead and energy consumption while reducing robustness under unreliable this http URL address these challenges, this paper proposes a resilient communication-aware remote robotic control framework based on coupled control and wireless Joint Embedding Predictive Architecture (JEPA) world models that jointly capture robot dynamics and wireless channel evolution from visual observations and a combination of raw and structured radio frequency (RF) representations based on spectrograms and Persistence Images(PIs).The learned latent representations enable predictive communication scheduling by jointly forecasting future robot states and wireless conditions, thereby reducing unnecessary uplink transmissions while maintaining reliable control this http URL, an adaptive resilience mechanism detects latent prediction discrepancies and efficiently adapts perception embeddings to accommodate wireless and visual environmental changes without retraining the complete control this http URL proposed framework is evaluated in a synchronized Gazebo-Robot Operating System (ROS)-Sionna robot-wireless simulation environment under diverse wireless propagation and perception this http URL results demonstrate significant improvements in communication efficiency, robustness, and resilience while maintaining navigation performance compared with conventional Proportional Integral Derivative (PID), model-free Deep Q-Network (DQN), and predictive approaches based on Vision Transformers(ViTs).

---

## 5. Towards Neuro-Symbolic Procedural Reasoning for Long-Horizon Vision-Language-Action Manipulation

**Authors:** Vivek Chavan, Yahuan Shi, Oliver Heimann, Kevin Haninger, Jörg Krüger
**arXiv:** [2609.05369](https://arxiv.org/abs/2609.05369)
**Categories:** Robotics (cs.RO); Computer Vision and Pattern Recognition (cs.CV)

Vision-language-action (VLA) models can execute short manipulation skills, but remain brittle in long-horizon procedures requiring persistent task state, dependency-aware reasoning, conditional decisions, and reliable grounding. We investigate a neuro-symbolic framework that combines learned VLA control with explicit task graphs and multimodal procedural memory. Task graphs encode action dependencies, valid transitions, and branch conditions, while memory maintains the active step, completed actions, textual context, and task-relevant visual evidence. Together, these structures guide object selection, destination grounding, subgoal dispatch, and verification of expected state transitions. Human demonstrations provide additional spatial and temporal guidance through gaze or saliency cues. To isolate their effect on policy learning, our initial study bypasses cross-view gaze transfer and directly annotates pseudo-gaze in robot-view teleoperation videos. The resulting guidance is used during VLA fine-tuning and inference. We study two long-horizon manipulation domains, workspace clearing and surgical-instrument handling, which require ordered execution, visually grounded decisions, and conditional branching. We evaluate correct-object and destination selection, subtask completion, task progress, step-order consistency, complete-task success, and procedural or execution mistakes. This work positions structured symbolic reasoning and demonstration-derived visual guidance as complementary mechanisms for reliable long-horizon VLA manipulation.

---

## 6. TacPAC: Tactile Prediction and Real-Time Action Correction in World-Action Models for Contact-Rich Manipulation

**Authors:** Zipei Ma, Xiaofei Wei, Junzhe Jiang, Shunlin Lu, Li Zhang
**arXiv:** [2609.05266](https://arxiv.org/abs/2609.05266)
**Categories:** Robotics (cs.RO)

World-action models guide action generation with predicted future observations, but vision-centric predictions miss the local contact cues that decide contact-rich manipulation. However, naively predicting future tactile observations as additional views recovers only a third of the achievable gain in our experiments. This gap reflects a timing mismatch: predictions precede execution, while tactile feedback arrives during it. We introduce TacPAC, which turns tactile prediction into real-time action correction. Once the base model has planned an action chunk, TacPAC caches the predicted contact that plan was conditioned on together with the plan's own representation, and a tactile expert reads each newly observed tactile image against that cache to correct the actions not yet executed. Feedback is thus interpreted against what the plan anticipated rather than in isolation, and one correction is a single pass over that cache, $20.7\times$ cheaper than regenerating the chunk. On five real-robot tasks spanning precision insertion, fragile-object handling, object reorientation, and long-horizon manipulation, TacPAC leads every task and raises the average from 22% for its vision-only base model to 64%. Code is available at this https URL.

---

## 7. Reasoning Without Inference Cost: Latent Semantic Scaffolding for Robot VLA Policies

**Authors:** Andrew Ting Yan Li, Zhuo Li, Zhelin Yang, ..., Quentin Rouxel, Fei Chen
**arXiv:** [2609.04893](https://arxiv.org/abs/2609.04893)
**Categories:** Robotics (cs.RO)

Vision-language-action (VLA) models are trained by imitation and capture what action to take but not why; adding causal reasoning improves manipulation, but current methods pay for it at inference time - generating reasoning tokens or rolling out predicted future states at every step, a cost that compounds over long horizons. We ask whether this benefit can instead be captured during training and discarded before deployment. We introduce Latent Semantic Scaffolding (LSS), an auxiliary loss applied during human-demonstration pretraining that aligns a VLA's action-token representations to text embeddings of physical-reasoning rationales through a small projection head. The head is dropped at inference, leaving the unmodified base policy with zero added cost. Our central finding concerns alignment granularity: aligning each action token to the rationale of its own manipulation phase (Dense LSS) rather than to a single pooled episode-level embedding (Pooled LSS) yields representations that transfer markedly better to held-out tasks. Dense LSS attains both the best in-distribution success and the best transfer to tasks unseen during alignment, whereas pooled alignment over-specializes to the training task. A representational probe shows Dense LSS induces roughly twice the per-phase separability in the backbone, supporting that phase-local alignment is the operative mechanism.

---

## 8. FailureSpot: Label-Efficient Timestamp-Level Failure Detection for Vision-Language-Action Models

**Authors:** Jie Ma, Zongxi Liu, Yi Zhu
**arXiv:** [2609.04277](https://arxiv.org/abs/2609.04277)
**Categories:** Robotics (cs.RO); Computer Vision and Pattern Recognition (cs.CV)

Vision-language-action (VLA) policies have shown strong potential for general-purpose robotic manipulation, but they can still fail unpredictably during long-horizon execution, making reliable failure detection essential for safe deployment. Existing methods either rely on visual models that typically detect failures only after erroneous actions have occurred, or use lightweight proactive detectors trained on VLA internal representations. However, these proactive methods are often supervised with trajectory-level labels, causing normal pre-failure behavior in unsuccessful trajectories to be incorrectly labeled as failure. This supervision mismatch introduces label noise and limits both trajectory-level detection accuracy and precise timestamp-level failure localization. In this work, we study fine-grained timestamp-level VLA failure detection while addressing the cost of dense annotation. We propose a data-efficient framework that first leverages unlabeled VLA action chunks to construct action-derived weak supervision signals, capturing abnormal patterns such as inconsistent consecutive chunks, frozen or idle actions, and aggressive random motions. We then use active learning to select only the most uncertain trajectories for timestamp-level annotation and fine-tune the detector with these informative labels. Experiments across multiple VLA policies show that our method improves both timestamp-level and trajectory-level failure detection performance.

---

## 9. TourPhysics: Bringing Physics to World Models for Exploration and Manipulation from a Single Image

**Authors:** Xin Zhang, Yabo Chen, Zixuan Duan, ..., Feng Xu, Xuelong Li
**arXiv:** [2609.04911](https://arxiv.org/abs/2609.04911)
**Categories:** Computer Vision and Pattern Recognition (cs.CV)

Interactive visual world models must distinguish observation from physical intervention. Camera motion reveals new surfaces, whereas intervention changes object motion, contact, and deformation. Current video world models are largely driven by appearance priors and often lose physical or spatial consistency over long horizons. We present TourPhysics, an online framework initialized from a single image and a declarative physical configuration. TourPhysics extends PhysOmni, our ACM Multimedia 2026 work, from finite physics-grounded video synthesis to persistent exploration and manipulation. TourPhysics combines deterministic simulation with video generation while assigning separate roles to simulator state, geometric evidence, generator controls, and appearance memory. For each action, the simulator computes a finite physical and camera trajectory before the corresponding observation is generated. Accepted observations publish the terminal state and update the appearance memory and subsequent generator controls, while the committed state and simulator geometry remain fixed throughout synthesis and retry. We further separate the simulator geometry used for projection and visibility from the relative depth used to condition the generator. A reference-anchored memory retrieves accepted static appearance through geometric cross-view correspondence and incorporates it through a bounded residual that reverts to the native path when no valid correspondence exists. On simulator-defined camera tours and object manipulations, TourPhysics follows prescribed camera and object trajectories more closely than the evaluated baselines, preserves the input scene, and reduces appearance drift during long-horizon revisits.

---
