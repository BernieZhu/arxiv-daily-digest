# arXiv Daily Digest — 2026-11-20

**Mode:** direct
**Categories:** cs.AI, cs.LG, cs.RO, cs.CV
**Keywords:** VLA, RSI, agentic robot, self-improving robot, self-evolving robot, robot harness
**Papers found:** 15

---

## 1. System-One RSI: Building Muscle Memory for Interactive Agents through Guided Practice

**Authors:** Qingxu Fu, Xuanfa Jin, Ziqian Chen, Zhaoyang Liu, Bolin Ding
**arXiv:** [2611.26007](https://arxiv.org/abs/2611.26007)
**Categories:** Artificial Intelligence (cs.AI)

Reasoning models provide strong multimodal task understanding but struggle with sub-second control because deliberation increases decision latency. Fast decision models can meet the response window, yet prompting and few-shot examples do not readily provide the fine-grained experience required by a new task. Inspired by coached motor learning, this paper presents System-One Recursive Self-Improvement (System-One RSI), which couples two loops. The high-frequency online inner loop is an Observe, Orient, Decide, Act (OODA) cycle: a decision model maps each visual observation and task question to structured judgments, and a decision tree converts them into timed actions without invoking a reasoning model. The offline outer loop is a recursive improvement cycle carried out by a team of reasoning agents. The team revises the decision-model prompt and decision tree, captures interaction records, derives supervision from those records, and trains or deploys updated model parameters. The improved system then returns to the environment and generates the experience for the next round, consolidating learned distinctions as external muscle memory. The framework operates with a small number of real episodes, without expert demonstrations, environment modification, sandboxing, or parallel simulation. Experiments in Snake, Zenless Zone Zero, and Black Myth: Wukong use a 27B decision model. Mean Snake score increases from 1.30 to 7.35. In an evaluated scenario of Zenless Zone Zero, median completion time decreases by 8.4%. In an evaluated combat scenario of Black Myth: Wukong, the evasive policy achieves 11 times the mean survival time of a stationary reference, while the offensive policy win rate rises from 0% to 66.7% across the evaluated configurations.

---

## 2. DMT-Attack: Diffusion-Prior Texture Search for Closed-Loop Vision-Language-Action Policies

**Authors:** Jun Xia, Shangwen Wang, Jun Ma, ..., Huijun Liu, Jie Yu
**arXiv:** [2611.25695](https://arxiv.org/abs/2611.25695)
**Categories:** Artificial Intelligence (cs.AI)

Vision-language-action (VLA) policies rely on visual feedback throughout manipulation, making them vulnerable to persistent texture attacks. However, optimized patterns can stand out from their surroundings, making an attack easier to notice and its carrier more likely to be inspected or removed. To address this limitation, our key insight is to search the structured image distribution of a diffusion model for natural-looking textures while using closed-loop feedback to identify task-disruptive candidates. Based on this idea, we propose DMT-Attack, a gradient-free gray-box attack that generates textures for ordinary scene objects such as tablecloths. A frozen text-conditioned diffusion model defines the search space, and an eight-expert latent proposal network is initialized from evaluated teacher latents and refined using rollout feedback. We evaluate DMT-Attack against pi_0.5 and OpenVLA-OFT across four LIBERO suites. DMT-Attack achieves a macro clean-conditioned attack success rate (cASR) of 57.9%, compared with 44.7% for UPA-RFAS and 19.7% for random natural textures. It also attains higher scene similarity and a lower clean-calibrated detector flag rate (45% versus 97.5-100% for optimized patch baselines). These results demonstrate that natural-looking textures can disrupt VLA visual feedback and closed-loop decision-making, motivating defenses that jointly assess visual appearance and task behavior.

---

## 3. Cyber-Physical RSI for AI-RAN: A Case Study

**Authors:** Binghan Wu, Kai Zeng, Zhiqi Li, ..., Joseph Sifakis, Ye Ouyang
**arXiv:** [2611.25619](https://arxiv.org/abs/2611.25619)
**Categories:** Artificial Intelligence (cs.AI)

Learned models for radio access networks (RANs) are often developed using simulation, yet their predictions can shift when exposed to physical propagation conditions, protocol behavior, and equipment implementations. This paper presents a cyber-physical recursive self-improvement (RSI) framework for AI-RAN that connects a task-oriented student model, an experiment-planning coach agent, a calibratable virtual environment, and a physical host agent. Physical measurements are organized as evidence for both model adaptation and subsequent experiment planning. We examine an implementation of the physical-feedback pathway using ping-pong handover as a case study. The system completes 12 physical executions organized into six baseline--candidate pairs, updates the student from measured outcomes, and evaluates the revised model on reserved physical configurations. In the observed short-window tests, increasing the time-to-trigger from 320 to 1280\,ms changes the ping-pong count from three to zero. The updated student achieves a grouped-validation mean absolute error (MAE) of 2.673 round trips/min, while a common three-configuration physical evaluation yields MAEs of 1.240 and 1.601 round trips/min for the pre-feedback and post-feedback models, respectively. These results characterize both the operational feedback loop and the parameter-dependent generalization behavior revealed by new physical experiments.

---

## 4. FastRoverVLA: Fast Vision-Language-Action Execution for Off-Road Autonomous Driving

**Authors:** Changtao Zhao, Yingxue Guan, Li Wang, ..., Qing Wang, Ziying Song
**arXiv:** [2611.26242](https://arxiv.org/abs/2611.26242)
**Categories:** Robotics (cs.RO); Artificial Intelligence (cs.AI)

Off-road vision-language-action (VLA) models generate scene-conditioned plans, but frequent trajectory updates can repeatedly invoke expensive multimodal inference. Reusing a prediction reduces this demand while leaving its commands exposed to changes in vehicle motion. FastRoverVLA addresses this mismatch by decoupling visual plan generation from motion-conditioned execution. Its training-free interface maintains decoded plans between visual predictions. A speed-curvature action buffer is aligned with measured motion at each update, integrated into a local trajectory, and advanced by consuming the current action. The corrected remainder is written back to the buffer, preserving motion corrections across successive updates. A bounded refresh rule normalizes speed and curvature variations within a newly decoded plan and assigns a short or long reuse budget according to the resulting plan-roughness score. The interface requires neither backbone features nor an additional learned driving policy. Over a 3 s horizon, independent real-request evaluation achieves average displacement error (ADE) and final displacement error (FDE) of 0.328/0.596 m on ORAD-3D and 0.266/0.526 m on RELLIS-3D, reducing FDE by 18.0% and 36.7% at request rates of 6.0% and 4.8%, respectively. These runs retain lower errors across four backbones and both datasets and reduce Qwen3-VL request-processing cost by factors of 16.6 and 20.8 under serial replay, while mechanism and motion-only controls identify persistent state correction as the main source of the observed accuracy benefit. The source code and evaluation materials are publicly available at this https URL.

---

## 5. A$^2$-VLA: Adapting Vision-Language-Action Policies to New Tools through Agentic Affordance Discovery

**Authors:** Chenyuan Zhou, Chaoyi Huang, Zibo Wang, Zhiyuan Li, Yong-Lu Li
**arXiv:** [2611.25656](https://arxiv.org/abs/2611.25656)
**Categories:** Robotics (cs.RO); Artificial Intelligence (cs.AI)

Tools with different shapes can have similar functions, but transferring manipulation skills across tools requires understanding how tool geometry relates to the specific task and adjusting the manipulation strategy accordingly. The key challenge is to discover the common affordances that contribute to task completion across different tools and verify whether they support new tools in performing similar work. We present A$^2$-VLA, a tool-adaptation framework that combines an embodied agent with a VLA policy. It treats tool affordances as hypotheses the agent can construct, test, and revise. Given teleoperated demonstrations with a few source tools, the agent reconstructs the scenes in simulation and autonomously determines task-relevant affordance features: functional regions and their key geometric properties. It develops affordance-extraction skills and refines both the features and skills through autonomous experiments in the reconstructed scenes. Validated extraction skills accumulate in a reusable skill library for unseen tools. Finally, A$^2$-VLA uses encoded functional-region features as conditioning inputs to a $\pi_{0.5}$ backbone during training and inference. Evaluation examines affordance reliability in reconstructed scenes and real-robot task success on unseen tools. Our method achieves 86.1% success in simulated cross-tool trajectory retargeting based on affordances. On three real-robot tool-use tasks, A$^2$-VLA improves task success by 30.7 percentage points over $\pi_{0.5}$.

---

## 6. Dune: A Zeroth-Order Optimizer with Time-Conditioned Historical Error Regression for VLA Test-Time Adaptation

**Authors:** Chengyang Dong, Ze Chen, Kai Ye, ..., Ruize Han, Jialong Sun
**arXiv:** [2611.25400](https://arxiv.org/abs/2611.25400)
**Categories:** Robotics (cs.RO); Artificial Intelligence (cs.AI)

Test-Time Adaptation (TTA) enables Vision-Language-Action (VLA) models to handle distribution shifts during deployment without source-domain retraining. However, backpropagation-based adaptation incurs heavy memory overhead on resource-constrained robots, whereas zeroth-order (ZO) methods suffer from high estimation variance under limited perturbation budgets. We observe that while ZO estimation enables low-memory adaptation with rapid initial gains, it often stalls or degrades over long-horizon updates due to noisy gradient estimates. To address these limitations, we propose Dune, a zeroth-order optimizer that stabilizes long-horizon adaptation by coupling online historical error prediction with current perturbation observations. Specifically, Dune learns a lightweight, time-conditioned error predictor from past optimization dynamics and fuses its predictions with instantaneous ZO estimates, achieving effective variance reduction without backpropagation or extra forward passes. Additionally, we theoretically characterize how estimation variance restricts convergence in high-dimensional, small-population regimes, motivating the use of historical statistics. Extensive experiments on LIBERO and real-world robots demonstrate that Dune achieves superior success rates under a low memory footprint, with ablations confirming improved closed-loop stability and post-disturbance recovery.

---

## 7. PhyDEX: A Benchmark for Physical Reasoning in Vision-Language-Action Models via Dynamic Extrinsic Dexterity

**Authors:** Hao Vo, Taisei Hanyu, Yuki Ikebe, ..., Anh Nguyen, Ngan Le
**arXiv:** [2611.26565](https://arxiv.org/abs/2611.26565)
**Categories:** Robotics (cs.RO)

Vision-Language-Action (VLA) models have advanced rapidly in language-conditioned robotic manipulation, yet existing benchmarks mainly evaluate gripper--object contact and largely ignore how objects interact with the environment through gravity, friction, inertia, and mass distribution. As a result, it remains unclear whether current policies truly understand physics or merely interpolate from their training data. We address this gap through the lens of dynamic extrinsic dexterity and introduce PhyDEX, a throwing benchmark in which a robot must infer an object's mass, center of mass, and friction to send it to a destination beyond its kinematic workspace. PhyDEX contains 35K trajectories (143 hours) across nine tasks and 100 scenes, covering uniform, irregular, and dynamic-mass objects with static, multiple, and moving destinations. All data are generated by a scalable, fully automatic pipeline that combines grasp generation, motion planning, and closed-loop throw optimization under randomized physical properties. We evaluate three representative VLAs, GR00T N1.7, DynamicVLA, and ForceVLA, and find that all achieve success rates below 3\%. Our analysis reveals two key bottlenecks: limited robustness of pretrained models, which causes most failures before the throw, and physical blindness, as providing ground-truth physical properties roughly doubles success. Experiments on a humanoid robot and in the real world show the same failure patterns. We hope PhyDEX will drive the development of physically grounded robot policies.

---

## 8. TacInno: Teaching Vision-Language-Action Models the Contact Dynamics Beyond Vision and Action

**Authors:** Weile Li, Yunfan Lou, Muqing Shi, ..., Xiyu Zhu, Zhibo Pang
**arXiv:** [2611.26405](https://arxiv.org/abs/2611.26405)
**Categories:** Robotics (cs.RO); Computer Vision and Pattern Recognition (cs.CV)

Vision-Language-Action (VLA) models have recently been equipped with tactile sensing to perceive visually subtle contact events in contact-rich manipulation. However, adding tactile input yields inconsistent gains, and some visuo-tactile VLA models rely little on tactile input, because much of the tactile change, such as the gel deformation during gripper closure, is predictable from visual observations and executed actions. To address this problem, we introduce TacInno, which isolates the contact dynamics that vision and executed actions cannot explain, termed tactile innovation, and uses tactile innovation only as a training target. Specifically, the TacInno tokenizer, conditioned on visual observations and executed actions, compresses the future tactile change into a discrete code, and the policy, TacInno-VLA, learns to predict the code, adding no module for the code at deployment. TacInno-VLA achieves average success rates of 87.5% across six simulation tasks and 70.5% across four real-world tasks, outperforming the strongest visuo-tactile baseline by 10.7 and 9.0 percentage points, respectively. Ablation studies validate the contributions of visual and action conditioning, multi-frame encoding, and auxiliary code prediction. Together, these results demonstrate the effectiveness of tactile innovation as a supervision signal for contact-rich manipulation.

---

## 9. Beyond the Sink Interpretation: Radial Attention in Flow-Based VLA Policies

**Authors:** Yuxi Zheng, Yueqian Lin, Yudong Liu, ..., Hai Helen Li, Yiran Chen
**arXiv:** [2611.26385](https://arxiv.org/abs/2611.26385)
**Categories:** Robotics (cs.RO)

Prior work calls the high attention on the first and last action tokens of a flow-based VLA policy a radial action sink, and uses these tokens to set the execution horizon. In language models, a sink is a token with high incoming attention, a small value, and little effect on the output. We test whether that profile holds, not the horizon rule, in one $\pi_{0.5}$ checkpoint on five RoboCasa tasks. The two endpoints receive 5.4% of action-key mass, 1.4 percentage points above their uniform share, and rotary positional encoding produces this excess: directly in shallow layers and through upstream action-token RoPE deeper in the network. The endpoints do not fit the sink profile. Their value norms stay near the action-token mean in all 18 layers. On 250 paired episodes, masking them or zeroing their values changes success by less than 4 points, and replacing their value directions with those of another observation lowers it by 3.2 to 7.2 points across three donors, whereas the same replacement on two non-endpoint tokens in the executed prefix lowers it by 28.4 points. The token that does fit the sink profile on mass and value norm is the prefix BOS; on this checkpoint, zeroing its value raises success in two paired runs, by +13.2 points (95% CI [+7.0, +19.4]) and +6.0 points ([+0.2, +11.8]). Inside the action chunk, a relative-offset routing profile estimated on other tasks keeps 75% of action-token spread and keeps closed-loop success on three held-out tasks (42.7% against a 38.7% baseline), while uniform or shuffled routing drops success to 3-4%. High attention mass alone does not tell what a token does.

---

## 10. Reasoning on Call: Efficient Agentic Robot Control for Long-Horizon Robot Manipulation

**Authors:** Zilang Cen, Chao Tang, Fangcheng Liu, ..., Tingguang Li, Xiaoyuan Zhang
**arXiv:** [2611.26341](https://arxiv.org/abs/2611.26341)
**Categories:** Robotics (cs.RO)

Large multimodal models can support long-horizon robot manipulation, but frequent model calls incur substantial latency and token costs. The central challenge is determining when agent assistance or intervention is needed and whether errors require correcting robot execution, subtask planning, or both. To address this problem, we propose RoC (Reasoning on Call), an efficient framework that coordinates a low-level policy and a high-level reasoning agent through an online task-state monitor. The monitor combines temporal visual observations with ordered interaction memory to jointly estimate progress within the active subtask and predict its successor. These predictions guide event-triggered agent review for coordinated execution repair and plan revision. Verified outcomes govern memory updates and subtask transitions, allowing routine execution to remain with the policy while reasoning focuses on decisions requiring additional assessment. On RMBench, RoC improves task success rate by 24.0 percentage points and reduces token consumption by 65.3% compared with the strongest agent-based baseline. It also outperforms the strongest policy-based baseline by 15.1 percentage points in task success rate. Real-world experiments further validate its effectiveness across three long-horizon manipulation tasks. Overall, RoC supports efficient agent intervention and coordinated recovery across execution and planning for long-horizon robot manipulation.

---

## 11. Teaching Vision-Language-Action Models to Stop Safely

**Authors:** Zheyuan Liu, Chuhan Wang, Jinduo Guo, ..., Ningshan Ma, Meng Jiang
**arXiv:** [2611.26239](https://arxiv.org/abs/2611.26239)
**Categories:** Robotics (cs.RO)

Vision-language-action (VLA) models enable robots to perform diverse tasks from visual observations and language instructions. While prior work has explored task suppression and refusal, stopping prohibited behavior once execution is underway and controlling the resulting physical response remain challenging. Our evaluation reveals that policies which suppress a task from its initial state can still complete it when taking over partway through execution. Even when the task remains unfinished, the robot may drop a held object, making non-completion an incomplete measure of safety. To address these challenges, we introduce State-Aware Fallback Imitation (SAFI) for tasks where holding provides an appropriate alternative response. SAFI comprises two stages, (1) fallback target construction, which assigns stationary arm commands and consistent gripper targets throughout prohibited-task demonstrations, and (2) joint policy adaptation, which learns these targets alongside the original actions of retained tasks. This supervision teaches an explicit alternative response at intermediate execution states while maintaining the robot's other skills. Extensive experiments with OpenVLA-OFT across LIBERO and BadLIBERO tasks evaluate prohibited completion, physical incidents, and retained-task performance. On the evaluated LIBERO tasks, SAFI reduces aggregate target success after takeover to 1.3\%, with no recorded physical incidents or action saturation, while preserving high retained-task success.

---

## 12. One View, One Action: Spatially Generalizable VLAs through Observation-Aligned Experts and Cross Graph Consistency

**Authors:** Jinxi Liu, Ruifeng Zhai, Hao Liu, Guangrun Wang
**arXiv:** [2611.26161](https://arxiv.org/abs/2611.26161)
**Categories:** Robotics (cs.RO)

Multi-view vision-language-action (VLA) models still face challenges in spatial generalization, particularly under changes in camera viewpoints and robot initial states. These models typically receive action supervision only in the robot base frame, requiring them to implicitly learn the spatial correspondence between observations from each view and base-frame actions. We propose One View, One Action (OVOA-VLA), which learns to predict actions in each view's camera frame, allowing the same physical motion to provide diverse, observation-aligned supervision across views. OVOA-VLA jointly trains a base-frame expert and view-specific action experts, whose robot-state inputs and action targets are expressed in their respective camera frames. Two complementary directed attention graphs model both directions of interaction between the base and view-specific experts, jointly leveraging view-specific action supervision to improve base-frame prediction. Cross Graph Consistency further encourages agreement between the two graphs' base-frame predictions for the same sample. With the same multi-view inputs, the model supports both full and base-only inference. Experiments across multiple simulation benchmarks demonstrate improved manipulation performance and robustness to camera-viewpoint and robot-initialization perturbations. Full and base-only inference achieve average success rates of 88.1% and 85.7% on LIBERO-Plus, respectively. In real-world evaluations, base-only inference raises the average success rates from $\pi_{0.5}$'s 28.3% to 58.3% across three tasks under spatial distribution shifts.

---

## 13. CauSyncVLA: Causal Latent World Modeling for Asynchronous Robot Control

**Authors:** Xu Pan, Chubin Zhang, Xingrui Yu, ..., Bo An, Ziwei Wang
**arXiv:** [2611.25667](https://arxiv.org/abs/2611.25667)
**Categories:** Robotics (cs.RO); Computer Vision and Pattern Recognition (cs.CV)

Vision-Language-Action (VLA) policies must react while visual inference is still running. Overlapping computation and execution reduces waiting, yet leaves perceptual memory stale and successive action chunks disconnected. We present CauSyncVLA, an asynchronous dual-system controller that aligns perceptual-memory prediction and trajectory correction with actual robot execution. Rather than forecasting pixels or physical states, a Causal Latent World Model predicts current perceptual memory from delayed visual anchors and executed state-action history, supervised through action-sensitive distillation to retain the frozen expert's control response. Conditioned on this updated memory, Predictive Flow Warm-Starting (PFWS) aligns the unexecuted action horizon for single-step flow correction without extra training. On LIBERO-10, CauSyncVLA reaches 93.8% success at 5.04$\times$ inference throughput, improving closed-loop robustness and robot motion smoothness.

---

## 14. WEVO: World Model-Enabled VLA Optimization for Whole-Body Loco-Manipulation

**Authors:** Qianzhong Chen, Muyuan Lin, Yuyin Sun, ..., Cheng-Hao Kuo, Roberto Martín-Martín
**arXiv:** [2611.25251](https://arxiv.org/abs/2611.25251)
**Categories:** Robotics (cs.RO)

Reinforcement learning (RL) can improve vision-language-action (VLA) policies beyond imitation, but humanoid exploration is unsafe and simulator RL can exploit residual sim-to-real gaps. We present WEVO, a teleoperation-free framework for post-training a whole-body humanoid VLA in an action-conditioned video world model (WM). Simulated manipulation and locomotion play data improve contact-dynamics and viewpoint-change prediction. A VLA trained on synthetic demonstrations collects 20 autonomous real robot rollouts per task to align the WM with deployment observations. The VLA, whole-body controller (WBC), and video WM then form a closed-loop RL environment with dense progress rewards. Across three real robot tasks, play data improves every evaluated WM metric and downstream policy success; video WM RL raises mean success from 23.3% to 75.0%, compared with 48.3% for real robot RL. We therefore leverage the complementary strengths of both environments: simulation provides policy initialization and broad coverage, while the video WM offers a deployment-aligned environment for policy improvement. Project website: this https URL.

---

## 15. Risk-Controlled Test-Time Adaptation for Vision-Language-Action Models

**Authors:** Zixuan Liu, Hashem Haghbayan, Zizhan Zheng, Siavash Khajavi
**arXiv:** [2611.26438](https://arxiv.org/abs/2611.26438)
**Categories:** Computer Vision and Pattern Recognition (cs.CV)

Retrieval-augmented vision-language-action (VLA) models enable efficient test-time adaptation by leveraging expert demonstrations as additional context without updating model parameters. However, even when retrieved demonstrations are relevant to the current task, the VLA may fail to effectively utilize the retrieved information, ultimately leading to task failure. To address this challenge, we propose R2-VLA, a risk-controlled retrieval-augmented VLA framework that enables reliable test-time adaptation by satisfying a user-specified task success rate requirement with minimal expert assistance. Specifically, R2-VLA learns an uncertainty predictor that estimates the uncertainty of the VLA's predicted actions given the retrieved demonstrations, guiding when to act autonomously or request expert assistance. We further introduce a task-level risk-control procedure that calibrates the uncertainty threshold to satisfy a user-specified task-failure risk requirement. Moreover, R2-VLA continually incorporates expert corrections into its retrieval memory to improve future adaptation while preserving the prescribed task-level risk guarantee. Experiments across three VLA backbones and four LIBERO benchmark suites demonstrate that R2-VLA improves average task success by 9.2--11.2 percentage points, achieving the desired target with fewer expert requests. These results highlight the effectiveness of connecting the usefulness of retrieved demonstrations with task-level risk control to enable successful robotic manipulation.

---
