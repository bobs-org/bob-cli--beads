# Bead: bob-cli-df.4 — Preserve tracked and untracked edits across a failed-close relaunch reset

[Bead Pages](../README.md) / [bob-cli-df](README.md) / bob-cli-df.4

**Status:** ◐ in_progress · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-dd.land--3](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-dd.land.md) · **Assignee:** `bob-cli-df.4` · **Size:** large
**Created:** 2026-10-27 21:24:44 EDT
**Plan:** [202610/backlog\_batch\_b4.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/backlog_batch_b4.md)

## Description

dirty-tree-preservation: resolve the remaining bob-cli-cv loss in sase by proving and repairing the relaunch reset that still drops tracked edits after sase-1oh reopened failed closes; stash or otherwise preserve the full dirty tree before any hard reset.

## Notes

[2026-10-28T01:37:42Z · bob-cli-df.4] PLANNING: Audited B4 design, bob-cli-cv, closed sase-yo and sase-1oh.4; this phase had no prior work notes. At sase daf54c5b2d, failed-close reopening is landed but reset_replay still aborts before a HEAD-only snapshot, errors lose prior recovery refs, and stash-failure/reclone paths accept best-effort rescue without proof of dirty-content preservation. No source changes or historical reproduction claimed. Authored a four-phase child epic (verified snapshot, reset replay, relaunch cleanup, failed-close evidence) with parent_bead bob-cli-df.4; validated with --explain then revalidated, both pass with zero warnings. Submitting through sase plan propose; child land must verify full tracked/staged/untracked recovery and close df.4 only, leaving cv and df to B4 land.

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-df.4](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-df.4.md) | [bob-cli-df.4](bob-cli-df.4.md) | 0 |
