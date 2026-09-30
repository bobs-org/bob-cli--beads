# Bead: bob-cli-2y.12 — Install, deploy, end-to-end check, and Bryan's checklist

[Bead Pages](../README.md) / [bob-cli-2y](README.md) / bob-cli-2y.12

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.3n](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.3n.md) · **Assignee:** `bob-cli-2y.12` · **Size:** small
**Created:** 2026-09-30 16:42:00 EDT · **Closed:** 2026-09-30 18:57:10 EDT
**Plan:** [202609/retire\_now\_sticky\_lanes.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202609/retire_now_sticky_lanes.md)

## Description

rollout: install bob on apollo, sync every plugin, finish any Mac step hooks-resume could not, run the end-to-end checks, finalize the Surfaces table, and hand Bryan the triage and trial checklist.

## Notes

[2026-09-30T22:56:53Z · bob-cli-2y.12] PROPOSED FOLLOW-UP: cargo clippy --all-targets denies tests/cli/capture/pomodoro_shift.rs:581 (unnecessary_to_owned) so just lint fails on the committed tree; cargo test passes. Needs a task bead for the clippy fix.

[2026-09-30T22:57:10Z · bob-cli-2y.12] Rollout done. Installed bob from master on apollo (cargo install --locked --force) and on the Mac (git pull to 473cca3 + cargo install); plugins pulled to origin/master and synced (ledger/block-id/nav-hotkeys up to date); Mac cron line active and Mac dry-run shows cleared=[] cleared_in_progress=[]. E2E: bob plan schema v2 (TODAY 5, NEXT 26/15, PENDING 52/10); hooks dry-run clears nothing; trailing #now gives the ordinary trailing-tag error identical to #foo; @sase+memory-file-versions! dry-run gives unlink/status_changed=false; dash 4 blocks parse error=null with TODAY empty headless; rg leaves only intentional retired-text/compat hits; cargo test passes; Surfaces table finalized; vault-sync pushed clean. Known pre-existing: just lint fails on pomodoro_shift.rs:581 clippy (recorded as follow-up).

## Dependencies

- **Depends on:** [bob-cli-2y.10](bob-cli-2y.10.md) ✓ · ⧖ 2026-09-30
- **Depends on:** [bob-cli-2y.11](bob-cli-2y.11.md) ✓ · ⧖ 2026-09-30
- **Depends on:** [bob-cli-2y.3](bob-cli-2y.3.md) ✓ · ⧖ 2026-09-30
- **Depends on:** [bob-cli-2y.6](bob-cli-2y.6.md) ✓ · ⧖ 2026-09-30

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-2y.12](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-2y.12/README.md) | [bob-cli-2y.12](bob-cli-2y.12.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`297ecb4`](https://github.com/bobs-org/bob-cli/commit/297ecb474445479390dba26e75eb7c52164d9441) | docs(plan): finalize Surfaces table for retired-#now rollout (bob-cli-2y.12) | [bob-cli-2y.12](bob-cli-2y.12.md) | 2026-09-30 18:59:06 EDT |
