# technical-docs

## Development
```sh
poetry install
cp .env.example .env # edit the .env file with your own values
```

```sh
set -a
source .env
set +a
poetry run mkdocs serve
```

## Deployment
```sh
poetry run mkdocs gh-deploy
```

- edit `docs/CNAME` to point to your own domain if you have one
- set the `GLOBAL_PASSWORD` environment variable in GitHub secrets for github actions to use
