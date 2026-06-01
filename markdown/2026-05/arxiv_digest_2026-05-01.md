# arXiv Daily Digest — 2026-05-01

**Mode:** direct
**Categories:** cs.AI, cs.LG, cs.RO, cs.CV
**Keywords:** VLA, world model, world action model
**Papers found:** 8

---

## 1. Graph World Models: Concepts, Taxonomy, and Future Directions

**Authors:** Jiawei Liu, Senqiao Yang, Mingjun Wang, Yu Wang, Bei Yu
**arXiv:** [2604.27895](https://arxiv.org/abs/2604.27895)
**Categories:** Artificial Intelligence (cs.AI)

As one of the mainstream models of artificial intelligence, world models allow agents to learn the representation of the environment for efficient prediction and planning. However, classical world models based on flat tensors face several key problems, including noise sensitivity, error accumulation and weak reasoning. To address these limitations, many recent studies use graph structure to decompose the environment into entity nodes and interactive edges, and model virtual environments in a structured space. This paper systematically formalizes and unifies these emerging graph-based works under the concept of graph world models (GWMs). To the best of our knowledge, GWMs have not yet been explicitly defined and surveyed as a unified research paradigm. Furthermore, we propose a taxonomy based on relational inductive biases (RIB), categorizing GWMs by the specific structural priors they inject: (1) spatial RIB for topological abstraction; (2) physical RIB for dynamic simulation; and (3) logical RIB for causal and semantic reasoning. For each model category, we outline the key design principles, summarize representative models, and conduct comparative analyses. We further discuss open challenges and future directions, including dynamic graph adaptation, probabilistic relational dynamics, multi-granularity inductive biases, and the need for dedicated benchmarks and evaluation metrics for GWMs.

---

## 2. LaST-R1: Reinforcing Action via Adaptive Physical Latent Reasoning for VLA Models

**Authors:** Hao Chen, Jiaming Liu, Zhonghao Yan, ..., Shanghang Zhang, Pheng-Ann Heng
**arXiv:** [2604.28192](https://arxiv.org/abs/2604.28192)
**Categories:** Robotics (cs.RO); Computer Vision and Pattern Recognition (cs.CV)

Vision-Language-Action (VLA) models have increasingly incorporated reasoning mechanisms for complex robotic manipulation. However, existing approaches share a critical limitation: whether employing explicit linguistic reasoning that suffers from latency and discretization, or utilizing more expressive continuous latent reasoning, they are predominantly confined to static imitation learning that limits adaptability and generalization. While online reinforcement learning (RL) has been introduced to VLAs to enable trial-and-error exploration, current methods exclusively optimize the vanilla action space, bypassing the underlying physical reasoning process. In this paper, we present \textbf{LaST-R1}, a unified VLA framework that integrates latent Chain-of-Thought (CoT) reasoning over physical dynamics prior to action execution, along with a tailored RL post-training paradigm. Specifically, we propose \textbf{Latent-to-Action Policy Optimization (LAPO)}, a novel RL algorithm that jointly optimizes the latent reasoning process and the action generation. By bridging reasoning and control, LAPO improves the representation of physical world modeling and enhances robustness in interactive environments. Furthermore, an \textbf{adaptive latent CoT mechanism} is introduced to allow the policy to dynamically adjust its reasoning horizon based on environment complexity. Extensive experiments show that LaST-R1 achieves a near-perfect 99.8\% average success rate on the LIBERO benchmark with only one-shot supervised warm-up, significantly improving convergence speed and performance over prior state-of-the-art methods. In real-world deployments, LAPO post-training yields up to a 44\% improvement over the initial warm-up policy across four complex tasks, including both single-arm and dual-arm settings. Finally, LaST-R1 demonstrates strong generalization across simulated and real-world environments.

---

## 3. Flying by Inference: Active Inference World Models for Adaptive UAV Swarms

**Authors:** Kaleem Arshid, Ali Krayani, Lucio Marcenaro, David Martin Gomez, Carlo Regazzoni
**arXiv:** [2604.27935](https://arxiv.org/abs/2604.27935)
**Categories:** Robotics (cs.RO); Signal Processing (eess.SP); Systems and Control (eess.SY)

This paper presents an expert-guided active-inference-inspired framework for adaptive UAV swarm trajectory planning. The proposed method converts multi-UAV trajectory design from a repeated combinatorial optimization problem into a hierarchical probabilistic inference problem. In the offline phase, a genetic-algorithm planner with repulsive-force collision avoidance (GA--RF) generates expert demonstrations, which are abstracted into Mission, Route, and Motion dictionaries. These dictionaries are used to learn a probabilistic world model that captures how expert mission allocations induce route orders and how route orders induce motion-level behaviors. During online operation, the UAV swarm evaluates candidate actions by forming posterior beliefs over symbolic states and minimizing KL-divergence-based abnormality indicators with respect to expert-derived reference distributions. This enables mission allocation, route insertion, motion adaptation, and collision-aware replanning without rerunning the offline optimizer. Bayesian state estimators, including EKF and PF modules, are integrated at the motion level to improve trajectory correction under uncertainty. Simulation results show that the proposed framework preserves expert-like planning structure while producing smoother and more stable behavior than modified Q-learning. Additional validation using real-flight UAV trajectory data demonstrates that the learned world model can correct symbolic predictions under noisy and non-smooth observations, supporting its applicability to adaptive UAV swarm autonomy.

---

## 4. MotuBrain: An Advanced World Action Model for Robot Control

**Authors:** MotuBrain Team, Chendong Xiang, Fan Bao, ..., Zeyuan Wang, Jun Zhu
**arXiv:** [2604.27792](https://arxiv.org/abs/2604.27792)
**Categories:** Robotics (cs.RO)

Vision-Language-Action (VLA) models achieve strong semantic generalization but often lack fine-grained modeling of world dynamics. Recent work explores video generation models as a foundation for world modeling, leading to unified World Action Models (WAMs) that jointly model visual dynamics and actions. We present MotuBrain, a unified multimodal generative model that jointly models video and action under a UniDiffuser formulation with a three-stream Mixture-of-Transformers architecture. A single model supports multiple inference modes, including policy learning, world modeling, video generation, inverse dynamics, and joint video-action prediction, while scaling to heterogeneous multimodal data such as video-only and cross-embodiment robot data. To improve real-world applicability, MotuBrain introduces a unified multiview representation, explicit language-action coupling, and an efficient inference stack, achieving over 50x speedup for real-time deployment.

---

## 5. HERMES++: Toward a Unified Driving World Model for 3D Scene Understanding and Generation

**Authors:** Xin Zhou, Dingkang Liang, Xiwu Chen, ..., Hengshuang Zhao, Xiang Bai
**arXiv:** [2604.28196](https://arxiv.org/abs/2604.28196)
**Categories:** Computer Vision and Pattern Recognition (cs.CV)

Driving world models serve as a pivotal technology for autonomous driving by simulating environmental dynamics. However, existing approaches predominantly focus on future scene generation, often overlooking comprehensive 3D scene understanding. Conversely, while Large Language Models (LLMs) demonstrate impressive reasoning capabilities, they lack the capacity to predict future geometric evolution, creating a significant disparity between semantic interpretation and physical simulation. To bridge this gap, we propose HERMES++, a unified driving world model that integrates 3D scene understanding and future geometry prediction within a single framework. Our approach addresses the distinct requirements of these tasks through synergistic designs. First, a BEV representation consolidates multi-view spatial information into a structure compatible with LLMs. Second, we introduce LLM-enhanced world queries to facilitate knowledge transfer from the understanding branch. Third, a Current-to-Future Link is designed to bridge the temporal gap, conditioning geometric evolution on semantic context. Finally, to enforce structural integrity, we employ a Joint Geometric Optimization strategy that integrates explicit geometric constraints with implicit latent regularization to align internal representations with geometry-aware priors. Extensive evaluations on multiple benchmarks validate the effectiveness of our method. HERMES++ achieves strong performance, outperforming specialist approaches in both future point cloud prediction and 3D scene understanding tasks. The model and code will be publicly released at this https URL.

---

## 6. Visual Generation in the New Era: An Evolution from Atomic Mapping to Agentic World Modeling

**Authors:** Keming Wu, Zuhao Yang, Kaichen Zhang, ..., Shijian Lu, Bin Wang
**arXiv:** [2604.28185](https://arxiv.org/abs/2604.28185)
**Categories:** Computer Vision and Pattern Recognition (cs.CV)

Recent visual generation models have made major progress in photorealism, typography, instruction following, and interactive editing, yet they still struggle with spatial reasoning, persistent state, long-horizon consistency, and causal understanding. We argue that the field should move beyond appearance synthesis toward intelligent visual generation: plausible visuals grounded in structure, dynamics, domain knowledge, and causal relations. To frame this shift, we introduce a five-level taxonomy: Atomic Generation, Conditional Generation, In-Context Generation, Agentic Generation, and World-Modeling Generation, progressing from passive renderers to interactive, agentic, world-aware generators. We analyze key technical drivers, including flow matching, unified understanding-and-generation models, improved visual representations, post-training, reward modeling, data curation, synthetic data distillation, and sampling acceleration. We further show that current evaluations often overestimate progress by emphasizing perceptual quality while missing structural, temporal, and causal failures. By combining benchmark review, in-the-wild stress tests, and expert-constrained case studies, this roadmap offers a capability-centered lens for understanding, evaluating, and advancing the next generation of intelligent visual generation systems.

---

## 7. Judge, Then Drive: A Critic-Centric Vision Language Action Framework for Autonomous Driving

**Authors:** Lijin Yang, Jianing Huang, Zhongzhan Huang, Shu Liu, Hao Yang
**arXiv:** [2604.27366](https://arxiv.org/abs/2604.27366)
**Categories:** Computer Vision and Pattern Recognition (cs.CV)

Recent advances in vision language action (VLA) models have shown remarkable potential for autonomous driving by directly mapping multimodal inputs to control signals. However, previous VLA-based methods have not explicitly exploited the critic capability of VLAs to refine driving decisions, even though such capability has been well demonstrated in other LLM-based domains, thereby limiting their performance in complex closed-loop scenarios. In this work, we present a theoretically inspired two-stage framework, CriticVLA, which extends the role of VLAs from acting to judging. CriticVLA first generates a rough trajectory and then refines it through multimodal evaluation and single-step optimization guided by a VLA-based critic, yielding higher-quality driving behaviors. To support this process, we construct a large-scale synthetic dataset of 12.9 million annotated trajectories covering diverse driving scenarios, which enhances the critic's reasoning and refinement abilities. Extensive closed-loop experiments on the Bench2Drive benchmark show that CriticVLA significantly surpasses state-of-the-art baselines, achieving a 73.33% total success rate and delivering about 30% improvement in challenging scenarios.

---

## 8. Dreaming Across Towns: Semantic Rollout and Town-Adversarial Regularization for Zero-Shot Held-Out-Town Fixed-Route Driving in CARLA

**Authors:** Feeza Khan Khanzada, Jaerock Kwon
**arXiv:** [2604.27994](https://arxiv.org/abs/2604.27994)
**Categories:** Robotics (cs.RO)

Learned driving agents often degrade when deployed in unseen environments. This paper studies a deliberately bounded instance of that problem in the CARLA simulator: zero-shot transfer of a closed-loop fixed-route driving agent from Town05 and Town06 to unseen Town03 and Town04. The study isolates structural town shift by keeping weather fixed to ClearNoon and removing traffic and pedestrians. We build on a Dreamer-style latent world-model agent and add two training-only auxiliary losses: multi-horizon prediction of future visual-semantic embeddings along imagined rollouts and town-adversarial supervision on a semantic projection of the recurrent latent state. A causal context feature conditions the semantic rollout predictor, while the actor and critic retain the standard control feature. The policy receives no navigation command, route polyline, goal pose, or map input; the reference route is used only by the environment for reward, progress, success, and termination. Across the evaluated held-out towns, the proposed model achieves the highest mean success rate among the included Dreamer-family methods. Secondary safety and lane-keeping metrics are mixed across towns. These results support a bounded conclusion: in this controlled fixed-weather CARLA setting, semantic rollout supervision combined with town-adversarial regularization improves mean held-out-town route completion.

---
