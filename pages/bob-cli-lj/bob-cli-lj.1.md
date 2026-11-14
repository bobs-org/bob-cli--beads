# Bead: bob-cli-lj.1 — bob bank report -c child-period aggregate

[Bead Pages](../README.md) / [bob-cli-lj](README.md) / bob-cli-lj.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.4m.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.4m.linker.w0.md) · **Assignee:** `bob-cli-lj.1` · **Size:** medium
**Created:** 2026-11-14 09:39:37 EST · **Closed:** 2026-11-14 13:44:37 EST
**Plan:** [202611/bank\_period\_charts.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/bank_period_charts.md)

## Description

report: share the periods calendar's child partition, then add an opt-in `-c/--charts` aggregate to `bob bank report` with per-bucket money, coverage states, targets, group totals, folded categories, tests, and the JSON contract docs.

## Notes

[2026-11-14T18:44:37Z · bob-cli-lj.1] Start gate: bob-cli-lh CLOSED. Shared child partition moved to src/native/periods/children.rs (column_specs, child_specs, group_specs, dates/weeks/quarters/years_between, clip_span, period_bounds, day_caption); periods/report.rs delegates with no behavior change (all existing periods tests pass unchanged) plus golden tests for W46, W01, W53, Q4 (14 weeks), ISO 2026 (53 weeks grouped Q1-Q4), all-time across years, and caption parity. New src/native/bank/charts.rs (+charts_tests.rs): period_id_for, buckets/groups via compute_totals, states, targets, top_out, folded categories, 64-quarter->year coarsening and >64-year null; BankReport carries charts; to_json emits charts only with -c. CLI -c/--charts (alphabetical, help, example) with exit-2 refusal for -D/-m/-y/default month/-p day (JSON ok:false); human aligned bucket+group table (In green, waiting yellow, non-tracked dim, NO_COLOR respected). Tests: 22 unit tests (every invariant for W46, Q4, ISO 2026, W53, W01, all; ids/labels vs shared API; state boundaries incl IT==T; transfer/cash-account/cash-category/refund/bare-credit/zero-cent rows; pinned/one-leftover/tie/rest folding; day targets with and without headings; -s -c days []; no charts key without -c; future-only history -> buckets []; coarsen/null) and 2 CLI tests. Docs: docs/bank.md Commands + new JSON 'Report charts' subsection, json-outputs bank-reports line; just docs-gen regenerated docs/reference/cli/bank.md; just docs-check passed; just check passed (fmt, clippy, 6960 lib + 3653 cli tests, 0 failures).

## Dependencies

- **Depends on:** [bob-cli-lh](../bob-cli-lh/README.md) ✓ · ⧖ 2026-11-14
- **Blocks:** [bob-cli-lj.4](bob-cli-lj.4.md) ✓ · ⧖ 2026-11-14

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-lj.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-lj.1/README.md) | [bob-cli-lj.1](bob-cli-lj.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`b3dc64a`](https://github.com/bobs-org/bob-cli/commit/b3dc64a04fd7b2ac9c9b8835c86e3dca6885c7b1) | feat(bank): add bob bank report -c child-period chart aggregate | [bob-cli-lj.1](bob-cli-lj.1.md) | 2026-11-14 13:46:57 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-lj.1][1] | Check notes from earlier agent | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-lj.1.md

<!-- sase:referenced-by:end -->
