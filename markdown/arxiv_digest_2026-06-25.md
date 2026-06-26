# arXiv Daily Digest — 2026-06-25

**Mode:** direct
**Categories:** cs.AI, cs.LG, cs.RO, cs.CV
**Keywords:** VLA, world model, world action model
**Papers found:** 14

---

## 1. FORCE: Efficient VLA Reinforcement Fine-Tuning via Value-Calibrated Warm-up and Self-Distillation

**Authors:** Shuyi Zhang, Yunfan Lou, Hongyang Cheng, ..., Zhongyuan Wang, Shanghang Zhang
**arXiv:** [2606.26006](https://arxiv.org/abs/2606.26006)
**Categories:** Robotics (cs.RO); Artificial Intelligence (cs.AI)

Vision-Language-Action (VLA) models are often constrained by the imitation ceiling imposed by sub-optimal data. While Reinforcement Learning (RL) fine-tuning can surpass this limit, it is notoriously sample inefficient. This challenge arises from two core issues: (1) catastrophic initial unlearning due to an unstable Q-function and (2) inefficient policy updates caused by low-quality exploration data, often forcing a reliance on costly human interventions. We introduce FORCE, a 3-stage framework that stabilizes fine-tuning by tackling both issues. FORCE first incorporates a Value-Calibrated Warm-Up phase, utilizing on-policy rollouts to mitigate the distributional shift of the Q-function. Subsequently, during the online stage, this calibrated Q-function acts as a filter for both the policy's own action proposals and expert data, ensuring only high-value actions are used for the policy update. We evaluate FORCE on various simulation and real-world tasks, and the result shows that FORCE achieves a 79% absolute improvement in success rates and outperform prior RL methods by 10%, while accelerating training by 32.5%. Critically, it mitigates the common success rate drop and achieves this robust performance without human intervention, marking a significant step towards deploying capable and autonomous robotic agents.

---

## 2. ROAD-VLA: Robust Online Adaptation via Self-Distillation for Vision-Language-Action Models

**Authors:** Kejing Wang, Toan Nguyen, Minh Hoang Nguyen, Simon Khan, Flora D. Salim
**arXiv:** [2606.25800](https://arxiv.org/abs/2606.25800)
**Categories:** Machine Learning (cs.LG); Robotics (cs.RO)

Effective online adaptation of vision-language-action (VLA) models remains challenging, as sparse rewards provide weak supervision for high-dimensional autoregressive action policies. Although self-distillation can in principle provide denser training signals, we find that text-based privileged teachers conditioned on demonstrations, retrieved experiences, or high-level plans are ineffective for VLA adaptation, exposing a modality gap between symbolic guidance and low-level robot actions. We propose ROAD-VLA, an advantage-guided self-distillation framework that constructs a proximal teacher directly in action space by perturbing action-token logits with calibrated advantage estimates. This converts sparse rewards into dense token-level supervision while keeping the teacher close to the current policy. We further derive a policy-improvement lower bound under calibrated advantages and accurate teacher matching. Across seven robotic manipulation environments with in-distribution and out-of-distribution shifts, ROADVLA outperforms PPO in nearly all settings, demonstrating robust online VLA adaptation.

---

## 3. Conformal Orbit-Valid Trust Horizons for Equivariant World Models

**Authors:** Hongbo Wang
**arXiv:** [2606.24946](https://arxiv.org/abs/2606.24946)
**Categories:** Machine Learning (cs.LG); Robotics (cs.RO)

Learned world models are useful only over horizons on which their rollout error remains controlled. We study trust-horizon certification for latent world models with known group symmetries. Given a one-step latent residual and a finite-time expansion estimate, we form a raw horizon curve and calibrate it with a split-conformal multiplicative factor. On the reproducible audit set, the conformal factor is $\gamma_\alpha=1.0$: the raw certificate is already conservative under the audit protocol. Across 50 stable audits, we observe zero anti-conservative violations, corresponding to an exact-binomial 95% upper bound of 5.8% on the violation rate. Our main structural result is that exact equivariance transports a calibrated trust-horizon curve over the group orbit: when the environment dynamics, encoder, predictor, action transform, and latent metric satisfy the stated equivariance/invariance conditions, rollout errors and trust horizons are orbit-constant. Empirically, the implemented models exhibit small orbit-transport residuals, with median 1.1% and maximum 4.1% over 14 orbit audits. The certificate is also non-vacuous (median certified-to-measured horizon ratio 0.67). A certificate-level calibration-cost study shows two complementary regimes. On a symmetric 2D substrate, equivariant, plain, and augmented models are all orbit-valid from a single calibration sector -- no separation, because the substrate already makes non-equivariant baselines approximately orbit-robust. A 3D yaw audit shows the other regime: the equivariant model obtains a one-sector safe and non-vacuous orbit-valid certificate, while healthy non-equivariant baselines pay violation, slack, sharpness, or additional-sector cost. The certificate is a conservative, distributional audit rather than a global reachability guarantee, and certificate-guided subgoal spacing is not confirmed in the current 3D CEM-MPC behavior layer.

---

## 4. When Do Conservation Laws Survive Learned Representations? Certified Horizons for Latent World Models

**Authors:** Hongbo Wang
**arXiv:** [2606.24945](https://arxiv.org/abs/2606.24945)
**Categories:** Machine Learning (cs.LG); Robotics (cs.RO)

We ask a representation-learning question about physical world models: when does a conservation law remain certifiable after a model learns a latent representation? A certified horizon bounds -- in advance, from measurable model defects -- how many steps a rollout provably stays on a physical invariant's level set. The key design choice is what is certified: not a learned latent Hamiltonian or a learned scalar witness (a model can conserve either while drifting in true energy), but the decoded physical invariant obtained by decoding the latent state and evaluating the known invariant. Around this object we derive shell-horizon certificates whose budget decomposes into representation, readout, and latent-dynamics defects, with a monotone alignment bridge through which a soft learned witness yields a certified horizon for the decoded invariant, and test them across state, learned-lift, and pixel observations on conservative systems. Conservation certificates can survive learned representation, but not all geometric priors survive equally: hard canonical symplectic structure yields the longest horizons in known phase coordinates yet does not cross a learned chart, whereas a controlled-Lipschitz-aligned soft invariant survives in the learned-representation settings we test; pixel certification is recovered on a readout-stable sub-tube; and the Kepler problem exposes a geometric boundary. The central object is therefore not a latent Hamiltonian, but a decoded physical invariant whose robustness to representation learning can be measured, certified, and falsified.

---

## 5. Causal-rCM: A Unified Teacher-Forcing and Self-Forcing Open Recipe for Autoregressive Diffusion Distillation in Streaming Video Generation and Interactive World Models

**Authors:** Kaiwen Zheng, Guande He, Min Zhao, ..., Jun Zhu, Qianli Ma
**arXiv:** [2606.25473](https://arxiv.org/abs/2606.25473)
**Categories:** Computer Vision and Pattern Recognition (cs.CV); Machine Learning (cs.LG)

Autoregressive video diffusion with causal diffusion transformers has emerged as a major paradigm for real-time streaming video generation and action-conditioned interactive world models. In this work, we extend rCM, an advanced diffusion distillation framework, to autoregressive video diffusion. The core philosophy of rCM lies in the complementarity between forward and reverse divergences, represented by consistency models (CMs) and distribution matching distillation (DMD), respectively, in diffusion distillation. This philosophy naturally carries over to the autoregressive setting, where teacher-forcing (TF) provides an offline, forward-divergence causal training paradigm, while self-forcing (SF) corresponds to an on-policy, reverse-divergence refinement.
Our contributions are: (1) through extensive experiments, we show that teacher-forcing CM is currently the best complement to self-forcing DMD as an initialization strategy (2) we present the first implementation of teacher-forcing-based continuous-time CMs (e.g., sCM/MeanFlow) for autoregressive video diffusion, enabled by our custom-mask FlashAttention-2 JVP kernel, achieving 10$\times$ faster convergence compared to discrete-time CMs (dCMs) (3) we introduce Causal-rCM, a leading, unified, and scalable algorithm-infrastructure open recipe for diffusion distillation and causal training (4) we achieve state-of-the-art streaming video generation performance in both frame-wise and chunk-wise settings, using only synthetic data for training.
Notably, our distilled 2-step causal Wan2.1-1.3B model achieves a VBench-T2V score of 84.63 with only 1 or 2 sampling steps. We further apply Causal-rCM to Cosmos 3, an advanced omnimodal world foundation model for physical AI with action-conditioned generation capability, enabling an interactive world model.

---

## 6. In-Context World Modeling for Robotic Control

**Authors:** Siyin Wang, Junhao Shi, Senyu Fei, ..., Jingjing Gong, Xipeng Qiu
**arXiv:** [2606.26025](https://arxiv.org/abs/2606.26025)
**Categories:** Robotics (cs.RO); Computer Vision and Pattern Recognition (cs.CV)

Modern Vision-Language-Action (VLA) models often fail to generalize to novel setups, such as altered camera viewpoints or robot morphologies, because they are typically conditioned only on current observations and language instructions. By ignoring the underlying system configuration as a variable, these models implicitly assume a fixed execution context encountered during training, necessitating data-intensive fine-tuning for any new environment. In this work, we introduce In-Context World Modeling (ICWM), a framework that treats system identification as an in-context adaptation problem. ICWM enables robot policies to autonomously infer essential system variables from a short history of self-generated, task-agnostic interactions. Unlike traditional In-Context Learning that uses demonstrations to specify what task to perform, ICWM leverages the context window to understand how the system operates. By processing these interactions before task execution, the model implicitly captures the world dynamics of the current system, enabling adaptation to novel configurations without parameter updates. Extensive experiments in simulation and on real-world robot platforms demonstrate that ICWM significantly outperforms standard VLA baselines on novel camera viewpoints.

---

## 7. Action ControlNet: A Lightweight Delay-Aware Adapter for Smooth Asynchronous Control in Vision-Language-Action Models

**Authors:** Tiecheng Guo, Meng Guo
**arXiv:** [2606.25985](https://arxiv.org/abs/2606.25985)
**Categories:** Robotics (cs.RO)

Vision-language-action (VLA) models have shown strong potential for general-purpose robot manipulation, but their inference latency remains a major obstacle to stable high-frequency control. Asynchronous execution mitigates this bottleneck by overlapping policy inference with action execution, yet the next action chunk is still predicted from stale observations while the robot continues to move. Direct chunk stitching therefore introduces handoff discontinuities, action jitter, and failures in contact-rich manipulation. Existing remedies typically require either full-policy retraining or architecture-specific runtime logic. This work proposes Action ControlNet (ACNet), a lightweight delay-aware adapter that uses the executed motion suffix as a residual condition for a mostly frozen action head. ACNet leaves the pretrained backbone unchanged, introduces few trainable parameters, and remains compatible with generative action heads such as diffusion and flow matching. On Kinetix, Meta-World MT50, and a real-world SO-ARM101 platform, ACNet improves robustness under inference delay and yields smoother asynchronous trajectories than direct chunk stitching, while remaining more lightweight than full delay-conditioned retraining.

---

## 8. WOLF-VLA: Whole-Body Humanoid Optimal Locomotion Framework for Vision-Language-Action Learning

**Authors:** Melya Boukheddimi, Omar Adjali, Daniel Sontag, Frank Kirchner
**arXiv:** [2606.25591](https://arxiv.org/abs/2606.25591)
**Categories:** Robotics (cs.RO)

Vision-Language-Action (VLA) models have recently demonstrated strong generalization in robotic manipulation, yet their applicability to whole-body, contact-rich humanoid locomotion remains severely underexplored due to data scarcity, the absence of dynamically consistent demonstrations, and the difficulty of encoding optimality and safety in learning-based pipelines. This work introduces a unified framework WOLF-VLA that integrates whole-body optimal-control (OC) motion synthesis with large-scale multi-modal dataset to train VLAs capable of generating humanoid locomotion policies directly from natural-language instructions. We construct a comprehensive dataset of dynamically feasible humanoid trajectories across six locomotion-related task families, each parameterized by environmental variations, object colors, placements, and visual distractors. We train a VLA model using the collected joint trajectories, ego-centric visual observations and natural language instruction, yielding a policy that exhibits strong reasoning and robustness to initial-condition variability, and competitive performance across several tasks and environment settings. A systematic ablation study demonstrates the impact of each modality on the model performance. The full dataset, model checkpoints, and benchmarking simulation suite will be openly released, establishing a reproducible dynamically consistent benchmark for whole-body humanoid locomotion rich VLA control and enabling future research in scalable transfer of instruction-driven locomotion policies.

---

## 9. Reflective VLA: In-Context Action Consequences Make VLAs Generalize

**Authors:** Qing Lian, Kent Yu, Lei Zhang
**arXiv:** [2606.25215](https://arxiv.org/abs/2606.25215)
**Categories:** Computer Vision and Pattern Recognition (cs.CV); Robotics (cs.RO)

Most vision-language-action (VLA) models are reactive: they predict the next action from the current instruction and observation, implicitly assuming that the current observation fully specifies the action-relevant state. In embodied control, however, embodiment-specific factors such as camera-to-robot geometry, robot calibration, or systematic actuation bias are often hard to identify from a single observation. As a result, reactive policies cannot reliably disambiguate these factors in general, overfitting to training environments and generalizing poorly at deployment. We propose Reflective VLA, which conditions each decision on a context of observation-action-consequence triplets. Each triplet records not only what the robot observed and executed, but also how the scene changed afterward, exposing the deployment-specific mapping from actions to observed effects. Architecturally, Reflective VLA routes all observation modalities through the VLM under shared attention, so the action expert reasons directly over past triplets and the current observation. A block-causal mask enables parallel multi-frame training without leakage and supports KV-cached real-time inference. On standard LIBERO and SimplerEnv-Bridge, Reflective VLA preserves strong in-distribution performance. Under distribution shift on LIBERO-Plus and the harder LIBERO-Plus-Hard, it improves average success rate by 5.4 and 4.2 percentage points over a matched reactive baseline. Ablations with a matched history-only baseline further show that action consequences -- rather than additional context length alone -- are the key to cross-environment generalization. Project page: this https URL

---

## 10. MANGO: Automated Multi-Agent Test Oracle Generation for Vision-Language-Action Models

**Authors:** Pablo Valle, Shaukat Ali, Aitor Arrieta, Lionel Briand
**arXiv:** [2606.24815](https://arxiv.org/abs/2606.24815)
**Categories:** Software Engineering (cs.SE); Robotics (cs.RO)

Vision-Language-Action (VLA) models are emerging robotic control systems that integrate perception, language understanding, and action generation in a unified architecture. Existing testing approaches for VLA-enabled robots rely on manually constructed symbolic test oracles that determine task success from final environment states. These oracles are costly to construct, require domain expertise, and are often tightly coupled to specific tasks and environments, limiting scalability and reuse. Furthermore, they provide only end-state assessments of task outcomes, offering limited insight into intermediate behavior and fault localization. To address these limitations, we introduce MANGO, a multi-agent framework that automatically generates fine-grained oracles from natural-language descriptions of robotic tasks. MANGO first generates a reusable library of atomic tasks, then generates simulator-grounded oracle definitions for each atomic task, and finally produces executable fine-grained oracles by decomposing complex instructions into ordered sequences of atomic actions and corresponding oracles. The framework uses collaborative Generator, Assessor, and Judge agents that iteratively refine generated artifacts through structured feedback. We evaluate MANGO on the LIBERO_10 and RoboCasa Humanoid Tabletop benchmarks. Results show that MANGO generates executable, fine-grained oracles that detect a similar number of failures as symbolic oracles while accurately localizing them and providing richer diagnostic information. Through ablation studies, we further analyzed component contributions and the effect of initial task set, while preserving oracle quality. Overall, the results show the feasibility and effectiveness of test oracle generation for VLA-enabled robots testing.

---

## 11. Hypergraph Normal World Models for Logical Visual Anomaly Detection

**Authors:** Weizhi Nie, Zibo Xu, Weijie Wang, Yuting Su
**arXiv:** [2606.25368](https://arxiv.org/abs/2606.25368)
**Categories:** Computer Vision and Pattern Recognition (cs.CV)

Visual anomaly detection is often deployed with only normal training images. Most one-class detectors map test patches or features to a normal reference distribution. This works well for local structural defects. Logical anomalies are different. Each visible part may look normal, while the whole image violates a normal count, co-occurrence, or spatial relation. This paper studies whether a model can learn such a category-specific normal world from nominal images alone. We propose the Hypergraph Normal World Model, a normal-only detector that distills frozen DINOv2 patch tokens into patch, relation, and hypergraph statistics. It builds spatial hyperedges over token groups. It then scores each test image with an information quotient that separates local, relational, hyperedge, and hyperedge-relation evidence. On the available MVTec LOCO breakfast-box validation data, the full hypergraph model improves logical anomaly AUROC from 0.8434 for DINOv2 patch-kNN to 0.9279. It also improves over the non-hypergraph variant, from 0.9013 to 0.9279. Few-shot experiments show that the model remains effective with very limited normal images. We also test whether the score reflects normal-world knowledge rather than a shallow mapping. t-SNE separates logical anomalies in the learned energy space. Relation counterfactuals increase the information quotient by 83.13 on average. Random hypergraphs reduce logical AUROC, and hyperedge attribution is much larger on logical anomalies. Qualitative examples show that high scores are driven by relation-bearing terms. These results suggest that logical visual anomaly detection should model normal relations, not only normal local patches.

---

## 12. Learning Action Priors for Cross-embodiment Robot Manipulation

**Authors:** Dong Jing, Tianqi Zhang, Jiaqi Liu, ..., Zhiwu Lu, Mingyu Ding
**arXiv:** [2606.26095](https://arxiv.org/abs/2606.26095)
**Categories:** Robotics (cs.RO); Artificial Intelligence (cs.AI); Computer Vision and Pattern Recognition (cs.CV)

Most Vision-Language-Action (VLA) models build on a Vision-Language Model (VLM) backbone by attaching an action module and optimizing the full policy jointly. This design inherits strong visual and linguistic priors from the VLM, but leaves the action module to learn physical motion almost from scratch. As a result, the policy lacks an explicit motion prior, forcing early optimization to simultaneously discover temporal action dynamics and cross-modal alignment, a challenge further amplified in cross-embodiment settings. In this work, we propose to pretrain the action module with motion priors before cross-modal VLA alignment. Specifically, we introduce a two-stage training framework that equips the action module with cross-embodiment temporal motion structure before VLA training begins. In Stage~1, a lightweight flow-matching-based encoder-decoder action module efficiently learns temporal motion structure solely from unconditioned action trajectories, without processing visual or language tokens. In Stage~2, this learned prior is transferred to VLA training through decoder reuse and early-stage latent distillation, aligning visual-language features with the action embedding space while still allowing end-to-end policy refinement. In addition, the trained encoder serves as a compact history compressor, summarizing state-action histories into a single temporal context token for history-aware modeling at negligible cost. Extensive experiments across 13 diverse cross-embodiment tasks on both simulated and real-world platforms validate the effectiveness of our approach. Compared with VLA training without action priors, our model achieves faster convergence, higher success rates, and substantially stronger performance on data-scarce real-world tasks. Moreover, scaling up the action data in Stage~1 yields a more generalizable action prior that directly improves downstream VLA performance.

---

## 13. Decoupling Semantics and Geometric Grounding: Spatial Visual Prompts for Language-Conditioned Imitation Learning

**Authors:** Yanzhe Tang, Xinyu Shao, Yuxuan Hu, ..., Xiu Li, Long Zeng
**arXiv:** [2606.25360](https://arxiv.org/abs/2606.25360)
**Categories:** Robotics (cs.RO)

While end-to-end Vision-Language-Action (VLA) models show promise in robotic manipulation, their monolithic paradigm inherently couples semantic reasoning and spatial control. This creates a severe alignment bottleneck, limiting precise target disambiguation in data-constrained imitation learning. To overcome this, we propose SVP-IL, a decoupled architecture that explicitly extracts spatial visual grounding from the action generation loop. By leveraging vision-language foundation models, we parse instructions into zero-shot geometric masks, translating language into explicit Spatial Visual Prompts (SVP). These priors are injected into a continuous action generator via a lightweight direct feature-level fusion mechanism. This integration provides explicit and uncorrupted spatial gradient guidance while ensuring highly stable optimization under low-data regimes. Extensive experiments demonstrate that SVP-IL significantly outperforms state-of-the-art VLAs and pure visuomotor baselines. Trained on as few as 50 to 100 demonstrations, SVP-IL improves average success rates on highly ambiguous language-conditioned tasks from 24.0% to 39.5%, achieving 67.8% on standard benchmarks. Real-world robotic experiments further validate its robustness and data efficiency in unstructured physical environments.

---

## 14. USS: Unified Spatial-Semantic Prompts for Embodied Visual Tracking with Latent Dynamics Learning

**Authors:** Yuchen Xie, Xinyu Zhou, Kuangji Zuo, ..., Boyu Ma, Jianfei Yang
**arXiv:** [2606.25880](https://arxiv.org/abs/2606.25880)
**Categories:** Computer Vision and Pattern Recognition (cs.CV)

Embodied Visual Tracking (EVT) requires an agent to continuously follow a specified target while actively moving through dynamic environments. However, prevailing EVT paradigms predominantly rely on language-based target indication. While language is expressive and convenient, cluttered scenes often contain multiple objects that satisfy the same semantic description, leading to ambiguous target grounding. We therefore propose a paradigm shift, reframing target indication in EVT from text-only specification to unified spatial-semantic prompting. Based on this paradigm, we introduce Unified Spatial-Semantic Prompts for Embodied Visual Tracking with Latent Dynamics Learning, USS, an end-to-end embodied tracking framework that supports text, point, bounding box, and mask prompts within a unified architecture. USS encodes heterogeneous prompts with modality-specific encoders, fuses prompt tokens with visual features through hybrid attention, and decodes compact prompt-conditioned representations into egocentric waypoints. To further improve temporal robustness, USS incorporates a latent world model that predicts future representations through self-supervised alignment. Real-robot experiments demonstrate that explicit spatial target cues yield higher success rates than text-only prompts, particularly in scenarios involving similar distractors and longer-horizon tracking where maintaining instance-level target identity is critical. In the simulation benchmark, USS also achieves state-of-the-art performance among non-MLLM-based methods and competitive results against recent MLLM-based approaches with faster inference speed. Our findings reveal that spatial-semantic prompting provides a more precise and flexible target indication interface for embodied visual tracking. Project site: this https URL.

---
