# arXiv Daily Digest — 2026-08-24

**Mode:** direct
**Categories:** cs.AI, cs.LG, cs.RO, cs.CV
**Keywords:** VLA, world model, world action model
**Papers found:** 11

---

## 1. Graph-Operator World Models for Morphology-Parameter Generalization in Continuous Control

**Authors:** Xu Yang, Yiqin Yang, Qianchuan Zhao
**arXiv:** [2608.20936](https://arxiv.org/abs/2608.20936)
**Categories:** Artificial Intelligence (cs.AI); Robotics (cs.RO)

World models for continuous control are commonly trained for a fixed physical system and can degrade when known morphology parameters such as link lengths, masses, damping, and actuation change. Existing approaches often provide these parameters as conditioning information, but leave unspecified which part of the learned transition should remain reusable and which part should change with morphology. We propose Graph-Operator World Models (GraphOp-WM), a structured world model for generalization across unseen morphology parameters within related articulated robot families. GraphOp-WM represents bodies and their kinematic relations as an attributed graph and factorizes each transition into a morphology-independent local dynamics basis and a morphology-conditioned structured operator. The operator combines node-local modulation, kinematic-tree coupling, and a low-rank global correction, while architectural information separation, basis normalization, and paired-morphology supervision encourage static morphology dependence to be carried by the operator pathway. Graph-level readout and edge-wise action representations provide a compatible interface for reward, value, and TD-MPC-style planning. We further define controlled MuJoCo parameter splits covering interpolation, extrapolation, and held-out compositions of link geometry, mass, damping, and actuation parameters in Hopper, Walker2d, and HalfCheetah.

---

## 2. ForeTime-VLA: Causal Future-Token Distillation from a World Action Model for Conveyor-Belt Manipulation

**Authors:** Siyuan Ma, Yutian Zhang, Boshi Zhang, ..., Dong Wei, Xiaojin Huang
**arXiv:** [2608.20735](https://arxiv.org/abs/2608.20735)
**Categories:** Artificial Intelligence (cs.AI); Robotics (cs.RO)

Manipulating moving objects requires a policy to anticipate contact events, yet vision-language-action (VLA) policies are commonly fine-tuned from the current observation alone. World action models (WAMs) learn predictive dynamics, but running a video-scale teacher or explicitly imagining future frames at deployment is costly. We introduce ForeTime-VLA, a dense pi0.5 policy that distills a future-aware, action-equivalent representation from a frozen Fast-WAM-derived teacher while remaining causal at inference. Offline, current and future video latents are compressed into a whitened 64-D target. Online, an eight-frame history encoder predicts this target together with manipulation phase and normalized time-to-transition. Four future tokens and one phase token condition the VLM prefix, while the predicted future and transition horizon condition the action expert. Training retains the original flow-matching action target and adds cosine, relational geometry, phase, time-to-transition, and action-equivalence objectives. On a deduplicated conveyor-belt dataset, we compare 40k-step checkpoints on 768 matched windows per split. Test MAE decreases from 0.134119 to 0.130593 (2.63%; paired-bootstrap 95% CI: 0.82-4.48% improvement), and test L2 decreases by 3.02%, at a 2.46-2.93% latency cost. In quantitative real-robot evaluation, ForeTime-VLA achieves 81.1% stationary and 58.9% slow-moving grasp success, exceeding the next-best reference by 12.2 and 22.2 percentage points, respectively. Across three belt speeds, it completes 44/90 grasps versus 23/90 for pi0.5, including 11/30 versus 2/30 at fast speed. The agreement between offline orientation gains and reduced real-robot contact-pose failures supports causal future-token distillation as an effective way to improve dynamic manipulation without deploying the world-model teacher.

---

## 3. World models of environment, agent and joint agent-environment systems

**Authors:** Manuel Baltieri, Filippo Torresan, Yivan Zhang, Alexander Boyd, Fernando E. Rosas
**arXiv:** [2608.20401](https://arxiv.org/abs/2608.20401)
**Categories:** Artificial Intelligence (cs.AI); Machine Learning (cs.LG)

World models are a central component of model-based reinforcement learning. They are usually discussed in terms of what variables they predict, such as observations, rewards, states, latent or information states. We argue that there is a prior distinction: which channel they model. We consider three cases: the environment channel $O_{:} \mid A_{:}$, the agent channel $A_{:} \mid O_{:}$, and the realised joint process $(A, O)_{:}$, equivalently viewed as a channel with no inputs. Using computational mechanics, we define canonical predictive models for these three cases as $\epsilon$-transducers or $\epsilon$-machines. Canonical environment models recover standard predictive state representations, while the other two give analogous notions of canonical models for the agent and the joint system. We then build canonical support-restricted environment and agent models induced by closed-loop coupling, whose predictive equivalences range over continuations supported by the realised interaction. The key structural result is that canonical support-restricted environment states factor through the canonical joint causal states, and their transition structure is induced directly from the joint model; the agent-side construction is dual. Finally, we give a POMDP/controller example in which the unrestricted environment model has infinitely many states while the canonical support-restricted model induced by the coupling is finite. The framework clarifies what different world models are models of, and how coupling and support restriction can change their canonical predictive structure and complexity.

---

## 4. CIVA: Critic-Induced Value-Subspace Attacks on Visual World-Model Agents

**Authors:** Jiancheng Wang, Mingli Zhu, Tong Zhang, ..., Siyuan Liang, Dacheng Tao
**arXiv:** [2608.21114](https://arxiv.org/abs/2608.21114)
**Categories:** Computer Vision and Pattern Recognition (cs.CV); Artificial Intelligence (cs.AI)

Visual world-model agents such as DreamerV3 act through a recurrent latent state rather than a single observation, which weakens frame-wise observation attacks and makes their perturbations vary sharply over time under a strict per-frame perturbation constraint. We study white-box, causal, online attacks on such agents and propose Critic-Induced Value-Subspace Attacks (\textbf{CIVA}). Our key observation is that, along a rollout, critic-guided perturbations concentrate in a low-dimensional subspace induced by the victim's own critic. Based on this observation, CIVA first probes the frozen victim offline with critic-guided PGD and extracts a low-rank value-subspace by SVD. At test time, it optimizes only the subspace coefficients, smooths them with an exponential moving average (EMA), and maps them back to pixels. This design attacks value-sensitive recurrent dynamics while keeping the online optimization cheap and temporally coherent. Extensive experiments on DMC walker walk, Atari Pong, and Crafter show that CIVA consistently outperforms five recent methods; on DMC walker walk, it achieves the largest reward drop of 26.07\% while keeping temporal variation low, with TempAbs of 0.646.

---

## 5. WA-JEPA: Rethinking the Video JEPA Paradigm for World-Action Modeling in Autonomous Driving

**Authors:** Xinlin Wang, Yujiao Xiang, Yuheng Zhou, ..., Hangning Zhou, Mu Yang
**arXiv:** [2608.20974](https://arxiv.org/abs/2608.20974)
**Categories:** Computer Vision and Pattern Recognition (cs.CV); Artificial Intelligence (cs.AI)

Video Joint Embedding Predictive Architecture (V-JEPA) learns powerful spatiotemporal representations from video through self-supervised latent feature prediction. However, V-JEPA is built around random-mask completion and deterministic regression, making it fundamentally ill-suited for autonomous driving planning that demands future-directed prediction tightly coupled with action. To address this, we rethink the V-JEPA paradigm and present WA-JEPA, a V-JEPA-native world-action model designed for autonomous driving planning. Instead of random spatiotemporal masking, WA-JEPA employs hybrid future-masked pre-training, where the model infers future latents from observed context. Departing from deterministic regression, we recast future prediction as conditional flow matching over latent futures, which substantially improves the model's ability to generate plausible future latents for downstream planning. Finally, a joint future-action predictor is proposed to denoise future scene tokens and ego trajectories together in a unified spatiotemporal latent space, allowing action supervision to directly shape planning-relevant world representations. Pre-trained on nuPlan videos and fine-tuned on NAVSIM, WA-JEPA reaches 91.7 EPDMS on NAVSIM-v2, surpassing the strongest end-to-end and world-action baselines by 1.6 and 1.3 EPDMS, and, without HUGSIM-specific fine-tuning, attains the best HD-Score of 0.4462 on the closed-loop HUGSIM benchmark under the same evaluation protocol. These results validate V-JEPA-native world-action modeling as a powerful and scalable paradigm for autonomous driving planning. Code is available at this https URL.

---

## 6. CertVLA: Certified Defense against Physical Visual Attacks for Vision-Language-Action Models

**Authors:** Hui Lu, Zhijie Peng, Yuqi Lin, ..., Alex Kot, Xudong Jiang
**arXiv:** [2608.20791](https://arxiv.org/abs/2608.20791)
**Categories:** Computer Vision and Pattern Recognition (cs.CV); Artificial Intelligence (cs.AI)

Vision-Language-Action (VLA) policies are vulnerable to localized physical perturbations, yet existing certified patch defenses target discrete labels and cannot directly certify continuous, temporally correlated actions. We introduce CertVLA, a certified defense for closed-loop VLA control under bounded patch and texture attacks. CertVLA proposes a calibrated region of behaviorally consistent actions, while deterministic covering masks ensure that at least one checked prediction is attack-free. Specifically, CertVLA normalizes action disagreement by the benign variation of each mask pair and accepts a single-mask anchor only when it remains consistent under every second mask. It then calibrates the resulting max-min-max episode score to provide finite-sample clean coverage. Conjoining query-level decisions extends the action certificate to the complete closed-loop rollout. Furthermore, we prove that against any adaptive attacker satisfying the bounded-support threat model, every rollout certified by CertVLA executes only action chunks consistent with attack-erased clean predictions. Under dual-mask rollout correctness, this consistency certificate further guarantees task success. The certificate is independent of patch content, generation method, and physical transformation. Experiments in simulation and the real world demonstrate the empirical and certified effectiveness of CertVLA against patch attacks, with additional simulation validation on texture attacks.

---

## 7. AudioWorldSim: Realistic Binaural Audio Datasets For World Models

**Authors:** Luis Vitor Zerkowski, Luiz Velho
**arXiv:** [2608.21075](https://arxiv.org/abs/2608.21075)
**Categories:** Sound (cs.SD); Machine Learning (cs.LG)

This technical report presents AudioWorldSim, an open-source platform designed to generate realistic binaural audio datasets and advance research in audio-based machine learning, particularly world models. Built as a custom extension of Meta's SoundSpaces 2.0 platform, AudioWorldSim leverages their comprehensive acoustics framework, but focuses on the automatic rollout of random agent navigations, as well as implements crucial fixes to how continuous sound is composed. AudioWorldSim is made publicly available to the research community at this https URL to facilitate reproducibility.

---

## 8. Logic-VLA: A Temporal Logic Conditioned Vision-Language-Action Model

**Authors:** Celina Shiyu Wang, Yiqi Zhao, Junjie Ye, Yue Wang, Jyotirmoy V. Deshmukh
**arXiv:** [2608.20556](https://arxiv.org/abs/2608.20556)
**Categories:** Robotics (cs.RO); Logic in Computer Science (cs.LO); Systems and Control (eess.SY)

Vision-language-action (VLA) models can follow natural-language (NL) task instructions, but such instructions may not precisely specify safety-critical or spatiotemporal requirements on the resulting behavior. We introduce Logic-VLA, a formal-requirement-aware VLA that conditions on Signal Temporal Logic (STL) specifications supplied at inference time. Logic-VLA uses a syntax-graph-based STL encoder pre-trained to capture temporal logic semantics. Policy adaptation proceeds in two stages: STL-conditioned supervised fine-tuning on satisfying demonstrations is followed by trajectory-level preference optimization over matched satisfying-violating rollout pairs using a flow-matching surrogate for Identity Preference Optimization. This formulation improves formal requirement satisfaction while preserving the nominal NL task. We evaluate Logic-VLA in closed-loop quadcopter navigation simulation across randomized photorealistic environments and test generalization to STL formulas unseen during training. Across the evaluation benchmarks, Logic-VLA improves STL satisfaction rate over an STL-blind base policy by 24.8 to 40.7 percentage points (pp) while reducing nominal NL task success by at most 1.8 pp, showing that a single VLA can adapt its behavior to varying formal requirements without requiring a separate policy for each specification.

---

## 9. Just Noticeable Difference Modeling for Token Compression in Vision-Language-Action Models

**Authors:** Zhuoyuan Li, Rui Zhao, Jin Wang, ..., Weisi Lin, Kin-Man Lam
**arXiv:** [2608.21247](https://arxiv.org/abs/2608.21247)
**Categories:** Computer Vision and Pattern Recognition (cs.CV); Robotics (cs.RO)

Token compression has become a key technique for reducing the inference cost of large foundation models, with approaches such as token pruning and KV-cache reuse widely adopted in vision-language models and recently explored for embodied agents. In embodied agents, tokens not only support perception and semantic understanding but also directly affect latency-sensitive closed-loop robot action prediction. Existing schemes typically guide compression using redundancy or importance cues, such as visual similarity, attention scores, and saliency. However, these cues only indirectly measure the key factor for safe compression: how much a token can change before causing an unacceptable deviation in downstream actions. This receiver-dependent tolerance is closely related to the principle of just noticeable difference (JND). Classical JND characterizes signal tolerance in the human visual system, while machine-oriented JND extends this concept to downstream machine responses. Building on this progression, we introduce Action-JND, which extends JND modeling to embodied perception by defining noticeability through the language-conditioned action response of a vision-language-action (VLA) policy in closed-loop control. A token change is considered admissible only when the induced action deviation remains within a tolerated margin. To realize this concept, we develop a lightweight token-wise JND estimator in deep visual-feature space to predict the maximum tolerable perturbation while preserving policy responses. The resulting action-tolerance score serves as a plug-and-play criterion for VLA compression paradigms, including stale-KV reuse and token pruning, prioritizing action-tolerant tokens for compression. Experiments on the LIBERO benchmark with OpenVLA and OpenVLA-OFT demonstrate that Action-JND consistently improves compression reliability, especially under aggressive compression ratios.

---

## 10. A Collaborative Multi-Modality Interaction for VLA-based End-to-End Autonomous Driving

**Authors:** Jingtao Sun, Xiaohai He, Yike Zhang, ..., Ajmal Mian, Mike Zheng Shou
**arXiv:** [2608.20890](https://arxiv.org/abs/2608.20890)
**Categories:** Computer Vision and Pattern Recognition (cs.CV); Robotics (cs.RO)

Vision-Language-Action (VLA) models have emerged as a powerful paradigm for end-to-end autonomous driving by jointly integrating perception, reasoning, and decision making within a unified multimodal framework. However, most existing VLA models formulate end-to-end autonomous driving as a visual question answering task, leading to unreliable and less interpretable decision reasoning. In addition, they fail to establish effective multi-modal interaction across heterogeneous sensors, thereby limiting robust scene perception and reliable driving reasoning in long-tail driving scenarios. To this end, we propose a robust VLA-based end-to-end autonomous driving system that combines multi-modality interaction with multi-trajectory planning and optimization, enabling more reliable, interpretable, and safer driving decisions. Our method comprises three core components: (1) Affinity-Guided Optimal Transport for main-auxiliary modality two-way interaction; (2) Distribution-Consistent Modality Transfer for heterogeneous modality distribution transfer and cross-modal interaction; (3) Multi-modal Multi-Trajectory Planning along with Perception-Oriented Trajectory Refinement for better driving decisions to long-tail driving scenarios. Experimental results in open-loop and closed-loop datasets demonstrate improvements in safety long-horizon driving reasoning and road scene perception over existing driving systems, highlighting the ability of our mutli-modality interaction and multi-trajectory planning and optimization for scalable VLA-based systems.

---

## 11. RISE: Adaptive Imagination for World Action Models

**Authors:** Hongbo Lu, Liang Yao, Chenghao He, ..., Tao He, Pai Peng
**arXiv:** [2608.20430](https://arxiv.org/abs/2608.20430)
**Categories:** Computer Vision and Pattern Recognition (cs.CV)

World Action Models (WAMs) improve planning by incorporating future world evolution into action generation, yet existing methods allocate a fixed imagination budget to every scene. We propose RISE (\textbf{R}efining \textbf{I}magination through \textbf{SE}lective Rollout), a system-level adaptive imagination framework that makes sequential \textsc{Roll}/\textsc{Stop} decisions according to the expected planning benefit of continued rollout. At each step, a Latent Evaluator estimates the risk revealed by the current prefix and how much planning could improve if imagination continues, while a Rollout Gate weighs this expected benefit against additional computation cost. Since factual driving logs expose only one realized future, we further construct \textbf{CounterDrive}, a counterfactual dataset with diverse outcomes and risk levels, to enrich future dynamics and provide localized risk supervision. Each retained sample undergoes expert verification and annotation of trajectory validity, incident onset, and causal category, providing a reusable resource for safety-critical world-modeling research. Experiments on NAVSIM and nuScenes show that RISE achieves the best overall planning performance while reducing unnecessary rollout, with additional transfer results supporting its plug-in generality across WAM architectures.

---
