# OKAY DEV® Snippets — Canvas (2D)

Small, focused HTML5 Canvas 2D snippets.

## What belongs here
- Drawing primitives, state management
- Pixel operations, image manipulation
- Animation loops and interaction patterns

## Snippet guidelines
- Keep it minimal; avoid frameworks
- Add description and usage
- No secrets or proprietary content
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
// Title: Basic Canvas Loop
// Description: RequestAnimationFrame loop with clear/draw steps.

export function startLoop(ctx) {
  function frame() {
    const { width, height } = ctx.canvas;
    ctx.clearRect(0, 0, width, height);
    // draw...
    requestAnimationFrame(frame);
  }
  requestAnimationFrame(frame);
}
```


