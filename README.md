# gei
a demo of gei

## pre-requisites
- ensure migrations are enabled in GHES
- create **classic** PAT tokens which meet [requirements](https://docs.github.com/en/enterprise-server@3.8/migrations/using-github-enterprise-importer/preparing-to-migrate-with-github-enterprise-importer/managing-access-for-github-enterprise-importer#personal-access-tokens-for-github-products)
- either set variables in a .env file and set them with `set -o allexport; source .env; set +o allexport` or export them in your shell


## bootstrap
You can bootstrap this script on mac using the following command:
```bash
./scripts/bootstrap.sh
``` 

## Migrate a single repository from GitHub Enterprise Server to GitHub Enterprise Cloud
```bash
gh gei migrate-repo --github-source-org $GH_SOURCE_ORG --source-repo $GH_SOURCE_REPO --github-target-org $GH_DESTINATION_ORG --target-repo $GH_DESTINATION_REPO --ghes-api-url $GHES_API_URL
```


## thanks
- official docs
https://docs.github.com/en/migrations/using-github-enterprise-importer/migrating-repositories-with-github-enterprise-importer/migrating-repositories-from-github-enterprise-server-to-github-enterprise-cloud
- shared Gist https://gist.github.com/mihow/9c7f559807069a03e302605691f85572