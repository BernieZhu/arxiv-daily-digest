# arXiv Daily Digest — 2026-09-25

**Mode:** direct
**Categories:** cs.AI, cs.LG, cs.RO, cs.CV
**Keywords:** VLA, RSI, agentic robot, self-improving robot, self-evolving robot, robot harness
**Papers found:** 7

---

## 1. Breaking the Environment Wall: Evolving LLM Agent Environments for Recursive Self-Improvement

**Authors:** Yukai Wu, Yuanjing Yang, Le Zhou, ..., Xuanhe Zhou, Fan Wu
**arXiv:** [2609.29773](https://arxiv.org/abs/2609.29773)
**Categories:** Artificial Intelligence (cs.AI)

Many real-world tasks (e.g., office workflows, scientific experimentation) require LLM agents to interact repeatedly with their environments for context-dependent operations. However, such environments are often not agent-ready. First, information is often scattered and fragmented across the environment. Second, relevant evidence in the environment is often mixed with misleading information and conflicting versions. Third, environments evolve over time, introducing new noise and more challenging tasks. These challenges can substantially degrade performance for state-of-the-art AI agents (e.g., from 83.9% to 57.6%). To address these challenges, we propose Env-Rethink (a system with 27B post-trained model) that supports three main capabilities: (1) It adaptively builds Collection Maps (for organizing related files) and Event Logs (for contextualizing cross-data relationships) to supplement necessary context; (2) It further leverages the post-trained model (through offline trajectory learning) to identify underlying noise issues in the environment; (3) It ultimately evolves environments through virtual event histories that alter environmental states and evidence relationships, producing more tricky ones for further agent improvement. Experiments show that Env-Rethink can effectively improve downstream task performance (with over 15.1% rubric pass rate improvement across nine models on 30 tasks).

---

## 2. Decoupled Early Exits for Task-Dependent Compute Allocation in Flow-Matching VLAs

**Authors:** Riccardo Andrea Izzo, Rimvydas Rubavicius, Gianluca Bardaro, ..., Matteo Matteucci, Alessandro Suglia
**arXiv:** [2609.29382](https://arxiv.org/abs/2609.29382)
**Categories:** Robotics (cs.RO); Machine Learning (cs.LG)

Flow-matching Vision-Language-Action (VLA) models have emerged as a potential solution for generalist robot control, designed by combining a pretrained Vision-Language Model (VLM) backbone with an action expert that generates continuous robot actions. While these models exhibit impressive capabilities, due to their very high number of parameters, their computational requirements are often prohibitive for robotics control. To mitigate these inefficiencies, existing methods predominantly skip VLM backbone layers with early exits or reduce denoising steps, while leaving action expert depth untouched. We propose a framework that exposes backbone depth $V$, action expert depth $A$, and denoising steps $D$ as three jointly configurable compute axes in a VLA. Starting from a pretrained VLA, we attach lightweight Exit Transformers (ET) at intermediate depths in both the backbone and the action expert, trained to distil the last layer of the policy into each exit. Furthermore, we introduce a KV Cache synthesis mechanism that manages the missing keys and values of the skipped backbone layers, allowing the action expert to exit deeper than the backbone. Finally, we show that the optimal compute budget is task-dependent, with different tasks benefiting from different axes and depths. Notably, our method does not require training the original policy from scratch, and for each exit, it increases the number of parameters by only $2.1\%$ for SmolVLA and $4.1\%$ for $\pi_{0.5}$. We validate our approach across two flow-matching VLAs (SmolVLA, $\pi_{0.5}$) and two benchmarks (LIBERO, Meta-World), revealing complementary effects: $V$ and $A$ respectively reduce FLOPs and latency, while $D$ improves both. Our joint configurations $(V,A,D)$ reduce latency by $79.2\%$ and computation (FLOPs) by $31.8\%$, while improving mean success rate by $5.6\%$.

---

## 3. Uncertainty-Gated Exploration Noise Suppresses Task Collapse in Online RL Fine-Tuning of a Flow-Matching Vision-Language-Action Policy

**Authors:** Mehmet Turan Yardımcı, Yunus Emre Çoğurcu
**arXiv:** [2609.28838](https://arxiv.org/abs/2609.28838)
**Categories:** Robotics (cs.RO); Machine Learning (cs.LG)

Online reinforcement learning fine-tuning of pretrained flow-matching vision-language-action (VLA) policies promises robots that keep learning after deployment, but continued updates often destroy competence on individual tasks while the aggregate still looks healthy. We study this failure mode, which we call task collapse, under a matched small-compute budget on LIBERO-10 with a 450M-parameter SmolVLA policy trained by PPO with stochastic (SDE) sampling. Three exploration-noise policies differ in one live variable: a fixed noise scale, a ReinFlow-style learned noise network, and an uncertainty-gated controller that redistributes exploration across task streams from task-agnostic novelty and competence signals, without task labels or episode boundaries. Under the pooled definition, fixed noise collapses tasks in two of three seeds and learned noise in every seed measured to iteration 200, while the controller collapses none in any of its three seeds. Measured parameter displacement shows the controller's action expert keeps changing, while its mean applied noise is close to the fixed scale in the available logs. The matched comparison supports the controller's effect on task preservation; the separate contributions of its adaptation across states and over time are not disentangled. A lower fixed scale slows the decline but does not stop it. No arm improves on the behavior-cloning baseline in this budget. Two properties of that regime are measured beside this result, not offered as its cause: following the reference recipe, training runs in bfloat16 with no fp32 master copy, under which 96.02% of the action expert's elements stay bit-identical across three consecutive iterations, and an fp32 master copy at the reference learning rate collapses both arms in a single-seed observation. We release tools measuring per-task collapse under four definitions, rescoring noise and instrument tares.

---

## 4. Self-Adaptive VLA for Robust Robot Deployment

**Authors:** Hongxin Zhang, Chunru Lin, Tsun-Hsuan Wang, Zhenjia Xu, Chuang Gan
**arXiv:** [2609.30092](https://arxiv.org/abs/2609.30092)
**Categories:** Robotics (cs.RO); Computer Vision and Pattern Recognition (cs.CV)

While Vision-Language-Action (VLA) models demonstrate impressive capabilities in robotic manipulation, their memoryless nature renders them brittle to test-time environment shifts, particularly hardware shifts caused by wear or imperfect calibration. Enabling these models to self-adapt during deployment without requiring continuous on-site recalibration remains a critical bottleneck for real-world scalability. In this work, we introduce Self-Adaptive VLA, a novel post-training recipe that enables the policy to iteratively adapt to deployment-time hardware shifts leveraging its own rollouts as context. To do so, we first collect policy rollouts under deliberately injected hardware shifts. We then transform the base policy's training data into shift-conditioned expert demonstrations by pre-compensating the expert actions for these known shifts. Next, we introduce a lightweight, plug-in context encoder that compresses the context, including visual observation, proprioception, and actions in the shifted environment, into a latent context token. This token modulates the policy through adaptive layer normalization (AdaLN). Furthermore, we find that context tokens can be ensembled, allowing the policy to iteratively self-correct and mitigate failures step by step. Extensive experiments across four precision-critical bi-manual and dexterous manipulation tasks show that Self-Adaptive VLA recovers over 80% of the base policy's performance under hardware shifts, such as actuation bias and joint encoder offsets. Moreover, Self-Adaptive VLA enables more robust deployment to new workstations compared to the base policy. Our approach provides a pathway for robust large-scale real-world robot deployments and easier maintenance. See videos at this https URL.

---

## 5. AdaHVLA: Adaptive Harnesses for Long-Horizon Vision-Language-Action Execution

**Authors:** Junyi Tang, Jie Peng, Zezhen Ding, Yuan Shen, Tianlong Chen
**arXiv:** [2609.29204](https://arxiv.org/abs/2609.29204)
**Categories:** Robotics (cs.RO)

Vision-language-action (VLA) models offer strong local control and instruction following but often struggle with long-horizon tasks requiring persistent memory and planning. Task harnesses provide persistent context for agent reasoning by retaining task history and tracking progress across execution stages. To bring these complementary capabilities together, we introduce AdaHVLA, an adaptive harness that refines code-based coordination policies through robot experience to better align agent reasoning and memory with VLA execution. Its decoupled multiagent adaptation process separates evidence analysis, harness revision, and behavioral assessment into distinct working contexts, using testable coordination hypotheses to guide revisions and subsequent rollouts to assess their predicted effects. A stateful revision graph links execution evidence, hypotheses, revisions, and observed effects, preserving alternative harnesses and adaptation memory to guide refinement across repeated attempts and continued adaptation across tasks and environments. In simulation, AdaHVLA raises mean test success on NaVILA-LH from 22.5\% to as high as 57.5\% and improves manipulation test success across three VLA backbones by up to 30.8 percentage points over the initial harness. Real-world deployment further illustrates how the adapted policies support stable execution across task stages.

---

## 6. Know Your Body: A Harness for Direct and Self-Improving Robot Control with VLMs

**Authors:** Zeyu Lou, Yanhong Zeng, Yong Wang, Chenyang Si
**arXiv:** [2609.28530](https://arxiv.org/abs/2609.28530)
**Categories:** Robotics (cs.RO)

A general-purpose vision-language model can understand a task goal without knowing how a particular robot's motion and functional parts produce the intended effect. We introduce KnowBody, a harness that makes these action-relevant body relations explicit, queryable, and revisable while keeping the model weights frozen. Initialized from one off-task trajectory, a partial body model guides action selection and the interpretation of past interactions. New evidence refines the model, and knowledge dependent on revised body estimates is rechecked before reuse. Across 32 fixed-budget trials on four real-robot tasks, initialized KnowBody achieves 75% completion versus 25% for the native harness and requires fewer planner rounds on successful trials in tasks completed by both. With persistent updates enabled, planner rounds decrease by 29-53% from the first to the fifth recorded success.

---

## 7. Direction-Scale Decomposition in Action Representation: Rethinking What to Tokenize for Vision-Language-Action Models

**Authors:** Yufei Duan, Hang Yin, Alberta Longhini, Chao Tang, Danica Kragic
**arXiv:** [2609.28865](https://arxiv.org/abs/2609.28865)
**Categories:** Computer Vision and Pattern Recognition (cs.CV); Robotics (cs.RO)

Action representation plays a central role in discrete-token vision-language-action (VLA) learning but remains underexamined. Under conventional pose-increment representations, action tokens are sensitive to execution speed and dataset-specific normalization, potentially obscuring geometric structure shared across demonstrations and datasets. We introduce Direction-Scale Decomposition (DSD), an action representation that decomposes translation and rotation increments into direction and scale components before tokenization. DSD isolates motion direction while retaining magnitudes in separate scale channels. We evaluate DSD with uniform binning (BIN) and BEAST, a B-spline-based tokenizer, in simulation and real-world manipulation under both single-dataset and mixed-dataset training. On LIBERO, DSD improves average success rates with both tokenizers. On SimplerEnv, DSD-BIN outperforms BIN by 10.3 percentage points in overall success rate under mixed-dataset training. Real-robot experiments further show gains both with and without robotics pretraining. These results support DSD as an effective action representation for discrete-token VLA models and suggest its potential to mitigate performance degradation when training on large and diverse dataset mixtures. Our project page with additional resources is available at this https URL

---
