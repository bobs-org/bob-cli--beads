# Bead: bob-cli-gb.6 — bob-plugins: spelling tables, offclock: inheritance in Obsidian starts and closes, copied vectors

[Bead Pages](../README.md) / [bob-cli-gb](README.md) / bob-cli-gb.6

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase · **↺ Reopened:** ↺1
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.31.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.31.linker.w0.md) · **Assignee:** `bob-cli-gb.6` · **Size:** medium
**Created:** 2026-11-02 17:38:45 EST · **Closed:** 2026-11-02 22:31:41 EST
**Plan:** [202611/off\_on\_tags\_and\_offclock\_areas.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/off_on_tags_and_offclock_areas.md)

## Previously Closed

> ↺ Closed 2026-11-03T03:03:25Z · done
>
> (none)
>
> Reopened 2026-11-03T03:12:32Z by `sase bead open`

## Description

plugins-clock: one spelling table per plugin, #on wins, the ledger-tools chain walker reads offclock: and exports taskEffectiveOffClock, se<X> starts and the cycler close use it with a tag-only fallback, and vectors are copied byte-for-byte.

## Notes

[2026-11-03T03:03:25Z · bob-cli-gb.6] Implemented shared #off/#on clock parsing, inherited area/project offclock defaults for starts and closes, and tag-only fallback; refreshed copied vectors. Verified npm build, build:check, 112 focused tests, clean diff check, byte-identical vectors, and both plugins synced up to date.

[2026-11-03T03:31:17Z · bob-cli-gb.6] PROPOSED FOLLOW-UP: npm test has 6 failures that reproduce identically on clean bob-plugins HEAD — Chromium-missing command-mode DOM, freshness reload event, note-ready startup storm, relationIndex layout-ready timeout, Pending future-schedule still [/], and cycler relation-successor vectors not byte-identical to bob-cli. Reduced-motion CSS test is flaky (failed on this tree, passed on HEAD).

[2026-11-03T03:31:41Z · bob-cli-gb.6] Wired se<X> starts to taskEffectiveOffClock, exported {offClock,source,notePath} on api.pomodoroClock v1, cycler close consumes the object with tag-only fallback, copied pomodoro_clock and meet_event_run vectors byte-for-byte, and documented #off/#on/offclock inheritance. Verified npm run build, build:check, validate, docs:check, 154 focused clock/lifecycle tests, identical vectors, and bob plugins sync of ledger-tools and cycler. Full npm test still has 6 failures that reproduce on clean HEAD (noted as PROPOSED FOLLOW-UP).

## Dependencies

- **Depends on:** [bob-cli-gb.2](bob-cli-gb.2.md) ✓ · ⧖ 2026-11-02
- **Blocks:** [bob-cli-gb.7](bob-cli-gb.7.md) ◐ · ⧖ 2026-11-02

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-gb.6](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-gb.6/README.md) | [bob-cli-gb.6](bob-cli-gb.6.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@2f172a2`](https://github.com/bobs-org/bob-plugins/commit/2f172a2403c79af47823574fb739e44c9686080b) | feat(clock): inherit offclock defaults on starts and closes | [bob-cli-gb.6](bob-cli-gb.6.md) | 2026-11-02 22:34:28 EST |
