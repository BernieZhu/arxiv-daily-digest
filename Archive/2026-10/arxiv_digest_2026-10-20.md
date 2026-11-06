# arXiv Daily Digest — 2026-10-20

**Mode:** direct
**Categories:** cs.AI, cs.LG, cs.RO, cs.CV
**Keywords:** VLA, RSI, agentic robot, self-improving robot, self-evolving robot, robot harness
**Papers found:** 20

---

## 1. VLA-Rolling: Fewer Denoising Steps, Better Control via Adaptive Action Reuse

**Authors:** Sicheng He, Yi Pan, Qiuting Yu, ..., Xuhong Zhang, Jianwei Yin
**arXiv:** [2610.25043](https://arxiv.org/abs/2610.25043)
**Categories:** Artificial Intelligence (cs.AI); Robotics (cs.RO)

Flow-matching vision-language-action (VLA) models generate an action chunk by iteratively denoising Gaussian noise, but typically execute only a short prefix before replanning with updated observations. Under this receding-horizon paradigm, the unexecuted remainder---the action tail---is discarded, and the next chunk is regenerated from fresh noise. We show that this discarded tail retains transferable denoising progress: action-tail initialization can match or outperform a native 10-step Gaussian baseline using fewer denoising steps. However, the optimal denoising budget varies substantially across samples, indicating that tail reuse should be adapted to the updated environment. Based on this observation, we introduce VLA-Rolling, a lightweight inference framework that reuses action tails through three stages: action-tail inheritance, per-action confidence estimation, and confidence-guided refinement through renoising and denoising budget allocation, while the underlying VLA remains frozen. Across $\pi_{0.5}$, SmolVLA, X-VLA, and MolmoAct2 on LIBERO, MetaWorld, LIBERO-Plus, and RoboTwin 2.0, VLA-Rolling reduces action-chunk inference cost in all 16 model--benchmark pairs, achieving up to a $1.48\times$ speedup, while improving success rate in 14 pairs by up to $15.08$ percentage points. These results show that action tails are not merely discarded predictions, but reusable intermediate states that enable more efficient and accurate VLA inference. These results demonstrate that the action tail can support the generation of better actions with fewer denoising steps. Our project is available at this https URL.

---

## 2. Learning to Compose: Recursive Self-Improvement of Shared Executable Stacks for Zero-Shot Long-Horizon Robot Manipulation

**Authors:** Yangzhi Chen, Feiran Liu, Zishuo Wang, ..., Lecheng Ruan, Wenjuan Han
**arXiv:** [2610.24464](https://arxiv.org/abs/2610.24464)
**Categories:** Artificial Intelligence (cs.AI)

Individually competent robot skills can fail when composed: tools may lack a required capability, completion signals may misrepresent physical progress, and one skill may leave a state that violates its successor's prerequisites. We introduce Recursia, a recursive self-improvement framework that treats the shared executable stack, rather than individual task programs, as the persistent unit of improvement. The stack integrates tools, skills with execution contracts, handoffs, and verifiers. Source-side execution traces guide failure attribution and the generation of missing tools or repairs to existing shared components. Generality checks, mechanism tests, and paired selection and regression gates determine which changes become the next parent. The resulting stack is frozen and reused through declarative task adapters, allowing source-derived changes to support new compositions without target-side code repair. Experiments cover LIBERO-Pro Long simulation and a physical Franka FR3 equipped with a Franka Hand. In simulation, Recursia improves success over ASPIRE by 5.8 percentage points under Pos perturbations and 15.1 points under Task perturbations. Across three physical compositional target tasks, it improves mean success over the Skill Document Only baseline by 40 percentage points. Analyses of constituent execution, candidate rejection, and inference drivers distinguish local mechanism improvements from complete task success and characterize the cost of feedback-conditioned orchestration. These results examine shared executable interfaces as a concrete mechanism for compositional transfer in robot programming.

---

## 3. MELD: Recursive Self-Improvement via Hierarchical Coordination for Multi-Agent Scientific Discovery

**Authors:** Sizhe Tang, Zuyuan Zhang, Zeyu Fang, Tian Lan
**arXiv:** [2610.24454](https://arxiv.org/abs/2610.24454)
**Categories:** Artificial Intelligence (cs.AI)

Multi-agent scientific discovery with large language models raises a coupled learning problem: research assignments determine both which experiments are pursued and the experiences from which agents adapt. We introduce MELD, a unified hierarchical test-time training framework that jointly adapts a team-level Coordinator policy and agent-level individual Scientist policies within a single discovery process. The Coordinator generates a joint portfolio of search branches and research directives over a shared derivation tree, while Scientists develop hypotheses and execution plans implemented by a shared frozen Executor. Both levels receive alternating GRPO-style parameter updates under a shared smooth best-of-budget objective, allowing team organization and individual research behavior to co-evolve in a recursive self-improvement loop. Our analysis establishes objective alignment for the hierarchy, characterizes conditions for coordination gains over independent parallel discovery and the first-order benefit of private adaptation, and derives a finite-budget regret bound for adapted models. On 22 MLGym and MLE-bench tasks, MELD is best on 20 of them and achieves the highest aggregate normalized scores on MLGym, using a 4B backbone for coordination and research. Most baselines use proprietary Scientists, and all systems share one frozen Executor.

---

## 4. Where is Physical RSI capability from? An Observational Scaling Law of LLM-as-policy

**Authors:** Zekai Li, Jiayi Yu, Jinlu Zhang, ..., He Wang, Li Yi
**arXiv:** [2610.26848](https://arxiv.org/abs/2610.26848)
**Categories:** Robotics (cs.RO); Artificial Intelligence (cs.AI); Computer Vision and Pattern Recognition (cs.CV)

In this paper, we systematically investigate the mechanisms, scaling behavior, and generalization of physical Recursive self-improvement. We introduce PhysRSI-eval to quantify physical RSI through a five-axis metric: First-Attempt Performance, Efficiency, Success, Budget and Improvement from failure. Different VLMs are evaluated on 18 manipulation tasks under a fixed interaction budget. The analysis of experimental results motivates the Physical Barrel Hypothesis: different capabilities may constrain different parts of improvement. The five-axis metrics also distinguish systems with close public benchmark averages and show that high scores need not come with early or efficient gains. We study observational scaling from two perspectives: predicting the relative performance of VLM agents from their public capabilities, and forecasting later progress from early physical feedback. Together, these analyses ask how quickly and how far an agent can improve. Moreover, we conduct workspace interventions and then analyze what improvement leaves behind. Removing history reduces late-round success, frozen workspaces remain useful on unseen layouts, and three cross-task cases achieve success earlier. The results suggest that scene-specific adaptation and reusable experience can coexist.

---

## 5. SPAR: Structural Pruning and Action Recovery for Vision-Language-Action Models

**Authors:** Shenli Zheng, Zhou Fang, Yuan Du, Yijiang Liu, Li Du
**arXiv:** [2610.26487](https://arxiv.org/abs/2610.26487)
**Categories:** Robotics (cs.RO); Artificial Intelligence (cs.AI)

The limited onboard computing resources of robots make the inference demands of vision-language-action (VLA) models costly to accommodate. Reducing these demands through aggressive compression, however, can degrade manipulation performance beyond what supervised fine-tuning alone recovers. We present SPAR (Structural Pruning and Action Recovery), which simultaneously prunes the hidden and feed-forward intermediate dimensions of the large language model (LLM) backbone through pruning-aware tuning, then applies reinforcement learning (RL) to recover policy performance. Applied to $\pi_{0.5}$, SPAR reduces the language backbone from 2.34B to 0.09B parameters and the full model from 3.37B to 1.12B, removing approximately 96% and 67% of their parameters, respectively. At this compression level, RL raises average success across the four LIBERO suites from 84.55% to 93.45%, an 8.90-percentage-point gain. The compressed policy achieves a $1.98\times$ full-policy inference speedup over the unpruned model. These results identify substantial intermediate-dimension redundancy and show that post-pruning RL can recover manipulation performance in compact policies.

---

## 6. Robotic Photography System based on Vision-Language-Action Model

**Authors:** Song-Li Wu, Chubin Zhang, Wenbo Ding, Yansong Tang
**arXiv:** [2610.26287](https://arxiv.org/abs/2610.26287)
**Categories:** Robotics (cs.RO); Artificial Intelligence (cs.AI)

Modern robotic photography requires understanding photographic intent, planning camera motions, and producing aesthetically pleasing images in complex environments. We present RoboPhoto-VLA, a unified Vision-Language-Action framework that jointly models perception, reasoning, and camera control for autonomous robotic photography. RoboPhoto-VLA incorporates PhotoCoT for structured action planning and Aesthetic Direct Preference Optimization (ADPO) to align camera behaviors with human aesthetic preferences. To facilitate training and evaluation, we construct OpenPhotography, a robotic photography dataset with language-guided demonstrations. Extensive real-world experiments demonstrate that RoboPhoto-VLA produces photographs better aligned with human aesthetic preferences while generalizing effectively to unseen subjects, viewpoints, poses, and complex photographic instructions.

---

## 7. PaceVLA: Adaptive Temporal Action Quantization in Vision-Language-Action Models

**Authors:** Hojin Jeon, Jimin Lee, Taekwan Kim, ..., Joonwoo Ahn, Jinwoo Shin
**arXiv:** [2610.25961](https://arxiv.org/abs/2610.25961)
**Categories:** Robotics (cs.RO); Artificial Intelligence (cs.AI)

Fast and reliable manipulation is crucial for practical robot deployment. Although Vision-Language-Action (VLA) models have recently shown remarkable progress as generalist robot policies, their execution often remains temporally inefficient. A key source of this inefficiency is that policies learn fine-grained temporal patterns from teleoperated demonstrations, requiring many low-level action steps. Temporal action quantization offers a simple way to accelerate execution by aggregating consecutive low-level actions into temporally coarser actions. However, applying action quantization without considering when fine-grained control is required introduces a speed-accuracy trade-off: accelerated actions may efficiently reduce redundant steps in some phases, while discarding critical motion details in precision-sensitive interactions. To address this, we propose PaceVLA, a unified framework for adaptive temporal execution in VLAs that integrates two coupled components: (1) mode-specific action decoders built on a shared action expert, supporting multiple temporal granularities and prediction horizons, and (2) a quantizability-guided mode selection scheme which decides whether coarse execution is appropriate, and a context-conditioned router that selects an execution mode at each inference step. Experiments across three multi-task simulation benchmarks and six real-world tasks show that PaceVLA improves execution efficiency while maintaining task success rate across multiple embodiments, including long-horizon and dexterous manipulation.

---

## 8. Compile Once, Run Cheap: Frozen, Portable Skills for Embodied Agents, and What Recursive Self-Improvement Adds

**Authors:** Jingwen Bai, Guochao Bai, Canbo Zhang, ..., Weichun Huang, Shuang Liu
**arXiv:** [2610.25114](https://arxiv.org/abs/2610.25114)
**Categories:** Robotics (cs.RO); Artificial Intelligence (cs.AI); Machine Learning (cs.LG)

Embodied AI lacks the data-rich pretraining that gave language models their agents and skills, so new manipulation capability costs demonstrations per task or a frontier model in every episode. We study a third route: a strong general model acts only as an offline author that writes, runs, diagnoses and repairs a manipulation skill in simulation until it passes an exam on layouts drawn after freezing; the frozen skill then runs as code alone or under a cheap caller that reads only its description. We call this skill-level recursive self-improvement Skill-RSI and specify a compile protocol (isolated, audited author; hidden validation layouts; no-feedback and inherit-only controls; tamper-evident ledger) and a reuse protocol that runs the identical files with executors from another model family. On 7 RoboTwin 2.0 tasks with cluttered tables, Claude Code compiled 4 tasks into 7 frozen skills, 5 from a first draft needing only qualification, at USD 4.29-8.22 of author cost each (USD 55 per skill counting the 13 failed campaigns). The other three tasks did not compile in 18 campaigns, including five with GPT-6 and a pre-registered 150-layout run: on the hardest task every campaign scored 78-95 of 100 but had 3-16 safety aborts, failing the gate of 95% success with zero aborts; a 100-episode exam bounds an abort rate only to 3.6%. On hidden layouts, repair that inherits the previous version beat from-scratch rewriting in 8 of 8 controlled campaigns (sign test p = 0.004); an inherit-only lineage attributes most of the gap to inheritance, with development feedback adding a little (3 of 3, p = 0.125). Write-once campaigns found no detectable first-draft effect of practice (minimum detectable effect 14 points). The frozen skills kept 148/150 successes on new layouts with no model and 147/150 with a DeepSeek-flash caller at USD 0.00028-0.00054 per episode; no direct-control baseline was run.

---

## 9. Scene-Adaptive VLA: Efficient Autonomous Driving via Dynamic Layer Routing

**Authors:** Yujia Yang, Quan Yuan, Jiawei Fan, ..., Guiyang Luo, Jinglin Li
**arXiv:** [2610.24590](https://arxiv.org/abs/2610.24590)
**Categories:** Computer Vision and Pattern Recognition (cs.CV); Artificial Intelligence (cs.AI); Robotics (cs.RO)

Vision-Language-Action (VLA) models offer a promising paradigm for autonomous driving. However, the massive parameter scale of VLAs strains onboard computational resources during real-time inference. This directly increases energy consumption and limits vehicle battery range, making it critical to minimize computational overhead without compromising driving capability and explainability. Current research on efficient VLA-based driving focuses on sequential adaptation (\textit{e.g.}, Chain-of-Thought and token adjustment), leaving structural adaptation underexplored despite parameter redundancy across dynamic driving scenes. To address this gap, we propose Scene-Adaptive VLA, an efficient framework leveraging dynamic layer routing to adjust active parameters based on real-time scenes. Inspired by the temporal continuity of scenes and model predictive uncertainty, our approach characterizes model-perceived scene complexity via frame-level temporal scene variations and decision deviations. To uncover latent scene-to-parameter correspondences, we encode this characterization into scene-aware tokens, alongside two specialized queries. A budget-conditioned layer routing mechanism evaluates these refined queries to allocate a budget that determines the active parameter ratio and subsequently selects appropriate layer combinations. The entire framework is optimized end-to-end. Extensive evaluations on the Bench2Drive benchmark show that when adapted to a state-of-the-art VLA model, our approach significantly reduces inference-time computational overhead by 53.5\% with negligible degradation in driving and language capabilities. Code is available at https:github.com/yang-luvu/Scene-Adaptive-VLA.

---

## 10. CoEvo-RSI: When Harnesses Evolve, Which Models Should Follow?

**Authors:** Jiaqi Su, Guibin Zhang, Jie-Jing Shao, ..., Haiyan Yin, Shuicheng Yan
**arXiv:** [2610.25078](https://arxiv.org/abs/2610.25078)
**Categories:** Machine Learning (cs.LG); Computation and Language (cs.CL)

Model--harness co-evolution has emerged as a prominent paradigm for recursive self-improving (RSI) agents, jointly evolving their execution scaffolds and intrinsic capabilities. We study the persistent yet often overlooked brain--body mismatch problem in this paradigm, where an evolving harness (body) demands behaviors its model (brain) has not learned or restricts capabilities it already possesses. We introduce CoEvo-RSI, a RSI framework that advances model--harness co-evolution through agent-driven, bidirectional historical inheritance. Drawing on a shared evolutionary archive and execution feedback, a meta-agent coordinates harness development from historical designs with model checkpoint selection or merging and subsequent adaptation under the selected harness, aligning inherited capabilities with evolving execution requirements to reduce brain--body mismatch. Using only supervised fine-tuning (SFT) on its own rejection-sampled trajectories, CoEvo-RSI makes Qwen3.5-9B competitive with larger models across diverse vertical applications, including multi-agent failure attribution, role-aware text-to-SQL, and smart-home instruction following. It surpasses DeepSeek-V4-Pro on TraceElephant (+14.16 agent accuracy) and GLM-5.3 on HomeBench VM (+4.90 success rate), underscoring the need for brain--body alignment and the potential of bidirectional historical inheritance to advance agent co-evolution.

---

## 11. Robot Learning with Vision-Language-Action Models for Agricultural Manipulation

**Authors:** Hamid Hafezi, Javad Mohammadpour Velni, Mohammadreza Davoodi
**arXiv:** [2610.26717](https://arxiv.org/abs/2610.26717)
**Categories:** Robotics (cs.RO)

Robotic manipulation in agricultural environments remains challenging due to variations in plant geometry, occlusion, and camera viewpoints. Pretrained vision-language-action (VLA) and generalist robot policies offer a promising approach to addressing these challenges by learning manipulation behaviors from multimodal observations and language instructions. However, adapting these policies to agricultural tasks requires domain-specific demonstrations, which are costly and time-consuming to collect on physical robots. In this work, we develop a simulation-to-real robot-learning framework for agricultural reaching and grasping that integrates task-specific demonstration collection and pretrained policy adaptation. A MuJoCo-based agricultural environment is developed with diverse tomato plant structures to support demonstration collection and controlled evaluation. Expert demonstrations are collected through joystick teleoperation, with a low-level controller used to execute robot actions. Two pretrained generalist robot policies, Octo and $\pi_{0.5}$, are adapted using simulated demonstrations, followed by further fine-tuning on a physical Franka Research 3 manipulator using real-robot demonstrations. The adapted policies are evaluated under in-distribution, viewpoint/spatial-shift, and out-of-distribution conditions in simulation, followed by physical-robot experiments. The influence of proprioceptive information on policy performance is also investigated. Results show that $\pi_{0.5}$ achieves higher task-performance scores than Octo and exhibits less degradation under distribution shifts. These findings demonstrate the potential of integrating pretrained generalist policies with task-specific demonstration learning for agricultural manipulation.

---

## 12. HAF-VLA: Hierarchical Action Flow Framework for Humanoid Vision-Language-Action Control

**Authors:** Langzhe Gu, Chengkai Hou, Meng Li, ..., Shanghang Zhang, Zhengping Che
**arXiv:** [2610.26584](https://arxiv.org/abs/2610.26584)
**Categories:** Robotics (cs.RO)

Humanoid robots hold great promise as general-purpose agents in human-centered environments, yet adapting generalist vision-language-action (VLA) policies to real-world humanoid loco-manipulation remains challenging. Unlike fixed-base or wheeled manipulators, humanoids must coordinate locomotion, posture, gaze, and dual-arm manipulation over a high-dimensional whole-body action space, where inaccurate base or waist motions can easily induce unstable and aggressive upper-body compensation. We propose HAF-VLA, a hierarchical action-flow framework for humanoid VLA control. Built upon a pretrained flow-matching VLA, HAF-VLA inherits the vision-language prefix encoder and action expert weights, and adapts them to humanoid whole-body loco-manipulation with learnable stage embeddings and cross-stage KV-cache conditioning. Instead of generating the full action chunk in a single pass, HAF-VLA progressively denoises a shared whole-body action space: first locomotion and head commands, then waist refinement, and finally full-body manipulation. To preserve structural dependencies across stages, we introduce a cross-stage KV cache conditioning mechanism, enabling subsequent action generation stages to refine and augment their outputs based on the action representations from preceding stages. Experimental results across six real-world tasks demonstrate that our framework significantly enhances the performance of existing models in humanoid loco-manipulation tasks, demonstrating an effective pathway for adapting strong mobile-manipulation VLAs to humanoid whole-body loco-manipulation.

---

## 13. FR-VLA: Implicit Force Reasoning VLA for Contact-Rich Manipulation

**Authors:** Jiaju He, Zhiyuan Yang, Ruyang Han, ..., Zhiping Lin, Haiyue Zhu
**arXiv:** [2610.25981](https://arxiv.org/abs/2610.25981)
**Categories:** Robotics (cs.RO)

Integrating force awareness into Vision-Language-Action (VLA) models involves not merely encoding wrench measurements as an additional modality, but determining when and how strongly physical interaction should influence robot action generation. Existing VLAs that use force typically inject it through a fixed pathway, without explicitly determining when it is relevant to the current action. This calls for an intermediate force relevance mechanism inside the VLA, in which visual-language context estimates the relevance of physical feedback to the current task before force enters the action pathway. FR-VLA addresses this gap with a Vision-Language Force-Reasoning Model that uses learnable force query tokens to derive a force admission signal grounded in visual-language context, and uses this signal to modulate an external tokenized force pathway for action generation. In real-world experiments on five contact-rich tasks across two robotic platforms, FR-VLA achieves the highest mean success rate over six evaluated stages, and trajectory visualizations show that its force admission varies with the interaction phase.

---

## 14. AeroDASH: Asynchronous Vision-Language-Action Control for Continuous UAV Flight

**Authors:** Zhe Liu, Yuxuan Zheng, Jinzhe Qin, Ziqi Gao, Boyu Zhou
**arXiv:** [2610.25407](https://arxiv.org/abs/2610.25407)
**Categories:** Robotics (cs.RO)

Onboard inference latency creates a mismatch between the trajectories predicted by vision-language-action (VLA) policies and the ongoing motion of unmanned aerial vehicles (UAVs). We present AeroDASH, an asynchronous VLA framework for continuous language-conditioned flight. A B-spline policy is initialized through supervised fine-tuning on expert demonstrations, providing continuous trajectory references in position and yaw. During execution, trajectory fusion removes the expired prediction prefix and connects the remaining segment to the active reference with derivative continuity while limiting trajectory deformation. To account for deviations induced by asynchronous execution, execution-aware group relative policy optimization (GRPO) further adapts the policy using trajectory-level rewards. On the UAV-Flow test set, AeroDASH achieves a success rate of 76.56%, exceeding OpenVLA-UAV and AeroDASH w/o GRPO by 38.1 and 20.1 percentage points, respectively. Execution experiments show that AeroDASH sustains motion during inference and reduces acceleration, jerk, and speed fluctuations relative to asynchronous tracking of waypoint sequences. We further demonstrate language-conditioned flight with onboard inference and asynchronous trajectory execution. The code will be released upon acceptance.

---

## 15. EndoVLA-OOV: Language-Conditioned Out-of-View Target Acquisition in Robotic Endoscopy

**Authors:** Chi Kit Ng, Yidong Zhang, Tianchun Wu, ..., Raymond Tang, Hongliang Ren
**arXiv:** [2610.24747](https://arxiv.org/abs/2610.24747)
**Categories:** Robotics (cs.RO)

The scan-then-revisit workflow of upper gastrointestinal endoscopy requires bringing a previously observed suspicious region back into view for closer inspection. Acquiring such targets requires translating anatomical and appearance descriptions into camera motions from partial observations of a confined, deformable environment. We present EndoVLA-OOV, a language-conditioned vision-language-action policy for out-of-view target acquisition in robotic endoscopy. The policy adapts a pretrained backbone to continuous two-degree-of-freedom distal bending commands and combines initial, intermediate, and current images to guide search. To support policy learning, we provide an open-source VLA dataset containing 1,050 episodes across six tasks and approximately 262k observation-action pairs. Physical evaluation spans wet-lens and low-light conditions, two unseen stomach phantoms, and cross-embodiment transfer to an unseen ex-vivo environment. In the cross-embodiment evaluation, the full-data policy achieves 93.3% target acquisition success (28/30). In a controlled training-data comparison, expanding the corpus from 312 to 1,050 episodes increases acquisition success from 40.0% to 90.0% under the same model, training, and test configuration. Instruction and observation interventions further support the use of language and temporal context in the evaluated acquisition tasks. These results support language-guided endoscopic revisitation across the evaluated environments and robot embodiments and demonstrate the benefit of expanded task-specific demonstrations.

---

## 16. Relational Spatial Alignment for Vision-Language-Action Models

**Authors:** Chaoran Zhu, Hengyi Wang, Chenglin Cui, ..., Taein Kwon, Changjae Oh
**arXiv:** [2610.24705](https://arxiv.org/abs/2610.24705)
**Categories:** Robotics (cs.RO)

Spatial understanding is essential for robots to perceive their surrounding environments and execute actions. Existing approaches typically encode 3D awareness into vision-language-action (VLA) models by directly aligning their representations with pre-trained 3D foundation models. However, we observe that such direct geometric feature alignment essentially exploits 3D foundation priors as a form of low-rank regularization in the feature space, resulting in severe rank collapse of the pre-trained VLA representations. In contrast, we shift the focus from enforcing point-wise equality to aligning pair-wise relationships. We propose a representation-alignment method that enables the injection of 3D spatial awareness without compromising the model's original expressivity. Extensive experiments on public benchmarks, our new spatial reasoning benchmark, and real-world manipulation scenarios demonstrate that our approach effectively incorporates 3D spatial representations into VLA reasoning, achieving robust performance and enhanced spatial awareness across diverse manipulation tasks.

---

## 17. Retrieval-triggered Action Projection Adjustment for Frozen VLA Policies: An Empirical Study and Failure Analysis

**Authors:** Jinming Wang, Ruiheng Zhang, Yong Wang, Zipan Xiong, Keyuan Luo
**arXiv:** [2610.24573](https://arxiv.org/abs/2610.24573)
**Categories:** Robotics (cs.RO)

Frozen Vision-Language-Action (VLA) policies cannot incorporate previously encountered failures without updating the underlying model. We present retrieval-triggered projection correction (RTPC), an auditable external-memory wrapper for frozen OpenVLA policies that retrieves stress-collected local-depth records and applies translation-only projection correction while keeping rotation and gripper commands unchanged. RTPC is evaluated on CALVIN single-task manipulation using primary and independent replication cohorts. In the primary evaluation, RTPC reduced a depth-based near-collision or stall proxy event rate without changing task-success count. However, this reduction was not reproduced in the independent replication, and retrieved correction directions were not distinguishable from random same-family directions. Analysis identifies endpoint coupling, batch sensitivity, and the lack of a trigger-matched memory-free baseline as limitations for attributing effects to retrieval-based correction. These findings do not establish physical safety improvement or memory-specific benefits, but provide an empirical evaluation and failure analysis of retrieval-conditioned intervention for frozen VLA policies.

---

## 18. AutoPruner: Agentic Depth Pruning for Vision-Language-Action Models

**Authors:** Tao Lin, Yikeng Chen, Qiwei Liang, ..., Zhengtu Liang, Renjing Xu
**arXiv:** [2610.23880](https://arxiv.org/abs/2610.23880)
**Categories:** Robotics (cs.RO)

Layer pruning reduces the size and inference cost of vision-language-action (VLA) models, but selecting a deployable configuration requires deciding both which layers to remove and how to recover task performance. These decisions depend on the model and task, and a failed trial can reflect either the deletion set or insufficient recovery. We present AutoPruner, an agent-driven framework that jointly searches pruning structures and recovery recipes through closed-loop experimentation. Offline layer interventions measure changes in action output to provide functional evidence. An LLM agent combines this evidence with evaluation history and retained diagnoses to propose deletion sets and recovery recipes within a search budget. Each proposal is executed and evaluated on the target tasks, and the resulting feedback guides the next experiment. Across OpenVLA-OFT, StarVLA, and FastWAM on four LIBERO suites, AutoPruner removes 16.7--87.5% of backbone layers while maintaining task success above 90%, with measured inference speedups of up to 2.50$\times$. Further analysis shows that functional probes identify action-sensitive layers despite high representation similarity, and that recovery can make previously failing structures viable.

---

## 19. CondenseVLA: Learnable History Condensation for Efficient Multi-Frame VLA

**Authors:** Feiyang Hong, Yujie Wei, Bo Zhao, ..., Hongxun Yao, Shuo Yang
**arXiv:** [2610.25927](https://arxiv.org/abs/2610.25927)
**Categories:** Computer Vision and Pattern Recognition (cs.CV); Robotics (cs.RO)

Robot manipulation often depends on short-term cues - such as brief contacts, temporary occlusions, and intermediate object states - that are ambiguous in a single frame and can only be resolved by integrating observations over time. However, injecting historical information solely by enlarging the history window is computationally costly and frequently yields limited gains due to substantial redundancy and task-agnostic, inflexible sampling of observations. We propose CondenseVLA, a multi-frame VLA policy with a learnable decoder-side history condensation module for using short-term visual context in action decoding. Given a sequence of cached per-frame features from the VLM backbone, CondenseVLA distills observation history into a fixed set of slot tokens using learnable queries and multi-head cross-attention. Simple auxiliary regularization penalizes overlap among slot attention maps and decorrelates slot embeddings, encouraging complementary attention and reducing slot redundancy. Across the evaluated tasks, CondenseVLA improves Simpler-WidowX success from 58.7% to 69.8% (+11.1 percentage points), achieves 97.2% on LIBERO, and reaches 52.8% on real-world tasks. It achieves 21.6% success on memory-dependent RMBench tasks. These results support selective condensation of bounded recent visual evidence for action decoding, while harder multi-observation tasks expose the limits of a finite history window. Project page: this https URL

---

## 20. Think Densely, Act Sparsely: Latent Expert Cognitive Chains for Vision-Language-Action Autonomous Driving

**Authors:** Jie Wang, Guang Li, Zhijian Huang, ..., Yahong Han, Long Chen
**arXiv:** [2610.25734](https://arxiv.org/abs/2610.25734)
**Categories:** Computer Vision and Pattern Recognition (cs.CV); Robotics (cs.RO)

Autonomous driving fundamentally demands dense understanding of visual, semantic, and geometric information, yet existing Vision-Language-Action (VLA) models are typically trained with sparse supervision such as language instructions or trajectory signals. This direct mapping from dense visual observations to sparse representations forces the model to compress or even discard critical scene information essential for safe driving. We argue that this limitation does not stem from insufficient model capacity, but from the lack of explicit mechanisms that encourage the formation of dense world representations in the latent space. In this spirit, we propose a novel paradigm for driving intelligence, Think Densely, Act Sparsely, and instantiate it with an efficient and interpretable framework, LECDrive (Latent Expert Cognitive Chains for Vision-Language-Action autonomous Driving). The core idea is to mimic the hierarchical perception process of humans by embedding a progressive chain of latent expert cognition within the VLA model. Concretely, we inject a compact set of task-specific latent tokens as carriers, enabling the model to internalize dense knowledge from foundational vision models, including visual representations (DINOv3), semantic structures (SAM3), and spatial geometry (DepthAnything3), while maintaining efficient inference. This interdependent cognitive chain follows a curriculum learning principle, where supervision is progressively structured from representation to semantics and geometry. Extensive experiments demonstrate that LECDrive consistently improves the performance of base VLMs across multiple autonomous driving benchmarks, covering key tasks such as object perception, state prediction, and trajectory planning. These findings suggest that constructing dense world models through structured latent expert chains is a promising direction for VLA-based autonomous driving.

---
