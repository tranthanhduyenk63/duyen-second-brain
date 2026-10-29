---
type: concept
tags: [concept, sre, operations, automation]
created: 2026-10-29
aliases: [Operational Toil]
source: "Google, Site Reliability Engineering, ch. 5 Eliminating Toil (2016)"
---

# Toil

> [!todo] Drafted by Claude: generic definition. Rewrite in your own words.

## Definition (in my words)
Manual, repetitive, automatable operational work that has no lasting value and grows with the size of the system. For example, running the same fix-up script by hand every time a ticket arrives.

## Why it matters
- It eats engineering time, interrupts focus, and is error-prone.
- Recurring toil is often a signal of a deeper cause, such as a [[Requirements Gap]], not just something to automate.

## When to use (this lens)
- Any task you've done by hand three or more times. Ask whether to automate it, turn it into a feature, or remove its cause.

## When to avoid
- One-off tasks, where automating costs more than doing it by hand.

## Links
- [[Requirements Gap]]

## Applied in
- [[Checkpoint Exam Restart]]: a reset script was run 3–4 times a month; eliminated by an operator self-service feature.
