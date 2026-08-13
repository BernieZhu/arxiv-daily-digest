# arXiv Daily Digest — 2026-08-12

**Mode:** direct
**Categories:** cs.AI, cs.LG, cs.RO, cs.CV
**Keywords:** VLA, world model, world action model
**Papers found:** 14

---

## 1. XCoT-VLA: Executable Chain-of-Thought for Vision-Language-Action Driving

**Authors:** Foundation Model Team, XPeng Inc
**arXiv:** [2608.10976](https://arxiv.org/abs/2608.10976)
**Categories:** Artificial Intelligence (cs.AI)

Vision-Language-Action (VLA) models can connect scene understanding, semantic reasoning, and trajectory generation for autonomous driving. However, verbose natural-language Chain-of-Thought (CoT) is poorly suited to real-time control because it is open-ended, costly to decode, and difficult to optimize as an action-facing representation. We propose XCoT-VLA, which replaces descriptive rationales with compact executable CoT tokens learned from automatically constructed Reason-Action supervision. Logged trajectories provide action evidence, while scene context supplies causal semantics. The predicted XCoT sequence remains in context and conditions fixed trajectory queries through shared multimodal self-attention. Deterministic token-function routing applies the Reason FFN to XCoT tokens and the Control FFN to trajectory queries for flow-matching trajectory generation. We further introduce XCoT Policy Optimization (XCPO) as an optional refinement extension in the same executable token space. XCoT-VLA reduces longitudinal ADE from 1.645 to 1.323 on a general-distribution set and lateral FDE from 1.616 to 0.648 in lane-change scenarios. By representing driving-oriented reasoning with only 2-6 executable XCoT tokens, our method substantially reduces autoregressive reasoning overhead and remains within the real-time planning budget. These results demonstrate that driving-oriented reasoning can be compact, executable, and directly connected to trajectory generation.

---

## 2. Hidden in Plain Sight: Diffusion-Based Unrestricted Robotic Attacks on Vision-Language-Action Models

**Authors:** Jiahui Han, Yuhui Yao, Xin Wang, ..., Guanchu Wang, Xia Hu
**arXiv:** [2608.10393](https://arxiv.org/abs/2608.10393)
**Categories:** Artificial Intelligence (cs.AI); Robotics (cs.RO)

Vision-Language-Action (VLA) models have shown strong capabilities in controlling robots across diverse manipulation tasks. However, their adversarial robustness remains largely underexplored, and exploiting this weakness can lead to physical-world harm. Existing attacks on VLA models often rely on pixel-space perturbations or white-box access, resulting in noticeable artifacts and limited deployability in real-world robotic systems. In this work, we propose DURA, a diffusion-based unrestricted robotic attack that generates visually natural adversarial patches for VLA models. DURA supports both white-box and black-box attack settings, where the black-box setting requires only the predicted actions of the victim model. By optimizing along the latent trajectory of a pretrained diffusion model, DURA generates visually natural patches while steering the robot toward attacker-specified target actions. Extensive experiments in both simulation and the real physical world show that DURA consistently outperforms existing methods. Our findings expose a safety risk for physically deployed VLA models and call for stronger defenses.

---

## 3. Surgical WAM: A World-Action Model for Data-Efficient Surgical Robot Learning

**Authors:** Wenrui Bao, Tianyun Jiang, Zhiben Chen, ..., Peter D. Peng, Yuzhang Shang
**arXiv:** [2608.11204](https://arxiv.org/abs/2608.11204)
**Categories:** Robotics (cs.RO); Artificial Intelligence (cs.AI); Computer Vision and Pattern Recognition (cs.CV)

Learning reliable surgical manipulation policies is bottlenecked by the scarcity of action-labeled demonstrations: teleoperated surgical robot (e.g., dVRK) trajectories with synchronized kinematics are costly to collect, while surgical tasks demand precise contact handling, long-horizon reasoning, and bimanual coordination. Endoscopic video is comparatively inexpensive and abundant relative to synchronized video--kinematics trajectories, and a natural way to exploit it is to learn world models of surgical scenes. However, existing surgical world models use video primarily for simulation or policy evaluation, and rarely translate the learned dynamics into closed-loop control. This gap raises our central question: under a fixed budget of action-labeled demonstrations, does action-free video pretraining improve closed-loop surgical manipulation? To answer it, we introduce the Surgical World-Action Model (Surgical WAM), a unified generative model built on Cosmos Policy that jointly predicts future endoscopic observations and executable surgical robot action chunks. Surgical WAM first learns surgical visual dynamics from action-free video and is then fine-tuned on the fixed action-labeled budget; at deployment, it acts as a closed-loop, receding-horizon controller that executes a short prefix of each predicted action chunk and replans from the resulting observation. On a suite of four simulated surgical manipulation tasks, video pretraining improves the average success rate from 63.5% to 77.8%, including an absolute gain of 20 percentage points on PegTransfer, with the largest improvements on contact-rich and bimanual tasks. These results demonstrate that action-free video provides transferable visual dynamics priors for learning surgical robot control with limited action supervision, positioning data-efficient video pretraining as a practical path toward scaling up surgical robot learning.

---

## 4. Lost in Reconstruction: Aligning Action Representations with Language in Vision-Language-Action Models

**Authors:** Li Wenjie, Yash Jangir, Ignacy Stepka, ..., Marion Kipsang, Yonatan Bisk
**arXiv:** [2608.10484](https://arxiv.org/abs/2608.10484)
**Categories:** Robotics (cs.RO); Artificial Intelligence (cs.AI); Computation and Language (cs.CL)

Action verbs describe not only the physical outcomes of actions, but also how those actions are performed. Yet action representations in vision-language-action models (VLAs) are typically optimized for reconstruction under L1/L2 losses in raw action space, where numerical proximity need not reflect linguistically meaningful distinctions. On BridgeV2, we show that action trajectories contain verb-grounding information beyond visual state changes, and that reconstruction-only discrete tokenization systematically erodes this information. To address this problem, we introduce SALT, a Semantically ALigned action Tokenizer that augments a VQ-VAE-style tokenizer with an auxiliary objective requiring a frozen vision-language model to recover the episode instruction from quantized action latents. Policies trained with SALT achieve 71.9% average success in SimplerEnv, compared with 42.7% for a reconstruction-only VQ-VAE tokenizer and 31.2% for FAST. SALT also develops verb-specialized codes while maintaining reconstruction fidelity. These results show that robot action trajectories provide a source of language grounding and that preserving this structure in action representations can substantially improve language-conditioned control.

---

## 5. FACT: Failure-Aware Causal Training for World-Action Models

**Authors:** Quanquan Peng, Yutong Liang, Rui Yan, Nicklas Hansen, Xiaolong Wang
**arXiv:** [2608.10232](https://arxiv.org/abs/2608.10232)
**Categories:** Robotics (cs.RO); Artificial Intelligence (cs.AI); Machine Learning (cs.LG)

Recent world-action models (WAMs) show that co-training policies with future prediction can provide physical priors for action generation. Building on the future-prediction ability of video models, many WAMs generate future videos and recover actions with inverse-dynamics models, or use these predicted videos as goal conditions for action generation. In both cases, the world model is trained mostly on successful demonstrations and has little reason to predict the consequences of bad actions. We introduce FACT, a causal World-Action Model that predicts future video and task progress conditioned on the executed action. This action-conditioned interface allows failure rollouts to supervise action consequences, turning bad actions into valid future targets rather than being discarded. Failure-aware training makes the progress predictor aware of both successful and failed action outcomes, which can optionally be used to score sampled action candidates at inference. Extensive experiments on simulation and real-world bimanual manipulation tasks show that FACT outperforms many existing baselines, improves as failure data are incorporated into training, and reduces success-biased future hallucination under bad actions. See more details at this https URL

---

## 6. Dreamer-SAC: Off-Policy Learning in Latent World Models for Sample-Efficient Autonomous Driving

**Authors:** Jiazhuo Li, Linjiang Cao, Qi Liu, Xi Xiong
**arXiv:** [2608.10386](https://arxiv.org/abs/2608.10386)
**Categories:** Machine Learning (cs.LG); Robotics (cs.RO)

Sample-efficient reinforcement learning for autonomous driving is often limited by the trade-off between data efficiency and model bias. While world models reduce the reliance on costly environment interactions, policy optimization over learned dynamics remains sensitive to prediction errors. This paper proposes the Dreamer-SAC framework, which integrates a recurrent state-space world model with an off-policy soft actor-critic algorithm trained directly in latent space. The framework uses a combination of real interactions and short-horizon generated trajectories with n-step target estimation and multi-objective supervision. Evaluated in autonomous driving scenarios with objectives encompassing driving efficiency and safety, the proposed framework consistently outperforms representative reinforcement learning baselines, including DreamerV3, SAC, and PPO, while achieving improved performance with substantially fewer real environment interactions. Experiments reveal an inverted-U relationship between rollout horizon and policy performance, where short-horizon latent rollouts achieve the best trade-off between additional training signals and accumulated model bias. Furthermore, n-step target estimation demonstrates more effectiveness over one-step temporal-difference targets in exploiting predicted experience for value learning.

---

## 7. The Evaluation Protocol Determines the Result: An Independent Reproduction of LeWorldModel on TwoRoom

**Authors:** Joyjeet Singh
**arXiv:** [2608.10145](https://arxiv.org/abs/2608.10145)
**Categories:** Machine Learning (cs.LG)

LeWorldModel trains a latent world model with a prediction loss and a single anti-collapse regulariser, and reports approximately 87% of goals reached on TwoRoom, its simplest diagnostic environment. We reproduce that result by independent reimplementation on roughly $25 of rented compute, with all evaluation on one laptop CPU.
We reach 94.0% at the repository's evaluation goal offset, against 84.0% for the authors' own released checkpoint measured under our protocol on identical episodes, and we reproduce the reported representation result directly (position probe Pearson r = 0.9988 against a reported 0.996). Reaching that point required four conventions that determine the outcome and appear in no released configuration file: dense action gathering across a frameskip block, a programmatically-set action-encoder width, ImageNet pixel normalisation, and action z-scoring. A reproducer following the released configurations alone obtains a model whose predictor cannot converge.
The evaluation protocol is itself contested by the released material. The paper's appendix and the repository's configuration specify different goal offsets and step budgets; on the authors' own weights these yield 14.0% and 84.0%, and only the configuration's values reproduce the reported figure. On fifty identical episodes, changing nothing but how the goal is constructed moves that checkpoint from 84.0% to 8.0%.
Two findings generalise. One-step prediction accuracy does not predict long-horizon planning success: across three checkpoints spanning a sevenfold range in prediction error, including the authors' own, it orders short-horizon success monotonically and fails to order long-horizon success at all. And a batch normalisation layer inflated our reported validation loss by up to a factor of 300, concealing a training loss that was flat throughout.

---

## 8. VIScore: Diagnosing Planning-Relevant Quality in Latent World Models

**Authors:** Haiyu Wu, Randall Balestriero, Morgan Levine
**arXiv:** [2608.11174](https://arxiv.org/abs/2608.11174)
**Categories:** Robotics (cs.RO)

Regulating the latent space to an isotropic Gaussian distribution provides a stable and information-maximized landscape for world model planning. However, the latent space property and successful planning remain disconnected. We first study this by comparing SIGReg and VISReg, two regularization loss functions with the same distribution target but different properties. Compared with SIGReg, VISReg has more flexibility in controlling the weights of center, scale, and shape regularization, and a larger batch size brings a finer distribution approximation. We find that the former, despite being beneficial in self-supervised learning (SSL), does not help the planning, whereas the latter improves the planning success on out-of-domain (OOD) datasets. This motivates a deep understanding of the factors that correlate with the success rate. Unlike the previous metrics focusing on the encoded latent only, we propose the Veracity-Influence-Sobriety score (VIScore), a metric that quantifies the reachability and capacity of a predictor given the encoded feature, and the hallucination of the searching-based planner. Compared with straightness, physical-state probing, and empowerment, we show that, with the measurement covering encoder, predictor, and planner, VIScore explains the success rate better than the others, as reflected by a strong Spearman correlation. Specifically, VIScore consistently achieves a Spearman correlation over 0.75 on both seen and unseen models and datasets on the cross-task success rate pool. Moreover, VIScore is the only metric that has a calibration error below the constant fit across all testing scenarios, showcasing the importance of these three aspects in planning success. We hope this metric can help future studies on world model design and diagnosis.

---

## 9. Flex-$π$: A Multi-Stream World-Action Model with Compute Flexibility

**Authors:** Ge Yan, Jinghao Liu, Yuzhi Fan, ..., Jesse Zhang, Dieter Fox
**arXiv:** [2608.10860](https://arxiv.org/abs/2608.10860)
**Categories:** Robotics (cs.RO); Computer Vision and Pattern Recognition (cs.CV)

World-action models (WAMs) predict the future to act better, but nearly all of them predict only RGB latents, trained purely for pixel reconstruction, with no explicit signal for the 3D geometry or object semantics manipulation needs. We find a surprising free lunch: the same frozen video-generation VAE that encodes RGB also encodes 3D pointmaps almost losslessly, with no pointmap-specific training at all. This lets us supervise Flex-$\pi$, a 6B-parameter WAM, on 3D geometry and object-centric DINO semantics alongside RGB, at no cost in new sensors, new pre-training, or inference latency. Every visual signal is projected into this shared latent space and denoised jointly with actions inside a Mixture-of-Transformers backbone; per-stream dropout with cross-modality forcing then lets a single trained checkpoint run on any subset of these streams, from a fast action-only mode to full joint generation. The result is a policy that is exceptionally demonstration-efficient and generalizes well, beating the strongest baselines by up to 2-7$\times$ on dexterous, precise, real-world bimanual manipulation tasks both in and out of distribution, all while running faster than $\pi_{0.5}$. Our project website: this https URL

---

## 10. Neural Introspection Gating for Adaptive KV-Cache Reuse in Vision-Language-Action Models

**Authors:** Zhijie Wu, Kento Kawaharazuka, Kei Okada
**arXiv:** [2608.10824](https://arxiv.org/abs/2608.10824)
**Categories:** Robotics (cs.RO); Computer Vision and Pattern Recognition (cs.CV)

Vision-Language-Action(VLA) models map camera images and language instructions directly to motor commands through a single autoregressive transformer. In real-time control, they still spend substantial compute recomputing key-value(KV) representations for visual tokens that barely change across neighboring frames. Recent work such as VLA-Cache reduces that cost by reusing KV states for visually static patches, but its policy relies only on observation-space heuristics and does not account for the model's own uncertainty. We propose Gated VLA-Cache, a lightweight, training-free extension that augments visual-similarity caching with neural introspection. The method monitors the logit margin between the top two predicted action tokens, a zero-cost confidence signal available during decoding. When the margin drops below a threshold, the cache is invalidated and a full recompute is triggered. Evaluated on four LIBERO benchmark suites with both OpenVLA and OpenVLA-OFT, Gated VLA-Cache improves reliability when blind caching hurts. On LIBERO-Goal and LIBERO-Long, it recovers over 100% of the lost accuracy while retaining 80% of the compute savings.

---

## 11. JEPA-WAM: Stage-Level Joint-Embedding Prediction for World-Action Models in Robot Manipulation

**Authors:** Xiao Liu, Yuguang Yang, Xi Wang, ..., Yilun Chen, Yan Wang
**arXiv:** [2608.10780](https://arxiv.org/abs/2608.10780)
**Categories:** Robotics (cs.RO)

Generalist robot policies aim to map multimodal observations and linguistic task instructions to actions across diverse tasks. However, existing methods typically represent the future as a fixed, short video-action chunk. This short-term future captures local scene evolution for action execution, but it does not explicitly describe the stage-level future that specifies how a task should progress from its current stage to the next. We therefore distinguish two complementary futures for robot manipulation: a short-term physical future to capture local scene evolution and a stage-level semantic future to represent task progress. We introduce JEPA-WAM, which augments a Motus-based World Action Model (WAM) with Stage-JEPA, a goal-conditioned Joint-Embedding Predictive Architecture (JEPA) predictor. Given the current observation and task instruction, Stage-JEPA uses a frozen V-JEPA2 encoder to extract the current-state representation and predicts the latent target of the next inferred stage. Across 50 RoboTwin 2.0 tasks in clean and randomized environments, JEPA-WAM achieves 90.25% overall success and reduces the mean number of execution steps in successful rollouts by 5.97% relative to the strongest baseline.

---

## 12. Toward the Cognitive--Physical Limits of Embodied Intelligence through a World-Model-Centric Autonomous Racing Agent

**Authors:** Zitong Shan, Baichuan Lou, Yanxin Zhou, ..., King Ho Holden Li, Chen Lv
**arXiv:** [2608.10618](https://arxiv.org/abs/2608.10618)
**Categories:** Robotics (cs.RO)

Embodied artificial intelligence aims to develop agents that perceive, reason, and act through continuous interaction with the physical world. However, most embodied systems are still evaluated within conservative safety margins or moderate interaction regimes, leaving their capability boundaries under extreme conditions insufficiently understood. Autonomous racing provides a stringent testbed by combining high-frequency localization and perception, adversarial interaction, near-saturated vehicle dynamics, and strict safety constraints. Existing systems push high-speed performance but rarely model and refine cognitive and physical limits jointly. Here we show that a world-model-centric autonomous racing agent provides a concrete step toward exploring these coupled limits. The framework learns predictive world models from near-limit successes and failures to capture interaction evolution, ego dynamics, and feasible-motion boundaries, coupling world-state construction, future-aware reasoning, and near-limit control in a closed-loop refinement process. Training data were collected from real-vehicle autonomous racing, where the onboard system maintained robust localization and perception at speeds up to 256.3 km/h and peak lateral acceleration of 26.8 m/s$^2$. In full-scale simulated racing, the well trained world-model-centric agent achieves an 88.3% interaction success rate across various challenging simulated racing scenarios. Closed-loop refinement of the world model and policy further improved utilization of cognitive-physical limits, recovery from failure modes, and generalization across varying conditions and unseen circuits. These results suggest a boundary-aware methodology in which world models help embodied agents represent, predict, and continually refine their capability boundaries for safer real-world deployment.

---

## 13. DriveVLA-M0: Failure-Aware Memory Augmentation for Autonomous Driving

**Authors:** Zebin Xing, Yupeng Zheng, Qiang Chen, ..., Qichao Zhang, Dongbin Zhao
**arXiv:** [2608.10413](https://arxiv.org/abs/2608.10413)
**Categories:** Computer Vision and Pattern Recognition (cs.CV)

Vision-Language-Action (VLA) models have recently emerged as a promising paradigm for end-to-end autonomous driving by enabling unified reasoning across perception, language, and planning. However, existing approaches lack mechanisms to exploit past failures or adapt to distribution shifts, causing the model to persistently underperform on similar scenarios where it has previously failed. In this paper, we propose DriveVLA-M0, a retrieval-augmented VLA with failure-aware latent memory. We construct a latent memory pool that stores failure cases along with their structure scene representations and expert trajectory labels, and design a dedicated Retrieve Model that decouples static road structure and dynamic agent interactions to enable structurally grounded retrieval. At inference time, retrieved cases are injected into the model via a lightweight decoupled LoRA-based test-time training (TTT) mechanism, allowing targeted and scenario-specific correction without modifying the backbone. Extensive experiments on NAVSIMv1 and NAVSIMv2 benchmark demonstrate that our approach consistently outperforms prior methods, achieving 94.1 PDMS on Navtest and 47.0 EPDMS on Navhard with only 26.44 ms TTT backward latency overhead. Furthermore, we show that DriveVLA-M0 scales effectively with additional memory, enabling training-free performance gains through memory expansion. The code is available at this https URL.

---

## 14. 4D-WAM: 4D Consistent World Modeling for Autonomous Driving

**Authors:** Jiacheng Fu, Yibo Yuan, Meng Tian, ..., Hang Xu, Zhiwei Xiong
**arXiv:** [2608.10107](https://arxiv.org/abs/2608.10107)
**Categories:** Computer Vision and Pattern Recognition (cs.CV)

Emerging World-Action Models (WAMs) have demonstrated promising performance in autonomous driving by jointly modeling future driving scene evolution and trajectory planning. However, existing WAMs are typically trained with video data, which is only 2D projections of the underlying 4D driving scene. Consequently, WAMs fail to understand and capture the structure of 4D scenes and thus generate visually plausible yet 4D inconsistent future predictions that mislead downstream planning. To alleviate this issue, we present 4D-WAM, a model that leverages geometric foundation models for training-time supervision to enable 4D consistent world modeling. Specifically, we feed WAM-predicted future frames into a geometric foundation model, and use 4D-aware responses to define a 4D consistency loss. This loss encourages the model to understand, represent, and predict physically consistent 4D scenes during training, without additional inference cost. Moreover, we identify an early-decision phenomenon in WAMs and propose a decision-oriented timestep sampling strategy that emphasizes supervision at early, high-noise stages, where driving decisions are primarily formed. By propagating 4D supervision to this critical decision-formation phase, the proposed strategy further improves trajectory planning. Extensive experiments demonstrate that 4D-WAM effectively models 4D consistent scene evolution and achieves state-of-the-art performance on challenging NAVSIM-v1 and NAVSIM-v2 benchmarks.

---
