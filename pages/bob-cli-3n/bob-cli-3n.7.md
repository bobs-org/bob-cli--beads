# Bead: bob-cli-3n.7 — Vault-wide Ctrl+Shift+P Depends on stage

[Bead Pages](../README.md) / [bob-cli-3n](README.md) / bob-cli-3n.7

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.0vl](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.0vl.md) · **Assignee:** `bob-cli-3n.7` · **Size:** medium
**Created:** 2026-10-02 16:54:36 EDT · **Closed:** 2026-10-02 20:56:29 EDT
**Plan:** [202610/task\_dep\_links.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/task_dep_links.md)

## Description

nav-stage: add the vault-wide candidate pool from the Tasks cache and open buffers, a port of the capture ranker, the CURRENT/RESULTS/BLOCKED layout, guards (self, cycle, unencodable, stale), the + id flow, every entry point including Task Link mode and the line itself, the summary pill, and notices.

## Notes

[2026-10-03T00:56:17Z · bob-cli-3n.7] PROPOSED FOLLOW-UP: Same-note marked-batch +id never pre-writes confirmed ^ids, so planDependencyEdit fails target-not-found and the batch refuses; nav-stage vault batches pre-write via prepareDependencyTargetNote, same-note executeDependencyBatch does not

[2026-10-03T00:56:29Z · bob-cli-3n.7] Vault-wide Depends on stage in bob-navigation-hotkeys 1.54.0: Tasks-cache pool with open-buffer overrides plus one-time scan fallback, capture-ranker port (DK1-DK8 pinned), CURRENT/RESULTS/BLOCKED layout with 60-row cap, self/cycle/unencodable/stale guards, target-note +id flow, all entry points (task line, Depends-On line skip, Task Link row, counted, chip api, edit-task-dependencies palette), ⛓ pill, §6.7 notices. Verified: 1278/1278 npm tests incl. 16 new stage tests, validate 6/6, deployed via bob plugins sync.

## Dependencies

- **Depends on:** [bob-cli-3n.6](bob-cli-3n.6.md) ✓ · ⧖ 2026-10-02
- **Blocks:** [bob-cli-3n.8](bob-cli-3n.8.md) ✓ · ⧖ 2026-10-02
- **Blocks:** [bob-cli-3n.9](bob-cli-3n.9.md) ◐ · ⧖ 2026-10-02

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-3n.7](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-3n.7/README.md) | [bob-cli-3n.7](bob-cli-3n.7.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@08d1560`](https://github.com/bobs-org/bob-plugins/commit/08d15603d22aa11fc2df3f916bd71de4c461baf8) | feat(nav): vault-wide Ctrl+Shift+P Depends on stage (1.54.0) | [bob-cli-3n.7](bob-cli-3n.7.md) | 2026-10-02 20:57:49 EDT |
