# arXiv Daily Digest — 2026-07-09

**Mode:** direct
**Categories:** cs.AI, cs.LG, cs.RO, cs.CV
**Keywords:** VLA, world model, world action model
**Papers found:** 7

---

## 1. Grounding Spatial Relations in a Compact World Model: Instruction Leakage and a Goal-Free Dynamics Fix

**Authors:** Yufeng Wang, Lu Wei, Haibin Ling
**arXiv:** [2607.06925](https://arxiv.org/abs/2607.06925)
**Categories:** Artificial Intelligence (cs.AI)

Compact world models that condition on a language goal promise to ground relations such as ``put the red block left of the blue block'' using a sparse set of explicit \emph{reference anchors}. We ask when such references actually ground a relation, and identify a trap: a goal-conditioned predictor reaches a striking $0.90$ relation-readout accuracy, yet this is \emph{instruction transcription}, not perception. Withholding the goal collapses it to chance ($0.90\!\to\!0.27$, three seeds) and a counterfactual instruction makes the predicted anchors follow the \emph{false} instruction $94.5\%$ of the time (true scene $2.3\%$; $N{=}256$). Tested across three settings and a within-task ablation, our central claim characterizes the confound: \textbf{instruction leakage occurs when the scored quantity is transcribable from the instruction (when the instruction names the answer) and is essentially independent of how predictive the non-instruction inputs are.} Our tabletop and the external BabyAI benchmark leak, whereas a Language-Table forward-dynamics world model whose instruction names \emph{referents} does not, until the instruction is augmented to name the direction; and degrading the action never increases leakage, the opposite of what predictor-competition predicts. The diagnosis prescribes the fix: keep the goal out of the dynamics (it belongs to the planner's cost) and supervise the \emph{read} path, recovering genuine, instruction-independent grounding ($0.88$, identical with and without the goal). The detection protocol and remedy apply to any goal-conditioned world model whose instruction names the scored quantity.

---

## 2. Validate the Dream Before You Trust Its Verdict: Admissibility for World-Model Simulators

**Authors:** Christian Oefinger, Finn Rasmus Schäfer, Korbinian Moller, Mattia Piccinini, Johannes Betz
**arXiv:** [2607.07196](https://arxiv.org/abs/2607.07196)
**Categories:** Robotics (cs.RO); Artificial Intelligence (cs.AI); Machine Learning (cs.LG); Software Engineering (cs.SE)

Across robotics, World Models (WMs) are increasingly used to evaluate action policies by simulating the consequences of actions in an imagined world, and returning a success or safety verdict. Yet a verdict is only as trustworthy as the WM that produced it, and the WM itself needs to be certified. In video-generation WMs, fidelity metrics such as Fréchet Video Distance (FVD) reward visual realism, but ignore whether the world responds correctly to the policy's actions, including those unseen in training. Classical simulation-based validation assumes a trusted simulator evaluating an untrusted policy, whereas generative WMs are themselves unverified learned artifacts. Hence, we argue that any WM used as a test oracle must first be accredited before its verdicts can serve as evidence. Building on credibility practices from safety-critical simulation, including Verification, Validation & Accreditation (VV&A), Safety of the Intended Functionality (SOTIF), and scenario-based testing standards, we define an admissibility ladder (L0-L4) that a WM must climb before its closed-loop verdicts are accepted as assurance evidence. Our framework is embodiment-agnostic, and is instantiated in autonomous driving (AD), where assurance methods for traditional simulation are most mature. Applied to two driving WMs, the lower rungs reveal a reversal: the model that ranks higher on visual generation quality (L0) ranks lower on action-following (L1-L2), so visual fidelity does not predict the action-robustness a closed-loop verdict depends on.

---

## 3. WAM-TTT: Steering World-Action Models by Watching Human Play at Test Time

**Authors:** Yusen Feng, Bingchen Han, Jiangran Lyu, ..., Zhizheng Zhang, He Wang
**arXiv:** [2607.06988](https://arxiv.org/abs/2607.06988)
**Categories:** Robotics (cs.RO); Artificial Intelligence (cs.AI)

Steering robot foundation models (RFMs) toward new task variants or user-preferred behaviors remains challenging, often requiring additional robot demonstrations, task-specific fine-tuning, or long-context conditioning. We present WAM-TTT, a test-time training framework for steering world action models from raw human videos. Rather than treating human videos as trajectories to imitate, WAM-TTT absorbs them into a lightweight adaptive memory inside a frozen WAM through self-supervised video prediction. To make this memory useful for control, we introduce a meta-training stage that aligns human demonstrations with robot behaviors using paired human-robot data and a key--value memory reconstruction objective. At test time, only unlabeled human videos are required to adapt the memory, while the pretrained WAM remains frozen. This enables efficient and reusable steering without robot actions, human-side annotations, or task-specific fine-tuning, while preserving the generalization ability of the foundation model. Extensive experiments show that WAM-TTT consistently outperforms in-context human-video conditioning baselines across diverse manipulation tasks and generalization settings.

---

## 4. Vision Language Action (VLA) Models for Unmanned Aerial Robotics and Bimanual Manipulation: A Review

**Authors:** Inkyu Sa, Chanoh Park, Hea-Min Lee, Donghee Noh, Ho Seok Ahn
**arXiv:** [2607.06706](https://arxiv.org/abs/2607.06706)
**Categories:** Robotics (cs.RO); Artificial Intelligence (cs.AI); Machine Learning (cs.LG)

Vision Language Action (VLA) models unify visual perception, natural-language understanding, and action generation within a single foundation model, allowing a robot to follow instructions such as fold the towel or fly to the red building directly from camera images. Because VLAs inherit world knowledge from internet-scale pre-training, they have become the dominant framework for learning-based manipulation, with bimanual coordination serving as the most demanding testbed: two arms with 7 degrees of freedom each must move in concert to fold, assemble, and reorient objects. Unmanned aerial robotics faces a structurally similar challenge: a drone must coordinate thrust, attitude, and increasingly gripper commands from visual observations under strict latency and payload constraints. This review covers 183 contributions spanning 2017-2026 and organized along seven dimensions: VLA architectures, training recipes, action representations, bimanual coordination (2022-2026), unmanned aerial vehicle (UAV) navigation and control (2017-2026), language grounding, and cross-cutting concerns including memory and world models. We show that the coordination strategies, training recipes, and action representations developed for bimanual VLAs transfer to unmanned aerial systems and identify fourteen research directions across both domains.

---

## 5. The Rank-One Corner: How Much Value Equivalence Does a Task Need from a World Model?

**Authors:** Donna Vakalis
**arXiv:** [2607.06640](https://arxiv.org/abs/2607.06640)
**Categories:** Machine Learning (cs.LG); Artificial Intelligence (cs.AI)

A learned world model is usually judged by how faithfully it reconstructs its observations or predicts reward, as though quality were something the model simply has or lacks. But what a task actually needs from a model is narrower: the few predictive coordinates its queries depend on, which we call the closure. We show that how much of that closure a latent comes to represent is set not by the model's capacity or its observations but by the dimensionality of the objective it is trained against, and we measure this directly on a DreamerV3 stack in a controlled environment with known ground-truth closure. An aligned scalar value signal -- the objective at the heart of value equivalence -- installs only a one-dimensional projection of a closure that needs several dimensions: read through a single linear probe, the recoverable structure rises from R^2=0.10 to 0.76 as the scalar is replaced by the full objective. Sweeping the objective's dimensionality from one to four installs exactly that many predictive directions through an auxiliary head, and the same staircase appears -- at attenuated magnitude but the same rank -- through the model's own value head, so the dissociation is dimensional rather than an artifact of head form. Capacity-matched comparisons and in-situ pressure checks rule out the obvious alternatives. The law governs a regime, and we measure its boundary: on a companion closed-loop task whose structure is observable frame by frame, reconstruction installs that structure and the scalar objective suffices -- the objective decides what a latent represents exactly where cheaper training signals cannot already recover it. Value equivalence is thus not all-or-nothing but dimensional: the familiar single-reward objective is its rank-one corner, and a model installs as much of a task's structure as the objective it is asked to predict.

---

## 6. Pelican-VLA 0.5: Attending Before Acting Benefits Generalization

**Authors:** Zeyuan Ding, Wenhai Liu, Yang Xu, ..., Jian Tang, Xiaozhu Ju
**arXiv:** [2607.06655](https://arxiv.org/abs/2607.06655)
**Categories:** Robotics (cs.RO); Machine Learning (cs.LG)

In this report, we present Pelican-VLA 0.5, a unified VLA model that integrates vision-language understanding, future-frame generation, and action prediction within a single architecture. Pelican-VLA 0.5 achieves attention-level generalization: without object annotations, segmentation masks, attention supervision, or task-specific fine-tuning, its action pathway already focuses on the manipulation-relevant object and contact region. This behavior persists across unseen scenes and unseen robot embodiments, and is substantially stronger than in other open-source VLA baselines. We verify that this ability originates from the learnable Bottleneck Token inserted between perception and action: by routing task-relevant visual information through a compact bottleneck, the tokens interface induces manipulation-centric attention during pre-training and remains effective across different policy structures, including a MoT-style architecture.

---

## 7. Dual Latent Memory in Vision-Language-Action Models for Robotic Manipulation

**Authors:** Hongyu Qu, Jianzhe Gao, Xiaobin Hu, ..., Xiangbo Shu, Shuicheng Yan
**arXiv:** [2607.07608](https://arxiv.org/abs/2607.07608)
**Categories:** Robotics (cs.RO); Computer Vision and Pattern Recognition (cs.CV)

Mainstream Vision-Language-Action (VLA) models predict actions primarily from the current observation under a Markovian assumption, thus struggling with long-horizon, temporally dependent tasks. Existing memory-augmented VLAs either expand the observation window or retrieve history from the memory bank as auxiliary policy-side context. However, they leave memory outside the native latent embedding space of VLA reasoning, preventing historical experience from being fluidly interleaved with multimodal reasoning and action formation. To this end, we introduce LaMem-VLA, a latent-memory-native framework that reconstructs historical experience into latent memory tokens and directly interweaves them with VLA reasoning. At its core, LaMem-VLA introduces four coordinated components: (i) a curator that organizes historical experience into two complementary short-term and long-term memory vaults; (ii) a seeker that queries both vaults using the multimodal cognition to retrieve context-relevant evidence; (iii) a condenser that reconstructs the retrieved evidence into compact short-term and long-term latent memory tokens; and (iv) a weaver that injects these memory tokens with the current observation and instruction into one continuous embedding sequence. By representing, retrieving, and consuming historical experience entirely in the same continuous latent space, LaMem-VLA enables memory to directly participate in VLA reasoning and guide action generation under a bounded context. Extensive experiments on SimplerEnv and LIBERO demonstrate the superiority of our LaMem-VLA.

---
