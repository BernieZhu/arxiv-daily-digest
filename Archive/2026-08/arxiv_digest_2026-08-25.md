# arXiv Daily Digest — 2026-08-25

**Mode:** direct
**Categories:** cs.AI, cs.LG, cs.RO, cs.CV
**Keywords:** VLA, world model, world action model
**Papers found:** 27

---

## 1. ReWorld: An Interactive World Model with Long-Horizon Memory

**Authors:** Zhifei Chen, Luozhou Wang, Guibao Shen, ..., Lianghua Huang, Yingcong Chen
**arXiv:** [2608.23565](https://arxiv.org/abs/2608.23565)
**Categories:** Artificial Intelligence (cs.AI)

An interactive world model must follow the user's actions, remember the places it has shown, and stream in real time. The tension is structural: control wants a short horizon, memory wants an unbounded one. ReWorld separates the two during training and bounds them at inference. Mixed per-head attention windows confine most heads to the recent past while a small set of global heads attends over the entire history, and random head routing keeps either capability from binding to particular heads; random chunk dropping makes sparse histories in-distribution. At inference the whole past lives under a fixed budget: a bounded KV cache backed by a pose-indexed landmark bank, from which the model retrieves the landmarks nearest the current pose. A metric-scale-aligned data engine places eight sources -- Unreal-rendered fly-throughs, game roaming, and real-world footage -- on one physical action scale, so the same key press moves the camera the same distance in every source, and palindrome trajectories supply the revisit evidence that memory training needs. Distribution-matching distillation confined to a LoRA adapter then compresses sampling to four steps: one backbone serves both a high-fidelity multi-step mode and a real-time interactive one, streaming 704x1280 video across photorealistic, game-style, and stylized worlds. Under a three-axis protocol covering action following, long-horizon recall, and video quality, against six recent interactive world models it attains the best control fidelity ($11.95^\circ$ rotation error and the best camera-motion consistency) and the best generation quality; and on minute-long out-and-back rollouts ($64$\,s, $384$ latents), its fixed 12-chunk cache still regenerates the starting view -- at rollout lengths where a sliding window has long evicted the evidence and full-KV attention runs out of memory.

---

## 2. Correcting a learned physical invariant improves world-model rollouts

**Authors:** Richard Bao
**arXiv:** [2608.23526](https://arxiv.org/abs/2608.23526)
**Categories:** Artificial Intelligence (cs.AI)

World models can predict video without learning dynamics that they reliably preserve. We test whether a frozen DreamerV3 trained only on pendulum video learns a scalar that its own latent transition treats as approximately conserved. A label-free search recovers the same energy-like invariant across independently trained conservative models, while the same procedure finds no comparable invariant in matched damped models. During autonomous rollouts, this quantity drifts. Projecting the latent state back toward its initial level set reduces rollout error in all three conservative models, whereas matched random constraints usually increase it. These results distinguish a dynamically meaningful invariant from a merely decodable correlate and reveal a concrete failure mode: a world model can learn a physical constraint from pixels yet violate that constraint when it imagines forward.

---

## 3. From Generation to Simulation: How Far Are World Models from Being True Simulators?

**Authors:** Tong Wang, Huan Deng, Mucheng Yang, ..., Xiaohui Kuang, Gang Zhao
**arXiv:** [2608.23070](https://arxiv.org/abs/2608.23070)
**Categories:** Artificial Intelligence (cs.AI); Computer Vision and Pattern Recognition (cs.CV)

With the rapid progress of diffusion models and large-scale video generation, generative world models are increasingly expected to replace traditional simulators, including physics engines, game engines, and reinforcement-learning environments. Yet the remaining distance from generation to simulation lacks a systematic assessment. We present a capability-based study using an external yardstick: eight capabilities of a traditional simulator, namely asset construction, physics engine, interaction, controllability, stability, state feedback, diversity, and evaluation metrics. We trace three main technical routes--latent dynamics, video generation, and joint-embedding prediction--and map exactly 200 representative works published from 2018 to June 2026 onto these capabilities. Our analysis shows that world models have achieved functional substitution in interaction and controllability for specific scenarios, but remain short of traditional simulators in formal guarantees of physical laws, structured state feedback, and reproducible long-horizon evolution. State feedback is the most neglected cross-route shortcoming: only 6 of 163 implementation papers expose a runtime interface for querying entity states or physical parameters. We identify six research directions: formalized physics, a unified action interface, first-class state feedback, long-horizon stability, downstream-utility evaluation, and cross-route hybridization. Project page: this https URL

---

## 4. Where World Models Break: Natural-Input Failure Discovery

**Authors:** Zhanpeng Shi, Zi Liang, Rong Feng, ..., Xuyang Chen, Hongzong Li
**arXiv:** [2608.22421](https://arxiv.org/abs/2608.22421)
**Categories:** Artificial Intelligence (cs.AI)

World models predict action-conditioned futures and serve as critical internal simulators for downstream planning and control. However, catastrophic prediction failures of world models could dangerously propagate through the control pipeline, as subsequent agent or model training and decision-making depend heavily on the continuous environment evolution forecasted by these world models. Existing evaluations overlook this systemic risk: by aggregating average errors over benign generations from general queries, they fail to stress-test the model against catastrophic collapses under rare or unobserved condition-action combinations. To bridge this gap, we formalize the natural-input failure discovery problem: under a finite query budget, finding environment-valid conditions and action prefixes that induce severe prediction risk, verifying whether these failures reproduce on fresh seeds, and testing their persistence under nearby valid edits. Discovering such critical failures is computationally challenging, as valid condition-action combinations explode exponentially, rendering exhaustive search or standard sampling infeasible given the high cost of noisy rollouts. To tackle this, we propose BasinLens, which exploits the underlying structure of valid inputs, where each coordinate possesses environment-defined semantic types and admissible domains, by pairing uncertainty-guided global search with typed local replacements. Across diverse benchmarks and world-model families, BasinLens exposes reproducible and locally persistent failure modes that conventional evaluations fail to reveal, showing that average-case benchmarks can mask important vulnerabilities in world-model-driven control.

---

## 5. WAM-OPD: On-Policy Distillation for World Action Models

**Authors:** Liuhaichen Yang, Zhuang Jiang, Chenchao Sheng, Zezhi Tang
**arXiv:** [2608.22364](https://arxiv.org/abs/2608.22364)
**Categories:** Artificial Intelligence (cs.AI); Robotics (cs.RO)

World action models (WAMs) couple visual future prediction with robot action generation, but accelerated students can lose task capabilities during distillation and later encounter states that are poorly represented by offline data. We study whether on-policy distillation (OPD) can repair such a student without requiring sparse-reward reinforcement learning. We introduce WAM-OPD, a deployment-consistent post-training recipe for a video-first WAM. The student acts in the environment and therefore determines the history distribution. A frozen teacher labels those student histories with coherent video and action targets, while the student action branch is trained under its own generated video plan, as it is at deployment. Joint video and action losses update lightweight adapters in the shared backbone, together with an action flow-matching regularizer. In preliminary RoboTwin 2.0 studies on two tasks, the released one-video/one-action-step Flash-WAM improves from 0.0% to 58.3% success on HANDOVER MIC, and from 16.7% to 33.3% on PUT OBJECT CABINET. These task-specific results are an initial capability proof rather than evidence of broad or uniform generalization. They nevertheless suggest that dense teacher supervision on student-induced histories is a promising post-training interface for video-first WAMs.

---

## 6. Act with Intent: Distilling Behavior Intent for Vision-Language-Action Models

**Authors:** Sangoh Lee, Sangwoo Mo, Wook-Shin Han
**arXiv:** [2608.23478](https://arxiv.org/abs/2608.23478)
**Categories:** Robotics (cs.RO); Artificial Intelligence (cs.AI); Computer Vision and Pattern Recognition (cs.CV)

Vision-Language-Action (VLA) models can turn multimodal context into robot actions, but their action decoders are still trained largely by behavior cloning. This supervises which motor command was demonstrated while leaving implicit the local objective served by the behavior under the instruction. Future-based supervision enriches action learning with frames, latent observations, trajectories, or motion representations, but these signals capture particular realizations of what may happen rather than the shared semantic objective of the forthcoming behavior. We propose Intention Distillation (INDI), which distills behavior-level intent into the action decoder. During training, a frozen teacher VLM interprets a demonstrated segment from the current observation, instruction, coarse action summary, and corresponding execution video. From its standard inputs, the deployed VLA recovers the resulting multimodal intent representation at an intermediate decoder layer and uses it to organize action prediction together with representations of how the behavior unfolds and what it achieves. On SimplerEnv-Bridge, INDI improves GR00T-N1.7 from 64.3% to 84.7%, and on RoboCasa Kitchen it improves the controlled GR00T-N1.7 baseline from 64.1% to 70.3%, with consistent gains on $\pi_{0.5}$ across both benchmarks. In real-world tasks, INDI improves average success from 62.0% to 68.7%, with gains of up to 12.0 pp on longer-horizon tasks. Further analyses show that the recovered latent is used by the decoder, captures behavior objective and execution progress, and organizes downstream predictions in an objective-dependent manner. These results show that action decoders benefit from explicitly modeling the semantic objective of the behavior they generate.

---

## 7. Future Querying: Can LLMs Serve as Implicit Medical World Models?

**Authors:** Siri Willems, James Butterworth, Lore Goetschalckx, ..., Elke Giets, Ludovic Denoyer
**arXiv:** [2608.23248](https://arxiv.org/abs/2608.23248)
**Categories:** Computation and Language (cs.CL); Artificial Intelligence (cs.AI)

Traditional clinical prediction models rely on task-specific pipelines and curated, structured data, which scale poorly and underutilize unstructured text. To address this, we introduce future querying, a paradigm that probes whether large language models (LLMs) can function as implicit medical world models by evaluating their ability to answer time-indexed clinical queries about a patient's future. Our framework operates on unstructured clinical documentation using endpoint-agnostic training, enabling a single model to answer diverse clinical queries over patient trajectories without manual feature engineering or task-specific retraining. We show that small, locally fine-tuned open-weight models can match or approach larger proprietary systems, making the framework suitable for privacy-preserving, on-premise deployment. Evaluated on a new synthetic medical reports dataset and real ICU notes from the MIMIC-IV dataset, our results provide encouraging evidence that LLMs can capture aspects of clinical dynamics.

---

## 8. Think Only When Needed: Prompt-Authority Control for Selective Slow-Path Intervention in Vision-Language-Action Manipulation

**Authors:** Zhiruo Zhou, Zelin Li, Xiwen Chen, ..., Huiming Chen, Xiaojun Zhu
**arXiv:** [2608.23224](https://arxiv.org/abs/2608.23224)
**Categories:** Robotics (cs.RO); Artificial Intelligence (cs.AI); Computer Vision and Pattern Recognition (cs.CV)

Retrieval can efficiently and effectively augment a frozen vision--language--action (VLA) policy without retraining, yet retrieved text becomes a control intervention once it enters the executed prompt. In a matched audit, raw appended text reduces mean success from 92.47\% to 3.00\%, while meaningful and length-matched meaningless appends both fail on all 500 states. This result identifies \emph{prompt-form collapse}: changing the instruction form, rather than adding useful semantics, can dominate execution. We introduce TOWN-VLA (Think Only When Needed), a prompt-authority interface that separates candidate generation from permission to alter the policy input. A fixed compatibility rule authorizes a canonical compact instruction; otherwise, the interface restores the original Base prompt exactly. Across 900 audited routes, every route follows this contract: 525 routes recover Base with matching hashes, and all 375 authorized prompts preserve the task signature. On a matched $4\times7$ LIBERO-Plus evaluation with 10{,}030 episodes per method, success rises from 69.5\% to 73.1\% ($+362$ episodes; 95\% CI 1.89--5.45 points), improving on six perturbation axes and all four suites. On a physical PiPER arm with a frozen \pizerofive{} checkpoint, success rises from 52.7\% to 78.7\% over 150 trials per method ($p=3.16\times10^{-6}$). Prompt authority is enforceable for a frozen controller; oracle-free admission calibration is the next deployment target.

---

## 9. Pointing-VLA: Typed Spatial Grounding Interfaces for Vision-Language-Action Manipulation

**Authors:** Xiwen Chen, Zelin Li, Zhiruo Zhou, ..., Chenwei Wang, Xiaojun Zhu
**arXiv:** [2608.23138](https://arxiv.org/abs/2608.23138)
**Categories:** Robotics (cs.RO); Artificial Intelligence (cs.AI); Computer Vision and Pattern Recognition (cs.CV)

Vision-language-action (VLA) models often expose spatial grounding through autoregressive text coordinates or opaque action tokens, creating brittle interfaces between multimodal reasoning and robot execution. We present Pointing-VLA, a typed hidden-state spatial readout built on Embodied-R1. Geometry-specific heads predict normalized points, object-functional grounding (OFG) heatmaps, and visual trajectories without serializing geometry as text. For the evaluated Bridge/WidowX and physical pick-place deployments, an explicit execution contract assigns PICK to source-conditioned OFG and PLACE to Pointing, providing direct stage-aligned spatial targets. Pointing-VLA achieves SOTA performance on Bridge/WidowX, averaging 72.9\% across the evaluated four-task set without Bridge-specific finetuning under collision-enabled CuRobo execution. Pointing and OFG show complementary strengths across native and cross-dataset evaluations. The OFG/contact readout transfers to NORA-1.5, preserving or improving success while reducing recorded controller time by more than 20$\times$; typed heads are also 6.68--6.90$\times$ faster than Embodied-R1 text decoding on a shared external suite. When integrated as spatial guidance for a $\pi_{0.5}$ action policy, Pointing-VLA raises autonomous real-robot success from 52.7\% to 80.7\% across three visual contexts. These results establish typed spatial readouts as an efficient, inspectable interface between embodied reasoning and robot execution.

---

## 10. Geo-VLA: Geometry-Aware Vision-Language-Action Planning via Internalization of Map Semantics

**Authors:** Ran Chen, Jiaxing Ren, Zhikun Zhang, ..., Junbao Zhuo, Bochao Zou
**arXiv:** [2608.21440](https://arxiv.org/abs/2608.21440)
**Categories:** Robotics (cs.RO); Artificial Intelligence (cs.AI)

Vision-language-action (VLA) models have advanced end-to-end autonomous driving by leveraging foundation models for semantic reasoning and long-tail generalization. However, their planning performance remains limited in complex driving environments because image-only representations inadequately capture planning-relevant road geometry and topology. In this paper, we propose Geo-VLA, a plug-and-play framework that enhances VLA models by learning geometry-aware visual representations. During training, Geo-VLA internalizes geometric map semantics to strengthen road-structure representations, while requiring no HD maps or additional lane information during inference. To support this approach, we introduce Geo-QA, a geometry-focused question-answering dataset that injects road geometry into vision-language representations through contrastive learning and instruction tuning. Experiments on NAVSIM v1 demonstrate that Geo-VLA consistently improves VLA planners with distinct action-generation architectures, achieving 92.1 PDMS and establishing a new state-of-the-art among single-camera VLA planners.

---

## 11. Mamba-based Selective State Space Modeling Improves the Accuracy-Complexity Tradeoff of SmolVLA Vision-Language-Action Experts

**Authors:** Farida Mohsen, Thowayba Elkaffash, Mohammad Reza Chalak Qazani, ..., Nader Meskin, Ali Safa
**arXiv:** [2608.21407](https://arxiv.org/abs/2608.21407)
**Categories:** Robotics (cs.RO); Artificial Intelligence (cs.AI)

Vision-language-action (VLA) models face a crucial tradeoff between their task success rate and the policy-call frequency. Executing a single action per inference ($N=1$) enables accurate robot control but comes at the cost of huge compute time overheads, making real-time implementation infeasible. On the other hand, executing longer action horizons before replanning ($N\gg1$) reduces compute complexity, but inevitably degrades the system's success rate. In order to improve the VLA accuracy-complexity tradeoff, this paper investigates Mamba's selective state-space modeling as an alternative to causal self-attention within the action expert of the popular SmolVLA model, widely used as a reference model for its highly accurate yet low complexity nature. We evaluate both the Mamba- and Transformer-based experts on the widely-adopted LIBERO benchmark suites across three execution horizons $N\!\in\!\{1,25,50\}$, respectively corresponding to high, moderate and low compute complexities. Our results remarkably show that the advantage of the Mamba expert increases with the execution horizon, indicating significant success retention under long execution horizons $N = 50$ and $N = 25$. When $N = 50$ actions are executed before replanning (i.e., corresponding to feasible real-time deployment), the Mamba expert outperforms the Transformer baseline by $7.8\%$. In addition, when $N = 25$ actions are executed before replanning, our Mamba expert outperforms the Transformer baseline by $3.7\%$. Finally, under per-action replanning ($N=1$), our Mamba variant matches the Transformer-based mean success rate while significantly reducing the overall model parameter complexity by $24\%$ thanks to Mamba's compute-efficient nature.

---

## 12. LpWM: A Case for Sparse Representations in World Models

**Authors:** Yilun Kuang, Yash Dagade, Quentin Le Lidec, ..., Randall Balestriero, Yann LeCun
**arXiv:** [2608.22764](https://arxiv.org/abs/2608.22764)
**Categories:** Machine Learning (cs.LG)

Joint-embedding predictive architectures (JEPAs) learn latent dynamics for planning and avoid representation collapse by matching features to maximum-entropy distributions such as isotropic Gaussians, yielding dense representations. However, it is unclear whether dense representations are the most favorable geometry for modeling dynamics. In this work, we ask whether a different geometry, sparse representations, can make action-conditioned latent dynamics easier to model, and what dynamical structure emerges from such representations. We first show that nonlinear Lipschitz dynamics can be approximated arbitrarily well by action-conditioned linear dynamics in a sufficiently high-dimensional one-hot latent space, with rollout error vanishing as the dimension grows. This motivates distributed sparse representations as a practical relaxation of one-hot sparsity. We introduce LpWorldModel (LpWM), a JEPA model regularized with Rectified Distribution Matching Regularization (RDMReg) to match encoder features to a Rectified Generalized Gaussian distribution, yielding non-negative sparse codes. Empirically, sparsity lowers the predictor complexity required for successful planning: on PushT, sparse LpWM outperforms dense LeWM by up to 57% in planning success at intermediate predictor capacities. This advantage also extends beyond Gaussian distribution matching, with LpWM outperforming dense VICReg representations across multiple predictor families. We further find that the learned sparse representations are mode-factored, with support encoding discrete dynamical regimes and feature magnitudes capturing continuous within-regime state. Together, these results suggest that sparse representations can reduce the predictor complexity required for control while revealing interpretable structure.

---

## 13. MOSH-WM: Mask-Grounded Soft-Hamiltonian Dynamics for Object-Centric World Models

**Authors:** Zhekai Wang, Haoxiang Huang, Xiang Liu, ..., Miao Liu, Sen Cui
**arXiv:** [2608.22750](https://arxiv.org/abs/2608.22750)
**Categories:** Machine Learning (cs.LG)

Object-centric world models forecast future videos by evolving a set of entity slots, but the variables receiving dynamics supervision are often unconstrained visual features. We introduce \method{}, a mask-grounded soft-Hamiltonian world model that makes its position-like state explicitly depend on slot-owned image support. A frozen video-slot encoder produces slots and masks; spatial moments of mask-owned support form a canonical state $Q$, temporal differences form $P$, and a learned energy supplies a soft directional bias to a bounded learned increment. Decoder-relevant appearance and identity are stored separately in a causal visual context. A gated composer and bounded residual then combine this context with the propagated phase state to reconstruct decoder-compatible slots. On OBJ3D, given six observed frames and evaluated over the following 30 frames, \method{} reduces LPIPS by 25.0\% and spatial MSE by 33.7\% relative to the strongest object-centric baseline. On CLEVRER, given six observed frames and evaluated over the following ten frames, the corresponding reductions are 14.5\% and 18.7\%. Horizon-resolved visual and object-state measurements show that the complete model accumulates error more slowly throughout the 30-frame closed-loop rollout. Project page:this https URL.

---

## 14. On the Capability Separation Between World-Model Policy Learning and Imitated World-Action Models

**Authors:** Yang Yu
**arXiv:** [2608.22197](https://arxiv.org/abs/2608.22197)
**Categories:** Machine Learning (cs.LG)

World-action models predict a future outcome and then infer an associated action. Although this factorization can improve representation learning and data efficiency, it is unclear whether it provides stronger control capability than direct behavior cloning when both are trained from the same observational demonstrations.
We compare a direct behavior-cloning policy, an imitation-trained world-action policy, and a policy optimized with an action-conditioned world model. At the controller-class level, every world-action policy can be flattened into a direct stochastic policy with the same closed-loop trajectory distribution. At the population level, under realizability, exact optimization, common deployment information, and distribution-preserving deployment, direct behavior cloning and world-action imitation both recover the observational behavior policy. Thus, future prediction changes the learning factorization but not the unrestricted external policy class or ideal imitation target.
Action-conditioned world-model learning differs by predicting outcomes under specified actions and comparing them through a control objective. We characterize the irreducible action-specific prediction error of future models that do not condition on the candidate action, identify conditions under which a world-action joint can recover an interventional forward model, and show that observational demonstrations do not identify action effects in general. Finally, we construct an environment family in which every observational learner has positive worst-case regret, whereas one informative intervention permits zero regret. The key distinction is therefore between predicting futures associated with observed behavior and predicting consequences of specified actions for policy optimization.

---

## 15. Reading the Room: Implicit Confusion Encoding in Recurrent World Model States

**Authors:** Donald Aadithiyan
**arXiv:** [2608.21582](https://arxiv.org/abs/2608.21582)
**Categories:** Machine Learning (cs.LG)

World models built on the RSSM architecture, such as DreamerV3, keep a recurrent hidden state $h_t$ trained only to reduce prediction error. We show this state also tracks its own confusion, hiding in plain sight: nearly orthogonal to $h_t$'s directions of greatest variance, invisible to any variance-based method. It is functionally distinct from ensemble disagreement, which flags new inputs, and reconstruction error, which flags bad predictions right now. On a test holding prediction error fixed while confusion varies, a linear probe on $h_t$ finds the signal (AUROC 0.72, 5 runs), while an ensemble baseline scores below chance. A discounted count of recent high-error steps explains 80% of the probe's output ($R^2=0.80$). We confirm the signal is causally used, not merely present, by editing $h_t$ directly and watching behaviour change, including a check using real values from other trajectories instead of synthetic edits. Its geometry and closed form generalize across three control tasks; the decisive dissociation test itself holds cleanly on only one, and its practical use, deciding when to check reality instead of trusting imagination, generalizes to only two of the three tasks.

---

## 16. RiskWorld: Object-Centric Latent World Modeling for Autonomous Driving Risk Identification

**Authors:** Jingzheng Li, Yufei Ge, Qianren Mao, ..., Baochang Zhang, Xianglong Liu
**arXiv:** [2608.21414](https://arxiv.org/abs/2608.21414)
**Categories:** Robotics (cs.RO); Machine Learning (cs.LG)

Autonomous driving risk identification aims to determine which observed object is likely to become safety-critical to the ego vehicle. Existing approaches typically predict scene-level accidents, infer risk objects indirectly from ego behavior, or apply geometric checks after trajectory forecasting, without directly using predicted ego--object relations for risk-source localization. We propose RiskWorld, an object-centric latent world model that identifies risk from the imagined evolution of each candidate relative to the ego vehicle. RiskWorld combines pretrained predictive video representations with structured ego--object histories, contextualizes observed interactions, and rolls relation-aware object states into the future using RSSM-style latent dynamics. It decodes the rollout into object-level risk scores, supported by auxiliary future-relation and temporal-risk predictions. Inference uses only observations up to the current time, while logged futures provide training supervision. On RiskBench, RiskWorld achieves the best overall F1 of 63.0\% and the lowest false-alarm rate of 2.1\%. Further analyses show that the learned rollout captures the evolution of object-level risk before critical events, while RiskWorld's selections preserve planning-critical information under filtered observation.

---

## 17. ROS2SmolVLA: Enabling Small Vision-Language-Action Models for Integration into Industrial-Grade Lightweight Robots

**Authors:** Nils Mandischer, Noah Böckmann, Ludwig Holl, Lars Mikelsons
**arXiv:** [2608.23320](https://arxiv.org/abs/2608.23320)
**Categories:** Robotics (cs.RO)

Industrial demand changes the paradigms of production. Due to smaller batch sizes and more variations in products, companies face a growing challenge to adopt more adaptive production systems. In particular, robot-based automation is usually static and fails to respond to constantly changing processes. Vision-Language-Action (VLA) Models are a promising opportunity to mitigate this challenge by generating robot actions based on the observed system state. However, current research either focuses on large models that cannot be computed on premise, creating compliance and security challenges, or use lab-grade robot hardware that obscures exploitation in real industrial settings. In this work, we adapt Hugging Face's SmolVLA for Universal Robots lightweight robots. Further, we release the open-source repository ROS2SmolVLA that implements an interface for ROS 2 to SmolVLA, and makes it applicable for industrial-grade hardware. By this, we allow a lenient adoption into lab and industrial environments. We validate the functionality of SmolVLA for a Universal Robots UR10e using a pick-and-place task and give implementation guidelines. Our findings support that SmolVLA is a well-suited option for small-sized tasks that need to be computed on premise.

---

## 18. UniMem: Unifying Multimodal Memory and Control for Vision-Language-Action Models

**Authors:** Lars Osterberg, Maggie Wang, Mac Schwager
**arXiv:** [2608.22869](https://arxiv.org/abs/2608.22869)
**Categories:** Robotics (cs.RO); Computer Vision and Pattern Recognition (cs.CV)

While Vision-Language-Action (VLA) models have leveraged internet-scale pretraining and task-focused finetuning to achieve strong performance on long-horizon tasks, they often struggle with non-Markovian tasks that require memory. Existing approaches to memory typically involve additional Vision-Language-Models (VLMs) for long-term memory management, introducing a memory bottleneck and a fractured training pipeline. Conditioning on multiple historical frames can provide the VLA with access to more descriptive features of past scenes, but can degrade performance if frames are chosen at arbitrary, fixed intervals. To address these limitations, we present UniMem, a framework that unifies high-level, multimodal memory and low-level control under one backbone. UniMem employs an event classifier for memory updates, a keyframe encoder for dense spatial memory, and a keyframe caching technique to minimize overhead during policy rollouts. We evaluate UniMem across five simulation and four hardware tasks targeting sequential and spatial memory, demonstrating that our unified, single-model system outperforms fixed-interval image sampling baselines (93.4% vs. 68.2%) in simulation and hierarchical baselines (80.0% vs. 43.5%) in hardware, while offering faster inference and a simple training pipeline for easy adoption. Project website: this https URL

---

## 19. Robust Bimanual Vision-Language-Action Models via Embarrassingly Simple Modality Masking

**Authors:** Dongzhou Cheng, Ziang Li, Yixiao Zhou, ..., Jie Gui, Jiaqi Wang
**arXiv:** [2608.22419](https://arxiv.org/abs/2608.22419)
**Categories:** Robotics (cs.RO); Computer Vision and Pattern Recognition (cs.CV)

Query-based Vision-Language-Action (VLA) models offer low-latency inference that is attractive for bimanual robotic manipulation, but we observe that they can still exhibit discontinuous actions and execution failures in complex dual-arm tasks. We hypothesize that unstable multi-view and language fusion is one contributing factor in these failures, often coinciding with attention spreading to distracting regions. To improve robustness, we introduce the Modality Masking Mechanism (M3), an embarrassingly simple, training-only strategy that requires no architectural changes or large-scale robot pretraining. M3 stochastically masks subsets of modality channels during training, exposing the policy to controlled partial observations and encouraging it to rely less on distracting cues and more on evidence that remains reliable. We evaluate M3 on ten bimanual tasks from RoboTwin 2.0 and on three long-horizon real-world tasks. Compared with the Adapter baseline, M3 improves average success by 21.7% in the Clean setting and 11.4% in Clean2Rand, where policies are trained on clean demonstrations and evaluated on randomized scenes, while also improving averaged real-world full-task success by over 30%. These results suggest that structured training-time masking is a practical way to improve the robustness of query-based VLA policies for bimanual manipulation.

---

## 20. LD4WAM: Learning Latent Dynamics from Human Videos for World Action Models

**Authors:** Zhenhao Shen, Jiaqi Liang, Jasper Lu, ..., Chen Xie, Ruihai Wu
**arXiv:** [2608.22403](https://arxiv.org/abs/2608.22403)
**Categories:** Robotics (cs.RO)

Human video is playing an increasingly central role in training World Action Models (WAMs), owing to its diversity and low collection cost relative to teleoperated robot data. However, most WAMs learn from such video only by predicting pixel-level future frames, giving dynamics that are not directly actionable, whereas motion retargeting recovers directly actionable actions but leaves a large visual gap across embodiments. We therefore propose motion-aligned latent dynamics as an embodiment-agnostic representation to bridge video priors and low-level actions. We further present LD4WAM, which pairs a Latent Dynamics Model trained with semantic reconstruction and real motion alignment with a World Dynamics Action Model built as a mixture-of-transformers (MoT), which preserves full future-video generation and uses learnable queries to distill these latent dynamics from generated futures for action conditioning. Pretrained on our curated unified dataset of over 5{,}000 hours of human and robot data, LD4WAM performs strongly in RoboTwin simulation and on real robots equipped with both grippers and dexterous hands, while generalizing well to unseen objects and backgrounds.

---

## 21. Beyond Instance Slots: Semantically Rich World Models for Physical Interaction Planning

**Authors:** Juntao Cheng, Jingkai Wang, Yijun Shen, Xiansheng Chen, Zhiwei Yu
**arXiv:** [2608.22294](https://arxiv.org/abs/2608.22294)
**Categories:** Robotics (cs.RO)

World models for physical interaction are typically trained to predict future observations or latent features; however, a planning-oriented model must answer a fundamentally different question: whether a candidate action produces a task-consistent future while preserving essential this http URL state representations obscure the underlying entities, while standard instance-level object slots merely identify \emph{what} is present without specifying \emph{what role} each entity plays in the task context. To bridge this gap, we present the Semantically Rich World Model (SR-WM), a task-conditioned world model structured around five functional roles: gripper, target, goal, relation, and this http URL SR-WM, a visual entity encoder extracts soft entity hypotheses from pretrained patch features, allowing segmentation masks to serve as optional proposal priors without mandating them as required state representations or inference inputs.A role binder subsequently maps these hypotheses to task-specific roles, while an action-conditioned dynamics model predicts role transitions alongside fine-grained semantics, including grasp/contact, predicate establishment, relation preservation, fixture state, and phase this http URL, this unified role state grounds downstream multi-candidate action generation, stage-aware reranking, and violation-aware suffix this http URL comprehensive evaluation protocol spans all four LIBERO simulation suites, cross-suite transfer, perception diagnostics, and action-sensitivity this http URL, this formulation transforms object-centric prediction into a semantic interface linking visual dynamics with planning-oriented decision making.

---

## 22. DreamMimic: Learning Visuomotor Whole-Body Loco-Manipulation via World Model

**Authors:** Jie Yin, Xingyu Lai
**arXiv:** [2608.22278](https://arxiv.org/abs/2608.22278)
**Categories:** Robotics (cs.RO)

Vision-based whole-body loco-manipulation on humanoid robots is challenging due to partial observability, contact-rich dynamics, and the difficulty of learning long-horizon behaviors from high-dimensional visual inputs. We present \href{this https URL}{DreamMimic}, a framework that distills privileged teacher policies into vision-based humanoid controllers via world-model-assisted distillation. Instead of using a Dreamer-style RSSM for planning, we repurpose it to learn predictive latent dynamics that serve as both a representation space and an action-conditioned multi-step supervision signal, while exposing compact predictive features to the student policy to reduce long-term drift. Beyond standard reconstruction objectives for proprioceptive and visual observations, we add auxiliary prediction heads for privileged state, contact, object state, and reward estimation. These heads provide additional supervision related to agent--object interaction and task progress, encouraging the latent representation to retain signals that are useful for contact-rich loco-manipulation. We further introduce Performance-Conditioned Guidance (PCG), a reward-driven adaptive distillation schedule that computes performance scores for both teacher and student to dynamically balance guidance and exploration. PCG prevents both premature teacher annealing and excessive teacher interference in challenging visual settings. Experiments on OMOMO and BEHAVE show improved tracking-based loco-manipulation performance over strong vision-based baselines, without exposing online privileged interaction states to the student at deployment. Qualitative simulations further examine morphology and simulator changes. These results suggest that world models can provide a useful mechanism for stabilizing visual policy distillation in contact-rich humanoid behaviors.

---

## 23. CounterAlign: Counterfactual Supervision for Vision-Language-Action Models

**Authors:** Haru Kondoh, Kei Ota, Asako Kanezaki, Yueh-Hua Wu
**arXiv:** [2608.21740](https://arxiv.org/abs/2608.21740)
**Categories:** Robotics (cs.RO)

Vision-Language-Action (VLA) models are typically trained with behavior cloning (BC) on expert demonstrations. However, BC provides only positive supervision for expert actions, without explicit negative supervision indicating which actions are instruction-inconsistent or otherwise inappropriate. Reinforcement learning (RL) can provide such corrective signals, but often relies on externally specified rewards or curated non-expert data, both of which are costly to obtain in robotics. We show that offline RL for VLA models need not rely on curated non-expert trajectories: successful expert demonstrations alone can be transformed into dense corrective supervision through instruction relabeling. Specifically, by pairing expert actions with mismatched alternative instructions, we synthesize counterfactual instruction-observation-action tuples from the dataset and combine them with adversarial discriminator training to learn an instruction-grounded reward model for offline RL, without collecting additional rollouts or annotations. On the robustness-focused LIBERO-PRO benchmark, our method improves robustness to object position and task perturbations over a strong state-of-the-art baseline. It also outperforms competitive baselines in real-robot experiments on the TX-G2 (compatible with AGIBot G2). More broadly, our results suggest that, for data-constrained VLA learning, extracting denser supervision from each demonstration can complement collecting additional data.

---

## 24. Selective Cross-View Consistency for World Action Models: Held-Out Viewpoint Robustness Without Test-Time Camera Information

**Authors:** Bingqi Huang, Bingchuan Wei, Yingkai Cai, Zhaokui Wang
**arXiv:** [2608.21402](https://arxiv.org/abs/2608.21402)
**Categories:** Robotics (cs.RO); Computer Vision and Pattern Recognition (cs.CV)

World action models (WAMs) jointly denoise future video frames and robot actions, and the video prior is expected to generalize their control. Camera viewpoint change remains one of their hardest perturbation axes. We study a question specific to this model class: when training with same-state cross-view image pairs, on which output coordinates should a consistency loss be imposed? The WAM denoising target mixes view-covariant coordinates, namely the predicted future scene, with view-invariant coordinates, namely the action chunk, future proprioception, and value. We show that consistency applied to the covariant block is provably harmful, shrinking legitimate view-specific content to a fraction $1/(1+4\lambda)$ of its true value, and we verify this shrinkage law in controlled experiments. Selective cross-view consistency (SCVC) therefore constrains only the invariant block, requires no camera labels, extrinsics, depth, or view synthesis at training or test time, and leaves the deployment interface unchanged. We introduce a carve-and-hold-out evaluation protocol on the LIBERO-Plus camera track that separates a distribution-matched ceiling from genuine interpolation and extrapolation to held-out viewpoints, with a matched pair-trained control isolating the effect of the consistency term from pair exposure. On held-out orbital viewpoints beyond the training envelope, SCVC improves closed-loop success over the matched control by 12.2 points (95% CI [7.4, 17.0]; +15.5, CI [11.7, 19.4], under an independent second seed) -- an effect two further camera axes replicate -- while interpolation within the envelope shows no gain in either seed (-1.2 and -4.3 points) and in-distribution competence is preserved (-0.6, -0.2). We also report a cross-backbone audit showing that published camera-robustness numbers are confounded by wrist-camera pose stability.

---

## 25. GeoWAM: Visual Geometry World Action Models for Autonomous Driving

**Authors:** Yiren Lu, Xin Ye, Jiaming Liu, ..., Danhua Guo, Burhan Yaman
**arXiv:** [2608.23486](https://arxiv.org/abs/2608.23486)
**Categories:** Computer Vision and Pattern Recognition (cs.CV); Robotics (cs.RO)

World action models (WAMs) have recently gained increasing attention as a framework for jointly modeling scene evolution and ego actions in autonomous driving. Most existing WAMs learn scene dynamics in pixel space by combining a video-generation backbone for future-observation prediction with an action head for ego-trajectory prediction. Pixels, however, provide only an indirect representation of these dynamics: they entangle geometry and motion with appearance, texture, and illumination, forcing the model to infer three-dimensional transformations from two-dimensional observations. We argue that geometry, represented by point clouds, offers a more natural state space for driving because it explicitly captures spatial structure and the rigid and non-rigid transformations that govern scene evolution while directly aligning with the space in which driving actions are executed. Building on this insight, we introduce \textbf{GeoWAM}, a visual geometry world action model for autonomous driving. Rather than predicting future images, GeoWAM is pretrained to forecast future scene geometry, yielding representations that jointly encode spatial structure and temporal evolution. A geometry-conditioned action head then leverages these learned geometric dynamics to predict future ego trajectories. Extensive open-loop and closed-loop evaluations show that visual geometry world modeling yields substantially stronger driving policies than image-based alternatives, establishing future-geometry prediction as an effective pretraining objective for autonomous driving.

---

## 26. EchoWM: Open and Enterable Omnimodal World Models

**Authors:** Songchun Zhang, Yaowei Li, Junhao Zhuang, ..., Anyi Rao, Nan Duan
**arXiv:** [2608.23189](https://arxiv.org/abs/2608.23189)
**Categories:** Computer Vision and Pattern Recognition (cs.CV)

We present EchoWM, an omnimodal world model for enterable generative media that responds to continuous navigation while jointly generating 720p video, environmental sound, music and speech. We organize interaction around camera intent: in first-person scenes, it specifies observer motion, while in third-person scenes, camera--character dynamics are learned from data without view-specific controllers. Discrete commands and continuous poses are mapped to a shared metric-scale relative 6-DoF trajectory, with dataset-level calibration preserving motion magnitude across heterogeneous data. To jointly learn audio-visual generation and trajectory control, we construct a complementary data engine and adopt progressive training followed by autoregressive post-training for long-horizon generation. Extensive evaluations show that \model achieves strong trajectory following and high visual quality on public world-model benchmarks, supporting both first- and third-person interaction across varied subjects, and maintaining synchronized environmental sound and speech over long-horizon generation.

---

## 27. WorldMind: Decoupled Game World Model for State-Aware NPC Behavior

**Authors:** Zhiyang Deng, Boran Zhang, Danze Chen, Yeying Jin
**arXiv:** [2608.21439](https://arxiv.org/abs/2608.21439)
**Categories:** Computer Vision and Pattern Recognition (cs.CV)

Game world models have recently demonstrated promising capabilities in generating visually coherent and action-controllable gameplay videos. However, non-player character (NPC) behavior in existing models is either implicitly entangled with video generation or explicitly prescribed through external control signals. Consequently, a game world model has to jointly understand the state, plan the NPC's response and render its visual outcome, limiting its ability to produce responsive and state-aware NPC behavior. The challenge lies in the lack of an explicit interface for state-grounded decision-making. To this end, we introduce WorldMind, to our knowledge the first decoupled framework for state-aware NPC behavior in game world models. WorldMind separates interactive world modeling into four layers: an Understanding Layer that constructs a compact state from generated frames; a Decision Layer that reasons over the compact state to plan the NPC's next action; a Control Layer that translates the actions into temporally aligned conditions; and a Generation Layer that synthesizes their visual outcomes. By reconnecting layers in a closed interaction loop, WorldMind grounds NPC behavior in the evolving game state. We further introduce BOSS-140K, a dataset of gameplay videos paired with rich internal game states, together with an agent that automates the collection at scale. Experiments on BOSS-140K demonstrate reliable compact state reconstruction and mechanics-grounded planning, with WorldMind preferred over the baselines in approximately 70% of pairwise comparisons for its more tactically appropriate and coherent NPC behavior. Project page: this https URL

---
