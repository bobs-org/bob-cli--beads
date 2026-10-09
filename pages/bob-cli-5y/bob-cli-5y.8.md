# Bead: bob-cli-5y.8 — Bob Mac Capture reads located ref tasks

[Bead Pages](../README.md) / [bob-cli-5y](README.md) / bob-cli-5y.8

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.0z0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.0z0.md) · **Assignee:** `bob-cli-5y.8` · **Size:** medium
**Created:** 2026-10-09 12:29:34 EDT · **Closed:** 2026-10-09 15:17:11 EDT
**Plan:** [202610/ref\_tasks\_live\_with\_parent.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/ref_tasks_live_with_parent.md)

## Description

mac-refs-v2: decode the task object, join Today on path and block ID, refresh on root-note changes, and show the book symbol for ref tasks in pickers and the inspector.

## Notes

[2026-10-09T19:16:43Z · bob-cli-5y.8] PROPOSED FOLLOW-UP: Add decisions strand ref-tasks-live-with-their-parent recording residence-is-parent, tag-plus-link identity, and Ready-only REFERENCES (epic memory_ref_parent_decision = no)

[2026-10-09T19:16:48Z · bob-cli-5y.8] PROPOSED FOLLOW-UP: Update glossary strands reference-task, reference-note, and area-note for the v2 parent-residence model (epic memory_glossary_ref_terms = no)

[2026-10-09T19:16:51Z · bob-cli-5y.8] PROPOSED FOLLOW-UP: master CI red on pre-existing CapturePanelView.swift:2449 type () cannot conform to View from bob-cli-5z.6 commits; mac-refs-v2 commit aa47c1f CI run 37978861414 fails identically at Build with lint passing and no errors in Refs/picker files

[2026-10-09T19:17:11Z · bob-cli-5y.8] mac-refs-v2 landed as aa47c1f on bob-mac-capture master: RefTask decode + plan block_id, (path,block_id) Today join with note-path fallback, root+done watcher, book symbol in ^ : + & ! pickers, inspector Reading task row, real-route v2 parent captions, README updates, refs-list-v2/refs-plan-v2 fixtures. Verified: swift build clean, all 935 Linux-runnable tests pass (RefsCore+CaptureCore incl. 15 new tests), swift-format lint passes on CI, epic-symbols clean. CI run 37978861414 fails only on the pre-existing CapturePanelView.swift:2449 error identical to the clean base (recorded as PROPOSED FOLLOW-UP); no errors in any touched file.

## Dependencies

- **Blocks:** [bob-cli-5y.12](bob-cli-5y.12.md) ◐ · ⧖ 2026-10-09
- **Blocks:** [bob-cli-5y.13](bob-cli-5y.13.md) ◐ · ⧖ 2026-10-09
- **Depends on:** [bob-cli-5y.5](bob-cli-5y.5.md) ✓ · ⧖ 2026-10-09

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-5y.8](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-5y.8/README.md) | [bob-cli-5y.8](bob-cli-5y.8.md) | 0 |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-5y.8][1] | Need the phase scope and design file | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-5y.8/README.md

<!-- sase:referenced-by:end -->
