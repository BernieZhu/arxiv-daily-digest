# arXiv Daily Digest — 2026-07-28

**Mode:** direct
**Categories:** cs.AI, cs.LG, cs.RO, cs.CV
**Keywords:** VLA, world model, world action model
**Papers found:** 9

---

## 1. A Motion-Aware Vector Quantization Framework with Centroid Reuse for Efficient VLA Inference

**Authors:** Zhuoran Song, Haozhe Jiang, Chunyu Qi, ..., Xiaoyao Liang, Haibing Guan
**arXiv:** [2607.24148](https://arxiv.org/abs/2607.24148)
**Categories:** Artificial Intelligence (cs.AI)

Vision-Language-Action (VLA) models have demonstrated strong potential for embodied AI, yet their high inference latency on GPUs limits real-time deployment. Existing accelerators, such as Dadu-Corki, improve efficiency but treat VLA models as full-precision workloads, leaving substantial redundancy in both memory and computation underexploited.
In this paper, we propose VQVLA, an algorithm-hardware co-design framework that accelerates VLA inference by exploiting weight similarity and execution dynamics. We first introduce MotionVQ, a motion-aware vector quantization scheme that dynamically adjusts quantization precision based on the robot's execution state, reducing memory access while preserving task success rate. We then propose a merged-centroid vectorized GEMM paradigm that operates on the codebook-index representation, eliminating redundant multiplications through spatial aggregation and temporal reuse of centroids. To realize these optimizations, we design an accelerator that efficiently supports dynamic precision selection and centroid-reuse computation. Experimental results show that VQVLA achieves 6.5x, 2.8x, 1.9x, 3.3x, and 4.3x speedup over the A100 GPU, Dadu-Corki, LUT-DLA, CodeGEMM, and ShiftAddLLM, respectively, with negligible accuracy degradation.

---

## 2. Embodied GPT-5.1: Evidence of a World Model?

**Authors:** Roberto Spinelli, Thiago C. Martins
**arXiv:** [2607.23899](https://arxiv.org/abs/2607.23899)
**Categories:** Robotics (cs.RO); Artificial Intelligence (cs.AI)

This exploratory study examines whether a large multimodal language model, GPT-5.1, can serve as the high-level controller of a physical mobile robot despite having no prior embodiment, no training in simulated environments, and no exposure to sensorimotor experience. Using only low-resolution first-person images and a discrete action set, the model was tasked with navigation and object-directed behaviors such as locating and contacting a target toy. Across multiple trials, GPT-5.1 demonstrated emergent capabilities that suggest elements of spatial reasoning and physical understanding. These included maintaining short-term memory of object locations after they left the camera frame, inferring the physical consequences of its own movements, and executing coherent action sequences such as colliding with an object and reversing to visually verify the outcome. At the same time, the model displayed inefficiencies and perceptual limitations, including imprecise alignment strategies and occasional misidentification of distant distractors. Overall, the results indicate that GPT-5.1 exhibits signs of world-model-like behavior in an embodied setting, despite the absence of any embodiment-related training, a finding that challenges long-standing views in cognitive science and robotics which hold that a physical body is a necessary prerequisite for developing such forms of intelligence. The findings motivate deeper investigation into the emergence, limits, and robustness of physical understanding in large language models.

---

## 3. Action from Adjacent Set in Physical Space Outperforms the Best Prediction in World Models

**Authors:** Liangyu Li, Qingwen Liu, Mingqing Liu
**arXiv:** [2607.23602](https://arxiv.org/abs/2607.23602)
**Categories:** Robotics (cs.RO); Artificial Intelligence (cs.AI); Machine Learning (cs.LG)

Controllers based on sampling and latent world models assign a predicted terminal cost to each candidate action sequence, choose the minimum, execute its first action block, and replan. This rule can fail even when the terminal cost perfectly and accurately reflects the true task objective in the physical world. Residual prediction error can give an infeasible sequence an anomalously low cost, and a larger proposal pool gives such errors more chances to outrank feasible alternatives. We call this conditional failure proposal overgeneration. In Cube candidate execution audits, increasing the total proposal budget from 72 to 288 reduces the feasibility of selection by minimum latent cost from .375 to .062 for position targets and from .344 to .031 for targets defined by position and yaw, although every larger pool contains a feasible sequence. We introduce Adjacent Set Action Reconstruction (ASAR). Among proposals with low cost, ASAR measures density from standardized early action prefixes and reconstructs a full sequence from an adjacent set with a light anchor from the sequence with minimum cost. On a Carry and Release evaluation set of 75 queries, Kernel ASAR improves event completion success over matching selection by 28.0, 24.0, and 18.7 percentage points under latent cost and by 18.7, 20.0, and 17.3 points under a trajectory reachability cost at 72, 144, and 288 proposals. Analysis of finite proposal pools characterizes selection risk from the lower tail, separation by a related radius support statistic, and sequence containment under an explicit local feasibility condition.

---

## 4. False Prophets: On the Security of World Models in Agentic Systems

**Authors:** Erik Imgrund, Anna Wimbauer, Klim Kireev, Konrad Rieck
**arXiv:** [2607.23147](https://arxiv.org/abs/2607.23147)
**Categories:** Cryptography and Security (cs.CR); Artificial Intelligence (cs.AI)

Large language models now power autonomous agents capable of complex, multi-step tasks in different environments. Accurate and reliable execution of these tasks requires the agent to predict the results of its actions. Recent research proposes to enhance predictive capabilities via specially trained environment simulators-world models. While world models can improve performance, they can also mislead agents into executing harmful actions, creating significant security and privacy risks. In this paper, we raise security concerns regarding the usage of world models in agentic systems. We discover a range of world model specific vulnerabilities, which can be exploited in terminal-based agents to execute malicious code or extract sensitive data. To facilitate future development, we introduce a security benchmark dataset designed for text-based world models. We argue that some risks are intrinsic to approximate world modeling, and show that attackers can induce mispredictions in agentic pipelines with up to 95% success rate, possibly resulting in unintended command execution, denial of service, drainage of wallet and private information extraction. Finally, we provide practical recommendations for practitioners to mitigate the discovered harms and harden agentic systems.

---

## 5. Real2Sim2Real for Vision-Language-Action Manipulation: An AMD ROCm-Based Pipeline

**Authors:** Qing Yang, Xun Wang, Ziguan Wang, ..., Hongqiang Wang, Dongdong Weng
**arXiv:** [2607.22997](https://arxiv.org/abs/2607.22997)
**Categories:** Robotics (cs.RO); Artificial Intelligence (cs.AI); Graphics (cs.GR); Machine Learning (cs.LG)

Physical AI -- the integration of large vision-language-action (VLA) models with embodied agents that act in the real world -- has emerged as the next major frontier for AI, echoed by industry leaders such as Jensen Huang (``the next big thing is Physical AI, AI with a body,'' GTC Paris, June 2025) and Dr. Lisa Su (`we're entering the world of Physical AI ... this is where AI enters the real world,' CES 2026). This paper presents an end-to-end, fully AMD-accelerated technology stack for embodied manipulation, spanning data-center training silicon, Radeon PRO simulation/rendering GPUs, and Ryzen AI edge compute, unified by the open ROCm software stack. We demonstrate that training and deploying VLA-based manipulation policies does not require a CUDA-locked ecosystem. Four progressive demonstrations are presented: (1) a Sim-to-Real manipulation pipeline trained with SmolVLA and deployed on a physical Franka arm; (2) a semantic, language-grounded object-selection task (`one-of-three'); (3) a Real2Sim synthetic-data generation pipeline that fuses 3D Gaussian Splatting (3DGS) reconstructions of real scenes with the Genesis physics engine; and (4) large-scale reinforcement learning for quadruped and humanoid locomotion benchmarked across multiple hardware platforms. All pipelines run natively on ROCm + PyTorch on RDNA4 (Radeon AI PRO R9700) and RDNA3.5 (Radeon PRO W7900) hardware and are reproducible on the free Radeon Cloud Platform.

---

## 6. τ: Learning Touch-Augmented Vision-Language-Action Models from Future Visual Supervision

**Authors:** Ning Cheng, Jinan Xu, Wanlin Li, ..., Kelan Peng, Wenjuan Han
**arXiv:** [2607.24485](https://arxiv.org/abs/2607.24485)
**Categories:** Robotics (cs.RO)

Learning the informative tactile representation while effectively adapting it to pretrained Vision-Language-Action (VLA) models remains challenging at both the data and modeling levels. At the data level, limited task-specific demonstrations constrain representation quality, whereas large-scale pretraining incurs substantial costs. At the modeling level, existing methods either focus on instantaneous contact states or model temporal interaction dynamics using 6D wrench sequences, leaving high-dimensional tactile signals underexplored. To address these challenges, we present {\tau}, a touch-augmented VLA framework that learns an action-conditioned spatiotemporal tactile representation from future visual supervision inspired by the Joint-Embedding Predictive Architecture (JEPA), and fuses it with vision-language features for action generation under limited data. This supervision operates in latent space and is used only during training, adding no deployment overhead. We also introduce TacAura, a dataset of synchronized vision, proprioception, and vision-based tactile signals across four representative contact-rich manipulation tasks. Experiments show that {\tau} outperforms existing models and generalizes to unseen objects and scenes, delivering improved manipulation performance and robustness

---

## 7. FeelWorld: Visuo-Tactile World Model for Hierarchical Contact Prediction and Planning

**Authors:** Wenxuan Ma, Chaofan Zhang, Chao Xue, ..., Shaowei Cui, Shuo Wang
**arXiv:** [2607.24267](https://arxiv.org/abs/2607.24267)
**Categories:** Robotics (cs.RO)

Humans plan physical interactions by imagining the possible outcomes of candidate actions. However, existing visual world models primarily capture appearance dynamics while overlooking the tactile states that govern contact-rich interactions, potentially producing imagined futures that appear visually plausible but violate physical dynamics. We introduce FeelWorld, a hierarchical visuo-tactile world model that jointly predicts future visual latents and three tactile states. FeelWorld organizes these states hierarchically as contact state, a 3D tactile latent that encodes force-related information, and slip state. These states are jointly predicted by a shared latent dynamics model with explicit supervision. To prevent irrelevant tactile signals during free-space motion from degrading visual prediction, we introduce a contact-gated asymmetric attention mechanism that maintains a visual-only prediction pathway before contact and enables joint visuo-tactile dynamics prediction during contact. The model is further trained with autoregressive rollouts and context noise injection to improve robustness to compounding errors. The predicted contact and slip states also support contact-aware CEM planning. Experiments on chip grasping, fruit grasping, and USB insertion show that FeelWorld reduces 10-step LPIPS from 0.084 to 0.058 and maintains an LPIPS that is 61% lower than that of the visual baseline after an 80-step autoregressive rollout. FeelWorld also achieves an average zero-shot planning success rate of 81.7%, providing an effective approach for incorporating tactile sensing into world models.

---

## 8. $N_0$-TWAM: Scaling Tactile-Native World-Action Model for Contact-Rich Manipulation

**Authors:** NeoteAI Team, Fudan TEAI Team
**arXiv:** [2607.23783](https://arxiv.org/abs/2607.23783)
**Categories:** Robotics (cs.RO)

We present $N_0$-TWAM, a tactile-native world-action model for contact-rich manipulation that predicts both future vision and future contact. To our knowledge, it is the first tactile world-action model trained at large scale, and it shows strong capability on contact-rich tasks. We pre-train $N_0$-TWAM at large scale with visuo-tactile joint training over tactile-rich demonstrations spanning six embodiments and 450 tasks. We use NeoForce, a unified force-based tactile representation, to form a physically grounded contact signal that conditions action generation. To improve long-horizon and multi-stage manipulation, we introduce tactile contact events for task staging and advance through them during execution. For real-time efficiency, we adopt an asymmetric Mixture-of-Transformers architecture that pairs a full-width expert for video prediction with slim experts for downstream action and tactile prediction. Evaluations on both real and simulated benchmarks justify the capabilities of $N_0$-TWAM across a range of contact-rich tasks, and demonstrate the benefit of data scaling for precise tactile and action prediction. In summary, $N_0$-TWAM endows a world-action model with predictive capabilities to foresee vision, touch and action, building a solid foundation for fine-grained manipulation on open contact-rich tasks. The codebase and model checkpoints will be made publicly available to foster further research and development in tactile-enabled robotic manipulation.

---

## 9. Real-Time Human-Centric World Modeling for Upper-Body Human-Object Interaction

**Authors:** Chaonan Ji, Jinwei Qi, Peng Zhang, Bang Zhang
**arXiv:** [2607.23517](https://arxiv.org/abs/2607.23517)
**Categories:** Computer Vision and Pattern Recognition (cs.CV)

We present a real-time human-centric world model for upper-body interactive generation, aiming to synthesize coherent local world dynamics centered on a person, where coordinated body, hand, and facial motions evolve jointly with controllable human-object discrete interaction. To this end, we adopt a continuous-discrete joint control scheme with two complementary components: a continuous human state and a discrete interaction state. For continuous human-state control, we introduce a unified implicit representation based on multi-scale motion encoding, in which motion latents from the upper body, hands, and face are fused into a shared latent space. This multi-scale design improves expressiveness across different spatial scales, captures fine-grained human dynamics more effectively, and enables direct control without explicit retargeting. For discrete object interaction-state control, we represent object contact using a small set of language-encoded discrete interaction states, where text serves as an explicit interaction-state command, such as \emph{no contact} or \emph{grasp}, rather than an open-ended generation prompt, and we further construct a dedicated rendering pipeline for human-object interaction data to supervise such discrete interaction states. By combining continuous implicit human-state control with discrete interaction-state control, our model enables precise modeling of how a person moves and interacts with the local environment, including controllable changes to nearby scene states. Finally, we distill the model for efficient streaming real-time inference, achieving 25 FPS on two H100 GPUs. Experiments demonstrate improved fine-grained motion fidelity, more realistic hand-object coordination, and effective real-time interaction, establishing a practical step beyond motion reproduction toward real-time human-centric world modeling.

---
