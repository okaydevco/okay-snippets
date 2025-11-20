# OKAY DEV® Snippets — Performance

Small performance patterns and measurement helpers.

## What belongs here
- Memoization, batching, scheduling
- Web Vitals, profiling, timing marks/measures
- Code splitting and lazy patterns

## Snippet guidelines
- Keep it practical and measurable
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
// Title: rafThrottle
// Description: Throttle a function to animation frames.

export function rafThrottle(fn) {
  let queued = false;
  let lastArgs;
  return (...args) => {
    lastArgs = args;
    if (!queued) {
      queued = true;
      requestAnimationFrame(() => {
        queued = false;
        fn(...lastArgs);
      });
    }
  };
}
```


