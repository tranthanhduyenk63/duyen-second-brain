---
type: concept
tags: [concept, search, opensearch, databases]
created: 2026-10-29
---

# Secondary Search Index

> [!todo] Drafted by Claude: generic definition. Rewrite in your own words.

## Definition (in my words)
Keeping the main database as the source of truth and copying the data into a dedicated search engine (OpenSearch or Elasticsearch) that handles search queries.

## Why it matters
- Search engines handle full-text search, relevance ranking, filtering and aggregations far better than general-purpose database indexes.
- The cost is keeping the copy in sync, and accepting that search results may briefly lag behind the database.

## When to use
- When search requirements exceed what the main database's indexes can handle.

## When to avoid
- Simple exact-match lookups that a normal database index already handles well.

## Links
- [[Document Model]] · [[Event-Driven Data Synchronization]]

## Applied in
- [[LMS Platform]]: OpenSearch alongside MongoDB. TODO(ask): how is it kept in sync (Kafka events, change streams, batch)?
