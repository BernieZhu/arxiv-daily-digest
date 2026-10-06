# arXiv Daily Digest — 2026-09-22

**Mode:** direct
**Categories:** cs.AI, cs.LG, cs.RO, cs.CV
**Keywords:** VLA, RSI, agentic robot, self-improving robot, self-evolving robot, robot harness
**Papers found:** 30

---

## 1. MedRSI: Recursive Self-Improvement for Medical Agents via Clinically Aligned Self-Evolution

**Authors:** Junde Wu, Jiayuan Zhu, Minghao Hu, Fenglin Liu, Jiazhen Pan
**arXiv:** [2609.24838](https://arxiv.org/abs/2609.24838)
**Categories:** Artificial Intelligence (cs.AI)

Medical agents increasingly combine general reasoning models with specialized clinical tools, yet their capabilities remain largely fixed by what clinicians and engineers design before deployment. Recursive self-improvement (RSI) offers a different paradigm in which agents learn from their own failures and autonomously expand their capabilities, but directly applying RSI to medicine introduces fundamental safety challenges. We introduce MedRSI, the first recursive self-improvement framework for medicine, which continuously transforms diagnostic failures into new clinical capabilities through tool composition and task-specific model training. Inspired by clinical practice, MedRSI introduces two mechanisms for clinically aligned self-evolution. Clinical-cost-aware failure prioritization directs improvement toward errors according to their potential clinical consequences rather than frequency alone. Fast discovery with slow registration separates rapid capability invention from conservative adoption, allowing new tools to enter the persistent agent only after demonstrating sustained benefit across subsequent patient cohorts. Across public glaucoma and heart disease benchmarks and two private clinical tasks, MedRSI progressively develops segmentation, measurement, prediction, multimodal reasoning, and generative capabilities, surpasses manually engineered medical agents, and autonomously discovers solutions to clinical problems not anticipated by its original designers. Our results show that medical agents need not remain constrained by capabilities specified before deployment: with clinically grounded mechanisms governing what to improve and what to retain, they can continuously construct, validate, and accumulate new capabilities from diagnostic experience. Code is available at this https URL.

---

## 2. RRSI: Regularized Recursive Self-Improvement of Agent Harnesses

**Authors:** Peng Xia, Rujun Han, Zifeng Wang, ..., Tomas Pfister, Chen-Yu Lee
**arXiv:** [2609.24972](https://arxiv.org/abs/2609.24972)
**Categories:** Machine Learning (cs.LG); Artificial Intelligence (cs.AI); Computation and Language (cs.CL)

An LLM agent's capability is largely magnified by its harness, namely the prompts, control flow, tooling, memory, and context management surrounding the frozen backbone model. Recent methods increasingly automate this process by iteratively proposing and selecting component-wise edits of an agent harness, practically establishing a form of recursive self-improvement (RSI) at the agent-system level. However, such recursive evolution may overfit by memorizing the training tasks, showing large in-distribution gains that shrink or even vanish on out-of-distribution benchmarks. We introduce Regularized Recursive Self-Improvement of Agent Harnesses (RRSI), which incorporates the principles of regularizations into harness self-improvement by constraining the evolution candidate proposal and selection. The proposer operates with a temporally annealed budget, limiting how many edits a candidate can bundle, and it encourages unexplored trajectories based on evolution history. The selector is equipped with a critic and a pruner: the critic screens benchmark-specific proposals, while the pruner, removes changes that are too small, too expensive, or no longer useful. Together these constraints favor reusable agent mechanisms over benchmark-specific ones or even noises. Across eight benchmarks spanning coding, agentic workspace and engineering design tasks, RRSI gains up to 14.1 points on the split it evolves against and up to 4.7 points on the five out-of-distribution benchmarks, while producing a harness that runs on 30% fewer policy tokens than the unregularized evolution. Code is available at this https URL and project page is this https URL.

---

## 3. FoldQuantVLA: Native Low-Bit Quantization of Vision-Language-Action Models via Consistent Folding

**Authors:** Hung T. Ho, Khanh D. Nguyen, Quang D. Nguyen, ..., Vien A. Ngo, An T. Le
**arXiv:** [2609.24433](https://arxiv.org/abs/2609.24433)
**Categories:** Robotics (cs.RO); Artificial Intelligence (cs.AI); Systems and Control (eess.SY)

Low-bit vision-language-action inference must reduce observation-to-action latency while preserving robot behavior. We present FoldQuantVLA, a post-training quantization framework that carries a consistent activation representation through calibration, weight rounding, and native integer execution. It combines channel scaling and block Hadamard transforms with dynamic per-token quantization, without policy retraining. Custom TensorRT plugins execute projections in both the language backbone and iterative action expert with four-bit weights and activations (W4A4) on Ada GPUs and Jetson AGX Orin. Evaluation spans LIBERO, SimplerEnv, and two robot platforms. Across three GR00T checkpoints and $\pi_{0.5}$, W4A4 achieves $1.20$ to $1.33\times$ speedups over floating-point TensorRT on Orin and $1.25$ to $1.52\times$ on desktop. Retaining language attention-output and feed-forward down projections at eight bits (W8A8) improves held-out action fidelity on all four checkpoints. Across four real-robot tasks, this configuration raises observed GR00T N1.7 success from $80.0\%$ with uniform W4A4 to $92.5\%$ over 80 trials per configuration, with a measured additional Orin latency of 1 ms.

---

## 4. ReVeal: A Reconstruction-Aware Real-to-Sim Framework for VLA Policy Evaluation

**Authors:** Xinyi Wang, Heng Hao, Wenjun Hu, ..., Hankyu Moon, Yeong-Dae Kwon
**arXiv:** [2609.23910](https://arxiv.org/abs/2609.23910)
**Categories:** Robotics (cs.RO); Artificial Intelligence (cs.AI)

Simulation-based evaluation provides a scalable and repeatable alternative to real-world evaluation of vision-language-action (VLA) policies. However, reconstruction errors can cause simulated policy performance to diverge from real-world performance, motivating the need to assess reconstructed environments for downstream VLA policy evaluation. We present ReVeal, a real-to-sim assessment framework combining workspace reconstruction, reconstruction-level assessment, and matched closed-loop policy evaluation. Novel-View Mesh Fidelity (NVMF) and Annotated Planar Geometry Fidelity (APGF) assess observation and planar geometric fidelity, respectively. We also develop PGSR-D, a reconstruction pipeline incorporating monocular depth supervision to improve geometry where multi-view visual cues are limited. Across 8 assessment scenes, NVMF and APGF consistently distinguish the fidelity of 2DGS, PGSR, and PGSR-D. Matched evaluations of GR00T, SmolVLA, and pi0.5 across 8 humanoid manipulation tasks show consistent ordering between reconstruction fidelity and real-sim performance agreement across pipelines. Further analysis of the evaluation workspaces shows that higher fidelity is associated with stronger real-sim agreement.

---

## 5. MaskVLA: Visual Masking Against Trajectory Overfitting of Vision-Language-Action Model

**Authors:** Yuxuan Jiang, Jiaying Huang, Ge Wang, ..., Yatong Han, Zhen Li
**arXiv:** [2609.23565](https://arxiv.org/abs/2609.23565)
**Categories:** Computer Vision and Pattern Recognition (cs.CV); Artificial Intelligence (cs.AI); Robotics (cs.RO)

Vision-Language-Action (VLA) models integrate vision-language understanding with executable robot actions, enabling end-to-end learning for robot control. However, our empirical analysis reveals that existing models exhibit severe trajectory overfitting when finetuned on limited datasets. To guide the model in effectively utilizing wrist camera information, we propose MaskVLA, a masking-based fine-tuning strategy. By randomly masking a small portion of the main camera's visual information, the model is guided to autonomously learn more fine-grained, task-relevant, and effective visual features. This process leads to the emergence of robust policies, thereby enhancing the model's capability to tackle complex manipulation tasks and improving its generalization performance. Our method has been comprehensively evaluated on RoboTwin 2.0, achieving an average success rate improvement of 23.2% and 16.8% compared to $\pi_0$ and OpenVLA-OFT, respectively. Furthermore, experiments on real-world ALOHA robots also demonstrate the effectiveness of our approach.

---

## 6. Beyond the Leaderboard: Counterfactual Diagnosis of End-to-End and VLA Driving Policies Under Domain Shift

**Authors:** Ruolin Yang, Zilin Huang, Buoyue Wang, ..., Zihao Sheng, Sikai Chen
**arXiv:** [2609.22582](https://arxiv.org/abs/2609.22582)
**Categories:** Computer Vision and Pattern Recognition (cs.CV); Artificial Intelligence (cs.AI)

End-to-end and vision-language-action (VLA) driving policies are compared by leaderboard rank, but a rank reports an outcome, not the behaviour behind it, so it predicts poorly how a policy will behave at a new site. On six released policies, rank on nuScenes open-loop error or on NAVSIM's leaderboard does not carry over to scenes with a pedestrian near the ego corridor at a new site. We propose a counterfactual check-up: a few hundred real frames, each edited two ways (pedestrian removed, or re-lit by a night-style perturbation), every edit verified by an independent detector, and the change in the planned trajectory read as a diagnosis rather than a score. From these edits two causal axes are read, and five exams built on them separate what a score merges: how far the policy plans to drive, whether seeing the pedestrian buys safety, whether that response scales with danger, whether the plan moves when nothing requires it, and how much an irrelevant lighting change moves it. On 246 NAVSIM near-pedestrian scenes, in the cells where the pedestrian lies on the planned path only 1.9% of responses are genuine avoidance, and under our open-loop protocol the median clearance change is at most 0.03 m and the median change in planned distance at most 0.08 m for every policy. In a pre-registered test from left- to right-hand drive, the exposure and specificity orderings, the lighting verdict and the collision outcome transfer, while point values and the hazard-sensitivity verdict do not. Read as a selection report, the profiles say which policy is safe because it plans short, which covers a human-like distance without yielding, and which is unsteady under a change that requires no reaction, and they price each verdict: most settle within a few dozen frames, hazard sensitivity needs hundreds. Code and edited frames will be released.

---

## 7. Validating, Not Sampling: Region-Level Robustness of Vision-Language and Vision-Language-Action Models

**Authors:** Bogdan Aron, Christopher Brix, Benedikt Brückner, ..., Panagiotis Kouvaros, Alessio Lomuscio
**arXiv:** [2609.22293](https://arxiv.org/abs/2609.22293)
**Categories:** Computer Vision and Pattern Recognition (cs.CV); Artificial Intelligence (cs.AI)

Vision-language models (VLMs) and vision-language-action models (VLAs) are increasingly deployed in real-world applications. There, a small perturbation to the recorded camera image may change a decision significantly. However, existing benchmarks for these models only sample perturbations, which does not guarantee the absence of a failure in the untested region. We present the first robustness validation of six VLMs (drawn from the Gemma, InternVL, LLaVA, and Qwen families) and five VLAs (drawn from the GR00T, OpenVLA, and $\pi$ families) over entire continuous regions of photometric and geometric image perturbation: brightness shifts, camera rotations, and their composition. To this end, we build on the validation framework H$^2$V and introduce H$^2$V-M, a margin-aware convergence rule that makes validation affordable at the 32B parameter scale. We demonstrate that H$^2$V-M outperforms H$^2$V by an order of magnitude in model queries and that it finds counterexamples faster than random sampling while providing soundness guarantees. Our VLM and VLA robustness validation shows that robustness is mostly dependent on the perturbation type, rather than the model, and that VLMs are more robust to large camera rotations than VLAs. For VLAs, even perturbations as small as $\pm1^\circ$ can change the commanded action in many cases. We also show that robustness depends more on model family than on model size.

---

## 8. Prioritized Rollouts for Efficient World Model-based Vision-Language-Action Policy Optimization

**Authors:** Yifei Sheng, Haoxiang Ren, Zhilong Zhang, ..., Haoxin Lin, Yang Yu
**arXiv:** [2609.22879](https://arxiv.org/abs/2609.22879)
**Categories:** Machine Learning (cs.LG)

Vision-Language-Action (VLA) models have emerged as a powerful paradigm for embodied intelligence, but fine-tuning them with reinforcement learning (RL) remains constrained by the cost of real-world robot interaction. Model-based reinforcement learning (MBRL) reduces this cost by using a learned world model to generate rollouts for policy optimization. However, it becomes computationally expensive as VLA policies and world models scale. Existing methods typically treat states equally, overlooking substantial differences in their utility for policy improvement. In this paper, we show that policy uncertainty helps identify states with greater potential for policy improvement. The policy exhibits high uncertainty at only a small subset of states, often during decision-sensitive stages where small action differences can alter task outcomes, suggesting that policy improvements at these states could be particularly valuable. Building on these findings, we introduce U-GROW, a lightweight, plug-and-play sampling layer that directs more model rollouts to these informative states. By modifying only the branched-start distribution, U-GROW can be integrated into existing MBRL pipelines without changing the policy optimization objective. Experiments in both simulated and real-world manipulation tasks demonstrate the efficiency and effectiveness of U-GROW, supporting the use of policy uncertainty to guide experience generation.

---

## 9. Beyond Appearance Shifts: Task-Semantic Action Calibration for VLA Models

**Authors:** Shuaijun Liu, Feiyang You, Chengyu Wu, ..., Xingwei Chen, Ningxin Su
**arXiv:** [2609.23650](https://arxiv.org/abs/2609.23650)
**Categories:** Robotics (cs.RO); Machine Learning (cs.LG)

Vision-language-action (VLA) models have achieved strong performance in embodied manipulation, but still lack a clear mechanism to balance behavioral stability with task-semantic sensitivity. We identify two complementary failure modes. Under task-preserving changes, where task semantics remain unchanged but scene appearance varies (e.g., style, illumination, clutter, or paraphrasing), policies often exhibit unnecessary action drift. Conversely, under semantic-breaking changes, where key task semantics such as the target object or constraint are altered, policies frequently fail to produce sufficiently distinct behaviors and instead follow the original trajectory. To address this gap, we propose BAS-VLA, a task-semantic action calibration framework built on top of a frozen base VLA. BAS-VLA adopts a breaking-centered calibration core as the default path, and introduces a selective evidence-gated preserving auxiliary that activates only when nuisance variation is detected while task semantics remain consistent. On the OpenPI-pi0.5 / LIBERO-Object Milk-Swap benchmark, BAS-VLA maintains high success on clean (98.0%) and semantics-preserving conditions (97.5%), while reducing clean-criterion success to 0.0% under deliberate target-object swaps, demonstrating strong stale-task suppression and task-semantic separation. On validated style-preserving shifts, it improves success from 42% to 70% without degrading clean performance. These results highlight that reliable VLA behavior requires moving beyond appearance robustness toward explicit task-semantic action calibration.

---

## 10. Anatomy of a Closed-Loop Collapse: A Causal Case Study of a Compressed VLA Policy

**Authors:** Fengze Jia
**arXiv:** [2609.23048](https://arxiv.org/abs/2609.23048)
**Categories:** Robotics (cs.RO); Machine Learning (cs.LG)

Compressed manipulation policies can pass offline evaluation while failing in closed-loop execution; this dissociation is established in prior work and is not our claim. We contribute a causal anatomy of one naturally occurring case. An 8-layer distillation of Octo-Base retains 86% of parameters, passes every offline check we applied (0.996 and 1.000 teacher-ratios on the family's own validation metrics), and collapses in closed loop: 0/72 vs. the teacher's 40/72 on a simulated WidowX pick-and-place task. The collapse is structured, not diffuse: early task stages degrade gradually (the student moves the object at 90% of the teacher's rate and grasps at 55%), while transport-to-target fails categorically, at 0% in every training variant. Paired action-trace forensics isolate the signature: a negative, late-heavy $z$ residual, roughly 10x its post-repair magnitude, and persistent across the base distillation and both continuation branches. Four standard therapies fail under matched controls: continued training and in-domain offline data leave success at zero, even though the latter measurably improves marginal action statistics; command-level compensation recovers nothing at any offset, although the same perturbations degrade healthy policies; clamping the symptom in the command channel preserves grasping, yet success stays at floor. A minimal-pair intervention that substitutes half of the training stream with deployment-distribution teacher rollouts, with every other setting held fixed, restores parity with the teacher (18/36 vs. 17/36 held-out), eliminates that signature, and recovers a teacher-like perturbation-response profile. We claim existence, not universality. Operationally, offline gates, including a family's own validation metrics, are insufficient acceptance tests for compressed policies; a few dozen closed-loop trials sufficed to find what they missed.

---

## 11. StateMem: Single-State Residual Memory with Adaptive Inference for Vision-Language-Action Policies

**Authors:** Wenzhuo Li, Qiongfeng Shi, Yi Zhou
**arXiv:** [2609.22684](https://arxiv.org/abs/2609.22684)
**Categories:** Robotics (cs.RO); Machine Learning (cs.LG)

Memory-dependent robotic manipulation often requires later actions to use information from earlier interactions. Existing vision-language-action (VLA) policies primarily rely on current observations, limiting historical information retention. Memory-augmented VLAs, such as MemoryVLA, address this limitation with external memory banks but require explicit storage and retrieval. To address these limitations, we propose StateMem, a single-state residual memory framework for VLA policies that uses prediction error to update a persistent memory token through low-rank residuals and to adaptively route cached prefixes. A training-free controller adjusts the routing threshold online, while fast correction compensates for stale prefix features during cache reuse. We evaluate StateMem on LIBERO, RoboMemArena, and real-world manipulation tasks. On LIBERO, StateMem achieves an average success rate of 97.6% and reduces the average VLM prefix refresh rate by 20.25% relative to full refresh. In the Occlusion category of RoboMemArena, StateMem achieves the best performance among single-VLA methods, reaching 21.8% Task Success Rate (TSR) and 44.3% Cumulative Success Rate (CSR). Across six real-world manipulation tasks, it achieves +21% in average success rate.

---

## 12. Think Like a World Model, Act Like a VLA: Distilling World-Model Representations into Compact Robot Policies

**Authors:** Trung Dao, Sankalp Yamsani, Jaden Park, Joohyung Kim, Yong Jae Lee
**arXiv:** [2609.24682](https://arxiv.org/abs/2609.24682)
**Categories:** Robotics (cs.RO); Computer Vision and Pattern Recognition (cs.CV)

Vision-Language-Action (VLA) models map observations to actions with no objective that accounts for how the world responds, so their robustness is bounded primarily by data coverage. World models carry precisely that missing objective and are better grounded for it, yet rolling the future forward costs seconds per decision and rules them out of the control loop. We show the two can be separated. What a world model knows about physical scenes lives in its internal features; generating the future is merely the objective that produced them, so the grounding can be inherited while the generative machinery is left behind. We add one feature-alignment term to ordinary VLA training: a frozen world model is run over the training frames once and cached, and the student learns to agree with that cache. No teacher is loaded during training, the projector is discarded after it, and the deployed policy is identical to the undistilled baseline, running in 32ms and 1.86GB on a consumer RTX5090, so every gain is attributable to the representation rather than to added capacity or test-time compute. A 0.8B student reaches 97.9% on LIBERO, improves from 48.2% to 50.5% on RoboCasa-GR1 humanoid manipulation, and the same objective carries over to real hardware, on both a single-arm and a bimanual platform. The gain survives changes of student scale, backbone, alignment layer, and teacher, indicating a broad representational prior rather than a fragile alignment between two particular networks. Project page: this https URL.

---

## 13. Bridge3D: Enabling Vision-Language-Action Models to See and Act in 3D

**Authors:** Haoxuan Li, Sixu Yan, Lianghui Zhu, ..., Shikang Wang, Xinggang Wang
**arXiv:** [2609.24525](https://arxiv.org/abs/2609.24525)
**Categories:** Robotics (cs.RO)

Vision-Language-Action (VLA) models have demonstrated remarkable generalization in robotic manipulation via large-scale multimodal pretraining. However, VLA models are mainly trained on 2D-centric observations, which inherently constrains their capacity for precise spatial manipulation. Previous methods enhance 3D awareness by introducing implicit spatial priors, but still lack explicit geometry guidance. In this paper, we propose Bridge3D that integrates both implicit and explicit 3D geometry guidance into pre-trained 2D VLA models, enabling them to ''see'' and ''act'' in 3D. Bridge3D introduces two strategies: 1) Implicit Fusion, which enriches visual tokens with features from 3D foundation models to improve ''seeing'' in 3D; 2) Explicit Conditioning, which integrates action denoising with an explicit 3D semantic field to achieve ''acting'' in 3D. Furthermore, we utilize the proposed layer-wise linear probing to improve learning efficiency. Experiments show that Bridge3D achieves superior performance against state-of-the-art methods. On the RoboTwin 2.0 benchmark, Bridge3D exceeds $\pi_0$ by 14.0 percentage points, while in real-world experiments, it outperforms Spatial Forcing by 11.7 percentage points. These results demonstrate Bridge3D's strong capabilities in high-precision and spatial-sensitive manipulation tasks.

---

## 14. StenoVLA-3D: 3D-Aware Reasoning VLA for Navigation Through Gastrointestinal Stenoses

**Authors:** Tamima Tabassum, Yiming Huang, Tianchun Wu, ..., Jiewen Lai, Hongliang Ren
**arXiv:** [2609.24187](https://arxiv.org/abs/2609.24187)
**Categories:** Robotics (cs.RO); Computer Vision and Pattern Recognition (cs.CV)

Autonomous endoscopic navigation requires the policy model to predict actions from texture-poor monocular observations, make safe control decisions, and retain evidence of lesions after they leave the field of view. Existing vision-language-action (VLA) models primarily rely on visual appearance and short-term context, limiting geometric grounding and episode-level reporting. We introduce StenoVLA-3D, a 3D-aware VLA framework for navigating through stenotic regions. We integrate point-maps into the Cosmos-Reason 2 backbone through learned geometry-gated fusion, and also propose a temporal state branch to model traversal progress. Our reasoning-and-action backbone predicts grounded reasoning with actions, while dedicated heads estimate stenosis shape and generate the final lesion report. We further introduce EndoCausal, an episode-level dataset with lesion annotations, actions, and temporally grounded reasoning. On 40 held-out recorded test episodes, StenoVLA-3D reaches 95.2\% semantic accuracy and 83.4\% action accuracy. On the physical 3-DoF endoscope, it attains 88.9\% and 77.8\% task success in esophageal and colonic phantoms (36 trials each), substantially outperforming the evaluated baselines.

---

## 15. CARE: Experience-Guided Atomic Corrective Execution for Vision-Language-Action Policies

**Authors:** Junlan Xiao, Junwei Jiang, Zaibin Zhang, ..., Huchuan Lu, Lijun Wang
**arXiv:** [2609.24118](https://arxiv.org/abs/2609.24118)
**Categories:** Robotics (cs.RO)

Vision-Language-Action (VLA) policies achieve strong performance in robotic manipulation but remain brittle once execution deviates from nominal trajectories. We propose CARE (Corrective Atomic Robotic Execution), a framework that improves recovery by learning from failures encountered during execution. Instead of generating corrective data from manually designed or random perturbations, CARE collects failed rollouts, models stage-conditioned post-failure deviations, and uses the resulting empirical distributions to synthesize representative failure states and corrective demonstrations. At inference time, CARE combines stage-wise planning with physically grounded 3D monitoring to trigger atomic adjustments or re-operations while preserving task progress. We further introduce the Failure State Recovery Benchmark (FSR-Bench), which evaluates recovery from intermediate failure states under local deviations and structural anomalies. Experiments across multiple VLA backbones, simulation benchmarks, and real-world dual-arm tasks show consistent improvements, with average task-success gains of 14.5 points in simulation and 15.9 points in the real world. Code, models, and data are available at this https URL

---

## 16. Imagine-RL: Residual-Confidence-Guided Cross-Attention for World-Model-Augmented VLA Reinforcement Learning

**Authors:** Kejia Hu, Wentong Zhai, Bo Zhao, Shuai Liang
**arXiv:** [2609.24033](https://arxiv.org/abs/2609.24033)
**Categories:** Robotics (cs.RO)

Reliable action evaluation in contact-rich manipulation requires looking beyond the current observation to future visual and contact consequences. Existing noise-space reinforcement learning efficiently steers a frozen Vision-Language-Action (VLA) policy, but its critics largely ignore these consequences. We present Imagine-RL, which augments noise-space VLA post-training with action-conditioned visual-torque imagination. For each candidate action chunk, a frozen visual-torque latent world model (VTLWM) autoregressively predicts compact future representations without pixel reconstruction. A current image-state-action query attends to observed histories and predicted futures, while previous-window prediction residuals provide token-wise confidence priors that suppress unreliable future tokens. By combining current evidence with predicted consequences, the action critic better evaluates candidate actions and supervises the actor, while the VLA and VTLWM remain frozen. Across four real-robot tasks with 50 evaluation trials per task, Imagine-RL uses only 100 RL trajectories and improves the average success rate by (23.6%) over DSRL and by (60%) over VLA baselines.

---

## 17. Opt2VLA: Force-Aware Vision-Language-Action for Contact-Rich Humanoid Whole-Body Manipulation

**Authors:** Fukang Liu, Yipu Chen, Jaehwi Jang, ..., Zsolt Kira, Ye Zhao
**arXiv:** [2609.23968](https://arxiv.org/abs/2609.23968)
**Categories:** Robotics (cs.RO)

Humanoid robots are expected to perform diverse human-level tasks in daily environments, many of which require precise regulation of interaction forces. While recent vision-language-action (VLA) models have shown promise for semantic planning and visuomotor control, existing humanoid systems primarily represent actions through geometric motion goals and rely on whole-body controllers focused on motion tracking, with limited explicit reasoning or control of interaction forces. This limitation is particularly relevant in contact-rich tasks, where geometrically similar motions may require different force regimes depending on the task context and where visual observations may become unreliable after contact. In this work, we present Opt2VLA, a force-aware VLA framework that introduces explicit force commands at the VLA-to-control interface for humanoid whole-body manipulation. A single multi-task VLA policy jointly predicts both geometric motion goals and continuous contact-force references, which are tracked by task-specific reinforcement learning (RL)-based whole-body controllers. To provide scalable and physically grounded supervision, we generate dynamically feasible and contact-consistent training data via whole-body trajectory optimization (TO) with explicit force references. We evaluate Opt2VLA on three contact-rich humanoid tasks and show that explicit force conditioning enables more accurate and consistent force regulation than motion-only control, while physically grounded torque supervision from TO further improves force tracking accuracy and stability. Closed-loop evaluations further demonstrate language-conditioned force modulation with Opt2VLA in simulation and on humanoid hardware.

---

## 18. Topology-Informed Visual Prompting For Vision Language Action Policies

**Authors:** Haoyang Wu, Abhinav Kumar, Dmitry Berenson
**arXiv:** [2609.23944](https://arxiv.org/abs/2609.23944)
**Categories:** Robotics (cs.RO)

Vision-language-action (VLA) policies can struggle with manipulation tasks with complex obstacle geometries due to partial observability. These complex geometries can lead to similar visual observations or robot configurations requiring qualitatively different actions, a distinction that can be quantified using topological signatures. While motion planners with full knowledge of environment geometries and object states can reason about these signatures in planning, this information is often not known at deployment. To address this issue, we present a topology-guided visual-prompting framework that uses simulation-based planning to augment a nominal demonstration dataset and provides vision-based guidance at deployment. Our method uses a Gauss-Linking-Integral topological signature representation to capture important topological properties of the environment. Using privileged geometry information from a simulation approximation of our environment, we augment a VLA fine-tuning dataset with trajectories that move the system to a demonstrated signature and, from the new configuration, resume task execution. A vision-language model (VLM) is fine-tuned on the same dataset to both predict signatures from live camera observations and predict end-effector waypoints, which are rendered as visual prompts on the observations to guide the VLA. Across three simulated bimanual tasks and a real-world box pickup task, our method outperforms a VLA fine-tuned only on nominal demonstrations and a VLM-prompting baseline that can remove topology-relevant information from observations. On hardware, it exceeds the strongest baseline by 40% in task success. Project website: this https URL.

---

## 19. Structured World-State Reasoning for Agentic Robotic Search

**Authors:** Finley R. Holt, Luis A. Pabon, John Irvin Alora, Jonas Frey, Marco Pavone
**arXiv:** [2609.23841](https://arxiv.org/abs/2609.23841)
**Categories:** Robotics (cs.RO)

Long-horizon robotic search must resolve natural language against heterogeneous, incomplete, and often ambiguous evidence: textual information, prior maps, and observations arriving over time. The core challenge is to contextualize these streams and decide where to gather evidence before selecting a target. We present WORLDS: World-state Observation and Reasoning for Language-guided Discovery and Search, a framework that grounds reasoning in a persistent graph initialized from geospatial priors and updated by perception. Parallel Reasoners maintain competing candidate interpretations and request evidence to distinguish between them. We collect and process the requested observations with a multimodal Examiner, after which a Judge selects a grounded target or requests another pass. WORLDS achieves 51.8% navigation success across all 5,311 CityNav test episodes, the highest reported success rate, exceeding the previous published best by 15.7 percentage points under an OSM-only, high-resolution orthographic protocol. On 1,000 shared episodes, it achieves 50.0% versus 27.9% for the strongest adapted baseline using the same model, prior, sensing stack, and movement budget. Observation-based verification by the Examiner contributes 5.9 points of this success, and at a reduced reasoning-effort setting WORLDS still exceeds the adapted GeoNav baseline by 18.8 points while generating fewer tokens. We also demonstrate WORLDS on a quadrotor, which flies the generated sensing waypoints and grounds three language targets, including a vehicle absent from the map, from its onboard imagery.

---

## 20. CompVLA: A Variable Compliance Vision-Language-Action Model for Contact-rich Manipulation

**Authors:** Jongmin Kim, Junsu Ha, Che-Sang Park, ..., Jianlong Fu, Frank C. Park
**arXiv:** [2609.23614](https://arxiv.org/abs/2609.23614)
**Categories:** Robotics (cs.RO)

Contact-rich manipulation, requiring robots to regulate not only motion but also how they yield to external forces, has emerged as the next frontier for Vision-Language-Action (VLA) models. However, existing VLAs output purely kinematic commands, degrading performance on real-world contact-rich tasks. In this paper, we introduce CompVLA, a unified VLA framework that jointly predicts motion and stiffness matrix from RGB and language inputs. Our approach augments the conventional architecture with a dedicated Compliance Expert, which outputs time-varying stiffness and virtual displacement profiles executed via geometric impedance control. We demonstrate that CompVLA achieves the highest average success rate across diverse contact-rich tasks, outperforming both vanilla and compliance-aware VLA baselines, with ablations confirming each component is essential.

---

## 21. TaskAnchor: Grounding Task State in Reactive VLAs for Long-Horizon Manipulation

**Authors:** Hengyan Liu, Wenlve Zhou, Bo Yue, ..., Xiaofen Xing, Kui Jia
**arXiv:** [2609.23580](https://arxiv.org/abs/2609.23580)
**Categories:** Robotics (cs.RO)

Reactive vision--language--action (VLA) models struggle with long-horizon manipulation when visually similar observations can correspond to different actions depending on the task stage or interaction history. We refer to this ambiguity as task-state aliasing and introduce TaskAnchor, a lightweight adapter that grounds pretrained VLAs in execution history. TaskAnchor combines history-conditioned visual refinement with a milestone-supervised task-state coordinate, a scalar representing the semantic stage of execution. These signals are injected through the native visual and language interfaces, respectively, without introducing an explicit planner or modifying the action-generation mechanism. On RMBench, TaskAnchor achieves approximately 4.9--5.5$\times$ the average success rates of the published $\pi_{0.5}$ and X-VLA baselines, with consistent gains on RoboMemArena and real robots. The added latency is only 2.08\,ms per action chunk for $\pi_{0.5}$.

---

## 22. SCULPT-VLA: Learning Structured Control through Staged Action Grounding

**Authors:** Wenbo Li, Yiteng Chen, Wei Zhang, ..., Jun Yang, Qingyao Wu
**arXiv:** [2609.23275](https://arxiv.org/abs/2609.23275)
**Categories:** Robotics (cs.RO)

Vision-language-action (VLA) policies increasingly incorporate structured intermediate supervision beyond action labels. Yet specifying what an intermediate representation should encode leaves open how action prediction learns to depend on it. We introduce \textbf{SCULPT-VLA}, a policy that learns structured control through staged action grounding. Its action-conditioning state comprises complementary factors for task progression, scene dynamics, and spatial grounding. Training first forms these factors with teacher scaffolds, then grounds coarse action prediction through their composition as scaffold inputs are withdrawn. Direct perceptual access is subsequently restored for continuous refinement, combining the learned state with perceptual detail. The curriculum separates learning to condition actions on structure from refining continuous control. Deployment requires neither teachers nor discrete-action autoregression. SCULPT-VLA achieves higher average success than shared-backbone baselines on LIBERO, SimplerEnv-WidowX, and RoboTwin 2.0 Full. On SimplerEnv-WidowX, final success is 83.5\%, versus 71.3\% when Stage-II action learning directly accesses vision and language. Across four physical robot tasks, average success under the tested distribution shifts reaches 58.1\%, compared with 45.6\% for $\pi_{0.5}$. Training ablations and factor-wise interventions support the staged design and show that the learned state continues to contribute to control after direct perceptual access is restored.

---

## 23. An Empirical Study and Open Testbed for Federated Fine-Tuning of Vision-Language-Action Models

**Authors:** Zhekai Duan, Kevin Ziyang Xie, Xinyu Tan, ..., Gaowen Liu, Chris Xiaoxuan Lu
**arXiv:** [2609.22973](https://arxiv.org/abs/2609.22973)
**Categories:** Robotics (cs.RO)

Adapting a pretrained Vision-Language-Action (VLA) model to a new robot, environment, or task requires demonstrations that are collected locally and often discarded. Federated learning is a promising approach to exploiting such distributed demonstrations by learning a shared policy. However, whether it can adapt large pretrained VLAs remains an open question, and a lack of reproducible benchmarks for pretrained VLAs and reusable training frameworks makes existing results difficult to compare. In this paper, we conduct a systematic study of federated fine-tuning of three modern pretrained VLA policies on the 40 simulated tasks of the LIBERO manipulation benchmark, and on six real-world tasks in two real-robot experiments, with demonstrations collected across two and three sites, respectively. Our study analyzes the key choices in this setting, spanning multiple federated parameter scopes, three aggregation algorithms, and evaluation under distribution shift. Based on the study, we derive a series of lessons, including the dominance of the federated scope over the choice of aggregation algorithm and the difficulty of matching centralized fine-tuning on physical robots, where cross-site heterogeneity is stronger than simulation captures. We also highlight opportunities for federated VLA learning, such as the ability to match centralized fine-tuning on heterogeneous data, to remain at least as robust as centralized fine-tuning under distribution shift, and to personalize, with each client federating part of the policy and keeping the rest local, which helps where the policy's pretraining is weak but leaves no usable global model. We open-source \decentvla{}, the model- and runtime-agnostic testbed behind the study, to facilitate future research and fair comparisons in federated VLA learning.

---

## 24. H-VLA: Hierarchical Vision-Language-Action Model with Key-Action Reasoning and Motion Planning in a Unified Action Space

**Authors:** Xiongfeng Peng, Lu Xu, Yandong Wang, ..., Daehyun Ji, Chao Zhang
**arXiv:** [2609.22895](https://arxiv.org/abs/2609.22895)
**Categories:** Robotics (cs.RO)

Vision-Language-Action (VLA) models have shown strong potential for robotic manipulation, but many existing methods still rely on direct mappings from language and visual observations to dense actions. This formulation can weaken the semantic reasoning capability inherited from pre-trained Vision-Language Models (VLMs), which are mainly optimized for visual-linguistic understanding rather than low-level control, and becomes fragile under spatial variations, including changes in object positions, scene layouts, robot embodiments, and camera viewpoints. To address these limitations, we propose H-VLA, a hierarchical VLA framework that decouples high-level key-action reasoning from low-level motion generation. H-VLA combines a Key-Action Model for predicting a key-action as the next manipulation subgoal, a Motion Planning Model for generating dense future actions conditioned on the predicted key-action, and a Unified Camera-Centric Action Space for consistent representation across datasets, embodiments, and viewpoints. We further adopt a two-stage training strategy that emphasizes key-action reasoning during pre-training and dense motion generation during fine-tuning. Experiments show that H-VLA achieves strong performance on SimplerEnv, reaching 91% on Google Robot visual matching, 84% on Google Robot variant aggregation, and 81% on WidowX visual matching. On Agilex real-robot tasks, H-VLA improves over the strongest baseline by 10, 47, and 16 percentage points under in-distribution, out-of-distribution position, and out-of-distribution scene/object settings, respectively.

---

## 25. Stable and Efficient Real-World Online VLA Post-Training via Asynchronous Replay-Anchored Policy Improvement

**Authors:** Jiarui Yang, Jiajin Zhang, Bin Zhu, Jingjing Chen, Yu-Gang Jiang
**arXiv:** [2609.22888](https://arxiv.org/abs/2609.22888)
**Categories:** Robotics (cs.RO)

Online post-training of vision-language-action (VLA) models requires efficient use of robot interaction and reliable policy improvement from continually collected experience. We propose asynchronous Replay-Anchored Policy improvement (RAPolicy), a framework that performs rollout and learning concurrently while grounding both critic and actor updates in replayed behavior. The critic learns chunk-level values from recorded actions and constructs Bellman targets without predicting next actions, reducing computation and dependence on action-value estimates outside replay coverage. The one-step flow actor reuses the initial noise stored during rollout and learns through advantage-weighted conditional likelihood, directly supervising the action mapping used for execution. We evaluate RAPolicy across four single-task settings and one joint five-task setting in the real world, with online training budgets of only 1--2 hours. Starting from policies fine-tuned on just 10 demonstrations per task, RAPolicy rapidly adapts to new single tasks and achieves an average 86.3% success rate. In the joint multi-task setting, RAPolicy improves overall success rate from 52% to 88% while preserving performance on already reliable tasks and improving weaker capabilities. Overall, RAPolicy substantially outperforms the baselines in aggregate task success while requiring fewer human interventions, demonstrating stable policy improvement and high online training efficiency. Project page: this https URL.

---

## 26. SmoLSTM: A Compact Vision-Language-Action Model with Recurrent Memory that Persists

**Authors:** Jan-Gerrit Habekost, Parsa Mastouri Kashani, Connor Gäde, ..., Stefan Wermter, Jae Hee Lee
**arXiv:** [2609.22854](https://arxiv.org/abs/2609.22854)
**Categories:** Robotics (cs.RO); Computer Vision and Pattern Recognition (cs.CV)

Vision-language-action models often predict actions from only the current observation, which can leave tasks involving object occlusion or visually identical objects ambiguous without episode history. The usual countermeasure, widening the observation window, turns the horizon into a hyperparameter and lets per-step cost grow with it. We instead capture the episode in a recurrent state. SmoLSTM couples a frozen 256M-parameter SmolVLM backbone to a matrix-memory LSTM control layer in which observation tokens and action queries are unified in a single causal stream that is never reset throughout the entire episode. Recurrent-state storage is therefore O(1) in episode length. A flow-matching action head predicts chunks of 10 end-effector pose deltas and gripper commands at each control step. Our single policy, trained jointly on 7,461 demonstrations across 140 tasks and evaluated on held-out initial states, performs best, reaching 85.1% subgoal coverage and 77.5% full-task success on LIBERO-Mem with 0.04B trainable parameters, surpassing both the benchmark's own object-centric baseline and recent memory-based approaches. Resetting the recurrent state at every control step reduces full-task success to 7.0%, showing that the trained policy relies on context carried between decisions. The same model achieves 79.6% average success on standard LIBERO.

---

## 27. ForceRFT: Refining VLA Actions through Force-Guided Residual Reinforcement Learning

**Authors:** Yichen Wang, Chaoyang Zhang, Xuqi Su, ..., Haiyue Zhu, Xiaocong Li
**arXiv:** [2609.22840](https://arxiv.org/abs/2609.22840)
**Categories:** Robotics (cs.RO)

Force-conditioned vision-language-action (VLA) policies can respond to contact, but when trained solely on demonstrations, their recovery behavior may be limited by demonstration coverage, and they do not learn from deployment outcomes. Human corrective imitation provides additional recovery examples, but its objective matches local action targets without explicitly optimizing task return. We present ForceRFT, a force-guided residual reinforcement learning framework that learns contact-dependent corrections from human supervision and autonomous task outcomes. A frozen, demonstration-trained SmolVLA-based prior generates force-conditioned action chunks, while a lightweight residual actor refines individual end-effector pose commands using wrist feedback acquired during chunk execution. The decision-time wrist wrench, its temporal change, and the selected base motion condition both residual correction and value estimation. Human corrections supervise the residual actor, while verified autonomous transitions train the twin critics and support value-guided updates to the same actor. Bootstrapping is restricted to autonomous segments, preventing TD credit from crossing human-intervention boundaries. Real-robot experiments on plug insertion, ring-on-peg assembly, and whiteboard wiping show higher autonomous success rates than the evaluated demonstration-trained and residual-imitation baselines. Comparisons with residual imitation support value-guided residual optimization, while plug-insertion ablations indicate the benefit of direct execution-time wrist feedback.

---

## 28. VT-Bridge: Bridging Pretrained Foundation VLAs to VTLAs via Lightweight Residual Adaptation

**Authors:** Yansong Wu, Tuo Yang, Rongping Zhao, ..., Fan Wu, Alois Knoll
**arXiv:** [2609.22606](https://arxiv.org/abs/2609.22606)
**Categories:** Robotics (cs.RO)

Vision-Tactile-Language-Action (VTLA) models have demonstrated clear advantages over Vision-Language-Action (VLA) models in contact-rich manipulation. However, developing VTLA models is severely constrained by the massive amounts of vision-tactile data and computational resources required. To address this bottleneck, we propose VT-Bridge, a lightweight residual adaptation strategy that bridges pretrained foundation VLAs to VTLAs. Rather than training a VTLA model from scratch or modifying the original architecture of a pretrained VLA, VT-Bridge employs an identical lightweight residual-adapter architecture across VLA backbones and uses backbone-specific weights to refine actions at the robot execution frequency. This design substantially lowers the data and training barriers. Specifically, it requires up to 50 vision-tactile demonstrations per task to fine-tune a VLA backbone and train a 0.98M-parameter residual adapter. Experiments with three representative VLA backbones ($\pi_0$, $\pi_{0.5}$, and SmolVLA) across four contact-rich manipulation tasks further demonstrate its consistent effectiveness across VLA architectures. On average, VT-Bridge raises the task completion rate from 11.7% with task-level VLA fine-tuning alone to 62.9%. Together, these findings demonstrate the broad applicability, effectiveness, and accessibility of VT-Bridge for contact-rich manipulation. The project page is available at this https URL.

---

## 29. React When You Need To: Event-Triggered Asynchronous Inference for VLA Policies

**Authors:** Yansong Wu, Huaqing Li, Tianding Hou, Lingyun Chen, Alois Knoll
**arXiv:** [2609.22587](https://arxiv.org/abs/2609.22587)
**Categories:** Robotics (cs.RO)

Vision-Language-Action (VLA) models commonly predict action chunks, limiting their ability to react to environmental changes during execution. Existing asynchronous inference methods improve reactivity but typically rely on a fixed inference gap. In this paper, we propose an event-guided dynamic inference strategy that adapts the inference gap according to scene changes observed since the previous inference. Thereby, it simultaneously preserves motion consistency and prompt reactivity. Across static and dynamic real-world settings, our method consistently performs best, averaging 95% success and exceeding the strongest baseline by 55 percentage points. The code will be made publicly available upon acceptance. The project page is available at this https URL.

---

## 30. KerColle: Unlocking Fine-Grained GPU Concurrency in Vision-Language-Action Models

**Authors:** Anna Li, Christina Giannoula, Nandita Vijaykumar
**arXiv:** [2609.22335](https://arxiv.org/abs/2609.22335)
**Categories:** Hardware Architecture (cs.AR); Robotics (cs.RO)

Vision-Language-Action (VLA) models have emerged as foundational models for next-generation robotics. High VLA inference throughput is critical for meeting the control-rate requirements of robots. VLA models comprise two phases, a vision-language model (VLM) and an action head, that can be decoupled and executed asynchronously and concurrently across independent robot requests. Through a detailed characterization of four state-of-the-art VLAs, we observe that GPUs are severely underutilized in VLA inference as the Cooperative Thread Array (CTA) scheduler of GPU is unable to fully overlap the two independent phases of VLA execution. We identify that this inefficiency is caused by head-of-line blocking in the hardware thread-block dispatcher.
We demonstrate that prior scheduling frameworks do not address the challenges posed by VLA concurrency. First, the independent phases across different robot requests each comprise numerous kernels, and at any given time, there are different combinations of kernels that are executed in parallel. This makes static or ahead-of-time scheduling policies largely ineffective. Second, many of the action-head operators are short-running kernels and there are numerous such kernels. This leaves no headroom for online profiling or preemption-based mechanisms. To address these challenges, we present KerColle, a lightweight GPU scheduling framework that leverages online Streaming Multiprocessor (SM) utilization and individual kernel resource requirements to intelligently and dynamically co-schedule kernels to efficiently overlap the two phases of execution by (1) mitigating head-of-line blocking, and (2) co-scheduling kernels with complementary resource requirements. We demonstrate in simulation, across two GPU architectures, for 4 state-of-the-art VLA models, that KerColle delivers throughput gains of up to $28\%$.

---
