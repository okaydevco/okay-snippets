# OKAY DEV® Snippets — Config

Minimal configuration snippets and starter files.

## What belongs here
- ESLint/Prettier/Stylelint configs
- TypeScript, Babel, SWC, Jest/Vitest setup files
- Vite/Webpack/Rollup minimal configs

## Snippet guidelines
- Prefer portable, lowest‑friction examples
- Add description and usage (where to place the file)
- MIT license; attribution optional
- See: [README](../README.md), [CONTRIBUTING](../CONTRIBUTING.md), [LICENSE](../LICENSE)

## Recommended snippet format
1. Title
2. Description
3. Usage/location
4. Snippet

### Optional attribution header
```text
// Copyright (c) 2025 Your Name
// Licensed under the MIT License.
```

### Example skeleton
```js
// Title: basic.eslintrc.cjs
// Description: Minimal ESLint config for modern JS/TS.

module.exports = {
  env: { es2022: true, browser: true, node: true },
  extends: ['eslint:recommended'],
  parserOptions: { ecmaVersion: 'latest', sourceType: 'module' },
};
```


