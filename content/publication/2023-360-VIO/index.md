---
title: '360-VIO: A Robust Visual-Inertial Odometry Using a 360° Camera'

# Authors
# If you created a profile for a user (e.g. the default `admin` user), write the username (folder name) here
# and it will be replaced with their full name and linked to their profile.
authors:
  - Qi Wu
  - Xiangyu Xu
  - Xieyuanli Chen
  - Ling Pei
  - Chao Long
  - Junyuan Deng
  - Guoqing Liu
  - admin
  - Shilei Wen
  - Wenxian Yu
# Author notes (optional)
author_notes:
  - 
  - 
  - 
  - 
  - 
  - 
  - 
  - 
  - 
  - 

date: '2023-12-25T00:00:00Z'
# doi:  '10.1109/ICRA.2019.8794299'

# Schedule page publish date (NOT publication's date).
publishDate: '2023-12-25T00:00:00Z'

# Publication type.
# Accepts a single type but formatted as a YAML list (for Hugo requirements).
# Enter a publication type from the CSL standard.
publication_types: ["article-journal"]

# Publication name and optional abbreviated publication name.
publication: IEEE Transactions on Industrial Electronics

abstract: Visual-inertial odometry (VIO) is an important component for robots working in industrial environments to obtain accurate and robust pose estimation. In this article, we introduce a novel VIO algorithm designed specifically for 360° cameras, exploiting their wide field of view. We build our algorithm based on an EKF-based filtering framework and propose a novel measurement model for 360° camera leveraging the reprojection error on the tangent plane of the spherical surface. By this, our 360-VIO effectively mitigates errors caused by the image distortion and fully exploit the omnidirectional observation, resulting in superior accuracy and robustness toward illumination changes and fast camera movements. To the best of our knowledge, no public 360-based visual-inertial dataset is currently available. To address this gap, we have constructed a novel 360° camera dataset under different challenging environments to evaluate the performance of our proposed algorithm. The results of our experiments demonstrate the impressive robustness and accuracy of our method compared with other state-of-the-art VIO methods across diverse and challenging environments.

# Summary. An optional shortened abstract.
# summary: Lorem ipsum dolor sit amet, consectetur adipiscing elit. Duis posuere tellus ac convallis placerat. Proin tincidunt magna sed ex sollicitudin condimentum.

tags:
  - SLAM
  - TIE

# Display this page in the Featured widget?
featured: false

# Custom links (uncomment lines below)
# links:
# - name: Custom Link
#   url: http://example.org

url_pdf: 'https://ieeexplore.ieee.org/document/10373205'
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
