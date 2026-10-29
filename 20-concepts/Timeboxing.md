---
type: concept
tags: [concept, process, decision-making, agile]
created: 2026-10-29
aliases: [Timebox, Time-boxing]
source: "James Martin, Rapid Application Development (1991); used in Scrum (sprints, spikes) and DSDM"
---

# Timeboxing

> [!todo] Drafted by Claude: generic definition. Rewrite in your own words.

## Definition (in my words)
Setting a fixed, non-negotiable amount of time for an activity (design, research, a spike, a meeting) and deciding or shipping whatever you have when the time runs out. Scope flexes and time doesn't.

## Why it matters
- It forces a decision before uncertainty is fully gone, which is the main cure for [[Analysis Paralysis]].
- It makes the cost of exploration explicit and limited.
- When time runs out, the remaining questions usually reveal what to ask stakeholders, or what to learn by shipping a small slice ([[Continuous Delivery]]).

## When to use
- Domain or system design with unclear requirements, e.g. timebox the model, then validate it with the PO.
- Spikes and research, debugging rabbit holes, and choosing between tools.

## When to avoid
- Work where the deadline doesn't change the quality bar, such as security fixes or data-migration correctness. There, timebox the *investigation*, not the *fix*.

## Links
- [[Analysis Paralysis]] · [[Continuous Delivery]] · [[YAGNI]] · [[Domain-Driven Design]]

## Applied in
- TODO(ask): none recorded yet. Adopted as a lesson from [[Student Profile Domain Design]] ([[LMS Initial Build]]).
