---
title: "HeteroFusion: Dense Scene Reconstruction Integrating Multi-Sensors"
authors:
- admin
- Beichen Li
- Minghua Liu
- Yu-Kun Lai
- Leif Kobbelt
- Shi-Min Hu
author_notes:
-
- 
- 
- 
- 
- 
date: "2019-05-28T00:00:00Z"
# doi:  "10.1109/TVCG.2019.2919619"

# Schedule page publish date (NOT publication's date).
publishDate: "2019-05-28T00:00:00Z"

# Publication type.
# Accepts a single type but formatted as a YAML list (for Hugo requirements).
# Enter a publication type from the CSL standard.
publication_types: ["article-journal"]

# Publication name and optional abbreviated publication name.
publication: "IEEE Transactions on Visualization and Computer Graphics"
publication_short: "**TVCG**"

abstract: We present a novel approach to integrate data from multiple sensor types for dense 3D reconstruction of indoor scenes in realtime. Existing algorithms are mainly based on a single RGBD camera and thus require continuous scanning of areas with sufficient geometric features. Otherwise, tracking may fail due to unreliable frame registration. Inspired by the fact that the fusion of multiple sensors can combine their strengths towards a more robust and accurate self-localization, we incorporate multiple types of sensors which are prevalent in modern robot systems, including a 2D range sensor, an inertial measurement unit (IMU), and wheel encoders. We fuse their measurements to reinforce the tracking process and to eventually obtain better 3D reconstructions. Specifically, we develop a 2D truncated signed distance field (TSDF) volume representation for the integration and ray-casting of laser frames, leading to a unified cost function in the pose estimation stage. For validation of the estimated poses in the loop-closure optimization process, we train a classifier for the features extracted from heterogeneous sensors during the registration progress. To evaluate our method on challenging use case scenarios, we assembled a scanning platform prototype to acquire real-world scans. We further simulated synthetic scans based on high-fidelity synthetic scenes for quantitative evaluation. Extensive experimental evaluation on these two types of scans demonstrate that our system is capable of robustly acquiring dense 3D reconstructions and outperforms state-of-the-art RGBD and LiDAR systems.

# Summary. An optional shortened abstract.
# summary: Lorem ipsum dolor sit amet, consectetur adipiscing elit. Duis posuere tellus ac convallis placerat. Proin tincidunt magna sed ex sollicitudin condimentum.

tags:
- 3D Reconstruction
- TVCG
featured: false

# links:
# - name: ""
#   url: ""
url_pdf: 'https://ieeexplore.ieee.org/document/8723521'
url_code: ''
url_dataset: ''
url_poster: ''
url_project: ''
url_slides: ''
url_source: ''
url_video: ''

# Featured image
# To use, add an image named `featured.jpg/png` to your page's folder. 
image:
  caption: ""
  focal_point: ""
  preview_only: false

# Associated Projects (optional).
#   Associate this publication with one or more of your projects.
#   Simply enter your project's folder or file name without extension.
#   E.g. `internal-project` references `content/project/internal-project/index.md`.
#   Otherwise, set `projects: []`.
projects: []

# Slides (optional).
#   Associate this publication with Markdown slides.
#   Simply enter your slide deck's filename without extension.
#   E.g. `slides: "example"` references `content/slides/example/index.md`.
#   Otherwise, set `slides: ""`.
slides: ""
---