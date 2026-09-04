# arXiv Daily Digest — 2026-09-03

**Mode:** direct
**Categories:** cs.AI, cs.LG, cs.RO, cs.CV
**Keywords:** VLA, world model, world action model
**Papers found:** 12

---

## 1. Discriminative World Models for Web Agents

**Authors:** Kelvin Li, Dhruv Pendharkar, Anish Pahilajani, ..., Trevor Darrell, Roei Herzig
**arXiv:** [2609.02885](https://arxiv.org/abs/2609.02885)
**Categories:** Artificial Intelligence (cs.AI); Machine Learning (cs.LG)

Recent web agents use world models for test-time action selection by sampling candidate actions, predicting the resulting web states, and ranking them with a ranker model or a Process Reward Model (PRM). These world models are typically trained via supervised next-state prediction to generate fixed representations like HTML or AXTree snapshots. However, this objective is misaligned with the downstream ranker, which relies on predicted states being discriminative across candidates to accurately score them. To address this, we introduce predicted-state matching, a training objective where the predicted representation must distinguish the true resulting state from those reached by alternative actions. We train these models using a branching web-agent dataset derived from WebArena Go-Browse trajectories, where every decision point contains multiple alternative actions and their resulting states. Experiments on our held-out predicted-state matching benchmark show that our approach outperforms world models trained with supervised next-state prediction. We further show that our approach improves PRM-style action ranking on WebPRMBench compared with action-only PRMs and PRMs augmented with supervised-next-state world models. Finally, on WebArena-Lite, using our world model for test-time action selection improves end-to-end task success. Our project page is available at: this https URL.

---

## 2. Belief-Calibrated Optimization: An Explicit World Model for Agentic Optimization

**Authors:** Yuhan Chen, Zhihua Tian, Mahavir Dabas, ..., Nan Wang, Ruoxi Jia
**arXiv:** [2609.01861](https://arxiv.org/abs/2609.01861)
**Categories:** Artificial Intelligence (cs.AI)

The performance of an LLM agent depends on the scaffold around a frozen model. A common way to improve that scaffold is to use a coding agent as an optimizer: it reads current scores and traces and iteratively edits the source, producing a new candidate each round. Each edit is chosen according to a belief about how the environment will respond: what went wrong, and which change should help. That belief is typically implicit. It lives in the coding agent's reasoning on the current call, or remains latent in its parameters, rather than as something written down. Later calls therefore see scores and traces, but they do not use that belief. We introduce Belief-Calibrated Optimization (BCO), a method that writes that belief down as a persistent in-context document and continually revises that document as new candidates are evaluated. The resulting document is a world model: the current account of how the environment responds to edits. Added to an otherwise standard loop, BCO reaches a higher train passrate than a matched control that lacks only the world model, on five benchmarks spanning memory QA, tool-use QA, code-as-action app agents, and terminal agents. The gap remains on every held-out split, which is not used to select the candidate. After a target-model swap, in which the frozen model is replaced and the scaffold is not, the selected BCO scaffold leads on the tasks we test, except where context-window overruns leave it unfinished. An offline ablation then asks whether that gap comes from what the world model says. A fresh predictor given the accumulated document forecasts how the environment will respond more accurately than predictors given either no document or a same-form copy whose content has been falsified. The comparison indicates that the document carries reusable information in its content, not only in its form.

---

## 3. Modeling What Changes: Sparse, Residual World Models for Object-Centric Manipulation

**Authors:** Param Thakkar, Parsika Paresh Shah, Manisha Sushant Gote
**arXiv:** [2609.02046](https://arxiv.org/abs/2609.02046)
**Categories:** Robotics (cs.RO); Artificial Intelligence (cs.AI)

Monolithic world models predict the entire next state at every step, spending capacity re-predicting the static majority of a scene and injecting error into it. We ask whether explicitly modeling change (a per-object change gate plus a residual delta head that perturbs only the objects the gate flags) is a more effective and interpretable bias for physical prediction and control. On a MuJoCo tabletop pushing benchmark scaling from 3 to 8 objects, the sparse/residual model predicts next-state poses 2.5 to 4.6 times more accurately than a dense multilayer perceptron at 8.6 to 11.1 times fewer parameters, sustains change-detection F1 of 0.80 to 0.87 where the dense baseline is degenerate, transfers across object counts with zero retraining (99.4 percent F1 retention), and reaches about 90 percent of its full-data accuracy with a quarter of the data. In autoregressive rollout it compounds far less error, hugging the no-motion floor while the dense model drifts. Finally, inside a sampling-based planner, prediction-only models fail (though a true-simulator oracle solves the task with the identical planner, confirming the planner is sound), but once featurized and trained for the states a planner visits, the sparse model begins to plan (0.23 plus or minus 0.06 success over three seeds) while the dense monolith stays at zero at every seed. Modeling what changes, rather than re-predicting the whole world, is a simple, effective bias for object-centric physical AI; code, data generators, and all checkpoints will be released upon publication.

---

## 4. WMLLM: Self-Evolving Optimization Agents via Predict-Then-Act World Modeling

**Authors:** Zhongzheng Li, Qingsong Ran, Shikun Feng, ..., Yue Wang, Xiaoguang Zhao
**arXiv:** [2609.01608](https://arxiv.org/abs/2609.01608)
**Categories:** Machine Learning (cs.LG); Artificial Intelligence (cs.AI)

Black-box optimization problems remain challenging because of large, weakly structured, and high-dimensional search spaces. Existing methods often suffer from poor sample efficiency because they rely on direct candidate generation or trial-and-error refinement. A natural way to improve search efficiency is to use world modeling, which can help identify promising optimization directions before costly evaluation. Large language models can predict the outcomes of these candidates with nontrivial accuracy because of their implicit knowledge. Motivated by this observation, we propose WMLLM, a self-evolving optimization-agent framework based on predict-then-act world modeling. The agent first predicts promising directions and then acts to generate candidates. Combined with agentic multi-turn refinement, population-based search, and reinforcement learning, WMLLM refines both its implicit world model and its optimization strategy during search. Experiments on black-box optimization tasks, especially multi-objective molecular optimization, show that WMLLM improves sample efficiency and final optimization performance. On the multi-objective molecular optimization benchmark, WMLLM achieves state-of-the-art results under a limited evaluation budget.

---

## 5. Do Better Imagined Rollouts Mean Better Robot Control? A Controlled Study of World-Model Evaluation Under Feedback

**Authors:** Dharini Raghavan, Amritpal Singh
**arXiv:** [2609.02811](https://arxiv.org/abs/2609.02811)
**Categories:** Robotics (cs.RO)

Predictive models are increasingly used in robotics for state estimation, planning, control, and policy evaluation, yet they are often judged by open-loop prediction accuracy over a fixed horizon. In closed-loop operation, a robot repeatedly acts, receives new measurements, updates its state estimate, and recomputes control. We study this difference in a differential-drive path-tracking task with biased odometry and intermittent landmark sensing. Six state estimators are evaluated across 24 sensing conditions using trajectory replay, a 20-step measurement-free rollout, and closed-loop tracking. Replay position RMSE correlates more strongly with closed-loop cross-track RMSE than rollout error (Spearman rho = 0.923 vs. 0.774) and selects a different estimator from the closed-loop optimum in 5/24 conditions, compared with 18/24 for the rollout metric. We then vary rollout horizon and measurement-update interval. With H=20, rank agreement decreases from rho = 0.916 with measurements at every step to rho = 0.774 with no measurements. A horizon-update grid shows that long prediction horizons remain informative when regular corrections are retained, whereas long rollouts without correction can produce rankings that differ substantially from closed-loop behavior. We also test recurrent estimators trained on longer sensing outages. This improves the EKF-anchored models under combined sensing degradation, reducing GRU-EKF cross-track RMSE from 1.72 m to 1.06 m, but the gain is not consistent across isolated outages or estimator architectures. These results show that predictive-model evaluation in robotics should specify both prediction horizon and measurement-update schedule. For models used in feedback, offline rollouts are most informative when their sensing and correction pattern reflects closed-loop operation. Code is available at this https URL

---

## 6. Latent Cluster Analysis for Vision-Language-Action Models

**Authors:** Theodor Wulff, Sergio Lanza, Tamara Bila, ..., Stefan Wermter, Igor Farkas
**arXiv:** [2609.02634](https://arxiv.org/abs/2609.02634)
**Categories:** Robotics (cs.RO)

Vision-Language-Action (VLA) Models are increasingly used in robotics for their ability to ground language and perception into action, yet the internal representations driving their behaviour remain poorly understood. We propose LAVLA, a framework for latent cluster analysis of VLA models, and conduct a layer-wise study of the state-of-the-art GR00T N1.5 model, with particular focus on its action decoder. To better characterise the latent space during action diffusion, we introduce a cross-attention-based embedding-weighting method that amplifies relevant features while suppressing less informative ones. Quantitative evaluation shows that weighted clustering consistently outperforms the baseline. To improve interpretability, we extract human-interpretable concepts for each cluster, linking latent representations to semantic descriptions. Our analysis shows that latent clusters progressively disentangle spatiotemporal and kinematic features, with representations becoming more refined in the middle layers and stabilising toward the output. As such, LAVLA advances the interpretability of language-driven robotic systems.

---

## 7. ZETA: A Controlled Study of Zero-Shot Cross-Embodiment VLA Transfer for Tabletop Manipulation

**Authors:** Mi Yan, Wenhao Zhang, Zhiqi Zhang, ..., Zhizheng Zhang, He Wang
**arXiv:** [2609.02546](https://arxiv.org/abs/2609.02546)
**Categories:** Robotics (cs.RO)

Zero-shot generalization to unseen embodiments is important for generalizable vision-language-action (VLA) models as robot hardware evolves and task-specific data collection remains costly. However, a systematic understanding of this problem remains limited, in part because the literature lacks a unified zero-shot transfer definition and controlled evaluation settings that isolate embodiment changes from differences in tasks, scenes, or protocols. To address this gap, we first distinguish strict zero-shot transfer, where the target embodiment is absent from all training data, from pretrain-exposed zero-shot transfer, where it appears only during pretraining. We then introduce a controlled benchmark spanning 14 held-out target embodiments across simulation and real-world validation. Within this framework, we conduct a controlled analysis of four factors: state-action representations, pretraining embodiment diversity, auxiliary co-training objectives, and target-embodiment exposure. Experimental results show that local end-effector (EEF) state-action representations, the source embodiment diversity, and auxiliary co-training improve cross-embodiment transfer by around 15, 18, and 7 percentage points, respectively. We further find that adding only 5% target-embodiment data during pretraining improves average target-embodiment progress by 13.4 percentage points, showing that strict and pretrain-exposed zero-shot transfer are distinct and should be reported separately. Together, these findings provide practical guidance for evaluating and improving cross-embodiment VLA transfer in stationary tabletop manipulation with two-finger grippers, while motivating future investigation of broader settings including mobile-base control, dexterous hands, and long-horizon tasks.

---

## 8. World-Model-Augmented Visual Locomotion for Humanoids on Foothold-Constrained Terrain

**Authors:** Yuxi Liu, Lijun Han, Ziming Wang, ..., Cong Yang, Wei Sui
**arXiv:** [2609.02542](https://arxiv.org/abs/2609.02542)
**Categories:** Robotics (cs.RO)

Foothold-constrained terrain is characterized by sparse, discontinuous, or geometrically restricted feasible foot contacts, as encountered on stepping stones, across gaps, and on narrow stair treads. On such terrain, a single misstep often leaves little room to recover, so policies that base foot-placement decisions primarily on the immediately visible terrain are prone to failure. We ask whether a learned predictive summary of near-future observations and rewards can provide the anticipatory information required in such settings. We present World-Model-Augmented Visual Locomotion (WM-LOCO), which jointly trains a recurrent world model and a PPO policy. Conditioned on proprioception and a single onboard depth image, the world model produces a predictive recurrent feature that guides the policy, without explicit foothold labels. In simulation, WM-LOCO succeeds on gaps and stepping stones where a matched baseline fails completely, and matches the baseline's success rate on stairs while improving stride efficiency and reducing pelvis acceleration. We deploy the same policy onboard a physical Unitree G1 humanoid using onboard proprioception and a single depth stream; it traverses all three terrain classes with an average success rate of 93.3%.

---

## 9. Spatially Aware World Action Model via Geometric Latent Diffusion

**Authors:** Javier Alejandro Lopetegui Gonzalez, Paul Pacaud, Cordelia Schmid
**arXiv:** [2609.02531](https://arxiv.org/abs/2609.02531)
**Categories:** Computer Vision and Pattern Recognition (cs.CV); Robotics (cs.RO)

World Action Models (WAMs) leverage the capabilities of large-scale pretrained video diffusion models to jointly predict future observations and actions, inheriting rich visual and physical priors from internet-scale video. This has made them a promising paradigm for robot policy learning, yet the prevailing models operate exclusively on RGB observations and do not leverage 3D information. To bridge this gap, we introduce a Spatially Aware World Action Model (SA-WAM), which repurposes a pretrained video model for joint action, RGB, and depth prediction, enabling 3D-aware world modeling and action prediction within a single diffusion backbone. We use a nonlinear encoding that maps the unbounded depth signal into the bounded input domain expected by the frozen VAE tokenizer. This allows us to reuse the tokenizer without 3D-specific fine-tuning, incorporating geometric information without sacrificing the pretrained priors. SA-WAM achieves state-of-the-art results on the RoboCasa and LIBERO-Plus benchmarks, while simultaneously improving future-state predictions. Furthermore, SA-WAM outperforms strong baselines in real-world evaluation using a UR5 robotic arm, with strong gains in randomized environments. We analyze the correlation between world model prediction quality and rollout success, providing insights into WAM performance and avenues for its improvement.

---

## 10. SolarWM: Open Data and Scalable Training for Long-Horizon Video World Models

**Authors:** Junchao Huang, Guian Fang, Shengju Qian, ..., Mike Zheng Shou, Li Jiang
**arXiv:** [2609.02886](https://arxiv.org/abs/2609.02886)
**Categories:** Computer Vision and Pattern Recognition (cs.CV)

We introduce SolarWM, a fully open foundation for building interactive video world models from data preparation through long-horizon inference. Training across heterogeneous data sources and video backbones is challenging: datasets differ in temporal scale, camera geometry, visual quality, motion, and captioning styles, while video generators use distinct representations and architectures. Naive data mixing and model-specific implementations therefore produce inconsistent supervision and make results difficult to reproduce and compare. SolarWM addresses this coupling with a reconfigurable multi-source data engine and a backbone-native adaptation framework. The engine converts 1.43 million canonical clips from 10 datasets into a unified, frame-aligned contract covering visual observations, metric camera geometry, captions, quality metadata, selection decisions, and provenance, while decoupling source processing from mixture construction. Under shared camera-conditioning, training, and inference interfaces, we instantiate four 5B--33B models based on Wan2.2, LTX-2.5, and MiniMax-H3 while preserving their native representations and objectives. A unified three-stage recipe combines bidirectional adaptation, teacher-forced autoregressive initialization, and distribution matching distillation. The resulting causal models enable real-time interaction over rollouts ranging from minutes to hours after being trained on only 5s sequences. By releasing the resulting data, pipeline, recipes, weights, and framework, SolarWM provides a reproducible and extensible foundation for interactive world-model research.

---

## 11. Towards Zero-Shot Transfer Across Embodiments For Driving VLAs

**Authors:** Caio Azevedo, Stefano Sabatini, Sascha Hornauer, Fabien Moutarde
**arXiv:** [2609.02341](https://arxiv.org/abs/2609.02341)
**Categories:** Computer Vision and Pattern Recognition (cs.CV)

Vision-Language-Action models (VLAs) have shown strong potential in autonomous driving by leveraging multimodal pretraining for instruction following, visual reasoning, and scene-level generalization. In robotic manipulation, scaling VLA fine-tuning across multiple robot setups--especially when unifying representations across embodiments--has been shown to improve in-dataset performance and cross-embodiment generalization; in autonomous driving, however, VLAs remain largely trained on individual datasets and are rarely evaluated for zero-shot transfer to unseen datasets and camera rigs; furthermore naively adding more datasets to the training data does not necessarily lead to better performance within seen embodiments. To address these problems, we study multi-dataset training for the driving task and BEV-Forcing, an auxiliary objective that transfers ground-plane object-layout information from a specialized Bird's-Eye-View model into the VLA backbone. By encouraging the model to represent object position through a shared BEV spatial interface, we show that an auxiliary task such as BEV-Forcing can improve both in-distribution and out-of-distribution performance when training on a small number of camera rigs. As the number of training embodiments increases, however, the benefits of the auxiliary task are reduced; we present this as evidence that new techniques in the literature may see their benefits diminish when simply scaling up training diversity, which motivates presenting results taking into account data scaling.

---

## 12. World-Coherent Decoding: Self-Verifying Test-Time Planning for World Action Models

**Authors:** Chuhan Zhang, Seiji Ito, Kenta Hoshino, Satoshi Ikehata, Ikuro Sato
**arXiv:** [2609.02159](https://arxiv.org/abs/2609.02159)
**Categories:** Computer Vision and Pattern Recognition (cs.CV)

World Action Models (WAMs) aim to control robots by stochastically generating visual futures and then decoding actions, but empirical observations indicate that the results can strongly depend on which future is selected. We propose World-Coherent-Decoding (WCD), a self-verifying test-time planning framework that treats WAM rollouts as falsifiable future--action hypotheses. At each decision step, WCD samples multiple candidates from a frozen WAM and ranks them using internal generative signals: flow-based video surprisal for visual plausibility and action path effort for action-generation stability. After execution, the realized observation audits the selected imagination, yielding an imagination--reality mismatch that trains a lightweight online predictor for future candidate selection. Thus, WCD converts delayed self-verification into pre-execution reliability estimation without updating the backbone model. On RoboTwin 2.0, WCD improves Hard success under limited randomized-scene supervision from $55.80\%$ to $60.90\%$, with a $+16.43$ gains on Horizon-3 tasks, and shows qualitative robustness on real Franka visual-shift tests. These results highlight a simple principle: test-time scaling for WAMs depends less on sampling more futures than on selecting reliable ones.

---
