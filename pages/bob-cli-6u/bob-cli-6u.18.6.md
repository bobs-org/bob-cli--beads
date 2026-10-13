# Bead: bob-cli-6u.18.6 — Install the fixed bob and plugins on the MacBook, then this host

[Bead Pages](../README.md) / [bob-cli-6u.18](bob-cli-6u.18.md) / bob-cli-6u.18.6

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.bob-cli-6u.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-6u.land.md) · **Assignee:** `bob-cli-6u.18.6` · **Size:** small
**Created:** 2026-10-12 18:07:07 EDT · **Closed:** 2026-10-12 19:59:58 EDT
**Plan:** [202610/prj\_line\_blocking\_landing\_fixes.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/prj_line_blocking_landing_fixes.md)

## Description

rollout: bob on the MacBook first, then this host, then plugins on both; dry-run verification only; record versions and what Bryan still has to do.

## Notes

[2026-10-12T23:59:51Z · bob-cli-6u.18.6] Rollout results 2026-10-12: THIS HOST DONE — bob-cli b09612e (origin/master tip) `just install` exit 0, `bob --version` 0.1.0; `BOB_DIR=~/bob bob task reconcile --dry-run -f json` exit 0 with zero planned changes (all change-lists empty); `BOB_DIR=~/bob bob projects sync --dry-run` exit 0 ("85 projects - 0 status updated - 0 ^prj edited - 0 task schedules updated - 0 warnings", no hoists, no errors); `bob plugins sync -n -r <bob-plugins@a7fafed>` all 6 up to date, `bob plugins list` 6 synced / 0 drift (block-id-prompt 1.28.0, bob-ledger-tools 1.49.0, bob-navigation-hotkeys 2.25.0, bob-project-tasks 1.0.0, bob-vim-surround 1.5.2, task-status-cycler 1.32.0). MACBOOK NOT DONE — ssh mac timed out on 5 attempts (Tailscale kellys-macbook-pro, port 22); Mac bob NOT updated so Mac plugins deliberately NOT synced. LEFT FOR BRYAN (on MacBook, when reachable): cd ~/projects/github/bobs-org/bob-cli && git pull --ff-only && just install; then BOB_DIR=~/bob bob task reconcile --dry-run -f json and BOB_DIR=~/bob bob projects sync --dry-run (expect exit 0, no errors); only then ssh-side bob plugins sync + bob plugins list; then reload plugins (or restart Obsidian) and pilot: Ctrl+Shift+P b on a ^prj add/remove, Schedule on ^prj, link gesture on a resident of an unblocked project with a future date (should pull forward).

[2026-10-12T23:59:58Z · bob-cli-6u.18.6] Host rollout verified: bob-cli b09612e just install exit 0; reconcile --dry-run -f json exit 0 with zero planned changes; projects sync --dry-run exit 0, 0 hoists, 0 errors; plugins sync all 6 up to date (a7fafed), list 6 synced/0 drift. MacBook unreachable over ssh (5x timeout) so Mac bob+plugins left for Bryan with exact commands recorded in bead note; per plan Mac plugins correctly not synced.

## Dependencies

- **Depends on:** [bob-cli-6u.18.1](bob-cli-6u.18.1.md) ✓ · ⧖ 2026-10-12
- **Depends on:** [bob-cli-6u.18.2](bob-cli-6u.18.2.md) ✓ · ⧖ 2026-10-12
- **Depends on:** [bob-cli-6u.18.3](bob-cli-6u.18.3.md) ✓ · ⧖ 2026-10-12
- **Depends on:** [bob-cli-6u.18.4](bob-cli-6u.18.4.md) ✓ · ⧖ 2026-10-12
- **Depends on:** [bob-cli-6u.18.5](bob-cli-6u.18.5.md) ✓ · ⧖ 2026-10-12

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-6u.18.6](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-6u.18.6/README.md) | [bob-cli-6u.18.6](bob-cli-6u.18.6.md) | 0 |
