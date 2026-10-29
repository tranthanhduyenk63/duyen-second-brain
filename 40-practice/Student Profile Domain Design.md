---
type: practice
tags: [practice, ddd, domain-modeling, requirements]
created: 2026-10-29
---

# Student Profile Domain Design

## Context
On [[LMS Initial Build]], designed with [[Domain-Driven Design]]. The task was a **student profile** domain that collects student data from various other domains into one place.

## Problem
The design took a long time, for two reasons:
1. I didn't think the domain was necessary.
2. The requirements were unclear about which data needed to be shown and which didn't.

## What I did
TODO(ask): How was it resolved? Did you build it anyway? How did it collect the data: events from other services ([[Event-Carried State Transfer]]), calls to them at read time, or a copy of their data?

## Result
TODO(ask): Was the student profile used in the end? Was your doubt about it justified?

## Lessons
- When I doubt a requirement is needed, raise it early with the PO instead of working on the design while stuck. Unresolved doubt turns into [[Analysis Paralysis]].
- Before modelling a domain that collects data from others, pin down exactly which data it must show. Unclear requirements → unclear model.
- Next time: [[Timeboxing|timebox]] the domain design, then validate the model with the PO instead of refining it alone.
- TODO(ask): confirm or rewrite these in your own words.

## Linked concepts
- [[Domain-Driven Design]] · [[Analysis Paralysis]] · [[Timeboxing]] · [[YAGNI]]
