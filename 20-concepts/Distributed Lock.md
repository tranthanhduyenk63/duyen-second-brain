---
type: concept
tags: [concept, distributed-systems, concurrency, redis]
created: 2026-10-29
---

# Distributed Lock

> [!todo] Drafted by Claude: generic definition. Rewrite in your own words.

## Definition (in my words)
A lock shared by multiple service instances (e.g. stored in Redis), so that only one of them performs a critical section at a time.

## Why it matters
- Prevents duplicate or conflicting work when several pods handle the same entity or job.

## When to use
- Scheduled jobs that must run only once, or preventing two instances from processing the same entity at once.

## When to avoid
- When correctness truly depends on the lock. Without fencing tokens, a lock can expire while its holder is still working, so prefer database constraints or idempotency.

## Links
- [[Idempotent Consumer]]

## Applied in
- [[LMS Platform]]: Redis. TODO(ask): what does it protect?
