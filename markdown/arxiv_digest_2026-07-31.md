# arXiv Daily Digest — 2026-07-31

**Mode:** direct
**Categories:** cs.AI, cs.LG, cs.RO, cs.CV
**Keywords:** VLA, world model, world action model
**Papers found:** 12

---

## 1. QuantWAMs: Calibrating at the Right Granularity for World Action Models

**Authors:** Jiacheng Zhou, Jinfan Lv, Ruixuan Li, ..., Wenqiang Zhang, Lizhe Qi
**arXiv:** [2607.28405](https://arxiv.org/abs/2607.28405)
**Categories:** Artificial Intelligence (cs.AI); Machine Learning (cs.LG)

World Action Models (WAMs) jointly predict future observations and actions, but their iterative denoising and closed-loop execution make efficient deployment costly. Existing post-training quantization (PTQ) methods are poorly suited to WAMs because they rely on open-loop objectives, homogeneous model assumptions, and calibration distributions that do not reflect deployment. We present QuantWAMs, a PTQ framework that aligns quantization decisions with the calibration context defined by model structure, rollout distribution, and task objective. QuantWAMs introduces three strategies: shared-basis outlier calibration, which pools activation evidence only across coordinate-compatible modules; co-training-objective saliency, which computes empirical-Fisher scores from the joint video--action gradient and assigns weight precision at a calibration-stable layer granularity; and fixed-intervention rollout auditing, which revises denoising-step protection schedules using reachable closed-loop states without changing the precision budget. We evaluate QuantWAMs on Fast-WAM and LingBot-VA across RoboTwin 2.0, LIBERO, and real-robot manipulation with an AgiBot G2. Under a W4A4-dominant setting, the reported simulation means differ from FP16 by 0.2--0.7 percentage points. Real-robot trials further establish deployment feasibility on three manipulation tasks. For the targeted video and action blocks, QuantWAMs reduces peak weight-and-activation memory to about 29\% of FP16 and provides 1.4--1.6$\times$ block-level speedups.

---

## 2. Tycho: Active Abstraction with Programmatic World Models for ARC-AGI-3

**Authors:** Jens Lehmann, Andrei Aioanei, Sahar Vahdati
**arXiv:** [2607.28287](https://arxiv.org/abs/2607.28287)
**Categories:** Artificial Intelligence (cs.AI); Computer Vision and Pattern Recognition (cs.CV); Symbolic Computation (cs.SC)

ARC-AGI-3 turns abstraction into an interactive problem of skill acquisition. A player must infer an unfamiliar game's rules, hidden state, and goal while maintaining action efficiency because every move counts. We formalize these environments as parameterized rendered deterministic Moore machines and introduce Tycho, a coding-agent system that constructs and uses game-specific models during interaction. Tycho separates actionable observations from intermediate animation, level-completion, and game-over frames. From this structured history, an agent can model, test, plan with, repair, or bypass a free-form executable hypothesis.
In one matched public-set run per policy, we compare four orchestration policies on all 25 public games using Claude Opus 4.8 under matched inference budgets. Actor-requested delegation to a model builder obtains the highest observed mean Relative Human Action Efficiency (RHAE), 88.49. With this selected policy, GPT-5.6 Sol and Opus 5 both reach 100.00 RHAE and complete all 183 levels. Their game-balanced first-run human-replay midranks are 98.5 and 100.0. Opus 5 uses 61% fewer scored actions than the aggregate official human baselines.
Automatic repair after verification failures produces models that reproduce observed transitions much more accurately, yet reaches only 83.07 RHAE. Transition match indicates whether a simulator reproduces observed dynamics, not whether it has identified the objective or improves the next action. Strong play also requires deciding when to construct, repair, use, or bypass a model. We call this joint problem active abstraction: generating a testable model from costly interaction and deciding when acquiring or using it is worth its cost.

---

## 3. World Action Planner: Generalizable Decision-Making with Action-Conditioned World Models

**Authors:** Xiangcheng Zhang, Yilun Du
**arXiv:** [2607.27599](https://arxiv.org/abs/2607.27599)
**Categories:** Artificial Intelligence (cs.AI); Robotics (cs.RO)

Building generalizable agents for diverse applications remains a fundamental challenge. While imitation learning-based policies succeed in specific training environments, they often fail to generalize to novel scenes and tasks. In this work, we propose World Action Planner, a robot planning system that leverages the reasoning capabilities of Vision-Language Models (VLMs) and the physical grounding of a multi-task pose-image conditioned world model. Our system enables an agent to propose initial action plans and iteratively refine them via optimization and search, reasoning over imagined world model rollouts. We demonstrate that our approach achieves superior performance across compositional tasks, new layouts, and zero-shot generalization scenarios, significantly outperforming state-of-the-art end-to-end policy models such as VLAs and WAMs. Project website at this http URL

---

## 4. QQWorld: Quantile-Quantile Matching for World Model Regularization

**Authors:** Zhoushun Yu, Xiaoyu Hu, Xiangyu Xu
**arXiv:** [2607.28415](https://arxiv.org/abs/2607.28415)
**Categories:** Machine Learning (cs.LG); Artificial Intelligence (cs.AI); Computer Vision and Pattern Recognition (cs.CV); Multimedia (cs.MM); Robotics (cs.RO)

Latent world models enable efficient planning by predicting future states in a compact representation space, but their performance depends critically on the quality of the learned latent distribution. LeWorldModel (LeWM) regularizes its latents toward an isotropic Gaussian using the Epps-Pulley (EP) objective. We show that the corrective gradients of EP rapidly vanish for isolated tail samples, leaving heavy-tailed deviations insufficiently controlled. To address this limitation, we propose QQWorld, which replaces EP with a quantile-quantile matching objective that directly aligns projected latent samples with rank-matched Gaussian quantiles, thereby maintaining effective corrective gradients in the tails. We further develop cross-batch QQ, which enlarges the effective ranking pool using detached samples from previous batches, and characterize its bias-variance trade-off. Across four control environments, QQWorld effectively improves the average planning success rate of LeWM, while consistently yielding better Gaussian alignment and thinner latent tails.

---

## 5. ShadowDancer: Teaching Video World Models Any Action by Learning Unified Dynamics Representations from a Video and Its Shadow

**Authors:** Jin Cao, Zian Meng, Kaipeng Zhang
**arXiv:** [2607.28362](https://arxiv.org/abs/2607.28362)
**Categories:** Computer Vision and Pattern Recognition (cs.CV); Artificial Intelligence (cs.AI); Machine Learning (cs.LG)

We present ShadowDancer, a novel approach to any-action, frame-level control of interactive video world models. The obstacle is representational: existing interfaces either encode an action loosely, leaving how it unfolds for the model to improvise, or encode it exactly through structured signals that serve one family and are hard to acquire, so precise control across diverse dynamics remains impractical. Demonstration videos are the natural remedy, specifying any dynamics frame by frame; yet a video shows its dynamics only through one particular appearance, a single shadow of the underlying dynamics, so actions learned from demonstrations transfer poorly to new scenes. ShadowDancer addresses this with two key innovations: (1) shadow pairs, video pairs that replay the same dynamics under independently resampled appearance, constructed at scale by our Shadow Library, so that a dynamics family becomes controllable exactly when such pairs can be constructed for it; and (2) cross-shadow prediction, which learns actions by predicting one shadow from the other, so that whatever the pairing resamples is discarded by construction and whatever it preserves becomes the action, yielding a unified dynamics representation that drives a block-causal world model. Any demonstrated clip thus becomes a reusable action asset, replayed in new environments without action labels, motion estimators, or fine-tuning. Experiments demonstrate improved action transfer and long action rollout over strong latent-action and interactive world model baselines across diverse dynamics families, with an average blinded win rate of 86% in rollout comparisons. We show video results at this https URL

---

## 6. EgoGenesis: Egocentric World-Action Modeling with Online Anchored Projective Memory and Action-3D RoPE

**Authors:** Zexuan Yan, Yuzhou Wu, Yue Ma, ..., Jinghong Liu, Linfeng Zhang
**arXiv:** [2607.28243](https://arxiv.org/abs/2607.28243)
**Categories:** Computer Vision and Pattern Recognition (cs.CV); Artificial Intelligence (cs.AI)

Egocentric video offers rich manipulation experience for embodied AI, yet collecting diverse egocentric data across scenes, objects, motions, and embodiments remains costly. We present \method, an egocentric world-action simulator that synthesizes controllable, high-quality manipulation videos to expand scarce real-world training data. \method{} builds on a pretrained video generation prior and introduces two geometry-aware conditioning mechanisms. Online Anchored Projective Memory (OAPM) preserves a first-frame 3D scene anchor while periodically refreshing a recent state during autoregressive generation. Action-3D Rotary Position Embedding (A3D-RoPE) encodes end-effector motion with camera-aware 3D rotary coordinates, injecting action geometry into skeleton-to-video cross-attention for precise control. Together, these components improve visual fidelity, geometric stability, and action alignment in long egocentric rollouts. Moreover, augmenting 400 real trajectories with 400 \method-generated trajectories improves out-of-distribution real-robot success from 77\% to 84\% on single-arm tasks and from 53\% to 70\% on dual-arm tasks, demonstrating that the synthesized data substantially improve downstream WAM generalization.

---

## 7. Security of World-Model-Based Embodied AI: A Lifecycle of Threats, Defenses, and Evaluation

**Authors:** Fazhong Liu, Zhuoyan Chen, Haozhen Tan, ..., Guoxing Chen, Haojin Zhu
**arXiv:** [2607.28226](https://arxiv.org/abs/2607.28226)
**Categories:** Cryptography and Security (cs.CR); Artificial Intelligence (cs.AI)

World models give embodied AI a predictive core: they compress observations into states, simulate action-conditioned futures, and enable planning beyond reactive control. This predictive layer, however, opens a new security boundary-compromise can propagate from data, sensors, prompts, or feedback into physical action. Rather than treating world models as an isolated component, this survey traces threats across their entire lifecycle-from data construction and representation learning, through state grounding and imagination, to trajectory evaluation, execution, and long-term adaptation via memory and tools. We show that familiar attack families: poisoning, backdoors, adversarial examples, sensor spoofing, prompt injection, trajectory manipulation, and supply-chain attacks take on distinct meanings when they corrupt world states, learned dynamics, affordance estimates, or safety costs. We also highlight a duality: world models can serve as runtime safety shields, yet when compromised or over-trusted they generate predictive safety illusions. The survey offers a lifecycle taxonomy, maps existing attacks to world-model security properties, outlines evaluation protocols for safety failures, and structures defenses across provenance, robust grounding, uncertainty-aware prediction, trajectory gating, feedback auditing, and deployment assurance.

---

## 8. RedFlow: Redirect Failure into Action-Level Corrections for Flow-matching VLA Policy

**Authors:** Zhengyang Yan, Junhao Li, Fangqi Zhu, ..., Zicong Hong, Song Guo
**arXiv:** [2607.27782](https://arxiv.org/abs/2607.27782)
**Categories:** Robotics (cs.RO); Artificial Intelligence (cs.AI)

Flow-matching Vision-Language-Action (VLA) policies have shown strong potential for robotic manipulation but often suffer from compounding errors caused by distribution shifts during deployment. While offline reinforcement learning (RL) provides a practical way to improve deployed policies using rollout data, existing methods either ignore failure data or exploit it only at the trajectory level, resulting in low learning efficiency and persistent errors. We propose **RedFlow**, a fine-grained offline RL framework that redirects failure experiences into action-level corrective supervision for flow-matching VLA policies. RedFlow consists of two key components: (1) a **Context-Aware Corrective Matching** mechanism that identifies failure-inducing actions and retrieves successful alternatives from similar contexts as corrective targets, and (2) an **Adaptive Redirection Objective** that jointly reinforces successful actions, suppresses undesirable ones, and redirects recoverable failures toward corrective targets. By converting both successful and failed experiences into dense supervision, RedFlow enables robust recovery learning from mixed-quality data. Experiments on the LIBERO benchmark and three real-world manipulation tasks show that RedFlow consistently outperforms state-of-the-art offline RL baselines, improving the real-world success rate from 56.7% to 74.7%. It also matches strong on-policy methods (PPO, GRPO, and DDPO) while requiring roughly an order of magnitude fewer training samples.

---

## 9. TacWAM: Anchor-Guided World Action Model with Mechanics-Aware Tactile Prediction

**Authors:** Lei Jin, Yiding Ma, Xin Zhang, ..., Wei Wu, Yong Li
**arXiv:** [2607.28391](https://arxiv.org/abs/2607.28391)
**Categories:** Robotics (cs.RO)

World Action Models (WAMs) combine future-state prediction with robot action generation, but existing approaches largely rely on visual futures. Visual prediction captures scene structure and object motion, yet provides limited supervision for force, deformation, shear, and slip during contact-rich manipulation. This creates two design requirements: tactile futures should carry meaningful physical information, and they should not become privileged cues for action generation. We present TacWAM, a mechanics-aware tactile WAM that addresses this challenge in three steps. First, a Spatially Aligned Fusion (SAF) Tactile Encoder maps tactile appearance, dense force fields, and deformation flow into a shared latent prediction space, with bilateral force and torque reconstruction preserving global contact information. Second, a tactile history encoder provides temporal context so future tactile prediction reflects how force and deformation change beyond the current tactile observation. Third, Anchor-Guided Tri-Modal (AGT) Attention separates current visual and tactile anchors, future prediction tokens, and action tokens, allowing future tactile states to supervise training without being directly read by the action branch. We evaluate TacWAM on four real-world contact-rich manipulation tasks covering fragile grasping, sustained surface contact, and dynamic in-hand manipulation. TacWAM achieves an average success rate of 75.0%, exceeding the strongest evaluated baseline by 37.5 percentage points. Staged ablations show consistent degradation when tactile history is removed and access to future prediction targets is relaxed. These results indicate that future tactile supervision can improve contact-aware action learning when combined with informative tactile representations and deployment-consistent information constraints.

---

## 10. Failure Detection for Surgical Robot Imitation Policies via Flow-Matching World Modeling

**Authors:** Zhefeng Huang, Yilin Cai, Ankit Patel, ..., Brendan Browne, Yue Chen
**arXiv:** [2607.27511](https://arxiv.org/abs/2607.27511)
**Categories:** Robotics (cs.RO)

Imitation learning has shown increasing promise for autonomous robotic surgery, yet safe deployment remains challenging due to the safety-critical nature of surgical tasks and the complexity and variability of surgical environments. Failure detection is therefore an essential safeguard, but its development remains difficult due to the challenges of scarce failure data, highly variable manipulation dynamics, and the need to balance missed detections against disruptive false alarms. To address these challenges, we introduce FoMo-FD (Flow-Matching World Model for Failure Detection), a failure detection method that learns nominal short-horizon visual dynamics with an action-conditioned flow-matching world model. FoMo-FD scores the inverse-transport nonconformity of observed endpoint latents, enabling window-level detection of visual-action inconsistencies without requiring failure demonstrations. Detection thresholds are obtained by conformal calibration on successful executions, yielding task-specific alarms without assuming future failure types. We evaluate FoMo-FD on four surgically relevant manipulation tasks with twenty failure modes across simulation and real-world experiments using the da Vinci Research Kit (dVRK). Results show that FoMo-FD outperforms observation-level anomaly baselines and a prediction-error variant of the same world model, with the wrist-camera view achieving the strongest performance, including a 96.6% failure detection rate (FDR) at a 1.3% false alarm rate (FAR).

---

## 11. PhiZero: A World Model Built Around Physical Language

**Authors:** Shuyao Shang, Yuqi Wang, Ruopeng Gao, ..., Lue Fan, Zhaoxiang Zhang
**arXiv:** [2607.28624](https://arxiv.org/abs/2607.28624)
**Categories:** Computer Vision and Pattern Recognition (cs.CV)

We introduce PhiZero, a physical world model built around physical language, a compact discrete representation of world-state transitions. Existing physical world models typically predict future videos directly in pixel space, leaving the underlying world dynamics implicit within high-dimensional visual predictors. Motivated by humans' ability to abstract predictive structure from visual experience and organize it in natural language for explicit reasoning, we learn physical language from in-the-wild videos through self-supervision and use it to explicitly reason about how the physical world evolves. Accordingly, PhiZero adopts a reason-then-render paradigm: it first infers future world evolution as a physical-language sequence and then renders the inferred transitions into videos. Extensive experiments across generation and understanding benchmarks validate the ability of PhiZero to model physically coherent world evolution. We further show its potential for realistic and interactive world modeling, fine-grained action-conditioned simulation, and zero-shot motion transfer.

---

## 12. AuricularWorld: Hierarchical Action-Guided World Modeling for Fine-Grained Auricular Structure Segmentation from CT Scans

**Authors:** Jingwen Yang, Senmao Wang, Luoyao Kang, ..., Lin Lin, Haiyue Jiang
**arXiv:** [2607.28487](https://arxiv.org/abs/2607.28487)
**Categories:** Computer Vision and Pattern Recognition (cs.CV)

Fine-grained segmentation of auricular structures in CT is challenging because the ear occupies a small image region, cartilage boundaries are highly irregular, and interfaces between cartilage and surrounding soft tissues are often ambiguous. Clinical annotations may also include both composite structures containing cartilage and adjacent skin and their corresponding cartilage-only regions, producing nested and overlapping labels. We propose a world-model-based segmentation framework that enables iterative anatomical reasoning beyond conventional feed-forward prediction. Built on an encoder-decoder architecture, the framework introduces a deterministic recurrent state-space model into the intermediate latent space. Multi-scale encoder features and partially decoded representations are fused to form a structural observation that initializes the latent dynamics. During inference, the model performs a three-step latent rollout without ground-truth guidance. Hierarchical anatomical actions update the recurrent state and progressively refine the latent representation. The resulting latent trajectory is projected back into the decoder and combined with high-resolution features to produce the final segmentation. To learn reliable latent transitions, we introduce a balanced hierarchical action objective that addresses foreground sparsity, missing anatomical groups, and imbalance between add and remove operations. Extensive experiments show that the proposed framework consistently improves segmentation accuracy and reduces HD95 by more than 43% for small, irregular, and overlapping auricular structures in CT. These results demonstrate the effectiveness of latent world-model reasoning for challenging medical image segmentation.

---
