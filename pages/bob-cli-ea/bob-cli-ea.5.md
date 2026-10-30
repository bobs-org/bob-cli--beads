# Bead: bob-cli-ea.5 — Event fetch, inclusion rule, root precedence, and bob gcal list

[Bead Pages](../README.md) / [bob-cli-ea](README.md) / bob-cli-ea.5

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.2w.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.2w.linker.w0.md) · **Assignee:** `bob-cli-ea.5` · **Size:** medium
**Created:** 2026-10-29 19:40:04 EDT · **Closed:** 2026-10-30 00:22:34 EDT
**Plan:** [202610/bob\_gcal\_daily\_events.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/bob_gcal_daily_events.md)

## Description

gcal-list: fetch one DST-safe local day per calendar as a complete snapshot, normalize events, classify them as task, context, or omitted, choose and validate roots (route token, colour, calendar, default), and ship the read-only list as the bare default.

## Notes

[2026-10-30T04:22:34Z · bob-cli-ea.5--1] Implemented the gcal event snapshot, classification, root selection, read-only list, and pre-login guidance. Verified cargo test --lib native::gcal:: (21 passed), cargo test --test gcal_list --test gcal_cli (10 passed), just docs-gen, and just docs-check (all gates passed; 448 docs tests). epic-symbols reported none.

## Dependencies

- **Depends on:** [bob-cli-ea.4](bob-cli-ea.4.md) ✓ · ⧖ 2026-10-29
- **Blocks:** [bob-cli-ea.6](bob-cli-ea.6.md) ✓ · ⧖ 2026-10-29

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-ea.5](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-ea.5.md) | [bob-cli-ea.5](bob-cli-ea.5.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`44058f6`](https://github.com/bobs-org/bob-cli/commit/44058f67ee227e3de850e5294edc44da21b0b349) | feat(gcal): add calendar list command | [bob-cli-ea.5](bob-cli-ea.5.md) | 2026-10-30 00:25:23 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-ea.5--1][1] | Need the phase scope and design file | 3 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-ea.5.md

<!-- sase:referenced-by:end -->
