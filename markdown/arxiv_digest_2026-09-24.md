# arXiv Daily Digest — 2026-09-24

**Mode:** direct
**Categories:** cs.AI, cs.LG, cs.RO, cs.CV
**Keywords:** VLA, RSI, agentic robot, self-improving robot, self-evolving robot, robot harness
**Papers found:** 9

---

## 1. MemBodied: Recurrent Associative Memory for Vision-Language-Action Models

**Authors:** Tej Deep Pala, Navonil Majumder, Bryce Goh, ..., Liming Chen, Soujanya Poria
**arXiv:** [2609.28256](https://arxiv.org/abs/2609.28256)
**Categories:** Robotics (cs.RO); Artificial Intelligence (cs.AI); Computer Vision and Pattern Recognition (cs.CV)

Vision-Language-Action models provide a strong foundation for general-purpose robot control, yet a vast majority of policies do not preserve and leverage episode-level information beyond the current observation. This limitation is consequential in history-dependent manipulation tasks that depend on information available only in past observations. Retaining past observations in context can aid in recovering this information, but at the significant cost of ever-growing, bloated context and inference latency. We thus introduce MemBodied, a fixed-size episodic memory with two complementary components: an associative state that records interactions across policy calls and an episode anchor that preserves a compact representation of the initial scene as a reference. At each policy call, the model conditions action generation on the current input and the memory components, rather than directly using past observations. Across five evaluated RMBench tasks requiring memory, MemBodied achieves $7.81\times$ the mean success rate of a stateless policy and $2.98\times$ of vanilla recurrent memory, while outperforming the strongest memory-augmented baseline by $1.3\times$ with $10\times$ fewer added parameters. On the fully observable LIBERO-Long suite, it reached 90.6%, a 5.4% improvement over the stateless $\pi_0$ policy. These findings support MemBodied as a practical alternative to expanding the policy context for history-dependent manipulation.

---

## 2. BEE: Intervention-Adaptive Real-World Reinforcement Learning with Vision-Language-Action Models

**Authors:** Weihui Zhao, Xiaohan Yan, Zunian Wan, ..., Wei Shan, Maoqing Yao
**arXiv:** [2609.27450](https://arxiv.org/abs/2609.27450)
**Categories:** Robotics (cs.RO); Artificial Intelligence (cs.AI)

Vision-language-action (VLA) models handle long-horizon manipulation, yet success hinges on a few precision-critical phases where millimeter-scale errors undo all prior progress. Online reinforcement learning (RL) can optimize exactly these actions, but free exploration is far too costly on real robots, which makes human corrections indispensable. However, existing online RL methods for VLAs either cannot incorporate such corrections or fold them into undifferentiated supervision. Yet human corrections are not uniformly noisy but reliable along some action dimensions and variable along others. Building on this, we introduce BEE, an intervention-adaptive framework for real-world RL on a frozen VLA that lets the policy go BEyond Expert imitation. We formulate human corrections not as actions to reproduce but as evidence about a constraint: a Correction Model predicts how a human would correct a given VLA proposal and how consistent the correction is along each action dimension. This predicted consistency sets the per-dimension tightness of a constraint on policy optimization. Where corrections are consistent the policy stays close to the human, and where they vary, the constraint relaxes. We evaluate BEE on three real-world manipulation tasks and one LIBERO-Pro simulation task at a matched online-data budget. BEE attains the highest success rate on every task, 91.2% on average against 57.5% for RLT and 42.1% for DSRL, and the lowest human intervention rate on all real-world tasks.

---

## 3. Less Language, More Latents: Annotation-Efficient VLAs for Driving

**Authors:** Alexey Zakharov, Kemal Oksuz, Puneet K. Dokania
**arXiv:** [2609.27747](https://arxiv.org/abs/2609.27747)
**Categories:** Robotics (cs.RO); Machine Learning (cs.LG)

Vision-language-action models (VLA) promise human-steerable autonomous driving, but their training is bottlenecked by the scarcity of frames paired with natural-language instructions: while camera streams and expert trajectories are logged at scale, language annotations (e.g., turn left at the intersection) remain scarce and expensive to acquire. To address this challenge, we introduce Latent Action Driving Annotations (LADA), a three-stage pipeline that transforms abundant unlabelled observation-trajectory pairs into a substrate for language-conditioned control. First, we train a latent action model with a vector-quantised bottleneck, producing a compact codebook of high-level vehicle intents. Second, a small language-annotated subset is used to train a vision-language translator to map observations and language instructions into this codebook. Third, we train a driving VLA on observation-latent-action pairs over the full unlabelled corpus. Using fewer than 5% of language annotations and without leveraging any auxiliary chain-of-thought reasoning or visual question answering streams, LADA achieves a Driving Score of 87.98 and a Success Rate of 70.46% on the closed-loop Bench2Drive benchmark, matching or surpassing fully supervised baselines.

---

## 4. EvoAudio: Recursive Self-Improvement for Audio Understanding

**Authors:** Yuxiang Wang, Shengbo Cai, Yingda Shen, ..., Steve Yevs, Zhizheng Wu
**arXiv:** [2609.27389](https://arxiv.org/abs/2609.27389)
**Categories:** Sound (cs.SD); Machine Learning (cs.LG)

Audio language models understand what is said far better than how it sounds. Closing this gap takes more than data. Detailed acoustic annotation is costly, labels from stronger models inherit their errors and limits, and fixed data cannot adapt as the learner improves. We therefore propose EvoAudio, a recursive self-improvement system for audio understanding. To our knowledge, it is the first to evolve the model, waveforms, questions, and difficulty in one closed loop. EvoAudio uses the current model's performance to set the focus and difficulty of the next training data. A library of audio tools then constructs questions whose answers follow from how the audio was made, providing verifiable supervision without new human annotation. Reinforcement learning updates the model, and validation decides whether it enters the next evolution round. Across 13 rounds, EvoAudio improves five models with different audio encoders and language backbones on MMSU, MMAU-Pro, and MMAR. It achieves the highest average for every backbone, raising overall performance by up to 6.3 points. The improvement unfolds over successive rounds, with each stronger model starting the next round.

---

## 5. TANDEM: Task and Motion Planning with As-Needed Demonstrations for Efficient Vision-Language-Action Model Fine-tuning

**Authors:** Samrat Sahoo, Liang Ji, Tom Silver, Yixuan Huang
**arXiv:** [2609.28314](https://arxiv.org/abs/2609.28314)
**Categories:** Robotics (cs.RO)

Human teleoperators spend substantial time demonstrating behaviors that robots can already perform autonomously, limiting the scalability of data collection for robot foundation models. Task and motion planning (TAMP) can automate many of these behaviors, but a fixed planning domain may not support every stage of a long-horizon manipulation task. We present TANDEM (Tamp with As-Needed Demonstrations for Efficient Model fine-tuning), a system that combines TAMP with selective human teleoperation to collect demonstrations for tasks beyond the planner's capabilities. Our key idea is to represent human assistance as an on-demand planning capability. Given a language instruction and visual observation, TANDEM uses pretrained vision-language models to extend the planning domain with missing predicates and human-executed magic operators. This allows the planner to interleave autonomous and human-executed stages without task-specific intervention points. After each human stage, TANDEM re-perceives the scene and checks whether the intended effects hold before resuming autonomous planning. To support fine-tuning vision-language-action (VLA) models, TANDEM also uses example pretraining trajectories to align planner-generated motions with the target model's pretraining distribution. We evaluate TANDEM on five long-horizon manipulation tasks beyond the TAMP domain's capabilities. On a representative long-horizon task, TANDEM collects 2.9x as many demonstrations as full-task teleoperation at the same human intervention time. Fine-tuning a pretrained \pi_{0.5}-DROID model on 20 TANDEM demonstrations per task increases average task success from 0% to 60% across the five tasks.

---

## 6. Dissecting Advantage-Guided Post-Training for Vision-Language-Action Policies

**Authors:** Jiahang Cao, Hanye Zhao, Hang Lai, ..., Yong Yu, Weinan Zhang
**arXiv:** [2609.28161](https://arxiv.org/abs/2609.28161)
**Categories:** Robotics (cs.RO)

Advantage-guided reinforcement learning provides a practical way to post-train vision-language-action (VLA) policies using limited robot data. However, its performance depends on several coupled choices, including how critic-derived advantages are constructed, calibrated, and used for policy training. Existing recipes often combine these choices into a single end-to-end procedure, making their individual effects difficult to identify. In this work, we dissect advantage-guided VLA post-training through a controlled empirical study that separates these design choices while accounting for their distinct estimands. We develop stage-specific offline evaluation methods to screen alternative choices efficiently, without requiring extensive real-robot policy evaluations for every possible combination. The staged evaluation identifies a modular recipe that combines temporal-difference advantage construction, group-wise calibration, and continuous advantage weighting. Across four real-world bimanual tasks, the resulting recipe improves mean task progress and success over the SFT initialization by 0.42 and 0.63, respectively. Moreover, the proposed evaluation diagnostics show an overall alignment with downstream real-world performance, supporting their use for interpreting empirical outcomes and selecting advantage-guided post-training designs in practice.

---

## 7. RegenHarness: A Robot Agent Harness with Evidence-Gated Recursive Self-Improvement

**Authors:** Kailin Wang, Haoxiang Jie, Yaoyuan Yan, Zhiyou Heng, Zhaosong Li
**arXiv:** [2609.27612](https://arxiv.org/abs/2609.27612)
**Categories:** Robotics (cs.RO)

Long-horizon robot execution requires a clear distinction between a model's proposal, a controller's termination, and verified task completion. We present RegenHarness, an evidence-gated robot-agent harness connecting task planning to heterogeneous robot skills. Its execution architecture couples a model loop for context-conditioned proposals with an agent loop for dispatch, observation, verification, commitment, and bounded recovery. Four role-isolated contexts separate planning, supervision, verification, and recovery inputs. Versioned memory distinguishes observed facts from accepted task progress, while an identity- and version-bound commit gate controls updates to trusted task state. The runtime combines duplicate-dispatch control, resource leases, and recovery budgets under explicit backend contracts, and checks the original user goal before reporting completion. To our knowledge, we are the first to introduce an evidence-gated recursive self-improvement (RSI) protocol for embodied robotic agents. Across missions, execution records motivate candidate changes to context rules, task templates, routing, and recovery policies; fixed regression checks and release authorization govern their acceptance; versioned rollout and rollback preserve configuration traceability. This RSI protocol revises the harness configuration without online model-weight updates or permission to weaken the commit gate. A real quadruped deployment documents voice-triggered warehouse navigation, panoramic inspection, visual analysis, message delivery, return, and spoken reporting through linked audio, images, trajectories, and receipts. A separate circuit demonstrates why completion depends on execution history rather than endpoint proximity alone. Together, the cases demonstrate integrated perception, physical execution, communication, and history-dependent completion in real-world robot tasks.

---

## 8. AWM-VLA: AlignedWorld Modeling for Efficient and Explainable Vision-Language-Action Policies

**Authors:** An Lanji, Dawei Liu, Jin Li, ..., Mei Chen, Yu Tian
**arXiv:** [2609.27753](https://arxiv.org/abs/2609.27753)
**Categories:** Computer Vision and Pattern Recognition (cs.CV)

Vision-language-action (VLA) models have become a powerful paradigm for generalist robotic manipulation, yet they are often reactive: the policy maps the current observation directly to an action chunk without reasoning about the long-term consequences of its decisions. Prior attempts to endow policies with world models either reconstruct future frames in pixel space---expensive and dominated by task-irrelevant detail---or decouple the world model from the policy, weakening control. We present AWM-VLA, a unified framework that embeds aligned world modeling directly inside a diffusion-transformer policy. Following the Future Latent REpresentation Alignment (FLARE) principle, we add learnable future tokens whose intermediate activations are aligned with vision-language embeddings of future observations, enabling the policy to anticipate long-term consequences while generating actions. We extend this paradigm in two ways. First, we introduce an object-centric decoupled alignment objective that predicts future object-level semantics alongside the global future embedding, improving both interpretability and multi-instruction generalization. Second, we balance the global and object-centric alignment terms against the action flow-matching loss through a principled weighting, yielding a controllable accuracy--interpretability trade-off. On RoboCasa and humanoid tabletop manipulation benchmarks, AWM-VLA outperforms prior VLA and world-model baselines by up to 21% in success rate, improves generalization to novel objects and instructions, and produces object-centric rationales that are preferred by human raters in 83 of cases. Our approach adds only a few learnable tokens to the policy and is compatible with any diffusion or flow-matching policy, making aligned world modeling an inexpensive, broadly applicable component of generalist manipulation.

---

## 9. CereVLA: Cerebellum-Inspired Consequence-Aware Residual Governance for Efficient Vision-Language-Action Execution

**Authors:** Shuai Zeng, Yuxuan Liang, Hangmiao Hu, ..., Wenxi Hong, Hang Zhao
**arXiv:** [2609.27468](https://arxiv.org/abs/2609.27468)
**Categories:** Computer Vision and Pattern Recognition (cs.CV); Systems and Control (eess.SY)

Action-chunked vision-language-action (VLA) policies improve inference efficiency, but limited feedback within committed action chunks can lead to accumulated execution errors. Residual adaptation can correct such deviations without retraining the VLA; however, existing corrections are typically optimized for reference-action consistency without explicitly considering their downstream consequences. To address this limitation, we present Cerebellum-Inspired Consequence-Aware Residual Governance (CereVLA), a unified framework that integrates lightweight residual refinement and predictive consequence evaluation into frozen VLA execution. Corrective actions are first generated by flow-based residual refinement, and their short- and interval-horizon consequences are then evaluated by a recurrent state-space model and a history-aware classifier. Residual corrections predicted to be unfavorable are selectively suppressed by a lightweight governor. Comparisons with state-of-the-art methods on LIBERO-10 and LIBERO-GOAL demonstrate the effectiveness of CereVLA. On SO-101, CereVLA increases task success from 57.5% to 90.0% and reduces mean control steps by 19.6% among successful trials, relative to the frozen SmolVLA baseline.

---
