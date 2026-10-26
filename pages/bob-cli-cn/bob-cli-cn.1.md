# Bead: bob-cli-cn.1 — bob stats — additive \`typical\` object on day-grouped count and minutes points

[Bead Pages](../README.md) / [bob-cli-cn](README.md) / bob-cli-cn.1

**Status:** ◐ in_progress · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.research.5d.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.research.5d.linker.w0.md) · **Assignee:** `bob-cli-cn.1` · **Size:** medium
**Created:** 2026-10-26 13:12:28 EDT
**Plan:** [202610/day\_strip\_typical\_day.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/day_strip_typical_day.md)

## Description

typical-field: in bob-cli, add the optional `typical` object (window D−7…D−1, median, ≥4 usable days, relation, words, detail) to current day-grouped `points` of count and minutes metrics. Share the usable-value rule with rolling medians and extend the Day lead-in from 6 to 7 days. Cover it with hand-derived unit and golden tests, document the schema-1 field in docs/stats.md, and check parity read-only on the live vault.

## Dependencies

- **Blocks:** [bob-cli-cn.2](bob-cli-cn.2.md) ◐ · ⧖ 2026-10-26

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-cn.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-cn.1/README.md) | [bob-cli-cn.1](bob-cli-cn.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`3f41764`](https://github.com/bobs-org/bob-cli/commit/3f417646f1c65db71ea86106906a0184b5908b03) | feat(stats): add typical day to daily points | [bob-cli-cn.1](bob-cli-cn.1.md) | 2026-10-26 14:00:55 EDT |
