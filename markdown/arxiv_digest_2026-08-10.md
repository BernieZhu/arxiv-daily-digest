# arXiv Daily Digest — 2026-08-10

**Mode:** direct
**Categories:** cs.AI, cs.LG, cs.RO, cs.CV
**Keywords:** VLA, world model, world action model
**Papers found:** 19

---

## 1. MemWM: Memory-Augmented Text-Based World Model

**Authors:** Yujun Wang, Tao Zhang, Jinhe Bi, ..., Hinrich Schütze, Yunpu Ma
**arXiv:** [2608.07107](https://arxiv.org/abs/2608.07107)
**Categories:** Artificial Intelligence (cs.AI)

World models are increasingly used to support planning in agents by predicting how environment states evolve in response to agent actions. Yet fluent next-state predictions can still omit task-critical facts, corrupt product attributes, or apply incorrect transition rules. To address such systematic prediction errors, we introduce MemWM, a memory-augmented text-based world model. MemWM uses world memory, a curated memory bank of transition rules, state caches, and hard-to-predict facts, to condition next-state imagination. We evaluate factual state preservation with Structured State Fidelity (SSF), which scores predicted states through benchmark-specific facts and fields. Compared with SFT, memory-augmented training improves SSF by up to 206.3%. In the full planning setting, we keep the policy model frozen and provide policy-side world skill: retrieved task-level skills and step-wise corrective guidance for action selection. Across ALFWorld, WebShop, and ScienceWorld, memory-augmented agents improve downstream success over an SFT-trained world-model agent, with up to a 65.4% relative gain. Sensitivity analyses further show that retrieved memory improves task success and efficiency under different memory and action-budget settings.

---

## 2. Transformers Struggle to Use Their Emergent World Models: Revisiting the Tower of Hanoi, and the Illusion of Thinking

**Authors:** Devin Pereira, Willem Zuidema
**arXiv:** [2608.07077](https://arxiv.org/abs/2608.07077)
**Categories:** Artificial Intelligence (cs.AI); Machine Learning (cs.LG)

The Tower of Hanoi is a simple planning puzzle that in prior work has proven challenging for large reasoning models (LRMs). Current models solve the standard formulation of the puzzle, but still struggle with the flat-to-flat variant (where initial and goal states are not restricted to have all rings on a single peg). This paper presents an in-depth study of how both small, in-house Transformers and large, third-party LRMs solve this task. To understand the failures mechanistically, we first train small Transformers from scratch on precomputed solution traces. Using a variety of interpretability techniques, we show that these Transformers develop an emergent world model: a linearly decodable, geometrically faithful representation of the puzzle's state space (the Sierpinski triangle), that is causally involved in solving the puzzles. Second, we return to the large LLMs and apply our techniques to two frontier reasoning models, Qwen3.6-27B and DeepSeek-R1-Distill-Qwen-32B, that attempt to solve the task through extended chain-of-thought. Surprisingly, we find that both models encode the Sierpinski world model near-perfectly at the end of the prompt, and yet fail at the majority of tasks when there are more than 3 rings. We locate the source of this failure in the decaying representation of the world model. We probe for the representation at different stages during planning, and establish causality by showing that performance can be improved by injecting the prompt-time representation at inference. The failure of the models is thus one of maintenance of the required representations, not their absence, and performance is at least partially recoverable. These results thus reframe the reported collapse in performance from prior work: current Large Reasoning Models build a world model, and then lose it.

---

## 3. Surg-UniWorld: A Unified Surgical World Model with Multimodal Control Experts

**Authors:** Rulin Zhou, Wanhao Liu, Guoheng Ma, ..., Luping Zhou, Hongliang Ren
**arXiv:** [2608.06770](https://arxiv.org/abs/2608.06770)
**Categories:** Artificial Intelligence (cs.AI); Computer Vision and Pattern Recognition (cs.CV)

Controllable surgical world models can provide a generative foundation for surgical artificial intelligence and simulation by synthesizing realistic instrument--tissue interactions. However, existing methods lack a unified multimodal control paradigm, while direct fusion of heterogeneous visual conditions often causes anatomical distortion, instrument appearance drift, and temporally inconsistent interactions. In this work, we propose {Surg-UniWorld}, a unified surgical world model with multimodal control experts. Surg-UniWorld first constructs a {Hierarchical Surgical Anchor} from first-frame appearance and hierarchical semantic masks to preserve persistent scene identity, anatomical organization, and interaction boundaries. {Anchor-Relative Modality Experts} then interpret edge, depth, and optical-flow evidence relative to the shared anchor, capturing complementary boundary, geometric, and motion information. A {Multimodal Control Expert} further performs contribution-preserving stage-wise composition of the activated modality increments and generates control hints for the Wan2.2 video diffusion backbone. To support multimodal surgical world modeling, we further construct Cholec80-SurgWAM, a benchmark for controllable surgical video generation. Extensive experiments demonstrate that Surg-UniWorld consistently outperforms existing controllable video generation methods and surgical world-model baselines in generation quality, temporal consistency, and multimodal controllability.

---

## 4. TaskSense: Focusing on What Matters in World Models

**Authors:** SM Mazharul Islam, Manfred Huber
**arXiv:** [2608.06544](https://arxiv.org/abs/2608.06544)
**Categories:** Artificial Intelligence (cs.AI); Computer Vision and Pattern Recognition (cs.CV); Machine Learning (cs.LG)

World models for visual control typically learn compact latent states by reconstructing observations, implicitly encouraging representations to preserve information across the entire visual input. However, task-relevant content often occupies only a small fraction of the observation, while background clutter and distractors consume valuable representational capacity. This mismatch between visual reconstruction and control objectives biases latent representations to model task-irrelevant visual content, diluting learning signals for control-relevant features and severely degrading downstream performance under visual distractions. We introduce TaskSense, a task-centric world modeling framework that enforces task relevance before latent encoding through a differentiable stochastic spatial attention mechanism conditioned on the previous latent state. To steer attention toward control-relevant regions, we augment training with an auxiliary inverse-dynamics objective. Rather than reconstructing the full observation, the world model reconstructs only the attended regions, encouraging latent representations to preserve task-relevant information while discarding irrelevant visual content. The decoder is further conditioned on the sampled attention map, enabling consistent reconstruction despite stochastic attention. Compared with the DreamerV3 baseline, TaskSense maintains competitive performance on the DeepMind Control Suite while consistently outperforming DreamerV3 on the Distracting Control Suite, demonstrating substantially improved robustness to visual distractions. Qualitative analysis further confirms that the learned attention, guided by inverse-dynamics supervision, consistently localizes control-relevant regions while suppressing irrelevant visual content.

---

## 5. Decoupling Intention from Trajectory: A Representational Deduction Framework for World Action Models

**Authors:** Xiangkai Ma, Yue Ma, Junjie Wang, ..., Wenzhong Li, Zhihao Yuan
**arXiv:** [2608.06994](https://arxiv.org/abs/2608.06994)
**Categories:** Robotics (cs.RO); Artificial Intelligence (cs.AI)

World Action Models (WAMs) aim to construct a unified architecture capable of understanding world state evolution and guiding to generative motion planning. However, existing visual branches focus on predicting static visual observation, rather than reflecting potential transition information that captures the evolution of world states under motion interactions. This leads to representational entanglement between high-level physical condition evolution and low-level action trajectory generation within the Action Model, creating a structural bottleneck while weakening the predictive capability of world evolution modeling for action generation. We propose PILOT (Physical Inference for Latent Optimized Trajectories), whose core Representational Deduction (RD) bridges this gap by integrating motion thought-of-chain (CoT) guidance as a native model capability. Specifically, RD aims to encourage the action branch to explicitly model potential state transition tokens, which are retained as CoT in the reasoning space to guide fine-grained motion trajectory. Experiments demonstrate that RD not only significantly improves the success rate and generalization ability of WAMs in complex robotic manipulation tasks but also enhances the model's physical interpretability by decoupling high-level motion semantics from low-level trajectory details. Furthermore, the abundant state transition supervision signals introduced by RD effectively alleviate the sparse supervision in action generation, enabling it to serve as an efficient few-shot real-robot fine-tuning strategy and demonstrating superior scalability for migration to mainstream WAM architectures.

---

## 6. Dueling World Models: Advantage-Style Action Channels for Common-Mode Distractor Rejection

**Authors:** Jiazhuo Li, Yiming Fei, Zhiruo Zhou, Heikichi Hayashi
**arXiv:** [2608.06706](https://arxiv.org/abs/2608.06706)
**Categories:** Machine Learning (cs.LG); Artificial Intelligence (cs.AI)

Latent world models plan by predicting future states from an action, but when a scene contains motion the agent does not control, they quietly go action-blind: predictions for different actions become indistinguishable even as the training loss keeps improving. Existing remedies suppress this distraction with reconstruction, task reward, or auxiliary objectives, each adding machinery or assumptions. We show that a minimal alternative suffices, borrowed from the dueling decomposition of value into a state baseline and an action advantage: in latent dynamics, subtracting a prediction's mean effect over actions cancels whatever the actions share--the action-independent variation where distractors live--leaving a clean, controllable channel, with no reward, no reconstruction, and no distractor-specific auxiliary loss. Because this is only a subtraction at readout time, it applies unchanged to any action-conditioned world model, including frozen pretrained ones. Across a gridworld, synthetic generators with known factors, distracting continuous control, and natural-pixel Atari, the isolated channel recovers the agent's own effect where entangled predictors fail, with nuisance leak indistinguishable from zero; applied post hoc it surfaces an action channel in off-the-shelf models that their raw readouts miss, and it converts into goal-reaching control in the gridworld. We prove the cancellation is exact in finite samples for both discrete and sampled action sets, and we state its measured boundary--distractors whose motion tracks the action--together with the remaining limitations in the appendix.

---

## 7. Beyond Myopic World Models: Long-Horizon End-to-End Training for Direct Future Prediction

**Authors:** Xinyi Li, Zaishuo Xia, Chenjie Hao, Yubei Chen
**arXiv:** [2608.07420](https://arxiv.org/abs/2608.07420)
**Categories:** Machine Learning (cs.LG)

World models are expected to support imagination over extended temporal horizons, yet most are still trained through local few-step prediction objectives and deployed by recursively rolling out their own predictions. This creates a fundamental mismatch: few-step losses optimize local transition fidelity, while long-horizon prediction depends on how errors and gradients propagate through the entire trajectory. As a result, transitions with different downstream influence on the endpoint are treated uniformly during training, and small local errors are amplified through recursive inference. We argue that long-horizon accuracy is better achieved by optimizing directly, through an end-to-end endpoint prediction objective. To instantiate this paradigm, we introduce the Direct Prediction World Model (DPWM), a non-recursive architecture that compresses an action sequence of arbitrary length into a single embedding and predicts the endpoint observation in a single forward pass. This design avoids recurrent rollout in both prediction and gradient propagation, making long-horizon end-to-end training practical at horizons where unrolled autoregressive training becomes unstable. Empirically, DPWM substantially improves long-horizon endpoint prediction over recursive world-model baselines on continuous-control and pixel-based benchmarks, with larger gains as the prediction horizon increases. We further show that recurrent baselines benefit similarly when retrained with the same long-horizon endpoint objective, supporting our central claim that the training objective, rather than the particular backbone choice, is the main driver of long-horizon prediction accuracy. Our results suggest that world models can benefit from being trained and evaluated at the temporal scales where they are ultimately used, shifting the focus from local transition modeling toward long-horizon predictive accuracy.

---

## 8. From Optimal Actions to World Models: Identifiability of Transition Kernels in Discounted MDPs

**Authors:** Neal Batra
**arXiv:** [2608.07301](https://arxiv.org/abs/2608.07301)
**Categories:** Machine Learning (cs.LG)

We study what can be recovered about the transition probabilities of a Markov decision process from optimal actions alone. This is closely related to the inverse problem considered by Letcher et al., who ask when the dynamics can be recovered from numerical \(Q\)-values. Here the numerical values themselves are not observed; only the optimal actions are known, for every reward in a given class.
For state-action rewards \(r(s,a)\), knowing the optimal actions for every reward also tells us how much better one action is than another when each is followed by the same fixed policy. This is still not enough to determine the transition probabilities uniquely. We prove that two kernels give the same optimal actions for every reward exactly when \[ Q_{s,a} =
\Bigl(P_{s,a}+\tfrac1\gamma e_s^{\mathsf T}(L-I)\Bigr)L^{-1} \] for one invertible matrix \(L\) satisfying \(L\mathbf 1=\mathbf 1\). Near a kernel with strictly positive entries, there is an \(n(n-1)\)-dimensional family of different kernels with this property. The result is unchanged if we consider only rewards having a unique optimal action at every state.
We then compare this with rewards of the forms \(r(s)\) and \(r(s,a,s')\). Rewards that depend on the next state can usually recover the transition kernel itself: every row at a state with at least two actions is determined, and we describe exactly when a row at a state with one action can remain hidden. State rewards reveal less: two kernels give the same optimal actions exactly when every deterministic policy is optimal for the same set of rewards. The results show how the form of the reward affects what can be learned about the dynamics from optimal actions alone.

---

## 9. Addressable Memory for Video World Models

**Authors:** Xindi Wu, Sven Elflein, James Lucas, ..., Jonathan Lorraine, Aljoša Ošep
**arXiv:** [2608.07408](https://arxiv.org/abs/2608.07408)
**Categories:** Computer Vision and Pattern Recognition (cs.CV); Machine Learning (cs.LG)

We study visual persistence in interactive video world models. These models rely on a Key-Value (KV) cache as a growing visual memory to carry forward previously generated frames. However, we find that models can no longer reliably address stored content once rollouts extend beyond the training horizon, because temporal Rotary Positional Embeddings (RoPE) offsets then fall outside the range seen during training and the model struggles to retrieve the relevant visual information through attention. Moreover, naively compressing the cache in the RoPE-rotated space corrupts memory by averaging together incompatible positional phases. To address this, we propose WorldTrace, a training-free memory framework for long-horizon visual persistence. WorldTrace keeps compressed memory addressable by assigning each summary slot a distinct, in-distribution virtual position. Within this addressable cache, we study two memory compression approaches: WorldTrace-Field compresses history for temporal coherence, while WorldTrace-Landmark stores verbatim scene traces at detected transitions for episodic recall. We further introduce LoopBench, a benchmark evaluating whether a compressed cache can reconstruct a previously visited scene after a long detour. WorldTrace-Field improves temporal consistency by +15.5%, and WorldTrace-Landmark improves episodic recall by +19.5% on LoopBench, extending visually persistent generation without retraining.

---

## 10. Fast and Accurate: An Adaptive VLA Inference Framework through Environment-aware Model Selection

**Authors:** Yuewei Sun, Lang Qin, Zechuan Tian, ..., Qinghai Guo, Yuxin Ma
**arXiv:** [2608.06434](https://arxiv.org/abs/2608.06434)
**Categories:** Robotics (cs.RO); Machine Learning (cs.LG)

Embodied intelligence demands both long-horizon reasoning and real-time closed-loop responsiveness. Recent dual-system Vision-Language-Action (VLA) architectures combine fast reactive control with slow deliberative reasoning to balance inference speed and task success rate. However, existing dual-process VLAs tightly couple the fast module to intermediate representations of the slow module, necessitating end-to-end joint training and limiting modularity, extensibility and flexible system switching. In this paper, we propose Environment-aware Model Selection (EMS), an adaptive VLA inference framework that switches between two fully decoupled systems of different scales through environment-aware model selection. The large-scale deliberative system provides globally consistent trajectory planning to ensure task success, while a lightweight reactive system enables high-frequency closed-loop control. A reinforcement-learning-based switching policy dynamically selects which system to invoke based on real-time feedback, enabling sparse use of the slow system and thereby balancing pretrained knowledge utilisation with runtime efficiency. Our design offers three key advantages over prior hierarchical VLA frameworks: (1) a fully decoupled and modular dual-system architecture that supports plug-and-play model replacement; (2) an adaptive, environment-aware switching strategy; (3) high-frequency inference for responsive closed-loop control. We extensively evaluate EMS in both simulation and real-world environments. On the LIBERO benchmark, EMS achieves success rates comparable to the large-scale baseline while increasing the effective action frequency to 93.4 Hz. The framework further demonstrates strong extensibility in real-world dual-arm manipulation tasks, where it accelerates task completion while maintaining robust performance.

---

## 11. Depth-Wise Probing and Pruning of the Planning Token in a Driving Vision-Language-Action Model

**Authors:** Harisankar Babu, Benjamin Coors, Christopher Lang, ..., Tamim Asfour, Simon Foell
**arXiv:** [2608.07361](https://arxiv.org/abs/2608.07361)
**Categories:** Robotics (cs.RO); Computer Vision and Pattern Recognition (cs.CV)

Vision-language-action (VLA) models route driving decisions through a deep language model, but it is unclear how much of that depth the action itself requires. We study a representative driving VLA whose entire plan is carried by a single planning token that a generative planner decodes into a trajectory. Borrowing the planner as a trajectory-space logit lens, we decode the planning token from every one of the 32 decoder layers and measure two signals: the linear decodability of the navigation command and trajectory compatibility with the frozen native planner. Our diagnostic shows that semantic intent is linearly decodable early: command-probe accuracy reaches 97.7\% after the first decoder layer, compared with 16.7\% chance. In contrast, compatibility with the frozen native planner improves gradually across depth, with open-loop Avg-L2 reaching its minimum of 2.11\,m only at the final layer. Learned readouts from the first layer recover much of this gap, indicating that planning information is already present early but is not yet represented in the format expected by the deployed planner. Ranking decoder layers by the angular deviation they induce in the planning token permits removal of 8 of 32 layers within an approximately 5\% relative open-loop error increase and yields a measured 1.33$\times$ decoder speedup. At the evaluated sample size, no family-specific degradation is statistically resolved. These findings are limited to the evaluated ORION checkpoint and Bench2Drive setup.

---

## 12. TEMPO: Semantic-Action Decoupled RL Post-Training for Vision-Language-Action Models

**Authors:** Ziheng Liu, Quantao Yang
**arXiv:** [2608.07314](https://arxiv.org/abs/2608.07314)
**Categories:** Robotics (cs.RO); Computer Vision and Pattern Recognition (cs.CV)

Vision-language-action (VLA) models are commonly adapted to downstream manipulation tasks via supervised fine-tuning (SFT) or online reinforcement learning (RL) post-training. SFT is prone to distribution mismatch, and existing RL approaches typically apply a single, uniform update strategy to all model components, ignoring their distinct functional roles. We propose TEMPO, a semantic-action decoupled, two-timescale RL post-training framework for VLA models. TEMPO freezes the pretrained vision-language backbone to preserve general semantic representations, and restricts adaptation to two components with dedicated RL optimization loops: the semantic projection layer and the low-level action expert. We update them at different rates--the semantic projection layer infrequently, to keep the latent action stable, and the action expert frequently, to rapidly incorporate control feedback from online interaction. This decoupling RL fine-tuning strategy prevents fast policy updates from destabilizing high-level semantic representations while still allowing the action expert to learn efficiently from online feedback. Experiments on the CALVIN benchmark and real-world manipulation tasks demonstrate that TEMPO consistently outperforms both pretrained state-of-the-art VLA models and the RL post-training baseline, while reaching and maintaining higher evaluation rewards on two real-world tasks.

---

## 13. Cross-View Action Consistency for Camera-Robust Vision-Language-Action Policies

**Authors:** Bingqi Huang, Bingchuan Wei, Xuan Wang, Yingkai Cai, Zhaokui Wang
**arXiv:** [2608.06965](https://arxiv.org/abs/2608.06965)
**Categories:** Robotics (cs.RO)

Vision-language-action (VLA) policies fine-tuned from a fixed scene camera can fail when the camera is moved, even when the task, objects, language, and robot state are unchanged. We study scene-camera viewpoint robustness using only a scene RGB image, language, and proprioception, without camera labels, extrinsics, depth, or point-cloud inputs. The wrist stream is masked throughout to prevent an unperturbed visual shortcut from confounding attribution to scene-camera variation. For flow-based VLAs, we propose to regularize the action-flow velocity field, the quantity directly integrated to generate continuous action chunks. We construct action-equivalent view pairs by resetting original LIBERO demonstrations to the same MuJoCo state and rendering nominal and perturbed scene-camera views. Both views are supervised by flow matching, while a cross-view loss encourages their predicted action-flow velocities to agree at the same sampled flow coordinates. On the LIBERO-Plus camera-perturbation track, our method reaches 87.2$\pm$0.4% (4,797 rollouts per seed across 3 training seeds), +7.4pp over flow-matching-only training on the same paired data (79.8$\pm$0.8%, also 3 seeds) and +12.5pp over naive mixed-camera SFT, while maintaining nominal-camera ID performance (95.0$\pm$0.8%; same-data FM-only: 95.0$\pm$4.3%). A shuffled-pair control collapses to 25.8%, showing that the gain depends on action-equivalent pairing. On a real robot, we evaluate three tabletop tasks with 10 rollouts per task and camera placement; held-out-camera success improves from 53.3% to 74.4% under the same single-scene-RGB inference interface.

---

## 14. Is Forward Prediction Enough? Physical State Grounding for JEPA World Models

**Authors:** Haodong Yan, Jiaguan Zhu, Mingyuan Jia, ..., Yuxiang Gao, Haoang Li
**arXiv:** [2608.06799](https://arxiv.org/abs/2608.06799)
**Categories:** Robotics (cs.RO); Computer Vision and Pattern Recognition (cs.CV)

Learning structured and control-relevant latent representations remains a key challenge for world models. Recent JEPA-based world models learn action-conditioned predictive latent dynamics from observation sequences. However, their forward-prediction objectives do not explicitly enforce reliable identifiability of robot-centric physical state from individual latents or state changes from latent pairs, which can limit downstream planning and policy performance. We propose PSG-JEPA, a physically grounded JEPA world model that shapes its latent space with two complementary grounding objectives beyond forward prediction: grounding individual latents in robot proprioceptive state, and grounding latent pairs in multi-horizon joint-angle changes. Both objectives are applied only during training, leaving the inference architecture and computational cost unchanged. To comprehensively evaluate PSG-JEPA, we conduct experiments at three levels: (1) latent identifiability via probing, (2) goal-conditioned planning on frozen latents, and (3) policy learning in simulation and on a real robot. Experiments demonstrate that our PSG-JEPA consistently outperforms state-of-the-art latent world-model baselines at all three levels.

---

## 15. AtlasVLA: Persistent World-Ego State Modeling for Vision-Language-Action Models

**Authors:** Guiyu Zhao, Longteng Guo, Yanghong Mei, ..., Jie Jiang, Jing Liu
**arXiv:** [2608.06729](https://arxiv.org/abs/2608.06729)
**Categories:** Robotics (cs.RO); Computer Vision and Pattern Recognition (cs.CV)

While Vision-Language-Action (VLA) models have advanced embodied AI, their fundamentally reactive paradigm severely limits performance in partially observable and long-horizon tasks. When restricted to a single wrist-mounted camera, they inevitably suffer from perception forgetting as objects exit the field of view, and temporal task-progress forgetting} during multi-step execution. To overcome these bottlenecks, we propose AtlasVLA, a novel framework that transitions from direct reactive manipulation to proactive reasoning through a persistent world-ego state. AtlasVLA features a dual-memory architecture: a 4D Persistent World State Memory that lifts transient 2D observations into a globally updated, voxel-hashed spatial state to resolve visual blind spots, and an Ego-Working State Memory that tracks historical ego state and task progress. By conditioning a diffusion transformer (DiT) on this joint World-Ego state, AtlasVLA enables robust spatial reasoning. Extensive evaluations across LIBERO, RLBench, and real-world benchmarks demonstrate that AtlasVLA achieves state-of-the-art performance using solely a wrist camera. Remarkably, it decisively outperforms multi-view baselines, yielding absolute success rate improvements of 9.4% on LIBERO-Long and 17.5% in real-world long-horizon tasks.

---

## 16. CrossTracer: Cross-Embodiment Navigation via VLA Model Reasoning and Trace Residuals Adapting

**Authors:** Yao Wang, Siyuan Wang, Zhirui Sun, ..., Jiankun Wang, Wenjun Xu
**arXiv:** [2608.06688](https://arxiv.org/abs/2608.06688)
**Categories:** Robotics (cs.RO)

Vision-language-action (VLA) models provide strong semantic priors for robot navigation, but they often ignore embodiment-specific mobility constraints. A path that is semantically plausible for one robot may be physically infeasible for another. We propose CrossTracer, a hierarchical framework for cross-embodiment navigation through adaptive trace residuals. CrossTracer represents navigation plans as normalized image-plane waypoints, forming a unified pixel-space interface between semantic reasoning and physical grounding. First, Vision-Language Trace Proposer (VL-Tracer) adapts a pretrained VLA model to predict an initial navigation trace from egocentric observations and flexible goal specifications. Second, CE-Adapter refines this trace by predicting embodiment-conditioned residual corrections from visual traversability cues, robot identity, and the initial trace. To train the refinement module without costly manual annotation, Cross-Embodiment RRT* (CE-RRT*) converts panoptic segmentation into robot-conditioned traversability cost maps and generates cost-minimizing pixel-space traces. We evaluate CrossTracer on the NaviTrace benchmark, which tests whether a model can generate embodiment-consistent navigation traces from egocentric observations, language instructions, and robot embodiment types. CrossTracer achieves a total score of 45.68, outperforming the strongest evaluated general-purpose baseline, Gemini-2.5-Pro, by 10.01 points, corresponding to a 28.1% relative improvement. Real-world deployment on wheeled and legged robots further shows improved navigation success and execution efficiency.

---

## 17. SimWAM: A Simple World Action Model for End-to-End Autonomous Driving

**Authors:** Zongchuang Zhao, Xin Zhou, Tianyang Xu, ..., Dingkang Liang, Xiang Bai
**arXiv:** [2608.07468](https://arxiv.org/abs/2608.07468)
**Categories:** Computer Vision and Pattern Recognition (cs.CV)

World-Action Models (WAMs) improve end-to-end autonomous driving by transferring video dynamics priors to action prediction, but existing methods require costly future generation at inference. We present SimWAM, a simple yet effective WAM that uses video generation purely as a training signal. It co-trains a pretrained video expert and a lightweight action expert with joint flow matching. An isolated attention mask keeps action prediction independent of future frames, allowing the video branch to be discarded after training and leaving a self-contained planner that directly predicts trajectories. Since the two experts share no parameters and interact only through a unified attention interface, the video backbone could be replaced and the action expert scaled independently without modifying the learning objective or inference pipeline. We further apply reinforcement learning to optimize a compositional driving reward beyond trajectory imitation. Our SimWAM achieves $91.5$ PDMS on NAVSIM, surpasses state-of-the-art WAM-based planners with substantially lower latency, and transfers zero-shot to nuScenes. These results position SimWAM as a simple yet solid baseline that could readily benefit from advances in video generation for efficient autonomous driving. The code and model weights are available at this https URL

---

## 18. UniJEPA: A Unified Joint-Embedding Predictive Architecture for Task-Agnostic Visual World Modeling

**Authors:** An Lanji, Dawei Liu, Jin Li, ..., Mei Chen, Yu Tian
**arXiv:** [2608.07409](https://arxiv.org/abs/2608.07409)
**Categories:** Computer Vision and Pattern Recognition (cs.CV)

Joint-Embedding Predictive Architectures (JEPAs) have emerged as a principled framework for self-supervised learning of world models in compact latent spaces, yet existing methods are fragmented: some predict masked parts of a single image in latent space (I-JEPA), others learn to predict global photometric transformations (Image World Models), while video-scale JEPAs predict future temporal states and are post-trained for action-conditioned planning (V-JEPA~2, DINO-World, DINO-WM). These objectives are treated as distinct recipes with separate encoders, predictors, and anti-collapse regularizers, hindering a single model from unifying image-level and video-level world modeling. We present UniJEPA, a unified JEPA that jointly learns photometric prediction (image-level transformations) and temporal prediction (video-level next-state dynamics) in one shared latent space. A single end-to-end objective, composed of a next-embedding prediction loss and a Gaussian regularizer, yields a provably anti-collapse encoder-predictor pair trainable from raw pixels without EMA, stop-gradient, or pre-trained encoders. We show that the same latent space supports controllable abstraction: photometric prediction learns invariant structure while temporal prediction learns equivariant dynamics. After action-conditioned post-training on offline trajectories, UniJEPA enables zero-shot planning by treating goal features as prediction targets. On image, video, and control benchmarks, UniJEPA matches or surpasses task-specific JEPAs while requiring a single loss hyperparameter, and plans up to tens of times faster than generative world models at comparable accuracy.

---

## 19. WNM-3D: A World Navigation Model with 3D Scene Conditioning for Closed-Loop VLN

**Authors:** Yuehao Huang, Yunzi Wu, Xiaotao Zhang, ..., Yong Liu, Xuelong Li
**arXiv:** [2608.07267](https://arxiv.org/abs/2608.07267)
**Categories:** Artificial Intelligence (cs.AI); Computer Vision and Pattern Recognition (cs.CV); Robotics (cs.RO)

Recent vision-language navigation (VLN) systems increasingly adapt pretrained vision-language models (VLMs) into vision-language-action (VLA) policies that map egocentric observations and language instructions directly to navigation actions. Although semantically capable, such action-centric training does not explicitly model how the agent's visual observations should evolve under its predicted motion. Generative world-action models (WAMs) jointly predict future observations and actions, yet existing WAMs for continuous VLN do not condition joint future-view and action generation on geometry-aware representations inferred from the observed history. We present WNM-3D, a generative World Navigation Model with 3D scene conditioning for continuous VLN. To consolidate past observations into persistent scene context, a frozen feed-forward geometry encoder extracts geometry-aware representations from the monocular egocentric RGB history, and a trainable 3D Scene-to-Token Adapter converts them into a fixed-length prefix in the token space of the world-action Diffusion Transformer. Through block-causal attention, this prefix conditions every future video-action block, providing a shared geometric context for both future-view and action generation. We train WNM-3D through supervised world-action fine-tuning on A*-generated demonstrations, DAgger-style adaptation on policy-visited states, and DanceGRPO-based closed-loop policy optimization. Experiments on GN-Bench show that WNM-3D outperforms strong VLM-based navigation policies and its 2D-conditioned counterpart in closed-loop navigation. On a fixed near-goal evaluation set, WNM-3D also achieves higher flow-action consistency and lower visual-motion error.

---
