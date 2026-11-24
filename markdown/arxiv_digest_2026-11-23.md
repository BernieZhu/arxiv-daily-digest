# arXiv Daily Digest — 2026-11-23

**Mode:** direct
**Categories:** cs.AI, cs.LG, cs.RO, cs.CV
**Keywords:** VLA, RSI, agentic robot, self-improving robot, self-evolving robot, robot harness
**Papers found:** 10

---

## 1. Search-RSI: Expanding Search Worlds Along Multimodal Agents' Capability Frontier

**Authors:** Chengchao Lv, Yin Wang, Chunzheng Zhu, Wanli Chang
**arXiv:** [2611.27780](https://arxiv.org/abs/2611.27780)
**Categories:** Computer Vision and Pattern Recognition (cs.CV); Artificial Intelligence (cs.AI)

Multimodal search agents answer knowledge intensive visual questions by grounding them in retrieved evidence, and recent recipes train them on multi hop tasks that are synthesized from knowledge graphs and grown online to keep pace with the agent. These recipes, however, treat the searchable world as fixed: a new question can be well formed and verifiable while its evidence is absent from the retrieval backend, so the agent issues the right query, retrieves nothing, and is penalized as if its policy were at fault. Such unreachable negatives accumulate with every round of growth. We propose Search-RSI, a recursive self improvement framework that expands the search world along the agent's capability frontier. In each round, the current policy diagnoses its partially mastered regions of a task space spanned by hop depth, relation rarity, and distractor density; new tasks there are grown together with their evidence; and the same policy decides how they are used: candidates on which its probes disagree feed reinforcement learning, while those beyond its reach become hint guided demonstrations of its own. Keeping the policy inside this loop matters: an improver frozen at the start of training loses 3.2 points. On nine multimodal search benchmarks, Search-RSI keeps improving where static task growth saturates, raising the average accuracy of the recipe it builds on by 9.8 and 9.5 points at 9B and 27B, of which 7.0 points are out of reach for a world that is merely made consistent. The loop uses no external model and only privileged task structure that is removed before training, at 1.27x the compute of static growth.

---

## 2. Embodied-Harness: Towards Recursive Self-Improvement for Robotic Manipulation

**Authors:** Zhenxuan Fan, Zhuoya Wang, Yuqian Yuan, ..., Siliang Tang, Yueting Zhuang
**arXiv:** [2611.27689](https://arxiv.org/abs/2611.27689)
**Categories:** Robotics (cs.RO); Artificial Intelligence (cs.AI); Computer Vision and Pattern Recognition (cs.CV); Multiagent Systems (cs.MA)

Vision-language model (VLM)-based agents offer a promising approach to robotic manipulation, yet remain limited by inadequate memory organization, uncertain failure attribution, and limited reuse of execution experience. We propose Embodied-Harness, a dual-agent framework that improves manipulation by refining the execution harness without updating model parameters. The Actor interacts with the environment through a robot-control interface, while the Reflector converts execution evidence into reusable operational guidance. Hierarchical Memory Architecture maintains short-term execution context and long-term experiential knowledge to support execution and reflection. Evidence-based Experience Reflection grounds failure diagnosis in observed interactions, while Recursive Harness Self-Improvement refines operational guidance across successive attempts. Experiments on RoboTwin 2.0, RoboSPA, and RMBench demonstrate the effectiveness of Embodied-Harness in generalization under environmental variations, spatial reasoning, long-horizon planning, and memory-dependent manipulation. Our method achieves success rates of 82.4%, 76.7%, and 94.4% on the three benchmarks, respectively. Real-world evaluation further yields an average success rate of 96.7% across three manipulation tasks. These results highlight the potential of Embodied-Harness to improve robotic manipulation through experience-driven harness self-improvement.

---

## 3. FoRe: A Force-Guided Framework for Autonomous Grasp Recovery in Vision-Language-Action Models

**Authors:** Shuai Peng, Yongkai Liao, Yuxin Cheng, Haoyuan Wang, Jian Huang
**arXiv:** [2611.27011](https://arxiv.org/abs/2611.27011)
**Categories:** Robotics (cs.RO); Artificial Intelligence (cs.AI)

Vision-language-action (VLA) models have demonstrated strong performance in grasp-based manipulation, yet reliable recovery from local grasping failures remains challenging. Specifically, in pick-and-place tasks, policies may continue transport after a failed grasp instead of retrying, potentially reflecting overreliance on proprioceptive cues for stage progression and limited retry supervision. Existing recovery approaches typically rely on deployment-time guidance or demonstration augmentation. We introduce Force-guided Recovery (FoRe), a framework for autonomous recovery from local grasping failures. Using force feedback, FoRe partitions demonstrations into approach-grasp and transport-placement stages to train separate policies. To supplement limited retry supervision, FoRe then initializes a dedicated retry policy from the approach-grasp policy and refines it through local reinforcement learning (RL) from post-failure states. To avoid inappropriate stage progression, a controller combines force feedback with grasp-command status at inference to coordinate the stage policies, detect grasp failures, and invoke the retry policy. We also construct LIBERO-SUCTION, a force-augmented suction manipulation benchmark adapted from LIBERO, with complete demonstration trajectories for policy training. FoRe consistently improves task success rates for VLA-Adapter and $\pi_{0.5}$ on LIBERO-SUCTION, LIBERO, and real-world tasks. On LIBERO-SUCTION, average absolute gains are 18.4% and 6.5%, respectively. The corresponding real-world absolute gains are 25.0% and 21.7%. FoRe also remains effective with only one demonstration per task on both simulation benchmarks.

---

## 4. MedicalRSI: Medical Recursive Self-Improving Agents via Clinical Model-Harness Co-Evolution

**Authors:** Ziqing Wang, Hamid Palangi, Lili Zhao, Kaize Ding
**arXiv:** [2611.26806](https://arxiv.org/abs/2611.26806)
**Categories:** Computation and Language (cs.CL); Artificial Intelligence (cs.AI)

Medical agents built on large language models (LLMs) have advanced rapidly, yet most stay fixed once deployed and do not keep using their experience to improve later attempts. As a result, the same kind of error can recur across patients. To address this, existing self-improvement methods update an agent's weights or its medical harness from its own experience, but their improving strategy stays fixed and never learns which changes actually help, which caps how much the agent can improve. Recursive self-improvement (RSI) instead improves both the agent and its improving strategy. However, achieving RSI for medical agents is challenging, because clinical workflows rarely come with a reference harness, and a change that fixes early errors may not fix the problems the agent meets later. We propose MedicalRSI, an RSI framework built on Clinical Model-Harness Co-Evolution, in which one model plays two roles. The Solver is the medical agent itself, and the Improver is its learnable improving strategy, which writes a medical harness from the agent's failures. Each harness is rewarded by its gain over acting without it, and both roles are trained together, so the Improver keeps adapting to the problems the Solver has not yet solved. On multiple benchmarks and LLM backbones, MedicalRSI outperforms existing context-level and weight-level self-improvement methods and transfers well to unseen workflows, new LLMs and new databases, a step toward medical agents that keep improving.

---

## 5. Efficient VLA Reinforcement Learning via Subchunk Rollouts in Latent World Models

**Authors:** Nan Tang, Han-Tao Zhang, Jing-Cheng Pang, ..., Hao-Xin Lin, Yang Yu
**arXiv:** [2611.27645](https://arxiv.org/abs/2611.27645)
**Categories:** Machine Learning (cs.LG)

Model-based reinforcement learning (MBRL) can improve pretrained vision-language-action (VLA) policies through imagined experiences. However, existing VLA-MBRL methods primarily rely on large-scale image or video generation world models, incurring large computational overhead. Latent world models offer a more efficient alternative but face two challenges: compounding errors during recursive prediction and incompatibility with VLAs' visual input interfaces. In this work, we propose LS-MBPO, a lightweight residual MBRL framework that leverages latent world models to improve upon pretrained VLAs. LS-MBPO introduces two key techniques: (1) Hierarchical Forcing, which combines dense causal supervision with autoregressive feedback to mitigate compounding prediction errors; and (2) Latent Subchunk Rollouts, which leverage action chunks from a frozen VLA policy and a latent residual policy for successive subchunk refinement, bridging the gap between latent imagination and VLA policy execution. We further introduce a Progress-Conditioned Branch-Start Curriculum that progressively shifts rollout starting points from later to earlier task stages, enabling effective policy learning from short imagined rollouts. Extensive experiments on LIBERO, RoboTwin, and a real-world ALOHA robot show that LS-MBPO achieves superior task performance and training efficiency compared to existing methods.

---

## 6. NavRSI: Recursive Harness Self-Improvement for Vision-and-Language Navigation

**Authors:** Guangzhao Dai, Guoxin Lian, Shuo Wang, ..., Xiangbo Shu, Bin Zhu
**arXiv:** [2611.27499](https://arxiv.org/abs/2611.27499)
**Categories:** Robotics (cs.RO)

Frontier large language models (LLMs) have enabled vision-and-language navigation (VLN) through direct closed-loop perception and action. However, navigation performance depends strongly on the harness governing LLM-environment interactions, while existing harnesses largely rely on manually designed navigation tools, memory, and agent roles. We introduce NavRSI, a harness-centric recursive self-improvement framework that optimizes the navigation behavior of frozen LLMs through closed-loop experience. In each round, NavRSI iteratively collects navigation trajectories and failure diagnostics, employs a designer agent to rewrite the harness, and retains the revisions that prove effective, while the designer accumulates experience from previous revisions so that the harness and this experience co-evolve. Privileged simulator diagnostics guide only the designer and remain inaccessible to the navigating LLM, enabling deployment with a single RGB camera and primitive actions, without task-specific model training or additional navigation tools. Experiments demonstrate consistent improvements across LLMs from four vendors, with 85.64% success rate on the full R2R-CE val-unseen split with GPT-6-Astra, surpassing the previously reported best by 4.13%. Evaluations on RxR-CE, NavRAG-CE, and a real humanoid robot further demonstrate its generalizability.

---

## 7. Learning from Incomplete Actions: Interval Motion Supervision for Vision-Language-Action Policies

**Authors:** Yunpeng Mei, Chenyu Wang, Xiaowen Zhu, ..., YuAn Wang, Gang Wang
**arXiv:** [2611.27171](https://arxiv.org/abs/2611.27171)
**Categories:** Robotics (cs.RO)

Visual labeling of egocentric demonstrations often leaves contiguous gaps in action supervision. Reliable poses around a gap still provide its net translation and rotation. We use this information to train vision-language-action policies while preserving ordinary flow matching on reliable local actions. A composition objective constrains the aggregate motion of missing-action estimates, combining multiple fixed windows when a gap exceeds the policy horizon. A shared interval branch learns from reliable endpoints and supplies the composition target. On LIBERO with 20% of demonstrations and 70.5% missing actions, the main method achieves 87.9% mean success over three training runs. In one paired comparison with matched observation exposure and training cost, its advantage over masking is 10.5%. On Ego-informed RoboTwin gaps, success is 45.4%, versus 40.3% for masking. On five real-robot tasks, mean success is 59.6%, versus 54.8% for interval flow matching alone and 48.8% for masking.

---

## 8. FORTH: Grounding Tactile VLA Execution via Forward-Only Proxy-Control Pairing

**Authors:** Junde Li, Wei-Han Yu, Xiangyi Chu, ..., Ka-Fai Un, Pui-In Mak
**arXiv:** [2611.26744](https://arxiv.org/abs/2611.26744)
**Categories:** Robotics (cs.RO); Systems and Control (eess.SY)

Vision-Language-Action (VLA) policies are widely credited with force control, operating on the unverified assumption that proxy loss minimization implies physical force grounding. In this work, we demonstrate that this assumption breaks down at three core deployment levels: frozen visual backbones discard contact geometry, downstream losses mask token-level gradient alignment, and discrete indicators trigger optimization collapse. To address these disconnections, we present FORTH, a forward-only measurement harness and execution framework that explicitly pairs the optimization objective at each level with its physical control observable. FORTH incorporates three grounded pillars: a layer-local, forward-only tactile encoder that preserves spatial contact geometry without backpropagation, a token-parallel zeroth-order adapter enabling activation-space updates, and SlipGuard, a continuous tactile verification gate that fires on incipient slip. On an elasto-plastic structural shell, FORTH's closed-loop gate peaks at 29 times lower grip force than a monotone reflex ramp, preventing structural crush where the baseline leaves permanent deformation. Furthermore, FORTH matches state-of-the-art execution performance with a 97.6% average success rate across three evaluated LIBERO suites, while reducing peak activation memory by 7.12 times compared to a backpropagated step on the same backbone. Enhanced perception enables deeper physical intelligence.

---

## 9. Analysis of Multi-Client Inference Techniques for Vision-Language-Action Models

**Authors:** Stefan de Lasa, Mohammadreza Mofayezi, Gennady Pekhimenko, Nandita Vijaykumar
**arXiv:** [2611.26944](https://arxiv.org/abs/2611.26944)
**Categories:** Distributed, Parallel, and Cluster Computing (cs.DC); Robotics (cs.RO)

Vision-Language-Action models (VLAs) are a new class of machine learning model for generalizable robot control. While they enable robots to perform complex tasks in unseen environments, serving VLAs leaves hardware idle between inference passes and under-utilized during inference. Serving multiple clients at once can improve utilization, but fundamental multi-client techniques such as batching and co-execution have not been characterized for VLAs. We therefore characterize the trade-offs these known techniques impose across latency, throughput, power, and hardware utilization. Our findings inform trade-offs and challenges for future multi-VLA serving systems.

---

## 10. SIR-Agent: Skill-Augmented Image Restoration Agent with Recursive Self-Improvement

**Authors:** Yijian Wang, Qingsen Yan, Weiyu Zhou, ..., Haokui Zhang, Jiantao Zhou
**arXiv:** [2611.27285](https://arxiv.org/abs/2611.27285)
**Categories:** Computer Vision and Pattern Recognition (cs.CV)

Agents for Image Restoration (IR) aim to leverage Multimodal Large Language Models (MLLMs) to autonomously perceive image degradation and invoke IR tools. However, existing IR agents typically rely on fine-tuning MLLM parameters to adapt to new IR tasks, leading to catastrophic forgetting of IR knowledge. To address this limitation, we propose a skill-augmented IR agent, dubbed SIR-Agent, that maintains IR knowledge in a scalable skill library and uses Recursive Self-Improvement (RSI) to facilitate efficient skill-library evolution. Specifically, we design a Chain Feedback-driven Skill Revision (CFSR) to evolve the skill library. The CFSR analyzes restoration chains to identify and revise weak operations in existing skills. The compatibility of a revised skill with known tasks decides if it replaces the original skill or is appended independently. Furthermore, to advance CFSR's skill-library evolution, we present an RSI-driven skill meta-learning mechanism, which identifies CFSR's inefficient operations and autonomously refines its revision strategy. Extensive experiments across 14 IR benchmarks, covering 6 single-degradation and 8 mixed-degradation scenarios, demonstrate SIR-Agent's superior IR performance. Further evaluation on 7 unseen tasks validates SIR-Agent's generalization to new IR tasks.

---
