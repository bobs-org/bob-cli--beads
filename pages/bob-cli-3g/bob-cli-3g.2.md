# Bead: bob-cli-3g.2 — Ledger-tools tiered queue, status bar, and lane marks

[Bead Pages](../README.md) / [bob-cli-3g](README.md) / bob-cli-3g.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.0v7](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.0v7.md) · **Assignee:** `bob-cli-3g.2` · **Size:** medium
**Created:** 2026-10-01 18:28:57 EDT · **Closed:** 2026-10-01 19:30:00 EDT
**Plan:** [202610/tiered\_morning\_review\_walk.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/tiered_morning_review_walk.md)

## Description

ledger-walk: mirror the tiered evaluator in bob-ledger-tools under freshness namespace v4, update the status bar and review meters, and give due lane tasks the due freshness mark.

## Notes

[2026-10-01T23:30:00Z · bob-cli-3g.2] ledger-walk landed on bob-plugins 91b8e40 base as 1.17.0 (1.16.0 was taken by 3f.4): tiered evaluator with lane intervals, v4 namespace + intervalForLine, new status bar/review meter on upkeepToday, lane marks M9/M10/M19/M20. Verified: npm test 1172/1172 green (freshness 46, marks 27, incl. Q1/Q2/L1-L5/R1/R2/S14/S15/B1 verbatim), npm run validate 6/6, deployed via bob plugins sync (vault shows 1.17.0); nav 1.49 suites pass unchanged against v4.

## Dependencies

- **Depends on:** [bob-cli-3g.1](bob-cli-3g.1.md) ✓ · ⧖ 2026-10-01
- **Blocks:** [bob-cli-3g.3](bob-cli-3g.3.md) ✓ · ⧖ 2026-10-01

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-3g.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-3g.2/README.md) | [bob-cli-3g.2](bob-cli-3g.2.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@cdadcde`](https://github.com/bobs-org/bob-plugins/commit/cdadcded6e5eccfac7cba8ac3db40001578a9167) | feat(ledger-tools): tiered morning review walk with daily lane review (1.17.0) | [bob-cli-3g.2](bob-cli-3g.2.md) | 2026-10-01 19:31:11 EDT |
