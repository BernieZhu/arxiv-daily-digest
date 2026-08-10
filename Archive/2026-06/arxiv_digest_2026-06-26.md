# arXiv Daily Digest — 2026-06-26

**Mode:** direct
**Categories:** cs.AI, cs.LG, cs.RO, cs.CV
**Keywords:** VLA, world model, world action model
**Papers found:** 25

---

## 1. EO-WM: A Physically Informed World Model for Probabilistic Earth Observation Forecasting

**Authors:** Junwei Luo, Shuai Yuan, Zhenya Yang, ..., Zhe Liu, Hengshuang Zhao
**arXiv:** [2606.27277](https://arxiv.org/abs/2606.27277)
**Categories:** Artificial Intelligence (cs.AI); Computer Vision and Pattern Recognition (cs.CV)

Earth Observation (EO) forecasting aims to predict future Earth surface dynamics from satellite observations under changing meteorological conditions. In this paper, we view this task as a partially observed, weather-driven world modeling problem, in which weather acts as a conditioning signal, while forecasting remains uncertain due to sparse observations and unobserved land-surface states. However, existing methods do not fully capture this setting: deterministic models collapse uncertainty into a single future prediction, while diffusion-based methods typically treat weather variables as undifferentiated conditioning signals, and existing benchmarks focus mainly on reconstruction accuracy rather than whether forecasts respond correctly to changed weather this http URL introduce EO-WM, a video diffusion transformer for multispectral EO forecasting. EO-WM incorporates a physically informed conditioning framework that represents meteorological forcing through a climatological baseline, weather anomalies, and cumulative physical stress signals. Specifically, it separates baseline and anomaly through distinct conditioning pathways, and accumulates anomalous forcing over time to capture sustained heat and drought stress. To evaluate weather-response behavior beyond standard metrics, we introduce two diagnostic benchmarks: an Extreme Summer Benchmark for severity-aware prediction of vegetation degradation under extreme weather, and a Seasonal Matched-Pair Benchmark for testing response fidelity under changed weather forcing. Experiments show that EO-WM reduces the error in predicted Normalized Difference Vegetation Index (NDVI) decline amplitude by a relative 5.63% and improves directional hit rate by a relative 7.80%, while remaining competitive on standard pixel-level metrics. The benchmarks and model will be made open-source at this https URL.

---

## 2. Einstein World Models

**Authors:** Munachiso Samuel Nwadike, Zangir Iklassov, Ali Mekky, Zayd M. Kawakibi Zuhri, Kentaro Inui
**arXiv:** [2606.26969](https://arxiv.org/abs/2606.26969)
**Categories:** Artificial Intelligence (cs.AI); Computation and Language (cs.CL); Computer Vision and Pattern Recognition (cs.CV)

Does intelligence require the ability to reason about phenomena beyond direct experience? It is natural to suspect that some complex thought cannot be captured through language alone. However, of particular concern to this work, is whether visualising counterfactual events can complement language as a mechanism for complex thought. We ask whether LLMs can be trained to utilise such visualisation mechanisms, in a way that benefits their reasoning abilities. Motivated by this question, we propose Einstein World Models. EWMs are a blueprint for LLM-based reasoning systems that place visual-temporal rollouts inside the reasoning trace, allowing them to reason in ways that text alone may not support well. In an EWM, the LLM calls a world-module (not to be confused with a world model), to produce short rollouts of scenes under consideration. The returned rollout is treated not as the answer, but as an inspectable hypothesis that can support later reasoning. Einstein World Models extend the capability of LLMs for tool calling (such as web search or code execution), into the domain of visual thought experiments.

---

## 3. LithoDreamer: A Physics-Informed World Model for Multi-Stage Computational Lithography

**Authors:** Yuqi Jiang, Yumeng Liu, Zimu Li, ..., Qi Sun, Cheng Zhuo
**arXiv:** [2606.26713](https://arxiv.org/abs/2606.26713)
**Categories:** Artificial Intelligence (cs.AI)

As semiconductor technology nodes scale, computational lithography is essential for ensuring yield and performance. However, lithography is a continuous physical process involving mask optimization, optical imaging, resist exposure, and development, which existing models fail to capture. To overcome this limitation, we present LithoDreamer, the first physics-informed World Model (WM) framework for computational lithography, which formulates the ``Layout-Mask-Resist Image-After Development Image (ADI)'' pipeline as a decision-driven multi-step evolution system. LithoDreamer captures feature changes between adjacent states to model stage-specific physics-informed latent spaces, in which it controls process intervention exploration and drives subsequent state transitions. To achieve interpretable intervention optimization without continuous supervision, we propose a contrastive variational optimization paradigm that contrasts the latent differences between intervention paths with variational evolution constraints, guiding the model to generate evolutions consistent with real lithography physics. Experiments show LithoDreamer achieves state-of-the-art performance in forward evolution and inverse planning. Our lithography dataset is publicly available at GitHub (this https URL).

---

## 4. Risk-Aware Selective Multimodal Driver Monitoring with Driver-State World Modeling

**Authors:** Daosheng Qiu, Haozhuang Chi, Hao Su, ..., Yongle Dong, Wei Zhang
**arXiv:** [2606.26922](https://arxiv.org/abs/2606.26922)
**Categories:** Robotics (cs.RO); Artificial Intelligence (cs.AI)

Continuous driver monitoring in automated vehicles requires low-latency inference while avoiding unsafe decisions under uncertain driver states. Large vision-language models provide broad multimodal priors, but their latency and limited reliability in this setting make them unsuitable as always-on in-cabin monitors. We propose a cost-aware selective inference framework for deployable multimodal driver monitoring. The core system is a lightweight RGB-physiological student that combines in-cabin visual observations with window-level HR/EDA signals, and a learned gate that decides when to accept the fast prediction or abstain for safety intervention. Additional controls show that the learned scores contain sample-level information beyond scenario priors, while exact physiological synchronization remains a limitation. To incorporate predictive evidence, we further study a compact driver-state world modeling module that rolls out latent driver-state features and estimates future fast-model errors and counterfactual system-level action costs. On scenario-induced driver-demand recognition, the RGB-physiological student improves over RGB-only and physiology-only baselines, reaching 0.7440 Macro-F1 and 0.9099 balanced accuracy with 11.39M parameters and 3.08ms inference latency. Cost-aware selective inference reduces unsafe false negatives from 17.37% under always-fast inference to approximately 5% across seeds, while maintaining deployment-level latency. While driver-state world modeling offers valuable predictive signals, worst-group evaluations highlight persistent operating-point calibration drift. Ultimately, reliable edge driver monitoring requires advancing not only perception backbones, but also risk-aware selective control and group-robust calibration.

---

## 5. Hallucination in World Models is Predictable and Preventable

**Authors:** Nicklas Hansen, Xiaolong Wang
**arXiv:** [2606.27326](https://arxiv.org/abs/2606.27326)
**Categories:** Machine Learning (cs.LG); Computer Vision and Pattern Recognition (cs.CV); Robotics (cs.RO)

Modern generative world models render increasingly realistic action-controllable futures, yet they frequently hallucinate: rollouts remain visually fluent while drifting from the ground-truth dynamics. We hypothesize that hallucination concentrates in low-coverage regions of the state-action space, where lightweight data-centric signals can both detect it and guide mitigation. To test this, we introduce MMBench2, a 427-hour, 210-task dataset for visual world modeling with ground-truth actions, rewards, and live simulators, and train a 350M-parameter world model on it. We identify three distinct hallucination modes: perceptual, action-marginalized, and scene-diverging -- each anchored to a different stage of the pipeline, and develop three signals that accurately predict where the model will fail. To close coverage gaps at training time, we develop a coverage-aware sampling technique; to close them online, our hallucination predictors serve as curiosity rewards for targeted data collection, yielding a data-efficient finetuning recipe that adapts the pretrained world model to entirely unseen environments with as few as 50 real environment trajectories. Overall, our findings reveal that hallucination in world models is inherently a data coverage issue, and that the same signals used to detect it can also be used for mitigation.
An interactive web version of our paper is available at this https URL

---

## 6. A Generalization Theory for JEPA-Based World Models

**Authors:** Jingyi Cui, Qi Zhang, Hongwei Wen, Yisen Wang
**arXiv:** [2606.27014](https://arxiv.org/abs/2606.27014)
**Categories:** Machine Learning (cs.LG)

Joint Embedding Predictive Architectures (JEPAs) have recently emerged as a promising paradigm for world modeling by learning predictive dynamics in a latent space rather than generating future observations at the input level. Despite their empirical success, the theoretical understanding of JEPA-based world models remains limited. In this paper, we develop the first generalization theory for JEPA-based world models. We formulate JEPA pretraining as a conditional spectral graph learning problem and show that the JEPA objective is equivalent to a low-rank factorization of an action-conditioned co-occurrence matrix. Building on this characterization, we establish a connection between JEPA pretraining error and downstream planning regret, leading to a finite-sample generalization bound for JEPA-based world models. Our analysis reveals an inherent trade-off between approximation and sample errors with respect to the latent dimension, providing theoretical insights into the advantages and limitations of latent predictive models compared with input-level predictive approaches.

---

## 7. Fast LeWorldModel

**Authors:** Yuntian Gao, Xiangyu Xu
**arXiv:** [2606.26217](https://arxiv.org/abs/2606.26217)
**Categories:** Machine Learning (cs.LG); Computer Vision and Pattern Recognition (cs.CV); Robotics (cs.RO)

Joint-Embedding Predictive Architectures (JEPAs), including recent LeWorldModel (LeWM), have become a promising foundation for reconstruction-free visual world models. For visual planning, however, LeWM evaluates candidate action sequences by repeatedly applying a local one-step latent transition model. This autoregressive rollout makes planning computationally expensive and exposes the predicted trajectory to accumulated latent errors as the horizon grows. We propose Fast LeWorldModel (Fast-LeWM), a fast latent world model that replaces repeated local rollout with action-prefix prediction. Given the current latent and a candidate action sequence, Fast-LeWM encodes its prefixes and predicts the future latents reached after executing those prefixes in parallel. By making action prefixes the basic prediction unit, Fast-LeWM directly models action effects accumulated to different extents over multiple horizons. This prefix-level supervision forces the model to learn how states continuously evolve under different action prefixes, rather than only fitting one-step state transitions. During planning, the predictor can use the last prefix token from the encoded action sequence to evaluate the corresponding future latent without explicitly rolling through each intermediate imagined state. Across multiple tasks, Fast-LeWM improves average success over LeWM while substantially reducing planning time, achieving lower open-loop latent loss whose growth becomes significantly slower as the rollout horizon increases.

---

## 8. World Action Models Enable Continual Imitation Learning with Recurrent Generative Replays

**Authors:** Manish Kumar Govind, Dominick Reilly, Smit Patel, Hieu Le, Srijan Das
**arXiv:** [2606.27374](https://arxiv.org/abs/2606.27374)
**Categories:** Robotics (cs.RO); Computer Vision and Pattern Recognition (cs.CV)

Going beyond predicting robot actions, World Action Models (WAMs) can also generate future visual observations. We build on this generative capability to propose Recurrent Generative Replay (REGEN), a continual imitation learning framework that synthesizes pseudo-replay trajectories, enabling a robot policy to rehearse previously learned tasks without storing their original human demonstrations. During continual adaptation, REGEN recursively queries the WAM to synthesize pseudo-replay trajectories conditioned only on prior task instructions and current-task observations. Experiments in both simulation and real-world manipulation settings show that REGEN reduces catastrophic forgetting by up to $50\%$ relative to sequential fine-tuning, while approaching the performance of privileged experience replay methods that require access to real replay data. Finally, we analyze the factors limiting generated replay, identifying long-horizon visual degradation and action-observation inconsistency as the primary bottlenecks. Our results establish WAMs as a promising foundation for continual robot learning without stored demonstrations.

---

## 9. RouterVLA: Turning Smoke Tests into Supervision for Heterogeneous VLA Selection

**Authors:** Xingyu Ren, Chugang Yi, Ge Ma, Youran Sun
**arXiv:** [2606.27355](https://arxiv.org/abs/2606.27355)
**Categories:** Robotics (cs.RO)

We study whether pre-deployment evaluation rollouts can be reused to supervise policy selection. Robot teams routinely smoke test candidate vision-language-action (VLA) policies, then compress those trials into a global winner. RouterVLA evaluates this idea with outcome-disjoint cross-fitting: recorded probes build a profile for each frozen expert, and a separate trial scores the selected expert without entering its profile. Across 34,752 LIBERO-Plus rollout records, a transparent probe-success rule raises held-out success from 0.4686 to 0.6149, a +14.64pp gain. Under the scalar-only profiles studied here, learned scorers are statistically indistinguishable from this rule, showing that commissioning carries the routing value while extra scalar scorer capacity does not create it. Reusing the scored trial inflates the measured gain by $1.87\times$, so credible ledger routing needs outcome separation; model scaling improves individual policies, while commissioning-aware routing improves the system built from them.

---

## 10. LA4VLA: Learning to Act without Seeing via Language-Action Pretraining

**Authors:** Tao Lin, Yuxin Du, Yiran Mao, ..., Gen Li, Bo Zhao
**arXiv:** [2606.27295](https://arxiv.org/abs/2606.27295)
**Categories:** Robotics (cs.RO)

Vision-Language-Action (VLA) models are commonly pretrained on robot demonstrations by jointly mapping visual observations and language instructions to actions. However, dense visual-action supervision can dominate the comparatively sparse language-action signal. As a result, policies may rely on visual shortcuts rather than learn how language conditions action execution, making them sensitive to visual variations. To address this limitation, we propose LA4VLA, a language-action pretraining framework that enables policies to acquire language-conditioned action priors without visual observations. These priors capture reusable manipulation skills shared across tasks and scenes, reducing reliance on scene-specific visual cues. Specifically, LA4VLA decomposes expert demonstration trajectories into atomic action segments and pairs each segment with a corresponding low-level action description. This yields LA4-33K, a dataset of 33K Language-Action (LA) episodes derived entirely from existing demonstrations without additional robot data collection. We further develop LA4VLA-1B, a lightweight 1B-parameter VLA model, and investigate three paradigms for incorporating language-action supervision into VLA learning: LA-only pretraining, sequential LA-to-VLA pretraining, and mixed LA-VLA pretraining. Across simulation and real-world tasks, LA-pretrained policies consistently outperform matched VLA-pretrained counterparts, while combining LA and VLA supervision leads to further gains. In particular, mixed LA-VLA pretraining improves the average success rate of LA4VLA-1B over the no-pretraining baseline by up to 17.8 and 45.0 percentage points in simulation and real-world tasks, respectively. These results establish LA4VLA as an effective and complementary pretraining strategy for building stronger and more robust VLA policies.

---

## 11. PhysReflect-VLA: Physical Feasibility and Self-Reflective Regulation for Reliable Vision-Language-Action Policies

**Authors:** Jiayu Yang, Tao Yang, Weijun Li, ..., Changjing Shang, Qiang Shen
**arXiv:** [2606.27146](https://arxiv.org/abs/2606.27146)
**Categories:** Robotics (cs.RO)

Long-horizon robotic manipulation is highly sensitive to physically infeasible transitions, contact-induced disturbances, and the lack of effective self-correction during execution. Although Vision-Language-Action (VLA) models provide strong task grounding through multimodal learning, they typically generate actions in a feed-forward manner without explicitly checking physical feasibility or diagnosing execution errors online. We present PhysReflect-VLA, a plug-and-play execution-time reliability framework that augments VLA policies with physical feasibility evaluation and structured self-reflection in a closed-loop control pipeline. A Feasibility Operator evaluates whether candidate actions induce dynamically consistent state transitions; an Action Explanation Operator verifies transition coherence; and an LLM-based Reflection Module analyzes state discrepancies to generate corrective guidance for subsequent actions. A two-stage training procedure stabilizes feasibility modeling and integrates reflection into the control loop. Experiments on multi-stage, contact-rich real-world manipulation tasks show consistent improvements in stage-wise stability and overall task success compared with representative VLA baselines with an average gain of 5.4\%. Ablation results further indicate that feasibility checking and reflection-based correction both contribute to improved execution robustness. These results highlight the importance of embedding physical consistency checks and online self-reflection for reliable long-horizon robotic manipulation.

---

## 12. PAMAE: Phase-Aware-MoE Action Experts Towards Reliable Flow-Matching Vision-Language-Action Policies

**Authors:** Jiayu Yang, Tao Yang, Xiang Chang, ..., Changjing Shang, Qiang Shen
**arXiv:** [2606.27144](https://arxiv.org/abs/2606.27144)
**Categories:** Robotics (cs.RO)

Reliable action generation for multi-stage robotic manipulation remains challenging for Vision-Language-Action (VLA) models. While existing flow-matching VLA policies offer strong multimodal grounding and generalization, they typically employ a single shared action expert, limiting their ability to capture phase-specific control patterns across distinct execution stages. We propose a plug-and-play Phase-Aware Mixture-of-Experts Action Module (PAMAE), as a step towards more reliable phase-consistent action generation. PAMAE replaces the original flow-matching action expert with a sparse expert mixture while preserving the pretrained VLA backbone. PAMAE introduces a phase-aware router that leverages execution-phase cues to allocate action generation across experts, supported by a lightweight phase prediction head and a routing alignment objective. To stabilize specialization, we adopt a two-stage training scheme that first warms up the expert module under the standard flow-matching loss and then optimizes phase-consistent routing under auxiliary supervision. On multi-stage manipulation simulation tasks, PAMAE improves task success by up to \textbf{9.2\%} over strong VLA baselines. Further ablations show that both phase-supervised routing and staged optimization are essential for the observed gains. Our results highlight phase-consistent expert allocation as an effective mechanism for improving the reliability and action quality of flow-matching VLA policies.

---

## 13. ForesightSafety-VLA: A Unified Diagnostic Safety Benchmark for Vision-Language-Action Models

**Authors:** Mingyang Lyu, Yinqian Sun, Yiyang Jia, ..., Feifei Zhao, Yi Zeng
**arXiv:** [2606.27079](https://arxiv.org/abs/2606.27079)
**Categories:** Robotics (cs.RO)

In embodied intelligence, safety is a prerequisite for reliable robot deployment in the physical world. Current vision-language-action (VLA) models continue to advance toward general-purpose task capability, yet their embodied safety limits remain poorly understood. To address this gap, we introduce ForesightSafety-VLA, a diagnostic benchmark that makes safety the primary evaluation target for VLA systems. We define a 13-category safety taxonomy covering physical interaction safety (Safe-Core), instruction-side safety (Safe-Lang), and perception-side safety (Safe-Vis), and evaluate policies under three controlled dimensions of variation -- scene structure, language command, and visual observation -- so that failure sources can be diagnosed rather than hidden in a single aggregate score. Beyond binary task success, ForesightSafety-VLA measures process-level risk through cumulative safety cost (CC) and risk exposure time (RET), together with a four-quadrant decomposition of safe/unsafe success and failure. We instantiate 66 safety-augmented base scenarios in RoboTwin across 5 embodiments and report results on representative VLA baselines. Across the evaluated baselines, even the strongest policy incurs non-trivial safety cost and unsafe nominal success, while structure and visual variation induce substantially stronger safety degradation than ordinary language variation. These results suggest that embodied safety is tightly coupled to perception, grounding, and control competence rather than being reducible to post-hoc safety filtering alone.

---

## 14. Improving Vision-Language-Action Model Fine-Tuning with Structured Stage and Keyframe Supervision

**Authors:** Yuan Xu, Yixiang Chen, Kai Wang, ..., Yan Huang, Liang Wang
**arXiv:** [2606.26801](https://arxiv.org/abs/2606.26801)
**Categories:** Robotics (cs.RO); Computer Vision and Pattern Recognition (cs.CV)

Vision-Language-Action (VLA) models have shown strong potential for generalizable robotic manipulation. During fine-tuning, however, action supervision applies equally across all timesteps, without structured supervision on which manipulation stage the robot is in or what the next gripper-event target should be. This causes failures to concentrate around challenging gripper-event transitions. To address this, we propose StaKe, a plug-in auxiliary supervision framework that automatically derives two complementary signals from demonstration gripper states without manual annotation: a stage classifier that identifies the current manipulation stage, and a keyframe predictor that estimates the target joint action at the next gripper transition. Both are modeled as lightweight auxiliary heads that enrich the learned representations during training, while leaving the base VLA policy architecture and inference loop unchanged. Experiments on bimanual simulation and single-arm Franka real-robot tasks show that StaKe consistently improves success rates (relative gains of 14% and 56%, respectively), with larger improvements on longer-horizon tasks that involve more gripper-event transitions. Ablation studies validate each design choice, and qualitative analysis confirms that the learned representations faithfully track manipulation stages. These results indicate that structured supervision is an effective and general strategy for enhancing VLA fine-tuning in long-horizon manipulation. Project website: this https URL

---

## 15. Tactile-WAM: Touch-Aware World Action Model with Tactile Asymmetric Attention

**Authors:** Siyu Wu, Linjing You, Junjie Zhu, ..., Jituo Li, Hengshuang Zhao
**arXiv:** [2606.26663](https://arxiv.org/abs/2606.26663)
**Categories:** Robotics (cs.RO)

World Action Models (WAMs) generate actions together with predicted futures, offering a powerful interface for robot decision making. In contact-rich manipulation, however, visually plausible futures can be physically incomplete: insertion, assembly, search, and reorientation often depend on slip, jamming, contact normals, or small alignment errors that are weakly visible or hidden in RGB. A natural solution is to predict future tactile states, however, we identify tactile pollution, a failure mode where unconstrained tactile-token injection degrades video and action prediction by forcing a visual dynamics model to absorb sparse, local, event-driven contact signals. To address this, we propose Tactile-WAM, a touch-aware WAM with a Tactile Asymmetric Attention Mechanism (TAAM). TAAM combines a VideoClean mask, which blocks video-query access to tactile key/value tokens while preserving action-query access, with a touch-aware bias for action attention. The VideoClean mask protects visual prediction while keeping contact information available for action generation; the touch-aware bias is derived from predicted touch changes and modulates action attention to tactile tokens during denoising. On ManiFeel, Tactile-WAM improves the mean success rate by 38.9% overall and by 86% on contact-rich tasks.

---

## 16. Not All Actions Are Equal: Rethinking Conditioning for Dexterous World Model

**Authors:** Zizhao Yuan, Zhengtu Liang, Taowen Wang, ..., Zecui Zeng, Renjing Xu
**arXiv:** [2606.27325](https://arxiv.org/abs/2606.27325)
**Categories:** Computer Vision and Pattern Recognition (cs.CV)

Recent advances in action-conditioned world models show promising progress in modeling complex interactions and forecasting future states under diverse action sequences. While these models are often driven by stronger visual representations and model capacity, action conditioning itself remains underexplored. Most existing approaches compress the entire action sequence into a single representation, which works well for low-DoF control but becomes less reliable in high-DoF scenarios. We observe that high-DoF dexterous actions are inherently heterogeneous, spanning multiple orders of magnitude, where large-scale motions coexist with subtle but important signals. When uniformly aggregated, optimization exhibits an imbalance across action components, which hinders the modeling of fine-grained effects and affects action fidelity. We therefore propose DexAC-WM, which treats action conditioning as a structured process rather than global compression. DexAC preserves dimension-level semantics via action tokenization and aligns action signals with visual dynamics through local refinement and global modulation. To address the limited high-level semantic grounding in existing world models, we further introduce a semantic branch that provides rich object-scene priors, which enables world model to capture dynamic visual details while supporting high-DoF action-conditioned video prediction. Experiments on EgoDex and EgoVerse show that combining the semantic branch with DexAC significantly improves FID, FVD, and PCK, demonstrating gains in visual-temporal realism and action-following consistency. We further verify that DexAC extends to other backbones, showing the scalability of our structured action-conditioning design. These results suggest that scaling world models to high-DoF control requires both structured action modeling and semantic grounding.

---

## 17. PhysEditWorld: A Large-Scale Dataset Toward Physics-Editable World Models

**Authors:** Bin Hu, Yanwen Ma, Jiehui Huang, ..., Jiaya Jia, Xiu Li
**arXiv:** [2606.26694](https://arxiv.org/abs/2606.26694)
**Categories:** Computer Vision and Pattern Recognition (cs.CV)

Recent game world models can synthesize visually plausible, action-conditioned rollouts. However, their interaction behaviors often remain limited to exploratory or wandering trajectories, and physical dynamics are typically learned as implicit correlations from data rather than as controllable variables. This limitation hinders their applicability to authored game environments, where physical rules are deliberately designed and require explicit manipulation. We introduce PhysEditWorld, a multimodal dataset with physical parameters, with a primary focus on gravity in this initial version. At its core, PhysEditWorld is built upon a replay paradigm implemented with a UE5 replay-and-rendering pipeline. Each scenario records a normalized action trace and replays the same initial state, character controller, action sequence, and camera policy under multiple gravity configurations, enabling controlled and attributable physical variation. PhysEditWorld contains 12 cinematic UE5 scenes, over 100 hours of gameplay interactions, and more than 60 million rendered rollout frames. Each sample provides synchronized multimodal signals, including RGB, depth, normals, audio, action traces, camera trajectory, engine states, semantic annotations, and explicit gravity labels. We further conduct initial utility studies on both generative video models and world understanding models, demonstrating that PhysEditWorld enables improved gravity-faithful dynamics modeling, enhances consistency under physical edits, and provides a scalable foundation for controllable world modeling research.

---

## 18. Look-Before-Move: Narrative-Grounded World Visual Attention in Dynamic 3D Story Worlds

**Authors:** Jiaming Bian, Bingliang Li, Yuehao Wu, ..., Huadong Mo, Zhenhong Sun
**arXiv:** [2606.26964](https://arxiv.org/abs/2606.26964)
**Categories:** Artificial Intelligence (cs.AI); Computer Vision and Pattern Recognition (cs.CV)

As embodied AI and world models increasingly operate in dynamic 3D environments, visual perception must move beyond passively interpreting given observations toward actively deciding what to observe. We study this problem through camera planning in dynamic 3D story worlds, where the camera must not only generate smooth motion, but also decide what visual evidence should be acquired before it moves. We formulate this capability as Narrative-Grounded World Visual Attention, where the camera acts as an embodied observer that determines what to observe, how to compose the observation, and how to shift attention over time under narrative intent and physical 3D constraints. To realize this capability, we propose Look-Before-Move, a camera planning framework that separates observation specification from motion execution. It first builds a Semantic Observation Contract to convert directorial intent into executable visual constraints, then performs Monte Carlo Viewpoint Search to find narrative-compliant and geometrically feasible viewpoints, and finally applies Semantic Trajectory Grounding to connect selected viewpoints into continuous, collision-aware, and temporally coherent camera motion. We further construct a dynamic 3D Story World Benchmark based on StoryBlender, covering 50 stories, 457 scenes, and 1585 shots with animated characters, semantic scene configurations, and executable 3D environments. Experiments show that our framework improves subject perception, intent consistency, and trajectory quality over representative baselines, demonstrating the importance of organizing visual attention before generating camera motion.

---

## 19. E-TTS: A New Embodied Test-Time Scaling Framework for Robotic Manipulation

**Authors:** Wen Ye, Peiyan Li, Tingyu Yuan, ..., Yan Huang, Liang Wang
**arXiv:** [2606.27268](https://arxiv.org/abs/2606.27268)
**Categories:** Robotics (cs.RO); Artificial Intelligence (cs.AI)

Recently, a few works have made early attempts to study test-time scaling for embodied tasks. However, two major challenges remain unsolved: (1) reasoning can effectively improve the performance of the policy, but its scaling mechanism has seldom been studied; (2) historical information is essential, as embodied tasks are inherently long-horizon and sequential, making sole reliance on current observations for action scaling inadequate due to the lack of historical context utilization. To address these challenges, we introduce E-TTS, a modular and plug-and-play Embodied Test-Time Scaling framework that unifies reasoning and action scaling for robotic manipulation via history-aware iterative refinement with vision-language verifiers. To support joint reasoning-action scaling, E-TTS performs reasoning-action joint sampling and scoring in a pairwise manner. To better utilize historical information, E-TTS uses a history buffer to store historical context, which is then used by reasoning and action verifiers to evaluate the sampled candidates. Unlike conventional open-loop TTS methods, E-TTS introduces feedback generation into the sampling process to form a closed-loop iterative refinement mechanism, enhancing both inference efficiency and environmental adaptability. Each component functions as an independent and composable module, allowing flexible and adaptive configuration depending on task requirements. To evaluate the advantages of our framework, we conduct experiments across 4 different benchmarks, 6 environments, 3 embodiments, and 4 base vision-language-action models. The experimental results demonstrate that, without requiring additional expert data collection or retraining, E-TTS consistently improves performance, achieving up to a 33.14% increase in simulation and 26.62% in real-world scenarios.

---

## 20. Advancing Omnimodal Embodied Agents from Isolated Skills to Everyday Physical Autonomy

**Authors:** Junhao Shi, Zezheng Huai, Siyin Wang, ..., Xipeng Qiu, Yu-Gang Jiang
**arXiv:** [2606.27251](https://arxiv.org/abs/2606.27251)
**Categories:** Robotics (cs.RO); Artificial Intelligence (cs.AI)

Building persistent embodied agents in unstructured environments demands unified orchestration of heterogeneous tools spanning both cyber (APIs, IoT) and physical (manipulation, navigation) domains, coupled with autonomous recovery from physical failures that inevitably arise over extended operation. Existing systems treat these as separate problems: VLM-based planners lack a unified cyber-physical action space, agent frameworks accumulate unbounded context that degrades temporal coherence, and VLA policies execute open-loop without detecting their own failures. We argue that persistent autonomy requires not a monolithic model but a hierarchical asynchronous architecture with explicit separation of planning, memory, and verification. To this end, we present OmniAct, a framework integrating a multimodal semantic planner for skill routing across unified action spaces, an adaptive hierarchical memory with event-boundary-driven compression for sub-linear context growth, and an asynchronous visual preemption engine that closes the semantic loop during physical execution. Across 40 real-world long-horizon tasks on two robotic platforms coordinating four IoT devices, OmniAct achieves consistent improvements in end-to-end success across all complexity levels, maintains near-flat token consumption over under 100k+ accumulated interaction tokens, and elevates mid-scale open-weight models to proprietary-level performance.

---

## 21. Learning to Fold: prizewinning solution at LeHome Challenge 2026 (1st place online, 2nd offline)

**Authors:** Ilia Larchenko
**arXiv:** [2606.27163](https://arxiv.org/abs/2606.27163)
**Categories:** Robotics (cs.RO); Artificial Intelligence (cs.AI); Machine Learning (cs.LG)

I describe my solution to the LeHome Challenge 2026, an ICRA 2026 competition on bimanual garment folding. The system placed 1st of 62 teams in the online (simulation) round and 2nd in the real-world final. It improves a vision-language-action (VLA) policy with a reinforcement-learning loop. The policy is its own value function: the same network that predicts actions also predicts success, progress, and a few task-relevant future quantities, and those predictions drive advantage estimation, live failure detection, and candidate selection. The work mostly recombines existing RL ideas with engineering and optimization contributions that can be used together as one recipe or individually: AWR + RECAP combined for flow-matching VLA; an asynchronous distributed training / rollout pipeline through HuggingFace Hub; inference-time hyperparameters optimization via Thompson sampling; a sim-to-real recipe with camera-alignment tooling, heavy augmentation and DAgger-like HIL data collection.

---

## 22. Scalable Behavior Cloning with Open Data, Training, and Evaluation

**Authors:** Arthur Allshire, Himanshu Gaurav Singh, Ritvik Singh, ..., Philipp Wu, Angjoo Kanazawa
**arXiv:** [2606.27375](https://arxiv.org/abs/2606.27375)
**Categories:** Robotics (cs.RO)

We introduce ABC, a fully open-source stack for manipulation with behavior cloning. At its core is ABC-130K: the largest open-source teleoperation dataset to date, featuring 3,500 hours of data spanning over 130K episodes across 195 diverse tasks. Furthermore, we open-source our accessible hardware setup, training infrastructure, and simulation pipeline. We also release 400 hours of sim-teleop data and provide a co-training recipe that produces correlated simulation and real-world evaluation, offering a reliable proxy for ablating model-design and training decisions before costly real-world evaluation. We explore various training recipes and compare common architectural choices for Diffusion Transformers (DiT) and Vision-Language-Action (VLA) models, grounding our findings in real-world evaluations. The resulting policies successfully execute dexterous tasks such as box folding and extracting credit cards from wallets. By providing a reproducible toolkit, we aim to place researchers on an equal footing, establishing the necessary foundation to learn the ABCs of Behavior Cloning together as a community.

---

## 23. KRVF: A Source-Aware Semantic Voxel World Representation for Edge Mobile Manipulation

**Authors:** Runfeng Ling
**arXiv:** [2606.26321](https://arxiv.org/abs/2606.26321)
**Categories:** Robotics (cs.RO)

Mobile manipulators need world models that are current, queryable, semantically meaningful, and usable under edge-compute constraints. This technical report presents KRVF, a source-aware semantic voxel world representation for edge mobile manipulation. Unlike reconstruction-centric mapping pipelines that primarily optimize global geometric fidelity, KRVF represents local world state as task-oriented voxels that encode occupancy, color, semantic evidence, temporal freshness, and evidence source. The representation separates measured occupancy from semantic-prior hypotheses, enabling depth-failure-aware object reasoning without silently corrupting persistent geometry. KRVF also closes a feedback loop between mapping and sensing by rendering map-prior depth for repair, and exposes task-level query operators for semantic objects and grasp candidates. The report formalizes the KRVF representation and documents a ROS 2 implementation that turns online RGB-D observations into a task-facing robot memory.

---

## 24. PhysiFormer: Learning to Simulate Mechanics in World Space

**Authors:** Yiming Chen, Yushi Lan, Andrea Vedaldi
**arXiv:** [2606.27364](https://arxiv.org/abs/2606.27364)
**Categories:** Computer Vision and Pattern Recognition (cs.CV)

We present PhysiFormer, a diffusion transformer for physically-plausible 3D object motion. Unlike video world models that operate in view-dependent pixel space, PhysiFormer represents objects as 3D meshes expressed in world coordinates. Given the initial vertex positions and velocities, as well as object material type, rigid or elastic, the model samples future vertex trajectories. While related neural physics approaches build on ad-hoc latent spaces or explicitly enforce rigidity and causality, PhysiFormer shows that excellent results can be obtained without any such inductive biases, by casting vertex trajectory prediction as a single denoising diffusion process directly in world coordinates. The probabilistic formulation captures uncertainty in the learned dynamics, enabling diverse plausible futures from initial conditions, making this framework potentially useful for applications with unobserved uncertainty. The model features attention factorised over time, space, and objects for efficiency, enabling permutation-invariant multi-object reasoning without needing explicit object encoding. Trained on over 100k simulated trajectories, PhysiFormer generates rigid and elastic mechanics, and generalises to mixed-material settings, unseen real-world geometries, and larger object counts. It substantially outperforms autoregressive baselines in trajectory accuracy, rigidity preservation, and momentum-based physical consistency. Our results position coordinate-space diffusion as a promising step toward view-invariant, geometry-aware world modelling for robotics, graphics, and physical design. Visualisations, code, and models are available at this https URL.

---

## 25. Neural Voxel Dynamics: Learning Implicit 3D Physics via Volumetric Feature Advection

**Authors:** Zican Wang, Niloy Mitra
**arXiv:** [2606.26410](https://arxiv.org/abs/2606.26410)
**Categories:** Computer Vision and Pattern Recognition (cs.CV)

We present a self-supervised framework for learning implicit 3D physical dynamics directly from video-derived supervisory signals. While current generative video models achieve high visual fidelity, they lack a 3D geometric foundation, often resulting in physical inconsistencies and a failure to maintain object permanence. We address this by shifting the predictive bottleneck from 2D image space to a `lifted' 3D Volumetric Latent Space. Our method unprojects semantic features from a Video Joint-Embedding Predictive Architecture (V-JEPA) into a voxelized grid, grounded by monocular depth priors. This lifting enables a Volumetric Feature Advection to learn an action-conditioned transition operator that treats physics as a spatio-temporal state advection problem, i.e., learn implicit 3D physics. Unlike state-of-the-art hybrid models that rely on explicit classical simulators for training and/or inference, our architecture tracks material states implicitly within high-dimensional V-JEPA features. This allows for the emergent simulation of heterogeneous phenomena (e.g., rigid body motion in fluid flow) within a single, unified pipeline. Supervised solely via end-to-end video-derived signal plus action conditions, without access to physics engine internal states, labels, or surrogate models, our model demonstrates good long-term structural stability and physical plausibility on multiple benchmarks (CLEVERER, PhysInOne, PhysGaia). We believe that this work opens a scalable pathway toward general-purpose dynamic world models that internalize the 3D invariants of the physical world solely through passive observation of monocular videos.

---
