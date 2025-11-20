# OKAY DEV® Snippets — Utils

General, language‑agnostic utility snippets (leaning JS/TS).

## What belongs here
- Small, reusable helpers (math, strings, objects)
- Tiny abstractions useful across apps
- No framework or environment assumptions

## Snippet guidelines
- Keep it tiny and dependency‑free
- Add description and usage
- MIT license; attribution optional
- See: [README](../README.md), [CONTRIBUTING](../CONTRIBUTING.md), [LICENSE](../LICENSE)

## Recommended snippet format
1. Title
2. Description
3. Usage
4. Snippet

### Optional attribution header
```text
// Copyright (c) 2025 Your Name
// Licensed under the MIT License.
```

### Example skeleton
```js
// Title: clamp
// Description: Clamp number n to inclusive [min, max].

export const clamp = (n, min, max) => Math.min(max, Math.max(min, n));
```


