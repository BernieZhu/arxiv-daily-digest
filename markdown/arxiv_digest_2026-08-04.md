# arXiv Daily Digest — 2026-08-04

**Mode:** direct
**Categories:** cs.AI, cs.LG, cs.RO, cs.CV
**Keywords:** VLA, world model, world action model
**Papers found:** 30

---

## 1. Faster-WAM: Do World Action Models Need Deep Action Modules?

**Authors:** Liheng Ma, Rui Heng Yang, Zhanguang Zhang, ..., Tongtong Cao, Yingxue Zhang
**arXiv:** [2608.02365](https://arxiv.org/abs/2608.02365)
**Categories:** Artificial Intelligence (cs.AI); Machine Learning (cs.LG); Robotics (cs.RO)

World Action Models (WAMs) couple robot action prediction with video world models. Existing WAMs with shared-backbone and Mixture-of-Transformers designs generally tie the depth of the action module to that of the video backbone, resulting in substantial computational overhead and high inference latency. To address this limitation, we introduce Dock of Transformer (DoT), a video-centric design principle that treats a pretrained video Transformer as a representation hub and connects lightweight output-heads through docking interfaces. This enables flexible output-head design while providing direct access to representations from all layers of the backbone. We then introduce \textbf{Faster-WAM}, an instantiation of DoT for WAMs, which docks a single-layer action head onto a 30-layer video backbone. The docking interface fuses keys and values from all video layers and applies RoPE realignment. Without additional embodied pretraining, Faster-WAM achieves competitive performance on LIBERO and RoboTwin 2.0 while demonstrating strong out-of-distribution generalization on LIBERO-Plus. Faster-WAM also achieves the lowest end-to-end latency in our controlled comparison, requiring only 66.5 ms per inference --- a \(3.2\times\) speedup over Fast-WAM. Overall, these results demonstrate that the video-centric DoT architecture supports flexible task-specific head design while delivering low inference latency, strong action-prediction performance, and robust generalization.

---

## 2. ProWorld: Progress-Aware Hyperbolic World Models for Long-Horizon Visual Goal Reaching

**Authors:** Zihan Liu, Yuzhe Zhuang, Yuanzu Li, ..., Min Zhou, Menglin Yang
**arXiv:** [2608.01926](https://arxiv.org/abs/2608.01926)
**Categories:** Artificial Intelligence (cs.AI)

JEPA-style visual world models offer an effective paradigm for visual goal planning by predicting future latent representations. Existing methods typically learn local transition consistency through next-step representation prediction. However, in long-horizon tasks, accurate local prediction alone need not ensure sustained progress toward the goal. First, multi-step rollouts can remain locally plausible while drifting away from goal-relevant trajectories. Second, locally similar future states can correspond to substantially different long-term progress, making them difficult to distinguish in a latent space optimized mainly for local consistency. To address these challenges, we introduce goal-conditioned progress order, a relative ordering of states according to how they advance toward a given goal. This order exhibits an asymmetric, coarse-to-fine structure: early states retain broader future possibilities, while later states concentrate on more specific goal-relevant regions. Such a structure is well suited to hyperbolic geometry. Motivated by this observation, we propose ProWorld, a progress-aware hyperbolic visual world model. ProWorld leverages goal-conditioned progress order to organize visual latent-space dynamics, maintains directional progress within trajectories via hyperbolic entailment learning, and mitigates progress ambiguity among locally similar future states via hyperbolic future discrimination. Furthermore, we design a progress-aware planning objective that scores candidate rollouts by jointly considering proximity to the goal and sustained progress across intermediate states. Experiments on four visual goal-reaching tasks demonstrate that ProWorld achieves an average absolute success-rate gain of 9.67 over LeWM. The code will be released after the paper is accepted.

---

## 3. Why Does the Future Branch? Identifiable Closure Tests for Stochastic Physical World Models

**Authors:** Yibin Dong
**arXiv:** [2608.00591](https://arxiv.org/abs/2608.00591)
**Categories:** Artificial Intelligence (cs.AI)

Stochastic world models are usually evaluated by the accuracy and calibration of their predicted futures. These criteria leave a decision-relevant ambiguity: the same conditional future distribution can arise because an observation aliases different physical states, or because the dynamics remain random after the declared full state is fixed. We prove that this attribution is not identifiable from ordinary transition data, even with an optimal probabilistic predictor. We introduce ClosurePairs, an interventional evaluation protocol that crosses compatible microstates with repeated exogenous disturbances. A two-way variance decomposition identifies state aliasing, process noise, and their nonlinear interaction; an independent-repeat variant applies when disturbances cannot be reused. On likelihood-equivalent Gaussian systems, paired supervision reduces alias-fraction error 15.96-fold at identical test NLL. Across 18 nonlinear Langevin conditions, it reduces attribution MAE from 0.372 to 0.051 and sensing regret from 0.0138 to 0.0003 without changing NLL. On a pixel-conditioned recurrent model, a frozen shared-state probe reduces alias-fraction MAE against a deep ensemble from 0.584 to 0.130 in distribution and from 0.630 to 0.170 out of distribution over ten seeds. Finally, in a matched-total-variance REFINE/BRANCH test, a total-variance router reaches 66.48 percent plus or minus 1.06 percent accuracy, whereas ClosurePairs reaches 99.99 percent plus or minus 0.02 percent and improves selected NLL from -2.087 to -2.717 over five seeds. ClosurePairs therefore measures why futures branch, information that proper forecast scores cannot identify.

---

## 4. WM-Cov: Test Adequacy for Interactive World-Model-Style Autonomous Driving Simulation

**Authors:** Jianxun Cui, Ping Wu, Stanisa Peric, Marko Milojkovic, Vladan Devedzic
**arXiv:** [2608.00298](https://arxiv.org/abs/2608.00298)
**Categories:** Artificial Intelligence (cs.AI)

World models and generative simulators are emerging as interactive testing infrastructure for autonomous driving because they can react to the ego planner and produce counterfactual, rare, and safety-critical rollouts. This changes a test scenario from a fixed replayed trajectory into an interactive scenario family whose realized evolution depends on the planner under test. The unresolved question is therefore not only whether dangerous rollouts can be generated, but what valid closed-loop evidence is enough to support a specified testing intent and stopping decision. This paper formulates interactive world-model-style testing adequacy and introduces WM-Cov, a provider-agnostic evaluation layer that converts raw provider outputs into requested, realized, and valid evidence. WM-Cov reports adequacy through coverage growth, valid-failure discovery, failure-mode diversity, realism, artifact suppression, duplicate accounting, and valid-evidence precision. Studies on executed TeraSim/SUMO events, WM-like mixed trace pools, and a real DriveArena TrafficManager--WorldDreamer matrix show that dangerous-looking events can include valid ADS failures, duplicates, partial realizations, and artifacts. The DriveArena matrix evaluates two planners, two horizons, six prompt conditions, and 360 ego-route requests; 304 attempts become fully realized evidence and 56 remain partial. A disjoint 80-request route-slice check yields 74 fully realized and 6 partial attempts. The results support evaluating world-model-style testing by convergence of valid interactive evidence under budget, rather than by raw generated failures or prompt coverage alone.

---

## 5. Demystifying When and Why VLAs Fail in Contact-Rich Tasks and How to Fix Them

**Authors:** Carlota Parés-Morlans, Nils Kuhn, Isabel Liu, Alberta Longhini, Jeannette Bohg
**arXiv:** [2608.01402](https://arxiv.org/abs/2608.01402)
**Categories:** Robotics (cs.RO); Artificial Intelligence (cs.AI)

We address the problem of understanding when and why Vision-Language-Action models struggle with contact-rich manipulation tasks that require precise physical interaction. Prior work has primarily focused on addressing contact failures through force-augmented architectures and training-time regularizers, yet the root causes of these failures remain underexplored. We identify two distinct failure modes underlying this gap. Precision failures are rooted in a flow-matching policy training mismatch, and force failures arise from the distinctive structure of force signals. We address each failure mode with a targeted mechanism and combine them into FACT, which achieves 66% average success rate across five contact-rich tasks against 41% for the best prior baseline, in an evaluation spanning almost 2,500 real-world rollouts.

---

## 6. WAM-Diff2: Hierarchical AR-to-Diffusion Distillation for Highly Efficient Autonomous Driving VLA

**Authors:** Zhihao Zhu, Hanlin Shang, Mingwang Xu, ..., Hang Xu, Siyu Zhu
**arXiv:** [2608.01035](https://arxiv.org/abs/2608.01035)
**Categories:** Robotics (cs.RO); Artificial Intelligence (cs.AI); Computer Vision and Pattern Recognition (cs.CV)

Vision-Language-Action (VLA) models have emerged as a prominent paradigm for end-to-end autonomous driving; however, their efficient deployment is severely constrained by high computational latency and exposure bias arising from sequential autoregressive decoding. Conversely, while specialized diffusion policies enable low-latency, parallel execution, training them from scratch typically yields narrow, single-task architectures that lack holistic visual-linguistic reasoning. Successfully transforming pre-trained autoregressive generalists into parallel diffusion models could combine multi-task cognitive intelligence with execution efficiency, yet this transition presents a formidable architectural challenge due to mismatched attention patterns (causal versus bidirectional) and divergent optimization objectives. To bridge this divide, we introduce WAM-Diff2, a multi-task discrete diffusion VLA framework powered by a three-stage hierarchical distillation strategy. By structuring the architectural shift through progressive block-wise adaptation, block-wise distillation, and model-wise cross-scale distillation, WAM-Diff2 preserves the underlying semantic foundations of the base model while accelerating inference. Extensive evaluations across driving understanding, perception, and planning benchmarks demonstrate that WAM-Diff2 effectively mitigates exposure bias and achieves performance parity with autoregressive baselines. Crucially, the autoregressive-to-diffusion transition yields a 2.8x decoding speedup, which scales to an ultimate 15.1x acceleration when combined with system-level optimizations including FlashInfer and CUDA Graphs.

---

## 7. VLAGuard: A Framework for Evaluating and Mitigating Physical Attention Hijacking in Vision-Language-Action Robots within Wireless Sensor Networks

**Authors:** Dongfu Yin, Jinquan Zhang
**arXiv:** [2608.01028](https://arxiv.org/abs/2608.01028)
**Categories:** Robotics (cs.RO); Artificial Intelligence (cs.AI)

Deploying Vision-Language-Action (VLA) robots as mobile edge nodes within wireless sensor networks (WSNs) requires robust protection against physical adversarial threats. We present VLAGuard, a framework to assess and mitigate a critical vulnerability: policy-critical action-to-vision attention hijacking. We first introduce a stress-test module, Visuomotor Attention-guided Semantic Attack (VASA), using printable patches to severely distract the robot's action-conditioned cross-attention. To counter this, we propose Attention-Protective Fine-Tuning (APFT), a defense that stabilizes spatiotemporal attention and enforces geometric consistency with zero inference overhead. Evaluations across simulated and physical WSN-assisted smart environments demonstrate significant robustness gains. APFT reduces the OpenVLA failure rate from 100.0% to 25.9% in LIBERO simulations. Furthermore, across 2,000 real-world trials, APFT improves the average success rate from 23.0% to 67.4% under severe patch attacks. This highlights that protecting attention pathways is important for improving the robustness of VLA-driven edge nodes in sensor networks.

---

## 8. Latency-Tolerant Cloud-Edge Collaborative Vision-Language-Action Models via Emergent Representational Specialization

**Authors:** Daojie Peng, Fulong Ma, Bingtao Wang, Sheng Wang, Jun Ma
**arXiv:** [2608.00569](https://arxiv.org/abs/2608.00569)
**Categories:** Robotics (cs.RO); Artificial Intelligence (cs.AI); Systems and Control (eess.SY)

Deploying billion-parameter Vision-Language-Action (VLA) policies on mobile robots creates a systems conflict: semantic reasoning benefits from cloud GPUs, whereas closed-loop control must respond locally despite network delay and jitter. Existing hierarchical and asynchronous policies improve throughput, but their slow-path representations can still arrive stale or require explicit scheduling and delay cues. We introduce CloudEdgeVLA, a cloud-edge policy that treats temporal misalignment as a representation-learning problem. A cloud VLA encodes delayed observations into slowly varying task features, while a lightweight edge head combines the latest available cloud feature with current local vision. During training, current and randomly delayed frames are paired with the same current action target in fresh and stale paths. This objective encourages the cloud representation to preserve task-level information while the edge path supplies state-sensitive corrections. Across four LIBERO suites, CloudEdgeVLA retains 63.8--78.0% success with a 40-step uniform-delay window, whereas VLASH reaches at most 6.4% and the evaluated single-path baselines at most 3.0%. By removing blocking synchronization from the control loop, the design offers a practical route to scalable VLA deployment in which cloud models can grow while edge computation remains lightweight and responsive.

---

## 9. The Gate, Not the Cache: Gate Provenance Bounds the Closed-Loop Reliability of Training-Free VLA Token Skipping

**Authors:** Qi Luo, Shuaijun Liu, Hao Zhao, ..., Dongsheng Wang, Yun Chen
**arXiv:** [2608.00391](https://arxiv.org/abs/2608.00391)
**Categories:** Robotics (cs.RO); Artificial Intelligence (cs.AI)

Token skipping is a widely used training-free way to accelerate vision--language--action (VLA) models by bypassing computation for most visual tokens at each control step according to a gate. When the next gate is harvested from the previous accelerated forward, however, the tokens skipped at one step are also the ones least visible to the next gate, and the damage can compound across control steps until the task fails. We study the two mechanisms this class is built on, reuse and deletion, crossing each against where its gate signal comes from on identical episodes. At a skip ratio of 0.9 on LIBERO-Object, both collapse when the gate comes from the model's own accelerated forwards, to 0.68 under reuse and to 0.31 under deletion against a dense 1.00, and the collapse is invisible to the action-level detectors we evaluate. What separates collapse from dense-level operation is not the mechanism but whether the gate is clean, computed by a forward that skipped nothing. We therefore propose actuation-slack refresh, one dense pass run while the robot executes its current action chunk, off the critical path, that hands the next step a clean gate and a fresh KV base. Since the measured detectors do not reliably reveal the failure, the refresh is unconditional rather than triggered. Both mechanisms then recover to 0.98, keeping the speed of skipping and the information of a dense pass. We then integrate the refresh into state-of-the-art caching and pruning methods across two VLA policies, 4 LIBERO suites, and 4 SIMPLER tasks, where it repairs every collapse caused by using a self-harvested gate. Serve latency drops 18--22\% below dense, measured both in simulation and on a physical robot. Where the gate signal comes from, not how tokens are skipped, decides closed-loop reliability for accelerated VLAs.

---

## 10. WorldDynCache: Risk-Controlled Latent Dynamics Approximation for Diffusion World Model

**Authors:** Leyang Chen, Junyi Wu, Shaoqiu Zhang, Yulun Zhang
**arXiv:** [2608.01845](https://arxiv.org/abs/2608.01845)
**Categories:** Machine Learning (cs.LG); Computer Vision and Pattern Recognition (cs.CV)

Diffusion world models generate high-quality futures, but re- peated transformer evaluations make inference prohibitively slow. Existing caches reuse intermediate features, selectively update tokens, or reuse and extrapolate denoising outputs ac- cording to local drift or short native-space histories. These criteria can miss both approximation-induced latent transition defects that accumulate across skipped steps and phase- or condition-dependent changes in the direction of latent evo- lution. We propose WorldDynCache, a risk-controlled latent dynamics approximation framework with two core compo- nents. First, a lightweight latent-transition risk estimator tracks the accumulated future impact of approximation defects and calibrates its predictions against counterfactual defects ob- served at exact anchors. Second, a condition- and phase- aware lifted latent surrogate approximates latent evolution without extra transformer evaluations. On HunyuanVoyager- 13B and Aether-5B, WorldDynCache achieves 4.92 times and 2.15 times speedups, respectively, while attaining the best gen- eration quality among the compared caching methods across WorldScore, PSNR, SSIM, and LPIPS.

---

## 11. Grounded Semantic Re-Binding for Robust Instruction Generalization in Vision-Language-Action Models

**Authors:** Zhaokai Yin, Zhipeng Zhang
**arXiv:** [2608.02497](https://arxiv.org/abs/2608.02497)
**Categories:** Robotics (cs.RO)

Vision-Language-Action (VLA) models excel in robotic manipulation but suffer catastrophic performance drops when canonical instructions are simply paraphrased. Although this brittleness is typically addressed through costly data scaling, our probing reveals that the root cause is architectural rather than a lack of semantic understanding. Specifically, we demonstrate that current VLAs successfully retain the correct task identity internally. The failure actually stems from the joint encoding of dynamic visual observations and text, which introduces systematic feature shifts. Because the downstream action policy is highly vulnerable to these variations, it fails to translate the preserved semantics into correct control commands. To resolve this structural bottleneck, we propose Grounded Semantic Re-binding (GSR), an elegant intervention that bypasses unstable joint routing by explicitly fusing independently extracted task semantics with native visual features to train a completely re-initialized action expert from scratch. This targeted intervention dramatically restores paraphrastic invariance using only canonical demonstrations. On the LIBERO-Para benchmark, GSR improves success rates by up to 44.6 percent. It enables lightweight models to rival massively scaled baselines and pushes state-of-the-art models to a new record PRIDE score of 70.4, outperforming the recently introduced large-scale pretrained model Xiaomi-Robotics-0 in instruction generation capabilities. Building on these insights, we also introduce ParaVLA, a natively decoupled 0.33B-parameter model exhibiting near-perfect robustness to instruction rewording. Ultimately, our work proves that robust semantic grounding can be achieved through elegant structural design, bypassing the inefficient brute-force data scaling paradigm.

---

## 12. ChainVLA: Chaining Vision-Language-Action Queries through a Unified Execution State for Long-Horizon Manipulation

**Authors:** Yuzhi Huang, Weijue Bu, Ziyi Xiong, ..., Jingyan Jiang, Zhi Wang
**arXiv:** [2608.02326](https://arxiv.org/abs/2608.02326)
**Categories:** Robotics (cs.RO)

Humans perform long-horizon manipulation by retaining knowledge of what earlier actions have established while continuously adapting the motion underway. By contrast, action-chunked vision-language-action (VLA) policies repeatedly replan from the current input at each query. Existing methods preserve either long-term task evidence through memory or short-term motion through action reuse and ensembling, leaving the cross-query handoff incomplete. We introduce ChainVLA, a 1.2B-parameter VLA policy that chains successive queries through a joint and revisable execution state. Progress Context combines a recurrent Working State with sparse event memory to carry observation-derived task progress, while Motion Tail feeds the preceding prediction's unexecuted continuation into state construction and action generation. Together, the two components condition a decoder that regenerates each action horizon under the latest observation, allowing the carried state to guide the next prediction without fixing it. ChainVLA reaches 62.8% average success on RMBench and 98.8% across four LIBERO suites, while removing Motion Tail or Progress Context reduces RMBench success to 11.2% and 3.0%, respectively. These asymmetric ablations are consistent with motion continuity helping preserve the observation stream from which task progress is inferred.

---

## 13. Learning Panorama-Aware VLA for Mobile Manipulation with Whole-Body Teleoperation

**Authors:** Donglin Yang, Haoran Chen, Xingyu Chen, ..., Xiaojian Ma, Si Liu
**arXiv:** [2608.02257](https://arxiv.org/abs/2608.02257)
**Categories:** Robotics (cs.RO)

Mobile manipulation is a key capability for embodied intelligence, enabling robots to accomplish complex multi-stage tasks in open-world environments. However, mobile manipulation poses two key challenges for vision-language-action (VLA) policies: At the data level, the efficient collection of high-quality whole-body demonstrations demands the coordinated control of both the mobile base and the robotic arms; at the model level, existing VLA models predominantly rely on local camera observations, whose limited field of view hinders global spatial understanding. To address these challenges, we develop a whole-body teleoperation system and a panoramic-aware VLA policy. The system enables coordinated control of a wheeled bimanual robot through a single VR interface and supports the acquisition of a real-world mobile manipulation dataset comprising 5.5 hours of multimodal demonstrations. Building upon this dataset, we propose PanoVLA, a panorama-aware vision-language-action policy for mobile bimanual manipulation. Built upon a Mixture-of-Transformers architecture, PanoVLA introduces global spatial context through dedicated panorama encoding and fusion modules, enabling effective integration of panoramic observations with language instructions and robot states for action generation. Evaluation on four real-world mobile manipulation tasks demonstrates that PanoVLA achieves an average stage completion rate of 91.3\% and an end-to-end success rate of 73.4\%, substantially outperforming local-view baselines. These results demonstrate that incorporating panoramic spatial context improves spatial understanding and closed-loop manipulation performance in mobile robots.

---

## 14. Look Where It Matters: Adaptive Visual Refinement for Vision-Language-Action Models

**Authors:** Jin Cui, Yanbin Hu, Xinyue Long, ..., Boran Zhao, Pengju Ren
**arXiv:** [2608.02197](https://arxiv.org/abs/2608.02197)
**Categories:** Robotics (cs.RO)

Visual representations of VLA models remain unreliable for spatially precise robotic manipulation. We uncover that vision encoders in VLAs also exhibit attention artifacts previously documented in generic Vision Transformers, and further show that, in embodied policies, these artifacts are closely associated with spatial perception capabilities acquired during post-training. As the encoder learns task-relevant information such as object location, depth ordering, and local geometry, limited global-token capacity causes part of this information to spill into low-information patch tokens. We introduce AtVLA, a framework that inserts learnable register tokens into the visual encoder. Trained end-to-end using only embodied data and the original action objective, these registers emerge as dedicated carriers of embodied spatial information, while the remaining patch tokens recover clean and spatially faithful attention distributions crucial for precise target localization and fine-grained contact. Clean attention restores reliable localization, but cannot recover geometric details lost in low-resolution observations. AtVLA therefore couples attention rectification with uncertainty-gated local refinement. The action expert samples multiple action chunks and estimates uncertainty from their disagreement; only for uncertain predictions, action-conditioned attention rollout identifies the task-relevant region, which is cropped, re-encoded at high resolution, and appended to the cached prefix for refined action generation. Across LIBERO, SimplerEnv, and a challenging single-view real-world benchmark, AtVLA improves the average LIBERO success rate from 94.2% to 98.4% and real-world success from 46.5% to 69.0%. The cropping is triggered on approximately 30% of replanning steps, resulting in only 1.4-1.6x the total computation of the base model under the representative deployment setting.

---

## 15. World Action Models in Real Time: An Empirical Study of Smooth Execution via Asynchronous Deployment

**Authors:** Motubrain Team
**arXiv:** [2608.01880](https://arxiv.org/abs/2608.01880)
**Categories:** Robotics (cs.RO)

World Action Models generate fixed-horizon action chunks through iterative denoising, creating substantial inference latency that can cause pauses, stale actions, and discontinuities during robotic execution. We present an empirical study of asynchronous deployment strategies that overlap model inference with action execution to enable responsive and smooth control. We compare six strategies, including synchronous execution, pure asynchronous switching, post-hoc action blending, denoising-time blending, inference-time velocity guidance, and prefix-conditioned generation, on a 10 Hz bimanual robot. Evaluation combines offline trajectory analysis with online experiments across dynamic manipulation, precision-critical placement, and long-horizon tasks. Our results identify accurate temporal alignment between observations, predictions, and executed commands as a fundamental requirement. Alignment errors produce persistent chunk-boundary discontinuities that cannot be corrected through blending alone. With proper alignment, direct action weighting provides a simple and smooth baseline but sacrifices accuracy in precision-critical tasks. Inference-time velocity guidance fails to reliably constrain committed actions on our platform. In contrast, prefix-conditioned generation achieves the best overall balance between task performance, execution speed, and trajectory smoothness by learning consistent action continuations during training. These findings clarify the practical trade-offs among asynchronous deployment strategies and provide guidance for deploying high-latency World Action Models in real-time robotic systems.

---

## 16. Multi-View Unified Camera Fields: Geometry-Shaped Action-Facing Representations for RGB-Only Multi-Camera VLA Policies

**Authors:** Jiarui Yang, Yehao Lu, Yuning Su, ..., Enyu Li, Junwei Liang
**arXiv:** [2608.01826](https://arxiv.org/abs/2608.01826)
**Categories:** Robotics (cs.RO)

Vision-Language-Action (VLA) models have shown strong generalization in robotic manipulation, yet complex contact-rich tasks often benefit from multi-camera observations that jointly capture the end effector, objects, and targets under occlusion. Existing multi-camera VLAs usually concatenate view tokens, leaving action representations weak in metric depth and inconsistent across cameras. We introduce Multi-View Unified Camera Fields (MVUCF), a training-only framework that forms a shared action-facing latent field across views. A coordinate-query depth objective makes metric depth recoverable, while a preprocessing-aware correspondence objective aligns tokens observing the same physical point from different cameras. Both directly shape the hidden states consumed by the action module. After geometry injection, depth, camera calibration, and auxiliary heads are removed, so deployment uses the original RGB-only graph with no extra inference FLOPs. Held-out probes confirm stronger depth recovery and cross-view matching. Under matched GR00T-N1.6 settings, MVUCF reaches 98.9% on LIBERO, improves LIBERO-Plus by 22.4 points, and raises success by 23.3 points across six RoboTwin tasks spanning three action families: touch, move-and-place, and contact interaction. Real-world humanoid experiments further provide evidence of its practical effectiveness under RGB-only deployment.

---

## 17. Uncovering and Mitigating Positional Blind Spots in Vision-Language-Action Models

**Authors:** Dongdong An, Pengjie Zhao, Yihao Huang, ..., Jifeng Ning, Qin Zhao
**arXiv:** [2608.01573](https://arxiv.org/abs/2608.01573)
**Categories:** Robotics (cs.RO)

Recent Vision-Language-Action (VLA) models achieve promising performance in robotic manipulation, typically measured by success rates aggregated over predefined object configurations, an evaluation that implicitly assumes spatially uniform competence across the workspace. However, this assumption does not hold: even with the instruction and every other scene factor held fixed, merely relocating a task-irrelevant distractor can sharply raise the failure probability within localized, spatially coherent regions, which we term Positional Blind Spots (PBS). In this paper, we propose a two-stage black-box framework to uncover and mitigate PBS. During the uncovering stage, we grid the workspace and apply a one-sided log-likelihood-ratio test to localize PBS cells with significantly elevated risk. During the mitigation stage, we fine-tune the policy via LoRA on demonstrations collected from these PBS regions, improving competence there while largely preserving performance across the rest of the workspace. We evaluate our framework on five state-of-the-art VLA policies across two benchmarks, and find that PBS are pervasive and spatially concentrated in all of them, with failure rates up to 0.58. Our search strategy achieves an average F1-score of 0.678, outperforming random search and adaptive sampling baselines by 0.268 and 0.178, respectively. Guided by the discovered regions, targeted fine-tuning reduces the overall failure rate by 40.00%--85.19%.

---

## 18. SG-WAM: Self-Guided World Modeling in Geometry-Aware Policy Space

**Authors:** Ruiteng Zhao, Zhengshen Zhang, Yue Su, ..., Marcelo H. Ang Jr., Haiyue Zhu
**arXiv:** [2608.01397](https://arxiv.org/abs/2608.01397)
**Categories:** Robotics (cs.RO); Computer Vision and Pattern Recognition (cs.CV)

World Action Models (WAMs) couple action generation with prediction of future states. Their effectiveness depends on whether future dynamics are modeled in a space that is both aligned with action generation and sufficiently geometry-aware to capture where and how actions change the scene. Existing WAMs typically satisfy only part of this requirement, relying on either perceptually heavy observation-space targets or auxiliary latent spaces that are not jointly structured for action relevance and geometry. We propose SG-WAM, a self-guided framework that learns geometry-aware action-conditioned dynamics directly in the policy-derived representation space. SG-WAM introduces learnable dynamics tokens and a Self-Guided World Predictor that forecasts their future latent states conditioned on intervening robot actions. Prediction targets are generated by an exponential moving average copy of the same policy backbone, providing stable supervision within the representation family used by the action expert. Geometric supervision further structures the policy image-token representations, providing spatially grounded context for the dynamics tokens and yielding a future-alignment space that is both action-relevant and geometry-aware. Latent future prediction, geometric grounding, and flow-matching action generation are jointly optimized end-to-end in a unified framework. Built on a 0.9B model without large-scale embodied pretraining, SG-WAM achieves 98.5% average success on LIBERO and 73% on LIBERO-Plus, while outperforming strong baselines in both in-distribution and out-of-distribution real-world evaluations.

---

## 19. DreamTrajectory: Trajectory-Guided Action Generation with World Model Alignment for Mobile Manipulation

**Authors:** Zheng Yang, Wenjie Zhang, Xiangyu Chen, ..., Renjing Xu, Xiaowen Chu
**arXiv:** [2608.01381](https://arxiv.org/abs/2608.01381)
**Categories:** Robotics (cs.RO)

Mobile manipulation requires a robot to coordinate base and arm motion under continuously changing viewpoints and contact conditions, within an action space far larger than that of fixed-base manipulation. Existing Vision-Language-Action (VLA) policies are limited in two respects. (i)They map observations directly to whole-body action chunks, searching this large action space without an explicit task-space motion plan, which makes coordinated base--arm prediction imprecise. (ii)They execute the predicted chunk open-loop, without checking whether the actions can realize the motion the policy intended, so control errors and unmodeled contacts accumulate into a gap between planned and realized motion. We present DreamTrajectory, a trajectory-guided framework for language-conditioned mobile manipulation that introduces one component for each limitation. Addressing(i), DreamTrajectory jointly predicts an intention-level end-effector trajectory and a whole-body action chunk in a single action expert, so that the trajectory explicitly guides base--arm action generation instead of remaining implicit. Addressing(ii), a lightweight trajectory world model predicts the trajectory that a candidate action chunk would induce, and a test-time search--predict--score procedure selects the candidate best aligned with the planned trajectory. On MS-HAB, trajectory guidance raises average success from 32.3% to 47.5% and test-time refinement further to 54.8%, with the largest gains on contact-rich articulated-object tasks. On three real-world mobile manipulation tasks, the corresponding average success rates are 63.3%, 81.7%, and 90.0%.

---

## 20. Hermite Curves as Trajectory Priors for Vision-Language-Action Models

**Authors:** Qi Lv, Jianming Xing, Zhao Yang, ..., Mike Zheng Shou, Xiang Deng
**arXiv:** [2608.01265](https://arxiv.org/abs/2608.01265)
**Categories:** Robotics (cs.RO); Computer Vision and Pattern Recognition (cs.CV)

Despite recent progress in Vision-Language-Action (VLA) models for robotic manipulation, the action chunk remains a weakly structured interface. Existing work typically flatten each chunk into per-timestep controls, relying on implicit data learning that manifests as jagged motion and boundary discontinuities during physical execution. To address these limitations, we introduce Hermite trajectory priors, parameterizing the chunk trajectory as a piecewise cubic Hermite curve defined by endpoint positions and velocities to explicitly enforce smoothness and continuity. We instantiate this fixed operator across discrete autoregressive and continuous generative paradigms via three variants: (1) Hermite Tokens, which predict quantized boundary variables autoregressively; (2) Hermite Scaffold, which decomposes clean actions into a base scaffold and residuals; and (3) Hermite Regularization, which applies the prior strictly as an auxiliary training objective. Across simulation benchmarks and real-robot platforms, Hermite Regularization achieves superior performance among these three variants, improving {\pi}0.5 baseline success rates from 95.9% to 98.7% on LIBERO, 85.7% to 90.9% on LIBERO-plus, and 63.4% to 90.0% across four real-robot tasks without additional inference overhead. Trajectory analyses reveal that explicitly structuring trajectory priors serves most effectively as a learning inductive bias rather than a runtime constraint.

---

## 21. EndoWAM: A Grounded World-Action Model for Generalizable Endoscopic Navigation

**Authors:** Jinsong Lin, Zikang Pan, Wanhao Liu, ..., Huxin Gao, Hongliang Ren
**arXiv:** [2608.01221](https://arxiv.org/abs/2608.01221)
**Categories:** Robotics (cs.RO)

Autonomous endoscopic navigation can reduce clinicians' operational burden, yet robust control remains challenging due to tissue deformation, transient occlusions, and rapidly changing viewpoints. Existing learning-based policies typically predict actions from current observations without explicitly modeling future dynamics, limiting their robustness and reliability in safety-critical settings. World Action Models (WAMs) offer a promising alternative by coupling predictive visual dynamics with action generation, but extending them to robotic endoscopy remains challenging due to limited training data, restricted viewpoint diversity, deformable anatomy, and high inference latency. We present EndoWAM, which is, to our knowledge, the first WAM for generalizable robotic endoscopic navigation. EndoWAM introduces future grounding, which predicts task-relevant target regions in future observations from intermediate denoising features of a video world model. Specifically, EndoWAM couples a lightweight diffusion transformer for future target-region prediction with a discrete action expert through a shared predictive representation. This design injects target-aware supervision into predictive dynamics modeling, improving robustness to visual degradation and viewpoint changes while enabling real-time control in a single denoising pass. We further introduce EndoMotion, a robotic endoscopic motion dataset spanning three anatomically distinct procedures: ureteroscopy, esophagoscopy, and endoscopic retrograde cholangiopancreatography (ERCP). EndoWAM consistently outperforms all baselines and alternative grounding strategies, while demonstrating strong zero-shot generalization to unseen viewpoints, environments, and targets. These results establish EndoWAM as a predictive, target-grounded framework for accurate, generalizable, and long-horizon navigation in visually constrained endoscopic environments.

---

## 22. OC-VLA++: Monocular Geometry-Guided Cross-View Consistency for Viewpoint-Robust Robotic Manipulation

**Authors:** Tianyi Zhang, Ziyang Gong, Zhenjie Yang, Zhe Qian, Haonan Duan
**arXiv:** [2608.01066](https://arxiv.org/abs/2608.01066)
**Categories:** Robotics (cs.RO)

We propose OC-VLA++, an extension of OC-VLA for viewpoint generalization under limited camera coverage. While OC-VLA grounds robot actions in the camera coordinate system to align action supervision with visual observations, camera-space grounding alone can still overfit to the few viewpoints observed during training. OC-VLA++ addresses this limitation by introducing geometry-guided paired-view supervision and an explicit cross-view action-equivariance objective. Given paired observations of the same manipulation scene from geometrically related viewpoints, the model is trained such that their camera-space predictions correspond to the same robot-frame action. This objective explicitly supervises how action predictions should transform across viewpoints, rather than relying solely on image-level augmentation. Experiments demonstrate substantial improvements in unseen-view generalization under limited camera coverage, with performance degrading more gracefully under increasing camera displacement. These results establish cross-view action equivariance as an effective complement to observation-centric action grounding for robust real-world deployment.

---

## 23. RL Bootstrapping of OpenVLA-OFT for a Novel Robot Embodiment

**Authors:** Damir Nurtdinov, Alexei Kornaev, Alexander Maloletov
**arXiv:** [2608.01013](https://arxiv.org/abs/2608.01013)
**Categories:** Robotics (cs.RO)

Adapting a pretrained vision-language-action (VLA) policy to a new robot usually assumes embodiment-specific demonstrations. This assumption is especially restrictive for custom robots whose morphology differs strongly from the manipulators seen in large robot datasets. We study a harder setting: zero-demo embodiment alignment of OpenVLA-OFT on a cable-driven parallel robot (CDPR) with a simple gripper and a previously unseen control interface. Instead of supervised fine-tuning, we use reinforcement learning in simulation with dense geometric rewards computed from simulator state. The training is performed in two stages: a PPO stage for directional motion primitives, followed by GRPO continuation from the PPO checkpoint with an expanded instruction space that includes object-conditioned commands. On the four shared directional instructions, the average held-out success rate improves from 34.25\% after PPO to 53.50\% after PPO$\rightarrow$GRPO, with especially large gains on \texttt{move left} and \texttt{move backward}. In the GRPO stage we additionally introduce \texttt{move to <object>} over eight target objects and obtain 39/400 = 9.75\% strict success, while qualitative rollouts frequently show correct target-directed approach behavior before late-stage instability. Compared with prior OpenVLA and OpenVLA-OFT results, which rely on demonstration datasets and mostly standard rigid-arm embodiments, our method uses no embodiment-specific dataset at all. The results do not yet establish robust manipulation, but they provide stronger evidence that RL-only bootstrapping can create the first usable language-conditioned controller for a genuinely novel embodiment.

---

## 24. DynamicWAM: Dual-Path Motion Conditioning for World-Action Models in Dynamic Manipulation

**Authors:** Yunfan Lou, Hewen Gao, Xiyu Zhu, ..., Boxian Yao, Zhibo Pang
**arXiv:** [2608.00793](https://arxiv.org/abs/2608.00793)
**Categories:** Robotics (cs.RO)

Dynamic manipulation requires robots to infer target motion and respond promptly, yet existing World-Action Models (WAMs) typically condition only on the current frame and execute large backbones synchronously, limiting motion awareness and responsive control in dynamic scenes. We propose DynamicWAM, a compact WAM for dynamic object manipulation with dual-path motion conditioning. DynamicWAM introduces history-flow conditioning, encoding temporally aligned optical-flow frames alongside the current observation through a frozen pretrained video VAE to preserve spatial motion structure, while injecting kinematic descriptors of displacement, duration, velocity, and acceleration into the action expert to provide motion magnitude and timing. The two complementary paths are fused through joint world-action attention. A distilled compact backbone and real-time chunking (RTC)-based asynchronous execution further enable responsive control. On DOMINO, DynamicWAM achieves a 38.2% success rate and a 53.2 manipulation score, outperforming all evaluated baselines. Across 12 real-world tasks spanning linear, circular, and compound target motion, it achieves a 46.7% average success rate, exceeding the strongest baseline by 22.9 percentage points.

---

## 25. SelfWAM: A Self-Grounded Unified World Action Model for Fast Robot Control

**Authors:** Bikang Pan, Fan Liu, Haotao Lu, Jingya Wang, Ye Shi
**arXiv:** [2608.00725](https://arxiv.org/abs/2608.00725)
**Categories:** Robotics (cs.RO)

World Action Models (WAMs) improve robot policy learning by jointly modeling actions and future observations. However, conditioning future prediction only on the task prompt and observation context risks capturing generic task progression rather than the action-specific consequences of the executed action. We introduce SelfWAM, a unified self-grounded WAM built on a modality-specialized Mixture-of-Transformers (MoT) architecture that jointly predicts actions, action-conditioned future RGB frames, and robot self-masks, thereby grounding future prediction in the robot's visible body and its action-induced motion. During joint training, SelfWAM allows future visual queries to attend to a clean copy of the demonstrated action, turning the video branch into an action-specific consequence model while leaving the fast action-only inference path unchanged. To focus video learning on action-relevant visual changes, we use prompt-specific objectives for future robot self-mask prediction, which removes appearance details and provides a target whose temporal evolution is tightly coupled with the conditioning action. Together, clean-action conditioning and future self-mask supervision make future predictions more directly reflect how the executed action changes the robot's visible motion and the surrounding scene. Experiments on RoboTwin 2.0 and real-world manipulation tasks show that SelfWAM produces more action-sensitive futures and preserves fast policy inference, while improving policy performance.

---

## 26. FlowPilot: Real-Time World-Action Modeling for Agile UAV Navigation

**Authors:** Runqing Wang, Ding Yu, Pengyuan Min, ..., Fu Zhang, Gang Wang
**arXiv:** [2608.00635](https://arxiv.org/abs/2608.00635)
**Categories:** Robotics (cs.RO)

We present FlowPilot, a compact world-action model for real-time onboard UAV navigation from depth. Unlike map-then-optimize pipelines that require local reconstruction or end-to-end policies that lack explicit scene prediction, FlowPilot jointly denoises future depth observations and executable trajectories with flow matching. A dual-stream mixture-of-transformers couples video and action experts through shared attention, allowing future-scene prediction and trajectory generation to inform each other. At deployment, the model runs action-centrically and outputs only a trajectory. To ensure trackability, actions are parameterized as degree-7 Bernstein polynomials: the current state constrains the initial control points, and the network predicts five free control points, yielding C^2-continuous references with closed-form velocity, acceleration and jerk. FlowPilot is trained on a three-level depth pyramid spanning high-throughput simulation, photorealistic simulation, and real onboard data. In closed-loop simulation, it outperforms learning- and optimization-based baselines under increasing clutter and commanded speeds up to 8m/s. On a physical quadrotor, the full perception-to-action pipeline runs in under 18ms on a Jetson Orin NX and reaches 5.5m/s in cluttered indoor and forest environments using only onboard sensing and computation.

---

## 27. Disentangling Visuo-Tactile Foresight: Oracle-Guided Interface Discovery for World Action Models

**Authors:** Zihang Yao, Chaoyue Ding, Yingying Yu
**arXiv:** [2608.00547](https://arxiv.org/abs/2608.00547)
**Categories:** Robotics (cs.RO)

Contact-rich manipulation remains challenging because successful control depends on physical interaction cues that are often weakly observable from vision alone. Recent tactile world action models jointly model future visual observations and tactile signals to guide action generation, but how such futures should be structured for effective use by the action expert remains underexplored. Directly studying this question with learned world action models is difficult because end-to-end behavior entangles physically invalid visual futures, unreliable predictions, inaccurate or cross-modally inconsistent tactile forecasts, and an unreadable future-to-action interface. To make this interface independently studyable, we introduce Oracle Visuo-Tactile Foresight (OVTF), a controlled framework that supplies paired RGB and tactile futures from successful trajectories verified in simulation. By fixing the future provider, OVTF isolates the interface and asks a cleaner question: if the future is successful and physically executable, what representation allows the action expert to absorb its benefit? Within OVTF, we propose Asymmetric Phase-Local Future Memory (AFM), in which visual memory reads future vision, each tactile memory jointly attends to its own tactile stream and phase-aligned future vision, and cross-tactile access is blocked. We compare AFM with Modality-Isolated Future Memory (IFM), which removes visual-to-tactile access and processes each future modality independently. Across seven tasks on the UniVTAC simulation benchmark, AFM achieves 32.0% average success, compared with 23.7% for IFM and 14.9% for UniVTAC-ACT. This controlled comparison shows that selective phase-aligned visual-tactile routing provides a more actionable future-to-action bridge than complete modality isolation.

---

## 28. WorldExam: Benchmarking World Models from Apparent Appearance to Inherent Reactivity

**Authors:** Yuxue Yang, Shuyao Shang, Jiahe Wang, ..., Lue Fan, Zhaoxiang Zhang
**arXiv:** [2608.02603](https://arxiv.org/abs/2608.02603)
**Categories:** Computer Vision and Pattern Recognition (cs.CV)

Controllable video generation models are increasingly being developed as world models. Accordingly, evaluating them in this role extends beyond the apparent appearance of generated videos to the inherent reactivity of the worlds they depict: the ability to infer from the scene state how the world should react and to generate plausible consequences not explicitly described in the input. Yet existing benchmarks mainly assess visual quality or explicit instruction fulfillment by checking whether requested actions and interaction outcomes are realized, leaving inherent reactivity underexamined. We introduce WorldExam, a hierarchical diagnostic benchmark spanning four levels: Visual Quality, Control Adherence, Spatial Consistency, and World Reactivity. It comprises 1,474 cases across eight dedicated tasks and supports unified evaluation of camera-, action-, and language-driven model paradigms. The World Reactivity level evaluates scene-conditioned reactions and goal-directed behaviors beyond what is explicitly specified in the input. Evaluation of 20 representative models reveals a clear capability split. Camera-driven models excel at camera control, but their interfaces do not support dynamic interaction; action-driven models control subjects more precisely but often leave the world unresponsive; and language-driven models perform better on interaction but follow complex controls less faithfully. No model combines broad task coverage with consistently strong performance, showing that high visual quality and explicit instruction fulfillment do not guarantee inherent reactivity.

---

## 29. DF$^3$: World Modeling via Decoder-Free Feature Forecasting in Autonomous Navigation

**Authors:** Jiaming Chen, Guoan Xu, Aoshen Huang, ..., Yang Li, Wei Pan
**arXiv:** [2608.02428](https://arxiv.org/abs/2608.02428)
**Categories:** Computer Vision and Pattern Recognition (cs.CV)

Forecasting future states from video sequences is a critical challenge for autonomous robotic systems and a fundamental objective of world modeling. Prior generative methods operating at the pixel level inevitably overemphasize task-irrelevant details, leading to prohibitive computational overhead. While latent-based approaches attempt to mitigate this by predicting features directly, the persistent reliance on heavy decoders for state-to-task mapping remains a computational bottleneck. In this work, we propose Decoder-Free Feature Forecasting (DF$^3$), a novel framework that models world evolution entirely within the latent space and directly derives task outputs, completely eliminating the need for a decoder. Specifically, DF$^3$ injects learnable spatial queries into the terminal blocks of a frozen vision foundation model to extract future state representations directly. By employing a lightweight, unified Motion-Aware Context Fusion (MACF) mechanism that seamlessly integrates coarse flow warping with fine-grained latent cross-correlation, these queries interact with historical token representations to explicitly align and forecast the feature of the next frame. Subsequently, a specialized set of task queries probes these forecasted features for the downstream task. Extensive experiments on public benchmarks and zero-shot deployment in a robotic simulator demonstrate that DF$^3$ achieves performance comparable to state-of-the-art methods while offering superior efficiency and flexibility for integrated perception and control.

---

## 30. MiniWorld: Democratizing the Training of Video World Models from Scratch

**Authors:** Yian Zhao, Ruochong Zheng, Hongcan Guo, ..., Jian Zhang, Jie Chen
**arXiv:** [2608.01127](https://arxiv.org/abs/2608.01127)
**Categories:** Computer Vision and Pattern Recognition (cs.CV)

Video world models predict future observations conditioned on historical observations and control signals, enabling long-horizon generation through autoregressive state transitions. Unlike conventional video generation models that primarily capture visual appearance and motion, video world models learn the underlying dynamics governing environment evolution under agent actions, providing a foundation for embodied AI and interactive simulation. Recent progress has largely relied on adapting pretrained video generation models through post-training or distillation. Although effective, these approaches often require complex training pipelines, substantial computational resources, and suffer from the mismatch between bidirectional pretraining and causal streaming inference. Recent studies have shown that training autoregressive video world models from scratch is feasible and scalable. However, the community still lacks a lightweight, transparent, and fully reproducible baseline trainable end-to-end with modest computational resources. We present MiniWorld, a reproducible framework for training streaming video world models from scratch. MiniWorld employs a block-causal Video Diffusion Transformer trained with Flow Matching in the latent space of a pretrained Video VAE. Building on Diffusion Forcing, it adopts a chunk-wise non-decreasing noise schedule and two-stage continued training to improve temporal modeling and stability. During inference, MiniWorld combines a rolling KV cache with pipelined asynchronous denoising for efficient streaming generation under bounded computation. The entire model can be trained within several days on a single 8-GPU server. By releasing the training and inference codebase and pretrained checkpoints, we hope MiniWorld will facilitate future research on video world modeling.

---
