# Prettier Config

My personal [Prettier](https://prettier.io) config.

## Usage

### Install

```bash
pnpm add -D prettier @will-stone/prettier-config
```

### Use config

```js
// prettier.config.js (or .mjs if in CJS env)
export { default } from '@will-stone/prettier-config'
```

### Lint Staged

If you would like to apply formatting before every commit, you can add the
following to your `package.json`:

```json
{
  "lint-staged": {
    "*.{css,json,md}": ["prettier --write"]
  }
}
```

and then

```bash
pnpm add -D husky lint-staged
pnpm husky init
echo "lint-staged" > .husky/pre-commit
```
