# OKAY DEV® Snippets — AI

Small, practical AI integration snippets.

## What belongs here
- API client helpers (env‑based keys only)
- Prompt templates and response post‑processing
- Rate limiting, retries, streaming, token budgeting

## Snippet guidelines
- Never commit secrets; use environment variables and examples
- Add description and usage, note provider specifics
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
// Title: callAI
// Description: Example AI client using an API key from env.

export async function callAI(prompt, fetchImpl = fetch) {
  const apiKey = process.env.AI_API_KEY || '<YOUR_API_KEY>';
  if (!apiKey) throw new Error('AI_API_KEY missing');
  const res = await fetchImpl('https://api.example.ai/v1/complete', {
    method: 'POST',
    headers: {
      'Content-Type': 'application/json',
      'Authorization': `Bearer ${apiKey}`,
    },
    body: JSON.stringify({ prompt }),
  });
  if (!res.ok) throw new Error(`AI error ${res.status}`);
  return res.json();
}
```


