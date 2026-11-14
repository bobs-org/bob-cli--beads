# Bead: bob-cli-lh.1 — bob bank report counts stats-strip periods

[Bead Pages](../README.md) / [bob-cli-lh](README.md) / bob-cli-lh.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.4l.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.4l.linker.w0.md) · **Assignee:** `bob-cli-lh.1` · **Size:** medium
**Created:** 2026-11-14 06:52:51 EST · **Closed:** 2026-11-14 07:54:33 EST
**Plan:** [202611/bank\_badge\_strip\_family.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/bank_badge_strip_family.md)

## Description

report-periods: add -p/--period (resolved by the periods calendar, all time over the bank's own history) and -s/--summary to bob bank report, route day totals through compute_totals, emit coverage and navigation JSON, document and test it.

## Notes

[2026-11-14T12:54:33Z · bob-cli-lh.1] report-periods done: -p/--period (day/ISO week/quarter/ISO year/all/last-*/note path) and -s/--summary on bob bank report; day totals routed through compute_totals; coverage and navigation JSON on every report plus a human coverage line; docs/bank.md updated with CLI reference regenerated. Verified: 8 new report tests pass, all 142 bank lib tests pass, bank CLI integration + docs_reference pass, just fmt/lint/docs-check pass, manual -p 2026-Q4/-p all/-p 2026-W46 runs verified. Committed fb0426b3. Full workspace cargo test exceeds the single-command time limit (timed out mid-run, unrelated suites still going); no failures observed.

## Dependencies

- **Blocks:** [bob-cli-lh.3](bob-cli-lh.3.md) ✓ · ⧖ 2026-11-14
- **Blocks:** [bob-cli-lh.4](bob-cli-lh.4.md) ◐ · ⧖ 2026-11-14

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-lh.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-lh.1/README.md) | [bob-cli-lh.1](bob-cli-lh.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`575f9e6`](https://github.com/bobs-org/bob-cli/commit/575f9e66d638d0034978574dba19016c4a35b010) | feat(bank): report counts stats-strip periods with coverage and navigation | [bob-cli-lh.1](bob-cli-lh.1.md) | 2026-11-14 07:57:44 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-lh.1][1] | Need the phase scope and design file | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-lh.1/README.md

<!-- sase:referenced-by:end -->
