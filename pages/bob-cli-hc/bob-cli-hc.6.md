# Bead: bob-cli-hc.6 — Dual-key love.md and body.md, then the cutover

[Bead Pages](../README.md) / [bob-cli-hc](README.md) / bob-cli-hc.6

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.3c.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.3c.linker.w0.md) · **Assignee:** `bob-cli-hc.6` · **Size:** small
**Created:** 2026-11-05 10:03:56 EST · **Closed:** 2026-11-05 12:37:09 EST
**Plan:** [202611/offclock\_types.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/offclock_types.md)

## Description

vault-migration: record the drift baseline, add a block-list `offclock_types: [MEET]` beside `offclock: true` in love.md and body.md, register the property as multitext, verify with a workspace-built bob, and then handle removing `offclock: true` as the cutover decision says.

## Notes

[2026-11-05T17:37:09Z · bob-cli-hc.6] Dual-key landed and verified. Baseline: clock_drift=1, no note_offclock lints. Added offclock_types:[MEET] under offclock:true in love.md and body.md, registered offclock_types:multitext in .obsidian/types.json (autosync committed; vault-sync status clean, local==remote). Workspace bob: stats shows note_offclock_shadowed for love.md+body.md, no note_offclock_invalid, drift still 1. Live dry-run @love:spotify=3 previews [t:: 15m]; scratch dual-key probe: MEET start previews [off:: 25m] with clock_note love.md, untyped previews [t:: 25m]. Re-scan: exactly 1 open love/body-rooted Event Task (Unami w/ Abby via abby), type MEET, no non-MEET strays. gcal list not verifiable here (no OAuth creds on this host). Cutover staged as gate custom-74557157 (cutover OR defer): guard aborts if installed bob predates offclock_types (confirmed current install sees no shadowed lint), if any non-MEET love/body event exists, then deletes the two offclock:true lines and expects drift unchanged and no shadowed lint. Do not remove offclock:true until Bryan confirms just install-all on athena, apollo, and Mac.

## Dependencies

- **Depends on:** [bob-cli-hc.2](bob-cli-hc.2.md) ✓ · ⧖ 2026-11-05
- **Depends on:** [bob-cli-hc.4](bob-cli-hc.4.md) ✓ · ⧖ 2026-11-05

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-hc.6](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-hc.6/README.md) | [bob-cli-hc.6](bob-cli-hc.6.md) | 0 |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-hc.land][1] | Need the child scope and notes | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-hc.land.md

<!-- sase:referenced-by:end -->
