# arXiv Daily Digest — 2026-06-09

**Mode:** direct
**Categories:** cs.AI, cs.LG, cs.RO, cs.CV
**Keywords:** VLA, world model, world action model
**Papers found:** 40

---

## 1. FF-JEPA: Long-Horizon Planning in World Models with Latent Planners

**Authors:** Sergi Masip, Jonathan Swinnen, Yutong Hu, Renaud Detry, Tinne Tuytelaars
**arXiv:** [2606.09311](https://arxiv.org/abs/2606.09311)
**Categories:** Artificial Intelligence (cs.AI)

Joint Embedding Predictive Architectures (JEPAs) have shown promising world modeling capabilities, enabling planning in latent space by optimizing action trajectories using methods like the Cross-Entropy Method (CEM). These methods are, however, too computationally expensive and ineffective for long-horizon planning. Furthermore, these methods typically require an explicit image of the goal state, which is not always possible in real-world tasks. In this work, we tackle these limitations by proposing Forward-Forward-JEPA (FF-JEPA), a hierarchical approach leveraging two forward dynamics models. Alongside a standard action-conditioned forward model, we introduce an action-free latent planner that predicts the next subgoal given the current state. This approach removes the need for goal images and enables long-horizon planning by decomposing complex trajectories into a sequence of tractable, short-term optimization problems. Preliminary results on PushT demonstrate that FF-JEPA successfully overcomes flat world models' long-horizon collapse, highlighting this approach as a promising direction for goal-free planning.

---

## 2. AHA-WAM:Asynchronous Horizon-Adaptive World-Action Modeling with Observation-Guided Context Routing

**Authors:** Jisong Cai, Long Ling, Shiwei Chu, ..., Ran Zheng, Yao Mu
**arXiv:** [2606.09811](https://arxiv.org/abs/2606.09811)
**Categories:** Robotics (cs.RO); Artificial Intelligence (cs.AI); Computer Vision and Pattern Recognition (cs.CV)

World-action models have emerged as a promising paradigm for robot manipulation, jointly modeling visual scene dynamics and actions to inject physical priors into policy learning. However, existing world-action models couple world prediction and action execution at the same temporal resolution, forcing the world branch to model near-term frame variations that are redundant and weakly informative. We posit that strictly binding world prediction and action execution to the same temporal rhythm may underutilize the potential of the video branch for embodied control. Therefore, we propose AHA-WAM, an Asynchronous Horizon-Adaptive World-Action Model built on a dual Diffusion Transformer (DiT) architecture that reorganizes world-action modeling around this temporal asymmetry. AHA-WAM instantiates the video DiT as a low-frequency world planner that maintains rolling key-value memory over past observations and exposes reusable layerwise latent context encoding long-horizon scene evolution, while a high-frequency action DiT executes short action chunks in closed loop by querying this context through layerwise joint attention. To support asynchronous execution, we introduce horizon-adaptive offset training and Observation-Guided Video-Context Routing (OVCR), which together let the action expert exploit long-horizon world context while remaining responsive to real-time execution state without rerunning the video DiT. Experiments on RoboTwin and real-world manipulation tasks show that AHA-WAM achieves state-of-the-art performance without any robot-data pretraining, attaining 92.80% average success on RoboTwin and 78.3% success across 4 real-world tasks, while reaching 24.17 Hz closed-loop control with a 4.59x speedup over Fast-WAM.

---

## 3. ReCoVLA: VLM-Guided Reward Compilation for Failure Recovery in Vision-Language-Action Policies

**Authors:** Haodi Hu, Chung-Ta Huang, Jing Liu, ..., Matthew Brand, Toshiaki Koike-Akino
**arXiv:** [2606.09630](https://arxiv.org/abs/2606.09630)
**Categories:** Robotics (cs.RO); Artificial Intelligence (cs.AI); Machine Learning (cs.LG)

Vision-language-action (VLA) policies provide strong priors for language-conditioned manipulation, but remain brittle in off-nominal states requiring targeted recovery. We propose ReCoVLA -- a failure-conditioned residual recovery framework that keeps a pretrained VLA policy frozen, uses an external vision-language model (VLM) to infer the failure mode and recovery stage, and compiles a structured reward from task-relevant components. Rather than using the VLM to generate actions or rewards directly, ReCoVLA uses it as a semantic reward selector: it predicts a recovery descriptor and reward mask for in-simulation residual-policy training, followed by zero-shot sim-to-real deployment of the trained recovery policies. This decouples high-level failure understanding from low-level corrective control to support different VLAs. Experiments across short-horizon, long-horizon, and contact-rich manipulation tasks show that ReCoVLA outperforms the tested baselines on average. In simulation, our reward compiler improves average success from 36.7% for the fine-tuned $\pi_{0.5}$ baseline to 66.7%. In physical zero-shot sim-to-real experiments, ReCoVLA achieves the best average performance, with 61.7% success.

---

## 4. Targeting World Models to Compromise Robot Learning Pipelines

**Authors:** Ethan Rathbun, Ahmed Agha, Saaduddin Mahmud, ..., Alina Oprea, Eugene Bagdasarian
**arXiv:** [2606.09499](https://arxiv.org/abs/2606.09499)
**Categories:** Robotics (cs.RO); Artificial Intelligence (cs.AI); Cryptography and Security (cs.CR)

World models have recently seen a rapid growth in both their popularity and capability as more data efficient tools for generating robot training data or simulating real world environments, with many works proposing their integration into the robot learning pipeline. While highly practical, in this work we demonstrate that world models introduce a uniquely stealthy and effective data poisoning entry point into the robot learning supply chain that can result in the deployment of unsafe or otherwise compromised robotic policies despite training on seemingly safe ground truth training data. In contrast to traditional data poisoning techniques which directly implant dangerous trajectories into sold or uploaded datasets, our novel attack methods inject malicious prompts or compromising transition dynamics into visibly safe teleoperated datasets which are only activated once fed through a world model as input. This can result in the generation of synthetic, dangerous robot training trajectories and subsequently unsafe or compromised robot policies. We demonstrate the effectiveness of our attacks against both state of the art action conditioned and text conditioned world models, showing a full end-to-end backdoor on a downstream DRL policy and a proof-of-concept for the VLA setting. Overall these findings necessitate research into more secure world models and reevaluating their position within the robot learning supply chain.

---

## 5. ATM: Action-Consistency Transfer Matrix for Diagnosing and Improving Latent World Models

**Authors:** Jiaheng Chen
**arXiv:** [2606.09028](https://arxiv.org/abs/2606.09028)
**Categories:** Computer Vision and Pattern Recognition (cs.CV); Artificial Intelligence (cs.AI); Robotics (cs.RO)

Latent world models are increasingly used for control and goal-conditioned planning, yet assessing whether their learned representations are useful for planning usually requires slow, planner-coupled simulator evaluation with CEM or similar planners. Such evaluation is black-box and model-complexity-dependent: under the same protocol, different world models may require minutes to hours per checkpoint. In this work, we propose ATM, an Action-Consistency Transfer Matrix for diagnosing whether latent transitions preserve action semantics relevant to planning. ATM compares action information in real encoded transitions and model-predicted transitions through lightweight post-hoc probes, producing an interpretable matrix that reveals representation quality, transition-domain inconsistency, and failure modes without simulator rollout. It can also be collapsed into a simple screening score for within-task ranking across checkpoints, variants, and world models. When the true success gap is non-trivial, ATM achieves highly reliable pairwise ranking, while reducing minutes-to-hours CEM evaluation to seconds-level transition analysis, yielding more than 100x speedup in our setup. We further introduce AITS, showing that action-identifiability is not only diagnostic but also a useful training signal for improving downstream planning without changing the planner.

---

## 6. Benchmarking Vision-Language-Action Models on SO-101: Failure and Recovery Analysis

**Authors:** Yi Yu, Xinchuan Qiu
**arXiv:** [2606.08881](https://arxiv.org/abs/2606.08881)
**Categories:** Robotics (cs.RO); Artificial Intelligence (cs.AI)

Vision-Language-Action (VLA) models have demonstrated strong generalization in robotic manipulation, yet existing evaluations are primarily conducted in simulation or on expensive robotic platforms, leaving their robustness on affordable real-world robots largely unexplored. We present a standardized real-world benchmark for evaluating representative VLA and imitation learning policies on the low-cost SO-101 robotic platform. The benchmark comprises four representative manipulation tasks together with unified evaluation protocols, enabling systematic comparison under embodiment uncertainty. Using real-world teleoperated demonstrations, we fine-tune and evaluate $\pi_{0.5}$, SmolVLA, Wall-X, and ACT directly on the physical platform. Beyond conventional task success rates, the benchmark incorporates a structured failure taxonomy, semantic- and execution-level failure decomposition, and recovery-aware evaluation metrics to characterize policy robustness. Experimental results show that stronger pretrained VLA policies generally outperform the imitation learning baseline, although performance remains highly task-dependent under low-cost robotic deployment conditions. Execution instability emerges as the dominant failure source, while recovery capability varies substantially across architectures. These results highlight the importance of failure and recovery analysis beyond binary task success and establish SO-101 as a practical benchmark for evaluating embodied AI systems under realistic low-cost robotic deployment conditions.

---

## 7. Unifying Object-Centric World Models and Diffusion Policy: A Hierarchical Framework for Multi-Stage Robotic Tasks

**Authors:** Raktim Gautam Goswami, Prashanth Krishnamurthy, Yann LeCun, Farshad Khorrami
**arXiv:** [2606.08775](https://arxiv.org/abs/2606.08775)
**Categories:** Robotics (cs.RO); Artificial Intelligence (cs.AI)

Visual world models have shown great potential in learning complex system dynamics. Recent advancements leverage these models as transition functions within Model Predictive Control (MPC) frameworks to solve various control tasks. When applied to robotics, however, they are limited to single-stage tasks such as reaching or grasping, and struggle with multi-stage ones that demand complex sequential planning. In this work, we introduce WorldDP, a world model framework designed for multi-stage robotic manipulation. Our hierarchical approach utilizes a high-level world model as a transition function to optimize for feasible subgoals during runtime, which are subsequently reached by a low-level Diffusion Policy. To further aid in learning dynamics and planning, we incorporate object-centric representations that decouple environmental entities and enable us to plan sequentially with respect to each. Evaluated across several robotics benchmarks, WorldDP consistently outperforms existing baselines, validating that coupling the world model's physically grounded planning with diffusion policy's efficient execution yields superior multi-stage performance.

---

## 8. FiberTune: Preserving Action-Fiber Visual Residuals in Vision-Language-Action Fine-Tuning

**Authors:** Haihao Lin, Xiangsheng Huang, Xiao Yang, ..., Zhengyang Wang, Jiahui Du
**arXiv:** [2606.08653](https://arxiv.org/abs/2606.08653)
**Categories:** Computer Vision and Pattern Recognition (cs.CV); Artificial Intelligence (cs.AI); Machine Learning (cs.LG); Robotics (cs.RO)

Action-supervised fine-tuning of vision-language-action (VLA) policies fits demonstrations effectively but constrains only the directions that change predicted actions, leaving visual structure consistent across action-equivalent states free to collapse. We formalize this as residual visual collapse along local action fibers and propose FiberTune, a training-time objective that preserves teacher-structured visual residuals without adding inference-time overhead. FiberTune uses an online action probe to estimate action-predictive feature directions, filters them from intermediate visual-token representations, and aligns the resulting probe-filtered residuals to a frozen visual teacher while regularizing their effective rank. Under identical training conditions, FiberTune improves over task-loss-only fine-tuning in every one of six controlled simulation settings spanning two benchmarks and two architectures (pi_0.5 and OpenVLA-OFT), as well as on physical SO-101 pick-place; representative gains include +10.7 percentage points SR(5) on long-horizon CALVIN ABC-to-D and physical SO-101 task success rising from 72.7% to 78.1%. Residual diagnostics show that these gains coincide with increased probe-filtered residual teacher alignment and effective rank, consistent with the action-fiber motivation.

---

## 9. GEAR-VLA: Learning Geometry-Aware Action Representations for Generalizable Robotic Manipulation

**Authors:** Yuan Zhang, Shiqi Zhang, Yedong Shen, ..., Xingyi Zhang, Jia Pan
**arXiv:** [2606.08530](https://arxiv.org/abs/2606.08530)
**Categories:** Robotics (cs.RO); Artificial Intelligence (cs.AI)

Vision-Language-Action (VLA) models achieve strong benchmark performance but still struggle in real-world deployment with unseen objects, background shifts, and different robot embodiments. We argue that this stems from the lack of a unified geometry-aware manipulation representation, leaving existing VLAs vulnerable to low-level trajectory supervision, misaligned 3D features, and embodiment differences. To address this, we propose GEAR-VLA, a VLA framework for learning unified geometry-aware action representations for generalizable robotic manipulation. GEAR-VLA adopts coarse-to-fine action learning, where multi-source embodied pretraining equips the VLM with embodied reasoning and discrete action understanding before latent action tokens connect action semantics to a gradient-decoupled DiT continuous action expert. It further performs semantic-aligned 3D integration by aligning a trainable 3D spatial backbone with the VLA representation while freezing the original VLM-aligned visual pathway. To share this representation across robots, GEAR-VLA uses embodiment canonicalization, where embodiment-aware states and embodiment-invariant actions confine robot differences to the low-level interface. Extensive simulation and real-world experiments demonstrate strong generalization: GEAR-VLA achieves state-of-the-art performance on LIBERO, zero-shot LIBERO-Plus, and RoboTwin 2.0, reaches 85.9% success on AgileX and 81.0% on the pretraining-unseen LDT-01 embodiment, and obtains 90.1% success on a 6,360-trial universal grasping benchmark with 212 unseen objects. Code and models will be released at this https URL.

---

## 10. Ego-Pi: VLA Fine-Tuning for Ego-Centric Human and Robot Data

**Authors:** Ji Woong Kim, Ke Wang, Zipeng Fu, ..., Jeff Lai, Chelsea Finn
**arXiv:** [2606.08107](https://arxiv.org/abs/2606.08107)
**Categories:** Robotics (cs.RO); Artificial Intelligence (cs.AI)

Robotics faces a fundamental challenge of data scarcity. Unlike language or vision research, there is no internet-scale dataset for robotic manipulation. A promising path forward is to leverage egocentric human data, which can be collected more easily, with greater breadth, and at a larger scale. Towards this end, we investigate key design choices for learning across human and humanoid embodiments equipped with dexterous five-finger hands, using the $\pi_{0.5}$ model as a foundation. Our results show that human data enables robots to learn new task semantics and compose existing skills into novel behaviors without corresponding robot data. The paper website is here: this https URL

---

## 11. vla.cpp: A Unified Inference Runtime for Vision-Language-Action Models

**Authors:** Khanh D. Nguyen, Hung T. Ho, Chinh T. Nguyen, ..., Vien A. Ngo, An T. Le
**arXiv:** [2606.08094](https://arxiv.org/abs/2606.08094)
**Categories:** Robotics (cs.RO); Artificial Intelligence (cs.AI); Machine Learning (cs.LG); Systems and Control (eess.SY)

Vision-Language-Action (VLA) policies are typically shipped as Python/PyTorch stacks that assume a workstation-class GPU, a mismatch for the hardware on which robots actually run. We present this http URL, a portable C++ inference runtime built on this http URL. To our knowledge, it is the first ggml-class engine to natively serve the flow-matching and diffusion VLA inference pattern, in which a cached vision-language prefix is consumed by a cross-attending action expert integrated over several solver steps. A single runtime serves seven architectures spanning five backbone and four action-head families behind one request/response protocol, with each model packaged as a self-contained bundle. On LIBERO-Object, the engine matches a state-of-the-art checkpoint to within one episode out of 200, and runs BitVLA at 100% success in 1.3 GiB of memory. The same bundle runs unchanged across three hardware tiers, from a consumer GPU down to an 8 GB embedded module. A cross-hardware roofline analysis shows that batch-1 VLA inference is compute-bound, so utilization rather than bandwidth is the deployment lever; an IMMA ladder GEMM derived from this analysis cuts BitVLA per-step latency by 4.5x. We then frame an on-robot stress test on an ALOHA arm that isolates the latency constraint under which a learned VLA must replan against a moving target on the hardware it was trained for. Code, demo videos, and the reproducible benchmark scaffold are available at this https URL.

---

## 12. PRISM: PRior-guided Imagination Sampling in world Models

**Authors:** Yuhai Wang, Jiawei Xia, Rongxuan Zhou, ..., Jing Du, Yang Ye
**arXiv:** [2606.07974](https://arxiv.org/abs/2606.07974)
**Categories:** Robotics (cs.RO); Artificial Intelligence (cs.AI)

A learned world model provides a powerful physical intuition for evaluating future states. But its effectiveness in continuous control also depends critically on how candidate actions are generated for model-based planning. Rather than solely asking how accurately a model can simulate the future, we ask: which candidate actions are worth evaluating in the first place? Existing planners typically search arbitrarily or use expert demonstrations only to initialize a sampling mean, discarding the expert's state-conditioned confidence. Properly guiding this search requires a robust action prior, yet current approaches often rely on independent visual encoders or large-scale VLMs to obtain one. We argue that this architectural bloat is unnecessary: the exact same data - and the learned representations of the world model itself - inherently encode the agent's action intuition. We introduce PRISM, a task-agnostic framework that extracts both from a single dataset while maintaining strict architectural simplicity. Building on a standard JEPA-style latent world model, PRISM attaches a lightweight MLP directly to its frozen encoder to predict a state-conditioned Gaussian prior. At plan time, PRISM fuses this prior into the planner's sampling distribution via a precision-weighted Product-of-Gaussians update. This parameter-free, closed-form integration steers the sampling process, making the prior confident where it is and ceding control where it is not. PRISM improves success rates by 35 percentage points over vanilla world-model-based MPC on Cube and 32 percentage points on PushT, without introducing significant inference overhead.

---

## 13. What Makes Video World Model Latents Action-Relevant: Prediction over Reconstruction

**Authors:** Jewon Yeom, Hanseul Kim, Jeongjae Park, ..., Jaejin Lee, Taesup Kim
**arXiv:** [2606.07687](https://arxiv.org/abs/2606.07687)
**Categories:** Computer Vision and Pattern Recognition (cs.CV); Artificial Intelligence (cs.AI)

Video world models are increasingly used to provide predictive visual representations, yet it remains unclear which pretraining signals induce action-relevant structure in their latent spaces. We study this question through a unified probe-based evaluation across diverse encoder families, including image-only self-supervision, video pretraining with and without latent prediction, reconstruction-based autoencoders, diffusion models, and shortcut-forcing dynamics models. Using a common inverse-dynamics probing objective, we find that action-relevant structure is driven primarily by temporal video pretraining rather than pixel reconstruction fidelity: models with strong pixel decoding quality can exhibit near-zero action recoverability, while video-pretrained self-supervised encoders consistently achieve the best Pareto trade-off between visual fidelity and action prediction. Comparing V-JEPA and VideoMAE further shows that most gains arise from natural-video temporal context, with feature-level latent prediction providing a smaller additional benefit. These trends transfer across robotic benchmarks, though CALVIN reveals that static-environment tasks can partially mask the importance of temporal structure by allowing strong image priors to suffice. Finally, inverse-dynamics supervision substantially improves robustness to visual corruption, suggesting that action-aware objectives regularize latent geometry beyond clean-setting performance. Our results identify temporal predictive structure -- not reconstruction fidelity -- as the primary ingredient underlying action-relevant video representations.

---

## 14. Toward Compiler World Models: Learning Latent Dynamics for Efficient Tensor Program Search

**Authors:** Haolin Pan, Lianghong Huang, Xvlin Zhou, Mingjie Xing, Yanjun Wu
**arXiv:** [2606.09312](https://arxiv.org/abs/2606.09312)
**Categories:** Machine Learning (cs.LG); Programming Languages (cs.PL)

Tensor program optimization is essential for modern machine learning systems, but its search space is enormous. Existing auto-schedulers reduce measurement cost with learned cost models, yet they usually evaluate each candidate as a static code snapshot, ignoring the schedule trajectory that produced it. This makes them insensitive to action dependencies and vulnerable to superficial code variations. We propose a \emph{world-model-inspired} evaluator that models schedule evaluation as action-conditioned latent dynamics over program states. Starting from the initial program, it rolls out scheduling actions in a continuous latent space with a lightweight transition model, avoiding expensive AST mutation and repeated code encoding. The final dynamic representation is combined with action and hardware features to rank candidates. Implemented in TVM AutoScheduler, our method improves representative-subgraph latency over Ansor by 1.37$\times$ on GPU and 1.54$\times$ on CPU under the same 64-trial budget. It also matches Ansor-10K within 2.2% geometric mean using 10$\times$ fewer measurements, and accelerates full-model inference over PyTorch/PyTorch-opt(cuDNN) by 4.61$\times$/3.67$\times$ geometric mean.

---

## 15. C$^3$ache: Accelerating World Action Models with Cross Inference Chunk Cache

**Authors:** Weisen Zhao, Lam Nguyen, Zhicong Lu, Yuzhang Shang
**arXiv:** [2606.08962](https://arxiv.org/abs/2606.08962)
**Categories:** Machine Learning (cs.LG); Computer Vision and Pattern Recognition (cs.CV); Robotics (cs.RO)

World Action Models (WAMs) generalize better than standard Vision-Language-Action (VLA) policies to novel motions and environments, because a video-modeling objective lets them learn from abundant unlabeled video rather than scarce labeled robot demonstrations. This generalization is computationally expensive. To complete a task, a WAM runs over multiple inference chunks, and each chunk requires a costly denoising process. Existing acceleration methods reduce this cost by caching and reusing computation within a single chunk's denoising trajectory. Our empirical analysis reveals a substantial source of redundancy they overlook: redundancy across chunks. When a robot executes a smooth behavior, the residuals computed at a given denoising step are strongly correlated from one chunk to the next. We introduce C$^3$ache, a training-free method that caches and reuses these residuals across inference chunks at the same denoising step. Experiments on benchmarks with a Fast-WAM backbone show that C$^3$ache achieves up to a $2.5\times$ speedup in total wall-clock inference time, with negligible degradation in task success rate.

---

## 16. Echo-Memory: A Controlled Study of Memory in Action World Models

**Authors:** Wayne King, Zeyue Xue, Yuxuan Bian, ..., Haoyang Huang, Nan Duan
**arXiv:** [2606.09803](https://arxiv.org/abs/2606.09803)
**Categories:** Computer Vision and Pattern Recognition (cs.CV); Graphics (cs.GR); Machine Learning (cs.LG)

We present \textbf{Echo-Memory}, a controlled study of memory mechanisms in action-conditioned world models. These models generate multi-segment videos from a first frame, text prompt, and camera-action sequence, but their central failure is often memory rather than local image synthesis: after the camera leaves and returns, the scene or salient object may silently change. Existing memory designs are hard to compare because gains are entangled with backbone, training, retrieval, and evaluation differences. Echo-Memory fixes the action-to-video interface and varies only how history is stored and read by the generator. Under a shared video diffusion backbone, optimizer, camera-action representation, sampler, and evaluation pipeline, we compare raw context, compression-based memory, spatial summaries with different read-out paths, and state-space recurrence. This matched matrix separates four otherwise conflated axes: \emph{capacity}, \emph{compression}, \emph{read-out}, and \emph{recurrence}. We also evaluate memory through a three-branch protocol: replay quality, in-domain loop revisit, and open-domain return probes. The branches routinely disagree, showing that replay fidelity is not a sufficient proxy for remembering a world. Three findings follow. Raw context is a strong capacity baseline and improves open-domain return far more than it improves replay metrics. Compactness is not a free substitute for capacity: aggressive spatial and hybrid-compression memories lose the salient evidence needed for return. Finally, block-wise state-space recurrence is the strongest open-domain return mechanism in our matrix, showing that the structure of implicit memory matters as much as the decision to use it. These results provide a compact protocol for studying memory in action world models beyond isolated replay metrics.

---

## 17. Your Model Already Knows: Attention-Guided Safety Filter for Vision-Language-Action Models

**Authors:** Seongbin Park, Fan Zhang, Baharan Mirzasoleiman, Shahriar Talebi, Nader Sehatbakhsh
**arXiv:** [2606.09749](https://arxiv.org/abs/2606.09749)
**Categories:** Robotics (cs.RO); Machine Learning (cs.LG)

Vision-Language-Action (VLA) models have demonstrated impressive end-to-end performance across a variety of robotic manipulation tasks. However, these policies offer no guarantees against collisions with task-irrelevant objects in the scene. Existing safety filters sidestep this problem by querying a vision-language model (VLM) to identify obstacles and their locations. This, however, is too slow to run in the control loop and can only be invoked at episode initialization, leaving the filter unable to track moving obstacles. We discover that a small number of attention heads within a VLA model reliably localize the object the policy intends to approach. These heads can be exploited within a training-free safety framework that obtains the active target from the attention heads at every step, treats the remainder of the scene as obstacles, and feeds these into a Control Barrier Function (CBF) filter. Together with a lightweight real-time object tracker, this allows for collision avoidance for non-static obstacles. We evaluate our framework on SafeLIBERO, which we extend with moving obstacles. On the original static benchmark, our method performs comparably to an oracle that uses privileged simulator state to identify the target, emulating a VLM-based identification step run once at episode initialization. On the dynamic variant, where the oracle's init-time target assignment becomes stale, our method substantially outperforms it by 43%, on average. Our findings suggest that the perceptual signals needed for real-time safety filtering are already present within VLA policies and can be exploited without additional training or heavy auxiliary models.

---

## 18. MemoryVLA++: Temporal Modeling via Memory and Imagination in Vision-Language-Action Models

**Authors:** Hao Shi, Weiye Li, Bin Xie, ..., Ping Luo, Gao Huang
**arXiv:** [2606.09827](https://arxiv.org/abs/2606.09827)
**Categories:** Robotics (cs.RO); Computer Vision and Pattern Recognition (cs.CV)

Temporal modeling is essential for robotic manipulation, as effective control requires both memory of past interactions and imagination of future states. However, most VLA models rely primarily on the current observation and therefore struggle with long-horizon, temporally dependent tasks. Cognitive science suggests that humans rely on working memory to buffer short-lived context, the hippocampal system to preserve episodic memory of past experience, and internal models to imagine possible future state evolution. Inspired by these mechanisms, we propose MemoryVLA++, a full temporal modeling framework that equips VLA models with memory and imagination for robotic manipulation. A pretrained VLM encodes the current observation into perceptual and cognitive tokens, forming working memory. These tokens query a Perceptual-Cognitive Memory Bank to retrieve relevant historical context. This bank stores low-level details and high-level semantics from past interactions, and is updated through redundancy-aware consolidation. A world model imagines future states in a denoising latent space, and the imagined latents are integrated under memory guidance to form full temporal-aware tokens. The resulting tokens condition a diffusion action expert to predict temporally consistent action sequences. We conduct extensive experiments on 5 simulation benchmarks and 3 categories of real-robot tasks across 3 robots, covering general manipulation, long-horizon temporal tasks, robustness, and generalization. Our method achieves strong performance across Libero, SimplerEnv, Mikasa-Robo, Calvin, Libero-Plus, and diverse real-robot tasks, validating the effectiveness of full temporal modeling with memory and imagination. For example, on real robots, it achieves +9%, +26%, +28% gains on general, memory-dependent, and imagination-dependent tasks. Project Page: this https URL

---

## 19. iMaC: Translating Actions into Motion and Contact Images for Embodied World Models

**Authors:** Zhenyu Wu, Xiuwei Xu, Yukun Zhou, ..., Jiwen Lu, Haibin Yan
**arXiv:** [2606.09813](https://arxiv.org/abs/2606.09813)
**Categories:** Robotics (cs.RO); Computer Vision and Pattern Recognition (cs.CV)

Embodied world models have emerged as a pivotal paradigm for visual robotic decision-making and interactive environment simulation. However, conventional embodied frameworks rely on low-dimensional structured action vectors (e.g., joint angles and end-effector poses), which suffer from limited expressive capacity, poor generalization across diverse embodiments, and unnatural dynamic modeling for complex physical interactions. To address these limitations, this paper proposesiMac (Image as Action Control), a novel unified control paradigm that treats raw visual images as native action representations for embodied world models. Departing from traditional explicit kinematic action encoding, iMac formulates continuous visual manipulation as image-based action tokens, which inherently encapsulate spatial motion intentions, interactive geometric constraints and subtle physical dynamics. We construct a dual-branch embodied architecture consisting of an image-action encoder and a dynamic world predictor: the encoder compresses target-driven visual images into compact action embeddings, while the predictor learns environment transition rules conditioned on image actions to achieve high-fidelity future state prediction and closed-loop embodied control. Extensive experiments are conducted on public embodied manipulation benchmarks and real-world robotic scenarios. The results demonstrate that iMac outperforms vector-based action control baselines in prediction accuracy, task success rate and cross-scene generalization ability. Moreover, our image-action design eliminates the reliance on manually defined action spaces, realizing flexible and universal control for heterogeneous embodied agents. This work provides an innovative visual-action perspective for embodied world models, offering a simple yet effective paradigm for scalable robotic perception and manipulation.

---

## 20. ProbeAct: Probe-Guided Training-Free Failure Recovery in Vision-Language-Action Models

**Authors:** Fan Zhang, Seongbin Park, Baharan Mirzasoleiman, Shariar Talebi, Nader Sehatbakhsh
**arXiv:** [2606.09740](https://arxiv.org/abs/2606.09740)
**Categories:** Robotics (cs.RO)

Vision-Language-Action (VLA) models demonstrate strong perfor-1 mance on language-conditioned robotic manipulation within their training dis-2 tribution, yet their generalization capabilities remain fundamentally limited. They3 lack the robustness required to handle perturbations, frequently failing when con-4 fronted with lighting changes, altered camera viewpoints, or small initial-state5 variations. We propose PROBEACT, a training-free runtime intervention frame-6 work that detects and recovers from grasping and placement failures in pre-7 trained VLA policies without modifying their weights or requiring additional8 demonstrations. PROBEACT combines three components: (i) a lightweight multi-9 target hidden-state probe that predicts the 3D positions of task-relevant objects10 from intermediate VLA features, with Hungarian-matched identity tracking for11 multi-object scenes; (ii) an object-agnostic kinematic state machine that detects12 grasp, transport, and placement failures using only gripper-internal signals and13 end-effector kinematics; and (iii) a hierarchical Control Barrier Function (CBF)14 filter that encodes repeated-failure locations as soft safe-set constraints, mini-15 mally correcting VLA actions while preserving baseline behavior. As a plug-and-16 play, training-free intervention loop, PROBEACT is orthogonal to existing train-17 ing pipelines. Evaluated on the LIBERO-plus benchmark, our framework acts as18 a universal safety net, improving the success rate of the OpenVLA-OFT model19 from 69.6% to 74.1%, while demonstrating broad applicability to both base and20 fine-tuned VLA policies.

---

## 21. $ω$-EVA: Envision, Verify, and Act with Latent Interactive World Models

**Authors:** Zhenguo Sun, Yu Sun, Hande Huang, Alois Knoll
**arXiv:** [2606.09457](https://arxiv.org/abs/2606.09457)
**Categories:** Robotics (cs.RO)

Embodied policies typically map current observations directly to actions, leaving candidate-action consequences implicit. World models provide predictive supervision, representations, or external simulation, but rarely let a policy inspect the imagined consequence of its own proposal before acting. We introduce $\omega$-EVA, a latent interactive world model that realizes an Envision--Verify--Act loop for embodied action generation. Its three-stage framework learns action-conditioned latent dynamics, trains a language-conditioned flow policy on dynamics-aware visual representations, and feeds the policy's proposal back through the world model. A tri-branch refiner jointly reasons over the current state, proposal-conditioned future, and proposed action to produce the final action chunk. Because consequence reasoning remains in latent feature space, $\omega$-EVA avoids generating future videos at inference. Evaluations across diverse single-arm, bimanual, long-horizon, and perturbed simulation settings show that the complete interaction pipeline consistently improves the proposal policy, while latent diagnostics indicate meaningful action-conditioned future structure. With approximately 1.2B parameters and no additional robot-data pretraining, $\omega$-EVA demonstrates a compact and competitive performance--scale--data trade-off, making the world model an active action-feedback module rather than a passive predictor.

---

## 22. TORL-VLA: Tactile Guided Online Reinforcement Learning for Contact-Rich Manipulation

**Authors:** Huaihang Zheng, Yi Yang, Kai Ma, ..., Yinian Mao, Baoxu Liu
**arXiv:** [2606.09337](https://arxiv.org/abs/2606.09337)
**Categories:** Robotics (cs.RO)

Vision-Language-Action (VLA) models have become a powerful framework for robotic manipulation, and recent studies have introduced tactile or force feedback into VLAs to address contact-rich tasks. However, these models are typically deployed as offline policies. When contact conditions shift from the training distribution, the policy cannot perform online adaptation, leading to problems such as inappropriate contact forces and inefficient retries. Therefore, we propose TORL-VLA, a tactile-guided online reinforcement learning framework that couples tactile feedback with policy refinement for contact-rich manipulation. Our method introduces a tactile-derived wrench-aware VLA to predict reference actions and future wrench sequences, while a lightweight online RL module is used to refine the reference actions. To stabilize learning from mixed exploratory policy-generated and human-intervention data, we introduce an intervention-censored critic that prevents post-intervention success from being wrongly credited to policy-generated actions preceding intervention. Real-robot experiments on long-horizon contact-rich tasks, including latch manipulation, coffee-cup placement, and egg handling, show that TORL-VLA improves success rates at both subtask and full-task levels, as well as time-bounded execution efficiency over strong baselines.

---

## 23. Back to the Familiar Future: Failure Recovery for VLA Policies via Pre-Imagined Milestone Selection

**Authors:** Suyeon Shin, Juwon Kim, Hyeonbin Park, ..., Hyung-Sin Kim, Byoung-Tak Zhang
**arXiv:** [2606.09258](https://arxiv.org/abs/2606.09258)
**Categories:** Robotics (cs.RO)

Vision-language-action (VLA) policies can deviate from nominal trajectories during manipulation, even when tasks remain physically feasible. Recovering from these deviations is challenging, as they push the policy into unfamiliar state spaces where direct re-planning frequently destabilizes action sequences. We propose Back to the Familiar Future (B2FF), a recovery framework for foresight-driven VLAs that leverages future visual conditioning as a recovery interface. Before execution, the VLA generates a milestone bank of familiar future states conditioned on the clean initial observation. At recovery time, a recoverability-aware selector selects a recovery milestone from this bank and enforces it as a fixed visual goal. This enables the VLA to robustly map off-trajectory observations back to a familiar future. On failure-injected LIBERO, under controlled recovery timing aligned with the injected failure, B2FF increases the average success rate of a baseline VLA from 56.3% to 74.0%, demonstrating that pre-imagined milestones can guide recovery without fine-tuning the low-level action generator.

---

## 24. MotionWAM: Towards Foundation World Action Models for Real-Time Humanoid Loco-Manipulation

**Authors:** Jia Zheng, Teli Ma, Yudong Fan, ..., Shuo Yang, Junwei Liang
**arXiv:** [2606.09215](https://arxiv.org/abs/2606.09215)
**Categories:** Robotics (cs.RO)

World Action Models (WAMs) couple a video dynamics prior to the policy and have shown encouraging results on tabletop manipulation, but iterative denoising over high-dimensional video-action latents leaves them too slow for real-time humanoid loco-manipulation. The problem is compounded by the dominant hierarchical paradigm, in which a high-level manipulation policy controls only the upper body while a low-level controller tracks coarse base commands -- placing upper and lower body in inconsistent action spaces and reducing the legs to balance-preserving locomotion. We present MotionWAM, a real-time WAM that drives autonomous humanoid loco-manipulation from a single egocentric camera by conditioning the policy on the intermediate denoising features of a video world model. MotionWAM replaces the upper-lower split with a unified motion latent and predicts whole-body motion tokens that jointly cover locomotion, torso motion, height regulation, foot interaction, and hand manipulation in a single action space. A three-stage learning framework progressively adapts the video world model to egocentric visual dynamics and to the target humanoid embodiment. On nine real-world Unitree G1 tasks, MotionWAM runs in real time, substantially outperforms Vision-Language-Action (VLA) baselines fine-tuned on the same demonstrations by over 30% in overall success rate, and executes task-driven foot interaction that decoupled upper-lower policies cannot reach. Our results suggest that video-pretrained WAMs can be lifted from tabletop manipulation to coordinated, human-like whole-body humanoid control.

---

## 25. Dream-Tac: A Unified Tactile World Action Model for Contact-Rich Robot Manipulation

**Authors:** Yunfan Lou, Yifan Ye, Yankai Fu, ..., Zhihe Lu, Shanghang Zhang
**arXiv:** [2606.08737](https://arxiv.org/abs/2606.08737)
**Categories:** Robotics (cs.RO)

World action models inherit the predictive capability of world models, enabling action generation to be guided by anticipated future observations. However, they rely primarily on vision and often fail in contact-rich manipulation, where critical cues arise from physical interaction. In this paper, we propose Dream-Tac, a unified Tactile-World Action Model that jointly models actions, future visual observations, and tactile dynamics. Specifically, Dream-Tac introduces (i) contact-gated visuotactile fusion to selectively integrate tactile signals and (ii) a contact-aware attention bias to better regulate cross-modal interactions during manipulation. To support real-time deployment, we further design a dual-level acceleration strategy, reformulating the contact-aware bias to preserve the fused attention path during training and introducing cache-based diffusion acceleration at inference, achieving up to 2.9$\times$ faster training and 1.8$\times$ faster inference. Across six contact-rich manipulation tasks, Dream-Tac improves action accuracy by 31.7\% on average, demonstrating the effectiveness of unified visuotactile world this http URL is available at this https URL.

---

## 26. FAWAM: Force-Aware World Action Models for Closed-Loop Contact-Rich Manipulation

**Authors:** Haotian He, Zeyu Yan, Qipeng Liu, Ning Guo, Wenzhao Lian
**arXiv:** [2606.08555](https://arxiv.org/abs/2606.08555)
**Categories:** Robotics (cs.RO)

Force signals provide critical interaction cues for contact-rich robotic manipulation. However, existing methods mostly use force as an additional observation modality, without fully exploiting its role in modeling future interaction dynamics or guiding execution-time feedback correction. In this paper, we propose FAWAM, a force-aware world action model that incorporates force information at three levels: perception, prediction, and closed-loop execution. FAWAM first encodes historical 6-axis force/torque signals to modulate action generation, then jointly predicts future actions and end-effector wrenches to explicitly model contact evolution. It further introduces a residual correction module that uses the predicted wrench trajectory as an execution-time reference to refine actions online based on real-time force feedback. Real-world experiments across multiple contact-rich tasks show that FAWAM improves the average success rate by 36.25% over vision-only baselines and 21.25% over existing force-aware baselines, demonstrating the effectiveness of our force-aware framework for robust contact-rich manipulation.

---

## 27. Two Bridges, One Pathway: From VLMs to Generalizable VLAs with Embodied Trajectory-Coupled Data

**Authors:** Linqi Yin, Shiduo Zhang, Shenling Qiu, ..., Xuanjing Huang, Yu-Gang Jiang
**arXiv:** [2606.08520](https://arxiv.org/abs/2606.08520)
**Categories:** Robotics (cs.RO)

Vision-language models (VLMs) are powerful general-purpose reasoners, yet converting them into robot control policies (VLAs) is surprisingly difficult. The root cause is a two-fold gap: VLMs are trained on internet-scale images with language-understanding objectives, while VLAs must perceive robot scenes and predict motor actions. Fine-tuning a VLM directly on robot action data forces the model to cross both gaps at once -- the learning curve is steep and the rich generalizations learned during pretraining tend to degrade rather than transfer. We argue that this gap can be bridged gradually with the right intermediate data. We introduce \emph{embodied trajectory-coupled (ETC) data} -- vision-language supervision derived from the same robot scenes and trajectories used for action learning. Because ETC data shares the visual context of robot operation while retaining familiar language-understanding objectives, it provides a natural stepping stone between VLM pretraining and VLA fine-tuning. Building on this, we design a three-stage training recipe. Distribution Bridging first adapts the VLM to embodied visual-language semantics. Objective Bridging then gradually shifts the model toward action prediction while preserving the acquired representations. Retentive Adaptation finally specializes the policy to the target deployment domain. We further show that mixing task-relevant out-of-distribution ETC data with a small amount of action data enables the model to generalize to novel visual-language conditions without requiring additional robot demonstrations. Simulation and real-robot experiments confirm that this gradual bridging strategy is the key to transferring VLM generalization into robust, deployable robot policies.

---

## 28. MotionVLA: Injecting Geometric Motion into Vision-Language-Action Model

**Authors:** Shanglin Yuan, Weiheng Zhao, Xianda Guo, ..., Wenyu Liu, Xinggang Wang
**arXiv:** [2606.08288](https://arxiv.org/abs/2606.08288)
**Categories:** Robotics (cs.RO)

Vision-language-action (VLA) models increasingly condition robot policies on history, depth, or 4D features to resolve ambiguity in long-horizon manipulation. However, more spatiotemporal evidence is not necessarily better: when the injected evidence is not motion-consistent, it can introduce geometric drift, fragmented temporal cues, and unstable action generation. This raises a simple question: should a VLA remember past frames, or remember the motion that connects them? We introduce MotionVLA, a motion-history interface that converts a short past-only video window into compact, time-continuous trajectory-field tokens. Instead of treating history as a sparse set of ndependently lifted frames, MotionVLA represents recent observations as physically coherent motion evidence. Current visual tokens query this history to retrieve task-relevant motion information, which is then recoupled into the VLA stream under trajectory-grounded supervision. Experiments across simulation benchmarks and preliminary real-robot rollouts show that MotionVLA improves long-horizon manipulation while producing smoother and more direct executions. These results suggest that effective VLA memory is not just about providing more 4D context, but about exposing motion-consistent evidence that is usable for control.

---

## 29. Q-VGM: Q-Guided Value-Gradient Matching for Flow-Matching VLA Policies

**Authors:** Ziqian Wang, Jiayu Sun, Xingjian Mao, Minqian Wang, Yao Mu
**arXiv:** [2606.08015](https://arxiv.org/abs/2606.08015)
**Categories:** Robotics (cs.RO)

We propose Q-Guided Value-Gradient Matching (Q-VGM), an off-policy reinforcement learning (RL) method that tackles a long-standing challenge in fine-tuning flow-matching vision-language-action (VLA) policies: efficiently improving an expressive flow-matching action expert with respect to a learned Q-function. Effective improvement must exploit the first-order (gradient) information of the critic, but this is difficult for flow policies, because directly back-propagating the value through their multi-step denoising process is numerically unstable at VLA scale, while the tractable action likelihoods required by policy-gradient methods are unavailable under iterative denoising. Existing value-based methods either backpropagate through the full denoising chain, use the critic only at test time without updating the policy, or distill critic-improved actions as terminal labels without supervising the velocity field. Q-VGM sidesteps these issues by leveraging VGG-Flow, a value-gradient view of flow alignment in generative modeling that transforms value gradient into a denoising-time value-gradient field rather than an unstable end-to-end objective. This requires no action likelihoods and no backpropagation through the denoising chain, and operates on a fixed replay buffer. The critic is an action-sensitive Cal-QL ensemble over compact RLT features with per-layer action injection. Q-VGM enables a practical few-shot initialization then learn-from-experience paradigm: starting from a few-shot-SFT pi0.5 VLA, the method leverages self-generated rollout data to substantially improve task performance without additional expert supervision. On LIBERO, Q-VGM raises the average success rate from 75.0% to 92.5%; on RoboTwin 2.0, from 76.4% to 87.2%; and on two real-robot tabletop tasks, from 40.0% to 67.5%, outperforming all same-backbone, same-critic baselines across all three settings.

---

## 30. TBD-VLA: Temporal Block Diffusion Vision Language Action Model

**Authors:** Sung-Wook Lee, Xuhui Kang, Yen-Ling Kuo
**arXiv:** [2606.07895](https://arxiv.org/abs/2606.07895)
**Categories:** Computer Vision and Pattern Recognition (cs.CV); Robotics (cs.RO)

Discrete Vision-Language-Action (VLA) models typically formulate action generation as next-token prediction over discretized action spaces, conditioning each token autoregressively on prior context. While effective, this paradigm incurs high inference latency and largely ignores the temporal structure inherent in action trajectories. Recent efforts introduce parallel decoding to improve efficiency, enabling faster inference, but lack explicit mechanisms for modeling token dependencies. We introduce TBD-VLA, a discrete token-based VLA framework that incorporates block diffusion to enable temporal action generation. We partition action sequences into temporal blocks and perform masked discrete diffusion within each block, while maintaining autoregressive generation across blocks. This design unifies temporal autoregression and parallel action decoding, achieving both strong temporal coherence and improved inference speed. In addition, the explicit temporal modeling enables asynchronous execution of action chunks (e.g., Real-Time Chunking) via temporal in-painting. TBD-VLA significantly outperforms prior VLA approaches in both simulation and real-world manipulation tasks, offering a scalable path toward fast, temporally aware, discrete VLA models. Project webpage: this https URL

---

## 31. Latent Spatial Memory for Video World Models

**Authors:** Weijie Wang, Haoyu Zhao, Yifan Yang, ..., Yuqing Yang, Bohan Zhuang
**arXiv:** [2606.09828](https://arxiv.org/abs/2606.09828)
**Categories:** Computer Vision and Pattern Recognition (cs.CV)

Video world models that maintain 3D spatial consistency across generated frames typically rely on explicit point cloud memory constructed in RGB space. This design is both computationally expensive, requiring repeated rendering and VAE encoding, and inherently lossy, as the round trip through pixel space discards rich features of the learned latent representation. In this paper, we introduce \emph{latent spatial memory} for video world models, a persistent 3D cache that stores scene information directly in the diffusion latent space, avoiding pixel-space reconstruction. Building on this, we propose Mirage, a latent-space spatial memory framework that constructs the memory by lifting latent tokens into 3D via depth-guided back-projection and queries it by synthesizing novel views through direct latent-space warping. This unified formulation eliminates both the information loss of pixel-space reconstruction and the computational burden of repeated encoding and rendering. Experiments show that latent spatial memory achieves up to \textbf{10.57}$\times$ faster end-to-end video generation and \textbf{55}$\times$ reduction in memory footprint relative to explicit 3D baselines. Leveraging the geometric prior of the diffusion model, Mirage attains state-of-the-art performance on WorldScore and strong reconstruction quality on RealEstate10K.

---

## 32. Prisma-World: Camera-Controllable Multi-Agent Video World Model

**Authors:** Huiqiang Sun, Zhan Peng, Size Wu, ..., Ziwei Liu, Wei Li
**arXiv:** [2606.09507](https://arxiv.org/abs/2606.09507)
**Categories:** Computer Vision and Pattern Recognition (cs.CV)

Video world models have made rapid progress in generating controllable visual experiences, but most of them still simulate the world from a single observer. Extending such models to multiple agents raises a central challenge: if each agent's future state is generated independently, overlapping views may instantiate different versions of the same scene, leading to inconsistent objects, layouts, and appearances across agents. Conventional camera conditioning controls individual trajectories, but it does not explicitly couple the generation of views that should agree under shared scene geometry. We introduce Prisma-World, a camera-controllable multi-agent world model that formulates multi-agent generation as a joint geometry-aware denoising process for cross-view consistency. Prisma-World processes all agent videos within one full-attention sequence, uses a multi-agent RoPE design to distinguish agent identities while preserving synchronized temporal coordinates, and injects relative camera geometry into attention to bias overlapping viewpoints toward shared scene evidence. To further strengthen multi-view consistency and enhance global spatial perception, we augment our framework with an overlap-decaying curriculum training paradigm alongside minimap-conditioned structural guidance. To facilitate the training and evaluation of multi-agent models, we introduce PrismaDataset, a large-scale UE5 dataset with panoramic acquisition across diverse scenes, composable multi-agent view groups with flexible agent counts and complex camera trajectories, and precise camera/action annotations for consistency training and evaluation. Experiments show that a single Prisma-World model can generate high-fidelity multi-agent videos with flexible agent numbers, camera controllability, improved cross-view consistency, and spatial grounding under minimap guidance.

---

## 33. Scaling by Diversified Experience for Vision-Language-Action Models

**Authors:** Leiyu Wang, Zhaofengnian Wang, Xueqi Li, ..., Cewu Lu, Nanyang Ye
**arXiv:** [2606.09009](https://arxiv.org/abs/2606.09009)
**Categories:** Computer Vision and Pattern Recognition (cs.CV)

Vision-Language-Action models face significant challenges in real-world deployment due to the entanglement of high-level reasoning with low-level control, and the instability of policy optimization. In this paper, we introduce SyVLA, a robust VLA model trained with diversified experiences. We propose an Intention Decoupling algorithm to isolate control-relevant features from reasoning contexts and a similar-sample guided RL pipeline to stabilize policy updates and mitigate distribution shift. Extensive experiments on real-world robotic tasks and multi-modal benchmarks demonstrate that SyVLA achieves superior task success rates and stronger out-of-distribution generalization compared to existing methods, while effectively preserving core vision-language capabilities. Codes and Datasets is released on \href{this https URL}{project page}.

---

## 34. BLUE: Toward Better Language Use in Efficient Vision-Language-Action Models for Autonomous Driving

**Authors:** George Ling, Lijin Yang, Hao Yang, Zhongzhan Huang
**arXiv:** [2606.08684](https://arxiv.org/abs/2606.08684)
**Categories:** Computer Vision and Pattern Recognition (cs.CV)

We present BLUE, a minimal method for better language use in vision-language-action (VLA) models for autonomous driving (AD). Through extensive analysis, we reveal that language matters on only a small fraction of routes, but on those routes it can greatly improve or degrade performance. Generating language at every frame is therefore inefficient, since most computation is spent on frames that do not benefit from language. We further show that pretrained VLA hidden states potentially already encode whether language will benefit a given frame, even though scene complexity and kinematic features alone struggle to predict this. Based on this finding, BLUE trains a lightweight gate on frozen VLA hidden states to decide per frame whether to activate language generation or predict actions directly, without modifying the backbone or requiring additional human annotation. With just a 0.11M-parameter gate, BLUE sets a new state of the art on both benchmarks, achieving 76.2% success rate on Bench2Drive and 36 driving score on Longest6 v2, while delivering 2.54x inference speedup and 8.9% success rate improvement over the backbone. BLUE provides a practical path toward efficient language-augmented AD, showing that VLA models can retain the benefits of language at a fraction of the cost. Our code, data, logs and checkpoints are fully available on this https URL.

---

## 35. Light-WAM: Efficient World Action Models with State-Fusion Action Decoding

**Authors:** Ziang Li, Dongzhou Cheng, Yibin Wang, ..., Juan Wang, Jiaqi Wang
**arXiv:** [2606.08242](https://arxiv.org/abs/2606.08242)
**Categories:** Computer Vision and Pattern Recognition (cs.CV)

World Action Models (WAMs) extend robot policy learning by incorporating future prediction as an additional training objective, encouraging the policy to encode task-relevant temporal structure in its representations. Current WAMs often rely on large-scale generative architectures that incur high training costs and inference latency, making them difficult to deploy as efficient closed-loop policies. We propose Light-WAM, a lightweight World Action Model for efficient robot manipulation. Specifically, it is built with a compact video backbone and performs future-video supervision in a downsampled latent space, reducing the cost of video co-training while retaining its benefits for representation learning. For action prediction, Light-WAM introduces the StateFusionActionExpert, which reads adapted states from multiple backbone layers, fuses them through learned-query pooling, and directly predicts action chunks in a single forward pass. This design provides an efficient interface between video backbone representations and robot actions, avoiding the need for heavy generative action experts. Experiments demonstrate that Light-WAM maintains strong performance on LIBERO and achieves usable multi-task performance on RoboTwin 2.0, while using only 0.44B trainable parameters. It also achieves 72.03ms inference latency with 4.1GiB peak GPU memory and improved training throughput.

---

## 36. DisCo: World Models with Discrete Camera Motion Control

**Authors:** Hongrui Huang, Junke Wang, Quanhao Li, Yu-Gang Jiang, Zuxuan Wu
**arXiv:** [2606.07967](https://arxiv.org/abs/2606.07967)
**Categories:** Computer Vision and Pattern Recognition (cs.CV)

Controllable video world models target interactive world exploration, where models must faithfully execute explicit action commands while preserving visual quality and temporal coherence. However, most existing approaches rely on continuous camera trajectories as action conditions, which often lead to unreliable action following, especially under complex motion sequences. In this work, we identify action representation entanglement as a key bottleneck in controllable video generation, and show that continuous camera representations lead to high feature similarity across distinct motion patterns, degrading action controllability. Based on this insight, we propose DisCo, a controllable video world model that conditions generation on a compact set of discrete action primitives to improve action separability. We further introduce DisCoBench, a comprehensive benchmark for evaluating the ability of models in short-term, long-horizon, and highly dynamic exploration scenarios. Extensive experiments demonstrate that DisCo achieves significantly more reliable action following while preserving visual quality.

---

## 37. CT-VAM: A Cerebello-Thalamic-Inspired Vision-Action Model for Efficient Visuomotor Control

**Authors:** Jiacheng Li, Yize Guo, Jiabin Guo, Qingchen Liu, Jiahu Qin
**arXiv:** [2606.09572](https://arxiv.org/abs/2606.09572)
**Categories:** Robotics (cs.RO); Artificial Intelligence (cs.AI)

Vision-language-action models have shown strong promise for robot manipulation, yet raw language is primarily needed to specify task intent rather than to be repeatedly processed during high-frequency low-level execution. Motivated by this separation, we propose a cerebello-thalamic-inspired vision-action model (CT-VAM) for efficient task-conditioned visuomotor control. CT-VAM acts as a compact local execution policy that predicts action chunks from dualview visual observations, proprioception, and a lightweight task condition, potentially enabling a practical cloud-edge paradigm in which high-level semantic reasoning can be handled by large models while fast closed-loop control runs on local hardware. To fuse heterogeneous inputs effectively, CT-VAM introduces TARS (Thalamic Action Routing Stream), a stream-separated conditional attention decoder that independently routes action, visual and task streams, preventing dense sensory tokens from overwhelming compact task-relevant conditions. With only 68M parameters, CT-VAM achieves LIBERO success rates competitive with substantially larger VLA models, while reducing inference latency. Together with flow-consistent inpainting for asynchronous chunk execution, CT-VAM supports high-frequency control and demonstrates robust realworld deployment on resource-constrained robotic platforms.

---

## 38. CLASP: Language-Driven Robot Skill Selection and Composition using Task-Parameterized Learning

**Authors:** Markus Knauer, Valentin Gieraths, Tai Mai, ..., Freek Stulp, João Silvério
**arXiv:** [2606.08169](https://arxiv.org/abs/2606.08169)
**Categories:** Robotics (cs.RO); Artificial Intelligence (cs.AI); Computation and Language (cs.CL); Human-Computer Interaction (cs.HC); Machine Learning (cs.LG)

Enabling robots to understand and execute tasks from natural language commands while maintaining data efficiency remains challenging. Foundation models such as vision-language-action (VLA) and vision-language models (VLMs) provide intuitive interaction channels but require extensive data; task-parameterized imitation learning achieves data efficiency but lacks natural language grounding. This work bridges this gap through a modular architecture combining task-parameterized kernelized movement primitives (TP-KMPs) with pretrained VLMs. During learning, skills are acquired from 2 to 5 kinesthetic demonstrations, and the VLM generates skill schemas describing each skill's parameters and preconditions. During execution, the VLM interprets commands to select skills, reason about parameter bindings, and create novel behaviors through covariance-weighted composition. When no skill or composition suffices, the system identifies capability gaps and requests targeted demonstrations, all without fine-tuning. Validation on a 7-DoF manipulator shows success rates of 73.3%-100% in scenarios requiring skill selection, composition, and active learning.

---

## 39. EgoPriMo: Egocentric Motion Generation for Interactive Humanoid Control

**Authors:** Haoyang Ge, Peng Ren, Yukun Shi, ..., Kun Li, Kai Chen
**arXiv:** [2606.08495](https://arxiv.org/abs/2606.08495)
**Categories:** Robotics (cs.RO); Computer Vision and Pattern Recognition (cs.CV)

Humanoid robots require whole-body motions that adapt to scene context, task requirements, and user intent. Motion tracking reproduces specified trajectories, and humanoid vision-language-action systems provide semantic interfaces, but neither offers a scalable and interactive prior for broad full-body behavior. We introduce EgoPriMo (Egocentric Motion Prior for Humanoid Robots), a unified framework that learns such priors from egocentric human demonstrations. Given egocentric observations and a text prompt, EgoPriMo reconstructs, generates, and forecasts SMPL-based full-body motion. Language is used as a high-level control signal rather than a complete motion specification. At the core of EgoPriMo is a Triple-stream DiT that jointly models body dynamics, egocentric visual context, and text; task-conditioning masks route different tasks and missing-modality data through the same checkpoint. Experiments on Nymeria and EgoExo4D show that one checkpoint improves egocentric motion generation over UniEgoMotion while supporting reconstruction and forecasting; the generated SMPL motions can also be executed by a Unitree humanoid controller. These results indicate a practical path from scalable egocentric observations to generalizable and interactive humanoid motion priors.

---

## 40. SIMPLE: Simulation-Based Policy Learning and Evaluation for Humanoid Loco-manipulation

**Authors:** Songlin Wei, Zhenhao Ni, Jie Liu, ..., Di Huang, Yue Wang
**arXiv:** [2606.08278](https://arxiv.org/abs/2606.08278)
**Categories:** Robotics (cs.RO)

Humanoid foundation models are advancing faster than we can evaluate them. While real-world testing is expensive and difficult to reproduce, existing simulation benchmarks focus primarily on table-top or wheeled robots. A scalable and reproducible benchmark for whole-body humanoid loco-manipulation remains an open problem. To this end, we present SIMPLE, a unified simulation testbed for humanoid policy learning and evaluation. SIMPLE couples the accurate contact-rich dynamics of MuJoCo with the photorealistic rendering of IsaacSim. It provides a large-scale environment comprising 60 diverse whole-body tasks, 50 indoor scenes, and over 1,000 object assets. To facilitate scalable data collection, the framework integrates two data generation pipelines: automated trajectory generation via motion planning and a low-latency VR teleoperation interface. We further integrate and benchmark mainstream humanoid policies at scale in SIMPLE, including lightweight imitation networks, large vision-language-action (VLA) models, and recent world action models (WAMs). Our experiments reveal a strong correlation between policy performance in simulation and the real world. Furthermore, we demonstrate that policies trained on data collected in SIMPLE can be transferred zero-shot to physical humanoid robots under similar settings, providing a robust and reproducible foundation for humanoid robotics research.

---
