---
name: api
description: Design or review an API — use when the user asks to design endpoints, review API structure, create a REST or GraphQL API, or improve an existing API.
---

# API Design

Design or review an API for the feature or module described.

Cover:
1. **Endpoints** — method, path, request shape, response shape, status codes
2. **Auth** — how callers authenticate, what scopes/permissions apply
3. **Errors** — consistent error envelope, meaningful codes
4. **Pagination** — cursor or offset, limit caps
5. **Caching** — which responses can be cached, TTLs, cache keys
6. **Rate limiting** — per-key limits, retry-after headers
7. **Versioning** — how breaking changes are handled

Output as a concise spec, not prose. Use code blocks for shapes.
