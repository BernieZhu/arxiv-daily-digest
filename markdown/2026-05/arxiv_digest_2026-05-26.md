# arXiv Daily Digest — 2026-05-26

**Mode:** direct
**Categories:** cs.AI, cs.LG, cs.RO, cs.CV
**Keywords:** VLA, world model, world action model
**Papers found:** 27

---

## 1. Back to Parsimonious Latents: Learning Task-Centric World Models from Visual Foundations

**Authors:** Minghao Fu, Fan Feng, Nicklas Hansen, Biwei Huang
**arXiv:** [2605.25620](https://arxiv.org/abs/2605.25620)
**Categories:** Artificial Intelligence (cs.AI)

World models enable agents to predict future dynamics conditioned on actions, making the choice of latent representation central to planning and control. Such representations are often either learned directly from pixels with limited semantic structure or inherited from frozen visual foundation models with excessive task-irrelevant detail, yielding state spaces that are poorly matched to downstream planning and control. This is especially challenging in reward-free offline settings, where the model must learn from fixed trajectories without reward supervision or online interaction. To address this, we propose TC-WM, a framework for turning foundation-model embeddings into compact, task-sufficient world representations. The key design is to treat the pretrained embedding space as a semantic scaffold rather than as the final state space: TC-WM linearly projects high-dimensional visual embeddings into a compact latent as the dynamic space, aligns a subspace with the agent's physical state via contrastive learning, and reconstructs embeddings to preserve useful visual structure. This combines the generality of foundation features with the controllability of task-centric dynamics. Theoretically, we show that TC-WM suffices to identify the underlying task-centric latent factors up to a simple transformation. Empirically, TC-WM enables test-time planning across diverse environments (e.g., Robomimic and D4RL), achieving better world-modeling quality and more precise control than state-of-the-art approaches.

---

## 2. Distilling Game Code World Model Generation into Lightweight Large Language Models

**Authors:** Tyrone Serapio, Arjun Prakash, Haoyang Xu, Kevin Wang, Amy Greenwald
**arXiv:** [2605.24375](https://arxiv.org/abs/2605.24375)
**Categories:** Artificial Intelligence (cs.AI)

Large Language Models (LLMs) have shown great ability in generating executable code from natural language, opening the possibility of automatically constructing environments for AI agents. Recent work on Code World Models (CWMs) demonstrates that LLMs can translate game rules into Python implementations compatible with solvers like Monte Carlo Tree Search. We study this problem in game settings, where generated environments must implement rules, legal actions, state transitions, observations, and rewards. We refer to these game-specific executable models as Game Code World Models (GameCWMs). However, current approaches to generating code world models rely on frontier models and inference-time refinement loops, limiting accessibility and scalability. This work investigates whether GameCWM generation capabilities can be distilled into smaller models through post-training. We introduce: (1) a curated dataset of 30 games spanning perfect and imperfect information games, (2) a verification framework that evaluates generated code against structural and semantic game properties, and (3) a post-training pipeline combining Supervised Fine-Tuning (SFT) with Reinforcement Learning with Verifiable Rewards (RLVR). We experiment with Qwen2.5-3B-Instruct and find that SFT can increase syntactic correctness, while RLVR can improve execution-level adherence to game rules, thereby improving Qwen's ability to generate valid GameCWMs in both perfect and imperfect information games. Overall, our pipeline makes Qwen2.5-3B-Instruct more capable of generating valid GameCWMs, thereby offering a scalable path toward automatic environment generation from natural language.

---

## 3. Reason--Imagine--Act: Closed-Loop LLM Decision Making with World Models for Autonomous Driving

**Authors:** Zhengqi Sun, Yiwen Sun, Boxuan Liu, ..., Tianxu Guo, Jiabin Liu
**arXiv:** [2605.24004](https://arxiv.org/abs/2605.24004)
**Categories:** Artificial Intelligence (cs.AI); Computer Vision and Pattern Recognition (cs.CV); Machine Learning (cs.LG); Robotics (cs.RO)

Large language models (LLMs) are promising for autonomous driving, but semantics-only decision policies can yield physically unsafe behavior in dynamic traffic. Existing methods either perform online language reasoning without explicit dynamics verification or use world models mainly in offline pipelines, leaving a gap between semantic intent and physical feasibility at decision time. We propose Reason--Imagine--Act (RIA), a closed-loop framework that couples an LLM reasoner with an action-conditioned world model for online safety verification. At each step, the LLM proposes an action template and candidate sub-actions, the world model performs short-horizon rollouts, and a safety scorer selects the safest executable action with feedback to the next reasoning step. Under a unified CARLA point-goal protocol (1000 episodes), RIA achieves 80.05% route completion, 51.10% arrival rate, and 0.20% collision rate. Under the same closed-loop interface, RIA consistently outperforms training-free baselines, including CARLA TM and MADA, on core closed-loop metrics. For reproducibility, code is available at this https URL.

---

## 4. Why We Need World Models for AGI: Where LLMs Fail and How World Models May Outperform

**Authors:** Feisal Alaswad, Batoul Aljaddouh, Maher Alrahhal, Poovammal E, Talal Bonny
**arXiv:** [2605.23972](https://arxiv.org/abs/2605.23972)
**Categories:** Artificial Intelligence (cs.AI); Computation and Language (cs.CL); Robotics (cs.RO)

Large language models achieve strong performance in language generation and knowledge-intensive tasks, yet remain limited in settings requiring causal reasoning, persistent state tracking, and long-horizon planning. We argue that these limitations may arise from an objective-level mismatch between sequence prediction and reasoning over latent environment dynamics. To formalize this distinction, we introduce Latent Dynamics Inference (LDI), a conceptual perspective that interprets language and multimodal observations as partial evidence of underlying transition dynamics. To empirically investigate this perspective, we introduce Flux, a sequential reasoning environment specified entirely through natural-language rules. As a proof-of-concept case study, the rules are first compiled into an explicit state-transition simulator, illustrating that structured latent transition dynamics can, in some cases, be operationally extracted from textual rule descriptions. This enables a controlled comparison between the LLMs operating purely over textual observations and reinforcement-learning agents trained directly within the extracted latent state space. Within this case study, agents operating with explicit access to the latent state space exhibit substantially more stable behavior in long-horizon gameplay, achieving an aggregate win rate of approximately 79% versus 11% for LLMs. Qualitative analysis further reveals failure modes consistent with unstable persistent state tracking, including invalid actions, state-tracking errors, and short-horizon reasoning failures. The complete implementation of the Flux environment available at this https URL Within the evaluated setting, these results suggest that strong sequence prediction alone may struggle to support robust long-horizon dynamic reasoning without mechanisms for persistent state tracking and transition modeling

---

## 5. EXPO-FT: Sample-Efficient Reinforcement Learning Finetuning for Vision-Language-Action Models

**Authors:** Perry Dong, Kuo-Han Hung, Tian Gao, Dorsa Sadigh, Chelsea Finn
**arXiv:** [2605.25477](https://arxiv.org/abs/2605.25477)
**Categories:** Robotics (cs.RO); Artificial Intelligence (cs.AI)

The ability to efficiently and reliably learn new tasks has been a foundational challenge in robotics. Vision-Language-Action (VLA) models have demonstrated strong generalization across diverse manipulation tasks, yet pretrained policies consistently fall short of the reliability required for real-world deployment. Reinforcement learning (RL) fine-tuning offers a promising path to bridge this gap, but existing approaches either train from scratch without fully leveraging pretrained priors, or fine-tune VLAs without achieving the sample efficiency and success rates that practical deployment demands. We present EXPO-FT, a system for stable, sample-efficient RL finetuning of pretrained VLA policies that closes this gap. Our system solves a suite of challenging manipulation tasks, including routing string lights and inserting the plug to light it up, striking a pool ball into a pocket, and inserting a flower into a wine bottle, each requiring combinations of high precision, dynamic actions, and robustness to varied initial states. Our system achieves perfect task performance (30/30 successes) across all evaluated tasks within an average of 19.1 minutes of online robot data, outperforming both prior RL-from-scratch and VLA finetuning approaches. We release an open-source codebase with the aim of facilitating broader adoption of RL finetuning of VLA models in robotics.

---

## 6. UWM-JEPA: Predictive World Models That Imagine in Belief Space

**Authors:** Santosh Kumar Radha, Oktay Goktas
**arXiv:** [2605.25313](https://arxiv.org/abs/2605.25313)
**Categories:** Machine Learning (cs.LG); Artificial Intelligence (cs.AI); Robotics (cs.RO); Machine Learning (stat.ML)

World models for partially observed environments must imagine multiple compatible hidden futures and steer between them under counterfactual actions. Joint Embedding Predictive Architectures (JEPAs) do this in latent space, but a vector-valued latent has no internal structure for carrying the belief over hidden continuations through blind rollout. We introduce the Unitary World Model JEPA (UWM-JEPA), a JEPA world model with a density-matrix latent on a joint system-environment space and a learned unitary predictor. The construction preserves the joint-state spectrum exactly during rollout, so the predictor itself cannot dissipate the represented uncertainty.
On a hidden-velocity indicator task requiring five-step forward simulation under a given action sequence with the target observation masked, UWM-JEPA reaches 0.77 accuracy and degrades monotonically as actions are perturbed; a parameter-matched LSTM-JEPA trained under the same counterfactual-target objective and action head collapses to majority-class accuracy (0.53) under every action condition. Under blind rollout, UWM-JEPA loses fewer than ten points of probe R^2 at short horizons while vector-latent baselines lose forty-one and sixty-eight; both nevertheless tie on a held-out context probe, locating the separation in the predictor rather than the encoder. Action sensitivity itself requires training against counterfactual rather than teacher-forced targets, a finding that applies beyond the unitary parameterisation. For JEPA world models to imagine under partial observability, latent geometry and predictor dynamics matter, not frozen context-encoding capacity alone.

---

## 7. ActQuant: Sub-4-bit Action-Guided Quantization for Vision-Language-Action Models

**Authors:** Arash Akbari, Arman Akbari, Masih Eskandar, ..., Stratis Ioannidis, Yanzhi Wang
**arXiv:** [2605.24011](https://arxiv.org/abs/2605.24011)
**Categories:** Computer Vision and Pattern Recognition (cs.CV); Artificial Intelligence (cs.AI)

Vision-Language-Action (VLA) models exhibit remarkable action generation for embodied intelligence, but their heavy compute make deployment on edge platforms impractical. Aggressive, sub-4-bit weight quantization is the natural solution, yet existing post-training quantization (PTQ) methods suffer severe performance degradation in this regime. To address this, we introduce ActQuant, an action-guided mixed-precision PTQ framework that operates in two stages: (1) an inter-tensor bit allocator that assigns each weight matrix a single bit-width based on how much it contributes to predicting the agent's actions; (2) an intra-tensor scale optimizer tunes per-block quantization scales using action-aware curvature, so that dynamic range is concentrated on the weights most influential for control. To deliver the on-device benefits of our aggressive quantization, we further introduce this http URL, an agentic conversion pipeline that ports architectures into a native C/C++ runtime with efficient low-bit kernels. We evaluate ActQuant both in simulation and on a real-world 6-DoF UR3 arm, with all models deployed through this http URL. On the LIBERO benchmark, ActQuant is the only method that operates at or below 3 bits-per-weight, retaining 95.0% on OpenVLA-OFT and 94.8% on $\pi_{0.5}$. Pushed further, ActQuant reaches 2.5 bpw at 90.1% on OpenVLA-OFT, compressing the backbone from 14.3 GB to 2.7 GB (5.3$\times$). On the physical UR3 arm, $\pi_{0.5}$ quantized with ActQuant retains the baseline's success rate while reducing the memory footprint by 2.5$\times$.

---

## 8. Nano World Models: A Minimalist Implementation of Future Video Prediction

**Authors:** Siqiao Huang, Partha Kaushik, Michael Chen, ..., Fernando Moreno-Pino, Max Simchowitz
**arXiv:** [2605.23993](https://arxiv.org/abs/2605.23993)
**Categories:** Computer Vision and Pattern Recognition (cs.CV); Artificial Intelligence (cs.AI); Machine Learning (cs.LG)

World models have become a central paradigm for learning predictive simulators that support generation, planning, and decision-making. Yet, despite rapid progress in industry-scale interactive video generation, the broader research community still lacks compact, reproducible, and easily extensible implementations for studying the design choices underlying modern world models. We introduce Nano World Models, a minimalist codebase for future video prediction centered around diffusion forcing. Nano World Models provides a unified interface for generative objectives, model scales, action-conditioning mechanisms, latent observation spaces, datasets, evaluation protocols, and long-horizon rollout procedures. This design enables controlled studies of world-modeling components that are often entangled across separate implementations. Through experiments across simple control environments, game simulation, and real-robot data, we examine how prediction parameterization, architecture scale, action injection, sampling budget, and domain complexity affect video prediction quality and autoregressive rollout behavior. By releasing code, configurations, evaluation scripts, and pretrained checkpoints, Nano World Models aims to provide a compact yet extensible experimental substrate for open, reproducible, and scientific world-model research.

---

## 9. A World Model of Radiologist Reading for Medical Image Representation Learning

**Authors:** Yiwei Li, Zihao Wu, Huaqin Zhao, ..., Tianming Liu, Lin Zhao
**arXiv:** [2605.23992](https://arxiv.org/abs/2605.23992)
**Categories:** Computer Vision and Pattern Recognition (cs.CV); Artificial Intelligence (cs.AI)

Radiologist eye-tracking data provide a rich record of how experts search, compare, and accumulate evidence during image reading; yet, existing methods exploit this signal only partially, either as a static spatial prior or as an auxiliary prediction target decoupled from diagnosis. We propose GazeWorld, a medical imaging world model that treats the image as the world and the radiologist's fixation sequence as a trajectory through it. GazeWorld autoregressively predicts the latent representation of the next fixated patch from all previously visited ones, while a spatial-completion branch covers unvisited regions. At inference, GazeWorld generates a sequence of patch representations from the image alone without requiring real gaze data. Frozen GazeWorld features achieve state-of-the-art diagnostic accuracy across all nine supervised settings on CheXpert, RSNA Pneumonia, and SIIM-ACR Pneumothorax, as well as the highest zero-shot accuracy on all three benchmarks. On the GazeSearch benchmark, a generic decoder trained on the same frozen features outperforms the purpose-built LogitGaze-Med by over 16\% in ScanMatch and 22\% in SED, despite not being explicitly trained to predict gaze. GazeWorld demonstrates that modeling how experts read, not just what they conclude, offers a promising pretraining paradigm for medical imaging AI.

---

## 10. Reinforcement Learning for Laser Additive Manufacturing Scan-Order Optimisation: A Bilevel Proxy--FEA Diagnostic Framework for Reward and World-Model Diagnosis

**Authors:** Xian Wu, Haoran Li, Dongbin Zhao, ..., Yuanqi Chu, Bin Wang
**arXiv:** [2605.25063](https://arxiv.org/abs/2605.25063)
**Categories:** Machine Learning (cs.LG); Materials Science (cond-mat.mtrl-sci)

Reinforcement learning offers a promising approach for scan-order optimisation in laser additive manufacturing, where sequential scan decisions critically influence thermal accumulation, residual stress, distortion, and final part quality. A central challenge in applying RL to this domain lies in reward and world-model fidelity: full finite-element analysis is computationally prohibitive for dense in-the-loop evaluation, while cheap thermo-inspired proxy metrics, though efficient, may capture only partial aspects of the true thermo-mechanical objectives. This paper investigates a bilevel Proxy--FEA diagnostic framework for reward and world-model diagnosis in reinforcement-learning-guided scan-order optimisation. The lower level employs lightweight scan-path and thermo-inspired proxies for rapid candidate generation and preliminary policy-side screening, while the upper level utilises sparse Abaqus FEA simulations to provide simulation-based reference labels. The framework is examined on a simplified whole-track heating LDED32 stripe benchmark comprising ten representative scan strategies. Final-cooling residual Mises stress, U3 vertical distortion, and PEEQ plasticity metrics reveal an observed stress--distortion trade-off rather than a single monotonic quality objective. Within the evaluated set, the center_out strategy emerges as a robust compromise candidate, while raster_left_to_right and edge_in form opposing endpoints of the trade-off. Proxy--FEA alignment analysis shows that current cheap path-based metrics predominantly capture distortion-related (U3) behaviour and exhibit only weak correlation with the sparse FEA reference labels. These findings highlight that proxy-only reward designs risk misalignment in future RL training and underscore the value of sparse FEA reference signals for diagnostic-guided reward and world-model refinement prior to large-scale policy optimisation.

---

## 11. ECHO: Terminal Agents Learn World Models for Free

**Authors:** Vaishnavi Shrivastava, Piero Kauffmann, Ahmed Awadallah, Dimitris Papailiopoulos
**arXiv:** [2605.24517](https://arxiv.org/abs/2605.24517)
**Categories:** Machine Learning (cs.LG); Computation and Language (cs.CL)

CLI agents are the closest thing language models have to an embodied setting: the model emits commands, the terminal executes them, and the returned stream -- stdout, errors, files, logs, and traces -- records the consequences. We argue that this stream is a supervision signal, but standard agent RL discards it: GRPO-style training updates action tokens with sparse outcome-level rewards while ignoring environment responses already in the rollout. Failed rollouts provide little policy-gradient signal despite containing rich evidence about how the environment responds. We introduce ECHO (Environment Cross-entropy Hybrid Objective), a hybrid objective that combines the standard policy-gradient loss on action tokens with an auxiliary loss that trains the policy to predict environment observation tokens resulting from its own actions. ECHO reuses the same forward pass as GRPO, requires no additional rollouts, and turns terminal feedback into dense supervision for all rollouts. ECHO doubles GRPO pass@1 on TerminalBench-2.0: Qwen3-8B improves from 2.70% to 5.17%, and Qwen3-14B from 5.17% to 10.79%. ECHO also produces policies that better predict terminal dynamics, even on trajectories they did not generate: across held-out rollouts, it sharply reduces environment-token cross-entropy while GRPO alone barely changes it. From base Qwen3-8B, ECHO matches expert-SFT-then-GRPO performance on held-out terminal tasks without expert demonstrations, and recovers roughly half of the expert-SFT initialization benefit on TerminalBench-2.0. In some settings, the environment prediction loss alone enables verifier-free self-improvement, allowing policies to improve on unseen OOD tasks by learning only from environment interactions. Together, these results suggest that environment observations are not merely context for future actions, but a dense, on-policy supervision signal already present in every rollout.

---

## 12. Capability and Robustness Cannot Both Be Free: An Information-Theoretic Bound for Vision-Language-Action Models

**Authors:** Jianwei Tai
**arXiv:** [2605.25889](https://arxiv.org/abs/2605.25889)
**Categories:** Cryptography and Security (cs.CR); Machine Learning (cs.LG)

Vision-Language-Action (VLA) models are increasingly deployed on real robots, where each predicted action is executed and each failure carries a safety cost. They reach high success rates on clean inputs but collapse under small adversarial perturbations. A $16/255$ PGD attack on OpenVLA-7B drops LIBERO success from above $95\%$ to under $5\%$. Empirical defenses recover some robustness at a cost in clean accuracy, but the literature does not say whether the trade-off has a theoretical floor. We prove that it does. For any VLA policy with discrete actions, the sum of capability (mutual information between policy action and oracle action) and robustness (mutual information preserved under adversarial perturbation, net of trivial channel leakage) is upper-bounded by a policy-independent budget: task entropy plus adversarial channel capacity. The proof is two applications of the Data Processing Inequality plus MI non-negativity. The pixel-level bound is policy-independent but loose ($\sim 10^3$ nats); an encoder-specific corollary tightens it on a per-experiment basis to $\approx 86$--$156$ nats at $\eps=8/255$ on OpenVLA, depending on which defense is in place. We validate the bound across $252$ closed-form Gaussian-VLA cells and $48$ OpenVLA-7B $\times$ LIBERO $\times$ PGD cells (zero violations). The encoder bound additionally diagnoses where a defense intervenes in the channel: input-side defenses (JPEG-50) shift the encoder budget by $+41$ to $+101$ nats across $\eps \in \{2,4,8,16\}/255$ ($+68$ at $\eps=8/255$), while LLM-side defenses (rank-16 LoRA) shift it by $\le 9\%$ at every $\eps$ and only $0.7\%$ at $\eps=8/255$. We propose encoder-specific slack as a diagnostic axis paired with raw $\Rob$ for defense reporting, and release all code, manifests, and results.

---

## 13. X-DiffVLA: X-Embodied Diffusion Action Heads for Vision-Language-Action Models

**Authors:** Boyu Li, Chaoyi Xu, Haoqi Yuan, ..., Haoran Li, Zongqing Lu
**arXiv:** [2605.25044](https://arxiv.org/abs/2605.25044)
**Categories:** Robotics (cs.RO)

Learning universal policies from cross-embodied data remains a fundamental challenge in robotics. Although Vision-Language-Action (VLA) models are pre-trained on large and diverse datasets, they typically rely on embodiment-specific fine-tuning to achieve strong performance in downstream tasks. This requirement severely limits their generalization capability and restricts knowledge transfer across embodiments performing similar tasks. To overcome these limitations, we focus on cross-embodied settings with shared robotic bases and heterogeneous end-effectors, and propose X-DiffVLA, a diffusion-based VLA model featuring a unified cross-embodied action head. X-DiffVLA can leverage the generative strengths of diffusion models to capture both the diversity and latent correlations in cross-embodied datasets. Specifically, we introduce Embodiment Forcing, a classifier-free guidance technique to implicitly steer action generation toward embodiment-specific functional components, capturing fine-grained structural nuances without explicit supervision. In addition, a Morphological Tree Diffusion approach is designed to strengthen behavioral correlations across diverse end-effectors, maximizing the transferability of heterogeneous demonstrations. Experimental results across RoboCasa and Isaac Gym, covering different embodiments from grippers to dexterous hands, show that X-DiffVLA achieves state-of-the-art performance, with improvements of 15.3% and 12.5%, respectively. Real-world evaluations further validate the robustness of the proposed framework and its effectiveness in scalable cross-embodied policy learning.

---

## 14. Afford-VLA: Action-Aligned Visual Planning via Internalized Affordance

**Authors:** Runze Wang, Yuqian Fu, Yu Li, ..., Yu-Gang Jiang, Xiangyang Xue
**arXiv:** [2605.24203](https://arxiv.org/abs/2605.24203)
**Categories:** Robotics (cs.RO)

Vision-language-action (VLA) models have shown strong potential for generalist robot manipulation, yet they remain limited by insufficient spatial reasoning, particularly in determining where to interact in complex visual scenes. While recent efforts introduce various forms of visual planning to address this issue, existing approaches either rely on global geometric cues, symbolic intermediate representations, or externally generated visual signals, which are often weakly coupled with downstream action prediction. In this work, we revisit visual planning in VLA systems and argue that effective planning should be local, visually grounded, internally generated, and directly aligned with action. Based on this insight, we propose Afford-VLA, a unified framework that internalizes task-conditioned affordance as an explicit visual planning interface within VLA models. Concretely, we introduce learnable <AFF> tokens to query task-relevant interaction regions, decode affordance masks from multimodal features, and convert them into compact embeddings that directly condition action generation. This design enables affordance to be both generated and utilized within the VLA, forming a tightly coupled perception-action pathway. To further support this integration, we adopt a training strategy that allows the affordance pathway to be jointly optimized with action prediction, improving its effectiveness for downstream control. We evaluate our method on multiple simulation benchmarks, including LIBERO, LIBERO-Plus, and SimplerEnv, achieving consistent state-of-the-art performance, along with strong real-world results. These findings demonstrate that internalizing affordance as action-aligned visual planning provides a powerful paradigm for improving VLA systems.

---

## 15. Drift-Resistant Navigation World Model with Anchored Epipolar Guidance

**Authors:** Po-Chien Luan, Zimin Xia, Wuyang Li, Yang Gao, Alexandre Alahi
**arXiv:** [2605.24761](https://arxiv.org/abs/2605.24761)
**Categories:** Computer Vision and Pattern Recognition (cs.CV); Robotics (cs.RO)

We propose Drift-Resistant Navigation World Model, a generative model that mitigates both perceptual drift and geometric drift in conventional rollout-based navigation world models. Existing methods recursively feed generated content into subsequent steps, causing noise accumulation and degraded predictions, i.e., perceptual drift. Meanwhile, their predictions often deviate from the agent's motion, resulting in geometry drift. We address both types of drift by redesigning world-model prediction as an anchor-guided rollout. Instead of rolling out every frame sequentially, we first predict sparse future anchors that serve as stable long-range targets, and then generate intermediate frames within each chunk conditioned on both past context and future anchors. Importantly, these sparse anchors also provide geometric constraints, supported by bidirectional epipolar geometry, to localize where corresponding content should appear in the intermediate frames. Experiments on four benchmarks demonstrate consistent improvements over strong baselines in long-horizon visual quality, geometric consistency, and multi-view coherence. These gains further translate into improved downstream planning performance under the same planners, highlighting the importance of drift-resistant, geometry-aware prediction for reliable navigation world models.

---

## 16. Understanding the Impact of Geometric Foundation Models on Vision-Language-Action Models

**Authors:** Yurou Yang, Muyuan Lin, Roberto Martin-Martin, ..., Cheng-Hao Kuo, Luca Carlone
**arXiv:** [2605.24642](https://arxiv.org/abs/2605.24642)
**Categories:** Computer Vision and Pattern Recognition (cs.CV); Robotics (cs.RO)

Recent work explores new opportunities at the intersection of vision-language-action models (VLAs) and geometric foundation models (GFMs) for 3D reconstruction, such as VGGT. While the resulting geometric VLAs often show improved performance, it remains unclear (i) if modern VLAs already have sufficient geometric understanding to start with, (ii) what is the best architecture to inject geometric understanding into a VLA, and (iii) what is the effect of other design choices that affect geometric VLAs. In this paper we provide a rigorous experimental analysis to shed light on these questions, for a specific choice of VLA (GR00T-N1.5) and GFM (VGGT). Our first contribution is to formalize prior work's intuition that current VLAs lack geometric understanding, by providing a rigorous analysis based on linear probing. The analysis quantifies, for the first time, the "geometric gap" between VLAs and GFMs. Our second contribution is to identify and compare different strategies to bridge GFMs with VLAs. We implement three different architectures, which differ in the way they inject geometry in the VLA, while keeping low-level implementation details as similar as possible, to ensure a fair comparison. Finally, we analyze the impact of non-architectural choices (e.g., training data, number of cameras, reconstruction quality) on the performance of the geometric VLAs.

---

## 17. WBench: A Comprehensive Multi-turn Benchmark for Interactive Video World Model Evaluation

**Authors:** Kaining Ying, Hengrui Hu, Siyu Ren, ..., Xunliang Cai, Henghui Ding
**arXiv:** [2605.25874](https://arxiv.org/abs/2605.25874)
**Categories:** Computer Vision and Pattern Recognition (cs.CV)

Interactive world models are advancing rapidly, yet existing benchmarks cover only part of the required competencies, leaving no unified standard for systematic evaluation. To fill this gap, we introduce WBench, a comprehensive multi-turn benchmark for interactive world model evaluation along five dimensions, namely video quality, setting adherence, interaction adherence, consistency, and physics compliance. WBench contains 289 test cases and 1,058 interaction turns, where each case specifies a world setting and a multi-turn interaction sequence, covering diverse scenes, styles, subjects, and both first- and third-person perspectives, together with four interaction types, including navigation, subject action, event editing, and perspective switching. For navigation, WBench unifies text, 6-DoF pose, and discrete-action control, enabling evaluation of models with different native input interfaces. Evaluation uses 22 automatic sub-metrics that combine specialist vision models with large multimodal models, and all metrics are validated against human judgments. Across 20 state-of-the-art models, we find that no single model performs strongly across all dimensions. We provide detailed diagnostic insights into the characteristic strengths, weaknesses, and open challenges of each model. Code and data are available at this https URL.

---

## 18. Rethinking VLM Representation for VLA Initialization

**Authors:** Weifeng Lin, Siyuan Huang, Hao Li, ..., Jianbo Liu, Hongsheng Li
**arXiv:** [2605.25802](https://arxiv.org/abs/2605.25802)
**Categories:** Computer Vision and Pattern Recognition (cs.CV)

Vision-Language-Action (VLA) models widely adopt pretrained Vision-Language Models (VLMs) as policy backbones, yet it remains unclear what kind of pretrained VLM representation is useful as a VLA initialization. In this paper, we study VLA initialization as a controlled representation-design problem along three axes: capability-level embodied VQA supervision, parameter-update strategy, and robot-data pretraining. Our experiments show that the original pretrained VLM representation is a key source of action performance. However, embodied VQA adaptation does not yield uniform gains: its benefit depends on downstream bottlenecks, and gains from different capability domains are not simply additive. For update strategy, LoRA provides a more reliable initialization than Full Finetune, indicating that overly reshaping the pretrained representation can weaken VLA initialization. Robot-data pretraining further improves VLA initialization, with the strongest variant obtained by staged LoRA-based training. Together, these findings suggest that effective VLM-to-VLA adaptation should inject action-relevant embodied and robot-trajectory signals while preserving the pretrained VLM representation that remains useful for action learning.

---

## 19. WorldCraft: From Camera Navigation to Object Manipulation in Interactive Video World Models

**Authors:** Bohai Gu, Taiyi Wu, Yueyang Yuan, ..., Alan Zhao, Song Guo
**arXiv:** [2605.25077](https://arxiv.org/abs/2605.25077)
**Categories:** Computer Vision and Pattern Recognition (cs.CV)

Recent video-based world models have made pixel-space environments interactive at the camera level: users can navigate viewpoints while the model generates coherent visual continuations. Yet their action spaces remain incomplete: users can move the camera, but cannot act on individual objects. Since real-world interaction is inherently object-centric, such models remain closer to passive scene observers than truly manipulable environments. We present WorldCraft, a framework that expands interactive video world models from camera navigation to object-level trajectory actions. Given a user click and a sketched path, WorldCraft generates future frames in which the selected object follows the prescribed trajectory while the camera continues to navigate the scene. WorldCraft achieves this through a trajectory-centric control pipeline: First, Normalized World Trajectory (NWT) represents user-drawn motion in a camera-invariant world coordinate system and dynamically re-projects it under the current camera pose, separating object motion from camera-induced screen-space displacement; Spatial-Pathway LoRA (SP-LoRA) then injects this world-space signal through the model's spatial-control pathway, adding object manipulation capability while preserving the pretrained camera controller; finally, Trajectory-Anchored State Persistence (TASP) treats the world trajectory as a persistent spatial state and refreshes autoregressive memory after trajectory-conditioned generation, allowing moved objects to reappear at their updated positions after leaving the camera view. Experiments show that WorldCraft enables accurate object control, preserves the video-based world model's camera fidelity under camera-only evaluation, and maintains object state across long autoregressive rollouts with off-camera excursions.

---

## 20. X-Foresight: A Joint Vision-Action Causal Forecasting Network via Predictive World Modeling

**Authors:** Baolu Li, Jingyu Qian, Rui Guo, ..., Yu Zhang, Xianming Liu
**arXiv:** [2605.24892](https://arxiv.org/abs/2605.24892)
**Categories:** Computer Vision and Pattern Recognition (cs.CV)

Physical world knowledge resides mainly in videos. Equipping Vision-Language-Action (VLA) models with such knowledge is fundamental for safe and generalizable planning. Predictive world modeling enables VLA to internalize physical dynamics and long-term causality by predicting future video from past observations. However, naive next-frame prediction faces two challenges: 1) unlike semantically distinct text tokens, video tokens are low-entropy and redundant, causing prediction to degenerate into trivial extrapolation. 2) world modeling poses a temporal dilemma: dense prediction captures instantaneous dynamics, but cannot efficiently model long-horizon causality.
To learn world knowledge effectively, we introduce X-Foresight, a predictive world model integrated directly into the VLA architecture to jointly learn world modeling and real-time action control. At its core lies a long-horizon chunk-wise auto-regressive strategy that addresses both challenges: by predicting semantically distant chunks rather than adjacent frames, it escapes trivial extrapolation, while preserving dense intra-chunk frames for instantaneous dynamics and sparse inter-chunk transitions for long-term causality. A curriculum learning schedule progressively extends prediction horizons and stabilizes long-horizon training. To capture long-term causality effectively, we present temporal importance sampling, which concentrates supervision on safety-critical chunks identified by ego-motion and behavioral signals. We further delegate photorealistic synthesis to a diffusion-based multi-view renderer, improving photorealistic appearance.
Comprehensive experiments demonstrate that X-Foresight significantly outperforms VLA baselines in planning performance while maintaining strong generative fidelity, establishing a robust paradigm for world-knowledge-driven autonomous systems.

---

## 21. QuoVLA: Quotient Space for Vision-Language-Action Models

**Authors:** Xuan Wang, Yinan Wu, Haoran Duan, Jungong Han
**arXiv:** [2605.24890](https://arxiv.org/abs/2605.24890)
**Categories:** Computer Vision and Pattern Recognition (cs.CV)

Vision-Language-Action (VLA) models commonly adapt pretrained Vision-Language Models (VLMs) to robot control by mapping visual observations and language instructions to continuous actions. Existing approaches typically take an action-insufficiency view, assuming that pretrained VLM latents either lack directly usable action information or should be shielded from action-learning signals. Against this view, our \textit{Quotient Theory for VLA} shows that pretrained VLM latents are not action-insufficient but action-sufficient: they already contain the information needed for control, yet remain overcomplete by distinguishing prompt-level variations that induce the same optimal action behavior. To operationalize this theory, we propose QuoVLA, a quotient-space framework for VLA that compresses pretrained VLM latents into action-sufficient representations. Specifically, QuoVLA instantiates this principle with a quantization module and a dual-branch design with relative temporal-complexity regularization, preserving action-relevant information while removing prompt-level redundancy. Extensive experiments across multiple benchmarks demonstrate that QuoVLA achieves strong performance, with particularly notable improvements in generalization under visual, linguistic, and environmental distribution shifts. Our code will be made publicly available.

---

## 22. World Models as Group Actions

**Authors:** Zijie Wang, Wei Zhang, Weiming Zhang, ..., Yipeng Qin, Guanbin Li
**arXiv:** [2605.24578](https://arxiv.org/abs/2605.24578)
**Categories:** Computer Vision and Pattern Recognition (cs.CV)

Video world models have achieved strong visual realism, but this does not ensure that their dynamics are truly governed by actions. In this work, we argue that action faithfulness should be understood through the compositional structure of actions, which in many embodied settings follows a group structure (e.g., SE(2) for navigation). Based on this insight, we formalize action-conditioned world modeling as realizing a group action on the state space, providing a principled criterion for evaluating dynamics beyond visual quality. To operationalize this framework, we propose a unified approach that enforces identity, inverse, and composition consistency via latent-space regularization with synthesized supervision, avoiding additional data collection. We further introduce two metrics: Group-Action Consistency (GAC) and Group-Action Robustness (GAR), to evaluate structural correctness and rollout stability. Extensive experimental results show that our method consistently improves both GAC and GAR in state-of-the-art video world models without degrading perceptual quality.

---

## 23. SparseWorld: Enhancing End-to-End Autonomous Driving via World Models with Sparse Scene Representation

**Authors:** Ruoyu Wang, Jingke Wang, Yukai Ma, ..., Aixue Ye, Yong Liu
**arXiv:** [2605.24354](https://arxiv.org/abs/2605.24354)
**Categories:** Computer Vision and Pattern Recognition (cs.CV)

Recently, world models have made significant progress in enhancing end-to-end driving systems through both future situation forecasting and improved scene understanding. However, existing driving world models are typically built upon dense scene representations, causing high computational costs and redundant information. In this paper, we present SparseWorld, a lightweight world model that focuses on predicting only the critical layout of the scene, enabling efficient future forecasting for end-to-end driving systems. SparseWorld first performs autoregressive rollout to forecast future map elements and surrounding agents, enabling the model to learn how driving scenarios evolve over time. It then leverages these predicted futures to refine downstream motion prediction and trajectory planning. Specifically, we propose a Sparse Dreamer that anticipates future instances in the latent space through joint temporal and spatial attention. By interacting with predicted future instances, the motion planner captures more accurate motion patterns and generates more informed and safety-aware trajectories. Extensive experiments demonstrate that SparseWorld significantly reduces collision risk and achieves state-of-the-art performance on the open-loop planning metrics of the nuScenes dataset with a collision rate of 0.05\%. Moreover, it substantially outperforms the baseline method in closed-loop planning metrics on the Bench2Drive benchmark. Supplementary material is available at the project page: this https URL.

---

## 24. Causal Physics Steering in Video World Models via Concept Activation Vectors

**Authors:** Nahid Alam
**arXiv:** [2605.24322](https://arxiv.org/abs/2605.24322)
**Categories:** Computer Vision and Pattern Recognition (cs.CV)

Video world models learn representations of physical dynamics, but controlling their physical expectations at inference time remains an open problem. Recent interpretability work identified a Physics Emergence Zone (PEZ), a group of middle transformer layers in VideoMAE where physical plausibility is represented separately from other visual features. However, it remained unclear whether this structure could be used to directly control the model's physics reasoning. We present physics steering, a training-free method that uses the weight vector of a linear probe at a PEZ layer as a Concept Activation Vector (CAV) and injects it into hidden states during inference. This shifts the model's physical expectations without changing any model weights. On the IntPhys benchmark, this intervention reliably shifts the model's plausibility judgment in either direction, depending on the steering sign. The effect appears only when the intervention is applied within the Physics Emergence Zone, suggesting that the relevant physics representation is localized there. We further find that physics is encoded separately from motion direction, and that different intuitive physics principles occupy distinct directions within this representation space. Together, these results show that physical reasoning in VideoMAE is not only readable, but also directly steerable.

---

## 25. Unified 3D Scene Understanding Through Physical World Modeling

**Authors:** Wanhee Lee, Klemen Kotar, Rahul Mysore Venkatesh, ..., Khai Loong Aw, Daniel L. K. Yamins
**arXiv:** [2605.24321](https://arxiv.org/abs/2605.24321)
**Categories:** Computer Vision and Pattern Recognition (cs.CV)

Understanding 3D scenes requires flexible combinations of visual reasoning tasks, including depth estimation, novel view synthesis, and object manipulation, all of which are essential for perception and interaction. Existing approaches have typically addressed these tasks in isolation, preventing them from sharing a common representation or transferring knowledge across tasks. A conceptually simpler but practically non-trivial alternative is to unify these diverse tasks into a single model, reducing different tasks from separate training objectives to merely different prompts and allowing for joint training across all datasets. In this work, we present a physical world model for unified 3D understanding and interaction (3WM), formulated as a probabilistic graphical model in which nodes represent multimodal scene elements such as RGB, optical flow, and camera pose. Diverse tasks emerge from different inference pathways through the graph: novel view synthesis from RGB and dense flow prompts, object manipulation from RGB and sparse flow prompts, and depth estimation from RGB and camera conditioning, all zero-shot without task-specific training. 3WM outperforms specialized baselines without the need for finetuning by offering precise controllability, strong geometric consistency, and robustness in real-world scenarios, achieving state-of-the-art performance on NVS and 3D object manipulation. Beyond predefined tasks, the model supports composable inference pathways, such as moving objects aside while navigating a 3D environment, enabling complex geometric reasoning. This demonstrates that a unified model can serve as a practical alternative to fragmented task-specific systems, taking a step towards a general-purpose visual world model.

---

## 26. OASIS: Observation-Action Space Alignment via SE(3) Trajectory Prediction for Robotic Manipulation

**Authors:** Xinzhe Chen, Sihua Ren, Liqi Huang, ..., Zeyang Liu, Xuguang Lan
**arXiv:** [2605.25829](https://arxiv.org/abs/2605.25829)
**Categories:** Robotics (cs.RO); Artificial Intelligence (cs.AI)

Recent vision-language-action (VLA) models and world action models (WAMs) advance robotic manipulation by enriching intermediate representations with auxiliary spatial features or future visual-state prediction. However, these representations largely remain within the observation space and do not share the rigid-body geometry of the action space, forcing the action decoder to implicitly recover this geometry. We propose OASIS, a visuomotor policy that aligns the intermediate representation with the action space via $SE(3)$ end-effector trajectory prediction. OASIS couples a 3D-aware feature encoder that fuses vision-language and metric-depth features with an $SE(3)$ trajectory predictor that produces a camera-frame end-effector trajectory. Conditioned on the predictor's pose-supervised hidden states, the action decoder generates action chunks consistent with rigid-body motion. Across simulation and real-world experiments, OASIS outperforms VLA and WAM baselines in success rate and out-of-distribution generalization. Our project page is available at this https URL.

---

## 27. Teaching Video Generators to Remember: Eliciting Dynamic Memory for Out-of-Sight State Evolution

**Authors:** Tianshuo Xu, Yichen Xie, Depu Meng, ..., Yihan Hu, Wei Zhan
**arXiv:** [2605.25333](https://arxiv.org/abs/2605.25333)
**Categories:** Computer Vision and Pattern Recognition (cs.CV)

Video world models should maintain evolving states when evidence is unobserved, yet current generators often freeze hidden states upon interruption. This is not simply a capacity problem: pretrained video diffusion transformers already possess KV-cache mechanisms capable of non-local retrieval, but they are rarely trained to use them as dynamic memory. We introduce ReMind, a framework eliciting dynamic memory behavior via memory-oriented data, event-aware training, and cache adaptation. Organized around a taxonomy of 100+ dynamic events, we build a camera-annotated training mixture combining VLM-filtered real videos, generated hard dynamics, synthetic camera loops, and memory-interruption augmentations. Each clip is converted into a frame graph with protected anchors, degraded intervals, and explicit temporal gaps. A node-structured curriculum, including node-drop, noisy memory, frontier continuation, and reference-cache training, forces the model to retrieve relevant past states across interruptions rather than relying solely on local continuity. PM-RoPE, an elegant camera-phase RoPE extension, unlocks spatiotemporal retrieval at a single-attention cost while preserving pretrained pathways. ReMind achieves the best overall scores on STEVO-Bench and recovery tasks. Furthermore, general image-to-video evaluations confirm this curriculum avoids catastrophic forgetting. We will open-source our code, data, and models.

---
