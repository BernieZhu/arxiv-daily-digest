# arXiv Daily Digest — 2026-07-01

**Mode:** direct
**Categories:** cs.AI, cs.LG, cs.RO, cs.CV
**Keywords:** VLA, world model, world action model
**Papers found:** 22

---

## 1. Ask the World Before Acting: Budgeted Environment Probing for World-Model Calibration

**Authors:** Xinyuan Song, Zekun Cai
**arXiv:** [2606.31422](https://arxiv.org/abs/2606.31422)
**Categories:** Artificial Intelligence (cs.AI)

Long-horizon language agents do not only choose actions; they carry a private model of the world from one decision to the next. When that model drifts, a later failure can be decided before the failing action is ever taken. We study a direct repair mechanism: before committing to the next task action, an agent may ask the environment about one belief field and write the answer back into its world model. This makes environment interaction a scarce calibration resource, not merely a way to advance the task. We introduce \method, a budgeted probing operator for structured belief tables. The useful probes are not the same everywhere. Procedural beliefs, such as tool dependencies, can often be repaired by targeted checks, but those checks spend steps that the task may need. Spatial beliefs, such as object locations and graph edges, rely more on structural cues; the agent's own confidence can be a poor guide when the world changes off-screen. A type-stratified analysis formalizes this probe-action frontier, and controlled experiments show that mid-planning environment evidence reduces terminal world-model error when the probe policy follows the structure of the task.

---

## 2. World-Model Collapse as a Phase Transition

**Authors:** Xinyuan Song, Zekun Cai
**arXiv:** [2606.31399](https://arxiv.org/abs/2606.31399)
**Categories:** Artificial Intelligence (cs.AI)

Water looks unchanged as it warms, then at a critical point it boils. We ask whether long-horizon language agents show an analogous transition in their implicit world models. In some parameter settings, changing state load by a small amount, or adding a single step of horizon, leaves behavior nearly unchanged; near a critical boundary, the same small change causes a sudden world collapse. We study this effect in a deterministic task family with exact per-step gold state. A large grid search over state cardinality, dependency density, horizon, branching, observation mode, and mutation rate reveals a phase diagram: a solved plateau, a narrow transition band, and a collapse floor. Per-step traces show the mechanism: world-state fidelity fails before action validity, so the agent is not merely choosing a bad action; it is acting from a corrupted world. Stronger models translate the critical boundary but do not remove the qualitative transition. These results make world-model collapse a measurable bottleneck for long-horizon agents.

---

## 3. Delta-JEPA: Learning Action-Sensitive World Models via Latent Difference Decoding

**Authors:** Zhenghao Zhang, Yuanxiang Wang, Zhenyu Guan, ..., Jingjing Zhou, Jungang Xu
**arXiv:** [2606.31232](https://arxiv.org/abs/2606.31232)
**Categories:** Artificial Intelligence (cs.AI)

Learning visual world models for planning requires compact latent dynamics that remain sensitive to actions, yet reconstruction-free joint-embedding objectives can collapse to action-insensitive representations. We propose Delta-JEPA, an end-to-end reconstruction-free world model that augments latent forward prediction with a Latent Difference Action Decoder (LDAD). Unlike inverse decoders that infer actions from concatenated endpoint embeddings, LDAD reconstructs the executed action from the latent displacement between consecutive observations. This displacement-level supervision directly regularizes transition geometry: adjacent embeddings cannot collapse without losing action information, and different actions are encouraged to induce distinguishable latent changes for rollout-based planning. Delta-JEPA uses only latent prediction and action reconstruction, avoiding pixel reconstruction and distribution-matching regularizers. Across four visual continuous-control tasks, Delta-JEPA improves planning over JEPA-based and representation-learning world model baselines. Ablations show that displacement-based action decoding is consistently more effective than endpoint concatenation, and action-sensitivity analyses show clearer action-conditioned latent responses. These results indicate that supervising latent differences is a simple and effective mechanism for collapse-resistant and action-sensitive world model learning.

---

## 4. AdaJEPA: An Adaptive Latent World Model

**Authors:** Ying Wang, Oumayma Bounou, Yann LeCun, Mengye Ren
**arXiv:** [2606.32026](https://arxiv.org/abs/2606.32026)
**Categories:** Machine Learning (cs.LG); Artificial Intelligence (cs.AI)

Latent world models enable planning from high-dimensional observations by predicting future states in a compact latent space. However, these models are typically kept frozen at test time: when their predictions become inaccurate, planning can fail, especially under test-time distribution shift. To address this, we propose AdaJEPA, an adaptive latent world model that performs test-time adaptation within the closed loop of model predictive control (MPC). After training, AdaJEPA plans and executes the first action chunk, uses the observed next-state transition as a self-supervised adaptation signal, and replans with the updated model. This closed-loop update continuously recalibrates the world model without additional expert demonstrations. Across a range of goal-reaching tasks, AdaJEPA substantially improves planning success with as few as one gradient step per MPC replanning step.

---

## 5. Z-1: Efficient Reinforcement Learning for Vision-Language-Action Models

**Authors:** Lang Cao, Renhong Chen, Luyi Li, ..., Mofan Peng, Yitong Li
**arXiv:** [2606.31846](https://arxiv.org/abs/2606.31846)
**Categories:** Robotics (cs.RO); Artificial Intelligence (cs.AI)

Vision-Language-Action (VLA) models offer a promising framework for robotic manipulation by connecting language instructions, visual observations, and continuous control. However, most existing policies remain limited by behavior cloning or supervised fine-tuning (SFT) from fixed demonstrations, which provides limited opportunity to improve from the policy's own failures. In this paper, we present Z-1, a reinforcement learning (RL) post-training framework for flow-based VLA models. Built on top of $\pi_{0.5}$, Z-1 uses only publicly released RoboCasa demonstrations for SFT and then applies a task-wise Group Relative Policy Optimization (GRPO) strategy across $24$ standard RoboCasa tasks. To improve the efficiency and stability of online optimization, Z-1 combines shared-prefix rollout construction, tree-structured trajectory branching, completion-aware reward calibration, and selective joint training of VLM and Action Expert. Across all $24$ RoboCasa tasks, Z-1 achieves an average success rate of $80.6\%$, improving over its SFT initialization by $13.2\%$ points and outperforms the published sota models. These results show that systematic GRPO post-training can substantially improve flow-based VLA policies without additional private demonstrations.

---

## 6. WorldRoamBench: An Open-World Benchmark for Long-Horizon Stability of Interactive World Models

**Authors:** Ting-Bing Xu, Jiacheng Sui, Zhe Gao, ..., Yong Li, Baoquan Chen
**arXiv:** [2606.31672](https://arxiv.org/abs/2606.31672)
**Categories:** Computer Vision and Pattern Recognition (cs.CV); Artificial Intelligence (cs.AI)

Despite rapid progress in interactive world models (IWMs), existing benchmarks evaluate action following only at trajectory level and ignore memory and interaction physics. We introduce WorldRoamBench, an open-world benchmark for long-horizon stability across four dimensions, each with tailored innovations: (i) Action: per-frame action metric bypassing cross-model semantic scale disparity and exposing failures hidden by trajectory; (ii) Vision: segment-based drift metric capturing non-monotonic mid-sequence collapse missed by start-vs-end comparisons; (iii) Physics: controllability-gated evaluation over mechanics, optics, and 3D consistency, scoring plausibility under faithful action execution; (iv) Memory: action-decoupled protocol evaluating scene memory via transition-localized 3D point-cloud reconstruction and subject memory via tracking-plus-VLM reasoning. The benchmark comprises 600+ test cases across Nature, Urban, and Indoor scenes in first/third-person views with WASD 10-60s continuous interaction. Evaluating 10+ open/closed-source models reveals none reliably satisfies all dimensions; even the best achieves only moderate scores. Advances on WorldRoamBench are steps toward IWMs that are stable, physically grounded, memory-faithful, and deployable in real-world applications.

---

## 7. 3D HAMSTER: Bridging Planning and Control in Hierarchical Vision Language Action Models through 3D Trajectory Guidance

**Authors:** Dongyoon Hwang, Byungkun Lee, Dongjin Kim, ..., Hyunseung Kim, Jaegul Choo
**arXiv:** [2606.31329](https://arxiv.org/abs/2606.31329)
**Categories:** Robotics (cs.RO); Artificial Intelligence (cs.AI)

Hierarchical Vision-Language-Action (VLA) models decouple high-level planning from low-level control to improve generalization in robot manipulation. Recent work in this paradigm uses 2D end-effector trajectories predicted by a Vision-Language Model (VLM) as explicit guidance for a downstream policy. However, state-of-the-art low-level policies operate in 3D metric space on point clouds, and feeding them 2D guidance that lacks depth forces each waypoint to be assigned the depth of whatever scene surface lies beneath it, producing geometrically distorted trajectories. We propose 3D HAMSTER, a hierarchical framework that closes this gap by having the planner directly output metrically reliable 3D trajectories. We augment a VLM with a dedicated depth encoder and a dense depth reconstruction objective to predict 3D waypoint sequences, which are directly integrated into a pointcloudbased low-level policy. Across 3D trajectory prediction, simulation, and real-world manipulation, 3D HAMSTER consistently outperforms proprietary VLMs and 2D-guided baselines, with the largest gains under appearance-altering shifts and unseen language, spatial, and visual conditions. The project page is available at this https URL.

---

## 8. MIRTH: Mutual-Information Reasoning with Temporal Hubs for Vision-Language-Action Agents

**Authors:** Hao Sun, Yu Song, Shiyu Teng, Ziwei Niu, Yen-Wei Chen
**arXiv:** [2606.31167](https://arxiv.org/abs/2606.31167)
**Categories:** Robotics (cs.RO); Artificial Intelligence (cs.AI)

VLA models have emerged as a powerful paradigm for transferring semantic knowledge from web-scale data to physical robotic control. However, current single-frame architectures suffer from intrinsic limitations: temporal myopia that discards historical dynamics, reasoning gaps between high-level instructions and low-level motor commands, and inference inefficiency due to autoregressive scalar decoding. In this work, we propose MIRTH, a unified framework designed to address these challenges. MIRTH augments a pretrained VLA backbone with three key innovations: (1) dual-scale temporal memory hubs that compress long-term scene evolution and short-term motion trends into compact embeddings; (2) latent reasoning tokens optimized via a mutual-information objective carving out a semantic plan space to align multimodal context with action trajectories; and (3) a parallel action decoding scheme that replaces autoregressive generation with vector-wise prediction to maximize control throughput. Extensive evaluations on the LIBERO simulation benchmark and a real-world LeRobot platform demonstrate that MIRTH achieves state-of-the-art performance and exhibiting emergent error recovery capabilities. The codes and collected datasets are released at this http URL.

---

## 9. A Modular Vision-Language-Action Robotics Framework for Indoor Environments

**Authors:** Anindya Jana, Snehasis Banerjee, Arup Sadhu, Ranjan Dasgupta
**arXiv:** [2606.31144](https://arxiv.org/abs/2606.31144)
**Categories:** Robotics (cs.RO); Artificial Intelligence (cs.AI)

This paper presents an integrated system for the CMU Vision-Language-Action (VLA) Challenge, designed to enable an autonomous agent to perform complex tasks based on natural language instructions. Our framework employs a modular architecture that orchestrates environment mapping, question processing, and navigation. The system operates in two parallel streams: a perception pipeline that constructs a semantic voxel map from real-time camera feeds using OwlViT embeddings, and a language pipeline that classifies user commands with a Vision-Language Model. The mapping is time-constrained; the system proceeds with a partial map if a 500-second exploration limit is reached. The classified query is then grounded in the geometric and semantic context of the map to generate a detailed prompt for the VLM. This yields an actionable output, demonstrating a capable solution for bridging the gap between human language and robotic action.

---

## 10. Position: Vision-Language-Action Models Cannot Be Verified to Perform Physical Reasoning

**Authors:** Taozhao Chen, Ian Manchester, Huaming Chen
**arXiv:** [2606.30686](https://arxiv.org/abs/2606.30686)
**Categories:** Robotics (cs.RO); Artificial Intelligence (cs.AI)

Vision-Language-Action (VLA) systems, built on pretrained vision-language models (VLMs), have shown rapidly improving performance on robot manipulation benchmarks. These gains are commonly interpreted as evidence that semantic representations learned from internet-scale data transfer to physical execution generalization. This position paper argues that the assumption underlying this interpretation -- that semantic generalization is sufficient to support physical action decisions -- has not been independently verified and cannot be tested under current evaluation protocols. We support this claim by decomposing VLA policies into semantic mapping and physical action decision, and showing that task success rate -- the dominant evaluation metric -- cannot distinguish between these two sources of capability. As a result, improvements in benchmark performance are consistent with multiple competing explanations, including semantic matching, distributional overlap, and genuine physical generalization. We further argue that this identifiability gap has been reinforced through narrative drift, whereby successive systems inherit and strengthen prior interpretations of performance gains without isolating the underlying causal mechanism. To address this limitation, we propose a research direction based on evaluation designs that introduce controlled variation to separately measure semantic and physical generalization. Such designs make it possible to causally attribute performance without requiring access to model internals, and to empirically assess the role of VLM backbones as semantic interfaces rather than implicit sources of physical competence. Our goal is not to refute the role of VLMs in robotics, but to clarify the conditions under which claims of physical generalization can be meaningfully evaluated.

---

## 11. DVG-WM: Disentangled Video Generation Enables Efficient Embodied World Model for Robotic Manipulation

**Authors:** Ziyu Shan, Zhenyu Wu, Xiaofeng Wang, Zheng Zhu, Ziwei Wang
**arXiv:** [2606.32028](https://arxiv.org/abs/2606.32028)
**Categories:** Robotics (cs.RO)

Video-based embodied world models provide an appealing substrate for robotic manipulation by predicting future states, yet current approaches remain limited by a fundamental entanglement: accurately modeling dynamics typically requires low-level temporal reasoning, while producing high-resolution frames demands expansive visual synthesis according to high-level semantics. This entanglement results in slow inference speed for iterative planning or too coarse predictions to retain contact-rich details. To solve this dilemma, we present Disentangled Video Generation World Model (DVG-WM), an efficient framework that explicitly decomposes world modeling into dynamics learning and visual synthesis. Conditioned on an initial observation and a language instruction, our model first generates a plausible sequence of intermediate visual states to preview the physical interaction and refines them to obtain high-fidelity videos. Furthermore, an efficient cascading mechanism is proposed, where DVG-WM uses flow matching to directly map the dynamics to video latents, and introduces a latent degradation mechanism to regenerate contact-rich details. Experiments on LIBERO and real-world platforms demonstrate improved video quality with up to 3.97 times acceleration, validating that disentangled video generation can be an efficient embodied world model for robotic manipulation.

---

## 12. UniTacVLA: Unified Tactile Understanding and Prediction in Vision Language Action Models

**Authors:** Xidong Zhang, Yichi Zhang, Jiaxin Shi, ..., Xiaojun Wu, Weihao Yuan
**arXiv:** [2606.31723](https://arxiv.org/abs/2606.31723)
**Categories:** Robotics (cs.RO)

Vision-language-action (VLA) models have achieved strong performance in many robotic manipulation tasks, yet remain limited in contact-rich dexterous manipulation. To overcome this limitation, recent vision-tactile-language-action (VTLA) methods incorporate tactile sensing into VLA models to provide direct contact information. However, they typically treat tactile signals as passive auxiliary inputs, making it difficult to model tactile semantics and future physical interactions. To this end, we propose a unified tactile learning framework for contact-rich manipulation that models tactile signals as dynamic interaction cues for both contact understanding and prediction. Specifically, we construct a unified tactile latent space and jointly model current tactile states and future contact changes through tactile chain-of-thought reasoning and coarse-to-fine future tactile prediction, thereby forming a state-aware and dynamics-aware tactile prior. Based on this prior, we introduce a tactile-action mixed controller that combines real-time and predicted tactile feedback to refine low-frequency action chunks with high-frequency corrections. Real-world experiments on four categories of contact-rich tasks, including adjustment, insertion, wiping, and assembly, under both clean and externally perturbed settings, show that our method improves success rate, manipulation accuracy, and contact robustness over existing methods, demonstrating its effectiveness in dexterous physical interaction.

---

## 13. Revisiting Parameter Redundancy in Vision-Language-Action Models: Insights from VLM-to-VLA Adaptation

**Authors:** Fengnian Zhang, Tao Huang, Siyu Xu, Zhong Jin, Chang Xu
**arXiv:** [2606.31382](https://arxiv.org/abs/2606.31382)
**Categories:** Robotics (cs.RO)

Vision-Language-Action (VLA) models have made significant strides in embodied intelligence by integrating the powerful representations of pre-trained Vision-Language Models (VLMs). However, the massive parameter scale of VLAs imposes a heavy computational burden, and these models exhibit extreme sensitivity to parameter pruning. Current paradigms often treat the resulting performance degradation as inevitable, relying on fine-tuning or low-rank corrections to recover efficacy. We challenge this convention by questioning whether the removed parameters are truly redundant if VLA pruning necessitates performance recovery to be effective, or if this paradigm masks the indiscriminate pruning of critical parameters. We revisit parameter redundancy through the lens of VLM-to-VLA adaptation, first quantifying the spatial distribution of parameter divergence during adaptation to reveal structured patterns across different modules. Subsequently, we introduce controlled pruning as a diagnostic probe: by comparing the direct impact of removing different parameter subsets on VLA performance without any fine-tuning, we establish a causal link between adaptation-induced divergence signals and functional contributions. Based on the discovered modular heterogeneities, we design a multi-module joint pruning scheme. Evaluations on the LIBERO benchmark demonstrate that our approach reduces the parameters of OpenVLA and $\pi_{0.5}$ by 12\%--30\% while maintaining approximately 90\% of the original performance without any post-pruning recovery. In contrast, existing parameter pruning criteria result in total performance collapse when evaluated under the same recovery-free constraints. Our study reveals the parameter evolution mechanism in VLA adaptation and provides a new path for deploying efficient, robust robotic policies in resource-constrained environments.

---

## 14. Efficient Sim-to-Real Transfer of World-Action Models from Synthetic Priors

**Authors:** Zixing Wang, Kausik Sivakumar, Jinghuan Shang, ..., Xiaohan Zhang, Karl Schmeckpeper
**arXiv:** [2606.31101](https://arxiv.org/abs/2606.31101)
**Categories:** Robotics (cs.RO)

Bridging the sim-to-real gap is a core challenge in deploying learned manipulation policies. Sim-to-real learning is attractive because it can replace expensive real robot demonstrations with scalable synthetic data, yet world-action models have not previously been shown to transfer from simulation to real robotic manipulation. We study whether a world-action model can be trained from synthetic priors and deployed zero-shot in the real world. To this end, we build upon Cosmos Policy, a video diffusion model adapted for visuomotor control. We construct simulation environments with extensive domain randomization and generate demonstrations using the AnyTask motion planning pipeline. We evaluate our approach across object lifting, drawer opening, and pick-and-place tasks using ${\sim}800$ synthetic demonstrations per task and no real demonstrations. When deployed zero-shot on a Franka Robot, our policy attains a 35\% average success rate. To our knowledge, this represents the first successful sim-to-real transfer of a world-action model for robotic manipulation.

---

## 15. MemLearner: Learning to Query Context memory for Video World Models

**Authors:** Jiwen Yu, Jianxiong Gao, Jianhong Bai, ..., Kun Gai, Xihui Liu
**arXiv:** [2606.31734](https://arxiv.org/abs/2606.31734)
**Categories:** Computer Vision and Pattern Recognition (cs.CV)

Video World Models are interactive video generation models that predict future world states based on user actions and history video frames. A critical challenge in video world models is the lack of memory, causing inconsistent generated scenes over extended durations. Previous methods explored rule-based context frame retrieval as memory, but they fail to generalize in scenarios with scene occlusions and dynamic objects. We propose MemLearner, a learning-based adaptive context query method using query tokens to bridge context and predicted tokens. By leveraging the video generation model itself for context querying, MemLearner exploits pre-trained visual priors without training additional modules from scratch, and incorporates efficient strategies for training and inference. We collect a dataset of long videos with scene occlusions and dynamic objects, paired with camera pose annotations, and propose a multi-dataset training strategy leveraging both annotated rendered and unannotated real-world videos. Extensive experiments demonstrate that MemLearner significantly outperforms prior video world models in terms of scene consistency and memory, particularly under challenging occlusion and dynamic scenarios.

---

## 16. Reasoning-aware Speculative Decoding for Efficient Vision-Language-Action Models in Autonomous Driving

**Authors:** Anh Dung Dinh, Simon Khan, Flora Salim
**arXiv:** [2606.31160](https://arxiv.org/abs/2606.31160)
**Categories:** Computer Vision and Pattern Recognition (cs.CV)

Modern Vision-Language-Action (VLA) planners for autonomous driving emit a chain-of-causation (CoC) reasoning step \emph{before} producing a trajectory. The reasoning is autoregressive and dominates inference latency, while the trajectory head is parallel and cheap. Latency is an operational constraint in autonomous driving, so accelerating the reasoning step is the central problem we address. We observe that CoC reasoning has two qualitatively different needs: most tokens continue routine setup that follows naturally from the ego-trajectory history, and a small fraction encode commitments that require fresh visual evidence about an unexpected situation. We split this reasoning into two specialized paths: a \emph{routine reasoner} that handles the predictable continuation by attending to trajectory history, and a \emph{deliberative reasoner} (the unmodified VLA target) that handles novel cases by attending to current visual evidence, using the speculative decoding framework as the architectural template for how the two paths cooperate. Unlike standard speculative decoding, our routine reasoner is not a smaller replica of the target; the two reasoners are deliberately specialized to read different parts of the prompt. We propose two techniques to realize this. First, we introduce \textbf{FlatRoPE}, a 1D rotary positional embedding in the draft that breaks the rotational symmetry of the target's 3D M-RoPE, redirecting attention away from visual tokens and onto trajectory-history tokens. Second, we introduce \textbf{Action-aware RL (AARL)}, a post-training stage that uses an action-quality reward together with a static-reference KL anchor. Together, our two-reasoner system reduces the reasoning-step running time by approximately $4\times$ relative to the original Alpamayo planner.

---

## 17. Human-as-Humanoid: Enabling Zero-Shot Humanoid Learning from Ego-Exo Human Videos with Human-Aligned Embodiments

**Authors:** Xiaopeng Lin, Ruoqi Yang, Shijie Lian, ..., Bojun Cheng, Kai Chen
**arXiv:** [2606.32009](https://arxiv.org/abs/2606.32009)
**Categories:** Robotics (cs.RO)

Vision-language-action (VLA) models across robot embodiments require high-quality observation--action supervision to learn deployable action distributions, yet scaling such robot data remains difficult, especially for high-DoF humanoids. Teleoperation provides controller-aligned supervision, while human egocentric videos capture diverse bimanual manipulation but do not directly provide executable robot actions. We introduce Human-as-Humanoid, a human-to-humanoid supervision framework that enables near-real-time human-centric action generation, making human demonstrations usable for high-DoF humanoid VLA training by jointly aligning the robot embodiment, the sensing setup, and the action-label interface. Built on PrimeU, a human-aligned 60-DoF upper-body humanoid, Human-as-Humanoid uses synchronized ego-exo videos to pair deployment-aligned egocentric observations with exocentric motion recovery, retargets the recovered human motion through staged Inverse Kinematics (IK) into controller-aligned 60-DoF action chunks, and trains the VLA model with Forward Kinematics (FK)-aware supervision to preserve wrist and fingertip task-space geometry. This converts large-scale human demonstrations from visual observations into executable observation--action supervision for the target humanoid. Experiments validate the conversion chain at the motion-recovery, robot-action-space, and real-robot deployment levels. Human-as-Humanoid yields a 4.8--7.2x raw demonstration-throughput gain over humanoid teleoperation in our data-collection analysis, and on several downstream tasks, policies post-trained only with the converted human labels generalize to real-robot deployment without target-task robot demonstrations. The official project website is available at this https URL.

---

## 18. OopsieVerse: A Safety Benchmark with Damage-Aware Simulation for Robot Manipulation

**Authors:** Arnav Balaji, Arpit Bahety, Sriniket Ambatipudi, ..., Junhong Xu, Roberto Martín-Martín
**arXiv:** [2606.31993](https://arxiv.org/abs/2606.31993)
**Categories:** Robotics (cs.RO)

While robotic manipulation capabilities have advanced rapidly, physical safety remains a major barrier to deploying household robots: task success is insufficient if the robot damages itself or its surroundings. Simulation offers a harm-free alternative to costly and dangerous real-world training and evaluation, yet existing simulators lack general mechanisms to detect, quantify, and represent damage. To address this gap, we introduce OOPSIEVERSE, a unified simulation framework and benchmark for damage-aware household manipulation. OOPSIEVERSE provides damage as an explicit, physically-grounded, and taskagnostic signal by converting sources such as contact forces, temperature changes, and liquid interactions into corresponding mechanical, thermal or fluid damage. OOPSIEVERSE comprises two core elements: (1) DAMAGESIM, a simulator-agnostic framework for detecting and quantifying damage during navigation and manipulation, and (2) a suite of household tasks designed to evaluate common damage modes and distinguish between task completion and safe execution. We demonstrate the generality of our framework by instantiating DAMAGESIM in two simulators with different physics backends, OmniGibson (Nvidia Omniverse) and RoboCasa (MuJoCo). We further showcase the utility of OOPSIEVERSE across multiple use cases, including (1) guiding safer demonstration collection via real-time damage feedback, (2) learning safer manipulation policies through damage-conditioned imitation learning and reinforcement learning, (3) benchmarking the safety of state-of-the-art Vision Language Action policies, and (4) improving real-world safety of sim-to-real transferred policies. Together, our results highlight the potential of OOPSIEVERSE as an open-source foundation for systematic, scalable research on safe robot manipulation. For code and more information, please refer to this https URL

---

## 19. Adapting Generalist Robot Policies with Semantic Reinforcement Learning

**Authors:** Jagdeep Singh Bhatia, Andrew Wagenmaker, William Chen, Sergey Levine
**arXiv:** [2606.31958](https://arxiv.org/abs/2606.31958)
**Categories:** Robotics (cs.RO)

Generalist robot policies learn a diverse repertoire of behaviors from large-scale pretraining. In principle, this makes them excellent priors for downstream adaptation via reinforcement learning (RL). In practice, however, standard RL methods leveraging this prior optimize directly over robot actions, requiring the base policy's action distribution to be close to that of a performant policy from the start. This assumption breaks down for complex or long-horizon tasks that fall outside the pretraining distribution. Our key insight is that, for sufficiently expressive generalist policies, language prompts are an effective alternative space for learning to solve such tasks: modulating language inputs elicits skills already within the policy's repertoire, which can be composed to solve tasks beyond its zero-shot capabilities. We propose Semantic Action Reinforcement Learning (SARL), which learns to optimize this prompt space through online interaction, treating the generalist policy as a controllable skill prior. Importantly, leveraging pretrained skills rather than learning new ones from scratch yields structured, semantically meaningful exploration and highly efficient online improvement, and learning to modulate prompts through experience grounds them in induced real-world behaviors for robust task-solving. Across real-world settings and simulated benchmarks, we show SARL unlocks fundamentally new capabilities -- adapting VLA behavior to solve complex, long-horizon tasks -- and significantly outperforms existing approaches for improving robot behavior in deployment.

---

## 20. ELASTIC: Efficiently Learning to Adaptively Scale Test-Time Compute for Generative Control Policies

**Authors:** Andrew Zou Li, Gokul Swamy, Yonatan Bisk, Andrea Bajcsy
**arXiv:** [2606.31132](https://arxiv.org/abs/2606.31132)
**Categories:** Robotics (cs.RO)

Generative control policies (GCPs), such as diffusion policies and flow-based vision-language-action models, enable test-time scaling in robot control. Test-time compute can be allocated along two axes: sequential scaling, which increases denoising steps to refine actions, and parallel scaling, which samples multiple candidate actions to search across modes of the policy distribution. However, the optimal allocation of sequential and parallel compute is hard to know a priori as it is state-, task-, and policy-dependent. For example, early stages of a grasp may benefit from broader parallel exploration, while near-contact phases may require more sequential refinement for precision. We present ELASTIC, an algorithm that learns state-dependent test-time compute schedules for GCPs. We formulate compute allocation as a meta-Markov Decision Process in which a meta-policy interacts with a frozen pretrained robot policy and selects sequential steps and parallel samples at each denoising iteration to maximize task success while minimizing compute. Using reinforcement learning, this meta-policy also learns adaptive compute schedules without access to the GCP's training data. Across simulated manipulation benchmarks with diffusion policies, ELASTIC Pareto-dominates fixed and single-axis scaling baselines at matched compute budgets. On real-world robot manipulation with the $\pi_{0.5}$ vision-language-action model, ELASTIC matches best-of-$10$ success while reducing wall-clock latency by 34%.

---

## 21. One Video, One World: Turning Monocular Video into Physical 4D Scenes

**Authors:** Junhao Chen, Boran Zhang, Mingjin Chen, ..., Zhihao Li, Yufei Wang
**arXiv:** [2606.31388](https://arxiv.org/abs/2606.31388)
**Categories:** Computer Vision and Pattern Recognition (cs.CV)

We introduce \textbf{OVOW}, the first training-free system that reconstructs \emph{instance-level, simulation-ready} 4D mesh scenes from a single monocular video. Recent 4D reconstruction achieves impressive rendering quality, but its outputs (\eg, implicit fields, Gaussian primitives, or point clouds) lack the watertight topology, instance separation, and standardized physical interfaces required by physics simulators and embodied AI. OVOW closes this gap with a four-stage pipeline: a vision-language model discovers, labels, and motion-classifies all instances; category-aware reconstruction yields per-instance meshes for rigid objects and topology-consistent mesh sequences for deformable ones; an iterative render-match-optimize procedure recovers metric scale and 6-DoF pose trajectories; and physics-grounded assembly enforces ground contact and inter-object support. Crucially, we model all motion, rigid and non-rigid, through direct vertex deformation without category-specific priors or skeleton rigging, producing watertight mesh scenes ready for downstream physics simulation and editing. We further establish the first benchmark for \emph{structured Video-to-4D} evaluation, with metrics for geometric correctness, instance separation, and physical plausibility beyond visual fidelity; the same pipeline doubles as a scalable engine for \emph{synthesizing} paired video-to-4D simulation data for future 4D world models and embodied AI. Across two synthetic benchmarks (static and 4D), OVOW attains the best overall layout and geometry accuracy and the lowest photometric and semantic error among all baselines, and on monocular video runs one to two orders of magnitude faster than the baselines, while downstream physics simulation confirms its physical stability.

---

## 22. ForgeDrive: Bidirectional Cross-Conditioning for Unified Visual-Action Generation in Autonomous Driving

**Authors:** Xuchang Zhong, He Zheng, Chenxu Zhao, ..., Congyang Zhao, Yang Cai
**arXiv:** [2606.31226](https://arxiv.org/abs/2606.31226)
**Categories:** Computer Vision and Pattern Recognition (cs.CV)

World-model-based autonomous driving endows the model with the ability to understand scene evolution. Yet this promise is undermined by the prevailing imagine-then-act paradigm, which allows errors from the more challenging visual generation stage to cascade into action planning. We introduce ForgeDrive, a unified autoregressive diffusion framework with visual-action cross-conditioning that closes this gap through act-then-imagine paradigm. ForgeDrive factorizes the future as a sequence of per-timestep frame-action pairs, intertwining each action with its corresponding visual observation. During training, we decouple the diffusion timesteps of the two modalities and introduce a UniDiffuser-style noise scheduler to get the ability to infer either modality from its counterpart and deepen understanding of relationships between images and actions. At inference, we propose a novel act-then-imagine inference paradigm, and find that at each step, action generation is a capability internalized during training, requiring no clean future frame as a prerequisite at inference time; instead, the generated action can improve the accuracy of future frame generation, which in turn enhances the quality of the next action. Additionally, we augment each step with future ego-status prediction, further sharpening planning ability. Extensive experiments on NAVSIM demonstrate that ForgeDrive not only unifies driving simulation, planning, and visual odometry into a single model, but also outperforms existing strong planners without any post-training strategy.

---
