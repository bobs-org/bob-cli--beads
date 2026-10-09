# Bead: bob-cli-5w.7 — Pure successor helpers in task-status-cycler

[Bead Pages](../README.md) / [bob-cli-5w](README.md) / bob-cli-5w.7

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.0p.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.0p.linker.w0.md) · **Assignee:** `bob-cli-5w.7` · **Size:** medium
**Created:** 2026-10-09 11:54:15 EDT · **Closed:** 2026-10-09 12:42:20 EDT
**Plan:** [202610/successor\_links.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/successor_links.md)

## Description

cycler_engine: in task-status-cycler, add pure helpers that mirror the Rust planner: a dependents index built from the Tasks cache or from documents, eligibility, anchors, ordering, the breaker, the ported block-ID suggester, link form, placement edits, notice text, and config and today-path loaders. Ships SL and SB vector tests and no wiring.

## Notes

[2026-10-09T16:42:08Z · bob-cli-5w.7] PROPOSED FOLLOW-UP: test-navigation-roll-decay has 2 date-sensitive failures (picker-single Ctrl+Enter roll cases expect [?] for scheduled 2026-10-08) that fail identically on the clean base tree; triage separately

[2026-10-09T16:42:12Z · bob-cli-5w.7] PROPOSED FOLLOW-UP: skipped memory change per epic auto-decisions (decision_record=no, glossary_term=no): after landing, consider recording "a closed planned task hands its slot to its successors" as a decisions strand and adding a "Successor Link" glossary term

[2026-10-09T16:42:20Z · bob-cli-5w.7] Pure successor helpers landed in bob-plugins task-status-cycler: 085-successor-plan.js (774 lines: index, normalizers, live links, anchors, planSuccessors), 086-successor-ids.js (406 lines: Rust suggester port, cleanDescription, mint, link form), 087-successor-place.js (638 lines: insertions, notice text, loaders; third fragment required by the 1000-line build gate, loaders-in-either-fragment allowed it). Verified: npm run build + build:check green, new suite 41/41 (all SB1-9 verbatim; SL1,SL3-19,SL23-28; SL2/SL20/SL21-hooks excluded per plan), full npm test 2274/2276 with 2 roll-decay failures that reproduce identically on the clean tree (recorded as follow-up). No wiring, no version bump, no sync.

## Dependencies

- **Depends on:** [bob-cli-5w.2](bob-cli-5w.2.md) ✓ · ⧖ 2026-10-09
- **Blocks:** [bob-cli-5w.8](bob-cli-5w.8.md) ✓ · ⧖ 2026-10-09

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-5w.7](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-5w.7/README.md) | [bob-cli-5w.7](bob-cli-5w.7.md) | 0 |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-5w.7][1] | Need the phase scope and design file | 1 |
| read-by | [agent:bob-cli-5w.8][2] | Need pure helper API from cycler_engine to wire in 5w.8 | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-5w.7/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-5w.8/README.md

<!-- sase:referenced-by:end -->
