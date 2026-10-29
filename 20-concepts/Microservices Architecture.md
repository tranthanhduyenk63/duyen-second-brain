---
type: concept
tags: [concept, architecture, distributed-systems]
created: 2026-10-29
---

# Microservices Architecture

> [!todo] Drafted by Claude: generic definition. Rewrite in your own words.

## Definition (in my words)
A system split into independently deployable services, each owning one part of the domain and its own data. Services talk over the network, either synchronously (HTTP) or asynchronously (messaging).

## Why it matters
- Teams can deploy and scale services independently.
- The cost is distributed-systems complexity: data consistency across services ([[Event-Carried State Transfer]]), observability, and many repositories to maintain.

## When to use
- Several teams, or parts of the domain that need to deploy or scale independently.

## When to avoid
- A small team or a single owner, where a modular monolith is often cheaper. TODO(ask): is this your view after running ~15 repos alone?

## Links
- [[Command Message]] and [[Event Message]]

## Applied in
- [[LMS Platform]]: layered as web → api → services → integrations.
