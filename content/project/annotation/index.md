---
title: Data Curation Chain
date: 2023-10-01
tags:
  - Alibaba
image:
  preview_only: true
summary: |
  We maintain vertification and annotation tools for preparing our data warehouse.
---


### Full-Stack Curation for Driving Clips via Powerful Auto-Labeling and Smart Quality Inspection

Raw sensor frames (Vision), driver–customer dialogues (Language), and final driving decisions (Action) are three fundamental modalities for advancing Driving AI agents, enabling both low-level vehicle control and high-level task specification and execution. Although ground truth for these modalities is readily obtainable from sensors and onboard systems, modern data curation and closed-loop validation still face two critical challenges:

The first challenge is to develop an effective and reliable way to **distinguish between high-quality and low-quality raw driving clips**, so that they can be prioritized, filtered, and utilized appropriately in the training and evaluation of Driving AI agents. This requires going beyond simple heuristics such as clip length or resolution, and instead designing multi-dimensional quality metrics that consider factors such as sensor integrity (e.g., exposure, motion blur, calibration status), scenario richness (e.g., complex traffic interactions, rare corner cases, diverse weather and lighting conditions), annotation completeness and correctness, and relevance to the target tasks and behaviors the agent needs to learn. An effective differentiation mechanism should ideally combine **automated scoring models** (such as learned quality predictors and anomaly detectors) with **targeted human-in-the-loop review** for ambiguous or high-impact cases, allowing large-scale datasets to remain both manageable in size and rich in informative content, while minimizing noise, redundancy, and bias in the data pipeline.

The second challenge lies in our ability to dive deeply into a given driving clip and precisely **reconstruct what is happening** throughout the recording, including the evolving scene, the driver’s intentions, and the causal chain between perception and action. This fine-grained understanding is particularly beneficial for both canonical two-stage end-to-end systems (which separate perception from planning) and one-stage VLA systems that rely on visual–language chain-of-thought reasoning, because it allows us to explicitly model and supervise the intermediate cognitive steps that connect raw sensory inputs to final decisions. By injecting rich intermediate signals — such as how a human driver or operator would describe the surrounding environment, explain why certain agents are behaving in a particular way, or articulate the rationale behind a chosen maneuver — we can provide the model with structured “thought processes” rather than only outcomes. This strengthens its capacity to understand spatial relationships, anticipate other actors’ behaviors, and generalize to novel scenarios. In practice, this involves **temporally aligned multimodal annotations** (e.g., frame-level narrations, Q&A about ambiguous situations, or causal explanations for interventions) that transform passive driving footage into an interpretable sequence of **perceptions, hypotheses, and actions**, ultimately improving both the transparency and robustness of Driving AI agents.

Therefore, we are pleased to introduce our AI infrastructure products designed to streamline the data curation process. These solutions have been successfully deployed for years to support the development of Alibaba’s unmanned vehicles. Although the underlying technologies are patented, our team is excited to make them available commercially. Please contact us if you are interested in **licensed usage and private deployment**, or in exploring deeper collaboration through **fully open-sourced, strategically aligned partnerships**.

### 1. Driving Clip Verification and Agentic Bug Reporting

*To Be Announced*.

### 2. Full-Modality Annotation with Human-in-the-loop Validation

| Static | Splited | Dynamic |
|---|---|---|
| ![Static Annotated](static.gif) | ![Splited](sensor.gif) | ![Temporal Annotated](temporal.gif) | 

Given verified driving clips, it is often necessary to reconstruct them in detail to enable precise ground-truth validation and open-loop evaluation of key perception and decision-making tasks, such as occupancy prediction, instance-level tracking, online vectorized mapping, and final action selection. To support these needs, we have developed FusionX, an all-in-one framework for jointly annotating perception and planning signals, providing a comprehensive foundation for training and validating advanced Driving AI agents.

![Overall Magic Annotation](picking.gif)

FusionX adopts an architecture with two tightly coupled components that together significantly improve the efficiency and quality of multimodal annotations:

![Quality Inspection](jumpy.gif)

1. **Spatial Modeling and Auto-Labeling:** Given a multi-sensor driving clip, FusionX first estimates the most accurate possible sensor and motion parameters, including camera intrinsics, distortion models, extrinsics, and the ego-vehicle trajectory. On this basis, it reconstructs scene geometry and appearance (e.g., texture and, where applicable, albedo) throughout the recorded scenario, while separating dynamic objects from the static background and resolving them into distinct instances. Leveraging Large Vision–Language Models (LVLMs) that have undergone domain-specific post-training, FusionX then performs open-vocabulary panoptic segmentation to produce structured scene representations and derive auxiliary chain-of-thought-style descriptions that capture semantic and contextual information useful for downstream tasks.

![Detailed Box Adjustment](annotation.gif)

2. **Manual Refinement and Inspection:** Based on the confidence estimates produced by the auto-labeling models, professional annotators use FusionX’s dedicated UI to focus their efforts on ambiguous or low-confidence regions. In close collaboration with UI and tool designers, they continuously refine Standard Operating Procedures (SOPs) to improve annotation consistency and throughput. The manually curated corrections are fed back into the system as additional post-training data, enabling FusionX to iteratively improve its models and achieve self-reinforcing gains in annotation quality and efficiency over time.

![Decision Labeling](pnclabeling.gif)
