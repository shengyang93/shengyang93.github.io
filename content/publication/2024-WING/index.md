---
title: 'WING: Wheel-Inertial Neural Odometry with Ground Manifold Constraints'

# Authors
# If you created a profile for a user (e.g. the default `admin` user), write the username (folder name) here
# and it will be replaced with their full name and linked to their profile.
authors:
  - Chenxing Jiang
  - Kunyi Zhang
  - admin
  - Shaojie Shen
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

date: '2024-07-16T00:00:00Z'
# doi:  '10.1109/ICRA.2019.8794299'

# Schedule page publish date (NOT publication's date).
publishDate: '2024-07-16T00:00:00Z'

# Publication type.
# Accepts a single type but formatted as a YAML list (for Hugo requirements).
# Enter a publication type from the CSL standard.
publication_types: ["article-journal"]

# Publication name and optional abbreviated publication name.
publication: IEEE Transactions on Intelligent Vehicles
publication_short: "**TIV**"

abstract: In this paper, we propose an interoceptive-only odometry system for ground robots with neural network processing and soft constraints based on the assumption of a globally continuous ground manifold. Exteroceptive sensors such as cameras, GPS and LiDAR may encounter difficulties in scenarios with poor illumination, indoor environments, dusty areas and straight tunnels. Therefore, improving the pose estimation accuracy only using interoceptive sensors is important to enhance the reliability of navigation system even in degrading scenarios mentioned above. However, interoceptive sensors like IMU and wheel encoders suffer from large drift due to noisy measurements. To overcome these challenges, the proposed system trains deep neural networks to correct the measurements from IMU and wheel encoders, while considering their uncertainty. Moreover, because ground robots can only travel on the ground, we model the ground surface as a globally continuous manifold using a dual cubic B-spline manifold to further improve the estimation accuracy by this soft constraint. A novel space-based sliding-window filtering framework is proposed to fully exploit the C2 continuity of ground manifold soft constraints and fuse all the information from raw measurements and neural networks in a yaw-independent attitude convention. Extensive experiments demonstrate that our proposed approach can outperform state-of-the-art learning-based interoceptive-only odometry methods.

# Summary. An optional shortened abstract.
# summary: Lorem ipsum dolor sit amet, consectetur adipiscing elit. Duis posuere tellus ac convallis placerat. Proin tincidunt magna sed ex sollicitudin condimentum.

tags:
  - SLAM
  - TIV

# Display this page in the Featured widget?
featured: false

# Custom links (uncomment lines below)
# links:
# - name: Custom Link
#   url: http://example.org

url_pdf: 'https://arxiv.org/pdf/2407.10101'
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
