# Bead: bob-cli-6u.18.7.6.4 — Install the fixed bob and plugins on this host and the MacBook

[Bead Pages](../README.md) / [bob-cli-6u.18.7.6](bob-cli-6u.18.7.6.md) / bob-cli-6u.18.7.6.4

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.bob-cli-6u.18.7.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-6u.18.7.land.md) · **Assignee:** `bob-cli-6u.18.7.6.4` · **Size:** small
**Created:** 2026-10-12 22:09:27 EDT · **Closed:** 2026-10-12 22:45:57 EDT
**Plan:** [202610/prj\_line\_blocking\_final\_audit\_fixes.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/prj_line_blocking_final_audit_fixes.md)

## Description

rollout: bob then plugins on this host, then best-effort on the MacBook with a detached install; dry-run verification only; record versions and what Bryan still has to do.

## Notes

[2026-10-13T02:45:48Z · bob-cli-6u.18.7.6.4] Rollout verified on apollo: installed bob from bob-cli commit 2fcf41a with `just install` (bob 0.1.0); completion stayed registered. `BOB_DIR=~/bob BOB_NOW=2026-10-12 bob task reconcile --dry-run -f json` exited 0 with no warnings or planned edits (the 2026-10-13 daily note does not exist; 2026-10-12 is the latest daily note). `BOB_DIR=~/bob bob projects sync --dry-run` exited 0: 85 projects, 0 status updates, 0 ^prj edits, 0 task schedule updates, 0 warnings. Opened bob-plugins checkout was current at 5d8975b; `bob plugins sync -n -r <opened checkout>` preview exited 0 with 0 copied, 0 skipped, 16 unchanged. `bob plugins list` reports six synced/enabled plugins: block-id-prompt 1.29.0, bob-ledger-tools 1.49.0, bob-navigation-hotkeys 2.27.0, bob-project-tasks 1.0.0, bob-vim-surround 1.5.2, task-status-cycler 1.34.0. MacBook is offline in Tailscale and SSH timed out on three attempts; prior rollout logs and its installed versions could not be read, no Mac install or plugin sync was run. Remaining for Bryan: retry Mac install and dry-run verification when reachable, sync plugins only after bob verifies, record its commit/plugin versions, reload plugins or restart Obsidian, then pilot Ctrl+Shift+P b add/remove on ^prj; Schedule and Ctrl+D; Ctrl+Shift+M into a project whose ^prj depends on another project’s blocked ^prj; Alt+] on a blocked ^prj whose remaining dependency is closed.

[2026-10-13T02:45:57Z · bob-cli-6u.18.7.6.4] Installed bob from 2fcf41a; host reconcile and project sync dry runs passed with no planned changes or warnings, and plugin sync preview found all files unchanged. Recorded host plugin versions and the unreachable MacBook follow-up; epic-symbol audit found no entries.

## Dependencies

- **Depends on:** [bob-cli-6u.18.7.6.1](bob-cli-6u.18.7.6.1.md) ✓ · ⧖ 2026-10-12
- **Depends on:** [bob-cli-6u.18.7.6.2](bob-cli-6u.18.7.6.2.md) ✓ · ⧖ 2026-10-12
- **Depends on:** [bob-cli-6u.18.7.6.3](bob-cli-6u.18.7.6.3.md) ✓ · ⧖ 2026-10-12

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-6u.18.7.6.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-6u.18.7.6.4/README.md) | [bob-cli-6u.18.7.6.4](bob-cli-6u.18.7.6.4.md) | 0 |
