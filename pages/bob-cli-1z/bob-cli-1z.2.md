# Bead: bob-cli-1z.2 — Pure toggle planners for the route note and the daily ledger

[Bead Pages](../README.md) / [bob-cli-1z](README.md) / bob-cli-1z.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.0ir](https://github.com/bobs-org/bob-cli--agents/blob/main/families/bbugyi200.athena.0ir.md) · **Assignee:** `bob-cli-1z.2` · **Size:** medium
**Created:** 2026-09-10 13:19:08 EDT · **Closed:** 2026-09-10 14:46:31 EDT
**Plan:** [202609/capture\_task\_toggle.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202609/capture_task_toggle.md)

## Description

engine: add a new native module of pure, unit-tested planners that compute the route-note task mutation (status, future-schedule pull-forward, Schedule Log entry) and the daily-note Pomodoro task-link insertion, cleanup, and removal.

## Notes

[2026-09-10T18:46:31Z · bob-cli-1z.2] Added src/native/capture_task_toggle.rs: pure planners plan_task_next/plan_task_open (status transition, future-scheduled-field pull-forward with the underscore-emphasis Schedule Log formatter distinct from capture_schedule_log's asterisk form) and plan_link_insertion/plan_link_removal (Pomodoro task-link idempotent insertion with future-duplicate cleanup, and all-open-Pomodoro removal with whole-subtree-vs-token-only bullet handling), plus 27 unit tests covering every case in the phase checklist (no/one/two/past scheduled fields, with/without an existing Schedule Log, indentation reuse and fallback, already-linked idempotence, later-open-entry duplicate cleanup, completed-Pomodoro links left untouched, sole-content vs shared-bullet removal, and CRLF preservation). Registered the new module in src/native.rs (mod declaration only, no CLI wiring). Verified with `just all` (cargo fmt --check, cargo clippy --all-targets --all-features, cargo test): all checks pass, 0 warnings in the new file, 27/27 new tests plus the full existing suite (491 tests total) green. No epic-symbol entries for this phase (sase bead epic-symbols bob-cli-1z.2 confirmed clean). Not wired into bob capture — that is the capture phase's job per the plan.

## Dependencies

- **Blocks:** [bob-cli-1z.3](bob-cli-1z.3.md) ✓ · ⧖ 2026-09-10

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-1z.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-1z.2/README.md) | [bob-cli-1z.2](bob-cli-1z.2.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`ce9d984`](https://github.com/bobs-org/bob-cli/commit/ce9d98419a797eb5d03cfaa293667352b1ac6e70) | feat(capture-task-toggle): add pure route-note and Pomodoro-ledger toggle planners | [bob-cli-1z.2](bob-cli-1z.2.md) | 2026-09-10 14:47:02 EDT |
