---
type: practice
tags: [practice, incident, bug, data-integrity, lms]
created: 2026-10-29
---

# Attendance Records Lost on Holiday Reschedule

## Context
On [[LMS Platform]]. When a class schedule was rescheduled by the holiday setting, the class's existing attendance records went missing. This is the bug that took me the longest to find, out of the many I've fixed.

> [!question] TODO(ask): Is this related to the holiday reschedule script mentioned in [[Requirements Gap]]?

## Problem
- Symptom: after a holiday reschedule, existing attendance records for the class disappeared.
- TODO(ask): How was it noticed (teacher or operator report)? How often did it happen?

## What I did
- TODO(ask): Why did it take so long to find? E.g. it only happened under some conditions, it crossed several services, or there were no logs.
- TODO(ask): What was the root cause? E.g. the reschedule deleted and recreated sessions (losing the attendance linked to them), a Kafka event handled out of order, or a [[Dual Write Problem]].
- TODO(ask): What was the fix? Did you recover the lost data?

## Result
TODO(ask)

## Lessons
- TODO(ask)

## Linked concepts
- TODO: fill in once the root cause is known.
