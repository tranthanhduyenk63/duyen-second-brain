---
type: concept
tags: [concept, architecture, design]
created: 2026-10-29
aliases: [Ports and Adapters]
source: "Alistair Cockburn (2005)"
---

# Hexagonal Architecture

> [!todo] Drafted by Claude: generic definition. Rewrite in your own words.

## Definition (in my words)
Also called Ports and Adapters. Business logic sits at the centre and depends only on interfaces (ports) that it defines. HTTP controllers, databases, Kafka and external APIs are adapters that plug into those ports, so the core does not depend on any framework or infrastructure.

## Why it matters
- The core can be unit-tested without infrastructure.
- Infrastructure (DB, broker, vendor) can be swapped by writing a new adapter.
- Every service has the same predictable layout, which helps people and [[Agent-Friendly Codebase|AI agents]] know where code goes.

## When to use
- Services with real business logic that will live a long time.

## When to avoid
- Thin CRUD services or small scripts, where the extra layers add little.

## Links
- Contrast with a framework-centric layered structure, where business logic imports the ORM directly.
- [[Domain-Driven Design]] · [[Incremental Migration]] · [[Use-Case-Driven Testing]]

## Applied in
- [[LMS Platform]]: restructured the NestJS services to this pattern. See [[Preparing a Codebase for AI Coding Agents]].
