# Bead: bob-cli-1n.1 — Converge both vaults and fix what the first \`git add -A\` would sweep in

[Bead Pages](../README.md) / [bob-cli-1n](README.md) / bob-cli-1n.1

**Status:** ◐ in_progress · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.0ez](https://github.com/bobs-org/bob-cli--agents/blob/main/families/bbugyi200.athena.0ez.md) · **Assignee:** `bob-cli-1n.1` · **Size:** medium
**Created:** 2026-08-27 12:48:58 EDT
**Plan:** [202608/vault\_git\_sync.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202608/vault_git_sync.md)

## Description

reconcile: back up both vaults, close the five remaining athena/MacBook differences, gitignore `lit_review/` and `xlib/`, add `.gitattributes`, run `git gc`, and land the 206-path commit backlog so both machines start from one known SHA.

## Notes

[2026-08-27T16:56:56Z · bob-cli-1n.1] Backups: athena vault /home/bryan/var/backups/bob-pre-gitsync-athena-20260827T125528; MacBook vault /Users/bbugyi/var/backups/bob-pre-gitsync-macbook-20260827T125528; athena quiesce crontab copy /home/bryan/var/backups/bob-pre-gitsync-metadata-20260827/athena-crontab-pre-quiesce-20260827T142313Z.txt; MacBook crontab backup /Users/bbugyi/var/backups/macbook-crontab-pre-gitsync-20260827T125407.txt. MacBook crontab writes failed with Operation not permitted over SSH, so temporary wrappers were installed under /Users/bbugyi/var/backups/bob-cli-1n1-mac-cron-guard-20260827T125513 and will be restored before close.

## Dependencies

- **Blocks:** [bob-cli-1n.5](bob-cli-1n.5.md) ◐ · ⧖ 2026-08-27

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-1n.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-1n.1/README.md) | [bob-cli-1n.1](bob-cli-1n.1.md) | 0 |
