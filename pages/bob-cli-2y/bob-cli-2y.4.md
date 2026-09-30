# Bead: bob-cli-2y.4 — No bob capture path lowers a lane

[Bead Pages](../README.md) / [bob-cli-2y](README.md) / bob-cli-2y.4

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.3n](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.3n.md) · **Assignee:** `bob-cli-2y.4` · **Size:** medium
**Created:** 2026-09-30 16:42:00 EDT · **Closed:** 2026-09-30 17:29:57 EDT
**Plan:** [202609/retire\_now\_sticky\_lanes.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202609/retire_now_sticky_lanes.md)

## Description

capture-toggle-lanes: make @route+id! a link-presence toggle, keep In Progress under Ensure Next, word dropped rows as 'stays <status>', and fix capture docs that promise hooks demotion.

## Notes

[2026-09-30T21:29:40Z · bob-cli-2y.4] PROPOSED FOLLOW-UP: clippy deny clippy::overly_complex_bool_expr at tests/cli/capture/pomodoro_name.rs:808 fails just lint identically on the clean base tree (verified via stash); fix the bool expr or allow the lint so just all goes green

[2026-09-30T21:29:57Z · bob-cli-2y.4] capture-toggle-lanes done: @route+id! is now a link-presence toggle (link/unlink JSON directions, status_changed, linked/unlinked human lines), Ensure Next keeps In Progress via plan_task_link, plan_task_open deleted, dropped rows read 'stays <status>' in close+start output, cli help/docs/capture.md/README updated. Verified: cargo fmt clean, full cargo test green (1334 lib + 653 cli + integration, 0 failed); clippy deny at pomodoro_name.rs:808 reproduces identically on clean base (recorded as follow-up). No epic-symbol leftovers.

## Dependencies

- **Blocks:** [bob-cli-2y.11](bob-cli-2y.11.md) ◐ · ⧖ 2026-09-30
- **Depends on:** [bob-cli-2y.2](bob-cli-2y.2.md) ✓ · ⧖ 2026-09-30
- **Blocks:** [bob-cli-2y.6](bob-cli-2y.6.md) ◐ · ⧖ 2026-09-30

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-2y.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-2y.4/README.md) | [bob-cli-2y.4](bob-cli-2y.4.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`63305f0`](https://github.com/bobs-org/bob-cli/commit/63305f02b7d437e7830f89d6ba919a43a9a15a6e) | feat(capture): make @route+id! a link-presence toggle that never lowers a lane | [bob-cli-2y.4](bob-cli-2y.4.md) | 2026-09-30 17:31:39 EDT |
