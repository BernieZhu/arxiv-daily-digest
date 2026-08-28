# arXiv Daily Digest — 2026-08-27

**Mode:** direct
**Categories:** cs.AI, cs.LG, cs.RO, cs.CV
**Keywords:** VLA, world model, world action model
**Papers found:** 12

---

## 1. Agentic Game Development as a Verifiable Trajectory Data Engine for Scaling World Models

**Authors:** Pengfei Zhou, Hexin Wang, Zhengfeiyang Zhang, ..., Wangbo Zhao, Yang You
**arXiv:** [2608.25518](https://arxiv.org/abs/2608.25518)
**Categories:** Artificial Intelligence (cs.AI)

A common strategy for scaling world models is to train on more crawled video with more compute. We argue that this strategy is inefficient: scaling world models also requires a recursive data engine that offers grounded reward signals. The success of code agents illustrates why this matters. As code is executable, compilers and runtimes can provide high-quality rewards for Reinforcement Learning (RL) post-training of LLMs. By contrast, spatial generation still relies largely on fuzzy proxies such as CLIP scores. These signals are fuzzy and biased, making them hard to support RL post-training. Compared with these, game development provides a missing reward environment for spatial world models. A scene encoded by a game engine is an executable world specification: the engine can efficiently check collision, physics, navigability and bounded playability, while the developer provides the global verification signal by judging whether the scene should be accepted. Game development also provides real-world long-horizon trajectory data for RL post-training. We therefore propose Reinforcement Learning with Human-Engine Verification (RLHEV), a post-training paradigm that combines dense engine signals with implicit human acceptance feedback from the development process.

---

## 2. Code World Model: Coding Agent as World Brain

**Authors:** Yiwen Chen, Guosheng Lin, Chi Zhang
**arXiv:** [2608.25927](https://arxiv.org/abs/2608.25927)
**Categories:** Computer Vision and Pattern Recognition (cs.CV); Artificial Intelligence (cs.AI); Computation and Language (cs.CL)

World models aim to simulate how complex environments evolve under actions and events, yet existing video-based world models primarily learn dynamics from visual observations, which reveal outcomes rather than the underlying knowledge, rules, and mechanisms governing world evolution. This makes it difficult to maintain persistent consequences and support coherent, open-ended evolution. We introduce Code World Model, a framework that separates world evolution from visual realization by combining the reasoning and coding capabilities of language models with the generative priors of video models. A coding agent serves as the world brain, reasoning about events and their consequences and generating executable code to maintain persistent world state and perform rule-consistent evolution. To connect executable state with visual generation, we introduce a proxy representation that encodes frame-wise spatiotemporal constraints and is compiled into a proxy video, which conditions a video model to render high-fidelity visual observations. We further develop data pipelines for constructing aligned proxy-observation pairs from gameplay and real-world videos. After fine-tuning on paired gameplay data, MiniMax-H3 follows proxy-based spatiotemporal specifications from simple interactive worlds built by the coding agent while preserving rich visual details and dynamics. These results demonstrate the potential of combining code for persistent world evolution with video models for flexible visual realization, providing a new path toward open-ended world models.

---

## 3. ConfAL-WM: Confidence-Guided Active Learning for Action-Conditioned World Models

**Authors:** Xiang Liu, Sen Cui, Changshui Zhang
**arXiv:** [2608.25572](https://arxiv.org/abs/2608.25572)
**Categories:** Robotics (cs.RO); Artificial Intelligence (cs.AI)

Action-conditioned world models have become an important foundation for embodied prediction, planning, and synthetic data generation, but their errors under new task and scene distributions are often concentrated in localized spatiotemporal regions such as robot arms, manipulated objects, contact areas, and occluded objects. This paper presents ConfAL-WM, a confidence-guided active learning framework for post-training embodied world models. Built upon EVAC, we attach a lightweight confidence probe to UNet decoder features and predict dense confidence maps in the latent space. These maps are aggregated into task-, frame-, and patch-level scores, enabling both efficient data selection and localized training enhancement. Our pipeline first retrains the confidence probe and warms up EVAC with a small subset of target-domain data, then performs task-level prescreening to allocate sampling budgets, and finally applies selected-data retraining with optional frame or patch weighted data enhancement. Experiments on RoboTwin2.0 show that confidence-guided selection improves post-training efficiency, while dense frame and patch weighting further enhances prediction quality and embodied trajectory consistency compared with scalar reward, progress, and judge-based scoring baselines. A quick visual overview of this work is available at this https URL.

---

## 4. Rollout-Decoded Reconstruction for Long-Horizon Prediction in Latent World Models

**Authors:** Rishi Shah, Rishav Shrestha
**arXiv:** [2608.25017](https://arxiv.org/abs/2608.25017)
**Categories:** Machine Learning (cs.LG)

A latent world model trains its decoder on latents anchored to observations, then deploys it on the model's own free-running rollout, hundreds of steps past the last observation. Rollout-Decoded Reconstruction (RDR) closes this gap with a single loss term that free-runs the model during training exactly as evaluation will, decodes every rollout latent, and penalizes reconstruction error against ground truth. The term adds no parameters, costs training-time compute only, and reduces to the standard objective at weight zero, so every comparison in this paper is a one-flag A/B. On the chaotic Kuramoto-Sivashinsky equation, RDR raises valid prediction time (the time to first crossing of normalized error 0.5) from $3.87 \pm 0.23$ to $6.97 \pm 0.42$ time units at an identical 193,568 parameters, a $1.80\times$ improvement confirmed on seeds never used in selection and holding in 10 of 10 preregistered configurations at ratios of 1.71-2.50$\times$. The results come from a single system; a sweep in which the advantage grows with latent width is descriptive, and control experiments on two classic tasks are preliminary.

---

## 5. Zero-WAM: In-Context World-Action Modeling from Human Videos for Open-Ended Task Generalization

**Authors:** Jiaming Zhou, Qihang Zhang, Gangwei Xu, ..., Junwei Liang, Yinghao Xu
**arXiv:** [2608.26103](https://arxiv.org/abs/2608.26103)
**Categories:** Robotics (cs.RO); Computer Vision and Pattern Recognition (cs.CV)

Zero-shot cross-task generalization, where a policy must execute manipulation tasks never seen during training, remains a central challenge in robot learning. In large language models, a novel task can be performed simply by specifying it in the context, without any parameter update. This form of in-context learning (ICL) turns generalization into a problem of task specification. To achieve cross-task generalization, we bring this paradigm to robotic manipulation, and argue that the natural task specification for manipulation is a human video: unlike language, it provides rich visual cues about the intended task evolution. We present Zero-WAM, a causal video-action model that executes unseen tasks by following in-context human video guidance. To address the scarcity of task-rich paired human-robot data, we propose an automatic pipeline that converts task-sampled robot trajectories into semantically matched human videos, yielding HumanGen, a dataset of 74.2K human-robot ICL pairs across 8.6K tasks. For model training, we further introduce an in-context future chunk prediction (IFP) objective that suppresses shortcuts learned from seen tasks and forces the policy to draw task information from the video prompt. On seven unseen tasks in RoboTwin 2.0 simulation, Zero-WAM achieves a 47.0% average success rate, an absolute improvement of 29.5 percentage points over the strongest video-action baseline. In real-world evaluations, it follows human video guidance to generalize to unseen task configurations involving multi-object scenes, long-horizon manipulation, and fine-grained insertion.

---

## 6. MA-VLA: Multi-Arm Vision-Language-Action Model for Collaboration and Compositional Generalization

**Authors:** Zaibin Zhang, Junlan Xiao, Zhongbo Zhang, ..., Huchuan Lu, Lijun Wang
**arXiv:** [2608.25864](https://arxiv.org/abs/2608.25864)
**Categories:** Robotics (cs.RO)

Multi-arm collaboration is becoming a core capability in embodied manipulation. Recent vision-language-action (VLA) models integrate perception, language, and control, but most represent language as a single global instruction and do not provide an explicit mechanism for assigning and composing arm-specific behaviors. This design limits transfer to collaboration patterns that differ from those observed during training. We present MA-VLA, a unified framework for multi-arm collaboration via atomic action assignment. MA-VLA decomposes cooperative behavior into mid-level atomic prompts and allocates them to individual arms, enabling explicit subgoal specification and compositional reuse across tasks. To reduce reliance on fixed execution roles, we introduce Arm Shuffle, a training-time permutation of the observation, state, and assigned atomic prompts for each arm. This permutation enforces role-agnostic instruction following and supports recomposition into unseen coordination patterns, which we term multi-arm compositional generalization. We also construct a benchmark in which test-time collaboration patterns are absent in training set. Across simulation and real-world evaluations, prior state-of-the-art VLAs largely fail under these unseen collaborations, while MA-VLA consistently succeeds. These results indicate that structured, per-arm atomic action assignment offers a practical route to scalable generalization in multi-arm embodied systems. Code, models, and data are available at this https URL

---

## 7. GaussianDream++: Efficient 3D Gaussian World Modeling for Robotic Manipulation

**Authors:** Yuqing Jiang, Zijian Zhang, Weitao Zhou, ..., Ping Luo, Haibao Yu
**arXiv:** [2608.25659](https://arxiv.org/abs/2608.25659)
**Categories:** Robotics (cs.RO)

Vision-Language-Action (VLA) policies have advanced language-conditioned robotic manipulation, yet action-imitation objectives provide only weak supervision for metric 3D structure and short-horizon physical evolution. Geometry-enhanced policies mainly improve current-scene grounding, whereas predictive policies often model future dynamics in RGB or latent spaces and may incur substantial deployment cost. GaussianDream demonstrates that training-time current Gaussian reconstruction and future Gaussian prediction provide effective 3D supervision, but its dense VGGT/TGE-based prefix jointly carries state, dynamics, and action-conditioning information. We present \textbf{\methodname}, a compact, policy-native extension that inserts \textbf{World State Tokens} and \textbf{World Prediction Tokens} directly into the VLA backbone. A training-only \textbf{World Representation Head} decodes these tokens into a Current World and coupled Future Prediction over shared Gaussian primitives, while static--dynamic factorization preserves persistent structure and focuses residual motion on interaction-relevant regions. At inference, the head, renderer, auxiliary objectives, and VGGT/TGE pathway are removed, leaving only 20 world tokens without online Gaussian decoding or rollout. \method achieves \textbf{98.6\%} on LIBERO and \textbf{87.8\%} on LIBERO-Plus, with clear gains under Camera and Layout shifts. Real-robot experiments further improve average success from 29.2\% to 52.5\% over reproduced $\pi_{0.5}$ while maintaining efficient closed-loop control.

---

## 8. RA-VLA: Retrieval-Augmented VLA for Test-Time Adaptation

**Authors:** Sanghwan Jang, Minjin Jeon, Minsoo Kim, ..., Dongha Kim, Hwanjo Yu
**arXiv:** [2608.25585](https://arxiv.org/abs/2608.25585)
**Categories:** Robotics (cs.RO)

Vision-Language-Action (VLA) models provide a versatile foundation for general robotic manipulation, yet they exhibit significant brittleness when confronted with novel task distributions. While In-Context Imitation Learning (ICIL) offers a training-free alternative, existing frameworks suffer from an adaptation bottleneck that hinders the effective translation of expert context to executable actions. This failure originates from superficial retrieval mechanisms and an inherent behavioral inertia that anchors the policy to its pre-trained priors. To address these limitations, we present RA-VLA, a retrieval-augmented VLA framework that integrates behavior-aligned context retrieval with a grounded execution pipeline. By enforcing faithful adherence to functional cues within a scalable architecture, RA-VLA facilitates seamless task adaptation while preserving inference efficiency. Our empirical evaluations across the LIBERO benchmark and a real-world UR5e environment demonstrate that RA-VLA achieves superior success rates and computational efficiency, establishing a robust framework for training-free robotic adaptation.

---

## 9. GaussVLA: Geometry-Aware Spatial Reasoning for Vision-Language-Action Model

**Authors:** Md Selim Sarowar, Md Tanvir Islam, Sungho Kim, Sangtae Ahn
**arXiv:** [2608.24959](https://arxiv.org/abs/2608.24959)
**Categories:** Robotics (cs.RO); Computer Vision and Pattern Recognition (cs.CV)

Vision-Language-Action (VLA) models encode visual observations as flat 2D patch tokens that carry no intrinsic geometric structure, and augmenting them with dense monocular depth injects per-pixel scalar values that encode neither surface orientation nor geometric confidence. This leaves the policy with limited structured spatial reasoning for action prediction. We propose GaussVLA, a Mamba-based VLA that incorporates two custom modules: Gaussian Spatial Tokenizer (GST) to lift frozen semantic and depth features into compact 3D Gaussian tokens, pools geometrically salient regions with learned queries, and \emph{Depth-Aware Chain-of-Thought (DA-CoT)} that performs structured, non-autoregressive geometric reasoning under language and flow-time conditioning. Across both simulation and real-world evaluations, GaussVLA demonstrates strong spatial-manipulation performance while remaining parameter-efficient. On LIBERO, it achieves 93.5% average success and 100.0% success on the Spatial suite with only 200M parameters, improving over SpatialVLA by 19.7% relative average success while remaining significantly more parameter-efficient.

---

## 10. StreamPI: Streaming Multimodal Temporal Modeling for Vision-Language-Action Models

**Authors:** Zhe Liu, Jinghua Hou, Yuxiang Lu, ..., Zhi Hou, Hengshuang Zhao
**arXiv:** [2608.26067](https://arxiv.org/abs/2608.26067)
**Categories:** Computer Vision and Pattern Recognition (cs.CV)

Vision-Language-Action (VLA) models have demonstrated effectiveness in robot manipulation, yet state-of-the-art models such as pi0.5 operate under a single-frame paradigm, limiting their ability to retain past observations and develop precise spatial perception. In this paper, we propose StreamPI, a streaming multimodal temporal modeling framework that equips single-frame VLA with temporal reasoning capability without introducing any additional parameters. One core design is instruction-anchored temporal modeling. It treats each (visual observation, language instruction) pair as an atomic temporal unit: bidirectional attention within each pair enables cross-modal fusion, while causal attention across pairs preserves autoregressive streaming inference. This ensures the language instruction serves as a persistent semantic anchor throughout task execution. To bridge the gap between synchronous training and asynchronous real-robot deployment, we introduce a andom-interval streaming training strategy: a proper inter-frame interval (e.g., every 3 frames) enables faster and smoother action execution. Beyond this, randomizing the interval further improves robustness to frame-timing perturbations, supporting asynchronous deployment in practice. Furthermore, by leveraging the length extrapolation capability of the LLM backbone, StreamPI seamlessly inherits pretrained single-frame weights and supports flexible single-frame and multi-frame inference. Experiments on real-robot tasks spanning memory-dependent and precise perception scenarios, as well as the simulation benchmark LIBERO, demonstrate that StreamPI outperforms pi0.5 across diverse tasks.

---

## 11. 4DGS-WAM: Bridging Past and Future with an Object-Centric World Action Model based on 4D Gaussian Splatting

**Authors:** Yueen Ma, Zenglin Xu, Irwin King
**arXiv:** [2608.25956](https://arxiv.org/abs/2608.25956)
**Categories:** Computer Vision and Pattern Recognition (cs.CV)

Current world action models (WAMs) typically operate on 2D visual data. These models can achieve exceptional visual quality, but they lack explicit spatial structure for individual objects and repeatedly process redundant background content. Although point clouds can represent the world in 3D space, they can be difficult to align and accumulate across viewpoints. In this paper, we leverage an explicit 4D Gaussian Splatting (4DGS) representation that separately models dynamic objects and the static background of a scene. For dynamic objects, we use a policy model to predict future actor actions and a world model to predict transformations of their observed Gaussian splats. The static background need not be regenerated for future states, as much of it has already been observed in past frames. This forms an object-centric world action model, which we name 4DGS-WAM. It lifts 2D observations into a persistent 4D representation so that previously observed static content can be reused during future prediction. Future-state extrapolation can then focus on modeling the evolution of dynamic objects. Experiments on KITTI-MOT evaluate short-horizon prediction and past reconstruction.

---

## 12. V-Link: Recovering Lost Visual Representations in Action DiT for Vision-Language-Action Models

**Authors:** Yehao Lu, Jiarui Yang, Yuning Su, ..., Enyu Li, Xi Li
**arXiv:** [2608.25308](https://arxiv.org/abs/2608.25308)
**Categories:** Computer Vision and Pattern Recognition (cs.CV)

Vision-language-action (VLA) models provide a scalable path toward generalist robotic manipulation by integrating visual perception, language understanding, and continuous action control. However, we reveal a critical limitation of VLA architectures: the action expert has limited access to the 3D geometric and 2D semantic information available in VLM features. This accessibility gap weakens perceptual grounding and limits performance on fine-grained robotic manipulation. To address this issue, we propose V-Link, which explicitly recovers visual representations during the vision-language (VL) to action (A) feature transfer. Specifically, V-Link learns complementary Spatial and Semantic Query representations within the VLM and injects them into Action DiT through asymmetric pathways. Semantic Queries complement the original VLM image tokens, whereas Spatial Queries provide dedicated geometric conditioning for spatially grounded action generation. Across LIBERO, LIBERO-Plus, and RoboTwin 2.0, our V-Link improves the average success rate over base model GR00T N1.6 by +1.9%, +31.2%, and +18.8%, respectively. On the AGIBOT A3 Ultra, V-Link further achieves gains of +20% and +24% on two real-world humanoid tasks.

---
