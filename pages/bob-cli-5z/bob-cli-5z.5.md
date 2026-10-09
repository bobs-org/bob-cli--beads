# Bead: bob-cli-5z.5 — Bob Mac Capture restart and swap preview, footer, and notifications

[Bead Pages](../README.md) / [bob-cli-5z](README.md) / bob-cli-5z.5

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.61.w1.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.61.w1.w0.md) · **Assignee:** `bob-cli-5z.5` · **Size:** medium
**Created:** 2026-10-09 13:24:48 EDT · **Closed:** 2026-10-09 14:57:19 EDT
**Plan:** [202610/pomodoro\_override.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/pomodoro_override.md)

## Description

mac-override-card: decode the parse flag and `pomodoro_start.override`, extend the start presentation with restart/swap/idle variants, render the before→after and demoted rows on the start card, retitle the footer and notifications, and add real-bob fixtures, tests, and README rows.

## Notes

[2026-10-09T18:56:59Z · bob-cli-5z.5] Swift verification pending macOS CI: no Swift toolchain on agent host, so swift-format/build/test could not run here. Verified instead: 7 real-bob fixtures from swap-phase bob (BOB_NOW=2026-10-09 09:32:00 worked-example vault), fake-bob routes execute (bash -n + live draft probes for ==, ==#bugs, ==3#plan, ==#), every new presentation string reproduced exactly by an independent Python simulation of the Swift init, all touched Swift files re-read, brace-balance clean (one mismatch pre-exists on base), epic-symbols clean.

[2026-10-09T18:57:19Z · bob-cli-5z.5] mac-override-card done: override decode (spec flag + tolerant summary outcome, unknown action->plain start), restart/swap/idle presentation variants driving card/footer/notifications, 7 real-bob fixtures + fake-bob routes (probed live), 8 presentation + 5 panel-model + 3 notification tests added, README rows updated. Verified: fixture JSON from swap-phase bob, fake-bob execution, independent string simulation matching all expectations, full file re-reads, epic-symbols clean. Swift build/test pending macOS CI (no toolchain on host; noted on bead).

## Dependencies

- **Depends on:** [bob-cli-5z.3](bob-cli-5z.3.md) ✓ · ⧖ 2026-10-09
- **Blocks:** [bob-cli-5z.6](bob-cli-5z.6.md) ✓ · ⧖ 2026-10-09

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-5z.5](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-5z.5/README.md) | [bob-cli-5z.5](bob-cli-5z.5.md) | 0 |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-5z.5][1] | Need the phase scope and design file | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-5z.5/README.md

<!-- sase:referenced-by:end -->
