# :package: Gitlab python package template

This is cookiecutter template for generation python package
project with gitlab ci/cd included.

---

## :cake: How to use it

`pip install cookiecutter`

`cookiecutter https://github.com/KochankovID/Gitlab-python-package-template.git`

## ⚙️️ GitLab CI/CD environs

> You need to set these variables in the repository settings.

- **PAKAGE_REGISTRY** - url on package registry. Needed for package uploading
  from ci/cd.
  > You can take it from pyproject.toml after project generation
  > _tool.semantic_release.repository_url_
- **GL_TOKEN** - personal access token for GitLab. Needed for making version
  bumping commits from ci/cd.
- **DEPLOY_TOKEN_NAME** - Name of the access token for package registry. Needed for package uploading
  from ci/cd.
- **DEPLOY_TOKEN** - The access token for package registry. Needed for package uploading
  from ci/cd.

## 🧸 Summarise

1. `pip install cookiecutter`
2. `cookiecutter https://github.com/KochankovID/Gitlab-python-package-template.git`
3. Fill ci/cd variables
4. ✨
