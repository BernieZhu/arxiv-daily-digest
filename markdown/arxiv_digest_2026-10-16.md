# arXiv Daily Digest — 2026-10-16

**Mode:** direct
**Categories:** cs.AI, cs.LG, cs.RO, cs.CV
**Keywords:** VLA, RSI, agentic robot, self-improving robot, self-evolving robot, robot harness
**Papers found:** 14

---

## 1. Terminal-RSI: Recursive Self-Improving Terminal Agents via Recursive Self-Rewrite and Policy-Refine

**Authors:** Junyao Yang, Zongxia Li, Yucheng Shi, ..., Shuicheng Yan, Leowei Liang
**arXiv:** [2610.22192](https://arxiv.org/abs/2610.22192)
**Categories:** Artificial Intelligence (cs.AI)

Converting verifier outcomes into useful policy updates and partial progress into complete task resolution is crucial for terminal agents. We present Terminal-RSI, which alternates Recursive Self-Rewrite (RSR) of verified trajectories with critic-inheriting Recursive Policy-Refine (RPR). We formulate Turn-Boundary Skip-Observation GAE (TB-GAE) to retain token-specific baselines while applying decay across interaction turns. Family Dense Reward (FDR) calibrates semantic progress across task families; Success-Prioritized Reward (SPR) separates strict success from bounded partial credit. A Warm-up Critic Model, recursive critic handoff, and stage-specific learning rates coordinate the two refinement phases. The five-stage sequence from Qwen3.8-27B base model through RSR-1, RPR-1, RSR-2, and RPR-2 yields Terminal-RSI-27B: 19.84% on Terminal-Bench 4.0, 86.52% on Terminal-Bench 2.1, 16.95% on Terminal-Bench 3.0, and 79.00% on Terminal-Bench Hard. On LHTB, process reward rises from 0.21 to 0.37 and strict completion from 0/46 to 5/46; SWR100 success doubles from 3.00% to 6.00%. By recursively coupling verified trajectory rewriting with critic-inheriting policy refinement, each retained stage consolidates discovered behaviors and progressively advances the agent from partial local repairs to strict terminal verification.

---

## 2. RSIFlow: Adaptive Self-Improvement Workflows with an Evolving Meta-Agent

**Authors:** Huan Zhang, Mingju Chen, Dongxu Zhou, ..., Faguo Wu, Shiji Zhou
**arXiv:** [2610.21791](https://arxiv.org/abs/2610.21791)
**Categories:** Artificial Intelligence (cs.AI)

Large language model (LLM) agents have demonstrated strong capabilities in complex tasks, including code generation, tool use, and multi-hop question answering. Existing self-improvement methods enhance agent performance through model optimization, harness evolution, and executable artifact refinement, while recursive self-improvement (RSI) further extends optimization to the improvement mechanisms themselves. However, adapting self-improvement workflows to evolving performance bottlenecks while improving workflow orchestration through execution feedback remains a key challenge. We propose \textbf{RSIFlow}, a \textbf{R}ecursive \textbf{S}elf-\textbf{I}mprovement framework that integrates adaptive work\textbf{flow} orchestration with meta-agent capability evolution. RSIFlow diagnoses performance bottlenecks from task-agent trajectories and environmental feedback to dynamically select component-specific improvement workflows. The meta-agent then distills workflow outcomes into component-specific skills and cross-component principles, evolving its own harness to improve subsequent workflow orchestration. Experiments across six benchmarks and two backbone models show that RSIFlow achieves the SOTA average performance on all benchmarks. Ablation studies further demonstrate the contributions of adaptive workflow orchestration and meta-harness evolution. Code is available at this https URL.

---

## 3. LTM: Latent Transition Based In-Context Memory for Vision-Language-Action Models

**Authors:** Qixin Sun, WenLong Gao, Xiansheng Chen, ..., Si Liu, Pengwei Wang
**arXiv:** [2610.21362](https://arxiv.org/abs/2610.21362)
**Categories:** Robotics (cs.RO); Artificial Intelligence (cs.AI)

Robotic manipulation often requires remembering interactions that are no longer visible. We introduce Latent Transition Memory (LTM), which stores history as compact latent transitions between consecutive observations. Instantiated on $\pi_{0.5}$ as LTM-$\pi$, our method uses a frozen latent action encoder, a lightweight adapter, and causal KV caching for incremental inference without memory-specific semantic annotations or external reasoning-model calls. With DreamDojo transitions, LTM-$\pi$ achieves 58.54% success on RoboMME and 80.5% on LIBERO-Mem, performing best among baselines without external reasoning models or memory-specific annotations. Ablations support the contribution of transition content beyond temporal cues and the efficiency of delayed memory admission. Scaling RoboMME demonstrations tenfold improves success from 57.67% to 87.50%, while a Cup Swap diagnostic highlights the role of process supervision in temporal composition. Under a 200-token memory budget, success remains 84.00%, versus 87.50% without compression. Finally, real-robot counting success improves from 11.25% to 82.50%. Together, these results demonstrate the effectiveness, scalability, and efficiency of latent transition memory, highlighting its capacity for complex temporal information, bounded-context operation, and real-world robotic control.

---

## 4. REKI: Registering Knowledge in VLAs

**Authors:** Juliette Marrie, Paul Pacaud, Adrien Ramanana Rahary, Shizhe Chen, Moritz Böhle
**arXiv:** [2610.22178](https://arxiv.org/abs/2610.22178)
**Categories:** Robotics (cs.RO); Computer Vision and Pattern Recognition (cs.CV); Machine Learning (cs.LG)

We introduce REKI, a 2.4B vision-language-action model (VLA) pretrained exclusively on public data that sets a new Pareto frontier between performance and model size: on LIBERO-Plus, RoboTwin Clean2Rand and RoboCasa365, it is outperformed only by models about twice its size. REKI consists of a vision-language model (VLM) followed by a flow-matching action expert, and is pretrained on a curated mixture of public robot, egocentric human and vision-language data. Additionally, we endow it with a memory that gives the policy access to its recent past at negligible cost: a few register tokens in the action expert summarise the output of the VLM at each frame and persist in the expert's cache. This memory improves success in simulation and on real robots, and makes oscillations between poses about four times rarer. REKI uses a simple model design and training paradigm, and is optimised to be efficient at training and inference. We release the full code across data curation, training, inference and evaluation, deployment, and all pretrained and finetuned model weights: this https URL.

---

## 5. Policy-Aligned Predictive Verification for Adaptive VLA Action-Chunk Execution

**Authors:** Minkyu Kim, Junhoo Lee, Seungyeon Kim, ..., Donghoon Han, Nojun Kwak
**arXiv:** [2610.21434](https://arxiv.org/abs/2610.21434)
**Categories:** Robotics (cs.RO); Machine Learning (cs.LG)

Vision-language-action (VLA) policies generate action sequences that reduce repeated inference, but deciding how much of each sequence to execute is critical to task success. Existing adaptive methods make this decision using generation stability or prediction agreement, yet these signals do not establish whether executing a candidate prefix preserves the ability to complete the task. We introduce a policy-aligned predictive verifier (PAV) that anticipates the consequences of candidate action prefixes and evaluates their compatibility with successful continuation before execution. Rather than using future prediction to generate actions, our method evaluates existing proposals in the VLA's internal task-conditioned representation space. To learn local judgments from terminal task outcomes, we combine trajectory-level survival supervision with a localization prior that preserves useful behavior within failed rollouts. The resulting validity scores guide execution-horizon selection. Evaluations with pi_0 and pi_0.5 across LIBERO, RoboTwin 2.0, and real-world manipulation show improved success-query trade-offs. These findings point toward a different role for future prediction in robotics, using it to assess how far to trust a policy's proposed actions rather than to generate new ones.

---

## 6. A Phenomenology of Neural Geometry in Vision-Language-Action Models

**Authors:** Mozes Jacobs, Aiden Swann, Mathilde Papillon, ..., Matthew Kowal, Thomas Fel
**arXiv:** [2610.20840](https://arxiv.org/abs/2610.20840)
**Categories:** Robotics (cs.RO); Machine Learning (cs.LG)

Robotic manipulation is inherently geometric, but what shape does the world take inside the policy that performs it? Prior work on vision-language-action (VLA) policies establishes that task-relevant variables are linearly readable from activations, yet readability certifies only that a variable is present and says nothing about the shape its values trace, which may be curved and multi-dimensional. Using controlled sweeps, natural rollouts, linear probes, and activation interventions, we build a taxonomy of seven task-relevant concepts in VLA models. We find that realized geometry is predominantly multi-dimensional and is shaped by the constraints under which the policy acts. Physical joint limits, for example, leave wrist orientation an open arc rather than a circle, and distance to the target, a single scalar, is realized in two orthogonal subspaces, a coarse ruler for the approach and a fine ruler for the grasp. The same geometries reappear in two further VLA models on real-world robot data, indicating that they are neither model-specific nor artifacts of simulation. We demonstrate how the findings are actionable by steering along the geometry a concept realizes. Overall, this work lays out an initial phenomenology of realized geometry in VLA policies and demonstrates that a concept's shape carries as much importance as its readability.

---

## 7. FastVLA: Task-Conditioned and Temporally Adaptive Visual Token Compression for Efficient Vision-Language-Action Models

**Authors:** Jiuyi Xu, Chengyuan Qian, Zhengzhong Tu, Yang Sui, Yangming Shi
**arXiv:** [2610.22146](https://arxiv.org/abs/2610.22146)
**Categories:** Robotics (cs.RO)

Vision-Language-Action (VLA) models present a promising paradigm for general-purpose robot manipulation, but closed-loop deployment is often limited by inference efficiency: at each timestep, high-resolution, often multi-view images are encoded into hundreds of visual tokens that dominate transformer computation and latency. Token compression via attention is a natural solution but is challenging for VLA control because (1) decision-critical tokens are determined by the task, not generic visual saliency, and (2) the token budget varies substantially across steps, so static metrics and budgets waste computation or discard control-critical tokens. We introduce FastVLA, a training-free, task-aware, and temporally adaptive visual token compression framework. At each step, FastVLA scores token importance via task-to-vision attention and adaptively sets the compression rate from the importance-distribution uniformity, measured by an inverse-Simpson metric with online sliding-window calibration. We evaluate FastVLA on OpenVLA, OpenVLA-OFT, and CogACT across LIBERO and SIMPLER, and on a physical Franka Research 3 robot. In simulation, it reduces LLM-backbone FLOPs by 35-59\% and action latency by 9-32\% (a 1.09$\times$-1.46$\times$ speedup) while maintaining task success, achieving a comparable or better efficiency-performance trade-off than existing plug-and-play token compression/pruning/reuse baselines. On the real robot, it cuts end-to-end latency by 20\% (1.25$\times$ speedup) at comparable success. Code is available at this https URL.

---

## 8. VeriVLA: Adaptive Test-Time Verification for Flow-Based VLAs with Latent World Models

**Authors:** Xueli Sun, Yuxiang Lu, Yantong Liu, ..., Zhe Liu, Hengshuang Zhao
**arXiv:** [2610.21985](https://arxiv.org/abs/2610.21985)
**Categories:** Robotics (cs.RO)

Flow-based Vision-Language-Action (VLA) policies are inherently stochastic: different noise seeds can produce action chunks of varying quality from the same observation. At test time, however, the policy typically commits to a single sample without an explicit estimate of its quality. In fine-grained manipulation, executing a suboptimal action can irreversibly disrupt task progress and lead to failure. To exploit policy stochasticity, we introduce a training-free two-axis trigger that uses two initial samples to measure within-chunk temporal variation and cross-sample variance, detecting the critical states. Once triggered, a JEPA-based latent world model ranks candidate action chunks by predicting action-conditioned future latent states and the corresponding changes in task progress. By operating in latent space, the verifier avoids pixel reconstruction and enables efficient and more accurate ranking. Across three real-world tasks, $\textit{i.e.,}$ pen insertion, pipetting, and apple placement), our method raises the average completion score from 50.8% to 65.5%, while adding 326 ms for sampling and verification per triggered decision on a single RTX 4090. Consistent gains are also observed in simulation, where the average success rate rises from 66.4% to 73.6% in the clean setting of RoboTwin 2.0, from 62.8% to 69.6% in its randomized setting, and from 96.9% to 97.6% on LIBERO.

---

## 9. What Should Robot Policies Learn to Predict? Rethinking Supervision Targets in Vision-Language-Action Learning

**Authors:** Haitao Shen, Hanyu Liu, Yihan Lin, ..., Wenxin Li, Yuan Yao
**arXiv:** [2610.21915](https://arxiv.org/abs/2610.21915)
**Categories:** Robotics (cs.RO)

Vision-language-action (VLA) policies are typically trained with action prediction as the primary supervision signal, since robots ultimately execute actions. Auxiliary objectives such as latent-action (LA) and future-vision (FV) prediction are often added to improve policy learning, yet they compete with action prediction for the same training budget. We ask whether, under a fixed budget, allocating a substantial share of training samples to such objectives, rather than to further action prediction, can improve policy learning. We build a unified VLA framework that couples a two-stream multimodal diffusion transformer (MMDiT) with a sample-level router, which assigns each training sample to either action prediction or an auxiliary objective and thus makes supervision allocation explicit. Within this framework, we instantiate three LA targets based on LAPA and its DINO-feature variants, and three FV targets based on DINOv3, V-JEPA 2, and Wan2.2 representations. Across LIBERO, CALVIN, and four real-robot tasks, suitable LA and FV supervision outperforms action-only training under the same budget, even when action prediction receives no more than half of the training samples. FV generally outperforms LA, although the strongest LA target remains competitive on CALVIN. Diagnostic analyses suggest that DINO-based LA targets emphasize relative motion, whereas FV targets emphasize absolute position and task identity. We therefore argue that what robot policies learn to predict, and how training is allocated among these targets, should be treated as explicit design choices rather than defaulting to action-dominant training.

---

## 10. Multi-Teacher On-Policy Distillation for Flow-Based Vision-Language-Action Models

**Authors:** Lichao Ni, Yuhan Liu, Pengfei Li, Guanghuan Fang
**arXiv:** [2610.21522](https://arxiv.org/abs/2610.21522)
**Categories:** Robotics (cs.RO)

Specialized vision-language-action (VLA) policies acquire strong domain-specific skills, yet consolidating these skills into one shared policy remains challenging. On-policy distillation (OPD) transfers teacher knowledge on inputs induced by the student, addressing the distribution mismatch encountered during deployment. For flow-based VLAs, this mismatch arises at two levels: environment observations and intermediate action-generation states. We propose a two-level on-policy distillation framework that couples student-driven environment interaction with teacher velocity supervision along student-generated action flow trajectories. Frozen domain specialists jointly supervise one student. After each update, the student collects new environment experience and generates fresh action-flow trajectories. Starting from a joint supervised fine-tuning (SFT) initialization, Velocity Loss OPD yields absolute success-rate gains of 22.55% on LIBERO-40, 33.4% on CALVIN five-instruction sequences, and 22.6% on Meta-World MT50. Compared with Action Loss OPD and Teacher-rollout SFT, it achieves absolute success-rate gains of 6.4-9.5% on LIBERO-40, 9.7-18.3% on CALVIN, and 3.2-4.2% on Meta-World MT50. Analysis by sequence length further shows larger success-rate gains on longer CALVIN sequences. These results demonstrate effective multi-domain capability consolidation through two-level on-policy supervision, with a single student deployed across domains.

---

## 11. Fast-VLA: You Only Think Once for Robot Manipulation

**Authors:** Kehong Gong, Guanli Hou, Xiaoxu Zheng, ..., Mingyuan Zhang, Michael Bi Mi
**arXiv:** [2610.21389](https://arxiv.org/abs/2610.21389)
**Categories:** Robotics (cs.RO)

Vision-language-action (VLA) policies commonly place a multi-billion-parameter model inside the feedback loop, repeatedly recomputing task context whenever they predict a new action chunk. Yet task understanding changes far more slowly than the robot state. We introduce Fast-VLA, which invokes a frozen 4B VLM once per episode to contextualize the instruction and initial views as fixed, multi-layer key-value task memory. During execution, a lightweight online actor fuses learned time- and arm-indexed queries with current visual and proprioceptive feedback to form action queries. These queries retrieve task context from the fixed memory and predict action chunks without re-running the foundation model. Fast-VLA achieves 92.46% and 92.40% success on RoboTwin 2.0 Clean and Randomized, and 95.95% and 79.11% on LIBERO and LIBERO-Plus evaluation. Against three continually conditioned baselines on the same hardware, it reduces RoboTwin amortized policy inference time by 10.9-17.1x and requires 1.22 GiB of post-prefill online resident memory. Task-memory swaps further show that the actor relies on episode-matched task memory. These results show that task context can be established once while closed-loop control remains responsive throughout execution. Project page: this https URL

---

## 12. When to Ask for Help: A Decision-Theoretic Account and Measurement Standard for Slow-Module Scheduling in Dual-System Vision-Language-Action Models

**Authors:** Shilin Zhang
**arXiv:** [2610.21160](https://arxiv.org/abs/2610.21160)
**Categories:** Robotics (cs.RO)

Dual-system vision-language-action (VLA) models pair a high-frequency fast policy with a slow, expensive module, and published trigger mechanisms for invoking it lack a shared objective, measured costs, and any standard separating schedule quality from module quality. We provide the missing account: invocation is formalized as a calibrated decision problem whose fixed-ratio, fixed-budget, and history-gated schedules are degenerate cases of one quantity, the Value of Intervention (VoI); a renewal baseline proves the optimal schedule periodic under state-independent collapse, with adaptive gains governed by the cost ratio $\rho$ and the dispersion of collapse. Measured systems span three orders of magnitude in $\rho$ (FiS-VLA $0.95$; RoboICL about $10^3$), and a direct test confirms the low-$\rho$ prediction: calibrated gains vanish under homogeneous collapse and grow with heterogeneity. Fourteen closed-loop arms on LIBERO test the contested middle of the continuum ($\rho=1.53$): the adaptive trigger allocates its queries exactly as the threshold rule predicts, yet the language-rewrite channel cannot convert them into success on either suite, and a revert actuator that undoes a failed rewrite is the only intervention with zero net downside on both LIBERO-Spatial and LIBERO-Goal, where the rewrite deficit deepens from thirteen to forty-two points. A four-measure leak-free protocol cuts apparent early-warning AUC from $0.93$ to $0.62$ on $929$ deployment traces, a detection-limited frontier theorem converts detection quality into a schedulability statement, and a compilation loop turns measured value functions into per-task refresh periods within $2.4\%$ of the closed-loop oracle. Together these results turn slow-module invocation from a design opinion into a measured decision.

---

## 13. Do VLAs Really Follow Instructions? Diagnosing How-Level Instruction Following in Vision-Language-Action Models

**Authors:** Sangwu Park, Wonjoong Kim, Yeonjun In, Chanyoung Park
**arXiv:** [2610.21251](https://arxiv.org/abs/2610.21251)
**Categories:** Computer Vision and Pattern Recognition (cs.CV); Robotics (cs.RO)

Vision-language-action (VLA) models are expected to follow instructions like their language backbones, yet prior work has focused on What-level instructions that specify the task rather than How-level instructions that specify how to carry it out. Through our diagnoses, we find that How-level instructions do not help current VLAs and lower task success. We hypothesize that pairing each training episode with a single instruction limits How-level instruction following, and show that training with segment-level enriched instructions makes actions respond to such instructions without consistently raising task success. To measure How-level instruction following beyond standard benchmarks, we introduce SIMPLER-IN, where success requires conditions given only in the instruction. It shows that the gained responsiveness does not extend to demanding or out-of-distribution How-level instructions. How-level instruction following thus remains an open challenge.

---

## 14. VLA-$Δ$: Learning Physical State Transition for Vision-Language-Action Models

**Authors:** Qi Lu, Jiarun Li, Ce Zhang, ..., Wenqi Zhang, Xuhong Zhang
**arXiv:** [2610.21306](https://arxiv.org/abs/2610.21306)
**Categories:** Computer Vision and Pattern Recognition (cs.CV)

Vision-language-action (VLA) models transfer semantic knowledge acquired through vision-language pretraining to robot control, achieving strong performance across various benchmarks. However, most VLAs directly map observations to demonstrated actions without explicit supervision of intermediate physical state changes, making them prone to overfitting observation-action correspondences. Some methods introduce intermediate reasoning or future-state prediction in language, visual, or latent spaces to guide action generation, but do not explicitly supervise the physical state transition itself. We therefore propose VLA-$\Delta$, a general framework that uses physical changes between current and future states as explicit learning targets. To support this objective, we construct a large-scale pretraining dataset and derive physical state-transition annotations covering task-relevant semantics and visual motion changes, providing more direct supervision for continuous action generation. During inference, the model generates actions directly from current observations without additional inference overhead. VLA-$\Delta$ achieves performance competitive with the state of the art on LIBERO and RoboTwin, and outperforms $\pi_{0.5}$ in real-robot experiments. Our code is available at this https URL

---
