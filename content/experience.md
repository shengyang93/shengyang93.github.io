---
title: 'Experience'
date: 2023-10-24
type: landing

design:
  spacing: '3rem'

# Note: `username` refers to the user's folder name in `content/authors/`

# Page sections
sections:
  - block: resume-experience
    content:
      username: admin
    design:
      # Hugo date format
      date_format: 'January 2006'
      # Education or Experience section first?
      is_education_first: false
  # - block: resume-skills
  #   content:
  #     title: Teaching
  #     username: admin
  #   design:
  #     show_skill_percentage: false
  - block: markdown
    content:
      title: 'Academic Services'
      text: |-
        - **Journal Reviewer**
          - ACM TOG, IEEE TVCG, IEEE RA-L, CGF, RAS.
        - **Conference Reviewer**
          - ICRA, IROS, CVPR, ICCV, IEEE VR;
          - CVM, GMOD, PG, TVC, VRST, IJPRAI, 3DV, etc.
        - **Conference Program Committee**
          - Computational Visual Media.
  - block: markdown
    content:
      title: 'Funding'
      text: |-
        - **Low-cost Learning-based Multi-sensor Localization**
          - Alibaba-Zhejiang University Joint Institute of Frontier Technologies (AZFT). 
          - 2022-2023. Project Leader. 
          - Cultivated 1 Ph.D. and 1 bachelor research interns.
          - Published 1 TIV, 1 ICRA, and 1 IROS papers.
        - **LiDAR Point Cloud Feature Extraction and SLAM**
          - Alibaba Innovative Research (AIR).
          - 2021-2022. Project Leader.
          - Cultivated 2 Ph.D. research interns.
          - Published 1 ECCV paper.
  - block: experience
    content:
      title: Funding
      date_format: 2006
      items:
        - title: Low-cost Learning-based Multi-sensor Localization
          company: Alibaba-Zhejiang University Joint Institute of Frontier Technologies (AZFT)
          date_start: '2022-01-01'
          date_end: '2023-01-01'
          description: |2-
              Cultivated 1 Ph.D. and 1 bachelor research interns.

              Published 1 TIV, 1 ICRA, and 1 IROS papers.
        - title: Low-cost Learning-based Multi-sensor Localization
          company: Alibaba Innovative Research (AIR)
          date_start: '2021-01-01'
          date_end: '2022-01-01'
          description: |2-
              Cultivated 2 Ph.D. research interns.

              Published 1 ECCV paper.
    design:
      columns: '1'
  - block: markdown
    content:
      title: 'Teaching Assistant'
      text: |-
        - **Advanced Computer Graphics**
          - Tsinghua University. 2017-2018. 2 semesters.
          - Post-graduate course. 
        - **Fundamental of Computer Graphics**
          - Tsinghua University. 2016-2018. 3 semesters, 2 classes for each.
          - Under-graduate course, including [Yao class](https://iiis.tsinghua.edu.cn/en/yaoclass/). National Excellent Courses.
        - **C++ Programming**
          - Tsinghua University. 2015. 1 semester.
          - Under-graduate course.
  # - block: resume-awards
  #   content:
  #     title: Teaching
  #     username: admin
  # - block: resume-languages
  #   content:
  #     title: Languages
  #     username: admin
---
