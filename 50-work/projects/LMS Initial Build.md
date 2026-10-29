---
type: project
tags: [project, lms, ddd, team, nestjs, nextjs, mongodb, kafka, redis]
created: 2026-10-29
status: completed
role: [developer]
---

# LMS Initial Build

A learning management system built at the same company to support the operations team: Customer Support, Head Office and Teachers.

> [!question] TODO(ask): Is this the same system as [[LMS Platform]] at an earlier stage, or a separate LMS? When did it run?

## Goal
Support the operations team (Customer Support, Head Office, Teachers) in running classes and students. TODO(ask): specific goals or success measures.

## Team & role
- About 5 developers, 1 APO (TODO(ask): Associate Product Owner?) and 1 BA.
- **My role:** developer. I owned work by feature.
- **Side quest:** set up the infrastructure for the team's Metabase system. TODO(ask): what this involved, e.g. deployment, data sources, read replicas.

## Architecture
- Same stack as [[LMS Platform]]: Next.js, NestJS, MongoDB, Kafka, Redis.
- Designed deliberately with [[Domain-Driven Design]].

## Key decisions
- Model the system with [[Domain-Driven Design]]. See [[Student Profile Domain Design]].

## Problems I hit
- **Domain design took a long time,** e.g. the student profile domain. See [[Student Profile Domain Design]].
- **Late delivery:** the work was released as one big chunk, and it shipped late.
- **Built features nobody needed:** a task module that turned out to be useless, and many others ([[YAGNI]]).

## What I'd do differently
- **Act sooner and avoid [[Analysis Paralysis]]:** spend less time stalled before acting, e.g. [[Timeboxing|timebox]] design.
- **Release continuously** instead of waiting for one big chunk ([[Continuous Delivery]]). I now release small and every day on [[LMS Platform]].
- **Challenge requirements from the PO** before building, so features like the task module don't get built ([[YAGNI]]). Related: [[Requirements Gap]], the same problem from the opposite side (something needed was missed, rather than something unneeded built).

## Linked concepts
- [[Domain-Driven Design]] · [[Analysis Paralysis]] · [[Timeboxing]] · [[Continuous Delivery]] · [[YAGNI]] · [[Requirements Gap]]
