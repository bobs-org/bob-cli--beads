# Bead: bob-cli-3n.12.9.5 — Reinstall bob and resync plugins across the fleet with the landing fixes

[Bead Pages](../README.md) / [bob-cli-3n.12.9](bob-cli-3n.12.9.md) / bob-cli-3n.12.9.5

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-3n.12.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-3n.12.land.md) · **Assignee:** `bob-cli-3n.12.9.5` · **Size:** small
**Created:** 2026-10-03 01:27:48 EDT · **Closed:** 2026-10-03 02:33:28 EDT
**Plan:** [202610/task\_dep\_links\_landing\_fixes.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/task_dep_links_landing_fixes.md)

## Description

rollout: reinstall bob from master and sync the plugins on athena and apollo, update the MacBook best effort, dry-run the hooks against the real vault and explain every dependency count, and record versions and what is left for Bryan.

## Notes

[2026-10-03T06:33:21Z · bob-cli-3n.12.9.5--1] Rollout results (2026-10-03, bob-cli @72964be on athena+apollo):
- athena: bob reinstall from workspace checkout @72964be (fix(hooks) 3n.12.9.4 closeout); bob 0.1.0; hooks capability verified (task-status-hooks --dry-run runs against real vault). plugins @2bd875d, all 6 synced, 0 drift: block-id-prompt 1.20.0, bob-ledger-tools 1.21.0, bob-navigation-hotkeys 1.61.0, bob-project-tasks 1.0.0, bob-vim-surround 1.5.2, task-status-cycler 1.22.0.
- apollo: pulled to 72964be (was 79e39af), cargo install ok, bob 0.1.0; plugins @2bd875d, 8 copied/8 unchanged (task-status-cycler main.js refresh), 6 synced 0 drift, same versions as athena.
- mac: UNREACHABLE, best effort exhausted (5 ssh attempts to kellys-macbook-pro.tail297af1.ts.net, all connection timeout, 120s sleeps). LEFTOVER FOR BRYAN: pull bob-cli, cargo install bob, and resync plugins on the MacBook when it is back online.
- real-vault dry-run (athena): exit=1, ok=false, zero dependency counts because it failed before projection: "daily note does not exist: /home/bryan/bob/2026/20261003.md". No dependency counts to explain; rerun after 20261003.md daily note exists. Full log: sase monitor show xb4k5pw78t68 --all-lines; dry-run JSON: /tmp/rollout-dryrun-athena.json.

[2026-10-03T06:33:28Z · bob-cli-3n.12.9.5--1] athena+apollo on bob-cli 72964be/bob 0.1.0, 6 plugins synced 0 drift; mac unreachable after 5 tries (leftover for Bryan); hooks dry-run verified runnable, real-vault run blocked only by missing 20261003.md daily note (zero counts, nothing to explain)

## Dependencies

- **Depends on:** [bob-cli-3n.12.9.1](bob-cli-3n.12.9.1.md) ✓ · ⧖ 2026-10-03
- **Depends on:** [bob-cli-3n.12.9.2](bob-cli-3n.12.9.2.md) ✓ · ⧖ 2026-10-03
- **Depends on:** [bob-cli-3n.12.9.3](bob-cli-3n.12.9.3.md) ✓ · ⧖ 2026-10-03
- **Depends on:** [bob-cli-3n.12.9.4](bob-cli-3n.12.9.4.md) ✓ · ⧖ 2026-10-03

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-3n.12.9.5](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-3n.12.9.5.md) | [bob-cli-3n.12.9.5](bob-cli-3n.12.9.5.md) | 0 |
