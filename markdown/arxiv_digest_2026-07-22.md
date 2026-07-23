# arXiv Daily Digest — 2026-07-22

**Mode:** direct
**Categories:** cs.AI, cs.LG, cs.RO, cs.CV
**Keywords:** VLA, world model, world action model
**Papers found:** 9

---

## 1. DWM: Separating World Effects from Actions in Latent World Models

**Authors:** Yi-Ge Zhang, Tianqi Du, Qi Zhang, Yisen Wang
**arXiv:** [2607.18715](https://arxiv.org/abs/2607.18715)
**Categories:** Artificial Intelligence (cs.AI)

Latent world models underpin much of modern model-based control, yet current action-conditioned formulations supervise
the next-latent transition with a single, undifferentiated target, forcing a monolithic learning signal to absorb every
source of state change. In real world, however, transitions arise from two heterogeneous sources: an action-driven
component induced by the agent, and an action-invariant world effect -- the change that would still occur under a null
action, dictated by the environment's intrinsic dynamics (e.g., gravity-driven sliding, inertia, contact rebound, and
persistent drift). Fusing them into a single target entangles the two inside the latent transition, prevents the model
from attributing observed changes to their underlying causes, and undermines the transferability of the learned
dynamics. We introduce DWM (Decomposed World Model), a supervision-level framework that operationalizes this
decomposition. DWM augments the predictor of a latent world model with an auxiliary world head, regularized by a
normalized world-contrastive objective to be action-invariant, while the original pred head is coupled to it via an
orthogonality constraint; together, the two signals induce an explicit additive decomposition of the predicted
transition into an action-invariant and a complementary action-driven component, without altering the underlying
architecture or inference pipeline. To evaluate DWM under persistent world effects, we construct W-variants of three
standard control benchmarks -- PushT-W, Reacher-W, and TwoRoom-W -- each instantiating a distinct action-invariant
dynamic. DWM matches strong baselines on the flat counterparts and delivers a mean absolute improvement of 13.1% in CEM
planning success across the W-variants.

---

## 2. Do AI-Native Biotechs Need Departments? Benchmarking Company World Models for AI-Driven Drug Development

