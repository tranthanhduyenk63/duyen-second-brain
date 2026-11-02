---
type: concept
tags: [concept, reliability, distributed-systems, sre]
created: 2026-11-02
aliases: [Degraded Mode, Fail Soft]
source: "Common reliability engineering term; Google SRE book, ch. 22 (load shedding and graceful degradation)"
---

# Graceful Degradation

> [!todo] Drafted by Claude: generic definition. Rewrite in your own words.

## Definition (in my words)
When a dependency fails, the system keeps its core function working with reduced capability, instead of failing completely. For example, logins still work, and events are queued, retried or skipped until the broker returns.

## Why it matters
- It stops a failure in a non-critical dependency from spreading ([[Cascading Failure]]).
- It decides whether users get an outage or only a degraded experience.

## When to use
- Any dependency that is not essential to the core user action: messaging, analytics, recommendations, notifications.
- **At startup:** a service should start without optional dependencies and connect to them later, instead of crashing.

## When to avoid
- When continuing without the dependency would corrupt data or break correctness. There, failing fast is safer.

## Links
- [[Cascading Failure]] · [[Single Point of Failure]]

## Applied in
- [[Kafka Outage Took Down Authentication]]: removed auth's startup dependency on Kafka, so auth runs while Kafka is down.
