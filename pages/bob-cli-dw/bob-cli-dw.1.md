# Bead: bob-cli-dw.1 — Expose RecoveryAssessment for failed-close snapshot imports

[Bead Pages](../README.md) / [bob-cli-dw](README.md) / bob-cli-dw.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-dp.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-dp.land.md) · **Assignee:** `bob-cli-dw.1` · **Size:** small
**Created:** 2026-10-28 15:35:24 EDT · **Closed:** 2026-10-28 15:56:05 EDT
**Plan:** [202610/backlog\_batch\_b6.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/backlog_batch_b6.md)

## Description

recovery-assessment-public: resolve bob-cli-dt in sase by exposing the shared failed-close assessment type through a public name and updating _failed_close_recovery_snapshots.py (and any other consumers) to import that public name. Do not suppress, whitelist, or pragma the private _RecoveryAssessment misuse. Read SASE symvision policy first. Verify with focused failed-close snapshot/recovery tests plus sase tool run check in the opened sase checkout. Independent clean witness 13ea2a464abef73b3eab4bfee9e624d7 already makes this KNOWN; later checks including 5d1634e22bc172fe358db97b9279961f still report it.

## Notes

[2026-10-28T19:55:54Z · bob-cli-dw.1] PROPOSED FOLLOW-UP: triage the 9 unused-public symvision findings unmasked by the RecoveryAssessment fix (ArtifactLinkCollisionPartition, FinderFeature, SnapshotEvidence, admission_sequence_for, candidates_from_tier, discover_nested_git_repos, overlay_payload, reduce_events, review_settings) — each needs delete/privatize/pragma per the symvision decision hierarchy

[2026-10-28T19:55:58Z · bob-cli-dw.1] PROPOSED FOLLOW-UP: recovery-test env mismatch — all 24 failed-close recovery tests fail identically on clean base with TypeError bead_close() takes 2-9 args but 10 given (Rust core binding vs facade drift); focused suite cannot go green until core pin is reconciled

[2026-10-28T19:56:05Z · bob-cli-dw.1] Exposed RecoveryAssessment as public in sase src/sase/finalizers/_failed_close_recovery_assess.py (renamed class, all 6 constructors, 2 annotations, added to __all__ keep-sorted) and updated the cross-module import in _failed_close_recovery_snapshots.py plus the retry test. Verified: dt private-import symvision node is gone on just _lint-symvision; ruff/mypy/keep-sorted/fmt pass via sase tool run check; focused recovery suite (7 modules) gives byte-identical results on patched vs clean base (24 pre-existing bead_close Rust-binding env failures, 1 pass) so zero regressions. sase tool run check stays red only on 9 pre-existing unused-public items in untouched files (masked on base; recorded as follow-up) and the pre-existing binding mismatch (recorded as follow-up). No --epic-symbol entries. dt left for the land agent to close.

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-dw.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-dw.1/README.md) | [bob-cli-dw.1](bob-cli-dw.1.md) | 0 |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-dw.1][1] | Need the phase scope and design file | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-dw.1/README.md

<!-- sase:referenced-by:end -->
