# Bead: bob-cli-h8.8 — Align task-status-cycler's deferred-only close with bob

[Bead Pages](../README.md) / [bob-cli-h8](README.md) / bob-cli-h8.8

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.18c](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.18c.md) · **Assignee:** `bob-cli-h8.8` · **Size:** small
**Created:** 2026-11-04 16:39:09 EST · **Closed:** 2026-11-04 17:56:05 EST
**Plan:** [202611/top\_ten\_bead\_bundles.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/top_ten_bead_bundles.md)

## Description

cycler-keeps-timed-close: apply the chosen bob-cli-g4 policy. By default, remove the task-status-cycler deferredOnlyClose/deletedClosedEntry special case so a closed timed row survives while its links still defer. Assert the full expected_day of the shared vector, update the docs, and close g4.

## Notes

[2026-11-04T22:56:05Z · bob-cli-h8.8] Applied g4 keep policy in bob-plugins task-status-cycler: removed the deferredOnlyClose/deletedClosedEntry special case (src 060/060b/135/137/170), rebuilt main.js (build:check clean, zero special-case refs). Shared vector close-defers-not-started-off-clock asserts full expected_day byte-for-byte, matching bob capture x. Docs updated (task-status-cycler.md, pomodoro_clock README). Verified: all cycler suites 533/533, full npm test 5448/5448, docs inventory + docs-check pass, bob plugins sync deployed and vault main.js byte-identical. Closed g4. No epic-symbol leftovers. Uncommitted changes left in the linked bob-plugins checkout for review (no commit per policy).

## Dependencies

- **Depends on:** [bob-cli-h8.1](bob-cli-h8.1.md) ✓ · ⧖ 2026-11-04
- **Blocks:** [bob-cli-h8.13](bob-cli-h8.13.md) ◐ · ⧖ 2026-11-04

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-h8.8](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-h8.8/README.md) | [bob-cli-h8.8](bob-cli-h8.8.md) | 0 |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-h8.8][1] | Need the phase scope and design file | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-h8.8/README.md

<!-- sase:referenced-by:end -->
