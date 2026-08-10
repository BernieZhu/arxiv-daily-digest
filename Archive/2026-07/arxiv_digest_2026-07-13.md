# arXiv Daily Digest — 2026-07-13

**Mode:** direct
**Categories:** cs.AI, cs.LG, cs.RO, cs.CV
**Keywords:** VLA, world model, world action model
**Papers found:** 3

---

## 1. GATS: Graph-Augmented Tree Search with Layered World Models for Efficient Agent Planning

**Authors:** Maureese Williams, Dymitr Nowicki
**arXiv:** [2607.08894](https://arxiv.org/abs/2607.08894)
**Categories:** Artificial Intelligence (cs.AI); Machine Learning (cs.LG)

Large Language Model (LLM) agents have shown promise in multi-step planning tasks, but existing approaches like LATS (Language Agent Tree Search) and ReAct rely heavily on LLM inference during planning, leading to high computational costs and stochastic behavior. We present \textbf{GATS} (Graph-Augmented Tree Search), a planning framework that combines systematic UCB1-based tree search with a layered world model to eliminate LLM calls during inference while achieving superior planning performance. Our three-layer world model integrates: (L1) exact symbolic action matching, (L2) statistics learned from execution logs, and (L3) LLM-based prediction for unknown actions. On synthetic planning tasks with branching paths and dead-ends, GATS achieves \textbf{100\% success rate} compared to 92 % for LATS and 64\% for ReAct. On a comprehensive stress test spanning 12 challenging scenarios -- including coding workflows, web navigation, and long-horizon tasks -- GATS maintains \textbf{100\% success} while LATS drops to 88.9 % and ReAct to 23.9%. GATS requires \textbf{zero LLM calls per task} during planning (vs. 37 per task for LATS) and produces deterministic plans with zero variance across runs. Our results demonstrate that systematic search with learned world models can substantially outperform LLM-guided exploration for agent planning.

---

## 2. CLAP: Direct VLM-to-VLA Adaptation via Language-Action Grounding

**Authors:** Yuri Ishitoya, Jeremy Siburian, Masashi Hamaya, ..., Cristian C. Beltran-Hernandez, Mai Nishimura
**arXiv:** [2607.08974](https://arxiv.org/abs/2607.08974)
**Categories:** Robotics (cs.RO); Artificial Intelligence (cs.AI)

Vision-language-action models (VLAs) inherit semantic capabilities from pretrained VLMs, yet large-scale post-training on robot data and architectural modifications can reshape the backbone so extensively that it becomes difficult to isolate what the VLM contributes to control. Directly converting pretrained VLMs into VLAs with minimal architectural change offers a more transparent path to understanding how VLM capabilities transfer across model scales. The core obstacle is output-distribution mismatch: predicting actions as bare numeric token sequences moves generation away from the VLM's pretrained language distribution, degrading the capabilities we seek to preserve. To address this, we propose CLAP (Causal Language-Action Prediction), which prepends each numeric action sequence with a natural-language action description, causally conditioning precise action-token prediction on a language-action plan without modifying the backbone architecture. With single-epoch fine-tuning alone, 2B CLAP achieves 90.8% on LIBERO (+14.9 pt over VLA-0) and improves robustness on LIBERO-PRO under language, object, and spatial perturbations. We will release CLAP at 0.8B, 2B, and 4B as an open-weight, multi-scale compact VLA family from a single VLM lineage, enabling controlled analysis of VLM-to-VLA capability transfer.

---

## 3. Causally Debiased Latent Action Model for Embodied Action Conditioned World Models

**Authors:** Yufan Wei, Kun Zhou, Lingjun Mao, ..., Fan Feng, Biwei Huang
**arXiv:** [2607.09185](https://arxiv.org/abs/2607.09185)
**Categories:** Computer Vision and Pattern Recognition (cs.CV); Robotics (cs.RO)

Action-conditioned world models (ACWMs) aim to simulate future observations conditioned on embodied actions, offering a promising foundation for robot planning, policy evaluation, and data augmentation. However, learning controllable ACWMs requires large-scale action-labeled data, which remains costly to collect in the real world. Latent action models (LAMs) mitigate this bottleneck by inferring latent actions from unlabeled videos, but existing LAMs are typically trained with reconstruction-only objectives and therefore entangle action-relevant dynamics with action-irrelevant visual factors such as backgrounds and untouched objects. In this work, we identify this action-irrelevant bias as a key obstacle to controllable ACWMs and introduce evaluation metrics to measure latent-action bias, action following, and robustness. We propose CD-LAM, a causally debiased framework for LAM-based ACWMs. CD-LAM introduces three efficient fine-tuning objectives: embodiment-centric reconstruction, action-centric contrastive learning, and latent space calibration, which together encourage embodiment-focused, action-aware, and calibrated non-collapsed latent action representations. Experiments on 2B and 14B ACWM backbones show that CD-LAM substantially improves latent-action controllability, downstream robot-action following, visual fidelity, and adaptation efficiency, requiring only 6k fine-tuning steps and more than 12$\times$ fewer robot-action adaptation updates than the baseline.

---
