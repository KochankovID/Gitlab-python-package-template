# :tophat: Contributing

---

## Setting up for development

### :snake: Pip

- `pip install -r requirements.txt`

### :honey_pot: Poetry

- `poetry install`
- `poetry shell`

## :runner: Run

### :white_check_mark: Run all tests (with py3.9 and py3.10) and linters

`tox`

### :heavy_check_mark: Run only pytest

`pytest`

### :100: Run only linters

`tox -e lint`

### :trident: Run pre-commit hooks

- `pre-commit install`
- `pre-commit run --all-files`
