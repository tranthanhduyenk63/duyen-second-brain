---
type: concept
tags: [concept, release, devops, testing]
created: 2026-10-29
aliases: [Feature Flags, Feature Switches]
source: "Pete Hodgson, Feature Toggles (martinfowler.com, 2017)"
---

# Feature Toggles

> [!todo] Drafted by Claude: generic definition. Rewrite in your own words.

## Definition (in my words)
A runtime switch that turns a code path on or off, globally or for specific users or groups, without redeploying. This separates *deploying* code from *releasing* it.

## Why it matters
- Enables [[Testing in Production]], gradual rollouts, and an instant kill switch.
- Lets unfinished work be merged and deployed continuously ([[Continuous Delivery]]).

## When to use
- Risky changes, testing in production, gradual rollouts, migrations.

## When to avoid
- Leaving flags in place forever. Stale flags pile up as technical debt, so remove them once a change is fully rolled out.

## Links
- [[Testing in Production]] · [[Continuous Delivery]] · [[Incremental Migration]]

## Applied in
- [[Testing in Production with Feature Flags]]
