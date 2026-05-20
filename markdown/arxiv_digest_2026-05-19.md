# arXiv Daily Digest — 2026-05-19

**Mode:** direct
**Categories:** cs.AI, cs.LG, cs.RO, cs.CV
**Keywords:** VLA, world model, world action model
**Papers found:** 31

---

## 1. ECG-WM: A Physiology-Informed ECG World Model for Clinical Intervention Simulation

**Authors:** Zhikang Chen, Yue Wang, Sen Cui, ..., Tianling Ren, Tingting Zhu
**arXiv:** [2605.17580](https://arxiv.org/abs/2605.17580)
**Categories:** Artificial Intelligence (cs.AI)

Electrocardiogram (ECG)-based models have achieved strong performance in diagnostic tasks, yet they remain limited in modeling how cardiac dynamics evolve under external interventions. In particular, existing approaches focus primarily on static prediction and lack mechanisms to capture ECG variations under different pharmacological conditions. In this work, we propose an ECG World Model for action-conditioned predictive simulation of cardiac electrophysiology. Moving beyond disjoint pipelines, our framework features a principled integration of physiological ordinary differential equation (ODE) priors into latent diffusion dynamics via energy regularization. This structural constraint enables the synthesis of physiologically plausible post-intervention ECG trajectories while effectively mitigating generative hallucinations. Building on this simulation process, we introduce an uncertainty-aware evaluation strategy that leverages the stochasticity of diffusion sampling to characterize both the expected clinical risk and its variability, allowing a more reliable comparative assessment of candidate interventions. We evaluate our method across diverse settings, including controlled drug-response scenarios and real-world clinical records. Beyond standard waveform metrics, experimental results demonstrate improved risk calibration and strong alignment with expert-informed treatment preferences. These results establish our approach as a robust foundation for safe and intervention-aware clinical decision support.

---

## 2. Self-supervised Hierarchical Visual Reasoning with World Model

**Authors:** Yuanfei Xu, Lin Liu, Wengang Zhou, Mingxiao Feng, Houqiang Li
**arXiv:** [2605.17537](https://arxiv.org/abs/2605.17537)
**Categories:** Artificial Intelligence (cs.AI)

3D open-world environments with adversarial opponents remain a core challenge for reinforcement learning due to their vast state spaces. Effective reasoning representations are essential in such settings. While existing self-supervised visual foresight reasoning approaches often suffer from multi-step error accumulation, many recent studies resort to injecting domain-specific knowledge for more stable guidance. Our key insight is that the photorealistic fidelity of visual reasoning representations is secondary; what truly matters is providing informative, task-relevant signals. To this end, we propose ResDreamer, a hierarchical world model in which each higher-level layer is trained to reconstruct the residuals of the layer below. This design enables progressive abstraction of increasingly sophisticated world dynamics and fosters the emergence of richer latent representations. Drawing inspiration from the "Bitter Lesson", ResDreamer trains its reasoning representations in a purely self-supervised manner. The higher-level residual representations are used to modulate lower-level predictions, allowing the world model to scale effectively with only linearly increasing cross-layer communication costs. Experiments show that ResDreamer achieves state-of-the-art sample efficiency and parameter efficiency. This scalable hierarchical visual foresight reasoning architecture paves the way for more capable online RL agents in open-ended, dynamic environments. The code is accessible at \url{this https URL}.

---

## 3. Is VLA Reasoning Faithful? Probing Safety of Chain-of-Causation

**Authors:** Nicanor Mayumu, Xiaoheng Deng, Patrick Mukala
**arXiv:** [2605.17268](https://arxiv.org/abs/2605.17268)
**Categories:** Artificial Intelligence (cs.AI); Computer Vision and Pattern Recognition (cs.CV); Robotics (cs.RO)

We present the first systematic study of faithfulness in Vision-Language-Action (VLA) driving models, analyzing 300 Alpamayo-R1-10B inferences across 100 diverse PhysicalAI-AV scenarios. Our main finding is that output natural-language rationales with trajectories may be significantly unfaithful: (i) overall reasoning fidelity is only 42.5%, with Chain-of-Causation matching scene reality less than half the time; (ii) 94 missed pedestrians in one-third of pedestrian-relevant scenes; (iii) 97.7% trajectory fragility under mild visual perturbations; and (iv) only 48.3% mean reasoning-action consistency, with 53.3% of inferences exhibiting low consistency, including 37.9% of stop-claimed cases where the model continues instead. We formalize faithfulness information-theoretically, define entity and action fidelity with verification criteria, and outline a four-component safety architecture aligned with these results.

---

## 4. From Static Risk to Dynamic Trajectories: Toward World-Model-Inspired Clinical Prediction

**Authors:** Pujun Feng, Xiaoyu Guo, Seyed Ehsan Saffari, ..., Yue Sun, Bin Cui
**arXiv:** [2605.16927](https://arxiv.org/abs/2605.16927)
**Categories:** Artificial Intelligence (cs.AI)

Clinical decision-making is a feedback system where risk estimates influence treatment, which in turn changes disease trajectories, and both shape clinicians' measurement practices. Static prediction often fails clinically: models trained on observational care logs conflate disease biology with clinician behavior, particularly under treatment confounder feedback and irregular or informative observation. This Review focuses on intervention-aware disease trajectory modeling in clinical AI--methods estimating patient-specific longitudinal disease evolution and assessing trajectory changes under alternative treatments. We organize the field around six linked components: three decision tasks (factual forecasting, counterfactual estimation, policy evaluation) and three data-generating mechanisms (disease evolution, treatment assignment, observation process) that determine identifiability. We present the first unified framework bridging forecasting, counterfactual trajectories, and policy evaluation across discrete/continuous time, explicitly addressing treatment assignment, time-varying confounding, and observation bias. We synthesize key method families (multistate/joint models, temporal point-process, deep sequence architectures, longitudinal causal inference), map them to relevant components, and align evaluation with claim strength via overlap diagnostics, uncertainty quantification, off-policy robustness, and target-trial validation. This synthesis advances benchmark prediction to decision-grade clinical evidence, enabling treatment-sensitive individualized futures, pre-deployment policy stress-testing, and safer closed-loop learning health systems that adapt/abstain when evidence is insufficient.

---

## 5. Baba in Wonderland: Online Self-Supervised Dynamics Discovery for Executable World Models

**Authors:** SeungWon Seo, DongHeun Han, SeongRae Noh, HyeongYeop Kang
**arXiv:** [2605.16725](https://arxiv.org/abs/2605.16725)
**Categories:** Artificial Intelligence (cs.AI)

Executable world models can be read, edited, executed, and reused for planning, but only if the program captures the environment's transition law rather than semantic shortcuts in its surface vocabulary. We study online executable world-model learning under prior misalignment, where an agent must induce state-dependent dynamics from interaction evidence alone, without rule descriptions, reward signals, or trustworthy lexical priors. We introduce Alice, a closed-loop system that treats failed candidate updates as structural signal: when a candidate explains a new transition but loses previously explained ones, the preservation conflict reveals dynamics that the current program had conflated. Alice refines these conflicts into hypothesis classes that both provide compact, class-stratified preservation counterexamples for update and guide frontier exploration toward transitions that are novel and underrepresented with respect to the current program. We evaluate Alice on Baba in Wonderland, a prior-misaligned variant of Baba Is You that preserves simulator dynamics while replacing semantically meaningful rule-property labels with unrelated words. Experiments show that Alice substantially improves executable world-model learning under prior misalignment, and ablations show that both class refinement and class-aware exploration contribute.

---

## 6. PH-Dreamer: A Physics-Driven World Model via Port-Hamiltonian Generative Dynamics

**Authors:** Xueyu Luan, Chenwei Shi
**arXiv:** [2605.18303](https://arxiv.org/abs/2605.18303)
**Categories:** Machine Learning (cs.LG); Artificial Intelligence (cs.AI); Computer Vision and Pattern Recognition (cs.CV); Robotics (cs.RO)

World models built on recurrent state space architectures enable efficient latent imagination, yet remain physically unstructured, producing dynamics that violate conservation and dissipative principles. We introduce a unified Port-Hamiltonian framework that remedies this through three synergistic mechanisms. First, we embed implicit physical priors into recurrent transitions by modeling projected latent evolution as action controlled energy routing governed by flow and dissipation, biasing the projected PH phase space toward a more compact and physically structured representation. Second, we develop a kinematics aware energy world model that estimates the Hamiltonian and power balance from proprioceptive observations, providing an explicit physical signal for thermodynamic reasoning. Third, leveraging these energy gradients, we establish an energy guided Actor-Critic that uses Lagrangian multipliers to regularize policy optimization toward lower energy and smoother control. Across visual control benchmarks, this paradigm not only attains superior asymptotic returns but also elevates internal simulator fidelity by establishing a tighter, lower variance alignment between imagined and real rewards, all while reducing latent phase space volume by 4.18-8.41%, energy consumption by up to 7.80%, and mean squared jerk by up to 9.38%.

---

## 7. Event-Grounded Sparse Autoencoders for Vision-Language-Action Policies

**Authors:** Xinchen Jin, Aditya Chatterjee, Pranav Kumar, Rohan Paleja
**arXiv:** [2605.17204](https://arxiv.org/abs/2605.17204)
**Categories:** Robotics (cs.RO); Artificial Intelligence (cs.AI)

Vision-Language-Action (VLA) policies translate language and visual inputs into robot actions, where their hidden representations directly shape closed-loop behavior. However, mechanistic interpretability tools from language and vision-language models do not transfer cleanly to VLAs: outputs are robot actions rather than human-readable tokens, and interventions can only be tested via expensive closed-loop rollouts. We propose an event-grounded interpretability pipeline that anchors SAE feature analysis to behavioral events rather than text contexts. End-effector keyframes are clustered within each task using visual, state, and temporal cues, linking SAE features to behaviorally salient events and, via optional VLM annotations, to semantic context. To our knowledge, our pipeline is among the first to ground SAE-based VLA analysis in closed-loop behavioral events. Across two simulation architectures and a real-robot study, event-grounded ranking yields the strongest causal effects on OpenVLA and transfers to the continuous action chunks of $\pi_{0.5}$. SAE is a sparse but imperfect intervention basis: usability varies with architecture and intervention site, and aggressive intervention reveals safety and interpretability limits. Overall, event-grounded SAE analysis emerges as a practical starting point for behavior-anchored VLA interpretability, motivating future work on SAE features beyond action-aligned coordinates, finer-grained closed-loop evaluation, and safe interventions for high-stakes VLA deployments. Code is available at \url{this https URL}.

---

## 8. Contrastive Conceptor Activation Steering (COAST): Unlocking Vision-Language-Action Models through Hidden States

**Authors:** Miranda Muqing Miao, Subin Kim, Brandon Yang, Lyle Ungar
**arXiv:** [2605.17144](https://arxiv.org/abs/2605.17144)
**Categories:** Robotics (cs.RO); Artificial Intelligence (cs.AI); Machine Learning (cs.LG)

Vision-Language-Action (VLA) models leverage powerful perceptual priors from web-scale Vision-Language Model (VLM) pre-training, yet they remain surprisingly brittle in practice, frequently failing at simple robotic tasks. To mitigate this, we propose Contrastive Conceptor Activation Steering (COAST). COAST builds on the notion of a "conceptor", a linear operator that soft-projects data into the principal components of a target distribution. COAST uses conceptors to identify success-critical subspaces for a target robotic task from a few examples of success and failure rollouts. At inference time, it steers VLA latents into these identified success subspaces to improve task outcomes. Across three architecturally distinct neural policies (flow-matching VLA, autoregressive VLA, and Diffusion Policy), COAST improves absolute mean simulation and real-robot task success rate by over 20 and 40% respectively. The activation subspace geometry reveals that failure modes share substantial structure across tasks while success representations remain largely task-specific. When tasks share similar failure modes, this structure enables previously fitted conceptors to improve performance on new tasks without refitting. Ultimately, our results suggest that current VLAs retain substantial task-relevant knowledge in their latent representations, and that the action expert's decoding bottleneck could be mitigated by steering its residual stream toward task-relevant subspaces. COAST provides a lightweight, training-free path to unlocking these latent capabilities by steering the model towards its own "success" distributions.

---

## 9. GeoWorld-VLM: Geometry from World Models for Vision-Language Models

**Authors:** Renjie Gu, Kaichen Zhou, Yan Luo, Mengyu Wang
**arXiv:** [2605.16713](https://arxiv.org/abs/2605.16713)
**Categories:** Computer Vision and Pattern Recognition (cs.CV); Artificial Intelligence (cs.AI)

Modern Vision-Language Models (VLMs) achieve strong semantic recognition, yet remain brittle on elementary spatial relations such as left of, on, behind, and between. One cause of this failure arises before language reasoning begins: the visual pathway may compress or discard critical 3D structural cues during feature extraction, so the language model receives image representations that are already insufficient for reliable spatial judgment. We introduce GeoWorld-VLM, a VLM-side distillation framework that transfers geometric structure from frozen camera-conditioned video world models into VLMs. GeoWorld-VLM fine-tunes only the image encoder and multimodal projector, aligning post-projector image features with intermediate world-model representations while leaving the main backbone frozen. Given images, a prompt, and a sampled camera trajectory, the world-model teacher converts static visual input into a synthetic multi-view spatial signal. Training combines spatial answer supervision, teacher-student feature alignment, and a preservation anchor to the original VLM. Since the language model remains frozen, GeoWorld-VLM preserves the original model's linguistic capabilities while attributing spatial improvements to the enhanced visual pathway. To evaluate the effectiveness and generality of the proposed method, we apply GeoWorld-VLM to two distinct VLM architectures and observe consistent improvements across both backbones. GeoWorld-VLM improves performance by approximately 4 percent on both the What'sUp and VSR benchmarks, suggesting that world-model-guided visual alignment generalizes across model structures and spatial reasoning datasets.

---

## 10. Identifiable Token Correspondence for World Models

**Authors:** Youngin Kim, Ray Sun, Inho Kim, Bumsoo Park, Hyun Oh Song
**arXiv:** [2605.16457](https://arxiv.org/abs/2605.16457)
**Categories:** Machine Learning (cs.LG); Artificial Intelligence (cs.AI); Computer Vision and Pattern Recognition (cs.CV)

Transformer-based world models have shown strong performance in visual reinforcement learning, but often suffer from temporal inconsistency in long-horizon rollouts, including object duplication, disappearance, and transmutation. A key reason is that most existing approaches treat next-frame prediction purely as a token generation problem, without explicitly modeling correspondence between tokens across time. We formulate next-frame prediction as a structured probabilistic inference problem with latent token correspondence variables, deriving a model in which each next-frame token is explained either by copying a token from the previous frame or by generating a new token. Our experiments show state-of-the-art performance on 4 challenging benchmarks. The proposed method achieves a return of 72.5% and a score of 35.6% on the Craftax-classic benchmark, significantly surpassing the previous best of 67.4% and 27.9%. We release our source code on this https URL.

---

## 11. World Model-Enabled Causal Digital Twins for Semantic Communications in Physical AI Systems

**Authors:** Lingyi Wang, Tingyu Shui, Walid Saad, Pascal Adjakple
**arXiv:** [2605.16547](https://arxiv.org/abs/2605.16547)
**Categories:** Machine Learning (cs.LG)

Semantic communication has emerged as a promising paradigm for enabling goal-oriented networking. However, most existing semantic communication solutions are tailored to one-shot tasks and optimize instantaneous performance. Hence, they cannot be used to support closed-loop dynamic systems with physical artificial intelligence (AI), in which the transmitted semantics affect not only the current inference outcome but also future control actions, state evolution, and ultimately long-horizon task performance. To address this gap, this paper investigates goal-oriented semantic communications for physical AI systems with closed-loop sensing-communication-inference-control. In particular, the problem of semantic communications is formulated as a long-term return-per-bit maximization under wireless bit-budget constraints while capturing both control efficiency and communication efficiency. To solve this problem, a novel causal information value (CIV) metric is introduced to evaluate the marginal contribution of each semantic token to the expected long-term return by transmission interventions. Then, a world-model-enabled causal digital twin (WM-CDT) framework is proposed to capture the dynamics of closed-loop physical AI systems and enable counterfactual reasoning for long-horizon imagined rollouts. Based on these imagined rollouts, an actor-critic policy is trained for long-horizon agent control with high data efficiency, while the semantic token selector is trained through CIV-per-bit evaluation. Extensive simulations on an AirSim-Sionna-based unmanned aerial vehicle (UAV) navigation simulator show that the proposed WM-CDT framework achieves significant improvement in return-per-kbit and navigation success rate compared to existing reinforcement learning solutions.

---

## 12. DyGRO-VLA: Cross-Task Scaling of Vision-Language-Action Models via Dynamic Grouped Residual Optimization

**Authors:** Sixu Lin, Yunpeng Qing, Litao Liu, ..., Xiaoyi Fan, Guiliang Liu
**arXiv:** [2605.17486](https://arxiv.org/abs/2605.17486)
**Categories:** Robotics (cs.RO); Machine Learning (cs.LG)

Recent progress in Reinforcement Learning (RL) provides a principled approach to optimizing Vision-Language-Action (VLA) models, facilitating a shift from trajectory imitation to active learning in the task environment. Despite improvements in control precision, most RL optimizers remain task-specific, which reduces VLA models from generalist controllers to policies that overfit to a narrow set of tasks. In this study, we conduct an in-depth analysis of this phenomenon and highlight the importance of cross-task feature representations for improving the generalizability of VLA models. Motivated by this finding, we introduce DyGRO-VLA, a two-stage optimization framework that 1) effectively captures cross-task latent representations based on information-theoretic principles, and 2) dynamically refines policy optimization via a mixture-of-RL-residuals. DyGRO-VLA enables the RL optimizer to exploit task-relevant latent information while strategically mitigating adverse interference on the learned representations throughout the optimization process. We evaluate our approach on LIBERO, RoboTwin2 benchmarks, and further validate it on real world, demonstrating consistent improvements over strong baselines under multi-task training and distribution shift.

---

## 13. OrbiSim: World Models as Differentiable Physics Engines for Embodied Intelligence

**Authors:** Jiajian Li, Jingyuan Huang, Junru Gong, ..., Xiaokang Yang, Yunbo Wang
**arXiv:** [2605.16395](https://arxiv.org/abs/2605.16395)
**Categories:** Robotics (cs.RO); Machine Learning (cs.LG)

We present OrbiSim, a novel robotic simulation paradigm that redefines world models as a fully differentiable physics engine for embodied intelligence. Unlike prior world models that focus on unconstrained imagination in latent or visual domains, OrbiSim establishes a unified, physically-grounded pathway that bridges structured scene assets, neural dynamics, and downstream reinforcement learning. By enabling end-to-end differentiability throughout the entire simulation loop -- spanning from explicit state transitions to visual observation generation -- OrbiSim supports tasks traditionally intractable for classical simulators, such as differentiable contact modeling, gradient-based policy optimization under sparse rewards, and intuitive physical inference. Empirical results demonstrate that OrbiSim significantly outperforms state-of-the-art world models in both predictive fidelity and control performance. Furthermore, its consistent responsiveness to asset configurations and physical parameters suggests its potential as a differentiable tool for enhancing robot simulation and policy training.

---

## 14. Dexora: Open-source VLA for High-DoF Bimanual Dexterity

**Authors:** Zongzheng Zhang, Jingrui Pang, Zhuo Yang, ..., Hongyang Li, Hao Zhao
**arXiv:** [2605.18722](https://arxiv.org/abs/2605.18722)
**Categories:** Robotics (cs.RO)

Vision-Language-Action (VLA) models have recently become a central direction in embodied AI, but current systems are restricted to either dual-gripper control or single-arm dexterous hand manipulation. While low-dimensional gripper control can often be handled with simpler methods, high-dimensional dexterous hand control benefits greatly from full end-to-end VLA learning. In this work, we introduce Dexora, the first open-source VLA system that natively targets dual-arm, dual-hand high-DoF manipulation. We design a hybrid teleoperation pipeline that decouples gross arm kinematics (captured with a custom exoskeleton backpack) from fine finger motion (markerless hand tracking via Apple Vision Pro), and that drives both a physical dual-arm dual-hand platform and an identical MuJoCo digital twin. Using that interface, we assemble a large training corpus: an embodiment-matched synthetic corpus (100K simulated trajectories, 6.5M frames) and a real-world dataset of 10K teleoperated episodes (2.92M frames). To mitigate noisy teleoperation demonstrations, we propose a data-quality-aware training recipe: an offline discriminator provides clip-level weights for diffusion-transformer policy training, down-weighting low-quality demonstrations. Empirically, Dexora outperforms competitive VLA baselines on both basic and dexterous benchmarks (e.g., average dexterous success 66.7% vs. 51.7%), attains 90% success on basic tasks, and shows robust out-of-distribution and cross-embodiment generalization. Ablations confirm the importance of real data and the discriminator for dexterity.

---

## 15. WorldArena 2.0: Extending Embodied World Model Benchmarking on Modality, Functionality and Platform

**Authors:** Yu Shang, Yinzhou Tang, Yiding Ma, ..., Chen Gao, Yong Li
**arXiv:** [2605.17912](https://arxiv.org/abs/2605.17912)
**Categories:** Robotics (cs.RO); Computer Vision and Pattern Recognition (cs.CV)

World models have emerged as a central paradigm for embodied intelligence, enabling agents to predict action-conditioned future and reason about environmental dynamics. However, existing embodied world model benchmarks are still largely confined to vision-only prediction, offline embodied applications, and simulator-based evaluation, making them insufficient for assessing increasingly comprehensive world models. In this work, we introduce WorldArena 2.0, an expanded benchmark that systematically broadens embodied world model evaluation along three dimensions: modality, functionality, and platform. Along the modality dimension, WorldArena 2.0 extends evaluation from vision-only to visuotactile modalities, enabling assessment of multimodal perception and prediction. Along the functionality dimension, it extends beyond policy evaluation and planning to assess world models as interactive RL environments for policy optimization. Along the platform dimension, it moves beyond simulator-only evaluation to a diverse suite of simulated and real-world robotic settings across multiple embodiments. Under a standardized protocol, WorldArena 2.0 comprehensively evaluates perceptual quality, interactive utility, and cross-platform performance, providing a comprehensive testbed for tracking progress toward embodied world models. The benchmark is available at: this https URL.

---

## 16. RoboFlow4D: A Lightweight Flow World Model Toward Real-Time Flow-Guided Robotic Manipulation

**Authors:** Sixu Lin, Junliang Chen, Huaiyuan Xu, ..., Lap-Pui Chau, Guiliang Liu
**arXiv:** [2605.17522](https://arxiv.org/abs/2605.17522)
**Categories:** Robotics (cs.RO)

Planning and acting in 3D environments is a fundamental capability for robotic manipulation in the real world. Although prior work has explored predictive flow planners to guide 3D manipulation, existing approaches often rely on modular pipelines stacking multiple submodels, resulting in high computational overhead and limited real-time performance. To address these challenges, we introduce RoboFlow4D, a lightweight flow world model that unifies perception and planning by estimating temporal motion in physical 3D space. As an end-to-end framework, RoboFlow4D directly predicts multi-frame 3D flows from visual observations and textual instructions, providing explicit flow-based planning to guide action generation. This design allows seamless integration with general action policies, forming an efficient observation-planning-execution closed loop. Through slow-fast collaboration between flow prediction and action control, RoboFlow4D enables real-time and resource-efficient manipulation. Extensive experiments in both simulation and real-world settings demonstrate that RoboFlow4D consistently improves manipulation success rates and computational efficiency, advancing flow-guided planning for embodied intelligence.

---

## 17. AffordVLA: Injecting Affordance Representations into Vision-Language-Action Models via Implicit Feature Alignment

**Authors:** Weijie Kong, Zhian Su, Wei Yu, Huixu Dong
**arXiv:** [2605.17517](https://arxiv.org/abs/2605.17517)
**Categories:** Robotics (cs.RO)

Recent advances in Vision-Language-Action (VLA) models have shown strong potential for general-purpose robotic manipulation. However, the visual representations of most VLA models are often dominated by global object appearance and struggle to focus on task-relevant functional interaction regions, which limits their robustness in unstructured environments. Existing affordance-based methods typically rely on explicit mask injection or external perception modules, requiring additional annotations while introducing cascading perception errors and inference overhead. To address these limitations, we propose AffordVLA, an affordance-enhanced VLA framework that internalizes manipulation-centric affordance perception into VLA visual representations through implicit representation alignment. Specifically, we construct a zero-shot affordance teacher to extract task-conditioned affordance visual representations from RGB observations and language instructions. AffordVLA aligns the intermediate visual representations of the VLA with the affordance visual representations extracted by the teacher, thereby implicitly injecting manipulation-centric affordance perception into VLA visual representations and improving action accuracy. Extensive simulation and real-world experiments demonstrate that AffordVLA and its affordance teacher achieve state-of-the-art performance and outperform strong baselines. Ablation analyses show that AffordVLA effectively reshapes VLA visual representations while preserving inference efficiency, leading to improved manipulation success rates and training efficiency.

---

## 18. StableVLA: Towards Robust Vision-Language-Action Models without Extra Data

**Authors:** Yiyang Fu, Chubin Zhang, Shukai Gong, ..., Jianan Wang, Daquan Zhou
**arXiv:** [2605.18287](https://arxiv.org/abs/2605.18287)
**Categories:** Computer Vision and Pattern Recognition (cs.CV); Robotics (cs.RO)

It is infeasible to encompass all possible disturbances within the training dataset. This raises a critical question regarding the robustness of Vision-Language-Action (VLA) models when encountering unseen real-world visual disturbances, particularly under imperfect visual conditions. In this work, we conduct a systematic study based on recent state-of-the-art VLA models and reveal a significant performance drop when visual disturbances absent from the training data are introduced. To mitigate this issue, we propose a lightweight adapter module grounded in information theory, termed the Information Bottleneck Adapter (IB-Adapter), which selectively filters potential noise from visual inputs. Without requiring any extra data or augmentation strategies, IB-Adapter consistently improves over the baseline by an average of 30%, while adding fewer than 10M parameters, demonstrating notable efficiency and effectiveness. Furthermore, even with a 14x smaller backbone (0.5B parameters) and no pre-training on the Open X-Embodiment dataset, our model StableVLA achieves robustness competitive with 7B-scale state-of-the-art VLAs. With negligible parameter overhead (<10M), our approach maintains accuracy on long-horizon tasks and surpasses OpenPi under both synthetic and physical visual corruptions.

---

## 19. Incantation: Natural Language as the Action Interface for Multi-Entity Video World Models

**Authors:** Shangwen Zhu, Qianyu Peng, Zhao Pu, ..., Fan Cheng, Ruili Feng
**arXiv:** [2605.18601](https://arxiv.org/abs/2605.18601)
**Categories:** Computer Vision and Pattern Recognition (cs.CV)

Modern interactive video world models have achieved impressive visual fidelity, yet lack fine-grained multi-entity control and cross-entity, cross-world generalization. We trace this gap to the action interface: standard control protocols (e.g. animation IDs, device inputs, scene-level captions) bind action semantics to specific entities or engines at design time. We propose natural language as the interface to unlock expressiveness that no prior interface can achieve, and we present Incantation, the first interactive video world model with per-latent-frame (0.25 s) natural-language conditioning that supports simultaneous multi-entity control and concept-level cross-entity transfer beyond any fixed rendering pipeline. We pair a pretrained bidirectional video backbone with frame-local text cross-attention, and enable real-time long-horizon streaming through ODE-initialized Self-Forcing distillation with a RoPE-decoupled sliding KV-cache. We surpass the Action-Index baseline on cross-entity transfer (89% vs. 43%) and out-of-vocabulary prompts (90% vs. 0%), and our 2-step student sustains 19.7 FPS at 480p with stable FVD over 2-hour rollouts. We further apply the same architecture and training recipe to The King of Fighters, changing only the per-entity action vocabulary slots. We have released a preview subset of the Incantation dataset at this https URL, containing manually collected Elden Ring player-boss combat clips with structured action-oriented metadata. Larger-scale Elden Ring and KOF data will be released with the full project.

---

## 20. Xiaomi EV World Model: A Joint World Model Integrating Reconstruction and Generation for Autonomous Driving

**Authors:** Lijun Zhou, Hongcheng Luo, Zhenxin Zhu, ..., Bing Wang, Haiyang Sun
**arXiv:** [2605.18137](https://arxiv.org/abs/2605.18137)
**Categories:** Computer Vision and Pattern Recognition (cs.CV)

This report presents a unified technical system addressing the two core capabilities of world models for autonomous driving: world representation and world generation. For world representation, we propose WorldRec, a feed-forward reconstruction architecture driven by sparse scene queries. WorldRec initializes structured queries in 3D space, leveraging them to aggregate cross-view, cross-temporal features, thereby naturally enforcing spatial consistency across frames and yielding compact yet high-fidelity 3D Gaussian scene representations. For world generation, we propose WorldGen, a two-stage training framework of bidirectional pretraining followed by causal fine-tuning through three progressive stages (Teacher Forcing, ODE distillation, and DMD), enabling high-quality online causal video generation in as few as 4 denoising steps. Building on both modules, we further introduce the JWM, which deeply integrates WorldRec and WorldGen to achieve synergistic gains in generation stability, cross-frame consistency, and visual fidelity, providing a solid foundation for closed-loop simulation, data synthesis, and end-to-end training in autonomous driving.

---

## 21. PanoWorld: A Generative Spatial World Model for Consistent Whole-House Panorama Synthesis

**Authors:** Jinrang Jia, Zhenjia Li, Yijiang Hu, Yifeng Shi
**arXiv:** [2605.17916](https://arxiv.org/abs/2605.17916)
**Categories:** Computer Vision and Pattern Recognition (cs.CV)

Generating a consistent whole-house VR tour from a floorplan and style reference requires both photorealistic panoramas and cross-view spatial coherence. Pure 2D generators produce appealing single panoramas but re-imagine geometry and materials when the viewpoint changes, whereas monolithic 3D generation becomes expensive and loses fine texture at multi-room scale. We introduce PanoWorld, a generative spatial world model that treats whole-house synthesis as autoregressive generation of node-based 360-degree panoramas, matching the discrete navigation used by real VR tour products. PanoWorld uses a floorplan-derived 3D shell as a global geometric proxy and a dynamic 3D Gaussian Splatting cache as renderable spatial memory. A feed-forward panoramic LRM designed for metric-scale multi-room 360-degree inputs lifts generated panoramas into local 3DGS updates, while Room-aware Group Attention suppresses cross-room feature interference. A topology-aware progressive caching strategy fuses these local updates without repeatedly reconstructing the full history. By decoupling shell-based geometry guidance from cache-rendered visual memory, PanoWorld preserves high-frequency 2D synthesis quality while improving cross-node layout and material consistency. The project link is this https URL

---

## 22. DeTrack: A Benchmark and Altitude-Aware Dual World Model for Drone-embodied Tracking

**Authors:** Guyue Hu, Haoming Liu, Siyuan Song, ..., Feng Chen, Jin Tang
**arXiv:** [2605.17451](https://arxiv.org/abs/2605.17451)
**Categories:** Computer Vision and Pattern Recognition (cs.CV)

Aerial object tracking has broad applications in public safety, emergency rescue, wildlife monitoring, and related fields. However, existing aerial tracking benchmarks are mainly based on passive 2D video sequences captured from fixed camera locations or predefined flight paths, where drones are treated as passive cameras rather than embodied agents that actively perceive, interact, and control their motion in dynamic 3D scenes. In this paper, we define a new drone-embodied tracking task, termed DeTrack, which requires a drone to track a target in interactive 3D environments using online egocentric observations and active flight control in a closed loop. We build a large-scale benchmark containing 11,368 target trajectories across diverse scenes, rendering conditions, semantic regions, and moving distractors, together with evaluation metrics for target visibility, tracking accuracy, and trajectory success. We further propose AaDWorlds, an altitude-aware dual world model framework for drone-embodied tracking. AaDWorlds consists of an altitude-aware perception module and dual world models that imagine future states under both high- and low-altitude regimes. By combining pseudo altitude-aware observations and imagined future states, AaDWorlds alleviates the intrinsic altitude-mediated contradiction between target visibility and flight safety. Experiments on the DeTrack benchmark demonstrate that AaDWorlds improves closed-loop tracking performance across all evaluation metrics.

---

## 23. SWoMo: Neuro-Symbolic World Model for Cataract Surgery Simulation

**Authors:** Ssharvien Kumar Sivakumar, Akwele Johnson, Anirudh Dhingra, ..., Ghazal Ghazaei, Anirban Mukhopadhyay
**arXiv:** [2605.16530](https://arxiv.org/abs/2605.16530)
**Categories:** Computer Vision and Pattern Recognition (cs.CV)

Realistic surgical simulation plays a crucial role in training novice surgeons and in the development of autonomous agents. World models can scale such simulation environments to realistic and diverse procedures by predicting future patient states conditioned on current observations and surgical actions. However, current state-of-the-art approaches often fail to satisfy key criteria required for clinical applicability, including visual realism, physically grounded interactions, and the ability to simulate scenarios beyond the training distribution. Hence, we introduce SWoMo, a neuro-symbolic world model for cataract surgery simulation that decouples motion generation from visual realism. The symbolic component, consisting of a rule-based simulator and scene graph representations, models motion dynamics and tool-tissue interactions, while a diffusion model produces realistic visual appearance, including textures and tissue deformations. We propose an inverse pairing strategy that reconstructs real surgical videos in the simulator to obtain paired simulated and real videos, which are then used to train our video diffusion model for the reverse objective of sim-to-real translation. Our experiments show both qualitative and quantitative improvements over prior work. We demonstrate that our simulator further satisfies the key criteria, including generalisation to unseen interaction geometries, improvements in downstream phase detection, and unsupervised video style transfer. The code, data, and model weights are available at: this https URL

---

## 24. Actionable World Representation

**Authors:** Kunqi Xu, Jitao Li, Jianglong Ye, ..., Sifei Liu, Xueyan Zou
**arXiv:** [2605.18743](https://arxiv.org/abs/2605.18743)
**Categories:** Artificial Intelligence (cs.AI)

Inspired by the emergent behaviors in large language models that generalized human intelligence, the research community is pursuing similar emergent capabilities within world models, with a emphasis on modeling the physical world. Within the scope of physical world model, objects are the fundamental primitives that constitute physical reality. From humans to computers, nearly everything we interact with is an object. These objects are rarely static; they are actionable entities with varying states determined by their intrinsic properties. While current methods approach object action states either via video generation or dynamic scene reconstruction, none explicitly model this basic element in a unified, principled way to build an actionable object representation. We propose WorldString, a neural architecture capable of modeling the state manifold of real-world objects by learning directly from point clouds or RGB-D video streams. Serving as a versatile digital twin, it acts as a foundational building block for physical world models; thus, we name it WorldString. Sweetly, its fully differentiable structure seamlessly enables future integration with policy learning and neural dynamics.

---

## 25. Scalable Environments Drive Generalizable Agents

**Authors:** Jiayi Zhang, Fanqi Kong, Guibin Zhang, ..., Chenglin Wu, Yuyu Luo
**arXiv:** [2605.18181](https://arxiv.org/abs/2605.18181)
**Categories:** Artificial Intelligence (cs.AI); Computation and Language (cs.CL)

Generalizable agents should adapt to diverse tasks and unseen environments beyond their training distribution. This position paper argues that such generalization requires environment scaling: expanding the distribution of executable rule-sets that agents interact with, rather than only increasing trajectories or tasks within fixed benchmarks. Current scaling practices largely focus on collecting more experience or broader task sets under fixed interaction rules, leaving agents brittle when underlying interfaces, dynamics, observations, or feedback signals change. The core challenge is therefore a world-level distribution shift: agents need systematic exposure to environments with meaningfully different executable rule-sets. To clarify this challenge, we propose a unified taxonomy that separates trajectory scaling, task scaling, and environment scaling by their primary deliverables and by what changes in the executable rule-set. Building on this taxonomy, we synthesize construction paradigms for scalable environments, contrasting programmatic generators that prioritize controllability and verifiability with generative world models that offer broader coverage and open-endedness. We further outline how environment scaling can be coupled with stateful learning mechanisms, emphasizing learned update rules for cross-environment adaptation. We conclude by discussing alternative perspectives and argue that scalable environments provide the essential substrate for measurable and controllable progress toward robust general agents.

---

## 26. Key-Gram: Extensible World Knowledge for Embodied Manipulation

**Authors:** Jingjing Fan, Siyuan Li, Botao Ren, Zhidong Deng
**arXiv:** [2605.18556](https://arxiv.org/abs/2605.18556)
**Categories:** Robotics (cs.RO); Artificial Intelligence (cs.AI)

Embodied control increasingly requires models to follow compositional language instructions while reasoning over dynamic visual states. However, current vision-language-action policies and world-action models often couple linguistic knowledge with visual computation in a shared backbone or conditioning pathway, leading to modality competition and making knowledge extension dependent on backbone updates. In this paper, we introduce Key-Gram, a conditional-memory framework that separates language-derived world knowledge from visual-state reasoning for embodied control. At its core is a memory module that decomposes an instruction into task-specific key-grams, retrieves static linguistic priors through deterministic hashed lookup, and injects the retrieved entries into selected hidden layers through context-aware gating and lightweight convolutional fusion. This design allows the backbone to devote its main capacity to visual reasoning and action inference, while reusable instruction knowledge is stored in an extensible external memory. The logical memory table can be conveniently partitioned during training and, due to its $O(1)$ lookup pattern, efficiently placed on host memory during inference. Across RoboTwin2.0, LIBERO/LIBERO-Plus, and real-world dual-arm manipulation, Key-Gram consistently improves both $\pi_{0}$ and $\pi_{0.5}$ backbones, with average relative gains of $29.5\%/9.9\%$ on RoboTwin2.0, $35.8\%/4.5\%$ on LIBERO-Plus transfer without target-domain fine-tuning, and $15.4\%/8.1\%$ on real-world long-horizon tasks. These results demonstrate that externalized linguistic memory provides an effective and extensible mechanism for improving compositional grounding, transfer, and real-world manipulation.

---

## 27. CLAP: Contrastive Latent-space Prompt Optimization for End-to-end Autonomous Driving

**Authors:** Ruiyang Zhu, Yuehan He, Boyuan Zheng, ..., Qingzhao Zhang, Z. Morley Mao
**arXiv:** [2605.17284](https://arxiv.org/abs/2605.17284)
**Categories:** Computer Vision and Pattern Recognition (cs.CV); Artificial Intelligence (cs.AI); Machine Learning (cs.LG); Robotics (cs.RO)

End-to-end autonomous driving systems powered by Vision-Language-Action (VLA) models achieve strong performance on common driving scenarios, yet remain brittle in rare but safety-critical long-tail situations such as active construction zones and complex yielding geometries. In this paper, we present a method that addresses the long-tail challenging scenes beyond data scaling and model training. We introduce CLAP (Contrastive Latent-space Prompt optimization), a location-aware adaptation framework that augments a frozen VLA driving model with per-roadblock soft prompts, optimized from crowdsourced data and retrieved on demand via Vehicle-to-Everything (V2X) communication. Our approach rests on two observations from VLAs' latent space: (i) at the VLA's hidden-state layer, scenarios from the same roadblock cluster tightly and occupy compact regions of the latent space; and (ii) within a single roadblock, long-tail and normal frames are heavily intermixed in the latent representation, making it difficult to improve one without disturbing the other. CLAP addresses this via a two-stage pipeline: supervised contrastive learning to discover a roadblock-specific hard-scene direction, followed by directionally regularized prompt optimization that selectively improves challenging frames while preserving normal frame performance. On the NAVSIM benchmark with various state-of-the-art VLA backbones, CLAP reduces challenging scenario planning error by 24% with no regression on normal frames, significantly improving planning performance.

---

## 28. How to Instruct Your Robot: Dense Language Annotations Power Robot Policy Learning

**Authors:** Bosung Kim, Ruiyi Wang, David Acuna, ..., Yejin Choi, Prithviraj Ammanabrolu
**arXiv:** [2605.17077](https://arxiv.org/abs/2605.17077)
**Categories:** Robotics (cs.RO); Artificial Intelligence (cs.AI)

Scaling robot policy learning is bottlenecked by the cost of collecting demonstrations, while language annotations for existing demonstrations are comparatively cheap. We study language density as a lever for extracting more signal from a fixed robot or egocentric-video corpus. We introduce DeMiAn (Dense Multi-aspect Annotation), a two-stage approach that first re-labels demonstration segments with VLM-generated annotations along four complementary aspects: physical motion, scene composition, arm pose, and reasoning. A learned instructor then maps a task description and initial scene snapshot to a task-appropriate annotation at deployment, running asynchronously so generation latency is hidden behind policy execution. Across over 1M robot manipulation clips and 50K EgoVerse human-egocentric videos, DeMiAn improves both a vision-language-action policy and a video-based world-action model without collecting new demonstrations. On RoboCasa, the instructor raises success by 5 points over a task-only baseline and comes within 3 points of a per-task oracle. No fixed annotation aspect dominates across tasks, showing that selecting the right dense language matters. DeMiAn also improves composite-task and out-of-distribution performance, and shifts the compute-performance frontier in both mid-training and post-training after accounting for annotation-generation FLOPs. These results position dense re-annotation as a practical scaling lever for robot policy learning.

---

## 29. Thinking with Patterns: Breaking the Perceptual Bottleneck in Visual Planning via Pattern Induction

**Authors:** Yichang Jian, Boyuan Xiao, Zhenyuan Huang, Yifei Peng, Yao-Xiang Ding
**arXiv:** [2605.16848](https://arxiv.org/abs/2605.16848)
**Categories:** Computer Vision and Pattern Recognition (cs.CV); Artificial Intelligence (cs.AI); Computation and Language (cs.CL); Machine Learning (cs.LG)

Planning from raw visual input remains a significant challenge for current Vision-Language Models (VLMs), when the complexity of input is beyond their one-step perception capability. Motivated by recent advances in Thinking with Images (TWI), a reasonable solution is to decompose the perception process into simpler steps by iteratively acquiring and incorporating local visual evidence. However, even though current VLMs are well-trained in general TWI ability, their perceptual bottleneck in the planning domain remains. To tackle this challenge, we formulate TWI as a tool to gradually build and reflect an accurate internal world model. We find that the resulting training-free planning strategy enables VLMs to solve tasks that are far beyond their initial capabilities, at the cost that too many TWI operations would significantly increase the computational overhead. To further improve efficiency, we propose Pattern Inference, a novel TWI strategy enabling VLMs to actively recognize known visual patterns in the new tasks and directly infer local world model structures. To obtain these patterns, we propose Pattern Induction, an online inductive learning strategy treating visual patterns as composite and reusable experts, which are autonomously discovered and optimized from experience. Experimental evaluations in FrozenLake, Crafter and CubeBench domains show that our approaches achieve a desirable balance between accuracy and efficiency.

---

## 30. Robo-Cortex: A Self-Evolving Embodied Agent via Dual-Grain Cognitive Memory and Autonomous Knowledge Induction

**Authors:** Nga Teng Chan, Yi Zhang, Yechi Liu, ..., Yong Dai, Xiaozhu Ju
**arXiv:** [2605.18729](https://arxiv.org/abs/2605.18729)
**Categories:** Robotics (cs.RO); Computer Vision and Pattern Recognition (cs.CV)

The ability to navigate and interact with complex environments is central to real-world embodied agents, yet navigation in unseen environments remains challenging due to "experiential amnesia," where existing trajectory-driven or reactive policies fail to synthesize generalizable strategies from past interactions. We propose Robo-Cortex, a self-evolving framework that enables robots to autonomously induce navigation heuristics and refine cognitive strategies through a continuous reflection-adaptation loop. By abstracting success patterns and failure pitfalls into natural-language heuristics, Robo-Cortex enables a transition from passive execution to active strategy evolution. Our core innovation is an Autonomous Knowledge Induction (AKI) mechanism that distills multimodal trajectories into a structured Navigation Heuristic Library for knowledge generalization. The architecture further incorporates a Dual-Grain Cognitive Memory system, comprising a Short-term Reflective Memory (SRM) for real-time local progress analysis, and a Long-term Principle Memory (LPM) that abstracts past trajectories into reusable guiding and cautionary principles. To ensure robust decision-making, we introduce a multimodal Imagine-then-Verify loop, where a world model simulates potential outcomes and a VLM-based evaluator validates action plans. Extensive evaluations on IGNav, AR, and AEQA show that Robo-Cortex consistently outperforms strong baselines in both task success and exploration efficiency, with gains of up to +4.16% SPL over the strongest prior method and up to +15.30% SPL under heuristic transfer to unseen environments. Preliminary real-world robotic experiments further support the effectiveness of Robo-Cortex in physical settings.

---

## 31. GEM: Gaussian Evolution Model for Occupancy Forecasting and Motion Planning

**Authors:** Cheng Chen, Hao Huang, Saurabh Bagchi
**arXiv:** [2605.17682](https://arxiv.org/abs/2605.17682)
**Categories:** Computer Vision and Pattern Recognition (cs.CV)

Future 3D semantic occupancy forecasting and motion planning are central to autonomous driving, as they require models to reason about how surrounding scenes evolve and how the ego vehicle should act. Existing occupancy world models commonly discretize scenes into latent embeddings, volumetric features, or quantized tokens, and forecast future states through fixed-step autoregressive generation. This limits temporal flexibility, obscures scene evolution, accumulates errors over long horizons, and poorly matches the continuous-time dynamics of real driving scenes. We propose GEM, a Gaussian Evolution Model for non-autoregressive occupancy world modeling, where driving scenes are represented as explicit continuous 4D Gaussian primitives with learned dynamics. Instead of rolling out future occupancy states step by step, GEM directly queries the Gaussian world representation at arbitrary timestamps and splats the corresponding conditional 3D Gaussians into semantic occupancy volumes. This enables efficient forecasting over the full horizon while retaining a compact and interpretable scene representation. By decoupling spatial geometry, temporal support, and primitive motion, GEM makes the predicted world easier to inspect, as each primitive's evolution can be followed continuously over time. The same representation also supports motion planning by predicting future ego trajectories from the learned Gaussian world. Extensive experiments show that GEM achieves state-of-the-art future semantic occupancy forecasting and strong motion planning performance, while providing flexible temporal querying.

---
