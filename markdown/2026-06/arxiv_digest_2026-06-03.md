# arXiv Daily Digest — 2026-06-03

**Mode:** direct
**Categories:** cs.AI, cs.LG, cs.RO, cs.CV
**Keywords:** VLA, world model, world action model
**Papers found:** 18

---

## 1. A Close Look At World Model Recovery In Supervised Fine-Tuned LLM Planners

**Authors:** Patrick Emami, Nan Qiang, Peter Graf
**arXiv:** [2606.03685](https://arxiv.org/abs/2606.03685)
**Categories:** Machine Learning (cs.LG); Artificial Intelligence (cs.AI)

Supervised fine-tuning (SFT) improves end-to-end classical planning in large language models (LLMs), but do these models also learn to represent and reason about the planning problems they are solving? Due to the relative complexity of classical planning problems and the challenge that end-to-end plan generation poses for LLMs, it has been difficult to explore this question. In our work, we devise and perform a series of interpretability experiments that holistically interrogate world model recovery by examining both internal representations and generative capabilities of fine-tuned LLMs. We find that: a) Supervised fine-tuning on valid action sequences enables LLMs to linearly encode action validity and some state predicates. b) Models that struggle to use output probabilities for classifying action validity may still learn internal representations that separate valid from invalid actions. c) Broader state space coverage during fine-tuning, such as from random walk data, yields more accurate recovery of the underlying world model. In summary, this work contributes a recipe for applying interpretability techniques to planning LLMs and generates insights that shed light on open questions about how knowledge is represented in LLMs.

---

## 2. PHASER: Phase-Aware and Semantic Experience Replay for Vision-Language-Action Models

