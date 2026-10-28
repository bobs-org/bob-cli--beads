# Bead: bob-cli-df.4.1.1 — Verified durable checkout snapshots

[Bead Pages](../README.md) / [bob-cli-df.4.1](bob-cli-df.4.1.md) / bob-cli-df.4.1.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-df.4](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-df.4.md) · **Assignee:** `bob-cli-df.4.1.1` · **Size:** medium
**Created:** 2026-10-27 21:39:18 EDT · **Closed:** 2026-10-27 22:25:04 EDT
**Plan:** [202610/preserve\_failed\_close\_worktrees.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/preserve_failed_close_worktrees.md)

## Description

verified-snapshot: add a non-destructive, verified snapshot adapter around workspace rescue; retain tracked, staged, and untracked content outside the checkout, and refuse incomplete preservation.

## Notes

[2026-10-28T02:03:11Z · bob-cli-df.4.1.1] Callable contract for integration phases (reset-replay, relaunch-cleanup, failed-close-evidence):

  from sase.workspace_provider.snapshot import (
      PreservationError, SnapshotRecord, snapshot_git_repo, restore_git_snapshot,
  )

  record = snapshot_git_repo(repo_root, workspace_dir=..., workspace_num=..., label=..., reason=...)
  \# None: proven no-work (clean index+worktree, no unmerged).
  \# SnapshotRecord: verified snapshot; record.manifest_path is absolute; record.snapshot_id is stable.
  \# PreservationError: incomplete preservation. Source index, worktree, HEAD, and operation state are unchanged. The in-progress capture dir is discarded. Successful snapshots are kept. None is never returned on failure.

  restore_git_snapshot(record.manifest_path, dest_repo)  # dest may be empty; pack is self-contained.

Keep rescue_git_repo for existing best-effort callers until those phases migrate. Capture uses temporary indexes and GIT_OBJECT_DIRECTORY copies, not stash push. Payloads live in the existing rescue store outside the checkout; retention is unchanged. Size-cap, status/diff, missing-payload, write, and mid-capture change failures raise PreservationError rather than skipping.

[2026-10-28T02:24:45Z · bob-cli-df.4.1.1--1] PROPOSED FOLLOW-UP: SASE Justfile still has --epic-symbol sase-1p1.6(Overlay) and sase-1p1.6(load_overlay) after that bead closed — just check lint(symvision) fails identically on clean HEAD (KNOWN witness d7760f1346444dcb440fd30f5f921aac); this phase has no epic-symbol leftovers.

[2026-10-28T02:24:49Z · bob-cli-df.4.1.1--1] PROPOSED FOLLOW-UP: sase validate plan-links fails invalid-root because an external sase checkout has no sase/repos/plans sidecar — reproduced after stashing snapshot work; environmental, not caused by verified-snapshot.

[2026-10-28T02:25:04Z · bob-cli-df.4.1.1--1] Verified snapshot adapter is in sase: snapshot_git_repo/restore_git_snapshot/PreservationError, non-destructive capture, fail-closed on incomplete preservation. 11 snapshot tests plus 16 existing rescue tests passed (27 total). just check still fails on two clean-tree issues recorded as PROPOSED FOLLOW-UP: stale sase-1p1.6 epic-symbols and missing sase/repos/plans sidecar in this external checkout.

## Dependencies

- **Blocks:** [bob-cli-df.4.1.2](bob-cli-df.4.1.2.md) ✓ · ⧖ 2026-10-27
- **Blocks:** [bob-cli-df.4.1.3](bob-cli-df.4.1.3.md) ✓ · ⧖ 2026-10-27
- **Blocks:** [bob-cli-df.4.1.4](bob-cli-df.4.1.4.md) ◐ · ⧖ 2026-10-27

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-df.4.1.1](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-df.4.1.1.md) | [bob-cli-df.4.1.1](bob-cli-df.4.1.1.md) | 0 |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-df.4.1.1--1][1] | Need the phase scope and design file | 2 |
| read-by | [agent:bob-cli-df.4.1.3][2] | Check sibling phase completion and contract for relaunch-cleanup | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-df.4.1.1.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-df.4.1.3/README.md

<!-- sase:referenced-by:end -->
