# arXiv Daily Digest — 2026-08-20

**Mode:** direct
**Categories:** cs.AI, cs.LG, cs.RO, cs.CV
**Keywords:** VLA, world model, world action model
**Papers found:** 8

---

## 1. DA-WAM: Decision-Aligned Future Latents for Driving World Models

**Authors:** Ruiguo Zhong, Benshan Ma, Xiaolong Chen, ..., Pei Liu, Jun Ma
**arXiv:** [2608.19085](https://arxiv.org/abs/2608.19085)
**Categories:** Robotics (cs.RO); Artificial Intelligence (cs.AI)

Anticipating how scenes evolve under ego actions is fundamental to safe autonomous driving, yet the full potential of world models for decision-making remains unrealized. The critical challenge lies in ensuring that future modeling is not merely predictive, but decision-informative: the predicted future must directly shape which trajectory is selected. Existing approaches decouple future representation learning from planning optimization, or share predicted states across trajectory candidates, thereby diluting the action-specific consequences that ought to guide selection. To bridge this gap, we propose DA-WAM, a framework that unifies predictive representation learning, action-conditioned future modeling, and trajectory scoring under a single decision-making objective. DA-WAM maintains predictive supervision throughout planner optimization via an online encoder and a stable momentum target, allowing future representations to co-evolve with the driving task. An action-conditioned predictor generates a distinct future latent state per trajectory candidate, which is then evaluated by a future-latent-conditioned factorized scorer. For the expert-matched trajectory, the predicted future latent is supervised by the observed future representation, while safety-critical hard negatives provide additional supervision near planning boundaries. Extensive experiments on NAVSIM-v1 and NAVSIM-v2 demonstrate state-of-the-art performance, while ablations and diagnostic analyses validate the key components.

---

## 2. GS-VLA: Plug-and-Play Viewpoint Canonicalization for Frozen VLA Policies via Gaussian Splatting

**Authors:** Yechan Park, HyunJin Kim
**arXiv:** [2608.19066](https://arxiv.org/abs/2608.19066)
**Categories:** Computer Vision and Pattern Recognition (cs.CV); Artificial Intelligence (cs.AI)

This paper proposes a lightweight, plug-and-play framework that improves robustness to viewpoint shifts in Vision-Language-Action (VLA) policies without policy retraining. To our knowledge, this is the first approach to directly leverage 3D Gaussian-based novel-view synthesis for observation-space adaptation in VLA policies. Current VLA performance relies on the implicit assumption that training and deployment camera configurations are identical. Our experiments show that even a small displacement of the camera mount can reduce the success rate on the LIBERO benchmark from about 90% to about 10% in the worst case. Prior approaches, such as large-scale fine-tuning or generative data augmentation, are computationally expensive and risk catastrophic forgetting. To address this, viewpoint shifts are reformulated as a localized novel-view synthesis problem. Under a Locality assumption, that camera perturbations remain within a small bounded region relative to the workspace, viewpoint normalization reduces to a scene- and policy-independent disocclusion task. Our work implements this idea with a 4M-parameter 3D-Gaussian canonicalizer prepended to a frozen VLA policy. Without modifying policy weights, GS-VLA improves performance across three orthogonal axes: (1) Policy architectures, (2) Unseen task suites, and (3) Perturbation scales. These results show that a lightweight visual module can recover a large fraction of the performance lost under viewpoint shift, without policy retraining.

---

## 3. Partition the Support, Reconstruct the Residual: Training-Free Sparse Attention for Video Generation and World Models

**Authors:** Pardis Taghavi, Reza Langari, Gaurav Pandey
**arXiv:** [2608.18484](https://arxiv.org/abs/2608.18484)
**Categories:** Computer Vision and Pattern Recognition (cs.CV); Artificial Intelligence (cs.AI); Machine Learning (cs.LG)

Training-free block-sparse attention can accelerate video transformers, but row-wise attention concentration does not by itself specify an executable sparse operator. Queries sharing a block route may have poorly overlapping supports, while retained attention mass alone does not determine the post-softmax error from skipped interactions. We show that partition geometry affects both pooled support and the predictability of the remaining residual from the sparse output. We introduce SparsePR, which combines Response-Coupled Partitioning with Probe-Fitted Residual Reconstruction. Sampled-query key responses form paired K/V groups, whose centroids induce query-response coordinates for shared routing. A small set of exact query rows then calibrates a call-specific affine correction from the sparse output within the output subspace observed in the probe residuals. Across four heterogeneous video generation and world models, SparsePR consistently reduces attention-reconstruction error. Ablations show that probe fitting accounts for most of this reduction, while response-coupled partitioning lowers hard-drop error and improves reconstruction under a finite probe budget. SparsePR preserves generation quality at 22.0-26.0% realized executed-pair density while achieving 1.48x-2.61x end-to-end speedups. Project page: this https URL

---

## 4. GigaBrain-WBC-0.5: A Behavior World Model for Robust Whole-Body Control with Environment Interaction

**Authors:** Ziyang Cheng, Tianshu Tang, Jinxin Lan, ..., Zheng Zhu, Jiwen Lu
**arXiv:** [2608.18234](https://arxiv.org/abs/2608.18234)
**Categories:** Robotics (cs.RO); Artificial Intelligence (cs.AI); Machine Learning (cs.LG)

Whole-body motion tracking policies turn a humanoid into a robust control interface: the teleoperator---or an upstream model---only supplies a coarse movement intent, while the low-level policy keeps the robot balanced and physically feasible. Existing trackers deliver this interface only on flat ground: trained in empty scenes, they never learn how contact with terrain and objects reshapes their dynamics, and they attempt to teach the policy to balance under any command by continually enlarging the reference-motion corpus, which stops working once feasible behaviors become environment-dependent. We present GigaBrain-WBC-0.5, the first Behavior World Model (BWM) for humanoid whole-body control. Rather than a purely reactive tracker, we train a causal Transformer to jointly predict its next action, next state, and the distribution over its next latent behavior command, so the network that acts also models how the environment shapes what it can do next. An automatic terrain-annotation pipeline recovers full 3D contact geometry from retargeted motion, enabling terrain annotation at the scale of existing motion datasets. The predicted distribution is reused at deployment to detect implausible commands online and retract them onto learned behaviors, so the robot attempts tasks in a "best-effort" manner. The result is a unified policy that takes real-time command, interacts with environment, and stays robust to implausible commands, falls, and disturbances. GigaBrain-WBC-0.5 achieves the highest success rate across all four regimes among three large-scale tracker baselines: 81.3% on terrain interaction (4.3x the strongest baseline), 83.1% under implausible commands, and 99.3% fall recovery (16.8x the strongest baseline). Hardware trials show robust interaction under missing supports and disturbances; the Unitree G1 checkpoint transfers to the Maker L01 robot with simple fine-tuning.

---

## 5. Decision-Metric Alignment in Latent World Models: Diagnostics and Action-Conditioned Objectives for MPC Planning

**Authors:** Jiawei Wang, Ke Rui, Yushen Zuo, Yichun Feng, Minglei Li
**arXiv:** [2608.18746](https://arxiv.org/abs/2608.18746)
**Categories:** Machine Learning (cs.LG); Computer Vision and Pattern Recognition (cs.CV)

JEPA-style latent world models can use Euclidean distance to a goal latent as the cost for model-predictive control (MPC). Strong decoding of task variables, however, does not guarantee that this particular cost ranks candidate action sequences by real task progress. We call the latter property \emph{decision-metric alignment}. We introduce Plan-Real Spearman, which measures latent--real rank agreement on random plans, and CEM-stage Spearman, which measures the same agreement as cross-entropy-method (CEM) search concentrates its proposal. We analyze sufficient conditions under which latent distance preserves real-cost rankings, identifying encoder distortion, terminal rollout error, and candidate margins as the controlling quantities. Guided by the observed empirical alignment gap, DA-LeWM augments LeWM with inverse-dynamics and demonstration-conditioned goal-action heads. Across all our experiments, DA-LeWM accelerates convergence and achieves higher online success than LeWM, while probe scores remain similar. These results show that action-conditioned objectives improve the geometry used by Euclidean-cost, CEM-based latent MPC.

---

## 6. Reinforced Planning with Latent World Models

**Authors:** Armin Sommer, Jannik Schilling
**arXiv:** [2608.18669](https://arxiv.org/abs/2608.18669)
**Categories:** Machine Learning (cs.LG)

Humans solve complex problems by constructing plans and mentally simulating their outcomes with an internal model of the world. Machine learning has produced world models that similarly predict the outcomes of action sequences, but the improvement of candidate plans still isn't fully learned. Current planners are either hand-designed, distilled from a hand-designed optimizer, or learned only to inform an amortized policy rather than to revise the plan itself. We introduce the Reinforced Planning, a method based on the idea that search can be learned by reinforcing good search rules into a neural planner. Our implementation RP1 learns both how to evaluate imagined outcomes through a critic, as well as how to improve multi-step plans through an optimizer trained fully offline from imagined world-model roll-outs. To our knowledge, RP1 is the first method to fully learn how to improve multi-step plans. Furthermore, it can be trained independently of and attached to any pretrained latent world model. Across visual navigation, arm reaching, and robotic manipulation on two world-model backbones, RP1 substantially outperforms hand-designed search algorithms, reaching near-perfect success in several settings while using $1,000 \times$ less world-model rollouts and being up to $67 \times$ faster than the strongest alternative under concurrent planner inference.

---

## 7. Role-Conditioned Sub-Token Routing for Efficient Vision-Language-Action Policies

**Authors:** Wei Jiang, Wei Wang
**arXiv:** [2608.18410](https://arxiv.org/abs/2608.18410)
**Categories:** Machine Learning (cs.LG)

Vision-Language-Action (VLA) models process long multimodal token sequences, making inference expensive in both memory and computation. Existing efficiency methods mainly reduce visual tokens, but aggressive token pruning becomes fragile because removing a token discards its entire representation. Sub-token compression provides a complementary alternative by retaining more tokens while reducing their value width. However, directly applying sub-token compression to VLA policies is less effective because information important for perception, language understanding, and control is distributed differently across the multimodal representation.
We introduce Role-Conditioned Sub-Token Routing (RoleSub), which learns how to compress the value representations of retained tokens. After visual token reduction, RoleSub partitions each retained value representation into groups in an orthogonal space and uses a lightweight router to determine which groups should be preserved. The routing decision is conditioned on the token representation, a learned latent role representation, and language context. The same mechanism can also be applied to language values, allowing visual and language representations to be compressed without removing additional tokens.
We evaluate RoleSub on OpenVLA-OFT-7B across the four LIBERO suites. At matched visual-KV budgets, RoleSub outperforms a trained token-only control in 33 of 36 settings, with the largest gains under aggressive compression. Combining visual and language compression reduces total KV to 9.2--11.3% of the original while retaining strong control performance on most tasks. These results show that reducing the representation within retained tokens provides an effective complement to token pruning for aggressive VLA compression.

---

## 8. Progressive Experience Fusion for Multi-Task World Model Control in Endovascular Navigation

**Authors:** Harry Robertshaw, Maxence Boels, Nikola Fischer, ..., Alejandro Granados, Thomas C Booth
**arXiv:** [2608.18647](https://arxiv.org/abs/2608.18647)
**Categories:** Robotics (cs.RO); Machine Learning (cs.LG)

Autonomous endovascular navigation could support the delivery of mechanical thrombectomy to underserved areas, but controllers must navigate long, multi-stage paths across varying vascular anatomies. This study investigates Progressive Experience Fusion (PEF) to train a multi-task TD-MPC2 controller. We additionally evaluate a heuristic that changes the Model Predictive Path Integral planning horizon using residual action-sequence dispersion, and fine-tuning in a patient-specific simulation. Across five subtasks in ten known training anatomies with held-out targets, PEF achieved a mean success rate of 74%, compared with 37% for Soft Actor-Critic (p < 0.001) and 65% for base TD-MPC2 (p = 0.053). A PEF controller with adaptive-horizon planning trained on 30 vasculatures achieved a mean success rate of 90% in ten held-out vasculatures. The PEF agent successfully transferred to an unseen in vitro stroke patient vasculature under fluoroscopy, achieving a mean path ratio improvement from 63% to 80% with fine-tuning (p < 0.001), following 40x103 fine-tuning steps (corresponding to approximately 107 min of clinical inter-hospital transfer time). This work represents a proof of concept for multi-vasculature training and patient-specific adaptation, while further validation is required before clinical deployment.

---
