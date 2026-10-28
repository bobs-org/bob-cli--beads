# Bead: bob-cli-df.2.1.4 — Repair artifact-link durability ordering and quarantine replay

[Bead Pages](../README.md) / [bob-cli-df.2.1](bob-cli-df.2.1.md) / bob-cli-df.2.1.4

**Status:** ◐ in_progress · **Type:** ▸ plan · **Tier:** epic
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-df.2.1.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-df.2.1.land.md) · **Assignee:** `bob-cli-df.2.1.4.land`
**Created:** 2026-10-28 02:07:52 EDT
**Plan:** [202610/artifact\_link\_quarantine\_landing\_repairs.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/artifact_link_quarantine_landing_repairs.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| implemented-by | [plan:202610/artifact_link_quarantine_landing_repairs.md][1] | derived from the plan's `bead_id:` frontmatter field |
| related | file:explicit:4ea0ec4a426fca44ad0e64e8 | attached via sase artifact create --bead |
| related | file:explicit:93c39bb2954df550e568ab38 | attached via sase artifact create --bead |

_Plus 1 automatic references — see [Referenced By](#referenced-by)._

[1]: https://github.com/bobs-org/bob-cli--plans/blob/main/202610/artifact_link_quarantine_landing_repairs.md

<!-- sase:links:end -->

## Description

Preserve the earliest provable durable payload and make quarantined replays settle idempotently without weakening corruption checks.

## Notes

[2026-10-28T08:30:13Z · bob-cli-df.2.1.4.land] LAND AUDIT / FOLLOW-UP TRIAGE: read this epic (no discretionary DECISIONS), both child scopes and every note, original parent .2.1 and all three children, linked quarantine plans, B4 plan, previous audit, landed source/commits core f4bf6074 and SASE ac23f63ee4. Clean SASE fast-forwarded to ac23f63ee4; core remains f4bf6074; both match fetched origin/master. Pin is the real core repair SHA. Post-start dae555aa20 and 0028e6765d are Footprint UI/review changes, with no new competing artifact-link reducer; preserve sibling inlet rollback 1b1162b313. FOLLOW-UP OUTCOMES: .4.1 #1 corroborated existing bob-cli-dh (reported identical clean-base 27 Clippy errors, no fresh check claimed); .4.2 #1 corroborated bob-cli-dg (reported clean-base plans-sidecar invalid-root); .4.2 #2 supplemented DISCOVERED ISSUE on causal active bob-cli-df for sibling _RecoveryAssessment import, witness 13ea2a464abef73b3eab4bfee9e624d7; .4.2 #3 created medium ready bob-cli-di after searches/sweep/active-epic audit found no duplicate or causal owner. Independently reproduced lost outer Justfile core settings in nested _core-overrides-arg; phase observed downgrade, but bare-name-overrides diagnosis needs verification. Original .2.1.2 stale Footprint proposal remains declined as already fixed by c80a6c791a per prior parent audit; no new task. REMAINING EPIC WORK: extracted current Rust helpers discard A first durable at 10:00 when a late copy of A descends from B at 11:00 (actual winner B); actual Python history module omits Git-provable ancestry across roots; actual quarantine load/reuse accepts a symlinked v1 namespace (wire validation stubbed in path probe); approved lib/prelude cleanup omitted; planned empty-store outbox restart/crossover/local and truly independent timezone coverage absent. Probe file:explicit:93c39bb2954df550e568ab38 records methods. No production changes, global wheel use, or fresh full-gate pass claimed. Current Python checkout unprovisioned and exact wheel cache lookup misses. All df.2.1.4/df.2.1/df.2 epic-symbol audits empty. Epic and plans stay open/wip. Plan only these repairs in two sequential phases because Python must pin the next committed core fix; no child coding closeout phase.

[2026-10-28T08:33:50Z · bob-cli-df.2.1.4.land] Detailed landing audit and all follow-up dispositions: file:explicit:4ea0ec4a426fca44ad0e64e8; bounded reproduction source: file:explicit:93c39bb2954df550e568ab38. Authored remaining-work child epic Finish collision provenance and quarantine path safety, parent_bead=bob-cli-df.2.1.4, with two medium sequential phases (copy chronology/import cleanup, then consumer pin/cross-root history/path safety/recovery tests). Validated with --explain and revalidated without it, both zero warnings. This needs a committed core SHA before Python verification, so a single tale cannot complete the dependency. Child land resumes df.2.1.4, then rechecks/closes df.2.1 and only phase df.2 when ready; B4 and 5m remain outer-land responsibilities. No parent closure, plan done status, or fresh just check pass claimed.

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-df.2.1.4.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-df.2.1.4.land.md) | [bob-cli-df.2.1.4](bob-cli-df.2.1.4.md) | 0 |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-df.2.1.4.1--5][1] | Need parent epic decisions that govern the artifact-link collision ordering phase | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-df.2.1.4.1.md

<!-- sase:referenced-by:end -->
