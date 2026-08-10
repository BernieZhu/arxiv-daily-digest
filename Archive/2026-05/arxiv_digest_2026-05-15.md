# arXiv Daily Digest — 2026-05-15

**Mode:** direct
**Categories:** cs.AI, cs.LG, cs.RO, cs.CV
**Keywords:** VLA, world model, world action model
**Papers found:** 9

---

## 1. Agentifying Patient Dynamics within LLMs through Interacting with Clinical World Model

**Authors:** Minghao Wu, Yuting Yan, Zhenyang Cai, ..., Benyou Wang, Hongyuan Zha
**arXiv:** [2605.14723](https://arxiv.org/abs/2605.14723)
**Categories:** Artificial Intelligence (cs.AI); Computation and Language (cs.CL); Machine Learning (cs.LG)

Sepsis management in the ICU requires sequential treatment decisions under rapidly evolving patient physiology. Although large language models (LLMs) encode broad clinical knowledge and can reason over guidelines, they are not inherently grounded in action-conditioned patient dynamics. We introduce SepsisAgent, a world model-augmented LLM agent for sepsis treatment recommendation. SepsisAgent uses a learned Clinical World Model to simulate patient responses under candidate fluid--vasopressor interventions, and follows a propose--simulate--refine workflow before committing to a prescription. We first show that world-model access alone yields inconsistent LLM decision performance, motivating agent-specific training. We then train SepsisAgent through a three-stage curriculum: patient-dynamics supervised fine-tuning, propose--simulate--refine behavior cloning, and world-model-based agentic reinforcement learning. On MIMIC-IV sepsis trajectories, SepsisAgent outperforms all traditional RL and LLM-based baselines in off-policy value while achieving the best safety profile under guideline adherence and unsafe-action metrics. Further analysis shows that repeated interaction with the Clinical World Model enables the agent to learn regularities in patient evolution, which remain useful even when simulator access is removed.

---

## 2. Quantitative Video World Model Evaluation for Geometric-Consistency

**Authors:** Jiaxin Wu, Yihao Pi, Yinling Zhang, Yuheng Li, Xueyan Zou
**arXiv:** [2605.15185](https://arxiv.org/abs/2605.15185)
**Categories:** Computer Vision and Pattern Recognition (cs.CV); Artificial Intelligence (cs.AI)

Generative video models are increasingly studied as implicit world models, yet evaluating whether they produce physically plausible 3D structure and motion remains challenging. Most existing video evaluation pipelines rely heavily on human judgment or learned graders, which can be subjective and weakly diagnostic for geometric failures. We introduce PDI-Bench (Perspective Distortion Index), a quantitative framework for auditing geometric coherence in generated videos. Given a generated clip, we obtain object-centric observations via segmentation and point tracking (e.g., SAM 2, MegaSaM, and CoTracker3), lift them to 3D world-space coordinates via monocular reconstruction, and compute a set of projective-geometry residuals capturing three failure dimensions: scale-depth alignment, 3D motion consistency, and 3D structural rigidity. To support systematic evaluation, we build PDI-Dataset, covering diverse scenarios designed to stress these geometric constraints. Across state-of-the-art video generators, PDI reveals consistent geometry-specific failure modes that are not captured by common perceptual metrics, and provides a diagnostic signal for progress toward physically grounded video generation and physical world model. Our code and dataset can be found at this https URL.

---

## 3. IntentVLA: Short-Horizon Intent Modeling for Aliased Robot Manipulation

**Authors:** Shijie Lian, Bin Yu, Xiaopeng Lin, ..., Cong Huang, Kai Chen
**arXiv:** [2605.14712](https://arxiv.org/abs/2605.14712)
**Categories:** Robotics (cs.RO); Artificial Intelligence (cs.AI); Computation and Language (cs.CL); Computer Vision and Pattern Recognition (cs.CV)

Robot imitation data are often multimodal: similar visual-language observations may be followed by different action chunks because human demonstrators act with different short-horizon intents, task phases, or recent context. Existing frame-conditioned VLA policies infer each chunk from the current observation and instruction alone, so under partial observability they may resample different intents across adjacent replanning steps, leading to inter-chunk conflict and unstable execution. We introduce IntentVLA, a history-conditioned VLA framework that encodes recent visual observations into a compact short-horizon intent representation and uses it to condition chunk generation. We further introduce AliasBench, a 12-task ambiguity-aware benchmark on RoboTwin2 with matched training data and evaluation environments that isolate short-horizon observation aliasing. Across AliasBench, SimplerEnv, LIBERO, and RoboCasa, IntentVLA improves rollout stability and outperforms strong VLA baselines

---

## 4. Hand-in-the-Loop: Improving Dexterous VLA via Seamless Interventional Correction

**Authors:** Zhuohang Li, Liqun Huang, Wei Xu, ..., Xinjun Sheng, Ruoshi Wen
**arXiv:** [2605.15157](https://arxiv.org/abs/2605.15157)
**Categories:** Robotics (cs.RO); Machine Learning (cs.LG)

Vision-Language-Action (VLA) models are prone to compounding errors in dexterous manipulation, where high-dimensional action spaces and contact-rich dynamics amplify small policy deviations over long horizons. While Interactive Imitation Learning (IIL) can refine policies through human takeover data, applying it to high-degree-of-freedom (DoF) robotic hands remains challenging due to a command mismatch between human teleoperation and policy execution at the takeover moment, which causes abrupt robot-hand configuration changes, or "gesture jumps". We present Hand-in-the-Loop (HandITL), a seamless human-in-the-loop intervention method that blends human corrective intent with autonomous policy execution to avoid gesture jumps during bimanual dexterous manipulation. Compared with direct teleoperation takeover, HandITL reduces takeover jitter by 99.8% and preserves robust post-takeover manipulation, reducing grasp failures by 87.5% and mean completion time by 19.1%. We validate HandITL on tasks requiring bimanual coordination, tool use, and fine-grained long-horizon manipulation. When used to collect intervention data for policy refinement, HandITL yields policies that outperform those trained with standard teleoperation data by 19% on average across three long-horizon dexterous tasks.

---

## 5. Evo-Depth: A Lightweight Depth-Enhanced Vision-Language-Action Model

**Authors:** Tao Lin, Yuxin Du, Jiting Liu, ..., Gen Li, Bo Zhao
**arXiv:** [2605.14950](https://arxiv.org/abs/2605.14950)
**Categories:** Computer Vision and Pattern Recognition (cs.CV); Robotics (cs.RO)

Vision-Language-Action models have emerged as a promising paradigm for robotic manipulation by unifying perception, language grounding, and action generation. However, they often struggle in scenarios requiring precise spatial understanding, as current VLA models primarily rely on 2D visual representations that lack depth information and detailed spatial relationships. While recent approaches incorporate explicit 3D inputs such as depth maps or point clouds to address this issue, they often increase system complexity, require additional sensors, and remain vulnerable to sensing noise and reconstruction errors. Another line of work explores implicit 3D-aware spatial modeling directly from RGB observations without extra sensors, but it often relies on large geometry foundation models, resulting in higher training and deployment costs. To address these challenges, we propose Evo-Depth, a lightweight depth-enhanced VLA framework that enhances spatially grounded manipulation without relying on additional sensing hardware or compromising deployment efficiency. Evo-Depth employs a lightweight Implicit Depth Encoding Module to extract compact depth features from multi-view RGB images. These features are incorporated into vision-language representations through a Spatial Enhancement Module via depth-aware modulation, enabling efficient spatial-semantic enhancement. A Progressive Alignment Training strategy is further introduced to align the resulting depth-enhanced representations with downstream action learning. With only 0.9B parameters, Evo-Depth achieves superior performance across four simulation benchmarks. In real-world experiments, Evo-Depth attains the highest average success rate while also exhibiting the smallest model size, lowest GPU memory usage, and highest inference frequency among compared methods.

---

## 6. SANA-WM: Efficient Minute-Scale World Modeling with Hybrid Linear Diffusion Transformer

**Authors:** Haoyi Zhu, Haozhe Liu, Yuyang Zhao, ..., Song Han, Enze Xie
**arXiv:** [2605.15178](https://arxiv.org/abs/2605.15178)
**Categories:** Computer Vision and Pattern Recognition (cs.CV)

We introduce SANA-WM, an efficient 2.6B-parameter open-source world model natively trained for one-minute generation, synthesizing high-fidelity, 720p, minute-scale videos with precise camera control. SANA-WM achieves visual quality comparable to large-scale industrial baselines such as LingBot-World and HY-WorldPlay, while significantly improving efficiency. Four core designs drive our architecture: (1) Hybrid Linear Attention combines frame-wise Gated DeltaNet (GDN) with softmax attention for memory-efficient long-context modeling. (2) Dual-Branch Camera Control ensures precise 6-DoF trajectory adherence. (3) Two-Stage Generation Pipeline applies a long-video refiner to stage-1 outputs, improving quality and consistency across sequences. (4) Robust Annotation Pipeline extracts accurate metric-scale 6-DoF camera poses from public videos to yield high-quality, spatiotemporally consistent action labels. Driven by these designs, SANA-WMdemonstrates remarkable efficiency across data, training compute, and inference hardware: it uses only $\sim$213K public video clips with metric-scale pose supervision, completes training in 15 days on 64 H100s, and generates each 60s clip on a single GPU; its distilled variant can be deployed on a single RTX 5090 with NVFP4 quantization to denoise a 60s 720p clip in 34s. On our one-minute world-model benchmark, SANA-WM demonstrates stronger action-following accuracy than prior open-source baselines and achieves comparable visual quality at $36\times$ higher throughput for scalable world modeling.

---

## 7. EponaV2: Driving World Model with Comprehensive Future Reasoning

**Authors:** Jiawei Xu, Zhizhou Zhong, Zhijian Shu, ..., Jian Yang, Wei Yin
**arXiv:** [2605.14696](https://arxiv.org/abs/2605.14696)
**Categories:** Computer Vision and Pattern Recognition (cs.CV)

Data scaling plays a pivotal role in the pursuit of general intelligence. However, the prevailing perception-planning paradigm in autonomous driving relies heavily on expensive manual annotations to supervise trajectory planning, which severely limits its scalability. Conversely, although existing perception-free driving world models achieve impressive driving performance, their real-world reasoning ability for planning is solely built on next frame image forecasting. Due to the lack of enough supervision, these models often struggle with comprehensive scene understanding, resulting in unsatisfactory trajectory planning. In this paper, we propose EponaV2, a novel paradigm of driving world models, which achieves high-quality planning with comprehensive future reasoning. Inspired by how human drivers anticipate 3D geometry and semantics, we train our model to forecast more comprehensive future representations, which can be additionally decoded to future geometry and semantic maps. Extracting the 3D and semantic modalities enables our model to deeply understand the surrounding environment, and the future prediction task significantly enhances the real-world reasoning capabilities of EponaV2, ultimately leading to improved trajectory planning. Moreover, inspired by the training recipe of Large Language Models (LLMs), we introduce a flow matching group relative policy optimization mechanism to further improve planning accuracy. The state-of-the-art (SOTA) performances of EponaV2 among perception-free models on three NAVSIM benchmarks (+1.3PDMS, +5.5EPDMS) demonstrate the effectiveness of our methods.

---

## 8. Coding Agent Is Good As World Simulator

**Authors:** Hongyu Wang, Jingquan Wang, Bocheng Zou, Radu Serban, Dan Negrut
**arXiv:** [2605.14398](https://arxiv.org/abs/2605.14398)
**Categories:** Artificial Intelligence (cs.AI)

World models have emerged as a powerful paradigm for building interactive simulation environments, with recent video-based approaches demonstrating impressive progress in generating visually plausible dynamics. However, because these models typically infer dynamics from video and represent them in latent states, they do not explicitly enforce physical constraints. As a result, the generated video rollouts are not physically plausible, exhibiting unstable contacts, distorted shapes, or inconsistent motion. In this paper, we present an agentic framework constructing physics-based world models through executable simulation code. The framework coordinates planning, code generation, visual review, and physics analysis agents. The planning agent converts the natural language prompt into a structured scene plan, the code agent implements it as executable simulation code, and the visual review agent provide visual feedback while the physics analysis agent checks physical consistency. The code is iteratively revised based on the feedback until the simulation matches the prompt reqirements and physical constraints. Experimental results show that our framework outperforms advanced video-based models in physical accuracy, instruction fidelity and visual quality, which could be applied to various scenarios including driving simulation and embodied robot tasks.

---

## 9. Slot-MPC: Goal-Conditioned Model Predictive Control with Object-Centric Representations

**Authors:** Jonathan Spieler, Angel Villar-Corrales, Sven Behnke
**arXiv:** [2605.14937](https://arxiv.org/abs/2605.14937)
**Categories:** Machine Learning (cs.LG); Artificial Intelligence (cs.AI); Robotics (cs.RO)

Predictive world models enable agents to model scene dynamics and reason about the consequences of their actions. Inspired by human perception, object-centric world models capture scene dynamics using object-level representations, which can be used for downstream applications such as action planning. However, most object-centric world models and reinforcement learning (RL) approaches learn reactive policies that are fixed at inference time, limiting generalization to novel situations. We propose Slot-MPC, an object-centric world modeling framework that enables planning through Model Predictive Control (MPC). Slot-MPC leverages vision encoders to learn slot-based representations, which encode individual objects in the scene, and uses these structured representations to learn an action-conditioned object-centric dynamics model. At inference time, the learned dynamics model enables action planning via MPC, allowing agents to adapt to previously unseen situations. Since the learned world model is differentiable, we can use gradient-based MPC to directly optimize actions, which is computationally more efficient than relying on gradient-free, sampling-based MPC methods. Experiments on simulated robotic manipulation tasks show that Slot-MPC improves both task performance and planning efficiency compared to non-object-centric world model baselines. In the considered offline setting with limited state-action coverage, we find that gradient-based MPC performs better than gradient-free, sampling-based MPC. Our results demonstrate that explicitly structured, object-centric representations provide a strong inductive bias for controllable and generalizable decision-making. Code and additional results are available at this https URL.

---
