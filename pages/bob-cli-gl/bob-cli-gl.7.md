# Bead: bob-cli-gl.7 — Bob Mac Capture moves band, ghost titles, move hint, offers label, and notification

[Bead Pages](../README.md) / [bob-cli-gl](README.md) / bob-cli-gl.7

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.35.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.35.linker.w0.md) · **Assignee:** `bob-cli-gl.7` · **Size:** medium
**Created:** 2026-11-03 13:39:31 EST · **Closed:** 2026-11-03 22:07:55 EST
**Plan:** [202611/capture\_move\_bullets.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/capture_move_bullets.md)

## Description

mac-preview: In bob-mac-capture, decode `project_note.moved_tasks`, the move summary, the move hint, and offer `moved_from`. Render the "Moves N tasks from cash.md" preview band, inline ghost titles after each move bullet, the discoverability hint, the "moved from" label on Pull-In rows, the notification copy, and VoiceOver labels. Update the docs and fixtures.

## Notes

[2026-11-04T03:02:26Z · bob-cli-gl.7] PROPOSED FOLLOW-UP: docs-check generated-drift stage fails on sase/memory/glossary/task-merge.md (no front matter); reproduces identically on pristine mac HEAD, unrelated to mac-preview docs work

[2026-11-04T03:07:55Z · bob-cli-gl.7] mac-preview done: tolerant decode of moved_tasks/move_summary/repaired_files/move_hint/moved_from; moves band above Links/Offers with repair footer and VoiceOver summary; ghost titles with byte-range anchors and draft-equality staleness; move hint line; moved-from Pull-In labels; Created/move-count notification. Verified: 15 new CaptureCore tests + full portable suite 2087 tests 0 failures on athena; docs lint ok (budgets 5992/5997); new MV1/MV4/MV5/MV17 real-bob fixtures. macOS-only targets (view/model/notification/choice UI) parse-clean but unverified: mac offline, no Xcode here.

## Dependencies

- **Depends on:** [bob-cli-gl.5](bob-cli-gl.5.md) ✓ · ⧖ 2026-11-03
- **Depends on:** [bob-cli-gl.6](bob-cli-gl.6.md) ✓ · ⧖ 2026-11-03

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-gl.7](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-gl.7/README.md) | [bob-cli-gl.7](bob-cli-gl.7.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-mac-capture | [`bob-mac-capture@2940666`](https://github.com/bobs-org/bob-mac-capture/commit/2940666a76e65545bb3416bced36dd4f1f5c9b67) | feat(capture): preview project-note moves with band, ghosts, hint, and notification | [bob-cli-gl.7](bob-cli-gl.7.md) | 2026-11-03 22:09:53 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-gl.7][1] | Need the phase scope and design file | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-gl.7/README.md

<!-- sase:referenced-by:end -->
