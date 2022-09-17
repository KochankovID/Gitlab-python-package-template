# 🎩 Contributing

---

## Setting up for development

### 🐍 Pip

```bash
pip install -r requirements.txt
```

### 🍯 Poetry

```bash
poetry install
poetry shell
```

## 🏃 Run

### ✔️ Run all tests (with py3.9 and py3.10) and linters

```bash
tox
```

### ✅ Run only pytest

```bash
pytest
```

### 💯 Run only linters

```bash
tox -e lint
```

### 🔱 Run pre-commit hooks

```bash
pre-commit install
pre-commit run -a
```

## 🚀 Deploy to GitLab Package Registry

### Add gitlab deploy token to your poetry config

```bash
poetry config http-basic.gitlab gitlab-ci-token <your_personal_token> --local
```

where:

- <your_personal_token> - is your Deploy tokens with access to
  read_package_registry (for example 5WJpU5v_ms53z6xDt_nG)

full example:

```bash
poetry config http-basic.gitlab gitlab-ci-token 5WJpU5v_ms53z6xDt_nG
```
