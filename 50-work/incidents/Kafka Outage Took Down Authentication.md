---
type: practice
tags: [practice, incident, kafka, reliability, authentication]
created: 2026-10-29
---

# Kafka Outage Took Down Authentication

## Context
On [[LMS Platform]]. Kafka carries commands and events between services ([[Command Message]], [[Event Message]]).

## Problem
When Kafka went down, the whole system crashed, because the authentication service depended on Kafka. With authentication down, nobody could use anything: a [[Cascading Failure]] from a [[Single Point of Failure]].

## What I did
- TODO(ask): Why did authentication depend on Kafka? E.g. publishing login events synchronously, or consuming user data from it.
- TODO(ask): How did you recover, and did you remove or soften the dependency afterwards?

## Result
TODO(ask)

## Lessons
- A critical path service (authentication) should not need asynchronous infrastructure to be up. TODO(ask): confirm, or put it in your own words.

## Linked concepts
- [[Cascading Failure]] · [[Single Point of Failure]] · [[Event Message]]
