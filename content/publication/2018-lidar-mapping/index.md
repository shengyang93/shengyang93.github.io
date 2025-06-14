---
title: 'A robust pose graph approach for city scale LiDAR mapping'

# Authors
# If you created a profile for a user (e.g. the default `admin` user), write the username (folder name) here
# and it will be replaced with their full name and linked to their profile.
authors:
  - admin
  - Xiaoling Zhu
  - Xing Nian
  - Lu Feng
  - Xiaozhi Qu
  - Teng Ma
# Author notes (optional)
author_notes:
  - "Corresponding Author"
  - 
  - 
  - 
  - 
  - 

date: '2018-10-01T00:00:00Z'
doi: '10.1109/IROS.2018.8593754'

# Schedule page publish date (NOT publication's date).
publishDate: '2018-10-01T00:00:00Z'

# Publication type.
# Accepts a single type but formatted as a YAML list (for Hugo requirements).
# Enter a publication type from the CSL standard.
publication_types: ['paper-conference']

# Publication name and optional abbreviated publication name.
publication: IEEE/RSJ International Conference on Intelligent Robots and Systems
publication_short: IROS

abstract: This paper presents a method for reconstructing globally consistent 3D High-Definition (HD) maps at city scale. Current approaches for eliminating cumulative drift are mainly based on the pose graph optimization under the constraint of scan-matching factors. The misaligned edges in the graph may have negative impacts on the results. To address this problem and further handle inconsistency caused by multi-task acquisitions in urban environments, we introduce a refined structure of the factor graph considering systematical initialization bias, where the scan-matching factors are twice validated through a novel classifier and a robust optimization strategy. In addition, we incorporate a multi-hypothesis extended Kalman filter (MH-EKF) to remove dynamic objects. Quantitative experimental results demonstrate that the proposed method outperforms state-of-the-art techniques in terms of map quality.

# Summary. An optional shortened abstract.
# summary: Lorem ipsum dolor sit amet, consectetur adipiscing elit. Duis posuere tellus ac convallis placerat. Proin tincidunt magna sed ex sollicitudin condimentum.

tags:
  - SLAM
  - IROS

# Display this page in the Featured widget?
featured: false

# Custom links (uncomment lines below)
# links:
# - name: Custom Link
#   url: http://example.org

url_pdf: 'https://ieeexplore.ieee.org/abstract/document/8593754'
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
