# Black

- Base image: `python:3.8-alpine`
- Packages: [`black`](https://github.com/psf/black/)

Image used to format Python code using [`pre-commit`](https://pre-commit.com) hooks and to check if all the files are correctly formatted on CI.

`pre-commit` hook example:

```yaml
- repo: local
  hooks:
    - id: black
      name: black-code-formatter
      language: docker_image
      entry: --entrypoint black testthedocs/black:22.1.0
      types: [python]
```

CLI usage example:

`docker run -ti -v "$(pwd)":/src -v "$(pwd)/.blackcache":/home/black/.cache --workdir=/src testthedocs/black:22.1.0 black .`
