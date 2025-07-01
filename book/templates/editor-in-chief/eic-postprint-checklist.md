(templates-eic-preparation-checklist)=

```markdown
# Initial configurations
- [ ] Create and checkout a new branch `postprint`
- [ ] Remove files in the `images` folder
- [ ] Create and add `thumbnail.png` to the `images` folder
- [ ] Set `.bumpversion.cfg`

# Archive in Zenodo
- [ ] Create a Zenodo record for the notebook repository
- [ ] Use the nomenclature of the .bumpversion.cfg file to set the version number

# Notebook 
- [ ] Add `Citing this Notebook` section to the notebook before the `Additional Information` section. 
    ```markdown
    ## Citing this Notebook
    
    Please see [CITATION.cff](https://github.com/eds-book/[repository-name]/blob/main/CITATION.cff) for the full citation information. The citation file can be exported to APA or BibTex formats (learn more [here](https://docs.github.com/en/repositories/managing-your-repositorys-settings-and-features/customizing-your-repository/about-citation-files)).
    ```

# myst.yml file
- Complete missing fields in the `myst.yml` file:
    ```yaml
    project:
      reviewers:
        - id: TBA
          name: TBA
          orcid: TBA
          github: TBA
          roles:
            - Writing – review & editing
          affiliations:
            - TBA
      editors:
        - id: TBA
          name: TBA
          orcid: TBA
          github: TBA
          roles:
            - Writing – review & editing
          affiliations:
            - TBA
       thumbnail: images/thumbnail.png
       doi: 10.5281/zenodo.XXXXXXX
       date: YYYY-MM-DD
       exports:
        - format: cff
          version: [version]
          identifiers:
            - description: "Open review report for this notebook"
              type: url
              value: "https://github.com/eds-book/notebooks-reviews/issues/[review-issue]"
       bibliography:
        - references.bib
    ```
  
- Change the version in the cell `print('Notebook repository version: [version]')`

# README 
- [ ] Between the title and how to run sections, add the following lines replacing `[repository-name]`, `[zenodo-doi]`, `[zenodo-badge]` and `[review-issue]` in:
    ```markdown
    <p align="center">
        <a href="https://github.com/eds-book/[repository name]/actions/workflows/monthly-build.yaml/badge.svg">
            <img alt="Continuous integration badge" src="https://github.com/eds-book/[repository name]/actions/workflows/monthly-build.yaml/badge.svg">
        </a>
        <a href="http://mybinder.org/v2/gh/eds-book/[repository name]/main?labpath=notebook.ipynb">
            <img alt="Binder" src="https://mybinder.org/badge_logo.svg">
        </a>
        <a href="https://doi.org/10.5281/zenodo.[zenodo-doi]">
            <img alt="doi" src="https://zenodo.org/badge/[zenodo-badge].svg">
        </a>
        <a href="https://github.com/eds-book/notebooks-reviews/issues/[review-issue]">
            <img alt="notebook review" src="https://img.shields.io/badge/view-review-purple">
        </a>
    </p>
    
    <p align="center">
    <img src="images/thumbnail.png" alt="thumbnail" width="500"/>
    </p>
    ```

# Validate preview
- [ ] Commit and push changes to the `postprint` branch
- [ ] Open a PR to the `main` branch with the title `postprint` and the description
- [ ] Check the publish action in the Actions tab runs successfully
- [ ] Validate the preview in GitHub pages at `https://eds-book.github.io/[repository name]/`
- [ ] If OK, merge the PR to the `main` branch.

```