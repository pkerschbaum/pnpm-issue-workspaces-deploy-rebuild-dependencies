## Reproduce the issue

```sh
pnpm install
TEMP_DEPLOY_DIR="$(mktemp -d /tmp/temp-deploy-dir-XXX)/package-a-deployed"
pnpm deploy --filter package-a "${TEMP_DEPLOY_DIR}"
cd "${TEMP_DEPLOY_DIR}"
pnpm rebuild
# does not rebuild "canvas", but should
```