**Authors:** Yinan Wang
**arXiv:** [2607.18696](https://arxiv.org/abs/2607.18696)
**Categories:** Artificial Intelligence (cs.AI)

AI-native biotechnology companies are often designed by copying human biotech org charts into agent roles. We argue for a different abstraction: a Company World Model, defined as a persistent asset-to-value state representation with transition models, explicit value functions, planning, and updating across scientific, regulatory, BD, commercial, financial, and execution constraints. We introduce a dry-lab benchmark for testing whether AI-agent organizations should mimic departments or operate around such a world model. The benchmark contains 45 retrospective public-information decision cases with strict time cutoffs, hidden outcomes, common schemas, automatic scoring, and blinded pairwise judging. We compare human-org-mimic, stronger human-org-mimic-plus, AI-native asset-centric, and AI-native value-conversion architectures. The value-conversion architecture is a prompt-level approximation of a Company World Model: a Live Asset Value Record updated by Deal, Approval, Revenue, and Investment Arbiter loops. Under a success function defined by external BD, regulatory approval and launch, and revenue discipline, it achieved the highest automatic value-conversion score and was strongly preferred over the original baselines by value-specific blinded judges. Stress tests narrowed the claim: a stronger human baseline remained competitive, and a neutral judge did not show robust value-conversion dominance. Codex-only mechanistic ablations suggest that Revenue Room, Deal Room, and Approval Room carry useful work under the target objective. The central finding is objective-sensitive: departments may remain useful governance views, but the core AI-native operating primitive should be a shared, predictive asset-to-value state rather than a static human org chart. The study is dry-lab only and does not establish real-world drug success, clinical benefit, or revenue prediction accuracy.

---

## 3. AlayaWorld: Interactive Long-Horizon World Modeling -- Full Technical Report

**Authors:** AlayaWorld Team, Kaipeng Zhang, Chuanhao Li, ..., Zian Meng, Zihui Gao
**arXiv:** [2607.18367](https://arxiv.org/abs/2607.18367)
**Categories:** Artificial Intelligence (cs.AI)

Unlike conventional video game development, which relies on labor-intensive pipelines for asset production, animation, physics, and programming, video world models generate interactive environments from user inputs instantly. It enable us to create customized, explorable, and continuously evolving virtual world from text, an image, or video. Realizing this vision requires four tightly coupled capabilities: interaction, persistent spatiotemporal consistency, stable long-horizon generation, and efficient response. We present AlayaWorld, an interactive long-horizon video world model that generates 24-fps video at 540p and 720p. Built on a 15B video diffusion transformer, AlayaWorld generates short latent chunks autoregressively under camera trajectories and switchable text prompts. Its bounded visual context combines a persistent sink frame, compressed temporal history, geometry-aligned spatial memory, and recent-frame conditioning. To reduce long-term drift, the model is trained with corrupted histories and prediction residuals collected from its own roll-outs. We further introduce a discrete autoregressive distillation formulation that combines distribution-matching distillation, self-forcing++, and consistency distillation, reducing inference from approximately 30 sampling steps to four steps per chunk. On iWorld-Bench, AlayaWorld achieves the best performance over long-horizon generation. Conceived as a full-stack, open-source, and long-term project, AlayaWorld is intended to provide an extensible foundation for future research on interactive video world models.

---

## 4. Agentic Real2Sim: Physics-based World Modeling with Vision-Language Agents

**Authors:** Guanxiong Chen, Qianjun Xia, Jiawei Peng, ..., Chenfanfu Jiang, Peter Yichen Chen
**arXiv:** [2607.19190](https://arxiv.org/abs/2607.19190)
**Categories:** Robotics (cs.RO); Artificial Intelligence (cs.AI)

Real-to-sim conversion for robotic interaction with objects remains labor-intensive because it requires more than visual reconstruction: a streamlined real2sim process must recover scene geometries and object states, infer physical parameters, and assemble actors, objects, cameras, poses, and trajectories into a runnable physical simulation. Today this process still depends on manual tuning of visual foundation models, mesh cleanup, coordinate-frame alignment, and brittle workflow glue across visual perception tools and simulators. We introduce \textit{Agentic Real2Sim}, a framework for generalized physical world modeling with vision-language agents, converting a real-world recording of object-robot interaction into a simulatable episodic twin which preserves observations, geometries, robot interactions, and object states. We evaluate Agentic Real2Sim on rigid-object manipulation, deformable-object interaction, and humanoid motion scenes, spanning domains that are usually handled by separate Real2Sim pipelines, marking a first step toward scalable conversion. The framework's agentic decisions can be driven by an open-weight VLM backend at a small fraction of the cost of frontier models, while attaining comparable conversion success rate. We aim to use the resulting real-world-aligned twins for downstream robotics tasks, specifically policy learning and evaluation. The project site is available at this https URL.

---

## 5. FilmWorld: Agentic Novel-to-Film Generation through Dynamic Cinematic World Modeling

**Authors:** Jialong Zuo, Haotong Zuo, Shiwei Zhang, ..., Changxin Gao, Xiang Bai
**arXiv:** [2607.19038](https://arxiv.org/abs/2607.19038)
**Categories:** Computer Vision and Pattern Recognition (cs.CV); Artificial Intelligence (cs.AI)

Translating novels into films poses a grand challenge for generative artificial intelligence, requiring conversion of abstract literary prose into long-form, multi-scene visual narratives. While current video generation models excel at short, single-scene clips within narrow temporal and spatial contexts, novel-to-film generation operates in a more complex regime, demanding long-duration content across diverse scenes with dynamically evolving entity states. To address this, we formalize novel-to-film generation as dynamic cinematic world modeling, decomposed into two phases: construction, which grounds abstract, underspecified literary narratives into concrete, stateful, and persistent world entities; and evolution, which governs how these entities dynamically update under plot progression to maintain causal consistency across scenes. We propose FilmWorld, an end-to-end agentic system where two groups of specialized agents collaborate to instantiate these phases. Construction-side agents perform narrative structured translation, world entity state modeling with visual anchoring, and state-driven shot planning, progressively projecting literary language into a cinematic blueprint. Evolution-side agents perform state-anchored visual generation, cross-shot dynamic state propagation, and closed-loop state verification to maintain causal consistency and visual coherence. To address the evaluation gap in long-form generation, we introduce FilmEval, a systematic evaluation framework that couples a difficulty-graded benchmark of 15 representative novels with an automated protocol of nine objective metrics spanning three dimensions: cinematic presentation, film consistency, and novel fidelity. Experiments demonstrate that FilmWorld consistently outperforms state-of-the-art video generation agent systems, with particularly pronounced improvements in narrative fidelity and cross-scene consistency.

---

## 6. WorldScape Policy 2.0: Empowering Steerable World Action Modeling with Reasoning-Augmented Memory

**Authors:** Haisheng Su, Zongdai Liu, Xin Jin, ..., Yong Li, Wei Wu
**arXiv:** [2607.18840](https://arxiv.org/abs/2607.18840)
**Categories:** Robotics (cs.RO)

World Action Models (WAMs) offer a promising paradigm for robotic manipulation by jointly modeling visual state transitions and robot actions. However, existing WAMs are constrained by limited temporal context, coarse episode-level language supervision, and predominantly text-only conditioning, which hinder task-progress tracking and fine-grained language-video-action grounding while limiting visual-context reasoning and cross-embodiment transfer. In this paper, we introduce WorldScape Policy 2.0, a controllable WAM with reasoning-augmented long short-term memory. Its causal short-term visual memory supplies recent observations as DiT prefill to preserve local interaction dynamics, while its long short-term event memory organizes historical VLM outputs into global-history, local-active, and event-boundary representations for progress-aware retrieval. The retrieved history augments perception and autoregressively generated planning tokens, yielding an implicit subgoal condition for autonomous planning; semantic forcing further transfers event-level instruction semantics into this latent planning pathway. To establish fine-grained multimodal controllability, we construct ManipEvent-5M, an event-grounded embodied pretraining dataset containing nearly 5 million event segments with aligned action trajectories, episode-level task instructions, segment-level subtask captions, goal images, and video demonstrations. These designs provide a unified interface for autonomous planning from high-level instructions and controllable execution from fine-grained text, goal-image, or video-context prompts. Experiments in both simulation and real-world platforms demonstrate superior capabilities in long-horizon autonomous planning, fine-grained instruction following and in-context adaptation.

---

## 7. RoboInter1.5: A Holistic Intermediate Representation Suite for Embodied World Modeling and Robotic Manipulation

**Authors:** Ziqin Wang, Hao Li, Weijun Wang, ..., Jiangmiao Pang, Si Liu
**arXiv:** [2607.18709](https://arxiv.org/abs/2607.18709)
**Categories:** Robotics (cs.RO)

Existing robot datasets remain expensive to curate, embodiment-specific, and insufficiently annotated with the fine-grained structure required for generalizable reasoning, execution, or long-horizon environment dynamics simulation. Building on our prior work, RoboInter1.0, we present RoboInter1.5, an extended and holistic suite of intermediate representations for both robotic manipulation and embodied world modeling. RoboInter1.5 provides a unified resource of data, benchmarks, and models centered on dense manipulation-oriented intermediate representations. Specifically, RoboInter-Data contains over 230k manipulation episodes across 571 scenes with dense per-frame annotations covering more than ten types of intermediate representations, including subtasks, primitive skills, object and gripper grounding, segmentation, affordance, grasp poses, contact points, motion traces, etc. Built upon these annotations, RoboInter-VQA introduces spatial and temporal embodied VQA tasks to benchmark and improve the intermediate-representation reasoning capabilities of our RoboInter-VLM. RoboInter-VLA further studies how such representations benefit action execution through implicit, explicit, and modular plan-then-execute paradigms. To better model the physical world, we further introduce RoboInter-World, which leverages intermediate representations as structured conditioning signals for controllable prediction of future world states. Extensive evaluations demonstrate that RoboInter1.5 provides a unified spatiotemporal scaffolding for intermediate representations. Rather than treating intermediate representations merely as interpretable signals, RoboInter1.5 conceptualizes them as a bidirectional interface that both regularizes low-level action spaces and constrains the latent rollouts of open-world physical simulators.

---

## 8. Masked Visual Actions for Unified World Modeling

**Authors:** Hadi Alzayer, Wenlong Huang, Haonan Chen, ..., Jiajun Wu, Jia-Bin Huang
**arXiv:** [2607.19343](https://arxiv.org/abs/2607.19343)
**Categories:** Computer Vision and Pattern Recognition (cs.CV); Robotics (cs.RO)

Video models absorb rich priors over how the visual world moves, interacts, and responds to contact, making them promising substrates for robotic world modeling. The central challenge is how to communicate action to such models in a form aligned with the visual space in which they learned these interaction priors, yet still grounded in physical manipulation. We introduce Masked Visual Actions, a pixel-space control interface that expresses action as a partially revealed trajectory of an arbitrary entity in a video. Revealing robot motion makes the model act as a forward dynamics model that predicts the scene's response to low-level robot actions, while revealing desired object motion makes the same model recover robot behavior consistent with that outcome. Finetuned with only 15 hours of masked examples from real videos and simulation, a single checkpoint achieves strong visual fidelity and controllability across diverse scenes and multiple embodiments. In downstream manipulation settings, the model produces imagined rollouts whose outcomes correlate with real-world execution for policy evaluation, improves decision making by ranking candidate futures in model-based planning, and supports inverse modeling by synthesizing robot motion from desired object motion.

---

## 9. ABot-World-0: Infinite Interactive World Rollout on a Single Desktop GPU

**Authors:** Fan Jiang, Zhaoxu Sun, Mengchao Wang, ..., Mu Xu, Ning Guo
**arXiv:** [2607.19191](https://arxiv.org/abs/2607.19191)
**Categories:** Computer Vision and Pattern Recognition (cs.CV); Artificial Intelligence (cs.AI); Machine Learning (cs.LG)

We present ABot-World-0, an action-conditioned video world model for real-time, long-horizon closed-loop interaction, supported by a multi-source data infrastructure spanning AAA games, simulation engines, and internet videos to learn controllable world dynamics. WorldExplorer performs agent-driven collection guided by training feedback, while a unified pipeline applies 14 deterministic quality checks, VLM-based assessment, and synchronized action and text annotation. We progressively distill a bidirectional action-conditioned teacher into a causal student through teacher forcing and ODE distillation, and introduce LongForcing to align long student self-rollouts with an extended-horizon teacher, mitigating accumulated distribution shift and autoregressive drift. Raw keyboard actions provide a unified control interface for scene roaming and third-person character interaction, while reference-character memory provides persistent appearance cues for identity consistency during third-person rollouts. For deployment, we co-design a streaming inference stack with a lightweight VAE decoder, efficient attention, memory-aware scheduling, and low-bit DiT inference. Across optimized low-bit configurations, ABot-World-0 streams 720P video at up to 16 FPS on a single NVIDIA RTX 5090 desktop GPU, with 1.2s action-to-first-frame latency and approximately 19GiB peak VRAM. Experiments on WorldRoamBench and extended interactive rollouts demonstrate competitive controllability and coherent long-horizon world evolution.

---
