# arXiv Daily Digest — 2026-07-02

**Mode:** direct
**Categories:** cs.AI, cs.LG, cs.RO, cs.CV
**Keywords:** VLA, world model, world action model
**Papers found:** 14

---

## 1. AGI Maze as a Benchmark Framework for World-Modeling Agents

**Authors:** Alexey Potapov
**arXiv:** [2607.00627](https://arxiv.org/abs/2607.00627)
**Categories:** Artificial Intelligence (cs.AI)

Large language models (LLMs) are powerful pattern-completion systems, but their default operating mode - predicting the next token from a static context - does not reliably produce persistent, manipulable representations of an external world. Many tasks that look like "reasoning" in text become substantially harder once the environment is partially observable, stateful, and requires memory and structured hypotheses about hidden state. AGI Maze is a lightweight framework for building such environments without requiring high-dimensional sensory inputs. It provides a family of grid-based maze tasks with a clean API and multiple difficulty regimes. The goal is to create benchmarks where agents must learn and use world state representations, not just infer a local rule over readily provided observations. We provide an initial evaluation of several vanilla LLMs on simple mazes showing that they fail to represent mazes internally at LLM inference time. We also introduce a baseline agent, which is allowed to use its message history as a working memory to construct descriptions of observations at agentic runtime. Although this can improve performance, it is still insufficient for an LLM agent to reliably solve even small mazes within a step budget that is more than enough for humans.

---

## 2. Multi-scale Mixture of World Models for Embodied Agents in Evolving Environments

**Authors:** Jinwoo Jang, Daniel J. Rho, Sihyung Yoon, Hyunsuk Cho, Honguk Woo
**arXiv:** [2607.00457](https://arxiv.org/abs/2607.00457)
**Categories:** Artificial Intelligence (cs.AI)

Embodied agents operating in the real world require multi-scale reasoning and knowledge adaptation as conditions change. We identify two challenges in applying Mixture of Experts (MoE) to this setting: routing lacks an explicit notion of scale, preventing targeted updates at specific scales, and a uniform update policy cannot accommodate the different rates at which knowledge at each scale becomes outdated. We present MuSix, a framework that addresses both challenges through scale-aware world model mixture and evolution. A two-stage routing mechanism grounds scale selection in experiential distance, a measure of situational novelty inspired by Construal Level Theory: a meta-router first maps this quantity to a weight over continuous scale space, then per-scale base routers select world models within the identified scale. For adaptation, scale-dependent forgetting rates allow low-scale knowledge to refresh rapidly while high-scale abstractions persist, and gated inter-scale transfer maintains coherence across the hierarchy. Experiments on EmbodiedBench and HAZARD show that MuSix improves over state-of-the-art baselines on multi-scale reasoning and dynamic adaptation.

---

## 3. FurnitureVLA: Learning Long-Horizon Bimanual Furniture Assembly with Vision-Language-Action Model

**Authors:** Chenyang Ma, Yue Yang, Radu Corcodel, ..., Chiori Hori, Diego Romeres
**arXiv:** [2607.01212](https://arxiv.org/abs/2607.01212)
**Categories:** Robotics (cs.RO); Artificial Intelligence (cs.AI)

Current work on robot furniture assembly mostly focuses on toy-scale settings or single-arm manipulation. We introduce FurnitureVLA, the first systematic study of real-scale bimanual furniture assembly using Vision-Language-Action models (VLAs). We formalize the task, develop a scalable simulation pipeline for expert data generation and evaluation, and build a VR teleoperation system for single-operator bimanual control to collect high-quality real-world demonstrations. To address extreme long-horizon assembly with up to 7 subtasks and 1550 control steps, we propose a progress-enhanced VLA, finetuned on semantically grounded subtasks, that jointly predicts actions and a continuous progress signal, enabling automatic subtask transitions and reducing compounding errors during inference. We further study perception and control design factors that critically affect precision in real-scale assembly. FurnitureVLA improves average simulation success from 48% to 80% compared to baselines across three furniture types, with an additional 21% gain from our design factor study. We validate on a real Kinova Gen3 platform with only 16% drop on the hardest task.

---

## 4. Valdi: Value Diffusion World Models

**Authors:** Christopher Lindenberg, Kashyap Chitta
**arXiv:** [2607.00917](https://arxiv.org/abs/2607.00917)
**Categories:** Machine Learning (cs.LG); Artificial Intelligence (cs.AI)

World models can enable Model Predictive Control (MPC), but this requires dynamics prediction that is both fast enough for online use and expressive enough to represent uncertain futures. Diffusion models offer a natural mechanism for modeling uncertain dynamics, yet their iterative inference procedure makes them difficult to use for low-latency latent planning. We bridge this gap with Value Diffusion World Models (Valdi), combining end-to-end online training for MPC with a latent diffusion dynamics model. In preliminary experiments on the CarRacing environment, we show that Valdi, using a single diffusion step at both training and inference, matches a deterministic MLP baseline. Our experiments expose a trade-off between predictive multimodality and control performance in this setup. Code is available at this https URL.

---

## 5. DeWorldSG: Depth-Aware 3D Semantic Scene Graph Generation via World-Model Priors

**Authors:** Seok-Young Kim, Abdelrahman Elskhawy, Taewook Ha, ..., Benjamin Busam, Woontack Woo
**arXiv:** [2607.00889](https://arxiv.org/abs/2607.00889)
**Categories:** Computer Vision and Pattern Recognition (cs.CV); Artificial Intelligence (cs.AI)

We present DeWorldSG, a novel framework that generates spatio-temporally robust 3D Semantic Scene Graphs from RGB-D sequences. Existing methods often struggle to construct reliable 3D scene graphs due to unstable 3D object representations and missing relations caused by frame-wise inference. DeWorldSG addresses these issues by estimating instance-level geometric 3D Gaussian distributions through depth-guided filtering and representing each object as a probabilistic 3D node rather than a single projected point. To mitigate relational sparsity from frame-wise inference, our framework further aggregates spatiotemporal evidence across object pairs and refines relations using contextual priors derived from a world model (V-JEPA 2). Experiments on the 3DSSG and ReplicaSSG datasets demonstrate state-of-the-art (SoTA) performance in both object and predicate prediction, while producing temporally consistent scene structures. In particular, our method improves triplet recall by 77.4% and predicate recall by 23.2% over prior SoTA approaches, making it suitable for robotic manipulation and AR applications. Our code and models are open-sourced.

---

## 6. From World Models to World Action Models: A Concise Tutorial for Robotics

**Authors:** Xiaoxiong Zhang, Xiong Zeng, Wei Zhang
**arXiv:** [2607.00836](https://arxiv.org/abs/2607.00836)
**Categories:** Robotics (cs.RO); Artificial Intelligence (cs.AI); Systems and Control (eess.SY)

World models are increasingly used in embodied intelligence and generative simulation, yet their scope remains ambiguous across communities. This tutorial presents a design-space view of world models as action-conditioned predictive models that estimate the future evolution of task-relevant observations or states. We categorize existing methods into observation-space and state-space world models, comparing their trade-offs in visual fidelity, spatial structure, physical interpretability, and control usability. We further introduce world action models, which connect predicted futures with executable robot actions, and summarize four representative paradigms: imagine-then-execute, video-feature-conditioned action prediction, joint video-action modeling, and auxiliary video prediction for policy learning. The goal of this tutorial is to clarify the conceptual scope of world (action) models and provide a structured taxonomy for embodied prediction and control.

---

## 7. RetailSMV: Exocentric vs. Egocentric Adaptation of Foundation Video World Models in Retail

**Authors:** Amirreza Rouhi, Rajat Aggarwal, Parikshit Sakurikar, Anoop M. Namboodiri, Sashi P. Reddi
**arXiv:** [2607.00310](https://arxiv.org/abs/2607.00310)
**Categories:** Computer Vision and Pattern Recognition (cs.CV); Artificial Intelligence (cs.AI)

Foundation video diffusion models are increasingly viewed as world simulators for embodied agents, yet their pretraining on internet-scale generic video leaves them poorly aligned with real-world deployment domains. We study parameter-efficient adaptation of a pretrained foundation video world model to retail scenes: when synchronized egocentric and exocentric video of the same activity are available, which viewpoint of training data produces the strongest adapted model?
We introduce RetailSMV (Retail Synchronized Multi-View), a corpus of 32,105 captioned retail clips from five supermarkets with synchronized ego/exo capture from the store-staff perspective (stocking, arranging, weighing, managing supply carts, scanning at checkout), rather than the customer-centric framing of prior retail video corpora, and train three matched Low-Rank Adaptation (LoRA) configurations of Cosmos3-Nano (egocentric-only, exocentric-only, combined) under identical hyperparameters. On a 200-clip held-out test set evaluated with seven complementary metrics under a strict paired statistical protocol, exocentric-only adaptation matches or exceeds combined adaptation on six of seven point estimates and is significantly better on LPIPS, PSNR, and DreamSim, despite training on only 15,985 exocentric clips (versus 32,105 for combined). A symmetric paired comparison further shows that adding exocentric data to egocentric-only training helps while adding egocentric data to exocentric-only training hurts. The absolute adaptation gap is largest at the shortest rollout time, identifying the near-horizon prediction window as the regime in which adaptation is most beneficial.

---

## 8. Domain Arithmetic: One-Shot VLA Adaptation under Environmental Shifts

**Authors:** Taewook Kang, Taeheon Kim, Donghyun Shin, Jonghyun Choi
**arXiv:** [2607.00666](https://arxiv.org/abs/2607.00666)
**Categories:** Robotics (cs.RO); Computer Vision and Pattern Recognition (cs.CV); Machine Learning (cs.LG)

Vision-Language-Action (VLA) models often fail to perform the same learned tasks under environmental shifts, such as changes in camera pose and shifts to a different but similar robot (e.g., from Panda to UR5e). Adapting these models to the shifted environment (i.e., target domain) often requires training on multiple demonstrations for each task, which are costly to collect. To reduce the burden of data curation and training, we propose an analogy-based method that adapts VLA models under environmental shifts through weight vector arithmetic with domain-specific information addition, named Domain ARiThmetic (DART). Unlike prior approaches, DART requires collecting only a single demonstration, enabling efficient adaptation. To accurately isolate domain-specific information for addition, DART performs subspace alignment between singular components in weight vectors to filter out noisy components. In both simulated and real-world experiments, DART outperforms existing VLA adaptation methods in one-shot scenarios across diverse visual and embodiment shifts. Code is available at this https URL.

---

## 9. Path Planning in Physically Viable World Models

**Authors:** Su Ann Low, Cheng-Hsi Hsiao, Xingjian Li, ..., Ufuk Topcu, Krishna Kumar
**arXiv:** [2607.00673](https://arxiv.org/abs/2607.00673)
**Categories:** Robotics (cs.RO)

Robots deployed in unstructured outdoor environments often plan from scene reconstructions collected before deployment because operators cannot remap large or remote sites before every mission. As a result, robots must make long-horizon planning decisions using stale maps that assume the terrain remains unchanged, even though physical changes to the environment may render previously feasible routes unsafe or unreachable at execution time. We present a physically viable world model for evaluating what-if queries for robot navigation under future terrain change. The system augments reconstructed 3D Gaussian splat scenes with physics-based simulation to generate physically modified versions of the same environment without recollecting sensor data or rebuilding the map. We then implement a terrain-aware planner that accounts for physical events, obstacles, and deformations that are simulated by the world model. This allows robots and human operators to evaluate whether planned routes remain feasible before committing to a planned route, particularly in constrained environments where retreat or recovery may become impossible once conditions change. We evaluate the system on a real outdoor field site in Central Texas using simulated flooding across multiple severity levels. We measure route and mission feasibility as terrain conditions deteriorate under physically simulated interventions. Our results show that physically viable world models expose long-horizon route failures and rerouting behavior that are not apparent when planning only on the original reconstructed environment, allowing robots to evaluate how future terrain changes may affect route feasibility before deployment.

---

## 10. Unleashing More Actions via Action Compositional Training for VLA Models

**Authors:** Kai Peng, Jie Lu, Xiaojiang Peng
**arXiv:** [2607.00351](https://arxiv.org/abs/2607.00351)
**Categories:** Robotics (cs.RO)

Vision-Language-Action models excel at robotic manipulation, driven by the scale and diversity of demonstration data. However, standard training paradigms often cause VLA models to severely overfit to specific behavioral patterns, rendering them unable to generalize to out-of-distribution scenarios even when those scenarios merely require novel combinations of identical sub-skills. While expanding datasets can mitigate this overfitting, acquiring high-quality robot data remains notoriously labor-intensive and cost-prohibitive. To resolve this impasse without expensive human teleoperation and to truly unleash more actions,i.e., enable VLA models to compose known sub-skills into a much broader set of executable behaviors beyond the original demonstrations-we propose ACT-VLA (Action Compositional Training for VLA Models), an offline data augmentation framework that leverages the model's latent task representations to synthesize novel, physically valid demonstrations directly from existing tasks for policy training. By eliminating additional manual data collection, our method automatically expands the training distribution and mitigates overfitting. We evaluate our approach on challenging manipulation tasks in simulation. Experiments demonstrate that while baseline VLA models generalize poorly due to original distribution overfitting, policies trained with our synthesized data achieve substantially higher success rates, validating that leveraging existing tasks for automated demonstration synthesis provides an effective, scalable, and data-efficient route to broadening VLA generalization.

---

## 11. 3D Point World Models: Point Completion Enables More Accurate Dynamics Learning

**Authors:** Skand Peri, Hung Nguyen, Chanho Kim, Li Fuxin, Stefan Lee
**arXiv:** [2607.00148](https://arxiv.org/abs/2607.00148)
**Categories:** Robotics (cs.RO); Computer Vision and Pattern Recognition (cs.CV)

Learning predictive models of the world enables robotic control through planning, potentially allowing robots to improvise solutions on new tasks. However, large video-based dynamics models lack explicit 3D spatial structure and suffer from geometrically inconsistent long-term rollouts with compounding errors. Emerging 3D dynamics models based on partial point clouds improve geometric consistency but remain sensitive to occlusions and accumulated prediction drift. To address these challenges, we present 3D Point World Models (3DPWM) - a task-agnostic world model that operates entirely in 3D space by first completing partial point clouds and then learning action-conditioned dynamics in this completed 3D scene. By operating on completed geometry, 3DPWM enables reliable long-horizon rollouts and more accurate cost evaluation for model-based planning while supporting adaptation to new tasks. Experiments across different robotic embodiments and tabletop manipulation benchmarks demonstrate that 3DPWM achieves significantly more reliable long-horizon rollouts (100-300+ steps), supports both open-loop and closed-loop planning, and enables successful sim-to-real transfer.

---

## 12. ABot-M0.5: Unified Mobility-and-Manipulation World Action Model

**Authors:** Ronghan Chen, Yandan Yang, Zuojin Tang, ..., Zhiheng Ma, Xinyuan Chang
**arXiv:** [2607.00678](https://arxiv.org/abs/2607.00678)
**Categories:** Computer Vision and Pattern Recognition (cs.CV); Robotics (cs.RO)

Mobile manipulation is a key capability for general-purpose robots, yet remains challenging for current embodied learning methods. VLA policies are typically reactive and lack explicit world modeling, while existing World Action Models (WAMs) are still poorly aligned with the structure of mobile manipulation: they operate on coarse video chunks, model entangled navigation-manipulation actions, and train inverse dynamics under supervision that does not match autoregressive inference. As a result, they often miss fine-grained contact dynamics, suffer from action-distribution conflicts, and accumulate errors over long-horizon rollouts. We propose ABot-M0.5, a new WAM built on the insight that mobile manipulation requires alignment at three levels: temporal granularity, action space, and train-test consistency. To align temporal granularity, we introduce intermediate latent actions that capture local visual state transitions and serve as an bridging action space between video latents and embodiment-specific controls. To align action space, we design a dual-level Mixture-of-Transformers architecture that disentangles both modality representations and heterogeneous action subspaces such as base movement and arm manipulation. To align inference conditions, we propose the dream-forcing training strategy that progressively trains inverse dynamics on model-predicted videos, improving train-test alignment and robustness during autoregressive prediction. Experiments on challenging mobile and fine-grained manipulation benchmarks demonstrate that ABot-M0.5 achieves state-of-the-art performance in both long-horizon task success and finegrained control accuracy. These results highlight the critical importance of granularity-aligned, action-disentangled, and inference-consistent world-action modeling.

---

## 13. RoboWorld: Fast and Reliable Neural Simulators for Generalist Robot Policy Evaluation

**Authors:** Byeongguk Jeon, Seonghyeon Ye, JaeHyeok Doo, ..., Hyungmok Son, Kimin Lee
**arXiv:** [2607.01060](https://arxiv.org/abs/2607.01060)
**Categories:** Robotics (cs.RO)

Video world models are emerging as a scalable alternative for evaluating generalist robot policies, bypassing the physical constraints and engineering burdens of real-world deployment. However, evaluating policies with video world models remains challenging, as world-model errors can make generated rollouts unreliable and slow inference limits large-scale throughput. We introduce RoboWorld, an automated evaluation pipeline that pairs a fast autoregressive video world model with a task-progress-aware vision-language model scoring. To enable reliable long-horizon autoregressive world-model rollouts, we propose Step Forcing, which combines anchored and one-step self-forwarded contexts to reduce train--test mismatch while preserving action--observation dynamics. Together, these components enable RoboWorld to align strongly with real-world robot evaluation across tasks and environments, achieving Pearson's r = 0.989 and Spearman's \r{ho} = 0.970.

---

## 14. EmbodimentSemantic: A Spatial Scene-Graph Dataset and Benchmark for Vision-Language Models on Embodied Manipulation Trajectories

**Authors:** Hassan Jaber, Refinath S N, Luca Cagliero, Christopher E. Mower, Haitham Bou-Ammar
**arXiv:** [2607.00020](https://arxiv.org/abs/2607.00020)
**Categories:** Robotics (cs.RO)

Spatial grounding remains a key limitation of vision-language-action (VLA) systems for robotic manipulation. While current models can recognize objects and follow language instructions, they often lack an explicit representation of how objects are arranged in space, including support, containment, ordering, occlusion, and depth-sensitive relations. We introduce EmbodimentSemantic, a spatial scene-graph dataset and benchmark for evaluating relational grounding in embodied manipulation. EmbodimentSemantic represents scenes as directed object-relation-object triplets, where each triplet specifies a spatial relation between an ordered pair of objects using a fixed set of relations. This representation enables direct evaluation of object binding, relation prediction, and spatial consistency. The dataset includes real-world manipulation observations collected with the low-cost SO101 robot arm, together with generated scene graphs for studying spatial grounding in practical robotic settings. To provide controlled validation, we also introduce a simulator-grounded LIBERO benchmark with over 60K manipulation frames and more than 120K camera-specific scene graphs across paired third-person and wrist views, where ground-truth relations are derived automatically from MuJoCo geometry, world coordinates, camera projections, and visibility constraints. We further test whether scene graphs improve downstream control by injecting them into existing VLA policy prompts. Experiments across open-source and commercial VLMs show that current models often predict plausible relations but struggle with exact depth-aware and viewpoint-dependent spatial structure. EmbodimentSemantic provides a unified framework for diagnosing spatial grounding in VLM perception and testing its utility for VLA manipulation.

---
