# Bead: bob-cli-q4.1 — Hand-edit mirror never writes across notes

[Bead Pages](../README.md) / [bob-cli-q4](README.md) / bob-cli-q4.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.1fw](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.1fw.md) · **Assignee:** `bob-cli-q4.1` · **Size:** medium
**Created:** 2026-11-25 08:51:35 EST · **Closed:** 2026-11-25 09:06:13 EST
**Plan:** [202611/better\_o\_gesture\_settle.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/better_o_gesture_settle.md)

## Description

mirror-guard: fix bead bob-cli-py. Check the debounced dependency and mention mirrors against the original note path, flush or cancel them when the note changes, stop the baseline cache poisoning, and add a regression test that switches notes inside the debounce window.

## Notes

[2026-11-25T14:05:47Z · bob-cli-q4.1] PROPOSED FOLLOW-UP: task_reqs fixture skew (plugin NOTES vs bob-cli bold **Notes**) fails test-task-reqs-twin-copies and task-reqs-vectors canonical comparisons when the bob-cli checkout is present; files untouched by mirror-guard, belongs to ph.7 spelling-flip scope (open-lines/notes-key phases)

[2026-11-25T14:05:52Z · bob-cli-q4.1] PROPOSED FOLLOW-UP: frees-marks 25ms synthetic-build budget flake (32ms observed) fails intermittently; already tracked by task bead bob-cli-io per bob-cli-pf.4.1 notes, +1 evidence there

[2026-11-25T14:06:13Z · bob-cli-q4.1] Mirror-guard done and verified: debounced dependency/mention mirrors drop the pass when the editor switched notes (600a guard mixin + lifecycle cancel on leaf/file change, no baseline poisoning), 5 new regression tests pass (16/16 mirror suite, 76/76 across mirror+relation suites), build:check and docs inventory clean, nav bumped 2.107.3->2.107.4. Pre-existing failures recorded as PROPOSED FOLLOW-UP (task_reqs NOTES skew, frees-marks budget flake already tracked by bob-cli-io); full unit suite 9429/9436 with only those 3 unrelated failures.

## Dependencies

- **Blocks:** [bob-cli-q4.13](bob-cli-q4.13.md) ◐ · ⧖ 2026-11-25
- **Blocks:** [bob-cli-q4.5](bob-cli-q4.5.md) ◐ · ⧖ 2026-11-25

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-q4.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-q4.1/README.md) | [bob-cli-q4.1](bob-cli-q4.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@9a98738`](https://github.com/bobs-org/bob-plugins/commit/9a987385709c0d4ada689c94b9c0e66798e81c2f) | fix(nav): drop debounced hand-edit mirror pass when the editor switched notes | [bob-cli-q4.1](bob-cli-q4.1.md) | 2026-11-25 09:07:04 EST |
