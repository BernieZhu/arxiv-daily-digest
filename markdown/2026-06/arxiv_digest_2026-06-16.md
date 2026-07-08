# arXiv Daily Digest — 2026-06-16

**Mode:** direct
**Categories:** cs.AI, cs.LG, cs.RO, cs.CV
**Keywords:** VLA, world model, world action model
**Papers found:** 35

---

## 1. Medical world models: representing medical states, modelling clinical dynamics and guiding intervention policies

**Authors:** Ke Liu, Mengxuan Li, Yanyi Bao, ..., Jiajun Bu, Haishuai Wang
**arXiv:** [2606.16721](https://arxiv.org/abs/2606.16721)
**Categories:** Artificial Intelligence (cs.AI)

Medical diagnosis and treatment are dynamic processes in which patient states evolve over time and clinical interventions alter future outcomes. Although current medical AI can detect disease, estimate risk and generate reports, many systems still return static labels or scores, offering limited insight into how illness may progress or how alternative interventions may reshape its trajectory. Medical world models adapt the world-model idea from artificial intelligence to healthcare by learning internal simulators of patient-state dynamics. Their long-term goal is to help clinicians anticipate deterioration, compare treatment-conditioned futures and tailor care to individual patients. Yet relevant work remains scattered across foundation models, longitudinal modelling, disease simulation, treatment-effect estimation, reinforcement learning and digital twins. To bridge this gap, this review outlines a roadmap for advancing medical AI from isolated diagnosis and prediction toward medical world models that simulate disease evolution and support intervention decisions. This roadmap is organized around three coupled capabilities: patient-state construction, clinical dynamics modelling and intervention decision support. Across representative systems, the comparison highlights what each capability contributes and how partial components can be integrated into more mature perception--dynamics--planning systems. Finally, we identify the challenges involved in turning plausible rollouts into clinically useful simulators. Related literature is available at this https URL.

---

## 2. ARB4WM: An Adversarial Robustness Benchmark for World Models in Continuous Control

**Authors:** Junjian Zhang, Hao Tan, Ruonan Li, ..., Aiping Li, Zhaoquan Gu
**arXiv:** [2606.16605](https://arxiv.org/abs/2606.16605)
**Categories:** Artificial Intelligence (cs.AI)

World models are widely used in robotic and agentic engineering control systems due to their ability to learn latent dynamics for planning and decision-making. As these systems are increasingly deployed in safety-critical settings, understanding their robustness under adversarial conditions has become essential. However, existing evaluations lack a unified benchmark for testing adversarial threats across the policy, value, and latent-dynamics levels of world-model agents. To fill this gap, we present ARB4WM, a unified evaluation framework for pre-deployment robustness and risk assessment of world-model agents under visual perturbations. ARB4WM defines five white-box loss objectives across these three levels and studies their effects when combined with single-step or multi-step perturbation strategies and temporal attack modes, including full-frame, half-sequence, and sparse-frame exposure. Specifically, we evaluate four Dreamer-style agents across 20 tasks from MetaWorld and the DeepMind Control Suite under different loss objectives, perturbation strategies, and temporal attack modes. Results show that attacks targeting value estimation, latent representations, and RSSM dynamics can be as damaging as direct policy disruption, and that early or frequent perturbations are especially harmful, while input-level defenses provide limited recovery under adaptive attacks. These findings suggest that safety, risk, and reliability assessment for world models should cover multiple component-oriented attack objectives and temporal exposure protocols rather than relying solely on action-space robustness. Source code is available at this https URL.

---

## 3. Kairos: A Native World Model Stack for Physical AI

**Authors:** Kairos Team, Fei Wang, Shan You, ..., Dacheng Tao, Xiaogang Wang
**arXiv:** [2606.16533](https://arxiv.org/abs/2606.16533)
**Categories:** Artificial Intelligence (cs.AI); Computer Vision and Pattern Recognition (cs.CV)

World models are transitioning from passive visual generators to foundational, operational infrastructure for Physical AI: they must natively acquire world knowledge from heterogeneous experience, maintain persistent states over long horizons, and execute efficiently within real deployment constraints. We introduce Kairos, a native world model stack designed around these requirements. (1) Kairos learns the world by pioneering a Native Pre-training Paradigm governed by a Cross-Embodiment Data Curriculum, which organizes open-world videos, human behavioral data, and robot interactions into a progressive developmental pathway. (2) Kairos maintains the world by unified world understanding, generation, and prediction within a Native Unified Architecture equipped with Hybrid Linear Temporal Attention, where sliding-window attention captures local dynamics, dilated sliding windows capture mid-range dependencies, and gated linear attention maintains persistent global memory. We establish formal theoretical bounds demonstrating that this temporal factorization strictly limits error accumulation, mathematically guaranteeing state propagation across extended horizons. (3) Kairos runs the world by incorporating a Deployment-Aware System Co-Design to support low-latency rollout generation on server and consumer-grade hardware for real-world observation-action-feedback loops. Experiments on embodied world-model, long-horizon, and action-policy benchmarks show that Kairos achieves top level performance while offering a strong efficiency-capability trade-off. Together, these results position Kairos as a cohesive operational foundation for future self-evolving physical intelligence.

---

## 4. Mind-Studio: Executable World Models with Lookahead Evaluation for Partially Observable Games

**Authors:** Yifei Dong, Mingen Zheng, Linquan Wu, Jeff Z. Pan, Jiaxin Bai
**arXiv:** [2606.16070](https://arxiv.org/abs/2606.16070)
**Categories:** Artificial Intelligence (cs.AI)

World-model synthesis aims to turn interaction experience into an internal model of environment dynamics. Existing symbolic approaches often fit observed transitions or mixtures of local rules, but they do not produce a complete executable program that can run independently of the real environment. We present Mind-Studio, a framework that synthesizes executable pygame-style world models from state-action-next-state trajectories using large language models. Mind-Studio combines entropy-selected traces with a lightweight game skill file containing object, action, and static scene information extracted from screenshots. We evaluate synthesis quality with a K-step lookahead fidelity protocol that compares generated world-model rollouts against Real-ALE rollouts from the same state. On Montezuma's Revenge, Mind-Studio improves chosen-action next-state prediction from 0.3% for PoE-World to 48.7% while verifying 5 of 8 subgoals; across Alien, Assault, and Skiing, it achieves stronger branch-level fidelity than prior learned lookahead sources.

---

## 5. FlowMPC: Improving Flow Matching policies with World Models

**Authors:** Chandon Hamel
**arXiv:** [2606.16286](https://arxiv.org/abs/2606.16286)
**Categories:** Machine Learning (cs.LG); Artificial Intelligence (cs.AI); Robotics (cs.RO)

Flow Matching (FM) is a powerful approach for behavior cloning in multimodal action spaces [Jiang et al., 2025], but because it is not trained to directly maximize expected return, there is still room to improve how FM policies act at test time. This work investigates whether a learned world model can improve FM policies by enabling Model Predictive Path Integral (MPPI) planning over candidate action sequences proposed by the policy. Building on TD-MPC2 [Hansen et al., 2024], I introduce FlowMPC, a framework that combines an imitation-learned FM policy with a learned world model for test-time planning in ManiSkill manipulation tasks [Tao et al., 2025]. Across PickCube and PickSingleYCB, adding the world model improved performance over the FM policy alone, with especially clear gains in end-of-episode success. These results suggest that world-model-based planning can effectively complement flow-based imitation policies without modifying the FM training objective.

---

## 6. Learned Image Compression for Vision-Language-Action Models

**Authors:** Hyeonjun Kim, Jegwang Ryu, Sangbeom Ha, ..., Hyemin Ahn, Jaeho Lee
**arXiv:** [2606.16253](https://arxiv.org/abs/2606.16253)
**Categories:** Computer Vision and Pattern Recognition (cs.CV); Artificial Intelligence (cs.AI)

Vision-language-action (VLA) models increasingly rely on high-frequency multi-camera observations, making visual communication a major bottleneck for real-time robotic control in bandwidth-constrained or distributed deployment settings. Existing image and video codecs, however, are designed to preserve generic visual fidelity rather than the control performance of downstream VLA policies. In this work, we introduce SPARC (SPatially Adaptive Rate Control), a learned image compression framework tailored for VLA-driven robots. Our key observation is that the importance of visual information varies substantially across both camera views and spatial regions within an image. Based on this observation, SPARC employs a lightweight temporal mask selector that adaptively allocates bitrate over latent representations according to task relevance while leveraging temporal context. We further introduce a tilted rate loss that stabilizes training by reducing the tendency of entropy-based objectives to over-suppress rare yet task-critical visual patterns. Experiments on diverse robotic benchmarks, including RoboCasa365, VLABench, and LIBERO, show that SPARC consistently achieves stronger control performance than conventional image/video codecs and recent learned compression methods under the same bitrate budget. We additionally demonstrate real-world deployment benefits in remote-control settings, where our method substantially improves the bitrate-success tradeoff.

---

## 7. Phys-JEPA: Physics-Informed Latent World Models for Multivariate Time-Series Forecasting

**Authors:** Weizhi Nie, Weichao Liu, Honglin Guo, Yuting Su
**arXiv:** [2606.16076](https://arxiv.org/abs/2606.16076)
**Categories:** Machine Learning (cs.LG); Artificial Intelligence (cs.AI); Computer Science and Game Theory (cs.GT)

Multivariate forecasting in physical systems requires models that predict coupled temporal variables while preserving meaningful state evolution. Deep forecasters can fit temporal correlations, and physics-informed models can regularize predictions with scientific constraints, but these directions are often connected only at the decoded-output level. As a result, the hidden predictive state that generates future trajectories may remain statistically useful but physically unstructured. We introduce Phys-JEPA, a physics-informed joint-embedding predictive architecture for multivariate time-series forecasting. Phys-JEPA learns a latent world model in which predictive states are decomposed into physical and residual components, and physical consistency is imposed directly on latent states and latent transitions rather than only on decoded forecasts. This formulation uses known physical variables to organize the representation space while retaining residual capacity for unresolved dynamics. On Jena Climate 2009--2016, Phys-JEPA reduces aggregate MSE from 0.12482 to 0.12273 and temperature MSE from 0.01892 to 0.01831 at H=24. On Traffic, full Phys-JEPA improves aggregate MSE over the supervised baseline across all tested horizons, reducing H=192 MSE from 0.800784 to 0.773873. On Electricity, the best variant depends on horizon: static latent consistency is strongest at H=24 and H=48, while full Phys-JEPA gives the best aggregate and target-variable MSE at H=192. These initial results suggest that moving physics-informed learning from output space to latent predictive state space is a promising direction for interpretable temporal world models.

---

## 8. LaWAM: Latent World Action Models for Efficient Dynamics-Aware Robot Policies

**Authors:** Jialei Chen, Kai Wang, Kang Chen, ..., Yuanbo Xu, Chao Yu
**arXiv:** [2606.15768](https://arxiv.org/abs/2606.15768)
**Categories:** Robotics (cs.RO); Artificial Intelligence (cs.AI)

Vision-Language-Action models (VLAs) leverage large-scale vision-language pretraining for semantic robot control, but often lack explicit foresight into how robot actions change the scene. World-Action Models (WAMs) address this limitation by conditioning policies on predicted futures, yet existing approaches typically rely on computationally expensive video generation with substantial pixel-level redundancy. We present LaWAM, a Latent World Action Model that exposes predictive dynamics to robot policies through compact latent visual subgoals instead of reconstructed future video. At the core of LaWAM is a latent-action-conditioned Latent World Model (LaWM). We obtain LaWM by training a latent action model in the latent space of a pretrained vision foundation model and repurposing its forward decoder to predict future observation features for scene evolution. LaWAM then conditions action generation on these predicted latent visual subgoals to enable dynamics-aware robot control. LaWAM achieves state-of-the-art or competitive success rates (SRs) across LIBERO (98.6% SR), RoboTwin (91.22% SR), and real-world manipulation tasks while retaining low-latency inference. LaWAM runs in 187 ms per action-chunk prediction and achieves up to 24x lower wall-clock latency than pixel-space WAMs.

---

## 9. Retrieve, Don't Retrain: Extending Vision Language Action Models to New Tasks at Test Time

**Authors:** Jeongeun Park, Juhan Park, Taekyung Kim, ..., Dongyoon Han, Sangdoo Yun
**arXiv:** [2606.15631](https://arxiv.org/abs/2606.15631)
**Categories:** Robotics (cs.RO); Artificial Intelligence (cs.AI)

Extending a vision-language-action (VLA) policy to a new task typically requires task-specific teleoperated demonstrations and per-task fine-tuning, making adaptation costly in both data collection and compute. In this paper, we show that this target-side per-task adaptation cost can be replaced by retrieval. Our retrieval-augmented policy is trained once on paired demonstrations from the target embodiment (query) and a cheaper embodiment (pool, e.g., human-hand video), then frozen. New tasks are added at deployment by appending pool-side demonstrations to a retrieval pool. The frozen policy conditions on retrieved trajectories at every control step, so new tasks are absorbed by indexing data rather than updating parameters. Fine-tuning is needed only to take on a new, unseen embodiment, not for each new task. We show that retrieval improves policies beyond a specific backbone, including standard VLA policies, but its effect is especially pronounced in Cosmos Policy, a video-generation-based world-action model (WAM). In this setting, retrieval supplies coarse task progression, while the WAM's future-image objective provides an additional visual consistency signal that strengthens the retrieval-conditioned actions. On PushT, we study how retrieval provides a reusable high-level motion prior for cross-embodiment generalization to unseen goal angles, while on RoboTwin 2.0 our method outperforms cross-embodiment baselines on unseen tasks, and we additionally demonstrate the method on a real robot.

---

## 10. Pixels to Proofs: Probabilistically-Safe Latent World Model Control via Parallel Conformal Robust MPC

**Authors:** Devesh Nath, Anutam Srinivasan, Haoran Yin, ..., Jeffrey Fang, Glen Chou
**arXiv:** [2606.15594](https://arxiv.org/abs/2606.15594)
**Categories:** Robotics (cs.RO); Artificial Intelligence (cs.AI); Computer Vision and Pattern Recognition (cs.CV); Machine Learning (cs.LG); Systems and Control (eess.SY)

We present SLS^2, a framework for safe feedback motion planning from pixels using robust model predictive control (MPC) in learned latent world models. Our approach trains an action-conditioned joint-embedding world model with compact Markovian latent states, enabling efficient gradient-based trajectory optimization through learned latent dynamics. To enforce safety for the true system despite imperfect latent predictions, we inform a GPU-accelerated system level synthesis (SLS) robust MPC scheme with conformal prediction to obtain calibrated latent error bounds and robust latent-space constraint sets. We further learn and conformalize a latent constraint checker, allowing the SLS planner to impose probabilistic safety constraints during closed-loop execution. We evaluate our method on vision-based control tasks, where it improves both goal-reaching performance and safety over latent world-model and safe-planning baselines.

---

## 11. Separable Neural Architectures as Physical World Models: from Mathematical Theory to Applications

**Authors:** Reza T Batley, Andrew Kichline, Sourav Saha
**arXiv:** [2606.14934](https://arxiv.org/abs/2606.14934)
**Categories:** Machine Learning (cs.LG); Artificial Intelligence (cs.AI)

This work introduces the Separable Neural Architecture (SNA), a function representational class combining neural approximation with tensor decomposition. The SNA decouples localized coordinate functions (atoms) from global interactions governed by a sparse, low-rank interaction object. This architecture possesses a compact and smooth inductive bias well-suited for solving partial differential equations (PDEs). When viewed as a Galerkin trial space under the variational SNA (VSNA) framework, the formulation satisfies classical variational guarantees under Lax-Milgram: well-posedness, quasi-optimality, convergence, and stability. In high-dimensional spatiotemporal--parametric PDEs, the VSNA mitigates the curse of dimensionality by scaling algebraically rather than exponentially. Exploiting an entirely factorized, tensor-native alternating least squares (ALS) optimization framework reduces this cost to linear in dimension. The VSNA is validated across elliptic, hyperbolic, and parabolic systems, demonstrating close alignment with predicted algebraic and spectral scaling rates. We showcase the SNA as a "solve once, query anywhere" physical world model via two engineering case studies: a 7D parametric manufacturing simulation and an experimental thermal-to-property inversion pipeline for Inconel 718. The VSNA executes a 1,000,000-query Monte Carlo sweep in 102s on a standard laptop CPU, yielding a 150,000x speedup over a full-grid finite element baseline hosted on an NVIDIA A100 GPU. It further enables real-time generative inverse-mode reconstructions under 100ms. These results demonstrate that the SNA serves as a compact mathematical substrate for continuous parameter manifolds to enable real-time inversion, optimization loops, and rapid uncertainty propagation.

---

## 12. ScoutVLA: UAV-Centric Active Perception via a Dual-Expert VLA Model for Open-World Embodied Question Answering

**Authors:** Wenhao Lu, Zhengqiu Zhu, Xiaofeng Wang, ..., Jinlong Zhu, Zheng Zhu
**arXiv:** [2606.14772](https://arxiv.org/abs/2606.14772)
**Categories:** Computer Vision and Pattern Recognition (cs.CV); Artificial Intelligence (cs.AI)

Aerial Embodied Question Answering (EQA) requires Unmanned Aerial Vehicles (UAVs) to actively perceive the environment and answer natural language questions. Existing outdoor EQA systems usually stop once the target enters the UAV's field of view, leaving the fine-grained viewpoint adjustment needed for evidence-seeking questions largely unresolved. To address this issue, we introduce FG-EQA, a fine-grained active perception EQA benchmark with more than 40K simulated trajectories and 1K real-world trajectories. Drawing inspiration from the ``waggle dance'' of scout bees, which iteratively adjust their flight paths to verify target information, we propose ScoutVLA, an evidence-driven Vision-Language-Action model for outdoor EQA. To emulate this active exploration behavior, ScoutVLA features a decoupled dual-expert architecture: a vision-language expert infers the semantic intent to identify missing evidence, while an independent action expert employs high-DoF flow matching to generate continuous viewpoint-refinement trajectories. To balance the competing demands of continuous control and semantic reasoning, we devise a decoupled training strategy with a knowledge insulation mechanism that prevents the action gradients from erasing the model's multimodal reasoning ability. Extensive simulated experiments and a qualitative real-world field study both verify the superiority of ScoutVLA over the state-of-the-art baselines, demonstrating a 10.48$\boldsymbol{\times}$ higher average strict success rate and a 7.72$\boldsymbol{\times}$ higher average QA correctness.

---

## 13. X-Tokenizer: A Multimodal Action Tokenizer for Vision-Language-Action Pretraining

**Authors:** Xirui Kang, Yanpei Shi, Lucy Liang, ..., Xianyuan Zhan, Hang Su
**arXiv:** [2606.14752](https://arxiv.org/abs/2606.14752)
**Categories:** Computer Vision and Pattern Recognition (cs.CV); Artificial Intelligence (cs.AI); Machine Learning (cs.LG); Robotics (cs.RO)

Modern Vision-Language-Action (VLA) models must bridge pretrained vision-language reasoning and precise continuous robot control. Existing action tokenizers discretize actions primarily for reconstruction, producing codes that preserve motion geometry but provide only weak semantic supervision to the backbone. We therefore formulate action tokenization not as mere compression, but as semantic interface learning between multimodal reasoning and executable control. To this end, we introduce X-Tokenizer, a lightweight encoder-Semantic Residual Quantization (SRQ)-decoder architecture that provides a shared action interface across diverse robotic arm embodiments. Its key component, SRQ, imposes an asymmetric structure on residual vector quantization: the first level is trained with Masked Action Modeling (MAM) to form a discrete action language that captures coarse motion intent, while deeper levels remain reconstruction-oriented residuals that preserve fine-grained details. To further align action tokens with multimodal semantics, X-Tokenizer is pretrained with contrastive alignment to the representation space of a pretrained foundation model and with next-frame vision-language feature prediction. Pretrained on 2.4M trajectories (2.0B action frames), a single frozen X-Tokenizer plugs into a mixed discrete-continuous VLA as a representation-shaping supervision signal. X-Tokenizer achieves top real-world aggregate and strong RoboTwin 2.0 simulation results. Outperforming FAST in multimodal grounding (+13.5%) and long-horizon tasks (+8.25), it shows that action tokenizers serve as semantic interfaces for VLA pretraining beyond mere action compression.

---

## 14. BRICKS-WM: Building Reusability via Interface Composition Kinetics for Structured World Models

**Authors:** Shaowei Zhang, Jiahan Cao, Xunlan Zhou, Shenghua Wan, De-Chuan Zhan
**arXiv:** [2606.16489](https://arxiv.org/abs/2606.16489)
**Categories:** Machine Learning (cs.LG)

Model-based Reinforcement Learning (MBRL) has achieved remarkable success in continuous control by leveraging latent world models. However, prevailing approaches typically rely on monolithic latent dynamics, entangling environment dynamics into a coupled process. This coupling severely limits reusability: altering the agent necessitates retraining the entire world from scratch, even if the environment remains constant. To address this, we introduce BRICKS-WM (Building Reusability via Interface Composition Kinetics for Structured World Models), a framework for the modular assembly of structured world models. Driven by the insight that the physical world is composed of independent entities, we posit that global dynamics can be modeled as a composition of distinct dynamical modules interacting via latent interfaces. As a minimal instantiation, we factorize the latent state space into an actuated Agent module and an external Background module, bridged by a learned latent interface. Unlike prior object-centric methods that prioritize visual segmentation, BRICKS-WM enforces a functional separation in transition dynamics, ensuring that background dynamics remains agnostic to the agent's dynamics. Empirically, BRICKS-WM achieves control performance comparable to strong monolithic baselines when trained from scratch, and enables the reuse of frozen background dynamics across agents.

---

## 15. How Should World Models Be Evaluated? A Decision-Making-Centric Position

**Authors:** Yang Yu, Shiyuan Zhang, Yifei Sheng, Haoxiang Ren, Haoxin Lin
**arXiv:** [2606.15032](https://arxiv.org/abs/2606.15032)
**Categories:** Machine Learning (cs.LG)

World models have rapidly become one of the central abstractions in modern AI. Yet the term now refers to several different objects: action-conditioned environment models, latent imagination models, future-video predictors, interactive neural simulators, latent predictive representations, and synthetic-data engines. Evaluation has broadened with the term. Recent papers measure video realism, perceptual similarity, instruction following, physical plausibility, policy ranking, executability, planning success, and downstream policy improvement. The result is not only metric diversity but also a recurring problem of claim/evidence mismatch: papers frequently make a stronger claim about what their model is useful for than their evaluation can actually establish.
This paper surveys the recent literature and argues that the central question is use-dependent. When a model is presented as a world model for embodied decision-making, a more decisive issue is not whether it generates visually compelling videos, but whether it supports reliable counterfactual reasoning, policy evaluation, planning, and policy optimization under intervention, policy-induced distribution shift, and long-horizon rollout. We organize the literature using an L0--L7 ladder that ranges from visual plausibility to policy optimization utility. In our interpretation, L0--L3 are most naturally read as diagnostics of generated artifacts, L4 is often the first genuinely interventional test, and L5--L7 provide the most direct evidence of decision usefulness. Based on this diagnosis, we propose a decision-making-centric evaluation framework and a benchmark protocol that foreground counterfactual action fidelity, closed-loop rollout validity, reward/value prediction, policy-ranking agreement, optimization lift, model exploitability, and uncertainty calibration.

---

## 16. Hierarchical Advantage Weighting for Online RL Fine-Tuning of VLAs from Sparse Episode Outcomes

**Authors:** Tongyan Fang, Siyuan Huang, Naiyu Fang, ..., Ying Dong, Hongsheng Li
**arXiv:** [2606.17043](https://arxiv.org/abs/2606.17043)
**Categories:** Robotics (cs.RO); Machine Learning (cs.LG)

When pretrained VLA policies are fine-tuned through online RL, each rollout episode produces only a single binary outcome (success or failure), yet the actor update requires per-transition supervision. Existing approaches commonly reduce this sparse outcome to a single scalar reward or advantage signal, which conflates distinct forms of transition-level feedback and provides limited guidance once basic task success becomes achievable. First, a single scalar signal conflates the two objectives of viability and efficiency; once basic success is achieved, the binary label provides no gradient to distinguish efficient completions from slow ones. Second, real-world rollouts mix autonomous and intervention segments; naively assigning episode outcomes across these boundaries introduces incorrect credit assignment. To address these issues, we propose Hierarchical Advantage-Weighted Behavior Cloning (HABC), which trains separate critic heads for these two objectives on different data subsets and combines their outputs with a state-adaptive balance. A state-adaptive gate $g_t$ merges their one-step advantages, prioritizing viability when success is uncertain and shifting to efficiency only when viability is high, and converts the result into per-transition weights on the actor loss. Intervention-aware credit assignment further restricts outcome labels to segments executed by the current policy, preventing supervision from leaking across intervention boundaries. In real-robot experiments on three contact-rich bimanual tasks, HABC raises success from supervised fine-tuning (SFT) baselines of 36%, 44%, and 12% to 92%, 88%, and 38%.

---

## 17. DLWM: Diverse Latent World Models for Efficient Multimodal Reasoning

**Authors:** David Huang, Lianlei Shan
**arXiv:** [2606.15160](https://arxiv.org/abs/2606.15160)
**Categories:** Computer Vision and Pattern Recognition (cs.CV); Machine Learning (cs.LG)

Reasoning capabilities of multimodal large language models (MLLMs) have improved considerably in recent years. Existing approaches typically rely on explicit chain-of-thought or continuous latent-space trajectories to enhance multi-step reasoning. However, these methods generally assume that an input admits a single latent interpretation and unfold reasoning along a fixed path or under a uniform computation budget. In real-world multimodal settings, visual observations are often subject to occlusion, blur, viewpoint variation, or semantic ambiguity, giving rise to multiple plausible interpretations. A uniform reasoning strategy not only limits the model's ability to explore multiple hypotheses but also incurs high memory usage and rollout cost. We present DLWM (Diverse Latent World Models), a multimodal reasoning framework that combines latent-space reasoning with reinforcement learning. First, we construct a set of diverse latent world hypotheses in continuous latent space, each capturing a different plausible interpretation of the visual input, and unfold latent reasoning independently on each hypothesis. An orthogonality-based diversity regularizer explicitly prevents hypothesis collapse. Second, we formulate the latent reasoning process as a resource-constrained sequential decision problem and introduce a resource-aware reinforcement learning policy that adaptively allocates computation across hypotheses, dynamically deciding whether to expand, terminate, or merge reasoning paths, thereby substantially reducing memory footprint and improving rollout efficiency. Experiments on multiple multimodal reasoning benchmarks demonstrate that DLWM outperforms existing methods by 2-5 points in accuracy while reducing memory usage by 24%.

---

## 18. Think Less, Act Early: Reinforced Latent Reasoning with Early Exit in Vision-Language-Action Models

**Authors:** Dianqiao Lei, Lianlei Shan
**arXiv:** [2606.15099](https://arxiv.org/abs/2606.15099)
**Categories:** Computer Vision and Pattern Recognition (cs.CV); Machine Learning (cs.LG); Robotics (cs.RO)

Existing Vision-Language-Action (VLA) models predominantly rely on explicit Chain-of-Thought (CoT) reasoning to bridge perception and action. While effective, this paradigm suffers from high computational costs and error propagation in multi-step tasks. In this paper, we propose Adaptive Variable Alignment VLA (AVA-VLA), a novel Latent Reasoning VLA framework that models reasoning as a sequence of unobservable latent variables, bypassing the need for explicit text generation. However, latent trajectories are inherently susceptible to noise interference and misalignment with downstream objectives. To address this, we introduce a Reinforcement Learning-based Denoising mechanism that treats latent state generation as a sequential decision process, optimizing reasoning trajectories via task-level rewards. Furthermore, we incorporate an Early-Exit Strategy that adaptively terminates reasoning based on state confidence, enabling a dynamic trade-off between depth and efficiency. Extensive experiments on embodied decision benchmarks demonstrate that AVA-VLA achieves a 6x inference speedup over explicit CoT methods while attaining a 98.3% average success rate on LIBERO, improving both efficiency and long-horizon stability over full-reasoning baselines.

---

## 19. SAPS: Shared Autonomy for Policy Steering by Blending Teleoperation with a Pretrained VLA

**Authors:** Crystal Zhou, Jehan Yang, Douglas J. Weber, Zackory Erickson
**arXiv:** [2606.15568](https://arxiv.org/abs/2606.15568)
**Categories:** Robotics (cs.RO)

Recent advancements in Vision-Language-Action (VLA) models have demonstrated impressive generalist capabilities in robot manipulation, yet these policies can be brittle under out-of-distribution spatial and semantic perturbations. While human teleoperation offers reliable recovery, it can demand high cognitive load and precise manual control, and existing policy steering methods often require auxiliary models or sampler modifications. In this work, we introduce Shared Autonomy for Policy Steering (SAPS), a framework that blends real-time human teleoperation commands with pretrained policy actions at the action level. SAPS requires no policy retraining, auxiliary dynamics models, or architectural modifications. We propose and evaluate three arbitration strategies to balance human and VLA policy control, including a dynamic Cosine-similarity arbitration strategy that computes the geometric agreement between human and policy actions. Across evaluations in simulation (LIBERO, LIBERO-PRO, CALVIN) and on real-world robot hardware, SAPS improves task success rates over autonomous execution by up to 82% in both simulation and the real world. Furthermore, our approach drastically reduces human intervention compared to pure teleoperation, while simultaneously achieving faster task completion times than both autonomous execution and pure teleoperation. These results demonstrate that action-level shared autonomy is a practical, model-agnostic approach for reliably deploying generalist robot policies in real-world contexts involving a human operator,with promising applications in assistive teleoperation and scalable data collection.

---

## 20. Acting While Understanding: Asynchronous Semantic-Action Decoupling for Real-Time Vision-Language-Action Models

**Authors:** Shenhao Yan, Ge Wang, Qi Liu, ..., Yiming Zhao, Yatong Han
**arXiv:** [2606.15285](https://arxiv.org/abs/2606.15285)
**Categories:** Robotics (cs.RO)

Vision-Language-Action models (VLAs) have demonstrated strong task understanding and generalization in robotic manipulation, yet the high computational cost of full-model inference limits their deployment in low-latency, high-frequency closed-loop control. We propose an asynchronous semantic-action decoupling framework that separates semantic understanding from action generation along the internal semantic-action interface of existing VLAs, without redesigning the vision-language backbone or introducing an external planner. A low-frequency understanding module asynchronously updates reusable semantic conditions, while a high-frequency action module continuously outputs control actions without repeatedly invoking the full model. To mitigate the temporal mismatch between stale semantics and the current execution state, we further introduce historical action conditioning and time-misalignment training, which provide short-horizon execution context and improve feedback control robustness under stale semantic conditions. Experiments on LIBERO with $\pi_{0.5}$ and UniVLA, together with real-robot deployment using UniVLA, show that the proposed framework achieves up to 35.6 Hz server-side action-module inference throughput and offers a low-intrusion path to high-frequency closed-loop control without running full VLA inference at control rate.

---

## 21. Steering Autoregressive Vision-Language-Action Policies via Action Token Intervention

**Authors:** Jason Chan, Jonathan C. Kao
**arXiv:** [2606.15021](https://arxiv.org/abs/2606.15021)
**Categories:** Robotics (cs.RO)

We present Token Steering (TS), a method for dynamically steering trajectories generated by an autoregressive vision-language-action (VLA) model through direct intervention in the action-token space. TS injects low-dimensional user inputs into the model's native action-token representation, allowing users to influence trajectory generation without modifying the underlying vision-language model (VLM) architecture. Because TS operates entirely at inference time, it requires no additional training or finetuning. User inputs guide rather than override the pretrained policy, allowing users to influence robot actions while preserving the dexterity, smoothness, and task priors learned by the VLA. We evaluate TS on two household manipulation tasks -- drawer closing after object placement and state-aware object swapping -- and improve success rates from 10.0% to 72.5% and from 16.7% to 93.8%, respectively. By enabling lightweight, intuitive steering over robot foundation models, our interface has the potential to improve human-robot interaction in consumer environments and broaden accessibility for individuals with limited physical control. Project website: this https URL .

---

## 22. Beyond English: Uncovering the Multilingual Gap in Vision-Language-Action Models

**Authors:** Hanyang Chen, Hongliang Li, Jiarui Cao, ..., Shengnan Guo, Huaiyu Wan
**arXiv:** [2606.15714](https://arxiv.org/abs/2606.15714)
**Categories:** Computation and Language (cs.CL); Robotics (cs.RO)

Vision-Language-Action models have recently demonstrated promising capabilities in learning generalist robot policies from large-scale multimodal data. However, most existing VLA systems are trained and evaluated primarily with English instructions, leaving their ability to understand and execute instructions in other languages largely unexplored. While the underlying large language models often possess multilingual capabilities, it remains unclear whether these multilingual capabilities transfer to VLAs during training. In this work, we present the first systematic study of multilingual instruction following in VLA models. We first construct multilingual instructions by extending existing benchmarks with translations of their instructions. Using these instructions, we evaluate several representative VLA models across a range of tasks in simulation settings. Our experiments reveal a significant multilingual gap: models trained primarily on English instructions exhibit substantial performance degradation when evaluated on other languages, even when the underlying language backbone is multilingual. We provide several findings and analyses to understand the multilingual gap. Cross-lingual transfer behavior analysis shows that performance drops correlate with both instruction understanding and action execution. Representation analyses suggest that multilingual instruction-caused representation shifts may contribute to the multilingual gap. Motivated by these findings, we further explore strategies to improve multilingual performance in VLAs. We propose a simple yet effective multilingual fine-tuning approach, Multilingual Principal Component Alignment, which leverages Principal Component Analysis to get the principal component subspace and align projected multilingual representations, effectively reducing the multilingual performance gap.

---

## 23. VLALeaks: Membership Inference Attacks against Vision-Language-Action Models

**Authors:** Xukun Luan, Jinyan Liu, Xuesong Li, ..., Zhongxiang Lei, Di Wang
**arXiv:** [2606.15165](https://arxiv.org/abs/2606.15165)
**Categories:** Cryptography and Security (cs.CR); Robotics (cs.RO)

Vision-Language-Action (VLA) models enable end-to-end robot control and have garnered widespread attention. However, the memorization of training data inherent to VLA, coupled with the high cost of robotic data acquisition, raises serious concerns regarding data privacy leakage and intellectual property infringement. Membership inference attacks (MIAs) aim to determine whether a given sample belongs to the training set. While representing a significant privacy threat, this attack remains underexplored in the context of VLA models. To bridge this gap, we propose VLALeaks, which is based on attention discrepancies in VLA models. We reveal, for the first time, the privacy vulnerabilities of VLA models. Specifically, it comprises a two-stage process: (1) membership feature extraction, and (2) attack model construction. Experimental results across multiple VLA benchmarks demonstrate that VLALeaks readily reveals membership information and achieves optimal attack AUC and TPR@1\%FPR, highlighting the privacy vulnerabilities in current VLA model deployments. Our work is the first systematic study of MIAs on VLA models, aiming to provide insights for secure and trustworthy VLA models.

---

## 24. MotionVLA: Vision-Language-Action Model for Humanoid Motion

**Authors:** Nonghai Zhang, Siyu Zhai, Yanjun Li, ..., Boxin Shi, Hao Tang
**arXiv:** [2606.15142](https://arxiv.org/abs/2606.15142)
**Categories:** Computer Vision and Pattern Recognition (cs.CV); Robotics (cs.RO)

Generating realistic humanoid motion from scene images and text involves both low-frequency pose semantics and high-frequency physical dynamics. However, many existing methods tokenize motion with a single shared codebook, forcing heterogeneous motion signals into the same quantization space. Our frequency-domain analysis of human motion data reveals a clear mismatch between single-codebook quantization and motion statistics: five DCT coefficients capture 93% of joint-position energy but only 37% of joint-velocity energy, which can bias quantization toward pose statistics and under-represent high-frequency velocity components. A second challenge lies in adapting a standard autoregressive model to effectively model high-frequency physical signals in motion sequences. Therefore, we propose DSFT, a dual-stream frequency tokenizer that separates motion into Base and physical streams and compresses them independently with DCT truncation and BPE. Furthermore, we present MotionVLA, a Qwen3.5-based model that arranges Base and physical tokens in a unified sequence, where Phys tokens are predicted after Base tokens. Experiments on HumanML3D and MBench show that, despite using a lightweight 2B backbone, MotionVLA reduces the Diversity gap to real data by over 50% on HumanML3D and improves Motion-Condition Consistency by 3.8% on MBench, supporting frequency-aware dual-stream decoupling as an effective formulation for autoregressive motion generation. Code: this https URL. Website: this https URL.

---

## 25. Qwen-RobotWorld Technical Report: Unifying Embodied World Modeling through Language-Conditioned Video Generation

**Authors:** Jie Zhang, Xiaoyue Chen, Anzhe Chen, ..., Xiong-Hui Chen, Chenfei Wu
**arXiv:** [2606.17030](https://arxiv.org/abs/2606.17030)
**Categories:** Computer Vision and Pattern Recognition (cs.CV)

We introduce Qwen-RobotWorld, a language-conditioned video world model for embodied intelligence. With natural language as a unified action interface, it predicts physically grounded future visual trajectories from current observations across robotic manipulation, autonomous driving, indoor navigation, and human-to-robot transfer. This unified formulation provides three promising application directions: synthetic data generation for policy training augmentation, scalable virtual environments for policy evaluation, and language-guided planning signals for downstream robot control. This is achieved through a three-part design: a) Double-Stream MMDiT with MLLM Action Encoding, where a 60-layer double-stream diffusion transformer couples frozen Qwen2.5-VL semantics with video-VAE latents through layer-wise joint attention; b) Embodied World Knowledge (EWK), an 8.6M video-text corpus (200M+ frames) with action-language mapping over 20+ embodiments and 500+ action categories; and c) General+Expert Progressive Curriculum, a two-stage training strategy that first learns general visual priors and then injects embodied specialization under a shared language interface. Extensive results show strong competitiveness: ranks 1st overall on EWMBench and DreamGen Bench, outperforms all open-source models on WorldModelBench and PBench. Additional zero-shot analyses on RoboTwin-IF benchmark further support robust generalization and multi-view consistency.

---

## 26. DreamX-World 1.0: A General-Purpose Interactive World Model

**Authors:** DreamX Team, Yancheng Bai, Rui Chen, ..., Shen Zhang, Jiashu Zhu
**arXiv:** [2606.16993](https://arxiv.org/abs/2606.16993)
**Categories:** Computer Vision and Pattern Recognition (cs.CV)

DreamX-World 1.0 is a general-purpose interactive text/image-to-video world model for controllable long-horizon generation. It supports camera navigation, revisits to previously observed regions, and promptable events across photorealistic, game-style, and stylized domains. Our data engine combines camera-accurate Unreal Engine rendering, action-rich gameplay recordings, and real-world videos with recovered camera geometry. For camera control, we introduce E-PRoPE, a lightweight variant of projective positional encoding that retains PRoPE's projective camera geometry while applying camera-aware attention to spatially reduced tokens. We convert a bidirectional video generator into a few-step autoregressive world model using causal forcing, DMD-style distillation, and long-rollout training. Training on self-generated long-horizon contexts exposes the model to its own generated history and reduces the style and color drift that accumulates across autoregressive chunks. Memory-Conditioned Scene Persistence retrieves earlier views through camera-geometry-based retrieval, while residual recycling makes the conditioning path less sensitive to imperfect memory latents. Event Instruction Tuning adds composable event control, and reinforcement learning alignment recovers camera control and visual quality after distillation. With mixed-precision DiT execution, residual reuse, 75\%-pruned VAE decoding, and asynchronous pipeline parallelism, DreamX-World 1.0 reaches up to 16\,FPS on eight RTX\,5090 GPUs. On our 5-second basic evaluation, DreamX-World 1.0 achieves a camera-control score of 73.75 and an overall score of 84.76, outperforming HY-WorldPlay 1.5 and LingBot-World in overall score, which achieve 80.79 and 80.45, respectively.

---

## 27. BadWorld: Adversarial Attacks on World Models

**Authors:** Linghui Shen, Mingyue Cui, Xingyi Yang
**arXiv:** [2606.16519](https://arxiv.org/abs/2606.16519)
**Categories:** Computer Vision and Pattern Recognition (cs.CV)

Visual world models (VWMs) synthesize interactive, action-conditioned rollouts from a single context image. However, it remains an open question how robust these models are to adversarial perturbations. Standard adversarial attacks fail to assess this vulnerability because attackers lack ground-truth future videos and cannot predict subsequent user controls. We introduce BadWorld, a label-free adversarial framework tailored for autoregressive VWMs that systematically overcomes both constraints. First, to bypass the need for future supervision, we propose a self-supervised velocity attack that directly disrupts the early denoising dynamics of the model. Second, to ensure the attack generalizes across unpredictable user actions, we formulate a trajectory-adaptive bi-level optimization that actively mines hard control sequences to forge control-agnostic perturbations. Evaluated on representative VWMs with continuous and discrete controls, BadWorld exposes severe structural fragility. Visually indistinguishable adversarial images reliably trigger catastrophic degradation in future rollouts, leading to incomplete denoising, structural collapse, and control inconsistency. These findings reveal critical risks for deploying VWMs in safety-critical systems while highlighting a practical mechanism for privacy protection.

---

## 28. GraphWorld: Long-Horizon Planning with World Models for End-to-End Autonomous Driving

**Authors:** Ziying Song, Caiyan Jia, Lin Liu, ..., Chen Lv, Yadan Luo
**arXiv:** [2606.16274](https://arxiv.org/abs/2606.16274)
**Categories:** Computer Vision and Pattern Recognition (cs.CV)

End-to-end autonomous driving has made significant progress by unifying perception, prediction, and planning within a single learning framework, achieving strong performance in short-horizon decision making. However, most existing E2E-AD methods remain confined to short-horizon planning and lack the ability to model long-term temporal dependencies, which severely limits their generalization and security in complex and highly interactive driving scenarios. In this work, we propose GraphWorld, an E2E-AD framework that explicitly enhances long-horizon planning through latent world modeling. We introduce an Ego-Centric Interaction Graph, which adaptively models critical neighboring agents based on spatial proximity, and propagates relational context to planning queries via cross-node cross-attention. We present a World-State-Conditioned Planning that learns ego-centric latent world representations by modeling interactions between an ego vehicle and surrounding agents. This latent world state captures key interaction dynamics and safety-relevant semantics, and serves as a conditioning signal to guide long-horizon, safety-aware trajectory planning. Extensive experiments on Bench2Drive, NAVSIMv1/2, and nuScenes demonstrate that GraphWorld significantly reduces collision rates and improves long-horizon planning performance, validating its effectiveness in complex driving environments.

---

## 29. Metis: A Generalizable and Efficient World-Action Model for Autonomous Driving and Urban Navigation

**Authors:** Jingyu Li, Zhe Liu, Dongnan Hu, ..., Xiatian Zhu, Li Zhang
**arXiv:** [2606.15869](https://arxiv.org/abs/2606.15869)
**Categories:** Computer Vision and Pattern Recognition (cs.CV)

World action models~(WAMs) have shown great promise for autonomous driving and urban navigation. Built upon Vision-Language-Action models or video generation models, existing approaches suffer key limitations: (1) High inference latency due to future observation prediction at test time, and (2) tightly coupled video and action modeling leading to representational mismatch and degraded generalization. To address both issues, we propose Metis, an end-to-end WAM framework that decouples video generation and action prediction. Specifically, Metis employs a Mixture-of-Transformers architecture with dedicated experts for video generation and action prediction, preserving the intrinsic distributional properties of each task. To enhance efficiency, we introduce an asymmetric attention mask that enables joint training of both experts while allowing the action model to bypass explicit video generation during inference. This design ensures training-inference consistency and significantly reduces computational costs without compromising planning performance. Extensive experiments demonstrate state-of-the-art performance on the NAVSIM navhard and navtest benchmarks and the CityWalker navigation benchmark, validating both the generalizability and efficiency across diverse tasks. Real-robot deployments further confirm the practical feasibility of our approach.

---

## 30. CausalDrive: Real-time Causal World Models for Autonomous Driving

**Authors:** Tianyi Yan, Huan Zheng, Dubing Chen, ..., Cheng-zhong Xu, Jianbing Shen
**arXiv:** [2606.15341](https://arxiv.org/abs/2606.15341)
**Categories:** Computer Vision and Pattern Recognition (cs.CV)

World models have emerged as a promising paradigm for scaling autonomous driving (AD) data, yet existing video generative models fall short as interactive simulators. Layout-conditioned renderers rely on "oracle" future trajectories of all background agents, rendering them strictly non-reactive. Conversely, pure action-conditioned predictors lack semantic control over complex interactions and suffer from prohibitive diffusion latencies, hindering closed-loop policy learning. To bridge this gap, we present CausalDrive, a controllable, real-time foundation driving world renderer. CausalDrive operates solely on the initial front-view frame, the ego-vehicle's trajectory, and a macroscopic text prompt. By excluding future NPC layouts, we compel the model to intrinsically predict causal interactions, enabling text-driven control over Driving Sociology, allowing users to dynamically orchestrate diverse counterfactual reactions to identical ego-actions. To overcome the efficiency bottleneck and address the covariate shift in autoregressive generation, we propose a novel Context-Forced DMD architecture. This combines continuous flow-matching with a self-correcting distillation objective, achieving interactive speeds of 12 FPS. This breakthrough transforms the passive video generator into a playable neural simulator. We demonstrate its versatility across three downstream applications: (1) generative closed-loop evaluation with significantly mitigated collision artifacts, (2) large-scale Reinforcement Learning (RL) post-training driven by a Video2Reward module, and (3) real-time human-in-the-loop simulation. Extensive experiments validate that policies trained within CausalDrive's reactive scenarios exhibit superior interaction capabilities in the real world.

---

## 31. Inference-time Policy Steering via Vision and Touch

**Authors:** Yilin Wu, Zilin Si, Zeynep Temel, Oliver Kroemer, Andrea Bajcsy
**arXiv:** [2606.14981](https://arxiv.org/abs/2606.14981)
**Categories:** Robotics (cs.RO); Artificial Intelligence (cs.AI); Machine Learning (cs.LG)

Inference-time steering adapts pre-trained generative robot policies during deployment by verifying candidate actions before execution. While prior methods typically perform this verification only with visual observations, vision alone is often insufficient for contact-rich manipulation, where success depends on both global task progress and subtle local interactions such as contact force. We introduce ViTaL, a visuo-tactile inference-time steering framework that formulates multimodal guidance as a bi-level optimization problem. At the high level, visual sampling-and-verification performs long-horizon mode selection, deciding what behavior the robot should execute. At the low level, tactile-guided diffusion editing refines the selected action sequence over a shorter horizon to satisfy local contact requirements. To support outcome-based steering, ViTaL learns a visuo-tactile latent world model and employs semantically aligned visual and tactile verifiers, including a novel text-conditioned tactile reward that scores predicted tactile futures directly in latent space. Across three real-world contact-rich manipulation tasks, ViTaL improves overall success by 51% over the base policy, outperforms unimodal steering by at least 33%, and exceeds naive multimodal fusion by at least 20%. Website: this https URL.

---

## 32. Geometric Action Model for Robot Policy Learning

**Authors:** Jisang Han, Seonghu Jeon, Jaewoo Jung, ..., Seungryong Kim, Sunghwan Hong
**arXiv:** [2606.17046](https://arxiv.org/abs/2606.17046)
**Categories:** Robotics (cs.RO); Computer Vision and Pattern Recognition (cs.CV); Machine Learning (cs.LG)

Generalist robot policies must follow user instructions while reasoning about how objects, cameras, and robot actions interact in the 3D physical world. Recent vision-language-action models (VLAs) and video world-action models (WAMs) inherit strong semantic or temporal priors from large-scale foundation models, but they still operate primarily on 2D image frames or 2D-derived latent spaces, leaving implicit the 3D geometry required for contact-rich manipulation. We propose the Geometric Action Model (GAM), a language-conditioned manipulation policy that directly repurposes a pretrained geometric foundation model (GFM) as a shared substrate for perception, temporal prediction, and action decoding. GAM splits the GFM at an intermediate layer: the shallow layers serve as an observation encoder, and a causal future predictor inserted at the split layer forecasts future latent tokens conditioned on language, proprioception, and action history. The predicted future tokens are then routed through the remaining GFM blocks for feature propagation and decoding, allowing a single backbone to produce both future geometry and actions. This design equips the GFM with language-conditioned temporal world modeling through minimal architectural modification while preserving its rich geometric priors. Across a broad suite of simulation and real-robot manipulation benchmarks, GAM is more accurate, more robust, faster, and lighter than current foundation-model-scale baselines.

---

## 33. ROVE: Unlocking Human Interventions for Humanoid Manipulation via Reinforcement Learning

**Authors:** Wei Xiao, Weiliang Tang, Yuying Ge, ..., Li Zhang, Yixiao Ge
**arXiv:** [2606.17011](https://arxiv.org/abs/2606.17011)
**Categories:** Robotics (cs.RO); Machine Learning (cs.LG)

Human interventions provide crucial corrective signals for post-training Vision-Language-Action (VLA) models. However, enabling seamless humanoid interventions is a formidable systems challenge due to complex whole-body kinematics and dexterous-hand control. Consequently, the collected intervention trajectories are often suboptimal, and methods that rely on human interventions as expert supervision can absorb hesitant, inefficient, or even erroneous behaviors. To address both the system and algorithmic challenges, we propose ROVE, a reinforcement learning framework for humanoid VLA post-training with imperfect human interventions. First, ROVE introduces a human-in-the-loop pipeline capable of collecting deployment and intervention data for humanoid manipulation. Second, it utilizes Optimistic Value Estimation (OVE) to prioritize high-value behaviors from mixed-quality trajectories. To further robustify value estimation, we incorporate cross-embodiment human experience videos to provide rich supervision for long-tailed failure and recovery modes. The resulting critic yields informative advantage signals, steering the VLA actor to focus on high-value behaviors rather than indiscriminately imitating all actions. On challenging real-world contact-rich and fine-grained humanoid manipulation tasks, ROVE outperforms experience-learning baselines and consistently improves across multiple rollout-intervention iterations.

---

## 34. VANDERER: Map-Free Exploration using Future-Aware and Visual-Curiosity-Guided Diffusion Policy

**Authors:** Venkata Naren Devarakonda, Raktim Gautam Goswami, Prashanth Krishnamurthy, Farshad Khorrami
**arXiv:** [2606.14879](https://arxiv.org/abs/2606.14879)
**Categories:** Robotics (cs.RO); Computer Vision and Pattern Recognition (cs.CV); Machine Learning (cs.LG)

Mobile agents require efficient exploration strategies to map unseen environments and autonomously plan tasks. Traditional methods rely on generating occupancy maps and optimizing the sequence in which unexplored regions are visited. However, in sensor-constrained settings, such as those limited to monocular cameras, generating accurate occupancy maps is challenging. To address this, we propose VANDERER, an exploration framework that leverages a Visual Curiosity Module (VCM) to guide pre-trained diffusion policies using only monocular image data. This curiosity module predicts the outcomes of proposed actions via a navigation world model and evaluates them through a curiosity cost. The cost then guides the diffusion process toward generating actions that maximize exploration. Evaluated across diverse simulated environments, VANDERER consistently outperforms established baselines, exploring an average of 13.4% more area than NoMaD. Our results reveal a direct correlation between visual and geometric curiosity in outdoor environments, demonstrating that VANDERER can effectively leverage this relationship for efficient exploration using sensor-constrained agents.

---

## 35. Scaling Short-Term Memory of Visuomotor Policies for Long-Horizon Tasks

**Authors:** Rutav Shah, Rajat Kumar Jenamani, Xiaohan Zhang, ..., Deva Ramanan, Karl Schmeckpeper
**arXiv:** [2606.16178](https://arxiv.org/abs/2606.16178)
**Categories:** Robotics (cs.RO)

Many robotic tasks require short-term memory, whether it's retrieving an object that's no longer visible or turning off an appliance after a set period. Yet, most visuomotor policies trained via imitation learning rely only on immediate sensory input without using past experiences to guide decisions. We present PRISM, a transformer-based architecture for visuomotor policies to effectively use short-term memory via two key components: (i) gated attention, which filters retrieved information to suppress irrelevant details, improving performance by reducing the spurious correlations between the history and current action prediction, (ii) a hierarchical architecture that first compresses local information into compact tokens and then integrates them to capture temporally extended dependencies, improving its compute and memory footprint. Together, these mechanisms enable us to scale short-term memory in visuomotor policies for up to two minutes. To systematically evaluate memory in visuomotor control, we introduce ReMemBench -- a benchmark of eight diverse household manipulation tasks spanning four categories of short-term memory -- designed to foster general memory mechanisms rather than siloed, task-specific solutions. PRISM consistently outperforms prior works, including recurrent architectures, transformers, and their variants -- achieving an absolute improvement of 5%--12% over the strongest baseline. On the RoboCasa and LIBERO benchmarks, it achieves absolute improvements of 11%--15% over its no-memory variant and fine-tuned Vision-Language-Action baselines such as GR00T-N1-3B and OpenVLA, despite not leveraging any large-scale pretraining. Together, PRISM and ReMemBench establish a foundation for developing and evaluating short-term memory-augmented visuomotor policies that scale to long-horizon tasks. Additional materials are available at this https URL

---
