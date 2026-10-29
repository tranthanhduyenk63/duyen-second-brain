---
type: concept
tags: [concept, reliability, distributed-systems, sre]
created: 2026-10-29
aliases: [Cascade Failure]
source: "Google, Site Reliability Engineering, ch. 22 Addressing Cascading Failures (2016)"
---

# Cascading Failure

> [!todo] Drafted by Claude: generic definition. Rewrite in your own words.

## Definition (in my words)
A failure in one component spreads to others that depend on it, until a large part or all of the system is down. A local fault becomes a global outage.

## Why it matters
- In [[Microservices Architecture]], hidden dependencies (especially on shared infrastructure like a message broker) can turn one outage into a full outage.

## How to prevent
- Keep critical paths independent of non-critical infrastructure.
- Timeouts, circuit breakers, [[Graceful Degradation]], and async work that fails open instead of blocking.

## When to use (this lens)
- Reviewing dependencies of critical services (auth, payments, gateways).

## Links
- [[Single Point of Failure]] · [[Microservices Architecture]]

## Applied in
- [[Kafka Outage Took Down Authentication]]
