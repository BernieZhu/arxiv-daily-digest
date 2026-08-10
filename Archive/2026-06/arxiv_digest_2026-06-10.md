# arXiv Daily Digest — 2026-06-10

**Mode:** direct
**Categories:** cs.AI, cs.LG, cs.RO, cs.CV
**Keywords:** VLA, world model, world action model
**Papers found:** 20

---

## 1. WorldKernel: A World Model is the Coupling Kernel of Admissible Possible Worlds

**Authors:** Fabio Rovai
**arXiv:** [2606.10934](https://arxiv.org/abs/2606.10934)
**Categories:** Artificial Intelligence (cs.AI)

A common assumption holds that enough observational and interventional data, given to a strong enough predictor, suffices. We report a failure mode that contradicts it. Across hundreds of structural causal models, on identified quantities a strong predictor and a Bayesian baseline both succeed, but on unidentified quantities (the couplings between counterfactual worlds) the predictor collapses to a point, on 28% of models to one no valid model can produce, while the truth is an admissible interval more data never narrows. The gap is structural: prediction cannot represent uncertainty over counterfactual couplings. We cast a world model as a single positive semidefinite coupling kernel K(T,T') over admissible worlds, whose diagonal is the ordinary posterior (what a predictor recovers) and whose off-diagonal is the cross-world coupling it cannot, which every counterfactual reads. The paper is the theory of that off-diagonal. It is real: two states with identical posteriors differ on a cross-world query, and the off-diagonal is the coupling that fixes counterfactuals. It can be bounded: positive semidefiniteness is partial-identifying information the marginals lack, and enforcing it bounds counterfactuals in polynomial time where the exact response-type program is intractable. Logical structure sharpens it: ontology axioms tighten the bound by up to a third, propagating to couplings they never touch. It can be acquired: targeted scars, constraints learned from encountered infeasibilities, close the gap several times faster than untargeted ones. Its full reconstruction is approximate counting of the admissible worlds, tractable below the Sly-Sun threshold and inapproximable above; we do not claim to beat the worst case.

---

## 2. ReflectiChain: Epistemic Grounding in LLM-Driven World Models for Supply Chain Resilience

**Authors:** Jia Luo
**arXiv:** [2606.10359](https://arxiv.org/abs/2606.10359)
**Categories:** Artificial Intelligence (cs.AI)

AI agents in supply chains face a fundamental epistemic gap: large language models (LLMs) interpret policies but lack physical grounding, while reinforcement learning (RL) optimizes flows but is semantically blind to unstructured constraints. We introduce REFLECTICHAIN, bridging this gap through a Generative Supply Chain World Model (SC-WM) - encoding heterogeneous supply networks into a 6-dim graph-latent space with physical conservation - and Double-Loop Learning that separates epistemic uncertainty (KL-trust-region-bounded policy adaptation) from aleatoric uncertainty (stochastic latent rollouts). On Semi-Sim, a 10-node semiconductor benchmark with SIR risk propagation, 6 perturbation types, and 10 policy constraint templates, REFLECTICHAIN improves Rationale Consistency Score by 33.0% (p < 0.0001, d = 2.78), maintains 82.3% operability under adversarial shocks, and exhibits anti-fragile behavior (+40.2% gain under moderate pressure). We identify three operational epistemic mechanisms - uncertainty separation, knowledge-boundary detection, and empirical Bayesian policy updating - and discuss five limitation categories.

---

## 3. Business World Model

**Authors:** Cecil Pang, Hiroki Sayama
**arXiv:** [2606.10044](https://arxiv.org/abs/2606.10044)
**Categories:** Artificial Intelligence (cs.AI)

Businesses are increasingly adopting AI-enabled tools to improve productivity, reduce costs, and enhance products and services. However, the transformative potential of AI extends beyond automating predefined tasks: it lies in enabling intelligent systems to plan, optimize, and execute business initiatives from high-level strategic objectives. This paper introduces the concept and architecture of a business world model (BWM), a world model specialized for business and organizational environments. Inspired by world models in artificial intelligence, cognitive science, and control theory, a BWM encodes business states, dynamics, constraints, objectives, and feasible action space to support autonomous decision-making. We propose a business-semantics-centric formulation in which business states, dynamics and actions are linked to key business entities. Within this framework, agents can simulate alternative action sequences, estimate their effects on future business outcomes, and evaluate trade-offs under uncertainty. The proposed architecture integrates semantic data representations, probabilistic machine learning models, deterministic business rules, and explicit action space into a coherent structure for planning and counterfactual reasoning. Although its individual components are not new, the contribution of BWM lies in organizing them as an executable internal simulator for business initiatives. This work establishes a conceptual foundation for autonomous business systems capable of moving from instruction-based execution toward goal-driven planning and execution.

---

## 4. LIBERO-Occ: Evaluating and Improving Vision-Language-Action Models under Scene-Induced Occlusion via Viewpoint Imagination

**Authors:** Taishan Li, Jiwen Zhang, Siyuan Wang, Xuanjing Huang, Zhongyu Wei
**arXiv:** [2606.10862](https://arxiv.org/abs/2606.10862)
**Categories:** Computer Vision and Pattern Recognition (cs.CV); Artificial Intelligence (cs.AI)

Vision-Language-Action (VLA) models achieve strong performance on standard manipulation benchmarks, but most evaluations assume that task-relevant objects are fully visible. This assumption often fails in realistic settings, where occlusion makes manipulation partially observable. In this paper, we study \textit{scene-induced occlusion} as a fundamental challenge for VLA models and introduce \textbf{LIBERO-Occ}, an occlusion-oriented extension of LIBERO. Experiments show that state-of-the-art VLAs suffer substantial performance degradation under occlusion. To address this issue, we propose \textbf{Viewpoint Imagination (VIM)}, which generates a complementary view from an occluded primary observation and conditions action prediction on both observed and imagined evidence. VIM improves robustness across task suites, occlusion types, and severity levels without requiring additional cameras at deployment time, suggesting that viewpoint imagination is an promising mechanism for perception completion in partially observable manipulation. Our benchmark and corresponding code are available at: \href{this https URL}{this https URL}.

---

## 5. Can Image Models Imagine Time? ImageTime: A Novel Benchmark for Probing Visual World Modeling Through Spatiotemporal Consistency

**Authors:** Xinrui Wu, Lichen Huang
**arXiv:** [2606.10620](https://arxiv.org/abs/2606.10620)
**Categories:** Computer Vision and Pattern Recognition (cs.CV); Artificial Intelligence (cs.AI)

Image generation models now produce high-quality static images, yet their ability to represent how a visual world changes over time remains poorly understood. Practical workflows such as storyboarding, step-by-step illustration, reference-guided editing, and video previsualization require models to preserve identities, objects, spatial relations, and causal order across multiple visual states. Existing evaluations largely measure single-image correctness, compositional alignment, or video quality, leaving open whether an image model can coherently imagine a temporally ordered process. We introduce ImageTime, a diagnostic benchmark that uses spatiotemporal consistency as a behavioral probe of visual world modeling in image generation. Given an action instruction, and optionally a reference image specifying the initial state, a model must generate one image containing four ordered key states: initial state, action onset, transition state, and final state. This four-keyframe protocol is more temporally demanding than single-image generation while avoiding the confounds of dense video dynamics. ImageTime organizes tasks with a progressive capability hierarchy and decomposes each scenario into stage-wise state predicates, cross-frame temporal constraints, and forbidden causal violations. GPT-5.5 scores all generated images under a structured VLM-as-judge protocol, producing interpretable capability scores, diagnostic subscores, and failure labels. Through multi-family benchmarking, ImageTime reveals where current image generation systems succeed, fail, and drift when asked to maintain coherent visual world states over time.

---

## 6. A Practical Recipe Towards Improving Sim-and-Real Correlation for VLA Evaluation

**Authors:** Shuo Wang, Hanyuan Xu, Yingdong Hu, Fanqi Lin, Yang Gao
**arXiv:** [2606.10366](https://arxiv.org/abs/2606.10366)
**Categories:** Robotics (cs.RO); Artificial Intelligence (cs.AI)

Simulation has become an essential tool for evaluating and improving vision-language-action (VLA) policies, offering scalable, reproducible, and controllable alternatives to costly real-world robot evaluation. Recent simulation benchmarks have made substantial progress on realism and diversity, yet these platforms have not been widely adopted as reliable proxies for real-world policy evaluation. In this work, we investigate this issue through the lens of sim-and-real correlation. We conduct a systematic study across multiple simulation platforms, VLA policies, tasks, and perturbation factors, measuring whether simulated evaluation preserves real-world conclusions in terms of policy ranking consistency, performance correlation, and perturbation-wise failure patterns. This analysis allows us to characterize the limitations of existing simulators and identify what kinds of simulation signals are more aligned with real-world deployment. We further examine how users should exploit simulation for policy improvement, including when simulator-based finetuning is beneficial and how the amount of post-training data affects sim-and-real alignment. Overall, our work provides a unified framework for measuring, interpreting, and improving the usefulness of simulation for VLA policies, offering guidance both for simulator designers and for practitioners who use simulation as part of the policy development pipeline.

---

## 7. What Matters in Orchestrating Robot Policies: A Systematic Study of Hierarchical VLA Agents

**Authors:** Jiaheng Hu, Mohit Shridhar, Caden Lu, ..., Jie Tan, Annie Xie
**arXiv:** [2606.10267](https://arxiv.org/abs/2606.10267)
**Categories:** Robotics (cs.RO); Artificial Intelligence (cs.AI); Machine Learning (cs.LG)

Hierarchical vision-language-action (Hi-VLA) systems have emerged as a promising paradigm for complex robot manipulation, by using high-level VLM planners to decompose tasks into language subgoals executed by low-level VLA controllers. Despite recent empirical progress, there is a lack of unified design principles for these systems: existing Hi-VLA systems differ in how they choose and connect planners, controllers, mechanisms to switch between the two, and how observations and memory are represented in the planner. In this paper, we present a systematic study of Hi-VLA design for robot manipulation. We unify representative Hi-VLA agents under an options-style control framework and benchmark core design choices across short-horizon, long-horizon, and reasoning-intensive tasks. Our analysis distills practical principles for building Hi-VLA systems, showing how model choices and interface mechanisms jointly shape performance. Applying these principles yields a substantially stronger system than either flat VLA control or a naively designed hierarchy, across experiments both in simulation and on a real ALOHA robot. Overall, our results provide a foundation for building more capable, robust, and principled hierarchical VLA agents. More information and video at this http URL.

---

## 8. Flow Control: Steering Vision-Language-Action Models with Simple Real-Time Inputs

**Authors:** Jonathan C. Kao, Jason Chan, Andy Wang
**arXiv:** [2606.10180](https://arxiv.org/abs/2606.10180)
**Categories:** Robotics (cs.RO); Artificial Intelligence (cs.AI); Human-Computer Interaction (cs.HC)

We introduce flow control of vision-language-action (VLA) models, a simple and effective way to steer VLA actions in real-time through generic inputs, such as a keyboard. This method can be used out-of-the-box and does not require retraining or fine-tuning VLAs. It enables relatively crude user inputs to steer a VLA to align with user intent. The VLA transforms these inputs into action samples drawn from the VLA expert action distribution learned during training, so that the generated actions are high quality (conformity to the action expert distribution) and high fidelity (reflecting the user's intent). We demonstrate that flow control has many desirable properties: (1) flow control accurately and responsively steers robot actions with user inputs, (2) it is robust to suboptimal user inputs, (3) it enables users to steer VLAs to achieve significantly higher success rates and faster task completion, and (4) fine-tuning a VLA on flow control trajectories improves the autonomous policy. Together, these results provide a simple and intuitive way for users to help steer VLA actions, increasing task performance.

---

## 9. BiWM: Advancing Open-Source Interactive Video World Models with Bidirectional Autoregression

**Authors:** Shaohao Rui, Xiaofeng Mao, Zhanyu Zhang, ..., Haibin Wan, Weijie Ma
**arXiv:** [2606.10135](https://arxiv.org/abs/2606.10135)
**Categories:** Computer Vision and Pattern Recognition (cs.CV); Artificial Intelligence (cs.AI)

Transitioning bidirectional video diffusion models into an autoregressive paradigm improves the interactivity of video world models, but existing causal pipelines need many stages (control fine-tuning, autoregressive training, causal initialization, few-step distillation) and still trail bidirectional models in quality due to error accumulation. Recent world models such as Yume-1.5 and Matrix-Game-3.0 instead adopt a bidirectional autoregressive approach, gaining fidelity and stable long-horizon rollout from self-correcting error propagation, yet open-source frameworks (e.g., minWM) support only causal models. We present BiWM, the first full-stack framework for interactive video world models under the bidirectional autoregressive paradigm, jointly optimizing generation quality and inference speed. From a pretrained video backbone, BiWM injects camera control by fine-tuning, then runs a few-step Distribution Matching Distillation (DMD) stage that turns the backbone into an action/camera-controllable world model: just two training stages instead of four in minWM, converging in a few hundred steps on 8xH200 GPUs. A single recipe spans Wan2.1-1.3B, Wan2.2-5B, HunyuanVideo-1.5-8B, and LTX-2.3-22B, and also supports secondary fine-tuning of existing bidirectional models. BiWM enables real-world camera control where minWM loses controllability, integrates pluggable history compression (FramePack-style and PackForcing-style) for long rollouts, and offers an optional NVFP4 4-bit training/inference pipeline. To counter DMD's mode-seeking degradation, we add GAN and mass-covering forward-KL objectives that preserve scene dynamics. We open-source BiWM for resource-constrained research and high-fidelity environment simulation.

---

## 10. One Lens, Many Worlds : A Capability-Typed Interface for World-Model Interpretability

**Authors:** Bhavith Chandra Challagundla, Sanskar Pandey, Param Thakkar, ..., Mohamed Deraz Nasr, Spursh Deshpande
**arXiv:** [2606.09936](https://arxiv.org/abs/2606.09936)
**Categories:** Machine Learning (cs.LG); Artificial Intelligence (cs.AI)

World models are now built on substantially different computational substrates. Latent recurrent state-space models such as PlaNet and the Dreamer family compress observations into recurrent states; token-based models such as IRIS quantize observations into a learned codebook and predict autoregressively with a transformer; and joint-embedding predictive architectures such as I-JEPA predict in a learned latent space with no pixel decoder. The interpretability methods applied to these models, including probing, activation patching, sparse autoencoders, and surprise analysis, share a common set of primitives, yet they are re-implemented from scratch for each architecture because existing hook-and-cache tooling assumes a transformer language model with no notion of actions, environment steps, or imagined rollouts. We argue that this fragmentation reflects the tooling rather than the models, and that the shared structure of world models is captured by a small typed interface. We present WorldModelLens, an open-source interpretability substrate organized around a capability-typed adapter: every model implements four required methods (encode, transition, initial state, sample) and declares a set of optional heads (decode, reward, continue, actor, critic) through an explicit capability descriptor, so that reinforcement-learning and self-supervised world models are first-class without either imitating the other. A single hook and cache layer exposes time-indexed activations, imagination rollouts, and intervention replay over this interface, allowing each analysis to be written once.

---

## 11. TacForeSight: Force-Guided Tactile World Model for Contact-Rich Manipulation

**Authors:** Yujie Zang, Yuhang Zheng, Xian Nie, ..., Shuicheng Yan, Wenchao Ding
**arXiv:** [2606.11184](https://arxiv.org/abs/2606.11184)
**Categories:** Robotics (cs.RO)

Contact-rich manipulation requires robots to continuously perceive and regulate evolving physical interactions under dynamic contact transitions or complex surface geometries. Recent imitation learning methods improve contact-aware control by incorporating tactile or force feedback, but they rarely model the asymmetric spatiotemporal roles of global force and local tactile sensing. To address this, we propose TacForeSight, a lightweight force-conditioned tactile foresight framework for real-time manipulation. The core component is TacForceWM, a tactile world model that predicts short-horizon tactile latent dynamics from dual-finger tactile observations conditioned on high-frequency wrist force and torque signals. Another key component, the Predictive Tactile-Conditioned Policy, leverages the predicted latents as anticipatory contact priors, models the current-to-future tactile evolution via cross-attention, and adaptively fuses visuo-tactile features through a tactile-guided gating module. By forecasting purely within a compact latent space, TacForeSight enables proactive contact reasoning with efficient real-time inference suitable for high-frequency manipulation control. Real-robot experiments on five representative tasks and three in-process perturbation settings show that TacForeSight consistently outperforms existing baselines, particularly under dynamic contact disturbances. All models and datasets will be made publicly available on the project website at this https URL.

---

## 12. VeriSpace: Spatially Grounded Action Verification for Vision-Language-Action Models

**Authors:** Guiyu Zhao, Longteng Guo, Junyou Zhu, ..., Xingjian He, Jing Liu
**arXiv:** [2606.10568](https://arxiv.org/abs/2606.10568)
**Categories:** Robotics (cs.RO)

Vision-language-action (VLA) models have shown strong promise for robotic manipulation, but their reliability at test time remains limited by one-shot action prediction, where even small action errors can cause grasp failure, collision, or incorrect task progression. A natural alternative is to equip VLA systems with test-time verification, allowing multiple candidate actions to be proposed and evaluated before execution. However, reliable action verification is challenging because it requires not only distinguishing subtle geometric differences between candidate actions, but also assessing whether an action makes meaningful progress toward the task goal. We present VeriSpace, a 3D-aware action verifier for test-time action selection in VLA systems. VeriSpace evaluates candidate actions through two key components: Dual-Path 3D-Injected Scene Encoding, which constructs a scene representation that jointly preserves visual semantics and explicit 3D geometry, and Spatially-Grounded Action Reasoning, which evaluates each action by reasoning over task-relevant spatial relations, geometric validity, and expected goal progress. Together, these components enable more reliable discrimination between subtle yet outcome-critical action candidates while remaining fully compatible with existing VLA policies. Experiments on public benchmarks and real-world robotic manipulation tasks show that VeriSpace consistently improves decision reliability over both underlying VLA policies and prior verification-based methods, yielding substantial gains in both in-distribution and out-of-distribution settings.

---

## 13. Uncovering Vulnerability of Vision-Language-Action Models under Joint-Level Physical Faults

**Authors:** Minsoo Jo, Taeju Kwon, Junha Chun, Youngjoon Jeong, Taesup Kim
**arXiv:** [2606.10501](https://arxiv.org/abs/2606.10501)
**Categories:** Robotics (cs.RO)

Deploying Vision-Language-Action (VLA) models in real robotic systems requires robustness not only to semantic and perceptual variations, but also to embodiment-side faults that change how actions are physically realized. Real robots can experience joint-level changes caused by actuator degradation, hardware faults, safety limits, collision damage, or wear-induced friction. These faults are critical because they alter the action-to-motion interface of a policy, disrupting the learned closed-loop relationship between commanded actions, realized motion, and subsequent observations. In this work, we study realistic joint-level physical faults and show that VLA models are vulnerable when predicted actions are executed through a perturbed robot body. Our analysis reveals joint-dependent effects, with heterogeneous degradation in task success across affected joints. We also show that performance drops cannot be attributed solely to physical infeasibility, since feasible faults such as increased joint friction can still substantially reduce success rates and induce closed-loop execution mismatch. Motivated by these findings, we propose Joint-level Physical-fault Aware Residual Calibrator (J-PARC), a lightweight residual calibration framework built on top of a frozen VLA policy. J-PARC infers a latent joint-fault regime from recent joint dynamics and conditions a shared residual calibrator on this regime, enabling adaptive action correction across faulty joints. Experiments show that J-PARC improves robustness under joint-level faults while preserving fault-free environment performance.

---

## 14. Act on What You See: Unlocking Safe Social Navigation in Vision-Language-Action Models

**Authors:** Qingzi Wang, Xiyang Wu, Guangyao Shi, ..., Xianfeng Yang, Dinesh Manocha
**arXiv:** [2606.10495](https://arxiv.org/abs/2606.10495)
**Categories:** Robotics (cs.RO)

Safe social navigation requires robots to distinguish people from ordinary obstacles and to react before danger becomes imminent. We show that pretrained Vision-Language-Action (VLA) models already encode pedestrian-object distinctions and future collision signals in their internal representations, but behavior cloning fails to translate these signals into socially appropriate actions. To address this mismatch, we propose SALSA, a two-stage annotation-free post-training framework: (1) social behavioral alignment bridges intermediate-layer social features to the action head and trains on counterfactual human-object scene pairs to break visual saliency shortcuts; (2) temporal safety alignment provides automatically generated future-risk supervision to enable anticipatory collision avoidance. On SCAND and real-world deployment, SALSA reduces near-collisions by 86.4% and improves social counterfactual accuracy from 53% to 93%, demonstrating that safer social navigation can be achieved by teaching VLA policies to act on representations they already possess. These results show that pretrained VLA policies can be adapted for safer social navigation by better aligning their latent representations with action generation.

---

## 15. HiMem-WAM: Hierarchical Memory-Gated World Action Models for Robotic Manipulation

**Authors:** Xiaoquan Sun, Ruijian Zhang, Chen Cao, ..., Mingqi Yuan, Jiayu Chen
**arXiv:** [2606.10363](https://arxiv.org/abs/2606.10363)
**Categories:** Robotics (cs.RO)

World Action Models (WAMs) have emerged as a new powerful paradigm for embodied intelligence, learning action-relevant visual dynamics that significantly enhance generalization and robustness. However, existing WAMs still struggle with task-relevant memory in long-horizon robotic manipulation. To address this, we present HiMem-WAM, a Hierarchical Memory-Gated WAM that integrates motion-centric latent actions, high-level skill latents, and boundary-triggered memory updates. Specifically, we develop a hierarchical latent action framework that jointly learns low-level motion and high-level skill latents, providing structured temporal abstraction. Meanwhile, a boundary-aware memory gate writes compact task states at predicted skill transitions, enabling causal inference without test-time generation of future video or optical flow estimation. Evaluated on LIBERO, LIBERO-PLUS, RMBench and real-world tasks, HiMem-WAM shows that hierarchical latents improve robustness under deployment perturbations, and the memory module substantially benefits memory-dependent long-horizon manipulation.

---

## 16. Efficient-WAM: A 1B-Parameter World-Action Model with Low-Cost Future Imagination

**Authors:** Jiajun Li, Tiecheng Guo, Yifan Ye, ..., Meng Guo, Shanghang Zhang
**arXiv:** [2606.10040](https://arxiv.org/abs/2606.10040)
**Categories:** Robotics (cs.RO)

World-Action Models (WAMs) have emerged as a promising paradigm for embodied control by coupling future visual prediction with action generation. However, most existing WAMs rely on photorealistic future prediction, which incurs high inference latency and makes real-time robot deployment difficult. This motivates a more efficient WAM design that preserves the control benefits of future visual prediction while reducing its inference cost. We introduce Efficient-WAM, a World-Action Model that reduces the cost of future imagination while preserving its control benefit. Efficient-WAM improves inference efficiency via a compact video expert transferred from WAN-2.2-5B, token-sparse video latents, and asymmetric video-action denoising that allocates fewer sampling steps to video than to actions. Instead of optimizing the future branch for visual fidelity, Efficient-WAM treats future video prediction as a compact guidance signal for action generation. Comprehensive experiments on RoboTwin 2.0 and real-world manipulation tasks show that Efficient-WAM maintains strong action performance despite visibly coarse future predictions. While maintaining competitive control capabilities, our 1B-parameter model can reduce per-chunk latency to around 100 ms during physical deployment, achieving a 30x speedup over existing WAMs.

---

## 17. SAFE-Pruner: Semantic Attention-Guided Future-Aware Token Pruning for Efficient Vision-Language-Action Manipulation

**Authors:** Shilin Ma, Chubin Zhang, Changyuan Wang, ..., Zheng Zhu, Yansong Tang
**arXiv:** [2605.29662](https://arxiv.org/abs/2605.29662)
**Categories:** Computer Vision and Pattern Recognition (cs.CV); Robotics (cs.RO)

Real-time inference of vision-language-action (VLA) models is essential for robotic control. While visual token pruning has shown strong potential for accelerating inference, most existing methods mainly base pruning decisions on shallow-layer cues and risk discarding visual information required by deep layers. To address this issue, we propose SAFE-Pruner, a plug-and-play pruning framework that incorporates attention cues of future layers into pruning decisions. Specifically, we identify semantic attention consistency, the tendency that VLA models concentrate their attention probability mass on the same semantic entity across execution steps. Based on this observation, we design a forward-looking strategy to forecast the token saliency in deep layers, which prevents the premature removal of critical tokens and leads to more stable acceleration. We further introduce an adaptive subtask division strategy to detect abrupt attention shifts, thereby improving forecasting accuracy and pruning reliability. Extensive experiments in simulation and real-world settings demonstrate that our method achieves up to 1.89x speedup with a minimal degradation in success rate of less than 1.7%, while outperforming state-of-the-art methods by up to 1.9%.

---

## 18. Next Forcing: Causal World Modeling with Multi-Chunk Prediction

**Authors:** Gangwei Xu, Qihang Zhang, Jiaming Zhou, ..., Xin Yang, Yinghao Xu
**arXiv:** [2606.11187](https://arxiv.org/abs/2606.11187)
**Categories:** Computer Vision and Pattern Recognition (cs.CV)

Autoregressive video generation has emerged as a powerful paradigm for World Action Models (WAMs). However, existing approaches suffer from slow training convergence and limited converged accuracy, particularly at high frame rates, as the training supervision is confined to the current chunk without explicit signals about future dynamics; they also suffer from slow inference due to iterative video denoising. In this paper, we present Next Forcing, a multi-chunk prediction (MCP) framework for causal world modeling that enables faster training, higher accuracy, and accelerated inference. Inspired by multi-token prediction in large language models, Next Forcing introduces an MCP training objective that augments the main model with lightweight auxiliary MCP modules to simultaneously denoise video chunks at multiple future temporal horizons (next$^1$, next$^2$, next$^3$ chunks). These MCP modules form a causal chain across prediction depths, where intermediate features fused from multiple layers of the main model are leveraged to predict future dynamics, allowing near-future predictions to inform farther-future ones and providing dense multi-scale temporal supervision back to the main model. During training, the MCP modules significantly accelerate convergence and improve converged accuracy, especially at high frame rates: at 50 fps, Next Forcing achieves a 93.1% relative improvement over LingBot-VA at 5k training steps and 2.3x faster convergence, and establishes new state-of-the-art results on the RoboTwin benchmark (94.1/93.5% on Clean/Random). At inference, the MCP modules can be retained to predict the next video chunk in parallel with the current one, achieving 2x inference acceleration. Next Forcing also demonstrates significant improvements on PhyWorld, a benchmark evaluating adherence to physical laws in video generation, and over 50% FVD reduction on general video pretraining.

---

## 19. WorldOlympiad: Can Your World Model Survive a Triathlon?

**Authors:** Yuke Zhao, Wangbo Zhao, Weijie Wang, ..., Wei Wang, Bohan Zhuang
**arXiv:** [2606.11129](https://arxiv.org/abs/2606.11129)
**Categories:** Computer Vision and Pattern Recognition (cs.CV)

We introduce WorldOlympiad, a benchmark for diagnosing video-based world models across physical faithfulness, geometric consistency, and interaction fidelity. While existing benchmarks often focus on visual quality, semantic alignment, or short-term temporal coherence, they provide limited insight into whether generated videos obey physical rules, preserve coherent 3D structure, and sustain controllable interactions over long horizons. To address this gap, WorldOlympiad decomposes world-model evaluation into three complementary dimensions. The physical track uses object segmentation and MLLM-as-judge to assess whether generated videos follow interpretable rules in mechanics, thermal phenomena, and material properties. The geometry track reconstructs generated videos with Gaussian splatting and evaluates structural consistency, cross-view coherence, and camera-trajectory alignment. The interaction track assesses whether generated rollouts follow complex action prompts and maintain smooth, coherent transitions across consecutive video chunks. WorldOlympiad further covers three major downstream scenarios, including gaming, robotics, and general real-world videos, capturing diverse challenges from interactive control and embodied manipulation to open-domain motion and camera dynamics. Together, these tracks and scenarios form a scalable and interpretable evaluation suite that exposes failure modes beyond generic video quality. Experiments on state-of-the-art models reveal substantial gaps in physical reasoning, 3D consistency, and long-horizon interaction, underscoring the need for more structured evaluation protocols for generative world models.

---

## 20. Dexterous Point Policy: Learning Point-based Dexterous Hand Policies from Human Demonstrations

**Authors:** Beomjun Kim, Seong Hyeon Park, Seunghoon Sim, ..., Sanghyeok Lee, Jinwoo Shin
**arXiv:** [2606.10614](https://arxiv.org/abs/2606.10614)
**Categories:** Robotics (cs.RO); Computer Vision and Pattern Recognition (cs.CV); Machine Learning (cs.LG)

Robotic foundation models pre-trained on human demonstration videos have shown promise, but a significant embodiment gap remains when the resulting policies are deployed on real robots. A common remedy is to fine-tune these models on robot-specific demonstrations. However, robot data collection can be prohibitively expensive and time-consuming, which is particularly acute in dexterous manipulation, e.g., teleoperating a multi-fingered hand for even a single atomic task can take days. To address this, we introduce Dexterous Point Policy, a framework that learns dexterous manipulation policies directly from human videos and requires no robot demonstrations. Our core insight is that a unified 3D keypoint representation can bridge human and robot embodiments when used for both observations and actions. Specifically, we extract 3D keypoints of task-relevant objects and human hands from raw videos, and train an autoregressive transformer over these keypoints. We observe that at the keypoint level, specifically the wrist and fingertips, human and robot behaviors closely align, enabling direct policy transfer. On a suite of real-robot tasks spanning pick-and-place and tool use, Dexterous Point Policy attains 75.0% success, whereas a state-of-the-art VLA baseline reaches only 1.0%. Furthermore, our method generalizes strongly to unseen scenarios, including multi-object environments and novel object categories.

---