**Authors:** Ziyang Chen, Shaoguang Wang, Weiyu Guo, ..., Yiren Zhao, Yandong Guo
**arXiv:** [2606.03598](https://arxiv.org/abs/2606.03598)
**Categories:** Robotics (cs.RO); Artificial Intelligence (cs.AI); Computer Vision and Pattern Recognition (cs.CV)

Vision-Language-Action (VLA) models have achieved remarkable success in language-conditioned robotic manipulation. However, deploying these models in open-ended environments requires continuously acquiring novel skills, a process that inevitably triggers severe catastrophic forgetting of previously learned behaviors. While experience replay (ER) serves as a standard mitigating strategy, naive uniform sampling fundamentally misaligns with the temporal characteristics of manipulation trajectories. It systematically under-samples brief but causally critical sub-skills, leading to phase starvation, and completely overlooks the varying degrees of forgetting across historical tasks. To overcome these limitations, we introduce PHASER, an architecture-agnostic continual learning framework. PHASER employs a phase-centric capacity allocation to guarantee equal memory support for all sub-skills, coupled with a multi-modal interference routing strategy that dynamically prioritizes historical phases at high risk of forgetting. Furthermore, to enable fully autonomous lifelong adaptation, we integrate Auto-PC, a lightweight pipeline combining unsupervised action-signal change-point detection with VLM-based semantic verification to extract temporal boundaries without intensive manual supervision. Evaluated across three VLA backbones on LIBERO continual learning suites, PHASER yields substantial empirical improvements, increasing Average Success Rate (ASR) by up to 31% over matched-budget ER and achieving an 87.8% final ASR on the LIBERO-Goal CL setting.

---

## 3. AirDreamer: Generalist Drone Navigation with World Models

**Authors:** Zian Liu, Andong Yang, Chunkai Yang, ..., Chao Gao, Guyue Zhou
**arXiv:** [2606.03252](https://arxiv.org/abs/2606.03252)
**Categories:** Robotics (cs.RO); Artificial Intelligence (cs.AI)

Navigating a drone in unseen and cluttered environments requires reliable generalization to unseen scene layouts and understanding of environmental structure relative to the robot's capabilities. Previous methods, which assume the same environment configuration, often rely heavily on human-designed perception pipelines and predefined rules to guide the robot toward the target. This process is environment-dependent and generalizes poorly across environments. Inspired by animal navigation behavior, we design a navigation framework that navigates with a reinforcement-learning-based policy on top of a world-model-based environment understanding to overcome these issues. In addition, a sparse reward function without hand-crafted shaping terms is designed to avoid local minima traps and encourage yaw control behaviors. In simulation and on real drones, our method exhibits emergent capabilities for navigating complex, unseen environments and escaping local optima where other methods fail. In challenging maps, it achieves a 5.3% higher navigation success rate than best baseline. Furthermore, the proposed framework achieves effective sim-to-real transfer without any tuning during deployment. The code will be publicly available.

---

## 4. NVIDIA OmniDreams: Real-Time Generative World Model for Closed-Loop Autonomous Vehicle Simulation

**Authors:** NVIDIA, Aarti Basant, Amlan Kar, ..., Zan Gojcic, Zian Wang
**arXiv:** [2606.03159](https://arxiv.org/abs/2606.03159)
**Categories:** Computer Vision and Pattern Recognition (cs.CV); Artificial Intelligence (cs.AI); Robotics (cs.RO)

As autonomous vehicle capabilities advance, the safe evaluation of driving policies in long-tail scenarios remains a critical bottleneck. In closed-loop simulation, the driving policy model actively interacts with the environment, where its actions dynamically update the simulator state and directly influence the next set of generated sensor observations. While recent reconstruction-based neural simulators offer photorealism, they are fundamentally constrained by their initial captured data and struggle to generalize to highly dynamic or novel scenes. To overcome these limitations, we introduce OmniDreams, a foundation generative world model mid- and post-trained from the Cosmos diffusion model to autoregressively generate action-conditioned videos in real time. By leveraging the rich visual priors of Cosmos and mid- and post-training on 21k hours of driving scenarios, OmniDreams synthesizes complex, unobserved phenomena that are hard for traditional simulators to capture, such as extreme weather and unpredictable dynamic agent behaviors. Crucially, it autoregressively conditions its photorealistic sensor generation on past frames, the current simulator state, and immediate driving actions. Deployed in a closed-loop system with the Alpamayo 1 policy model and AlpaSim orchestrator, OmniDreams acts as a highly responsive, reactive environment, providing a scalable and comprehensive solution for training and evaluating next-generation autonomous driving policies. We additionally show preliminary results indicating that a world-action model (WAM) post-trained from OmniDreams achieves strong performance on the Physical AI Autonomous Vehicles NuRec dataset, surpassing the VLA-based Alpamayo 1.5 research policy model while using only 1/5 the total parameters. These results highlight the potential for a real-time world model like OmniDreams to also serve as a backbone for policy architectures.

---

## 5. Cosmos 3: Omnimodal World Models for Physical AI

**Authors:** Aditi, Niket Agarwal, Arslan Ali, ..., Artur Zolkowski, et al. (191 additional authors not shown)
**arXiv:** [2606.02800](https://arxiv.org/abs/2606.02800)
**Categories:** Computer Vision and Pattern Recognition (cs.CV); Artificial Intelligence (cs.AI); Machine Learning (cs.LG); Multimedia (cs.MM); Robotics (cs.RO)

We introduce Cosmos 3, a family of omnimodal world models designed to jointly process and generate language, image, video, audio, and action sequences within a unified mixture-of-transformers architecture. By supporting highly flexible input-output configurations, Cosmos 3 seamlessly unifies critical modalities for Physical AI -- effectively subsuming vision-language models, video generators, world simulators, and world-action models into a single framework. Our evaluation demonstrates that Cosmos 3 establishes a new state-of-the-art across a diverse suite of understanding and generation tasks, demonstrating omnimodal world models as scalable, general-purpose backbones for embodied agents. Our post-trained Cosmos 3 models were ranked as the best open-source Text-to-Image and Image-to-Video models by Artificial Analysis, and the best policy model by RoboArena at the time the technical report was written. To accelerate open research and deployment in Physical AI, we make our code, model checkpoints, curated synthetic datasets, and evaluation benchmark available under the Linux Foundation's OpenMDW-1.1 this https URL License at this https URL}{this http URL and this https URL . The project website is available at this https URL .

---

## 6. MetaWorld: Scaling Multi-Agent Video World Model from Single-view Video Data

**Authors:** Teng Hu, Mingchun Lu, Yating Wang, ..., Lizhuang Ma, Dacheng Tao
**arXiv:** [2606.02753](https://arxiv.org/abs/2606.02753)
**Categories:** Computer Vision and Pattern Recognition (cs.CV); Artificial Intelligence (cs.AI)

Video world models are a foundational generative technology for embodied AI and the Metaverse, yet existing approaches are inherently limited to a single agent observing from a single perspective. Extending these models to multi-agent settings introduces two critical challenges: data scarcity (coordinated multi-view recordings are prohibitively expensive to collect for general open-domain scenarios) and world state alignment (independently generated video streams cannot ensure that shared physical environments and events evolve consistently across views). To address these challenges, we propose MetaWorld, a novel framework that scales multi-agent video world models to open-domain environments directly from single-view videos. First, we introduce Monocular World-State Unrolling (MWSU) to explicitly decompose monocular footage into the camera operator's ego-motion and the visible subject's spatial trajectory. This camera-trajectory decomposition naturally extracts synchronized multi-agent motion data within a shared 3D space, completely bypassing the need for multi-camera setups. Second, for precise visual control, we develop the Subject-Aware World Generator to enable appearance-driven simulation conditioned on per-agent identity images. Finally, to ensure both views are grounded in the identical physical reality, we propose World-State Alignment, a per-frame inter-branch cross-attention mechanism inserted at every transformer layer of the video DiT. By jointly synchronizing the denoising process, WSA enforces both static geometric consistency and dynamic motion consistency, encouraging that the shared 3D environment and physical events remain well-aligned across both egocentric views. Extensive experiments demonstrate that MetaWorld achieves superior cross-view consistency and identity fidelity, establishing a highly scalable, physics-driven paradigm for multi-agent video world modeling.

---

## 7. See Less, Specify More: Visual Evidence Budgets for Generalizable VLAs

**Authors:** Yueh-Hua Wu, Tatsuya Matsushima, Kei Ota
**arXiv:** [2606.02735](https://arxiv.org/abs/2606.02735)
**Categories:** Robotics (cs.RO); Artificial Intelligence (cs.AI); Machine Learning (cs.LG)

Generalization remains a central bottleneck for vision-language-action (VLA) models: under distractors, appearance shifts, and semantically similar tasks, the policy must often infer local execution details from coarse instructions while also deciding which parts of the image matter for control. We present S2 (See Less, Specify More), a framework for improving VLA generalization by training the executor under a cleaner interface.
Specify More preserves the original instruction as a stable high-level goal while relabeling each trajectory into refined trajectory- and subtask-level language that disambiguates the current execution mode. Unlike native attention, See Less imposes an explicit visual evidence budget, training the executor to act from task-sufficient evidence rather than unconstrained visual context, without any region or mask annotation.
This interface lets the executor follow detailed guidance without relying on distracting visual patches or resolving avoidable ambiguity on its own, and it remains compatible with off-the-shelf VLM planners through in-context learning. Across our main evaluation settings, S2 improves overall generalization metrics by changing the executor's learning problem: coarse instructions induce avoidable supervision aliasing, goal-preserving local guidance outperforms instruction replacement in our main ablations, and explicit evidence budgeting reduces dependence on broad visual context beyond efficiency considerations.
Across eight real-robot tasks on TX-G2 (an AgiBot G2-compatible variant) and HSR, S2 raises mean subtask success from 54.2% to 79.0% over pi0.5. Together, these results suggest that VLA generalization improves when the executor is trained to act from informative local guidance and task-sufficient visual evidence, rather than recovering both from weak supervision.

---

## 8. TRAP: Hijacking VLA CoT-Reasoning via Adversarial Patches

**Authors:** Zhengxian Huang, Wenjun Zhu, Haoxuan Qiu, Xiaoyu Ji, Wenyuan Xu
**arXiv:** [2603.23117](https://arxiv.org/abs/2603.23117)
**Categories:** Cryptography and Security (cs.CR); Artificial Intelligence (cs.AI); Robotics (cs.RO)

By integrating Chain-of-Thought (CoT) reasoning, Vision-Language-Action (VLA) models have demonstrated strong capabilities in robotic manipulation, particularly by improving generalization and interpretability. However, the security of CoT-based reasoning mechanisms remains largely unexplored. In this paper, we show that CoT reasoning introduces a novel attack vector for targeted behavior hijacking--for example, causing a robot to mistakenly deliver a knife to a person instead of an apple--without modifying the user's instruction. We first provide empirical evidence that CoT strongly governs action generation, even when it is semantically misaligned with the input instructions. Building on this observation, we propose TRAP, the first targeted behavior-hijacking adversarial attack against CoT-reasoning VLA models. By targeting the reasoning-to-action pathway, TRAP uses an adversarial patch (e.g., a tablecloth placed on the table) to steer intermediate CoT reasoning and downstream actions toward adversary-defined behaviors. Extensive evaluations on three representative reasoning VLAs, spanning distinct CoT reasoning mechanisms, demonstrate the effectiveness of TRAP. Notably, we implemented the patch by printing it on paper in a real-world setting. Our findings highlight the urgent need to secure CoT reasoning in VLA systems. The project page is available at this https URL.

---

## 9. A 3D Isovist World Model -- Revealing a City's Unseen Geometry and Its Emergent Cross-City Signature

**Authors:** Xuhui Lin, Stephen Law, Nanjiang Chen, Kunyao Li, Tao Yang
**arXiv:** [2606.03609](https://arxiv.org/abs/2606.03609)
**Categories:** Robotics (cs.RO); Machine Learning (cs.LG)

Embodied agents that navigate cities rely on world models that predict how their surroundings will change as they move. But for navigation, what matters is not what the buildings look like; it is where the agent can go. Most world models nonetheless predict appearance, learning how a scene looks rather than the space an agent can move through. Those that do target geometry, such as bird's-eye-view occupancy grids, flatten the three-dimensional environment onto a ground plane, discarding the above-ground and multi-level structure that shapes real navigation. What is missing is a predictive target that captures the navigable geometry an agent actually traverses, without photometric entanglement and without collapsing the third dimension. Our key idea is to model the open volume between buildings, the negative space, encoded as a 3D isovist: a spherical visibility-depth map recording the distance to the nearest surface in every direction. We introduce an embodied world model that predicts the next isovist from a short history of past isovists and a movement action. The prediction is formulated as a depth residual so the decoder inherits sharp building edges, trained with self-rollout scheduled sampling to keep corrupted context on the geometry manifold, and equipped with a persistent latent bird's-eye-view spatial map for cross-path consistency. Our central finding is emergent and unexpected: a single city-blind model trained on Manhattan and Paris develops a cross-city spatial signature, with city identity linearly decodable from its temporal latents far above single-frame baselines, so the signature lives in the learned dynamics rather than in appearance. The representation is lightweight, interpretable, and reproducible, offering a geometric substrate for spatial reasoning in embodied AI, robotics, and urban analysis, released with an open dataset and pipeline.

---

## 10. Partially Observable Adversarial Patch Attacks on Vision-Language-Action Models in Robotics

**Authors:** Xiaofei Wang, Mingliang Han, Tianyu Hao, ..., Yun-Bo Zhao, Keke Tang
**arXiv:** [2606.03556](https://arxiv.org/abs/2606.03556)
**Categories:** Robotics (cs.RO)

Vision-language-action (VLA) models are gaining attention in robotics, yet their robustness to adversarial attacks remains largely unexplored. Existing work shows that adversarial patches can mislead VLA-based robots but assumes full access to the entire execution trajectory, an unrealistic requirement in practice. We address this limitation by formulating a partially observable threat model, where the adversary can exploit only a short prefix of the trajectory to generate a fixed patch applied to all subsequent frames. Under this setting, we propose a two-phase framework. First, we localize the patch using the model's attention maps to identify visually critical regions that correspond to the full instruction. Then, we optimize the patch to disrupt the semantic grounding of target objects and increase the curvature of action trajectories, thereby compounding failures in both perception and control. Extensive experiments in simulation and real-world robotic environments show that our method sustains adversarial effects under partial observability, inducing long-horizon disruptions and significantly reducing task success rates.

---

## 11. GeoAlign: Beyond Semantics with State-Guided Spatial Alignment in VLA Models

**Authors:** Yizhi Chen, Zhanxiang Cao, Xinyi Peng, ..., Cewu Lu, Yue Gao
**arXiv:** [2606.03240](https://arxiv.org/abs/2606.03240)
**Categories:** Robotics (cs.RO)

Current Vision--Language--Action (VLA) models often optimize for semantic grounding, whereas executable manipulation requires geometry-aware spatial alignment and dynamic affordance selection. We introduce GeoAlign, a state-guided spatial alignment architecture for VLA policy learning. GeoAlign post-trains an RGB geometry branch with robot-domain RGB-D supervision, yielding RGB-derived Geometry-Enhanced Post-Trained (GEP) features for policy rollout. The robot's proprioceptive state queries the GEP feature grid, producing compact, phase-dependent geometry tokens for action prediction. GeoAlign achieves 99.0% on LIBERO, 85.3% across three SimplerEnv-Fractal tasks, and 78.8% on eight geometry-critical real-world ALOHA tasks, with ablations confirming the value of geometry post-training and proprioceptive-state-guided querying.

---

## 12. GeoSem-WAM: Geometry- and Semantic-Aware World Action Models

**Authors:** Fulong Ma, Daojie Peng, Wenjun Yue, ..., Qiang Zhang, Jun Ma
**arXiv:** [2606.03188](https://arxiv.org/abs/2606.03188)
**Categories:** Robotics (cs.RO)

Recent World Action Models (WAMs) have demonstrated impressive capabilities in embodied decision-making. However, whether their effectiveness stems from explicit future imagination during inference or representation learning induced by predictive training remains an open question. Emerging evidence suggests the primary advantage lies in learning robust latent representations rather than generating future observations at test time. Nevertheless, existing WAMs mainly rely on RGB-based future prediction, which provides limited structural and spatial understanding of complex environments. To address this, we propose a structured world modeling framework that enhances latent representations through geometric and semantic supervision. Alongside future RGB prediction, our model introduces two auxiliary prediction branches for future geometry and semantic representations, enabling it to jointly capture scene dynamics, spatial geometry, and semantic context within a unified latent space. Crucially, our approach preserves efficient inference by avoiding explicit future rollout or video generation at test time. Extensive experiments show that incorporating structured world supervision consistently improves action prediction accuracy, scene understanding, and robustness under challenging embodied scenarios, highlighting its potential for advancing scalable and efficient WAMs.

---

## 13. TTT-VLA: Test-Time Latent Prompt Optimization for Vision-Language-Action Models

**Authors:** Wenbo Zhang, Jianxiong Li, Shuai Yang, ..., Lingqiao Liu, Xiao Ma
**arXiv:** [2606.03127](https://arxiv.org/abs/2606.03127)
**Categories:** Robotics (cs.RO)

Vision-Language-Action (VLA) models trained on large-scale data have made remarkable progress, but they remain vulnerable to distribution shifts at deployment time. Recent VLA models suggest that prompts can serve as an efficient interface for steering policy behavior, but existing prompt-based steering typically relies on external guidance. This raises a natural question: can test-time training (TTT) for VLA be achieved by optimizing a prompt, so that the steering interface itself can be learned and adapted from interaction? We address this question with TTT-VLA, a test-time training framework based on Latent Prompt Optimization (LPO). During training, the latent prompt is learned with an additional proxy task, providing an extra learned conditioning signal for policy learning. At test time, TTT is performed by collecting interaction data from the current environment and optimizing only the latent prompt on those data using the proxy task's self-supervised signal, without modifying the policy itself. Experiments on SimplerEnv demonstrate that the proposed method consistently improves task success rates in both single- and multi-embodiment settings. Further analysis shows that the gains arise primarily from correcting a small number of critical decisions rather than globally altering policy behavior. These results suggest that LPO provides an effective and practical pathway for deployment-time improvement of foundation manipulation policies.

---

## 14. World Models Meet Language Models: On the Complementarity of Concrete and Abstract Reasoning

**Authors:** Yucheng Zhou, Wei Tao, Yiwen Guo, Jianbing Shen
**arXiv:** [2606.03603](https://arxiv.org/abs/2606.03603)
**Categories:** Computer Vision and Pattern Recognition (cs.CV); Computation and Language (cs.CL)

World models and multimodal large language models (MLLMs) provide complementary capabilities for predicting future outcomes from static visual observations. World models can generate concrete visual rollouts of possible futures, while MLLMs can reason abstractly over questions, goals, and rules. However, generated rollouts are stochastic and may be visually plausible but task-incorrect, making it necessary to determine when visual simulation is useful, whether a rollout is credible, and how it should influence the final answer. We formulate this problem as controlled concrete reasoning, where a model learns to invoke, verify, and integrate visual future simulation alongside abstract reasoning. To study this setting, we construct two human-verified benchmarks, VRQABench for controllable spatial lookahead and OpenWorldQA for open-domain physical prediction, and propose Privileged-Future On-Policy Self-Distillation (PF-OPSD). During training, PF-OPSD uses ground-truth future videos and answers only as teacher-side privileged context to evaluate on-policy concrete-reasoning trajectories, while the deployable student never observes true futures at test time. Experimental results show that PF-OPSD outperforms baseline by 10.6% and 10.9% on VRQABench and OpenWorldQA, respectively, while increasing robustness to noisy or conflicting rollouts. Our code and dataset are available at this https URL.

---

## 15. Grasp-Then-Plan with Failure Attribution: A Closed Two-Stage Framework for Precise and Generalizable Robotic Manipulation

**Authors:** Jiahao Xu, Peiyuan Wang, Hanzhuo Zhang, ..., Chenchen Fu, Wanyuan Wang
**arXiv:** [2606.03385](https://arxiv.org/abs/2606.03385)
**Categories:** Robotics (cs.RO); Artificial Intelligence (cs.AI)

In robotic manipulation, the tight coupling between grasping and motion planning often obscures the true source of failure, leading to inefficient trial-and-error. To enable efficient long-horizon manipulation, we propose GTP-FA (Grasp-Then-Plan with Failure Attribution), a task-oriented two-stage grasp-then-plan framework that generates grasp candidates and performs downstream motion planning conditioned on the selected grasp. Given a failed manipulation trajectory, we learn a failure attribution model that generalizes to unseen grasps and produces a stable distribution over failure modes for diagnosis-guided optimization. Based on these attribution results, we then optimize both modules in a diagnosis-driven manner: on the grasping side, we inject task-level priors and risk penalties into grasp candidate scoring and optimization to suppress unstable or task-incompatible grasps; on the planning side, we target high-risk initial states through data collection and fine-tuning to address genuine planning bottlenecks. We evaluate the proposed framework in both simulation and real-robot experiments, and show that GTP-FA improves the corresponding base learners across RL, IL, diffusion-policy, and VLA-based settings, achieving substantially higher overall task success rates.

---

## 16. SeeTraceAct: Visibility-Aware Latent Planning from Cross-Embodiment Demonstration Videos

**Authors:** Jaehyeon Son, Junhyun Kim, Kyle Kam, ..., Dieter Fox, Zsolt Kira
**arXiv:** [2606.02745](https://arxiv.org/abs/2606.02745)
**Categories:** Robotics (cs.RO); Machine Learning (cs.LG)

Vision-language-action models (VLAs) are promising general-purpose robot policies, but adapting them to new tasks typically requires costly task-specific teleoperation data. As an alternative, we study one-shot demo-conditioned VLAs, where a robot policy is conditioned on a single demonstration video of an unseen task. We find that existing end-to-end approaches often struggle when successful execution requires precisely localizing small target regions. To address this limitation, we propose SeeTraceAct, a demo-conditioned VLA framework that encourages precise spatial grounding through visibility-aware prediction of future end-effector traces. To enable reproducible evaluation with cross-embodiment demonstrations, we introduce and release RoboCasa-DC, a demo-conditioned extension of RoboCasa with episode-paired humanoid videos. Experiments on RoboCasa-DC and a real-world benchmark, where a Franka Panda arm is conditioned on human demonstrations, show that SeeTraceAct outperforms baselines, achieving the best success rate across all four RoboCasa-DC settings and improving real-world average success by 12.5 percentage points.

---

## 17. Revisiting Embodied Chain-of-Thought for Generalizable Robot Manipulation

**Authors:** Nan Sun, Yuan Zhang, Yongkun Yang, ..., Xinghang Li, Huaping Liu
**arXiv:** [2606.03784](https://arxiv.org/abs/2606.03784)
**Categories:** Robotics (cs.RO)

Embodied chain-of-thought (CoT) aims to bridge linguistic reasoning and robotic control, but its effective form and integration strategy remain underexplored. In this paper, we revisit embodied CoT for vision-language-action (VLA) models at large scale. We construct the largest embodied CoT corpus to date, comprising 978,743 trajectories, 226.3M samples, and 2592.5 hours of robot data. Through extensive experiments, we find that effective embodied CoT should ground high-level semantic understanding into concrete action guidance, such as end-effector movement descriptions and image-space trajectories, while high-level reasoning alone brings only marginal gains. We further show that explicit CoT does not scale reliably when used as an autoregressive action prefix, as it suffers from compounding inference errors and unstable reasoning-action coupling. To address these limitations, we propose ERVLA, a VLA model that uses embodied CoT as representation-shaping supervision rather than mandatory test-time reasoning. ERVLA is trained with a reasoning-dropout strategy, enabling the model to absorb rich reasoning traces during training while predicting actions directly without CoT decoding during inference. This design improves scalability with increasing pre-training data and avoids autoregressive instability. ERVLA achieves state-of-the-art performance on LIBERO-Plus with an 86.9% success rate and reaches 53.2% success rate on VLABench, demonstrating strong out-of-distribution generalization. In real-robot experiments, ERVLA further outperforms competitive state-of-the-art baselines, especially on tasks requiring semantic disambiguation and long-horizon execution.

---

## 18. Unified Video-Action Joint Denoising for Dexterous Action and Data Generation

**Authors:** Dingrui Wang, YuAn Wang, Jinkun Liu, ..., Yu Sun, Johannes Betz
**arXiv:** [2606.03868](https://arxiv.org/abs/2606.03868)
**Categories:** Computer Vision and Pattern Recognition (cs.CV)

Recent world action models leverage video foundation models by aligning broad visual-dynamics priors with executable robot actions. We revisit this alignment from a distributional perspective. Existing formulations typically narrow the aligned prior into an observation-conditioned policy distribution over future actions. In contrast, we keep the distribution broader by modeling the joint space of interaction videos and executable hand trajectories under multiple conditioning regimes. We propose Donk, a unified video-action denoising model for dexterous hands. With language, an initial image, and the initial hand state, Donk samples future videos and bimanual MANO trajectories as an action policy. Without the image condition, the same denoising architecture samples paired video-action rollouts from a text-conditioned distribution, turning the aligned video prior into a data engine. Across action, video, and text-only generation evaluations, Donk improves dexterous trajectory accuracy, preserves strong video fidelity, and produces smooth text-conditioned action rollouts under the same unified training recipe.

---
