# OKAY DEV® Snippets — Svelte

Small Svelte components, stores, and actions.

## What belongs here
- Component patterns and accessibility helpers
- Stores (readable/writable/derived)
- Actions and lifecycle utilities

## Snippet guidelines
- Keep it minimal and Svelte‑idiomatic
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
<!-- Copyright (c) 2025 Your Name -->
<!-- Licensed under the MIT License. -->
```

### Example skeleton
```svelte
<!-- Title: toggle store -->
<!-- Description: A tiny boolean store with toggle. -->
<script>
  import { writable } from 'svelte/store';
  export const createToggle = (initial = false) => {
    const value = writable(initial);
    const toggle = () => value.update(v => !v);
    return { value, toggle };
  };
</script>
```


