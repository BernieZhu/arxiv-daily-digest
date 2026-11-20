# arXiv Daily Digest — 2026-11-19

**Mode:** direct
**Categories:** cs.AI, cs.LG, cs.RO, cs.CV
**Keywords:** VLA, RSI, agentic robot, self-improving robot, self-evolving robot, robot harness
**Papers found:** 19

---

## 1. EVA-RSI: Recursive Self-Improvement of Video Evaluators for Judging Temporal Quality

**Authors:** Yu Yuan, Ruizhou Ding, Shaoheng Fang, Stanley H. Chan, Zhuo Chen
**arXiv:** [2611.23890](https://arxiv.org/abs/2611.23890)
**Categories:** Artificial Intelligence (cs.AI)

Video evaluators play an important role in video generation, yet they miss motion defects, limiting the quality of generated videos. Recursive self-improvement (RSI) has made strong progress in mathematics and coding, where explicit verifiers provide reliable feedback on a single goal. Video evaluation poses two difficulties for RSI: it has no verifier, and it must judge many dimensions at once, such as physics, smoothness and dynamics, where a gain on one can cost another. We introduce EVA-RSI, a multi-agent framework for exploring RSI under these two constraints. We build a fixed proxy exam with construction-defined targets by applying controlled changes to videos, such as temporal reversal and frame dropping. These edits supply supervision without human annotation. A small set of human-labeled real videos anchors the exam to human judgment. Each dimension has an LLM agent that proposes improvements. A leader agent coordinates the proposals, and a Nash bargaining rule selects updates that balance progress across dimensions. Humans design the exam, review candidate changes and revise the curriculum between stages. Starting from Qwen3-VL-8B, EVA-RSI improves motion evaluation, with the largest gain on smoothness, and the gains carry over to defect types never seen during the run. On the dynamics subsets of public benchmarks, our evaluator achieves the highest observed scores among 21 tested models. As an RL reward, it increases generated motion and earns human preference. A data-selection pipeline incorporating it also increases motion.

---

## 2. RoboBuilder: Agentic Robot Co-Design with Real-world Video Feedback in the Loop

**Authors:** Ghadi Nehme, Dahyun Nam, Akshay Govind Srinivasan, Faez Ahmed
**arXiv:** [2611.23855](https://arxiv.org/abs/2611.23855)
**Categories:** Artificial Intelligence (cs.AI); Computer Vision and Pattern Recognition (cs.CV); Robotics (cs.RO)

Can AI agents design robots that work in the real world? We introduce RoboBuilder, a benchmark in which coding agents co-design a robot's hardware and program from standard parts, motors and a custom 3D-printed part, and every design that passes in simulation is built and tested on a physical course. Simulation alone is not enough: under public part data, none of 15 initial passing designs crossed the real course, so an agent learns the simulator from measurements it requests and videos of real runs. Across four frontier coding agents, ten obstacles at three difficulty levels, 16,427 simulations of 12,774 distinct robots and 135 physical robots built in an estimated 240 hours, agents solve nearly all easy obstacles and invent mechanisms our search baselines do not reach, but falter at harder levels, when one robot must cross every obstacle, and in the real world, where 66% of simulated passes hold across all levels. Closing the loop helps: shown a video of its real failure, an agent redesigns the robot, sometimes correcting its simulator, and removes 72% of level-1 and level-2 failures. RoboBuilder measures progress toward agents that engineer real machines. Project Page: this https URL

---

## 3. GUARD: Stabilizing Recursive Self-Improvement with Regret Guidance

**Authors:** Minghe Zhang, Xuetao Kang, Yifei Ming, ..., Yufan Zhuang, Chen-Yu Lee
**arXiv:** [2611.23476](https://arxiv.org/abs/2611.23476)
**Categories:** Artificial Intelligence (cs.AI); Machine Learning (cs.LG)

Autonomous AI agents pair a frozen base model with an editable harness of prompts, skills, tool rules, and memory. Recursive self-improvement (RSI) adapts this harness from experience without weight updates, yet self-editing without external graders often backfires: reflection and scalar scores conflate what an edit newly broke with what remains unsolved, causing local regressions, skill forgetting, and memory bloat. We introduce GUARD (Grader-free Unsupervised Environment Design [UED] with Adaptive Rule Distillation), a closed-loop framework for reference-free continual harness evolution. Our key insight is to decompose each task into pre-execution self-checks and guide harness updates via directional regret. Each round grades trajectories against these checks, pinning mastered rules while prioritizing newly broken behaviors, and selects among parallel candidate edits by critic-free group-relative fitness. A Soft-HURT gate then promotes an edit only when gains outweigh regressions, scoping specialized fixes to prevent over-triggering and guaranteeing non-regression on its gated buffer. At test time, one frozen harness runs in a single pass. Across benchmarks on memory, skill evolution, continual task streams, and domain reasoning, GUARD consistently improves performance without catastrophic forgetting or memory pollution while substantially cutting deployment token usage.

---

## 4. Piccolo: Co-Evolving Decision Models and Data through Recursive Self-Improvement

**Authors:** Zhenqing Ling, Qirui Jiao, Daoyuan Chen, ..., Bolin Ding, Jingren Zhou
**arXiv:** [2611.24651](https://arxiv.org/abs/2611.24651)
**Categories:** Computation and Language (cs.CL); Artificial Intelligence (cs.AI); Computer Vision and Pattern Recognition (cs.CV)

We present Piccolo, a family of multimodal decision models (0.8B to 27B) that coevolves model capabilities and training data via Agentic Data Engineering and recursive self-improvement (RSI). The models predict probabilities over candidate answers for general-purpose text and visual judgments, agent harnesses, data workflows, and interactive games. Piccolo-27B tops the Decision Index Vision Full leaderboard with a score of 75.59, while Piccolo-9B and Piccolo-4B achieve 68.35 and 67.46, respectively. All three rank first on the Private benchmark in their respective model-size categories. Research agents analyze model behavior, construct training data, conduct experiments, and use the results to refine subsequent proposals. Semantic slices and a shared research memory connect these actions across the model family's development. With training recipes comprising hundreds of thousands of examples, data selection and feedback-driven refinement are central to the self-improvement process. Our large-scale RSI exploration yields three counter-intuitive insights for decision-model development: (1) Backbone-recipe co-adaptation outweighs raw model recency: earlier backbones can surpass newer generations on visual tasks under identical recipes; (2) Targeted data curation enables 4B-9B models to rival 27B baselines on specialized workflows; and (3) Continuous loss reduction can decouple from and even degrade discrete decision accuracy. Together with the released weights and tools from the Data-Juicer and AgentScope ecosystems, Piccolo provides an actionable blueprint for building frontier decision models and scaling data-driven RSI.

---

## 5. BaseRSI: Recursive Self-Improvement of a Base Vision-Language Model via Training-Free Harness Internalization

**Authors:** Mingda Zhang, Yuanhao Dong, Qiang Huang, ..., Pinjia He, Xiaoying Tang
**arXiv:** [2611.24578](https://arxiv.org/abs/2611.24578)
**Categories:** Computer Vision and Pattern Recognition (cs.CV); Artificial Intelligence (cs.AI)

Recursive self-improvement (RSI) is moving from the harness of prompts and tools around a base model toward the model itself. However, existing RSI still faces key challenges, including harness-bound gains that stay outside the base model, black-box supervision that reads only the model's outputs, and imprecise edits whose site and strength are fixed in advance. To address these challenges, we propose BaseRSI, a new paradigm of Recursive Harness Internalization: the base model improves its harness, then writes what the harness adds into its own weights through training-free edits, round after round on its own responses. To support this paradigm, we introduce ReGap, a mechanism that supervises every transformer block with the high-dimensional activation difference that the harness makes at that block alone, and updates the block's weights along this signal in a low-dimensional subspace. Building on this mechanism, we further propose ReKey, an algorithm that writes this signal by regression into a few key-value neurons of every block, and measures the site and strength of each edit on the model's own responses. Moreover, the base model fills every role of this recursion with forward passes alone, and its edits, written at different sites, compose in one checkpoint without refitting. Experimental results on ten visual reasoning benchmarks show that BaseRSI consistently improves a base vision-language model both in distribution and on held-out benchmarks. Our code is available at this https URL.

---

## 6. Towards Pose-Robust Few-Shot Vision-Language-Action Models

**Authors:** Wenhao Li, Zhongyi Han, Yuhao Wei, ..., Yilong Yin, Liqiang Nie
**arXiv:** [2611.24360](https://arxiv.org/abs/2611.24360)
**Categories:** Robotics (cs.RO); Artificial Intelligence (cs.AI); Computer Vision and Pattern Recognition (cs.CV)

Fine-tuning a vision-language-action (VLA) model on a few dozen demonstrations is the standard way to put a manipulation policy on a robot, yet the resulting policy silently assumes that the camera and the robot base stay exactly where they were during data collection: a bumped tripod or a base re-docked a few centimetres away makes it reach for the wrong place. We show that both failures are one phenomenon, a change of the camera-to-base extrinsic that the policy has memorised, and that the robot carries everything needed to undo it. We introduce WACO, a world-anchored canonicalization framework for VLA models: the arm, placed by forward kinematics at the measured joint angles, serves as a metric calibration target, and the static scene serves as the world anchor that tells a moved camera from a moved robot. From a single RGB-D frame, WACO estimates both shifts without ground-truth extrinsics or extra data, canonicalises the image to the calibration viewpoint and the state, action and start pose to the calibration base frame, and fine-tunes the unmodified policy under the artefacts of its own estimator. We also introduce LIBERO-PoseShift, the first benchmark for RGB VLAs with graded camera, base and compound shifts. Across LIBERO-PoseShift, the LIBERO-Plus camera track and four real-world tasks on a UR5e robot, WACO consistently outperforms the standard few-shot recipe and prior viewpoint-robust methods, raising shifted success by 13.2 points in simulation and by 36.7 points on the real robot, recovering 90% of the simulation gap to a ground-truth oracle and 87% of the real-robot gap, and establishing a new state of the art among methods that use no perturbed training data, with no test-time calibration. Project page: this https URL.

---

## 7. AeroRSI: Recursive Self-Improvement for Aerial Vision-Language Navigation

**Authors:** Shiwei Wu, Yuwen Pan, Zhi Li, ..., Xuemiao Xu, Yu Liu
**arXiv:** [2611.24077](https://arxiv.org/abs/2611.24077)
**Categories:** Computer Vision and Pattern Recognition (cs.CV); Artificial Intelligence (cs.AI); Robotics (cs.RO)

Vision-language-action (VLA) models enable unmanned aerial vehicles (UAVs) to follow natural-language instructions, yet still fail frequently in closed-loop flight. Correcting these failures requires repairs, i.e., actions that avoid them at the states the policy itself reaches, which human pilots cannot label at scale and rule-based planners cannot supply reliably. In this paper, we present AeroRSI, a recursive self-improvement framework in which an aerial navigation policy iteratively learns from its own failures. Our key insight is that a failing policy should judge its own repairs by flying on from them. Judged in this way, its sampled actions and even rule-based proposals that hurt it when imitated directly become reliable supervision. Moreover, an episode terminates at its first failure, concealing subsequent failures until the earlier ones are repaired. AeroRSI thus renews its supervision in every round, anchoring the failures of the current policy, verifying repairs by its continuation, and distilling them while keeping its behavior elsewhere. On TravelUAV, three rounds raise the success rate of a supervised 2B-parameter policy from 46.4% to 67.5% and reduce collisions by half, surpassing the previous state of the art by 10.6 points from the same initialization without extra human labels or inference cost. Code and models are available at this https URL.

---

## 8. RePlan-VLA: Progress-Aware Replanning for Long-Horizon Vision-Language-Action Models

**Authors:** Apoorva Vashisth, Manav Kulshrestha, Damon Conover, Zachary Kingston, Aniket Bera
**arXiv:** [2611.23843](https://arxiv.org/abs/2611.23843)
**Categories:** Robotics (cs.RO); Artificial Intelligence (cs.AI); Machine Learning (cs.LG)

Vision-Language-Action (VLA) models have emerged as a promising paradigm for general-purpose robotic manipulation, yet their performance often degrades on long-horizon tasks that require multiple interdependent manipulations. Instead of burdening the VLA policies with long-horizon reasoning, memory, action generation, progress tracking, and error recovery, we argue for leveraging their short-horizon manipulation capabilities within an execution-aware framework. To this end, we introduce \textnormal{\textbf{RePlan-VLA}}, a VLA-agnostic framework that translates a VLA's short-horizon capabilities into reliable long-horizon execution. RePlan-VLA explicitly monitors the robot's motion for progress evaluation, and adaptively revises the future plan based on observed outcomes. We preserve the underlying VLA policy entirely, requiring no additional fine-tuning. Experiments on RoboCasa365 and CALVIN benchmarks show an improvement of 21.9% and 10.4% in success rate over the next strongest baseline. We also validate our approach for real-world deployment on a Franka Research 3 robot.

---

## 9. Safe Personal RSI: Evaluating and Repairing Personal-Agent Updates

**Authors:** Jiapeng Pei, Yuhang Yao, Sitan Liu, ..., Tianyu Shi, Shangding Gu
**arXiv:** [2611.23651](https://arxiv.org/abs/2611.23651)
**Categories:** Software Engineering (cs.SE); Artificial Intelligence (cs.AI); Computation and Language (cs.CL)

Kicker is a personal health assistant. Changes to an assistant's reusable instructions can improve task handling while changing what it discloses, which requests it follows, and how it reports actions. We study Safe Personal RSI, an update-evaluation component developed for Kicker. We restrict recursive self-improvement (RSI) to prompt updates, with model weights and runtime code fixed. The procedure tests proposed and current instructions, repeats failing cases, temporarily undoes changes to guide repairs, and checks safety and task performance before adoption. If no version passes, the current instructions stay in use. Our executable benchmark contains 29 email, calendar, health, and marketplace cases, with separate probes for authorization reuse, memory, and tool-output injection. Across three models and two deliberately risky edits, the procedure rejects 20 of 21 update attempts. In repair confirmation, an admitted GPT-5.6 Luna repair reduces attack violations from 10.7% to 0% and increases safe task completion from 89.7% to 100%; a broad handwritten authority rule matches these outcomes. Under stronger attacks, a repair transferred from Qwen2.5-7B-Instruct to Qwen3-14B reduces violations from 69.0% to 17.9% and increases safe task completion from 19.5% to 64.4%. Separate runtime probes examine memory-entry deletion and identify missing local OAuth scope checks in the evaluated snapshot.

---

## 10. RSIBench-Infra: Can Agents Optimize Their Own Training and Inference Infrastructure at Production Scale?

**Authors:** Hanlin Wu, Yifei Wang, Zhicheng Cai, ..., Jingjing Liu, Hao Zhou
**arXiv:** [2611.24395](https://arxiv.org/abs/2611.24395)
**Categories:** Machine Learning (cs.LG)

Improving the efficiency of training and inference infrastructure is a practical component of recursive self-improvement. Existing benchmarks for agent-driven optimization largely focus on individual software layers such as kernel, leaving unclear whether agents can deliver end-to-end performance gains under production workloads. We introduce RSIBench-Infra, a benchmark of 20 training and inference tasks spanning diverse model families and modalities, with deployments of up to 32 accelerators on NVIDIA GPUs and Ascend NPUs. Agents start from runnable baselines derived from official recipes and can modify the software stack across engine, kernel, and instruction levels. An OCI image-layer submission protocol captures these changes for reproducible deployment, while independent evaluation measures end-to-end performance under task-specific quality constraints. Across all task results, 66.2% exceed $1.10\times$ validated speedup. These results demonstrate that current agents can improve production-scale training and inference performance, but identifying effective optimization strategies and consistently translating local improvements into end-to-end gains remain challenging.

---

## 11. Meaning Reaches Object Choice but Not Completion: Where Is a VLA Vulnerable to Landmark Synonyms?

**Authors:** Ryoichi Kurihara, Kota Sunamoto
**arXiv:** [2611.24076](https://arxiv.org/abs/2611.24076)
**Categories:** Robotics (cs.RO); Computation and Language (cs.CL); Machine Learning (cs.LG)

VLA policies are fragile to rewording. Success rates alone cannot say whether a policy fails to choose the object or to complete the task, nor where in the policy to intervene. We study the released GR00T N1.7 on two LIBERO-Spatial tasks differing only in the landmark word telling which of two bowls to take. Synonyms absent from the training instructions send the policy to the bowl they name, unlike made-up words, yet complete 67.6% of one task's closed-loop episodes, against the original word's 100%. Before the connector between the vision-language model and the action generator, replacing only the landmark tokens' vectors with the other landmark's (pasting) sends nearly every episode to the other bowl. After the connector, pasting at the landmark, the remaining instruction, or the image tokens alone rarely moves the choice, but any two do. Hiding the landmark tokens from the action generator after the connector still lowers completion for the synonyms that fall short. Finetuning on diversified landmark words repairs that one task's completion for synonyms absent from finetuning; finetuning on the original instructions does not. Training only the connector on the diversified words suffices, as does copying the connector of a policy fully finetuned on them into one finetuned on the original instructions. An open-loop score on starting frames misses that weights outside the connector also carry part of the repair. For now, on this evidence, robustness to rewording should be judged in closed loop, with actions executed, intervening on both sides of the connector, scoring choice and completion separately.

---

## 12. Finetuning VLAs for Dexterous Manipulation: The Right Checkpoint Is All You Need

**Authors:** Artur Kuramshin, Charlotte Cloutier, Michael Przystupa, ..., Mohammad S. Akhter, Glen Berseth
**arXiv:** [2611.23676](https://arxiv.org/abs/2611.23676)
**Categories:** Robotics (cs.RO); Machine Learning (cs.LG)

Vision-Language-Action models have demonstrated strong manipulation capabilities. A limitation of VLA models is that most manipulation datasets focus on parallel-jaw gripper systems, making transfer to multi-finger hands challenging, particularly as teleoperation datasets are harder to collect with multi-fingered robots. In this work, we study how to best adapt VLAs to dexterous hands by pairing supervised fine-tuning (SFT) with diffusion-steering reinforcement learning (DSRL). Using $\pi_{0.5}$ and a LEAP hand, we evaluate five fine-tuning recipes across two simulation tasks using only a handful of demonstrations. Our empirical analysis yields three key insights: (1) SFT success is poorly correlated with post-DSRL success, meaning the best SFT checkpoint is rarely the most effective to steer; (2) freezing the vision-language model (VLM) and tuning only the action expert produces the most steerable policy for both training and out-of-distribution placements; and (3) low-rank adaptation (LoRA) is the least steerable approach. Consequently, we recommend an adaptation recipe that freezes the VLM, fully trains the action expert, and eschews SFT rollout success as a checkpoint selection metric.

---

## 13. $Z$-sight: Unifying Vision-Language-Action and Latent World Modeling

**Authors:** Junjie Ye, Yiqi Zhao, Muchen Xu, ..., Yue Wang, Yuliang Guo
**arXiv:** [2611.24940](https://arxiv.org/abs/2611.24940)
**Categories:** Robotics (cs.RO); Computer Vision and Pattern Recognition (cs.CV)

We introduce $Z$-sight, a unified robot foundation model that couples vision-language-action (VLA) and generative latent world modeling. Video-based world action models (WAMs) show the value of joint future-and-action generation for control, yet inherit the heavy cost of video generators. Recent latent-space policies avoid pixel generation, yet typically align intermediate features or rely on frozen target encoders, decoupling future prediction from the VLM's native feature space. $Z$-sight instead predicts the future directly in the visual token space in which its VLM perceives the present. Coupling a foresight expert and a continuous action expert with the VLM in a mixture-of-transformers, $Z$-sight jointly denoises future spatial tokens and actions at inference without pixel reconstruction or external encoders. Trained on human video and robot trajectories, $Z$-sight achieves 81.9% success on SIMPLE (+9.6 points over the strongest baseline) and 73.3% across six Unitree G1 tasks (+20.0 points) at 110 ms per chunk, while remaining competitive on tabletop benchmarks.

---

## 14. 3DTouch: A Tactile-aware VLA Model with 3D Geometric Relations for Dexterous Manipulation

**Authors:** Xin Zhang, Shiqi Zhang, Siyuan Cao, ..., Jiajun Deng, Yanyong Zhang
**arXiv:** [2611.23961](https://arxiv.org/abs/2611.23961)
**Categories:** Robotics (cs.RO)

In contact-rich dexterous manipulation, occlusion by the fingers and interacting objects obscures local geometry, preventing visual observations from fully capturing contact locations. Visually similar scenes may also differ subtly in the relative positions of interacting objects, leading to different contact states. We propose 3DTouch, a tactile-geometric conditioning approach for vision-language-action (VLA) models. 3DTouch constructs a shared 3D visuo-tactile representation by expressing RGB-D scene points and dense five-finger tactile measurements in the robot-base frame, preserving each taxel's spatial location and force vector. Hand-object and object-object relations derived from hand landmarks and pose-aligned reconstructed surfaces explicitly describe the relative arrangement of interacting entities. Together, these representations condition the VLA action expert on spatially localized contact forces and relative surface geometry, providing explicit cues for contact adjustment and object alignment. We evaluate 3DTouch on five real-world contact-rich dexterous manipulation tasks using a UR7e robot arm equipped with an XHand dexterous hand. 3DTouch improves the average success rate by 42 percentage points over the corresponding VLA baseline and by 20 percentage points over the strongest evaluated alternative. Ablation studies reveal the complementary benefits of scene geometry and spatial tactile feedback, with further gains from shared spatial grounding and explicit geometric relations.

---

## 15. GTI: Grounding Task Intent Throughout Long-Horizon VLA Manipulation

**Authors:** Tianqi Gong, Haochen Niu, Yusheng Zhao, ..., Rendong Ying, Peilin Liu
**arXiv:** [2611.23926](https://arxiv.org/abs/2611.23926)
**Categories:** Robotics (cs.RO)

Vision-language-action (VLA) models generate local actions from visual observations, language, and robot state, but long-horizon manipulation requires the global task intent to remain grounded in the currently executable context. We propose GTI (Grounding Task Intent), which uses the current observation and execution history to localize the active subtask and its execution phase. For the same local subtask, GTI generates two phase-dependent visual targets: an interaction/contact state and a local completion state. The local language instruction and the corresponding phase-specific visual target jointly condition the VLA, specifying both what to do now and what state should be reached at the current phase. During execution, anomaly monitoring and local recovery re-establish an intent-consistent execution context through rollback, re-observation, and phase re-evaluation after persistent deviation. We evaluate GTI on RoboCasa365, VLA-Arena Horizon-Long, and real-world PiPER tasks. Relative to matched Global-FT baselines, GR00T success on seen composite RoboCasa365 tasks increases from 14.6%/12.1% to 31.8%/20.4% under ID/OOD evaluation. On VLA-Arena, GTI+$\pi_{0.5}$ reaches 47.6% overall success versus 45.2% for an adapted ForeAct baseline, with gains of 5.2/6.0 percentage points on the harder L1/L2 tasks. In the three real-robot task experiments, mean full-task success increases from 21.7% to 59.2%. The results indicate that persistent semantic intent localization and phase-conditioned visual grounding improve multi-stage execution, while failure-triggered local recovery provides additional deployment-time support.

---

## 16. ExecGap: Exploiting Command-Execution Gap for Patch Attacks on Vision-Language-Action Models

**Authors:** Keke Tang, Guolin Qiu, Tianyu Hao, ..., Peican Zhu, Zhihong Tian
**arXiv:** [2611.23714](https://arxiv.org/abs/2611.23714)
**Categories:** Robotics (cs.RO)

Vision-Language-Action (VLA) models have become a powerful paradigm for robotic manipulation and show strong promise for real-world deployment, making adversarial robustness critical for reliable robot operation. Existing adversarial attacks on VLA-controlled robots mainly optimize prediction-level discrepancies or rollout-level deviations to disrupt manipulation. However, they rarely account for the fact that VLA-predicted commands are not executed directly, but must be realized through downstream control and robot embodiment. In this paper, we propose ExecGap, an adversarial patch attack framework that exploits this command-execution gap to expose embodiment-specific execution vulnerabilities. Specifically, ExecGap biases VLA-predicted task-space commands toward low-executability directions, which are estimated from kinematic inefficiency and dynamic weak actuation. This induces execution degradation, where the predicted command becomes difficult to realize effectively, thereby impairing task completion. Extensive simulation experiments across multiple VLA policies show that ExecGap induces larger command-execution mismatch and weaker realized execution than existing patch attacks. Real-robot experiments further validate that the deployed patch can induce execution degradation on physical platforms.

---

## 17. RageVLA: Augmentation-Trained Perception and Action for State-of-the-Art Robustness on LIBERO

**Authors:** Amrit Lal Singh, Smarak Kanjilal
**arXiv:** [2611.23517](https://arxiv.org/abs/2611.23517)
**Categories:** Robotics (cs.RO); Computer Vision and Pattern Recognition (cs.CV)

Vision-language-action (VLA) models look saturated on LIBERO, yet most of them fall apart on LIBERO-PRO as soon as an object moves or the instruction asks for something new. We argue that what is missing is not scale but decoupling.
In these policies, what to do is tied to where things were during training, to the scene around them and to the wording of the instruction. We cut these ties in two places. In the data, LIBERO demonstrations are re-arranged by general rules: every object and fixture is moved and rotated, tasks are carried into other environments and onto other surfaces, and every instruction is paraphrased. In the policy, a perception engine on frozen DINOv3 features, trained on this augmented data, hands the action model the scene in decoupled form: a list of objects with their positions, and a compact code of what the gripper is looking at, next to image and instruction embeddings from TinyCLIP. A flow-matching diffusion transformer, trained from scratch, acts on this view.
We call this combination of Robust Augmentation and Grounded Encoding RageVLA. With 0.21 billion parameters, RageVLA sets a new state of the art on LIBERO-PRO among VLA policies, scoring 0.72 against 0.53 for the best published model, and a larger variant reaches 0.73.
Two further tests on LIBERO-Object show that the policy acts on what it perceives. When the object positions it is given are shuffled while the camera images stay correct, its success falls from 0.965 to 0.215. When the target object is displaced by 28 cm, it still succeeds in 0.865 of the episodes, where $\pi_{0.5}$, run through the same harness, succeeds in 0.105.

---

## 18. NereidVLA: Learning to Understand and Navigate the Underwater World

**Authors:** Chenjie Zhao, Zhiliang Zhu, Quan Chen, ..., Mingwei Lin, Dejun Li
**arXiv:** [2611.24864](https://arxiv.org/abs/2611.24864)
**Categories:** Computer Vision and Pattern Recognition (cs.CV); Robotics (cs.RO)

Underwater navigation requires translating visual spatial cues into motion, yet marine vision-language datasets rarely include paired robot trajectories. We present NereidVLA, a vision-language-action model that transfers marine spatial knowledge to language-conditioned 3D navigation. We first train Sea2Know on approximately two million marine examples to learn target grounding, spatial relations, and scene structure without paired robot-motion supervision. We then adapt it using expert trajectories executed under simulated underwater vehicle dynamics. Given RGB histories and a language instruction, NereidVLA predicts discrete motion tokens that decode into local 3D trajectories for closed-loop tracking. Evaluation combines an independent six-dimensional underwater navigation understanding benchmark with offline prediction and closed-loop navigation. Under matched navigation training and execution settings, marine spatial pretraining increases simulation success from 72.4% to 84.4%. Without fine-tuning on the real test environment, NereidVLA achieves 78.75% success in laboratory-pool robot trials, compared with 47.50% for InternVLA-N1. These results show that marine spatial supervision can support downstream motion learning and physical underwater navigation.

---

## 19. Allocentric Memory, Egocentric Acting: A Dual-Frame VLA for Urban Aerial Navigation

**Authors:** Haotian Xu, Yue Hu, Zhengqiu Zhu, ..., Wenguan Wang, Quanjun Yin
**arXiv:** [2611.24247](https://arxiv.org/abs/2611.24247)
**Categories:** Computer Vision and Pattern Recognition (cs.CV); Robotics (cs.RO)

Language-goal aerial navigation requires a UAV to reach a destination specified in natural language using observations collected during flight. A key challenge is linking changing egocentric perception with spatial evidence anchored to stable locations for long-range navigation. We propose CityNav-VLA, a dual-frame vision-language-action model for urban navigation integrating dynamic egocentric context with persistent allocentric spatial memory. The UAV incrementally accumulates visual observations on a fixed north-up map initialized with geographic and landmark priors, preserving evidence across viewpoint changes. A dynamic query conditioned on the instruction, current observations, UAV state, and motion history retrieves relevant memory evidence to predict a map-frame target. A deterministic controller converts this target into body-frame commands using the UAV's current pose, connecting global reasoning with egocentric execution. To reduce target fluctuations over long horizons, early goal commitment (EGC) fixes the execution target to the coordinate-wise median of the first $K$ predictions without extra trainable parameters. On Test Unseen, CityNav-VLA reduces NE by 21.2% and improves SR and SPL by 15.8% and 30.9%, respectively. It also reduces NE by 6.2% and improves SR and SPL by 5.6% and 23.2%, respectively, relative to the former SOTA after dataset refinement. Cumulative ablations show that navigation-map features yield the largest gains, while metric coordinates further improve endpoint accuracy. With a 4B-scale backbone, inference averages 0.68 s per decision with 8.6 GB peak memory on a single A100, presenting remarkable model efficiency.

---
