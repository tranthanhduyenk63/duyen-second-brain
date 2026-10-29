---
type: concept
tags: [concept, security, authorization]
created: 2026-10-29
---

# Role-Based Access Control

> [!todo] Drafted by Claude: generic definition. Rewrite in your own words.

## Definition (in my words)
Granting permissions to roles (e.g. operator, student) instead of to individual users. A user can do an action only if one of their roles allows it, sometimes limited to a scope (e.g. *their own* class).

## Why it matters
- Sensitive actions can be safely handed to non-developers.

## When to use
- Any action that changes data for other people or bypasses normal rules, such as resets and overrides.

## When to avoid
- When the rules depend on many attributes (time, ownership, state) and roles alone can't express them. Consider attribute-based access control instead.

## Links
- [[Audit Trail]]

## Applied in
- [[Checkpoint Exam Restart - Missed Use Case]]: only the class's operator can restart a checkpoint.
