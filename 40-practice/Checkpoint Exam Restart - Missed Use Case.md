---
type: practice
tags: [practice, incident, product, requirements, support]
created: 2026-10-29
---

# Checkpoint Exam Restart: Missed Use Case

## Context
On [[LMS Platform]], inherited from another team. A recurring support issue: a student missed their checkpoint exam and then couldn't start it again. The previous team handled every occurrence by running a one-off script that reset the student's checkpoint record.

## Problem
It looked like an intermittent bug, but the system was doing exactly what it was built to do. Nobody had designed the case "a student misses a checkpoint and needs to retake it", so every occurrence turned into a manual data fix by a developer.

## What I did
- Suspected by instinct that it wasn't a defect but a [[Missed Use Case]].
- Verified with stakeholders what students actually needed, and confirmed that a student who misses a checkpoint is allowed to restart it.
- Built a **restart checkpoint** feature:
  - Only the class's operator can trigger it ([[Role-Based Access Control]]).
  - Every restart is recorded in an update history ([[Audit Trail]]).
- Handed the fix to operations as a button in the UI, replacing the developer-run script.

## Result
- Before: the script was run 3–4 times a month.
- The issue stopped coming to me. I never needed to run the script again.
- Operators handle it themselves with the feature button.

## Lessons
- A manual data fix that keeps recurring usually means a feature is missing, not that there's a bug. If the same script keeps running, ask what use case it stands in for.
- Confirm the business rule with stakeholders before "fixing" anything. Here the right behaviour (restart allowed) was a policy decision, not a technical one.
- Move recurring fixes from developers to operations with proper guards: a permission check and an audit history.
- Trust the instinct that something is a use case rather than a bug, but verify it with stakeholders before building.
- This was not a one-off. Other recurring scripts also stood in for missing use cases, e.g. a script to reschedule classes for holidays. See [[Missed Use Case]].

## Linked concepts
- [[Missed Use Case]] · [[Role-Based Access Control]] · [[Audit Trail]] · [[Owning a Product End-to-End]]
