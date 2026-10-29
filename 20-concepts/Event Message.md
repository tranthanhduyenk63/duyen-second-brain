---
type: concept
tags: [concept, messaging, kafka, distributed-systems]
created: 2026-10-29
aliases: [Domain Event, Event]
source: "Hohpe & Woolf, Enterprise Integration Patterns (2003)"
---

# Event Message

> [!todo] Drafted by Claude: generic definition. Rewrite in your own words.

## Definition (in my words)
A message announcing that something already happened, named in the past tense (`StudentEnrolled`). The publisher doesn't know or care who consumes it, and there can be zero or many consumers.

## Why it matters
- Consumers can react independently, and new consumers can be added without changing the publisher.

## When to use
- Notifying other services of a change, syncing data ([[Event-Carried State Transfer]]), and feeding data pipelines.

## When to avoid
- When you need one specific receiver to act and to know whether it succeeded. Use a [[Command Message]] or a synchronous call instead.

## Links
- [[Command Message]] · [[Event-Carried State Transfer]]

## Applied in
- [[LMS Platform]]: Kafka EVENT messages, e.g. "updated" events that other services consume to update their data, and events dispatched to the data pipeline.
