---
type: concept
tags: [concept, architecture, design, ddd]
created: 2026-10-29
aliases: [DDD]
source: "Eric Evans, Domain-Driven Design (2003)"
---

# Domain-Driven Design

> [!todo] Drafted by Claude: generic definition. Rewrite in your own words.

## Definition (in my words)
Designing software around a model of the business domain, built together with domain experts. The model uses a shared vocabulary (ubiquitous language), is divided into bounded contexts, and protects its rules with aggregates.

## Why it matters
- Code structure follows business concepts, so it can change as the business changes.
- Bounded contexts give natural service boundaries in [[Microservices Architecture]].

## When to use
- Complex business domains with many rules and long-lived systems.

## When to avoid
- Simple CRUD, or when requirements are too unclear to model. In that case, modelling turns into [[Analysis Paralysis]].

## Links
- [[Hexagonal Architecture]] · [[Microservices Architecture]]

## Applied in
- [[LMS Initial Build]]: used deliberately. See [[Student Profile Domain Design]].
