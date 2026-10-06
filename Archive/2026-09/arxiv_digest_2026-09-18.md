# arXiv Daily Digest — 2026-09-18

**Mode:** direct
**Categories:** cs.AI, cs.LG, cs.RO, cs.CV
**Keywords:** VLA, RSI, agentic robot, self-improving robot, self-evolving robot, robot harness
**Papers found:** 8

---

## 1. GeoAAC: Geometry-Based Adaptive Action Chunking from Denoising Trajectories in VLA Policies

**Authors:** Xin Chen, Sen Chen, Yujuan Ding, ..., Heng Tao Shen, Yi Bin
**arXiv:** [2609.20776](https://arxiv.org/abs/2609.20776)
**Categories:** Robotics (cs.RO); Artificial Intelligence (cs.AI); Machine Learning (cs.LG)

Action chunking is widely used for action generation and execution in Vision-Language-Action (VLA) policies, yet existing approaches commonly use a fixed action horizon. During a rollout, different task stages may require different levels of action continuity, control precision, and closed-loop feedback, making a fixed horizon unable to accommodate changing control requirements. We propose \textbf{GeoAAC}, a geometry-based adaptive action chunking method for flow-based VLA policies that adjusts the action horizon according to the reliability of the current action prediction. We show that the geometry of Flow Matching denoising trajectories provides process-level information for characterizing prediction reliability, with geometric variation across action prefixes remaining positively correlated with predictive uncertainty. GeoAAC uses this prefix-wise geometry to construct a horizon-wise geometric profile and adaptively determine the action horizon from a single generation without additional training. Experiments with GR00T N1.5 and {\pi}0.5 on LIBERO, LIBERO-Pro, RoboCasa365, and real-world manipulation tasks show consistent improvements over fixed-action-horizon baselines and existing adaptive methods, including up to 8.7 percentage points in simulation and an increase in average real-world success rate from 53.3\% to 74.4\%.

---

## 2. HIL-UMI: Bringing Human-in-the-Loop Post-Training of Vision-Language-Action Models to Universal Manipulation Interface

**Authors:** Zimu Han, Yiming Zeng, Jiyao Zhang, ..., Hui Shen, Hao Dong
**arXiv:** [2609.20659](https://arxiv.org/abs/2609.20659)
**Categories:** Robotics (cs.RO); Artificial Intelligence (cs.AI)

Large-scale vision-language-action (VLA) models provide powerful priors for robot manipulation, yet adapting them to a specific deployment remains challenging. Supervised fine-tuning (SFT) on task-specific demonstrations provides a step toward deployment, but faces two persistent limitations: static data provide limited coverage of out-of-distribution states, and standard imitation objectives do not distinguish progressing behavior from less useful data. Interactive post-training can address these limitations, but typically requires repeated policy execution and human intervention on a physical robot. We introduce HIL-UMI, a policy-guided Universal Manipulation Interface (UMI) framework for robot-free human-in-the-loop VLA post-training. During handheld UMI demonstrations, HIL-UMI queries the current policy on the same observation stream without executing its predictions. The Energy Score compares the human action trajectory with policy inference and triggers collection when their discrepancy indicates an out-of-distribution region. In a separate feedback loop, low online advantage predictions identify essential segments for refining a progress-based advantage estimator. The updated estimator then guides advantage-conditioned behavioral cloning using a balanced mixture of base demonstrations and new policy data. This design preserves the iterative and policy-aware nature of human-in-the-loop learning while decoupling data collection from robot deployment. Experiments on four real-world tasks spanning long-horizon and precise manipulation show that HIL-UMI achieves consistent improvement over SFT and benefits from both targeted collection and advantage refinement. Moreover, HIL-UMI outperforms HG-DAgger on Clean Up Table with lower per-frame collection time, suggesting a scalable path for VLA post-training across operators and locations.

---

## 3. SkipVLA: Skipping VLA Steps with Classical Planning for Fast Robot Manipulation

**Authors:** Kaivalya Agrawal, Md Ashiqur Rahman, Raymond A. Yeh, Zachary Kingston
**arXiv:** [2609.20648](https://arxiv.org/abs/2609.20648)
**Categories:** Robotics (cs.RO)

Vision-Language-Action (VLA) models are a class of generalist robot policies that map camera images and language instructions directly to robot actions. While promising, these models remain slow at test time, particularly for long-horizon tasks that require many queries to the policy. Recent efforts reduce VLA latency by distilling smaller models, overlapping asynchronous action chunks, or pairing the VLA with a fast low-level policy, but still run a learned policy for the entire task. In contrast to VLA, classical motion planners quickly find collision-free motions, but require an explicit goal and have no semantic understanding of the task. In this work, we present SkipVLA, a hybrid policy that combines a pretrained VLA with a classical motion planner, using the planner for free-space motion and querying the VLA only for contact-rich skills such as grasping and placing. SkipVLA reuses the frozen vision-language backbone of the VLA to predict a target pose for each planned motion, and learns this predictor without additional demonstrations introduced into the system by using what was already learnt by the large VLA. We evaluate SkipVLA with three VLAs on 13 LIBERO tasks in simulation and three pick-and-place tasks on a physical 6-DoF YAM arm, demonstrating up to 2.5x faster task completion and significantly lower energy consumption while achieving the same task success rate.

---

## 4. Co-VLA: Consensus-based Federated Training for Vision-Language-Action Models

**Authors:** Haolong Li, Guner Dilsad Er, Michael Muehlebach, Joerg Stueckler
**arXiv:** [2609.19923](https://arxiv.org/abs/2609.19923)
**Categories:** Robotics (cs.RO)

Vision-language-action models (VLAs) have emerged as a promising paradigm for general-purpose robot learning, with performance improving as models and datasets scale. Scaling robot data collection, however, remains challenging because data are naturally distributed across robots, tasks, and locations, making centralization costly or impractical. Federated learning offers a way to train on decentralized robot data, but applying it to VLAs requires accounting for heterogeneous robot client data distributions. We present Co-VLA, which applies consensus optimization using the Alternating Direction Method of Multipliers~(ADMM) to federated VLA training. We show that the same algorithm supports both full-model training and parameter-efficient fine-tuning with both fixed-rank and rank-adaptive adapters. The name Co-VLA reflects both consensus and collaboration: clients with different local robot datasets collaboratively train a shared model without sharing their data. Our experiments demonstrate that Co-VLA achieves performance comparable to centralized training in both full-model training and parameter-efficient fine-tuning settings.

---

## 5. Towards High-DoF Dexterous Manipulation through VLA Post-Training

**Authors:** Junlei Zhu, Shenzhe Yao, Chaogui Huang, ..., Jiahao Chen, Yide Liu
**arXiv:** [2609.19666](https://arxiv.org/abs/2609.19666)
**Categories:** Robotics (cs.RO)

Imitation-learned vision--language--action (VLA) foundation models acquire broad manipulation capabilities by scaling robot data across tasks and embodiments, but reliable deployment on a specific downstream task and hardware platform still requires post-training. Dexterous hands make this adaptation particularly difficult: their broad behavioural repertoire and high degree of freedom create a large and structured action space. Three obstacles are central: open-source VLAs do not natively provide an action interface for high-DoF hands; gesture mismatch during human-gated DAgger takeover creates command discontinuities and contaminates corrective trajectories; and reinforcement learning in the raw joint space is sample-inefficient. We present a unified four-step post-training pipeline comprising a learned temporal hand-action codec, supervised fine-tuning, DAgger, and real-world residual reinforcement learning. The codec adapts a pretrained VLA to absolute dexterous-hand commands. Buffered rollback, pose alignment, and smooth command blending enable continuous, task-relevant DAgger corrections, while latent residual RL confines exploration to coordinated hand motions captured by the codec. We evaluate the pipeline on five diverse real-world tasks spanning bimanual transfer, in-hand reorientation, and tool use. Within the reported post-training budgets, the resulting policies achieve 100\% success on every evaluated task over 20 trials per task. These results provide a practical path for adapting VLA foundation models to reliable real-world dexterous manipulation.

---

## 6. Recovering Aggressively Pruned Vision-Language-Action Models with Offline Hidden-State Distillation

**Authors:** Chiyoung Kim, Sanghyuk Roy Choi, Minhyeok Lee
**arXiv:** [2609.19579](https://arxiv.org/abs/2609.19579)
**Categories:** Robotics (cs.RO)

Vision-language-action (VLA) models let robots follow language instructions, but their language backbones of several billion parameters are the main obstacle to running them on robot hardware. Structured pruning reduces that backbone, and removing 63% of it from OpenVLA-OFT drops LIBERO-Long success from 93.2% to 0.8%. A recent approach restores such a model with supervised fine-tuning followed by reinforcement learning, which needs online rollouts and hundreds of GPU-hours. We recover most of the lost success entirely offline. Width pruning narrows the blocks but keeps the residual stream at its original size, so teacher and student hidden states have the same shape and are matched directly, without a projector. Training against a cache built in one teacher pass lifts the 63%-reduced student to within 3.5 points of the teacher in about 8 GPU-hours. A sweep over nine ratios locates where the recovery objective starts to matter. Up to 45% reduction the two do not differ significantly on OpenVLA-OFT. Hidden-state distillation then adds +2.1 to +4.5 points there between 63% and 87%, and +9.4 to +22.1 points on CogACT from 63% onward. At 81% on CogACT, a tripled recovery budget narrows the distilled student's gap to the teacher to 3.9 points on average, while supervised recovery stays more than 20 points below. At matched compression, width pruning yields higher success and depth pruning lower latency. On a 6-DoF manipulator, the distilled student at 72% reduction reaches 77.5% success against 59.5% for supervised recovery, runs 2.23x faster on-board than the teacher, and uses 62% less memory.

---

## 7. FASA: Feedback-Aware Sampling Adaptation for Efficient Diffusion-Based VLA Models

**Authors:** Yuchen Han, Jianhan Wu, Xiaoyang Qu, ..., Shiyi Li, Jianzong Wang
**arXiv:** [2609.19475](https://arxiv.org/abs/2609.19475)
**Categories:** Robotics (cs.RO)

Diffusion-based Vision-Language-Action (VLA) models achieve strong performance in embodied tasks, but their iterative sampling imposes heavy computational and memory-access cost, blocking real-time deployment on edge platforms. Existing acceleration methods either require expensive training (e.g., distillation, flow matching) or degrade perception via statically scheduled pruning and caching, ignoring the dynamic workload variance of robotic interactions. This paper presents FASA (Feedback-Aware Sampling Adaptation), a training-free runtime framework that treats real-time multimodal feedback as a control signal for the denoising pipeline: an interaction-driven range adaptor modulates the global sampling-step budget based on visual and gripper-force feedback, and a proprioception-aware step adaptor pinpoints the optimized step within the adapted range. This co-designed framework allows the underlying hardware architecture to adaptively match the workload demands of different execution phases. Comparative evaluations across several benchmarks show that the inference speed can be increased by up to 1.45$\times$ while maintaining competitive success rates, providing a novel dynamic runtime architecture paradigm for deploying heavy generative embodied AI workloads onto resource-constrained computing platforms.

---

## 8. Beyond Patch Removal: Persistent Adversarial Effects in Vision-Language-Action Policies

**Authors:** Enhao Wu, Fusen Guo, Yuxin Cao, ..., Lin Li, Wei Song
**arXiv:** [2609.19669](https://arxiv.org/abs/2609.19669)
**Categories:** Computer Vision and Pattern Recognition (cs.CV); Robotics (cs.RO)

Adversarial patches to Vision-Language-Action (VLA) policies can cause both immediate action corruption and persistent state effects that remain after the patch is removed. Existing evaluations largely focus on continuous attacks and do not separate these two effects. We introduce a state-restoration protocol that removes the patch at matched action-chunk boundaries and measures subsequent recoverability under the same remaining step budget. Clean, random-patch, deviation-matched, and fixed-direction controls distinguish adversarial effects from occlusion, action-error magnitude, and directional persistence. We also evaluate a recovery adapter trained on attack-induced states under controlled intervention latency. On OpenVLA-OFT with EDPA attacks, only 36.2% of LIBERO-Long episodes remain recoverable after five chunks, compared with 89.9% and 87.0% for the deviation-matched and fixed-direction controls. Similar persistent effects are observed on autoregressive OpenVLA. The recovery adapter improves recovery from 7.7% to 47.4% at one-chunk latency, but its benefit decreases substantially with delayed intervention. These results show that adversarial effects can persist after patch removal and that timely intervention is critical for recovery.

---
