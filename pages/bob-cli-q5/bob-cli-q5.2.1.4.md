# Bead: bob-cli-q5.2.1.4 — Publish later-today agenda rows and wake provenance

[Bead Pages](../README.md) / [bob-cli-q5.2.1](bob-cli-q5.2.1.md) / bob-cli-q5.2.1.4

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-q5.2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-q5.2.md) · **Assignee:** `bob-cli-q5.2.1.4` · **Size:** medium
**Created:** 2026-11-25 19:37:41 EST · **Closed:** 2026-11-26 05:57:41 EST
**Plan:** [202611/snoozed\_planned\_today.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/snoozed_planned_today.md)

## Description

agenda-provenance: add the schema-1 capture-pomodoros --tasks snoozed block and optional woke_at/snoozed_target item fields, including notes and zoned wake instants. Add agenda goldens and one cross-command lifecycle regression, update JSON contracts, and leave complete verification evidence for this child epic's land agent to close bob-cli-q5.2.

## Notes

[2026-11-26T10:57:16Z · bob-cli-q5.2.1.4] PROPOSED FOLLOW-UP: `just check` reports broad drawer/capture failures in the library and CLI targets (43 lib, 55 CLI); focused clean-base runs at HEAD 4a812173 reproduce `native::capture::block_diff::tests::annotate_drawer_lines_uses_after_snapshot_except_removed` and `capture::authored::capture_drawer_authored_children_and_composition` with identical assertions and exit 101. Same pre-existing issue is recorded in bob-cli-q5.2.1.3 note #1, which points to the existing bob-cli-q9, bob-cli-q4, and bob-cli-q7 tracks; no open task bead specifically matched this failure. Unrelated to snoozed agenda provenance.

[2026-11-26T10:57:41Z · bob-cli-q5.2.1.4] Implemented the schema-1 `capture-pomodoros --tasks` snoozed rows and next wake timestamp, plus optional woke_at/snoozed_target provenance on eligible agenda task items. Added agenda goldens, lifecycle coverage across snooze/reconcile/freshness/walks/plan/agenda and repeated wake, and updated capture, snooze, and JSON contracts. Verified cargo check --tests, all 25 pomodoros_agenda CLI tests, just docs-gen, just docs-check, and git diff --check. Full just check failed on 43 lib and 55 CLI pre-existing drawer/capture tests; focused clean-base runs reproduced representative failures identically and are recorded in note #1. epic-symbols returned no leftovers.

## Dependencies

- **Depends on:** [bob-cli-q5.2.1.1](bob-cli-q5.2.1.1.md) ✓ · ⧖ 2026-11-25
- **Depends on:** [bob-cli-q5.2.1.3](bob-cli-q5.2.1.3.md) ✓ · ⧖ 2026-11-25

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-q5.2.1.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-q5.2.1.4/README.md) | [bob-cli-q5.2.1.4](bob-cli-q5.2.1.4.md) | 2 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`f32e774`](https://github.com/bobs-org/bob-cli/commit/f32e774c92ec7ae564c5f6926563bd2a8adef772) | feat(agenda): publish snoozed rows and wake provenance | [bob-cli-q5.2.1.4](bob-cli-q5.2.1.4.md) | 2026-11-26 05:59:33 EST |
| bob-plugins | `bob-plugins@f32e774` | feat(agenda): publish snoozed rows and wake provenance | [bob-cli-q5.2.1.4](bob-cli-q5.2.1.4.md) | 2026-11-26 05:59:33 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-q5.2.1.4][1] | Need the phase scope and design file | 3 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-q5.2.1.4/README.md

<!-- sase:referenced-by:end -->
