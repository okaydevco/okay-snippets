# OKAY DEV® Snippets — Three.js

Concise Three.js setup and utility snippets.

## What belongs here
- Minimal scene/camera/renderer setup
- Controls, loaders, lights helpers
- Animation loops and resize handlers

## Snippet guidelines
- Favor small, composable snippets
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
// Title: createBasicScene
// Description: Minimal Three.js scene with resize handling.

import * as THREE from 'three';

export function createBasicScene(canvas) {
  const renderer = new THREE.WebGLRenderer({ canvas, antialias: true });
  const scene = new THREE.Scene();
  const camera = new THREE.PerspectiveCamera(60, 1, 0.1, 1000);
  camera.position.z = 4;

  function resize() {
    const { clientWidth: w, clientHeight: h } = canvas;
    renderer.setSize(w, h, false);
    camera.aspect = w / h;
    camera.updateProjectionMatrix();
  }
  resize();
  return { renderer, scene, camera, resize };
}
```


