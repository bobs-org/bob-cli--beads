# Bead: bob-cli-q5.2 — Snoozed rows in reconcile, walks, plan, and the agenda JSON

[Bead Pages](../README.md) / [bob-cli-q5](README.md) / bob-cli-q5.2

**Status:** ◐ in_progress · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.1fx](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.1fx.md) · **Assignee:** `bob-cli-q5.2` · **Size:** large
**Created:** 2026-11-25 10:22:52 EST
**Plan:** [202611/snoozed\_tasks.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/snoozed_tasks.md)

## Description

planned-today: reconcile treats live rows as recovery-only reach and never touches them; freshness, ]s, and bob walks exclude snoozed tasks; bob plan gains the snoozed meter and forecast lint; capture-pomodoros --tasks gains additive snoozed rows and woke_at.

## Dependencies

- **Depends on:** [bob-cli-q5.1](bob-cli-q5.1.md) ✓ · ⧖ 2026-11-25
- **Blocks:** [bob-cli-q5.4](bob-cli-q5.4.md) ◐ · ⧖ 2026-11-25
- **Blocks:** [bob-cli-q5.7](bob-cli-q5.7.md) ◐ · ⧖ 2026-11-25

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-q5.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-q5.2/README.md) | [bob-cli-q5.2](bob-cli-q5.2.md) | 0 |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-q5.1.1.land][1] | Check whether outer snooze phases consume wake-engine APIs before integration edits | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-q5.1.1.land.md

<!-- sase:referenced-by:end -->
