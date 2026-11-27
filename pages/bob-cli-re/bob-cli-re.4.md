# Bead: bob-cli-re.4 — Preserve Pomodoro block references around an existing timed entry

[Bead Pages](../README.md) / [bob-cli-re](README.md) / bob-cli-re.4

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-r8.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-r8.land.md) · **Assignee:** `bob-cli-re.4` · **Size:** medium
**Created:** 2026-11-27 15:31:19 EST · **Closed:** 2026-11-27 18:08:37 EST
**Plan:** [202611/task\_bead\_burndown\_3.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/task_bead_burndown_3.md)

## Description

timed-entry-close: fix the x=build stale Pomodoro reference, preserve closed time and children, and close bob-cli-qa.

## Notes

[2026-11-27T23:08:20Z · bob-cli-re.4] PROPOSED FOLLOW-UP: Triage clean-base just check failures (ToolRun 7deb599ecdc9172592a4025451478d14): native::prose::relocate::tests::relocation_round_trip_keeps_shortest_fragments_and_path_forms, native::prose::convert::inline::tests::extract_then_inline_preserves_eligible_sections, and prose::extract_refusals_return_the_contract_object_through_the_cli. These files were not touched by this phase; they match the prose failures bob-cli-re.3 already recorded and the plan assigned to bob-cli-qj. origin/master already has 7d48b7b2 (fix(prose): keep link form and shortest fragments across extract and inline).

[2026-11-27T23:08:37Z · bob-cli-re.4] Forwarded existing next Pomodoro identities through file_recorded_block drain-then-insert and pinned Next refs with locate_next_headline against the filed scan so after is an entry headline. x=build with a closed timed WORK child no longer panics; WORK time, child, and a trailing same-name BUILD stay. Verified: three new pomodoro_close record tests (dry-run/real, childless timed, reorder), 98 pomodoro_close, 34 pomodoro_past, 23 successor_verdicts including ID-less cancel, 41 capture::pomodoro lib tests. cargo fmt --check clean. just check (ToolRun 7deb599ecdc9172592a4025451478d14) exits 101 on three untouched prose tests already recorded as PROPOSED FOLLOW-UP; epic-symbols: none.

## Dependencies

- **Depends on:** [bob-cli-re.3](bob-cli-re.3.md) ✓ · ⧖ 2026-11-27
- **Blocks:** [bob-cli-re.5](bob-cli-re.5.md) ◐ · ⧖ 2026-11-27

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-re.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-re.4/README.md) | [bob-cli-re.4](bob-cli-re.4.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`f0ee435`](https://github.com/bobs-org/bob-cli/commit/f0ee43574e93287b89a1874415327c79d68df2a3) | fix(capture): pin Pomodoro Next refs after recording a timed entry | [bob-cli-re.4](bob-cli-re.4.md) | 2026-11-27 18:09:51 EST |
