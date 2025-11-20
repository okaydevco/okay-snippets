# OKAY DEV® Snippets — Accessibility

Snippets that improve accessibility and inclusive UX.

## What belongs here
- ARIA roles/attributes, keyboard navigation
- Focus management, traps, visible focus styles
- Reduced motion and color contrast helpers

## Snippet guidelines
- Follow WCAG/ARIA best practices
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
// Title: focusTrap
// Description: Trap focus within a container (e.g., modal).

export function focusTrap(container) {
  const selectors = [
    'a[href]', 'button:not([disabled])', 'textarea', 'input[type]',
    'select', '[tabindex]:not([tabindex="-1"])'
  ];
  const cycle = (e) => {
    if (e.key !== 'Tab') return;
    const nodes = container.querySelectorAll(selectors.join(','));
    if (!nodes.length) return;
    const first = nodes[0];
    const last = nodes[nodes.length - 1];
    if (e.shiftKey && document.activeElement === first) {
      last.focus(); e.preventDefault();
    } else if (!e.shiftKey && document.activeElement === last) {
      first.focus(); e.preventDefault();
    }
  };
  container.addEventListener('keydown', cycle);
  return () => container.removeEventListener('keydown', cycle);
}
```


