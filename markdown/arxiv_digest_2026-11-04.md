# arXiv Daily Digest — 2026-11-04

**Mode:** direct
**Categories:** cs.AI, cs.LG, cs.RO, cs.CV
**Keywords:** VLA, RSI, agentic robot, self-improving robot, self-evolving robot, robot harness
**Papers found:** 7

---

## 1. Human-to-Robot Transfer via Bridging Representation and Action Space in VLAs

**Authors:** Junhyeong Park, Wook Jung, Taeyoung Kim, Huiwon Jang, Jinwoo Shin
**arXiv:** [2611.04391](https://arxiv.org/abs/2611.04391)
**Categories:** Artificial Intelligence (cs.AI)

Pretrained Vision-Language-Action (VLA) policies provide a strong starting point for deployment, but adapting them to a target robot and environment still requires costly embodiment-specific demonstrations. Human demonstrations are far easier to collect, yet directly leveraging them is challenging due to the substantial human-robot embodiment gap, particularly when the underlying VLA has been pretrained primarily on robot data. We introduce H2RB (Human-To-Robot Bridge), a human-robot co-training framework for adapting pretrained VLA policies from unpaired human and robot demonstrations. H2RB bridges the embodiment gap at both interfaces: geometry-anchored alignment grounds human and robot observations in a compatible representation, while a decoupled-decoder tokenizer shares action latents without forcing both domains through a single action mapping. This design allows human demonstrations to provide useful behavioral supervision while retaining the rich visual, semantic, and control priors of the pretrained VLA. Across real-world tasks, H2RB substantially improves object transfer performance from 8.0 to 51.8 and enables skill transfer to score 62.7, in settings where co-train baselines totally fail to transfer human-demonstrated skills. The benefit also persists under object-placement shifts, improving out-of-distribution transfer from 6.0 to 45.3. H2RB suggests a way for human demonstrations to serve as a scalable supervision source for adapting pretrained robotic policies, reducing the dependence on costly target-robot data collection.

---

## 2. Training LLM Agents to Automate LLM Post-Training with RSI-Dojo

**Authors:** Shuzheng Gao, Zhaojian Yu, Penghao Yin, ..., Shilin He, Michael R. Lyu
**arXiv:** [2611.03698](https://arxiv.org/abs/2611.03698)
**Categories:** Artificial Intelligence (cs.AI)

Recursive Self-Improvement (RSI) aims to enable AI systems to autonomously build and improve AI systems themselves, including models, harnesses, and underlying infrastructure. Within this broader agenda, a central capability is enabling agents to train and improve base models. However, existing studies on automated model training primarily focused on workflow- or harness-level optimizations, rather than internalizing the ability to conduct post-training into the model itself. Developing this capability requires executable model training environments that can produce high-quality trajectories demonstrating how to select data, train models, diagnose failures, and iteratively improve results. In this paper, we introduce RSI-Dojo, a collection of executable model training environments designed to teach LLM agents to conduct post-training. To construct RSI-Dojo, we develop RSI-Craft, an automatic pipeline that converts human research artifacts into executable model training environments. RSI-Craft automatically collects research papers from top venues, instantiates datasets and metrics into a unified interface, and reproduces evaluation dependencies. It then filters tasks by data size, execution reliability, and discriminability, yielding RSI-Dojo with 281 seed model training tasks. Building on RSI-Dojo, we employ a trajectory collection method with an improved harness to collect high-quality model-training trajectories from frontier models, then retain examples through rubric-based and outcome-based filtering. We fine-tune Qwen3.5-9B and Qwen3.6-35B-A3B on these trajectories. The resulting RSI-Dojo-9B and RSI-Dojo-35B-A3B improve over their base models by 8.74 and 16.87 PostTrainBench points, respectively. RSI-Dojo-35B-A3B reaches 29.95 on PostTrainBench and 53.29 on PostTrainBench-Lite, matching the performance of frontier models such as GLM-5.2 and GPT 5.5.

---

## 3. Say the Same, Act Differently: Diagnosing and Steering Text-Action Divergence in Reasoning VLAs

**Authors:** Zihao Feng, Qingzhao Zhang, Chunyu Xia, ..., Z. Morley Mao, Ramesh Govindan
**arXiv:** [2611.04166](https://arxiv.org/abs/2611.04166)
**Categories:** Machine Learning (cs.LG); Cryptography and Security (cs.CR); Computer Vision and Pattern Recognition (cs.CV); Robotics (cs.RO)

Reasoning vision-language-action (VLA) models pair physical control with natural-language rationales that supervisors can read to monitor embodied safety. Prior attacks on VLA reasoning corrupt the rationale itself and leave visible evidence in the text. We show that visual perturbations can instead alter the physical action while keeping the generated rationale word-for-word identical. At the shared text/action interface of Alpamayo for driving and InstructVLA for manipulation, our text-neutral action-subspace (TNAS) diagnostic shows that the locally most action-sensitive direction is nearly orthogonal to the active text-loss gradients, with 1.87% and 5.28% norm overlap. At equal hidden-state perturbation norms across both models, interventions along this text-neutral residual shift actions 4.64x to 47.8x more than text-gradient perturbations, whereas text-gradient perturbations induce 21.2x to 277x more text drift. Steering visual perturbations along this direction reaches the same decoupling from the image. Across 154 obstacle-annotated driving scenes in Alpamayo, TNAS-guided attacks induce a new collision under a word-for-word identical rationale in 52.6% of scenes under full-image perturbations and 35.1% under a localized forward-camera patch, compared with 4.55% for unguided action attacks. Relative to a text-preserving baseline, TNAS guidance raises exact rationale preservation from 83.0% to 89.5% and cuts teacher-forced text drift by 68.4% at a comparable collision rate. In InstructVLA, TNAS guidance cuts text drift by 40.5% and preserves the exact response on 85.0% of examples alongside a 1.73-unit action-chunk shift. An unchanged rationale therefore cannot certify a safe action, so monitors for reasoning VLAs must verify the predicted action channel directly.

---

## 4. Should the Action Expert Train the VLM? Action-Token Supervision and Gradient Routing in Mixture-of-Transformer VLAs

**Authors:** Asher James Hancock, Boyi Li, Yuxiao Chen, ..., Boris Ivanovic, Marco Pavone
**arXiv:** [2611.05249](https://arxiv.org/abs/2611.05249)
**Categories:** Robotics (cs.RO)

Vision-language-action (VLA) models increasingly pair a pre-trained vision-language model (VLM) with a flow-matching expert that conditions its action predictions on the VLM's key-value representations. Those representations must carry information useful for control, yet the VLM was never trained for the action expert's flow-matching objective. Two signals can address this: gradients backpropagated from the expert's loss (coupling), or VLM supervision to predict discrete tokens encoding the same target actions. Prominent training recipes forgo the first, blocking expert-to-VLM gradients (insulation) to protect the VLM's existing capabilities, while also supervising it on vision-language data and action tokens. Because vision-language co-training also aims to preserve those capabilities, the additional protection provided by insulation is unclear. At the same time, insulation removes a direct signal about which features continuous action prediction requires. On the other hand, action-token supervision offers an alternative way to learn action-relevant representations, which may explain why insulation succeeds in practice. We disentangle these factors in autonomous driving and manipulation by independently varying action-token supervision and whether the expert's loss updates the VLM. In open-loop driving, insulation is competitive with coupling when action tokens are supervised; without them, coupling reduces trajectory-prediction error by roughly 25%. When both components are trained jointly from the outset, coupling increases closed-loop driving route progress by approximately 17% with action-token supervision and 40% without it, and similarly improves robot manipulation performance under both settings. These findings show that the value of gradient insulation depends on the VLM's action supervision and the evaluation setting, challenging insulation as a default VLA training recipe.

---

## 5. LoopQ: Fair, Closed-Loop Evaluation of Quantized Vision-Language-Action Models

**Authors:** Syed Umer Bukhari, Magnus Almgren, Ahmed Ali-Eldin
**arXiv:** [2611.05093](https://arxiv.org/abs/2611.05093)
**Categories:** Robotics (cs.RO)

Post-training quantization (PTQ) for vision-language-action (VLA) models promises smaller and faster VLA deployments. However, when analyzing existing VLA quantization works, we realised that it is hard to reason about the performance of the suggested quantization method compared to existing, similar, or in many cases, simpler PTQ methods. We present LoopQ, a closed-loop benchmark that compares multiple quantization policies on the same checkpoint, layers and engine, varying only the method and the kernels. We evaluate RTN, AWQ, GPTQ, ActQuant and QuantVLA on four VLAs with more than 180,000 episodes of LIBERO and LIBERO-plus, compare against QVLA's reported results on the same layers, and benchmark whether the four public VLA-quantization releases can be reproduced. We benchmark the methods on an NVIDIA H100, an L4, and a Jetson AGX Thor. Our results show that while quantization reliably saves memory, 2-3x for real low-bit models, VLA-specific PTQ methods underperform compared to simpler generic baselines. At 4 bits, RTN, AWQ and GPTQ match or exceed ActQuant and QuantVLA, plain RTN matches the calibrated methods, and plain AWQ matches the success QVLA reports for itself. Standard LIBERO hides the losses that do exist: configurations with no significant LIBERO loss lose 1.5-4.3 points under paired LIBERO-plus perturbations. Speed is a weaker story. At batch 1 on the H100, no quantized pi0.5 or OpenVLA-OFT configuration is faster than its 16-bit model (1.06-1.58x slower on library kernels); only the L4 with int8 kernels gains (4-14%), the Thor is slower on every 4-bit configuration, and the engine alone changes latency by 2.1x. Profiling explains why: pi0.5's quantized backbone is compute-bound, while its memory-bound action expert, 63% of GPU time and 13% of the parameters, stays in 16 bits.

---

## 6. Trusting Imagined Futures: Auditing Imagined Rewards for VLA Post-Training

**Authors:** Zicheng Kong, Zhenbo Xu, Haoyan Zhang, ..., Min Ren, Zhaofeng He
**arXiv:** [2611.04873](https://arxiv.org/abs/2611.04873)
**Categories:** Robotics (cs.RO); Computer Vision and Pattern Recognition (cs.CV)

Video world models enable candidate actions to be evaluated through imagined outcomes, but high predicted rewards can favor trajectories with poor execution quality. We introduce Trusting Imagined Futures (TIF), an offline supervision selection method for vision-language-action (VLA) post-training that audits predicted rewards using execution feedback. A multidimensional reward model predicts a utility score for candidate ranking and five dimensions of execution quality. An auditor uses reward predictions and uncertainty to identify overestimation patterns learned from paired imagined videos and real executions. TIF accepts the candidate with the highest predicted utility when its advantage over the existing trajectory exceeds a margin and its audit risk passes a threshold; otherwise, it retains the existing supervision. The retained real trajectories then supervise behavior cloning. Across four LIBERO suites and three training seeds, TIF achieves a mean success rate of 76.25%, improving over training on the existing trajectories by 3.00 percentage points with the same trajectory count and training budget. Adding audit gating yields 1.47 percentage points with the reward model and advantage margin held fixed. The gains persist against advantage ranking and logistic regression risk selection at matched replacement counts. On recorded videos from three real robot tasks, TIF increases clean completion among selected trajectories from 58.33% to 70.00% across 60 candidate pools.

---

## 7. RAFT: Reasoning-Aligned Fine-Tuning Improves Robustness of VLA Post-Training

**Authors:** Shresth Grover, Andrey Kolobov, Dhruv Shah
**arXiv:** [2611.04368](https://arxiv.org/abs/2611.04368)
**Categories:** Robotics (cs.RO); Computer Vision and Pattern Recognition (cs.CV)

Adapting a generalist vision-language-action (VLA) policy to a target task with limited demonstrations can improve nominal task success while reducing robustness to variations in appearance, objects, and instructions. We introduce reasoning-aligned fine-tuning (RAFT), a two-stage post-training procedure: RAFT first trains low-rank adapters on task-relevant reasoning annotations, then freezes them while fine-tuning the policy on action demonstrations. On a physical DROID robot, RAFT achieves $75.0\%$ out-of-distribution success, compared with $27.9\%$ for plain fine-tuning; on a multi-stage bimanual YAM task, it reaches $70.0\%$ mean success, compared with $36.0\%$ for the strongest baseline. RAFT also improves success under visual, object, and instruction shifts in simulated pick-and-place and open-drawer tasks. Compared with plain fine-tuning, RAFT policies place more attention on annotated task regions and yield higher linear-probe accuracy for object identity in later layers. A broader reasoning-data mixture further improves downstream success across demonstration budgets.

---
