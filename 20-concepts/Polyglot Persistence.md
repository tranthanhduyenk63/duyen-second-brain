---
type: concept
tags: [concept, databases, search, opensearch, architecture]
created: 2026-10-29
aliases: [Secondary Search Index]
source: "Martin Fowler & Pramod Sadalage, NoSQL Distilled (2012)"
---

# Polyglot Persistence

> [!todo] Drafted by Claude: generic definition. Rewrite in your own words.

## Definition (in my words)
Using different storage technologies for different needs within one system, each chosen for what it does best. A common case is keeping a primary database as the source of truth and copying data into a search engine (OpenSearch or Elasticsearch) that handles search queries.

## Why it matters
- One store rarely fits every access pattern. For example, document databases are good at nested reads but weak at full-text search, relevance ranking and aggregations.
- The cost is more infrastructure to run, plus keeping the copies in sync. Searches may briefly lag behind the source of truth.

## When to use
- When one access pattern (search, analytics, caching) is beyond what the primary store handles well.

## When to avoid
- Small systems, or needs the primary database's indexes already cover. Each extra store adds operations work and risk of inconsistency.

## Links
- [[Document Database]] · [[Event-Carried State Transfer]] · [[Dual Write Problem]] (the wrong way to keep copies in sync)

## Applied in
- [[LMS Platform]]: MongoDB as the primary store, with OpenSearch for search. TODO(ask): how is it kept in sync (Kafka events, change streams, batch)?
