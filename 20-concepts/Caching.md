---
type: concept
tags: [concept, performance, redis]
created: 2026-10-29
---

# Caching

> [!todo] Drafted by Claude: generic definition. Rewrite in your own words.

## Definition (in my words)
Storing the results of expensive reads in a faster store (e.g. Redis) so repeated requests skip the slow source.

## Why it matters
- Lower latency and less load on the database. The cost is stale data and cache invalidation.

## When to use
- Data that is read often, changes rarely, and can tolerate being slightly stale.

## When to avoid
- Data that must always be current, or data that is rarely read twice.

## Links
- TODO

## Applied in
- [[LMS Platform]]: Redis. TODO(ask): what is cached, and how is it invalidated?
