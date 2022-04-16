<div align="center">

# pre-commit hooks

[Overview](#overview)
•
[Documentation](#documentation)

</div>

## Table of contents

- [Overview](#overview)
- [Requirements](#requirements)
- [Usage](#usage)
- [Example projects](#example-projects)
- [Credits](#credits)

## Overview

A collection of pre-commit hooks.

## Requirements

- [pre-commit](https://pre-commit.com/)

## Usage

Example `.pre-commit-config.yaml`

```yaml
repos:
- repo: https://github.com/ocular-d/pre-commit-hooks.git
  rev: 0.0.6
  hooks:
    - id: python-black
    - id: python-isort
    - id: vale
    - id: markdown-lint
```

Check the official `pre-commit` [docs](https://pre-commit.com/) for detailed documentation.

## Example projects

- [Example Python](https://github.com/testthedocs/example-python)

## Credits

- [Kiwi.com](https://github.com/kiwicom/dockerfiles)
