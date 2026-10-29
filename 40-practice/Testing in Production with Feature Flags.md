---
type: practice
tags: [practice, testing, release, feature-flags]
created: 2026-10-29
---

# Testing in Production with Feature Flags

## Context
On [[LMS Platform]]. The dev environment was not fully or properly set up.

## Problem
I believed testing on dev first and then on prod was the safer, better order. That turned out wrong for this setup: with an incomplete dev environment, testing there was slow and didn't reflect production.

## What I did
Tested on production instead, using [[Feature Toggles|feature flags]] to limit who and what is affected. TODO(ask): what flag tool or mechanism? Flags per user, per class, or per operator?

## Result
Much faster testing.

## Lessons
- "Dev before prod" is not automatically better. If dev doesn't match prod, testing in production behind a flag is faster and more realistic ([[Testing in Production]]).
- Feature flags are what make it safe: they keep the damage small.

## Linked concepts
- [[Testing in Production]] · [[Feature Toggles]] · [[Continuous Delivery]]
