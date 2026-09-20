# Bead: bob-cli-23.2 — Auto-scan from bob\_xlib\_pull and follow the rename in chezmoi

[Bead Pages](../README.md) / [bob-cli-23](README.md) / bob-cli-23.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.16](https://github.com/bobs-org/bob-cli--agents/blob/main/families/bbugyi200.apollo.16.md) · **Assignee:** `bob-cli-23.2` · **Size:** medium
**Created:** 2026-09-20 15:38:36 EDT · **Closed:** 2026-09-20 16:03:07 EDT
**Plan:** [202609/highlights\_pre\_scan\_hook.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202609/highlights_pre_scan_hook.md)

## Description

dotfiles: update the managed bob config and `maybe_bob_highlights_sync` for the new names, make `bob_xlib_pull` run `bob highlights --no-hooks scan -w` after its pull on macOS with hook and cron-lock guards, extend the bashunit regression tests, and refresh the Highlights bridge documentation.

## Notes

[2026-09-20T20:03:07Z · bob-cli-23.2] chezmoi: config.yml key renamed to highlights.pre_scan_hook; maybe_bob_highlights_sync now checks BOB_HIGHLIGHTS_PRE_SCAN_HOOK / pre_scan_hook: (shared lock name commented in both scripts); bob_xlib_pull runs 'bob highlights --no-hooks scan -w' via run_waited after both handle_host calls, skipping silently when BOB_HIGHLIGHTS_IN_PRE_SCAN_HOOK is set or the maybe_bob_highlights_sync.lock dir is held, releasing that lock in cleanup only when it created it, resolving bob like maybe_bob_highlights_sync (PATH then ~/.cargo/bin), and exiting 1 on scan failure or missing bob. bashunit: bob stub + env threading in set_up/run_xlib_pull/start_xlib_pull, 11 new tests (scan-after-transfers, empty queues, unreachable hosts, transfer failure, hook marker, held lock, scan exit 7, non-Darwin, cargo fallback, missing bob, SIGTERM during scan releasing both locks); mutation-checked the marker guard, lock guard and lock release each fail a test. bob_xlib_pull_test.sh 35/35 pass, full 'just test-bash' 213/213 pass, sh -n clean on both scripts (shellcheck/shfmt not installed here). bob-cli docs/vault-git-sync.md Highlights bridge section updated and prettier-clean.

## Dependencies

- **Depends on:** [bob-cli-23.1](bob-cli-23.1.md) ✓ · ⧖ 2026-09-20

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-23.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-23.2/README.md) | [bob-cli-23.2](bob-cli-23.2.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`92042e9`](https://github.com/bobs-org/bob-cli/commit/92042e9c0cd74fa5aac9eab339b4d389b9e90109) | docs(highlights): describe bob\_xlib\_pull auto-scan | [bob-cli-23.2](bob-cli-23.2.md) | 2026-09-20 16:04:07 EDT |
