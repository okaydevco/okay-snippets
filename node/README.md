# OKAY DEV® Snippets — Node.js

Small Node.js utilities and server patterns.

## What belongs here
- FS, streams, child processes, CLI helpers
- Minimal HTTP servers and middleware patterns
- Small utilities for config/env handling

## Snippet guidelines
- Keep dependencies light
- Add description and usage
- No secrets; use environment variables and examples
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
// Title: tinyServer
// Description: Minimal Node HTTP server.
import http from 'node:http';

export function tinyServer(port = 3000) {
  const server = http.createServer((req, res) => {
    res.writeHead(200, { 'Content-Type': 'text/plain' });
    res.end('OK\n');
  });
  server.listen(port);
  return server;
}
```


