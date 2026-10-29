---
type: concept
tags: [concept, testing, architecture]
created: 2026-10-29
aliases: [Use Case Tests, Sociable Unit Tests]
coined: true
---

# Use-Case-Driven Testing

> [!question] TODO(ask): keep this coined name, or rename to **Sociable Unit Tests** (Fowler)?

> [!todo] Drafted by Claude: generic definition. Rewrite in your own words.

## Definition (in my words)
Writing tests around application use cases (e.g. "operator restarts a student's checkpoint") instead of around individual classes or methods. In [[Hexagonal Architecture]], use cases are the application core, so they can be tested with fake adapters.

## Why it matters
- Tests describe business behaviour, so they survive refactoring.
- Coverage can be measured as a share of use cases, which is meaningful to the business.

## When to use
- Services with clear use cases, especially during a refactor where behaviour must be preserved.

## When to avoid
- Pure utility code, where plain function-level unit tests fit better.

## Links
- [[Hexagonal Architecture]] · [[Unit Testing]]

## Applied in
- [[Preparing a Codebase for AI Coding Agents]]: about 10% of the use cases in one service are covered.
