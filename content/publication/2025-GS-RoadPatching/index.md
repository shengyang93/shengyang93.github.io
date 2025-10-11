---
title: 'GS-RoadPatching: Inpainting Gaussians via 3D Searching and Placing for Driving Scenes'

# Authors
# If you created a profile for a user (e.g. the default `admin` user), write the username (folder name) here
# and it will be replaced with their full name and linked to their profile.
authors:
- Guo Chen
- Jiarun Liu
- Sicong Du
- Chenming Wu
- Deqi Li
- Shi-Sheng Huang
- Guofeng Zhang
- admin
# Author notes (optional)
author_notes:
  - "*"
  - "*"
  - 
  - 
  - 
  - "†"
  - 
  - "†"

date: '2025-10-01T00:00:00Z'
# doi:  '10.1109/ICCV.2019.00597'

# Schedule page publish date (NOT publication's date).
publishDate: '2025-10-01T00:00:00Z'

# Publication type.
# Accepts a single type but formatted as a YAML list (for Hugo requirements).
# Enter a publication type from the CSL standard.
publication_types: ['paper-conference']

# Publication name and optional abbreviated publication name.
publication: ACM SIGGRAPH Conference and Exhibition on Computer Graphics and Interactive Techniques in Asia
publication_short: "SIGGRAPH Asia"

abstract: This paper presents GS-RoadPatching, an inpainting method for driving scene completion by referring to completely reconstructed regions, which are represented by 3D Gaussian Splatting (3DGS). Unlike existing 3DGS inpainting methods that perform generative completion relying on 2D perspective-view-based diffusion or GAN models to predict limited appearance or depth cues for missing regions, our approach enables substitutional scene inpainting and editing directly through the 3DGS modality, extricating it from requiring spatial-temporal consistency of 2D cross-modals and eliminating the need for time-intensive retraining of Gaussians. Our key insight is that the highly repetitive patterns in driving scenes often share multi-modal similarities within the implicit 3DGS feature space and are particularly suitable for structural matching to enable effective 3DGS-based substitutional inpainting. Practically, we construct feature-embedded 3DGS scenes to incorporate a patch measurement method for abstracting local context at different scales and, subsequently, propose a structural search method to find candidate patches in 3D space effectively. Finally, we propose a simple yet effective substitution-and-fusion optimization for better visual harmony. We conduct extensive experiments on multiple publicly available datasets to demonstrate the effectiveness and efficiency of our proposed method in driving scenes, and the results validate that our method achieves state-of-the-art performance compared to the baseline methods in terms of both quality and interoperability. Additional experiments in general scenes also demonstrate the applicability of the proposed 3D inpainting strategy.

# Summary. An optional shortened abstract.
# summary: Lorem ipsum dolor sit amet, consectetur adipiscing elit. Duis posuere tellus ac convallis placerat. Proin tincidunt magna sed ex sollicitudin condimentum.

tags:
  - 3DGS
  - SIGGRAPH Asia

# Display this page in the Featured widget?
featured: false

# Custom links (uncomment lines below)
# links:
# - name: Custom Link
#   url: http://example.org

url_pdf: 'https://arxiv.org/pdf/2509.19937'
url_code: 'https://shanzhaguoo.github.io/GS-RoadPatching/'

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
