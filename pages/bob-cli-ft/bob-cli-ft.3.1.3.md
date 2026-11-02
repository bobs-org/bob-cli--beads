# Bead: bob-cli-ft.3.1.3 — Reading view, embeds, hover previews, and Dataview task marks

[Bead Pages](../README.md) / [bob-cli-ft.3.1](bob-cli-ft.3.1.md) / bob-cli-ft.3.1.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-ft.3](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-ft.3.md) · **Assignee:** `bob-cli-ft.3.1.3` · **Size:** medium
**Created:** 2026-11-02 07:34:44 EST · **Closed:** 2026-11-02 08:55:52 EST
**Plan:** [202611/block\_marks\_editor.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/block_marks_editor.md)

## Description

rendered_views: map rendered task rows to canonical source text or a conservative own-text fallback; classify and refresh the row and its own checkbox in place. Cover nested rows, query origins, cleanup, and both toggle directions with DOM tests.

## Notes

[2026-11-02T13:55:04Z · bob-cli-ft.3.1.3] PROPOSED FOLLOW-UP: Pre-existing npm test failure on clean base — scripts/test-ledger-tools-keep-inbox.cjs:990 "forced check feedback follows the bob refresh result" actual "try after 12:30" vs expected 16:30; tracked by bob-cli-f7

[2026-11-02T13:55:06Z · bob-cli-ft.3.1.3] PROPOSED FOLLOW-UP: Pre-existing npm test failure on clean base — scripts/test-navigation-hotkeys-schedule-work-log.cjs:145 "future scheduling on Pending marks Blocked but still writes the Work Log" fixture pins scheduled:: 2026-11-02 and still has [/] instead of [?]; tracked by bob-cli-ff

[2026-11-02T13:55:07Z · bob-cli-ft.3.1.3] PROPOSED FOLLOW-UP: Pre-existing npm test failure on clean base — scripts/test-ledger-tools-note-ready.cjs:1149 "the startup storm is linear" 1 !== 2 scans, and scripts/test-ledger-tools-relation-index.cjs:258 relationIndex waitUntil timeout; both tracked by bob-cli-eh

[2026-11-02T13:55:07Z · bob-cli-ft.3.1.3] PROPOSED FOLLOW-UP: Pre-existing npm test failure on clean base — scripts/test-ledger-tools-freshness-namespace.cjs:295 "the reload event fires only when the due key set changes" expected Tasks reload event, got []; tracked by bob-cli-et

[2026-11-02T13:55:52Z · bob-cli-ft.3.1.3] rendered_views landed in bob-plugins: 142g mixin at processor order 40 maps Reading/embed/hover/Dataview rows via section text then retained canonical then conservative own-text fallback; skips Tasks; query origins use taskThemeOriginFromContext; hosts restore on toggle/unload. 25 DOM tests pass (families, nested, Dataview origin, Tasks skip, toggle both ways, cleanup). ledger-tools 1.89.0 deployed. 5 full-suite failures reproduce on clean base and are recorded as PROPOSED FOLLOW-UP citing bob-cli-et, bob-cli-f7, bob-cli-eh, bob-cli-ff. No epic-symbol leftovers. DECISIONS own_first/chevron/quiet honored; no memory edits.

## Dependencies

- **Depends on:** [bob-cli-ft.3.1.2](bob-cli-ft.3.1.2.md) ✓ · ⧖ 2026-11-02
- **Blocks:** [bob-cli-ft.3.1.4](bob-cli-ft.3.1.4.md) ✓ · ⧖ 2026-11-02

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-ft.3.1.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-ft.3.1.3/README.md) | [bob-cli-ft.3.1.3](bob-cli-ft.3.1.3.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@5f1c23c`](https://github.com/bobs-org/bob-plugins/commit/5f1c23cfe98868561c9f2fe835ba5d0d28964e6a) | feat(plugins): add Reading-view blocked mark lifecycle | [bob-cli-ft.3.1.3](bob-cli-ft.3.1.3.md) | 2026-11-02 08:57:23 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-ft.3.1.3][1] | Need notes, DECISIONS, and remaining work before close | 8 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-ft.3.1.3/README.md

<!-- sase:referenced-by:end -->
