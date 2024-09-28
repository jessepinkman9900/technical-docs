# technical-docs
![Static Badge](https://img.shields.io/badge/python-3.12-brightgreen)
![GitHub Actions Workflow Status](https://img.shields.io/github/actions/workflow/status/jessepinkman9900/technical-docs/deploy.yaml?branch=main&label=gh-deploy)

## Development
```sh
poetry install
poetry run pre-commit install
cp .env.example .env # edit the .env file with your own values
```

```sh
set -a
source .env
set +a
poetry run mkdocs serve
```

```sh
poetry run pre-commit run --all-files
```

## Deployment
```sh
poetry run mkdocs gh-deploy
```

- edit `docs/CNAME` to point to your own domain if you have one
- github actions
    - set the `GLOBAL_PASSWORD` environment variable in GitHub secrets for github actions to use
    - give workflow "read & write permisions" in repository settings
