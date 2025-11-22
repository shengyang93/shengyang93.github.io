---
title: Generative Scene 3R
date: 2025-03-01
tags:
  - Alibaba
image:
  preview_only: true
summary: |
  We maintain a generative reconstruction framework for an editable closed-loop simulation.
---

With a series of recent works now accepted, published, and patented, we are pleased to present Generative Reconstruction Suite v1.0 and summarize the full picture behind it. This technical project is built upon our accepted papers, which are listed on my homepage together with partially released code for reproducibility and ease of use. The suite has already been adopted at Alibaba Autonomous Driving Lab to advance both perception and end-to-end driving algorithms. If you are interested in collaboration or further details, please feel free to reach out.

<div class="text-xs">

[1] Xianming Zeng*, Sicong Du*, Qifeng Chen*, Lizhe Liu, Haoyu Shu, Jiaxuan Gao, Jiarun Liu, Jiulong Xu, Jianyun Xu, Mingxia Chen, Yiru Zhao, Peng Chen, Yapeng Xue, Chunming Zhao, **Sheng Yang†**, Qiang Li. <br> **Industrial-Grade Sensor Simulation via Gaussian Splatting: A Modular Framework for Scalable Editing and Full-Stack Validation**. <br> *IROS*, 2025.

[2] Ziqian Ni, Sicong Du, Zhenghua Hou, Chenming Wu, **Sheng Yang†**. <br> **Para-Lane: Multi-Lane Dataset Registering Parallel Scans for Benchmarking Novel View Synthesis**. <br> *3DV*, 2025.

[3] Guo Chen*, Jiarun Liu*, Sicong Du, Chenming Wu, Deqi Li, Shi-Sheng Huang†, Guofeng Zhang, **Sheng Yang†**. <br> 
**GS-RoadPatching: Inpainting Gaussians via 3D Searching and Placing for Driving Scenes**. <br> *SIGGRAPH Asia*, 2025.

[4] Sicong Du*, Jiarun Liu*, Qifeng Chen, Hao-Xiang Chen, Tai-Jiang Mu, **Sheng Yang†**. <br> **RGE-GS: Reward-Guided Expansive Driving Scene Reconstruction via Diffusion Priors**. <br> *ICCV*, 2025.

[5] Qifeng Chen, **Sheng Yang†**, Sicong Du, Tao Tang, Peng Chen, Yuchi Huo. <br> **LiDAR-GS: Real-time LiDAR Re-Simulation using Gaussian Splatting**. <br> *ArXiv*, 2024.

[6] Qifeng Chen, Jiarun Liu, Rengan Xie, Tao Tang, Sicong Du, Yiru Zhao, Yuchi Huo, **Sheng Yang†**. **LiDAR-GS++: Improving LiDAR Gaussian Reconstruction via Diffusion Priors**. <br> *AAAI*, 2026.

</div>

### Background and Applications from Generative Reconstruction

Generative AI further enhances data augmentation, closed-loop simulation, and even closed-loop training. We have already validated two particularly promising GenAI directions: (1) layout- and language-guided scene generation, and (2) driving-clip-conditioned scene expansion. This project focuses on the second direction, which enables more faithful reconstruction of historical driving scenarios and is therefore especially suitable for regressive model evolution and systematic problem diagnosis [1].

![[1] Sensor Simulation System](image.png)

### Key Procedure 1: Performing Multi-modal 3D Reconstruction

Given a crowd-sourced driving clip — typically uploaded because it involves risky behaviors or previously unseen environments — the off-board data curation pipeline first performs ego-state re-estimation, scene reconstruction, motion clustering, and semi-auto instance-wise labeling to understand what actually happened. We employ essentially the same pipeline to construct and release the Para-Lane dataset [2].

![[2] Para-Lane Dataset](image-1.png)

For our specific sensor suite and platform configuration, we additionally design a tailored scene representation and reconstruction strategy for the LiDAR modality, referred to as LiDAR-GS [5].

![[5] LiDAR-GS](image-2.png)

### Key Procedure 2: Editing the Reconstruction via Context, Database and UI

For efficient scene management, we explicitly separate high-value instances from the background. These high-value instances are made replaceable, and the motions of dynamic objects can be interactively edited via a user interface.

In many cases, we need to remove certain foreground instances from the reconstructed 3D assets after UI-based editing over the entire sensor clip, while keeping the previously occluded regions spatially and visually coherent. To this end, we introduce an intermediate procedure that follows the vanilla PatchMatch philosophy but operates directly on 3D reconstructed Gaussians, which we term GS-RoadPatching [3].

![[3] GS-RoadPatching](image-4.png)

### Key Procedure 3: Expansive the Reconstruction via Diffusion

![[4] RGE-GS](image-5.png)

Next, to enable physically coherent free-viewpoint novel view synthesis, we develop specialized approaches for both cameras and LiDAR. On the camera side, we adopt RGE-GS [4], and on the LiDAR side, we extend LiDAR-GS [5] to LiDAR-GS++ [6]. Both are designed to cooperate with diffusion models to expand the reconstructed regions while preserving consistency with real-world sensor observations.

![[6] LiDAR-GS++](image-3.png)

### Ongoing Submissions

We also have several ongoing submissions under review that address remaining technical challenges and move us toward a more comprehensive conclusion of the Generative Reconstruction Suite. Specifically, we are investigating:

- How to accelerate 3D reconstruction while maintaining high fidelity, for example via modern feed-forward fashions.
- How to more efficiently and effectively fine-tune the blending between mixed foreground and background regions.
- How to robustly retrieve desired 3D instances from an ever-growing instance database, and further refine or adapt them in a prompt-based manner.