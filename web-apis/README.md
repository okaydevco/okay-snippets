# OKAY DEV® Snippets — Web APIs

Focused examples using browser Web APIs.

## What belongs here
- Fetch/AbortController, Cache, Streams
- Storage (localStorage, sessionStorage, IndexedDB)
- Real‑time (WebSocket, BroadcastChannel)
- Service Worker, Notifications, Clipboard, Geolocation, IntersectionObserver, etc.

## Snippet guidelines
- Minimal, production‑ready examples
- Add a short description and usage notes
- No secrets or proprietary endpoints
- MIT license; optional attribution
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
// Title: Fetch with AbortController
// Description: Cancel an in‑flight request on demand.

export function fetchWithAbort(url, options = {}) {
  const controller = new AbortController();
  const promise = fetch(url, { ...options, signal: controller.signal });
  return { promise, abort: () => controller.abort() };
}
```


