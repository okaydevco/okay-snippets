# OKAY DEV® Snippets — Vue

Small Vue components and composables.

## What belongs here
- Single‑file component patterns
- Reusable composables (state, async, performance)
- Accessibility‑aware UI patterns

## Snippet guidelines
- Keep it minimal and Vue‑idiomatic
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
```vue
<!-- Title: useToggle -->
<!-- Description: Boolean toggle composable. -->
<script setup>
import { ref } from 'vue';
export function useToggle(initial = false) {
  const value = ref(initial);
  const toggle = () => (value.value = !value.value);
  return { value, toggle };
}
</script>
```


