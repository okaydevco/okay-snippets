# OKAY DEV® Snippets — WebGL

Minimal WebGL setup and rendering utilities.

## What belongs here
- Context creation, shader compilation/linking
- Buffer setup, attribute/uniform helpers
- Tiny rendering loops and utilities

## Snippet guidelines
- Keep examples short and educational
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
// Title: initWebGL
// Description: Create a WebGL context and basic error guard.

export function initWebGL(canvas) {
  const gl = canvas.getContext('webgl') || canvas.getContext('experimental-webgl');
  if (!gl) throw new Error('WebGL not supported');
  return gl;
}
```


