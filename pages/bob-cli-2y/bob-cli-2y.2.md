# Bead: bob-cli-2y.2 — Sticky lanes in bob task-status-hooks, docs, and superseding decision records

[Bead Pages](../README.md) / [bob-cli-2y](README.md) / bob-cli-2y.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.3n](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.3n.md) · **Assignee:** `bob-cli-2y.2` · **Size:** medium
**Created:** 2026-09-30 16:41:59 EDT · **Closed:** 2026-09-30 17:08:32 EDT
**Plan:** [202609/retire\_now\_sticky\_lanes.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202609/retire_now_sticky_lanes.md)

## Description

hooks-sticky: stop the hooks lowering Next and In Progress when links disappear (daily-note tasks keep clearing), verify with a simulated next-day dry run, update the hooks docs, and write the two superseding decision records.

## Notes

[2026-09-30T21:08:15Z · bob-cli-2y.2] PROPOSED FOLLOW-UP: clippy deny-error clippy::overly_complex_bool_expr at tests/cli/capture/pomodoro_name.rs:808 (|| true) fails just lint on the clean base tree (verified identical in HEAD 65f5b43); fails cargo clippy --all-targets independently of hooks-sticky

[2026-09-30T21:08:32Z · bob-cli-2y.2] hooks-sticky done: Next/In Progress sticky outside daily notes (task_transition takes is_daily_note; sticky stays do not count as kept_next); In Progress rollback removed (Transition::ClearInProgress gone, cleared_in_progress always []); daily-note [*] still clears without grace, KeptNext when directly recent. Verified: full cargo test green (2125 passed, 0 failed); fmt clean; unit test sticky_lanes_keep_next_and_in_progress_outside_daily_notes added; CLI expectations updated to stays. Simulated next-day dry run on ~/bob: installed bob cleared 25 / cleared_in_progress 48, new build cleared 0 / [] with identical marked_next 0, marked_blocked 0, unblocked 24. Scratch-vault demo: old cleared ordinary-next + area-work, new clears only daily-stale with cleared_in_progress []. Docs task-status-hooks.md + README updated; new decisions task-lanes-are-sticky + today-is-read-from-the-ledger, now-tag-is-user-owned superseded, task-status-is-derived superseded-in-part; sase memory init --check clean. Pre-existing clippy deny-error in untouched capture/pomodoro_name.rs:808 recorded as follow-up; epic-symbols none.

## Dependencies

- **Blocks:** [bob-cli-2y.3](bob-cli-2y.3.md) ✓ · ⧖ 2026-09-30
- **Blocks:** [bob-cli-2y.4](bob-cli-2y.4.md) ✓ · ⧖ 2026-09-30
- **Blocks:** [bob-cli-2y.5](bob-cli-2y.5.md) ✓ · ⧖ 2026-09-30
- **Blocks:** [bob-cli-2y.8](bob-cli-2y.8.md) ✓ · ⧖ 2026-09-30

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-2y.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-2y.2/README.md) | [bob-cli-2y.2](bob-cli-2y.2.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`33d5622`](https://github.com/bobs-org/bob-cli/commit/33d5622a466b72a0254f7b7866b3ebd6243fa11a) | feat(hooks): make Next/In-Progress lanes sticky outside daily notes | [bob-cli-2y.2](bob-cli-2y.2.md) | 2026-09-30 17:11:06 EDT |
