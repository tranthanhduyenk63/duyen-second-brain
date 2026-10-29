---
type: concept
tags: [concept, testing, release, devops]
created: 2026-10-29
aliases: [TiP, Test in Prod]
source: "Cindy Sridharan, Testing in Production, the safe way (2018)"
---

# Testing in Production

> [!todo] Drafted by Claude: generic definition. Rewrite in your own words.

## Definition (in my words)
Verifying changes in the real production environment, with real data, traffic and infrastructure, using safety controls that limit the damage: feature flags, canary releases or internal-only users.

## Why it matters
- Production is the only environment that is truly production-like. Staging and dev drift, and often aren't fully set up.
- It gives faster and more realistic feedback.

## When to use
- When pre-production environments are incomplete or unrepresentative, and the change can be isolated behind a flag.

## When to avoid
- Without a way to limit the damage (no flags, no rollback), or for irreversible operations such as destructive data migrations or payments.

## Links
- [[Feature Toggles]] · [[Continuous Delivery]]

## Applied in
- [[Testing in Production with Feature Flags]]
