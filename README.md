## Reproduce the issue

```sh
pnpm install
pnpm deploy --filter package-a ./package-a-deployed
cd ./package-a-deployed
pnpm rebuild
# does not rebuild "canvas", but should
```
