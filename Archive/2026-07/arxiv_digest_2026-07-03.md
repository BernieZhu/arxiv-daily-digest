# arXiv Daily Digest — 2026-07-03

**Mode:** direct
**Categories:** cs.AI, cs.LG, cs.RO, cs.CV
**Keywords:** VLA, world model, world action model
**Papers found:** 20

---

## 1. Repair the Amplifier, Not the Symptom: Stable World-Model Correction for Agent Rollouts

**Authors:** Xinyuan Song, Zekun Cai
**arXiv:** [2607.01767](https://arxiv.org/abs/2607.01767)
**Categories:** Artificial Intelligence (cs.AI)

As agent planning moves from short tool chains toward persistent workflows with thousands or tens of thousands of steps, failures will occur inside large planning graphs rather than in isolated predictions. Replanning the entire graph after every mistake is neither computationally realistic nor desirable: full-graph replay consumes large context budgets, exposes the LLM to many irrelevant symptoms, and can degrade long-context retrieval. This paper studies the missing component in such systems: a world-model corrector that repairs the failed planning graph in place. We compare two families of correctors. The first is the common engineering approach: scan nodes and edges, choose a suspicious local region, and ask an LLM to repair it. We implement strong engineering LLM correctors and find that they can help, especially when given very large contexts. The second family is our approach, WM-SAR (World-Model Subgraph Amplification Repair): instead of scanning for visible symptoms, it works backward from subgraph amplification, identifies the nodes and edges that keep re-amplifying error, and sends only that causal subgraph to the LLM. Across graph simulations and LLM repair experiments, WM-SAR substantially outperforms engineering correctors under realistic token budgets, achieves near-whole-graph stabilization with a compact region, and gives the LLM a cleaner repair target.

---

## 2. Safe and Adaptive Cloud Healing: Verifying LLM-Generated Recovery Plans with a Neural-Symbolic World Model

**Authors:** Junyan Tan, Haoran Lin, Siyuan Guo, ..., Tianyu Shen, Zeyu Qiao
**arXiv:** [2607.01595](https://arxiv.org/abs/2607.01595)
**Categories:** Artificial Intelligence (cs.AI); Computation and Language (cs.CL)

As the scale and complexity of cloud-based AI systems continue to escalate, ensuring service reliability through rapid fault detection and adaptive recovery has become a critical challenge. While existing approaches integrate Large Language Models (LLMs) for semantic understanding and Deep Reinforcement Learning (DRL) for policy optimization, they often rely on sequential, loosely coupled architectures that underutilize the generative and reasoning capabilities of LLMs. In this paper, we propose a paradigm shift with PASE, a Planning-Aware Semantic self-healing engine, a novel fault self-healing framework that reconceptualizes recovery as a neuro-symbolic program synthesis task. PASE employs an LLM as a core Plan Synthesis Engine to generate structured recovery plans from a library of semantic primitives. A Neural-Symbolic World Model verifies plan feasibility through simulation, while a Meta-Prompt Optimizer, trained via DRL, learns to generate optimal prompts that guide the LLM's planning process. This tight reason-plan-verify-adapt loop enables dynamic, context-aware recovery strategy generation beyond predefined action spaces. Experiments on a real-world cloud fault injection dataset demonstrate that PASE significantly outperforms state-of-the-art methods, reducing average system recovery time by over 40% and improving fault detection accuracy in unknown fault scenarios. Our framework advances autonomous system management by unifying LLM-based reasoning with model-assisted verification and meta-learned guidance.

---

## 3. OPINE-World: Programmatic World Modeling with Ontology-error-Prioritized Interactive Exploration

**Authors:** David Courtis, Wenhao Li, Scott Sanner
**arXiv:** [2607.01531](https://arxiv.org/abs/2607.01531)
**Categories:** Artificial Intelligence (cs.AI); Machine Learning (cs.LG)

Learning how an environment behaves from interaction is central to building agents that adapt to unfamiliar tasks. World models learned with deep networks are flexible but data-hungry and transfer poorly beyond their training distribution. Program-synthesized world models, written as source code by LLMs and refined through counterexample-guided inductive synthesis (CEGIS), are instead data-efficient and reusable, yet they have been demonstrated mainly on structured-state worlds with a given object vocabulary, and a single program search does not scale to pixel-rendered environments whose object structure must be hypothesized flexibly. We introduce OPINE-World, an LLM agent that learns an object-centric programmatic world model online from interaction. OPINE-World couples two cooperating agents in a loop of hypothesis and test, one acting in the environment and one synthesizing the model in code with replay verification and model-based planning, and it steers exploration with a Bayesian measure of object-type adequacy we call ontology error. We evaluate OPINE-World on ARC-AGI-3, a benchmark for skill-acquisition efficiency in which the object vocabulary, the goal, and the action semantics are withheld. OPINE-World solves 20 of 25 games without per-game training and reaches an action-efficiency score of 78.4 against the human baseline.

---

## 4. Learning to Move Before Learning to Do: Task-Agnostic pretraining for VLAs

**Authors:** Junhao Shi, Siyin Wang, Xiaopeng Yu, ..., Jingjing Gong, Xipeng Qiu
**arXiv:** [2607.02466](https://arxiv.org/abs/2607.02466)
**Categories:** Robotics (cs.RO); Artificial Intelligence (cs.AI)

Vision-Language-Action (VLA) models are fundamentally bottlenecked by the scarcity of expert demonstrations -- triplets of observations, instructions, and actions that are costly to collect at scale. We argue that this bottleneck stems from conflating two distinct learning objectives: acquiring physical competence (how to move) and acquiring semantic alignment (what to do). Crucially, only the latter requires language supervision. Building on this Decomposition Hypothesis, we propose Task-Agnostic Pretraining (TAP), a two-stage framework that first learns transferable motor priors from cheap, unlabeled interaction data -- including discarded off-task trajectories and autonomous robot play -- via a self-supervised Inverse Dynamics objective. A lightweight second stage then grounds these priors in language using minimal expert data. On the SIMPLER benchmark, TAP matches models trained on over 1M expert trajectories while using orders of magnitude less labeled data, yielding a 10% absolute gain over standard behavior cloning. On a real-world WidowX platform, TAP retains 25% success under camera perturbations where internet-scale baselines collapse to 0%, demonstrating that task-agnostic pretraining produces robust, transferable physical representations and offers a scalable path forward for Embodied AI.

---

## 5. WorldSample: Closed-loop Real-robot RL with World Modelling

**Authors:** Yuquan Xue, Le Xu, Zeyi Liu, ..., Bofang Jia, Ziwei Wang
**arXiv:** [2607.02431](https://arxiv.org/abs/2607.02431)
**Categories:** Robotics (cs.RO); Artificial Intelligence (cs.AI)

Reinforcement learning (RL) can overcome the demonstration-coverage limitation of imitation learning (IL) by allowing robots to improve through trial-and-error interaction beyond the states observed in demonstrations. However, deploying RL on real robots remains constrained by high interaction costs, since each physical rollout is costly and reflects only one realized action-outcome path. To address this challenge, we propose WorldSample, a physically grounded data augmentation framework for real-robot RL that closes a real-synthetic loop between physical rollouts, world-model generation, and policy improvement. Grounded on real rollouts, WorldSample generates high-fidelity synthetic transitions through a post-trained world model, which greatly lowers the visual hallucination. Specifically, rather than simply using these transitions as real-world experience, WorldSample introduces Policy-Paced Learning (PPL) to regulate the training process through sample selection and scheduling, balancing useful augmentation against value overestimation and mitigating the hallucination-induced noise. Experiments on robot manipulation tasks involving contact-rich and precise tasks show that WorldSample improves policy success rate by 28% while reducing training steps by 59% compared with baselines. Furthermore, WorldSample improves world model visual fidelity by 19.4dB in PSNR and 0.47 in SSIM over demonstration-only post-training, validating the effectiveness of the real-synthetic loop for both policy and world model performance.

---

## 6. ACID: Action Consistency via Inverse Dynamics for Planning with World Models

**Authors:** Gawon Seo, Dongwon Kim, Suha Kwak
**arXiv:** [2607.02403](https://arxiv.org/abs/2607.02403)
**Categories:** Robotics (cs.RO); Artificial Intelligence (cs.AI); Computer Vision and Pattern Recognition (cs.CV)

Decision-time planning with action-conditioned world models has become a popular paradigm for embodied control. However, the standard planning cost judges a candidate solely by how close its predicted terminal state lies to the goal, leaving the realizability of the intermediate transitions unchecked -- a predicted trajectory can look convincing while the environment rollout drifts away from it. In this paper, we propose ACID, a decision-time planning framework that introduces cycle action consistency: the action inferred backward from a predicted transition by an inverse dynamics model should recover the one that was conditioned on. We fold this per-step residual into the planning cost via a scale-invariant adaptive weight. Across four action-conditioned world models and six tasks spanning rigid and deformable manipulation, articulated control, and visual navigation, ACID consistently improves planning and matches the baseline's accuracy with substantially less planning compute.

---

## 7. Guided Action Flow: Q-Guided Inference for Flow-Matching Vision-Language-Action Policies

**Authors:** Liuhaichen Yang, Zhuang Jiang, Chenchao Sheng, Zezhi Tang
**arXiv:** [2607.02092](https://arxiv.org/abs/2607.02092)
**Categories:** Robotics (cs.RO); Artificial Intelligence (cs.AI)

Flow-matching vision-language-action policies generate robot action chunks through an iterative transport process, creating an opportunity for test-time guidance without retraining the base policy. We study this opportunity in Guided Action Flow, an inference-time framework that keeps a pretrained SmolVLA policy frozen and uses a learned action-chunk critic to guide its reverse-time flow sampler. The critic is trained from real success and failure rollouts, can condition on task-description features from the frozen SmolVLA language pathway, and is used only through action gradients during sampling. We evaluate the approach on LIBERO manipulation tasks. A single-task critic improves success from 68.0% to 82.0% on one seed window and from 82.0% to 86.0% on another. A multi-family task-description critic improves validation success from 46.0% to 56.0%, while the locked held-out test gain is positive but modest, from 65.0% to 67.5%. These results support the feasibility of Q-guided inference for frozen flow-matching VLA policies, while showing that critic generalization and uncertainty-aware guidance remain the central bottlenecks.

---

## 8. PhysMani: Physics-principled 3D World Model for Dynamic Object Manipulation

**Authors:** Peng Yun, Shouwang Huang, Hao Li, ..., Jianan Wang, Bo Yang
**arXiv:** [2607.01938](https://arxiv.org/abs/2607.01938)
**Categories:** Robotics (cs.RO); Artificial Intelligence (cs.AI); Computation and Language (cs.CL); Computer Vision and Pattern Recognition (cs.CV); Machine Learning (cs.LG)

Manipulating fast and dynamically moving targets in unstructured 3D environments remains challenging for embodied AI. Existing visual-language-action models and world models struggle with accurate 3D geometry and physically meaningful forecasting. We propose PhysMani, a framework that couples a physics-principled 3D Gaussian world model with a future-aware action policy model. The world model learns a divergence-free Gaussian velocity field via online optimization for fast and physically grounded future dynamics prediction. The policy model integrates the predicted 3D scene future dynamics through a learnable token based cross-attention module. We introduce PhysMani-Bench, a dynamic manipulation benchmark with 16 tasks, and demonstrate a superior success rate over strong baselines in both simulation and real-world robot experiments.

---

## 9. Predicting Closed-Loop Performance of Latent World Models: Offline Checkpoint Selection for MPC and Model-Based RL Under Non-Markovian Rewards in LunarLander

**Authors:** Nikolai Smolyanskiy
**arXiv:** [2607.01736](https://arxiv.org/abs/2607.01736)
**Categories:** Machine Learning (cs.LG); Artificial Intelligence (cs.AI); Systems and Control (eess.SY)

We study how to predict the downstream closed-loop performance of a learned latent world model from validation-time diagnostics alone. Choosing the right checkpoint from a world-model training run is difficult: validation loss and multi-step prediction RMSE keep improving long after closed-loop performance has collapsed. We present a suite of structural validation-time diagnostics drawn from optimal-control theory and apply them to Gymnasium's LunarLander v3, which features shaped rewards. We train an RSSM [5, 4] world model on it and treat per checkpoint CEM-MPC return as the oracle for closed-loop quality. By evaluating 40 metrics against this oracle, we find that the strongest single predictor is the Reward Observability Fraction (ROF), which measures the reward predictor's dependence on the observable subspace. We combine ROF with three structural regularizers into a single-number offline checkpoint selection score, the Composite Reward Observability Fraction (CROF). The CROF-selected world model trains a model-based A2C policy that beats a fairly evaluated model-free A2C baseline by ~24.5 return points while using ~65x fewer real-environment interactions, and the same world model also drives a strong zero-shot CEM-MPC policy. Code and data: this https URL.

---

## 10. VLAFlow: A Unified Training Framework for Vision-Language-Action Models via Co-training and Future Latent Alignment

**Authors:** Guoyang Xia, Fengfa Li, Hongjin Ji, ..., Kun Zhan, Yan Xie
**arXiv:** [2607.01586](https://arxiv.org/abs/2607.01586)
**Categories:** Computer Vision and Pattern Recognition (cs.CV); Artificial Intelligence (cs.AI); Robotics (cs.RO)

Vision-language-action models (VLAs) have recently advanced robotic manipulation, yet the effects of different robot-data pre-training paradigms remain difficult to compare because existing models often differ in architecture, data, action space, and evaluation protocol. We present VLAFlow (Vision-Language-Action Flow), a unified flow-matching framework for controlled comparison of VLA training objectives. Using a heterogeneous robot corpus, OXEMix, containing approximately 5,000 hours of data from DROID, OpenX-Embodiment, OpenX-Augmented, and RoboCOIN, we evaluate four paradigms under the same pi0-style architecture, shared VLM backbone, action expert, and 14-dimensional action space: action-only modeling (MindPI), language-supervised co-training (MindLPI), future latent alignment (MindWPI), and their combination (MindLWPI). Experiments on LIBERO, LIBERO-Plus, and SimplerEnv show that action-only pre-training is sensitive to heterogeneous data. In contrast, language supervision helps preserve vision-language generalization, while future latent alignment improves state-transition and action-outcome modeling. By combining both signals, MindLWPI achieves the most stable overall transfer performance across benchmarks. These results suggest a meta-action space view: language and future latent representations provide complementary intermediate constraints that make heterogeneous action supervision smoother and more transferable.

---

## 11. Certified World Models as Sensing Clocks: Drift-Aware Deadlines for Active Perception

**Authors:** Hongbo Wang
**arXiv:** [2607.01537](https://arxiv.org/abs/2607.01537)
**Categories:** Machine Learning (cs.LG)

Certified world models estimate how long their predictions remain valid. We turn this validity horizon into an operational sensing clock: a rule for when an agent should stop coasting and re-sense. Starting from an audited equivariant world model, we derive a deadline for no-sensing intervals and show that deployable deadlines in learned world models must be drift-aware: on-manifold Lyapunov rates alone overestimate coasting validity, while calibrated native rollout-drift envelopes carry the deployed guarantee. On a frozen 3D VN-JEPA model, the resulting clock controls held-out interval-simultaneous certificate violation across seeds and data shards. In a cue-conditioned theorem-bed (a synthetic bench where all schedulers share the exact model, isolating the scheduling rule), the clock remains valid on the deployment distribution and substantially reduces eventful-tail violations relative to exact-mixture expected-belief scheduling at matched sensing budget. We also report limits: in the short-horizon frozen VN-JEPA regime, empirical conformal horizons match the deployed clock on validity and budget, and a partial-reset exploration finds no clean budget-matched advantage for the spectral term. Thus the contribution is a certified sensing-clock primitive and drift-aware deployment method, not a claim that spectral clocks empirically dominate all non-spectral schedulers.

---

## 12. VT-WAM: Visual-Tactile World Action Model for Contact-Rich Manipulation

**Authors:** Shuai Tian, Yupeng Zheng, Yuhang Zheng, ..., Wenchao Ding, Dongbin Zhao
**arXiv:** [2607.02503](https://arxiv.org/abs/2607.02503)
**Categories:** Robotics (cs.RO)

Contact-rich manipulation requires policies to react to local deformation, pressure, slip, and friction, yet these cues are temporally sparse and often invisible in visual observations. Existing visual-tactile policies usually feed tactile observations directly into action prediction, but rarely model tactile deformation dynamics during action generation. In this paper, we introduce VT-WAM, a Visual-Tactile World Action Model that jointly learns future visual prediction, tactile deformation prediction, and action prediction within a unified flow matching framework. In particular, VT-WAM introduces (1) Asymmetric Mixture-of-Transformers (MoT) attention to bridge a first-frame visual anchor with temporal tactile dynamics, and (2) contact-gated Action-Visual-Tactile Attention Guidance (AVTAG) to encourage action queries to rely on tactile evidence during contact phases. Across six real-world contact-rich manipulation tasks, VT-WAM achieves a 71.67% average success rate, outperforming Fast-WAM by 26.67% and OmniVTLA by 35.84%. Ablations demonstrate that modeling tactile deformation dynamics and guiding contact-phase tactile attention are both important for contact-rich tasks. Project website: this https URL.

---

## 13. The Moving Eye: Enhancing VLA Spatial Generalization via Hybrid Dynamic Data Collection

**Authors:** Jincheng Tang, Yilong Zhu, Zhengyuan Xie, Jiang-Jiang Liu, Jiaxing Zhang
**arXiv:** [2607.02322](https://arxiv.org/abs/2607.02322)
**Categories:** Robotics (cs.RO); Computer Vision and Pattern Recognition (cs.CV)

Vision-Language-Action (VLA) models have shown remarkable promise in generalized robotic manipulation. However, their spatial generalization remains fragile. We argue that simply increasing the number of viewpoints is insufficient. Models often fall into the trap of Shortcut Learning, latching onto spurious correlations (e.g., fixed relative poses between objects or between the camera and robot base) rather than learning true spatial relationships. In this work, we propose a data-centric solution to enhance VLA spatial generalization. We utilize a dual-arm setup where one arm performs manipulation while the other serves as a mobile environmental camera. We systematically evaluate three data distribution patterns: Fixed, Multi-Fixed, and Moving Views. Our findings reveal that a hybrid strategy, combining continuous camera motion with diverse static viewpoints, yields the best performance by substantially reducing spurious correlations while maintaining training stability. Our experiments demonstrate that this strategy mitigates spurious correlations, enabling VLAs to generalize to unseen camera poses and object configurations where simply adding more static viewpoints fails. Crucially, we reveal that the susceptibility to shortcut learning and the struggle with spatial generalization are universal characteristics shared across diverse architectures. Consequently, all evaluated models (ACT, Diffusion, and VLA models including Pi0 and Gr00t) benefit significantly from our mixed data strategy.

---

## 14. VLA-Corrector: Lightweight Detect-and-Correct Inference for Adaptive Action Horizon

**Authors:** Yi Pan, Miao Pan, Qi Lu, ..., Xuhong Zhang, Wenqi Zhang
**arXiv:** [2607.01804](https://arxiv.org/abs/2607.01804)
**Categories:** Robotics (cs.RO)

Vision-Language-Action (VLA) foundation models have recently achieved strong progress in embodied intelligence. To reduce policy-call frequency while preserving temporal coherence, most generative policies adopt an action chunk mechanism, executing multiple future actions in an open-loop manner under a fixed action horizon. However, this "predict-then-blindly-execute" paradigm sacrifices closed-loop reactivity: in contact-rich physical interactions, even small local perturbations can rapidly amplify within the open-loop blind spot, leading to compounding errors and ultimately task failure. To address this limitation, we propose VLA-Corrector, a lightweight corrective inference framework for action-chunked VLA policies. Without modifying the backbone policy weights, VLA-Corrector introduces a lightweight Latent-space Vision Monitor (LVM) that continuously compares predicted and actual visual feature evolution, enabling online detection of visual dynamics deviations. Once persistent deviation is detected, the system triggers a truncation event, discards the remaining stale actions, and invokes corrective replanning via Online Gradient Guidance (OGG). The detect-and-correct mechanism of VLA-Corrector naturally induces an event-triggered adaptive action horizon: it preserves long-horizon execution when the current chunk remains reliable, and invokes short-horizon corrective replanning when execution begins to drift. In doing so, VLA-Corrector mitigates the trade-off imposed by static horizons between execution robustness and policy-call frequency. It can be integrated into different VLA models without further retraining the VLA backbone, interrupting compounding errors while preserving much of the efficiency benefit of action chunking and substantially improving robustness in long-horizon, contact-rich robotic manipulation tasks.

---

## 15. Neuro-Symbolic Safety Guidance for Vision-Language-Action Models via Constrained Flow Matching

**Authors:** William English, Hao Zheng, Rickard Ewetz
**arXiv:** [2607.01378](https://arxiv.org/abs/2607.01378)
**Categories:** Robotics (cs.RO); Systems and Control (eess.SY)

Vision-Language-Action (VLA) models have demonstrated promising generalization capabilities across robotic manipulation tasks, yet their real-world deployment remains limited by the lack of effective safety measures. Specifically, existing safety measures only prevent collisions caused by the robot's next action. In this paper, we propose a neuro-symbolic safety guidance mechanism for flow matching based VLAs that enables predictive collision avoidance. Flow matching based VLAs determine the next actions by predicting a trajectory (a sequence of actions) through an iterative neural flow matching process. Our method formulates safety enforcement as a minimum-norm constrained optimization problem that corrects safety violations during the denoising process of noisy intermediate trajectory predictions. By analyzing predicted trajectories and applying corrections during iterative denoising, our approach anticipates collisions before they become unavoidable. This interleaving of symbolic constraint satisfaction with neural trajectory generation enables predictive collision avoidance rather than reactive intervention. On the SafeLIBERO benchmark, our method achieves 82.8% collision avoidance and 81.6% task success, a 6.3% and 19.8% improvement respectively over single-step methods, with the largest gains on long-horizon tasks where compounding distribution shift is most pronounced. Video demonstrations of our approach are included on our project page at this https URL.

---

## 16. PWM-ArtGen: Part World Model for Articulated Object Generation

**Authors:** Wentao Zheng, Ancong Wu
**arXiv:** [2607.02045](https://arxiv.org/abs/2607.02045)
**Categories:** Computer Vision and Pattern Recognition (cs.CV)

The key challenge in articulated 3D object generation from a single image is accurately predicting the underlying kinematic structure. Existing methods either infer kinematic parameters directly from a static image that lacks dynamic part-level kinematic relationships, or estimate parameters from visual dynamics generated from a single image, which is prone to accumulated errors of two steps. Moreover, the limited scale and diversity of existing annotated datasets further hinder generalization to complex, real-world objects. To overcome these limitations, we propose to learn the joint distribution of visual dynamics and kinematic parameters. Recognizing that articulated objects can be formulated as dynamic systems, we propose a unified Part World Model called PWM-ArtGen. To leverage unannotated data, this model couples action diffusion and image diffusion with independent diffusion timesteps, which enables visual branch co-training. We further curate a photorealistic dataset of 19.7k part-level image pairs without kinematic annotations, to support co-training. Experiments demonstrate that PWM-ArtGen substantially outperforms existing baselines in the resting state and exhibits strong zero-shot generalization to out-of-distribution objects.

---

## 17. Teaching Vision-Language-Action Models What to See and Where to Look

**Authors:** Yuguang Yang, Canyu Chen, Zhewen Tan, ..., Bo Zhang, Xianbin Cao
**arXiv:** [2607.01658](https://arxiv.org/abs/2607.01658)
**Categories:** Computer Vision and Pattern Recognition (cs.CV)

Vision-Language-Action (VLA) models have emerged as a promising paradigm for end-to-end autonomous driving. However, existing VLAs' training relies heavily on text-centric visual question answering and chain-of-thought reasoning data, which emphasizes linguistic reasoning rather than action-grounded planning. As a result, the learned representations capture semantic knowledge but lack spatial dependencies crucial for reliable trajectory prediction. We propose DriveTeach-VLA, a framework that explicitly teaches VLAs what to see and where to look. Driving-aware Vision Distillation (DVD) injects driving-specific perceptual priors into the vision encoder, while 2D Trajectory-Guided Prompts (2D-TGP) provide spatial conditioning aligned with feasible driving trajectories. Together, they form a vision-guided learning pipeline: what to see (DVD pretraining) - where to look (TGP-guided SFT) - how to act (TGP-guided GRPO). DriveTeach-VLA achieves the state-of-the-art performance on NAVSIM and nuScenes. Our code is available at: this https URL.

---

## 18. Embodied.cpp: A Portable Inference Runtime of Embodied AI Models on Heterogeneous Robots

**Authors:** Ling Xu, Chuyu Han, Borui Li, ..., Sheng Zhong, Shuai Wang
**arXiv:** [2607.02501](https://arxiv.org/abs/2607.02501)
**Categories:** Robotics (cs.RO); Computer Vision and Pattern Recognition (cs.CV); Operating Systems (cs.OS)

Embodied AI models now span vision-language-action (VLA) models and world-action models (WAMs), but practical deployment remains fragmented across model-specific Python stacks, backend assumptions, and robot-side glue code, especially on heterogeneous edge devices. Existing inference runtimes are designed mainly for request-response serving and therefore do not satisfy the runtime contract of embodied deployment: multi-rate execution inside closed-loop control, latency-first batch-1 inference on heterogeneous hardware, and extensible embodied interfaces beyond fixed token I/O. We present this http URL, a portable C++ inference runtime for embodied models. Based on an architectural analysis of representative VLA models and WAMs, this http URL captures a shared execution path and organizes it into five layers: input adapters, sequence builders, backbone execution, head plugins, and deployment adapters. The runtime provides modular multi-rate execution, latency-first fused inference, and extensible operator and I/O support, enabling deployment across heterogeneous devices, robots, and simulators through one backend abstraction. We evaluate this http URL on two VLA models, HY-VLA and pi0.5, and on a preliminary WAM benchmark using a LingBot-VA Transformer block. The VLA deployments achieve successful closed-loop execution with 100.0% and 91.0% task success rates, respectively. The WAM benchmark reduces block memory from 312.2 MiB to 88.1 MiB. These results show that this http URL improves deployment efficiency while preserving high accuracy across diverse embodied model architectures.

---

## 19. Bridge-WA: Predicting Where and How the World Changes for Robotic Action

**Authors:** Yongjie Bai, Hanting Wang, Mingtong Dai, ..., Yang Liu, Liang Lin
**arXiv:** [2607.02195](https://arxiv.org/abs/2607.02195)
**Categories:** Robotics (cs.RO)

General-purpose vision-language-action models benefit from large vision-language priors, but effective manipulation also requires anticipating action-relevant scene changes. Existing world-action models often rely on large generative world models or dense future rollouts, which are expensive and spend capacity on visual details weakly coupled to control. We present Bridge-WA, a lightweight world-action framework that distills a frozen future-change teacher into three compact priors: future tokens for intended outcomes, change maps for intervention support, and motion-flow maps for local transition direction. A WorldBridge conditions the action transformer on these priors through multi-source attention memories and spatial-temporal biases, while the teacher model is removed at inference. Across VLABench, RoboTwin2.0, LIBERO-Plus and real-robot evaluations, Bridge-WA improves task success, progress, and robustness, with particularly clear gains under out-of-distribution visual shifts. By focusing action generation on where and how the scene will change, Bridge-WA suppresses nuisance appearance factors such as background, lighting, and distractors, leading to better generalization without deployment-time dense future-image generation. Code and visualizations are available at: this https URL .

---

## 20. WorldDirector: Building Controllable World Simulators with Persistent Dynamic Memory

**Authors:** Hanlin Wang, Hao Ouyang, Qiuyu Wang, ..., Yujun Shen, Qifeng Chen
**arXiv:** [2607.02517](https://arxiv.org/abs/2607.02517)
**Categories:** Computer Vision and Pattern Recognition (cs.CV)

We present WorldDirector, a highly controllable video world model framework designed for persistent dynamic object memory and unrestricted viewpoint exploration. Unlike existing world models that entangle physical dynamics with pixel rendering and rely on continuous visual observation to sustain motion, our framework explicitly decouples semantic motion orchestration from visual generation. By leveraging an LLM to coordinate 3D trajectories with camera movements and subsequently employing these orchestrated trajectories as control signals for video generation, our approach ensures strict physical logic and appearance stability, successfully preserving the exact visual identities of dynamic entities even when they re-enter the scene after prolonged periods out of view. Experimental results demonstrate that our method supports the synthesis of complex and extended events with unprecedented controllability and persistent dynamic object memory. Project Page: this https URL

---
