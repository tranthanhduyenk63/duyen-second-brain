---
type: concept
tags: [concept, api, ai-agents, documentation]
created: 2026-10-29
aliases: [API Specification, OpenAPI Specification]
coined: true
---

# Machine-Readable API Spec

> [!question] TODO(ask): rename to **OpenAPI Specification** if the endpoint serves OpenAPI/Swagger.

> [!todo] Drafted by Claude: generic definition. Rewrite in your own words.

## Definition (in my words)
A structured description of a service's API (endpoints, parameters, schemas), e.g. OpenAPI, published where tools and LLMs can fetch it, instead of only as prose docs.

## Why it matters
- Agents and client generators can discover and call APIs correctly without reading the source code.
- It is a single source of truth for the API contract.

## When to use
- APIs consumed by other services, external clients, or AI agents.

## When to avoid
- TODO

## Links
- [[Agent-Friendly Codebase]]

## Applied in
- [[LMS Platform]]: an endpoint that serves the specs of the APIs LMS provides. TODO(ask): OpenAPI or a custom format? Generated from NestJS decorators?
