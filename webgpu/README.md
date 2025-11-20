# OKAY DEV® Snippets — WebGPU

Small, focused WebGPU initialization and rendering helpers.

## What belongs here
- Adapter/device acquisition, swap chain setup
- Basic pipelines, passes, buffers, and textures
- Tiny compute or render examples

## Snippet guidelines
- Keep examples minimal and current (browser flags may change)
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
// Title: getDevice
// Description: Request a WebGPU adapter+device with basic guards.

export async function getDevice() {
  if (!('gpu' in navigator)) throw new Error('WebGPU not available');
  const adapter = await navigator.gpu.requestAdapter();
  if (!adapter) throw new Error('No suitable GPU adapter found');
  const device = await adapter.requestDevice();
  return device;
}
```


