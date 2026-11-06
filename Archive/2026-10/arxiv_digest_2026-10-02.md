# arXiv Daily Digest — 2026-10-02

**Mode:** direct
**Categories:** cs.AI, cs.LG, cs.RO, cs.CV
**Keywords:** VLA, RSI, agentic robot, self-improving robot, self-evolving robot, robot harness
**Papers found:** 13

---

## 1. Divide-and-Remember: Recursive Action-Relevant Memory for Long-Horizon VLA Policies

**Authors:** Xuehui Yu, Eason Yu, Meiyi Wang, ..., Stefano V. Albrecht, Harold Soh
**arXiv:** [2610.00982](https://arxiv.org/abs/2610.00982)
**Categories:** Robotics (cs.RO); Artificial Intelligence (cs.AI)

Vision-language-action (VLA) models struggle on history-dependent manipulation tasks, where the current observation alone does not determine the action, and the policy needs a memory of the history. Existing memory methods decide what to remember by design, for example, keeping frames with large pixel changes, and show inconsistent gains across tasks. We view what to remember as an optimisation problem. From the POMDP formulation of imitation learning, we show that the optimal memory maximises the conditional mutual information $I(a_t; m_t \mid o_t)$ between the action and the memory given the current observation. Intuitively, this means preserving the action-relevant information in the history that is not already contained in the current observation. Based on our analysis, we propose Divide-and-Remember (D&R), a recursive memory method that learns a memory function $m_t = M(h_t)$ and scales to long contexts while staying compute-light. It involves two strategies: (1) the selection over the full history is divided recursively into subproblems of top-$K$ selection over $2K$ tokens, so that fixed-size, lightweight selectors learned end-to-end support an unbounded history; (2) all recursion blocks share one selector, which captures the selection rule common to every block and keeps the method efficient. On RoboMME, a benchmark of 16 long-horizon manipulation tasks that require remembering when, where, what, and how to act, D&R achieves a state-of-the-art average success rate with consistent gains across all four suites under a budget of only 64 tokens; real-robot experiments show the same gain. Code, checkpoints and more results are at this https URL

---

## 2. TOAST: Stochastic Robot Action Tokenization for Autoregressive Vision-Language-Action Models

**Authors:** Keisuke Shirai, Tomohiro Motoda, Hanbit Oh, ..., Shotaro Miwa, Yukiyasu Domae
**arXiv:** [2610.00899](https://arxiv.org/abs/2610.00899)
**Categories:** Robotics (cs.RO); Artificial Intelligence (cs.AI); Machine Learning (cs.LG)

Autoregressive Vision-Language-Action models often represent continuous robot actions as discrete token sequences, enabling action prediction with standard next-token objectives. FAST has substantially improved this representation by compactly encoding action containing diverse temporal frequencies into relatively few tokens. However, while such compression reduces the number of action tokens required for autoregressive prediction, it does not necessarily improve the efficiency of policy learning from limited demonstrations. In particular, FAST typically assigns a single deterministic tokenization to each quantized action sequence, although multiple token sequences can represent and decode to the same robot motion. We investigate whether exploiting this representational redundancy can improve policy learning. In this paper, we propose TOkenization of Action sequences with STochastic sampling (TOAST), a stochastic action tokenization method that samples alternative tokenizations of the same quantized action sequence during policy training. This diversifies the discrete supervision while preserving the underlying robot action and requires no additional demonstrations. Experiments on LIBERO show that TOAST consistently improves over its deterministic counterpart, with the improvement increasing as training data decreases, achieving a 6.8 point gain in success rate when only 1/16 of training data is available. Across four real-robot manipulation tasks, TOAST further improves mean success rate by 15.8 points over the deterministic counterpart. These results demonstrate the effectiveness of stochastic action tokenization for autoregressive robot policy learning, particularly when training data are limited.

---

## 3. MIKASA-Robo-VLA: Benchmarking Memory in VLA Models for Long-Horizon Manipulation

**Authors:** Egor Cherepanov, Nikita Kachaev, Aleksandr I. Panov, Alexey K. Kovalev
**arXiv:** [2610.00604](https://arxiv.org/abs/2610.00604)
**Categories:** Machine Learning (cs.LG); Artificial Intelligence (cs.AI); Robotics (cs.RO)

Vision-language-action policies often see only one or a few recent frames, which makes it difficult to evaluate how they use information that disappears during a task. We introduce MIKASA-Robo-VLA, a benchmark of 90 language-conditioned manipulation tasks. All but 10 hide the cue an action depends on. Those 10 are reactive controls. MIKASA-Robo, the suite it rebuilds, has 32 tasks and uses language only in a representative VLA subset. Here every task provides an instruction, while memory-dependent tasks hide a task-relevant cue and reactive controls keep it available. For 70 tasks, environment phase timings specify an information gap, and for 28 of them the gap exceeds the 16-frame window of the widest fixed-context VLA we survey. The gap counts only the interval the cue is provably absent, not the full duration a policy must retain it, so every memory-dependent task still requires memory by construction, including the ones whose measured gap is short. We release 22,500 oracle trajectories across 10 memory types in RLDS and LeRobotDataset v3. A reference $\pi_{0.5}$ baseline with current images and proprioception, but no observation history or explicit memory module, is fine-tuned on 14 tasks and achieves 0.211 $\pm$ 0.044 mean task success. Its lower success on the evaluated Long-split tasks is confounded by open-loop chunking and the memory types represented in that subset. Project page: this https URL

---

## 4. When Reasoning Helps Action: Monitoring and Steering Chain-of-Thought in Vision-Language-Action Policies

**Authors:** Sathwik Karnik, Joseph JR. Lee, Aryaman Gupta, Somil Bansal
**arXiv:** [2610.00601](https://arxiv.org/abs/2610.00601)
**Categories:** Robotics (cs.RO); Artificial Intelligence (cs.AI)

Reasoning-enabled VLA policies expose chain-of-thought (CoT) traces that appear to explain and guide their actions, creating a potential interface for runtime safety through reasoning monitoring and correction. In this work, we define and operationalize two evaluation axes for assessing when this interface can improve embodied behavior: correctability, which measures whether unreliable reasoning can be detected and improved during generation, and actionability, which measures whether reasoning corrections produce behaviorally meaningful changes in the intended direction. To enable correctability, we introduce Token-level Reward for Utility-Steered Chain-of-Thought (TRUST), an offline-trained value model that predicts eventual reasoning correctness from partial prefixes and uses these estimates to monitor and selectively steer reasoning generation in frozen VLA policies. On the Alpamayo 1.5 driving VLA, TRUST monitors correctness with 88.9% accuracy and improves reasoning correctness from 75.9% to 90.0%. On a baseline-defined challenging subset in AlpaSim, TRUST reduces collision rate by 30.4% and maximum trajectory error by 11.5% relative to the unsteered policy, outperforming a compute-matched Best-of-4 baseline. On the DeepThinkVLA manipulation VLA, TRUST improves the correctness of grasp-state claims from 69.3% to 90.2% and action-choice claims from 68.8% to 85.9%, yet closed-loop task performance on LIBERO-Plus remains largely unchanged. Empirical analysis reveals intent-consistent behavioral effects in Alpamayo 1.5 but limited effects in DeepThinkVLA, helping interpret these different task-level outcomes. Together, our results show that gains in reasoning correctness do not automatically imply gains in embodied performance, motivating evaluation of correctability and actionability when using CoT as a runtime safety interface.

---

## 5. DriftOPD: Sequence-Level Reverse-KL Distillation for One-Step VLA Policies

**Authors:** Youngjun Jun, Kyumin Choi, Youngmin Kim, ..., Jangho Park, Jong Chul Ye
**arXiv:** [2610.00317](https://arxiv.org/abs/2610.00317)
**Categories:** Robotics (cs.RO); Artificial Intelligence (cs.AI); Computer Vision and Pattern Recognition (cs.CV); Machine Learning (cs.LG)

Vision-Language-Action (VLA) models increasingly rely on action experts that generate short action chunks under receding-horizon control. While chunk-level training is convenient across robot embodiments, it optimizes local action likelihood without explicitly accounting for long-horizon task success. Sequence-level reinforcement learning can address this limitation, but typically requires policy rollouts and closed-loop interaction, which are costly for real-robot manipulation. We introduce DriftOPD, a teacher-free, rollout-free framework for sequence-level on-policy distillation of continuous VLA action experts. We show that the sequence-level reverse Kullback-Leibler (KL) divergence decomposes into a chunk-level reverse-KL term and a future-potential term that captures the long-horizon effect of the current action. DriftOPD optimizes these two terms using a one-step drifting objective and a Q-function critic learned from offline demonstrations, respectively, enabling sequence-level optimization with only offline data and one-step action generation. Across multiple VLA architectures in simulation and real-world manipulation, DriftOPD generally outperforms existing one-step distillation baselines while achieving task success performance comparable to multi-step teacher policies. These results demonstrate that long-horizon behavior can be effectively distilled into one-step VLA action experts without online interaction or a separate teacher.

---

## 6. Same Scene, Different Task: Skill Alignment for Compositional Generalization in VLAs

**Authors:** Taegeun Yang, Youngju Na, Yoonki Cho, Sung-Eui Yoon
**arXiv:** [2610.00524](https://arxiv.org/abs/2610.00524)
**Categories:** Robotics (cs.RO); Machine Learning (cs.LG)

Vision-language-action (VLA) models often struggle to generalize to skill combinations absent from their fine-tuning demonstrations, even when every constituent skill has been demonstrated. We focus on a vision shortcut as one failure mode: during fine-tuning, visual observations can serve as a proxy for the instruction, so a policy may execute a demonstrated combination associated with similar observations rather than the instructed combination. This motivates training with counterfactual pairs formed by holding a demonstration observation fixed while changing the instruction to specify an undemonstrated combination. These pairs, however, lack corresponding demonstrated action targets. Crucially, the currently required skill has already been demonstrated, but actions from those executions cannot serve as direct targets because the same skill can require different actions across observations. We propose CRAFT, which transfers supervision from demonstrated executions of the required skill to counterfactual pairs using skill representations that can be reused across executions of the same skill. Across three VLA models and two simulation benchmarks, CRAFT improves success on undemonstrated combinations while maintaining high success on demonstrated ones; it also improves compositional generalization on a real robot. Project website: this https URL

---

## 7. ChunkVLA-AM: Parallel Action Chunking for Vision-Language-Action Robot Control in Additive Manufacturing

**Authors:** Zhugang Liu, Kaichuang Zhang, Jinman Zhang, ..., Qi Lu, Jinghao Yang
**arXiv:** [2610.01856](https://arxiv.org/abs/2610.01856)
**Categories:** Robotics (cs.RO)

Vision-language-action (VLA) models unify visual perception, language understanding, and action generation, offering new opportunities for automation in additive manufacturing (AM). However, deployment in AM remains challenging because adapting these models to unseen robot embodiments is costly, and performance can degrade under environment changes. In this work, we present a framework for deploying OpenVLA-OFT on a FAIRINO FR3 robot in a fixed AM workcell. A data pipeline converts monocular real-world demonstrations into OpenVLA-compatible TFDS/RLDS datasets to support adaptation to the FR3 embodiment. At runtime, each inference request predicts an eight-step chunk of 7-D actions. The FR3 executes each chunk open loop before capturing a new observation, providing closed-loop feedback between chunks. The system uses a cloud-edge architecture in which the FR3 client streams observations to a remote inference server through a FastAPI interface. In 42 physical A-to-B object-transfer trials, evenly split between red and blue targets, the system succeeded in 39 (92.9%). All three failures occurred during final placement, when insufficient release-height control caused the object to topple. An illumination sweep identified a low-error luminance range of 85-125 on a 0-255 scale, with the lowest mean spatial error at 95.

---

## 8. Is Success All You Need? Investigating the Impact of Input Perturbations on VLA Behaviour in Tabletop Manipulation Tasks

**Authors:** Sophie Higham, Riccardo Andrea Izzo, Matteo Matteucci, Alessandro Suglia
**arXiv:** [2610.01351](https://arxiv.org/abs/2610.01351)
**Categories:** Robotics (cs.RO)

Vision-Language-Action (VLA) models have achieved high task success rates on robot manipulation task benchmarks. More recently, there has been an emphasis on evaluating the robustness of VLA models to perturbations. However, this robustness is still predominantly measured through Task Success Rate (TSR). In this work, we propose a benchmark-agnostic evaluation framework to measure the behavioural robustness of models by characterising how successful trajectories are executed under perturbation. We implement this methodology by extending the widely-used LIBERO and LIBERO-Plus benchmarks. Across three state-of-the-art VLA models, four LIBERO task suites and seven perturbation conditions, we evaluate changes in both typical successful behaviour and its variability, including metrics of motion smoothness, efficiency and gripper behaviour. We find that perturbations can alter the behaviour of successful trajectories, a phenomenon which cannot necessarily be inferred from TSR alone. Across LIBERO suites, we identify cases where state-of-the-art VLA models achieve comparable TSR under the same perturbation condition, yet behaviour on successful trajectories diverges substantially. Therefore, to have a more robust assessment of task performance, we argue that suitable measures of robustness should capture not only whether a task is completed, but also how the robot behaves while completing it. When evaluating the robustness of VLA models, TSR may be complemented by behavioural evaluation metrics that characterise the nature and variability of successful task execution by robots.

---

## 9. WBAG: A Whole-Body and Attached-Geometry Safety Framework for Vision-Language-Action Manipulation

**Authors:** Samuel Zhen, Siwon Jo, Yanze Zhang, Wenhao Luo
**arXiv:** [2610.01083](https://arxiv.org/abs/2610.01083)
**Categories:** Robotics (cs.RO)

Vision-language-action (VLA) policies have demonstrated impressive capabilities in generalizable robotic manipulation, but their deployment in the real world remains challenging due to potential collisions involving different parts of the robot, manipulated objects, and the surrounding environment. Existing inference-time VLA safety frameworks typically rely on simplified end-effector-centered representations that do not explicitly model the full articulated robot and attached-object geometry. In this paper, we present WBAG, a safety framework that models the robot's whole-body and grasp-dependent attached geometry. WBAG constructs a grasp-conditioned safe set that adapts the protected geometry as objects are grasped, then converts this evolving geometry into differentiable CBF constraints that minimally modify the VLA's native six-dimensional operational-space action for collision avoidance across robot, scene, and attached geometry. On the SafeLIBERO benchmark, a variant of LIBERO augmented with obstacles for safety evaluation, WBAG achieves the best overall safety and safe task success among the evaluated methods under a scene-level safety evaluator that monitors all eligible non-task objects, reaching 97.38\% aggregate Scene Safety and 59.38\% Safe Success.

---

## 10. NarrativeFlow: Flow-Based Vision-Language-Action Model Using Robot Velocity Fields

**Authors:** Shota Kobayashi, Koki Seno, Daichi Yashima, Komei Sugiura
**arXiv:** [2610.00981](https://arxiv.org/abs/2610.00981)
**Categories:** Robotics (cs.RO); Computer Vision and Pattern Recognition (cs.CV)

We focus on language-conditioned flow-based manipulation, where robot flows (robot velocity fields) serve as embodiment-agnostic, motion-centric representations for leveraging data collected from multiple robot platforms. This task is crucial because language-conditioned manipulation is essential for practical robotic systems, yet scaling robot foundation models remains limited by the labor-intensive collection of embodiment-specific data. Existing methods either coarsely approximate robot flows with sparse keypoint displacements, or cannot handle language-conditioned manipulation. To address this limitation, we propose NarrativeFlow, which models robot flows as continuous velocity fields using a flow-matching formulation conditioned on language. Accordingly, NarrativeFlow generates robot flows that are physically consistent with real-world manipulation. To validate NarrativeFlow, we have conducted experiments on standard datasets for language-conditioned manipulation. The experimental results show that NarrativeFlow outperforms representative baseline methods on standard evaluation metrics. Furthermore, through real-world experiments, we show that NarrativeFlow achieves higher success rates than baseline methods across multiple manipulation tasks. The project page is available at this https URL

---

## 11. eRLT: Efficient VLA Reinforcement Learning via Action-Relevant Token Routing

**Authors:** Dehao Huang, Jianbang Liu, Jianpan Gao, ..., Yue Wang, Hong Zhang
**arXiv:** [2610.00913](https://arxiv.org/abs/2610.00913)
**Categories:** Robotics (cs.RO)

Vision-Language-Action (VLA) models provide strong behavioral priors for robotic manipulation, yet efficiently adapting them to downstream tasks remains challenging. Recent work addresses this challenge by adapting frozen VLAs through online reinforcement learning (RL), whose sample efficiency depends on the quality of the state representation used by the actor and critic. Existing methods construct such representations either with VLA-independent visual encoders or through fixed compression of internal VLA representations. Neither design explicitly extracts the task-specific action-relevant VLA features most useful for downstream action refinement and action-value estimation, therefore limiting sample efficiency. To address this limitation, we introduce eRLT, which constructs an effective state representation by routing task-specific action-relevant information across both tokens and layers of the frozen VLA. Specifically, learned routing tokens dynamically aggregate visual-language features at multiple depths, while a lightweight layer router combines these summaries into a fixed-dimensional RL token. The routing module is initialized using expert demonstrations to capture features predictive of expert actions and then refined using critic feedback from online interactions for action-value estimation. Across seven LIBERO and RoboTwin tasks, eRLT improves mean normalized learning-curve AUC by up to 23.7% over representative baselines. Real-robot experiments on USB connector insertion and motherboard ribbon-cable insertion further show AUC improvements of 108.9% and 46.7%, respectively, over the strongest baseline.

---

## 12. Continuous Conditioning of VLAs with Augmenting EMG and Visual Task Descriptors

**Authors:** Edward W. Staley, Connor O. Pyles, Rahul Hingorani, ..., Matthew S. Fifer, Michael Wolmetz
**arXiv:** [2610.01794](https://arxiv.org/abs/2610.01794)
**Categories:** Computer Vision and Pattern Recognition (cs.CV); Robotics (cs.RO)

Vision-Language-Action (VLA) models rely strongly on language for describing task information, despite having multimodal inputs. We hypothesize that other modalities in the state space may present opportunities for supplemental task conditioning, which may be particularly relevant in cluttered or otherwise ambiguous scenes. We introduce two tuned models to test this hypothesis: (1) an electrophysiology-conditioned VLA (EC-VLA) that incorporates 8-channel electromyography envelopes as continuous conditioning input concatenated to the proprioceptive vector, and (2) a visually-annotated VLA (VA-VLA) that incorporates visual segmentation annotations to the image inputs. On a cube-selection task evaluated across three participants, EC-VLA matches a language-prompted baseline in uncluttered, in-distribution conditions and substantially outperforms it in cluttered, out-of-distribution scenes. Similarly, VA-VLA shows modest improvements over a language-prompted baseline in in-distribution scenes with substantial improvement in cluttered, out-of-distribution trials. Together, these results provide strong evidence for the potential benefit of task-conditioning beyond language.

---

## 13. ATI-VLA: Action-Centric Predictive Vision-Language-Action Models via Actionable Alignment Then Adaptive Injection

**Authors:** Yijie Zhu, Rui Shao, Jie He, ..., Xiaojiang Peng, Zitong Yu
**arXiv:** [2610.01741](https://arxiv.org/abs/2610.01741)
**Categories:** Computer Vision and Pattern Recognition (cs.CV)

Predictive Vision-Language-Action (VLA) models aim to improve robotic manipulation via future observation or world dynamics forecasting. However, existing approaches often fail to realize this potential and underperform direct action prediction models. We argue that these limitations stem from modality misalignment between observations and actions, together with joint optimization conflicts that drive learning away from an action-centric objective. To this end, we introduce ATI-VLA, an Action-Centric Predictive Vision-Language-Action framework via Actionable Alignment Then Adaptive Injection. Specifically, it follows a two-step design: 1) Actionable Representation Alignment via a Shared Codebook. It aligns predictive observation and action representations by mapping both modalities into a shared discrete latent space via a unified codebook, making predictive observation latents readily usable for action generation and mitigating modality misalignment. 2) Action-Centric Adaptive Injection of Predictive Latents. Building upon this, it then injects predictive observation latents into action decoding as explicit predictive priors via a lightweight adaptive side-path, enabling adaptive predictive guidance under a single action-centric objective. Extensive experiments on both simulation and real-world robotic tasks demonstrate that ATI-VLA achieves state-of-the-art performance with faster convergence.

---
