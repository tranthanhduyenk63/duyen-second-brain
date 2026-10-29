---
type: project
tags: [project, backend, microservices, nestjs, nextjs, mongodb, kafka, redis, ai-agents]
created: 2026-10-29
status: active
role: [product-owner, business-analyst, developer, devops, customer-support]
---

# LMS Platform

A learning management system used by an internal operations team. I took full ownership about a year ago (~2025-10) after it was handed over from another team. I act as Product Owner, Business Analyst, Developer, DevOps and Customer Support.

## Goal
- Maintain and develop the system so it supports the operations team.
- Migrate the codebase so that AI coding agents can work on it productively. See [[Preparing a Codebase for AI Coding Agents]].

## Scale
- ~200–300 users per day
- ~15 repositories

## Architecture
- [[Microservices Architecture]], split into layers: **web → api → services → integrations**.
- **Web:** Next.js.
- **Backend:** NestJS services.
- **Messaging:** Kafka carries both commands and events (see [[Command vs Event Messages]]). It is used for:
  - Service-to-service communication. For example, a service listens to another service's "updated" event and updates its own copy of the data ([[Event-Driven Data Synchronization]]).
  - Dispatching events to a data pipeline.
- **Database:** MongoDB, inherited. The [[Document Model]] fits nested data well, but search and index performance were poor, so search moved to OpenSearch ([[Secondary Search Index]]).
- **Redis:** [[Caching]], [[Rate Limiting]] and [[Distributed Lock]]s.
- **Infrastructure:** Kubernetes, with CI/CD pipelines in Azure (TODO(ask): Azure DevOps Pipelines? AKS?).

## State when I inherited it
- Functionally fairly stable.
- The code mixed legacy code with half-finished migration code.
- Several intermittent bugs. The previous team fixed their effects by hand with one-off scripts instead of fixing the root cause.

## Key decisions
- Restructure services to follow [[Hexagonal Architecture]].
- Add API navigation for LLMs (TODO(ask): what this is, e.g. an API index or docs that agents read).
- Add unit tests.
- Refactor the CI pipelines.
- Remove legacy code.
- Use OpenSearch for search instead of relying on MongoDB indexes (TODO(ask): was this your decision or inherited?).

## Problems I hit
- Intermittent bugs that had been "fixed" with manual scripts. Several turned out to be [[Missed Use Case]]s, not defects. For example, checkpoint exam restarts (see [[Checkpoint Exam Restart - Missed Use Case]]) and rescheduling classes for holidays.
- Poor MongoDB search and index performance.
- Customer support tickets about login, enrollment requests and data export. Many of these became bug fixes or features. See [[Owning a Product End-to-End]].
- Context switching between roles.

## What I'd do differently
- TODO(ask)

## Linked concepts
- [[Microservices Architecture]] · [[Hexagonal Architecture]] · [[Command vs Event Messages]] · [[Event-Driven Data Synchronization]] · [[Document Model]] · [[Secondary Search Index]] · [[Caching]] · [[Rate Limiting]] · [[Distributed Lock]] · [[Agent-Friendly Codebase]] · [[Missed Use Case]] · [[Role-Based Access Control]] · [[Audit Trail]]
