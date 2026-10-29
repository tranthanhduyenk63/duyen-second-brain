---
type: concept
tags: [concept, messaging, kafka, distributed-systems]
created: 2026-10-29
---

# Command vs Event Messages

> [!todo] Drafted by Claude: generic definition. Rewrite in your own words.

## Definition (in my words)
- **Command:** a request for one specific receiver to do something, named in the imperative (`EnrollStudent`). The sender expects it to be handled.
- **Event:** a fact that something already happened, named in the past tense (`StudentEnrolled`). The publisher doesn't know or care who consumes it, and there can be zero or many consumers.

## Why it matters
- The distinction makes ownership and coupling explicit: a command ties the sender to the receiver, while an event leaves consumers free to react independently.

## When to use
- Commands: when you need a specific action done asynchronously.
- Events: to notify others of a change, for data sync and data pipelines.

## When to avoid
- Don't disguise commands as events. An "event" that only exists to make one specific service do something is really a command.

## Links
- [[Event-Driven Data Synchronization]]

## Applied in
- [[LMS Platform]]: Kafka carries both commands and events. TODO(ask): separate topics, or a type field in the payload?
