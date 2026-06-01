# arXiv Daily Digest — 2026-05-21

**Mode:** direct
**Categories:** cs.AI, cs.LG, cs.RO, cs.CV
**Keywords:** VLA, world model, world action model
**Papers found:** 8

---

## 1. Lost in Fog: Sensor Perturbations Expose Reasoning Fragility in Driving VLAs

**Authors:** Abhinaw Priyadershi, Jelena Frtunikj
**arXiv:** [2605.21446](https://arxiv.org/abs/2605.21446)
**Categories:** Robotics (cs.RO); Artificial Intelligence (cs.AI)

Interpretable autonomous driving planners depend not only on generating explanations, but also on those explanations remaining reliable under real-world sensor degradation. In this paper we present a controlled perturbation study of Vision-Language-Action (VLA) robustness in autonomous driving, evaluating Alpamayo R1 (10B parameters) across 1,996 scenarios under eight sensor perturbations (Gaussian noise at four intensities, two lighting extremes, and two fog levels; ${\sim}18{,}000$ inference trials). We find that reasoning consistency is a high-fidelity indicator of trajectory reliability: when Chain-of-Causation (CoC) explanations change after perturbation, trajectory deviation spikes $5.3{\times}$ (21.8m vs 4.1m), with $r\!=\!0.99$ across attack types and $r_{pb}\!=\!0.53$ per-sample (Cohen's $d\!=\!1.12$). A controlled ablation provides evidence that enabling CoC generation is associated with improved trajectory accuracy (11.8% on average across conditions; $p < 0.0001$) under matched inference settings. Over the tested noise range ($\sigma \in \{10, 30, 50, 70\}$), degradation is approximately linear ($R^2\!=\!0.957$), while standard input preprocessing defenses provide only marginal relief. Together, these results establish CoC consistency as a quantitative proxy for planning safety and motivate reasoning-based runtime monitoring for safer VLA deployment.

---

## 2. Grounding Driving VLA via Inverse Kinematics

**Authors:** Junsung Park, Hyunjung Shim
**arXiv:** [2605.21061](https://arxiv.org/abs/2605.21061)
**Categories:** Computer Vision and Pattern Recognition (cs.CV); Artificial Intelligence (cs.AI); Robotics (cs.RO)

Existing Driving VLAs predict trajectories while largely ignoring their visual tokens -- a phenomenon we trace not to insufficient training but to a structurally ill-posed task formulation. We show that trajectory recovery, when viewed through the lens of inverse kinematics, requires both a current and a future visual state as boundary conditions; existing VLAs supply only the former, which encourages the model to shortcut through ego status and text commands alone. To address this, we re-design Driving VLA in the style of an inverse kinematics solver. First, a next visual state prediction objective that requires the LLM to predict the future visual scene provides dense visual supervision and suppresses shortcut paths. Second, a separate Inverse Kinematics Network (a cross-attention-based conditional diffusion model) that takes only the current and future visual states as input is designed to suppress reliance on ego status and textual shortcuts during trajectory decoding. With this simple prescription alone, our 0.5B-scale model recovers visual grounding and reaches trajectory planning performance comparable to 7B--8B VLAs more than an order of magnitude larger, on both the closed-loop NAVSIM-v2 and the nuScenes benchmarks. Extensive analysis further shows that this improvement stems from a recovered ability to exploit visual features, with the effect being most pronounced in dynamic driving situations such as turning.

---

## 3. PointACT: Vision-Language-Action Models with Multi-Scale Point-Action Interaction

**Authors:** Shizhe Chen, Paul Pacaud, Cordelia Schmid
**arXiv:** [2605.21414](https://arxiv.org/abs/2605.21414)
**Categories:** Robotics (cs.RO); Computer Vision and Pattern Recognition (cs.CV)

Vision-Language-Action (VLA) models have shown strong potential for general-purpose robotic manipulation by leveraging large pretrained vision-language backbones. However, most existing VLAs rely primarily on 2D visual representations, which limit their ability to reason about fine-grained geometry and spatial grounding - capabilities that are essential for precise and robust manipulation in 3D environments. In this paper, we propose PointACT, a dual-system 3D-aware VLA policy that integrates hierarchical 3D point cloud representations directly into the action decoding process. PointACT employs a multi-scale point-action interaction mechanism with efficient bottleneck window self-attention, enabling evolving action tokens to densely attend to both local geometric detail and global scene structure. We evaluate PointACT on the LIBERO and RLBench benchmarks and systematically compare it against monolithic and dual-system VLA baselines, including variants augmented with point cloud inputs. PointACT achieves consistent improvements across both benchmarks, increasing success rates by 10% on the challenging RLBench-10Tasks suite over state-of-the-art pretrained VLAs, with even larger gains when the vision-language backbone is frozen and the action expert is trained from scratch. Extensive ablation studies demonstrate that tightly coupling hierarchical 3D geometry with pretrained 2D semantic representations is critical for robust and spatially grounded robot control. Our results also highlight the promise of pretrained 3D representations for 3D-aware VLA policies.

---

## 4. VLA-REPLICA: A Low-Cost, Reproducible Benchmark for Real-World Evaluation of Vision-Language-Action Models

**Authors:** Alex S. Huang, Jiahui Zhang, Shiqing Tang, Yu Xiang
**arXiv:** [2605.20774](https://arxiv.org/abs/2605.20774)
**Categories:** Robotics (cs.RO)

Vision-Language-Action (VLA) models have shown strong promise for general-purpose robotic manipulation, but their real-world evaluation remains limited by a lack of accessible, reproducible, and consistent benchmarks. Simulation benchmarks fail to capture real-world complexity, while existing real-world benchmarks often require expensive hardware, centralized evaluation, or are limited in task diversity. We introduce VLA-REPLICA, a low-cost, easily reproducible real-world benchmark for evaluating VLA models. Built from off-the-shelf components, our system can be quickly assembled and replicated across laboratories, providing a consistent environment for policy evaluation anywhere in the world. VLA-REPLICA includes a diverse suite of manipulation tasks and a small-scale demonstration dataset for target-domain adaptation, with real-world evaluation protocols for both in-distribution and out-of-distribution settings. Experiments with imitation learning and state-of-the-art VLA models reveal model strengths and limitations, while consistent results across independently constructed setups demonstrate the reproducibility of our benchmark.

---

## 5. GaussianDream: A Feed-Forward 3D Gaussian World Model for Robotic Manipulation

**Authors:** Zijian Zhang, Yuqing Jiang, Qian Cheng, ..., Weitao Zhou, Haibao Yu
**arXiv:** [2605.20752](https://arxiv.org/abs/2605.20752)
**Categories:** Robotics (cs.RO)

Vision-language-action (VLA) policies have advanced language-conditioned robotic manipulation by transferring semantic priors from pretrained vision-language models to action generation. Yet, standard action-imitation training often provides limited explicit supervision for 3D geometry, dense visual structure, and short-horizon environment evolution, which are critical for physically precise manipulation. We introduce \textbf{GaussianDream}, a feed-forward 3D Gaussian world-model plug-in that turns robot trajectories into structured spatial-temporal supervision. The key idea is to couple current Gaussian reconstruction with horizon-conditioned future Gaussian prediction during training, forcing a compact spatio-temporal prefix to be decodable into renderable 3D Gaussian states. This enables dense RGB rendering, depth, and pseudo 3D scene-flow supervision without requiring test-time Gaussian decoding. At inference, GaussianDream discards all auxiliary decoding heads and retains only the learned prefix to condition action generation, avoiding rendering, video rollout, or additional planning during closed-loop control. Experiments on LIBERO, RoboCasa Human-50, and real-robot tasks demonstrate strong and highly competitive performance, achieving \textbf{98.4\%} average success on LIBERO, \textbf{52.6\%} on RoboCasa Human-50, and \textbf{50.0\%} in real-world evaluation.

---

## 6. DriveMA: Rethinking Language Interfaces in Driving VLAs with One-Step Meta-Actions

**Authors:** Weicheng Zheng, Yixin Huang, Qiao Sun, Derun Li, Hang zhao
**arXiv:** [2605.21273](https://arxiv.org/abs/2605.21273)
**Categories:** Computer Vision and Pattern Recognition (cs.CV)

Driving Vision-Language-Action Models (Driving VLAs) commonly introduce natural-language reasoning as an intermediate interface for end-to-end planning, but reasoning-centric interfaces face three practical bottlenecks: obtaining high-quality reasoning annotations is difficult, generating and understanding long reasoning chains is challenging for compact models, and inference latency is substantially increased. In this paper, we rethink the design of language interfaces in Driving VLAs and show that concise one-step meta-actions are a simple yet effective alternative to verbose reasoning. Meta-actions provide semantic decision grounding while remaining low-entropy, and being automatically derivable from expert trajectories, enabling scalable supervision and reliable trajectory conditioning. Building on this interface, we propose DriveMA, which combines action-centric supervised training with a turn-level credit-assignment reinforcement learning framework that jointly optimizes meta-action correctness, trajectory quality, and trajectory--meta-action consistency. Experiments show that DriveMA already achieves a new state of the art on the Waymo End-to-End Driving Challenge with a 2B model, reaching a Rater Feedback Score (RFS) of 8.060, while its 4B version further improves the state of the art to 8.079; DriveMA also obtains competitive performance on NAVSIM. Ablations demonstrate that one-step meta-actions offer a better practical trade-off between expressiveness, predictability, and inference efficiency than natural-language reasoning or finer-grained action sequences. Code, data, and models will be released to facilitate future research.

---

## 7. Distill to Think, Foresee to Act: Cognitive-Physical Reinforcement Learning for Autonomous Driving

**Authors:** Yang Wu, Qiang Meng, Zhaojiang Liu, ..., Jian Yang, Jin Xie
**arXiv:** [2605.21139](https://arxiv.org/abs/2605.21139)
**Categories:** Computer Vision and Pattern Recognition (cs.CV); Machine Learning (cs.LG)

Current end-to-end autonomous driving models are fundamentally constrained by the behavioral cloning ceiling of imitation learning. While reinforcement learning offers a path to smarter autonomy, it demands two missing pieces of infrastructure: (1) a cognitive foundation that understands traffic semantics and driving intent, and (2) a foresighted physical environment that can anticipate the consequences of candidate actions. To this end, we propose CoPhy, a CognitivePhysical reinforcement learning framework for autonomous driving. To distill to think, we distill VLM knowledge into the BEV encoder and then discard the VLM entirely, retaining cognitive ability at zero inference cost while releasing the cognitive channel as a pluggable interface for optional human language commands. To foresee to act, we build an auto-regressive BEV world model that explicitly predicts future semantic maps conditioned on candidate actions, serving as an interpretable physical sandbox from which safety metrics are directly derived. Built upon this dual infrastructure, we optimize the driving policy via GRPO with a novel dual-reward mechanism: a physical reward derived from BEV rollouts enforces hard safety constraints, while a cognitive reward from a language-aligned scorer ensures intent compliance. Extensive experiments demonstrate that CoPhy not only achieves state-of-the-art results on NAVSIM v1 and v2 benchmarks, but also enables safer driving via cognitively informed scene compliance and flexible intent control through user-defined language instructions.

---

## 8. Demo-JEPA: Joint-Embedding Predictive Architecture for One-shot Cross-Embodiment Imitation

**Authors:** Jingyang He, Guangrun Li, Jieyu Zhang, ..., Zhengping Che, Shanghang Zhang
**arXiv:** [2605.20811](https://arxiv.org/abs/2605.20811)
**Categories:** Robotics (cs.RO)

Robotic imitation learning is often treated as reproducing demonstrated actions, but actions are inherently embodiment-specific. When demonstrations come from humans or robots with different morphology, kinematics, or action spaces, this action-centric view requires shared action spaces, heuristic retargeting, or large-scale multi-embodiment co-training. We instead view demonstrations as implicit specifications of future goals: the target agent should infer what state the demonstrator is trying to realize, rather than how the demonstrator executes it. We propose Demo-JEPA, a cross-embodiment imitation framework that decouples demonstration intent from embodiment-specific execution. Built on a JEPA-based world model, Demo-JEPA translates source visual demonstrations into target-compatible future latent trajectories in a shared predictive representation space. The target agent then uses these latent trajectories as subgoals and realizes them through planning under its own learned forward dynamics. Because Demo-JEPA avoids action-level correspondence and requires only visual demonstrations plus the target agent's own interaction experience, it supports flexible imitation across heterogeneous embodiments. Experiments on RLBench and real-world manipulation tasks show that Demo-JEPA matches specialized in-domain planners and generalizes to unseen tasks and embodiment configurations where prior methods fail.

---
