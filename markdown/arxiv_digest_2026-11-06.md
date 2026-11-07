# arXiv Daily Digest — 2026-11-06

**Mode:** direct
**Categories:** cs.AI, cs.LG, cs.RO, cs.CV
**Keywords:** VLA, RSI, agentic robot, self-improving robot, self-evolving robot, robot harness
**Papers found:** 5

---

## 1. Failure Prediction and Classification in Vision-Language-Action Models Via Calibrated Latent Probing

**Authors:** Michal P. Podolinsky, Yunhao Yang, Daniel Little, ..., Matthias Scheutz, Ufuk Topcu
**arXiv:** [2611.08425](https://arxiv.org/abs/2611.08425)
**Categories:** Robotics (cs.RO); Artificial Intelligence (cs.AI)

Vision-Language-Action models (VLAs) enable general-purpose embodied intelligence, but their performance is brittle under distribution shift, where unanticipated failures can damage equipment or endanger people. Deploying VLAs in real-world systems therefore requires a runtime monitor that is timely, calibrated, and informative while being efficient enough to run on the edge. Existing methods fail to fulfill these requirements. We present VLA-Tug, a lightweight probe over the latent layers of a VLA backbone that improves early failure detection and bounds the missed-detection and false-alarm rates, with minimal inference overhead. We show that supervising on the pre-failure segment of a trajectory increases early failure detection at matched false-positive rates by up to 30% over the strongest learned baseline. Under shift to unseen tasks, the bounds on missed-detection and false-alarm rates remain valid in up to 86% of runs, versus at most 21% for baselines. Unlike existing methods, VLA-Tug predicts the failure mode to enable corrective actions, raising top-3 accuracy on unseen tasks by up to 44% over a majority baseline. VLA-Tug enables real-time monitoring where the well-timed and informative probe supports lightweight steering that improves task success. We release a dataset of 3,180 annotated manipulation episodes to support future work on latent failure detection in VLAs at this https URL.

---

## 2. OopsieRecover: Learning Transferable VLA Corrections from Semantic Interventions

**Authors:** Arpit Bahety, Skand Peri, Sriniket Ambatipudi, ..., Masha Itkina, Roberto Martín-Martín
**arXiv:** [2611.08462](https://arxiv.org/abs/2611.08462)
**Categories:** Robotics (cs.RO)

Vision-Language-Action (VLA) models can perform a wide range of robotic manipulation tasks, but often fail during deployment. Teaching them to recover from these failures requires substantial corrective data: existing approaches learn to recover from failures by directly associating corrective actions with the observations in which they were demonstrated. For instance, DAgger-like fine-tuning can require tens to hundreds of interactions, yet the resulting policy may still fail to generalize the learned corrections beyond the demonstrated scenarios. We hypothesize that semantics can capture the underlying reasons for failures and their corrections, enabling policies to learn from only a handful of corrective demonstrations and generalize those corrections to novel objects, and scene variations. We propose OopsieRecover, a framework that uses abduction to infer the intent behind a small set of corrective demonstrations and encodes the inferred knowledge as dense spatial representations and conditional costs. These costs capture when a behavior is undesirable and steer the policy toward more desirable action regions. We experiment across 6 tasks and variations in object poses, scenes, and related tasks, and find that only a handful of corrective demonstrations can enable a VLA to overcome failures across a broad range of novel situations, without requiring new corrective data for each variation. Please refer to this https URL for videos.

---

## 3. T3R: Training-Free Two-Stage Token Refinement Towards Efficient and Robust VLA Models

**Authors:** Mohammed Hassan, Zhenyang Chen, Zheng Wang, ..., Yingyan, Chaojian Li
**arXiv:** [2611.08413](https://arxiv.org/abs/2611.08413)
**Categories:** Robotics (cs.RO); Computer Vision and Pattern Recognition (cs.CV)

Vision-Language-Action (VLA) models enable end-to-end robot control, but inference is increasingly expensive. Each decision processes hundreds of visual tokens, often across multiple cameras, leading to substantial computation while allowing irrelevant background content to distract action prediction under distribution shift. We argue that these issues stem from two complementary forms of redundancy: many visual tokens are spatially irrelevant, while attention over the remaining tokens is often misallocated. Based on this observation, we propose T3R, a Training-Free Two-Stage Token Refinement framework. In the first stage, segmentation-guided token pruning removes irrelevant visual patches to reduce computation and eliminate distracting context. In the second stage, saliency-guided attention biasing reallocates attention toward action-critical visual regions and language instructions within the retained tokens. Together, pruning produces a cleaner candidate set, while attention biasing further emphasizes the most decision-relevant evidence, yielding a better accuracy-efficiency frontier than either stage alone. On LIBERO-Spatial, T3R removes 85% of scene-camera visual tokens while essentially matching the unpruned success rate, and improves success by up to 7 percentage points under out-of-distribution object-placement perturbations. The timing comparison attributes 7.8 ms per inference call to pruning and attention-bias application. As input resolution increases, LLM-forward profiling shows up to a 3.3x speedup over the unpruned baseline. Evaluations across LIBERO, SIMPLER, and RoboTwin with three VLA backbones show the strongest accuracy-efficiency benefits in multi-camera settings. These results demonstrate that training-free token refinement is a practical approach to efficient and robust VLA inference.

---

## 4. RoboARCade: Benchmarking Agentic Robot Control

**Authors:** Satvik Sharma, Hengyuan Hu, Mihika Kamat, Dorsa Sadigh, Jeannette Bohg
**arXiv:** [2611.08209](https://arxiv.org/abs/2611.08209)
**Categories:** Robotics (cs.RO)

Improvements in multi-modal capabilities have enabled agents to act directly as robot policies, a setting we refer to as agentic robot control (ARC). We introduce RoboARCade, a benchmark of long-horizon manipulation tasks across three embodiments designed to test in-context adaptation, memory, and reasoning for precise control. The tasks build on existing open-source benchmarks, which we make harder by widening the range of initial conditions. RoboARCade is easy to use and extend: all tasks run on a single simulation backend, MuJoCo, each task is a self-contained data pack, and agents connect through interchangeable interfaces, so new tasks, agents, and interfaces can be added independently. The benchmark separates leading agents: GPT-6 Astra achieves 49.8% compared with 43.6% for Claude Fable 5.1, leaving substantial room for improvement. Comparing two interfaces, we find that a richer visual interface adds only 1.5 to 6.8 points at 1.7 to 2.3 times the cost. Failures stem mostly from choosing a poor manipulation strategy or executing a good one imprecisely, rarely from misunderstanding the scene, and agents incorrectly claim success on 24% to 39% of attempted subtasks. Agents can also improve without human input: one successful demonstration in context raises Astra's score from 53.5% to 73.0% on a five-task subset, and a prompt the agent writes and revises itself reaches 72.0%. Code, videos and full traces are available at this http URL.

---

## 5. AffectiveVLA: Safe and Intent-Aware VLA Control for Human-Humanoid Social Interaction

**Authors:** Nikita Kuzmin, Georgii Demianchuk, Mariya Lezina, ..., Miguel Altamirano Cabrera, Dzmitry Tsetserukou
**arXiv:** [2611.07712](https://arxiv.org/abs/2611.07712)
**Categories:** Robotics (cs.RO)

Social touch interactions, such as handshakes, fist bumps, and hugs, require humanoid robots to infer human intent, generate contact-rich motions, and maintain safe physical contact. We present AffectiveVLA, an intent-gated Vision-Language-Action (VLA) pipeline deployed on a Unitree G1 humanoid with dexterous hands. A lightweight RGB-based model recognizes interaction intent from two onboard cameras and converts it into a language prompt for the VLA policy. Low-confidence predictions suppress motion execution, reducing unintended activations. During physical contact, interaction-specific compliance profiles adjust arm impedance, while an independent voice-triggered mechanism initiates a latched safe-stop procedure. Using VR teleoperation, we collected approximately 1,300 multimodal interaction episodes and fine-tuned four VLA models: GR00T, RLDX-1, Being-H0.5, and UnifoLM-VLA-0. On-robot evaluation identifies GR00T as the best-performing standalone model. Integrating intent recognition increases its macro-F1 score from 0.75 to 0.90, while the intent model achieves a p95 inference latency of 6.27 ms. These results demonstrate that explicit intent gating improves the reliability of VLA-based social interaction without compromising real-time operation.

---
