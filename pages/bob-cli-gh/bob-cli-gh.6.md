# Bead: bob-cli-gh.6 — Period-note creation hook, open-week command, and agent callout style

[Bead Pages](../README.md) / [bob-cli-gh](README.md) / bob-cli-gh.6

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** `bbugyi200.apollo.research.34.linker.w0` · **Assignee:** `bob-cli-gh.6` · **Size:** small
**Created:** 2026-11-03 10:55:43 EST · **Closed:** 2026-11-03 12:39:22 EST
**Plan:** [202611/period\_notes\_and\_stats\_strips.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/period_notes_and_stats_strips.md)

## Description

hook: bob-ledger-tools runs `bob periods ensure` on daily-note creation and once per local day, gated on all_time.md; adds an "Open this week's note" command; and styles `[!agent]` callouts as one quiet folded line.

## Notes

[2026-11-03T17:39:14Z · bob-cli-gh.6] PROPOSED FOLLOW-UP: run the full bob-plugins npm test to completion (it exceeds a single-turn ceiling; the period-notes, gcal-events, plugin-build, startup-smoke, and docs suites all pass)

[2026-11-03T17:39:22Z · bob-cli-gh.6] Hook phase done in linked bob-plugins: 292b-plugin-period-notes fragment (adoption-gated ensure on daily-note create, once-daily layout-ready, 5s midnight tick; 15s spawn; older-bob warn once, lock_busy one retry, daily Notice; Open this week's note command), agent-callout quiet-line CSS, docs section, 12-test suite green, build/docs-check green, bob plugins sync deployed

## Dependencies

- **Depends on:** [bob-cli-gh.2](bob-cli-gh.2.md) ✓ · ⧖ 2026-11-03
- **Blocks:** [bob-cli-gh.9](bob-cli-gh.9.md) ✓ · ⧖ 2026-11-03

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-gh.6](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-gh.6/README.md) | [bob-cli-gh.6](bob-cli-gh.6.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@a56f0dc`](https://github.com/bobs-org/bob-plugins/commit/a56f0dc7bdd2158310874e021617df88855a6ace) | feat(ledger-tools): add period-notes hook ensuring period notes on daily-note creation | [bob-cli-gh.6](bob-cli-gh.6.md) | 2026-11-03 12:42:35 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-gh.6][1] | phase scope | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-gh.6/README.md

<!-- sase:referenced-by:end -->
