# OKAY DEV® Snippets — JavaScript

Small, framework‑agnostic JavaScript utilities and patterns.

## What belongs here
- DOM helpers, events, selectors
- Data utilities (arrays, objects, dates)
- Networking helpers (fetch, retry, timeouts)
- Small algorithms and performance helpers

## Snippet guidelines
- Keep it focused and dependency‑free when possible
- Add a brief description and usage notes
- No secrets or proprietary code
- Licensed under MIT; attribution optional
- See: [README](../README.md), [CONTRIBUTING](../CONTRIBUTING.md), [LICENSE](../LICENSE)

## Recommended snippet format
1. Title
2. Description (what/why)
3. Usage (short example)
4. Snippet

### Optional attribution header
```text
// Copyright (c) 2025 Your Name
// Licensed under the MIT License.
```

### Example skeleton
```js
// Title: debounce
// Description: Delay invoking fn until wait ms have elapsed since last call.

export function debounce(fn, wait = 200) {
  let timerId;
  return (...args) => {
    clearTimeout(timerId);
    timerId = setTimeout(() => fn(...args), wait);
  };
}
```


