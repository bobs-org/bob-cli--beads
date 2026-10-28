# Bead: bob-cli-df.2.1 — Quarantine artifact-link collisions and keep unrelated writes available

[Bead Pages](../README.md) / [bob-cli-df.2](bob-cli-df.2.md) / bob-cli-df.2.1

**Status:** ◐ in_progress · **Type:** ▸ plan · **Tier:** epic
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-df.2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-df.2.md) · **Assignee:** `bob-cli-df.2.1.land`
**Created:** 2026-10-27 21:43:18 EDT
**Plan:** [202610/artifact\_link\_collision\_quarantine.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/artifact_link_collision_quarantine.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| implemented-by | [plan:202610/artifact_link_collision_quarantine.md][1] | derived from the plan's `bead_id:` frontmatter field |
| related | file:explicit:15c5f62a7ee80433016f062f | attached via sase artifact create --bead |

_Plus 3 automatic references — see [Referenced By](#referenced-by)._

[1]: https://github.com/bobs-org/bob-cli--plans/blob/main/202610/artifact_link_collision_quarantine.md

<!-- sase:links:end -->

## Description

Preserve the earliest durable artifact-link payload, retain conflicting replays as visible quarantine evidence, and allow unrelated reads, writes, and outbox publication to complete.

## Notes

[2026-10-28T06:03:19Z · bob-cli-df.2.1.land] LAND AUDIT / FOLLOW-UP TRIAGE: reviewed epic (no discretionary DECISIONS), every note on closed .1/.2/.3, both linked plans, commits core 6613c9bb and sase 6470f7d7a0/d59c46296f, and current source/tests. Fast-forwarded clean SASE to a9abdd5c97; fresh fetch confirms that tip and core 31deb0d2 match origin/master. Core pin contains all six bindings. Non-epic Footprint/recovery/split drift adds no conflicting event reducer; sibling 1b1162b313 plan-inlet rollback remains needed. FOLLOW-UP OUTCOMES: .1 #1 deterministic 27-clippy clean-base failure -> medium ready CI task bob-cli-dh (phase evidence, no fresh full-gate run claimed). .2 #1 stale closed-phase Footprint exemptions -> declined as already removed in current tree by c80a6c791a; supplemental impact recorded on existing sase-o7, already routed to active sase-1p1 by df.4.1.land. .3 close-note missing external plans sidecar -> existing bob-cli-dg, no duplicate. .3 private _RecoveryAssessment import -> DISCOVERED ISSUE on active parent bob-cli-df, since sibling recovery dcb7d2a6e7 introduced it. REMAINING EPIC WORK: exact extracted Rust comparison probes choose the later instant across timezone offsets, choose a descendant under mixed ancestry/clock skew, and discard earlier same-digest evidence when the later copy has a smaller source locator. Actual Python history adapter in a synthetic depth-1 Git clone claims complete first-add evidence for the wrong boundary commit. Source trace also shows first-batch quarantine metadata changes after winner durability and therefore collides with its immutable record on retry, leaving the loser queued; new quarantine loader lacks path/project validation. Planning only these gaps. No production changes or full verification pass; both epic-symbol audits are empty. Epic and df.2 remain open.

[2026-10-28T06:06:37Z · bob-cli-df.2.1.land] Remaining-work evidence is file:explicit:15c5f62a7ee80433016f062f. Authored and validated (with --explain, then corrected phase description prefixes and revalidated without it; zero warnings) the child epic Artifact-link durability ordering and quarantine replay. Two medium sequential coding phases are needed: core policy first, then Python pin/wheel plus incomplete-history, immutable-retry, and record-validation repairs. A tale cannot verify a pin to its own future Rust commit; no child coding phase performs the parent closeout. parent_bead=bob-cli-df.2.1 returns the child lander to this audit, with explicit normal closure of df.2.1 and then only phase df.2 when complete. The current epic and original plan stay in progress. All proposing-bead follow-up dispositions are recorded in the prior landing note.

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-df.2.1.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-df.2.1.land.md) | [bob-cli-df.2.1](bob-cli-df.2.1.md) | 0 |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-df.2.1.1][1] | Need epic decisions and landing scope | 1 |
| read-by | [agent:bob-cli-df.2.1.2][2] | Need epic DECISIONS that are final for this phase | 2 |
| read-by | [agent:bob-cli-df.2.1.4.1--5][3] | Need the governing parent epic scope and decisions for this repair | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-df.2.1.1/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-df.2.1.2/README.md
[3]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-df.2.1.4.1.md

<!-- sase:referenced-by:end -->
