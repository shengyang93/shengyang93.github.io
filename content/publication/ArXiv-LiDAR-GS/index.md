---
title: "LiDAR-GS:Real-time LiDAR Re-Simulation using Gaussian Splatting"
authors:
- Qifeng Chen
- admin
- Sicong Du
- Tao Tang
- Peng Chen
- Yuchi Huo
author_notes:
-
- "†"
-
-
-
-
date: "2024-10-07T00:00:00Z"
# doi:  ""

# Schedule page publish date (NOT publication's date).
publishDate: "2024-10-07T00:00:00Z"

# Publication type.
# Accepts a single type but formatted as a YAML list (for Hugo requirements).
# Enter a publication type from the CSL standard.
publication_types: ["article"]

# Publication name and optional abbreviated publication name.
publication: "ArXiv Preprint"

abstract: We present LiDAR-GS, a Gaussian Splatting (GS) method for real-time, high-fidelity re-simulation of LiDAR scans in public urban road scenes. Recent GS methods proposed for cameras have achieved significant advancements in real-time rendering beyond Neural Radiance Fields (NeRF). However, applying GS representation to LiDAR, an active 3D sensor type, poses several challenges that must be addressed to preserve high accuracy and unique characteristics. Specifically, LiDAR-GS designs a differentiable laser beam splatting, using range-view representation for precise surface splatting by projecting lasers onto micro cross-sections, effectively eliminating artifacts associated with local affine approximations. Furthermore, LiDAR-GS leverages Neural Gaussian Representation, which further integrate view-dependent clues, to represent key LiDAR properties that are influenced by the incident direction and external factors. Combining these practices with some essential adaptations, e.g., dynamic instances decomposition, LiDAR-GS succeeds in simultaneously re-simulating depth, intensity, and ray-drop channels, achieving state-of-the-art results in both rendering frame rate and quality on publically available large scene datasets when compared with the methods using explicit mesh or implicit NeRF.

# Summary. An optional shortened abstract.
# summary: Lorem ipsum dolor sit amet, consectetur adipiscing elit. Duis posuere tellus ac convallis placerat. Proin tincidunt magna sed ex sollicitudin condimentum.

tags:
  - 3D Reconstruction

featured: true

url_pdf: https://arxiv.org/pdf/2410.05111v2
url_code: 'https://www.github.com/cqf7419/LiDAR-GS'
url_dataset: ''
url_poster: ''
url_project: ''
url_slides: ''
url_source: ''
url_video: ''

# Featured image
# To use, add an image named `featured.jpg/png` to your page's folder.
image:
  caption: ''
  focal_point: ''
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
