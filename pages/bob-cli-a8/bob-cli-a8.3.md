# Bead: bob-cli-a8.3 — Refs show, keystroke, ranking, and refresh optimizations

[Bead Pages](../README.md) / [bob-cli-a8](README.md) / bob-cli-a8.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** `bbugyi200.apollo.9q` · **Assignee:** `bob-cli-a8.3` · **Size:** medium
**Created:** 2026-10-20 15:55:14 EDT · **Closed:** 2026-10-20 18:35:04 EDT
**Plan:** [202610/mac\_capture\_panel\_switch\_and\_perf.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/mac_capture_panel_switch_and_perf.md)

## Description

refs_perf: drop the unread published row rect, cache the filter field, coalesce library-publish passes, skip unchanged inspector and Today republishes, precompute ranking sort keys, fix the stale prepared-item cache, and coalesce the panel-open Today refresh.

## Notes

[2026-10-20T22:35:04Z · bob-cli-a8.3--1] Verified: just portable-check passed (1,473 tests, 0 failures) and just docs-check passed (447 passed, 1 skipped; all implemented gates green). macOS bundle/typecheck targets remain unverified because the Mac SSH attempt timed out. epic-symbol check: no remaining entries.

## Dependencies

- **Depends on:** [bob-cli-a8.1](bob-cli-a8.1.md) ✓ · ⧖ 2026-10-20

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-a8.3](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-a8.3.md) | [bob-cli-a8.3](bob-cli-a8.3.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-mac-capture | [`bob-mac-capture@554c69e`](https://github.com/bobs-org/bob-mac-capture/commit/554c69eee19b5be1d0a7ce687dac04b40227d0f3) | perf(refs): optimize ranking and refresh paths | [bob-cli-a8.3](bob-cli-a8.3.md) | 2026-10-20 18:35:32 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-a8.3--1][1] | Need the complete phase design reference and notes before closure | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-a8.3.md

<!-- sase:referenced-by:end -->
