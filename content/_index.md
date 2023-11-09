---
# Leave the homepage title empty to use the site title
title: 'Aleksei Zhuravlev'
type: landing

sections:
  - block: about.biography
    id: about
    content:
      title: Bio
      # Choose a user profile to display (a folder name within `content/authors/`)
      username: admin
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
        - title: Research Assistant
          company: ETH Zurich
          company_url: ''
          location: remote
          date_start: '2023-04-01'
          date_end: ''
          description: |2-
              Supervised by [Dr. Danda Pani Paudel](https://people.ee.ethz.ch/~paudeld/), [Dr. Thomas Probst](https://probstt.bitbucket.io/)<br>

              - Developed a NeRF-based 3D reconstruction of the human hand from 60 images; evaluated on ∼500 sequences from the Interhand3.6m dataset <br>
              - Implemented a point-mesh distance finding algorithm on the GPU; reduced the calculation time from 5s to 0.3s compared to the CPU baseline <br> 
              - Introduced perceptual loss (LPIPS) to enhance the visual quality; improved PSNR score by 14% over MSE loss <br>

        - title: Research Assistant
          company: Moscow State University
          company_url: ''
          location: Moscow, Russia
          date_start: '2019-11-01'
          date_end: '2022-02-01'
          description:  |2-
              Supervised by [Prof. Sergei Popov](https://scholar.google.com/citations?user=6wyyiLkAAAAJ&hl=en), [Prof. Roberto Turolla](https://www.unipd.it/en/contatti/rubrica/?ruolo=1&checkout=cerca&persona=TUROLLA&key=A1136CDCCF2710E5179BC83D6E291FBA)<br>
              
              - Developed a dark matter detection model using satellite images of neutron stars; processed 3.1 TB of data collected over 4 years <br>
              - Utilized Very Deep Super-Resolution (VDSR) network to upscale low-resolution satellite images; improved SSIM metric by 11% over the baseline bicubic interpolation <br>
              - Implemented a background subtraction model based on the R-CNN network; achieved a 3x speedup compared to the GrabCut algorithm <br>
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

  - block: portfolio
    id: additional_experience
    content:
      title: Additional Experience
      filters:
        folders:
          - additional_experience
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
      flip_alt_rows: false #any columns the section has. Valid values: '1' or '2'

  - block: accomplishments
    id: accomplishments
    content:
      title: Additional Experience
      subtitle: ''
      text: ''
      # Date format: https://wowchemy.com/docs/customization/#date-format
      date_format: Jan 2006
      # Accomplishments.
      #   Add/remove as many `items` blocks below as you like.
      #   `title`, `organization`, and `date_start` are the required parameters.
      #   Leave other parameters empty if not required.
      #   Begin multi-line descriptions with YAML's `|2-` multi-line prefix.
      items:
        - title: Teaching assistant, University of Bonn 
          certificate_url: ''
          date_start: '2019-11-01'
          date_end: '2022-02-01'
          description: '• Co-developed programming assignments for the “Computer Vision” course, attended by 30+ MSc students'
          url: ''
        - title: Teaching assistant, Moscow State University 
          certificate_url: ''
          date_end: '2022-02-01'
          date_start: '2021-01-01'
          description: • Instructed groups of 20 undergraduates in the “Programming and Computer Science” course; average grades 4.7 out of 5.0
        - title: Scholarship for outstanding students, Moscow State University
          date_end: '2020-12-21'
          date_start: '2020-07-01'
          description: '• Awarded to top 5% of all students'
        - title: Moscow Informatics Olympiad
          description: '• 3rd place out of 70+ teams'
          date_end: '2020-12-21'
          date_start: '2020-07-01'
    design:
      # Choose how many columns the section has. Valid values: '1' or '2'.
      columns: '2'


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
