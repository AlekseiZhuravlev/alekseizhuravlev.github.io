---
# Leave the homepage title empty to use the site title
title: 'Aleksei Zhuravlev'
type: landing

design:
  background:
    # Choose a color such as from https://html-color-codes.info
    color: 'white'
    # Text color (true=light, false=dark, or remove for the dynamic theme color).
    text_color_light: false

sections:
  - block: about.biography
    id: about
    content:
      title: Bio
      # Choose a user profile to display (a folder name within `content/authors/`)
      username: admin


  - block: portfolio
    id: projects
    content:
      title: Projects
      filters:
        folders:
          - project
      # Default filter index (e.g. 0 corresponds to the first `filter_button` instance below).
      default_button_index: 0
      # Filter toolbar (optional).
      # Add or remove as many filters (`filter_button` instances) as you like.
      # To show all items, set `tag` to "*".
      # To filter by a specific tag, set `tag` to an existing tag name.
      # To remove the toolbar, delete the entire `filter_button` block.
    design:
      # Choose how many columns the section has. Valid values: '1' or '2'.
      columns: '2'
      view: compact
      # For Showcase view, flip alternate rows?
      flip_alt_rows: false


  - block: experience
    id: experience
    content:
      title: Experience
      # Date format for experience
      #   Refer to https://wowchemy.com/docs/customization/#date-format
      date_format: Jan 2006
      # Experiences.
      #   Add/remove as many `experience` items below as you like.
      #   Required fields are `title`, `company`, and `date_start`.
      #   Leave `date_end` empty if it's your current employer.
      #   Begin multi-line descriptions with YAML's `|2-` multi-line prefix.
      items:

        - title: Denoising Diffusion for Mesh Correspondence
          company: Master Thesis
          company_url: ''
          location: University of Bonn
          date_start: '2024-04-01'
          date_end: ''
          description: |2-
              - Trained a Denoising Diffusion Model (DDPM) to find correspondence between 100 scans of humans from the FAUST dataset

        - title: Implicit Hand Reconstruction
          company: Internship
          company_url: ''
          location: ETH Zurich
          date_start: '2023-05-01'
          date_end: '2023-12-01'
          description: |2-
              - Developed a NeRF-based reconstruction of the human hand from 60 images, using the Interhand3.6m dataset

        - title: Human Pose Forecasting
          company: Semester Project
          company_url: ''
          location: University of Bonn
          date_start: '2023-04-01'
          date_end: '2023-09-01'
          description: |2-
              - Developed a human pose prediction model based on temporal convolution, trained on the Human2.6m dataset <br>

        - title: Segmentation of satellite images 
          company: Research Assistant
          company_url: ''
          location: Moscow State University
          date_start: '2019-11-01'
          date_end: '2022-02-01'
          description:  |2-
              - Utilized the Very Deep Super-Resolution (VDSR) network to upscale the low-resolution satellite images of neutron stars
              - Implemented a background subtraction model based on the R-CNN network; achieved a 3x speedup compared to the GrabCut algorithm

    design:
      columns: '2'


  - block: collection
    id: publications
    content:
      title: Publications
      filters:
        folders:
          - publication
    design:
      columns: '2'
      view: compact

  # - block: portfolio
  #   id: additional_experience
  #   content:
  #     title: Additional Experience
  #     filters:
  #       folders:
  #         - additional_experience
  #     default_button_index: 0
  #     # Filter toolbar (optional).
  #     # Add or remove as many filters (`filter_button` instances) as you like.
  #     # To show all items, set `tag` to "*".
  #     # To filter by a specific tag, set `tag` to an existing tag name.
  #     # To remove the toolbar, delete the entire `filter_button` block.
  #   design:
  #     # Choose how many columns the section has. Valid values: '1' or '2'.
  #     columns: '2'
  #     view: compact
  #     # For Showcase view, flip alternate rows?
  #     flip_alt_rows: false #any columns the section has. Valid values: '1' or '2'

  # - block: accomplishments
  #   id: accomplishments
  #   content:
  #     title: Additional Experience
  #     subtitle: ''
  #     text: ''
  #     # Date format: https://wowchemy.com/docs/customization/#date-format
  #     date_format: Jan 2006
  #     # Accomplishments.
  #     #   Add/remove as many `items` blocks below as you like.
  #     #   `title`, `organization`, and `date_start` are the required parameters.
  #     #   Leave other parameters empty if not required.
  #     #   Begin multi-line descriptions with YAML's `|2-` multi-line prefix.
  #     items:
  #       - title: Teaching assistant, Moscow State University 
  #         organization: ''
  #         certificate_url: ''
  #         date_end: '2022-02-01'
  #         date_start: '2021-01-01'
  #         description: • Instructed a group of 20 students in the course “Algorithms and Complexity”
  #       - title: Scholarship for outstanding students, Moscow State University
  #         organization: ''
  #         date_start: '2020-09-21'
  #         date_end: '2022-05-01'
  #         description: '• Awarded to top 5% of all students'
  #       - title: Moscow Informatics Olympiad
  #         organization: ''
  #         description: '• 3rd place out of 70 teams'
  #         date_end: ''
  #         date_start: '2020-05-01'
  #   design:
  #     # Choose how many columns the section has. Valid values: '1' or '2'.
  #     columns: '2'
  #     view: card


  # - block: collection
  #   content:
  #     title: Projects
  #     filters:
  #       folders:
  #         - project
  #   design:
  #     columns: '2'
  #     view: citation
---
