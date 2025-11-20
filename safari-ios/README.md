# OKAY DEV® Snippets — Safari iOS

Workarounds and patterns for Safari on iOS.

## What belongs here
- Viewport unit quirks (100vh vs 100dvh), safe area insets
- Input zoom, fixed position, overscroll behaviors
- Touch/gesture, passive listeners, scrolling bugs

## Snippet guidelines
- Explain the issue and the workaround briefly
- Add usage notes and constraints
- MIT license; attribution optional
- See: [README](../README.md), [CONTRIBUTING](../CONTRIBUTING.md), [LICENSE](../LICENSE)

## Recommended snippet format
1. Title
2. Description (bug/quirk and fix)
3. Usage
4. Snippet

### Optional attribution header
```text
/* Copyright (c) 2025 Your Name */
/* Licensed under the MIT License. */
```

### Example skeleton
```js
// Title: setViewportHeightVar
// Description: Work around mobile 100vh by setting --vh unit.

export function setViewportHeightVar(win = window, doc = document) {
  const set = () => {
    const vh = win.innerHeight * 0.01;
    doc.documentElement.style.setProperty('--vh', `${vh}px`);
  };
  set();
  win.addEventListener('resize', set);
  return () => win.removeEventListener('resize', set);
}
```


