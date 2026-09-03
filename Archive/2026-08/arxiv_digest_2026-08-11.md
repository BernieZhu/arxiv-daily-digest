# arXiv Daily Digest — 2026-08-11

**Mode:** direct
**Categories:** cs.AI, cs.LG, cs.RO, cs.CV
**Keywords:** VLA, world model, world action model
**Papers found:** 29

---

## 1. Model Discovery Agent: LLM-assisted Bayesian experiment design for data-efficient discovery of mechanistic world models

**Authors:** Kevin Murphy
**arXiv:** [2608.09696](https://arxiv.org/abs/2608.09696)
**Categories:** Artificial Intelligence (cs.AI)

Predicting the answer to interventional ``what if'' questions --- the outcome of an action never taken --- requires a \emph{mechanistic}, causal model, not a curve fit; and learning such a model requires \emph{experiments}, because passive data leaves its mechanisms unidentified. Experiments are expensive, so the central problem is \emph{data efficiency}. We present the Model Discovery Agent (MDA), which couples a large language model (LLM), used as a \emph{proposer} of candidate structures, with standard Bayesian machinery --- sequential Monte Carlo (SMC) for parameter and structure posteriors, simulation-based inference (SBI) for intractable likelihoods, and value-of-information (VoI) for experiment design --- to discover latent mechanistic world models from few interventions. MDA operates in the M-open setting: when the truth lies outside the current hypothesis class, a predictive check flags the inadequacy and the proposer expands the hypothesis space with a new model whose parameters are then identified by designed experiments. We show that \emph{discovery and design reinforce}: the design step identifies the mechanism the discovery step proposes, and the identified mechanism improves predictions, enabling further discoveries from the remaining unexplained residuals. On three different benchmarks --- covering physics (\DPbench, \citep{wiemann2026discoverphysics}), chemistry (\CHEMbench, \citep{kabra2026autoscilab}) and biology (\HHbench, a new partially observed single-neuron electrophysiology benchmark we create) --- we show that MDA sets a new SOTA in terms of data-efficient model learning and reliable interventional prediction ability.

---

## 2. verdi: retrieval is not transfer for continual world model optimization

**Authors:** Junyu Wu, Shiqin Nie, Youyi Kou, ..., Sen Cui, Changshui Zhang
**arXiv:** [2608.09537](https://arxiv.org/abs/2608.09537)
**Categories:** Artificial Intelligence (cs.AI)

Foundation world models have made remarkable progress in planning, simulation, and embodied intelligence. However, optimizing a pretrained world model toward a user-specified objective remains difficult: each campaign typically rediscovers optimization strategies from scratch, and the resulting knowledge rarely transfers to the next model. Existing research agents automate the optimization loop but treat successful strategies as directly reusable recipes, without principled safeguards for when transfer is appropriate. We argue instead that retrieval is not transfer: a strategy validated on one model is at best an optimization hypothesis for another, and becomes transferable knowledge only after target-side experimental valida- tion. Guided by this principle, we propose VERDI , a continual framework for evidence-licensed world model optimization. VERDI characterizes each world model through shared inference-time probes to construct an Optimization Fin- gerprint, retrieves relevant prior experience as ranked hypotheses, and validates every candidate under a frozen target-side verifier before admitting it as reusable evidence; contradictions among nearby fingerprints further trigger probe evolution, continually refining the diagnostic representation itself. Experiments on Ctrl-World, the Cosmos family, and RoboCoin show that VERDI reduces search cost by 68%, GPU cost by 69%, and negative transfer from 0.34 to 0.06, while predicting transfer outcomes with 83% sign accuracy.

---

## 3. A Structural Dynamics Graph World Model: Unified Modeling, Constrained Rollout, and Interpretable Calibration

**Authors:** Wei Wang, Yaosen Chen, Han Yang, ..., Xuming Wen, Ming Liu
**arXiv:** [2608.08689](https://arxiv.org/abs/2608.08689)
**Categories:** Artificial Intelligence (cs.AI)

The state evolution of a complex system arises jointly from object laws, relational propagation, domain conservation, and unmodeled error. Forcing all sources into one black box makes mechanism attribution and constraint preservation unauditable; forcing every mechanism into one equation family discards mature domain solvers. We propose SD-GWM, a Structural Dynamics Graph World Model as an executable structural contract: nodes declare self-dynamics S, edges declare neighbor graph-coupled dynamics N---both fixed-form mechanism assets (rules, ODEs, solvers) calibrating only authorized parameters. An optional bounded residual R concentrates learnability, while a global projection maps states to feasibility, enforcing constraints without guaranteeing accuracy gains. On eight pre-registered research questions, SD-GWM delivers (i) heterogeneous integration: rules and solvers plug in natively; (ii) semantic fidelity: disabling R preserves source semantics bit-for-bit, with four theory properties under explicit proof/empirical boundaries; (iii) auditable governance: stepwise traces enable counterfactual fault localization (top-1 = 1.0) without post-hoc approximations. On a semi-synthetic flood testbed and USGS streamflow, SD-GWM reduces constraint violations to floating-point tolerance in analytical tests and to zero in semi-synthetic and real-data cases. Persistence matches SD-GWM in calm periods, but during a 254-day extreme-flood shift persistence and all neural baselines collapse (90-min RMSE 892-3007 cfs) while SD-GWM holds at 108 cfs (8-28x gain). The bounded residual cuts RMSE ~50% only under backbone bias. We position SD-GWM not as a universally superior forecaster, but as a verifiable substrate for auditable, constraint-safe spatiotemporal mining.

---

## 4. CausalNav: Reliability-Certified Causal World Models for Control under Physical-Parameter Shift

**Authors:** Yiyao Zhang, Diksha Goel, Hussain Ahmad, Shixun Huang, Jun Shen
**arXiv:** [2608.07809](https://arxiv.org/abs/2608.07809)
**Categories:** Artificial Intelligence (cs.AI)

A world model is only useful for physical AI if it changes what the agent does, and only safe if it declines to do so when it is wrong. We study both halves of that requirement with CausalNav, a controller built around a signed, action-conditioned transition graph over identified state coordinates. At deployment CausalNav simulates a small library of intervention sequences, converts their objective error into policy-logit advice, and admits that advice only when a scale-free predictive-reliability certificate, a policy-margin gate, and an argmax-agreement gate all pass; otherwise it falls back exactly to its own model-based base controller. We evaluate against nine controlled baselines (transformer, recurrent, split-latent, graph, causal-induction, and three recent model-based reasoning modules) on CartPole-v1 and discretized Pendulum-v1 with physical-parameter shifts, under one shared PPO trainer, one interaction budget, and ten held-out seeds (200 runs). CausalNav attains the best average rank (1.25 of ten). The diagnostic result is more informative than the ranking: the learned graph recovers structure well above chance (CartPole F1 = 0.59 +/- 0.09), yet per-seed structural fidelity is uncorrelated with per-seed control benefit (r = -0.15, p = 0.67), and the certificate abstains on 10/10 Pendulum seeds, where forcing the planner on costs return. Model fidelity did not predict downstream control utility in our setting; certified abstention, not better prediction, is what made the world model safe to deploy.

---

## 5. CMU-Drive and V2V-VLA: Cooperative Multi-agent Unified Driving with Reasoning Benchmark and Vehicle-to-Vehicle Vision-Language-Action Models

**Authors:** Hsu-kuang Chiu, Stephen F. Smith
**arXiv:** [2608.07621](https://arxiv.org/abs/2608.07621)
**Categories:** Artificial Intelligence (cs.AI); Computer Vision and Pattern Recognition (cs.CV); Robotics (cs.RO)

Vision-Language-Action (VLA) models have recently achieved impressive performance for end-to-end autonomous driving, yet existing approaches are primarily designed for an individual single autonomous driving agent with limited support for cooperative perception, reasoning, and planning. We present Cooperative Multi-agent Unified Driving with Reasoning (CMU-Drive), a closed-loop end-to-end benchmark for evaluating cooperative autonomous driving with multiple connected autonomous vehicles (CAVs) operating in safety-critical driving scenarios with background traffic participants. We further propose Vehicle-to-Vehicle Vision-Language-Action (V2V-VLA), a cooperative VLA model that integrates cooperative driving into a single forward pass by jointly generating driving actions, future waypoints, language reasoning, and communication policies. Experiments on CMU-Drive establish the first benchmark and baseline for cooperative VLA driving and provide a foundation for future research on multi-agent, closed-loop, end-to-end cooperative autonomous driving. Our code, benchmark, and model checkpoint will be publicly released to facilitate open-source research.

---

## 6. Energy-Structured Latent World Models with Neural Time Fields for Physically Constistent Open-World Motion Planning

**Authors:** Yapeng Liu, Yuanzhao Zhai, Bo Ding, Huaimin Wang, Lin Wang
**arXiv:** [2608.09876](https://arxiv.org/abs/2608.09876)
**Categories:** Robotics (cs.RO); Artificial Intelligence (cs.AI)

Physically consistent motion planning remains a fundamental challenge in embodied AI, as generated trajectories must strictly conform to real-world execution dynamics. While latent world models offer a promising approach by predicting these dynamics, existing methods learn unconstrained future representations where absorbed physics remains implicit. Therefore, they fail to form reusable physical knowledge, which compromises reliability in unpredictable open-world navigation. To address this, we propose a novel Energy-Structured Latent World Model (ELWM). Our key idea is to structure the ELWM latent state to explicitly carry energy and momentum, ensuring strictly causal transitions via dissipation and control ports. Trained on multimodal RGB-D and inertial interaction histories, our model guarantees physically consistent predictions. We further implement this for motion planning by constructing Physics-Conditioned Neural Time Fields (PC-NTF), a key technical cornerstone that integrates ELWM into an arrival time field via the Eikonal equation to yield a physically-informed navigation policy. Across held-out scenes, our evaluation reveals significant improvements. Compared to generic latent models, PC-NTF reduces 0.8-s motion-prediction NRMSE from 0.36 to 0.29. Against Active Neural Time Fields, it improves navigation success from 81.3% to 89.7% and SPL from 0.64 to 0.73, while cutting the physical collision rate from 12.1% to 5.8% and the Eikonal residual from 0.083 to 0.031. Beyond these targeted gains, our results demonstrate that embedding explicit physical structures into latent spaces intrinsically bridges the gap between predictive world models and safe, dynamically feasible motion planning.

---

## 7. WorldSimProbe: Diagnosing Simulator Faithfulness in Action-Conditioned World Models for Embodied Manipulation

**Authors:** Peterson Co, Sicheng Hu, Chunxuan Jiao, ..., Huajie Tan, Shanghang Zhang
**arXiv:** [2608.09298](https://arxiv.org/abs/2608.09298)
**Categories:** Robotics (cs.RO); Artificial Intelligence (cs.AI)

Action-conditioned world models (ACWMs) promise to provide embodied AI with scalable predictive simulators for planning, policy evaluation, and data generation. Realizing this promise requires precise action-conditioned transitions rather than merely plausible outputs. Yet their applicability remains difficult to establish because prevailing evaluations emphasize visual quality, task outcomes, or coarse rollout-level responsiveness without directly testing simulator fidelity. To address this gap, we evaluate ACWMs through the observable capabilities expected of physical simulators. Accordingly, we formalize Observable Simulator Contract, a minimal contract that any action-conditioned physical simulator should satisfy: supplied actions must induce corresponding agent motion, and environment responses must be grounded in that realized motion. To operationalize this contract, we introduce WorldSimProbe, comprising five controlled suites spanning local control sensitivity, global trajectory variation, source-diverse actions, interaction grounding, and dynamics. Suite-specific evaluators assess simulator-relative calibration, dense action-to-motion correspondence, false-interaction grounding, and primitive-level dynamics. We evaluate six open-source ACWMs on more than 18,000 instances across RoboTwin, ManiSkill, and LIBERO. World-SimProbe reveals systematic action-realization degradation across control variation, structured failures in interaction grounding and dynamics, and benchmark signals consistent with human judgments and downstream outcomes. Together, this capability-based framework provides a transparent, and standardized paradigm for diagnosing ACWM simulator fidelity beyond coarse, task-directed evaluation.

---

## 8. Population-Scalable Multi-Agent World Modeling

**Authors:** Renjie Zhao, Yuxiang Wu, Mingyu Zhang, ..., Jianyi Zhu, Yong-Lu Li
**arXiv:** [2608.08600](https://arxiv.org/abs/2608.08600)
**Categories:** Computer Vision and Pattern Recognition (cs.CV); Artificial Intelligence (cs.AI); Machine Learning (cs.LG)

World models have recently achieved impressive progress in visual prediction and interactive generation, but extending them to multi-agent environments introduces a fundamental scalability challenge. Existing methods generally assume a fixed number of agents during training and inference, which ties the model to a pre-determined agent population and limits inference-time scalability. Our key insight is that cross-view consistency should arise from a shared world state whose evolution does not assume a predefined number of agents, while agent-specific observations should be generated by querying this state through a unified rendering interface. Based on this insight, we propose Khora, a scalable multi-agent world model that supports inference-time expansion to arbitrary numbers of agents without retraining. Our framework decouples world-state evolution from visual rendering and introduces a population-agnostic rendering mechanism for incorporating other agent information. This design maintains cross-view consistency through the shared world state rather than through dense interactions among observation streams inside the expensive video generator, enabling approximately linear practical scaling with the number of queried views. Qualitative experiments demonstrate that our approach generalizes to unseen numbers of agents while maintaining visual quality and multi-agent consistency. We further implement a real-time interactive system to demonstrate scalable open-world simulation.

---

## 9. SpikeWorld: Fast-State Adaptation for Frozen Spiking World Models

**Authors:** Ziqiao Yu
**arXiv:** [2608.07712](https://arxiv.org/abs/2608.07712)
**Categories:** Computer Vision and Pattern Recognition (cs.CV); Artificial Intelligence (cs.AI)

A predictive model receives a self-supervised signal whenever the consequence of an action is observed. Using that signal after deployment is difficult when dynamics and semantics share parameters: freezing prevents adaptation, whereas weight updates require optimizer state and may alter the learned representation. Here we introduce SpikeWorld, a 1.45M-parameter sparse spiking model jointly trained for heterogeneous sensory prediction, semantics, image-text binding and action-conditioned dynamics. At deployment, all trained parameters are frozen. Delayed next-state residuals update two external paths: cumulative fixed-bank losses select the bounded action correction, while route-specific residual matrices refine next-state prediction. Neither path uses labels, teacher outputs, rewards, success signals or the true shift value. Joint optimization improves action next-state MSE by 17.10\% while also improving multimodal prediction, semantic accuracy and image-text retrieval. On held-out shear and attenuation streams, the combined external state improves aggregate prediction by 5.48\% and 30.01\%; its fixed-bank action path improves tracking by 24.20\% and 3.94\%, respectively. In a six-arm study comprising 450 new Meta-World trajectories (75 per arm), SpikeWorld raises frozen-policy reward by 7.90 (95\% CI [2.48, 14.06]); the 13.33-point success difference is descriptive (CI [0, 40]). For identical sensory inputs, model parameters and inherited semantic outputs remain bitwise unchanged. A 16-byte RLS estimator obtains the highest non-oracle reward on linear attenuation, showing that the contribution is not superior linear identification, but its integration with a frozen multimodal spiking checkpoint. Reference code is publicly available at this https URL.

---

## 10. Twin Rollouts: Noise-Coupled Counterfactual Branching in Interactive Video World Models

**Authors:** Yu Ma, Hongli Shi, Xinran Xu
**arXiv:** [2608.08982](https://arxiv.org/abs/2608.08982)
**Categories:** Machine Learning (cs.LG)

Interactive video world models generate rollouts autoregressively under an action stream, yet they are trained and evaluated almost exclusively on factual prediction. We study counterfactual generation inside the rollout: given a trajectory the model has itself generated, what would have happened had the actions differed from step t* onward? We formalize noise-coupled twin rollouts --- a factual and a counterfactual branch sharing the generated prefix and the future exogenous noise sequence, diverging only in the action stream at an intervention point. Because the factual branch is self-generated, its exogenous noise is known exactly: the abduction step of Pearl's counterfactual procedure is exact by construction, sidestepping the approximate-inversion problem faced by editing-based pipelines. Noise coupling further turns the minimal-change principle into a per-sample verifiable property: we define a spatiotemporal locality metric that penalizes divergence outside the causal descendants of the intervention, computable against simulator ground truth without a learned judge. Forking the simulator state at t* yields ground-truth counterfactual re-renders, which we use as verifiable rewards for post-training. This note establishes the formal framework, metric definitions, and positioning; experiments are forthcoming.

---

## 11. Did the Grid Erase the Event? EndoClock for Auditing Medical World-Model Pipelines

**Authors:** Yarin Udi, Tom Sharon-Shahak, Roee Masad, Dan Pri-Tal
**arXiv:** [2608.09266](https://arxiv.org/abs/2608.09266)
**Categories:** Computer Vision and Pattern Recognition (cs.CV); Machine Learning (cs.LG)

Medical world models commonly learn from multimodal recordings synchronized onto a fixed-rate grid. This preprocessing resamples each native stream onto a shared time axis. Each stream has an observation clock that governs when observations are emitted or updated. When this clock depends on the latent or acquisition state, it is endogenous. In such settings, synchronization may not be neutral and can erase task-relevant evidence before the model sees the data. We introduce a four-regime taxonomy that characterizes where the evidence needed to distinguish a target event or state survives. The relevant witness may remain in the sampled values, in grid-cell update patterns, in native timing, or only in an external acquisition channel. EndoClock operationalizes this taxonomy as a conservative pretraining audit. It reports the lowest witness-bearing representation supported by the available evidence, or unresolved when no regime can be established. We illustrate this failure in echocardiography, where B-mode video write-outs cease during pulsed-wave Doppler acquisition while the corresponding measurement events remain recorded only in an external acquisition log. This work is a preliminary failure alert and executable audit. Its practical message is to preserve the native observation process long enough to determine whether synchronization has erased information required by the intended task.

---

## 12. MotionCraft: Latent World Modeling with Sparse Attention for Visual Upscaling

**Authors:** Rong Fu, Chunlei Meng, Yangchen Zeng, ..., Chenhao Wang, Simon Fong
**arXiv:** [2608.08553](https://arxiv.org/abs/2608.08553)
**Categories:** Computer Vision and Pattern Recognition (cs.CV); Machine Learning (cs.LG); Multimedia (cs.MM)

Video super-resolution (VSR) aims to recover high-fidelity high-resolution videos from low-resolution inputs and is central to applications ranging from mobile capture to streaming and archival restoration. Existing approaches trade off among local-detail fidelity, long-range spatio-temporal modeling, perceptual realism, and efficiency: convolutional alignment techniques preserve local structure but suffer when motion is large or degradations are complex; transformer-based methods capture long-range dependencies yet require architectural or algorithmic adaptations to remain computationally feasible; and recent latent or diffusion-based generators synthesize rich texture but require specialized temporal constraints to maintain coherence. We present MotionCraft, a controllable VSR framework that formulates restoration as motion-aware latent state prediction inspired by world models and integrates adaptive sparse attention with an explicit user-accessible control interface. MotionCraft combines robust motion fusion, a Latent World Transformer that balances locality and targeted non-local interactions, and a compact conditional decoder to deliver temporally consistent, high-quality reconstructions under streaming constraints. Empirical evaluations show that MotionCraft achieves strong reconstruction and perceptual performance while enabling predictable trade-offs between temporal smoothness and reconstruction fidelity.

---

## 13. HarnessWAM: Bridging Prediction and Deliberation in World Action Models

**Authors:** Zhaopeng Gu, Bingke Zhu, Tianxi Lin, ..., Peng Su, Jinqiao Wang
**arXiv:** [2608.09516](https://arxiv.org/abs/2608.09516)
**Categories:** Robotics (cs.RO)

World Action Models (WAMs) jointly learn environmental dynamics and robot actions, introducing priors over physical evolution into embodied control. However, finite-horizon prediction and action generation are insufficient for complex embodied tasks that require global planning, cross-stage state maintenance, execution verification, and failure recovery. We refer to this mismatch as the prediction-deliberation gap of WAMs. To address this gap, we propose HarnessWAM, an agentic framework for WAMs. HarnessWAM employs a vision-language-model-based Task Manager to maintain an evidence-grounded scene belief and a structured task graph. A capability-conditioned executable-space projection further constrains open-ended semantic plans into sequences of atomic skills that satisfy task dependencies, embodiment-state constraints, and the capability boundary of the underlying WAM. During execution, HarnessWAM operates through an event-driven, dual-timescale feedback loop: a lightweight progress estimator continuously provides high-frequency execution evidence, while the Task Manager deliberates at salient milestones by jointly considering the current observation, task state, and interaction history to determine whether to advance the task, acquire additional observations, revise the plan, or initiate local recovery. This mechanism enables the robot to recover its state after a subtask failure and resume execution without discarding previously acquired scene knowledge. HarnessWAM achieves state-of-the-art full-task and subtask success rates of 59.6% and 69.9% on RoboMemArena, and an SR of 23.7% on RoboCerebra Ideal. These results demonstrate that model-external structured state maintenance and closed-loop agentic decision making can effectively extend the local control capabilities of WAMs into embodied task execution that is plannable, verifiable, and recoverable.

---

## 14. Rethink Before You Execute: Adaptive Execution for World Action Models

**Authors:** Feng Ye, Yiming Zhao, Yong Yu, ..., Peng Jia, Chuanmin Jia
**arXiv:** [2608.09492](https://arxiv.org/abs/2608.09492)
**Categories:** Robotics (cs.RO)

World Action Models (WAMs) jointly predict future actions and the evolution of the environment. At each inference, a WAM generates a chunk of actions and the robot executes a fixed prefix before replanning. We argue that this fixed execution horizon is poorly matched to execution dynamics: the chunk reliability varies across task stages, so when to replan depends on the result of accumulated execution, not on the step counts. We propose TempoWAM (Timing Execution by Monitoring Progress Online), a lightweight plug-and-play execution scheme for WAMs. A Recurrent Progress Monitor first estimates task progress from the current observation, task instruction, remaining actions, and execution history; and an Adaptive Execution Protocol then evaluates whether the chunk is advancing the task to decide if replanning is needed. To bridge the training-deployment gap, the protocol is calibrated by a task-dependent calibration factor with online adaptation. Experiments on LIBERO, RoboTwin, and real-world tasks show that TempoWAM consistently improves the efficiency-success trade-off of WAM execution. On real robots, it reduces WAM inferences by 26.9% on easy tasks while maintaining success, and improves success by 13.3 points on difficult tasks.

---

## 15. VANE: Reliable Test-Time Training for Vision-Language-Action Models via Future Visual Representation Prediction

**Authors:** Hongjin Ji, Guoyang Xia, Luoyang Sun, Fangxiang Feng, Lei Ren
**arXiv:** [2608.09448](https://arxiv.org/abs/2608.09448)
**Categories:** Robotics (cs.RO); Computer Vision and Pattern Recognition (cs.CV)

Test-time training (TTT) offers a lightweight way to adapt vision--language--action (VLA) policies from unlabeled deployment streams, but it remains difficult to use reliably in closed-loop manipulation. A shared adaptation space can mix incompatible task corrections, while an online update can alter subsequent actions before its consequences are known. We introduce a reliable TTT framework for VLA policies (VANE). VANE conditions prompt adaptation on the current vision--language context and learns from the future visual consequences of executed actions. Candidate updates are isolated from the live policy, evaluated on subsequent observations, and committed only when supported by future evidence, making adaptation selective and reversible. On SimplerEnv WidowX, VANE improves average success by $3.2$ percentage points over the corresponding TTT baseline. Results on Google Robot further show that deployment-time gains remain task- and embodiment-dependent. Together, these results demonstrate a constrained, evidence-based approach to adapting VLA policies during interaction.

---

## 16. JEPA-WAM: Learning Vision-Language-Action Policies with Joint-Embedding World Modeling

**Authors:** Yihan Lin, Jiawei He, Shifeng Bao, ..., Cheng Chi, Jing Zhang
**arXiv:** [2608.09381](https://arxiv.org/abs/2608.09381)
**Categories:** Robotics (cs.RO)

Robust robot control benefits from explicitly modeling state transitions, but video-generation world action models (WAMs) introduce substantial deployment cost. Existing latent WAMs avoid explicit future generation, but often compress predictive representations or separate predictive modeling from the representations used for action generation. We introduce JEPA-WAM, a latent WAM built in a pretrained V-JEPA space, which couples latent transition prediction with continuous action generation through a shared predictor. JEPA-WAM predicts a spatially structured joint current-future target that captures task-shared visual temporal structure between current and future observations, while preserving dense patch-level correspondence. Through the shared predictor, transition supervision directly shapes the backbone, from which dedicated representations are extracted for action prediction. The same design can also be instantiated in pretrained VLA policies while preserving their original perception and action pathways. On LIBERO-Plus, JEPA-WAM achieves 79.2%, the best result without large-scale robot-policy pretraining, while its pretrained $\pi_{0.5}$ instantiation reaches 86.3%, achieving the best overall performance. Experiments on RoboTwin 2.0 and real-world bimanual manipulation further demonstrate strong generalization under visual and spatial shifts.

---

## 17. Latent World Models with Monotone Planning Costs for Image-Goal Navigation

**Authors:** Amirhosein Chahe, Siwei Cai, Lifeng Zhou
**arXiv:** [2608.09073](https://arxiv.org/abs/2608.09073)
**Categories:** Robotics (cs.RO)

Image-goal navigation with latent world models requires not only accurate future prediction, but also a planning cost that reliably ranks candidate action sequences. We define the cost as the cosine distance between the predicted future embedding and the goal embedding, and show that poor cost ordering can mislead sampling-based planners such as Cross-Entropy Method (CEM). To address this, we propose a latent world model built on a frozen DINO-family encoder and train it with two complementary objectives. An autoregressive rollout loss reduces the gap between training and multi-step planning rollouts, while a Monotone Cost Ranking (MCR) loss directly encourages increasingly perturbed action sequences to receive higher planning costs. We also study InfoNCE-based action-contrastive training and find that temporal permutation negatives distort the latent geometry and degrade planning performance. On the GNM navigation dataset, our method outperforms Navigation World Models (NWM), DINO-WM, OmniVLA, and NoMaD, achieving state-of-the-art image-goal navigation performance while reducing orientation error by $2.7\times$ over the same-encoder DINO WM baseline. We also deploy the model zero-shot on a physical robot, where it follows goal-directed paths in unseen indoor and outdoor environments.

---

## 18. SG-WAM: Text-Grounded and Spatial-aware Semantic Guidance for World-Action Models

**Authors:** Junjie He, Junfeng Li, Zhide Zhong, ..., Shunbo Zhou, Haoang Li
**arXiv:** [2608.08839](https://arxiv.org/abs/2608.08839)
**Categories:** Robotics (cs.RO); Computer Vision and Pattern Recognition (cs.CV)

World-Action Models (WAMs) have emerged as a promising paradigm for robotic manipulation. However, most existing WAMs generate future videos and actions by relying mainly on visual cues rather than language instructions, since off-the-shelf text encoders embed instructions independently of visual observations. As a result, the videos predicted by these WAMs are often semantically misaligned with their corresponding language instructions, which degrades the accuracy of the predicted actions. To overcome this limitation, we propose SG-WAM, a semantic guidance method for world-action models that leverages a vision-language model (VLM) as a semantic planner to enhance the instruction-grounding capacity of world-action models. Specifically, we train a VLM-based planner to predict text-grounded and spatial-aware semantic foresight. The text-grounded semantic foresight grounds the instruction by identifying the correct target objects, and the spatial-aware semantic foresight provides the scene geometry for precise manipulation. We then inject this foresight into the world-action model as high-level semantic guidance, ensuring that both future-video generation and action prediction faithfully follow the language instruction. Extensive experiments in simulation and the real world demonstrate the superiority of our semantic guidance method, showcasing precise manipulation and strong instruction-following capabilities.

---

## 19. WA-SpecDec: World-Aware Speculative Decoding for Vision-Language-Action Models

**Authors:** Zikang Wen, Yuning Zhang, Dong Yuan
**arXiv:** [2608.08725](https://arxiv.org/abs/2608.08725)
**Categories:** Robotics (cs.RO)

Vision-language-action (VLA) policies generate robot controls autoregressively, making closed-loop latency dominated by repeated target-model forward passes. Speculative decoding reduces this cost by verifying blocks of draft action tokens in parallel, and recent VLA methods further relax token-level acceptance because small differences in action-token space often map to similar continuous controls. However, this relaxation remains scene-agnostic. A fixed token-distance tolerance treats the same action-token deviation as equally safe across states, although deviations that are harmless in free space can cause collisions or grasp failures near contact. We propose WA-SpecDec, a world-aware speculative decoding framework that injects world-model-derived physical scene awareness during the VLA prefill stage, producing shared world-aware prefill states for draft proposal and target verification without changing the relaxed acceptance rule. Across three state-of-the-art relaxed acceptance schemes, WA-SpecDec preserves higher task success under looser relaxation and enables longer accepted prefixes. At comparable-success operating points, WA-SpecDec achieves a 1.5x matched-success speedup over VLA speculative decoding alone and reduces near-contact failure (NCF) by 18.6% on average relative to the corresponding speculative baselines.

---

## 20. Vid2WAM: Distilling Video Diffusion Priors into World Action Models

**Authors:** Chenhao Qiu, Ruixiang Wang, Runyi Zhao, ..., Yanwei Fu, Simo Wu
**arXiv:** [2608.08558](https://arxiv.org/abs/2608.08558)
**Categories:** Robotics (cs.RO)

World Action Models (WAMs) improve robot policy learning by jointly modeling future visual dynamics and actions. However, their scalability and generalization remain constrained by their reliance on costly expert demonstrations. We challenge this by asking whether future supervision for WAMs must originate from target-task expert trajectories. In this paper, we propose Vid2WAM, an offline distillation framework that transfers visual diffusion priors from a large video foundation model into a compact WAM student. Given an observation and language instruction, Vid2WAM distills supervision through two complementary channels: task-conditioned future rollouts directly supervise the student's future prediction branch, while an inverse dynamics model recovers embodiment-specific pseudo-actions for action learning. To robustly integrate synthetic and real supervision, we introduce source-aware residual action adaptation that learns source-specific corrections around a shared action backbone and mitigates interference from noisy pseudo-actions. During inference, both the video teacher and inverse dynamics model are discarded, leaving only the WAM student for efficient deployment. Simulation and real-world experiments demonstrate that Vid2WAM improves novel-task generalization and data efficiency under limited expert demonstrations while preserving low-latency inference.

---

## 21. SurgWMBench: A Vision-Based Benchmark for World-Modeling Surgical Instrument Motion Planning

**Authors:** Huanrong Liu, Weiliang Huang, Bob Zhang, ..., Chunlin Tian, Qingbiao Li
**arXiv:** [2608.08070](https://arxiv.org/abs/2608.08070)
**Categories:** Robotics (cs.RO)

Reliable surgical planning requires models that move beyond recognizing the current surgical step or imitating expert demonstrations, and instead anticipate how instrument motion reshapes subsequent operative states. Most surgical video understanding methods focus on recognizing phases, actions, or workflow states, while providing limited support for explicitly modeling instrument motion. Conversely, existing tool motion prediction methods can forecast instrument trajectories, but they generally do not capture the coupled evolution of future surgical video states. World models offer a natural framework for jointly modeling visual state transitions and instrument motion dynamics. However, existing surgical world model studies remain largely centered on visual generation quality, relying on generation-oriented metrics such as FVD and CD-FVD. These metrics are poorly aligned with instrument motion planning, as they do not directly measure whether predicted trajectories are geometrically accurate, temporally coherent, or actionable for downstream planning. This limitation is partly structural, since the field lacks public datasets and standardized evaluation protocols that provide the benchmarking infrastructure needed to assess motion-centric capabilities in surgical world models. In this paper, we introduce SurgWMBench, a vision-based benchmark for short-horizon surgical motion planning and dynamics prediction. Given intraoperative image sequences and historical instrument trajectory, SurgWMBench evaluates both near-future instrument motion prediction and stability under continuous rollout or input perturbations.

---

## 22. 4D-WAM: Infusing Spatiotemporal Awareness into World Action Models through Trajectory Fields

**Authors:** Lishan Yang, Wenxuan Song, Xi Wang, ..., Feras Dayoub, Haoang Li
**arXiv:** [2608.08023](https://arxiv.org/abs/2608.08023)
**Categories:** Robotics (cs.RO)

Building on recent advances in world models, World Action Models (WAMs) jointly model video prediction and action generation. However, they typically represent videos in 2D pixel space, creating a representation gap with 3D space in which robotic actions are executed. Recent 3D approaches introduce 3D information, but fail to fully exploit the dynamics of 3D structures. In this work, we propose 4D-WAM, a model-agnostic training strategy that injects spatiotemporal knowledge from 3D trajectory fields into WAMs through representation alignment. To this end, we introduce two complementary objectives: 1) motion alignment, which aligns temporal feature variations across adjacent frames and encourages the model to build local 4D awareness during training, and 2) destination alignment, which guides the model to infer the final destination from the source frame by minimizing the gap between their attention-like similarity distributions. Together, these objectives provide both local motion supervision and long-horizon goal guidance, enabling WAMs to learn trajectory-level spatiotemporal representations. Extensive in-distribution and out-of-distribution experiments across different base models demonstrate the model's improvements in spatial understanding, execution precision, robustness, generalization, and versatility.

---

## 23. GWM-VLA: Geometry-Aware Latent World Modeling for Vision-Language-Action Learning

**Authors:** Yanping Zhao, Hang Yu, Yiwei Wang, ..., Chen Ye, Guang Chen
**arXiv:** [2608.07619](https://arxiv.org/abs/2608.07619)
**Categories:** Robotics (cs.RO)

Vision-Language-Action (VLA) models achieve strong robotic manipulation performance but often degrade under visual and environmental shifts. Latent world modeling offers a promising approach to improving robustness, yet existing methods commonly encode camera views independently and predict holistic scene dynamics without explicitly modeling their geometric relationships. We propose GWM-VLA, a geometry-aware latent world modeling framework for VLA learning. GWM-VLA combines geometry-aware multi-view state encoding, global context-conditioned target-view prediction, and shared latent-action representations grounded by robot-action supervision. Specifically, VGGT-$\Omega$ jointly aggregates multi-view observations at each timestep to construct geometry-aware multi-view states. The latent world model predicts the next-step patch tokens of a selected target view using patch and register tokens obtained after multi-view aggregation, thereby retaining multi-view geometric information without predicting the complete multi-view state. We use the wrist view as the target in our experiments, placing greater emphasis on end-effector motion and local gripper-object interactions. Finally, the shared latent-action representations condition both the latent world model and the flow-matching action head, allowing latent-prediction supervision and ground-truth robot-action supervision to jointly shape the same latent-action representations. Experiments across both simulation and real-world environments demonstrate the effectiveness and robustness of GWM-VLA.

---

## 24. LIRA: Local Cross-Layer Information Routing for Vision-Language-Action Decoding

**Authors:** Zhewei Zhang, Puyue Wang, Guanren Qiao, ..., Hong Jia, Xinhu Zheng
**arXiv:** [2608.07596](https://arxiv.org/abs/2608.07596)
**Categories:** Robotics (cs.RO); Computer Vision and Pattern Recognition (cs.CV)

Vision-Language-Action (VLA) models transform representations from pretrained vision-language models (VLMs) into robot actions, yet the interface that routes intermediate VLM features into action decoders remains underexplored. Existing designs either expose only a narrow part of the representation hierarchy or rigidly match each decoder block to one VLM layer, restricting access to complementary task evidence across depths. We introduce LIRA, a local cross-layer action-conditioning mechanism that formulates VLM-to-action conditioning as depth-aware information routing. LIRA operates on task-token features and LIRA Query features derived from intermediate VLM states, then assigns each Parallel Fusion Block a depth-aligned local window centered on its corresponding VLM layer. Parallel Fusion Blocks aggregate neighboring LIRA Query features and integrate them with task-token features and proprioceptive inputs before action prediction. This routing interface leaves the backbone architecture, action decoder, and supervised training recipe unchanged. Across LIBERO, LIBERO-Plus, CALVIN ABC$\rightarrow$D, and real-world manipulation, LIRA improves the principal aggregate metrics over the VLA-Adapter baseline under the same 0.5B-parameter configuration. In zero-shot transfer to LIBERO-Plus, LIRA increases average success from 59.1% to 78.0%, an 18.9-point gain indicating improved robustness under controlled distribution shifts.

---

## 25. SC$^{2}$-WM: A Self-Correcting World Model with Closed-Loop Feedback for Vision-and-Language Navigation in Continuous Environments

**Authors:** Xuan Yao, Yuze Zhu, Junyu Gao, Zongmeng Wang, Changsheng Xu
**arXiv:** [2608.07548](https://arxiv.org/abs/2608.07548)
**Categories:** Robotics (cs.RO); Computer Vision and Pattern Recognition (cs.CV)

Vision-and-Language Navigation in Continuous Environments (VLN-CE) requires agents to make fine-grained navigation decisions under partial observability. However, most existing methods rely on open-loop execution, lacking mechanisms to detect and correct internal state drift during inference. We propose SC$^{2}$-WM, a self-correcting world model framework that introduces internal feedback for closed-loop decision making in VLN-CE. Our method derives feedback from world-model foresight to perform state-level plan refinement before action execution. To handle challenging scenarios, we further introduce conditional world-aware adaptation, which enables model-level correction by selectively updating the world model at test time when feedback indicates model capacity insufficiency. Experiments on standard VLN-CE benchmarks demonstrate improved navigation robustness and generalization. Our code is available at this https URL.

---

## 26. Learning How the World Evolves: Extrapolative Video World Models via Latent Dynamics Reasoning

**Authors:** Haodong Li, Shaoteng Liu, Tianyu Wang, ..., Zhe Lin, Manmohan Chandraker
**arXiv:** [2608.09926](https://arxiv.org/abs/2608.09926)
**Categories:** Computer Vision and Pattern Recognition (cs.CV)

The world evolves following its dynamics, i.e., its laws of motion. However, leading video diffusion models largely fit the pixels without modeling how the pixels transit over time. Thus, they render visually plausible frames but may not accurately obey the laws. To capture the dynamics purely from pixels, we introduce Latent Dynamics Reasoning (LDR). LDR casts the latent transition as an explicit kinematic integration, where the lower-order dynamics are integrated numerically and the model regresses only the third- and higher-order residual that drives the rollout. For this integration to extrapolate better, LDR runs it on a structured latent rather than dense convolutional features. Following PhyWorld, we validate LDR on a controlled white-box physics benchmark spanning five tasks (uniform motion, parabola, collision, bouncing, looming), focusing on out-of-distribution scenarios that reveal whether a model has truly learned the underlying dynamics. LDR extrapolates the learned dynamics far better: the gap between its in- and out-of-distribution error is over 20$\times$ smaller than the video diffusion baseline's, under both single- and joint-task training at 256$^2$ resolution, while using 26$\times$ fewer parameters and running 143$\times$ faster. LDR can even generalize under severe shift: for example, trained only on red balls moving left-to-right, it correctly predicts the motion of a blue square moving right-to-left. To our knowledge, this is the first video world model that extrapolates learned dynamics beyond its training distribution. Project page: this https URL

---

## 27. World Tokens: Enhancing Embodied Policies with Training-Time World Modeling

**Authors:** Qu Tang, Benhui Zhuang, Bo Yuan, ..., Longteng Guo, Junlan Feng
**arXiv:** [2608.09730](https://arxiv.org/abs/2608.09730)
**Categories:** Computer Vision and Pattern Recognition (cs.CV)

Vision-language-action (VLA) models are a widely adopted paradigm for embodied policies. They excel at efficient closed-loop control but do not explicitly model how physical scenes evolve as a task unfolds. Recently emerging world-action models (WAMs) leverage pretrained video world models to capture spatiotemporal evolution, yet retaining future generation or a large video backbone in the control loop substantially increases inference cost. We introduce World Tokens, an embodied policy architecture built around a World Adapter that bridges visual-language understanding, world-dynamics modeling, and action generation. It uses world modeling during training to enhance the action policy while preserving efficient deployment. Specifically, the World Adapter transforms VLM features into a fixed set of world tokens, which condition a jointly fine-tuned future-video denoiser and simultaneously serve as the action expert's sole visual-language context. This shared conditioning allows gradients from future-video denoising to directly shape the representation used for action prediction, while exclusive routing prevents the policy from bypassing that representation. At deployment, the world-model branch is removed, leaving only the VLM, World Adapter, and action expert, with no online video-model inference. With a 2B backbone and no embodied action pretraining, World Tokens is highly competitive on LIBERO, attains the best reported averages on SIMPLER, substantially improves real-world R1 Pro success over a matched action-only baseline, and generates each action chunk at VLA-level latency.

---

## 28. Sekai2: From World Exploration to Interactive World Modeling

**Authors:** Kang He, Wenshuo Peng, Zihui Gao, ..., Kaipeng Zhang, Yongtao Ge
**arXiv:** [2608.09449](https://arxiv.org/abs/2608.09449)
**Categories:** Computer Vision and Pattern Recognition (cs.CV)

Video world models must capture how scenes evolve over time and across viewpoints. Training them for long-horizon generation and camera control therefore benefits from long videos paired with camera trajectories and temporally grounded semantics. Existing corpora rarely offer the three together: large-scale web video provides broad visual diversity but no trajectories or time-aligned text, while pose-annotated datasets are typically short-range or reconstruction-oriented. We introduce Sekai2, a multi-source real-world video dataset that carries the world-exploration footage of Sekai toward interactive world modeling. The release contains 128,892 clips totaling 2,826 hours from 10,428 source videos across 113 countries or regions, and is deliberately weighted toward sustained observation: under a common 120-second decomposition, 43,594 segments reach the full two minutes and account for 51.4% of all footage. Every clip includes a released camera trajectory and hierarchical annotations disentangling subject motion, environment dynamics, static scene content, and camera behavior, resulting in 649,597 temporally grounded segments. Crucially, we further introduce 982 panoramic sequences captured along non-linear trajectories with loops and revisits. These revisits provide repeated observations of the same locations across time and viewpoints, offering essential supervision for learning persistent scene representations, long-term spatial memory, and geometrically consistent world models. Corpus-scale analyses demonstrate complete pose-and-caption coverage, broad geographic and semantic diversity, varied camera trajectories, and highly non-redundant temporal descriptions. Together, these properties make Sekai2 a scalable resource for long-horizon video generation, camera-controllable synthesis, and interactive world-model pre-training.

---

## 29. Distilling Physical Priors into Streaming World Models

**Authors:** Liangliang Zhao, Junying Wang, Danni Yang, ..., Bowen Zhou, Yihao Liu
**arXiv:** [2608.07981](https://arxiv.org/abs/2608.07981)
**Categories:** Computer Vision and Pattern Recognition (cs.CV)

Streaming world models predict future visual states online while maintaining physically coherent dynamics over long horizons. However, their rollouts often violate basic physical constraints. A common approach distills pretrained bidirectional DiTs into few-step causal generators. However, this paradigm suffers from two fundamental limitations: generic bidirectional teachers acquire limited physical priors from visually oriented pretraining, and the limited priors suffer further loss during bidirectional-to-causal distillation. We present PhyS, a three-stage framework for distilling physical priors into streaming world models. To acquire physical priors from real-world interactions, we construct PhyS-120K, a dataset of 120K real-world physical-interaction videos spanning rigid-body dynamics, soft-body deformation, fluid phenomena, and phase transitions. Each video is annotated with structured descriptions of object properties and causal state transitions. Physics-aware supervised fine-tuning injects the physical priors into a bidirectional 14B DiT teacher, which we then distill into a lightweight 1.3B causal DiT for few-step autoregressive streaming generation. Finally, we use online reinforcement learning to incentivize the distilled model to generate physically plausible rollouts and further propose Temporal Credit Routing (TCR) to address temporal credit assignment. TCR evaluates physical consistency over overlapping temporal windows and routes the resulting group-relative advantages to temporally aligned denoising actions. On PhysicsIQ, PhyS improves the Wan2.1-14B teacher by 18.2\% and the Self Forcing, Rolling Forcing, and Causal Forcing by 23.7\%, 14.8\%, and 31.4\%, respectively. Results also improve the physics-aware video benchmarks VideoPhy, VideoPhy2, and PhyGenBench. The dataset, code, and more sample videos are available on our Project Page.

---
