# arXiv Daily Digest — 2026-10-05

**Mode:** direct
**Categories:** cs.AI, cs.LG, cs.RO, cs.CV
**Keywords:** VLA, RSI, agentic robot, self-improving robot, self-evolving robot, robot harness
**Papers found:** 10

---

## 1. Detect and Suppress: A Mechanistic Defense against Adversarial Patches in VLA Models

**Authors:** Yukiya Horiba, Koshiro Aoki, Shunsuke Yasuki, Bum Jun Kim, Taiki Miyanishi
**arXiv:** [2610.03498](https://arxiv.org/abs/2610.03498)
**Categories:** Robotics (cs.RO); Artificial Intelligence (cs.AI)

Adversarial patches can disrupt Vision-Language-Action (VLA) models by manipulating visual observations, leading to failures in robot control. However, it remains poorly understood which internal mechanisms underlie these failures and how targeted interventions can mitigate them. In this work, we mechanistically analyze VLA representations using a sparse autoencoder (SAE) and identify a feature whose activation strongly correlates with the presence of an adversarial patch. Based on this analysis, we suppress the identified feature at inference time only when a linear probe detects an attack. This intervention improves robustness without the cost of fine-tuning the VLA. We evaluate our method against VLA adversarial patch attacks on LIBERO-10. Conditional intervention improves success rate under intermittent attacks, whereas continuously applying the same intervention substantially degrades policy performance. These results show that attack-related internal representations can provide useful targets for VLA adversarial defense and that controlling when to intervene is important for limiting disruption to nominal policy behavior.

---

## 2. FastOPD: On-Policy Distillation for Lightweight VLA Deployment

**Authors:** Yoojin Oh, Jeongsol Kim, Yeonwoo Seo, ..., Kyumin Choi, Jong Chul Ye
**arXiv:** [2610.02832](https://arxiv.org/abs/2610.02832)
**Categories:** Robotics (cs.RO); Artificial Intelligence (cs.AI); Computer Vision and Pattern Recognition (cs.CV); Machine Learning (cs.LG)

Vision-Language-Action (VLA) foundation models have scaled rapidly to enhance manipulation performance and generalizability, but this scaling incurs high computational costs that render real-world deployment increasingly challenging. Existing approaches typically mitigate this issue by designing smaller architectures or reducing the iterative denoising steps in flow-based policies. In this work, we propose FastOPD, a foundation-to-lightweight VLA framework that enables the practical deployment of large-scale VLAs through efficient on-policy distillation. Specifically, FastOPD adapts a flow map for single-state teacher supervision and combines it with a self-consistency objective to construct a compact student that learns the teacher dynamics. Furthermore, we theoretically demonstrate that minimizing this objective allows the distilled student to recover a distribution on par with that induced by an ideal few-step teacher model. We evaluate FastOPD across diverse foundation policies in simulation and real-world experiments. On LIBERO, FastOPD retains 84% of the performance of $\pi_{0.5}$ with only two inference steps, reducing inference latency by 78.1% while outperforming existing few-step distillation baselines in average success rate. With LingBot-VLA as the teacher, FastOPD improves the single-step success rate over the base student by 15.9 percentage points on RoboTwin 2.0. We further demonstrate its applicability to a World Action Model (WAM) and deploy a compact student distilled from MolmoAct2 on a real robot.

---

## 3. MixVLA: Adaptive Mixing of Non-Invariant Information for Generalizable Vision-Language-Action Models

**Authors:** Pingrui Zhang, Yu Zhang, Pengyuan Wu, ..., Bin Zhao, Xuelong Li
**arXiv:** [2610.02898](https://arxiv.org/abs/2610.02898)
**Categories:** Robotics (cs.RO)

Vision-Language-Action (VLA) models have achieved remarkable advances in robotic manipulation, yet their zero-shot generalization under out-of-distribution (OOD) conditions remains limited. These models often entangle task-relevant invariant structure with environment-specific non-invariant factors, causing policies to rely on spurious appearance cues during action prediction. In this work, we propose \textbf{MixVLA}, a model-agnostic training framework that improves the generalization of VLA models without requiring additional OOD data or architectural modifications. The key component of MixVLA is \textbf{Adaptive Mixing of Non-Invariant Information (AMI)}. AMI stochastically mixes non-invariant representations to regularize distribution-specific variability while preserving complementary predictive cues. The mixed non-invariant features are then fused with invariant representations for final action prediction, resulting in improved robustness without sacrificing policy expressiveness. Extensive experiments across challenging manipulation settings, including LIBERO, LIBERO-Plus, the RoboTwin perturbation suite, and real-world tasks, demonstrate that MixVLA improves overall zero-shot robustness while retaining strong in-domain performance.

---

## 4. ManiPhysicsBench: Physics-Based Assessment of Object Preservation in VLA Manipulation

**Authors:** Sangwu Park, Yeonjun In, Wonjoong Kim, ..., Sein Kim, Chanyoung Park
**arXiv:** [2610.02802](https://arxiv.org/abs/2610.02802)
**Categories:** Robotics (cs.RO)

Vision-language-action (VLA) models aim to perform diverse manipulation tasks, but task success in existing rigid-body benchmarks does not indicate whether they preserve objects. We introduce ManiPhysicsZoo, which consolidates literature-supported material properties, 3D meshes, and supporting references into reusable object assets. Using these assets, a solver-based assessment computes grasp-specific damage thresholds from object geometry, material properties, and recorded grasp conditions and compares them with recorded contact forces to assess potential deformation and fracture. Building on these components, ManiPhysicsBench evaluates object preservation in LIBERO and SimplerEnv across three physics axes and three difficulty levels. Public VLA checkpoints show a substantial gap between task success and safe success, defined as task completion while preserving the object. Their gripper commands concentrate near full opening and closure, with largely similar aggregate distributions across objects, consistent with binary gripper supervision. We examine how object-specific continuous gripper labels change model behavior by retraining a VLA model. The retrained model shows more object-dependent gripping and higher safe success, but lower task success and limited generalization of object-preserving behavior.

---

## 5. SimpleTouch: Can Vision-Language-Action Models Master Contact-Rich Manipulation Without Tactile Policy Pretraining?

**Authors:** Chen Yang, Linzhe Shi, Changjie Wu, ..., Jiansheng Fan, Chen Wang
**arXiv:** [2610.02784](https://arxiv.org/abs/2610.02784)
**Categories:** Robotics (cs.RO)

Tactile sensing provides essential contact information for robotic manipulation, yet incorporating it into pretrained vision-language-action (VLA) models remains challenging. A common concern is that simply introducing touch during task-specific fine-tuning may fail to bridge the cross-modal gap, yielding limited gains or even reduced success. Consequently, existing methods often rely on large-scale tactile policy pretraining or separate visuotactile alignment, adding data requirements and training stages. We introduce SimpleTouch, a simple VLA extension that augments $\pi_{0.5}$ with a tactile expert, to test whether these additional stages are necessary. Leveraging all tokens from a frozen pretrained tactile encoder, the expert learns from action supervision and multi-horizon prediction of future tactile latents. This single-stage training uses only task demonstrations, without additional tactile policy pretraining or separate alignment. With 50 demonstrations per task, SimpleTouch achieves the highest success rate among evaluated methods on all six UniVTAC tasks. Its average success rate reaches 77.5%, compared with 45.2% for FTP-$\pi_{0.5}$ and 66.7% for FTP-1, corresponding to gains of 32.3 and 10.8 percentage points, respectively. Across four real-world tasks, it averages 71.3%, exceeding FTP-1 by 8.8 percentage points. These results demonstrate that, given pretrained VLA and tactile representations, additional tactile policy pretraining is not a prerequisite for strong performance on these tasks, offering a simpler route to contact-rich manipulation. Project page: this https URL

---

## 6. SocialVLA: A Social Perception Gateway for Human-Reaction-Based Failure Detection and Recovery in VLA Manipulation

**Authors:** Sofya Konstantinova, Miguel Altamirano Cabrera, Artem Lykov, Dzmitry Tsetserukou
**arXiv:** [2610.02360](https://arxiv.org/abs/2610.02360)
**Categories:** Robotics (cs.RO)

Vision-language-action (VLA) policies enable diverse robotic manipulation but can fail during execution without recognizing their own errors. Human observers provide complementary signals, as unexpected robot behavior can trigger rapid vocal, facial, or verbal reactions before failure is completed. We introduce SocialVLA, a local, policy-agnostic social perception gateway that converts spontaneous human reactions into runtime intervention signals for VLA manipulation. SocialVLA combines causal paralinguistic audio detection, visual reaction recognition, explicit stop phrases, and robot-relevance estimation. An asynchronous first-event fusion mechanism triggers a VLA hold from the earliest sufficiently confident signal, while a separate speech channel captures verbal corrections for participant-directed continuation, restart, or instruction revision. We evaluate SocialVLA on physical Unitree G1 manipulation using 15 participants, with 238 annotated intervention-worthy episodes and 1.038 h of non-intervention behavior. Frozen offline replay achieves 54.6% recall and 69.5% precision, while unfiltered audio-video fusion reaches 64.3% recall. Relevance estimation reduces false-stop episodes from 100 to 57 and increases precision from 60.5% to 69.8%. In prospective deployment on an unseen 16th participant, the frozen system achieves 59.5% recall and 91.7% precision. Median detector-to-fusion latency is 47.9 ms, VLA-gate-to-physical-hold latency is 336 ms, and reaction-onset-to-hold latency is 1.021 s. These results demonstrate a complete local pathway from spontaneous social reaction to physical VLA interruption and participant-directed recovery.

---

## 7. World-Calibrated Proposal-to-Action Flow for Vision-Language-Action Models

**Authors:** Jie He, Wei Li, Junwen Tong, ..., Wei-Shi Zheng, Liqiang Nie
**arXiv:** [2610.02323](https://arxiv.org/abs/2610.02323)
**Categories:** Robotics (cs.RO); Computer Vision and Pattern Recognition (cs.CV)

Flow-based Vision-Language-Action (VLA) policies generate action chunks by transporting samples from a task-agnostic isotropic Gaussian source. As this source is conditioned on neither recent execution nor predicted future evolution, (i) it discards the local continuity established by recently executed motion. (ii) Even when predictive world representations are introduced, they often only condition the transport dynamics rather than determine where generation starts, how far it may deviate, or along which action directions it may expand. Building on this observation, we introduce ProAct, a world-calibrated proposal-to-action framework that makes the generative source itself predictable. (i) To preserve motion continuity, a lightweight Proposal Expert converts recent actions into a scene-aware hypothesis via one motion-anchored endpoint flow-matching step, initializing generation near the demonstrated action manifold. (ii) To jointly capture intended scene evolution and proposal-future compatibility, a prospective World Expert treats the hypothesis as a soft motion prior while predicting the task-consistent latent future. (iii) From this compatibility, the model calibrates a proposal-centered anisotropic source, where a bounded per-step extent controls the allowed deviation and a trace-normalized low-rank geometry under a condition-number budget allocates refinement over coupled translation, rotation, and gripper directions. Compared with $\pi_{0.5}$, ProAct improves performance across simulation and real-world tasks while reducing denoising steps by 50%, inference latency by up to 25.8%, and increasing throughput by up to 34.8%.

---

## 8. CHASE-VLA: Post-Training Quantization Framework for Vision-Language-Action Models with Chunk-Aware Scale Estimation

**Authors:** Jin Hyun, Jung Gyu Min, Gyuhyun Jung, Youngjoo Lee
**arXiv:** [2610.02666](https://arxiv.org/abs/2610.02666)
**Categories:** Computer Vision and Pattern Recognition (cs.CV)

Vision-Language-Action (VLA) models map visual observations and language instructions to continuous robot actions, but a diffusion-based action expert (AE) poses a key challenge for low-bit post-training quantization (PTQ). The AE is repeatedly invoked across denoising steps and policy queries, where fixed calibration scales can be mismatched with activation ranges that vary with denoising progress and intended motion. We propose CHASE-VLA, a chunk-aware PTQ method that exploits a VLA-specific signal readily available from the policy: the generated action chunk, including its unexecuted future suffix. Rather than relying only on static scale matching for AE layers, CHASE-VLA combines the previously generated chunk as causal action context with denoising step group information to adapt AE activation scales. This enables W4A4 quantization of both MLP and attention projections in the repeated AE without modifying the pretrained policy. On LIBERO, CHASE-VLA achieves 97.3% average success rate on $\pi_{0.5}$ when both MLP and attention projections in the AE are quantized to W4A4, restoring FP16-level performance. CHASE-VLA also reduces the weight storage of the quantized AE linear layers by 73.4% and their single-chunk memory traffic by 70.9% and 71.2% on $\pi_{0.5}$ and GR00T N1.6, respectively, with a predictor overhead of at most 1.26% of the saved storage.

---

## 9. Imagine the Future, Internalize the Gist: Efficient VLA Reasoning via Internalized Spatiotemporal Imagination

**Authors:** Shenglan Li, Zhendong Mi, Hengyi Zhu, ..., Pu Zhao, Shaoyi Huang
**arXiv:** [2610.02626](https://arxiv.org/abs/2610.02626)
**Categories:** Computer Vision and Pattern Recognition (cs.CV)

Vision-language-action (VLA) models increasingly incorporate intermediate reasoning to improve robotic manipulation, yet existing approaches primarily reason about observed states without explicitly anticipating future scene evolution. Extending such reasoning to explicit future rollouts at every inference step, however, introduces substantial computational overhead. We propose IG-VLA, a VLA reasoning framework that enables models to imagine the future and internalize the gist. Our Latent Spatiotemporal Reasoning learns to imagine task-relevant future scene evolution directly in visual representation space, guiding action prediction without costly pixel-level video generation. To further reduce inference overhead, we introduce Scene Gist Memory, which internalizes reasoning-derived scene-behavior associations into a compact Scene Gist Token, preserving the benefits of future reasoning while bypassing explicit future imagination at inference. Extensive experiments on LIBERO, LIBERO-Plus, and VLABench demonstrate the effectiveness and efficiency of IG-VLA. On the LIBERO-Plus Language suite, both the reasoning and gist policies outperform the strongest baseline by nearly 6% in success rate. The gist policy also achieves up to 6.38x speedup over baselines, reducing inference latency from 1081ms to 169.5ms per action chunk on a single NVIDIA A6000 GPU. These results demonstrate that future spatiotemporal reasoning can be effectively internalized for efficient VLA deployment.

---

## 10. Recursive Self-Improvement in Unified Multimodal Models

**Authors:** Huijuan Wang, Chufan Shi, Cheng Yang, ..., Taylor Berg-Kirkpatrick, Xuezhe Ma
**arXiv:** [2610.03002](https://arxiv.org/abs/2610.03002)
**Categories:** Computation and Language (cs.CL); Computer Vision and Pattern Recognition (cs.CV)

Unified multimodal models (UMMs) understand and generate both text and images, which lets a model produce its own training data. Existing self-improvement in UMMs keeps supervision on the visual side, where image understanding judges image generation. We propose recursive cross-capability self-improvement (RSI), a training loop in which the text and visual abilities of a UMM supply training data for one another. In each round, the model generates images and reads them to find where it falls short. It then writes programs aimed at these shortcomings, and execution verifies every result against its specification. Verified renders train image generation, while labeled renders and the model's own correct programs train visual understanding and program writing. Program execution thus acts as a source of truth outside the model, so errors do not accumulate across rounds. We study RSI on charts and build BasicChartBench to evaluate open models early in training. On requests worded differently from training, four rounds of RSI raise the score from 45.7% to 60.2%, while continued training stays at 46.3%. Verified construction carries most of the gain, and targeting the model's failures adds 3.5%. Along the way, the share of verified programs rises from 48.9% to 95.2%, and the reader's accuracy on edited renders rises from 55.6% to 87.4%.

---
