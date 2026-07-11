# arXiv Daily Digest — 2026-07-10

**Mode:** direct
**Categories:** cs.AI, cs.LG, cs.RO, cs.CV
**Keywords:** VLA, world model, world action model
**Papers found:** 6

---

## 1. EgoWAM: World Action Models Beyond Pixels with In-the-Wild Egocentric Human Data

**Authors:** Baoyu Li, Xinchen Yin, Mengying Lin, Yixin Zhang, Danfei Xu
**arXiv:** [2607.08436](https://arxiv.org/abs/2607.08436)
**Categories:** Robotics (cs.RO); Artificial Intelligence (cs.AI)

Egocentric human data offers scalable supervision for robot manipulation. However, behavior cloning entangles transferable content like objects, scenes, and task semantics, with non-transferable factors like human morphology, head motion, and behavioral style. We study whether World Action Models (WAMs) provide a better training signal by requiring policies to predict not only actions, but also how the scene evolves. The central question is what world representation best enables human-to-robot transfer. We hypothesize that an effective world target should abstract appearance, capture agent-invariant physical effects, and separate camera motion from environment change. We introduce EgoWAM, a controlled human-robot co-training framework that fixes the policy backbone, action head, and data mixture while varying only the world prediction target, comparing Pixel, DINO, and 3D motion flow. Across three real-world bimanual tasks, WAM co-training scales more effectively with in-the-wild egocentric human data than behavior cloning. Pixel-based prediction transfers weakly, while DINO and 3D flow yield substantial gains: DINO improves out-of-distribution object and scene generalization by up to 4x, and 3D flow improves in-domain performance by 20-30%. More details: this https URL

---

## 2. WCog-VLA: A Dual-Level World-Cognitive Vision-Language-Action Model for End-to-End Autonomous Driving

**Authors:** Xuerun Yan, Zhexi Lian, Nuoheng Zhang, ..., Jia Hu, Binyang Song
**arXiv:** [2607.08375](https://arxiv.org/abs/2607.08375)
**Categories:** Computer Vision and Pattern Recognition (cs.CV); Artificial Intelligence (cs.AI)

Vision-Language-Action (VLA) models have advanced end-to-end autonomous driving. However, existing methods either lack comprehensive world cognition or suffer from fragmented world foresight, inherently confining these models to reactive driving. To address this limitation, we propose WCog-VLA, a novel dual-level World-Cognitive VLA framework that successfully bridges semantic world forecasting with generative world evolution to achieve proactive autonomous driving. At the semantic level, WCog-VLA unifies world cognition and reasoning by incorporating 3D spatial perception and injecting agent tokens to capture the world dynamics, while concurrently enabling Game-theoretic Chain-of-Thought (Game-CoT) reasoning. At the generative level, we introduce the Aligned Decoupled Diffusion Transformer (ADDT) as a powerful generative world model that synthesizes physically-plausible joint multi-agent trajectories. Through scene representation alignment, ADDT reduces the number of denoising steps required and thus significantly accelerates inference. To facilitate strategic reasoning, we further construct a large-scale dataset featuring 85k Game-CoT annotations. Extensive experiments on the NAVSIM benchmark demonstrate that WCog-VLA achieves a State-Of-The-Art (SOTA) PDMS score of 92.9.

---

## 3. LEEVLA: Seeing What Matters in Latent Environment Evolution for Vision-Language-Action

**Authors:** Qi Lyu, Baicheng Liu, Xudong Wang, ..., Lianqing Liu, Zhi Han
**arXiv:** [2607.08182](https://arxiv.org/abs/2607.08182)
**Categories:** Computer Vision and Pattern Recognition (cs.CV); Artificial Intelligence (cs.AI)

Vision-language-action (VLA) models aim to map multimodal inputs to robot actions. However, most existing approaches struggle to cover complex dynamic scenarios due to treating all visual tokens uniformly and reasoning with human-selected factors, which lack mechanisms to emphasize task-critical evidence and ignore underlying factors. To address this issue, we propose LEEVLA, a VLA architecture for seeing what matters in Latent Environment Evolution that explicitly guides the model toward informative regions while preserving the structured evolution of latent world representations. To identify salient and instruction-relevant regions, we introduce drift-guided dynamic prioritization (DGDP), which combines dynamic position prioritization (DPP) with semantic drift guidance (SDG) to guide the VLA agent where to attend during training. On top of this, we introduce structured feature flow generation (SFFG), which models how these prioritized features should evolve in latent space via prototype-to-periphery (P2P) prediction, and a mutual-neighborhood contrastive (MC) loss to maintain topological consistency among neighborhoods. Together, DGDP and SFFG form a task-aware "where-how" training framework. Extensive experiments on VLA benchmarks show that LEEVLA consistently outperforms prior methods, confirming that explicit task-evidence guidance and structured latent reasoning are both crucial for scalable VLA. Our code is available at this https URL.

---

## 4. Write-Protected Discrete Bottlenecks for Language-Grounded World Models: A Structural Limitation and Sufficient Fix

**Authors:** Jiayi Fang
**arXiv:** [2607.08312](https://arxiv.org/abs/2607.08312)
**Categories:** Machine Learning (cs.LG)

How should language interface with a world model's discrete symbol system? The dominant paradigm -- end-to-end injection of LLM/VLM features into robot world models (RT-2, Octo, PaLM-E) -- implicitly assumes that language gradients can directly shape physical symbol representations. We ask whether this assumption is safe, find that it is not, and characterize the minimal architectural constraint that prevents the failure. Any language gradient entering a Gumbel-softmax-based discrete symbol bottleneck forces a structural trade-off: the vanilla estimator collapses to 2.2/64 symbols (4/5 seeds), while five anti-collapse strategies maintain diversity but fail to learn semantic labels (all <= 9.2% accuracy). No tested GumbelBottleneck variant achieves both objectives simultaneously. Within this family of discrete bottlenecks, the failure is structural rather than a matter of optimization. We characterize a sufficient set of three constraints that prevent the failure: (1) cut the gradient chain (this http URL()), preventing language signals from reaching the symbol bottleneck; (2) provide a gradient-free semantic channel -- a non-parametric Memory Table (Dict[symbol -> Counter[label]], zero parameters, zero gradients) where co-occurrence counting replaces gradient-based binding; (3) handle symbol collisions via DP-Means streaming clustering for automatic sub-cluster splitting. All three layers together achieve 97.2% grounding accuracy vs. 22.2% without Layer 3. Across two experiments spanning 74 independent runs, we demonstrate zero symbol collapse in all 32 seeds, with the blackboard achieving 79-100% semantic binding across three encoder architectures (CNN, V-JEPA 300M, CLIP ViT-L), two environments, and three texture conditions. The fix trains fewer than 2M parameters and requires no LLM fine-tuning.

---

## 5. FabriVLA: A Lightweight Vision-Language-Action Model for Precise Multi-Task Manipulation

**Authors:** Shiyuan Yang, Borong Zhang, Jizheng Zhang, ..., Xu Bian, Qingbiao Li
**arXiv:** [2607.08575](https://arxiv.org/abs/2607.08575)
**Categories:** Robotics (cs.RO)

We present FabriVLA, a lightweight Vision-Language-Action model for Precise Multi-Task Manipulation. FabriVLA combines an InternVL3.5 vision-language backbone with a flow-matching action head featuring gated self-attention across action tokens and shallow VLM layer fusion for enriched spatial context. The model is trained via single stage joint optimization from a pretrained VLM and randomly initialized action head. On the Meta-World MT50 benchmark spanning 50 diverse manipulation tasks, FabriVLA achieves a tier-average success rate of 90.0%, demonstrating that a compact VLA built on a 1B scale VLM can achieve strong performance without relying on multi billion parameter VLA backbones.

---

## 6. Harness VLA: Steering Frozen VLAs into Reliable Manipulation Primitives via Memory-Guided Agents

**Authors:** Yixian Zhang, Huanming Zhang, Feng Gao, ..., Wenbo Ding, Chao Yu
**arXiv:** [2607.08448](https://arxiv.org/abs/2607.08448)
**Categories:** Robotics (cs.RO)

Language-conditioned manipulation requires both precise contact-rich control and robust reasoning over language, scenes, and long horizons. End-to-end Vision-Language-Action (VLA) models provide strong local visuomotor skills, but they are trained on in-distribution task trajectories and often fail under deployment perturbations such as semantic retargeting, goal re-binding, spatial-layout shifts, and unstable local contacts. LLM coding agents provide complementary semantic and compositional reasoning, but purely analytic primitives struggle with irregular grasping, constrained placement, and articulated-object interaction. We present Harness VLA, a memory-augmented agentic framework that exposes a frozen VLA as a retryable contact-rich primitive and composes it with a small fixed library of analytic primitives for grounding, staging, transport, navigation, and release. Rather than expanding the skill library, the harness learns the operating range of these fixed primitives from task-specific execution traces, global success rules, and failure models. By lifting semantic re-grounding, non-contact execution, and VLA re-staging to the planner while reserving the frozen VLA for local contact-rich phases, Harness VLA extends pretrained VLAs beyond their original trajectory distribution without finetuning. Across perturbed tabletop, household kitchen, and clean-to-randomized bimanual manipulation, Harness VLA improves over the strongest relevant baselines by 38.6 and 25.4 percentage points on LIBERO-Pro and RoboCasa365, respectively, and reaches 58.4% on RoboTwin C2R.

---
