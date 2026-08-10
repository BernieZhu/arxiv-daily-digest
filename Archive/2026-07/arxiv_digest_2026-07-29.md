# arXiv Daily Digest — 2026-07-29

**Mode:** direct
**Categories:** cs.AI, cs.LG, cs.RO, cs.CV
**Keywords:** VLA, world model, world action model
**Papers found:** 10

---

## 1. CoTinyVLA: Chain-of-Thought Distillation for a Sub-Billion-Parameter Vision-Language-Action Model

**Authors:** Minhyeok Lee, Chiyoung Kim, Chanhoe Gu, ..., Donghun Ryu, Seokhyun Kim
**arXiv:** [2607.25487](https://arxiv.org/abs/2607.25487)
**Categories:** Artificial Intelligence (cs.AI); Computer Vision and Pattern Recognition (cs.CV)

Vision-Language-Action (VLA) models translate natural-language commands into robot action sequences, but leading systems on the LIBERO-Plus robustness benchmark use three- to seven-billion-parameter backbones whose memory demands can exceed embedded robotic budgets. We present CoTinyVLA, a 0.9B-parameter action model on a Qwen3.5-0.8B backbone that obtains that robustness by structuring supervision instead of enlarging the model. Three components target different axes of the problem: dual-view temporal input of 16 history frames per step with textual camera and time markers; hierarchical chain-of-thought (CoT) distillation from a 35B teacher into an episode-level Plan and a chunk-level Think span over task phase, gripper state and next subaction; and paraphrase augmentation expanding 40 base commands into 800 variants. On LIBERO-Plus, spanning 10,030 perturbed tasks across seven perturbation dimensions, CoTinyVLA reaches 90.8% on Spatial, 87.3% on Object, 86.6% on Goal and 80.7% on Long, leading the strongest 7B baseline on all four suites by 4.7, 2.8, 15.9 and 3.0 points, with every margin interval excluding zero. The gains concentrate on the hardest axes of the benchmark: across the eleven published baselines none exceeds 53.2% on Robot Initial States in any suite, whereas CoTinyVLA reaches 73.6% on Goal against 39.9% for the strongest baseline. Ablations show the three components to be separable by perturbation axis, and at a matched image budget how frames are divided between the two cameras and across time accounts for 8.6 points on its own. Closed-loop inference peaks at 2.25 GiB of allocated GPU memory, and paired interventions show the episode Plan to be load-bearing: replacing it with an empty or contradictory span costs 40 to 45 points of success. Structured supervision thus lets a 0.9B backbone exceed all of them. Code: this https URL

---

## 2. SAM3D-Guided Object-Centric Representation Alignment for Vision-Language-Action Models

**Authors:** Zonghe Liu, Shanyuan Jie, Xiaoquan Sun, ..., Zongsheng Liu, Jiayu Chen
**arXiv:** [2607.25912](https://arxiv.org/abs/2607.25912)
**Categories:** Robotics (cs.RO); Artificial Intelligence (cs.AI)

Vision-Language-Action (VLA) models have shown strong potential for general robot manipulation, but most existing models rely on 2D visual-language backbones and lack fine-grained 3D understanding of target objects, especially under occlusion, pose variation, scale changes, and precise spatial interaction. We propose an object-centric 3D representation alignment framework built upon $\pi_0$, using SAM3D as a frozen 3D teacher to provide target-object 3D priors during training. Specifically, we localize task-relevant objects with object recognition models, generate corresponding object masks, and use SAM3D to extract dense object-level 3D representations, which are aligned with intermediate visual features of $\pi_0$. This enables the policy to internalize target-object 3D information while preserving the original RGB-language-to-action inference pipeline without requiring depth, point clouds, masks, SAM3D, or additional 3D modules at test time. Simulation experiments show consistent improvements, achieving 99.1\% on LIBERO and an average length of 4.11 on CALVIN. Real-world experiments further demonstrate that our method is particularly effective in long-horizon manipulation scenarios where the robot must focus on different target objects across multiple subtasks.

---

## 3. Reinformed Dreamer: An Asymmetric World Model Efficiently Trained through Latent Guidance

**Authors:** Gaspard Lambrechts, Adrien Bolland, Daniel Ebi, Damien Ernst
**arXiv:** [2607.26040](https://arxiv.org/abs/2607.26040)
**Categories:** Machine Learning (cs.LG); Machine Learning (stat.ML)

Much like humans benefit from guidance while learning, reinforcement learning algorithms may benefit from additional supervision beyond rewards. Leveraging additional information during training to learn better representations and behaviors has been the focus of asymmetric reinforcement learning. This learning paradigm has proven effective under partial observability when additional state information is available, but also under full observability when more refined state information is available. Focusing on model-based reinforcement learning, we study the effect of asymmetric learning on observation representations and on privileged information representations. First, we identify a limitation in the privileged information representations learned by an asymmetric model-based algorithm known as the Informed Dreamer. Then, we propose a novel asymmetric representation learning objective using latent guidance, resulting in a new algorithm called the Reinformed Dreamer. Experiments across several benchmarks show a more consistent improvement over Dreamer than previous asymmetric approaches.

---

## 4. INTACT: Isomorphic Intent-to-Action Learning for Search-Free World Models

**Authors:** Junhan Sun, Hao Zhao, Guofeng Zhang
**arXiv:** [2607.26056](https://arxiv.org/abs/2607.26056)
**Categories:** Robotics (cs.RO)

Forward latent world models predict how actions change a scene, but recover actions for a desired change only through expensive test-time search. We introduce INTACT (INtent-To-ACTion), an end-to-end JEPA that turns action-labeled, reward-free trajectories into a deployable intent-to-action interface. Each transition supplies physical intent $z_{t+1}-z_t$, while a future goal supplies deployment intent $\operatorname{sg}(z_g)-z_t$. The architecture is isomorphic between the local and goal motion-intent backbone-input graphs through an identical four-slot grammar and shared parameters, and between supported local and goal motion-intent families through action-law semantics induced by the same predictor rather than pointwise latent equality. INTACT also provides intact transfer from RGB evidence to action-effective latent intent coordinates and from intent families to their corresponding action-law families. Asymmetric endpoint gradients ground physical successors and fix future goals as anchors, joining representation learning and control without pointwise latent matching or globally linear dynamics. The resulting coordinates support a robust distributional action law: its conditional mean serves directly as a search-free policy, while sampling remains available for diversity or optional verification. On the four official LeWM tasks, one-epoch, zero-search models reach 85.78\%, 100.00\%, 97.67\%, and 97.89\% success. Optional local CEM centered on the Direct plan reaches 96.86\% macro success using 384 instead of 9,000 candidate sequences, reducing sampling by $23.44\times$ while improving pure CEM by 16.00 points. One shared four-task encoder reaches 89.39\% E5 Direct macro and improves every task over jointly trained LeWM, while predicted--expert action-family kNN tracks Direct success at $r=0.954$. Direct inference takes 2.9--5.5 ms.

---

## 5. DC-WAM: Dynamic-Centric Visual Supervision and Reasoning for World-Action Models

**Authors:** Haoyuan Ji, Lingxiang Fan, Shang Su, ..., Jun Gao, Shuo Feng
**arXiv:** [2607.25918](https://arxiv.org/abs/2607.25918)
**Categories:** Robotics (cs.RO)

World-Action Models (WAMs) augment robot policies with future visual prediction, but it remains unclear what the visual modality should learn for control. While photorealistic future prediction provides dense supervision, it also incurs substantial computation and can allocate capacity to texture, illumination, and background variations that are only weakly related to action selection. Recent efficient WAM variants suggest that the main benefit of the video branch may not lie in the rendered future itself, but in the control-relevant visual representations induced during training. In this work, we revisit future video prediction from a dynamic-centric perspective and ask whether an existing RGB-based WAM can be redirected from appearance-dominated reconstruction toward interaction-induced visual dynamics without introducing additional modality-specific predictions or online inputs at deployment. We propose DC-WAM, a dynamic-centric WAM framework that redistributes supervision and computation in the RGB video branch. At the supervision level, DC-WAM combines temporal-difference flow matching with trajectory-guided weighting, emphasizing dense temporal changes and localized regions where the gripper, manipulated objects, and contact areas move. At the reasoning level, DynaRoute predicts token-wise dynamic relevance and converts it into an attention bias, guiding the model toward control-relevant future tokens. Experiments in simulation and on real-world manipulation tasks show that DC-WAM consistently improves policy performance, especially under out-of-distribution perturbations in lighting, object appearance, and background texture.

---

## 6. A Causality-aware Infer-diagnose-refine Framework for Test-time Modality Adaptation in VLA Models

**Authors:** Haoyu Zhang, Yuwei Wu, Jin Chen, ..., Yongchun Liu, Fan Li
**arXiv:** [2607.25516](https://arxiv.org/abs/2607.25516)
**Categories:** Robotics (cs.RO)

Vision-language-action (VLA) models predict sequential actions to execute tasks specified by language instructions, conditioned on visual observations and proprioceptive states. However, how to fuse modalities in VLA models remains an open problem, since robot manipulation involves dynamic phases, such as long-distance movements and close-range interactions, in which the importance of visual observations may vary over time. In this paper, we propose an infer-diagnose-refine (IDR) framework, a model-agnostic framework that can be integrated with diverse VLA architectures for refining action predictions at test time. IDR first infers actions under factual and counterfactual scenarios of visual observations, and then diagnoses the causal effects of visual observations as the estimated dynamic importance, which is finally used to refine the action predictions in a training-free manner. We further design a causality-aware action refiner to realize the IDR framework, including zero-padding interventions for inferring counterfactual actions, norm-based quantification for diagnosing causal effects, and gated residual fusion for refining actions. Extensive experiments on both simulation benchmarks and real-world tasks show improvements in overall performance across multiple VLA backbones, demonstrating the efficacy of dynamically adjusting visual importance at test time.

---

## 7. Temporal-Distance JEPA: Plan-Aware Representation Learning for Latent World Model Predictive Control

**Authors:** Jiaxin Bai, Jiaxuan Xiong
**arXiv:** [2607.25337](https://arxiv.org/abs/2607.25337)
**Categories:** Computation and Language (cs.CL); Robotics (cs.RO)

Joint-Embedding Predictive Architectures (JEPAs) learn world models by predicting in representation space rather than reconstructing pixels, making them a natural backbone for latent model predictive control from offline demonstration logs. JEPA-style training optimizes short-horizon latent prediction, whereas planning requires a multi-step ranking of imagined futures by goal progress. Prior JEPA planners often inherit that ranking from embedding geometry, typically latent Euclidean distance, which arises as a byproduct of representation learning rather than as a progress cost mined from the logs. We propose Temporal-Distance-JEPA, which retains the LeWM encoder--predictor backbone and mines a directed temporal cost from reward-free trajectories: same-trajectory step order supplies positive targets, cross-trajectory pairs act as heuristic negatives, and a rollout-consistency term matches the planner horizon. The mined supervision serves two roles: as the deployed planning cost when progress is topological, and as a representation signal that improves Euclidean planning when contact geometry dominates. Under locked evaluation, deploying the mined cost raises Two-Room success to 100.0% versus LeWM's 97.4%, while shared Euclidean planning on the same temporally trained checkpoint raises OGB-Cube by 14.2 points over LeWM and improves Push-T. Against LeWM and the concurrent RC-aux baseline under locked evaluation, Temporal-Distance-JEPA matches or exceeds both methods on every environment. Ablations show that the directed head, cross-trajectory negatives, and rollout consistency each contribute. Temporal-Distance-JEPA narrows the train--plan gap for JEPA world-model planners by discovering temporal progress structure in offline logs and co-designing cost form with plan-time deployment. Code is available at this https URL.

---

## 8. VisualPatchWorld: Code World Models as Latent Structured Representations for Planning

**Authors:** Jiaxin Bai, Jiaxuan Xiong
**arXiv:** [2607.25236](https://arxiv.org/abs/2607.25236)
**Categories:** Computation and Language (cs.CL); Robotics (cs.RO)

Different research lines use the term world model in different ways, yet they share a common aim: to capture how the world evolves under action in a form that supports perception, simulation, and planning. Two prominent realizations are neural predictors that learn dynamics in continuous vector spaces, and hand-built physics engines that expose explicit state and physical laws. Neural predictors scale from data but leave the form of the dynamics implicit; physics engines are inspectable and editable but difficult to construct at scale. We introduce VisualPatchWorld (VPW), which represents world dynamics as code. VPW first selects a qualitative dynamical form with short active probes, then fits that form's free parameters from recorded state-action traces by minimizing multi-step prediction error. The resulting programs can be rolled forward like a simulator, inspected in source form, and used inside model-predictive control; image-derived scene graphs can supply the live state at replan time. Across comparisons with prior code-based world models, VPW attains 69.0% mean planning success and exceeds the strongest code baseline by 23.5 points. The largest gains arise when choosing the correct qualitative dynamics is essential. Under the same planner, the induced models approach ground-truth engine success on navigation and grasp-rich control; a residual gap remains for contact-rich pushing, and checking a shortlist of promising plans in the engine closes most of that gap. These results establish a practical route toward automatically constructed code world models that are useful for planning. Code is available at this https URL.

---

## 9. Wonder: Video World Model Done Better

**Authors:** Jiacong Xu, Hanwen Jiang, Zhixin Shu, ..., Vishal M. Patel, Yiqun Mei
**arXiv:** [2607.26037](https://arxiv.org/abs/2607.26037)
**Categories:** Computer Vision and Pattern Recognition (cs.CV); Graphics (cs.GR)

We present Wonder, a general-purpose video world model for real-time, camera-controllable world exploration. Given an image or a conditional video, Wonder constructs a playable world where users can navigate interactively by moving the camera, discovering unseen regions, and revisiting previously observed areas in real time and over a long-term horizon. Achieving this capability requires a system-level co-design of control method, memory mechanism, and training strategy. We introduce a novel camera conditioning with a dense coordinate field whose renderings provide spatially aligned motion and orientation cues, allowing the model to interpret camera motion directly as visual evidence. To support fast and precise memory retrieval over a growing generation context, we propose an efficient sparse attention-based memory mechanism, enabling the model to selectively attend to a small set of relevant context tokens at inference time, regardless of actual context length. We further develop several techniques to rectify the self-forcing-style distillation pipeline, improving the student model's ability to respect control signals, as well as maintaining diverse generation modes and long-term memory from the teacher. Together, these components enable Wonder to synthesize diverse, minute-scale videos at 16 FPS while preserving coherent geometry, appearance, and dynamics across long rollouts. Beyond image-to-video generation, Wonder naturally supports video-conditioned generation, allowing existing dynamic scenes to be re-shot in real time.

---

## 10. Medical world models in healthcare: foundations, applications, and challenges for trustworthy clinical translation

**Authors:** Zhaoyan Chen, Zhongxiu Cong, Zhuanfeng Jin, ..., Xiaofeng Liu, Cong Wang
**arXiv:** [2607.25242](https://arxiv.org/abs/2607.25242)
**Categories:** Computer Vision and Pattern Recognition (cs.CV)

Medical world models offer a framework for extending medical artificial intelligence beyond static prediction by representing evolving patient states and modelling how they change over time and in response to clinical interventions. This Review defines the conceptual boundaries, technical foundations, application domains, and evidence requirements of the field through a structured narrative synthesis with reproducible evidence this http URL screened 1,455 unique records and assembled a corpus of 98 sources, including 14 studies that met a strict empirical definition of a medical world model. The field is organised around four capabilities: patient state representation, temporal dynamics modelling, intervention-conditioned simulation, and clinician-supervised planning. Evidence spans medical imaging, longitudinal electronic health records, treatment response modelling, physiological and multimodal state modelling, ultrasound and surgical interaction, and population and health-system simulation; clinical digital twins are treated as a cross-cutting integration this http URL studies provide early evidence of technical feasibility for trajectory forecasting and comparison of candidate interventions, but most remain retrospective, task-specific, or preclinical. The evidence base is further limited by incomplete longitudinal intervention data, inconsistent action semantics, limited causal identifiability, long-horizon error accumulation, inadequate uncertainty estimation, and limited external validation. Clinical translation will therefore depend on precise intervention representations, robust causal and mechanistic grounding, calibrated trajectory-level uncertainty, safety-constrained planning, and prospective multicentre validation against clinically meaningful endpoints.

---
