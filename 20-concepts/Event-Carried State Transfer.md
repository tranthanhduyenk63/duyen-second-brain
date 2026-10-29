---
type: concept
tags: [concept, messaging, kafka, data-consistency]
created: 2026-10-29
aliases: [Event-Driven Data Synchronization]
source: "Martin Fowler, What do you mean by Event-Driven? (2017)"
---

# Event-Carried State Transfer

> [!todo] Drafted by Claude: generic definition. Rewrite in your own words.

## Definition (in my words)
Events carry the changed data itself (e.g. `CourseUpdated` with the new course fields). Consumers keep a local copy of another service's data up to date from these events, instead of calling that service synchronously each time they need the data.

## Why it matters
- Each service can read its local copy without a network call, and it keeps working when the source service is down.
- The cost is eventual consistency. Lost, duplicated or out-of-order events cause data to drift between services.

## When to use
- Read-heavy access to another service's data, when slightly stale data is acceptable.

## When to avoid
- When the reader needs data that is strongly consistent (always current).

## Links
- [[Command Message]] and [[Event Message]] · [[Idempotent Consumer]] · [[Outbox Pattern]]

## Applied in
- [[LMS Platform]]: services listen to "updated" events from other services and update their own data. TODO(ask): were the intermittent bugs related to this?
