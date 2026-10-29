---
type: concept
tags: [concept, devops, release, ci-cd]
created: 2026-10-29
aliases: [CD, Small Releases]
source: "Jez Humble & David Farley, Continuous Delivery (2010)"
---

# Continuous Delivery

> [!todo] Drafted by Claude: generic definition. Rewrite in your own words.

## Definition (in my words)
Keeping software always releasable and shipping in small, frequent increments through an automated pipeline, instead of saving changes up for big releases.

## Why it matters
- Small changes are less risky, easier to debug, and give earlier feedback from users.
- Big-batch releases tend to be late and to arrive with many bugs at once.

## When to use
- Almost always for web systems, provided automated tests and CI/CD make it safe.

## When to avoid
- Contexts where releases are inherently costly, such as firmware or regulated sign-off. Even then, aim to integrate continuously.

## Links
- [[Analysis Paralysis]]

## Applied in
- [[LMS Initial Build]]: a big-chunk release that shipped late.
- [[LMS Platform]]: now released small, every day.
