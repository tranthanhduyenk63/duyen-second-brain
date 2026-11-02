---
type: practice
tags: [practice, incident, bug, data-integrity, legacy-code, lms]
created: 2026-10-29
---

# Attendance Records Lost on Holiday Reschedule

## Context
On [[LMS Platform]]. The previous team handled holiday rescheduling with a one-off script ([[Toil]] caused by a [[Requirements Gap]]). I turned it into a feature: when a class is rescheduled by the holiday setting, its sessions are regenerated. To build it, I reused the legacy logic from the previous team's script and added my own logic on top.

## Problem
- **Symptom:** after a holiday reschedule, the class's existing attendance records went missing.
- **How it surfaced:** teachers reported it, 2–3 times a month.
- **Why it took so long to find** (my longest bug hunt). Everything made it hard:
  - It only happened intermittently.
  - The flow crossed several services.
  - The logs were missing or not enough.
  - It was hard to reproduce on dev.
  - The code mixed legacy and migration code.

## What I did
- **Investigation:** tried to reproduce the bug, and used AI to read the logs and propose fixes.
- **Root cause:** the session regeneration logic contained a rule that removes attendances. It came with the legacy script code I reused, and I didn't notice it ([[Side Effect]]). The logic worked as a one-off script but didn't hold up as a feature that runs regularly.
- **Fix:** rewrote the business flow of the feature instead of patching the reused logic.
- **Data recovery:** the attendance data had also been saved to the legacy database ([[Dual Write Problem]]), so I wrote a script to restore the lost records from there.

## Result
- The bug was fixed and the lost attendance records were recovered.
- No prevention added yet (no regression test or alert). I still think one is worth adding.

## Follow-up
- [ ] Add a regression test (or [[Characterization Test]]) for session regeneration that asserts existing attendance is preserved.
- [ ] Add an alert for unexpected attendance deletions. TODO(ask): which one first?

## Lessons
- **Read legacy code fully before reusing it.** Hidden rules, such as deleting attendance, come along with it.
- **One-off script logic is not feature-grade.** Logic written for a developer to run manually rarely holds up when it runs regularly as a feature. Rewrite the flow for the feature.
- **The dual write saved me here.** The redundant copy that was a problem elsewhere was what made recovery possible. Keep a recovery path (backups, history) for data that teachers depend on.
- **A test that captures what the legacy code does before changing it** ([[Characterization Test]]) would likely have exposed the attendance-removal rule earlier.

## Linked concepts
- [[Side Effect]] · [[Characterization Test]] · [[Requirements Gap]] · [[Toil]] · [[Dual Write Problem]]
