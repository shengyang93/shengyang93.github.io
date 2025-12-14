---
title: Generative Scene 3R
date: 2025-03-01
tags:
  - Alibaba
image:
  preview_only: true
summary: |
  We maintain a Generative Reconstruction framework for Closed-loop Simulation.
---

With a series of recent works now accepted, published, and patented, we are pleased to introduce **Generative Reconstruction Suite v1.0** and present the complete technical picture behind it. This project builds upon our peer-reviewed papers — listed below and on my homepage — along with partially released code to support reproducibility and practical adoption. The suite has already been deployed within the Alibaba Autonomous Driving Lab to advance both perception systems and end-to-end driving algorithms. We welcome inquiries regarding collaboration or technical details.

<div class="text-xs">

[1] Xianming Zeng*, Sicong Du*, Qifeng Chen*, Lizhe Liu, Haoyu Shu, Jiaxuan Gao, Jiarun Liu, Jiulong Xu, Jianyun Xu, Mingxia Chen, Yiru Zhao, Peng Chen, Yapeng Xue, Chunming Zhao, **Sheng Yang†**, Qiang Li. <br> **Industrial-Grade Sensor Simulation via Gaussian Splatting: A Modular Framework for Scalable Editing and Full-Stack Validation**. <br> *IROS*, 2025.

[2] Ziqian Ni, Sicong Du, Zhenghua Hou, Chenming Wu, **Sheng Yang†**. <br> **Para-Lane: Multi-Lane Dataset Registering Parallel Scans for Benchmarking Novel View Synthesis**. <br> *3DV*, 2025.

[3] Guo Chen*, Jiarun Liu*, Sicong Du, Chenming Wu, Deqi Li, Shi-Sheng Huang†, Guofeng Zhang, **Sheng Yang†**. <br> 
**GS-RoadPatching: Inpainting Gaussians via 3D Searching and Placing for Driving Scenes**. <br> *SIGGRAPH Asia*, 2025.

[4] Sicong Du*, Jiarun Liu*, Qifeng Chen, Hao-Xiang Chen, Tai-Jiang Mu, **Sheng Yang†**. <br> **RGE-GS: Reward-Guided Expansive Driving Scene Reconstruction via Diffusion Priors**. <br> *ICCV*, 2025.

[5] Qifeng Chen, **Sheng Yang†**, Sicong Du, Tao Tang, Peng Chen, Yuchi Huo. <br> **LiDAR-GS: Real-time LiDAR Re-Simulation using Gaussian Splatting**. <br> *ArXiv*, 2024.

[6] Qifeng Chen, Jiarun Liu, Rengan Xie, Tao Tang, Sicong Du, Yiru Zhao, Yuchi Huo, **Sheng Yang†**. **LiDAR-GS++: Improving LiDAR Gaussian Reconstruction via Diffusion Priors**. <br> *AAAI*, 2026.

</div>

### Background and Applications of Generative Reconstruction

Generative AI significantly expands the capabilities of data augmentation, closed-loop simulation, and even closed-loop training for autonomous driving systems. Among the various emerging directions, we have validated two particularly promising paradigms:

1. Layout and language guided scene generation;
2. **Driving clip conditioned scene expansion**.

This project focuses on the **second** paradigm, which enables faithful reconstruction and controlled expansion of historical driving scenarios. Such capability is especially valuable for auto-regressive model evolution, systematic failure analysis, and long-term performance tracking in industrial autonomous driving systems [1].

![[1] Sensor Simulation System](image.png)

### Key Procedure 1: Multi-Modal 3D Reconstruction

Given a crowd-sourced driving clip — typically uploaded due to risky behaviors, anomalous events, or previously unseen environments — the off-board data curation pipeline first performs ego-state re-estimation, scene reconstruction, motion clustering, and semi-automatic instance-level annotation. This process enables a precise understanding of what actually occurred during the recorded scenario.

We adopt essentially the same pipeline to construct and release the **Para-Lane** dataset [2], which provides registered multi-lane scans for benchmarking novel view synthesis methods.

![[2] Para-Lane Dataset](image-1.png)

For our specific sensor suite and platform configuration, we further design a dedicated scene representation and reconstruction strategy for LiDAR data, known as **LiDAR-GS** [5].

![[5] LiDAR-GS](image-2.png)

### Key Procedure 2: Editing the Reconstruction via Context, Database and UI

To support efficient scene management and editing, we explicitly separate **high-value dynamic instances** from the static background in the reconstructed assets. These instances are designed to be replaceable, and their trajectories and behaviors can be interactively modified through a dedicated user interface.

In many scenarios, it is necessary to remove selected foreground instances after UI-based editing, while maintaining spatial and visual coherence in regions that were previously occluded. To address this challenge, we introduce **GS-RoadPatching** [3], an intermediate inpainting procedure inspired by PatchMatch, but operating directly on **3D Gaussian primitives** rather than 2D pixels.

![[3] GS-RoadPatching](image-4.png)

### Key Procedure 3: Expanding the Reconstruction via Diffusion

![[4] RGE-GS](image-5.png)

To enable physically consistent free-viewpoint novel view synthesis, we develop specialized expansion techniques for both camera and LiDAR modalities. On the camera side, we introduce **RGE-GS** [4], while on the LiDAR side, we extend LiDAR-GS [5] to **LiDAR-GS++** [6]. Both approaches leverage diffusion priors to expand reconstructed regions while preserving consistency with real sensor observations and underlying scene geometry.

![[6] LiDAR-GS++](image-3.png)

### Ongoing Submissions

We currently have several submissions under review that address remaining technical challenges and move toward a more comprehensive Generative Reconstruction Suite. Our ongoing investigations include:

- Accelerating high-fidelity 3D reconstruction, for example through modern feed-forward architectures.
- Improving the efficiency and robustness of blending between mixed foreground and background regions.
- Enabling scalable retrieval of desired 3D instances from a continuously growing instance database, with further refinement and adaptation through prompt-based control.