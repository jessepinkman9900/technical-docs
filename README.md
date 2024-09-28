# technical-docs

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
