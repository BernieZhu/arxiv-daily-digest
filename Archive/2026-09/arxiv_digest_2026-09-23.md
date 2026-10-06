# arXiv Daily Digest — 2026-09-23

**Mode:** direct
**Categories:** cs.AI, cs.LG, cs.RO, cs.CV
**Keywords:** VLA, RSI, agentic robot, self-improving robot, self-evolving robot, robot harness
**Papers found:** 12

---

## 1. Recursive self-improvement of AI research agents

**Authors:** Dhruv Srikanth, Bingchen Zhao, Dixing Xu, Yuxiang Wu, Zhengyao Jiang
**arXiv:** [2609.26457](https://arxiv.org/abs/2609.26457)
**Categories:** Artificial Intelligence (cs.AI); Machine Learning (cs.LG); Software Engineering (cs.SE)

AI agents are beginning to automate research and development across the AI stack, from improving training efficiency to optimizing inference. A natural next step is to improve the research efficiency of the agents themselves. When an AI research agent's own code is the object of optimization, each accepted rewrite becomes the agent that the next round edits. We refer to this loop as recursive self-improvement. Its significance lies in a long-standing trend, in which increased cumulative spending on R&D yields diminishing returns. Sustained self-improvement offers a way to counter this trend. We present AIDE^2, a system that implements this loop for a frontier AI research agent. It proposes changes to its own code, benchmarks modified versions of itself on a suite of AI R&D tasks, and keeps the changes that perform best on hidden evaluations. In an autonomous 8-day run, AIDE^2 discovered seven successive improvements, ranging from a new search policy to memory mechanisms that compress and manage the agent's growing context. These gains generalize to four held-out benchmarks spanning machine learning engineering, heuristic algorithm engineering, and physics-based weather forecasting, the last of which is out of distribution from the selection tasks. On all four, the strongest discovered agent matches or exceeds a human-engineered production research agent that ranks among the strongest on FML-Bench. On a separate held-out task family, the discovered agents also exhibit reduced reward hacking, a property the loop never explicitly optimized for: the rate falls from 55% to 32% during the run, 7 percentage points below the human-engineered agent. Together, these results show that an AI research agent can improve its own research efficiency through recursive self-improvement, and that these gains transfer to tasks and domains the loop never encountered.

---

## 2. IndustrialVLA-Bench: A Traceable Multi-Axis Evaluation of Open Robot Policy Models

**Authors:** Yiqi Wang, Zhifeng Rao, Jiaqi Zhang, ..., Shan You, Taotao Cai
**arXiv:** [2609.25562](https://arxiv.org/abs/2609.25562)
**Categories:** Robotics (cs.RO); Artificial Intelligence (cs.AI)

Open robot policies increasingly follow two paradigms: vision-language-action models (VLAs) directly map observations and instructions to actions, whereas world-action models (WAMs) incorporate learned video or world dynamics into policy learning or action generation. Although both target the same manipulation tasks and represent alternative design choices, they are commonly reported under different evaluation protocols, leaving their capability, robustness, language sensitivity, and deployment-cost trade-offs unclear. We present IndustrialVLA-Bench, an evidence-aware evaluation of six released VLA and WAM systems under a unified reporting schema. It separately evaluates clean capability on LIBERO, non-language robustness on LIBERO-Plus, instruction sensitivity on LIBERO-Para, and observed execution cost. Reported task scores aggregate three complete evaluations with distinct random seeds under a fixed checkpoint and inference configuration. Across all six systems, clean LIBERO averages differ by only 1.58 points, whereas robustness and paraphrase summaries span 14.62 and 31.08 points. Restricting every comparison to the three protocol-faithful systems preserves the effect (1.36, 14.62 and 23.10 points), so the diagnostic separation reported here does not depend on the weaker evidence tiers. We additionally report observed inference latency, peak memory, runtime mode, and an evidence status for every system. Protocol-faithful, near-reproduction, and pending-verification entries remain visibly separated; only protocol-faithful entries support strict comparisons. Rather than claiming universal superiority of either paradigm, IndustrialVLA-Bench provides traceable evidence for comparing released robot policies on shared practical criteria. Code and evaluation records are available at this https URL.

---

## 3. VLAQuantBench: Closed-Loop Evaluation of Post-Training Quantization for Vision-Language-Action Models

**Authors:** Jiuyi Xu, Qing Jin, Meida Chen, ..., Yang Sui, Yangming Shi
**arXiv:** [2609.25376](https://arxiv.org/abs/2609.25376)
**Categories:** Robotics (cs.RO); Artificial Intelligence (cs.AI)

Post-training quantization reduces the memory requirements of vision-language-action (VLA) models, but precision selection must account for the interaction between layer scope, numerical format, and calibration. We introduce \textbf{VLAQuantBench}, a controlled evaluation with 409 runs and 94,574 simulation episodes: four models on LIBERO, with X-VLA additionally evaluated on three simulation benchmark families. Under uncalibrated W4A4 round-to-nearest quantization, expanding a $\pi_{0.5}$ action-head subset from 126 to 167 layers raises success from 7.0\% to 70.5\%. Fixed-observation replay confirms a corresponding numerical recovery. Two-episode calibration removes the severe joint failures in the tested subsets, whereas the same smoothing-and-clipping recipe lowers $\pi_0$ success and does not recover OpenVLA-OFT end-to-end. For OpenVLA-OFT, protecting one 28,672-parameter output projection instead restores near-baseline success: the remaining 441 eligible linear layers retain W3 on LIBERO-Long or eight-bit activations across all four suites. Task-clustered intervals support the large failure and recovery contrasts. These results establish recipe-dependent interactions and identify concrete precision assignments, rather than universal layer-sensitivity rules. Real-kernel and physical-robot measurements complement the accuracy analysis. Code, configurations, and episode records are publicly available at this https URL.

---

## 4. Beyond Reconstruction Error: Analytical and Data-Driven Action Tokenization for Autoregressive Vision-Language-Action Models

**Authors:** Yuxin Yang, Gaohan He, Changxue Guan, Hangming Liu
**arXiv:** [2609.25820](https://arxiv.org/abs/2609.25820)
**Categories:** Robotics (cs.RO); Machine Learning (cs.LG)

Discrete action tokenization is central to autoregressive vision-language-action (VLA) models, yet action representations are often evaluated primarily through reconstruction fidelity. We ask which representation properties actually matter for closed-loop control by comparing fixed analytical, data-driven linear, and nonlinear neural representations under a unified tokenization interface. Across rate-distortion analysis, sequence-modeling diagnostics, and 3,500 LIBERO rollouts, representation rankings change with the evaluation criterion. PCA achieves lower nominal reconstruction error than Temporal-DCT, but produces less predictable token sequences and 3.0 percentage points lower mean seen-task success across three policy-training seeds, with the policy ordering reversing in one seed. In a matched seed-42 ablation, an autoencoder further reduces reconstruction error yet does not yield the strongest policy and exhibits greater sensitivity to discrete token perturbations. These findings show that reconstruction fidelity alone cannot reliably select action representations for autoregressive control, motivating joint evaluation of geometric fidelity, sequence predictability, decoder stability, and closed-loop performance.

---

## 5. HABILIS Brain 0: Geometry-Change Supervision for Vision-Language-Action and Residual Flow Recovery

**Authors:** Jinu Pahk, Jesoon Kang, Taegeon Park, ..., Jaejoon Kim, Byoung-Tak Zhang
**arXiv:** [2609.25558](https://arxiv.org/abs/2609.25558)
**Categories:** Robotics (cs.RO); Machine Learning (cs.LG)

Vision-language-action policies benefit from geometric supervision, but current-frame geometry alone does not explicitly describe the changes associated with manipulation. This design is motivated by the goal of learning an embodiment-agnostic visual interface that can be pretrained across robot and egocentric video before robot-specific action alignment. We introduce Geometry-Change VLA (GC-VLA), which learns to predict multiview future-current geometry-change tokens from current observations. Offline frame pairs define a nominal 0.5-second prediction horizon; future observations are used only to construct training targets. Stage 1 trains a geometry-change vision-language model (GC-VLM). Stage 2 introduces a continuous ActionExpert and aligns it with robot actions while stopping action-flow gradients at the VLM interface. Stage 3 enables these gradients to update the trainable VLM components jointly with the ActionExpert. Stage 4 freezes GC-VLA and applies Geometry-Conditioned Residual Flow (GCRF), using a binary intervention router and a single bounded residual velocity policy learned from closed-loop feedback. GC-VLA achieves 95.20% success on LIBERO, and GC-VLA with GCRF achieves 99.55%. Inference uses current observations and the learned GC representation without executing the offline target encoders.

---

## 6. RouteRLT: Learning When and Which RL Specialist Should Control a Vision-Language-Action Policy

**Authors:** Chongyu Zhu, Jaden Hinds, Hyegang Kim, ..., Ramy Elmallah, Chi-Guhn Lee
**arXiv:** [2609.26467](https://arxiv.org/abs/2609.26467)
**Categories:** Robotics (cs.RO)

Vision-language-action (VLA) models provide broad manipulation competence, but often struggle during the precision-critical stages that dominate contact-rich industrial tasks such as connector insertion and cable management. A common remedy is to refine a pretrained VLA with reinforcement learning (RL), enabling task-specific improvement beyond behavior cloning. However, how to preserve its generalist behavior while deciding when RL refinement is needed and which specialized policy should act remains an open question. In this work, we present RouteRLT, a routing framework that learns when and which RL specialist, an RL policy trained for a single precision-critical phase, should take control from a generalist VLA. A phase selector identifies the active controller, a stabilizer suppresses transient switches, and an action-boundary manager handles transitions between chunked policy outputs. We evaluate RouteRLT on multi-object pick-and-place tasks in LIBERO, as well as on a real-world cable pickup and port-insertion task with multiple precision-critical stages. In simulation, the learned routing improves over the base VLA and matches routing with privileged phase boundaries, without accessing those boundaries at deployment. The real-robot evaluation validates automatic routing to both the pickup and insertion specialists under an operator-aligned handoff protocol. Altogether, these results show that learned routing applies RL specialist control where precise adaptation is most valuable while preserving generalist VLA behavior, including recovery from failed execution attempts.

---

## 7. SafeLoop: Risk-Aware Rollback for Vision-Language-Action Manipulation

**Authors:** Zeyu Lou, Tianran Zhang, Xinquan Yue, Ya Jing, Chenyang Si
**arXiv:** [2609.26313](https://arxiv.org/abs/2609.26313)
**Categories:** Robotics (cs.RO)

Recent vision-language-action (VLA) models are promising for general-purpose manipulation, but long-horizon execution remains fragile. Small state-estimation or control errors can lead to irreversible failures (e.g., collisions and object drops). Avoiding these risks requires a proactive safety mechanism capable of anticipating hazards. In this paper, we introduce SafeLoop, a non-invasive external wrapper that adds hazard prediction and rollback-based recovery to a VLA model without changing its parameters. SafeLoop trains a risk predictor from vision and proprioception to output four values: the probability and time-to-hazard for body collisions and for object failures. A lightweight controller then chooses one of three actions based on the predicted risk: continue execution (noop), save a safety checkpoint (record), or retreat in joint space (rollback). Rollback moves the robot back to a recent safe waypoint and queries the base policy again, which may yield an alternative continuation. Across 24 LIBERO tasks (16 random seeds each) and three real-robot tasks (25 rollouts each), SafeLoop achieves a stronger overall safety-success trade-off than alternative methods, reducing hazard cases by roughly 70% while preserving task success and the base-policy control rate. Project code is available at this https URL.

---

## 8. RoboTwin-Phys: Do WAMs and VLAs Understand the Physical World?

**Authors:** Jiaqi Zhang, Feng Ye, Mingjia Yang, ..., Siwei Ma, Chuanmin Jia
**arXiv:** [2609.26292](https://arxiv.org/abs/2609.26292)
**Categories:** Robotics (cs.RO)

Physical-condition diversity is largely missing from current benchmarks for robot manipulation. While large-scale simulation benchmarks increasingly incorporate variations in object appearance, scene layout, and visual observations, they typically keep the underlying physical parameters fixed. As a result, important sources of real-world variability, such as changes in mass, friction, and joint dynamics, remain largely untested. We introduce RoboTwin-Phys, a physics-diverse benchmark that treats physical-condition diversity as an explicit dimension of robot manipulation evaluation. The benchmark continuously varies 13 physical attributes within physically plausible ranges, providing a unified setting for evaluating policies across diverse physical operating conditions. We further release more than 5,000 expert demonstrations with ground-truth physical parameters, enabling physical-attribute estimation, condition-aware modeling, and physics-conditioned policy training. Evaluations of representative WAMs and VLAs reveal a substantial robustness gap: models that remain effective under existing visual and layout randomization can degrade markedly under changes in physical conditions. RoboTwin-Phys provides the benchmark, data, and evaluation protocol needed to systematically measure and improve robustness to physical-condition diversity in robot manipulation.

---

## 9. StrataVLA: Hierarchical and Efficient 3D Geometric Grounding for Vision-Language-Action Models

**Authors:** Jin Cui, Zhaoyu Pu, Botao Cai, ..., Boran Zhao, Pengju Ren
**arXiv:** [2609.26071](https://arxiv.org/abs/2609.26071)
**Categories:** Robotics (cs.RO)

Vision-Language-Action (VLA) models inherit strong semantic priors from large-scale vision-language pretraining, yet remain limited in robotic manipulation by insufficient 3D spatial awareness. Existing approaches either require explicit depth or point-cloud inputs, compress geometry into training-time supervision, or inject it only at the model input or action expert, leaving the vision-language backbone without persistent access to task-relevant spatial information. We introduce StrataVLA, a plug-and-play framework for hierarchical geometric grounding. A frozen geometry foundation model extracts shared geometric features from RGB observations, while sparse, layer-specific Geometry Adapters allow visual representations at selected backbone depths to retrieve relevant geometric evidence through cross-attention. To make inference-time geometry practical, StrataVLA further combines task-aware routing with an LRU feature cache that exploits temporal redundancy during task manipulation. Experiments on LIBERO, SimplerEnv, and real-world manipulation demonstrate consistent gains over strong VLA baselines. StrataVLA achieves 98.53% average success on LIBERO suites while reducing geometry-model invocations by up to 88%, establishing hierarchical geometry injection as an effective and efficient way to achieve spatially grounded robotic control.

---

## 10. MedVLA: A Hierarchical Vision-Language-Action Framework for Closed-Loop Precision Medical Robot Manipulation

**Authors:** Junjie Xie, Chuxuan He, Angen Ye, Yujia Song, Dapeng Zhang
**arXiv:** [2609.25756](https://arxiv.org/abs/2609.25756)
**Categories:** Robotics (cs.RO)

Precision medical robotics demands adaptive decision-making under strict safety, interpretability, and execution constraints. Although recent Vision-Language-Action (VLA) models show strong multimodal reasoning ability, their continuous action generation paradigm is not well suited for precision medical tasks, where reliable closed-loop operation may also depend on non-action system function calls. To address this gap, we propose MedVLA, a hierarchical framework that couples high-level multimodal reasoning with low-level function-constrained execution. We further introduce a scalable multi-agent pipeline to generate skill-oriented chain-of-thought(CoT) data for structured training. Built on different multimodal large-model backbones, MedVLA consistently improves performance after fine-tuning, demonstrating the effectiveness of the proposed framework across model variants. Under identical initial conditions, we perform 100 closed-loop flexible electrode implantation trials. The results show that MedVLA achieves a 95.0\% task success rate, substantially outperforming representative VLA baselines, including OpenVLA (8\%) and $\pi_0$ (15\%), in accuracy, stability, and safety. These results indicate that structured reasoning with constrained function-level execution is a practical route toward deployable precision medical robotics.

---

## 11. Fisheye-VLA: Decoupling Coverage and Acuity for Manipulation with a Single Fisheye Camera

**Authors:** Ziang Ren, Zike Yan, Raymond Zhang, Xuguo He, Zhongyu Li
**arXiv:** [2609.25750](https://arxiv.org/abs/2609.25750)
**Categories:** Robotics (cs.RO)

Manipulation requires both broad scene awareness and detailed local feedback, yet conventional camera rigs provide them through separate front and wrist cameras. We present Fisheye-VLA, a visual interface that brings these capabilities together using a single passive fisheye. A global view preserves the workspace, while local perspective crops direct detail toward the interaction. The key design question is where this local visual budget should go. We answer it through a controlled re-rendering study, comparing alternative crop directions on the same recorded observations. The study finds that end-effector-centered views capture most of the estimated benefit of a much larger candidate pool, motivating a compact allocation around both hands. Our interface uses calibrated end-effector projection and motion lead to track the crops, while a shared ray encoding preserves their spatial meaning as they move. Integrated with a pretrained VLA, it achieves 84% and 82% success in the two expanded tabletop regions, where some target placements extend beyond the front-camera coverage, and supports shelf and conveyor manipulation. Ablations show that local crops and their viewing directions become more important in the larger workspace regions. The results demonstrate that a single fisheye can support these manipulation tasks without physical wrist cameras.

---

## 12. CableVLA: Simulation-Privileged Global-Local Representation Learning for Cable Routing

**Authors:** Zhifei Teng, Bo Feng, Xiang Zou, ..., Zhouping Yin, Yiqun Li
**arXiv:** [2609.25606](https://arxiv.org/abs/2609.25606)
**Categories:** Robotics (cs.RO)

Cable routing requires coordinated control of global cable topology and changing local contacts. We present CableVLA, an end-to-end multimodal vision-language-action framework that converts simulation-privileged supervision into deployable cable-topology and tactile representations. TopoHead distills node-level physics and current and future cable-topology information into causal visual context for the action expert. TacSense uses complementary frame and taxel branches to learn contact dynamics from resistive arrays, with simulator-derived kinematics and contact events providing supervision beyond the measured force map. A contact gate activates force-tactile residuals that refine the next 8 arm-and-gripper actions of a frozen topology-conditioned policy. Across 345 MuJoCo evaluations, CableVLA improves success from 62.6% for the $\pi_{0.5}$-V visual baseline to 84.9%. TacSense achieves pronounced gains in slip-transition recognition over a CNN-LSTM baseline with a similar parameter count, and this advantage persists under frozen-encoder probes. Topology prediction and 57-task tactile evaluations assess representation quality, while policy adaptation studies evaluate downstream control performance. Cross-simulator and real-robot comparisons further examine zero-shot policy transfer under changes in dynamics and sensing.

---
