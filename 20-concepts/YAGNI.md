---
type: concept
tags: [concept, process, design, product]
created: 2026-10-29
aliases: [You Aren't Gonna Need It]
source: "Extreme Programming (Kent Beck, Ron Jeffries); Martin Fowler, Yagni (2015)"
---

# YAGNI

> [!todo] Drafted by Claude: generic definition. Rewrite in your own words.

## Definition (in my words)
Don't build a feature or abstraction until there's a real, present need for it. Speculative features cost time to build and maintain, and are often never used.

## Why it matters
- Every unused feature still adds code, tests and complexity that the team carries forever.

## When to use
- When a requirement is speculative or vague. Challenge it with the PO before building.

## When to avoid
- Decisions that are expensive to reverse later, such as data model foundations or security. Some upfront design pays off there.

## Links
- [[Requirements Gap]] (the opposite failure: something needed was missing) · [[Analysis Paralysis]]

## Applied in
- [[LMS Initial Build]]: built a task module that turned out useless, plus others. Lesson: challenge the PO's requirements.
