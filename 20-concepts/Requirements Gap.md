---
type: concept
tags: [concept, product, requirements]
created: 2026-10-29
aliases: [Missed Use Case, Missing Requirement]
source: "Business analysis (gap analysis)"
---

# Requirements Gap

> [!todo] Drafted by Claude: generic definition. Rewrite in your own words.

## Definition (in my words)
A real-world situation the system was never designed for. When it happens, the system behaves exactly as built, but the result is wrong for the user. It looks like a bug, but the fix is a product decision plus a feature, not a code correction. The recurring manual workaround it creates is [[Toil]].

## Why it matters
- Treating it as a bug leads to endless patching (manual scripts or data fixes) instead of a proper solution.
- How to spot one: the same manual fix keeps recurring, and the code involved has no clear defect.

## When to use (this framing)
- A recurring support ticket where the system behaves as specified, but the specification didn't cover what actually happened.

## When to avoid
- Real defects, where the code contradicts the intended behaviour.

## Links
- [[Toil]] · [[Role-Based Access Control]] · [[Audit Trail]]

## Applied in
- [[Checkpoint Exam Restart]]: the script reset checkpoint records 3–4 times a month; replaced by an operator restart feature.
- [[LMS Platform]]: a script to reschedule classes for holidays was another one. TODO(ask): was it replaced with a feature? Add more examples as you remember them.
