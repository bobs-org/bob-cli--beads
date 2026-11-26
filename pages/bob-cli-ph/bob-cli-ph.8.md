# Bead: bob-cli-ph.8 — Bob Mac Capture drawer rendering and typing

[Bead Pages](../README.md) / [bob-cli-ph](README.md) / bob-cli-ph.8

**Status:** ◐ in_progress · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.5x.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.5x.linker.w0.md) · **Assignee:** `bob-cli-ph.8` · **Size:** large
**Created:** 2026-11-22 17:36:49 EST
**Plan:** [202611/true\_case\_drawers.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/true_case_drawers.md)

## Description

mac-drawers: the Mac renders bob's drawer spans and preview annotations, dims the delimiters, drives the `*` assist through capture-rewrite, and stops uppercasing drawer titles.

## Notes

[2026-11-25T23:37:48Z · bob-cli-ph.8] Planning only: verified prerequisite bob-cli-ph.6 is closed and its Rust drawer contracts are present. Mac fc0d4551 still needs preview drawer annotation plumbing, title/delimiter styling, physical-star and span-driven typing assists, and removal of drawer uppercasing in transfer/merge presentations. Existing menu and sub-bullet title preservation is retained. Authored a medium tale covering implementation, fixtures, docs, and exact-SHA macOS verification; strict validation passed with zero warnings. No product source changed and no implementation attempted in this planning turn. Submitting through sase plan propose; keep this phase assigned until implementation and verification finish.

[2026-11-25T23:37:57Z · bob-cli-ph.8] PROPOSED FOLLOW-UP: Installed SASE lacks the documented on-demand roster selector — sase memory read roster:decisions -r ... exits with unknown memory web: roster on this host; sase memory read --help documents only flat/web/strand forms. Used sase memory web show decisions plus audited governing strand reads for this plan. Land agent should triage the runtime/instructions mismatch.

## Dependencies

- **Blocks:** [bob-cli-ph.11](bob-cli-ph.11.md) ◐ · ⧖ 2026-11-22
- **Depends on:** [bob-cli-ph.6](bob-cli-ph.6.md) ✓ · ⧖ 2026-11-22
- **Blocks:** [bob-cli-pq.5](../bob-cli-pq/bob-cli-pq.5.md) ✓ · ⧖ 2026-11-23

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-ph.8](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-ph.8.md) | [bob-cli-ph.8](bob-cli-ph.8.md) | 0 |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:1fk][1] | Research whether pq.3/pq.5 truly depend on bob-cli-ph | 1 |
| read-by | [agent:bob-cli-pq.1][2] | sequencing check for glyph-contract | 2 |
| read-by | [agent:bob-cli-pq.3][3] | Check prerequisite Mac drawer implementation status | 1 |
| read-by | [agent:g1][4] | Check whether phase is blocked on the release gate | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.1fk/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-pq.1/README.md
[3]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-pq.3/README.md
[4]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.g1/README.md

<!-- sase:referenced-by:end -->
