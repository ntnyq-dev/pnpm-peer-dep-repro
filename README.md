# pnpm-peer-dep-repro

## repro issue

Repro with pnpm v8

1. Run command `pnpm install`
2. Check `pnpm-lock.yaml`, the optional peer dep is saved as `dependencies`
3. Run command `pnpm upgrade`
4. Check `package.json`, the optional peer dep becames a `dependencies`

## Expected behavior

Uncomment `auto-install-peers=false` in `.npmrc` and repeat 1-4 again, everything works fine
