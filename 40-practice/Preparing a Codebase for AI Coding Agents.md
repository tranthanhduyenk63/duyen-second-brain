---
type: practice
tags: [practice, ai-agents, refactoring, testing, ci-cd, architecture]
created: 2026-10-29
---

# Preparing a Codebase for AI Coding Agents

## Context
On [[LMS Platform]], an inherited system of ~15 repositories that mixed legacy code with half-finished migration code. One goal was for AI coding agents to contribute code.

## Problem
In a codebase with inconsistent structure and leftover legacy paths, an agent has a hard time finding where things belong. Without tests, there is no automatic way to tell whether its changes are correct. TODO(ask): what specific problems did agents (or you) run into before the migration?

## What I did
- Restructured services to follow [[Hexagonal Architecture]].
- Added API navigation for LLMs. TODO(ask): format and how agents use it.
- Added unit tests.
- Refactored the CI pipelines. TODO(ask): what changed?
- Removed legacy code.

## Result
TODO(ask): How did agent output change? Fewer review fixes, more tasks delegated, faster delivery? Any numbers you can share?

## Lessons
- TODO(ask)

## Linked concepts
- [[Agent-Friendly Codebase]] · [[Hexagonal Architecture]] · [[Unit Testing]]
