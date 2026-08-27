# Bead: bob-cli-1e.2 — Evacuate old\_lib and push the deletions to the remote vault

[Bead Pages](../README.md) / [bob-cli-1e](README.md) / bob-cli-1e.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.0en](https://github.com/bobs-org/bob-cli--agents/blob/main/families/bbugyi200.athena.0en.md) · **Assignee:** `bob-cli-1e.2` · **Size:** medium
**Created:** 2026-08-27 08:13:35 EDT · **Closed:** 2026-08-27 08:29:30 EDT
**Plan:** [202608/unsync\_old\_lib.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202608/unsync_old_lib.md)

## Description

evacuate: quiesce the sync service and nightly cron, rename old_lib to a dot-prefixed staging directory so the sync client sees it as absent, canary-test that the server accepts deletes while over quota, then drain all 660 old_lib entries from the remote.

## Notes

[2026-08-27T12:29:30Z · bob-cli-1e.2] Verified canary and full remote drain for old_lib: state DB reports 0 live old_lib entries / 0.0 MB and remote live total 114.5 MB, down from the 965.7 MB baseline. Local /home/bryan/bob/old_lib is absent and /home/bryan/bob/.old_lib_migrating holds all 660 files / 851110473 bytes. ob-sync-bob.service is inactive, no obsidian-headless process is running, and the bob nightly cron line remains commented for phase exclude. Sync delete passes ended with Vault limit exceeded only after old_lib deletions, while attempting later uploads, so the live remote drain is complete.

## Dependencies

- **Depends on:** [bob-cli-1e.1](bob-cli-1e.1.md) ✓ · ⧖ 2026-08-27
- **Blocks:** [bob-cli-1e.3](bob-cli-1e.3.md) ✓ · ⧖ 2026-08-27

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-1e.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-1e.2/README.md) | [bob-cli-1e.2](bob-cli-1e.2.md) | 0 |
