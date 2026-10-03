# Bead: bob-cli-3u.3 — Apply dependency captures with staged multi-note writes

[Bead Pages](../README.md) / [bob-cli-3u](README.md) / bob-cli-3u.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.4m](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.4m.md) · **Assignee:** `bob-cli-3u.3` · **Size:** medium
**Created:** 2026-10-03 09:11:57 EDT · **Closed:** 2026-10-03 11:21:16 EDT
**Plan:** [202610/capture\_task\_dependencies.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/capture_task_dependencies.md)

## Description

dependency-writes: merge managed dependency lines and derived effects through the capture batch planner with validation, rollback, and final task previews.

## Notes

[2026-10-03T15:21:04Z · bob-cli-3u.3] PROPOSED FOLLOW-UP: Pre-existing clippy deny-by-default error in tests/cli/capture/pomodoro_name.rs:808 (`|| true` makes the boolean expression vacuous, clippy::logic_bug) reproduces identically on the clean base tree via `cargo clippy --all-targets --all-features`; makes `just lint` red independent of bob-cli-3u.3 — triage into a task bead.

[2026-10-03T15:21:16Z · bob-cli-3u.3] Staged dependency writer verified: new-task and dependency-only captures merge managed DEPENDS ON lines + derived dependsOn fields with Blocked/freshness effects; repeats idempotent (0 added), appends tally only new links; missing-note/missing-target/self-dep/ownerless failures leave vault intact; dry-run plans without writing. Full cargo test green (lib 1578 + cli 902, 0 failures), fmt clean; retired fail-closed test rewritten to writer behavior, docs/capture.md + capture-parse help updated. Pre-existing clippy logic_bug in pomodoro_name.rs:808 filed as follow-up (reproduces on clean tree).

## Dependencies

- **Depends on:** [bob-cli-3u.1](bob-cli-3u.1.md) ✓ · ⧖ 2026-10-03
- **Depends on:** [bob-cli-3u.2](bob-cli-3u.2.md) ✓ · ⧖ 2026-10-03
- **Blocks:** [bob-cli-3u.4](bob-cli-3u.4.md) ✓ · ⧖ 2026-10-03
- **Blocks:** [bob-cli-3u.5](bob-cli-3u.5.md) ✓ · ⧖ 2026-10-03

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-3u.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-3u.3/README.md) | [bob-cli-3u.3](bob-cli-3u.3.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`6718111`](https://github.com/bobs-org/bob-cli/commit/67181114af85467c1e4d3ecaa3ee98484d5d39c4) | feat(capture): implement staged capture writer with dependency parsing | [bob-cli-3u.3](bob-cli-3u.3.md) | 2026-10-03 11:22:40 EDT |
