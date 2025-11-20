# OKAY DEV® Snippets — CSS

This folder holds small, copy‑pasteable CSS snippets.

## What belongs here
- Layout primitives (Flexbox, Grid)
- Utilities (spacing, typography, visibility)
- Variables, theming, preferring-reduced-motion support
- Animations/transitions, resets/normalization

## Snippet guidelines
- Keep it minimal, composable, and framework‑agnostic
- Add a brief description at the top of the file
- No secrets, tokens, or proprietary code
- MIT license; attribution optional
- See: [README](../README.md), [CONTRIBUTING](../CONTRIBUTING.md), [LICENSE](../LICENSE)

## Recommended snippet format
1. Title
2. Description (1–3 lines)
3. Usage notes (class names, constraints)
4. The snippet

### Optional attribution header
```text
/* Copyright (c) 2025 Your Name */
/* Licensed under the MIT License. */
```

### Example skeleton
```css
/* Title: Visually Hidden (but accessible) */
/* Description: Hide content visually while retaining screen-reader access */

.visually-hidden {
  position: absolute;
  width: 1px;
  height: 1px;
  margin: -1px;
  padding: 0;
  border: 0;
  clip: rect(0 0 0 0);
  overflow: hidden;
  white-space: nowrap;
}
```


