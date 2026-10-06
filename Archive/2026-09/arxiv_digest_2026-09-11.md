# arXiv Daily Digest — 2026-09-11

**Mode:** direct
**Categories:** cs.AI, cs.LG, cs.RO, cs.CV
**Keywords:** VLA, agentic robot, robot harness
**Papers found:** 2

---

## 1. HuRo: Robotizing Human Videos for Scalable VLA Pretraining

**Authors:** Jinho Jeong, Se June Joo, Jaehyun Kang, ..., Hanjung Kim, Seon Joo Kim
**arXiv:** [2609.10706](https://arxiv.org/abs/2609.10706)
**Categories:** Robotics (cs.RO); Computer Vision and Pattern Recognition (cs.CV); Machine Learning (cs.LG)

Human video datasets have emerged as a compelling alternative to expensive real-robot data, offering rich diversity at scale. To bridge the human-to-robot embodiment gap, existing approaches either robotize videos in task-matched settings or address observation and action alignment separately at scale. In this work, we systematically examine whether robotized human videos can provide effective and scalable supervision for pretraining vision-language-action (VLA) policies. To this end, we develop a robotization pipeline that converts heterogeneous human videos into robot-aligned observations and action trajectories while inferring missing intermediate signals across annotation levels. Using this pipeline, we construct the HuRo dataset, comprising about 630K robotized episodes and 142M processed frames from five human-video sources. Across four real-world manipulation tasks, increasing robotized pretraining scale improves overall completion from 51.5% to 80.3% and OOD completion under spatial and visual shifts from 34.9% to 72.2%. Ablations further show that visual robotization improves OOD robustness and that end-to-end pretraining with retargeted actions outperforms visual-only transfer. Code and data are released on our website: this https URL.

---

## 2. IMLE-VLA: Fast Single-Step Action Generation for Vision-Language-Action Policies

**Authors:** Kian Hosseinkhani, Qinhe Peng, George Shramko, ..., Dinesh Jayaraman, Ke Li
**arXiv:** [2609.10915](https://arxiv.org/abs/2609.10915)
**Categories:** Robotics (cs.RO); Computer Vision and Pattern Recognition (cs.CV)

Vision-language-action (VLA) policies leverage pretrained vision-language backbones to achieve strong cross-task generalization. A leading design couples this backbone with a dedicated continuous action head trained via diffusion or flow matching. However, such heads rely on iterative multi-step sampling, for example 10 Euler steps in $\pi_{0.5}$. This creates an inference bottleneck that produces stop-and-go movement in the robot and slower task completion. We introduce IMLE-VLA, which replaces the iterative action head with a single-step conditional generator trained via conditional Implicit Maximum Likelihood Estimation (cIMLE). The cIMLE objective promotes multimodal action coverage, avoiding the mode collapse of naive regression heads while eliminating multi-step sampling entirely. When IMLE-VLA is applied to $\pi_{0.5}$, it increases inference frequency 3.67x (55 Hz vs. 15 Hz), enabling up to 11x higher action throughput. On the 40-task LIBERO benchmark, IMLE-VLA achieves the highest average success rate (98.0%) among all baselines while leading in inference frequency. Under the test-time perturbations of LIBERO-plus, IMLE-VLA retains $\pi_{0.5}$'s robustness while other baselines degrade sharply, confirming that the cIMLE head preserves generalization. Real-world experiments on a Franka Emika Panda across four tasks demonstrate smoother motion (2.2x to 3.0x lower jerk) and faster task completion, with IMLE-VLA outperforming $\pi_{0.5}$ on every task and reducing average VLA inference time per episode by 3.9x to 6.6x. Videos and code are available at this https URL

---
