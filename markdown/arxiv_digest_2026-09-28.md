# arXiv Daily Digest — 2026-09-28

**Mode:** direct
**Categories:** cs.AI, cs.LG, cs.RO, cs.CV
**Keywords:** VLA, RSI, agentic robot, self-improving robot, self-evolving robot, robot harness
**Papers found:** 7

---

## 1. Towards VLA-Dreamer: Refining VLA Behavior Using World Models

**Authors:** Parsa Mastouri Kashani, Jan-Gerrit Habekost, Stefan Wermter
**arXiv:** [2609.31313](https://arxiv.org/abs/2609.31313)
**Categories:** Robotics (cs.RO); Artificial Intelligence (cs.AI)

Vision-Language-Action models (VLAs), while showing strong potential for robot control, require massive amounts of high-quality imitation learning data. Moreover, the absence of an explicit world model casts further doubt on their control capabilities. In this concept paper, we propose a novel architecture that addresses sample efficiency in VLAs by training a predictive world model on the embedding space of the VLA's vision encoder. We hypothesize that these embeddings are action-relevant and usable for future prediction. To this end, we propose using the suggested architecture to investigate how well these embeddings predict the future based on actions, as the inability to do so would mark a key limitation of VLA architectures: the lack of a non-lossy implicit world model to simulate real-world dynamics. The proposed architecture differs from the standard world model dynamics as the loss comes from the embedding space rather than the pixel space, similar to joint embedding predictive architectures. Furthermore, the trained world model can be utilized for short-term planning tasks by sampling VLA actions given goal images. We intend to examine the richness of vision embeddings in VLAs and reduce their high data requirements through a world model that can also generate plans during inference.

---

## 2. The Linear Representation Hypothesis for Vision-Language-Action Models

**Authors:** Minseok Jeong, Hyewon Choi, Hiroyasu Tsukamoto, SooJean Han
**arXiv:** [2609.30996](https://arxiv.org/abs/2609.30996)
**Categories:** Machine Learning (cs.LG); Artificial Intelligence (cs.AI)

The linear representation hypothesis (LRH) has become a standard lens for measuring and intervening on semantic information through the internal representations of large language models (LLMs). A growing body of work has begun extending this perspective to vision-language-action (VLA) models, but the dynamical nature of embodied interaction introduces an additional challenge. Unlike semantic attributes commonly studied in LLMs, such as gender or language, a physical quantity of interest (QoI) in a VLA evolves jointly with the system dynamics: the representation influences the actions selected by the policy, which alter the physical state and, in turn, the next representation.
In this paper, we develop a theoretical, signature-based formulation of the LRH for VLA that unifies representations and policies. On the representation side, we establish the existence of representations from which the future evolution of a QoI under a candidate action trajectory can be recovered via linear probing. On the policy side, we introduce a signature generalized linear model for stochastic action chunks. This structure yields a monotonic change in the expected future QoI along linear paths in natural parameter space, enabling linear steering. We construct an explicit oracle representation in a planar control-affine navigation experiment and verify the predicted linear probing and steering mechanisms.

---

## 3. VLALight: Lightweight Vision-Language-Action Models for Emergency-Aware Traffic Signal Control

**Authors:** Kemou Jiang, Maonan Wang, Xingchen Zou, ..., Yirong Chen, Zhiyong Cui
**arXiv:** [2609.30709](https://arxiv.org/abs/2609.30709)
**Categories:** Computer Vision and Pattern Recognition (cs.CV); Artificial Intelligence (cs.AI)

Traffic signal control (TSC) is essential for mitigating urban congestion. Recent advances in vision-language models (VLMs) enable richer interpretation of intersection scenes, opening new opportunities for visual-context-aware TSC. However, the loose coupling and repeated information conversion between modules can lead to the loss of fine-grained visual details, while sequential inference introduces substantial latency. To address these limitations, we propose VLALight, a lightweight end-to-end vision-language-action framework that directly maps intersection observations and signal-phase information to discrete signal actions. To handle the multi-view nature of TSC, VLALight combines multiple directional camera views into a unified visual input and uses textual instructions to establish their correspondence with traffic movements and signal phases. This design enables direct action prediction with a compact 0.5 B-parameter model, without intermediate image-to-text descriptions or handcrafted traffic-state representations. Experiments show that VLALight delivers the best emergency-vehicle service of all compared methods, reducing pooled emergency waiting time by 21.1% over the cascaded VLMLight while running in real time on local hardware and generalizing to unseen intersection topologies and traffic-flow patterns.

---

## 4. Kintsugi-VLA: Turning Failed Robot Rollouts into Recovery Data through Interventional Recoverability

**Authors:** Ivan Snegirev, Elizaveta Semenyakina, Dmitrii Maliukov, Miguel Altamirano Cabrera, Dzmitry Tsetserukou
**arXiv:** [2609.31048](https://arxiv.org/abs/2609.31048)
**Categories:** Robotics (cs.RO)

Simulation enables scalable training of Vision-Language-Action policies by using privileged experts to generate visual demonstrations without requiring every trajectory to be collected through manual teleoperation. However, such pipelines typically retain successful demonstrations while failed rollouts are discarded, even though they expose precisely the off-nominal states from which recovery must be learned.
We introduce Kintsugi-VLA, a framework for converting failed rollouts into targeted synthetic recovery data by exploiting exact state restoration and branching in simulation. For a fixed privileged expert, we define interventional recoverability as the probability of completing the original task after the simulator is restored to a given state, estimate it using adaptive Monte Carlo continuations with pointwise Wilson intervals, and characterize its non-monotonic evolution along failed trajectories. These estimates identify an observed terminal low-recoverability frontier-the point after which measured recoverability remains below a threshold-which is then used to select informative recovery starting states.
In a simulated Franka manipulation task, targeted recovery data yield aggregate SmolVLA recovery success of 34.6\% and 38.4\% under difficulty- and frame-budget matching, respectively, 5.8 and 6.7 percentage points above uniform sampling within the same recovery window. The same ordering is observed under disturbed end-to-end execution and shifted clutter and physics conditions, while clean-task success decreases from 76.8\% to 74.7\%. Kintsugi-VLA demonstrates how failed simulator rollouts can be transformed from discarded experience into structured recovery-training data through direct interventional measurement.

---

## 5. Causeway: Restoring Task Accessibility for Instruction Switching in VLA Policies

**Authors:** Qingzi Wang, Kaixi Feng, Guangyao Shi, ..., Ang Li, Dinesh Manocha
**arXiv:** [2609.30913](https://arxiv.org/abs/2609.30913)
**Categories:** Robotics (cs.RO)

Vision-language-action (VLA) policies can execute many tasks from standard initial states, yet a new instruction may fail after another task has altered the robot's physical state. We study instruction switching, where a new task is issued during or after the execution of a different one. We observe that a target task that is reliably completed from its standard initial states can become inaccessible from states produced by a preceding task. We call such states task islands. We propose Causeway, a training-free inference-time intervention. Given the current state and a re-entry pose for the target task, Causeway back-propagates through the frozen decoding computation and applies a state-directed write within the action-stream representation. The VLA decodes the return motion itself, without parameter updates, a new action head, or external action generation. Across 71 cross-object pairs, three switch timings, and three VLA architectures on LIBERO-Goal, Causeway raises bare-switch success from 3-26% to 47-65% and increases the rate of reaching the handoff neighborhood by 42-72 percentage points across models. Additional experiments on LIBERO-Object and a real xArm platform show that the recovery extends beyond the main LIBERO-Goal setting, both in simulation and on a robot.

---

## 6. VLaRL: Augmenting Vision-Language-Action Models with Simulation-Trained Latent-Conditioned Residual RL

**Authors:** Namiko Saito, Kinam Kim, Heecheol Kim, Katsushi Ikeuchi, Yasuyuki Matsushita
**arXiv:** [2609.30868](https://arxiv.org/abs/2609.30868)
**Categories:** Robotics (cs.RO)

Vision-language-action (VLA) models provide broad, instruction-conditioned manipulation behaviors, but their physical execution can remain imprecise during contact-rich interaction. Residual reinforcement learning (RL) can correct such errors while keeping the VLA frozen, but real-robot RL is costly and safety-critical. We propose VLA Latent-Conditioned RL (VLaRL), which enables residual RL for frozen VLAs to be trained in simulation and deployed on real robots without real-world RL or online adaptation. The key challenge is transferring the learned residual policy despite the visual gap between simulation and reality. Rather than requiring pixel-level visual correspondence, VLaRL uses the VLA's internal vision-language latent representation to condition residual control and as the sim-to-real transfer interface, and learns a lightweight mapper that transforms simulation-derived latents toward the real latent distribution. Across four contact-rich manipulation tasks and two VLA backbones, VLaRL improves real-world success in all task-backbone combinations, while controlled ablations demonstrate the importance of both latent conditioning and latent alignment for transferring simulation-trained residual control.

---

## 7. Fast Plans, Faithful Actions: Closing the Planning-Execution Gap in Hierarchical Vision-Language-Action Models

**Authors:** Chuanliang Xie, Boyu Ma, Gen Li, ..., Xinyu Zhou, Jianfei Yang
**arXiv:** [2609.30833](https://arxiv.org/abs/2609.30833)
**Categories:** Robotics (cs.RO)

Hierarchical vision-language-action (VLA) systems consist of a high-level vision-language planner and a low-level action expert that generates continuous actions. This hierarchical design has practical value only if the planner can generate plans fast enough to meet real-time control requirements, and the resulting plans actually contribute to the generation of action. We study one such system, a waypoint hierarchy pipeline adapted from $\pi_{0.5}$, and find that neither requirement is satisfied. This baseline relies on token-level autoregressive decoding (Token-AR) to generate a waypoint plan, requiring 57 very expensive vision-language model (VLM) forward passes. However, we find that erasing the waypoint endpoints has little effect on task success. Two findings reveal the misalignment of planner-executor: the planner generates outputs at an excessively fine granularity, and the executor underuses plans as a control condition. We address the latency issue with waypoint-aligned block-autoregressive decoding (Block-AR), and plan underuse issue with normalized goal modulation (NGM), a layer-wise goal path constrained by phase gating and anti-shortcut training so that the waypoint influences action generation maintaining other signals. Our method reduces the maximum number of VLM forward passes from 57 to 8 on LIBERO, including one prefix prefill, and achieves an $8.7\times$ reduction in planning latency on a Rokae dual-arm robot. With normalized goal modulation and anti-shortcut training, Block-AR's success rate on LIBERO-Long increases from 91.0% to 96.2%, while its average success rate across the four suites increases from 95.85% to 98.45%. On three bimanual tasks with this robot, success rates remain comparable across methods.

---
