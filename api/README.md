# OKAY DEV® Snippets — API

Client‑side or lightweight server interaction patterns.

## What belongs here
- REST/GraphQL fetch wrappers, auth headers, retries/backoff
- Pagination, cursor handling, error normalization
- Small API client utilities and response validation

## Snippet guidelines
- Keep dependencies minimal; prefer fetch/URL APIs
- Add description and usage
- Do not include secrets; use environment variables when needed
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
// Title: createApi
// Description: Minimal JSON API helper with auth and error normalization.

export function createApi(baseUrl, getToken) {
  return async function api(path, init = {}) {
    const headers = {
      'Content-Type': 'application/json',
      ...(getToken ? { Authorization: `Bearer ${getToken()}` } : {}),
      ...init.headers,
    };
    const res = await fetch(new URL(path, baseUrl), { ...init, headers });
    if (!res.ok) {
      const message = await res.text().catch(() => res.statusText);
      throw new Error(`API ${res.status}: ${message}`);
    }
    return res.status === 204 ? null : res.json();
  };
}
```


