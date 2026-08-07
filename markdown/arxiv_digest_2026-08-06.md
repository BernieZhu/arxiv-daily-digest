# arXiv Daily Digest — 2026-08-06

**Mode:** direct
**Categories:** cs.AI, cs.LG, cs.RO, cs.CV
**Keywords:** VLA, world model, world action model
**Papers found:** 15

---

## 1. WorldCycle: Self-Verifiable Reinforcement Learning for Long-Horizon Video World Models

**Authors:** Bohai Gu, Yueyang Yuan, Taiyi Wu, ..., Alan Zhao, Song Guo
**arXiv:** [2608.04964](https://arxiv.org/abs/2608.04964)
**Categories:** Artificial Intelligence (cs.AI); Machine Learning (cs.LG)

Interactive video world models are essential for long-horizon planning and exploration, yet they suffer from compounding errors. Post-training methods such as reinforcement learning (RL) can improve these models, but they hit a verification bottleneck: for arbitrary action sequences, no ground-truth future state exists to measure long-term drift. Our key insight is that reversible action cycles make this verification possible: a sequence composed with its inverse must analytically return to the initial state, yielding annotation-free supervision on long-horizon correctness. Building on this, we introduce WorldCycle, a self-verifiable RL framework that constructs closed action cycles and their repeated executions from ordinary action sequences, and optimizes two complementary rewards: a spatial closure reward enforcing symmetry between mirrored forward and reverse segments, and a temporal consistency reward aligning states across repeated cycle executions. These rewards force the model to learn actions as consistent state operators rather than memorized temporal patterns, and extend naturally to out-of-distribution composite action cycles that the base model handles poorly. We further release CycleBench, a diagnostic benchmark for state-returning ability under complex action structures. WorldCycle reduces state returning drift by up to 44% and lifts composite-action accuracy nearly 4x over the base model, providing a vital foundation for physically grounded world models.

---

## 2. Explicit Language Memory for Long-Horizon Planning in Vision-Language-Action Models

**Authors:** Houze Xu, Jizhong Li, Ziyi Ye
**arXiv:** [2608.04765](https://arxiv.org/abs/2608.04765)
**Categories:** Robotics (cs.RO); Artificial Intelligence (cs.AI); Computer Vision and Pattern Recognition (cs.CV)

Vision-language-action (VLA) models provide a unified paradigm for connecting visual perception, language understanding, and robotic control. However, existing VLA models still face major challenges in long-horizon tasks: sparse expert demonstrations constrain cross-task compositional generalization; the non-Markovian nature of long-horizon tasks makes it difficult for policies conditioned only on current observations to maintain temporal consistency; limited closed-loop error correction allows execution errors to accumulate; and end-to-end action fine-tuning may weaken the high-level semantic representations of vision-language model (VLM) backbones. To address these issues, we propose a hierarchical long-horizon VLA architecture with an explicit language-memory module. The central idea is to convert discrete temporal observations into a coherent textual memory sequence with temporal logic. The system is decoupled into a high-level VLM and a low-level VLA: the high-level VLM performs semantic reasoning through a visual question answering training paradigm, while the low-level VLA executes precise continuous control conditioned on subtask instructions and visual observations. The high-level VLM recursively updates both language memory and subtask instructions using the previous memory as a contextual anchor, enabling persistent temporal tracking and dynamic correction during long-horizon execution. We evaluate the proposed method in multiple simulation environments and conduct sim-to-real experiments on a real robotic platform. The results demonstrate that explicit language memory improves the success rate and robustness of VLA models on complex long-horizon tasks while providing an interpretable semantic account of the decision process.

---

## 3. GUARD: Grounding Uncertainty and Ablation-Based Risk Detection for Diffusion-Based VLAs

**Authors:** Suhas Hegde, Jitendra Yasaswi Bharadwaj Katta
**arXiv:** [2608.04510](https://arxiv.org/abs/2608.04510)
**Categories:** Robotics (cs.RO); Artificial Intelligence (cs.AI)

Diffusion-based vision-language-action (VLA) policies can generate plausible actions even when their predictions are weakly grounded in the visual and language evidence defining the task. We introduce GUARD, a test-time failure detection method that measures this grounding without modifying the pretrained policy. GUARD estimates the influence of token-indexed entries in the final vision-language model key-value (KV) cache, constructs counterfactual caches by ablating salient KV entries, and compares their denoising responses with the original conditioning. Based on the comparison, we derive GUARD diagnostic stream including sensitivity, attention entropy, modality bias, and grounding efficiency, which are calibrated online and processed by a lightweight temporal classifier. We evaluate GUARD under task-held-out splits across five policy-benchmark settings, using Pi0, SmolVLA, and Alpamayo-1.5 on LIBERO, SimplerEnv, MetaWorld, and PhysicalAI-AV. GUARD achieves the best ROC-AUC on four of five unseen-task settings and ranks second on the remaining setting, improving the average unseen-task ROC-AUC by 5.73 percentage points over the strongest competing runtime monitor while remaining within 0.19 points of the best seen-task average. These results show that directly probing action-head dependence on multimodal evidence provides a transferable failure signal across policies, tasks, embodiments, and domains.

---

## 4. Suppression Sticks, Locality Is Fragile: A Closed-Loop Target-and-Control Audit of Task-Vector Negation in VLA Policies

**Authors:** Shaoguang Wang, Weiyu Guo, Rushi Dai, ..., Yandong Guo, Hui Xiong
**arXiv:** [2608.04692](https://arxiv.org/abs/2608.04692)
**Categories:** Robotics (cs.RO); Machine Learning (cs.LG)

Task-vector arithmetic offers a closed-form way to modify a model, yet its behavioral locality remains unclear in closed-loop robot control. We present a target-and-control audit of per-skill task-vector subtraction from multitask vision-language-action (VLA) policies. Across all ten LIBERO-Goal skills, subtraction produces three qualitatively different regimes: target-control separation for five skills, resistance for three, and global collapse for two. On held-out initial states, the five suppressible targets remain at 0% success; however, mean baseline-normalized control retention is only 52%, and each target-suppressing edit materially harms at least one nominally unrelated control. Additional Goal panels show separation across tested policies with continuous-regression, discrete-token, and flow-matching action heads, whereas we observe no clean separation on Spatial and control collapse on the tested Object and Long-horizon panels. Mean task-vector cosine does not account for this variation. A matched-norm control identifies a local sign asymmetry around one Goal anchor, while multi-vector outcomes vary with anchor and scale. Retain-aware gradient baselines provide data-dependent comparators but require removal-time data and optimization; subtraction is data- and gradient-free only at edit time, assuming precomputed expert deltas. Finally, a single-skill relearning probe is consistent with behavioral masking, not certified unlearning. These results characterize task-vector subtraction as a fast but brittle intervention and underscore the need for closed-loop target-and-control evaluation when assessing locality in embodied model editing.

---

## 5. Deltoris: Enabling Real-time VLA Inference in Embodied AI via Bit-level Sparsity and Speculative Inference

**Authors:** Zheng Liu, Zeyu Guo, Zihan Liu, ..., Yiming Gan, Yu Feng
**arXiv:** [2608.04428](https://arxiv.org/abs/2608.04428)
**Categories:** Hardware Architecture (cs.AR); Machine Learning (cs.LG)

Vision-language-action (VLA) models have emerged as a key component in embodied AI. Among existing approaches, diffusion-based VLA models achieve superior motion quality and generalization. However, diffusion-based VLA models are compute-intensive and must run at high control frequency, e.g., 50-200 Hz. Thus, it imposes strict latency and energy constraints on edge devices.
In this work, we present Deltoris, an algorithm-hardware co-design framework for efficient diffusion-based VLA inference. First, we exploit the temporal similarity of consecutive inputs and propose a \textit{temporal-aware bit-sparsity} algorithm that computes only the differences between consecutive inputs, eliminating redundant bit-level operations. To further address the extra off-chip traffic introduced by our algorithm, we propose a \textit{speculative inference} technique, which amortizes data loading across multiple control steps. Lastly, to support these techniques, we co-design a dedicated accelerator with customized 1D systolic bit-serial PE arrays that eliminate PE workload imbalance. Our evaluation shows that Deltoris achieves up to 34.2$\times$ speedup over mobile GPUs and 6.1$\times$ over prior accelerators, while maintaining comparable accuracy.

---

## 6. Helping Music Co-Creation Agents 'Listen' Well: Hierarchical Self-Supervised World Models for Understanding and Generation

**Authors:** Scott H. Hawley
**arXiv:** [2608.04378](https://arxiv.org/abs/2608.04378)
**Categories:** Sound (cs.SD); Machine Learning (cs.LG); Audio and Speech Processing (eess.AS)

Collaborative music agents need internal representations rich enough to support both understanding and generation, yet flexible enough for a workflow where the human retains agency. We present a hierarchical self-supervised ``world model'' for symbolic music: a 2.55M-parameter Swin V2 encoder trained on MIDI piano-roll images with JEPA-style objectives (pitch- and time-shift equivariance, masked embedding prediction, and a distributional regularizer), using no labels and no music-theory vocabulary. Probing the frozen embeddings shows that the level at which a musical property becomes decodable tracks its musical time scale: phrase boundaries are read off the coarsest levels, note density and harmonic detail off the finest. Temporal and phrase structure emerge from the self-supervised objectives alone, while harmonic content must be asked for; a small chord-supervision head raises joint chord recovery from .18 to .54, and key detection, which is never supervised, from .16 to .70. Following the Representation AutoEncoder paradigm, a conditional flow-matching model stands in for a trained decoder, flowing in pixel space from PCA-reduced conditioning: it reproduces a target window at pixel F1 $0.996$, and the same per-level conditioning dropout that controls how far variations stray also enables graphical prompting for masked inpainting with no inpainting-specific sampler. The pipeline runs on CPU producing a suggestion in $2.8$ s, or $0.6$ s on Apple MPS, which we demonstrate in a live interactive demo. In concert with an LLM-based brain, these capabilities supply the core of a collaborative music creation agent in service of, rather than in place of, human agency.

---

## 7. BridgeVLA++: A Data-Efficient, Generalizable, and Memory-Augmented Vision-Language-Action Framework for 3D Manipulation

**Authors:** Peiyan Li, Yuze Zhu, Yixiang Chen, ..., Liang Wang, Tieniu Tan
**arXiv:** [2608.05042](https://arxiv.org/abs/2608.05042)
**Categories:** Robotics (cs.RO)

Leveraging pre-trained vision-language models (VLMs) to construct vision-language-action (VLA) models has emerged as a promising paradigm for 3D robot manipulation. However, existing 3D VLA methods remain data-hungry, exhibit limited generalization under distribution shifts, and lack explicit memory of past observations. These limitations hinder their application to data-scarce, open-world, and memory-dependent manipulation scenarios. Our previous work, BridgeVLA, improves data efficiency and generalization by preserving the input--output alignment of a pre-trained VLM during 3D action learning: raw point clouds are projected into multi-view images, and intermediate heatmaps are predicted before generating robot actions. In this work, we develop BridgeVLA++ by equipping BridgeVLA with a unified spatio-temporal memory architecture that models persistent spatial context and temporal interaction history. The resulting memory-augmented framework can reason over observation histories while preserving BridgeVLA's data efficiency and generalization capabilities. Extensive experiments show that our framework achieves strong performance on spatial manipulation tasks while exhibiting robust generalization. BridgeVLA++ further achieves state-of-the-art performance on two challenging memory-dependent manipulation benchmarks without sacrificing the data efficiency and generalization of the original BridgeVLA. In addition, BridgeVLA++ performs effectively in bimanual manipulation settings and is validated on an additional real-world robotic platform, demonstrating its scalability across tasks, environments, and robotic platforms. These results establish BridgeVLA++ as a unified 3D vision-language-action framework that simultaneously supports data-efficient learning, robust generalization, and effective memory-aware robot manipulation. Project website: this https URL.

---

## 8. DreamWAM: Beyond RGB Future Prediction for World Action Models

**Authors:** Shanglin Yuan, Weiheng Zhao, Xin Shi, ..., Wei Sui, Xinggang Wang
**arXiv:** [2608.04996](https://arxiv.org/abs/2608.04996)
**Categories:** Robotics (cs.RO)

World Action Models (WAMs) learn action-relevant representations by predicting how the observed world will evolve. Most existing WAMs define this future in RGB space, where task-relevant state transitions are entangled with nuisance variations in texture, illumination, background, and viewpoint. We argue that WAMs should explicitly predict action-relevant future state rather than relying on RGB prediction alone. We introduce DreamWAM, which reformulates future prediction as structured world modeling beyond RGB, representing future states through complementary views of appearance, motion, geometry, and semantics. During training, DreamWAM combines joint latent denoising of RGB and motion with lightweight gated residual branches for geometry and semantics. Shared attention between VideoDiT and ActionDiT allows the action branch to learn from these future-state predictions, while all beyond-RGB supervision branches are disabled at inference and deployment remains RGB-only. Across both no-rollout and joint video-action inference, DreamWAM consistently improves the matched RGB-only baselines on LIBERO, from 97.30\% to 98.40\% and from 98.00\% to 98.90\%, respectively. The gains become larger under unseen LIBERO-Plus perturbations, from 51.36\% to 63.44\% and from 69.16\% to 75.47\%. The same robustness extends to real-world manipulation, where DreamWAM attains an average success rate of 74.4\% across unseen changes in lighting, background, and object layout, compared with 55.6\% for Fast-WAM-Joint. These results show that robust world-action learning depends not only on predicting the future, but on representing it in a form that matters for action. The code and models are publicly released at this https URL.

---

## 9. Mind-VLA: Instruction-Aware Spatial Representation Alignment for Vision-Language-Action Models

**Authors:** Xingyu Ding, Yuzhong Zhao, Yang Wu, ..., Yifan Zhang, Jian Cheng
**arXiv:** [2608.04633](https://arxiv.org/abs/2608.04633)
**Categories:** Robotics (cs.RO)

Recent Vision-Language-Action (VLA) methods improve generalization by aligning their representations with 3D scene geometry. However, these methods are fundamentally instruction-agnostic: the representations align the entire scene uniformly, neglecting the 3D geometry of the specific target object designated by the language instruction. This causes failures on fine-grained manipulation and target occlusion tasks, where success depends on accurate 3D understanding of the target object rather than the entire scene. To address this, we present Mind-VLA, an instruction-aware spatial representation alignment method for VLA models. Specifically, Mind-VLA first obtains the target object specified by the language instruction, then prepares its target-object tri-view and extracts the corresponding VAE and VGGT features. Finally, the latent representation of the VLA model is aligned with these features to enable instruction-aware 3D understanding. Mind-VLA reaches 93.9% on LIBERO and 4.47 on CALVIN with a compact 345M-parameter backbone. On real-robot tasks with target occlusion, Mind-VLA reaches 54% average success, outperforming the best-performing instruction-agnostic method in real-robot comparison by 32 percentage points. Code will be publicly available.

---

## 10. SAFECAST: Robust Failure Detection for VLA Policies with Contrast-Set Training and Calibration

**Authors:** Harshitha Rajaprakash, Aditeya Prajapati, Rong Xue, Abrar Anwar, Jesse Thomason
**arXiv:** [2608.04246](https://arxiv.org/abs/2608.04246)
**Categories:** Robotics (cs.RO); Computer Vision and Pattern Recognition (cs.CV)

Vision-language-action policies often fail under deployment-time distribution shifts such as clutter, distractor objects, lighting changes, novel objects, altered initial states, and reworded instructions. Hidden-state-based risk probes combined with functional conformal prediction can detect rollout failures, but their reliability depends on calibration data matching deployment conditions. We introduce SAFECAST, which leverages contrast set perturbations to improve hidden-state probe training and calibration for deployment time shift. SAFECAST statistically significantly improves failure detection ROC-AUC scores over a state of the art baseline in both real-world DROID and LIBERO simulation experiments across multiple VLM backbones. We further find that SAFECAST benefits most when both visual and language contrast set perturbations are used to augment data, and that with contrast set perturbations, sim-to-real calibration leads to better probes than using real rollout data only.

---

## 11. Overcoming Statistical Bias in Action-Controllable World Models

**Authors:** Yuhong Shi, Zhenhao Chu, Jie Wei, ..., Jianyi Liu, Jingwen Fu
**arXiv:** [2608.04653](https://arxiv.org/abs/2608.04653)
**Categories:** Computer Vision and Pattern Recognition (cs.CV); Robotics (cs.RO)

Action-conditioned world models aim to predict how visual environments evolve under an agent's actions. Yet future frames are often highly predictable from visual inertia and recurring motion patterns alone. This creates a shortcut: models can fit the data by exploiting statistical biases without making their visible dynamics meaningfully depend on the action. As a result, different actions may produce similar futures, while motion may persist even under zero action. The key question is how to reduce reliance on statistical shortcuts from dominating action-conditioned prediction. We argue that action control requires more than injecting action features; it requires enforcing consistency under counterfactual changes to actions and observations. Based on this insight, we introduce CoCo, a Counterfactual Consistency framework to enhance action controllability through two complementary constraints. Multi-step counterfactual consistency constrains reference, inverse-action, and zero-action rollouts, while action-spatial counterfactual consistency enforces consistent predictions under mirrored scenes and transformed actions. Together, they reduce reliance on statistical shortcuts from substituting for action-dependent dynamics. We further introduce Action Response Consistency (ARC) and Drift Energy (DE) to assess action controllability, together with Mini-SSMB for same-state, multi-action counterfactual evaluation. On Mini-SSMB, our full model achieved ARC_inv of 0.412 and ARC_ref of 0.483, while reducing DE by 17.07% relative to the baseline. On VP2 visual planning, it achieves the highest average success rate among SOTA models, at 73.1%. Experiments on BAIR and RoboNet further show that these gains preserve video prediction quality and transfer across model settings.

---

## 12. HelloWorld: Enabling Socially Interactive Characters in Video World Models

**Authors:** Liangyang Ouyang, Ruicong Liu, Xuangeng Chu, Kaipeng Zhang, Yoichi Sato
**arXiv:** [2608.05070](https://arxiv.org/abs/2608.05070)
**Categories:** Computer Vision and Pattern Recognition (cs.CV)

Despite the remarkable recent progress of video world models, social interaction between users and the characters within these worlds remains unsupported. To fill this gap, we present HelloWorld, a video world model that enables social interaction with in-world characters. With a single button press, users can prompt the on-screen character to respond toward the camera, e.g., turning to the viewer, waving, nodding, or speaking a short greeting. To make these interactions natural, we propose a self-distillation pipeline that finetunes the video generation model on data synthesized by itself. Each synthesized clip contains both social interactions and camera motion, allowing the model to learn camera-pose conditioning without degrading interaction quality. At inference, we further introduce a training-free module that determines when the interaction occurs. Upon a button press, it modulates the cross-attention masks of the DiT so that the interaction-related text prompt attends only to the frames within the press window, temporally localizing the character's response. We further build HelloWorldBench, a 400-sample benchmark with three social interaction metrics alongside three conventional metrics, for evaluation. Experiments demonstrate that HelloWorld surpasses a variety of baselines in interaction quality, while maintaining state-of-the-art picture aesthetics and camera-pose following. Project page: this https URL

---

## 13. MobileWAM: Bridging World Action Models to Mobile Manipulation with Chain-of-Foresight

**Authors:** Zehua Fan, Junjie He, Wenxuan Song, ..., Bailin Li, Yan Wang
**arXiv:** [2608.04657](https://arxiv.org/abs/2608.04657)
**Categories:** Computer Vision and Pattern Recognition (cs.CV)

World action models (WAMs) built on video generation backbones are a rising recipe for robot learning, yet remain confined to tabletop manipulation. Mobile manipulation demands simultaneous locomotion and whole-body manipulation amid scene-scale dynamics, yet is still dominated by dynamics-blind visual encoders with hand-crafted coordination. We bridge this gap with MobileWAM, a mixture-of-transformers architecture that fuses a pretrained video diffusion transformer with a lightweight action expert through layerwise joint attention, translating internet-scale motion priors into whole-body control. To reconcile the heterogeneous dynamics of moving and manipulating, each feed-forward layer of the action expert becomes a three-expert mixture of shared, locomotion, and manipulation experts, softly routed by the motion intent in the action tokens. To densify supervision, we further propose Chain-of-Foresight (CoF): intermediate representations sequentially predict a chain of future latent chunks, each step conditioned on its predecessor. CoF pairs naturally with our decoupled video--action denoising scheme. At deployment, the WAM serves as a pure current-frame encoder; foresight acts only through gradients, so at inference the foresight chain and video generation are discarded, leaving only policy-level cost. MobileWAM surpasses state-of-the-art mobile manipulation policies on ManiSkill-HAB and fine-tunes to a real ARX Lift2 mobile manipulator across diverse tasks with strong generalization. Code will be released soon.

---

## 14. Faster-WAM: Efficient Inference-Time Future Conditioning for Robust World Action Models

**Authors:** Weiheng Zhao, Haoyi Jiang, Xin Shi, ..., Wei Sui, Xinggang Wang
**arXiv:** [2608.04404](https://arxiv.org/abs/2608.04404)
**Categories:** Computer Vision and Pattern Recognition (cs.CV)

World Action Models (WAMs) improve robot manipulation by learning how the environment evolves beyond the current observation. However, existing approaches face a fundamental dilemma: Joint-WAMs preserve future-aware representations during inference but incur prohibitive computation costs, while efficient alternatives remove future modeling at inference time and may lose the robustness benefits of temporal reasoning. In this work, we revisit the role of future representations in WAMs and show that inference-time future conditioning is critical for generalization under distribution shifts. This observation motivates Faster-WAM, an efficient future-conditioning WAM that preserves future representations while avoiding expensive video-action interaction. Faster-WAM introduces a sparse future-conditioning framework that computes future representations once and selectively reuses them throughout action denoising. Specifically, we propose SparseMoT to replace ubiquitous layer-wise fusion with selective video-action interaction at a compact subset of network stages, and Interval KV-Fusion to aggregate multi-depth future representations without increasing attention complexity. Experiments demonstrate that Faster-WAM achieves a substantially better performance-efficiency trade-off than existing WAMs. On the out-of-distribution LIBERO-Plus benchmark, Faster-WAM improves success rate from 49.14% to 73.57% compared with Fast-WAM, while running 2.21$\times$ faster than Joint-WAM. It further achieves state-of-the-art performance on LIBERO and RoboTwin 2.0, while demonstrating strong robustness in real-world manipulation.

---

## 15. CofactVLA: Deconfounding Vision-Language-Action Models via Counterfactual Intervention

**Authors:** Yan Zhang, Yinan Wu, Haoran Duan, Jungong Han
**arXiv:** [2608.04396](https://arxiv.org/abs/2608.04396)
**Categories:** Computer Vision and Pattern Recognition (cs.CV)

Vision-Language-Action (VLA) models have driven significant progress in robotic manipulation, yet they fundamentally struggle with the vision-override phenomenon. Driven by the severe modality imbalance between dense visual streams and sparse linguistic instructions, VLAs frequently fall prey to causal confusion. Instead of treating language as the primary causal driver, the policy entirely bypasses the original instruction by overfitting to spurious visual confounders, such as prominent objects or familiar layouts. To systematically alleviate this bias, we formalize the process of action generation as a Dual-path Deconfounding Graph (DDG) and propose CofactVLA, a novel causal intervention framework. By dynamically constructing a language-masked counterfactual branch within a single forward pass, CofactVLA isolates and neutralizes visual confounders through two synergistic mechanisms. First, Action-Level Orthogonal Projection Guidance (OPG) geometrically projects the factual velocity field away from the counterfactual visual bias during continuous flow matching, extracting the pure semantic intent. Second, Feature-Level Counterfactual Covariance Reduction (CCR) mathematically deconfounds latent representations by penalizing the positive eigenspace of the covariance difference, explicitly suppressing dominant visual shortcuts while preserving the causal language intent. Extensive experiments demonstrate that CofactVLA establishes a new state-of-the-art across diverse simulation benchmarks. Beyond simulation, real-world robot experiments demonstrate the causal efficacy of our method in bridging the generalization gap, yielding a 52.3\% absolute success rate gain under out-of-distribution scenarios.

---
