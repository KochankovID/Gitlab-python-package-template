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

## 😊 Emoji Commit Messages

This project uses [gitmoji](https://gitmoji.dev/) for emoji commit messages. 
It's a great way to add some fun to your commits and make them more readable.

`Python Semantic Release` uses gitmoji to generate changelog, release notes and
version number. 

**So, please, use gitmoji in your commit messages.**

## 🚀 Deploy to GitLab Package Registry

### Add gitlab deploy token to your poetry config

```bash
poetry config http-basic.gitlab $GL_USERNAME $GL_TOKEN --local
```

### Build and deploy package

```bash
semantic-release publish
```
