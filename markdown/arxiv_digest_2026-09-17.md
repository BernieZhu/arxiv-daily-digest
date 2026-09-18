# arXiv Daily Digest — 2026-09-17

**Mode:** direct
**Categories:** cs.AI, cs.LG, cs.RO, cs.CV
**Keywords:** VLA, agentic robot, robot harness
**Papers found:** 10

---

## 1. rMuscle: Robotic Muscle Memory for Efficient Vision-Language-Action Model Inference

**Authors:** Kaijun Zhou, Zhiyang Li, Le Chen, Jinyu Gu
**arXiv:** [2609.19104](https://arxiv.org/abs/2609.19104)
**Categories:** Robotics (cs.RO); Artificial Intelligence (cs.AI)

Factory work is a promising early scenario for embodied AI: assigning repetitive manual jobs to robots has clear economic payoff, and a structured station keeps the jobs tractable for current policies. Vision-Language-Action (VLA) models now dominate as the policy paradigm for these robots. The inference latency of VLA models directly affects robot responsiveness and motion smoothness. However, existing VLA inference frameworks do not fully exploit the characteristics of embodied workloads or account for the distinct bottlenecks across different stages of VLA inference.
In this paper, we first characterize embodied workloads and identify substantial task similarity across repeated robot executions. We further find that such similarity extends beyond observations and action trajectories to internal model states. Drawing on these observations, we present rMuscle, a real-time VLA inference framework inspired by human muscle memory. It exploits cross-execution similarity through a dual-phase muscle-memory cache. The Context Cache reuses visual-token outputs to reduce computation, while the Action Cache reuses neuron activation patterns to reduce weight accesses. We keep both the cache memory footprint and access overhead low through online cache recomputation, sliding-window cache retrieval, and mask sharing across consecutive denoising steps. rMuscle achieves 1.29-1.42X speedup on RTX 4090 and Jetson Thor across LIBERO, RoboTwin, and physical manipulation tasks, while maintaining the original success rates on real-world robots.

---

## 2. ActionPiece: Rethinking Action Tokenization for Autoregressive Vision-Language-Action Models

**Authors:** Shijie Lian, Bin Yu, Zhaolong Shen, ..., Laurence T. Yang, Kai Chen
**arXiv:** [2609.18487](https://arxiv.org/abs/2609.18487)
**Categories:** Robotics (cs.RO); Artificial Intelligence (cs.AI); Computation and Language (cs.CL); Computer Vision and Pattern Recognition (cs.CV)

Action tokenizers play a central role in autoregressive vision-language-action (VLA) models, determining both the targets for policy training and the executable commands recovered from predicted tokens. Their fidelity is commonly evaluated using pointwise reconstruction metrics such as mean squared error (MSE), yet small individual errors do not fully characterize how faithfully action adjustments across demonstrations are preserved. After compression, similar actions may still cluster around a representative motion, while the adjustments needed for different contexts are diminished, distorted, or even reversed. We introduce physical rank consistency (PRC) to measure how well tokenization preserves local physical distance rankings after reconstruction. Evaluating decoded actions provides a common reference across token vocabularies and decoder architectures, complementing pointwise accuracy with a measure of relational fidelity. We further present ActionPiece, which preserves physical action relationships through joint supervision of representation learning and quantization. Physical rank preservation supervises near-far ordering in encoder and quantized feature distances, while quantization regularization applies the same ordering to codeword assignment distributions. Both objectives augment reconstruction, producing discrete action tokens for standard autoregressive policy learning and execution through a frozen decoder. Under the same Qwen3-VL-4B policy training setup, ActionPiece achieves 94.8% on LIBERO and 68.8% on unseen LIBERO-Plus, with additional evaluations reaching 71.9% on SimplerEnv and 51.5% across VLA-Arena L0-L2. Component ablations show that the two objectives jointly improve PRC and policy success, demonstrating the value of physical relationship supervision for action tokenization.

---

## 3. M2Tok: Multi-head Multi-codebook Discrete Action Tokenization for Vision-Language-Action Models

**Authors:** Chunpu Xu, Zhixuan Liang, Yuhao Zhang, ..., Xiaokang Yang, Yao Mu
**arXiv:** [2609.18259](https://arxiv.org/abs/2609.18259)
**Categories:** Robotics (cs.RO); Artificial Intelligence (cs.AI); Computation and Language (cs.CL); Computer Vision and Pattern Recognition (cs.CV)

Recent advancements have successfully adapted autoregressive language models to process multimodal signals, such as images and actions. Since raw action signals are continuous, effective tokenization is essential to map high-dimensional inputs into compact discrete tokens for autoregressive processing. However, existing discrete action tokenizers often suffer from high reconstruction loss, failing to preserve the fine-grained dynamics required for precise control. This "discretization bottleneck" significantly limits the performance ceiling of downstream Vision-Language-Action (VLA) models. To address this, we propose ${M}^2$Tok, a Multi-head Multi-codebook Action Tokenizer designed to minimize reconstruction error and enhance policy performance. Our approach introduces two key structural innovations: (1) we decompose the latent action features into multiple heads, enabling the model to implicitly align specific heads with distinct action dimensions; (2) we assign independent codebooks to each head for quantization. By leveraging the combinatorial nature of multiple codebooks, we significantly expand the representational expressivity of the tokenizer, leading to substantially lower reconstruction loss compared to previous methods. We evaluate the ${M}^2$Tok-based VLA on the RoboTwin, Simpler-Env, and 3 zero-shot real-world tasks. Experimental results demonstrate our method not only achieves superior reconstruction fidelity but also significantly boosts the success rate of VLA models. Comprehensive ablation studies further confirm the effectiveness of the multi-head and multi-codebook mechanisms. Code is available at this https URL.

---

## 4. VLA-ULAP: Interleaving Cloud VLA Calls with Ultra-Lightweight Local Action Prediction at the Edge

**Authors:** Deyu Cao, Ryuji Oi, Kosuke Matsushima, ..., Daichi Fujiki, Atsutake Kosuge
**arXiv:** [2609.18663](https://arxiv.org/abs/2609.18663)
**Categories:** Robotics (cs.RO); Machine Learning (cs.LG)

Billion-parameter vision--language--action (VLA) policies demand substantial onboard power, while communication delays in remote inference hinder timely responses. We propose VLA-ULAP, which interleaves remote VLA calls with an Ultra-Lightweight Local Action Predictor (ULAP). With approximately 7.4M parameters including the frozen vision encoder, ULAP combines current views, proprioception, and executed action history to predict chunks in one pass. Trained independently, it requires no VLA hidden states, online verification, or server round trips. On Jetson Orin Nano, ULAP takes 19.9 ms and 0.183 J per inference, compared with 284.3 ms and 50.55 J for GR00T on RTX A6000. Across three simulated base-policy/benchmark pairs, selected operating points remove 48.8--76.7\% of VLA calls while retaining 95.0--97.5\% of the baseline success rate. Against local VLA-acceleration alternatives on VLA-JEPA, ULAP uses an estimated 49.2\% less inference time and 51.0\% less GPU energy per successful episode than ACT at comparable success rates, and 77.1\% less time and 79.9\% less energy than SP-VLA at equal success rates. Physical SO-101 experiments retain 95.2--100\% of the baseline success rate across seen and held-out placements while reducing inference time by an estimated 47.9--58.0\% and inference-device energy by 52.1--62.5\%, based on successful-episode call counts and measured device costs. Faster responses also improve dynamic-task success rates: in latency-aware LIBERO-Safety simulation, VLA-ULAP exceeds $\pi_{0.5}$ by 11.0 and 15.5 percentage points on two tasks while approximately halving VLA calls.

---

## 5. Reinforcement Learning for Real-Time Vision-Language-Action Policies

**Authors:** Perry Dong, Kuo-Han Hung, Dorsa Sadigh, Chelsea Finn
**arXiv:** [2609.18207](https://arxiv.org/abs/2609.18207)
**Categories:** Robotics (cs.RO); Machine Learning (cs.LG)

Reinforcement learning fine-tuning on top of large, pretrained Vision-Language-Action (VLA) models offers promise for highly reliable robot deployment. However, because of their scale, modern VLA models suffer from high inference latency, so the observation used to select an action is often stale by execution time, creating a distribution shift that can substantially degrade reliability and performance. Prior work has explored asynchronous policy execution to reduce the effect of latency, but these methods are mostly built on imitation learning and offer no mechanism for moving beyond the training distribution toward higher reliability. We close this gap by enabling RL fine-tuning that meets the real-time control requirements of dynamic real-world manipulation. Our approach builds on EXPO-FT, a framework for sample-efficient, reliable VLA fine-tuning with reinforcement learning, and decouples slow, expressive action generation from fast, reactive action edits: a large pretrained VLA proposes action chunks using its strong behavior prior, while a lightweight edit policy performs fast, reactive decision-making by editing actions in response to changes in state, conditioned on the latest observation. We instantiate this as Real-Time EXPO-FT, an RL framework for finetuning real-time VLA policies. On the Kinetix benchmark, Real-Time EXPO-FT enables a delayed policy to achieve the best performance among delayed and non-delayed methods in 10 out of 10 environments. On four dynamic real-world tasks, robot object passing, ball balancing, table soccer kicking, and dynamic object picking, with online robot data capped at 10 minutes, Real-Time EXPO-FT improves average policy performance from 42% to 97%, all without human intervention, demonstrating rapid, sample-efficient adaptation to challenging real-world dynamics. Website: this https URL

---

## 6. Not All Layers Need Tuning: Diagnosing and Directing Adaptation in Vision-Language-Action Models

**Authors:** Shahram Najam Syed, Arthur Jakobsson, Prayuj Sachdev, Jeffrey Ichnowski
**arXiv:** [2609.18084](https://arxiv.org/abs/2609.18084)
**Categories:** Robotics (cs.RO); Computer Vision and Pattern Recognition (cs.CV); Machine Learning (cs.LG)

Fine-tuning a Vision-Language-Action (VLA) model for a new deployment environment is expensive, yet most methods apply uniform-capacity adapters to every network region as if every region requires equal adjustment. This paper tests that assumption on five architecturally diverse VLAs (OpenVLA-OFT, $\pi_0$, SmolVLA, DTP, Octo; 93M-7B parameters). Measuring per-region adaptation cost as normalized parameter displacement under region-isolated fine-tuning reveals an adaptation spectrum in which appearance shifts concentrate cost in the vision encoder, instruction shifts in the language backbone, and novel-object shifts in the vision encoder together with the action head, across all five architectures. To exploit this structure, we introduce a pipeline that observes, diagnoses, allocates, and adapts. From ten unlabeled target observations and without fine-tuning, the diagnostic estimates per-region cost by combining reference-free gradient and Monte Carlo Dropout signals with a Centered Kernel Alignment score against a cached source reference; the allocator converts the estimates into variable-rank LoRA adapters under a parameter budget and freezes well-calibrated regions; and standard LoRA fine-tuning trains the resulting adapters. The diagnostic ranks regions within each deployment at a median Spearman of 0.91, and the allocation matches or exceeds uniform LoRA at every budget we tested on LIBERO and CALVIN. On a physical xArm-7, the pipeline matches full fine-tuning under an instruction-wording shift with 0.04% of its trainable parameters, and on five held-out scenes evaluated without retraining it leads every baseline, with 11-23 successes of 30 rollouts against 8-18 for the strongest parameter-efficient baseline at equal or larger budgets and 2-11 for full fine-tuning. These results suggest that adaptation cost in VLAs is structured enough to measure before fine-tuning begins.

---

## 7. DistAL: Distance-based Advantage Learning for VLA Fine-Tuning

**Authors:** Reece O'Mahoney, Ioannis Havoutis
**arXiv:** [2609.18392](https://arxiv.org/abs/2609.18392)
**Categories:** Robotics (cs.RO)

Vision-language-action models (VLAs) have trans- formed the field of robotic manipulation in recent years by combining the semantic understanding of LLMs with the precise control of flow-matching policies. Advantage conditioning is a recent technique that iteratively improves VLAs by training a value function on deployment data and using this to train an advantage-conditioned policy. Previous works have only applied simple, low-information success/failure rewards, which leave the value function unable to distinguish states of differing quality beyond how far along the task they appear. Motivated by an exploration of out-of-distribution (OOD) detection methods, we introduce Distance-based Advantage Learning (DistAL), which, by using an embedding space distance as a reward, produces a more informative value function and subsequently a higher downstream task success rate. We validate our method on a series of simulation benchmarks and dexterous bi-manual manipulation tasks on real hardware.

---

## 8. ForceDelta-VLA: Distilling Force-Conditioned ActionCorrections for Contact-Rich Manipulation

**Authors:** Ju Dong, Yu Fu, Jian Chen, ..., Angela P. Schoellig, Jianwei Zhang
**arXiv:** [2609.18242](https://arxiv.org/abs/2609.18242)
**Categories:** Robotics (cs.RO)

Force-aware Vision-Language-Action (VLA) policies improve contact-rich manipulation, but typically combine task-level motion and contact-dependent adjustment in a single action prediction. Demonstrations provide no explicit labels for decomposing that prediction into a reusable reference action and a correction. We present ForceDelta-VLA, a correction-distillation framework that constructs an explicit force-correction target using paired predictions from a frozen teacher's force-conditioned and learned force-agnostic modes. A separate delay-correction target accounts for reference-action mismatch and the change in reference state. Training uses asynchronous schedule replay with the cached task context available during execution. The resulting lightweight policy adjusts the reference actions using recent force history and robot state, responding to contact changes between reference-action updates without regenerating complete action chunks. Across nine single-arm and bimanual contact-rich tasks, ForceDelta-VLA achieves an 82.2% mean success rate, compared with 54.4% for the original ForceVLA baseline. Direct execution of our Stage-1 Temporal Teacher achieves 70.6%. Relative to ForceVLA, the complete system reduces mean peak contact force over successful trials by approximately 26% on both platforms.

---

## 9. RAF-VLA: Representation Alignment with the Future for End-to-End Autonomous Driving

**Authors:** Dogun Kim, Yongjae Lee, Joonhee Lim, ..., Moogeun Park, Dongsuk Kum
**arXiv:** [2609.17728](https://arxiv.org/abs/2609.17728)
**Categories:** Robotics (cs.RO)

Recent Vision-Language-Action (VLA) models for autonomous driving have incorporated world modeling by predicting future driving scenes alongside driving actions, demonstrating strong planning performance. Future driving scenes are utilized as dense supervision, encouraging the policy to learn rich internal representations useful for planning. However, these World-Modeling VLAs rely on explicit future generation to learn such representations, thereby introducing two key limitations: additional training burden and inference latency. To address these limitations, we propose RAF-VLA (Representation Alignment with the Future), a VLA-based autonomous driving framework that shapes planning-relevant internal representations through direct guidance from future-frame representations. RAF-VLA employs Future-Aligned Supervised Fine-Tuning, in which a straightforward regularization aligns the policy's hidden states with future-frame representations obtained from a pretrained world encoder while learning driving actions. This simple alignment allows RAF-VLA to avoid the training burden and inference latency associated with future generation. Extensive experiments on the NAVSIM benchmark show that RAF-VLA achieves competitive planning performance against state-of-the-art VLA planners with substantially fewer training samples seen. Moreover, RAF-VLA incurs only 3.8% training overhead and a negligible 1 ms inference overhead.

---

## 10. FIVE-VLA: Fast and EffectIVE Autonomous Driving with Recurrent Action Memory

**Authors:** Kemal Oksuz, Alexandru Buburuzan, Yuhan Yao, Puneet K. Dokania
**arXiv:** [2609.18623](https://arxiv.org/abs/2609.18623)
**Categories:** Computer Vision and Pattern Recognition (cs.CV); Robotics (cs.RO)

State-of-the-art vision-language-action models (VLA) for autonomous driving face critical limitations: excessive parameter counts, inefficient high-resolution image processing, and lack of temporal memory. We introduce Fast and EffectIVE VLA (FIVE-VLA) to address these through two key contributions. First, we employ an efficient vision encoder that processes high-resolution ($448 \times 896$) images while generating only 98 tokens, over $5\times$ fewer than existing approaches, and bypass text generation entirely for single-pass trajectory prediction. Second, we propose Recurrent Action Memory (RAM), a lightweight module that conditions action prediction on previous action tokens, providing temporal context critical for manoeuvres such as overtaking and emergency braking. With only 641M parameters, FIVE-VLA completes $\sim$10% more routes without traffic rule infractions than the previous state-of-the-art VLA on the challenging Bench2Drive closed-loop driving benchmark. Non-reactive open-loop simulation on the large-scale real-world NVIDIA Physical AI AV dataset shows 10.2% and 7.7% lower collision-violation rates than SimLingo in single- and four-view settings, respectively. Additionally, FIVE-VLA runs at $\sim$30 fps on an A100 and $\sim$4 fps on a T4 GPU (proxy to an edge device), representing an 8-30$\times$ speedup over previous methods.

---
