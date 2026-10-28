# Bead: bob-cli-df.4 — Preserve tracked and untracked edits across a failed-close relaunch reset

[Bead Pages](../README.md) / [bob-cli-df](README.md) / bob-cli-df.4

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-dd.land--3](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-dd.land.md) · **Assignee:** `bob-cli-df.4` · **Size:** large
**Created:** 2026-10-27 21:24:44 EDT · **Closed:** 2026-10-28 00:36:08 EDT
**Plan:** [202610/backlog\_batch\_b4.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/backlog_batch_b4.md)

## Description

dirty-tree-preservation: resolve the remaining bob-cli-cv loss in sase by proving and repairing the relaunch reset that still drops tracked edits after sase-1oh reopened failed closes; stash or otherwise preserve the full dirty tree before any hard reset.

## Notes

[2026-10-28T01:37:42Z · bob-cli-df.4] PLANNING: Audited B4 design, bob-cli-cv, closed sase-yo and sase-1oh.4; this phase had no prior work notes. At sase daf54c5b2d, failed-close reopening is landed but reset_replay still aborts before a HEAD-only snapshot, errors lose prior recovery refs, and stash-failure/reclone paths accept best-effort rescue without proof of dirty-content preservation. No source changes or historical reproduction claimed. Authored a four-phase child epic (verified snapshot, reset replay, relaunch cleanup, failed-close evidence) with parent_bead bob-cli-df.4; validated with --explain then revalidated, both pass with zero warnings. Submitting through sase plan propose; child land must verify full tracked/staged/untracked recovery and close df.4 only, leaving cv and df to B4 land.

[2026-10-28T04:38:13Z · bob-cli-df.4.1.land] Child epic bob-cli-df.4.1 is complete. Failed-close relaunch now preserves tracked, staged, untracked, conflict-stage, and nested-repository work before abort/reset, launch eviction, reclone, and cleanup. Durable snapshot locators are attached to failure evidence and restore the original bytes and index stages.

Landed SASE commits already on master: 42512dc116 (snapshot adapter), 55ebb614f2 (relaunch/reclone guards), 2bb3e813d3 (reset/replay), dcb7d2a6e7 (failed-close evidence). This turn repairs conflict-stage worktree capture and strict nested preflight on that tip (no later drift). Isolated tests with sase-core-rs 0.43.0: 84 focused preservation tests passed; failed-close snapshot/relaunch/deferral suite 4/4 passed. Gate: sase tool run check ba742b7008803cf3b427577388663bd0 — product lint green; KNOWN Footprint whitelist noise on sase-1p1/sase-1p1.8; UNKNOWN missing plans sidecar owned by bob-cli-dg. Leave bob-cli-df, bob-cli-cv, and B4 plan status to the outer land agent.

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-df.4](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-df.4.md) | [bob-cli-df.4](bob-cli-df.4.md) | 0 |
