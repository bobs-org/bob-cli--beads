# Bead: bob-cli-46.4 — chezmoi and bob-plugins callers move to canonical names

[Bead Pages](../README.md) / [bob-cli-46](README.md) / bob-cli-46.4

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.4y](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.4y.md) · **Assignee:** `bob-cli-46.4` · **Size:** small
**Created:** 2026-10-04 07:02:06 EDT · **Closed:** 2026-10-04 09:07:49 EDT
**Plan:** [202610/bob\_command\_tree.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/bob_command_tree.md)

## Description

downstream-callers: switch the chezmoi shims, tmux.conf, and obsidian memory note to canonical names, fix the stale highlights-ref message, retire the stale bob_dataview skill copies, update the bob-plugins notice string, and guard the rollout so no host runs new spellings on an old bob.

## Notes

[2026-10-04T13:07:45Z · bob-cli-46.4] PROPOSED FOLLOW-UP: Corroborate bob-cli-3w: the stage-ranker 16 ms assertion failed twice in full npm test runs under suite load (19.75 ms and 29.20 ms), while its isolated run passed; phase edits are non-runtime caller/comment changes.

[2026-10-04T13:07:49Z · bob-cli-46.4] Updated chezmoi shims, tmux, Obsidian sync note, Highlights error text, and exact stale-skill removal list; updated plugin caller comments and notice to bob task reconcile and bumped its patch version. The grouped-command rollout guard and shim help checks passed; chezmoi dry run showed only expected caller edits, eight extant stale skill removals, and tmux reload. npm run build and npm run validate passed; npm test had one timing-sensitive stage-ranker failure in two full-suite runs, isolated rerun passed, tracked by bob-cli-3w. bob plugins sync deployed the linked checkout, and epic-symbol check found none.

## Dependencies

- **Depends on:** [bob-cli-46.2](bob-cli-46.2.md) ✓ · ⧖ 2026-10-04

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-46.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-46.4/README.md) | [bob-cli-46.4](bob-cli-46.4.md) | 0 |
