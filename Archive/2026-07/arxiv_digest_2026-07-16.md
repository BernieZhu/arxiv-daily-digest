# arXiv Daily Digest — 2026-07-16

**Mode:** direct
**Categories:** cs.AI, cs.LG, cs.RO, cs.CV
**Keywords:** VLA, world model, world action model
**Papers found:** 10

---

## 1. Learning Safe Agent Behaviour from Human Preferences and Justifications via World Models

**Authors:** Ilias Kazantzidis, Timothy J. Norman, Yali Du, Christopher T. Freeman
**arXiv:** [2607.13172](https://arxiv.org/abs/2607.13172)
**Categories:** Artificial Intelligence (cs.AI); Machine Learning (cs.LG)

We address the problem of safely training an agent policy and deploying a good and safe policy, in settings where the environment dynamics are unknown and no suitable reward function is available. In the context of safety-critical environments, we consider traditional reinforcement learning impractical and resort to the resource of human input. We introduce DROPJ, a human-centred method for both safe training and deployment. We first learn a world model (a learned simulator) from a dataset of prior real-world trajectories. A human then plays the game in this learned simulator to extract several informative simulated trajectories. From these, we sample pairs of simulated trajectory segments and elicit from a human their preference over these segments, as well as a reason (justification) for their choice. We then train a reward model from these justified preferences and use it, together with the world model, to directly deploy the agent using model predictive control. Running real-user experiments, we find that generating informative simulated trajectories from a user significantly reduces the computational cost during training compared to other strategies, and can also improve the performance during deployment. In the context of training within a learned simulator, we show that the use of preferences rather than other types of feedback substantially improves the performance during deployment. We further demonstrate that safety justifications accompanying preferences can significantly enhance safety or prioritise user-prescribed aspects of safety associated with them during deployment.

---

## 2. The SIGReg Objective as Variational Free Energy: A Theoretical Active-Inference Account of JEPA World Models

**Authors:** Fabio Arnez, Alexandra Gomez-Villa
**arXiv:** [2607.13612](https://arxiv.org/abs/2607.13612)
**Categories:** Machine Learning (cs.LG); Artificial Intelligence (cs.AI)

Joint-Embedding Predictive Architectures (JEPAs) are the dominant design for latent world models, yet they are usually justified by empirical performance rather than a normative principle. We show that the choice of anti-collapse regulariser determines whether a JEPA's training objective, a prediction loss plus a weighted embedding regulariser, is a valid Active Inference (AIF) variational free energy. We organise four non-contrastive regularisers (VICReg, LogDet, PairDist, and SIGReg) into an entropy-estimator hierarchy indexed by a prior-miscalibration gap, and show that the gap's sign, whether the estimator bounds the latent entropy from above or below, decides whether the AIF surprise bound survives: VICReg and LogDet are unsafe upper bounds, PairDist a safe lower bound, and SIGReg eliminates the gap. We then prove a correspondence theorem: under the standard constant-noise encoder model and successful SIGReg enforcement (isotropic-Gaussian embeddings), the gap vanishes, the objective becomes an exact information bottleneck, the surprise bound is preserved, and the latent goal cost becomes an exact proxy for AIF pragmatic value, whereas VICReg leaves an irreducible second-order anisotropy term. We extend the correspondence to multi-step expected free energy, ensemble epistemic value, and a learned-policy regime, and we identify the one AIF term no current JEPA world model computes: the state-epistemic value, a future-state coverage signal. The predictions differ in kind, not degree, and are stated here as theoretical consequences left for empirical test in separate work; full proofs are in Appendix A, and the algebraic core of every result is machine-verified in Lean 4 (Appendix D).

---

## 3. Grounded world models in biological organisms and future embodied AI

**Authors:** Giovanni Pezzulo, Davide Nuzzi, Marco D'Alessandro, ..., Roberto Bottini, Paul Cisek
**arXiv:** [2607.13560](https://arxiv.org/abs/2607.13560)
**Categories:** Neurons and Cognition (q-bio.NC); Artificial Intelligence (cs.AI)

Recent advances in generative and embodied AI have been driven by large-scale predictive learning over multimodal data. However, the resulting systems remain largely based on passive training regimes where linguistic regularities create the scaffold onto which information from other modalities is attached. Conversely, neuroscience and cognitive science suggest that biological intelligence is organized in the opposite way, where grounded world models acquired through interaction with the environment provide the semantic scaffold to which language is attached. Here, we illustrate five examples of neural circuits supporting grounded world modelling, which underlie navigation in physical and conceptual spaces, affordance-based perception and interaction with objects, active perception and exploratory learning, allostatic control and emotion, and the distinction between self- and world-generated outcomes. These examples highlight several features largely missing from current embodied AI, including the role of intrinsic dynamics as a foundation for learning, the centrality of action in aligning these dynamics with the external world, the prominence of autonomous experience and open-ended learning over passive assimilation of externally provided data, and the fact that early predictive and control mechanisms scaffold higher cognitive abilities such as reasoning, conceptual navigation, planning, imagination, understanding others' minds, and communication. Finally, we discuss whether and how principles derived from biological systems may inform future embodied AI, including training regimes based on social interaction to construct world models that are not only grounded but also socially shared and aligned with human norms and values.

---

## 4. S-squared-VLA: Decoupling Semantic and Spatial Streams in Vision-Language-Action Models for Autonomous Driving

**Authors:** Jianguo Yu, Rukang Wang, Duanfeng Chu, ..., Renju Feng, Liping Lu
**arXiv:** [2607.13926](https://arxiv.org/abs/2607.13926)
**Categories:** Robotics (cs.RO)

Vision-Language Models (VLMs) have demonstrated remarkable potential for high-level reasoning in autonomous driving, yet they fundamentally struggle to generate precise, low-level control actions. This limitation is rooted in a semantic-physical gap caused by the inherent mismatch between discrete language tokens and continuous trajectory planning. While Vision-Language-Action (VLA) architectures attempt to bridge this gap by unifying perception and control into a single policy, this entanglement creates a new bottleneck. Standard VLAs experience a severe spatial representation collapse, which irreversibly degrades the fine-grained spatial and geometric priors essential for safe, boundary-aware navigation. To address this limitation, we propose the S-squared-VLA, which explicitly decouples the semantic and spatial streams in Vision-Language-Action models. The semantic stream leverages hierarchical bridging to extract multi-scale VLM features for robust intent reasoning. In parallel, an independent spatial stream bypasses the autoregressive language bottleneck, directly preserving uncompressed spatial features from the visual encoder. By integrating auxiliary perception supervision, this stream explicitly equips the model with rich spatial and geometric priors. Finally, a dual-stream planning adapter fuses high-level semantic intent with precise spatial constraints via cascaded attention mechanisms. Evaluations on the NAVSIM closed-loop benchmark show that S-squared-VLA achieves a Predictive Driver Model Score (PDMS) of 87.1, establishing a new state-of-the-art for VLA models under a purely supervised fine-tuning (SFT) setting. By mitigating the spatial representation collapse of traditional VLMs, our framework significantly outperforms baselines, achieving the highest No Collision (NC) rate of 98.4 among all evaluated methods.

---

## 5. An Empirical Study on Stage-Information Interfaces for VLA Fine-Tuning

**Authors:** Yingwei Ji
**arXiv:** [2607.13605](https://arxiv.org/abs/2607.13605)
**Categories:** Robotics (cs.RO)

One high-level instruction in long-horizon manipulation can cover several action stages. We use segmented action annotations as an intermediate representation between the full-task instruction and VLA action chunks. A progress module tracks the active stage, while the action policy receives stage information either as current-stage text or as a normalized ordinal stage index in robot state. We compare these interfaces with GR00T N1.6 on LIBERO-10 under direct fine-tuning and continuation fine-tuning from a full-task instruction baseline. Under direct fine-tuning, full-task instruction, current-stage text, and Ordinal Stage-State achieve mean success rates of 57.45%, 50.24%, and 54.36%, respectively, showing that explicit stage information does not automatically improve the policy. Under continuation, the corresponding means are 49.07%, 50.00%, and 53.75%, with Ordinal Stage-State exceeding both alternatives in all three paired runs. The observed benefit differs across interface representations and training arrangements.

---

## 6. Generalizable VLA Finetuning via Representation Anchoring and Language-Action Alignment

**Authors:** Dwip Dalal, Shivansh Patel, Chahit Jain, ..., Svetlana Lazebnik, Unnat Jain
**arXiv:** [2607.13429](https://arxiv.org/abs/2607.13429)
**Categories:** Robotics (cs.RO); Computer Vision and Pattern Recognition (cs.CV)

Finetuning a pretrained vision-language model (VLM) on robot demonstrations via behavior cloning (BC) has become the standard recipe for vision-language-action (VLA) policies. However, BC finetuning progressively overwrites the pretrained representations that support visual and semantic generalization. Co-training on web image-text data, a common remedy, does not prevent this; it applies language and action losses to separate observations, leaving VLAs with language-action misalignment that standard manipulation benchmarks do not expose. We propose Anchor-Align, which augments BC with two objectives: Vision-Language Anchoring distills layer-wise representations from a frozen VLM copy to prevent this drift, while Language-Action Alignment converts each action target into a discrete motion-direction label and jointly trains language and action prediction on the same robot observation. On a physical xArm7 robot, across two widely used VLA architectures, Anchor-Align improves real-robot success on both (28% to 54% and 37% to 60%). At scale in simulation, we demonstrate consistent improvements on OOD perturbations, perceptual robustness, and long-horizon control across LIBERO-PRO, LIBERO-Plus, and CALVIN, respectively, suggesting that preserving pretrained representations and effective action learning are not fundamentally at odds. Project page: this http URL

---

## 7. Ego-Dynamics-Augmented World Model for Autonomous Driving with Zero-Shot Cross-Chassis Adaptation

**Authors:** Zhidong Wang, Jingsong Liang, Zirui Li, ..., Han Yu, Chen Lv
**arXiv:** [2607.13410](https://arxiv.org/abs/2607.13410)
**Categories:** Robotics (cs.RO)

World model (WM)-based reinforcement learning enables sample-efficient end-to-end autonomous driving learning by imagining long-horizon trajectories in latent space. However, most driving WMs operate on bird's-eye-view (BEV) representations that are inherently egocentric: the transition between consecutive frames entangles the ego vehicle's own motion with scene dynamics. As a result, the WM devotes significant capacity to recovering ego-motion from warped observations, at the cost of scene modeling fidelity and imagination accuracy. This work proposes DynaDreamer, a dynamics-augmented Dreamer-style reinforcement learning method to address this problem by augmenting the WM with an explicit ego-dynamics prior. A physics-informed ego-dynamics encoder-decoder extracts the ego-state history into a compact and identifiable context, which modulates a causal Transformer WM to condition both its prior and posterior latents. During imagination, the ego-dynamics predictor propagates this context forward to keep the ego-dynamics prior synchronized with the rollout. An information-theoretic analysis shows that conditioning on this context reduces both the predictive entropy of the observation transition and the prior--posterior Kullback--Leibler divergence, confining the WM's modeling burden to the scene dynamics beyond ego-motion. An additional benefit is zero-shot cross-chassis adaptation: the ego-dynamics context depends on identifiable chassis parameters, so that a vehicle with previously unseen dynamic characteristics can adapt the WM to the new chassis without retraining. Experiments demonstrate that DynaDreamer improves task success rates over the strongest baseline by 28% and 61% in urban and highway driving scenarios, respectively, with the advantage rising to 73% when extrapolating to unseen chassis.

---

## 8. M$^\text{4}$World: A Multi-view Multimodal Driving World Model for Interactive Object Manipulation and Minute-long Streaming

**Authors:** Ke Cheng, Hanqiao Ye, Lei Shi, ..., Kaining Huang, Shuhan Shen
**arXiv:** [2607.14005](https://arxiv.org/abs/2607.14005)
**Categories:** Computer Vision and Pattern Recognition (cs.CV); Robotics (cs.RO)

Driving-world generation has emerged as a core capability for scalable autonomous-driving simulation, yet existing methods remain limited in object-level controllability and long-horizon stability. We present M$^\text{4}$World, a Multi-view and Multimodal generative driving world model that synthesizes future surround-view video streams and synchronized LiDAR scans while supporting interactive object Manipulation and stable Minute-long streaming. Fine-grained object manipulation is realized through a flexible conditioning interface that supports explicit control over both the spatial layout and visual appearance of individual objects. Stable minute-long streaming, on the other hand, is achieved through a multi-stage training framework that enables online causal generation in only four denoising steps while maintaining coherent world dynamics throughout extended rollouts. Building on these components, we introduce an efficient few-clip post-training as well as a suite of visual reference-conditioned generation models, preserving general generation ability while allowing rare-case customization for long-tail controllability. To assess controllability beyond realism, we further introduce an automated VLM-based judging pipeline that evaluates scene-level condition adherence, view-wise object controllability, and cross-view object consistency. Comprehensive experiments show that M$^\text{4}$World consistently delivers high generation quality, precise controllability, and stable minute-long streaming. Together with downstream long-tail augmentation and scene editing, these results demonstrate the potential of M$^\text{4}$World for controllable, scalable driving simulation.

---

## 9. From Pixels to States: Rethinking Interactive World Models as Game Engines

**Authors:** Zhen Li, Zian Meng, Shuwei Shi, ..., Chuanhao Li, Kaipeng Zhang
**arXiv:** [2607.14076](https://arxiv.org/abs/2607.14076)
**Categories:** Computer Vision and Pattern Recognition (cs.CV)

Building interactive worlds that respond coherently to player actions has long been a shared goal of computer graphics, games, and artificial intelligence. Recent video generative models provide a data-driven route toward this goal by predicting future observations conditioned on user actions, and are increasingly regarded as potential next-generation game engines. Realizing a genuinely interactive game world, however, requires interaction outcomes that follow rules over evolving game conditions, consequences that persist over long horizons, and a generation loop that operates in real time. Conventional game engines realize these properties through a recurrent action-state-observation loop, in which player actions update an explicit game state according to predefined rules and observations are rendered from the resulting state. Taking this loop as an organizing lens, this paper examines interactive game world modeling along four dimensions: player action control, game state dynamics, state-observation persistence, and real-time interactive generation. For each dimension, we start from the capabilities required by an interactive game world, group existing approaches into representative families, and discuss the strengths and trade-offs of each family. Complementing this analysis, we present a scalable data engine for Black Myth: Wukong that collects over 90 hours of gameplay with frame-aligned player actions, ground-truth game states, and visual observations, together with structured and semantic annotations, as a resource for state-aware game world modeling. We hope this paper offers a clear picture of where the field stands and fosters progress toward interactive game worlds.

---

## 10. From Surface Forecasting to Observability Forecasting: A Latent World Model for Cloud-Aware EO Monitoring

**Authors:** Mohanad Albughdadi
**arXiv:** [2607.13651](https://arxiv.org/abs/2607.13651)
**Categories:** Computer Vision and Pattern Recognition (cs.CV)

The bottleneck of Earth Observation processing chains is not the arrival of new imagery but whether the surface is actually visible when the image arrives. We study this as an observability forecasting problem on EarthNet2021. Given recent multispectral imagery and exogenous weather drivers, the goal is to predict whether the next acquisition will be usable and, if not, when a usable view is likely to return. To do this, we adapt LeWorldModel, a joint-embedding predictive architecture world model, to cloud-aware Earth Observation sequences. The final pipeline converts raw minicubes into episodic HDF5 sequences with five image channels (blue, green, red, near-infrared, cloud mask) and eight meteorological and calendar covariates. The resulting model has 18.0M trainable parameters and is trained from scratch on 23,904 training episodes. The trained leWorldModel is evaluated under a locked protocol: linear probes are fit on train only, calibration choices are set on an internal validation split, and the fitted heads are then frozen for valsplit, IID, OOD, and extreme evaluation. On the full frozen-bundle observability benchmark, LeWorldModel consistently outperforms persistence. For next-step usability, balanced accuracy ranges from 0.769 to 0.887, compared with 0.493 to 0.556 for persistence. For exact first-usable-horizon prediction, accuracy ranges from 0.602 to 0.806, compared with 0.120 to 0.369 for persistence. Against a frozen LightGBM baseline fit on the same training windows, LeWorldModel is better on continuous clear/cloud regression and on exact recovery timing on valsplit, IID, and extreme, while LightGBM is stronger on the simpler binary any-usable-within-six task and is more robust on OOD. In separate sampled diagnostic analyses, LeWM also produces strong ranking-based anomaly signals under synthetic temporal inconsistencies.

---
