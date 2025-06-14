---
title: 'Probabilistic Projective Association and Semantic Guided Relocalization for Dense Reconstruction'

# Authors
# If you created a profile for a user (e.g. the default `admin` user), write the username (folder name) here
# and it will be replaced with their full name and linked to their profile.
authors:
  - admin
  - Zheng-Fei Kuang
  - Yan-Pei Cao
  - Yu-Kun Lai
  - Shi-Min Hu
# Author notes (optional)
author_notes:
  - "Corresponding Author"
  - 
  - 
  - 
  - 

date: '2019-05-20T00:00:00Z'
# doi:  '10.1109/ICRA.2019.8794299'

# Schedule page publish date (NOT publication's date).
publishDate: '2019-05-20T00:00:00Z'

# Publication type.
# Accepts a single type but formatted as a YAML list (for Hugo requirements).
# Enter a publication type from the CSL standard.
publication_types: ['paper-conference']

# Publication name and optional abbreviated publication name.
publication: IEEE International Conference on Robotics and Automation
publication_short: ICRA

abstract: We present a real-time dense mapping system which uses the predicted 2D semantic labels for optimizing the geometric quality of reconstruction. With a combination of Convolutional Neural Networks (CNNs) for 2D labeling and a Simultaneous Localization and Mapping (SLAM) system for camera trajectory estimation, recent approaches have succeeded in incrementally fusing and labeling 3D scenes. However, the geometric quality of the reconstruction can be further improved by incorporating such semantic prediction results, which is not sufficiently exploited by existing methods. In this paper, we propose to use semantic information to improve two crucial modules in the reconstruction pipeline, namely tracking and loop detection, for obtaining mutual benefits in geometric reconstruction and semantic recognition. Specifically for tracking, we use a novel probabilistic projective association approach to efficiently pick out candidate correspondences, where the confidence of these correspondences is quantified concerning similarities on all available short-term invariant features. For the loop detection, we incorporate these semantic labels into the original encoding through Randomized Ferns to generate a more comprehensive representation for retrieving candidate loop frames. Evaluations on a publicly available synthetic dataset have shown the effectiveness of our approach that considers such semantic hints as a reliable feature for achieving higher geometric quality.

# Summary. An optional shortened abstract.
# summary: Lorem ipsum dolor sit amet, consectetur adipiscing elit. Duis posuere tellus ac convallis placerat. Proin tincidunt magna sed ex sollicitudin condimentum.

tags:
  - 3D Reconstruction
  - ICRA

# Display this page in the Featured widget?
featured: false

# Custom links (uncomment lines below)
# links:
# - name: Custom Link
#   url: http://example.org

url_pdf: 'https://ieeexplore.ieee.org/document/8794299'
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
