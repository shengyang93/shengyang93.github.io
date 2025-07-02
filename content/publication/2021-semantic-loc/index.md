---
title: 'Road Mapping and Localization Using Sparse Semantic Visual Features'

# Authors
# If you created a profile for a user (e.g. the default `admin` user), write the username (folder name) here
# and it will be replaced with their full name and linked to their profile.
authors:
  - Wentao Cheng
  - admin
  - Maomin Zhou
  - Ziyuan Liu
  - Yiming Chen
  - Mingyang Li
# Author notes (optional)
author_notes:
  - "*"
  - "*"
  - 
  - 
  - 
  - 

date: '2021-03-25T00:00:00Z'
# doi:  '10.1109/ICRA.2019.8794299'

# Schedule page publish date (NOT publication's date).
publishDate: '2021-03-25T00:00:00Z'

# Publication type.
# Accepts a single type but formatted as a YAML list (for Hugo requirements).
# Enter a publication type from the CSL standard.
publication_types: ["article-journal"]

# Publication name and optional abbreviated publication name.
publication: IEEE Robotics and Automation Letters
publication_short: "**ICRA (with RAL)**"

abstract: We present a novel method for visual mapping and localization for autonomous vehicles, by extracting, modeling, and optimizing semantic road elements. Specifically, our method integrates cascaded deep models to detect standardized road elements instead of traditional point features, to seek for improved pose accuracy and map representation compactness. To utilize the structural features, we model road lights and signs by their representative deep keypoints for skeleton and boundary, and parameterize lanes via piecewise cubic splines. Based on the road semantic features, we build a complete pipeline for mapping and localization, which includes a) image processing front-end, b) sensor fusion strategies, and c) optimization back-end. Experiments on public datasets and our testing platform have demonstrated the effectiveness and advantages of our method by outperforming traditional approaches.

# Summary. An optional shortened abstract.
# summary: Lorem ipsum dolor sit amet, consectetur adipiscing elit. Duis posuere tellus ac convallis placerat. Proin tincidunt magna sed ex sollicitudin condimentum.

tags:
  - SLAM
  - ICRA

# Display this page in the Featured widget?
featured: false

# Custom links (uncomment lines below)
# links:
# - name: Custom Link
#   url: http://example.org

url_pdf: 'https://arxiv.org/pdf/2108.05047'
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
