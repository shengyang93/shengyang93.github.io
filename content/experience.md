---
title: 'Experience'
date: 2023-10-24
type: landing

design:
  spacing: '3rem'

# Note: `username` refers to the user's folder name in `content/authors/`

# Page sections
sections:
  # - block: experience
  #   content:
  #     username: admin
  #   design:
  #     # Hugo date format
  #     date_format: 'January 2006'
  #     # Education or Experience section first?
  #     is_education_first: false
  # - block: experience
  #   content:
  #     username: admin2
  #   design:
  #     # Hugo date format
  #     date_format: '2006'
  #     # Education or Experience section first?
  #     is_education_first: false
- block: experience
    content:
      title: Experience
      date_format: Jan 2006
      # Experiences.
      #   Add/remove as many experience `items` below as you like.
      #   Required fields are `title`, `company`, and `date_start`.
      #   Leave `date_end` empty if it's your current employer.
      #   Begin multi-line descriptions with YAML's `|2-` multi-line prefix.
      items:
        - title: Staff Research Scientist (Staff SDE)
          company: Unmanned Vehicle Dept., Cainiao Inc., Alibaba Group
          # company_url: ''
          # company_logo: org-gc
          location: Hangzhou, China
          date_start: '2024-04-01'
          date_end: ''
          description: |-
              Responsible for mass-production and cost-down of map and data.
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
  # - block: resume-awards
  #   content:
  #     title: Teaching
  #     username: admin
  # - block: resume-languages
  #   content:
  #     title: Languages
  #     username: admin
---
