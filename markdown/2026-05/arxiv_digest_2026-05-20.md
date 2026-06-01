# arXiv Daily Digest — 2026-05-20

**Mode:** direct
**Categories:** cs.AI, cs.LG, cs.RO, cs.CV
**Keywords:** VLA, world model, world action model
**Papers found:** 15

---

## 1. HalluWorld: A Controlled Benchmark for Hallucination via Reference World Models

**Authors:** Emmy Liu, Varun Gangal, Michael Yu, ..., Sachin Kumar, Steven Y. Feng
**arXiv:** [2605.19341](https://arxiv.org/abs/2605.19341)
**Categories:** Computation and Language (cs.CL); Artificial Intelligence (cs.AI); Machine Learning (cs.LG); Machine Learning (stat.ML)

Hallucination remains a central failure mode of large language models, but existing benchmarks operationalize it inconsistently across summarization, question answering, retrieval-augmented generation, and agentic interaction. This fragmentation makes it unclear whether a mitigation that works in one setting reduces hallucinations across contexts. Current benchmarks either require human annotation and fixed references that may be memorized, or rely on observations in settings that are difficult to reproduce. To study root causes, we introduce HalluWorld, an extensible benchmark grounded in an explicit reference-world formulation: a model hallucinates when it produces an observable claim that is false with respect to this world. Building on this view, we construct synthetic and semi-synthetic environments in which the reference world is fully specified, the model's view is controlled, and hallucination labels are generated automatically. HalluWorld spans gridworlds, chess, and realistic terminal tasks, enabling controlled variation of world complexity, observability, temporal change, and source-conflict policy, and disentangling hallucinations into fine-grained error categories. We evaluate frontier and open-weight language models across these settings and find consistent patterns: perceptual hallucination on directly observed information is near-solved for frontier models, while multi-step state tracking and causal forward simulation remain difficult and are not generally solved by extended thinking. In the terminal setting, models also struggle with when to abstain. The uneven profile of failures across probe types and domains suggests that hallucinations arise from distinct failure modes rather than a single capability. Our results suggest that controlled reference worlds offer a scalable and reproducible path toward measuring and reducing hallucinations in modern language models.

---

## 2. DEFLECT: Delay-Robust Execution via Flow-matching Likelihood-Estimated Counterfactual Tuning for VLA Policies

**Authors:** Yixiang Zhu, Yonghao Chen, Rui Meng, ..., Taowen Wang, Xinyu Chen
**arXiv:** [2605.19294](https://arxiv.org/abs/2605.19294)
**Categories:** Robotics (cs.RO); Artificial Intelligence (cs.AI)

Vision-Language-Action (VLA) policies are typically deployed with asynchronous inference: the robot executes a previously predicted action chunk while the model computes the next one. This creates a prediction-execution misalignment: the chunk is conditioned on the observation taken before inference began, but executes in a physical state that has already drifted forward by several control steps; naive asynchronous rollover collapses from 89% to under 1% on Kinetix as the inference cycle covers up to seven control steps. We introduce DEFLECT, a fully offline post-training refinement that applies as a near drop-in upgrade to existing async-VLA stacks by converting latency itself into a label-free preference signal: counterfactual fresh/stale action pairs are constructed from a frozen reference policy and scored under the deployment-time conditioning via an implicit flow-matching likelihood-ratio surrogate, with no human labels, reward models, or online rollouts. DEFLECT substantially extends the usable delay envelope of async VLA control, with +6.4 success-rate gain in the high-latency regime (5-7 control steps), +4.6 when transferred to a real-scale VLA at the longest delay, and consistent improvements on two real-robot tasks (a bimanual conveyor pick-and-place and a reactive whack-a-mole).

---

## 3. PhyWorld: Physics-Faithful World Model for Video Generation

**Authors:** Pu Zhao, Juyi Lin, Timothy Rupprecht, ..., Weiwei Chen, Yanzhi Wang
**arXiv:** [2605.19242](https://arxiv.org/abs/2605.19242)
**Categories:** Computer Vision and Pattern Recognition (cs.CV); Artificial Intelligence (cs.AI); Emerging Technologies (cs.ET); Machine Learning (cs.LG); Multimedia (cs.MM)

World simulators can provide safe and scalable environments for training Physical AI systems before real-world deployment. Large video generation models are emerging as a promising basis for such simulators because they can generate diverse and realistic visual futures. However, using them as world simulators requires physically faithful video continuations, namely, generated videos that preserve the physical state implied by the conditioning input, and evolve in ways consistent with basic physical principles. We propose PhyWorld, a video generation world model designed to produce temporally coherent and physically faithful scene continuations through two-stage post-training. In the first stage, we improve video-to-video continuation with flow matching fine-tuning, encouraging stable visual attributes and coherent motion dynamics across frames. In the second stage, we align generated dynamics with physical principles using Direct Preference Optimization (DPO) over physics preference pairs, guiding the model toward outputs with higher physical plausibility. To evaluate PhyWorld, we use both standard video-quality benchmarks and a dedicated physical-faithfulness benchmark with per-law scoring. Experiments show that PhyWorld improves video consistency, achieving an average score of 0.769 on VBench compared with 0.756 or below for state-of-the-art baselines. PhyWorld also improves physical plausibility, reaching an average score of 3.09 on our physical-faithfulness benchmark compared with 2.99 for the strongest baseline. These results suggest that post-training large video generation models with continuation and physics-preference signals can make them more effective world simulators for Physical AI.

---

## 4. Transformers Linearly Represent Highly Structured World Models

**Authors:** Roman Kniazev, Nathanaël Fijalkow
**arXiv:** [2605.18847](https://arxiv.org/abs/2605.18847)
**Categories:** Machine Learning (cs.LG); Artificial Intelligence (cs.AI)

Do transformers, when trained on sequential reasoning traces, build internal models of the underlying task? And if so, does the structure of those internal representations mirror the structure of the domain? We train an 8-layer transformer on Sudoku solving traces and perform a mechanistic analysis of its internal computation. We establish two results. First, the model builds a substructure world model: it does not represent the board state cell by cell, as a human analyst would expect, but organizes information around the rows, columns, and boxes that Sudoku's constraints act on. Second, we identify a naked-single circuit: a small set of dedicated neurons in the final MLP layer, each individually detecting when exactly one digit remains possible for a specific cell, and reliably promoting that digit. These findings show that the geometry of an emergent world model is shaped by the constraint algebra of the domain, not its surface presentation, and that the resulting decision circuit is sparse, monosemantic, and fully interpretable. More broadly, they demonstrate that mechanistic interpretability tools can recover an end-to-end algorithmic account of how a transformer solves a combinatorial reasoning task.

---

## 5. Composition of Memory Experts for Diffusion World Models

**Authors:** Sebastian Stapf, Pablo Acuaviva Huertos, Aram Davtyan, Paolo Favaro
**arXiv:** [2605.18813](https://arxiv.org/abs/2605.18813)
**Categories:** Machine Learning (cs.LG); Artificial Intelligence (cs.AI)

World models aim to predict plausible futures consistent with past observations, a capability central to planning and decision-making in reinforcement learning. Yet, existing architectures face a fundamental memory trade-off: transformers preserve local detail but are bottlenecked by quadratic attention, while recurrent and state-space models scale more efficiently but compress history at the cost of fidelity. To overcome this trade-off, we suggest decoupling future-past consistency from any single architecture and instead leveraging a set of specialized experts. We introduce a diffusion-based framework that integrates heterogeneous memory models through a contrastive product-of-experts formulation. Our approach instantiates three complementary roles: a short-term memory expert that captures fine local dynamics, a long-term memory expert that stores episodic history in external diffusion weights via lightweight test-time finetuning, and a spatial long-term memory expert that enforces geometric and spatial coherence. This compositional design avoids mode collapse and scales to long contexts without incurring a quadratic cost. Across simulated and real-world benchmarks, our method improves temporal consistency, recall of past observations, and navigation performance, establishing a novel paradigm for building and operating memory-augmented diffusion world models.

---

## 6. PROWL: Prioritized Regret-Driven Optimization for World Model Learning

**Authors:** Ahmet H. Güzel, Jenny Seidenschwarz, Benjamin Graham, ..., Jack Parker-Holder, Ilija Bogunovic
**arXiv:** [2605.18803](https://arxiv.org/abs/2605.18803)
**Categories:** Machine Learning (cs.LG); Artificial Intelligence (cs.AI)

Modern action-conditioned video world models achieve strong short-horizon visual realism, yet remain unreliable on rare, interaction-critical transitions that dominate downstream planning and policy performance. Because passive demonstration data systematically under-samples these high-impact regimes, improving robustness requires actively eliciting model failures rather than relying on their natural occurrence. We introduce a KL-constrained adversarial curriculum in which a policy is trained to expose high-error trajectories of a diffusion-based world model while remaining close to the behavior distribution. The world model is continuously fine-tuned on these adversarially discovered trajectories, yielding an adversarial training loop that converts rare failures into a stable, near-distribution training signal without drifting into out-of-distribution exploitation. To maintain pressure on unresolved weaknesses as the model improves, we propose a Prioritized Adversarial Trajectory (PAT) buffer that re-ranks trajectories based on prediction error, action fidelity, and learning progress, focusing training on unresolved failure modes rather than repeatedly revisiting solved cases. We implement our approach in the MineRL framework and evaluate it on held-out out-of-distribution trajectories; PROWL improves robustness over models trained on passive data alone, reveals reward-hacking behaviors under weak behavioral constraints, and demonstrates that effective adversarial world-model training critically depends on balancing exploratory failure discovery with explicit behavioral regularization. Our results suggest that scalable world models benefit not only from larger datasets, but also from selectively generating informative training data.

---

## 7. Rethinking Muon Beyond Pretraining: Spectral Failures and High-Pass Remedies for VLA and RLVR

**Authors:** Chongyu Fan, Gaowen Liu, Mingyi Hong, Ramana Rao Kompella, Sijia Liu
**arXiv:** [2605.19282](https://arxiv.org/abs/2605.19282)
**Categories:** Machine Learning (cs.LG)

Muon is a matrix-aware optimizer that leverages Newton-Schulz (NS) iterations to enforce spectral gradient orthogonalization by driving all singular values of the momentum matrix toward 1. While this uniform spectral whitening enhances exploration and outperforms AdamW in LLM pretraining, we show it could lead to fundamental limitations beyond pretraining in two regimes: (i) cross-modality vision-language-action (VLA) training, where inherently low-rank action-module gradients cause amplification of noisy tail directions, and (ii) reinforcement learning with verifiable rewards (RLVR), where low-SNR gradients and the need to preserve per-head specialization from prior training make whitening unstable. To address these challenges, we propose Pion, a drop-in replacement for Muon that preserves its computational efficiency while replacing uniform spectral whitening with a two-stage Promotion+Suppression mechanism, which we call the high-pass NS iteration. This design induces a sharp spectral high-pass effect, anchoring dominant singular values at 1 while suppressing noisy tail components toward 0, with controllable filter strength. To preserve pretrained per-head heterogeneity, Pion also supports a per-head mode that applies updates independently across attention heads via a simple reshape, at no extra cost. In VLA training on LIBERO and LIBERO-Plus, Pion consistently outperforms both baselines across l_1-regression (VLA-Adapter) and flow-matching (VLANeXt) architectures, e.g., reaching 100% success rate on LIBERO Object after 1,500 training steps with VLA-Adapter, vs. 97.0% for Muon and only 32.2% for AdamW. The advantage of Pion further extends to a real Franka Research 3 robot with a pi_0.5 backbone under the DROID setup on three grasp-and-place tasks. In RLVR post-training on Qwen3-1.7B/4B with GRPO and GMPO, Pion also outperforms AdamW on MATH and GSM8K while Muon collapses to zero.

---

## 8. RoVLA: Multi-Consistency Constraints for Robust Vision-Language-Action Models

**Authors:** Jingzhou Luo, Yifan Wen, Yongjie Bai, ..., Yang Liu, Liang Lin
**arXiv:** [2605.19678](https://arxiv.org/abs/2605.19678)
**Categories:** Robotics (cs.RO)

Vision-Language-Action (VLA) models have shown strong performance on embodied manipulation, yet they remain brittle under visual observation changes, paraphrased language instructions, and compounded perturbations. This limitation suggests that existing methods still rely heavily on shallow correlations in the training distribution, rather than learning stable couplings among task semantics, environment states, and action generation. Although recent efforts improve robustness through larger-scale training, post-training adaptation, or enhanced predictive modeling, they rarely enforce invariance-oriented consistency within the end-to-end policy itself. To address this issue, we propose RoVLA, a robust vision-language-action framework with multi-consistency constraints. RoVLA enforces consistency under three complementary transformations: instruction semantics, trajectory evolution, and observation perturbation. Specifically, Instructional Consistency (IC) promotes stable grounding under semantically equivalent instruction rewrites, Evolutionary Consistency (EC) preserves coherent action intent throughout the generation process, and Observational Consistency (OC) improves robustness to visual and proprioceptive perturbations by enforcing consistent predictions before and after targeted disturbances. By explicitly modeling these invariances during training, RoVLA reduces reliance on superficial correlations and improves robustness and generalization. Experiments on LIBERO-Plus, RoboTwin 2.0, and real-world manipulation tasks show that RoVLA consistently outperforms strong baseline methods and exhibits superior robustness under diverse task and observation shifts. These results demonstrate the effectiveness of multi-consistency learning for robust embodied control. Codes will be available at this https URL.

---

## 9. HEAT: Heterogeneous End-to-End Autonomous Driving via Trajectory-Guided World Models

**Authors:** Hoonhee Cho, Giwon Lee, Jae-Young Kang, ..., Heejun Park, Kuk-Jin Yoon
**arXiv:** [2605.19631](https://arxiv.org/abs/2605.19631)
**Categories:** Robotics (cs.RO); Computer Vision and Pattern Recognition (cs.CV)

End-to-end autonomous driving has emerged as a compelling alternative to traditional modular pipelines by directly mapping raw sensor data to driving actions. While recent approaches achieve strong performance on single-domain datasets, their performance degrades significantly when trained jointly across multiple heterogeneous domains. In practice, however, autonomous systems must operate across diverse environments with heterogeneous distributions, including different cities, sensor configurations, and traffic patterns, without domain-specific retraining. This gap highlights a key challenge in multi-domain learning: domain-specific variations across heterogeneous domains introduce conflicting learning signals, driving models toward compromised solutions that are suboptimal across domains. To address this, we propose a trajectory-driven learning paradigm that organizes training around planning trajectories, enabling the model to capture domain-invariant representations of driving intent. Furthermore, we incorporate a world model that predicts future latent features conditioned on ego actions, improving feature consistency and mitigating domain-induced biases. We evaluate our approach on three benchmarks, nuScenes, NAVSIM, and the Waymo end-to-end dataset, and show substantial improvements over existing methods across all domains. Our results demonstrate that a single unified model can be trained on heterogeneous datasets while maintaining strong performance within each domain, highlighting a step toward scalable real-world deployment. We will make our code publicly available.

---

## 10. FlyMirage: A Fully Automated Generation Pipeline for Diverse and Scalable UAV Flight Data via Generative World Model

**Authors:** Jinhan Li, Xijie Huang, Zhaoqi Wang, ..., Yuze Wu, Xin Zhou
**arXiv:** [2605.19600](https://arxiv.org/abs/2605.19600)
**Categories:** Robotics (cs.RO)

In the field of Vision-Language Navigation (VLN), aerial datasets remain limited in their ability to combine scale, diversity, and realism, often relying on either costly real-world scenes or visually limited simulations. To address these challenges, we introduce FlyMirage, a highly scalable and fully automated data generation pipeline for aerial VLN. Our approach leverages large language models (LLM) as an environment designer to promote scene diversity, paired with a generative world model that instantiates these designs into high-fidelity 3D Gaussian Splatting (3DGS) scenes. To substantially reduce human labor and ensure the feasibility of flight data, FlyMirage automates scene exploration and semantic information acquisition, and further integrates a dynamically feasible planner for uncrewed aerial vehicle (UAV) trajectory generation. Utilizing this toolchain, we generate a large-scale, diverse, and photorealistic aerial VLN dataset, with dynamically feasible flying trajectories, designed to support the development of next-generation embodied navigation models.

---

## 11. PAPO-VLA: Planning-Aware Policy Optimization for Vision-Language-Action Models

**Authors:** Peizheng Guo, Jingyao Wang, Changwen Zheng, Wenwen Qiang
**arXiv:** [2605.19580](https://arxiv.org/abs/2605.19580)
**Categories:** Robotics (cs.RO)

Vision-Language-Action (VLA) models show promising ability in language-guided robotic tasks. However, making VLA policies reliable remains challenging, because a manipulation task is completed through closed-loop interaction, where each action affects subsequent execution. To analyze this problem, we revisit VLA policy during execution and argue that a VLA policy acts both as a planner, which makes task-oriented decisions that change the direction of execution, and as an executor, which realizes these decisions through dense continuous actions. This view suggests that improving VLA reliability requires particular attention to planning actions. Existing optimization methods can imitate actions or improve complete trajectories, but they usually do not explicitly identify planning actions or measure their importance for task success. To address this issue, we propose Planning-Aware Policy Optimization for VLA models (PAPO-VLA). PAPO-VLA first identifies planning actions by jointly considering action variation and trajectory outcome, then estimates their importance through causal sufficiency and causal necessity, and finally incorporates this importance into GRPO advantage estimation. In this way, more important planning actions receive stronger optimization emphasis, while the whole trajectory is still optimized by trajectory-level feedback. Experiments on multiple benchmarks demonstrate the effectiveness of PAPO-VLA.

---

## 12. SafeAlign-VLA: A Negative-Enhanced Safe Alignment Framework for Risk-Aware Autonomous Driving

**Authors:** Kefei Tian, Yuansheng Lian, Kai Yang, Xiangdong Chen, Shen Li
**arXiv:** [2605.19524](https://arxiv.org/abs/2605.19524)
**Categories:** Robotics (cs.RO); Computer Vision and Pattern Recognition (cs.CV)

End-to-end autonomous driving systems excel in common scenarios but struggle with safety-critical long-tail cases. Vision-Language-Action (VLA) models are promising due to their strong reasoning capabilities. However, most VLA-based approaches rely on positive expert demonstrations, rarely exploiting negative samples, leading to insufficient understanding of risky behaviors and safety boundaries. To address this limitation, we propose SafeAlign-VLA, a unified negative-enhanced safe alignment framework that incorporates negative data into supervised learning and reinforcement learning. First, we develop a counterfactual safety pairing paradigm to generate structured safety labels and counterfactual positive trajectories from risky scenarios via counterfactual reasoning. Then, a two-stage training strategy is adopted: negative-enhanced supervised fine-tuning for failure feedback and trajectory correction, followed by anchor-based group relative policy optimization that uses positive and negative trajectories as contrastive anchors to steer sampling and penalize high-risk behaviors via group-relative advantages. Experiments on NAVSIM and DeepAccident validate the proposed framework. SafeAlign-VLA achieves 89.1 PDMS on the NAVSIM v1 testset, improving over the baseline without negative data by 1.3%. On DeepAccident, it reduces the collision rate to 3.36%, while achieving 84.2% language accuracy and 85.8% risk prediction accuracy. These results demonstrate the effectiveness of the proposed negative-enhanced safe alignment framework for safe and robust autonomous driving.

---

## 13. AffectVerse: Emotional World Models for Multimodal Affective Computing

**Authors:** Bo Zhao, Fanghua Ye, Yixin Ji, ..., Xiaojiang Peng, Zitong YU
**arXiv:** [2605.19950](https://arxiv.org/abs/2605.19950)
**Categories:** Computer Vision and Pattern Recognition (cs.CV)

Humans infer emotions by integrating observed multimodal cues with expectations about how affective states may unfold. Existing multimodal large language models (MLLMs), however, often treat emotion recognition as static fusion over complete audiovisual-text inputs, leaving affective dynamics implicit. We propose AffectVerse, a Qwen2.5-Omni-based model equipped with an Emotion World Module (EWM), an action-free representation-level module for short-horizon latent affective prediction. \rev{EWM contains three modules: 1) Cross-Modal Temporal Imagination predicts future video/audio representations from past tokens with multi-step rollout. 2) MAMA(Modality-Aware Multi-step Attention) Belief Aggregation compresses imagined tokens into modality-aware belief tokens. 3) Belief Injection inserts these belief tokens into the LLM for affective reasoning.} AffectVerse uses future prediction as a past-conditioned self-supervised signal: it does not replace modeling observed history or require unseen signals at inference, but forces the current belief state to encode transition cues that are predictive of subsequent affective change. Across nine benchmarks, AffectVerse improves at least 2.57\% over other models, while controlled ablations show additive gains from temporal imagination, cross-modal rollout, and belief aggregation. These results suggest predictive belief-state modeling is a practical alternative for affective computing.

---

## 14. SWEET: Sparse World Modeling with Image Editing for Embodied Task Execution

**Authors:** Yiren Song, Yihan Wang, Xiyao Deng, Zhuoran Yan, Mike Zheng Shou
**arXiv:** [2605.19319](https://arxiv.org/abs/2605.19319)
**Categories:** Computer Vision and Pattern Recognition (cs.CV)

Visual prediction has emerged as a promising paradigm for embodied control, where future observations are generated and then translated into actions. However, dense video generation is computationally expensive and often unnecessary for many manipulation tasks, whose progress can be summarized by a small number of task-relevant visual states. In this work, we study whether image editing models can serve as sparse visual world models for robot manipulation by predicting task-level future states without dense video rollout. We first conduct a controlled comparison between the video generation model Wan2.2 and the image editing model FLUX-Kontext under the same robotic data setting, and find that image editing produces more reliable task-level keyframes with better visual fidelity and substantially lower inference cost. Motivated by this observation, we propose SWEET, a one-shot sparse visual planning framework that progressively generates a sequence of task-relevant manipulation keyframes through successive image editing, conditioned on language instructions and optional arrow-based spatial guidance. A goal-conditioned diffusion action predictor then converts adjacent imagined keyframes into executable action chunks. To reduce the mismatch between real and edited visual subgoals, we further introduce a mixed-training strategy with filtered edited targets. Experiments on DROID and RoboMimic show that SWEET improves keyframe prediction across seen and unseen scenes and enables a full pipeline from sequential keyframe planning to executable robot actions, suggesting that image editing is a promising and underexplored direction for embodied visual prediction.

---

## 15. World-Ego Modeling for Long-Horizon Evolution in Hybrid Embodied Tasks

**Authors:** Zuyao Lin, Jianhui Zhang, Peidong Jia, ..., Shanghang Zhang, Xingyu Chen
**arXiv:** [2605.19957](https://arxiv.org/abs/2605.19957)
**Categories:** Computer Vision and Pattern Recognition (cs.CV); Artificial Intelligence (cs.AI); Robotics (cs.RO)

World models are widely explored in embodied intelligence, yet they typically predict distinct evolutions of the world and the ego within a single stream, where the world captures persistent instruction-agnostic scene regularities and the ego captures robot-centric instruction-conditioned dynamics. This world-ego entanglement leads to a degradation in long-horizon embodied scenarios, particularly in hybrid tasks with interleaved navigation and manipulation behaviors. In this paper, we introduce \emph{World-Ego Modeling}, a new conceptual paradigm that decomposes future evolution into world and ego components. We define the world-ego boundary from three perspectives, i.e., motion-, semantic-, and intention-based views, and analyze three disentanglement strategies with post-, pre-, and full disentanglement. Further, we instantiate this paradigm as the World-Ego Model (WEM), a unified embodied world model that couples an implicit separate world-ego planner with a cascade-parallel mixture-of-experts (CP-MoE) diffusion generator. To enable rigorous evaluation, we further construct HTEWorld, the first benchmark for long-horizon world modeling with hybrid navigation-manipulation tasks, providing 125K video clips (over 4.5M frames) with fine-grained action annotations and 300 multi-turn evaluation trajectories (over 2K instructions). Extensive experiments show that WEM achieves state-of-the-art performance on HTEWorld while remaining competitive on existing manipulation-only benchmarks.

---
