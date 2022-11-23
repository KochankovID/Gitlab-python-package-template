# :package: Gitlab python package template

This is cookiecutter template for generation python package
project with gitlab ci/cd included.

---

## :cake: How to use it

`pip install cookiecutter`

`cookiecutter https://github.com/KochankovID/Gitlab-python-package-template.git`

## ⚙️️ GitLab CI/CD environs

> You need to set these variables in the repository settings.

- **`GL_TOKEN`** - personal access token for GitLab. Needed for making version
  bumping commits from ci/cd.
- **`REPOSITORY_USERNAME`** - Name of the access token for package registry.
  Needed for package uploading from ci/cd.
- **`REPOSITORY_PASSWORD`** - The access token for package registry. Needed for
  package uploading from ci/cd.

## 🧸 Summarise

1. `pip install cookiecutter`
2. `cookiecutter https://github.com/KochankovID/Gitlab-python-package-template.git`
3. Fill ci/cd variables
4. ✨

## ✨ Features

- [x] GitLab CI/CD
-
    - [x] Linters (pre-commit)
-
    -
        - [x] Trailing-whitespace
-
    -
        - [x] Pyupgrade
-
    -
        - [x] Prettier
-
    -
        - [x] Isort
-
    -
        - [x] Black
-
    -
        - [x] Flake 8
-
    -
        - [x] Mypy
-
    -
        - [x] Pylint
-
    -
        - [x] Docstring formatter
-
    -
        - [x] Autoflake
-
    -
        - [x] Poetry check
-
    - [x] Tests
-
    - [x] Release (tag version bumping)
-
    - [ ] Documentation (TODO)
- [x] Pre-commit hooks
- [x] Readme
- [x] Contributing
- [x] License
