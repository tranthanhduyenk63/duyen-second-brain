---
type: concept
tags: [concept, messaging, kafka, distributed-systems]
created: 2026-10-29
aliases: [Command]
source: "Hohpe & Woolf, Enterprise Integration Patterns (2003)"
---

# Command Message

> [!todo] Drafted by Claude: generic definition. Rewrite in your own words.

## Definition (in my words)
An asynchronous message asking one specific receiver to do something, named in the imperative (`EnrollStudent`). The sender expects it to be handled.

## Why it matters
- The request is decoupled in time: the receiver can be down or slow. But the sender is still logically coupled to that receiver.

## When to use
- When you need a specific action done asynchronously by a known service.

## When to avoid
- Don't disguise it as an [[Event Message]]. An "event" that exists only to make one specific service act is really a command.

## Links
- [[Event Message]]

## Applied in
- [[LMS Platform]]: Kafka carries COMMAND messages between services. TODO(ask): separate topics, or a type field in the payload?
