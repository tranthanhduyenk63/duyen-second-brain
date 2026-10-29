---
type: concept
tags: [concept, reliability, architecture]
created: 2026-10-29
aliases: [SPOF]
source: "Common reliability engineering term"
---

# Single Point of Failure

> [!todo] Drafted by Claude: generic definition. Rewrite in your own words.

## Definition (in my words)
A component whose failure alone stops the whole system, because nothing else can take over its job and critical functions depend on it.

## Why it matters
- Shared infrastructure (a database, broker or auth service) often becomes a SPOF without anyone noticing, until it fails.

## How to prevent
- Redundancy (replicas, clusters), removing the hard dependency from critical paths, and [[Graceful Degradation]].

## When to use (this lens)
- Architecture reviews: ask "if X goes down, what else goes down?"

## Links
- [[Cascading Failure]]

## Applied in
- [[Kafka Outage Took Down Authentication]]: Kafka was effectively a SPOF because authentication depended on it.
