# Bead: bob-cli-an.6.6.6.5.6.5.5.6.6.6 — Backlog batch 11: gated live ref-id repair, Task Card close cleanup, popout mark gates, gkeep stdin EPIPE, and start-name again order

[Bead Pages](../README.md) / [bob-cli-an.6.6.6.5.6.5.5.6.6](bob-cli-an.6.6.6.5.6.5.5.6.6.md) / bob-cli-an.6.6.6.5.6.5.5.6.6.6

**Status:** ✓ closed · **Resolution:** done · **Type:** ▸ plan · **Tier:** epic
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.land.md) · **Assignee:** `bob-cli-an.6.6.6.5.6.5.5.6.6.6.land`
**Created:** 2026-10-25 11:34:35 EDT · **Closed:** 2026-10-26 08:22:56 EDT
**Plan:** [202610/backlog\_batch11\_ref\_repair\_taskcard\_popout\_gkeep\_again.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/backlog_batch11_ref_repair_taskcard_popout_gkeep_again.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| implemented-by | [plan:202610/backlog_batch11_ref_repair_taskcard_popout_gkeep_again.md][1] | derived from the plan's `bead_id:` frontmatter field |

_Plus 3 automatic references — see [Referenced By](#referenced-by)._

[1]: https://github.com/bobs-org/bob-cli--plans/blob/main/202610/backlog_batch11_ref_repair_taskcard_popout_gkeep_again.md

<!-- sase:links:end -->

## Description

Close five backlog tasks by repairing the live vault's reference ids only through a Bryan-approved gate, restoring the Task Card close cleanup, showing ledger marks in popout windows, removing the gkeep login stdin broken-pipe race, and listing repeated start names newest-first.

## Notes

[2026-10-26T12:22:56Z · bob-cli-an.6.6.6.5.6.5.5.6.6.6.land] BATCH-11 LANDER verification. All 5 phases are closed and every phase note was addressed.
(1) ref-id-live-repair: Bryan approved gate turn custom-ref-id-repair-20261026-f126bb62 and it repaired the ids (vault commits db7bd81a, c5b186b1). The lander re-verified read-only with a bob built from master 4ee76d11: reference ids ok (454 notes), 1134/1134 rows, 0 duplicate ids, 0 mismatches.
(2) task-card-close-cleanup: bob-plugins c07b125. Source confirmed; picker-lifecycle 18/18 pass; vault nav-hotkeys 2.56.4 is byte-identical to the repo.
(3) popout-mark-gates: bob-plugins 4e54e2f adds the mark-gate mixin. date/progress/unblocked suites pass 41/23/20 on master 04c61c7; the mixin is deployed in the vault.
(4) gkeep-stdin-epipe: bob-cli c8573d78. gkeep_auth 11/11 pass.
(5) start-name-again-order: bob-cli a8ef1718. A,B,A regression passes.
Target tasks b8, 4e, 9q, 2m, and bn are closed done with evidence.
DECISIONS honored:
- Live writes ran only inside the approved gate.
- Plugins were deployed only through bob plugins sync.
- No version or CHANGELOG edits.
Integration: bob-cli 5384319e..4ee76d11 (highlights overwrite/reread, homes root, docs) and bob-plugins 4150279..04c61c7 (Day strip, stats root parents) neither use nor conflict with the epic's changes. No new stdin-writing gkeep helpers; no new body-class gates. bob-ledger-tools 1.72.0 (repo) vs 1.71.0 (vault) is drift from another epic's Day-strip work and is left to its owner.
just check: the first run failed only the known capture_related perf flake (774/698 ms at load 15; passes isolated); +1 recorded on bob-cli-ca. The rerun exited 0.
FOLLOW-UPS:
- .1 note #3 (sase gate --turn missing_gate_turn_row): declined as a new task; it duplicates sase-1el in the sase project (root cause fixed there). +1 recorded on sase-1el.
- .3 note #2 (priority marks in popouts): created bob-cli-cb (small bug), widened after a source audit to the four remaining main-window-only body-class gates (priority, task-tag, fresh, today-off).
Epic symbols: none.

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.6.land](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.6.land/README.md) | [bob-cli-an.6.6.6.5.6.5.5.6.6.6](bob-cli-an.6.6.6.5.6.5.5.6.6.6.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli--plans | [`bob-cli--plans@6b9f799`](https://github.com/bobs-org/bob-cli--plans/commit/6b9f79901fc4ad38332a32fbf6499236781ab3ec) | chore(plans): mark backlog batch 11 plan done | [bob-cli-an.6.6.6.5.6.5.5.6.6.6](bob-cli-an.6.6.6.5.6.5.5.6.6.6.md) | 2026-10-26 08:26:36 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-an.6.6.6.5.6.5.5.6.6.6.2][1] | parent epic scope | 1 |
| read-by | [agent:bob-cli-an.6.6.6.5.6.5.5.6.6.6.3][2] | epic decisions | 1 |
| read-by | [agent:bob-cli-an.6.6.6.5.6.5.5.6.6.6.4][3] | parent epic DECISIONS and scope | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.6.2/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.6.3/README.md
[3]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.6.4/README.md

<!-- sase:referenced-by:end -->
