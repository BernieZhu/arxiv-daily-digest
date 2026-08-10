# arXiv Daily Digest — 2026-07-17

**Mode:** direct
**Categories:** cs.AI, cs.LG, cs.RO, cs.CV
**Keywords:** VLA, world model, world action model
**Papers found:** 15

---

## 1. Concept-Guided Spatial Regularization for World Models in Atari Pong

**Authors:** Yukuan Lu, Zaishuo Xia, Weyl Lu, Yubei Chen
**arXiv:** [2607.15142](https://arxiv.org/abs/2607.15142)
**Categories:** Artificial Intelligence (cs.AI); Machine Learning (cs.LG)

World models are usually evaluated as components of model-based reinforcement learning (MBRL) systems, while the world models themselves are rarely studied in isolation.
We examine five representative visual world-model agents in Atari Pong: DreamerV3, DIAMOND, TWISTER, Simulus, and STORM. After reproducing their training pipelines and matching the reported agent performance, we freeze the learned world models and evaluate them with a closed-loop rollout diagnostic: a policy trained separately from the corresponding MBRL agent interacts with each frozen model, and the generated video trajectories are inspected for visual and dynamical errors. Across all five models, the rollouts contain clear failures, including ball disappearance, incorrect ball motion, and invalid ball-paddle interactions.
Beyond visual trajectories, we further evaluate them with pixel-space zero-shot MBRL, where a new policy is trained entirely inside a frozen world model and then evaluated in the real environment. Across all five models, the resulting policies substantially underperform those produced by the corresponding original MBRL training pipelines. The gap is particularly large for DreamerV3, whose mean return drops from -5.5 to -20.9, near the minimum Pong return of -21.
We hypothesize that insufficient modeling of task-critical concepts, such as the ball in Pong, may contribute to these failures. We therefore propose Concept-Guided Spatial Regularization (CGSReg), an auxiliary pixel reconstruction loss applied to segmented concept regions. Experiments show that CGSReg improves both closed-loop rollouts and pixel-space zero-shot MBRL in DreamerV3, DIAMOND, and TWISTER. Its effects vary across the remaining models and evaluation metrics, indicating that CGSReg alone does not address all world-model bottlenecks.

---

## 2. Action QFormer: Structured Representation Shaping under Action Supervision in Vision-Language-Action Models

**Authors:** Yufeng Ji, Wenhao Tang, Haoyi Niu, ..., Yi Wu, Zhongyu Li
**arXiv:** [2607.14635](https://arxiv.org/abs/2607.14635)
**Categories:** Artificial Intelligence (cs.AI); Computer Vision and Pattern Recognition (cs.CV); Robotics (cs.RO)

Action supervision in vision-language-action (VLA) models is often treated as a downstream objective for learning action prediction. In this paper, we study it instead as a force that shapes inherited multimodal representations. We show that this shaping has a dual effect: it is necessary for forming action-compatible representations, but when action supervision is applied too directly to the inherited multimodal pathway, it can also destabilize representations that support language-side processing and object grounding. To address this tension, we introduce Action QFormer, a query-based action-facing interface that uses instruction-conditioned queries to reorganize inherited multimodal information into action-facing representations before downstream action generation. In zero-shot sim-to-real navigation, Action QFormer improves average closed-loop task success from 18.8% to 56.3%, raises fixed-instruction action-generation correctness from 22.5% to 75.5%, and nearly eliminates out-of-distribution instruction generations. Further analyses show that Action QFormer changes how action supervision shapes inherited multimodal representations, reducing broad upstream rewriting while preserving targeted and sometimes constructive action-supervised adaptation. These results suggest that improving VLA performance requires not only stronger pretrained backbones, but also better ways of selecting and organizing inherited multimodal information while controlling how it is shaped under action supervision.

---

## 3. When a Verified World Model Still Loses: Play-Adequacy vs Prediction-Accuracy in LLM-Synthesized Code World Models

**Authors:** Javier Aguilar Martín
**arXiv:** [2607.14169](https://arxiv.org/abs/2607.14169)
**Categories:** Artificial Intelligence (cs.AI); Machine Learning (cs.LG)

Large language models can synthesize a game's rules as executable code - a Code World Model (CWM) - which a classical planner then searches over. Such models are typically accepted when they reach high transition accuracy on sampled trajectories. We argue this is the wrong notion of adequacy for planning.
We show four things. (1) An LLM-synthesized CWM can pass a sampling gate at 100% transition accuracy and be $\geq 98\%$ state-accurate on the planner's own search distribution, yet lose systematically at play, because the $<1\%$ it gets wrong is exactly the pivotal dynamics; the play cost of the omitted rule is $0.091$ (seed-clustered 95% CI $[0.065,0.117]$, $n=4800$). We call this the verified-vs-correct gap, and confirm it end-to-end through the synthesis pipeline. (2) The harm follows a quantitative law, $\mathrm{danger}=\mathrm{play\_cost}\times(1-\mathrm{rarity})^N$, whose $(1-\mathrm{rarity})^N$ gate-miss factor is proven exact and whose play cost is empirically bounded. (3) The failure is not repaired by more data: LLM synthesis behaves as rule translation, not rule inference, and did not infer the omitted rule across models (GPT-5.x) and data regimes (including DAgger and targeted examples). (4) The same mechanism recurs on the belief-inference function of imperfect-information CWMs: we prove a coverage bound (a size-$N$ gate is identifying when $N\gtrsim b^{d_{\max}}$), explaining why shallow games such as Kuhn poker show no gap, and hand-construct Beacon, a verified-but-wrong inference function that passes the gate yet loses every game.
These results suggest adequacy for planning-oriented world models should be measured on the search distribution or by play directly, not by prediction accuracy on sampled transitions.

---

## 4. Steering Robustness into World Action Models via Mechanistic Interpretability and Optimal Control

**Authors:** Jihoon Hong, Julian Skifstad, Qiyue Dai, Alice Chan, Glen Chou
**arXiv:** [2607.14943](https://arxiv.org/abs/2607.14943)
**Categories:** Robotics (cs.RO); Artificial Intelligence (cs.AI); Machine Learning (cs.LG); Systems and Control (eess.SY); Optimization and Control (math.OC)

World Action Models (WAMs) enable semantically- and physically-informed control but are brittle under distribution shift. In this work, we use mechanistic interpretability to study how robustness-relevant perturbations are represented in WAM activation space. Comparing activations across successful and unsuccessful rollouts, we find some WAM architectures exhibit low-dimensional linear separability for robustness-critical features, while others do not. This motivates the use of contrastive activation directions for training-free WAM steering. We also show that local linearity in WAM activation dynamics enables efficient feedback steering via model-based optimal control, yielding World-Action Linear Quadratic Regulator (WA-LQR), a minimally-invasive reduced-order LQR controller. Via mechanistic evaluations, we predict strong steerability in the Cosmos-Policy and DiT4DiT models but weak steerability in LingBot-VA, consistent with steering intervention results. On Cosmos-Policy and DiT4DiT, WA-LQR generalizes contrastive directions to new tasks and improves robustness to camera, gripper, and visual-noise perturbations over unsteered and prompt steering baselines.

---

## 5. FoMoVLA: Bridging Visual Foresight and Motion Guidance for Vision-Language-Action Models

**Authors:** Wei Li, Peijin Jia, Yuan Ma, ..., Bailin Li, Kun Zhan
**arXiv:** [2607.14739](https://arxiv.org/abs/2607.14739)
**Categories:** Computer Vision and Pattern Recognition (cs.CV); Artificial Intelligence (cs.AI)

Vision-Language-Action (VLA) models have achieved impressive results in visuomotor policy learning, yet remain fundamentally reactive, mapping current observations and language to actions without explicit forward prediction of world dynamics. Existing visual foresight methods predict future visual states but lack explicit motion guidance: they show where to go but not how to get there. We argue that future feature prediction and sparse point tracking are naturally complementary: the former provides the goal state, while the latter captures the continuous motion path toward it. We propose FoMoVLA, a framework that augments VLA representations with explicit spatio-temporal supervision by jointly learning future feature foresight and sparse 2D point tracking, enhancing the continuous action policy. FoMoVLA introduces compact foresight tokens to decode future feature states, decodes sparse temporal 2D point trajectories to model compact geometric motion, and couples both through a lightweight future-conditioned cross-attention module that enables consistent reasoning between anticipated states and point dynamics. Extensive experiments on LIBERO, RoboCasa GR-1 Tabletop, and LIBERO-Plus demonstrate state-of-the-art performance and strong zero-shot generalization. Project page is available at this https URL.

---

## 6. Never Too Late for Force: Accelerating VLA Post-Training with Reactive Force Injection

**Authors:** Yi Wang, Wendi Chen, Zimo Wen, ..., Chuan Wen, Cewu Lu
**arXiv:** [2607.14236](https://arxiv.org/abs/2607.14236)
**Categories:** Robotics (cs.RO); Artificial Intelligence (cs.AI); Machine Learning (cs.LG)

Pretrained vision-language-action (VLA) policies provide strong language-conditioned manipulation knowledge, but they remain largely vision-driven and can struggle once manipulation enters contact states where the scene is occluded, depth is ambiguous, or small force errors push execution off the offline demonstration distribution. We present LIFT (Late Reactive Injection of Force for VLA Post-Training), a force-aware post-training framework that adds contact reactivity to a pretrained VLA policy while preserving its general manipulation knowledge. LIFT grafts a reactive action expert beside the original action expert, initializes it from pretrained action weights, and injects recent 6D end-effector force through causal force memory and zero-initialized cross attention, enabling actions to be refreshed during execution. To address the policy-dependent distribution shift of contact feedback, LIFT further couples reactive force injection with an online DAgger loop that trains on a mixture of offline task-alignment data and human-corrected online rollouts. Across towel folding, book insertion, and Hanoi ring placement, LIFT learns faster and reaches higher performance than vision-only post-training, while ablations show that reactive force memory and online corrective data are both important for robust contact-rich manipulation. Our code and data will be publicly available.

---

## 7. RENEW: Towards Learning World Models and Repairing Model Exploitation from Preferences

**Authors:** Logan Mondal Bhamidipaty, Mykel Kochenderfer, Subramanian Ramamoorthy
**arXiv:** [2607.14180](https://arxiv.org/abs/2607.14180)
**Categories:** Machine Learning (cs.LG); Artificial Intelligence (cs.AI)

World models are widely used in offline reinforcement learning (RL) to improve sample efficiency and generate experience beyond a fixed dataset. However, they are vulnerable to model exploitation where data coverage is thin. Prior work addresses this either by collecting more expert demonstrations, which is often expensive, unsafe, or unavailable, or by conservative algorithms that avoid uncertain regions, which limits generalization. We propose instead to repair exploitation directly using human preferences over imagined rollouts, leveraging the strong intuitive physics that allows humans to easily spot egregious dynamics hallucinations. We formalize this as Dynamics Learning from Human Feedback (DLHF), a Bradley-Terry preference loss over trajectory log-likelihoods under a learned dynamics model. Unfortunately, naive DLHF is sample inefficient, so we introduce RENEW, which uses epistemic uncertainty to focus finetuning where the model is most exploitable. We evaluate on several Jumanji and classic control environments and find that while naive DLHF requires an outsize preference budget, RENEW makes the framework practical by improving sample efficiency, limiting catastrophic forgetting, and reducing exploitation in pretrained world models. Taken together, our results provide initial evidence that preferences can supervise world model dynamics directly, offering a new approach to addressing exploitation in offline model-based RL.

---

## 8. BadWAM: When World-Action Models Dream Right but Act Wrong

**Authors:** Qi Li, Xingyi Yang, Xinchao Wang
**arXiv:** [2607.15207](https://arxiv.org/abs/2607.15207)
**Categories:** Machine Learning (cs.LG); Robotics (cs.RO)

World-action models (WAMs) are emerging as a promising foundation for embodied control: rather than predicting actions alone, they learn representations that couple action generation with future world prediction. This coupling is often viewed as a source of robustness, interpretability, and safety, as a robot's action can in principle be checked against its imagined future. In this paper, we show that this assumption is fragile. We introduce BadWAM, a unified framework for modeling and evaluating World-Action Drift Attacks: a new class of WAM-specific adversarial attacks that use small visual perturbations to break the alignment between what a WAM imagines and what it executes. BadWAM characterizes this attack surface along two natural criteria: attack strength and stealthiness. When the adversary prioritizes disruption, BadWAM instantiates an action-only adversarial attack, which directly drives the model toward task-failing actions. When the adversary additionally prioritizes stealth, BadWAM instantiates an imagination-preserving adversarial attack, which seeks to induce harmful action shifts while keeping the model's predicted future close to its clean imagination. Together, these two attacks capture a spectrum of WAM-specific failures: from overt action hijacking to stealthier cases where the model appears to imagine a plausible future but executes a desynchronized action. We evaluate BadWAM across different variants of WAMs. Results show that our attacks substantially reduce task success rates under closed-loop execution. For example, our action-only attack reduces the model performance from 96.5% to 43.1% success. The results of our imagination-preserving attack further exposes a WAM-specific vulnerability: moderate future-preserving regularization can maintain strong attack performance while reducing future imagination drift.

---

## 9. DriftWorld: Fast World Modeling through Drifting

**Authors:** Susie Lu, Haonan Chen, Weirui Ye, Yilun Du
**arXiv:** [2607.15065](https://arxiv.org/abs/2607.15065)
**Categories:** Robotics (cs.RO); Computer Vision and Pattern Recognition (cs.CV); Machine Learning (cs.LG)

Predictive world models enable robots to plan by imagining the outcomes of their actions, but their value for control hinges on generating many rollouts quickly. This creates a bottleneck for diffusion-based world models: multistep sampling makes each rollout expensive, limiting large-scale action search at inference time. We introduce DriftWorld, an action-conditioned world model based on drifting generative models. Rather than denoising iteratively at inference, DriftWorld learns an action-conditioned drift during training, allowing it to generate future frames from the current observation and a candidate action sequence in a single forward pass at 30+ fps, which is 17x faster on average than diffusion based baselines. We evaluate DriftWorld on standard vision-based robotic manipulation benchmarks, including Bridge-V2, RT-1, Language Table, Push-T, and Robomimic. By producing rollouts that are both accurate and fast, DriftWorld achieves state-of-the-art decision-making performance with far less inference time than diffusion-based world model baselines. Beyond online control, DriftWorld can also serve as an offline simulator for ranking real-world robot policies, with rollout-based scores correlating with ground truth at up to 0.99. These results show that drifting models are a strong fit for robot world modeling, where fast, high-quality imagination directly supports planning and policy evaluation.

---

## 10. DiMaS: Distribution Matching for Steering Vision-Language-Action Models

**Authors:** Pegah Khayatan, Sara Meziane, Jayneel Parekh, Matthieu Cord
**arXiv:** [2607.14280](https://arxiv.org/abs/2607.14280)
**Categories:** Robotics (cs.RO); Machine Learning (cs.LG)

Flow-matching-based vision-language-action (VLA) models have emerged as powerful policies for robotic manipulation, yet a critical capability remains underexplored: fine-grained behavioral control, the ability to govern how a robot performs a task by intervening on its internal representations. Representation steering is a well-established interpretability tool for language and vision-language models, where behavioral features are typically encoded as linear directions, but we show that these classic methods fall short in VLAs. We propose DiMaS, a Distribution-Matching Steering strategy tailored to flow-matching VLAs, which transports between representation distributions rather than shifting along a fixed direction, and show that it effectively controls behavior across two state-of-the-art VLAs. We further examine the generalizability of this strategy as the tasks it is learned from and evaluated on grow increasingly dissimilar, characterizing where behavioral control transfers and where it weakens. Finally, through an analysis of the representation structure of the action expert, we explain why classical linear steering falls short in the visuomotor setting: behavioral features are linearly decodable but not linearly steerable, which motivates the distribution-matching design of DiMaS. Our code is publicly available at this https URL, with additional results and videos at this https URL

---

## 11. CosFly-VLA: A Spatially Aware Vision-Language-Action Model for UAV Tracking

**Authors:** Ruilong Ren, Songsheng Cheng, Yunpeng Zhou, ..., Da Zhang, Kangli Wang
**arXiv:** [2607.15004](https://arxiv.org/abs/2607.15004)
**Categories:** Robotics (cs.RO)

Dynamic target tracking is essential for Unmanned Aerial Vehicles (UAVs) operating in complex urban environments, where both the target and the camera viewpoint change continuously. Existing Vision-Language-Action (VLA) policies can track visible targets effectively, but their performance often degrades when buildings, vegetation, or roadside objects block the line of sight. During sustained occlusion, a policy may lose the target state, execute actions toward an incorrect region, and amplify this error through subsequent observations until re-acquisition becomes impossible. To this end, we present CosFly-VLA, a spatially aware VLA model that jointly grounds the target, estimates its visibility, and generates continuous flight actions through a structured prediction interface. To train this policy, we use a large-scale recipe over diverse data sources. Spatially Grounded Continued Pretraining (CPT) on a 500k mixed pool injects UAV-view depth, distance, and 3-D spatial reasoning. A three-stage Curriculum-based Supervised Fine-Tuning (SFT) process then specializes the tracker through multi-head warm-up followed by two-stage curriculum learning over natural and hard / long-occlusion data. Chain-of-Thought (CoT) training subsequently teaches recovery-oriented reasoning traces before structured answers. Finally, a closed-loop Reinforcement Learning (RL) stage optimizes tracking behavior with a multi-component reward covering stand-off tracking, grounding quality, collision avoidance, and task success. Relative to OpenVLA, CosFly-VLA-0.8B reduces open-loop Average Displacement Error (ADE) by 34.1% on seen-test and 35.3% on unseen-test. Closed-loop optimization improves Success Rate (SR) by 29.8% and 2.5%, respectively. These results demonstrate progress from visible-frame imitation toward spatially grounded action-closed-loop control, evaluated under a shared oracle state history.

---

## 12. AeroAct: Action-Centered World-Action Models for Language-Conditioned Quadrotor Flight

**Authors:** Xinhong Zhang, Qiyuan Zhu, Yubo Huang, ..., Jian Sun, Gang Wang
**arXiv:** [2607.14997](https://arxiv.org/abs/2607.14997)
**Categories:** Robotics (cs.RO)

Language-conditioned quadrotor flight requires a policy to ground semantic goals, anticipate the visual consequences of ego-motion, and output control references that remain smooth and dynamically executable under rapidly changing first-person views. Existing aerial vision-language navigation and vision-language-action methods commonly use discrete actions, high-level waypoints, or instantaneous velocity commands, which provide limited supervision about how flight actions change future observations. We present AeroAct, an action-centered world-action model (WAM) for quadrotor navigation. To the best of our knowledge, AeroAct is the first WAM instantiated and demonstrated for real-world aerial flight. The model adapts a pretrained video diffusion Transformer to predict local trajectory-action chunks from egocentric visual history, proprioception, and language. Future first-person frames are used during training as dense consequence supervision, while deployment directly decodes actions without generating future video. To obtain aligned visual, state, language, and dynamically feasible action data, we build a DiffAero-based pipeline with complementary Isaac Lab and 3D Gaussian splatting renderers. We further introduce a low-cost handheld collection device that couples camera observations with motion estimates to recreate flight-like egocentric trajectories, and a self-guidance procedure that improves temporal consistency across overlapping trajectory chunks. Closed-loop simulation and real-world experiments show that temporal visual context improves target tracking and object-search performance, and that WAM-based policies can be executed on a physical quadrotor.

---

## 13. Towards Human-like Physical Intelligence: LifelongVision-Language-Action Learning for Robotic Manipulation

**Authors:** Yao He, Gan Sun, Wenqi Liang, Fazeng Li, Yang Cong
**arXiv:** [2607.14852](https://arxiv.org/abs/2607.14852)
**Categories:** Robotics (cs.RO)

Similar to the natural capabilities of humans to sequentially learn new tasks, robots with Vision-Language-Action (VLA) models should possess lifelong learning ability to learn a new task when deployed in open-world environments. However, most recently proposed lifelong learning models aim to effectively learn the current task (plasticity) or maintain high accuracy on previous tasks (stability), while the plasticity-stability trade-off remains largely unsolved in robotic manipulation models. To address this fundamental challenge, we propose a cache-efficient lifelong Vision-Language-Action learning framework for robotic manipulation (i.e., LifelongVLA), which alleviates the plasticity-stability trade-off with a dual-timescale adaptation mechanism while achieving low-cost robotic deployment with a cache-efficient replay strategy. More concretely, we propose a dual-timescale LoRA gating module to decompose VLA adaptation into two lightweight pathways: a short-term adapter for plasticity and a long-term adapter for stable consolidation. These pathways are integrated via a task-aware gate, enabling explicit control of the plasticity-stability trade-off. In the skill replay phase, a cache-efficient stochastic replay strategy is proposed to preserve more balanced retention signals without full-trajectory storage. Finally, experiments show that LifelongVLA outperforms existing baselines, demonstrating efficient skill expansion, robust retention of learned manipulation behaviors, and reduced reliance on retraining for real-world deployment on an xArm robot.

---

## 14. Lights, Camera, Malfunction: When Illumination Robustness Leaves VLA Models Blind to Color

**Authors:** Marino Watanabe, Takami Sato, Kentaro Yoshioka
**arXiv:** [2607.14698](https://arxiv.org/abs/2607.14698)
**Categories:** Robotics (cs.RO)

Vision-Language-Action (VLA) models have emerged as a powerful paradigm for general-purpose robot manipulation; however, their transition to real-world environments reveals vulnerabilities to minor environmental perturbations. We propose FLARE, an optimized physical spotlight attack framework that exploits these vulnerabilities via targeted illuminations, dropping baseline task success rates to zero without any access to model internals. While adversarial training is the standard countermeasure, we identify a critical and previously underestimated defensive pitfall: naive data augmentations incorrectly condition VLA models to discard color as noise, collapsing their visual perception into a purely shape-biased processor. We expose this degradation through a diagnostic grayscale evaluation, in which the defended model maintains high success rates on grayscale inputs, while its success rate on benign, color-dependent real-world tasks drops to at most 47.5%, well below the undefended baseline. To address this, we propose ChromaGuard, a chroma-preserving adversarial training method. On a physical 6-DoF robotic platform, we demonstrate that ChromaGuard achieves 97.5% and 92.5% success rates in benign and attacked color-dependent tasks, respectively.

---

## 15. Reflex: Real-Time VLA Control through Streaming Inference

**Authors:** Yuanchun Guo, Bingyan Liu
**arXiv:** [2607.14695](https://arxiv.org/abs/2607.14695)
**Categories:** Robotics (cs.RO)

Flow matching Vision-Language-Action (VLA) models promise precise continuous control, but their iterative denoising nature introduces fundamental incompatibilities with real-time robotics: global timestep injection invalidates KV-caching, forcing a choice between slow $O(N^2)$ re-computation or mathematically incorrect cache reuse. We present \textbf{Reflex}, a framework that enables \textit{real-time streaming inference} for flow matching policies by exploiting the \textit{Timestep-Invariance Property} -- that perception encoders are functionally independent of the denoising loop. Reflex partitions the attention context into static, sliding, and dynamic regions, enabling $O(1)$ incremental cache updates while preserving full-batch-equivalent attention outputs for fixed inputs. To ensure stability under continuous high-frequency inference, we introduce \textit{AdaRMSNorm}, an adaptive normalization layer that prevents BFloat16 numerical collapse by gating on flow phase. We further maximize throughput through an \textit{async pipeline} that decouples visual encoding from action generation, combined with \textit{operator fusion} that reduces kernel overhead. On LIBERO and Kinetix benchmarks, Reflex achieves a 2.58$\times$ inference speedup and 50Hz stable streaming, reducing reaction latency by up to 54\% and enabling efficient deployment without performance degradation.

---
