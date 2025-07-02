---
title: 'DIDO: Deep Inertial Quadrotor Dynamical Odometry'

# Authors
# If you created a profile for a user (e.g. the default `admin` user), write the username (folder name) here
# and it will be replaced with their full name and linked to their profile.
authors:
  - Kunyi Zhang
  - Chenxing Jiang
  - Jinghang Li
  - admin
  - Teng Ma
  - Chao Xu
  - Fei Gao
# Author notes (optional)
author_notes:
  -
  -
  - 
  - 
  - 
  - 
  -

date: '2022-07-07T00:00:00Z'
# doi:  '10.1109/ICRA.2019.8794299'

# Schedule page publish date (NOT publication's date).
publishDate: '2022-07-07T00:00:00Z'

# Publication type.
# Accepts a single type but formatted as a YAML list (for Hugo requirements).
# Enter a publication type from the CSL standard.
publication_types: ["article-journal"]

# Publication name and optional abbreviated publication name.
publication: IEEE Robotics and Automation Letters
publication_short: "IROS (with RAL)"

abstract: In this work, we propose an interoceptive-only state estimation system for a quadrotor with deep neural network processing, where the quadrotor dynamics is considered as a perceptive supplement of the inertial kinematics. To improve the precision of multi-sensor fusion, we train cascaded networks on real-world quadrotor flight data to learn IMU kinematic properties, quadrotor dynamic characteristics, and motion states of the quadrotor along with their uncertainty information, respectively. This encoded information empowers us to address the issues of IMU bias stability, quadrotor dynamics, and multi-sensor calibration during sensor fusion. The above multi-source information is fused into a two-stage Extended Kalman Filter (EKF) framework for better estimation. Experiments have demonstrated the advantages of our proposed work over several conventional and learning-based methods.

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

url_pdf: 'https://ieeexplore.ieee.org/document/9817624'
url_code: 'https://github.com/zhangkunyi/DIDO/'
url_dataset: ''
url_poster: ''
url_project: ''
url_slides: ''
url_source: ''
url_video: 'https://www.bilibili.com/video/BV1dU4y1Z773'

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
