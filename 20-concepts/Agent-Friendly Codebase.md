---
type: concept
tags: [concept, ai-agents, developer-experience, architecture]
created: 2026-10-29
aliases: [AI-Ready Codebase]
coined: true
---

# Agent-Friendly Codebase

> [!todo] Drafted by Claude: generic definition. Rewrite in your own words.

## Definition (in my words)
A codebase structured so that AI coding agents can find their way around, make changes in the right place, and verify those changes automatically.

## Why it matters
- Agents copy the patterns they see, so a consistent structure gives consistent output, and inconsistency gives inconsistent output.
- Tests and CI are the agent's feedback loop. Without them, every change needs a human to check it.

## When to use
- Whenever agents write a meaningful share of the code.

## When to avoid
- TODO(ask)

## Links
- [[Context Engineering]] (broader: everything fed into an LLM's context) · [[Hexagonal Architecture]] · [[Unit Testing]]

## Applied in
- [[LMS Platform]]: see [[Preparing a Codebase for AI Coding Agents]].
