# 📦 {{cookiecutter.package_name}}

{{cookiecutter.description}}

---

## ⬇️ Installation

### 🔑 Get access token for `{{cookiecutter.package_registry_repository_name}}` repository

> Get personal access token for python-package-index repository
> from [GitLab](https://{{cookiecutter.gitlab_host}}/-/profile/personal_access_tokens)

```bash
export GL_USERNAME=<your_gitlab_username> # <- your gitlab username
export GL_TOKEN=<your_personal_access_token> # <- your personal access token
```

where:

- `GL_USERNAME` - your gitlab username (for example ilya)
- `GL_TOKEN` - your personal access token with access to python-package-index
  repository (for example 5WJpU5v_ms53z6xDt_nG)

> full example:
>
> ```bash
> export GL_USERNAME=ilya
> export GL_TOKEN=5WJpU5v_ms53z6xDt_nG
> ```

### 🐍 PIP

```bash
pip install {{cookiecutter.package_name}} --extra-index-url https://$GL_USERNAME:$GL_TOKEN{{cookiecutter.gitlab_host}}/api/v4/projects/{{cookiecutter.package_registry_repository_id}}/packages/pypi/simple
```

### 🍯 Poetry

#### 1. Add gitlab repository to your poetry config

```bash
poetry config repositories.gitlab https://{{cookiecutter.gitlab_host}}/api/v4/projects/{{cookiecutter.package_registry_repository_id}}/packages/pypi/simple --local
```

#### 2. Add gitlab personal access token to your poetry config

```bash
poetry config http-basic.gitlab $GL_USERNAME $GL_TOKEN --local
```

#### 3. Add gitlab repository to your pyproject.toml

```toml
[[tool.poetry.source]]
name = "gitlab"
url = "https://{{cookiecutter.gitlab_host}}/api/v4/projects/{{cookiecutter.package_registry_repository_id}}/packages/pypi/simple/"
```

#### 4. Install package

```bash
poetry add {{cookiecutter.package_name}} --source gitlab
```

## 🎂 Usage

```python
""" Rock Paper Scissors
----------------------------------------
"""
import random
import os
import re

os.system('cls' if os.name == 'nt' else 'clear')

while (1 < 2):
    print("\n")
    print("Rock, Paper, Scissors - Shoot!")
    userChoice = input("Choose your weapon [R]ock], [P]aper, or [S]cissors: ")
    if not re.match("[SsRrPp]", userChoice):
        print("Please choose a letter:")
        print("[R]ock, [S]cissors or [P]aper.")
        continue
    # Echo the user's choice
    print("You chose: " + userChoice)
    choices = ['R', 'P', 'S']
    opponenetChoice = random.choice(choices)
    print("I chose: " + opponenetChoice)
    if opponenetChoice == str.upper(userChoice):
        print("Tie! ")
    # if opponenetChoice == str("R") and str.upper(userChoice) == "P"
    elif opponenetChoice == 'R' and userChoice.upper() == 'S':
        print("Scissors beats rock, I win! ")
        continue
    elif opponenetChoice == 'S' and userChoice.upper() == 'P':
        print("Scissors beats paper! I win! ")
        continue
    elif opponenetChoice == 'P' and userChoice.upper() == 'R':
        print("Paper beat rock, I win!")
        continue
    else:
        print("You win!")
```

## 🎩 Contributing

Read our [guide](CONTRIBUTING.md) to contribute.
