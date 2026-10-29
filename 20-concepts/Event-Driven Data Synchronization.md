---
type: concept
tags: [concept, messaging, kafka, data-consistency]
created: 2026-10-29
---

# Event-Driven Data Synchronization

> [!todo] Drafted by Claude: generic definition. Rewrite in your own words.

## Definition (in my words)
Keeping a copy of another service's data up to date by consuming that service's change events (e.g. `CourseUpdated`), instead of calling the service synchronously every time the data is needed.

## Why it matters
- Each service can read its local copy without a network call, and it keeps working when the source service is down.
- The cost is eventual consistency. Lost, duplicated or out-of-order events cause data to drift between services.

## When to use
- Read-heavy access to another service's data, when slightly stale data is acceptable.

## When to avoid
- When the reader needs data that is strongly consistent (always current).

## Links
- [[Command vs Event Messages]] · [[Idempotent Consumer]] · [[Outbox Pattern]]

## Applied in
- [[LMS Platform]]: services listen to "updated" events from other services and update their own data. TODO(ask): were the intermittent bugs related to this?
