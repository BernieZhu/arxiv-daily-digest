# arXiv Daily Digest — 2026-11-13

**Mode:** direct
**Categories:** cs.AI, cs.LG, cs.RO, cs.CV
**Keywords:** VLA, RSI, agentic robot, self-improving robot, self-evolving robot, robot harness
**Papers found:** 7

---

## 1. RSI-PDEbench: A Benchmark for Self-Improving Agents in PDE Solving

**Authors:** Binghang Lu, Lang Cao, Changhong Mou, ..., Na Lu, Guang Lin
**arXiv:** [2611.14949](https://arxiv.org/abs/2611.14949)
**Categories:** Artificial Intelligence (cs.AI)

Identifying and solving partial differential equations (PDEs) from sampled solution data often requires substantial expert effort in equation discovery, coefficient estimation, and numerical solver configuration, especially under noise and distribution shifts. Can large language model (LLM) agents automate this workflow accurately and efficiently? To investigate this question, we introduce \bench{}, a benchmark of 1,001 cases spanning 42 equation templates, including both classical and fractional PDEs. It provides three evaluation settings: Full evaluates performance on noise-free solution data; Noisy tests robustness to Gaussian noise with an RMS equal to 50\% of the clean-signal RMS; and Hard-OOD tests challenging out-of-distribution generalization to unseen equation templates and shifted coefficient ranges. We further introduce RSI-PDE, a recursively self-improving agent harness that shortlists candidate equations by residual loss, uses relative $L^2$ feedback to refine coefficients and numerical solvers, and applies a validation gate to policy and memory updates. We compare RSI-PDE with single-run baselines and native agent harnesses (Claude Code or Codex) across four frontier models. Across the three settings, RSI-PDE improves the pass rate averaged across the four models by 106.5--181.9\% relative to single-run baselines and by 3.0--19.6\% relative to native harnesses, while reducing total recorded model calls by 46.9\% across the 12 model--setting pairs. These results highlight the potential of validated recursive self-improvement in LLM agents to advance scientific computing.

---

## 2. Learning Low-Latency Action Verification for Frozen Vision-Language-Action Models

**Authors:** Wen-Han Hsieh, Ken Jiankun Zheng, Chia-Chien Chen, David M. Chan, Trevor Darrell
**arXiv:** [2611.14834](https://arxiv.org/abs/2611.14834)
**Categories:** Robotics (cs.RO); Artificial Intelligence (cs.AI); Computer Vision and Pattern Recognition (cs.CV)

Vision-language-action (VLA) models have made significant progress in general-purpose robotic manipulation. However, sampled action sequences can be ineffective, while evaluating alternatives with computationally expensive verifiers adds latency at each policy query. In this work, we propose HDH, a lightweight framework that uses hindsight from a frozen VLA's own deployments to improve action verification. The framework has three stages. First, we deploy the policy and collect its autonomous rollouts. We then train a compact action verifier to assign each action chunk a predicted task-success score. Finally, the frozen VLA generates action candidates, and the verifier selects the candidate with the highest score for execution. Across four LIBERO-10 tasks, HDH achieves an average success rate of 82.3\% and on three real-world manipulation tasks, HDH improves average success over the baseline policy by 22.6\%.

---

## 3. Experience-Handoff Reinforcement Learning for Recursive Self-Improvement

**Authors:** Doyoung Kim, Byeongguk Jeon, Kailin Zhang, Sherry Yang
**arXiv:** [2611.16409](https://arxiv.org/abs/2611.16409)
**Categories:** Machine Learning (cs.LG); Computation and Language (cs.CL)

It is common to train Large Language Models (LLMs) for agentic tasks with Reinforcement Learning (RL) from scalar rewards. However, this throws away the fine-grained information about the environment that the agent experienced during the trial (e.g., error logs). To utilize this rich information, recent works wrap the agent in a harness that refines its own inputs through reflection or compaction and hands past experience to future rollouts, but the construction of the handed-off artifacts (e.g., a playbook) is itself not learned. We want the best of both worlds: gradient updates from a scalar reward, while also utilizing environment information to hand off experience. As a concrete testbed, we fix the Agentic Context Engineering (\ace{}) harness and train one model to act, reflect, and curate task-local playbooks. Our method, \acerl{}, evaluates candidate experience-handoff artifacts by their downstream effect on future actor rollouts, and co-optimizes the role-specific behaviors (action generator, insight reflector, and playbook curator) under a fixed scaffold. Across agentic benchmarks, \acerl{} achieves higher held-out performance than baseline methods. The results suggest that agent training should optimize not only the actions in the current rollout, but also the model-written experience that future rollouts inherit.

---

## 4. What Can a VLA Learn from the Agent That Calls It? Task-Level Experience Distillation for Embodied Navigation

**Authors:** Jinze Tao, Yuxiao Han, Kangkang Dong, ..., Bokui Chen, Houde Liu
**arXiv:** [2611.16246](https://arxiv.org/abs/2611.16246)
**Categories:** Robotics (cs.RO); Machine Learning (cs.LG)

Navigation agents use a large language model (LLM) planner to call a vision-language-action (VLA) model. Each episode needs the LLM, adding cost and delay. We distill successful agent experience into the VLA instead of distilling the planner. The VLA then navigates alone at test time. Agent sessions are not VLA demonstrations. They include motions driven by planner tools and sub-instructions, along with detours. We present H2E, a task-level experience distillation method that converts these sessions into VLA training data. Every motion becomes a VLA action under the original task instruction, with the resulting poses as targets. H2E masks the loss on steps that move away from the goal. It labels every visited state within 1 m of the goal as a stop. We then update the VLA with low-rank adaptation. The VLA learns to stop at the goal and find goals the base model never reaches. On all 3,189 REVERIE-CE val-unseen episodes, H2E raises the success rate of an 8B VLA from 35.0% to 44.9%.

---

## 5. What Makes a VLA Reactive? A Study of Execution Strategies for Dynamic Manipulation

**Authors:** Zhuoyue Li, Zhendong Han, Pankhuri Vanjani, Wenting Li, Rudolf Lioutikov
**arXiv:** [2611.15491](https://arxiv.org/abs/2611.15491)
**Categories:** Robotics (cs.RO); Computer Vision and Pattern Recognition (cs.CV); Machine Learning (cs.LG)

Vision-language-action (VLA) models predict chunks of future actions, and when objects move, those chunks go stale before they are executed. We study what makes a pretrained VLA reactive, using \pihalf{} on two dynamic simulation benchmarks and three real-robot tasks. We vary the prediction and execution horizons, compare synchronous and asynchronous inference, test methods that deliver actions sooner or keep successive chunks continuous, and adapt the policy with motion cues and latent-space reinforcement learning. The best prediction horizon is about one second, and the best execution horizon depends on the checkpoint. Short horizons help more with asynchronous execution, and methods that keep the trajectory continuous outperform those that only reduce latency. Adapting the policy repairs targeted failures, but on the conveyor task changing the execution horizon gained as much. Reactivity depends on the execution pipeline as much as on the policy, so both should be evaluated together.

---

## 6. STVLA: Spatial-aware and Temporal-memory forVision-Language-Action Models

**Authors:** Zhuo Han, Yeqiang Wang, Xinran Wang, ..., Wei Shan, Maoqing Yao
**arXiv:** [2611.16589](https://arxiv.org/abs/2611.16589)
**Categories:** Robotics (cs.RO)

Robotic manipulation often requires both spatial scene understanding and task history. However, many vision-language-action (VLA) policies rely primarily on current observations, without explicitly integrating spatial structure and task history. Appearance-based memories can be sensitive to occlusion and viewpoint changes, while spatial representations of the current scene alone do not preserve how the scene has changed during task execution. We introduce STVLA, a framework that incorporates features from a pretrained visual geometry foundation model into temporal memory alongside visual representations. This allows the policy to recall past scene structure as context for current action decisions. To select informative history, STVLA uses a mathematically grounded scoring rule that balances relevance to the current observation with complementary evidence from memory. Across evaluations on LIBERO, LIBERO-Mem, MIKASA-Robo, and SimplerEnv Bridge, STVLA achieves the highest average success rate among the compared methods on each benchmark. On real-world block stacking, object organization, and phone packaging, it improves success over $\pi_{0.5}$ by $58.33$, $30.00$, and $35.00$ percentage points, respectively. These results support integrating scene geometry into temporal memory to improve manipulation requiring both spatial precision and task history. Project website: \href{this https URL}{this https URL}

---

## 7. Scaling VLA Serving Under Robotic Execution Constraints

**Authors:** Yue Zhang, Zicong Ye, Lufang Chen, ..., Ruyi Gan, Hao Wang
**arXiv:** [2611.14969](https://arxiv.org/abs/2611.14969)
**Categories:** Robotics (cs.RO); Distributed, Parallel, and Cluster Computing (cs.DC)

Vision-language-action (VLA) models have emerged as a promising paradigm for general-purpose robotic manipulation. In our production setting, hundreds of VLA-powered robots are already operating in real-world environments, creating an immediate need for efficient fleet serving. We present XInfer, a production-deployed VLA serving system designed to reduce the inference infrastructure cost of large-scale robotic deployments. XInfer jointly coordinates heterogeneous VLA computation with the evolving response requirements of robotic execution. By exploiting computational parallelism while managing interference, XInfer improves GPU efficiency while protecting time-critical robotic feedback. We evaluate XInfer across three VLA models using production-derived workloads, achieving 1.26-3.75 times the effective robot capacity (ERC) of state-of-the-art systems under physical-execution constraints. Our implementation is publicly available at this https URL.

---
