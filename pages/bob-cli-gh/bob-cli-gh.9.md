# Bead: bob-cli-gh.9 — Vault rollout, review rituals, and live verification

[Bead Pages](../README.md) / [bob-cli-gh](README.md) / bob-cli-gh.9

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** `bbugyi200.apollo.research.34.linker.w0` · **Assignee:** `bob-cli-gh.9` · **Size:** medium
**Created:** 2026-11-03 10:55:44 EST · **Closed:** 2026-11-03 16:12:22 EST
**Plan:** [202611/period\_notes\_and\_stats\_strips.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/period_notes_and_stats_strips.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| related | file:explicit:0eb5faa755b31caa853c49a2 | attached via sase artifact create --bead |
| related | file:explicit:1261514f8af75fb6d3de1e5b | attached via sase artifact create --bead |
| related | file:explicit:2a14d7d4a1b924604abc5827 | attached via sase artifact create --bead |
| related | file:explicit:3278eb434e5bc6c6e04ff470 | attached via sase artifact create --bead |
| related | file:explicit:6e0694c95f9b5ce46b434ef3 | attached via sase artifact create --bead |
| related | file:explicit:a35e5184764ca1952d37e1b2 | attached via sase artifact create --bead |
| related | file:explicit:d25e89e172d5c77b6d78e57d | attached via sase artifact create --bead |

_Plus 2 automatic references — see [Referenced By](#referenced-by)._

<!-- sase:links:end -->

## Description

rollout: install bob and the plugins, verify the recurrence strings, run the migration dry run and then apply it, switch the daily template, retire the monthly and yearly templates, update day.md, journal.md, org.md, and gtd_daily.md, pilot drafts, capture screenshots, and file the automation follow-up.

## Notes

[2026-11-03T21:11:44Z · bob-cli-gh.9] PROPOSED FOLLOW-UP: athena Monday job auto-drafts closed weeks with empty Review plus quarters on quarter starts and the year on the second Monday of January, enabled only after four pilot weeks with >=50% of drafts kept or edited

[2026-11-03T21:11:49Z · bob-cli-gh.9] PROPOSED FOLLOW-UP: opt-in backfill migration of 2023-2025 dailies via bob periods migrate -s 2023-01-02

[2026-11-03T21:11:57Z · bob-cli-gh.9] PROPOSED FOLLOW-UP: v1 agent callouts say `bob periods brief <id> -f md` but the CLI only accepts human|json (help example also shows -f md); fix the flag or the callouts with an INSTRUCTIONS_VERSION bump

[2026-11-03T21:12:01Z · bob-cli-gh.9] PROPOSED FOLLOW-UP: plugins npm run docs:check with default bob-cli resolution builds the docs-cache clone at b94eec2 which does not compile (missing note_pull at plan.rs:2019); passes with BOB_CLI_DIR pointed at a fixed tree

[2026-11-03T21:12:22Z · bob-cli-gh.9] Rollout landed and verified. Migrate applied as ff499d8 (51 creates, 1 adoption, 2 reparents, 298 rewrites, parity verify green); list -p shows zero dangling_daily_parent and zero missing_period_note for ISO 2026 (only expected unscaffolded/stale-instructions info rows on out-of-range 2024/2025.md); ensure is a no-op. Recurrence strings verified on both engines: rrule 2.8.1 scratch gives quarterly 04-05/07-05/10-04/2028-01-03 and yearly 2028-01-10; bob parses both rows and walks them in RECURRING on their scheduled dates. Hand edits committed (daily template to GGGG week parents + week nav, monthly/yearly templates deleted, day/journal/org/gtd_daily updated); weekly/quarterly/yearly rows walk due on 11-09/2027-01-04/2027-01-11. Live strips rendered from live JSON and eyeballed (W45 so-far 7h40m = 3h35m + 4h05m, 14-week Q4, 53-week year with hatched pre-ledger columns, all_time quarters by year, W46 Starts line, W01 hatched); 7 PNGs stored as artifacts; heights within budget. Pilot drafts committed singly: W44 (143w, headline shipped) and Q3 (199w, headline shipped), both state drafted. Mac steps + Bryan tasks (^wqy-stat-strips, ^prev-next-links) in report. NOTE: workspace holds an uncommitted 2-file fix the land agent must review/commit: duplicate note_pull removal in capture/plan.rs (master HEAD did not compile) plus migrate.rs parent-line insertion for 4 parentless dailies with a regression test; full cargo test, clippy, fmt, just docs-check, and plugins docs:check (via BOB_CLI_DIR) all green.

## Dependencies

- **Depends on:** [bob-cli-gh.1](bob-cli-gh.1.md) ✓ · ⧖ 2026-11-03
- **Depends on:** [bob-cli-gh.4](bob-cli-gh.4.md) ✓ · ⧖ 2026-11-03
- **Depends on:** [bob-cli-gh.5](bob-cli-gh.5.md) ✓ · ⧖ 2026-11-03
- **Depends on:** [bob-cli-gh.6](bob-cli-gh.6.md) ✓ · ⧖ 2026-11-03
- **Depends on:** [bob-cli-gh.8](bob-cli-gh.8.md) ✓ · ⧖ 2026-11-03

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-gh.9](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-gh.9/README.md) | [bob-cli-gh.9](bob-cli-gh.9.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`7de57d0`](https://github.com/bobs-org/bob-cli/commit/7de57d04abb5e53439b75b02563750f740d4d030) | fix(periods): insert missing daily parent on migrate; drop duplicate note\_pull field | [bob-cli-gh.9](bob-cli-gh.9.md) | 2026-11-03 16:14:05 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-gh.9][1] | Need the phase scope and design file | 2 |
| read-by | [agent:bob-cli-gh.land][2] | Need the child scope and notes | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-gh.9/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-gh.land/README.md

<!-- sase:referenced-by:end -->
