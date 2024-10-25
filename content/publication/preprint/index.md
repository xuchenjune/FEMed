---
title: "Few Exemplar-Based General Medical Image Segmentation via Domain-Aware Selective Adaptation"
authors:
#- admin
date: "2024-09-20T00:00:00Z"
doi: ""

# Schedule page publish date (NOT publication's date).
publishDate: "2017-01-01T00:00:00Z"

# Publication type.
# Accepts a single type but formatted as a YAML list (for Hugo requirements).
# Enter a publication type from the CSL standard.
publication_types: ["article"]

# Publication name and optional abbreviated publication name.
publication: ""
publication_short: ""

abstract: Medical image segmentation poses challenges due to domain gaps, data modality variations, and dependency on domain knowledge or experts, especially for low- and middle-income countries (LMICs). Whereas for humans, given a few exemplars (with corresponding labels), we are able to segment different medical images even without extensive domain-specific clinical training. In addition, current SAM-based medical segmentation models use fine-grained visual prompts, such as the maximum bounding rectangle generated from manually annotated lesion area segmentation masks, as bounding box prompt during the testing phase. However, in actual clinical diagnosis, no prior konwledge is avaiable for such fine-grained visual prompt. Our experimental results also reveal that previoums models nearly fail to predict when given coarser bbox prompts. Considering these drawbacks, we propose a domain-aware selective adaptation approach to adapt the general knowledge learned from a large model trained with natural images to the corresponding medical domains/modalities with access to only a few (e.g., less than 5) exemplars. Our method mitigates the aforementioned limitations, providing an efficient and LMICs-friendly solution. Extensive experimental analysis showcases the effectiveness of our approach, offering potential advancements in healthcare diagnostics and clinical applications in LMICs.

# Summary. An optional shortened abstract.
summary: Image segmentation · selective adaptation · few exemplar

tags:
- Source Themes
featured: false

links:
- name: Group Home Page
  url: https://mix.jianbojiao.com/#:~:text=We%20are%20the%20Machine%20Intelligence%20+%20x%20group%20at%20the
url_pdf: FEMedSegment.pdf #https://arxiv.org/abs/2410.09254
url_code: 'https://github.com/xuchenjune/FEMedSegment'
#url_dataset: '#'
#url_poster: '#'
url_project: 'https://xuchenjune.github.io/FEMed/'
#url_slides: ''
#url_source: '#'
#url_video: '#'

# Featured image
# To use, add an image named `featured.jpg/png` to your page's folder. 
image:
  caption: 'Image credit: [**Unsplash**](https://unsplash.com/photos/s9CC2SKySJM)'
  focal_point: ""
  preview_only: false

# Associated Projects (optional).
#   Associate this publication with one or more of your projects.
#   Simply enter your project's folder or file name without extension.
#   E.g. `internal-project` references `content/project/internal-project/index.md`.
#   Otherwise, set `projects: []`.
projects:
- internal-project

# Slides (optional).
#   Associate this publication with Markdown slides.
#   Simply enter your slide deck's filename without extension.
#   E.g. `slides: "example"` references `content/slides/example/index.md`.
#   Otherwise, set `slides: ""`.
slides: example
---
