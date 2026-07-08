# arXiv Daily Digest — 2026-06-05

**Mode:** direct
**Categories:** cs.AI, cs.LG, cs.RO, cs.CV
**Keywords:** VLA, world model, world action model
**Papers found:** 15

---

## 1. WorldFly: A World-Model-Based Vision-Language-Action Model for UAV Navigation

**Authors:** Shengtao Zheng, Kai Li, Weichen Zhang, ..., Yong Li, Xiao-Ping Zhang
**arXiv:** [2606.06147](https://arxiv.org/abs/2606.06147)
**Categories:** Artificial Intelligence (cs.AI)

End-to-end Vision-Language-Action (VLA) models have shown promise in UAV navigation. However, existing approaches typically rely on historical observations to directly predict actions, often struggling in dense urban environments where severe occlusions and sharp turns result in drastic viewpoint transitions. We argue that the ability to "imagine" future states -- inherent in World Models -- is critical for robust decision-making under such partial observability. To address this, we construct a challenging Urban Canyon Traversal Benchmark, specifically designed to evaluate spatial understanding in scenarios characterized by severe occlusions and drastic viewpoint transitions. To this end, we propose WorldFly, a novel world-model-based VLA framework that employs a dual-branch coupled flow matching mechanism to jointly generate future video predictions and navigation actions, thereby explicitly guiding the agent's policy via spatial imagination. Extensive evaluations on our benchmark demonstrate that WorldFly outperforms other baselines, particularly in unseen environments, validating the effectiveness of integrating world models into embodied aerial agents.

---

## 2. PLAN-S: Bridging Planning with Latent Style Dynamics for Autonomous Driving World Models

**Authors:** Xiaoyun Qiu, Jingtao He, Yijie Chen, ..., Yixuan Wang, Xinhu Zheng
**arXiv:** [2606.06014](https://arxiv.org/abs/2606.06014)
**Categories:** Artificial Intelligence (cs.AI); Robotics (cs.RO)

Latent world models (LWMs) have strengthened end-to-end autonomous driving by forecasting compact scene dynamics for downstream planning. However, existing LWM-based planners usually generate trajectories directly from entangled latent representations. This compact latent-to-planner pathway lacks explicit modeling of risk, drivability, and diverse style preferences, making driving-style dynamics difficult to supervise, inspect, or modulate before a final trajectory is selected. We propose PLAN-S (PLANning with latent Style dynamics), a planner-facing bridge that addresses this compactness-controllability dilemma by decoding a style-conditioned, four-channel semantic cost map from the latent representation. The cost map is conditioned on ego state and driving style and is consumed up-stream of the planning decision through two host-side interfaces: attention-level fusion for regression planners and reward-level fusion for anchor-score planners. We validate PLAN-S on two architecturally distinct hosts, ResWorld on nuScenes and WoTE on NAVSIM, while keeping the host backbones frozen to isolate the contribution of the proposed bridge. On nuScenes, PLAN-S reduces L2 at every horizon over the baseline, with 0.55 m average L2 and a 42% relative reduction in the 3 s collision rate. On NAVSIM, the rule-cost variant reaches 89.4 Predictive Driver Model Score (PDMS), while the learned cost variant provides complementary gains on baseline-challenging scenes. Ablations show that the cost pathway contributes most directly to safer trajectory selection. Qualitative results further show that PLAN-S can produce diverse cost maps, with spatially consistent variations aligned to different driving styles.

---

## 3. Towards World Models in Biomedical Research

**Authors:** Guangyu Wang, Jingkun Yue, Siqi Zhang, ..., Ping Zhang, Yong Li
**arXiv:** [2606.05925](https://arxiv.org/abs/2606.05925)
**Categories:** Artificial Intelligence (cs.AI)

A central goal of biomedicine is to understand, predict and ultimately control the dynamic mechanisms by which biological systems respond to perturbations, disease progression and therapeutic intervention. Although foundation models and large language models have accelerated biomedical data interpretation, most current systems remain focused on static pattern recognition rather than prospective simulation of biological futures. Here we propose biomedical world models as a paradigm for AI-driven discovery. These models learn latent representations of molecular, cellular, tissue and clinical states, together with intervention-conditioned dynamics that allow future trajectories to be simulated before actions are taken. We discuss how biomedical world models could function as data engines, environment simulators and scientific planning substrates across applications including virtual cells, organoids, virtual patients and surgical simulation. We outline the data infrastructure, evaluation benchmarks, safety constraints and governance frameworks required. Biomedical world models may provide a foundation for simulation-guided, closed-loop and experimentally actionable biomedical discovery.

---

## 4. TempoVLA: Learning Speed-Controllable Vision-Language-Action Policies

**Authors:** Dong Jing, Jingchen Nie, Tianqi Zhang, ..., Zhiwu Lu, Mingyu Ding
**arXiv:** [2606.06491](https://arxiv.org/abs/2606.06491)
**Categories:** Robotics (cs.RO); Artificial Intelligence (cs.AI)

Robot manipulation alternates between low-risk transit phases that call for fast execution and high-risk contact stages that demand slow, precise motion. Yet existing Vision-Language-Action models (VLAs) only inherit a single fixed speed from training demonstrations. Prior efforts to accelerate VLAs through model compression, KV-cache reuse, or reinforcement learning only shift the policy from one fixed speed to another, and leave deceleration almost unexplored. We observe that the magnitude of each predicted action already governs how fast the robot moves, opening a direct route to controllable execution speed. We turn this observation into TempoVLA, a single VLA whose execution speed is controlled by an explicit condition. TempoVLA combines two coupled components. (1) A data-side Variable-Speed Trajectory Augmentation (VSTA) that re-times demonstration to any target speed by merging or splitting actions while preserving its motion semantics. (2) A model-side conditioning mechanism that feeds the speed to the policy. Statistics show that VSTA reaches the requested speed with negligible motion error. Experiments in simulation and on real-world tasks demonstrate that TempoVLA achieves flexible speed control in both directions, while VSTA additionally boosts the default $1\times$ performance via better data utilization. Furthermore, by cooperating with a large multimodal model, TempoVLA realizes dynamic speed control, accelerating through low-risk phases and decelerating for high-risk ones.

---

## 5. MPCoT: Reward-Guided Multi-Path Latent Reasoning for Test-Time Scalable Vision-Language-Action

**Authors:** Boyang Zhang, Lianlei Shan
**arXiv:** [2606.06245](https://arxiv.org/abs/2606.06245)
**Categories:** Robotics (cs.RO); Artificial Intelligence (cs.AI)

Vision-Language-Action (VLA) policies remain brittle in long-horizon and high-uncertainty control, where one-pass action decoding provides limited inference-time deliberation. Explicit chain-of-thought can increase reasoning depth, but introduces token latency and an indirect text-to-action interface. We propose MPCoT, a reward-guided multi-path latent reasoning framework that initializes $M$ hypotheses, refines them for K weight-tied steps, and softly aggregates them before action decoding. A training-only path-preference objective evaluates candidate action branches with expert-action consistency, world-model/VLM-based progress, and success feedback to align the latent path scorer with downstream execution quality. MPCoT preserves the original 8-step action interface, generates zero reasoning tokens, and exposes configurable inference controls (K,M). Under matched protocols on LIBERO and CALVIN, MPCoT improves long-horizon performance, with ablations confirming depth-width effects, confidence-weighted aggregation, and reward-guided path supervision.

---

## 6. World-Language-Action Model for Unified World Modeling, Language Reasoning, and Action Synthesis

**Authors:** Yi Yang, Zhihong Liu, Siqi Kou, ..., Pengfei Liu, Zhijie Deng
**arXiv:** [2606.05979](https://arxiv.org/abs/2606.05979)
**Categories:** Robotics (cs.RO); Artificial Intelligence (cs.AI)

We propose world-language-action (WLA) models as a new class of embodied foundation models. WLA takes textual instructions, images, and robot states as inputs to jointly predict textual subtasks, subgoal images, and robot actions, conjoining the \emph{world modeling interface} to learn from extensive egocentric videos as in the world-action model (WAM) and the \emph{language reasoning} capacities to solve complex long-horizon tasks as in vision-language-action (VLA) models. At the core of WLA lies an \emph{autoregressive (AR)} Transformer backbone, instead of a bidirectional diffusion Transformer as in WAMs, to predict the \emph{next state}, comprising the \emph{semantic-level} textual intention and complementary \emph{fine-grained} physical dynamics. The physical dynamics are supervised by the world modeling objective based on a dedicated World Expert, and are leveraged to ease the characterization of the state-action correlation for the Action Expert. WLA leverages meta-queries to make the world prediction \emph{implicitly} impact the action generation so that the former can be disabled during inference. The world prediction can also be activated to enable test-time scaling for improved robot control. Our WLA-0 prototype, with 2B active parameters, achieves 40 ms per inference on an NVIDIA RTX 5090. Evaluations across simulated and real-world environments demonstrate that WLA-0 achieves state-of-the-art multi-task and long-horizon learning abilities, e.g., 92.94\% success rate on RoboTwin2.0 Clean and 56.5\% success rate on RMBench. WLA-0 also holds the promise to learn novel tasks directly from \emph{cross-embodiment robot videos} without action annotations.

---

## 7. Let It Be Simple: One-Step Action Generation for Vision-Language-Action Models

**Authors:** Yitong Chen, Shiduo Zhang, Jingjing Gong, Xipeng Qiu
**arXiv:** [2606.05737](https://arxiv.org/abs/2606.05737)
**Categories:** Computer Vision and Pattern Recognition (cs.CV); Artificial Intelligence (cs.AI); Machine Learning (cs.LG); Robotics (cs.RO)

Diffusion-based vision-language-action (VLA) models often inherit the image-generation view: actions are generated by iterative denoising. We argue that VLA action generation has a different condition-target structure: the policy is conditioned on rich observations, language, and state, but predicts only a compact, low-dimensional action chunk. Under this asymmetry, strong one-step action generation should not necessarily require the advanced one-step methods developed for image synthesis. We keep standard velocity prediction and add no teacher model, distillation stage, or auxiliary objective; in our main recipe, we simply bias the training time distribution toward high-noise states. We first isolate the effect in a controlled MNIST grid-to-sequence task, then test it with extensive robot-policy experiments. Across standard LIBERO, LIBERO-Plus, and LIBERO-Pro, one-step policies trained with high-noise biased schedules generally match ten-step decoding under the same recipe, and on standard LIBERO can exceed ten-step policies trained with a uniform time distribution. A real-robot bimanual YAM RSS evaluation gives a small-sample cross-architecture check of the same sampler trend. On a 1.4B VLM model with a 30M action head, one-step decoding reaches 95.6\% on LIBERO-Long. These results show that strong one-step VLA action generation can emerge from standard diffusion training, without importing the full few-step diffusion machinery developed for image generation.

---

## 8. Autoregressive Diffusion World Models for Off-Policy Evaluation of LLM Agents

**Authors:** Kaixuan Liu, Guojun Xiong, Weinan Zhang, Shengpu Tang
**arXiv:** [2606.05558](https://arxiv.org/abs/2606.05558)
**Categories:** Machine Learning (cs.LG)

Evaluating large language model (LLM) agents in multi-turn interactive environments is expensive and risky, as it requires online environment interaction. We propose ADWM (Autoregressive Diffusion World Model), an evaluation framework that estimates the performance of a new LLM agent policy purely from pre-collected trajectories. The core idea is to learn a latent diffusion world model that simulates how the environment responds to the evaluation policy, without ever executing it in the real environment. Existing diffusion-based OPE methods guide full trajectories in a single pass by jointly diffusing states and actions, an assumption that breaks down for LLM agents whose actions are discrete text that must be sampled from the policy after observing the environment. Unlike autoregressive world models that suffer from compounding errors, ADWM models each transition as an independent denoising process, enabling reliable step-by-step rollouts where the world model and agent alternate in causal order. Crucially, the LLM agent under evaluation directly guides the diffusion generation at each step via a policy-conditioned score function, ensuring that simulated trajectories accurately reflect its decision-making patterns. Empirically, ADWM achieves accurate value estimates and evaluation reliability across diverse multi-turn agent tasks, demonstrating its promise as a practical framework for offline LLM agent evaluation.

---

## 9. Flash-WAM: Modality-Aware Distillation for World Action Models

**Authors:** Arman Akbari, Ci Zhang, Arash Akbari, ..., Geng Yuan, Yanzhi Wang
**arXiv:** [2606.05254](https://arxiv.org/abs/2606.05254)
**Categories:** Machine Learning (cs.LG); Computer Vision and Pattern Recognition (cs.CV); Robotics (cs.RO)

World-action models (WAMs) jointly generate future video and robot actions through iterative diffusion, achieving strong performance on manipulation benchmarks but requiring tens of denoising steps, a cost that precludes real-time control. Step distillation has emerged as the natural remedy, but off-the-shelf methods break down in the joint video-action setting because video and action streams use different SNR-shifted noise schedules and reach training with substantially different marginal noise distributions, an asymmetry that single-modality distillation methods cannot accommodate. We introduce \textbf{Flash-WAM}, a modality-aware step-distillation framework inspired by consistency distillation that selects the consistency function for each modality to match its noise regime: a linear-gradient-scaling parametrization for the action stream's low-noise regime, paired with a variance-preserving parametrization for the video stream's high-noise regime, grounded in a structural analysis of the consistency-function family that characterizes the achievable gradient scaling under the consistency boundary condition. Instantiated on LingBot-VA, Flash-WAM compresses inference to a single step in each modality. On RoboTwin 2.0, this reduces per-chunk latency from $8.1$ seconds to $348$ ms on NVIDIA L40S, a $23{\times}$ speedup that enables real-time inference. Flash-WAM preserves task success on simulation benchmarks ($85.5\%$ RoboTwin 2.0, $95.7\%$ LIBERO) and substantially recovers real-world performance ($60\%$ average on a Unitree G1 humanoid robot), while naive consistency distillation drops to $24\%$ at the same step budget.

---

## 10. AffordanceVLA: A Vision-Language-Action Model Empowering Action Generation through Affordance-Aware Understanding

**Authors:** Qize Yu, Jiadi You, Yuran Wang, ..., Junwei Liang, Yingcong Chen
**arXiv:** [2606.06155](https://arxiv.org/abs/2606.06155)
**Categories:** Robotics (cs.RO); Computer Vision and Pattern Recognition (cs.CV); Multimedia (cs.MM)

Vision-Language-Action (VLA) models leverage the rich world knowledge of pretrained vision-language models (VLMs) to enable instruction-following robotic manipulation. However, the structural mismatch between VLM semantic spaces and embodied control policies often hinders the learning of precise perception--action mappings. To address this challenge, we propose \textbf{AffordanceVLA}, a unified framework that introduces structured affordance forecasting as a task-oriented intermediate representation to establish a more precise and robust perception--action mapping. Specifically, we progressively model manipulation priors through three complementary components: 1) \textbf{Which2Act} for object-centric grounding via visual latent prediction to suppress distractions; 2) \textbf{Where2Act} for 2D interaction localization via affordance map estimation; and 3) \textbf{How2Act} for 3D geometric reasoning to guide manipulation policies. These affordance cues provide spatially grounded, semantically conditioned, and action-coupled intermediate representations, thereby naturally bridging vision, language and action. We integrate these modules into a Mixture-of-Transformer (MoT) architecture with specialized experts and train the model using a three-stage training strategy with a progressive data curriculum. To overcome the scarcity of dense affordance labels in robotic datasets, we also develop a robust automated data augmentation pipeline. Extensive experiments on simulation and real-world demonstrate that AffordanceVLA achieves strong performance across diverse manipulation scenarios.

---

## 11. PiL-World: A Chunk-Wise World Model for VLA Policy-in-the-Loop Evaluation

**Authors:** Chong Ma, Taiyi Su, Jian Zhu, ..., Yi Xu, Hanli Wang
**arXiv:** [2606.05773](https://arxiv.org/abs/2606.05773)
**Categories:** Robotics (cs.RO)

Vision-language-action (VLA) policies operate in a closed loop in real-world robot tasks: a robot observes the scene, executes an action chunk, and conditions its next decision on the resulting observation. However, most existing world models for robot action evaluation are limited to open-loop prediction along pre-collected action trajectories. This prevents them from supporting closed-loop VLA evaluation, where each action chunk must be conditioned on the observation generated by the previous execution. To address this gap, we propose PiL-World, a chunk-wise world model designed for policy-in-the-loop VLA evaluation. Given the current observation and the action trajectory rolled out by a VLA policy, PiL-World generates multi-view future observations that are consistent with the VLA rollout and match the image inputs required by the policy. By alternating between VLA inference and world-model prediction, PiL-World enables closed-loop evaluation without real robot execution at every step. To improve rollout fidelity, PiL-World conditions video generation on action-derived visual control from head-view robot motion and latent histories that encode task execution context, while jointly predicting complementary multi-view observations. Beyond successful teleoperated demonstrations, it also learns from failed execution trajectories, helping the imagined rollouts better match the distribution of real policy executions. We evaluate PiL-World on three real dual-arm manipulation tasks. PiL-World generates imagined rollouts that are highly consistent with real robot executions. More importantly, compared with the baseline, it reduces the error between VLA success rates measured in real-world rollouts and those estimated through closed-loop world-model evaluation from 63.2% to 12.0%.

---

## 12. FlowPRO: Reward-Free Reinforced Fine-Tuning of Flow-Matching VLAs via Proximalized Preference Optimization

**Authors:** Yihao Wu, He Zhang, Junbo Tan, Xueqian Wang, Zhengyou Zhang
**arXiv:** [2606.05468](https://arxiv.org/abs/2606.05468)
**Categories:** Robotics (cs.RO)

Post-training Vision-Language-Action (VLA) models into policies that can be reliably deployed on real robots remains a major bottleneck. SFT and DAgger exploit failure signals only indirectly, and reward-based RL is bottlenecked by the difficulty of real-world reward design and of training reliable critics. We present FlowPRO, a reward-free offline reinforced fine-tuning framework for flow-matching VLAs. Algorithmically, we propose RPRO (Robotic Flow-matching Proximalized Preference Optimization), a preference-optimization objective tailored to the flow-matching action head of VLA models. RPRO pairs a contrastive optimizer with an explicit proximal regularizer that anchors the absolute magnitude of the implicit reward, thereby eliminating the reward-hacking failure mode of plain Flow-DPO. On the data side, a teleoperated intervention-and-rollback paradigm produces naturally paired positive and negative trajectories $(\tau^w, \tau^l)$ on a real robot from a single operator action; a Smooth Interpolation procedure, combined with batch mixing, then converts these sparse corrections into dense per-state supervision while preserving the base policy's capabilities. On four long-horizon bimanual tasks, FlowPRO attains the highest success rate, outperforming four representative baselines, and ablations confirm the contribution of each loss component.

---

## 13. DRIFT: A Residual Flow Adapter for Decoding Continuous Outputs in Vision-Language Models

**Authors:** Zhuoming Liu, Jinhong Lin, Kwan Man Cheng, ..., Shayok Bagchi, Yin Li
**arXiv:** [2606.05758](https://arxiv.org/abs/2606.05758)
**Categories:** Computer Vision and Pattern Recognition (cs.CV); Artificial Intelligence (cs.AI); Machine Learning (cs.LG)

Many modern vision-language models (VLMs) build on autoregressive decoding of discrete tokens. While text-based output interfaces enable scalable pretraining and strong zero-shot generalization across diverse tasks, they are poorly suited for problems that require precise continuous outputs, such as localizing temporal boundaries of events or generating robotic control actions. To address this challenge, we propose DRIFT, a general framework for adapting pretrained VLMs to continuous decoding tasks. DRIFT combines a base predictor, which provides a coarse estimate of the target output, with a generative refinement module based on flow matching that iteratively improves the prediction. This residual formulation transforms the generative modeling problem from learning a global output distribution to modeling a localized residual distribution around a strong prior, substantially simplifying optimization. We evaluate DRIFT on both perception and planning tasks, including visual grounding and robotic control. Across multiple tasks and architectures spanning MLLMs, VLAs, and WAMs, DRIFT consistently outperforms a strong set of regression- and generative-based solutions.

---

## 14. Discrete-WAM: Unified Discrete Vision-Action Token Editing for World-Policy Learning

**Authors:** Ziyang Yao, Haochen Liu, Yuncheng Jiang, ..., Guang Chen, Hangjun Ye
**arXiv:** [2606.05645](https://arxiv.org/abs/2606.05645)
**Categories:** Robotics (cs.RO)

Autonomous driving requires reasoning about how ego actions shape the evolution of the surrounding world. However, most end-to-end methods rely on direct state-to-action mappings, capturing correlations without explicitly modeling action-conditioned dynamics. Conversely, continuous-latent world models often lack compositional structure for causal reasoning across counterfactual futures. We introduce Discrete-WAM, a unified latent vision-action world policy that represents future visual states and ego actions as aligned discrete tokens, enabling compositional causal reasoning across alternative futures. Built upon this unified discrete alignment, Discrete-WAM establishes a shared discrete diffusion framework with unified generative tasks, jointly formulating world modeling, world-action policy, and hierarchical decision-enabled policy, supporting compositional generalization across diverse driving scenarios. Experiments on large-scale autonomous-driving benchmarks show that Discrete-WAM achieves competitive performance while supporting controllable generation and counterfactual reasoning, offering a principled path toward more reliable decision-making.

---

## 15. Thinking with Imagination: Agentic Visual Spatial Reasoning with World Simulators

**Authors:** Chenming Zhu, Jingli Lin, Yilin Long, ..., Jiangmiao Pang, Xihui Liu
**arXiv:** [2606.06476](https://arxiv.org/abs/2606.06476)
**Categories:** Computer Vision and Pattern Recognition (cs.CV)

While Vision-Language Models (VLMs) have shown strong visual reasoning capabilities, their spatial reasoning abilities remain largely constrained to the observed images and text-oriented chain-of-thought. They often struggle to infer unobserved layouts, maintain cross-view consistency, and reason from alternative viewpoints when only limited egocentric observations are available. In this work, we study this problem as thinking with imagination, where a VLM actively acquires imagined visual evidence by interacting with a world simulator during reasoning. We propose Astra, an agentic spatial reasoning framework that empowers VLMs with action-conditioned visual imagination. Specifically, Astra couples Astra-VL, an RL-trained VLM policy, with Astra-WM, a Bagel-based world simulator that generates novel-view observations from context images and natural-language camera motions. To provide reliable imagined evidence, Astra-WM is trained with view consistency tuning to improve pose and content consistency across views. In the RL stage, we propose a world-simulator-in-the-loop two-phase RL curriculum to stabilize tool-use exploration and advance the model's ability to invoke the simulator only when imagined observations improve over direct answering. Experiments demonstrate that both the world simulator and the agentic policy are necessary: Astra-WM improves simulator-augmented Gemini-3-Flash on MMSI-Bench from 45.1 to 49.5, while Astra-VL improves the Qwen3-VL backbone from 29.8 to 38.8 on MMSI-Bench and from 36.8 to 42.7 on MindCube. These results show that imagined observations can provide useful spatial evidence, but effective world-model-augmented reasoning requires learning when, where, and how to imagine.

---
