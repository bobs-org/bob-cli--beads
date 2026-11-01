# Bead: bob-cli-f5.2 — Live Preview rings, resolver, refresh, and toggle

[Bead Pages](../README.md) / [bob-cli-f5](README.md) / bob-cli-f5.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.16q](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.16q.md) · **Assignee:** `bob-cli-f5.2` · **Size:** medium
**Created:** 2026-11-01 09:24:20 EST · **Closed:** 2026-11-01 10:10:14 EST
**Plan:** [202611/task\_link\_marks.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/task_link_marks.md)

## Description

live_preview: add the target resolver (live doc, then Tasks memo, then metadata cache), the CM6 widget extension, click handling, the swap animation, refresh plumbing, and the session toggle, with vector-driven and performance tests.

## Notes

[2026-11-01T15:10:02Z · bob-cli-f5.2] PROPOSED FOLLOW-UP: five bob-plugins tests fail identically on the clean base — keep-inbox "forced check feedback follows the bob refresh result" (timezone-dependent: expects 16:30, gets 12:30), relation-index "registers after layout-ready and never reads non-markdown during startup replay" and "the startup storm is linear", gcal-events "create listener runs once for today's note after layout readiness", and note-ready/freshness-namespace "the reload event fires only when the due key set changes" — make them timezone- and timing-independent so npm test is green

[2026-11-01T15:10:14Z · bob-cli-f5.2] Live Preview rings landed in bob-plugins (bob-ledger-tools): 149-task-link-mark-live-model.js (live-doc model, swap bookkeeping, shared ring host buildTaskLinkMarkElement, TaskLinkMarkWidget), 284-plugin-task-link-marks.js (BobLedgerToolsTaskLinkMarksMixin: CM6 extension, toggle, coalesced scheduleTaskLinkMarksRefresh, listeners, setupMarkFamilies so 170-plugin-lifecycle.js shrank to 994 lines), 284a-plugin-task-link-marks-resolve.js (taskLinkMarkResolve: live doc, Tasks memo, metadata cache). dependencyTasksIndex now records duplicate keys (dependencyTasksDuplicateKeys); scheduleLiveWidgetRefresh fans out to the new refresh; styles.css swap selector fixed to .bob-task-link-mark.bob-task-link-mark-swap (f5.1 had a data-state selector that could never match). Decisions honored: ledger_rows=skip, dim_closed_links=no. Verified: new scripts/test-ledger-tools-task-link-marks-live.cjs (36 tests: TC/TR/TT vectors through the builder, three sources + precedence, toggle, refresh coalescing, swap rule, ring-last ordering pin, click rules, perf: warm viewport ~6ms, keystroke ~6ms, 2000 links ~16ms) passes and is in package.json; npm run build, npm run validate and just docs-check pass; npm test has exactly 5 failures that reproduce identically on the clean base (recorded as PROPOSED FOLLOW-UP). bob plugins sync deployed bob-ledger-tools with -F after confirming every line of the stale uncommitted vault build exists in HEAD; vault carries toggle-task-link-marks. Hand-off for f5.3 (reading): setupTaskLinkMarks calls this.setupTaskLinkMarksReading() and runTaskLinkMarksRefresh calls this.sweepTaskLinkMarksReading() when those methods exist; reuse buildTaskLinkMarkElement(doc,{state,tooltip,swap}) and taskLinkMarkResolve({linkpath,blockId,sourcePath}) with no liveDoc. Contract docs/task-link-marks.md updated with the two new fragment names and swap class.

## Dependencies

- **Depends on:** [bob-cli-f5.1](bob-cli-f5.1.md) ✓ · ⧖ 2026-11-01
- **Blocks:** [bob-cli-f5.3](bob-cli-f5.3.md) ✓ · ⧖ 2026-11-01

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-f5.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-f5.2/README.md) | [bob-cli-f5.2](bob-cli-f5.2.md) | 2 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`4ea4c33`](https://github.com/bobs-org/bob-cli/commit/4ea4c330df72b32c20bb91ec4a5440f8edab6a72) | docs(task-link-marks): name the Live Preview fragments and swap class | [bob-cli-f5.2](bob-cli-f5.2.md) | 2026-11-01 10:11:12 EST |
| bob-plugins | [`bob-plugins@13d40ac`](https://github.com/bobs-org/bob-plugins/commit/13d40ac4ec851f0f60cae581a21d581157fc0d07) | feat(task-link-marks): Live Preview rings, resolver, refresh, and toggle | [bob-cli-f5.2](bob-cli-f5.2.md) | 2026-11-01 10:11:28 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-f5.2][1] | Need the phase scope and design file | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-f5.2/README.md

<!-- sase:referenced-by:end -->
