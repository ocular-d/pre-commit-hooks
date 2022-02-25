## Isort

- Base image: `python:3.9-alpine`
- Packages: [`isort`](https://github.com/timothycrosley/isort/)

Image used to format Python code using [`pre-commit`](https://pre-commit.com) hooks and to check if all the imports are correctly sorted on CI.

`pre-commit` hook example:

```yaml
- repo: local
  hooks:
    - id: isort
      name: sort-python-imports
      language: docker_image
      entry: --entrypoint isort testthedocs/isort:$VERSION
      types: [python]
```

CLI usage example:

`docker run -ti -v "$(pwd)":/src --workdir=/src testthedocs/isort:5.7.0 isort **/*.py`
