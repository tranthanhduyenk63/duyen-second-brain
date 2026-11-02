---
type: concept
tags: [concept, testing, legacy-code, refactoring]
created: 2026-11-02
aliases: [Golden Master Test, Approval Test]
source: "Michael Feathers, Working Effectively with Legacy Code (2004)"
---

# Characterization Test

> [!todo] Drafted by Claude: generic definition. Rewrite in your own words.

## Definition (in my words)
A test that records what existing code *actually does* (not what it should do), written before you change or reuse that code. It pins current behaviour so that any change, intended or not, becomes visible.

## Why it matters
- Legacy code often has undocumented rules. Characterization tests surface them before they surprise you in production.

## When to use
- Before refactoring, migrating, or reusing legacy code you don't fully understand.

## When to avoid
- Code you're about to delete entirely, or code whose behaviour is fully specified and already tested.

## Links
- [[Side Effect]] · [[Use-Case-Driven Testing]] · [[Incremental Migration]]

## Applied in
- Not yet. Identified as the missing safeguard in [[Attendance Records Lost on Holiday Reschedule]], and planned as a follow-up there.
