---
type: concept
tags: [concept, reliability, redis, api]
created: 2026-10-29
---

# Rate Limiting

> [!todo] Drafted by Claude: generic definition. Rewrite in your own words.

## Definition (in my words)
Capping how many requests a client can make in a time window, to protect services from overload and abuse.

## Why it matters
- Protects shared resources and limits the damage from misbehaving clients.

## When to use
- Public endpoints, login, expensive operations such as exports, and calls to third-party APIs.

## When to avoid
- TODO

## Links
- TODO

## Applied in
- [[LMS Platform]]: Redis. TODO(ask): which endpoints, and which algorithm (fixed window, sliding window, token bucket)?
