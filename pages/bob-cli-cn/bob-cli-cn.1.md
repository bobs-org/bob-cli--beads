# Bead: bob-cli-cn.1 — bob stats — additive \`typical\` object on day-grouped count and minutes points

[Bead Pages](../README.md) / [bob-cli-cn](README.md) / bob-cli-cn.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.research.5d.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.research.5d.linker.w0.md) · **Assignee:** `bob-cli-cn.1` · **Size:** medium
**Created:** 2026-10-26 13:12:28 EDT · **Closed:** 2026-10-26 14:02:17 EDT
**Plan:** [202610/day\_strip\_typical\_day.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/day_strip_typical_day.md)

## Description

typical-field: in bob-cli, add the optional `typical` object (window D−7…D−1, median, ≥4 usable days, relation, words, detail) to current day-grouped `points` of count and minutes metrics. Share the usable-value rule with rolling medians and extend the Day lead-in from 6 to 7 days. Cover it with hand-derived unit and golden tests, document the schema-1 field in docs/stats.md, and check parity read-only on the live vault.

## Notes

[2026-10-26T18:01:53Z · bob-cli-cn.1] Live parity (local release binary, live ~/bob, read-only): Oct 25 matches research exactly — Worked 3h 25m below typical 4h 10m, Reviewed 75 above typical 54, Done 17 below typical 19, Created 9 below typical 23; Oct 6 Done 86 above typical 7; today shows mark-free typical line; typical JSON matches the plan contract byte-for-shape; typical(Oct 6)=rolling_median(Oct 5)=7. No vault drift.

[2026-10-26T18:01:58Z · bob-cli-cn.1] PROPOSED FOLLOW-UP: lib does not compile on the clean base tree — StoreWriteParams is missing the verified field in initializers (highlights_ref/create.rs, highlights_ref/overwrite/execute.rs); all cargo gates fail there identically with and without this phase.

[2026-10-26T18:02:02Z · bob-cli-cn.1] PROPOSED FOLLOW-UP: just docs-check lint fails on clean tree — BOB_TEST_FIXTURE_PDF undocumented env (highlights_ref/source_store.rs:194); unrelated to stats docs.

[2026-10-26T18:02:06Z · bob-cli-cn.1] PROPOSED FOLLOW-UP: 3 lib test failures reproduce without this phase — catalog public_leaves_are_entries_or_excluded (ref attach-source), completion every_value_arg_has_a_decision (ref code:number/page), highlights_ref source_store inspect test (1 vs 2); track as CI failure bead.

[2026-10-26T18:02:17Z · bob-cli-cn.1] Verified: 175 stats lib tests pass (14 new hand-derived typical tests + golden assertions); live-vault parity matches research exactly (Oct 25 four facts, Oct 6 Done 86/typical 7, provisional today mark-free); 4-week JSON +9.8% bytes with compute time within noise; committed 3f417646 feat(stats). Pre-existing clean-tree failures (highlights_ref verified-field compile break, docs-check env lint, 3 lib test failures) recorded as PROPOSED FOLLOW-UP notes.

## Dependencies

- **Blocks:** [bob-cli-cn.2](bob-cli-cn.2.md) ✓ · ⧖ 2026-10-26

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-cn.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-cn.1/README.md) | [bob-cli-cn.1](bob-cli-cn.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`3f41764`](https://github.com/bobs-org/bob-cli/commit/3f417646f1c65db71ea86106906a0184b5908b03) | feat(stats): add typical day to daily points | [bob-cli-cn.1](bob-cli-cn.1.md) | 2026-10-26 14:00:55 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-cn.1][1] | Need the phase scope and design file | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-cn.1/README.md

<!-- sase:referenced-by:end -->
