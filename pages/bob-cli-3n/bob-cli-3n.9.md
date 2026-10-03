# Bead: bob-cli-3n.9 — Install bob and sync plugins on every machine

[Bead Pages](../README.md) / [bob-cli-3n](README.md) / bob-cli-3n.9

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.0vl](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.0vl.md) · **Assignee:** `bob-cli-3n.9` · **Size:** small
**Created:** 2026-10-02 16:54:37 EDT · **Closed:** 2026-10-02 22:03:08 EDT
**Plan:** [202610/task\_dep\_links.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/task_dep_links.md)

## Description

fleet-rollout: install bob from master and sync the four plugins on this host, then on the MacBook (best effort), and record each machine's bob commit, hooks capability, and plugin versions.

## Notes

[2026-10-03T02:02:48Z · bob-cli-3n.9] fleet-rollout record (2026-10-02/03 UTC): athena (this host): bob @ 043d9c5 (cargo install --path . --locked --force from master, up-to-date), hooks capability TRUE (dry-run JSON has dependency_projection_updates; legacy_dependency_children=14, warnings=0), plugins all synced 0 drift (block-id-prompt 1.18.0, bob-ledger-tools 1.18.0, bob-navigation-hotkeys 1.55.0, bob-project-tasks 1.0.0, bob-vim-surround 1.5.2, task-status-cycler 1.20.0). apollo: bob @ 043d9c5 (checkout was 69 behind at 8f2a02e; pulled --ff-only, cargo installed), hooks capability TRUE (verified against temp BOB_DIR with minimal daily note), plugins pulled to 82aec34 and synced (10 copied; same versions as athena, 0 drift). MacBook: UNREACHABLE (ssh mac tailscale timeout, retried ~10 min x8 attempts) - bob commit, hooks capability, and plugin versions all UNVERIFIED. LEFT FOR BRYAN: (1) bring MacBook online, then from its bob-cli checkout (path install if path+file master, reinstall if git+ install) cargo install --locked --force, pull its bob-plugins checkout and bob plugins sync, verify with ssh mac bob task-status-hooks --dry-run -f json has dependency_projection_updates; (2) reload plugins in each running Obsidian (athena, apollo, Mac); (3) vault-migrate preflight must re-verify Mac capability before migrating.

[2026-10-03T02:03:08Z · bob-cli-3n.9] athena: bob@043d9c5 installed, hooks capability true, 6 plugins synced 0 drift. apollo: pulled 69 commits to 043d9c5, installed, capability true, plugins synced. MacBook unreachable after ~10min retries - left for Bryan with exact steps in bead notes. No epic-symbol leftovers. No repo files changed.

## Dependencies

- **Blocks:** [bob-cli-3n.10](bob-cli-3n.10.md) ✓ · ⧖ 2026-10-02
- **Depends on:** [bob-cli-3n.3](bob-cli-3n.3.md) ✓ · ⧖ 2026-10-02
- **Depends on:** [bob-cli-3n.4](bob-cli-3n.4.md) ✓ · ⧖ 2026-10-02
- **Depends on:** [bob-cli-3n.5](bob-cli-3n.5.md) ✓ · ⧖ 2026-10-02
- **Depends on:** [bob-cli-3n.7](bob-cli-3n.7.md) ✓ · ⧖ 2026-10-02
- **Depends on:** [bob-cli-3n.8](bob-cli-3n.8.md) ✓ · ⧖ 2026-10-02

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-3n.9](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-3n.9/README.md) | [bob-cli-3n.9](bob-cli-3n.9.md) | 0 |
