# Bead: bob-cli-74.6 — Install, verify on a vault copy, reach the MacBook, and record

[Bead Pages](../README.md) / [bob-cli-74](README.md) / bob-cli-74.6

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.73](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.73.md) · **Assignee:** `bob-cli-74.6` · **Size:** small
**Created:** 2026-10-12 23:40:12 EDT · **Closed:** 2026-10-13 01:51:27 EDT
**Plan:** [202610/project\_pull\_in\_line\_model.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/project_pull_in_line_model.md)

## Description

rollout: install bob and sync plugins on this host, verify a pull-in on a temporary vault copy (including sync agreement), install bob and then plugins on the MacBook best-effort, close bob-cli-6x, and record versions and Bryan's pilot steps.

## Notes

[2026-10-13T05:51:06Z · bob-cli-74.6] PROPOSED FOLLOW-UP: skipped decisions-web record project-pull-in-on-empty — epic decision_record=no, so rollout did not edit memory

[2026-10-13T05:51:11Z · bob-cli-74.6] PROPOSED FOLLOW-UP: distinct Bob Mac Capture copy for trigger: project_empty

[2026-10-13T05:51:15Z · bob-cli-74.6] PROPOSED FOLLOW-UP: ledger-tools 🔓 glyph on pulled-in links

[2026-10-13T05:51:20Z · bob-cli-74.6] Rollout on apollo (2026-10-13).
bob-cli installed from master 309e98a92ed290f3893b4fcf4c9e58bb857d94b4 (`just install`, never --force); bob 0.1.0 at ~/.cargo/bin/bob; zsh completion unchanged.
BOB_DIR=~/bob bob task reconcile --dry-run -f json exits 1 because 2026/20261013.md does not exist yet (same as 6u.18.7.6.4). With BOB_NOW='2026-10-12 21:00:00' it exits 0 against 2026/20261012.md: ok, no planned edits (applied_files empty). BOB_DIR=~/bob bob projects sync --dry-run exits 0: 85 projects, 0 status updated, 0 ^prj edited, 0 task schedules updated, 0 warnings.
Opened bob-plugins at 9e0537911d8eaf7c8f7f262b28b552f101c6cb31; `bob plugins sync -n -r <opened checkout>` 0 copied, 16 unchanged. `bob plugins list -n -r <opened>`: block-id-prompt 1.29.0, bob-ledger-tools 1.49.0, bob-navigation-hotkeys 2.28.0, bob-project-tasks 1.0.0, bob-vim-surround 1.5.2, task-status-cycler 1.35.0; all synced and enabled.
Copy verification: rsync of ~/bob to /tmp/bob-cli-74.6-vault (excluded .git/.trash). Created 2026/20261013.md in the copy with open Pomodoro PULLIN linking [[sase_agent_history#^e2e-test]] (wip project, one open unhidden task, ^prj #hide). Dry-run and live `bob capture -f json -- '!sase_agent_history:e2e-test'`: unblocked_check=checked, trigger=project_empty, hide_removed=true, link [[sase_agent_history#^prj]], status [ ]→[*], #hide stripped. Then `bob projects sync --dry-run` on the copy: 85 projects, 0 edits, no event line naming sase_agent_history. Copy deleted. Live ~/bob sase_agent_history.md and absence of 2026/20261013.md unchanged.
MacBook: Tailscale kellys-macbook-pro offline (last seen ~30m before retries started). ssh -o ConnectTimeout=20 -o BatchMode=yes mac failed 23 times over 30 minutes (kellys-macbook-pro.tail297af1.ts.net:22 Connection timed out). Could not read /tmp/bob-rollout-install*.log. No Mac bob install and no Mac plugin sync (bob must verify first).
Left for Bryan: when the Mac is reachable, `cd ~/projects/github/bobs-org/bob-cli && git pull --ff-only && just install`, then dry-run reconcile and projects sync there; only then `bob plugins sync` and `bob plugins list`. Reload plugins or restart Obsidian on the Mac, then pilot Ctrl+Enter on a project's last task link (^prj linked, [*], no #hide), a same-day reopen restoring it, and `bob capture '!note:id'` on a last task.
epic-symbols: no --epic-symbol entries for bob-cli-74.6.

[2026-10-13T05:51:27Z · bob-cli-74.6] Installed bob 309e98a and synced plugins on apollo (nav 2.28.0, cycler 1.35.0). Verified live pull-in on a ~/bob copy of sase_agent_history (trigger=project_empty, hide_removed=true, [[#^prj]] linked); copy sync --dry-run named no event for that project; live vault untouched. Closed bob-cli-6x. MacBook SSH timed out 23 times over 30 minutes (Tailscale offline); no Mac install or plugin sync. Skipped project-pull-in-on-empty memory record (decision_record=no).

## Dependencies

- **Depends on:** [bob-cli-74.3](bob-cli-74.3.md) ✓ · ⧖ 2026-10-12
- **Depends on:** [bob-cli-74.4](bob-cli-74.4.md) ✓ · ⧖ 2026-10-12
- **Depends on:** [bob-cli-74.5](bob-cli-74.5.md) ✓ · ⧖ 2026-10-12

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-74.6](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-74.6/README.md) | [bob-cli-74.6](bob-cli-74.6.md) | 0 |
