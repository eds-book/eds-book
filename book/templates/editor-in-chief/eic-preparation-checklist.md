(templates-eic-preparation-checklist)=

```markdown
# Check notebook repository
- [ ] The notebook repository is available in a public personal repository
- [ ] The notebook runs in Binder according to the PR indicated by the author

# Initial configurations
- [ ] Create and checkout a new branch `preparation`
- [ ] Activate the conda environment containing Jupyter Book v2 and run `jupyter book init` to create myst.yml file.
- [ ] Move environment.yml file to `.binder` folder
- [ ] Rename the `name` field in `.binder/environment.yml` with project id defined in `myst.yml` file

# Set up Quay.io
- [ ] Create a new Quay.io repository with the same name as the project id defined in `myst.yml` file and another including the suffix `_preview` (e.g., `my-project-id` and `my-project_preview-id`)
- [ ] Assign in settings the `edsbook+github_actions` bot as a collaborator with write access to the Quay.io repository

# GitHub repository settings
- [ ] Set `QUAY_PASSWORD` and `QUAYUSERNAME` keys and values from the bot in the repository secrets (go to the repository settings, left panel > Secret and variables > Actions)
- [ ] Check that the GitHub pages are enabled in the repository settings using actions.

# README (python)
- [ ] Rename the filename of the template to notebook.ipynb
- [ ] Copy README template (python) and replace the fields in the following lines:
- [ ] replace `[repository name]` in 
  - [ ] L20, `git clone https://github.com/eds-book/[repository name].git`
  - [ ] L25, `cd [repository name]`
  - [ ] L31, `conda activate [repository name]`
    
# Validate preview
- [ ] Commit and push changes to the `preparation` branch
- [ ] Open a PR to the `main` branch with the title `preparation` and the description
- [ ] Check the publish action in the Actions tab runs successfully
- [ ] Validate the preview in GitHub pages at `https://eds-book.github.io/[repository name]/`
- [ ] If OK, merge the PR to the `main` branch.

```