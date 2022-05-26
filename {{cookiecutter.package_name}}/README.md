# :package: {{cookiecutter.package_name}}

{{cookiecutter.package_registry_repository_url}}

---

## :arrow_down: Installation

### :snake: PIP

`pip install funccacher --extra-index-url https://__token__:<your_personal_token>@gitlab.com/api/v4/projects/{{cookiecutter.package_registry_repository_id}}/packages/pypi/simple`

where:

- \_\_token\_\_ - is your Deploy token username (for example Ilya)
- <your_personal_token> - is your Deploy tokens with access to
  read_package_registry (for example 5WJpU5v_ms53z6xDt_nG)

> full example:
> `pip install funccacher --extra-index-url https://Ilya:5WJpU5v_ms53z6xDt_nG@gitlab.com/api/v4/projects/{{cookiecutter.package_registry_repository_id}}/packages/pypi/simple`

### :honey_pot: Poetry

1. `poetry config repositories.gitlab https://gitlab.com/api/v4/projects/{{cookiecutter.package_registry_repository_id}}/packages/pypi/simple`

2. `poetry config http-basic.gitlab gitlab-ci-token <your_personal_token>`

where:

- <your_personal_token> - is your Deploy tokens with access to
  read_package_registry (for example 5WJpU5v_ms53z6xDt_nG)

full example:
`poetry config http-basic.gitlab gitlab-ci-token 5WJpU5v_ms53z6xDt_nG`

3. Add to your pyproject.toml

```toml
[[tool.poetry.source]]
name = "gitlab"
url = "https://gitlab.com/api/v4/projects/{{cookiecutter.package_registry_repository_id}}/packages/pypi/simple/"
```

> the url will change is package register will change

4. Install command: `poetry add funccacher --source gitlab`

## :cake: Usage

```python
""" Rock Paper Scissors
----------------------------------------
"""
import random
import os
import re


os.system('cls' if os.name=='nt' else 'clear')

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
    #if opponenetChoice == str("R") and str.upper(userChoice) == "P"
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

## :tophat: Contributing

Read our [guide](CONTRIBUTING.md) to contribute.
