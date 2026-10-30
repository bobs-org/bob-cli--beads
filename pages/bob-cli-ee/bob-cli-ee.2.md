# Bead: bob-cli-ee.2 — bob-cli retyping of targeted existing tasks with D8 relocation

[Bead Pages](../README.md) / [bob-cli-ee](README.md) / bob-cli-ee.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.b6](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.b6.md) · **Assignee:** `bob-cli-ee.2` · **Size:** medium
**Created:** 2026-10-30 04:22:33 EDT · **Closed:** 2026-10-30 10:39:28 EDT
**Plan:** [202610/capture\_type\_marker.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/capture_type_marker.md)

## Description

existing: let `t:` retype the existing task an item targets (whole-item links, Ensure Next, toggle, relationship owners), and share the D8 relocation applier with `bob task move` so the task's live Task Link keeps agreeing with its type.

## Notes

[2026-10-30T14:39:09Z · bob-cli-ee.2] PROPOSED FOLLOW-UP: Skipped decisions:type-marker-is-orthogonal record per plan memory_record=no (t: orthogonality and named-Pomodoro agreement rules stay undocumented in memory).

[2026-10-30T14:39:28Z · bob-cli-ee.2] Implemented existing-task t: retyping with shared D8 relocation: grammar accepts whole-item links, Ensure Next, toggle, relationship owners (link-close still refuses); retype stages field before gesture with agreement check and closed refusal; shared pomodoro_themes/relocation_apply used by capture and bob task move (task_move stays green); type_relocation JSON + ledger human rows; docs updated; verified via cargo test type_marker_existing (11 pass), capture_type_marker (11 pass), lib relocation_apply (7 pass), lib type_marker (26 pass), lib task_move (54 pass); just check timed out after 9m still passing, focused gates green.

## Dependencies

- **Depends on:** [bob-cli-ee.1](bob-cli-ee.1.md) ✓ · ⧖ 2026-10-30
- **Blocks:** [bob-cli-ee.4](bob-cli-ee.4.md) ◐ · ⧖ 2026-10-30

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-ee.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-ee.2/README.md) | [bob-cli-ee.2](bob-cli-ee.2.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`0e17806`](https://github.com/bobs-org/bob-cli/commit/0e17806152599506b963ac64c1f466943f8a782b) | feat(capture): retype existing tasks with t: and D8 relocation | [bob-cli-ee.2](bob-cli-ee.2.md) | 2026-10-30 10:56:56 EDT |
