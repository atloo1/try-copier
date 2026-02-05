# try-copier

[![Dynamic TOML Badge](https://img.shields.io/badge/dynamic/toml?url=https%3A%2F%2Fraw.githubusercontent.com%2Fatloo1%2Ftry-copier-uv%2Frefs%2Fheads%2Fmain%2Fpyproject.toml&query=%24.project.requires-python&label=python)](https://github.com/atloo1/try-copier-uv/blob/main/pyproject.toml)
[![Dynamic TOML Badge](https://img.shields.io/badge/dynamic/toml?url=https%3A%2F%2Fraw.githubusercontent.com%2Fatloo1%2Ftry-copier-uv%2Frefs%2Fheads%2Fmain%2Fpyproject.toml&query=%24.project.version&label=version)](https://github.com/atloo1/try-copier-uv/blob/main/pyproject.toml)
[![GitHub License](https://img.shields.io/github/license/atloo1/try-copier-uv)](https://github.com/atloo1/try-copier-uv/blob/main/LICENSE)
![GitHub code size in bytes](https://img.shields.io/github/languages/code-size/atloo1/try-copier-uv)

[![pre-commit](https://img.shields.io/badge/pre--commit-enabled-brightgreen?logo=pre-commit&logoColor=white)](https://github.com/pre-commit/pre-commit)

Python project templating via [copier](https://copier.readthedocs.io/en/stable/), supporting automated [1] package management via [uv](https://docs.astral.sh/uv), [2] dependency updates via [Renovate](https://github.com/renovatebot/renovate?tab=readme-ov-file#what-is-the-mend-renovate-cli), [3] testing via [pytest](https://github.com/pytest-dev/pytest), [4] linting via [mypy](https://github.com/python/mypy) & [ruff](https://github.com/astral-sh/ruff), & [5] CI/CD via [GitHub Actions](https://docs.github.com/en/actions/about-github-actions/understanding-github-actions#workflows) & [pre-commit](https://github.com/pre-commit/pre-commit)

## use

### prerequisites

- [copier](https://copier.readthedocs.io/en/stable/#installation) (preferably via [uv](https://docs.astral.sh/uv/getting-started/installation/))

### create a templated repo

```
copier copy \
    https://github.com/atloo1/try-copier \
    test-try-copier \
    -d project_description='test try-copier' \
    -d project_name_kebab_case='test-try-copier' \
    --defaults \
    --trust
```

### update a templated repo

```
cd /path/to/downstream-templated-repo/
copier update --defaults --trust
```

## develop

### prerequisites

- [uv](https://docs.astral.sh/uv/getting-started/installation/)

### setup

```
git clone https://github.com/atloo1/try-copier
cd try-copier/
uv sync --group dev
uv run pre-commit install
```
