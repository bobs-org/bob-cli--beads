# Bead: bob-cli-6l.4 — Obsidian Stats page — data path, tiles, and table

[Bead Pages](../README.md) / [bob-cli-6l](README.md) / bob-cli-6l.4

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.0u.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.research.0u.linker.w0/README.md) · **Assignee:** `bob-cli-6l.4` · **Size:** medium
**Created:** 2026-10-11 07:01:05 EDT · **Closed:** 2026-10-11 14:04:27 EDT
**Plan:** [202610/daily\_stats.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/daily_stats.md)

## Description

page: bob-ledger-tools api.stats v2 spawns bob stats with stale-while-revalidate caching, the bob-stats block renders the header, range controls, tile row, table view, and every honest state; the vault gains dash_stats.md, the dash entry point, the weekly-prune link, and Open Stats.

## Notes

[2026-10-11T18:04:09Z · bob-cli-6l.4] PROPOSED FOLLOW-UP: 18 plugin-suite failures (unblocked-glyph, roll-decay, successor-polish/wiring) reproduce identically on the clean base tree — date-sensitive, unrelated to the Stats page

[2026-10-11T18:04:14Z · bob-cli-6l.4] PROPOSED FOLLOW-UP: installed ~/.cargo/bin/bob on this machine predates `bob stats`; rollout (.6) must `just install` before opening Stats in Obsidian or the block shows bob-not-found

[2026-10-11T18:04:27Z · bob-cli-6l.4] Page phase done: api.stats v2 (fetch/bobPath, SWR LRU-8 cache, one flight + one coalesced follow-up, 20s spawn with BOB_DIR/NO_COLOR) in 236; bob-stats block (header chips/Custom/popover/offset/compare/table, tile row with selected focus, table + Copy CSV, footer provenance/warnings, skeleton/revalidating/error-card honest states, Open Stats command) in 237/238; palette CSS; dash_stats.md + weekly-prune link + label-only STATS chip in dash Browse row + docs/dashboard.md (stats_chip=yes). Verified: npm build+build:check+validate clean, 28/28 stats tests pass (data/block/journal/review-journal), plugin synced to vault (54 refs in deployed main.js), real argv smoke  returns schema-1/11 metrics, bob-cli fmt clean (docs-only change). 18 unrelated suite failures reproduce identically on clean base (recorded as follow-up); no epic-symbols. Focus chart/panels/interaction left to .5; Obsidian visual check left to .6 rollout.

## Dependencies

- **Depends on:** [bob-cli-6l.3](bob-cli-6l.3.md) ✓ · ⧖ 2026-10-11
- **Blocks:** [bob-cli-6l.5](bob-cli-6l.5.md) ◐ · ⧖ 2026-10-11

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-6l.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-6l.4/README.md) | [bob-cli-6l.4](bob-cli-6l.4.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`f74f3ad`](https://github.com/bobs-org/bob-cli/commit/f74f3ad305e5ecee85eef35312af918d60c6070b) | feat(stats): document the Stats child page and Browse chip | [bob-cli-6l.4](bob-cli-6l.4.md) | 2026-10-11 14:05:58 EDT |
