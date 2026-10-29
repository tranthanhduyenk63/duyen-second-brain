---
type: practice
tags: [practice, ai-agents, refactoring, testing, ci-cd, architecture, migration]
created: 2026-10-29
---

# Preparing a Codebase for AI Coding Agents

## Context
On [[LMS Platform]], an inherited system of ~15 repositories that mixed legacy code with half-finished migration code. One goal was for AI coding agents (I use Claude) to contribute code.

## Problem
The old codebase was hard for agents and for people:
- Code from different layers was mixed together.
- Legacy patterns were everywhere, so an agent would copy them.
- Very hard to debug.
- Data was saved twice, into two data sources ([[Dual Write Problem]]).

## What I did
- **[[Hexagonal Architecture]], one service at a time** ([[Incremental Migration]]). This is still in progress:
  - **Service 1:** another person did the architecture migration. I cleaned up the bugs the migration introduced.
  - **Service 2:** a heavy service. I am migrating it myself, in progress.
  - Remaining services: not started yet.
- **API spec endpoint:** an endpoint that serves the specs of the APIs LMS provides, so an LLM can discover the available APIs ([[Machine-Readable API Spec]]).
- **Unit tests organized by use case** ([[Use-Case-Driven Testing]]): roughly 10% of the use cases in one service are covered so far.
- Refactored the CI pipelines. TODO(ask): what changed?
- Removed legacy code.

## Hardest parts
- **Cognitive load:** keeping the legacy behaviour, the new architecture and the in-between state in my head at once.
- **Rolling out the migration** so that existing features keep working. TODO(ask): how did you protect them? Tests first, feature flags, running old and new side by side, comparing outputs?

## Result
- Much faster delivery: I can now ship **3 features in 3 days**. TODO(ask): what was the pace before? 
- TODO(ask): your workflow with Claude, i.e. how you give it a task and how you review its output.

## Lessons
- TODO(ask): what would you tell someone starting the same migration? Candidates from what you said:
  - Migrate one service at a time and let the first one teach you; service 1 produced bugs that needed cleaning up.
  - Even partial test coverage (~10% of use cases) gives agents a feedback loop.

## Linked concepts
- [[Agent-Friendly Codebase]] · [[Hexagonal Architecture]] · [[Incremental Migration]] · [[Dual Write Problem]] · [[Machine-Readable API Spec]] · [[Use-Case-Driven Testing]] · [[Cognitive Load]]
