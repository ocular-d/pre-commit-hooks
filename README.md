<!-- markdownlint-disable -->
<div align="center">

# pre-commit hooks

[Overview](#overview)
•
[Documentation](#documentation)

</div>
<!-- markdownlint-enable -->

## Table of contents

- [Overview](#overview)
- [Requirements](#requirements)
- [Usage](#usage)
- [Example projects](#example-projects)
- [Credits](#credits)

## Overview

<!-- vale off -->

A collection of pre-commit hooks.

| Check  | Description  | ID |
|---|---|---|
| Python Black  | Python code formatter  | python-black  |
| Python Isort  |  sort Python imports | python-isort  |
| Vale  | Prose linter  | vale  |
| Markdown lint | Markdown linter | markdown-lint |
| ShellCheck | Static analysis tool for shell scripts |

<!-- vale on -->
## Requirements

- [pre-commit](https://pre-commit.com/)

## Usage

Example `.pre-commit-config.yaml`

```yaml
repos:
- repo: https://github.com/ocular-d/pre-commit-hooks.git
  rev: 0.0.8
  hooks:
    - id: python-black
    - id: python-isort
    - id: vale
    - id: markdown-lint
    - id: shellcheck
```

Check the official `pre-commit` [docs](https://pre-commit.com/) for detailed documentation.

## Example projects

- [Example Python](https://github.com/testthedocs/example-python)

## Credits

- [Kiwi.com](https://github.com/kiwicom/dockerfiles)
