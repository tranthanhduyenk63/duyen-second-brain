---
type: practice
tags: [practice, incident, kafka, reliability, authentication, vendor]
created: 2026-10-29
---

# Kafka Outage Took Down Authentication

## Context
On [[LMS Platform]]. Kafka carries commands and events between services ([[Command Message]], [[Event Message]]). The Kafka cluster was a managed service from an external provider, and only DevOps had admin privileges on it.

## Problem
- The provider's Kafka went down.
- The authentication service **crashed on startup when it couldn't connect to Kafka**. With auth down, nobody could log in, so the whole system was effectively down: a [[Cascading Failure]] with Kafka as a [[Single Point of Failure]].
- Other services did **not** crash. They only lost their event flow.
- **Detection:** users reported it, not monitoring.
- **Duration:** about one hour.

## What I did
- **In the moment:**
  - Restarted the services.
  - Notified DevOps, who had admin privileges, to check Kafka's health.
- **Fix:** changed the code so services no longer depend on Kafka at startup. Auth now starts and serves logins even when Kafka is unavailable ([[Graceful Degradation]]).
- **Longer term:** planning to move Kafka to another vendor or to self-host it.

## Result
- The dependency was removed. A Kafka outage should no longer take down authentication.
- The vendor move is planned but not yet done.

## Lessons
- **Critical-path services must not have a hard startup dependency on async infrastructure.** Auth should still start if the broker is down, and reconnect when it's back.
- **Check what each service does when a dependency is unavailable,** especially at startup. Auth crashed while the other services degraded gracefully, so the behaviour was inconsistent.
- **Users found the outage before we did.** TODO(ask): did you add alerting on Kafka connectivity or auth health afterwards?
- **For a managed service from a vendor, know the escalation path in advance:** who has admin access, and how fast they can respond.

## Follow-up
- [ ] Move Kafka to another vendor or self-host.
- [ ] TODO(ask): alerting so the team finds out before users do?

## Linked concepts
- [[Cascading Failure]] · [[Single Point of Failure]] · [[Graceful Degradation]] · [[Event Message]]
