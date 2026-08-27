# Bead: bob-cli-1n.3 — Retire \`bulk-git-commit\` and rewire \`bob nightly\`

[Bead Pages](../README.md) / [bob-cli-1n](README.md) / bob-cli-1n.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.0ez](https://github.com/bobs-org/bob-cli--agents/blob/main/families/bbugyi200.athena.0ez.md) · **Assignee:** `bob-cli-1n.3` · **Size:** small
**Created:** 2026-08-27 12:48:58 EDT · **Closed:** 2026-08-27 13:30:59 EDT
**Plan:** [202608/vault\_git\_sync.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202608/vault_git_sync.md)

## Description

retire: delete the `bulk-git-commit` subcommand and its `bob_sync` script and binary aliases, drop the `ob sync` gate from `bob nightly`, and make nightly run vault-sync, move-done-tasks, vault-sync.

## Notes

[2026-08-27T17:30:59Z · bob-cli-1n.3] Retired bob bulk-git-commit and bob_sync from the CLI, embedded assets, install smoke, tests, and docs; rewired bob nightly to run vault-sync, move-done-tasks, vault-sync under the shared lock; verified no phase epic-symbols remain, cargo check passes, targeted nightly/vault-sync/help CLI tests pass, just all passes, and bob nightly --help no longer mentions ob sync or Obsidian sync.

## Dependencies

- **Depends on:** [bob-cli-1n.2](bob-cli-1n.2.md) ✓ · ⧖ 2026-08-27
- **Blocks:** [bob-cli-1n.5](bob-cli-1n.5.md) ◐ · ⧖ 2026-08-27

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-1n.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-1n.3/README.md) | [bob-cli-1n.3](bob-cli-1n.3.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`4051bf5`](https://github.com/bobs-org/bob-cli/commit/4051bf520dc308eef50721187ae042952fab3d8e) | feat(cli): retire bulk git commit | [bob-cli-1n.3](bob-cli-1n.3.md) | 2026-08-27 13:31:35 EDT |
