# Bead: bob-cli-df.4.1.3 — Protect workspace preparation and cleanup fallbacks

[Bead Pages](../README.md) / [bob-cli-df.4.1](bob-cli-df.4.1.md) / bob-cli-df.4.1.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-df.4](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-df.4.md) · **Assignee:** `bob-cli-df.4.1.3` · **Size:** medium
**Created:** 2026-10-27 21:39:19 EDT · **Closed:** 2026-10-27 22:50:09 EDT
**Plan:** [202610/preserve\_failed\_close\_worktrees.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/preserve_failed_close_worktrees.md)

## Description

relaunch-cleanup: require verified preservation before preparation, stash-failure reset, forced checkout, and reclone; ensure preservation failure cannot fall through to destructive cleanup.

## Notes

[2026-10-28T02:49:54Z · bob-cli-df.4.1.3] PROPOSED FOLLOW-UP: SASE symvision gate fails on stale sase-1p1(other_id)/custom_id epic-symbols — check run dd9cde550a6d74301ff566047f9245fe triages both as KNOWN (witness c65495a42177023e3c2c7bb989a06055); same class as 4.1.1-reported stale sase-1p1.6 symbols, not caused by relaunch-cleanup.

[2026-10-28T02:49:58Z · bob-cli-df.4.1.3] PROPOSED FOLLOW-UP: sase validate plan-links fails invalid-root in external sase checkout (missing sase/repos/plans sidecar) — same environmental failure 4.1.1 recorded as note #3 after stashing snapshot work; not caused by relaunch-cleanup.

[2026-10-28T02:50:09Z · bob-cli-df.4.1.3] Verified relaunch-cleanup: 30 focused tests pass (16 self_heal incl. updated dirty-tree external-recovery restore + stash-failure snapshot + preservation-failure refusal, 14 reclone incl. new dirty-worktree recoverable-after-removal + preservation-failure intact + non-eligible refusal); 11 snapshot, 51 provider git ops, 23 reset_replay all pass. mypy clean. Verified snapshot required before abort/clean/force-checkout/branch-recreate/sync-reset/reclone move-aside; preservation failures raise non-reclone-eligible errors and leave tracked+untracked bytes untouched; sase/repos sidecars use separate rescue boundaries. sase tool run check: only failures are the two clean-tree issues recorded as PROPOSED FOLLOW-UP (stale sase-1p1 symvision symbols KNOWN, missing plans sidecar invalid-root environmental).

## Dependencies

- **Depends on:** [bob-cli-df.4.1.1](bob-cli-df.4.1.1.md) ✓ · ⧖ 2026-10-27
- **Blocks:** [bob-cli-df.4.1.4](bob-cli-df.4.1.4.md) ✓ · ⧖ 2026-10-27

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-df.4.1.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-df.4.1.3/README.md) | [bob-cli-df.4.1.3](bob-cli-df.4.1.3.md) | 0 |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-df.4.1.3][1] | Need the phase scope and design file | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-df.4.1.3/README.md

<!-- sase:referenced-by:end -->
