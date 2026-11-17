# arXiv Daily Digest — 2026-11-16

**Mode:** direct
**Categories:** cs.AI, cs.LG, cs.RO, cs.CV
**Keywords:** VLA, RSI, agentic robot, self-improving robot, self-evolving robot, robot harness
**Papers found:** 8

---

## 1. VLAN: Vision-Language Accessible Navigation

**Authors:** Jie Hu, Yu Zheng, Wenzhi Wu, ..., Cunlei Cheng, Jiaming Zhang
**arXiv:** [2611.18346](https://arxiv.org/abs/2611.18346)
**Categories:** Artificial Intelligence (cs.AI); Computer Vision and Pattern Recognition (cs.CV)

Accessible mobility is user-conditioned rather than scene-intrinsic, as walkable paths for one embodiment are inaccessible to another. Yet, existing benchmarks evaluate traversability under a fixed and limited embodiment. We present Vision-Language Accessible Navigation (VLAN), containing 1,000 scenes, 20K navigation trajectories, and 160K keyframes across diverse lighting, environmental conditions, scene semantics, and path geometries. For each trajectory, VLAN provides embodiment-specific actions and accessibility features for legged and wheeled agents, including humanoid and quadruped robots and people with visual or mobility impairments, while everyday obstacles and accessibility labels are categorized as Passable, Bypass, HighRisk, and Blocked. Unlike goal-only evaluation, our benchmark measures physical safety and alignment with user-specific constraints via goal-reaching, collision-aware, and accessibility-aligned metrics. We benchmark modern vision-language models and find they often fail to consistently adapt obstacle relevance, path selection, and safety criteria across user profiles, suggesting accessibility-aware navigation requires dedicated datasets, tasks, and metrics beyond conventional embodied navigation evaluation. All data and code open-source at this https URL.

---

## 2. From AI-Enabled Remote Patient Monitoring Toward Agentic Robotics: Embodiment, Governance, and Care Integration

**Authors:** Ivana Ragusa, Lorenzo Guiducci, Filippo Cavallo
**arXiv:** [2611.18484](https://arxiv.org/abs/2611.18484)
**Categories:** Robotics (cs.RO); Artificial Intelligence (cs.AI); Multiagent Systems (cs.MA); Software Engineering (cs.SE); Systems and Control (eess.SY)

AI-enabled remote patient monitoring is evolving beyond passive data collection toward agentic AI systems that interpret patient states, coordinate care, and initiate action across domestic and clinical settings. This structured scoping review finds that mature agentic care has not yet emerged: Most systems remain human led, while stronger decision-action coupling and embodied AI remain largely confined to prototypes and pilots. Healthcare robotics makes the transition from monitoring to action especially visible by translating AI-generated recommendations and decisions into speech, movement, prompting, physical assistance, escalation, and care coordination, making embodiment, clinical integration, human oversight, and governance fundamental design requirements. Further progress requires safe and interoperable care architectures in which intelligent components operate through clinically validated and accountable workflows. We propose agentic robotics as a future direction for supervised systems embedded in the care ecosystem, connecting AI agents and robots with clinicians, caregivers, and patients through auditable workflows that can be interrupted and remain subject to human oversight and explicit AI governance.

---

## 3. Gamer: A Generalist Vision-Language-Action Foundation Model for Long-Horizon Real-Time Game Agent

**Authors:** Run Luo, Kuan Zhang, Qi Deng, ..., Dawei Jiang, Shaoqing Ren
**arXiv:** [2611.18397](https://arxiv.org/abs/2611.18397)
**Categories:** Computation and Language (cs.CL); Artificial Intelligence (cs.AI); Computer Vision and Pattern Recognition (cs.CV)

We introduce Gamer, a generalist agent framework built for long-horizon tasks in complex interactive environments. Its end-to-end architecture combines perception, memory management, and multi-step reasoning. A shared training and deployment pipeline supports interaction with both conventional 2D graphical interfaces and complex 3D simulated worlds. We first continue pre-training on a dataset constructed from tens of thousands of hours of device-level keyboard and mouse interaction. These trajectories span simulated games and embodied environments, allowing the model to learn environmental dynamics across both physical and virtual domains. Sparse-thinking instruction tuning then substantially reduces redundant computation while preserving the reasoning needed for complex decisions. We train the policy for long-horizon interaction with a stable multi-turn reinforcement learning method that addresses finite context windows, accumulated rollout errors, and sparse rewards. For real-time interaction, a cloud-edge inference engine serves numerous simulated game environments concurrently, supports unbounded-context execution, and keeps online inference latency low. Across multiple challenging 3D open-world games, Gamer demonstrates solid generalization and operational efficiency comparable to skilled players. It also achieves competitive results on a range of conventional 2D game benchmarks. These results suggest that even repetitive keyboard and mouse trajectories can support substantial gains from scaling data and learning algorithms. Training on these trajectories helps Gamer learn complex skills more steadily in environments with both physical and digital properties. This approach offers a path toward generalist agents that can interact across digital and physical worlds.

---

## 4. Vision-Language-Action Models: A Life-Cycle Survey of Design, Training and Deployment

**Authors:** Suvarna Kadam, Soran Parsa
**arXiv:** [2611.18372](https://arxiv.org/abs/2611.18372)
**Categories:** Robotics (cs.RO); Artificial Intelligence (cs.AI); Emerging Technologies (cs.ET); Machine Learning (cs.LG)

Vision-language-action (VLA) models adapt web-pretrained vision-language models to output robot actions, so that web knowledge carries over to physical control. In under 4 years the field has moved from RT-2, the first VLA, to open models that fine-tune on a single consumer GPU and to proprietary generalists that clean unseen homes. This survey reviews 88 works from December 2022 to October 2026, mainly on manipulation and navigation, plus humanoid control, world-action models and evaluation. We follow a VLA through its life cycle, from model design to training and deployment, along seven axes. Model design covers (a) inputs and memory, what the model observes; (b) architecture, how its pipeline is built; (c) action output, how it produces motor commands; and (d) intermediate predictions, what else it predicts, from reasoning steps to future observations. Training covers (e) pretraining data, the mix of robot, web, human and simulated data, and (f) post-training, adaptation to the target robot. Deployment covers (g) real-time execution, keeping pace with the robot. We analyse 22 models on these axes and report their training data, model size, inference speed and hardware. Three trends emerge: (i) training data has broadened, from about 10,000 hours of teleoperated robot data ($\pi_0$) to 23,000 community-collected episodes (SmolVLA) and 20,000 hours of egocentric human video (GR00T N1.7); (ii) model sizes have split: most recent models have 3-7 billion parameters, while a new group under one billion runs on consumer GPUs; and (iii) generalist VLAs are emerging that handle both manipulation and navigation, such as UniVLA and Qwen-VLA. We also compare VLAs with world-action models, which predict future observations as well as actions. We review evidence that some VLAs with near-perfect benchmark scores fail when objects or the camera move slightly, and open up further research questions.

---

## 5. Envisioning Agentic Robotics: A New Era of Robotic Systems

**Authors:** Grid Robotics, Qingfeng Lan, Duo Li, ..., Zuhao Yang, Tao Yu
**arXiv:** [2611.18359](https://arxiv.org/abs/2611.18359)
**Categories:** Robotics (cs.RO); Artificial Intelligence (cs.AI); Computation and Language (cs.CL); Computer Vision and Pattern Recognition (cs.CV)

The release of GPT-6 Astra marks the emergence of a new paradigm in robotics: agentic robotics. Within weeks, frontier models with agentic harnesses matched or exceeded task-specific policies on many embodied benchmarks. Instead of training a dedicated policy for each family of tasks, an agentic robotic system applies a foundation model to open-world embodied tasks. It operates in a closed loop: observing the environment, interpreting user intent, reasoning about the task, invoking skills and tools, verifying outcomes, and adapting its strategy. Despite these advances, the community has yet to converge on a shared definition, a reliable evaluation framework, or a research roadmap. We argue that Embodied System 2, realized by a foundation model together with an embodied harness, forms the decision-making core of agentic robotics. Its central challenge is to translate general-purpose reasoning into effective and verifiable actions under physical constraints such as limited reaction time, mechanical limits, unpredictable environment changes, and irreversible consequences. Motivated by this perspective, we propose an evaluation framework that measures both model capabilities and closed-loop system performance. Furthermore, we identify the principles that carry over from digital to physical agents and the challenges that must be addressed to achieve reliable physical autonomy. On top of the Embodied System 2 and the evaluation framework, we envision a research roadmap toward sustained autonomy: the ability to perform work safely and reliably with progressively broader responsibility, from executing individual primitives to fulfilling standing roles.

---

## 6. ESI: An Embodied Self-Improvement Flywheel for LLM-VLA Agents

**Authors:** Yundi Cai, Zihan Wang, Chenxi Han, ..., Houde Liu, Zilei Wang
**arXiv:** [2611.18176](https://arxiv.org/abs/2611.18176)
**Categories:** Robotics (cs.RO)

Independently pretrained language models and vision-language-action (VLA) policies provide complementary building blocks for embodied agents, but connecting them does not automatically produce coordinated behavior. The VLA may generate actions that diverge from the LLM's intended subtask and, upon regaining control after a correction, undo the promising state restored by the LLM. We introduce ESI (Embodied Self-Improvement), an automated flywheel that uses environmental interaction to align reasoning and action. ESI treats the modular agent as the unit of post-training, repeatedly refining the prompts that guide the LLM, the shared skill interface that expresses its intent, and the VLA parameters that realize that intent, then redeploying these components together. Our key insight is that collaboration itself can supply supervision for improving this interface. The LLM's subtask decisions provide semantic supervision for what the policy should execute, while its effective corrections and subsequent student continuations provide action-level supervision for recovery and handoff. The student also learns from its own effective execution, allowing locally useful experience to contribute even when the overall episode fails. On ten selected RoboDojo tasks, ESI achieves a mean Score of 62.03 and a mean success rate of 49.41% using an LLM-VLA agent without generating task-specific control code. On both metrics, it outperforms the published reference results of all hybrid embodied agents, including the Agent+WAM system GO-3 Nano Preview (47.27 Score and 36.60% success), as well as all compared code-based methods.

---

## 7. Agentic-Teacher: An Agentic Data Engine for Failure-Driven VLA Post-Training

**Authors:** Gongyue Teng, Yuqing Xie, Yixian Zhang, ..., Chao Yu, Xinlei Chen
**arXiv:** [2611.17394](https://arxiv.org/abs/2611.17394)
**Categories:** Robotics (cs.RO)

Improving a pretrained vision-language-action (VLA) model requires demonstrations that address its weaknesses and provide effective supervision for learning. Coding agents can autonomously generate demonstrations through environment interaction, yet successful execution alone does not ensure effective supervision for VLA learning. We introduce Agentic-Teacher, an autonomous data engine for failure-driven VLA post-training. Given a VLA checkpoint, a task specification, and configured environment tools, the engine analyzes failed rollouts, selects intervention states, and iteratively develops closed-loop code policies through execution feedback. Validated policies become reusable demonstration generators that collect successful continuations from states where the VLA struggles. To make these demonstrations suitable for learning, Agentic-Teacher introduces temporally correlated action noise to broaden state-action coverage, removes idle frames while preserving gripper transitions, and filters trajectories using the frozen base model's flow-matching loss. The resulting demonstrations are combined with successful VLA rollouts for post-training, yielding an updated policy that operates without coding-agent assistance. Agentic-Teacher thus connects the weaknesses of a target VLA to both the generation and curation of its training data. In simulation, it improves $\pi_0$ success rates from 79.4% to 87.8% on LIBERO-10, from 80.4% to 90.6% on MetaWorld-10, and from 0% to 30.0% across three RoboCasa tasks.

---

## 8. RecurIR: Learning When and How to Revise Restoration Policies via Recursive Self-Improvement

**Authors:** Hu Gao, Haoran Zhang, Yulong Chen, Lizhuang Ma
**arXiv:** [2611.18006](https://arxiv.org/abs/2611.18006)
**Categories:** Computer Vision and Pattern Recognition (cs.CV)

Agent-based image restoration has achieved promising performance by coordinating restoration tools to handle heterogeneous and coupled degradations. However, existing agents often improve their decisions through accumulated successful and failed executions, without explicitly identifying the conditions under which learned restoration strategies remain effective. Consequently, changes in degradation severity, spatial coverage, or interactions may invalidate previous decisions, while providing limited guidance on how these decisions should be revised. In this paper, we propose \textbf{RecurIR}, a recursive self-improvement framework that enables restoration agents to learn when and how to revise their decision rules. Specifically, we introduce a policy-hypothesis discovery mechanism to identify testable, condition-dependent rules through matched tool executions. We then design a rule-falsification-driven task evolution mechanism to generate targeted degradation variations, examine the validity of learned rules, and identify their applicability boundaries. Based on the resulting evidence, we develop a change-conditioned policy revision mechanism that learns how variations in degradation conditions should modify tool selection, execution order, operation strength, and processing regions. We further incorporate independent verification to retain effective revisions and use the resulting feedback to guide subsequent hypothesis discovery and task evolution. Through this recursive process, RecurIR progressively refines its restoration policies as degradation conditions change. Extensive experiments demonstrate the effectiveness of the proposed framework.

---
