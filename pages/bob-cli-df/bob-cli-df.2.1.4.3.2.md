# Bead: bob-cli-df.2.1.4.3.2 — Gather cross-root ancestry and finish safe quarantine recovery coverage

[Bead Pages](../README.md) / [bob-cli-df.2.1.4.3](bob-cli-df.2.1.4.3.md) / bob-cli-df.2.1.4.3.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-df.2.1.4.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-df.2.1.4.land.md) · **Assignee:** `bob-cli-df.2.1.4.3.2` · **Size:** medium
**Created:** 2026-10-28 04:35:24 EDT · **Closed:** 2026-10-28 06:38:59 EDT
**Plan:** [202610/artifact\_link\_provenance\_closeout.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/artifact_link_provenance_closeout.md)

## Description

adapter-recovery: pin the core repair, gather cross-root provenance, reject unsafe quarantine paths, and prove restart settlement.

## Notes

[2026-10-28T10:03:43Z · bob-cli-df.2.1.4.3.2] Pinned sase-core 00fe29d5 (isolated .venv head matches). Cross-root history adapter, unsafe quarantine path rejection, empty-store outbox restart, direct/outbox reverse, and document/ownerless recovery tests: 21/21 pass. Related store/core/health/quarantine/publisher/outbox/doctor/CLI add-rm/plan-formatting: 104 pass. just fix clean. epic-symbols empty.

[2026-10-28T10:14:31Z · bob-cli-df.2.1.4.3.2--1] just check failed mypy on attach_collision_history: ancestors_by_key.get received tuple[str, str] | None. Narrowed key after a missing-root continue and typed complete first-add commits as dict[tuple[str, str], str]. just fix clean; epic-symbols empty. Pin remains 00fe29d5.

[2026-10-28T10:38:43Z · bob-cli-df.2.1.4.3.2--2] PROPOSED FOLLOW-UP: External sase checkout plan links validate invalid-root for missing sase/repos/plans reproduces on clean HEAD (tool run c22e8134aaf51624cc76b121e7e284db) — already tracked by bob-cli-dg

[2026-10-28T10:38:47Z · bob-cli-df.2.1.4.3.2--2] PROPOSED FOLLOW-UP: KNOWN symvision private _RecoveryAssessment import in src/sase/finalizers/_failed_close_recovery_assess.py (witness 13ea2a464abef73b3eab4bfee9e624d7) — already on containing epic bob-cli-df / B4 land

[2026-10-28T10:38:59Z · bob-cli-df.2.1.4.3.2--2] Pinned sase-core 00fe29d5 (isolated wheel metadata sase_core_commit matches). Cross-root history, unsafe quarantine path rejection, empty-store outbox restart, direct/outbox reverse, and document/ownerless tests: 21/21. Related store/publisher/outbox/CLI add-doctor: 76+17 pass. just fix clean; ruff/mypy green; epic-symbols empty. just check stopped on clean-base plan links validate (bob-cli-dg) and KNOWN _RecoveryAssessment (witness 13ea2a464abef73b3eab4bfee9e624d7).

## Dependencies

- **Depends on:** [bob-cli-df.2.1.4.3.1](bob-cli-df.2.1.4.3.1.md) ✓ · ⧖ 2026-10-28

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-df.2.1.4.3.2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-df.2.1.4.3.2.md) | [bob-cli-df.2.1.4.3.2](bob-cli-df.2.1.4.3.2.md) | 0 |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-df.2.1.4.3.2--2][1] | Need the phase scope and design file | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-df.2.1.4.3.2.md

<!-- sase:referenced-by:end -->
