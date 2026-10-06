# arXiv Daily Digest — 2026-09-21

**Mode:** direct
**Categories:** cs.AI, cs.LG, cs.RO, cs.CV
**Keywords:** VLA, RSI, agentic robot, self-improving robot, self-evolving robot, robot harness
**Papers found:** 13

---

## 1. Designer-RSI: Evolving Procedural Memory from User Traffic for Agentic Graphic Design

**Authors:** Hongyang Du, Lan Yan, Christian Flores, Asim Kadav
**arXiv:** [2609.22086](https://arxiv.org/abs/2609.22086)
**Categories:** Artificial Intelligence (cs.AI); Computer Vision and Pattern Recognition (cs.CV)

Professional graphic design is a long-horizon agentic task in which structured, editable artifacts emerge from many interdependent actions, yet outcomes admit no reliable programmatic oracle. We introduce a continual adaptation framework in which a frozen frontier model operates professional design software through more than 230 tools, while an external procedural memory of natural-language skills accumulates and refines reusable design procedures from experience. The memory widens by acquiring procedures for recurring uncovered subtasks and deepens by revising existing procedures against their own successful and failed executions, while a matched replay gate admits only changes that repair failures without regressing observed successes. Five rounds over 1,406 real user briefs and 1,869 automatically graded trajectories, with no weight updates and no human labels, grow the bank from 76 documentation-derived skills to 139 and raise GenEval2 execution success on Claude-Sonnet-4 from 72.7% to 99.3% (+11.99 points in generation quality), with 61.8% and 67.6% win rates against the no-skill agent across four specialized design benchmarks on Claude-Sonnet-4 and Claude-Opus-4.6. We further show the two mechanisms are effective in combination: on 200 held-out briefs from user-traffic benchmark, widening or deepening alone reaches a 49.4% / 48.6% win rate over the no-skill agent, while their combination reaches 58.5% (p = 0.025). Procedural memory offers a practical route to continual adaptation of agents under noisy, unverifiable feedback.

---

## 2. Outcome-Conditioned End-Effector Geometry Across Vision-Language-Action Policies

**Authors:** Xingyu Lin, Zhuang Li, Zhongrun Wu, Shouquan Zhou, Dehui Du
**arXiv:** [2609.21659](https://arxiv.org/abs/2609.21659)
**Categories:** Robotics (cs.RO); Artificial Intelligence (cs.AI)

Vision-language-action (VLA) policies solve the same manipulation task through different action interfaces, but task success alone does not establish whether their physical executions agree. We study cross-policy end-effector geometry in 15,000 closed-loop LIBERO rollouts from four policies. The primary clean-condition analysis forms 3,600 configuration-matched, and therefore dependent, policy pairs. Both-success pairs have a median normalized dynamic time warping distance of 0.0120 m versus 0.0380 m when exactly one policy succeeds. This ordering holds in every task, every policy pair, and nine sampling and band-limited representations; however, the ratio varies severalfold across representations, so we report the direction rather than a fixed multiple. Both-failure pairs are more separated again but rest on thin, uneven support, so we report them as exploratory. Within successful executions, partner replacements separate more across tasks than across initial states. A matched baseline still reveals measurable, heterogeneous residual policy differences, so a low cross-policy distance does not imply interchangeability. Successful executions sit about as far from same-task demonstrations as those demonstrations sit from each other, compatible with task-associated geometry without separating training-data overlap from task constraints. A common 72-action window preserves the ordering but reduces its magnitude; endpoint and duration adjustment likewise leaves a positive mixed-outcome coefficient relative to both-success pairs, though its magnitude is specification-dependent. Under composite visual stress, policy rankings and pair composition change together.

---

## 3. SynthDemo-RL: Breaking the Zero-Reward Barrier in VLA Adaptation with LLM-Guided Synthetic Demonstrations

**Authors:** Hiroaki Kingetsu, Hiroaki Kurihara, Kaoru Yokoo, Kenji Fukumizu, Manohar Kaul
**arXiv:** [2609.21650](https://arxiv.org/abs/2609.21650)
**Categories:** Robotics (cs.RO); Artificial Intelligence (cs.AI)

Fine-tuning Vision-Language-Action (VLA) models commonly relies on human teleoperation demonstrations, while reinforcement learning (RL) with sparse binary rewards faces an exploration challenge when successful trajectories are rarely sampled. We propose SynthDemo-RL, a teacher-student framework in which an automated teacher converts simulator-privileged state into successful manipulation trajectories, a VLA student is distilled from them by supervised fine-tuning (SFT), and PPO with binary task-success rewards refines the student. We study reward coverage, the fraction of tasks for which at least one success is observed under the fixed evaluation protocol, as a complement to the average success rate. On LIBERO-PRO, a public benchmark of perturbed LIBERO tasks for which no demonstrations exist, 27 of 57 scored tasks are at exactly 0% success for a pi_0.5 policy fine-tuned on the original LIBERO tasks. Direct PPO from this policy, under the same PPO recipe and the same RL compute as SynthDemo-RL's refinement stage, rescues 10 of these 27 tasks and leaves 17 at 0%. SynthDemo-RL, with 50 synthesized trajectories per task and no new human demonstrations, rescues all 27 and reaches average success rates of 97.8% and 97.1% on the Position and Task axes of LIBERO-PRO, respectively. On standard LIBERO, the same pipeline reaches 96.0% with no human demonstrations, within 1.7 points of pi_0.5 trained on 50 human demonstrations per task. We further validate the pipeline on RoboTwin 2.0 and verify that trajectories from a policy trained in a MuJoCo twin execute open-loop on a physical robot.

---

## 4. VLA-Scope: Shift-Aware Failure Prediction for Vision-Language-Action Models

**Authors:** Kaiwen Zhu, Dongfang Liu, Liangkai Liu
**arXiv:** [2609.21246](https://arxiv.org/abs/2609.21246)
**Categories:** Robotics (cs.RO); Artificial Intelligence (cs.AI); Computer Vision and Pattern Recognition (cs.CV); Systems and Control (eess.SY)

Vision-language-action (VLA) models map visual observations and natural-language instructions to robotic actions, but distribution shifts can compromise their reliability. Because these models may still succeed under out-of-distribution (OOD) conditions, detecting OOD inputs alone is insufficient to predict execution failure. In this paper, we introduce VLA-Scope, a two-stage framework that combines input-shift characterization with execution history to predict failure during OOD rollouts. The first stage uses pooled image and language representations to detect OOD inputs and classify their shift categories. For inputs flagged as OOD, the second stage combines the predicted category, action-prefix features, and execution progress features. A logistic regression model shared across shift categories updates failure risk as execution proceeds. We evaluate the framework with OpenVLA on ten LIBERO-Spatial tasks using leave-one-group-out cross-validation. OOD detection achieves a ROC-AUC of 0.9454, and shift classification achieves 91% accuracy. Evaluated independently of the OOD gate on all 1,400 OOD rollouts, the failure predictor achieves a ROC-AUC of 0.8497 after 60 executed actions, compared with 0.7906 without execution progress features. It also achieves a higher ROC-AUC than the evaluated ActProbe and SAFE-MLP baselines. These results suggest that combining action features with temporally aggregated execution step representations improves failure prediction under input shifts.

---

## 5. FOCAL-VLA: Subtask-Guided Geometry Distillation and Implicit World Modeling for Vision-Language-Action Models

**Authors:** Zhiyuan Gao, Di Wen, Yanxiang Zhan, ..., Kunyu Peng, Michael Beetz
**arXiv:** [2609.21228](https://arxiv.org/abs/2609.21228)
**Categories:** Robotics (cs.RO); Artificial Intelligence (cs.AI); Computer Vision and Pattern Recognition (cs.CV)

Vision-language-action (VLA) models built on pretrained vision-language models have demonstrated strong performance across diverse robotic manipulation tasks. However, VLA models that directly map current 2D observations to actions often lack sufficient spatial and temporal understanding, limiting their performance in precise and long-horizon manipulation. Recent methods enhance VLA models through geometric supervision and future-state prediction across the entire scene. However, these methods can suffer from redundant scene information, distracting the model from learning the geometry and dynamics relevant to the current interaction. To address this issue, we propose FOCAL-VLA, a framework that combines subtask-guided geometry distillation with implicit world modeling to learn representations of current spatial structure and future interaction dynamics. To focus geometric learning on the current subtask, we transfer geometric knowledge from VGGT to the VLA model by aligning geometry latents with features from subtask-relevant image regions. To capture the future 3D evolution of the current interaction, we incorporate implicit world modeling using Track4World features from current and future demonstration frames. The two complementary representations jointly guide action generation without running VGGT or Track4World at inference time. Experiments show that FOCAL-VLA outperforms baselines on both simulation benchmarks and real-world manipulation tasks. Project website: this https URL.

---

## 6. Fewer Steps, Better Actions: Rethinking Flow-Matching Inference for VLA Policies

**Authors:** Zhipeng Tang, Xinda Chen, Weining Rao, ..., Xiao Shi, Xiaofang Zhao
**arXiv:** [2609.21216](https://arxiv.org/abs/2609.21216)
**Categories:** Robotics (cs.RO); Artificial Intelligence (cs.AI)

Vision-language-action (VLA) policies based on flow matching generate action chunks through repeated evaluations of an action expert. Increasing the number of integration steps raises inference cost, but does not necessarily improve closed-loop success. We propose Coda, which reallocates part of this integration budget to a single learned endpoint correction. A frozen policy first completes a few-step noise-to-action trajectory; a lightweight Transformer then predicts a demonstration-supervised residual using the candidate action, source noise, and shared observation-prefix cache. Only the corrector is trained. On 50 RoboTwin Easy tasks, five-step Coda improves success from 71.64% to 74.68% over the matched five-step baseline, while reducing forward latency by 30.2% relative to the default ten-step policy. A two-step configuration achieves 71.88% success with a 2.12$\times$ speedup. An independent 13-task control shows a 5.69-percentage-point gain at nearly equal latency, supporting correction as an effective alternative to additional integration. The same design also improves frozen official SmolVLA, raising two-step success from 60.8% to 69.4%. These results show that endpoint correction improves the quality-latency trade-off of frozen flow-matching policies.

---

## 7. GALA: Geometry-Aware Latent Action Modeling for Vision-Language-Action Model Pretraining across Embodiments

**Authors:** Yichen Liu, Puzhen Yuan, Xiang Zhu, Yanjiang Guo, Jianyu Chen
**arXiv:** [2609.21948](https://arxiv.org/abs/2609.21948)
**Categories:** Robotics (cs.RO); Computer Vision and Pattern Recognition (cs.CV)

Learning large-scale vision-language-action (VLA) models from multi-embodiment datasets remains challenging due to heterogeneous action spaces across end effectors. Although latent action models (LAMs) can learn embodiment-agnostic action representations from diverse video data, existing image-based LAMs often fail to capture fine-grained end-effector articulation, particularly finger-level geometric changes in human and dexterous robot hands. To address this limitation, we propose GALA, a Geometry-Aware Latent-Action modeling framework that augments image-based latent actions with 3D end-effector geometric motion. However, naively incorporating point clouds yields fine-grained action representations with limited shared semantics, hindering cross-embodiment pretraining. To address this issue, we introduce the Unified End-effector Motion Representation (UEMR), which preserves fine-grained motion information while improving the cross-embodiment generalizability of latent actions. Building upon UEMR, GALA combines visual latent actions that capture scene-level dynamics with geometric latent actions that capture shared fine-grained end-effector articulation, providing effective supervision for VLA pretraining from multi-embodiment data, including action-free ego-centric human videos. Experiments on fine-grained motion probing, cross-embodiment retrieval, and downstream VLA evaluation demonstrate GALA's effectiveness in modeling generalizable fine-grained motions across embodiments, achieving 68.3% RoboCasa-GR1 success rate and 75.5% real-world success rate. Code, appendix, and demos are available at this https URL.

---

## 8. CommitFlow: Semantic Commitment Verification and Local Correction for Long-Horizon Robot Manipulation VLA Execution

**Authors:** Zixiang Zhao, Yansong Feng, Yang Yang, ..., Chuang Cheng, Jianjun Ma
**arXiv:** [2609.21908](https://arxiv.org/abs/2609.21908)
**Categories:** Robotics (cs.RO)

Although vision-language-action (VLA) policies have advanced rapidly, long-horizon execution may still progress to the next task stage before the required physical effect has been established. We call this a mismatch between semantic commitments, physical conditions that a stage must establish or maintain, and the actual physical state. Because an action command alone cannot confirm such a condition, local deviations can propagate and cause task failure. To address this problem, we present CommitFlow, a closed-loop execution framework that combines commitment monitoring with local correction while keeping the base policy frozen. CommitFlow integrates three components. A Semantic Commitment Monitor (SCM) compares stage requirements against current state evidence and holds back dependent actions when a required condition is unmet or violated. BoundaryFlow then generates a local correction conditioned on the current state and base action, and Relation and Gain Calibration (RGC) selects the smallest correction strength that satisfies the relevant constraints. Across the ten common RoboTwin 2.0 benchmark tasks, CommitFlow achieves a mean success rate of 75.9 percent, improving on the base policy pi0.5 by 22.7 percent. Cross-policy experiments show consistent gains, pointing toward reliable long-horizon robot execution.

---

## 9. A Sim-to-Real Integration Pipeline for Training and Deployment of Chunk-Based VLA Manipulation Policies

**Authors:** Mathilde Kappel, Clémence Grislain, Mohamed Chetouani, ..., Stéphane Doncieux, Mahdi Khoramshahi
**arXiv:** [2609.21817](https://arxiv.org/abs/2609.21817)
**Categories:** Robotics (cs.RO)

Vision-Language-Action (VLA) models have become a prominent paradigm for mapping multimodal inputs, including semantic instructions, visual observations of the scene, and proprioceptive observations, to robot actions. Most state-of-the-art models predict actions in the end-effector pose space as sequences of action chunks. Training and evaluating these models requires large-scale collections of real-world demonstrations, pairing robot actions with the corresponding visual and proprioceptive observations. Collecting such data on real hardware typically relies on human teleoperation, making the process costly, time-consuming, and difficult to scale. We present an open-source sim-to-real experimental protocol that addresses this bottleneck: expert trajectories generated in simulation are replayed open-loop on a real Franka FR3 setup, where the corresponding real visual and proprioceptive observations are recorded and converted into a format compatible with VLA training. The same deployment stack is then reused, in closed-loop, to evaluate a trained policy on that setup, so that data collection and evaluation share an identical hardware configuration. Because each real recording is paired with the simulated trajectory that produced it, the protocol also yields a direct measurement of the sim-to-real gap. We release the collected datasets on Hugging Face together with the pipeline source code this https URL.

---

## 10. FAN: Foresight Action Normalization for Continual Adaptation of Vision-Language-Action Models

**Authors:** Yijun Hong, Jiarun Zhu, Xiaoquan Sun, ..., Wenjun Zeng, Jiayu Chen
**arXiv:** [2609.21358](https://arxiv.org/abs/2609.21358)
**Categories:** Robotics (cs.RO)

Vision-Language-Action (VLA) models pre-trained on large-scale, closed datasets have demonstrated remarkable success across diverse robotic manipulation tasks. However, their long-term real-world deployment necessitates continuously acquiring new skills while retaining previously learned capabilities. While pioneering works have explored continual VLA adaptation using techniques such as experience replay and reinforcement fine-tuning, they overlook a foundational mechanism: action normalization, which determines the underlying coordinate system in which policies perceive and execute physical actions. To bridge this gap, we systematically evaluate five normalization strategies across four real-world task streams covering single-arm and bimanual manipulation. Our analysis reveals that existing protocols induce severe failure modes due to inter-task coordinate drift, limited motion coverage, or train-test coordinate mismatches. Motivated by these insights, we formulate three core design principles: consistency, coverage, and causality (3C), and introduce foresight action normalization (FAN). FAN estimates normalization statistics once from a small, task-independent calibration set prior to continual learning and freezes them throughout adaptation. Across all evaluated streams, FAN achieves the highest performance and demonstrates consistent robustness, providing insightful guidance for building stable action representations in achieving effective lifelong VLA adaptation.

---

## 11. Catch Me If You Can: Real-Time Feedback Denoising for Responsive VLAs

**Authors:** Yiheng Ji, Xingru Zhou, Luis Sentis, Mingyo Seo
**arXiv:** [2609.21022](https://arxiv.org/abs/2609.21022)
**Categories:** Robotics (cs.RO)

Vision-Language-Action (VLA) models have shown strong generalization in robotic manipulation by combining semantic knowledge from pretrained vision-language models with expressive action-generation policies. Diffusion-based action generators are particularly effective for modeling temporally coherent action chunks, but these chunks are typically executed open-loop after inference. This limits responsiveness when objects move, contacts change, or the scene evolves during execution. We propose VLA-Feedback, a two-timescale architecture that combines low-frequency diffusion planning with high-frequency visual feedback. Rather than fully denoising an action chunk before execution, VLA-Feedback retains its final denoising step as a lightweight feedback interface, allowing each action to be corrected using the latest observation before it is executed. This design preserves the expressiveness of the diffusion planner while enabling real-time action correction without rerunning the full vision-language diffusion model. VLA-Feedback matched GR00T on static LIBERO tasks while improving average success on dynamic simulation tasks from 27.5% to 85.0%. On real-robot tasks, it improved average success from 51% to 73%. Additional materials can be found on our project page: this https URL.

---

## 12. ForeTac-VLA: A Forecasting-Based Tactile-Vision-Language-Action Model for Contact-Rich Robotic Manipulation

**Authors:** Zhengyu Tao, Xin Li, Xin Wang
**arXiv:** [2609.20980](https://arxiv.org/abs/2609.20980)
**Categories:** Robotics (cs.RO)

Vision-language-action (VLA) models have demonstrated strong capabilities in robotic manipulation, yet their reliance on visual perception limits robustness in contact-rich environments, where critical physical interaction states may not be visually observable. Existing tactile-enhanced VLA methods improve physical grounding using observed tactile feedback, but most remain largely reactive rather than explicitly modeling how contact may evolve. Therefore, we propose ForeTac-VLA, a forecasting-based tactile-vision-language fusion model that predicts future tactile states to guide action generation. Specifically, ForeTac-VLA encodes recent tactile observations into temporal representations and integrates them with vision-language features through bidirectional cross-attention. Further, a transformer-based forecasting module predicts multi-step future tactile states, enabling the model to reason jointly over observed and anticipated contact. Finally, the fused multimodal representations and predicted future tactile states are fed into the VLA backbone to condition action generation. To stabilize training, a ground-truth-to-prediction curriculum is employed when early forecasts are unreliable. Across four real-world contact-rich manipulation tasks, ForeTac-VLA achieves an average success rate of 95%, outperforming the fine-tuned VLA model by 36.25 percentage points and state-of-the-art tactile-enhanced VLA baselines by over 22 percentage points. ForeTac-VLA also maintains strong performance under low-illumination and visually cluttered conditions. Video demonstrations can be found on this https URL

---

## 13. PRIME: Perception Feedback with Situational Memory Embeddings in VLA Models

**Authors:** Erik Deinzer, Naya Baslan, Luca Paparusso, ..., Peter Knott, Luigi Palmieri
**arXiv:** [2609.22040](https://arxiv.org/abs/2609.22040)
**Categories:** Computer Vision and Pattern Recognition (cs.CV); Robotics (cs.RO)

Current Vision-Language-Action (VLA) models for autonomous driving operate primarily through feedforward inference across the perception--reasoning--planning hierarchy. While modern architectures maintain temporal recurrence within the perceptual module, early perception remains blind to downstream reasoning and navigation goals, processing visual inputs agnostically without prioritizing cues informed by prior decisions. To bridge this gap, this paper introduces PRIME, a learned feedback mechanism that conditions the VLA perceptual queries on a novel Situational Memory. By aggregating latent representations of past perception, reasoning, navigation goals, and predicted behaviors across an L-step window via cross-attention, PRIME enables intent-driven perceptual attention at minimal computational cost, adding only a maximum of 29.7M parameters (0.41% of the 7.3B-parameter base model). Evaluated on the Bench2Drive closed-loop benchmark, PRIME achieves a state-of-the-art Driving Score of 82.47 (+4.73 over ORION) and a Success Rate of 60.00% (+5.38 percentage points), the highest reported Driving Score among published VLAs trained on Think2Drive demonstrations.

---
