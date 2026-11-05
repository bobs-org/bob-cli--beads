# Bead: bob-cli-hd.6 — Close settle and new typed entries in bob

[Bead Pages](../README.md) / [bob-cli-hd](README.md) / bob-cli-hd.6

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.research.5q.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.research.5q.linker.w0.md) · **Assignee:** `bob-cli-hd.6` · **Size:** medium
**Created:** 2026-11-05 10:26:34 EST · **Closed:** 2026-11-05 13:06:27 EST
**Plan:** [202611/pomodoro\_names\_follow\_task\_types.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/pomodoro_names_follow_task_types.md)

## Description

bob-close-and-naming: close names settle to the worked types and the continuation is agreement-stable; a capture `#NAME` / `=name` entry created by the same run retypes the tasks landing in it.

## Notes

[2026-11-05T18:01:56Z · bob-cli-hd.6] PROPOSED FOLLOW-UP: plan::plan_reports_full_budget_as_json fails on clean base (6 unexpected type_mismatch lints); likely reconcile-pass residue, needs triage

[2026-11-05T18:02:04Z · bob-cli-hd.6] PROPOSED FOLLOW-UP: task_move::move_without_field_relocates_live_link_to_new_inherited_type fails on clean base (relocated empty); needs triage

[2026-11-05T18:02:08Z · bob-cli-hd.6] PROPOSED FOLLOW-UP: just lint and cargo fmt are red on clean base from task_status_hooks/sync.rs apply_type_agreement residue (collapsible_if at 1625, fmt drift) plus plan_budget/mod.rs fmt drift; needs triage

[2026-11-05T18:06:27Z · bob-cli-hd.6] Close settle via settle_closed + shed/agree-stable continuation (single-type may rename; MEET/x0/reuse unchanged); capture #NAME/=name into same-run-created entries retypes via shared landing choke point (recorded per-batch set); narrow_closed removed, narrow vectors kept for JS mirror; docs R6/Named-captures/close-names updated. Verified: lib 5095 pass, cli 3162 pass (2 failures + lint/fmt drift reproduce identically on clean base, recorded as PROPOSED FOLLOW-UPs), parity suites pass, task_status_hooks/pomodoro_close/themes/docs_reference 324 pass, just docs-check pass, fmt/clippy clean on touched files.

## Dependencies

- **Depends on:** [bob-cli-hd.5](bob-cli-hd.5.md) ✓ · ⧖ 2026-11-05
- **Blocks:** [bob-cli-hd.9](bob-cli-hd.9.md) ◐ · ⧖ 2026-11-05

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-hd.6](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-hd.6/README.md) | [bob-cli-hd.6](bob-cli-hd.6.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`bfd7b00`](https://github.com/bobs-org/bob-cli/commit/bfd7b00570d4eaea7eb6a2ff8021b9a1186619c8) | feat(capture)!: settle close names and retype tasks landing in created entries | [bob-cli-hd.6](bob-cli-hd.6.md) | 2026-11-05 13:07:49 EST |
