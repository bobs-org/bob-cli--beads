# Bead: bob-cli-fl.2 — bob-cli: a session is off the clock iff every Task Link it keeps is #offclock

[Bead Pages](../README.md) / [bob-cli-fl](README.md) / bob-cli-fl.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase · **↺ Reopened:** ↺1
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.2z.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.2z.linker.w0.md) · **Assignee:** `bob-cli-fl.2` · **Size:** medium
**Created:** 2026-11-01 21:46:35 EST · **Closed:** 2026-11-02 02:49:31 EST
**Plan:** [202611/off\_clock\_pomodoros.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/off_clock_pomodoros.md)

## Previously Closed

> ↺ Closed 2026-11-02T06:57:20Z · done
>
> (none)
>
> Reopened 2026-11-02T07:10:56Z by `sase bead open`

## Description

off-clock-rule: stamp the clock key at every capture start, close, and running-lineup edit from the counted-links rule, explain mixed sessions, and pin it in shared pomodoro_clock vectors.

## Notes

[2026-11-02T06:57:20Z · bob-cli-fl.2] Stamped [t::]/[off::] from the counted-links rule at capture start, close, and running-lineup restamp. MEET start uses the event-run clock; mixed sessions stay Worked and emit pomodoro_clock_mixed. 13 pomodoro_clock vectors plus restart and link-start extras pass, including dry-run parity.

[2026-11-02T07:20:03Z · bob-cli-fl.2--1] Recovery: restamp dest refs now pin pre-state headlines so moves do not panic; source restamp uses the post-move line; non-MEET all-offclock lineups write [off::]; ST6 and unnamed-entry assertions accept stamped keys.

[2026-11-02T07:49:31Z · bob-cli-fl.2--2] Verified: capture start, close, and running-lineup edits stamp [t::]/[off::] from the counted-links rule; MEET starts use the event-run clock; mixed sessions stay Worked and emit pomodoro_clock_mixed; 13 pomodoro_clock vectors plus restart/link-start extras pass including dry-run parity; restamp dest refs pin pre-state headlines; sase tool run check ac7b5cec172700fd69dbc762006c5e18 succeeded; no leftover epic symbols.

## Dependencies

- **Depends on:** [bob-cli-fl.1](bob-cli-fl.1.md) ✓ · ⧖ 2026-11-01
- **Blocks:** [bob-cli-fl.5](bob-cli-fl.5.md) ✓ · ⧖ 2026-11-01
- **Blocks:** [bob-cli-fl.7](bob-cli-fl.7.md) ✓ · ⧖ 2026-11-01

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-fl.2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-fl.2.md) | [bob-cli-fl.2](bob-cli-fl.2.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`71a65da`](https://github.com/bobs-org/bob-cli/commit/71a65dad49413ba3662098834f01fbecda70fdd9) | feat(capture): stamp session clock from counted Task Links | [bob-cli-fl.2](bob-cli-fl.2.md) | 2026-11-02 02:51:13 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-fl.2--2][1] | Need the phase scope and design file | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-fl.2.md

<!-- sase:referenced-by:end -->
