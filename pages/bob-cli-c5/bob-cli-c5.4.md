# Bead: bob-cli-c5.4 — Stats dash Root parents view and plugin rollup removal

[Bead Pages](../README.md) / [bob-cli-c5](README.md) / bob-cli-c5.4

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.145](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.145.md) · **Assignee:** `bob-cli-c5.4` · **Size:** medium
**Created:** 2026-10-25 10:27:23 EDT · **Closed:** 2026-10-25 12:00:54 EDT
**Plan:** [202610/day\_strip\_above\_badges\_root\_parents.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/day_strip_above_badges_root_parents.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| related | file:explicit:57074127d3acd69bb4cdc802 | attached via sase artifact create --bead |
| related | file:explicit:7f036f40df8f267226f1c12d | attached via sase artifact create --bead |
| related | file:explicit:845458523ab6dca13425c847 | attached via sase artifact create --bead |
| related | file:explicit:9709579771c9b3bb20a3e200 | attached via sase artifact create --bead |

<!-- sase:links:end -->

## Description

stats-roots: replace Areas & projects with a Root parents view grouped by area with sub-project disclosure, route the strip's hand-off to it, drop rollup from the JS home mirror, and refresh fixtures and previews.

## Notes

[2026-10-25T16:00:54Z · bob-cli-c5.4] stats-roots landed in bob-plugins working tree (uncommitted): Root parents default view with area groups, sub-project disclosure, bucket groups, Themes toggle, old-bob fallback, and openStatsForDay roots hand-off; JS rollup mirror removed and vectors synced to bob-cli 5078e8f82165; canonical.json regenerated (root_parent present, rev 5078e8f82165) and synthetic-homes* given root_parent parts/catalog; preview-stats-block zero-failure (4 PNGs attached) with a makeHtml $-escape fix; npm test 3667 pass, validate 7/7, docs:check pass; manifest bumped 1.70.0; bob plugins sync deployed

## Dependencies

- **Depends on:** [bob-cli-c5.2](bob-cli-c5.2.md) ✓ · ⧖ 2026-10-25
- **Depends on:** [bob-cli-c5.3](bob-cli-c5.3.md) ✓ · ⧖ 2026-10-25
- **Blocks:** [bob-cli-c5.5](bob-cli-c5.5.md) ◐ · ⧖ 2026-10-25

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-c5.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-c5.4/README.md) | [bob-cli-c5.4](bob-cli-c5.4.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@4150279`](https://github.com/bobs-org/bob-plugins/commit/41502791c5ab350415ac91a75c5adbfb3d23013e) | feat(ledger-tools): stats Root parents view with sub-project disclosure | [bob-cli-c5.4](bob-cli-c5.4.md) | 2026-10-25 12:02:50 EDT |
