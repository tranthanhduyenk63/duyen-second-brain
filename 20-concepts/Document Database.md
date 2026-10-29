---
type: concept
tags: [concept, databases, mongodb]
created: 2026-10-29
aliases: [Document Model, Document Store]
source: "Common industry term (e.g. MongoDB, Couchbase)"
---

# Document Database

> [!todo] Drafted by Claude: generic definition. Rewrite in your own words.

## Definition (in my words)
Storing data as self-contained JSON-like documents with nested fields and arrays (as in MongoDB), instead of normalized rows spread across tables.

## Why it matters
- An entity's nested data is read and written in one operation, without joins.

## When to use
- Data that is naturally hierarchical and usually accessed as a whole.

## When to avoid
- Heavy cross-entity queries, joins or full-text search.

## Links
- [[Polyglot Persistence]]

## Applied in
- [[LMS Platform]]: helped with nested field data, but search and index performance were poor.
