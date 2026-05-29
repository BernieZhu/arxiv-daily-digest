# arXiv Daily Digest — 2026-05-28

**Mode:** direct
**Categories:** cs.AI, cs.LG, cs.RO, cs.CV
**Keywords:** VLA, world model, world action model
**Papers found:** 24

---

## 1. Do LLMs Build World Models From Text? A Multilingual Diagnostic of Spatial Reasoning

**Authors:** Zhikai Pan, Chih-Ting Liao, Chunrui Liu, ..., Zhangquan Chen, Xin Cao
**arXiv:** [2605.28277](https://arxiv.org/abs/2605.28277)
**Categories:** Artificial Intelligence (cs.AI)

Whether large language models (LLMs) construct internal spatial world models from pure-text descriptions remains contested, and whether such capabilities transfer across languages has not been systematically studied. We introduce MentalMap, a multilingual diagnostic benchmark with a six-level capability hierarchy (L0-L5) spanning atomic spatial facts to generative world-graph construction, together with four diagnostic axes probing frame of reference, reading-direction bias, reasoning-effort allocation, and hallucination. MentalMap is built from 100 ProcTHOR household scenes, covers eight typologically diverse languages plus a structured-text control, and contains 39 task families across 1,950 evaluation cells. Evaluating thirteen LLMs across scales and model families, we identify a universal L3 reasoning cliff: no model retains even half of its L0 performance on viewpoint reasoning once baseline atomic accuracy exceeds 40%. The cliff persists across languages, scales, and prompting strategies, while structured-output failures and reasoning patterns vary substantially across models. Human evaluation under the identical pure-text protocol reproduces the same failure pattern, suggesting that the bottleneck arises from text-only working memory constraints rather than being specific to current LLM architectures. Our findings reframe pure-text spatial reasoning as a multi-axis world-modeling problem and motivate multimodal and scratchpad-augmented reasoning as future directions.

---

## 2. Hybrid Neural World Models

**Authors:** Pranav Lakshmanan, Paras Chopra
**arXiv:** [2605.28317](https://arxiv.org/abs/2605.28317)
**Categories:** Machine Learning (cs.LG); Artificial Intelligence (cs.AI); Numerical Analysis (math.NA); Computational Physics (physics.comp-ph)

Neural surrogates promise large speedups over classical solvers for physical dynamics but fail silently at sharp dynamical events such as shocks, fronts, and contact. We present hybrid neural world models for physical dynamics: a recipe for training and deploying multi-horizon surrogates in physical state space, where a single network with continuous horizon conditioning is trained with direct supervision against textbook reference solvers to predict any future state at horizon T in one forward pass. Although no part of the training data, loss function, or architecture supervises discontinuity location, the trained surrogate encodes it implicitly, recoverable from its forward passes alone as a per-trajectory error map that concentrates on shocks, fronts, and contacts, and stays small elsewhere. The map is competitive with or better than standard label-free baselines including deep ensembles, learned error heads, gradient-magnitude indicators, and locally-adaptive conformal prediction, while using only a single trained network and requiring no calibration set or governing-equation knowledge. The recipe supports two operating points. Mode 1 runs the surrogate alone for maximum throughput, with same-hardware CPU speedups of 26x to 72x against textbook solvers on the PDE environments. Mode 2 uses the error map to gate a reference-solver fallback, deferring uncertain trajectories and roughly halving the surrogate's residual error at the default operating point. The recipe applies without modification across reaction-diffusion, compressible Euler, and rigid-body collision dynamics.

---

## 3. Affective Music Recommendation: A Rollout-Based World Model for Offline Preference Optimization

**Authors:** Audrey Chan, Aaron Labbé, Jacob Lavoie, ..., Guillaume Lajoie, Laurent Charlin
**arXiv:** [2605.28810](https://arxiv.org/abs/2605.28810)
**Categories:** Machine Learning (cs.LG); Information Retrieval (cs.IR); Sound (cs.SD)

Functional music applications, from consumer focus and sleep aids to clinical interventions, share a distinctive recommendation problem: success is defined by the listener's affective state, but online experimentation on emotion is ethically constrained, particularly for clinical populations who cannot reliably skip a song or report distress. We describe AMRS, the Affective Music Recommendation System deployed on LUCID's health-and-wellness platforms, which serve clinical users (primarily older adults with neurocognitive conditions) and consumer-wellness users across energize, focus, calm, and sleep modes. AMRS is built around a rollout-based world model: a causal transformer trained on logged listening data to jointly predict engagement, binary rating, and self-reported valence and arousal. The world model serves both as an in-silico simulator for offline policy training and as a stress-testing tool before deployment. A recommender policy initialized by behaviour cloning is fine-tuned offline with Direct Preference Optimization (DPO) against a configurable multi-objective utility function. Under a strict cold-start protocol, the world model predicts both behavioural and affective signals with usable fidelity; DPO improves predicted valence and arousal over the cloned baseline while maintaining a similar diversity profile and avoiding the distributional collapse produced by greedy optimization. We position the work as an early deployed validation of a methodology for affective recommendation when online experimentation is ethically untenable.

---

## 4. Chreode: A Cell World Model for One-Step Temporal Dynamics and Perturbation Prediction

**Authors:** Mufan Qiu, Genhui Zheng, Yinuo Xu, ..., Qi Long, Tianlong Chen
**arXiv:** [2605.28111](https://arxiv.org/abs/2605.28111)
**Categories:** Machine Learning (cs.LG)

Predicting how a cell will change its transcriptional state under a developmental signal or a genetic perturbation is the computational core of in-silico biology and the AI Virtual Cell program. Existing approaches either fit static control-to-treated maps that discard time, or solve multi-step ODE / Schrödinger-bridge problems on each dataset independently. We introduce Chreode, a one-step cell world model that predicts action-conditioned cell-state transitions through a structured residual transition operator. It shifts distributional evolution from inference time to training time, enabling single-pass generation while preserving a Waddington-inspired decomposition into downhill landscape flow, rotational in-tangent dynamics, and stochastic spread. The model is pretrained with a shared scVI encoder and a DiT-based dynamics backbone on a 2.4M-cell mouse embryonic atlas spanning 7 datasets. As a fine-tuning initialization, Chreode improves per-target Sinkhorn distance on Weinreb hematopoiesis and Veres islet differentiation over matched scratch models, PI-SDE, and PRESCIENT. As a transferable gene-state embedding for GEARS, the pretrained dynamics representation reduces shared-vocabulary DE20 mean squared error on Norman Perturb-seq from 0.2121 to 0.1858, a 12.4% relative improvement, without changing the GEARS training procedure. We interpret this transfer to perturbation prediction as evidence that pretrained developmental-trajectory dynamics encode differentiation primitives transferable to CRISPR-induced state shifts, since both involve cell-state transitions in a shared latent geometry. The pretrained backbone additionally produces zero-shot clonal fate scores on Weinreb that are competitive with strong dynamic-OT baselines.

---

## 5. Ω-QVLA: Robust Quantization for Vision-Language-Action Models via Composite Rotation and Per-step Scaling

**Authors:** Xinyu Wang, Mingze Li, Sicheng Lyu, ..., Xiao-Wen Chang, Peng Lu
**arXiv:** [2605.28803](https://arxiv.org/abs/2605.28803)
**Categories:** Computer Vision and Pattern Recognition (cs.CV); Machine Learning (cs.LG)

Vision-Language-Action (VLA) models unify perception, reasoning, and control within a single policy, yet their multi-billion-parameter backbones and diffusion-based action heads make on-device deployment prohibitively expensive. Prior quantization efforts offer only partial solutions, compressing the LLM backbone while leaving the DiT action head at full precision, or resorting to mixed-precision schemes, driven by the belief that uniformly quantizing the action head is inherently unstable. We challenge this assumption with Omega-QVLA, the first training-free post-training quantization framework that compresses both the language backbone and the entire diffusion action head of a VLA model to a uniform W4A4 precision, eliminating the need for mixed-precision allocation. Omega-QVLA combines a composite SVD-Hadamard rotation that equalizes per-channel weight energy while diffusing residual activation outliers with per-step DiT activation scaling quantization that absorbs dynamic-range drift across denoising steps. On LIBERO, Omega-QVLA compresses Pi 0.5 and GR00T N1.5 to W4A4 with 98.0% and 87.8% task success rates, matching or exceeding their FP16 references of 97.1% and 87.0%, while reducing the static memory footprint by 71.3%. Real-world manipulation experiments further confirm smooth, accurate manipulation where prior methods fail. Code is available at this https URL.

---

## 6. How VLAs Fail Differently: Black-Box Action Monitoring Reveals Architecture-Specific Failure Signatures

**Authors:** Krishnam Gupta
**arXiv:** [2605.28726](https://arxiv.org/abs/2605.28726)
**Categories:** Robotics (cs.RO); Machine Learning (cs.LG)

We discover that VLA architectures fail in fundamentally different, predictable ways at the motor-command level. Running VQ-BeT, Diffusion Policy, and ACT on identical evaluation protocols (n=450 episodes across PushT and ALOHA 14-DOF bimanual manipulation), we find: (1) direction reversal rate is a universal failure predictor across all three architectures (AUROC=0.93, 0.79, 0.91; p<0.001); (2) jerk monitoring is predictive only for discrete-token architectures, following a discrete-to-continuous gradient (0.88, 0.69, 0.41); (3) velocity violations alone are non-predictive everywhere (AUROC 0.41-0.69), yet velocity checking is the most common safety mechanism in VLA deployment code; and (4) for continuous-family VLAs, velocity monitoring provides effectively zero predictive signal (AUROC=0.52 on ACT, 0.41 on Diffusion), proving that architecture-matched monitor selection is essential. These results quantify a monitoring consequence of the well-known discrete/continuous VLA distinction: the two families produce qualitatively different failure signatures that require different monitors. No single monitor works universally; architecture-matched selection is required. This finding was enabled by SafeContract, a training-free, black-box action monitoring toolkit with conformal calibration. Code: this https URL

---

## 7. ProgVLA: Progress-Aware Robot Manipulation Skill Learning

**Authors:** Seungsu Kim, Jinyoung Choi, Seungmin Baek, Jean-Michel Renders
**arXiv:** [2605.28231](https://arxiv.org/abs/2605.28231)
**Categories:** Robotics (cs.RO); Machine Learning (cs.LG)

We present ProgVLA, a compact vision-language-action (VLA) model designed for reliable robot manipulation under tight compute and memory budgets. The model specifically focuses on efficiently processing long multi-modal sequences by maintaining an explicit representation of task progress over extended horizons. To this end, ProgVLA integrates two key components. First, a multi-modal encoder with a two-stage Perceiver resampling scheme compresses variable-length visual, language, and proprioceptive streams into a fixed set of control-ready context tokens, substantially reducing sequence length while preserving cross-modal grounding. Second, an auxiliary set of progress heads is trained with offline reinforcement learning (RL) objectives to jointly learn critics over normalized remaining-horizon targets. This provides the policy with an internal estimate of task progress and enables advantage- and success-weighted flow-matching imitation learning. On two well-established multi-task robot manipulation benchmarks, a 0.1B-parameter ProgVLA model reaches success rates that are competitive with, and on long-horizon and harder task tiers exceed, substantially larger pretrained baselines. Ablations indicate that the learned context resampler and task-adaptive visual fine-tuning are the largest single contributors, while progress-aware training provides a consistent additional gain that is concentrated on long-horizon and multi-object tasks. We further validate the approach in real-world toy-kitchen environments.

---

## 8. PrimitiveVLA: Learning Reusable Motion Primitives for Efficient and Generalizable Robotic Manipulation

**Authors:** Yutai Li, Shaohui Peng, Jiaming Guo, ..., Xing Hu, Yunji Chen
**arXiv:** [2605.28634](https://arxiv.org/abs/2605.28634)
**Categories:** Robotics (cs.RO)

Vision-Language-Action (VLA) models offer a promising paradigm for generalist robotic policies, yet their adaptation is hindered by data inefficiency and poor generalization. We argue that these bottlenecks stem from the prevailing Direct Instruction-to-Control Mapping, which forces models to memorize monolithic trajectories rather than reusable motion patterns, i.e., primitives. We propose PrimitiveVLA, a framework that shifts this paradigm toward a Primitive-Centric Disassemble & Assemble paradigm. Supported by a shared Multimodal Canonical Representation (MCR), PrimitiveVLA unifies two phases: (1) Fine-tuning-phase Disassembly, which uses an automated pipeline to disassemble demonstrations into reusable primitives; and (2) Inference-phase Assembly, which employs a VLM-based planner and an LLM-generated switch module for robust closed-loop execution. By disassembling tasks into reusable primitives, PrimitiveVLA enables VLA models to learn invariant motion patterns instead of task-specific trajectories. Extensive experiments show that our framework improves data efficiency and achieves superior zero-shot generalization across unseen and long-horizon tasks.

---

## 9. What Frozen VLAs Already Know About Success: A Probing Study of Value-Like Structure in Foundation Robot Policies

**Authors:** Jiachen Zhang, Junnan Nie, Junyi Lao, ..., Jiaxin Jiang, Songfang Huang
**arXiv:** [2605.28527](https://arxiv.org/abs/2605.28527)
**Categories:** Robotics (cs.RO)

Vision--language--action (VLA) policies are trained to imitate actions; their loss never asks them to estimate reward, progress, or future success. Their frozen representations nevertheless carry such information, and it can be read out and used to guide action choice without retraining the policy. From mixed successful and failed manipulation trajectories on LIBERO-Goal, we recover Monte-Carlo outcome targets using lightweight linear probes on frozen features. The targets are consistently predictable from OpenVLA, Pi0.5, DINOv2, and CLIP features, and substantially less so from baselines built on progress, time-to-go, task identity, or proprioception. To rule out task and temporal shortcuts, we evaluate the probes under same-task, same-timestep matched comparisons: Pi0.5 probes still reach roughly 92% pairwise ordering accuracy, while label-shuffled controls stay at chance. Used as a test-time selector over sampled Pi0.5 action prefixes, the same probe turns this offline finding into behavior: on push-plate, success rises from 26.7% under greedy decoding to 44.3%, with a second positive case on wine-rack. The gains are not universal and require additional inference compute, but the underlying finding is clean: frozen VLAs already encode information about success that their imitation objective never explicitly demands.

---

## 10. Mag-VLA: Vision-Language-Action Model for Bimanual Magnetically Actuated Microrobot Manipulation

**Authors:** Yongchen Wang, Kangyi Lu, Lan Wei, Dandan Zhang
**arXiv:** [2605.28486](https://arxiv.org/abs/2605.28486)
**Categories:** Robotics (cs.RO)

Magnetically actuated microrobots have been used as wireless, non-contact manipulation tools at microscales, making them promising for minimally invasive applications. However, their control remains challenging due to indirect actuation, limited sensing, and nonlinear magnetic interactions. In this work, we propose Mag-VLA, a vision-language-action (VLA) model for dexterous magnetic microrobot manipulation using two robotic arms with mounted magnets for dynamic magnetic-field construction. Bimanual coordination enables capabilities such as microrobot reorientation that are difficult or infeasible with a single arm, but it also introduces coupled control challenges, as the policy must generate coordinated trajectories for both actuators within a shared workspace. Our framework adapts a Qwen2.5-VL-7B backbone using Low-Rank Adaptation (LoRA) to process visual observations and language instructions for action prediction. To capture task progression, we introduce a motion-aware phase classifier and a phase-conditioned Action Chunking Transformer (ACT) decoder for temporally coherent multi-step control. We further construct a teleoperated magnetic microrobot manipulation dataset covering three task configurations. Ablation studies show that the ACT-based decoder substantially outperforms alternative generative action heads. In real-robot experiments, Mag-VLA achieves a 90% approach success rate across all tasks and transport success rates of 80%, 70%, and 50% as task difficulty increases. These results demonstrate that hierarchical VLA modeling provides a promising framework for magnetic microrobot manipulation.

---

## 11. SANTS: A State-Adaptive Scheduler for World Action Models

**Authors:** Yirui Sun, Guangyu Zhuge, Keliang Liu, ..., Zhongxue Gan, Chunxu Tian
**arXiv:** [2605.27947](https://arxiv.org/abs/2605.27947)
**Categories:** Robotics (cs.RO)

World Action Models (WAMs) improve robot manipulation by using video-based future representations to condition action generation. In pixel-space WAMs, however, the best action condition is not necessarily the fully denoised video. Controlled denoising-depth scans show that video refinement can reduce action error up to a state-dependent point, after which the gain may saturate or even reverse when late predictions become less action-relevant or physically unreliable. This suggests that action generation should use a state-dependent point along the video noise trajectory rather than a fixed terminal denoising depth. We introduce State-Adaptive Noise Trajectory Scheduler (SANTS), a lightweight scheduler for video-to-action diffusion policies. At each video decision point, SANTS reads the current video-state representation and noise level, then jointly predicts a cumulative stopping hazard and a relative noise-progression ratio. SANTS is post-trained with a path-level reward computed after the frozen action branch generates the final action chunk, so the scheduler is optimized for downstream action quality rather than intermediate video fidelity, while redundant video-state updates are explicitly penalized. Experiments show that SANTS reaches \(94.4\%\) overall success on RoboTwin 2.0 and \(73.1\%\) average success across seven real-robot tasks, while reducing latency by \(81.7\%\) and \(79.0\%\) relative to full video denoising, respectively. These results indicate that adaptive selection along the video noise trajectory can preserve the control benefits of WAM-style future reasoning while removing much of its redundant inference cost.

---

## 12. Colosseum V2: Benchmarking Generalization for Vision Language Action Models

**Authors:** Jeremy Morgan, Prajwal Vijay, Hyeonho Oh, ..., Jesse Thomason, Ishika Singh
**arXiv:** [2605.27759](https://arxiv.org/abs/2605.27759)
**Categories:** Robotics (cs.RO)

Vision-Language-Action (VLA) models demonstrate promising generalization in robotic manipulation, driven by advances in large-scale vision and language pre-training. This progress can be misleading. Despite the zero-shot perception and language capabilities of VLAs, their overall task performance often degrades under distribution shifts, revealing gaps in how these systems translate high-level understanding into robust behavior. To systematically study this gap, we introduce Colosseum V2, a large-scale simulation benchmark for evaluating VLA generalization in robot learning across diverse conditions. The benchmark comprises 28 tasks spanning 13 task categories and two robot morphologies, covering a wide range of manipulation primitives and long-horizon behaviors. Built on the ManiSkill simulator, Colosseum V2 enables fast, GPU-parallelized evaluation and supports both in-domain and out-of-domain testing at scale. We evaluate state-of-the-art methods, including Action Chunking Transformers (ACT) and Pi0.5, and reveal limitations in both base performance and generalization. We demonstrate strong correlations between simulation and real-world metrics that support the ecological validity of the benchmark. By standardizing tasks, metrics, and evaluation protocols within a unified benchmark, Colosseum V2 enables reproducible and fair comparisons, reduced evaluation overhead, and accelerated progress toward general-purpose robot policies.

---

## 13. A Factory-Floor Deployment Case Study of VLA Pipelines for Industrial Packaging Task: Workflow, Failures, and Lessons

**Authors:** Brian Zhu, Philipp Schmitt, Philine Meister, ..., Felix Albrecht, Maxmillian Metzner
**arXiv:** [2605.27461](https://arxiv.org/abs/2605.27461)
**Categories:** Robotics (cs.RO)

Vision-Language-Action (VLA) policies have shown promising manipulation capabilities, yet their practical impact is often limited by the reliability demands of real-world deployment. We present a deployment study of an industrial packaging task at Siemens Factory (GWE, Erlangen, Germany), where a robot must pick a transparent accessory bag from a cluttered pile, insert it into the remaining cavity of a cardboard package, and ensure that the bag and its contents remain below the closing plane. Our goal is to understand the practical effort required to adapt a pretrained Pi0.5 policy to a single factory-floor task through iterative fine-tuning and deployment-driven refinement. The pipeline consists of repeated loops of data collection, curation, fine-tuning, evaluation, and targeted recovery data collection. We have accumulated 2535 episodes (10 hours) from the on-site factory settings. In this paper, we contribute an empirical account of a factory-floor VLA deployment, highlighting recurring failure modes and lessons that inform how to improve the deployment workflow.

---

## 14. Gamma-World: Generative Multi-Agent World Modeling Beyond Two Players

**Authors:** Fangfu Liu, Kai He, Tianchang Shen, ..., Zian Wang, Xuanchi Ren
**arXiv:** [2605.28816](https://arxiv.org/abs/2605.28816)
**Categories:** Computer Vision and Pattern Recognition (cs.CV)

World models for interactive video generation have largely focused on single-agent settings, where future observations are generated from a single control signal. However, many generated environments require multi-agent interaction: multiple players, robots, or embodied agents act simultaneously within a shared space. Scaling world models to such settings requires a principled multi-agent design: agents should remain independently controllable, permutation-symmetric, and support efficient inference while maintaining consistency across time and perspectives. In this paper, we present our generative multi-agent world model for interactive simulation. It introduces Simplex Rotary Agent Encoding, a parameter-free extension of 3D RoPE that represents agents as vertices of a regular simplex in rotary angle space. This gives each agent a distinct phase while making all agents permutation-equivalent, enabling scalable agent identity without learned per-slot identities or a fixed agent ordering. To avoid dense all-to-all attention across agents, we further propose Sparse Hub Attention, where learnable hub tokens mediate token interaction across agents, reducing cross-agent attention cost from quadratic to linear in the number of agents. For real-time rollout, we distill a full-context diffusion teacher into a causal student that generates temporal blocks sequentially with KV caching, enabling action-responsive generation at 24 FPS. Experiments in multiplayer virtual environments show that our model improves video fidelity, action controllability, and inter-agent consistency over slot-based and dense-attention baselines, while generalizing from two to four players without additional training.

---

## 15. DriveWAM: Video Generative Priors Enable Scalable World-Action Modeling for Autonomous Driving

**Authors:** Chen Shi, Jinrui Xu, Shaoshuai Shi, ..., Bo Zhang, Li Jiang
**arXiv:** [2605.28544](https://arxiv.org/abs/2605.28544)
**Categories:** Computer Vision and Pattern Recognition (cs.CV)

Pretrained foundation models have become an important basis for end-to-end autonomous driving. In contrast to vision-language models pretrained primarily on static image-text pairs, video generative models capture temporal dynamics and motion priors that are naturally suited for driving. We present DriveWAM, a driving world-action model that adapts a pretrained video diffusion transformer into an autoregressive video-action policy. DriveWAM organizes video and action streams into a unified temporal token sequence and trains them under a joint flow-matching objective, preserving the pretrained video-generation architecture while adapting its large-scale video priors to action generation. To incorporate high-level scene understanding, we introduce scene-evolving driving guidance, where a frozen VLM produces chunk-specific semantic intent to guide video-action generation. To keep long-horizon rollout bounded, we further introduce selective KV memory, which maintains bounded modality-aware video and action memory pools through relevance-redundancy cache selection at inference time. Experiments on NAVSIM and the PhysicalAI-Autonomous-Vehicles benchmark show that DriveWAM achieves strong planning performance, and a data-scaling study from 4k to 100k driving clips further confirms the scaling potential of world-action modeling for end-to-end autonomous driving.

---

## 16. VLA-Hijack: A Transferable Patch Attack against Vision-Language-Action Models via Visual Proprioception Hijacking

**Authors:** Jiyuan Fu, Kaixun Jiang, Jingkai Jia, ..., Dingkang Yang, Wenqiang Zhang
**arXiv:** [2605.28083](https://arxiv.org/abs/2605.28083)
**Categories:** Computer Vision and Pattern Recognition (cs.CV)

While Vision-Language-Action (VLA) models have emerged as powerful generalist policies, their severe vulnerability to adversarial patches significantly hinders their deployment in safety-critical domains. Moreover, existing patch attacks primarily focus on white-box settings, heavily overfitting to the specific action output space of the target model, which results in poor cross-architecture transferability. To overcome this limitation, we propose VLA-Hijack, a unified adversarial framework that breaks the transferability bottleneck by exploiting a fundamental vulnerability identified in this work: before planning any motion, a VLA model must first use visual information to locate its own robotic arm within the environment. Targeting this shared visual self-localization process, our approach concurrently optimizes Attention-Guided Proprioceptive Suppression to inhibit the real robotic arm's features, and Multimodal Proprioceptive Injection to establish the patch as a surrogate "phantom embodiment". By alternating between semantic concept anchoring and visual prototype projection, VLA-Hijack effectively severs the semantic relationship between the agent's true embodiment and its control policy. Extensive experiments across diverse architectures (OpenVLA, UniVLA, and CronusVLA) demonstrate that VLA-Hijack achieves superior optimization efficiency in white-box settings and sets a new SOTA for cross-architecture and cross-domain black-box transferability.

---

## 17. What-If World: A Causal Benchmark for General World Models in Embodied Scenarios

**Authors:** Kunlin Cai, Rui Song, Jinghuai Zhang, ..., Jiaqi Ma, Yuan Tian
**arXiv:** [2605.27589](https://arxiv.org/abs/2605.27589)
**Categories:** Computer Vision and Pattern Recognition (cs.CV)

Video generation models are increasingly used as world simulators for tasks like driving and robotic manipulation. What matters in these settings is not whether a single video looks right, but whether the model's output changes when its input changes. We test this by giving a model two prompts describing the same scene with one physical detail varied, and checking whether the two videos diverge the way physics predicts. The wording difference between the prompts is small by design, since only one variable is changed, but the correct physical difference is not. A model that misses this can still produce two videos that each look plausible individually, and existing benchmarks score videos one at a time and cannot detect this failure. We introduce What-If World, 319 such prompt pairs built on real frames from nuScenes and DROID, organized by a taxonomy of six physical variables shared across driving and manipulation. Each pair is scored with APEO, a four-part rubric checking whether each video follows its prompt (Adherence), is physically consistent (Physics), preserves the shared scene (Environment), and ends in the correct difference (Outcome). Across nine state-of-the-art models, no system exceeds 52% on the paired score, and open-source models cluster near 28%. Every model tested fails on a large fraction of causal interventions, indicating substantial room before these models can reliably support action-conditioned simulation or model-based planning. Where models do score well, performance appears to track the visual prominence of the intervention rather than the tractability of its underlying physics. Some visually subtle interventions score as low as 14.2%, while visually pronounced ones reach 40.4%.

---

## 18. Turning Video Models into Generalist Robot Policies

**Authors:** Sizhe Lester Li, Evan Kim, Xingjian Bai, ..., Max Simchowitz, Vincent Sitzmann
**arXiv:** [2605.27817](https://arxiv.org/abs/2605.27817)
**Categories:** Robotics (cs.RO); Artificial Intelligence (cs.AI); Computer Vision and Pattern Recognition (cs.CV); Machine Learning (cs.LG)

Video generative models have emerged as a promising robotics backbone, capable of generating videos that depict the completion of complex tasks across embodiments and environments. Recent work proposes robot foundation models that jointly predict future observations and actions by finetuning video models with action-labeled data. In this paper, we test the limits of an alternative approach: leave the video planner as-is while training an embodiment-specific inverse dynamics model (IDM). This decoupling offers several natural benefits: the video planner remains embodiment-agnostic, different video models can be interchanged easily without re-training the IDM, and the IDM can be independently trained with readily available self-play data. We present a closed-loop, video-to-action policy that combines an action-free video world model with a carefully-designed IDM based on the robot embodiment Jacobian. We demonstrate that our IDM design is both data-efficient and scalable to high-dimensional action spaces. Our policy, which we coin the Video-to-Embodied Robot Action Model (VERA), achieves strong performance across simulated and real-world benchmarks, including zero-shot Panda arm manipulation and 16-DoF Allegro-hand dexterous cube re-orientation. The same video planner can be used across multiple embodiments by pairing it with different embodiment-specific IDMs. Our results show that decoupled video planning plus faithful video-to-action translation is a viable alternative route towards zero-shot, cross-embodiment, and generalizable robot control. More results are available on our project website: this https URL.

---

## 19. Imitation Learning for Robot Assistance in Open Surgery: A Multi-Policy Evaluation on Suture Following

**Authors:** Xucheng Wang, Zhizhou Yang, Xiaoman Zhang, ..., Romain Hardy, Pranav Rajpurkar
**arXiv:** [2605.28736](https://arxiv.org/abs/2605.28736)
**Categories:** Robotics (cs.RO)

This study presents the first evaluation of general-purpose imitation learning for surgeon-robot collaborative assistance in open surgery, targeting suture following: the grab-pull-release motion an assistant performs at every stitch. We collect 160 teleoperated demonstrations (32,374 frames) on an open-source robot arm, benchmark four architecturally diverse imitation learning policies (ACT, Diffusion Policy, SmolVLA, $\pi_0$) across 28 trained models evaluated in 32 configurations along three clinically motivated dimensions: dataset size, camera viewpoint, and background variation. Our results demonstrate that under ideal conditions, the four policies achieve $50$-$75\%$ task success, with depth error as the dominant failure mode across all architectures. Among all policies, $\pi_0$ achieves the strongest results with a pretrained vision-language backbone, demonstrating superior data efficiency, greater robustness to background variation, and smoother trajectories compatible with surgical workflow. When deployed in a surgeon-robot suturing trial, $\pi_0$ yields a $92\%$ stitch completion rate. These findings establish collaborative robotic assistance in open surgery as a feasible target for imitation learning and highlight depth perception and end-effector design as key priorities for clinical translation.

---

## 20. Tabero: Learning Gentle Manipulation with Closed-Loop Force Feedback from Vision, Touch, and Language

**Authors:** Qiwei Wu, Rui Zhang, Xin Xiang, ..., Junjie Lai, Renjing Xu
**arXiv:** [2605.27886](https://arxiv.org/abs/2605.27886)
**Categories:** Robotics (cs.RO)

Tactile sensing is essential for robots to achieve human-like gentle manipulation. However, existing Vision-Language-Action (VLA) models struggle to exploit tactile feedback for gentle manipulation due to scarce aligned vision-tactile-language data and the lack of effective closed-loop force feedback mechanisms. To address these challenges, we introduce Tabero, a benchmark and model suite for gentle, language-conditioned robotic manipulation that demands fine-grained contact force perception. First, the Tabero benchmark addresses the scarcity of tactile data by presenting a data-efficient pipeline that repurposes open-source robot manipulation trajectories to generate diverse vision-tactile-language tasks, and establishes a multidimensional evaluation protocol that measures task success alongside physical interaction quality. Second, we propose Tabero-VTLA, an architecture with a decoupled force-position command interface; the resulting force-position commands are executed by a fixed hybrid controller to enable real-time, force-aware manipulation. Evaluated on Tabero, our model maintains high task success while reducing average grip force by over 70\% under gentle instructions, demonstrating its ability to modulate interaction forces based on multimodal experience. Our code is publicly available at this https URL.

---

## 21. Uni-LaViRA: Language-Vision-Robot Actions Translation for Unified Embodied Navigation

**Authors:** Hongyu Ding, Sizhuo Zhang, Ziming Xu, ..., Yang Gao, Jiebo Luo
**arXiv:** [2605.27582](https://arxiv.org/abs/2605.27582)
**Categories:** Robotics (cs.RO); Computer Vision and Pattern Recognition (cs.CV)

Embodied navigation requires an agent to map language and visual observations to a stream of spatial actions that drive a real robot through environments it has never seen. The dominant approach has been to scale vision-language-action (VLA) foundation models on ever-larger collections of robot trajectories. This paper argues that, for navigation specifically, generality can be obtained structurally, not only through data scale. The underlying decision structure of navigation reduces to a single Language-Vision-Robot Actions Translation. The language action emits semantic-level directional command and the vision action emits a pixel-level visual target. Both outputs lie inside the natural output manifold of pretrained multimodal large language models (MLLMs), so the task can be reasoned about by an agent rather than learned from robot data. Therefore, we present Uni-LaViRA, a unified agentic architecture that extends the same insight to four task families (VLN-CE, ObjectNav, EQA, and Aerial-VLN) and to four heterogeneous real robots (Wheeled, Quadruped, Humanoid robot, and a self-built UAV) in a zero-shot manner. Two agent-loop mechanisms make this unification practical. TODO List Memory (TDM) rewrites a structured checklist of pending sub-goals at every step, reciting the unfinished items back into the agent's most recent attention window. Second Chance Backtrack (SCB) rolls the robot back to the pre-error state and conditions the agent's next plan on the failed sub-trajectory, turning single-pass navigation into a self-correcting process. With zero training effort, Uni-LaViRA reaches 60.7% SR on VLN-CE R2R, 51.3% on VLN-CE RxR, 77.7% on HM3D-v2, 60.0% on HM3D-OVON, 54.7% on MP3D-EQA, and 40.0% on OpenUAV, matching or even surpassing recent training navigation foundation models that consume millions of samples and thousands of GPU-hours.

---

## 22. GE-Sim 2.0: A Roadmap Towards Comprehensive Closed-loop Video World Simulators for Robotic Manipulation

**Authors:** Boxiang Qiu, Liliang Chen, Yue Liao, ..., Maoqing Yao, Guanghui Ren
**arXiv:** [2605.27491](https://arxiv.org/abs/2605.27491)
**Categories:** Robotics (cs.RO)

We introduce GE-Sim 2.0 (Genie Envisioner World Simulator 2.0), a closed-loop video world simulator for robotic manipulation. Building on the action-conditioned video generation framework of Genie Envisioner, GE-Sim 2.0 is re-trained on thousands of hours of real-world robot data spanning teleoperation, contact-rich interaction, and on-robot policy deployment, substantially improving action-following fidelity and trajectory coverage. On top of this foundation, three new modules close the loop from video simulation to policy learning: a state expert that decodes proprioceptive state from video latents to support next-chunk prediction by downstream VLA policies; a world judge that scores generated rollouts against task instructions, yielding machine-verifiable success signals and rewards in place of manual inspection; and an acceleration framework that delivers a 25-frame rollout in 2.3 seconds on a single H100, with up to 4* frame skipping at inference for long-horizon evaluation. GE-Sim 2.0 tops the public WorldArena leaderboard at only 2B parameters, outperforming both dedicated robotic world models and closed-source general video generators, and policies trained against its rollouts and rewards translate into measurable real-world gains, establishing GE-Sim 2.0 as a practical platform for scalable evaluation and closed-loop learning of manipulation policies.

---

## 23. GEM: Generative Supervision Helps Embodied Intelligence

**Authors:** Ruowen Zhao, Bangguo Li, Zuyan Liu, ..., Han Hu, Jun Zhu
**arXiv:** [2605.28548](https://arxiv.org/abs/2605.28548)
**Categories:** Computer Vision and Pattern Recognition (cs.CV)

Embodied Vision-Language Models (VLMs) have demonstrated impressive performance and generalization in robotics, particularly within Vision-Language-Action frameworks. However, a significant gap remains between the high-level semantic focus of standard text-guided pre-training paradigms and the low-level spatial and physical knowledge critical for execution in embodied environments. In this paper, we introduce GEM, a Generative-supervised Embodied vision-language Model designed to bridge this divide. We propose integrating a depth map generation task directly into the VLM pre-training phase. By training this generative objective jointly with the main model, we observe substantial improvements in embodied intelligence, significantly enhancing both semantic understanding and physical operation capabilities. To support this paradigm, we curate and release GEM-4M, a comprehensive large-scale dataset featuring a mixture of grounding, reasoning, and planning data paired with high-quality depth supervision. Extensive experiments demonstrate that GEM achieves state-of-the-art results across diverse embodied benchmarks. Furthermore, our deployed action model, GEM-VLA, exhibits vastly superior task execution abilities in both simulation environments and real-world evaluations. Code, models, and datasets are available at this https URL

---

## 24. Proprio: Latent Self-Scoring and Inference-Time Refinement for Physically Plausible Video Generation

**Authors:** Mariam Hassan, Kaouther Messaoud, Wuyang Li, Alexandre Alahi
**arXiv:** [2605.28230](https://arxiv.org/abs/2605.28230)
**Categories:** Computer Vision and Pattern Recognition (cs.CV)

Modern video generative models produce visually impressive results, yet frequently violate basic physical principles. We propose Proprio, a training-free framework that enables a frozen video generator to assess and improve the physical plausibility of its own outputs. Inspired by proprioception, the biological sense of one's own movement, Proprio treats the model's flow residual under controlled latent perturbations as a self-scoring signal. Samples that are better explained by the generator's learned dynamics induce smaller and more stable residuals. We aggregate this signal across timesteps and perturbations, focus it on motion-relevant regions with a dynamic spatiotemporal mask, and use it for best-of-N search, gradient-based self-refinement, or both. Across text-to-video and image-to-video benchmarks, Proprio consistently improves physical plausibility, outperforming VLM-based scoring, and external world-model baselines in several settings. With TurboWan2.2, Proprio improves Physics-IQ from 32.2 to 37.5 (+16.5%) and VideoPhy2-hard physical commonsense from 45.6 to 55.0 (+20.6%). Human evaluation further shows that raters prefer Proprio-selected or refined videos for physical plausibility in roughly two-thirds of comparisons. These results suggest that frozen video generators contain actionable internal signals for evaluating and improving the physical plausibility of their own outputs.

---
