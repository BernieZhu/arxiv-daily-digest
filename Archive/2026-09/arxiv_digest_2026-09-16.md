# arXiv Daily Digest — 2026-09-16

**Mode:** direct
**Categories:** cs.AI, cs.LG, cs.RO, cs.CV
**Keywords:** VLA, RSI, agentic robot, self-improving robot, self-evolving robot, robot harness
**Papers found:** 6

---

## 1. ScienceBuddy: Recursive-in-Recursive Self-Improvement for Interactive Scientific Agents

**Authors:** Shuhan Xue, Jianyuan Zhong, Ziyuan Nan, ..., Yingcheng Wu, Ling Yang
**arXiv:** [2609.17523](https://arxiv.org/abs/2609.17523)
**Categories:** Artificial Intelligence (cs.AI); Computation and Language (cs.CL)

We introduce and release ScienceBuddy, an interactive scientific research workspace that brings continually improving scientific agents into researchers' everyday workflows. ScienceBuddy supports researchers in carrying out scientific tasks while transforming their requests, feedback, and execution evidence into tasks and evaluation rubrics for continual learning. At its core is recursive-in-recursive self-improvement, a paradigm that couples harness evolution with model reinforcement learning: the inner recursion improves the harness with the model fixed, while the outer recursion trains the model under the improved harness. Harness evolution shapes training experience, and model learning creates new opportunities for harness adaptation. We present case studies of researcher interaction, harness refinement, and model learning, with the benchmark cases spanning four scientific task families. By releasing ScienceBuddy as a research product, we make this paradigm available to the scientific community and take a step toward discovery intelligence: scientific AI that advances through sustained collaboration with researchers and evolves alongside the research it supports. Website: this http URL

---

## 2. FluxVLA Engine: A One-Stop VLA Engineering Platform for Embodied Intelligence

**Authors:** Yinhao Li, Weixin Mao, Zihan Lan, ..., Chengqi Shi, Hua Chen
**arXiv:** [2609.17210](https://arxiv.org/abs/2609.17210)
**Categories:** Robotics (cs.RO); Artificial Intelligence (cs.AI)

Vision-language-action (VLA) models, world-action models (WAMs), and offline reinforcement learning methods are rapidly expanding the design space of embodied policies, yet turning these algorithms into reliable robot systems remains constrained by fragmented data formats, training stacks, evaluation protocols, inference runtimes, and embodiment-specific interfaces. We present $\mathrm{FluxVLA}$ Engine, an open, configuration-driven platform that turns heterogeneous embodied-policy components into a reproducible data-to-deployment workflow. Rather than introducing another policy model, $\mathrm{FluxVLA}$ standardizes interfaces for datasets, visual-language and world models, action heads, reward- or advantage-weighted learning, distributed training, simulation evaluation, optimized inference, and robot operators. The engine further integrates compositional dual-arm simulation, scalable automatic data generation, and model-decoupled human-in-the-loop rollout, takeover, correction collection, and reward annotation. For responsive physical execution, it combines Real-Time Chunking (RTC) with accelerated inference backends, lightweight remote GPU serving, and configurable trajectory post-processing. Together, these capabilities connect offline learning, simulation validation, online correction, and real-robot execution through shared and auditable contracts. $\mathrm{FluxVLA}$ therefore targets the engineering bottlenecks separating promising embodied-learning algorithms from reproducible evaluation and dependable deployment. Code is available at this https URL

---

## 3. Intrinsic Robot Rewarding: Reusing VLA Representations for Autonomous Evaluation and Policy Improvement

**Authors:** Tobias Schaffer, Mohab Elkhayat, Daniela Nicklas, Mustafa Almohamad, Elham Al-Fuqara
**arXiv:** [2609.17115](https://arxiv.org/abs/2609.17115)
**Categories:** Robotics (cs.RO); Machine Learning (cs.LG)

Vision-language-action (VLA) systems already bring together two valuable resources for robot learning: rich visual representations and demonstrations of successful task execution. Intrinsic Robot Rewarding (IRR) proposes to use these resources for a second, complementary purpose: evaluating the robot's own outcomes and providing feedback for policy improvement. Successful demonstration endpoints define task-specific references, and the policy's frozen visual encoder provides the feature space in which new outcomes are assessed. The core reward mechanism adds a reference bank and a scoring operation to the existing pipeline, without requiring a separate learned evaluator or an additional perception backbone. Our position is that this reuse offers a promising route to lower integration effort, efficient reward computation, and reduced recurring human outcome scoring. Building on established research in visual rewards and learning from experience, IRR brings these ideas into the robot's existing perception and demonstration pipeline. An operational COMAU Racer 3 demonstrator is available at technology readiness level 4 (TRL 4). This laboratory foundation supports the next research step: connecting internal outcome evaluation to physical policy improvement. We present the reward formulation, central research questions, and an evaluation methodology linking reward reliability to task success and supervision effort. The intended contribution is a reusable approach to learn and improve from the data and experience already available in industrial robot systems.

---

## 4. SAVLA: Symmetry-Aware Vision-Language-Action Models for Robotic Manipulation

**Authors:** Junle Li, Weixian Waylon Li, Fuxiang Wu, Fusheng Hao, Fengxiang He
**arXiv:** [2609.16641](https://arxiv.org/abs/2609.16641)
**Categories:** Robotics (cs.RO)

Vision-language-action (VLA) models have become the dominant paradigm for language-conditioned robot manipulation. However, although images and language instructions inherently encode geometric information, VLAs acquire their spatial competence purely from demonstrations. As a result, they are reliable only within the range of scene poses that the demonstrations cover. We propose SAVLA, an end-to-end symmetry-aware VLA model for robust and data-efficient policy learning. Our approach keeps the pretrained vision-language backbone entirely frozen while combining it with an equivariant flow-matching action head and a learned canonicalizer. The head decomposes its state, action, and conditioning inputs into invariant and equivariant channels, and preserves this typing throughout all of its layers. The canonicalizer transforms oblique-view images into a canonical frame and rotates the geometric conditions consistently. We evaluate our model on LIBERO. Compared with the GR00T N1.5 baseline, SAVLA improves the success rate averaged over all four LIBERO suites by 5.1 points and increases the mean success rate under rotation on LIBERO-Goal from 41.5% to 90.4%.

---

## 5. Dense to MoE Adaptation for Compact Vision Language Action Policies

**Authors:** Muchun Niu, Shuang Chen, Yuzhou Wu, Linfeng Zhang
**arXiv:** [2609.16503](https://arxiv.org/abs/2609.16503)
**Categories:** Robotics (cs.RO)

Vision language action (VLA) policies continue to grow in parameter count, making deployment on resource-constrained robot platforms difficult. The central goal is to reduce the number of LLM-side parameters retained in the deployed policy while preserving downstream task performance. Our approach, AdaDE, adapts selected dense feed forward blocks into mixture of experts (MoE) layers and derives expert retention masks from router statistics during fine tuning. The Dense2MoE conversion preserves the original dense FFN function at initialization, so expert deactivation can start without a separate recovery stage. Instead of using a fixed shutdown rule, expert masks are updated dynamically from router usage statistics, with staged training and expert protection to avoid early collapse. With 40% of the LLM parameters deactivated, AdaDE retains 95.1% average success in LIBERO and 42.0% average success across all 50 RobotWin2.0 tasks. These results suggest that dense to MoE adaptation with dynamic expert deactivation is a practical direction for reducing active VLA model size without severe performance loss.

---

## 6. sensVLA: Spatially-Grounded Vision-Language-Action Model for Autonomous Wheel Loader

**Authors:** Gopi Krishna Erabati, Bjarne Johannsen, Angus Stewart, Vardeep Singh Sandhu
**arXiv:** [2609.17021](https://arxiv.org/abs/2609.17021)
**Categories:** Computer Vision and Pattern Recognition (cs.CV); Robotics (cs.RO)

Autonomous wheel-loader control requires joint reasoning over task semantics, egocentric vision, proprioception, and 3D scene geometry. We present sensVLA, a Vision-Language-Action (VLA) architecture that combines a Qwen3-2B Vision-Language Model (VLM) with a fully trainable transformer action expert trained by flow-matching velocity regression. sensVLA routes Bird's-Eye-View (BEV) features, extracted from fused front and rear lidar, directly to the action expert through a dedicated cross-attention pathway, while the VLM consumes front and rear RGB views to provide task-conditioned semantic context. This design decouples spatial grounding from linguistic reasoning while preserving interaction between both streams at decision time. The expert predicts six action dimensions: longitudinal velocity, steering, body-frame displacement, arm rate, and bucket rate. On a real-world dataset from a wheel loader, sensVLA reaches aggregate per-step parity with a strong camera-only baseline and reduces longitudinal velocity RMSE by 28% and displacement error by 9% on loading centric scenarios. It also degrades 29% less when the camera stream is corrupted or removed, evidencing that explicit spatial grounding improves accuracy and fault-tolerance for heavy equipment autonomy.

---
