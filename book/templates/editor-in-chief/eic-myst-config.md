(templates-eic-myst-config)=

```yaml
# See docs at: https://mystmd.org/guide/frontmatter
version: 1
extends:
  - https://raw.githubusercontent.com/eds-book/edsbook-config/main/edsbook.yml
project:
  id: [KEEP-THE-ORIGINAL-ID]
  title: [NOTEBOOK-TITLE] (Jupyter Notebook) published in the Environmental Data Science book
  short_title: [NOTEBOOK-SHORT-TITLE]
  abstract: Notebook developed to [SHORT-ABSTRACT].
  authors:
    - id: [SHORT-ID]
      name: [FIRST-AND-LAST-NAME]
      orcid: [ORCID]
      corresponding: true
      email: [EMAIL]
      github: [GITHUB-HANDLE]
      roles:
        - Investigation
        - Software
        - Visualization
      affiliations:
        - [ID-AFFILIATION]
#  reviewers:
#    - id: TBA
#      name: TBA
#      orcid: TBA
#      github: TBA
#      roles:
#        - Writing – review & editing
#      affiliations:
#        - TBA
#  editors:
#    - id: TBA
#      name: TBA
#      orcid: TBA
#      github: TBA
#      roles:
#        - Writing – review & editing
#      affiliations:
#        - TBA
  affiliations:
    - id: [ID-AFFILIATION]
      name: [AFFILIATION-NAME]
      department: [AFFILIATION-DEPARTMENT]
  subject: [SUBJECT] #according to Earth Engine Data Catalog categories, https://developers.google.com/earth-engine/datasets/categories
  keywords:
    - [SUBJECT]
    - [THEME]
    - [SUBMISSION]
    - [LANGUAGE]
  venue:
    title: Environmental Data Science Book
    short_title: EDS Book
    url: https://www.edsbook.org
  issue:
    name: [SUBMISSION-TYPE]
#  thumbnail: images/thumbnail.png
  requirements:
    - .binder/environment.yml
  #doi: 10.5281/zenodo.XXXXXXX
  github: https://github.com/eds-book/[KEEP-THE-ORIGINAL-ID]
  jupyter:
    binder:
      repo: eds-book/[KEEP-THE-ORIGINAL-ID]
  open_access: true
  license:
    content: CC-BY-4.0
    code: MIT
  date: YYYY-MM-DD
  toc:
    - file: README.md
    - file: notebook.ipynb
site:
  template: book-theme

```