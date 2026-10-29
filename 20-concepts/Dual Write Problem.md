---
type: concept
tags: [concept, distributed-systems, data-consistency, databases]
created: 2026-10-29
aliases: [Dual Writes]
source: "Common term in event-driven / CDC literature (e.g. Confluent, Debezium)"
---

# Dual Write Problem

> [!todo] Drafted by Claude: generic definition. Rewrite in your own words.

## Definition (in my words)
Application code writes the same change to two separate systems (two databases, or a database and a broker) with no transaction across both. If one write succeeds and the other fails, or they happen in a different order, the two sources disagree.

## Why it matters
- It causes inconsistencies that appear only sometimes and are hard to debug.
- It is often hidden in legacy code, where both writes look correct individually.

## When to use (this awareness)
- Whenever one operation updates more than one store.

## How to avoid
- Keep one source of truth. Propagate changes from it to the other store with the [[Outbox Pattern]], change data capture, or [[Event-Carried State Transfer]].

## Links
- [[Outbox Pattern]] · [[Event-Carried State Transfer]]

## Applied in
- [[LMS Platform]]: the legacy code saved data twice into two data sources. TODO(ask): which stores, and how did you fix it?
