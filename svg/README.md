# OKAY DEV® Snippets — SVG

Inline SVG techniques, icons, and filters.

## What belongs here
- Reusable symbols and sprite patterns
- Filters, gradients, masks, accessibility patterns
- Small utilities for styling or animating SVG

## Snippet guidelines
- Keep it minimal and copy‑pasteable
- Add description and usage notes
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
```html
<!-- Title: Reusable Icon Symbol -->
<svg aria-hidden="true" style="position:absolute;width:0;height:0;overflow:hidden">
  <symbol id="icon-check" viewBox="0 0 16 16">
    <path d="M6 10l-2-2  -1.5 1.5L6 13 13.5 5.5 12 4z"></path>
  </symbol>
  <!-- ... -->
  <!-- definitions only; reference with <use> -->
</svg>
```


