# Bead: bob-cli-1e.5 — Document the exclusion and file the discovered follow-ups

[Bead Pages](../README.md) / [bob-cli-1e](README.md) / bob-cli-1e.5

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.0en](https://github.com/bobs-org/bob-cli--agents/blob/main/families/bbugyi200.athena.0en.md) · **Assignee:** `bob-cli-1e.5` · **Size:** small
**Created:** 2026-08-27 08:13:36 EDT · **Closed:** 2026-08-27 08:42:01 EDT
**Plan:** [202608/unsync\_old\_lib.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202608/unsync_old_lib.md)

## Description

document: record old_lib and its sync exclusion in the bob-cli README vault layout, add a runbook for the procedure, and file task beads for the unbounded sync log and the sase memory note that omits the sync topology.

## Notes

[2026-08-27T12:41:03Z · bob-cli-1e.5] PROPOSED FOLLOW-UP: Add rotation for obsidian-headless sync.log - ~/.config/obsidian-headless/sync/<vault-id>/sync.log is append-only, was measured at 982 MB, and ob-sync-bob-poll writes to it every 30 seconds.

[2026-08-27T12:41:14Z · bob-cli-1e.5] PROPOSED FOLLOW-UP: Audit untracked remote-only vault files - 82 files totaling 23.6 MB, mostly under _meta/migration/ and xmind/, are on Obsidian Sync but not tracked in the vault Git repo, leaving Sync as their only off-machine copy.

[2026-08-27T12:41:24Z · bob-cli-1e.5] PROPOSED FOLLOW-UP: Update SASE Obsidian memory with sync topology - sase/memory/obsidian.md should document ob-sync-bob.service, the ob-sync-bob-poll loop, device-local exclusions, and the 1 GB Obsidian Sync Standard ceiling after explicit memory-edit approval.

[2026-08-27T12:42:01Z · bob-cli-1e.5] Verified README old_lib vault-layout row, docs/obsidian-sync-exclusions.md runbook and docs indexes, three PROPOSED FOLLOW-UP notes, cargo fmt --check, cargo package --list --allow-dirty includes the new doc, and sase bead epic-symbols bob-cli-1e.5 reports no entries.

## Dependencies

- **Depends on:** [bob-cli-1e.3](bob-cli-1e.3.md) ✓ · ⧖ 2026-08-27

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-1e.5](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-1e.5/README.md) | [bob-cli-1e.5](bob-cli-1e.5.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`9f9049b`](https://github.com/bobs-org/bob-cli/commit/9f9049bad22546e8d949c240ba1c2820842b9b1c) | docs: document obsidian sync exclusions | [bob-cli-1e.5](bob-cli-1e.5.md) | 2026-08-27 08:42:46 EDT |
