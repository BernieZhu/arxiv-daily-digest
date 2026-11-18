# arXiv Daily Digest — 2026-11-17

**Mode:** direct
**Categories:** cs.AI, cs.LG, cs.RO, cs.CV
**Keywords:** VLA, RSI, agentic robot, self-improving robot, self-evolving robot, robot harness
**Papers found:** 18

---

## 1. Bring Back Language to Actions: Restoring VLM capabilities in VLA Models via Parameter Merging

**Authors:** Mohamed Salim Aissi, Olivier Sigaud, Laure Soulier, Nicolas Thome
**arXiv:** [2611.18891](https://arxiv.org/abs/2611.18891)
**Categories:** Artificial Intelligence (cs.AI); Computer Vision and Pattern Recognition (cs.CV)

Vision-Language-Action models (VLAs) are obtained by fine-tuning pre-trained Vision-Language Models (VLMs) on robot demonstration data, enabling action prediction from visual observations and language instructions. However, this fine-tuning induces catastrophic forgetting, substantially degrading the semantic and visual grounding capabilities of the original VLM. We address this by merging the parameters of a VLM and its VLA derivative without retraining either model. Concretely, we extract the task vector (the difference between VLA and VLM weights) and decompose it via Singular Value Decomposition. For each component, we learn a scalar mixing coefficient controlling how much of the VLA adaptation is retained, optimised to jointly preserve action prediction and vision-language capabilities. Experiments show that our merged model performs well on both axes simultaneously, consistently outperforming established merging baselines.

---

## 2. Instructions Before Actions: Prospective and Retrospective Language Supervision for Driving Vision-Language-Action Data

**Authors:** Angel Martinez-Sanchez, Ross Greer
**arXiv:** [2611.20631](https://arxiv.org/abs/2611.20631)
**Categories:** Computer Vision and Pattern Recognition (cs.CV); Artificial Intelligence (cs.AI); Machine Learning (cs.LG); Robotics (cs.RO)

Driving vision-language-action (VLA) models can accept navigation instructions, yet predicting a driver's trajectory does not establish that a model follows the instruction. We study how driving-language supervision is collected and evaluated, distinguishing prospective instructions issued before an action from retrospective labels written after observing it. We develop ADVLAT-Engine to synchronize spoken instructions, road-scene video, and vehicle trajectories, and compare three navigation apps on 48 replayed routes. On 87 maneuvers announced by both Google Maps and a passenger, the passenger uses more scene-dependent language. We evaluate four open driving VLAs before and after fine-tuning on prospective navigation-app drives. Fine-tuning reduces passenger-drive trajectory error by 23-59%, but instruction effects remain inconsistent. At real intersections, counterfactual instructions reveal stronger responsiveness: fine-tuned Alpamayo~2 Super gains 31 and 18 accuracy points at 15 and 5~m, while Qwen-Drive follows alternative maneuvers more reliably with a discrete command than with a sentence. We additionally collected retrospective annotations from four people for the driving recordings and describe controlled comparisons of annotation content, timing, and downstream learning; those analyses are pending. Our findings separate maneuver prediction from instruction-following and establish a framework for comparing prospective and retrospective supervision.

---

## 3. NF-VLA: A Normalizing-Flow Baseline for Vision-Language-Action Learning

**Authors:** Ruichen Deng, Qinyu Zhao, Yong-Hyun Park, ..., Liang Zheng, Jiatao Gu
**arXiv:** [2611.20314](https://arxiv.org/abs/2611.20314)
**Categories:** Robotics (cs.RO); Artificial Intelligence (cs.AI)

Autoregressive normalizing flows (NFs) provide a tractable density for learning and sampling continuous robot actions. We show that a single maximum-likelihood objective can train vision--language--action (VLA) policies competitive with leading methods on manipulation benchmarks. We present NF-VLA, which combines conditional autoregressive normalizing flows with score-based action refinement. Its deep--shallow architecture concentrates visual, language, and proprioceptive prefix conditioning in a high-capacity deep block, while unconditioned shallow blocks provide a shared invertible action transformation. The vision--language backbone and flow are jointly trained by exact maximum likelihood on Gaussian-smoothed action chunks. The same learned density supplies a single score-based correction at inference, refining generated actions to account for training-time smoothing without a separately trained denoiser. Trained on LIBERO from a pretrained vision--language backbone without robot pretraining, NF-VLA achieves 98.35\% success across the four standard suites and 72.6\% on LIBERO-Plus using the same checkpoint without further fine-tuning. Ablations show that deep-only prefix conditioning and score-based refinement both improve closed-loop success. Together, these results establish carefully structured autoregressive flows as a competitive approach to VLA control, with one learned density supporting policy training, action generation, and refinement.

---

## 4. Right Goal, Wrong Body: Re-grounding Frozen VLAs under Actuation Shift

**Authors:** Umer Siddique, Peilang Li, Yongcan Cao
**arXiv:** [2611.20244](https://arxiv.org/abs/2611.20244)
**Categories:** Robotics (cs.RO); Artificial Intelligence (cs.AI); Machine Learning (cs.LG)

Vision-language-action (VLA) models are capable of producing desired robotic behaviors in ideal settings. However, they often fail when the robot's actuation changes at deployment. For example, remounting, mechanical wear, or command latency changes can lead to failed tasks and unsafe behaviors. To address the inevitable actuation shift, we propose ReGround, an inference-time method that keeps the VLA frozen and re-grounds its intended motion. ReGround learns the deployed robot's dynamics from task-agnostic motor babbling, and then tracks the policy's intended motion while staying close to the policy's own plan. ReGround activates only upon detecting a shift, and needs no rewards, demonstrations, or retraining. We show via two VLAs, eight LIBERO tasks, and five shift settings that ReGround can restore near-oracle success, such as raising $\pi_{0.5}$'s success from 0.16 to 0.90 under 400 ms latency, while remaining safer than a linear-calibration baseline. Project website and open-source code: this https URL.

---

## 5. ReactBench-AD: Do Driving VLAs and World-Action Models React to Imminent Hazards in Their Path?

**Authors:** Nikos Theodoridis, Reenu Mohandas, Sushil Sharma, ..., Tim Brophy, Ciarán Eising
**arXiv:** [2611.20011](https://arxiv.org/abs/2611.20011)
**Categories:** Computer Vision and Pattern Recognition (cs.CV); Artificial Intelligence (cs.AI); Robotics (cs.RO)

Vision-Language-Action models (VLAs) and World-Action Models (WAMs) have emerged in autonomous driving with the promise of strong generalization to long-tail scenarios. Although these models achieve state-of-the-art results on autonomous driving benchmarks, most existing benchmarks are dominated by nominal scenarios and therefore cannot test this promise. To test one such long-tail capability that is critical for safety, we introduce ReactBench-AD, a benchmark that measures how driving models react to objects that appear in the ego vehicle's path. Built on real NAVSIM and PhysicalAI-Autonomous-Vehicles scenes, ReactBench-AD composites a crossing pedestrian, a standing pedestrian, or a stationary car consistently across all camera views and history frames. Each edited scene thus forms an exact, pixel-level counterfactual pair with its original, which allows us to isolate the causal effect of the inserted object on the predicted trajectory. Evaluating four VLAs and two WAMs, we find that they react weakly, often barely at all. Finally, we test how easily one of the evaluated VLAs, ReCogDrive, can be taught to brake hard for imminent hazards: a short fine-tuning stage on edited scenes substantially improves its reactions, with the learned behavior generalizing to unseen objects and fully real scenes, at minimal cost to nominal driving. These results call into question the out-of-the-box long-tail capabilities of these models, but suggest that they can be a strong foundation for acquiring them with little additional training, highlighting the value of real or synthetic data that demonstrates the long-tail behaviors nominal datasets rarely contain. Code and data will be made publicly available.

---

## 6. Self-Improvement Memory Enables Continual Recursive Self-Improvement

**Authors:** Xin Yu, Fei Xia, Jiaqi Pan, ..., Lingzhou Xue, Ting Yu
**arXiv:** [2611.18856](https://arxiv.org/abs/2611.18856)
**Categories:** Machine Learning (cs.LG); Artificial Intelligence (cs.AI)

Harness optimization is often studied with a fixed policy model and benchmark. When either changes, the optimizer must decide which parts of an evolved harness to reuse or revise, but the harness alone may not explain why earlier edits were made or how they performed. In this work, we study Continual Recursive Self-Improvement (CRSI), a setting for continuing existing harness-optimization methods across compatible benchmarks or policy models. We propose Self-Improvement Memory (SIM) for the harness optimizer, rather than the task-solving policy. SIM groups edits by recurring harness problem and records their rationale, predicted and observed outcomes, and evaluation context. New attempts extend this history as optimization continues. In our experiments across four domains, SIM achieves higher final scores than harness-only and root-cause-only continuation in cross-dataset and pairwise cross-model comparisons. Across ten independent source runs in coding, paired continuations with SIM improve final scores by an average of 2.36 points over harness-only continuation ($p=0.003$).

---

## 7. RSIMed: Scaling Medical Foundation Models beyond Limited Clinical Data via Retrieval-Grounded Self-Evolution

**Authors:** Wei Dai, Qianchu Liu, Guanghui Qin, ..., Sheng Zhang, Paul Pu Liang
**arXiv:** [2611.18646](https://arxiv.org/abs/2611.18646)
**Categories:** Machine Learning (cs.LG); Artificial Intelligence (cs.AI)

Rare diseases are hard to diagnose, and the labeled clinical records needed to train models for them are few, private, and slow to extend, since a specialist must read every case. A model that writes its own training tasks could learn beyond these records, but no program can check a model-written diagnosis, and a wrong answer key corrupts training. To tackle this dilemma between data scarcity and difficulty of data annotations, we introduce RSIMed, Recursive Self-Improvement in Medicine, one of the first self-evolving pipelines in which a task proposer co-evolves in context with a diagnostic solver on real clinical records. Seeded by training admissions, a frozen copy of the solver writes each clinical question from retrieved medical evidence, so its answer rests on a source, and steers topics and difficulty toward what the solver still gets wrong. On rare-disease diagnosis from MIMIC-IV admissions, the accuracy of RSIMed-27B grows linearly with training compute, while a static pool of generated tasks collapses. Without any external model, RSIMed-27B and RSIMed-9B reach 0.516 and 0.488 diagnostic accuracy, above every off-the-shelf GPT-5.6 setting, whose best reaches 0.399 at 38 times the inference cost of RSIMed-27B. Tasks written by four external teachers, including GPT-5.5, train a less accurate diagnostician than the solver's own. Trained only on diagnosis, RSIMed-RL-27B also improves on the physician-written tasks of HealthBench Professional, from 0.291 to 0.303 in adjusted score.

---

## 8. PlanDiv: Test-Time Scaling with Latent Plans for Vision-Language-Action Models

**Authors:** Hanbo Zhang, Lianlei Shan, Liuhaichen Yang, Zezhi Tang
**arXiv:** [2611.20010](https://arxiv.org/abs/2611.20010)
**Categories:** Robotics (cs.RO); Computer Vision and Pattern Recognition (cs.CV); Machine Learning (cs.LG)

Test-time scaling improves vision-language-action (VLA) policies by drawing several action candidates and executing the best one. We find that its returns diminish quickly when the candidates are resampled from one decoder: they differ by noise rather than by plan, and for each of three resampling sources, going from four to eight candidates adds only 0.06-0.07 to the average number of completed tasks on CALVIN. We introduce PlanDiv, an action head that makes the candidates differ by plan: a lightweight planner proposes K latent plan hypotheses, a shared masked-diffusion executor decodes one action chunk per plan from a single backbone pass, and the policy executes the chunk that its own likelihood ranks highest. The plans are learned from demonstrations alone, without plan labels or rewards. With the backbone, data and training recipe held fixed, eight plan-conditioned candidates raise five-task chain success on CALVIN ABC$\rightarrow$D from 56.9% to 69.9%, while eight candidates from autoregressive, plan-free or same-plan resampling reach at most 64.9%. The same-plan baseline is PlanDiv's own checkpoint with the plan held fixed, so this gap comes from the plans, not from drawing more samples. On LIBERO-Long, four plans remove 40% of single-candidate failures, against at most 21% for matched resampling. On a real Franka arm the gain appears where a task admits more than one solution: PlanDiv is on par with a single-output OpenVLA-OFT+ baseline on a one-solution task and succeeds in 51 of 54 trials against 40 of 54 on two tasks with two solutions.

---

## 9. ScaleVLA: Scaling Vision-Language-Action Models to 552 Billion Parameters

**Authors:** Ruixi Yu, Dairu Liu, Xuchuan Chen, ..., He Wang, Li Yi
**arXiv:** [2611.21607](https://arxiv.org/abs/2611.21607)
**Categories:** Robotics (cs.RO)

Frontier Vision-Language Models (VLMs) such as GPT-6 Astra have demonstrated remarkable capabilities in robot control, suggesting that broad pretraining provides knowledge valuable for physical action. Yet most Vision-Language-Action (VLA) policies still rely on much smaller VLM backbones, leaving this potential largely untapped. We ask whether frontier-scale representations can provide a stronger foundation for robot learning. We introduce ScaleVLA, which connects a 552B DeepSeek-V4.1-Flash backbone to a trainable action DiT, and systematically compare VLMs from 2B to 552B under a shared training setup. We evaluate three fundamental capabilities of robot foundation models. In sample efficiency, just 10 demonstrations outperform a 2B backbone trained with 50 (87.8% vs. 85.6%). In generalization, LIBERO-PRO success reaches 45.1%, compared with at most 31.3% for smaller backbones. In precise manipulation, real-world charger insertion improves from 4/10 to 9/10 successes, with gains concentrated in contact-sensitive alignment. Despite its scale, ScaleVLA achieves 216 ms median latency per action chunk. Our findings suggest that frontier VLMs can serve not only as reasoning agents, but also as powerful representational foundations for efficient and generalizable robot policies.

---

## 10. Stochastic Self-Distillation for Flow-Based Vision-Language-Action Models

**Authors:** Jingru Guo, Alessandra Russo, Joey Bose, Christos Ziakas
**arXiv:** [2611.20460](https://arxiv.org/abs/2611.20460)
**Categories:** Robotics (cs.RO)

Flow-based vision-language-action (VLA) models achieve strong performance in robotics through imitation learning, yet fine-tuning them with on-policy reinforcement learning (RL) is limited. In group-based RL methods like Group Relative Policy Optimization (GRPO), every rollout step requires multi-step ODE integration, and the sampler's limited stochasticity leads to rollout groups with low variance. We propose VLA-SSD, which addresses both high inference latency and limited stochasticity. In particular, our method self-distills a pretrained flow-matching action head into a stochastic one-step policy by conditioning a single-jump generator on a Brownian path. We derive a conditional action density via our stochastic one-step policy, enabling efficient post-training via likelihood-ratio RL algorithms. We show that distilling VLA-SSD from the $\pi_0$ VLA reduces the action head's forward-pass time by a factor of 7.7, at the cost of a 5.5% relative decrease in the success rate on the LIBERO benchmark. However, by leveraging the increased sample diversity of VLA-SSD during group generation, post-training a $\pi_{0.5}$ VLA using GRPO yields a 20.6% relative improvement.

---

## 11. Ego2Sim2Humanoid: Agentic Real-to-Sim for Learning Loco-Manipulation VLAs without Robot Demonstrations

**Authors:** Chen Liu, Nikolaus Correll
**arXiv:** [2611.19196](https://arxiv.org/abs/2611.19196)
**Categories:** Robotics (cs.RO)

Imitation learning for visuomotor policies typically relies on teleoperated robot demonstrations, which are costly because every episode requires a trained operator controlling a physical robot in real time through teleoperation interfaces and wearable body-tracking hardware. Egocentric glasses capture human demonstrations without a robot or handheld grippers, yet they track only the head and in-view human hands, and directly copying human motion to a robot with different stature, arm reach and hand morphology fails to produce feasible contacts. \method{} converts egocentric glasses recordings into physically verified robot training trajectories. An agentic real-to-sim stage reconstructs collision and textured visual assets from the recorded RGB-D and head streams, completes unseen surfaces when needed, and predicts target contact bands on the manipulated objects. During motion adaptation, a grasp planner turns each contact band into a feasible robot wrist pose and finger closure, bilevel stance optimization plans collision-free standing postures that keep hand targets reachable, and a whole-body motion generator synthesizes lower-body locomotion and out-of-view arm motion. Two-stage motion correction then blends visibility transitions kinematically and trains a reinforcement-learning tracking policy in physics simulation under agent-designed semantic rewards, completing manipulation phases even when the object leaves the camera view. Rendering the reconstructed scene through the robot's onboard camera along the optimized rollout yields synchronized robot-view images, proprioception and verified action labels. Fine-tuned exclusively on this converted dataset, without real-robot demonstrations, GR00T N1.7 performed loco-manipulation tasks autonomously on a Unitree G1. Project page: this https URL

---

## 12. Wireless Edge-Assisted Adaptive Latent Reasoning for Vision-Language-Action Models in Physical AI

**Authors:** Fatih Temiz, Melike Erol-Kantarci
**arXiv:** [2611.19131](https://arxiv.org/abs/2611.19131)
**Categories:** Robotics (cs.RO); Networking and Internet Architecture (cs.NI)

Vision-language-action (VLA) models enable embodied artificial intelligence (AI) by translating visual observations and language instructions into robotic actions. Emerging use cases in physical AI are expected to drive the need for efficient inference and communication, as the computational demands of the VLA models pose challenges for real-time control with limited onboard resources. Test-time scaling through latent reasoning allows these models to refine hidden representations without generating explicit chain-of-thought (CoT) tokens, but introduces a trade-off between task success, inference latency, and energy consumption. In this paper, we address the efficient collaborative inference under a realistic communication scenario. We propose a wireless edge-assisted framework for adaptive latent reasoning (WEALR) that augments onboard computation with edge computing. A decision-making agent jointly selects the execution location and latent-reasoning convergence threshold. We formulate this joint adaptation as a constrained Markov decision process (CMDP). A Lagrangian-constrained deep reinforcement learning (CDRL) approach, namely trust region policy optimization Lagrangian (TRPO-Lag), learns to balance task performance and resource consumption under varying wireless conditions and task requirements. We evaluate the framework using LIBERO manipulation tasks, profiled VLA inference costs, and ray-traced wireless channels. Experimental results demonstrate that TRPO-Lag achieves up to 23% higher feasibility-weighted task success rate compared to benchmark CDRL methods.

---

## 13. Robustness as a Transferable Skill: Cross-Task Adversarial Defense for Vision-Language-Action Policies

**Authors:** Jinquan Zhang, Run Yang, Dongfu Yin, ..., Pengshuai Yin, F. Richard Yu
**arXiv:** [2611.18702](https://arxiv.org/abs/2611.18702)
**Categories:** Robotics (cs.RO); Computer Vision and Pattern Recognition (cs.CV)

Vision-Language-Action (VLA) policies are vulnerable to adversarial visual perturbations, while defenses often require task-specific adversarial fine-tuning. We investigate whether robustness learned on source manipulation tasks can protect independently specialized target policies without target-side adversarial training. We first show that even a single source defense update improves robustness on held-out tasks, establishing cross-task defense reuse independently of multi-source aggregation. To combine source updates, we introduce Source-Norm Transferable Robustness Vector (SN-TRV), which retains the direction of their mean while calibrating its magnitude using source-update norms. The resulting update is applied to the target visual encoder without target adversarial data, target-side gradient optimization, or additional inference modules. Evaluations across three VLA backbones, fixed and adaptive attacks, and different source defense recipes show improved robustness over naive averaging and identify limits in attack coverage. Physical PiPER trials increase average success under printed adversarial patches from 20.3% to 45.8%.

---

## 14. POKE: Probe Offline, Keep Efficiently for Vision-Language-Action Models

**Authors:** Jaehyuk Lee, Yeajin Lee, Suhyun Bae, Donghun Lee
**arXiv:** [2611.21033](https://arxiv.org/abs/2611.21033)
**Categories:** Computer Vision and Pattern Recognition (cs.CV)

Visual token pruning reduces the inference cost of Vision-Language-Action (VLA) models, but attention-based scores do not directly measure a token's effect on the predicted action. We define action sensitivity as the magnitude of the first-order action change when a token is replaced by its camera's mean token and estimate it for all tokens with a single backward pass. Computing it online is costly: scoring on the full (unpruned) graph needs an extra forward pass at every control step. Scoring on the pruned forward pass is cheaper but causes scoring-graph lock-in: removed tokens lose their direct paths through later layers and tend to receive lower scores, making those locations less likely to return. On replayed observations, even with a random conditioning mask, pruned-graph scoring re-selects 59% of the mask's tokens, versus 6% expected by chance; attention histories show a similar bias. POKE (Probe Offline, Keep Efficiently) computes full-graph action sensitivities offline and distills them into a student with under 0.3M parameters. At inference, the student scores the current observation without backpropagation or previous masks, and score-guided diversity selection retains the tokens. Keeping 32 of 512 visual tokens on LIBERO, POKE achieves 95.2% success on OpenVLA-OFT and 90.8% on $\pi_{0.5}$ at $1.85\times$ and $1.26\times$ speedups, outperforming attention-, diversity-, and distillation-based pruners, with larger margins on LIBERO-Plus.

---

## 15. FAVR: Flow-Aware Visual Residual Alignment for Vision-Language-Action Policies

**Authors:** Qixuan Wu, Xiaole Yang, Yuguang Yang, ..., Guodong Guo, Baochang Zhang
**arXiv:** [2611.20971](https://arxiv.org/abs/2611.20971)
**Categories:** Computer Vision and Pattern Recognition (cs.CV)

Pretrained video representations provide rich temporal information for robotic manipulation, yet effectively integrating them into existing vision-language-action (VLA) policies remains challenging. We present Flow-Aware Visual Residual Alignment (FAVR), a lightweight framework for flow-aware visual conditioning of frozen VLA policies. FAVR maintains a compact temporal visual state through linear Test-Time Training (TTT) and retrieves action-conditioned visual features throughout flow-based action generation. By exploiting the affine structure of the frozen action head, we explicitly characterize how injected visual features influence predicted action velocities and formulate flow-aware channel selection as a box-constrained optimization problem. We develop a FISTA-based solver for joint gate optimization and derive an efficient closed-form approximation through diagonalization and rescaling. With only 1.74-2.19M trainable parameters and 5,000 adaptation steps, FAVR improves pretrained VLA policies across benchmarks. On RoboTwin 2.0, FAVR improves LingBot-VLA from 87.12% to 90.04% under clean conditions and from 86.88% to 89.38% under randomized conditions. A controlled ablation on five RoboTwin tasks further shows that flow-aware gating increases average success from 72.0% with a gate shared across flow steps to 82.0%, demonstrating the benefit of adapting visual conditioning throughout action generation.

---

## 16. Competent Autonomous Driving Through Fine Tuning Vision Language Action Models with Symbolic Traffic Rules

**Authors:** Barkin Dagda, Vinal Asodia, Iman Sharifi, Peng Wei, Saber Fallah
**arXiv:** [2611.20648](https://arxiv.org/abs/2611.20648)
**Categories:** Computer Vision and Pattern Recognition (cs.CV)

Vision-language-action (VLA) models offer a unified approach to perception, reasoning, and control for autonomous driving, but accurate action prediction alone does not establish compliance with traffic regulations. This paper presents a rule-guided VLA framework that incorporates symbolic traffic-rule feedback into policy optimisation. The framework combines supervised fine-tuning on expert demonstrations with reinforcement learning (RL) refinement using a reward that encourages encoded-rule compliance while penalising deviations from expert actions. Selected provisions of the United Kingdom Highway Code are formalised as executable first-order logic rules using PyReason, covering speed adaptation, following distance, and road-user priority. A frozen vision-language model extracts scene predicates, which are combined with vehicle-state information to assess the projected consequences of candidate control actions. Offline evaluation on held-out data collected in the CARLA simulator compares three group-based RL methods. The results show improvements in both action prediction accuracy and encoded-rule compliance over the supervised baseline. The best-performing variant increases the overall rule pass rate from 92.9% to 97.6%, with zero observed violations of the encoded road-user-priority check in the evaluated samples. These findings support symbolic rule feedback as a means of improving VLA policy alignment with explicit traffic-rule criteria.

---

## 17. When Backdoors Can Be Switched Off: Suppression-Aware Backdoor Attacks on Vision-Language-Action Models

**Authors:** Nur Afsa Syeda, Mohamed Elmahallawy
**arXiv:** [2611.19774](https://arxiv.org/abs/2611.19774)
**Categories:** Computer Vision and Pattern Recognition (cs.CV); Cryptography and Security (cs.CR)

Vision-Language-Action (VLA) models map visual observations, robot states, and natural-language instructions to robotic actions, but their multimodal interfaces introduce new security risks. Existing VLA backdoor attacks primarily study trigger-based activation and stealthy action manipulation, leaving conditional suppression of malicious behavior underexplored. We investigate suppression-aware backdoors, which combine conjunctive trigger activation with instruction-conditioned suppression. We instantiate this design through three variants: Cross-Modal Trigger, combining robot-state and spatially separated visual triggers; Self-Suppressing Trigger, requiring a state trigger and a [DISRUPT] instruction token for activation, with [RESTORE] token suppressing the attack; and Multi-Trigger, additionally requiring a visual trigger while retaining suppression even when physical triggers persist. We evaluate these attacks using SmolVLA on two SO-100 manipulation datasets against four baselines: State Backdoor, BadVLA, TabVLA, and SilentDrift. Self-Suppressing and Multi-Trigger reduce Isolation Forest detection from 96--98% to 1--18% and action-space l divergence by 10--14X, achieving 63--71% attack success rates with perfect clean-task performance. Experiments with OpenVLA on LIBERO further show that the attacks transfer to a 7B-parameter policy, evading STRIP and action-distribution-shift detection. Our findings establish conditional suppression as an important dimension for evaluating backdoor threats in VLA policies.

---

## 18. From Recursion to Convolution: Parallel Self-Improvement for Multi-Agent Systems

**Authors:** Zheng Wang, Yuang Liu, Sachith Abeywickrama, ..., Xuefeng Jin, Zhangchun Zhao
**arXiv:** [2611.20891](https://arxiv.org/abs/2611.20891)
**Categories:** Artificial Intelligence (cs.AI); Computation and Language (cs.CL); Machine Learning (cs.LG)

Multi-agent self-improvement enables agents to improve through interaction and feedback. However, sequential dependencies across agents and refinement rounds can propagate errors, increase computational costs, and limit parallelism. Moreover, refining individual features or agents in isolation can overlook their dependencies and restrict collective coordination. To address these challenges, we propose ConvRSI, a framework for parallelizing multi-agent self-improvement through convolution. ConvRSI couples intra-agent convolution, which jointly refines related agent features, with inter-agent graph convolution, which aggregates messages according to the collaboration topology. Both stages operate in latent space, enabling parallel updates without repeatedly decoding and re-encoding intermediate messages. Experiments on MATH-500 show that ConvRSI achieves 5.04% performance improvement while reducing 17.27% inference cost, and 45.11% latency compared with RecursiveMAS. It also supports diverse collaboration patterns by representing their topologies as adjacency matrices. These results demonstrate the potential of convolutional co-evolution for efficient multi-agent self-improvement. Our code and datasets are provided in this https URL.

---
