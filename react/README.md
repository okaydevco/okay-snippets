# OKAY DEV® Snippets — React

Small React components, hooks, and utilities.

## What belongs here
- Hooks (state, effects, memoization, async)
- Components with clear accessibility patterns
- Context, reducers, testing helpers, performance tips

## Snippet guidelines
- Keep it framework‑native (no heavy deps)
- Add description and usage
- MIT license; attribution optional
- See: [README](../README.md), [CONTRIBUTING](../CONTRIBUTING.md), [LICENSE](../LICENSE)

## Recommended snippet format
1. Title
2. Description
3. Usage (JSX example)
4. Snippet

### Optional attribution header
```text
// Copyright (c) 2025 Your Name
// Licensed under the MIT License.
```

### Example skeleton
```jsx
// Title: useToggle
// Description: Boolean toggle with optional initial value.

import { useCallback, useState } from 'react';

export function useToggle(initial = false) {
  const [value, setValue] = useState(initial);
  const toggle = useCallback(() => setValue(v => !v), []);
  return [value, toggle, setValue];
}
```


