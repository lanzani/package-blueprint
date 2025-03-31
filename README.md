# UV Package Blueprint

[![Copier](https://img.shields.io/endpoint?url=https://raw.githubusercontent.com/copier-org/copier/master/img/badge/badge-grayscale-border.json)](https://github.com/copier-org/copier)
[![uv](https://img.shields.io/endpoint?url=https://raw.githubusercontent.com/astral-sh/uv/main/assets/badge/v0.json)](https://github.com/astral-sh/uv)
[![Ruff](https://img.shields.io/endpoint?url=https://raw.githubusercontent.com/astral-sh/ruff/main/assets/badge/v2.json)](https://github.com/astral-sh/ruff)

[![GitHub Release](/reports/version-badge.svg?dummy=8484754)]()
[![Coverage Status](/reports/coverage-badge.svg?dummy=8484744)](./reports/coverage/index.html)

## Tecnology stack

- [uv](https://docs.astral.sh/uv/) for python and project manager
- [pre-commit](https://pre-commit.com/) with [ruff](https://docs.astral.sh/ruff/) to mantain code consistency and pre-commit checks
- [GitHub Actions](https://github.com/features/actions) to create release and publish package (also on a private registry)

## Usage

**Note**: You need [uv](https://docs.astral.sh/uv/) (and uv only) installed on your machine.

To create a package using this repo as template, install copier as an uv tool:

```bash
uv tool install copier
```

Then proceed with creating the package and answer the prompted questions:

```bash
copier copy https://github.com/lanzani/package-blueprint path/to/destination
```

## Update

You can update a child repo that has been created with this template by running:

```bash
copier update
```

## Setup GitHub Actions

If you are not going to publish your package on a private index you can skip this section! Everything is already configured, happy coding!

If you want to publish on a private index that needs authentication you have to declare two secrets in your project's action settings:

- `UV_PUBLISH_USERNAME`
- `UV_PUBLISH_USERNAME`

Once done, you are good to go.

:)

## TODO

- [ ] Publish package on pypi
- [ ] Command "magic.py login" to store credentials
