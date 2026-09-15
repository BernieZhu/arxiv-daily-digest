# arXiv Daily Digest — 2026-09-14

**Mode:** direct
**Categories:** cs.AI, cs.LG, cs.RO, cs.CV
**Keywords:** VLA, agentic robot, robot harness
**Papers found:** 3

---

## 1. Dynin-Robotics: Omnimodal Unified Diffusion Vision-Language-Action Model

**Authors:** Hoeun Lee, Jaeik Kim, Jusang Oh, ..., Hyeonggeun Kim, Jaeyoung Do
**arXiv:** [2609.13053](https://arxiv.org/abs/2609.13053)
**Categories:** Robotics (cs.RO); Artificial Intelligence (cs.AI); Machine Learning (cs.LG)

Visual goal and dynamics prediction can provide language-conditioned robot policies with both a target outcome and a representation of action-dependent scene changes. We bring these predictions into action generation and selection through a shared trajectory model. Dynin-Robotics implements this formulation on Dynin-Omni, an omnimodal masked-diffusion backbone, representing language, visual observations, goals, and actions as discrete tokens. By varying conditioning and target spans, the same model learns action prediction, action-conditioned next-observation prediction, terminal goal-state prediction, and trajectory-to-instruction reconstruction. These interfaces support test-time scaling through goal prediction, action-candidate evaluation, and joint refinement of action and future-state predictions. We continually pretrain the model on approximately 1.33 million trajectories from 48 Open X-Embodiment datasets and adapt it separately to downstream domains. On two VLABench tasks, robot pretraining improves adaptation within a fixed Stage-2 step budget, and the full objective mixture improves shifted-instruction success over Policy-only post-training under the same coupled decoder. Combining goal guidance with joint action-next-state denoising further improves shifted-instruction success over action-only decoding; the benefit depends on how the predictions are composed. Dynin-Robotics achieves competitive performance on LIBERO and zero-shot LIBERO-Plus, together with a 78.4% average success rate across four manipulation conditions on a Franka Research 3 robot. An optimized block-parallel implementation accelerates model-side action decoding by up to 29.2x relative to the base implementation under the reported profiling setup. These results support shared trajectory modeling as a common interface for learning complementary robot objectives and composing their predictions during control.

---

## 2. Efficient Vision-Language-Action Management and Serving for Robot Factories

**Authors:** Dionysios Adamopoulos, Nattapol Chanpaisit, Basel Fakhri, Christina Giannoula
**arXiv:** [2609.12075](https://arxiv.org/abs/2609.12075)
**Categories:** Distributed, Parallel, and Cluster Computing (cs.DC); Hardware Architecture (cs.AR); Machine Learning (cs.LG); Performance (cs.PF); Robotics (cs.RO)

Vision-Language-Action (VLA) models show high robotic manipulation capabilities via a two-stage design: a Vision-Language Model (VLM) stage followed by an Action Diffusion Transformer (ADiT) stage. Since robots must meet strict Service-Level Objectives (SLOs) for safety, VLA inference is inherently latency-critical. Meeting these SLOs requires high-end GPUs, yet weight, cost, and power constraints preclude integrating such GPUs on-robot. Prior works offload VLA inference to edge servers that serve many robots on VLA models. However, current VLA systems lack support for multi-request, multi-model execution on a multi-GPU server under SLOs, while existing serving systems for multi-stage models are optimized for throughput and stage disaggregation across separate GPUs, which are ill-suited for the millisecond-scale stages of VLA models. We design Robion, the first VLA serving and management system for multi-robot, multi-model requests on multi-GPU edge servers that meets SLOs. Our serving engine disaggregates the VLM and ADiT stages within a GPU via two streams, dynamically restricting the SMs on VLM stream so ADiT always finds SMs to run alongside it, and co-locates multiple models by sharing these streams across them, prioritizing requests by least remaining SLO time. Our management engine enables flexible model placements on multi-GPU servers, and integrates an intelligent traffic controller that maximizes per-model batching under the chosen placement while bounding each GPU's load to meet SLOs. For individual models, Robion serves on average 6.7$\times$ and 1.5$\times$ higher robot load within 98% SLO attainment over vLLM-Omni, the most widely used multi-stage serving system, and Monolithic, which runs VLM and ADiT as a single pipeline, respectively. In a large-scale experiment of serving 8 different models on a 4-GPU server, Robion can serve up to 64 robots within 98% SLO attainment.

---

## 3. DATAFARM: Distribution-Aligned Task and Motion Planning for Fine-Tuning Vision-Language-Action Models

**Authors:** Samrat Sahoo, Yixuan Huang, Tom Silver
**arXiv:** [2609.12316](https://arxiv.org/abs/2609.12316)
**Categories:** Robotics (cs.RO)

Collecting high-quality robot data remains a fundamental challenge for training robot foundation models. Task and motion planning (TAMP) offers a scalable way to generate demonstrations, but our experiments show that raw TAMP trajectories provide surprisingly little benefit when used to fine-tune pretrained vision-language-action (VLA) models, despite successfully solving the target tasks. We hypothesize that this failure arises from a behavioral distribution mismatch between planner-generated trajectories and the data used to pretrain the VLA. To address this mismatch, we introduce DATAFARM: Distribution-Aligned Task And motion planning for Fine-tuning A Robot foundation Model, an approach that incorporates the pretraining distribution directly into TAMP trajectory generation. DATAFARM aligns generated trajectories with the pretraining data in robot joint configurations, motion style, and temporal execution profiles. We evaluate DATAFARM on three tabletop manipulation tasks that TAMP can perform and a cloth-folding task beyond the capability of TAMP. DATAFARM achieves an average success rate of 56.7%, substantially outperforming raw TAMP (8.3%) while approaching human teleoperation (61.7%). On Deformable Object Manipulation, which is outside the fine-tuning distribution, the fine-tuned model retains 85% success, compared with 90% for the pretrained model. These results show that aligning planner-generated demonstrations with the pretraining distribution can make TAMP an effective source of data for VLA fine-tuning. Website and code: this https URL

---
