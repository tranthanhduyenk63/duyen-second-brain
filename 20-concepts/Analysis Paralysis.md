---
type: concept
tags: [concept, process, decision-making]
created: 2026-10-29
aliases: [Paralysis by Analysis]
source: "Common software engineering anti-pattern (e.g. AntiPatterns, Brown et al. 1998)"
---

# Analysis Paralysis

> [!todo] Drafted by Claude: generic definition. Rewrite in your own words.

## Definition (in my words)
Being stuck in analysis or design and not acting, because of uncertainty, unclear requirements or fear of getting it wrong. Time passes while no feedback comes in.

## Why it matters
- It delays delivery and the real feedback that would resolve the uncertainty faster than more analysis.

## How to avoid
- [[Timeboxing|Timebox]] design and decisions.
- Ship a small slice to learn from it ([[Continuous Delivery]]).
- Escalate unclear requirements instead of designing around them.

## When to use (this lens)
- When a design has been in progress for a long time with no decision.

## Links
- [[Timeboxing]] · [[Continuous Delivery]] · [[YAGNI]]

## Applied in
- [[LMS Initial Build]]: domain design took too long. Lesson: less stalling, act sooner.
