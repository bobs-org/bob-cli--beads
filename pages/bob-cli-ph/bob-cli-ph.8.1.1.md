# Bead: bob-cli-ph.8.1.1 — Repair the drawer annotation build and cover the landed decoding

[Bead Pages](../README.md) / [bob-cli-ph.8.1](bob-cli-ph.8.1.md) / bob-cli-ph.8.1.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.bob-cli-ph.8](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-ph.8.md) · **Assignee:** `bob-cli-ph.8.1.1` · **Size:** small
**Created:** 2026-11-25 20:55:59 EST · **Closed:** 2026-11-25 22:42:09 EST
**Plan:** [202611/finish\_mac\_true\_case\_drawers.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/finish_mac_true_case_drawers.md)

## Description

annotation-build-repair: fix the CaptureDrawerSummary marker decode that broke Mac master at b45b1951, compile every target, and add portable coverage for the drawer annotation decoding and verbatim destination labels already landed.

## Notes

[2026-11-26T03:42:09Z · bob-cli-ph.8.1.1--4] Verified exact-SHA macOS CI run 45746741457 on snapshot a553cde880204896c52b106a4e7f5d7126593f passed, and portable-check on the same snapshot completed successfully on Athena (monitor 8e0x2eash6nn).

## Dependencies

- **Blocks:** [bob-cli-ph.8.1.2](bob-cli-ph.8.1.2.md) ◐ · ⧖ 2026-11-25
- **Blocks:** [bob-cli-ph.8.1.3](bob-cli-ph.8.1.3.md) ✓ · ⧖ 2026-11-25
- **Blocks:** [bob-cli-ph.8.1.6](bob-cli-ph.8.1.6.md) ◐ · ⧖ 2026-11-25

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-ph.8.1.1](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-ph.8.1.1.md) | [bob-cli-ph.8.1.1](bob-cli-ph.8.1.1.md) | 0 |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-ph.8.1.1--1][1] | Need phase scope, prior notes, and design file before continuing after CI failure | 2 |
| read-by | [agent:bob-cli-ph.8.1.1--4][1] | Inspect epic state and children before closing verified work | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-ph.8.1.1.md

<!-- sase:referenced-by:end -->
