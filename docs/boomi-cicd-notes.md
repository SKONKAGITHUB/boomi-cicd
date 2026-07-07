# Boomi CI/CD Notes

This repository was scaffolded with a starter GitHub Actions workflow and shell script pipeline.

## Current state

- Workflow: `.github/workflows/deploy.yml`
- Scripts:
  - `scripts/boomi-common.sh`
  - `scripts/boomi-preflight.sh`
  - `scripts/boomi-package.sh`
  - `scripts/boomi-deploy.sh`
  - `scripts/boomi-validate.sh`
  - `scripts/boomi-rollback.sh`

## Next steps

1. Define Boomi authentication approach (API token/OAuth/account model).
2. Add required secrets in GitHub repository settings.
3. Implement real deployment logic in `boomi-deploy.sh`.
4. Add meaningful validation checks in `boomi-validate.sh`.
5. Implement deterministic rollback strategy in `boomi-rollback.sh`.
6. Optionally split environments into separate jobs with approvals.

## Suggested secrets

- `BOOMI_ACCOUNT_ID`
- `BOOMI_USERNAME`
- `BOOMI_API_TOKEN`
- any environment-specific endpoint/atom identifiers
