---
type: concept
tags: [concept, programming, legacy-code, design]
created: 2026-11-02
aliases: [Hidden Side Effect]
source: "Functional programming / general computer science term"
---

# Side Effect

> [!todo] Drafted by Claude: generic definition. Rewrite in your own words.

## Definition (in my words)
Anything a function does besides returning its result: writing to a database, deleting records, publishing an event, changing shared state. A *hidden* side effect is one that the function's name or the caller doesn't suggest.

## Why it matters
- Reusing code reuses all of its side effects, including ones you didn't know about.
- Hidden destructive side effects (e.g. deleting records) cause data loss that is hard to trace.

## How to manage
- Separate pure decision logic from effects (in [[Hexagonal Architecture]], effects live in adapters).
- Name functions after everything they do, and capture existing behaviour with a [[Characterization Test]] before reusing code.

## Links
- [[Characterization Test]] · [[Hexagonal Architecture]]

## Applied in
- [[Attendance Records Lost on Holiday Reschedule]]: reused legacy session regeneration logic silently removed attendance.
