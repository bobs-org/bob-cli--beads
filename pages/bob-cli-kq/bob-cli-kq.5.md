# Bead: bob-cli-kq.5 — Small verified fixes

[Bead Pages](../README.md) / [bob-cli-kq](README.md) / bob-cli-kq.5

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.1bo](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.1bo.md) · **Assignee:** `bob-cli-kq.5` · **Size:** medium
**Created:** 2026-11-12 05:24:40 EST · **Closed:** 2026-11-12 06:23:56 EST
**Plan:** [202611/security\_audit\_fixes\_1.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/security_audit_fixes_1.md)

## Description

small-audit-fixes: prefix-match the pomodoro OVERDUE status, close the perl two-arg open in bob_pomodoro, report damaged albums as io instead of note_changed, require FILE args on bank import, and strip migration anchors by match span.

## Notes

[2026-11-12T10:49:35Z · bob-cli-kq.5] Verified prefix OVERDUE match (Rust notify + bob_notify), perl 3-arg open in bob_pomodoro, damaged albums as io not note_changed, required FILE on bank import with empty-list refusal, and tracker complete_line strip by BLOCK_ID match span. Focused tests passed; just check staged for host close.

[2026-11-12T11:22:48Z · bob-cli-kq.5--1] PROPOSED FOLLOW-UP: just check flake native::subprocess_runner::tests::{run,raw_run}_bounds_pipe_drain_when_detached_grandchild_holds_output — already tracked by bob-cli-kl; failed once under parallel full-suite load (exit 101, 6713 passed / 2 failed) and passed on an unchanged isolated rerun (2 passed, 4.02s).

[2026-11-12T11:23:56Z · bob-cli-kq.5--1] Implemented prefix OVERDUE match (Rust notify + bob_notify), Perl 3-arg open in bob_pomodoro, damaged albums as io not note_changed, required FILE on bank import with empty-list refusal, and tracker complete_line strip by BLOCK_ID match span. Focused tests passed. Full just check failed only on native::subprocess_runner pipe-drain tests already tracked by bob-cli-kl; those two passed on an unchanged isolated rerun. No leftover --epic-symbol entries.

[2026-11-12T12:01:46Z · bob-cli-kq.5--2] Second just check flake on recovery: native::subprocess_runner pipe-drain tests failed again under parallel load (6713 passed / 2 failed, tool run 8e18735080f6015c56939df7ca91e0cf). Isolated native::subprocess_runner::tests passed 6/6 in 4.22s. Already tracked by bob-cli-kl; five audit fixes unchanged.

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-kq.5](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-kq.5.md) | [bob-cli-kq.5](bob-cli-kq.5.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`736aa82`](https://github.com/bobs-org/bob-cli/commit/736aa820d4a9a25fe261f26a8103c4d69c9d5e7a) | fix: apply five small security-audit corrections | [bob-cli-kq.5](bob-cli-kq.5.md) | 2026-11-12 07:04:10 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-kq.5--2][1] | Need the phase scope, status, notes, and design file after failed just check recovery | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-kq.5.md

<!-- sase:referenced-by:end -->
