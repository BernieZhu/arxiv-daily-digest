# arXiv Daily Digest — 2026-08-19

**Mode:** direct
**Categories:** cs.AI, cs.LG, cs.RO, cs.CV
**Keywords:** VLA, world model, world action model
**Papers found:** 10

---

## 1. Towards Zero-Shot Task Transfer with Neurosymbolic World Models

**Authors:** Isidoro Tamassia, Lennert De Smet, Giuseppe Marra
**arXiv:** [2608.17959](https://arxiv.org/abs/2608.17959)
**Categories:** Artificial Intelligence (cs.AI); Machine Learning (cs.LG)

State-of-the-art model-based reinforcement learning methods learn neural world models that allow policy improvement by planning in a latent space, without assumptions on the structure of the underlying environment. While expressive, these models are generally task-dependent: they learn uninterpretable latent representations that are tied to the training task and thus hard to generalize to new tasks. In this work, we present a novel world model formulation where the reward prediction only depends on a subset of structured, symbolic components of the whole latent state. Decoupling observation reconstruction and reward prediction allows us to learn world models that can adapt zero-shot, i.e. without further environment interactions, to new reward functions defined over the same symbolic state space. We discuss the main advantages and challenges of learning these neurosymbolic world models and demonstrate the strong generalisation properties of our approach over purely neural methods.

---

## 2. An Omitted Mode Is a Rare Rule: The Sampling-Verification Danger Law in Continuous Code World Models

**Authors:** Javier Aguilar Martín
**arXiv:** [2608.17956](https://arxiv.org/abs/2608.17956)
**Categories:** Machine Learning (cs.LG); Artificial Intelligence (cs.AI); Systems and Control (eess.SY)

In the Code World Model paradigm an LLM synthesizes an executable world model that a classical planner searches, and the model is accepted when it reproduces sampled transitions. We ask what that acceptance certifies in continuous control. We define the pipeline's danger as an expected risk and isolate its exact factor: the probability that N i.i.d. gate rollouts all miss a critical event of probability r is exactly (1-r)^N; an independent acceptance sample adds its budget to the exponent. On three hybrid instruments the accepted mode-blind model is exploited: the planner is pinned at the mode boundary at a regret of nearly the whole attainable return. We prove a localization budget, valid at boundary points: models with Lipschitz constant at most L differing by eta at a point disagree above tolerance eps on a region of volume at least kappa((eta-eps)/L)^(d+m); the discontinuous reset modes studied pay no such budget. With real LLM synthesis, GPT-5.x repairs an omitted 1D clamp in 105 of 111 mode-containing draws -- every attempt exact on 50 of 56 instrument-stream blocks (95% CI [0.781, 0.960]). On 2D regions no artifact recovers the rule (0/156); eight targeted interventions leave the failure in place, and positive controls locate it: a located rule is not induced, while given form and location the constants follow exactly. A version-space certificate proves identification is class-relative: at the widest dose the declared fit succeeds in 20/20 blocks and every sample-consistent circle is within tolerance in 18/20. We prove a class of entry rules exactly consistent with every sample yet harmless at play, so identifiability is a measurable property of the instrument. Re-scoring all 1034 artifacts on independent samples confirms acceptance certifies sample consistency and no more: where the gate is provably informative it covers about two percent of the exploited planner's queries.

---

## 3. No Gaussian Required: Contrastive Inverse Dynamics for JEPA World Models

**Authors:** Jack Boylan, Chris Hokamp
**arXiv:** [2608.17542](https://arxiv.org/abs/2608.17542)
**Categories:** Machine Learning (cs.LG); Artificial Intelligence (cs.AI)

Joint-Embedding Predictive Architectures (JEPAs) learn world models by predicting future embeddings, but the objective admits a trivial solution of a constant encoder, so every practical system adds an anti-collapse mechanism (LeCun, 2022; Assran et al., 2023; Bardes et al., 2022; 2024). LeWorldModel (LeWM) prevents collapse with SIGReg, a regularizer that forces the latent distribution to match an isotropic Gaussian: the representation is stabilized by prescribing what it must look like, independently of the environment it models. We argue that the anti-collapse pressure can instead come from the transition data itself. Action-Contrastive Masked Transition Modeling (AC-MTM) keeps LeWM's forward latent-prediction objective and adds a training-only inverse-dynamics head trained with Action-NCE: each latent transition must identify the action that produced it among the other actions in the batch, a discrimination task that a collapsed encoder provably fails. The inverse branch is discarded after training, leaving test-time encoding, forward prediction, planning, and compute identical to LeWM. On four standard pixel-control tasks under a matched planning protocol, AC-MTM trains stably from scratch and matches SIGReg on average. On the harder multi-object OGBench Visual Scene task, results are consistent with the prescribed geometry becoming a bottleneck: AC-MTM reaches 80.0$\pm$2.0% success versus 58.0$\pm$2.0% for SIGReg, improving by 20-24 points in each training seed. A single 50-episode random-policy run gives a 52% baseline estimate. Contrastive inverse dynamics thus provides a distribution-free anti-collapse signal that requires no target network, stop-gradient, pretrained encoder, or reconstruction objective, and we characterize the action-space and observability assumptions under which it holds. We make our code available at this https URL

---

## 4. Q-Learning With World Models

**Authors:** Perry Dong, Yueru Jia, Chelsea Finn, Dorsa Sadigh
**arXiv:** [2608.17163](https://arxiv.org/abs/2608.17163)
**Categories:** Machine Learning (cs.LG); Artificial Intelligence (cs.AI)

Off-policy reinforcement learning (RL) has become increasingly sample-efficient, enabling applications such as RL fine-tuning of Vision-Language-Action models into reliable, high-performing policies. World models offer a further lever for sample efficiency, as they predict state changes rather than actions alone, but their success has largely been confined to supervised policy learning. Prior model-based RL methods often optimize the policy or value function directly on imagined rollouts, which is prone to compounding bias and struggles to scale to large, high-dimensional problems such as real-world robotics, a problem that worsens with task horizon and visual complexity. In this work, we instead ask whether we can leverage world models directly on top of standard Q-learning to improve performance, while remaining trained and grounded in the real, online setting. We propose QWM, a framework that leverages world models to perform test-time search over imagined trajectories on top of Q-learning to select high-value actions during both online rollouts and evaluation. Since the policy and value function are trained only on real transitions, QWM avoids compounding model bias while still gaining the sample-efficiency benefits of predictive search. On challenging manipulation benchmarks Robomimic and LIBERO, QWM significantly outperforms strong prior state-of-the-art methods on both sample efficiency and performance.

---

## 5. Prism-GRPO: Faster VLA Policy Optimization via Splitting Same-outcome Groups

**Authors:** Zeyun Deng, Yuzhe Lu, Yawei Wang, ..., Panpan Xu, Jun Huan
**arXiv:** [2608.17423](https://arxiv.org/abs/2608.17423)
**Categories:** Robotics (cs.RO); Machine Learning (cs.LG)

GRPO is increasingly used for reinforcement learning of vision-language-action (VLA) policies because, unlike PPO, it does not require training a critic. This simplification comes with a sampling cost: group-relative advantages require multiple rollouts from each scene. Under binary success rewards, groups whose rollouts all succeed or all fail have zero advantage and are discarded by dynamic sampling. These groups are especially common early in training, when most rollouts fail, wasting much of the expensive robotic rollout budget. We introduce Prism-GRPO, which augments binary outcome reward with a weighted trajectory-level execution-quality score. By splitting same-outcome groups into a quality spectrum, Prism-GRPO recovers training signal while ensuring that every success still outranks every failure. Quality scores can be derived from simulator contacts, executed actions, or visual observations, avoiding task-specific progress rewards. We prove that Prism-GRPO never increases the probability that a sampled group is discarded for having zero advantages, and derive a gradient-alignment condition under which its combined update remains a local ascent direction for task success. Across four RoboTwin tasks spanning different horizons and coordination patterns, Prism-GRPO improves success and quality at matched rollout budgets and reaches target success rates with up to 56% fewer rollouts. It also suppresses a reward-hacking shortcut, with the cleaner behavior transferring under direct deployment to a real robot. Through ablations, we show consistent gains across contact-, smoothness-, and VLM-derived quality signals.

---

## 6. WONDER: A Radio World Model-based Negotiation Framework for Multi-Agent UAV Coverage Optimization

**Authors:** Jiahao Huang, Rongpeng Li, Zhifeng Zhao, Guoru Ding, Honggang Zhang
**arXiv:** [2608.16955](https://arxiv.org/abs/2608.16955)
**Categories:** Multiagent Systems (cs.MA); Machine Learning (cs.LG)

Post-disaster damage to terrestrial infrastructure can disrupt wireless coverage,while Uncrewed Aerial Vehicle (UAV) swarms provide a promising solution for rapid this http URL, due to the limitations in local geometry observations hidden radio impact,and inter-UAV communication,there exists a significant gap between locally visible movement choices and swarm-level coverage this http URL combat this gap,we propose a raido World-model-based Optimized Negotiation framework for Distributed UAV covERage (WONDER).Particularly, to tackle the unavailability of the future radio field from onboard observations, WONDER uses a Joint-Embedding Predictive Architecture (JEPA)-based radio world model to learn and predict the incremental radio effect of each candidate trajectory from deployment-available this http URL-round negotiation in WONDER then coordinates ranked proposals by committing one trajectory at a time and re-evaluating the remaining proposals under the updated context. Our theoretical analyses further validate the effectiveness of such a world model-based framework. WONDER also adopts a Proximal Policy Optimization (PPO)-style Actor and alternates between updating the world model and the actor. Furthermore,we build RadioDynamics,a comprehensive simulation environment that integrates UAV mobility,radio propagation, inter-UAV communication modeling,and digital-twin geometry with ray-traced fields in $62$ metropolitan this http URL on $11$ testing scenes in RadioDynamics show that WONDER achieves the highest balanced score among seven evaluated methods,reaching $0.870$ with a $0.162$ coverage advantage over STACCA, while maintaining $100\%$ connectivity between UAVs.

---

## 7. Hydra-0: Action Flow for Generalist World Modeling and Control

**Authors:** Hongyu Li, Bowen Wen, Xinghao Zhu, ..., Chenran Li, Yan Chang
**arXiv:** [2608.18077](https://arxiv.org/abs/2608.18077)
**Categories:** Robotics (cs.RO)

We introduce Hydra-0, a generalist world model conditioned on action flow, which represents robot actions as pixel motion. This shared visual interface enables generalist world modeling and control by learning action consequences across embodiments, tasks, environments, and video-generation backbones. Our best configuration achieves 90.4% lower robot-motion error and 60.2% lower object-motion error than our action-conditioned baseline, while supporting zero-shot composition and data-efficient adaptation. On the RoboLab benchmark, Hydra-0 achieves a Pearson correlation of r=0.96 between replayed and reference success rates. Finally, we uncover an emergent inverse mode of this interface: a world action model that predicts compatible robot motion from desired object flow transferred from a human demonstration. A trained action head maps the resulting latent features to executable actions without requiring task-specific expert robot demonstrations. Together, these results demonstrate the potential of action flow as a shared control interface connecting heterogeneous training data, open-loop policy evaluation, and robot control.

---

## 8. LIBERO-VIFO: Benchmarking the Capability and Safety of Visual Cue Following in Vision-Language-Action Models

**Authors:** Zhengyan Qian, Rui Yan, Alex Jinpeng Wang, Jinhui Tang
**arXiv:** [2608.17600](https://arxiv.org/abs/2608.17600)
**Categories:** Robotics (cs.RO)

Visual cues are increasingly adopted to guide robot learning, but whether Vision-Language-Action (VLA) models can reliably follow authorized cues while disregarding unauthorized ones remains unclear. Existing work covers only a narrow range of cue forms and focuses on final task success, providing only a coarse assessment of cue-following capability. Treating all visual cues as authorized also leaves safety risks of unauthorized following unexplored. To address these gaps, we introduce LIBERO-VIFO, a benchmark to evaluate both the capability and safety of visual cue following in VLA models. LIBERO-VIFO defines eight visual cue families spanning diverse forms. A total of four protocols in two parts are defined: Part I tests cue understanding and authorized following, while Part II evaluates unauthorized visual cue following under language-cue conflict and empty language conditions. Evaluating seven VLA models reveals that although visual cue understanding does not reliably translate into execution, current VLAs are able to execute cue-indicated tasks without language instruction, exposing an emerging risk of unauthorized visual cue following. Extended experiments on scene-instantiated cues, safety-critical settings, and real-robot deployment corroborate these findings. LIBERO-VIFO brings both the capability and safety of visual cue following into systematic evaluation, establishing visual-centric safety as a new perspective for the VLA community.

---

## 9. EATR-Stereo: Embodiment-Aware Token Routing of Paired Stereo Evidence for Humanoid Vision-Language-Action Control

**Authors:** Songwei Wu, Rui Zhao, Fan Yang, ..., Yang Liu, Hong Liu
**arXiv:** [2608.17453](https://arxiv.org/abs/2608.17453)
**Categories:** Robotics (cs.RO)

Long-horizon humanoid vision--language--action (VLA) control with head-mounted stereo cameras requires visual interfaces that can exploit complementary views while maintaining compatibility with pretrained representations. Existing interfaces often discard complementary stereo evidence or fuse additional observations without preserving the native primary-view pathway and adapting auxiliary information to robot embodiment. We present EATR-Stereo, an embodiment-aware token-routing framework that retains primary-view tokens and constructs primary-aligned Cross-View Auxiliary Tokens (CVATs) by querying the synchronized auxiliary-view token sequence. A body-segmented proprioceptive encoder further conditions token-wise auxiliary usage on robot configuration history, enabling selective incorporation of stereo evidence during action generation. The routed auxiliary stream augments the language and primary-visual context of a pretrained VLA while keeping its vision--language model frozen. On a 33-DoF physical humanoid with a 37-D proprioceptive state, we evaluate nine configurations in over-100-s search--approach--grasp--place--return tasks. EATR-Stereo achieves 60.0% full-task success, 100.0% grasp success, and 80.0% stage success. Under severe asymmetric occlusion, it improves recovery to 80% compared with 30% for CVAT alone. Ablation studies further show the importance of preserving primary tokens and combining cross-view auxiliary features with structured proprioceptive routing. These results demonstrate that selectively routed paired stereo evidence improves spatial grounding for reliable long-horizon humanoid VLA control.

---

## 10. Inference-Time Attention Steering for Vision-Language-Action Driving Models

**Authors:** Darshan Nagendra Prasad, Lars Ullrich, Knut Graichen
**arXiv:** [2608.17095](https://arxiv.org/abs/2608.17095)
**Categories:** Computer Vision and Pattern Recognition (cs.CV)

Vision-language-action (VLA) driving models couple a reasoning stage with a diffusion-based trajectory decoder, but do not give a direct way to redirect attention toward safety-critical actors at inference time without retraining. We studied a bounded additive pre-softmax attention bias on the visual tokens of detector localized traffic actors on Alpamayo-R1's Qwen3-VL backbone. It is applied as a fail open forward pre-hook with no weight changes. On 50 lane-change scenarios from the Physical AI World Model Synthetic dataset. The trajectory decoder shows a monotonic dose response in the bias magnitude, separate from a paired zero bias control at every tested magnitude. It reaches $\approx 17$\,cm mean displacement with lateral shifts up to $\sim 140$\ cm at the clamp. A layer ablation places the action-relevant signal in late layers, where the effect increases with the number of hooked layers (2.0cm for the first 8 layers; 67.6cm for all 36). A per call injection audit explains why the Chain-of-Causation text never changes. The mask based bias never reaches the reasoning pathway in this serving stack, so the invariance is verified exposure, not robustness. Steered trajectories tend to shift toward the attended actor, suggesting the bias governs where the model looks rather than encoding a target behavior.

---
