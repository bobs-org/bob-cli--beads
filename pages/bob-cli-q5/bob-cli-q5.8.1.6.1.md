# Bead: bob-cli-q5.8.1.6.1 — Restore the build and verify each wake against a fresh bob read

[Bead Pages](../README.md) / [bob-cli-q5.8.1.6](bob-cli-q5.8.1.6.md) / bob-cli-q5.8.1.6.1

**Status:** ◐ in_progress · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-q5.8.1.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-q5.8.1.land.md) · **Assignee:** `bob-cli-q5.8.1.6.1` · **Size:** medium
**Created:** 2026-11-26 20:05:50 EST
**Plan:** [202611/mac\_snooze\_wake\_notice\_repair.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/mac_snooze_wake_notice_repair.md)

## Description

runtime-verify: fix the StatusItemGlyph build break, make every accepted receipt verify against a bob snooze read started after it, deliver immediately when nothing held, gate and atomically publish the notifier claim, and make the snooze process lanes serialize writes, surface bob refusals, and never cancel each other.

## Dependencies

- **Blocks:** [bob-cli-q5.8.1.6.2](bob-cli-q5.8.1.6.2.md) ◐ · ⧖ 2026-11-26

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-q5.8.1.6.1](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-q5.8.1.6.1.md) | [bob-cli-q5.8.1.6.1](bob-cli-q5.8.1.6.1.md) | 0 |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-q5.8.1.6.1--2][1] | Need phase scope and notes before finishing the assigned snooze wake repair | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-q5.8.1.6.1.md

<!-- sase:referenced-by:end -->
