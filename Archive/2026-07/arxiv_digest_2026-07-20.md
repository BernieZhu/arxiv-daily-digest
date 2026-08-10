# arXiv Daily Digest — 2026-07-20

**Mode:** direct
**Categories:** cs.AI, cs.LG, cs.RO, cs.CV
**Keywords:** VLA, world model, world action model
**Papers found:** 8

---

## 1. DSWorld: A Data Science World Model for Efficient Autonomous Agents

**Authors:** Zherui Yang, Fan Liu, Hao Liu
**arXiv:** [2607.15901](https://arxiv.org/abs/2607.15901)
**Categories:** Artificial Intelligence (cs.AI)

Despite strong capabilities in data understanding and decision-making, autonomous data science agents still heavily rely on trial-and-error workflows that involve expensive computation. This bottleneck motivates models that can anticipate the effects of data science operations before real execution. In this paper, we introduce the concept of Data Science World Model, which model the data science execution environment by predicting environment state transitions conditioned on current workflow states and candidate operations. We further propose DSWorld, a practical framework that combines structured state construction, cost-aware routing, lightweight real execution, and an LLM-based simulator for expensive operations. To support training, we construct an 8K-scale transition trajectory dataset and introduce Reflective World Model Optimization, an error-aware reinforcement learning strategy for improving transition prediction. Experiments show that DSWorld accelerates RL-based agent training by approximately $14\times$ and search-based inference by approximately $3$-$6\times$ while maintaining competitive performance, and outperforms the strongest LLM baseline by 35.6% on transition prediction tasks. The code is available at this https URL.

---

## 2. SeerGuard: A Safety Framework for Mobile GUI Agents via World Model Prediction

**Authors:** Xue Yu, Bo Yuan, Pengshuai Yang, ..., Hong Hu, Junlan Feng
**arXiv:** [2607.15550](https://arxiv.org/abs/2607.15550)
**Categories:** Artificial Intelligence (cs.AI)

Mobile graphical user interface (GUI) agents have demonstrated remarkable capabilities in automating complex tasks, yet they introduce critical safety risks where a single erroneous action can lead to irreversible consequences. Existing safety mechanisms are primarily reactive, lacking the ability to assess risks before execution. In this paper, we introduce SeerGuard, a consequence-aware safety framework designed to mitigate these risks through pre-execution instruction-level screening and action-level risk assessment. Specifically, the action-level assessment analyzes agent-proposed actions within current GUI states, anticipating likely outcomes to identify risks before they are executed. To enable these capabilities, we construct a unified safety-augmented world model (SAWM) via multi-task learning, integrating semantic next-state prediction with safety risk assessment. Extensive experiments demonstrate that SeerGuard generalizes effectively across diverse mobile GUI agents. On Qwen3-VL-8B-Instruct, it increases the safety-utility score from $0.191$ to $0.596$ at $\omega=0.8$ and reduces the risk-cost score from $0.347$ to $0.130$ at $\alpha=0.8$. Further analyses on our SAWM validate the effectiveness of the instruction-level screening, alongside the capability of action risk assessment and next-state prediction.

---

## 3. Do Coding Agents Need Executable World Models, Simplification, and Verification to Solve ARC-AGI-3?

**Authors:** Sergey Rodionov
**arXiv:** [2607.15439](https://arxiv.org/abs/2607.15439)
**Categories:** Artificial Intelligence (cs.AI)

Our previous ARC-AGI-3 agent bundled executable world modeling, scheduled simplification, and exact replay verification, leaving unclear which idea accounted for its performance. We address this attribution question with four nested Codex-based agents: a textual baseline; a flexible-interface executable world model without replay verification; the same executable model with scheduled simplification; and a fixed-interface verification treatment that retains simplification and requires exact reproduction of recorded observations. The main study evaluates all four agents with gpt-5.4 and gpt-5.5 at high and xhigh reasoning effort on the public ARC-AGI-3 games. Exploratory follow-ups evaluate the textual and verification variants with gpt-5.6-sol at xhigh and max. The most robust result is that every agent variant improves with a stronger model and with greater reasoning effort. Within each model-effort setting, differences among variants are smaller than anticipated, while the effects of individual components vary across settings. Requiring a persistent executable deliverable is not universally beneficial: the textual variant outperforms the flexible-interface executable variant in both gpt-5.5 settings. Simplification improves performance in three of the four model-effort settings, with the weakest setting as the only exception. The complete verification treatment ranks first in all four settings, although it uses substantially more resources. In the gpt-5.6-sol follow-up, the verification variant fully solves every public game at both reasoning efforts, achieves about 99% RHAE, and uses fewer than half the total actions of the human baseline. Because the model postdates these games and held-out performance remains untested, this result should be interpreted as saturation of the public set only.

---

## 4. JoyNexus: Service-Oriented Multi-Tenant Post-Training for VLA Models

**Authors:** Haoran Sun, Wentao Zhang, Junyang Hua, ..., Yicheng Gong, Junwu Xiong
**arXiv:** [2607.16074](https://arxiv.org/abs/2607.16074)
**Categories:** Distributed, Parallel, and Cluster Computing (cs.DC); Artificial Intelligence (cs.AI); Software Engineering (cs.SE)

The post-training of Vision-Language-Action (VLA) models is essential due to the diversity of simulators, robot embodiments, and task objectives. Existing compute services, whether offered as direct accelerator rental or batch-workload submission, typically allocate an exclusive set of GPU and CPU resources to a single tenant. While this paradigm maximizes client flexibility, it burdens users with infrastructure adaptation, and the fixed card-hour accounting model renders short or bursty workloads both expensive for tenants and inefficient for the service provider. To address these challenges, we present JoyNexus, a unified service for multi-tenant VLA supervised fine-tuning, reinforcement learning, and evaluation. JoyNexus decouples the Training Model Service, Inference Model Service, and Environment Service, each accessed through APIs and backed by resident shared base models with tenant-specific slots. Tenants can directly invoke high-level semantic APIs for training, rollout, and evaluation, or compose custom algorithms using lower-level APIs and their assigned endpoints. Multiple tenants submit workloads concurrently; their action modules, optimizers, rollout records, and policy versions remain isolated, and the service is scheduled by the global Training Queue and Inference Queue. To further improve multi-tenant training efficiency, JoyNexus introduces group batching for heterogeneous VLA data schemas that share a compatible model-facing prefix, enabling a single shared backbone forward pass over grouped samples. Finally, we evaluate JoyNexus through workload simulation and a group-batching pipeline in a realistic embodied scenario. Results show that, compared with isolated single-tenant execution, JoyNexus reduces aggregate GPU time and improves service utilization via cross-tenant scheduling on shared resources.

---

## 5. Orbis 2: A Hierarchical World Model for Driving

**Authors:** Sudhanshu Mittal, Arian Mousakhan, Silvio Galesso, ..., Rajat Sahay, Thomas Brox
**arXiv:** [2607.15898](https://arxiv.org/abs/2607.15898)
**Categories:** Computer Vision and Pattern Recognition (cs.CV); Artificial Intelligence (cs.AI); Machine Learning (cs.LG); Robotics (cs.RO)

Current world models operate at a single level of abstraction, with most prioritizing perceptual fidelity while lacking the spatial reasoning and semantic understanding required for real-world downstream tasks. We present a hierarchical driving world model that factorizes future prediction across two levels operating at distinct temporal and abstraction scales: a high-level predictor that forecasts coarse scene structure over extended temporal horizons, and a low-level generator that produces detailed predictions conditioned on the high-level output. This decomposition yields high perceptual fidelity while also capturing strong spatial and semantic representations. We further show that pretraining with a diffusion forcing objective yields substantially richer internal representations than the standard teacher forcing objective, while teacher forcing -- predicting only the next frame from clean context -- produces more stable autoregressive rollouts. We therefore introduce a generic two-stage training paradigm that pretrains the model with diffusion forcing and fine-tunes with teacher forcing, combining the representational benefits of the former with the rollout stability of the latter. Our approach achieves state-of-the-art results across the standard suite of driving world model evaluations on established benchmarks, including long-horizon generation fidelity, steering responsiveness evaluated on counterfactual scenarios, and internal representation quality. Project page with code, demo, checkpoints and qualitative results: this https URL

---

## 6. Think at 5 Hz, Act at 20 Hz: Asynchronous Fast-Slow Vision-Language-Action Inference for Closed-Loop Driving

**Authors:** Yun Li, Jiachen Gong, Simon Thompson, ..., Zixuan Guo, Manabu Tsukada
**arXiv:** [2607.15621](https://arxiv.org/abs/2607.15621)
**Categories:** Robotics (cs.RO); Artificial Intelligence (cs.AI)

Large language models bring instruction following and scene reasoning to end-to-end driving, but their inference latency collides with the control rate a vehicle requires. Existing closed-loop agents hide this gap by invoking the model on alternate simulation ticks and replaying the previous command in between, so half of all control outputs ignore the newest observations. We present a fast-slow architecture that removes this compromise. A frozen 7B vision-language backbone acts as the slow system, digesting navigation instructions and visual history at low frequency while exposing its per-layer key-value cache as a standing representation of the scene. A lightweight action expert acts as the fast system, attending to this cache and to the current camera frame at every simulation tick to regress waypoints in a single forward pass. Since the cache lags behind the world at deployment, we train the expert under randomized staleness, aligning training with asynchronous execution. On LangAuto-Short routes in CARLA, our system produces fresh control at every 50 ms simulation tick and lifts route completion from 37.0 to 94.0 over the frame-skipping baseline. A frame-skip ablation with the same expert separates the two factors at work: the expert raises the driving score on its own, while per-tick freshness raises completion from 82.1 to 94.0 and cuts red-light violations by a third. Trained on a single town, the expert transfers zero-shot to two unseen towns, holding 84-94% route completion where the baseline reaches 31-41%. It reduces open-loop waypoint error by nearly a factor of four compared to the backbone's own action head, at a per-tick model cost of 32 ms that is independent of history length on a single consumer GPU.

---

## 7. AC-VLA: Robust Out-of-Distribution Action Execution via Compositional Learning

**Authors:** Xiaojiang Peng, Kai Peng, Jie Lu, ..., Zitong YU, Xiaobo Wang
**arXiv:** [2607.15714](https://arxiv.org/abs/2607.15714)
**Categories:** Robotics (cs.RO)

Vision-Language-Action (VLA) models excel at end-to-end robotic manipulation but struggle with out-of-distribution (OOD) generalization when familiar sub-tasks are recombined in unseen configurations. We identify two mutually reinforcing failure modes: \emph{trajectory overfitting}, where models overfit to holistic trajectory patterns rather than compositional sub-skill semantics; and \emph{perceptual shortcut}, where action tokens over-rely on wrist-view textures at the expense of global spatial grounding. To address both, we introduce \textbf{AC-VLA}, a plug-and-play Action Compositional learning framework comprising two architecture-agnostic components: \textbf{(i)} a compositional learning module that uses an LLM-driven instruction decomposer and a proprioceptive trajectory aligner to generate dense sub-task supervision, followed by mixed training on complete demonstrations and decomposed data to endow the model with compositional generalization; and \textbf{(ii)} a state-conditioned asymmetric masking strategy that suppresses wrist-view inputs during closed-gripper phases, enforcing global semantic grounding. All components are architectural modification-free and directly integrable into any VLA backbone. Instantiated on $\pi_{0.5}$ and evaluated on LIBERO and LIBERO-OOD benchmarks, AC-VLA achieves a ~28% absolute improvement on compositional OOD tasks while maintaining near-perfect in-distribution performance.

---

## 8. Xiaomi-Robotics-1: Scaling Vision-Language-Action Models with over 100K Hours of Real-World Trajectories

**Authors:** Xiaomi Robotics Team, Jun Guo, Piaopiao Jin, ..., Han Zhao, Quanyun Zhou
**arXiv:** [2607.15330](https://arxiv.org/abs/2607.15330)
**Categories:** Robotics (cs.RO); Computer Vision and Pattern Recognition (cs.CV)

We present Xiaomi-Robotics-1, a foundational vision-language-action (VLA) model capable of (1) following diverse language instructions to perform a wide range of mobile manipulation tasks in unseen environments out-of-the-box, and (2) efficiently adapting to novel downstream tasks with minimal fine-tuning data. We propose a two-stage training recipe consisting of pre-training and post-training. During pre-training, we imbue the model with broad and generalizable action-generation capabilities by training on over 100k hours of real-world manipulation trajectories collected via UMI devices. Crucially, we develop a scalable auto-labeling pipeline that annotates trajectory clips with natural languages describing scene state transitions, providing rich and precise conditioning for action learning. During post-training, we aim to align these capabilities with robot embodiments and imperative instructions that humans naturally use to prompt robots. Extensive experiments demonstrate strong scaling behavior. Xiaomi-Robotics-1 consistently improves with increased data scales and model sizes during pre-training. This scaling behavior directly transfers to post-training, where a stronger pre-training model yields better out-of-the-box real-robot performance in unseen environments. Furthermore, Xiaomi-Robotics-1 serves as a strong robot foundation policy that can be efficiently fine-tuned on complex, dexterous tasks with high data efficiency. Across multiple simulation benchmarks, Xiaomi-Robotics-1 outperforms state-of-the-art methods. Notably, it establishes a new state-of-the-art with a 57.6% success rate on RoboCasa365, surpassing the previous best of 46.6%. Furthermore, it achieves an average score of 20.07 on RoboDojo, significantly outperforming the prior state-of-the-art (13.07). Code and model checkpoints will be released. Project page: this https URL

---
