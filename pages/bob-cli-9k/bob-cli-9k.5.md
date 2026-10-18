# Bead: bob-cli-9k.5 — Obsidian ledger home chips

[Bead Pages](../README.md) / [bob-cli-9k](README.md) / bob-cli-9k.5

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.research.4t.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.research.4t.linker.w0.md) · **Assignee:** `bob-cli-9k.5` · **Size:** medium
**Created:** 2026-10-18 16:35:49 EDT · **Closed:** 2026-10-18 17:50:49 EDT
**Plan:** [202610/pomodoro\_homes.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/pomodoro_homes.md)

## Description

ledger-chips: add a bob-ledger-tools JavaScript mirror of the resolver that runs the shared vectors verbatim. Draw quiet lowercase home chips on Pomodoro entry lines in Live Preview and Reading view, with the area-hue CSS tokens, the suppression rules, and a toggle. Then sync the plugins.

## Notes

[2026-10-18T21:50:33Z · bob-cli-9k.5] PROPOSED FOLLOW-UP: Repair six clean-base bob-plugins failures reproduced at 60148ab: the four Live Preview/Reading view unblocked-glyph tests, Keep counts once and saturates at 999 without reset, and forward conversion carries a Depends-On line and reverse restores it. Also stabilize the stage ranker timing check: it missed 16 ms once at 16.01 ms and passed unchanged on rerun at 10.83 ms. No open task bead matched unblocked, forward promotion, or stage ranker.

[2026-10-18T21:50:49Z · bob-cli-9k.5] Implemented and validated the pomodoro home resolver mirror, shared vectors, Live Preview and Reading view chips, hues, toggle, version/docs, and sync. Target tests and npm validate pass; plugin bundle matches the synced vault. Full suite's six functional failures reproduce on clean base 60148ab and the one timing miss passed unchanged on rerun; documented as PROPOSED FOLLOW-UP. No epic symbols remain.

## Dependencies

- **Depends on:** [bob-cli-9k.1](bob-cli-9k.1.md) ✓ · ⧖ 2026-10-18
- **Blocks:** [bob-cli-9k.6](bob-cli-9k.6.md) ◐ · ⧖ 2026-10-18

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-9k.5](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-9k.5/README.md) | [bob-cli-9k.5](bob-cli-9k.5.md) | 0 |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-9k.5][1] | Need to confirm the phase scope and design file before final validation | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-9k.5/README.md

<!-- sase:referenced-by:end -->
