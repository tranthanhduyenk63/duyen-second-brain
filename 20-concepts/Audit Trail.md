---
type: concept
tags: [concept, data, compliance, observability]
created: 2026-10-29
aliases: [Audit Log]
---

# Audit Trail

> [!todo] Drafted by Claude: generic definition. Rewrite in your own words.

## Definition (in my words)
A record of who changed what, when and why. It is stored alongside the data, or as an append-only history, instead of silently overwriting state.

## Why it matters
- Manual overrides become traceable and reversible, which builds trust when non-developers can change data.
- Support questions like "why can this student retake the exam?" can be answered without digging through logs.

## When to use
- Overrides, resets, permission changes, and anything involving grades or money.

## When to avoid
- High-volume, low-value changes, where the history costs more than it's worth.

## Links
- [[Role-Based Access Control]]

## Applied in
- [[Checkpoint Exam Restart]]: every checkpoint restart records an update history.
