---
type: concept
tags: [concept, architecture, migration, refactoring]
created: 2026-10-29
aliases: [Incremental Refactoring]
coined: true
---

# Incremental Migration

> [!question] TODO(ask): rename to **Strangler Fig Pattern** if old and new code run side by side while traffic is gradually moved over, or **Incremental Refactoring** if each service is refactored in place.

> [!todo] Drafted by Claude: generic definition. Rewrite in your own words.

## Definition (in my words)
Moving a system to a new architecture piece by piece (e.g. one service at a time), shipping each piece while the rest keeps running on the old design, instead of one big-bang rewrite.

## Why it matters
- Each step is smaller and can be rolled back, and the system keeps working throughout.
- Lessons from the first piece improve the next ones.
- The cost is living with two architectures for a long time, which adds cognitive load.

## When to use
- Production systems that can't stop, especially ones you inherited and don't fully understand.

## When to avoid
- Very small systems, where a rewrite is cheaper than the overhead of running both designs.

## Links
- [[Hexagonal Architecture]] · [[Strangler Fig Pattern]]

## Applied in
- [[Preparing a Codebase for AI Coding Agents]]: LMS services moved to hexagonal architecture one at a time.
