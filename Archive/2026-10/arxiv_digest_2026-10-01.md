# arXiv Daily Digest — 2026-10-01

**Mode:** direct
**Categories:** cs.AI, cs.LG, cs.RO, cs.CV
**Keywords:** VLA, RSI, agentic robot, self-improving robot, self-evolving robot, robot harness
**Papers found:** 18

---

## 1. DynaHarness: A Dynamic Physical Harness for Self-Evolving Robot Agents

**Authors:** Haoyuan Deng, Jiebin Liu, Tengxiao Zhang, ..., Hongye Cao, Ziwei Wang
**arXiv:** [2609.40306](https://arxiv.org/abs/2609.40306)
**Categories:** Robotics (cs.RO); Artificial Intelligence (cs.AI); Machine Learning (cs.LG)

Pretrained robot policies provide useful action priors, but long-horizon manipulation still requires coordination between semantic reasoning and physical execution. Semantic reasoning operates at a coarser timescale than physical interaction, while episode-level failures provide limited guidance on which system component should be revised. We propose DynaHarness, a dynamic physical harness that couples semantic reasoning with physical governance through a shared execution contract and turns failure evidence into validated capability revisions. To be more specific, the slow brain proposes capabilities and symbolic arguments, while the fast brain grounds and monitors commands, refuses unresolved actions, substitutes capabilities, and requests replans when needed. The physical execution contract bounds each accepted command and records execution evidence across analytic skills, recovery skills, and the frozen VLA. Failure attribution localizes faults in these records and directs targeted revisions of reusable capabilities or execution mechanisms. Paired regression checks govern admission or rejection, closing the self-evolution loop. On LIBERO-Pro, DynaHarness achieves 75.2% on 800 newly sampled initial states, compared with 17.5% for the frozen policy. With the same capability library, full dynamic execution reaches 74.0% versus 63.9% under nominal one-step replanning. This demonstrates the value of DynaHarness as a dynamic physical harness that governs how existing capabilities are grounded, monitored, and coordinated during execution. Our project page is at this https URL.

---

## 2. Learning from Runtime Feedback through Failure-Bank Self-Evolution for Vision-Language-Action Models

**Authors:** Mingyue Cui, Zheyuan Liu, Yihan Zhu, Zheyuan Zhang, Meng Jiang
**arXiv:** [2609.39820](https://arxiv.org/abs/2609.39820)
**Categories:** Robotics (cs.RO); Artificial Intelligence (cs.AI)

Vision-language-action (VLA) models generalize broadly across robotic manipulation tasks, but complex environments require balancing task success with unintended contact. Runtime shields can correct individual actions, but they leave the underlying policy unchanged, so repeated disagreements may create a persistent policy-shield mismatch that blocks task progress. To address this challenge, we introduce FailBank, a four-stage self-evolving framework that converts runtime feedback into persistent policy improvement. During collection, a fixed CBF-based safety module serves as an observe-only teacher, producing counterfactual corrections while the policy remains in control. Outcome-aware admission then converts useful proposals into corrective targets and retains successful uncorrected actions as quiet anchors for guarded LoRA updates. We evaluate FailBank on the VLA-Arena benchmark across two difficulty levels and two VLA backbones. Compared with the base policies, FailBank improves the joint success-cost operating point. Across the two backbones, FailBank improves task success rate by 8.5 and 6.9 percentage points, while reducing policy-induced cumulative cost by 35.6\% and 23.8\%, respectively. Compared with runtime shielding, FailBank raises task success rate by 25.4 and 9.5 percentage points, while maintaining comparable policy-induced cumulative cost. These results show that runtime feedback can serve as persistent policy supervision rather than only as a temporary action constraint.

---

## 3. Blackout vs. Freeze: Analyzing Physical Failure Modes of VLAs under Camera Faults

**Authors:** Heejae Suh, Jongwook Han, Zahra Gholami, Yohan Jo
**arXiv:** [2609.39145](https://arxiv.org/abs/2609.39145)
**Categories:** Robotics (cs.RO); Artificial Intelligence (cs.AI)

Unreliable visual inputs can harm task performance and cause potential physical safety risks for vision-language-action (VLA) models. We analyze how $\pi 0.5$ and GR00T models act under input faults such as image blackouts and freezing. We find that blackout and freezing produce distinct physical failure modes even when task-success rates are similarly low: freezing causes more extreme joint behavior, whereas blackout after gripper closure can cause more object drops, most markedly without proprioception. Selective intervention studies reveal that proprioception (current robot state) partly compensates for the removed robot depictions and reduces non-target contact. However, it cannot sufficiently restore task success when wrist-view object information is removed, even when aided by the remaining scene view. We then evaluate two mitigation approaches: camera-blackout training and training-free replacement of faulty visual embeddings. Both improve task success in selected conditions, but can increase unintended contact or disturbance to surrounding objects. Real-robot trials further show that successful execution under camera faults can still involve unintended physical interactions. These findings motivate designing VLA policies that use the robot and object information still available under camera faults to limit hazardous motion.

---

## 4. Online Evolution Strategy for Flow-Matching VLA Policies via Self-Supervised Trajectory Distribution Optimization

**Authors:** Gongxin Yao, Yongsheng Zhao, Jiayin Deng, ..., Lei Zhao, Baoping Cheng
**arXiv:** [2609.38855](https://arxiv.org/abs/2609.38855)
**Categories:** Robotics (cs.RO); Artificial Intelligence (cs.AI); Systems and Control (eess.SY)

Vision-Language-Action (VLA) models based on generative frameworks, such as Flow Matching, have recently achieved impressive performance in robotic manipulation. Unlike deterministic policies, Flow Matching enables VLA models to learn conditional action trajectory distributions, where latent noise vectors induce different actions under the same task scenario. However, we observe that these distributions are often ill-formed, with successful and failed behaviors coexisting while considerable probability mass remains in unfavorable regions. To this end, we propose Online-ES, an online adaptation framework for Flow Matching VLAs based on Evolution Strategy (ES), which refines the learned action trajectory distribution through interaction feedback. Instead of pruning the latent noise space, our method performs evolutionary exploration directly in the action trajectory space, where diverse trajectories generated by Flow Matching provide candidate solutions for adaptation. By perturbing sampled trajectories and evaluating their execution outcomes, we derive a self-supervised MSE objective that transfers the evolution direction from trajectory space into model parameter space. Mathematically, we prove that the proposed objective provides an unbiased estimator of the optimal evolution direction. Moreover, we also incorporate failure experiences as negative feedback to regularize the evolution direction, steering the policy away from previously explored failure regions. Experiments in both simulation and real-world environments demonstrate that Online-ES achieves policy improvement comparable to reinforcement fine-tuning, without learning a value model or computing advantages.

---

## 5. CollabFlow: Recursive Self-Improvement of Agent Collaboration

**Authors:** Xiao Huang, Mingda Zhang, Junming Zhang, ..., Zijia Wang, Xiaoying Tang
**arXiv:** [2609.38662](https://arxiv.org/abs/2609.38662)
**Categories:** Multiagent Systems (cs.MA); Artificial Intelligence (cs.AI)

Recursive self-improvement (RSI) lets a system improve from its own outcomes; in LLM-based multi-agent systems, Agents refine one another within a task, and outcomes improve how they collaborate across tasks. However, existing multi-agent collaboration leaves this loop open: collaboration is pre-defined at the operator level, topology-only learning keeps verbatim exchange that propagates errors, and reward maximization on a system's own outcomes concentrates on a few teams. To address these challenges, we propose CollabFlow, an RSI system of Learned Agent Collaboration: a trainable Collab-Director constructs teams of complete Agents, a frozen executor runs them, and each round's outcomes retrain the director. Within each round, the edges of a collaboration graph carry protocols of Evidence-Conditioned Communication: a receiver adopts a differing answer only when the sender's evidence is stronger by a margin, so the director learns who communicates and how. Across rounds, we further propose Collaborative Trajectory Balance (CTB), a flow-based objective that credits each team once across its construction orders and targets a reward-proportional distribution over teams, so several good teams stay in play. We also bound how far this self-generated target moves between rounds, which shrinks as records accumulate. On twelve datasets, CollabFlow outperforms all baselines and keeps improving across rounds. Code is available at this https URL.

---

## 6. When Instructions Retrieve Trajectories: Diagnosing and Mitigating Generalization Failures in VLA Models

**Authors:** Hung-Jen Chen, Yu-Hsun Hou, Yan-Hong Chen, ..., Min Sun, Chun-Yi Lee
**arXiv:** [2609.39971](https://arxiv.org/abs/2609.39971)
**Categories:** Robotics (cs.RO); Machine Learning (cs.LG)

Vision-language-action (VLA) models can exceed 90% success on in-distribution tasks and withstand nuisance changes that preserve the required action, yet fail under counterfactual changes that demand a different action. Aggregate robustness scores can therefore conceal a more specific failure, in which a policy responds to both language and vision yet does not combine them to select the action the task requires. We call this failure instruction-action binding. Instructions cue familiar trajectory families, and visual feedback adjusts their execution. Behavioral analyses of fine-tuned $\pi_{0.5}$ and GR00T-N1.7 policies reveal that failed rollouts often retain the source behavior or switch to another demonstrated task. These switches show that language is not simply ignored. Readouts and interventions connect these choices to task-conditioned internal states. Our analysis of the imitation objective shows how narrow conditional action support can leave grounded and instruction-keyed solutions indistinguishable on the demonstrations. This motivates Equivariant Counterfactual Training (ECT), which acts at two levels. ECT data supply valid demonstrations in which the same instruction requires different actions in distinguishable scenes, while the ECT loss trains each demonstration with its counterpart in the same update. In a controlled LIBERO-PRO comparison, full ECT raises $\pi_{0.5}$'s mean position-swap success from 36% to 59%. On CALVIN, where counterparts already occur in the original data, the ECT loss improves five-task completion without new demonstrations. On a real UR5e under a fixed demonstration budget, full ECT raises unseen-position success from 8% to 88%.

---

## 7. MotionWeave: Learning Motion-Centered Future Dynamics for Vision-Language-Action Policies

**Authors:** Jingqiu Wang, Yan Wang
**arXiv:** [2609.39324](https://arxiv.org/abs/2609.39324)
**Categories:** Robotics (cs.RO); Computer Vision and Pattern Recognition (cs.CV); Machine Learning (cs.LG)

Vision-Language-Action (VLA) models have recently incorporated world models to provide richer dynamic supervision beyond sparse action labels. However, explicitly predicting future images or videos may include control-irrelevant appearance, while guidance derived from holistic future visual representations and shared global action features may fail to establish timestep-specific correspondence between actions and local visual changes. To address this issue, we propose MotionWeave, a motion-centric future-dynamics framework for action-chunk prediction with two modules: the Action-Induced Motion Grounder (AIMG) and the Horizon Residual Composer (HRC). Specifically, AIMG conditions on action and proprioceptive representations to construct horizon-specific queries that localize interaction regions associated with each future action timestep from current visual tokens. HRC extracts differences between interaction representations at adjacent horizons, encodes them as temporal motion cues, and injects them into action tokens through a gated residual. During training, robot-arm masks rendered from future frames are used to construct KL-based motion-grounding supervision, while inference uses only the current observation. On six MetaWorld tasks, MotionWeave achieves a 75.3% average success rate, an absolute gain of 8.6% over {\pi}0 (66.7%), especially on sustained-interaction tasks. Our code is available at this https URL.

---

## 8. RSIGame: Autonomous Agentic Game Development with Recursive Self-improvement

**Authors:** Wenyi Wu, Minghao Fu, Jieyu You, ..., Qi She, Biwei Huang
**arXiv:** [2609.39045](https://arxiv.org/abs/2609.39045)
**Categories:** Computation and Language (cs.CL); Computer Science and Game Theory (cs.GT); Machine Learning (cs.LG); Multiagent Systems (cs.MA)

Recent advances in large language models have made automatic game generation increasingly feasible, yet reliably improving generated games beyond a playable version remains challenging. Naive iterative refinement can easily overfit a small set of test cases, producing fragile games with unresolved bugs, missing behaviors, and poor generalization to broader player interactions. We introduce RSIGame, an autonomous agentic game development framework with recursive self-improvement. RSIGame organizes development into complementary local and global loops. Concretely, a local explore-diagnose-improve loop broadly explores the executable game, diagnoses and prioritizes discovered issues, and performs evidence-grounded revision, where an evolving checklist continually accumulates new testing and improvement guidance. A global loop tracks overall quality, preserves the best checkpoint, and detects saturation or regression over long-horizon development. Beyond test-time improvement, RSIGame further internalizes successful development experience into the generator through training. Across 140 GameCraft-Bench tasks, two game engines, and five generators, RSIGame consistently improves game quality under matched development budgets. Notably, experience internalization enables Qwen3.8-27B to reach 61.38 on Godot and 58.53 on Phaser, exceeding GPT-5.5 one-shot scores while reducing Qwen's generation tokens by 11 times.

---

## 9. Correcting WHERE, Preserving HOW: Compositional Generalization for Vision-Language-Action Models via Referential Guidance

**Authors:** Yanyan Zhang, Disheng Liu, Xinpeng Li, ..., Vipin Chaudhary, Yu Yin
**arXiv:** [2609.38616](https://arxiv.org/abs/2609.38616)
**Categories:** Robotics (cs.RO); Computer Vision and Pattern Recognition (cs.CV); Machine Learning (cs.LG)

While Vision-Language-Action (VLA) models enable flexible action generation, their generalization across diverse environmental elements, including manipulated objects, destinations, and backgrounds, is limited by the lack of diversity in robotic training data. Trained end-to-end on such data, VLAs tend to exploit visual shortcuts, associating actions with task-irrelevant visual features rather than the intended task semantics. These shortcuts block recomposition of elements already seen by the policy, that is, compositional generalization. Existing approaches mitigate such entanglement through task-relevant perception or targeted data diversification, but offer no explicit mechanism for unseen recomposition and require backbone-specific modifications with retraining. We observe that under such recomposition, VLAs often fail at global grounding while retaining local manipulation skills that recover near the correct target in familiar configurations. Therefore, we propose Referential Guidance (ReGuide), a training-free wrapper that, given object poses from a grounding module, combines semantic and geometric rebinding to guide the end-effector into demonstration-supported configurations of the instructed referent, where the frozen policy can resume execution. Experiments in simulation across multiple VLA backbones as well as on a real robot show that ReGuide improves success rates under compositional shifts by up to 56.8 and 75.0 percentage points, respectively, while preserving standard-task performance.

---

## 10. Multi-Link Safety Filtering for VLA Policies Around Moving Hazards

**Authors:** Yatharth Agarwal, Vijay Raghunathan
**arXiv:** [2609.40007](https://arxiv.org/abs/2609.40007)
**Categories:** Robotics (cs.RO); Computer Vision and Pattern Recognition (cs.CV)

A vision-language-action (VLA) policy can finish a manipulation task while knocking over objects unrelated to it, so task success alone does not show that the policy is safe to deploy in clutter. We study how to keep a pretrained VLA policy clear of such hazards at run time without retraining it, which requires guarding more of the arm than the end effector, following the hazard as it moves, and sharing onboard compute with the policy. Our training-free shield covers the gripper, wrist, and forearm with five ellipsoids and filters every commanded motion through one barrier program against a keep-out ellipsoid fitted from RGB-D perception at reset. Sparse optical flow then carries that ellipsoid's center along with the hazard, with no repeated detection or refitting. Over six simulated hazard-motion conditions, the shield lowers collision from $65.62\%$ to $27.27\%$ and raises safe-success, task completion without collision, from $29.35\%$ to $50.43\%$. Ablations show that guarding the arm links protects beyond end-effector shielding, and that tracking recovers most of the protection lost when the hazard estimate is frozen at reset. On heterogeneous edge hardware, the five-ellipsoid barrier runs on the CPU in $2.2$~ms at the 99th percentile, and trimming the vision--language prefix and taking fewer flow-matching steps shortens each $\pi_{0.5}$ policy call on the integrated GPU from $343$ to $177.3$~ms. On a physical SO-101 arm across four tasks, the arm touched the hazard in 3 of 16 shielded episodes versus 11 of 16 unshielded ones. Project page: this https URL

---

## 11. Toward Real-Time VLAs: Stage-Aware Two-Step Flow Denoising and System-Level Evaluation

**Authors:** Di Wu, Rongtian Shen, Ping Liu, ..., Jianglin Zhang, Tao Zhang
**arXiv:** [2609.39822](https://arxiv.org/abs/2609.39822)
**Categories:** Robotics (cs.RO)

Vision-language-action (VLA) models face a timing gap between low-rate inference and high-rate robot execution. We characterize this gap through end-to-end latency measurements of model inference and the robot execution chain. Repeated Flow Matching denoising contributes substantially to inference cost, while robot-side delays mainly arise from perception acquisition, communication scheduling, and physical response. Analysis of the velocity field shows relatively stable magnitude and direction in early integration, followed by stronger directional correction near the terminal steps. Based on this stage heterogeneity, we propose two-stage non-uniform denoising, reducing the number of steps from 10 to 2 and model-inference time from 61.557 ms to 21.956 ms. We also develop a distributed real-time VLA framework with independent inference, action-publication, and robot-control rates, modular observation acquisition, and action-provenance logging. Using {\pi}0.5 as the baseline, we evaluate six real-time execution methods on a long-horizon physical garment-folding task. Legato performs best overall among training-based methods, while Temporal Smoothing leads among training-free methods; both perform strongly in task success, completion time, action continuity, and acceleration smoothness. Combining two-step denoising with representative execution methods substantially reduces inference cost with a small reduction in task performance. These results motivate joint optimization of model-inference efficiency and robot-system timing.

---

## 12. From Local Whole-Body VLA Behaviors to Scene-Scale Aerial Manipulation

**Authors:** Weixiang Guo, Rui Jin, Haotian Jin, ..., Kun Cao, Lihua Xie
**arXiv:** [2609.39670](https://arxiv.org/abs/2609.39670)
**Categories:** Robotics (cs.RO)

Vision-language-action (VLA) models enable task-conditioned interaction, but extending them to scene-scale aerial manipulation remains challenging due to costly whole-body demonstrations, latency-induced action-state misalignment, and cross-site behavior composition. We present a unified framework for synthetic policy training and scene-scale execution on articulated uncrewed aerial manipulators (UAMs). A scene-reconfigurable pipeline synthesizes task-conditioned, kinodynamically feasible trajectories and synchronized multiview observations for VLA training without physical-platform demonstrations. Measured-progress-aligned realization (MPAR) aligns asynchronously returned action chunks with measured execution progress and realizes them as continuous, dynamically feasible trajectories. A relational Scene Graph grounds language goals to object instances and feasible interaction regions, while topology-guided transfer connects local behaviors across sites. Local VLA skills achieve 39/60 successes (65.0%) in simulation under oracle target and feasible-handoff conditions. Under 500-ms added latency, with and without a transient command-update stall, MPAR reduces median takeover phase error by 0.212 s over nominal-time alignment. The complete system completes 21/50 simulated multi-site missions (42.0%) and is further validated on a physical articulated UAM.

---

## 13. DSDyn-VLA: A Dual-Stream Dynamic Manipulation Framework with Motion Perception, Future Awareness, and Realtime Correction

**Authors:** Wenhao Li, Xiu Su, Yu Han, ..., Shan You, Chang Xu
**arXiv:** [2609.39198](https://arxiv.org/abs/2609.39198)
**Categories:** Robotics (cs.RO)

While Vision-Language-Action (VLA) models excel in static tasks, they struggle in dynamic environments where objects are in motion (e.g., conveyor belt manipulation). We identify three fundamental limitations hindering current VLAs in these scenarios: the \textbf{perception gap}, where static visual inputs lack temporal motion cues; the \textbf{latency gap}, where inference delays render actions obsolete; and the \textbf{control gap}, caused by the open-loop action chunk execution without real-time adjustment. In this work, we propose \textbf{DSDyn-VLA}, a Slow-Fast \textbf{D}ual-\textbf{S}tream \textbf{Dyn}amic manipulation framework that integrates motion-aware foresighted planning with real-time residual correction. The slow \textbf{Flow-Planner} serves as a macro-planner. By enhancing the VLA with optical flow for temporal perception and a future state awareness mechanism to preemptively offset inference latency, it produces globally consistent, motion-aware action chunks. Complementing this, the fast \textbf{Res-Refiner} employs a lightweight RL policy to inject high-frequency, closed-loop corrections into the planned action chunks based on real-time observations. In addition, we introduce \textbf{DynBench}, a MuJoCo-based benchmark for dynamic object manipulation that comprises nine tasks. Extensive experiments demonstrate that DSDyn-VLA reduces the failure rate by over 76\% compared to current SOTA method in high-latency setting on the Kinetix dynamic benchmark, while achieving about 6$\times$ the success rate of PI0.5 in real-world dynamic settings and about 5$\times$ on DynBench. We will open-source all the code and weights.

---

## 14. Exploiting Vulnerabilities: Universal Adversarial Attacks on Vision-Language-Action Models in Robotics

**Authors:** Songhua Yang, Ziyu Liu, Yuanwei Liu, ..., Zheng Wang, Miao Li
**arXiv:** [2609.39178](https://arxiv.org/abs/2609.39178)
**Categories:** Robotics (cs.RO); Cryptography and Security (cs.CR); Computer Vision and Pattern Recognition (cs.CV)

Recently, Vision-Language-Action (VLA) models have revolutionized robotic manipulation by seamlessly integrating visual perception, language understanding, and action generation in an end-to-end learning framework. However, since these models are designed to interact directly with the physical world and humans, their security is critical, and even small vulnerabilities can lead to catastrophic failures. In this work, we propose the Universal Adversarial Object, a sphere with optimized surface texture that significantly degrades task success rates when placed within the robot's field of view. Specifically, our approach introduces a multi-level attack framework that jointly disrupts trajectory planning, task execution, and action control. We validate our method in both simulated and real-world robotic settings. Experimental results demonstrate that the adversarial object reduces the average task success rates by 31.2%-39.9% for two representative VLA models (Pi0 and RDT), with success rates dropping to near zero in complex scenarios. Index Terms--Vision-Language-Action models, adversarial attack, robotic security, universal adversarial object

---

## 15. EmbodiRSI: Recursive Self-Improvement for Data-Efficient Robot Adaptation

**Authors:** Haoran Lang, Haotao Lu, Shiyu Sang, ..., Ye Shi, Jingya Wang
**arXiv:** [2609.38905](https://arxiv.org/abs/2609.38905)
**Categories:** Robotics (cs.RO)

Adapting robot manipulation policies to new tasks and environments remains highly data-intensive, while the data needed for further improvement depends on the policy's current capabilities and failure modes. We introduce EmbodiRSI, an agentic system for recursive self-improvement (RSI) in a real-to-sim-to-real setting, where task-specific simulations are constructed from target deployment scenarios and used as low-cost environments for iterative policy improvement before transfer back to the physical world. EmbodiRSI uses policy execution feedback to guide subsequent experience acquisition and policy updates. Two complementary mechanisms close this loop: Collaborative Error Correction generates agent-assisted corrective trajectories from policy-reached states, while Adaptive Data Collection directs expert demonstration generation toward the current policy's weaknesses. The task-specific simulation serves as a reusable workspace for policy warm-up, repeatable evaluation, failure diagnosis, and targeted data generation across successive RSI rounds. Across three tabletop environments and 14 subtasks, EmbodiRSI increases scene-balanced autonomous simulation success from 50.4% to 83.5% over two RSI updates. With 400 adaptive simulated trajectories and only ten real-world refinement trajectories per subtask, EmbodiRSI achieves 83.1% scene-balanced autonomous real-world success, compared with 75.0% for adaptation using 200 real-world demonstrations per subtask. These results demonstrate that feedback-driven recursive improvement in deployment-specific simulations can enable data-efficient adaptation of embodied policies to physical environments.

---

## 16. Data-Efficient Adaptation of a Driving VLA to Class 8 Trucks

**Authors:** Satyajeet Das, Aaron Buxbaum, Niels Joubert, Gaurav S. Sukhatme
**arXiv:** [2609.38570](https://arxiv.org/abs/2609.38570)
**Categories:** Robotics (cs.RO)

Class 8 trucks differ from passenger cars in geometry, dynamics, and maneuvering requirements. As a result, vision-language-action (VLA) models trained for passenger vehicles do not readily transfer to Class 8 trucks, particularly in unstructured scenarios such as accident scenes and construction zones. Rather than training a truck-driving VLA from scratch, we propose an adapt-then-steer strategy that adapts an off-the-shelf VLA to generate trajectories for Class-8 trucks in these challenging scenarios. In the adapt stage, we use NVIDIA's Alpamayo 1.5 as the base model, fine-tuning only its action-generation stack on a few hundred real-world construction and accident-related highway scenarios. In the steer stage, we introduce Flow Velocity Steering (FVS) to further refine the model's predictions while holding the adapted VLA fixed. FVS is a compact, flow-time-conditioned residual module that adds learned corrections to the action-space flow velocity used to update the action sequence at each generation step. In open-loop evaluation on a scenario-disjoint held-out set, targeted fine-tuning more than halves single-candidate average displacement error (ADE) and final displacement error (FDE) over the entire 6.4 s horizon compared to the base model. Using the same targeted demonstrations, FVS further reduces the fine-tuned model's full-horizon ADE and FDE by 13.9% and 16.5%, respectively. At matched data budgets, targeted supervision yields 19-26% lower full-horizon ADE than general truck-driving supervision, while the targeted model remains competitive with a model fine-tuned on approximately 65 times as many general truck-driving scenarios. These results support adapt-then-steer for data-efficient vehicle-domain transfer to Class 8 trucks. Our project website is available at this https URL.

---

## 17. Inline Memory Meets Reusable Skills: Memory-centric Framework for Vision-Language-Action Model

**Authors:** Zaijing Li, Rui Shao, Bing Hu, ..., Dongmei Jiang, Liqiang Nie
**arXiv:** [2609.39794](https://arxiv.org/abs/2609.39794)
**Categories:** Computer Vision and Pattern Recognition (cs.CV); Robotics (cs.RO)

Vision-Language-Action (VLA) models have shown strong promise for general-purpose robotic manipulation, yet adapting them to new tasks and domains remains inefficient: existing methods often rely on parameter tuning, incurring substantial costs and risking catastrophic forgetting of previously learned tasks. To address this, we propose \textbf{Optimus-R}, a memory-centric VLA framework that formulates robotic adaptation as explicit query-skill memory tuning. Optimus-R introduces: (i) An \textbf{Inline Memory Interface for skill extraction}. It inserts learnable memory tokens into the VLA prefix stream, allowing the backbone to derive control-aware query and skill representations within the native action-conditioning pathway. (ii) A \textbf{Query-Skill Memory Bank for skill learning}. It externalizes skills into query prototypes for deciding \emph{what} to retrieve and skill values for specifying \emph{how} to act, supporting skill reuse and expansion with limited parameter updates. (iii) A lightweight \textbf{Bridge-and-Adapt mechanism for skill updating}. It aligns target-domain queries and skills with the existing memory space through a lightweight adapter and residual memory updates. Experiments on in-domain adaptation, cross-domain adaptation, and lifelong learning show that Optimus-R enables data-efficient skill learning while mitigating catastrophic forgetting.

---

## 18. Vision-Language-Action Autonomous Driving Agent with Language-based Memory

**Authors:** Kai Yan, Xiangyu Chen, Yulong Cao, ..., Wenjie Luo, Marco Pavone
**arXiv:** [2609.38641](https://arxiv.org/abs/2609.38641)
**Categories:** Computer Vision and Pattern Recognition (cs.CV); Robotics (cs.RO)

Vision-Language-Action (VLA) foundation models have recently emerged as one of the prevailing solutions for autonomous driving, as they can utilize knowledge acquired during vision-language pretraining for accurate and interpretable driving. However, VLAs can take only a limited number of frames as visual input due to the high token cost of an image, which is problematic for memory-dependent tasks such as determining the arrival order at all-way stops and long-horizon driving scene understanding. Existing solutions use latent vector memories accessed through cross-attention, which are neither interpretable nor portable. In this paper, we propose AD-Memo, a general-purpose VLA driving agent with language-based memory. The agent outputs memory as an extension of its Chain-of-Thought (CoT) to record surrounding objects critical to driving; this memory becomes part of the agent's future input. We curate memory-based datasets and train VLAs with a two-stage recipe: Supervised Fine-Tuning (SFT) and \textit{Da Capo}, a novel semi-closed-loop Reinforcement Learning (RL) algorithm which uses trajectory-level advantage for memory and step-level advantage for driving, leading to better credit assignment. Across scenarios such as all-way stops and general driving, AD-Memo improves driving quality, enables better question answering on driving scenes, and produces plug-and-play memory for other models.

---
