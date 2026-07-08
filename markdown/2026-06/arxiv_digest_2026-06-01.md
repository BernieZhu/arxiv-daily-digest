# arXiv Daily Digest — 2026-06-01

**Mode:** direct
**Categories:** cs.AI, cs.LG, cs.RO, cs.CV
**Keywords:** VLA, world model, world action model
**Papers found:** 16

---

## 1. Physically Viable World Models: A Case for Query-Conditioned Embodied AI

**Authors:** Adam J. Thorpe, Stepan Tretiakov, Cheng-Hsi Hsiao, ..., Ufuk Topcu, Krishna Kumar
**arXiv:** [2605.30542](https://arxiv.org/abs/2605.30542)
**Categories:** Artificial Intelligence (cs.AI)

World models for embodied AI must be physically viable: constructed to answer intervention queries by representing the physical structure governing action outcomes, rather than merely predicting future observations. Existing observation-predictive world models can produce visually plausible but physically wrong rollouts. This failure is structural; distinct physical systems can look identical yet diverge under intervention. We expose this problem with controlled benchmarks that fix the visible scene while varying latent physics. We show that such models may recommend infeasible actions, mispredict interaction outcomes, or certify unsafe behavior. We argue that embodied AI requires world models that identify the simplest physical abstraction sufficient to answer an intervention query. Such a model comprises modular components, including environment representation, latent state and parameter estimation, action specification, interventional dynamics, and query-level response. An autonomous orchestrator should identify the relevant abstraction and compose compatible learned and structured components per query. When closed-form physics is unavailable, uncertain, or costly, the transition model may be analytic, simulated, learned, or hybrid, but it must preserve the structure that determines interventional outcomes. This decomposition makes the model interpretable, its components verifiable, and its outputs auditable against the query. It also provides a design principle for new world models and a feasibility test for existing ones: the right abstraction is not the most detailed model of the world, but the simplest model that preserves the distinctions relevant to the query. We demonstrate this approach on queries that existing systems fail to answer correctly, and outline how an orchestrator can dynamically assemble and adapt physically viable models for planning, control, and verification.

---

## 2. Dreaming Of Others: Latent Teammate Modeling In World Models For Multi-Agent Reinforcement Learning

**Authors:** Tomas Leroy-Stone
**arXiv:** [2605.31361](https://arxiv.org/abs/2605.31361)
**Categories:** Multiagent Systems (cs.MA); Artificial Intelligence (cs.AI); Machine Learning (cs.LG)

In cooperative multi-agent reinforcement learning (MARL), agents must coordinate with partners whose internal policies and intentions are not directly observable. While world models such as Dreamer have demonstrated strong generalization and sample efficiency in single-agent settings, their application to MARL remains limited by an inability to handle teammate-induced uncertainty. We propose a new perspective: treat teammates as structured, learnable components within the agent's world model. We introduce an architecture that factorizes the latent state of a Dreamer-style recurrent state-space model (RSSM) into environment and teammate components, and learns an auxiliary Theory-of-Mind (ToM) head to infer latent embeddings of partner behavior such as character, intent, and predicted actions from partial trajectories. These teammate latents condition the actor and critic, enabling the agent to imagine and adapt to diverse collaborators. We outline how this approach can support zero-shot and few-shot coordination in partially observable settings and propose a set of benchmarks and evaluation protocols to assess its impact. This work positions world models as not only predictors of environmental dynamics, but as simulators of social behavior, opening new directions for generalizable, human-compatible AI.

---

## 3. DeMaVLA: A Vision-Language-Action Foundation Model for Generalizable Deformable Manipulation

**Authors:** Taiyi Su, Jian Zhu, Tianjian Wang, ..., Weihao Ding, Yi Xu
**arXiv:** [2605.31286](https://arxiv.org/abs/2605.31286)
**Categories:** Robotics (cs.RO); Artificial Intelligence (cs.AI)

Real-world household robots require Vision-Language-Action (VLA) foundation models that can acquire reusable manipulation skills across diverse objects, task conditions, and household environments. Deformable-object folding is a representative challenge, requiring robots to handle clothing items from random initial states across varying categories, geometries, materials, and scenes. However, existing VLA systems commonly train separate policies for different object categories, while naively mixed multi-task training often suffers from task interference and degraded performance. To move beyond category-specific folding policies, we introduce DeMaVLA, a VLA foundation model for generalizable Deformable Manipulation. DeMaVLA adopts a VLM backbone with an action expert and formulates continuous action generation using flow matching. To improve efficiency, the action expert is constructed by pruning every other transformer layer while preserving layer-wise alignment with the VLM backbone, reducing training and inference cost. DeMaVLA is first pre-trained on approximately 5,000 hours of selected real-world dual-arm demonstrations to acquire general manipulation priors. It is then post-trained on mixed folding data that aggregates self-collected demonstrations and corrective trajectories from real-robot failures across multiple folding tasks through a human-in-the-loop Data Aggregation~(DAgger) pipeline. Experiments show that DeMaVLA achieves competitive performance on RoboTwin and strong real-world results on our household folding benchmark. These results highlight the value of scalable real-world data, efficient action generation, and corrective learning for general-purpose VLA policies in deformable-object manipulation.

---

## 4. Does Visual Information Play a Decisive Role in Vision-Language-Action Model Driving Behavior?

**Authors:** Jingtao He, Hongliang Lu, Xiaoyun Qiu, Yixuan Wang, Xinhu Zheng
**arXiv:** [2605.31041](https://arxiv.org/abs/2605.31041)
**Categories:** Computer Vision and Pattern Recognition (cs.CV); Artificial Intelligence (cs.AI)

Vision-Language-Action (VLA) models have demonstrated promising capability in autonomous driving, highlighting the potential of unified multimodal architectures for jointly modeling perception and planning. However, how current VLA-based driving behavior is grounded in visual information remains poorly understood. Existing evaluation protocols mainly focus on aggregate performance metrics, lacking structured and practical diagnostics to quantify visual-behavior dependency. In this work, we introduce a structured multi-level visual perturbation framework to analyze visual-behavior dependency in VLA-based driving models systematically. The framework organizes controlled visual perturbations along three complementary dimensions: channellevel degradation, information-level disruption, and structurelevel modification. We apply it to VLA-based driving systems and evaluate behavioral responses under both open-loop trajectory prediction and interactive closed-loop safety evaluation. Experimental results reveal evaluation-dependent dependency patterns and uneven visual grounding across abstraction levels. These findings call for more structured analyses and principled design of VLA driving models to better understand how visual information shapes behavior and develop safer, more robust systems.

---

## 5. PatchWorld: Gradient-Free Optimization of Executable World Models

**Authors:** Jiaxin Bai, Yue Guo, Yifei Dong, ..., Jeff Pan, Yangqiu Song
**arXiv:** [2605.30880](https://arxiv.org/abs/2605.30880)
**Categories:** Computation and Language (cs.CL); Artificial Intelligence (cs.AI)

Text-agent environments are typically modeled as partially observable Markov decision processes (POMDPs), assuming that the simulator's latent state and transition dynamics are hidden from the agent. Yet little work has examined whether executable code can be induced to serve as a world model for prediction and planning under partial observability. We introduce PatchWorld, a gradient-free framework that turns offline trajectories into executable Python world models through counterexample-guided code repair. Instead of predicting the next observation with a black-box model, PatchWorld induces symbolic belief-state programs whose action updates can be inspected, replayed, and locally patched. Across seven AgentGym environments, PatchWorld-Simple achieves the highest code-based planning score among evaluated methods, reaching 76.4\% macro success in live one-step lookahead while invoking no LLM calls inside the world-model prediction module itself. We further find that a human-specified residual-memory bias improves surface observation fidelity but weakens decision utility. This exposes a tradeoff in executable world models, since improving observation fidelity can come at the expense of action-discriminative dynamics, and vice versa. Code is available at this https URL.

---

## 6. Hide-and-Seek in Trajectories: Discovering Failure Signals for VLA Runtime Monitoring

**Authors:** Seongheon Park, Wendi Li, Changdae Oh, ..., Michael Hagenow, Sharon Li
**arXiv:** [2605.30834](https://arxiv.org/abs/2605.30834)
**Categories:** Robotics (cs.RO); Artificial Intelligence (cs.AI)

Vision-Language-Action (VLA) models enable robots to follow natural language instructions and generalize across diverse tasks, but they remain vulnerable to execution failures that compromise reliability in real-world deployment. Detecting such failures during execution is therefore critical for the robust deployment of embodied systems. Existing failure detection methods either rely on expensive action resampling or external models, while alternatives propagate trajectory-level labels uniformly across every timestep, obscuring localized failure signals. In this paper, we propose \textbf{Hide-and-Seek}, a framework that formulates VLA failure detection as a coarsely supervised learning problem. By combining inter-trajectory and intra-trajectory contrastive objectives, Hide-and-Seek localizes failure-indicative actions and induces temporally structured failure signals from trajectory-level supervision alone, without any step-level annotation. We evaluate Hide-and-Seek on LIBERO, VLABench, and a real-world robotic platform across three representative VLA policies: OpenVLA, $\pi_0$, and $\pi_{0.5}$.Our method achieves state-of-the-art multi-task failure detection performance with a practical accuracy--timeliness trade-off under conformal prediction, and generalizes well to both seen and unseen tasks.

---

## 7. Subspace-Decomposed JEPAs: Disentangling Progression and Content in Latent World Models

**Authors:** Lucas Thil, Jesse Read, Rim Kaddah, Guillaume Doquet
**arXiv:** [2605.31111](https://arxiv.org/abs/2605.31111)
**Categories:** Machine Learning (cs.LG)

Joint-Embedding Predictive Architectures (JEPAs) learn compact latent world models by predicting future embeddings, but no single coordinate of the latent is designated to encode task progression. We carve the JEPA latent into two orthogonal subspaces with disjoint roles: a low-dimensional progression subspace shaped by a cosine-margin triplet loss, and a high-dimensional content subspace regularised by the existing SIGReg objective of LeWM. We prove that the two anti-collapse forces act on disjoint coordinates, so they compose additively rather than competing on the same dimensions. Our method, SD-JEPA improves over the LeWM baseline on the majority of its control benchmarks at matched compute, and outperforms the strongest non-LeWM JEPA baseline on Push-T; a subspace-ablation falsifier confirms the split is the load-bearing ingredient. Beyond planning, the resulting 1-D angular progression coordinate functions as a scene-aware compass on the latent. It advances with task progress, regresses when the agent backtracks, and under controlled perturbations both spikes and relocalises to a semantically appropriate new task-phase sector, separating the moment of surprise from its meaning in a way that prediction-error scalars cannot. Three quantitative tests back this up: $|\Delta\theta_t|$ outperforms the standard latent-prediction-error surprise at localising semantic events on 40 held-out cube episodes by up to +0.18 pooled AUROC (97.5% per-episode win rate at $\pm 1$-step tolerance); a within-episode linear probe across all four environments (40 episodes per env) shows the 8-dimensional progression subspace (4.2% of the latent) explains 72-95% of task-progress variance..

---

## 8. BOKBO (Best of K Bad Options): Calibrated Abstention for VLA Policies

**Authors:** Anya Singh, Cabrel Happi, Jai Relan, Varun Nair, Vidyut Baradwaj
**arXiv:** [2605.30660](https://arxiv.org/abs/2605.30660)
**Categories:** Machine Learning (cs.LG); Robotics (cs.RO)

Test-time scaling for vision-language-action (VLA) policies, methods such as RoboMonkey, SEAL, MG-Select, and V-GPS, samples K candidate action chunks at inference and executes the verifier-best. When all K candidates are unsafe, the system executes a violating action with no warning. We propose BOKBO, the first conformal abstention layer for K-sample VLA inference, providing finite-sample distribution-free guarantees on executed-violation rate. We provide both global and per-task (Mondrian) variants, with the per-task variant closing the conditional gap on the hardest tasks.
Our analysis exposes a structural failure of policy-internal nonconformity scores under perturbation-based K-sampling: the base-policy confidence proxy and K-sample disagreement correlate at 0.98 with the action-noise hyperparameter $\sigma$, while correlating at the noise floor with actual safety violations. We test the failure's scope by replicating the analysis under token-level temperature sampling and find the failure is mechanism-specific and partially mitigated under policy-stochasticity-based sampling. A learned violation predictor conditioned on semantic visual features and task identity supports tight calibration: at $\epsilon$ = 0.05 on libero_object_temp_x0.1 with OpenVLA-OFT, the conditional CRC bound holds on 86% of bootstrap splits with 78% coverage and 70% net task success. Mondrian-BOKBO raises the minimum per-task conditional hold fraction from 0.71 to 0.93. Results are stable across 5 training seeds, replicate within bootstrap noise on $\pi_0$-FAST, hold on libero_spatial_temp_x0.1 as a co-equal benchmark, and survive four within-suite distribution shifts. We additionally identify and correct a methodological pitfall: globally-set force thresholds well below expert-typical manipulation forces conflate unsafe behavior with normal manipulation, inflating violation rates by $5\times$.

---

## 9. Light Interaction: Training-Free Inference Acceleration for Interactive Video World Models

**Authors:** Jiacheng Lu, Haoyi Zhu, Sipei Yi, ..., Yu Li, Cheng Zhuo
**arXiv:** [2605.31158](https://arxiv.org/abs/2605.31158)
**Categories:** Computer Vision and Pattern Recognition (cs.CV); Machine Learning (cs.LG)

Interactive video world models generate video chunk by chunk in response to user-controlled camera movements, enabling applications such as real-time game simulation, virtual scene navigation, and embodied AI training. However, scaling to long interactive trajectories is prohibitively expensive due to growing context memory, quadratic attention complexity, and repeated denoising steps. We present Light Interaction, a training-free inference acceleration framework for interactive video world models. Our key insight is that interaction naturally enables trajectory-dependent adaptive computation: retrieved spatial memory can be discarded during novel exploration, temporal context can be adjusted according to local latent dynamics, and early-step model outputs can be reused when the camera revisits familiar regions. Based on this insight, Light Interaction combines adaptive context management, denoising cache acceleration, and hardware-software co-designed 3D block sparse attention with fused Triton kernels. Evaluated on HY-WorldPlay and Matrix-Game-3.0, Light Interaction achieves up to 2.59x speedup without model retraining while maintaining competitive visual quality.

---

## 10. AR Forcing: Towards Long-Horizon Robot Navigation World Model

**Authors:** Yifei Yang, Zehua Fan, Huan Li, ..., Bingchuan Sun, Yan Wang
**arXiv:** [2605.31314](https://arxiv.org/abs/2605.31314)
**Categories:** Robotics (cs.RO)

The diffusion based robot navigation world models are typically trained using parallel supervision, while autoregressive inference is employed during path planning. This results in a distribution shift between training and inference, which destabilizes the performance over long-horizon prediction. We propose AR Forcing, an autoregressive training strategy, which integrates the standard diffusion loss into the autoregressive training loop. At each step, the model uses its own predictions to update the context and optimize the single step noise prediction objective, thereby explicitly exposing the model to the inference state distribution during training. Our method does not require additional discriminators or distribution-matching losses, retains the original diffusion framework and sampler, and is easy to integrate. Experiments on multi-domain navigation datasets (RECON, SCAND, HuRoN, TartanDrive) show that compared with strong baselines, AR Forcing improved the consistency of generated images during long-horizon navigation and the accuracy of predicted trajectories, enhancing robustness of the model in complex known and unknown environments. We will release the code soon.

---

## 11. HARP-VLA: Human-Robot Aligned Representation Learning for Vision-Language-Action Model

**Authors:** Xiang Zhu, Puzhen Yuan, Yichen Liu, Jianyu Chen
**arXiv:** [2605.31234](https://arxiv.org/abs/2605.31234)
**Categories:** Robotics (cs.RO)

Learning generalizable vision-language-action (VLA) models from large-scale human videos is promising but challenging due to cross-embodiment discrepancies in both visual observations and executable actions. While latent action models reduce the action execution gap by learning action abstractions, they still rely on visual features. Thus, misaligned human and robot visual representations can lead to inconsistencies in policy inputs and induce domain-dependent latent actions, hindering effective co-training with human videos. To address this, we propose HARP, a human-robot aligned representation learning framework for more effective VLA pretraining from human videos. Specifically, HARP uses limited paired human-robot demonstrations as cross-embodiment bridges and abundant unpaired human and robot videos as a scalable dynamics supervision data source. It trains a robot-adapted visual encoder and a latent action model with manipulation-centric auxiliary cues and a source-relative pair-discriminative alignment loss, which adapts robot representations toward human semantics while preserving pair-level discrimination. The learned aligned vision encoder and latent action model provide a unified vision and action representation for VLA-style policy learning, where human and robot videos provide vision-language-to-latent-action supervision and a lightweight robot action head grounds latent actions into executable commands. Experiments on feature visualization, simulation, and realworld manipulation show improved human-robot alignment and downstream policy performance, achieving 4.481 average length on CALVIN ABC$\rightarrow$D and a 7.1\% realworld success rate gain over the strongest baseline.

---

## 12. Can Aerial VLA Models Cooperate? Evaluating Closed-Loop Air-Ground Coordination with CARLA-Air

**Authors:** Tianle Zeng, Yanci Wen, Xueang Yu, Hong Zhang
**arXiv:** [2605.31066](https://arxiv.org/abs/2605.31066)
**Categories:** Robotics (cs.RO)

Recent aerial vision-language-action (VLA) models show promising single-UAV capabilities, such as tracking moving objects and navigating to language-specified landmarks. However, it remains unclear whether these capabilities can transfer to air-ground cooperation, where a UAV and a UGV must act jointly in a shared, closed-loop physical world.
We study this question with CARLA-Air, a single-process air-ground evaluation environment that unifies CARLA and AirSim inside one Unreal Engine runtime. By sharing the same world state, physics tick, and sensing pipeline, CARLA-Air enables physically consistent UAV--UGV interaction and precise measurement of simulation-timestamp alignment and effective coordination latency.
Using CARLA-Air, we evaluate representative aerial VLA and planning baselines on two complementary diagnostic tasks: moving-platform landing and occlusion-recovery escort. The results show that current aerial VLA models can often track or follow a ground partner, but struggle to convert this single-agent competence into stable cooperative behavior. State prompting provides limited benefit, and naive bidirectional interaction fails to consistently improve performance and can amplify errors for most baselines. These findings suggest that, under the tested text-based cue interfaces, zero-shot cooperative air-ground VLA requires three components beyond the current paradigm: explicit partner-state grounding, low-latency action coordination, and team-level objective alignment. Our code is available at this https URL.

---

## 13. Primitive Subspaces Mediate Few-Shot Transfer in VLAs

**Authors:** Anya Singh, Cabrel Happi, Jai Relan, Varun Nair, Vidyut Baradwaj
**arXiv:** [2605.30695](https://arxiv.org/abs/2605.30695)
**Categories:** Robotics (cs.RO)

Deploying vision-language-action (VLA) policies in industrial environments requires the ability to teach new tasks at low cost, a property current VLAs lack, since each new task requires fine-tuning. We investigate whether primitive-aware training produces a transferable artifact: a learned library of sub-skills that can be composed at inference time, conditioned on a small number of demonstrations, to perform tasks the policy was never trained on. We train two VLA architectures with different inductive biases, OpenVLA and $\pi_{0.5}$, on the REASSEMBLE contact-rich assembly dataset under matched LoRA fine-tuning recipes and locked hyperparameters, varying training between flat trajectories and primitive-segmented episodes with primitive-specific language prompts. We hold out 6 object-task combinations from training and evaluate few-shot transfer: models receive $m \in \{0, 1, 3, 5, 10\}$ demonstrations of a held-out task and attempt execution without weight updates. We replicate across three training seeds and validate on a second dataset (LIBERO-Long). Primitive-trained models reach 78% of fine-tuned upper-bound performance with only m=3 demonstrations, while flat-trained models require m=10 demonstrations to reach the same level -- a $3\times$ sample efficiency gap that replicates across seeds, architectures, and datasets. To establish causation, we ablate the primitive-decodable subspace of hidden states and show few-shot transfer degrades by 32 percentage points while ablating a random subspace of equal dimensionality has no effect, indicating primitive representations are causally necessary rather than incidentally correlated with transfer. We identify and correct a methodological pitfall in evaluating chunked policies: family-wise inflation of single-step action-range gates produces order-of-magnitude higher false-failure rates against ground-truth human demonstrations.

---

## 14. ELAN4D: Embodiment-Centric 4D Supervision for Vision-Language-Action Models via Plug-and-Play Adaptation

**Authors:** Zeyuan He, Bowen Yang, Zhirui Fang, ..., Li Jiang, Jialin Yu
**arXiv:** [2605.30484](https://arxiv.org/abs/2605.30484)
**Categories:** Robotics (cs.RO)

Vision-Language-Action (VLA) models have shown promise for robotic manipulation, yet most existing policies operate reactively by directly regressing actions from current observations, without explicitly modeling future dynamics. This limits their ability to generalize under out-of-distribution perturbations. To address this issue, we propose ELAN4D, an embodiment-centric, 4D-aware training framework that enhances VLA policies with future robot keypoint tracks as predictive spatio-temporal supervision. Using only forward kinematics from proprioceptive states, we derive 3D displacement tracks of robot keypoints, such as joints and the end-effector, with negligible preprocess cost. These tracks provide metric and compact supervision without requiring external trackers or reconstruction. A plug-and-play auxiliary branch with a lightweight track decoder injects this 4D signal into the action expert while preserving the pretrained vision-language backbone through gradient isolation. The track decoder is discarded during inference, leaving the base policy interface unchanged. Extensive experiments on LIBERO, LIBERO-Plus, RoboTwin2.0 and real-world manipulation tasks demonstrate that ELAN4D consistently improves over strong VLA baselines, achieving the best overall performance and substantial gains under out-of-distribution perturbations, including camera, background, and layout shifts. These results highlight the effectiveness of embodiment-centric 4D supervision for building more robust and generalizable manipulation policies.

---

## 15. DriveMA: Driving Vision-Language-Action Models with verifiable Meta-Actions

**Authors:** Weicheng Zheng, Yixin Huang, Qiao Sun, Derun Li, Hang Zhao
**arXiv:** [2605.31271](https://arxiv.org/abs/2605.31271)
**Categories:** Computer Vision and Pattern Recognition (cs.CV)

Driving Vision-Language-Action Models (Driving VLAs) aim to use language to improve end-to-end planning, but the language-action gap limits this promise. We propose DriveMA, a Driving VLA framework built on verifiable meta-actions, which summarize future ego motion into compact language-domain intentions and can be constructed from expert trajectories with a trajectory-grounded annotation pipeline and can be verified against generated trajectories through rule-based projection. DriveMA exploits this verifiability with action-centric supervised training and a data-efficient turn-level credit assignment reinforcement learning framework, explicitly aligning high-level decisions with low-level trajectory planning through dense rewards and precise credit assignment. DriveMA sets a new state of the art on the Waymo Open Dataset Vision-based E2E Driving, achieving a Rater Feedback Score of 8.060 with a 2B model and further improving it to 8.079 with a 4B model; it also obtains competitive closed-loop planning performance on NAVSIM. These results show that even a simple meta-action interface can achieve state-of-the-art planning when made verifiable and optimized for language-action alignment. Code, data, and models will be released to facilitate future research.

---

## 16. IDOL: Inverse-Dynamics-Guided Future Prediction for End-to-End Autonomous Driving

**Authors:** Chenghao Zhang, Timin Li, Dongmei Li
**arXiv:** [2605.31476](https://arxiv.org/abs/2605.31476)
**Categories:** Robotics (cs.RO)

End-to-end autonomous driving has emerged as a compelling paradigm for learning planning directly from sensor observations, while recent world-model-based approaches further enrich this paradigm by enabling explicit reasoning about how the scene may evolve in the future. Yet future prediction alone does not guarantee better planning unless the predicted evolution can be converted into planning-relevant trajectory updates. Many current methods still forecast future scene states without explicitly decoding the motion implications hidden in state transitions. As a result, future reasoning often remains descriptively useful but only weakly coupled to executable motion generation. To address this limitation, we propose \mathbf{IDOL}, an inverse-dynamics-guided future prediction framework for world-model-based end-to-end planning in latent BEV space, where inverse dynamics serves as the key bridge between future prediction and trajectory optimization. IDOL first predicts multiple future latent scene states with a BEV world model, then applies an inverse dynamics model to adjacent latent futures to decode transition-aware trajectory features and recover planning-relevant motion deltas that explain how the latent world evolves over time. These inverse-dynamics-derived signals are used to optimize the planned trajectory, turning future forecasting from passive scene anticipation into actionable planning guidance. A lightweight closed-loop refinement module further improves long-horizon consistency by reusing the optimized trajectory for another round of future-aware reasoning. By introducing inverse dynamics into latent future reasoning, IDOL tightens the coupling between world modeling and planning. Extensive experiments on the NAVSIM v1 and NAVSIM v2 benchmarks show that IDOL achieves state-of-the-art performance among comparable methods.

---
