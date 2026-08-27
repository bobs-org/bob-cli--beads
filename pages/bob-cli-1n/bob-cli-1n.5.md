# Bead: bob-cli-1n.5 — Provision credentials, triggers, and the MacBook git clone

[Bead Pages](../README.md) / [bob-cli-1n](README.md) / bob-cli-1n.5

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.0ez](https://github.com/bobs-org/bob-cli--agents/blob/main/families/bbugyi200.athena.0ez.md) · **Assignee:** `bob-cli-1n.5` · **Size:** medium
**Created:** 2026-08-27 12:48:58 EDT · **Closed:** 2026-08-27 14:36:19 EDT
**Plan:** [202608/vault\_git\_sync.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202608/vault_git_sync.md)

## Description

machines: create a passphraseless deploy key for athena, add SSH ControlMaster, ship the chezmoi rsync bridge and config, convert the MacBook's `~/bob` into a clone in place, and install the systemd and launchd triggers without enabling them.

## Notes

[2026-08-27T18:36:02Z · bob-cli-1n.5] PROPOSED FOLLOW-UP: Fix MacBook chezmoi Neovim installer prerequisite — broad /opt/homebrew/bin/chezmoi apply currently fails in .chezmoiscripts/install_nvim because cmake is missing; targeted --include files was required for this phase.

[2026-08-27T18:36:19Z · bob-cli-1n.5] Verified athena env-i git access through deploy key, MacBook ~/bob converted to clean clone, both vaults clean at d79917e9, chezmoi bridge/config applied, bob installed with vault-sync and no bulk-git-commit on both machines, triggers installed inactive/not loaded, and _conflicts probe hidden from dash.md/blocked.md.

## Dependencies

- **Depends on:** [bob-cli-1n.1](bob-cli-1n.1.md) ✓ · ⧖ 2026-08-27
- **Depends on:** [bob-cli-1n.3](bob-cli-1n.3.md) ✓ · ⧖ 2026-08-27
- **Depends on:** [bob-cli-1n.4](bob-cli-1n.4.md) ✓ · ⧖ 2026-08-27
- **Blocks:** [bob-cli-1n.6](bob-cli-1n.6.md) ✓ · ⧖ 2026-08-27

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-1n.5](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-1n.5/README.md) | [bob-cli-1n.5](bob-cli-1n.5.md) | 0 |
