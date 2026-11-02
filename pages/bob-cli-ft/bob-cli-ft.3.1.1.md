# Bead: bob-cli-ft.3.1.1 — Shared blocked checkbox paint, miniature API, and contrast

[Bead Pages](../README.md) / [bob-cli-ft.3.1](bob-cli-ft.3.1.md) / bob-cli-ft.3.1.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-ft.3](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-ft.3.md) · **Assignee:** `bob-cli-ft.3.1.1` · **Size:** medium
**Created:** 2026-11-02 07:34:44 EST · **Closed:** 2026-11-02 07:59:43 EST
**Plan:** [202611/block\_marks\_editor.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/block_marks_editor.md)

## Description

paint_api: implement the gated held/waiting/stale CSS, glyphs and pip, listener-free api.blockMarks.render, and computed contrast tests. Record measured tokens and geometry in the contract. No editor or reading-view decorations yet.

## Notes

[2026-11-02T12:55:41Z · bob-cli-ft.3.1.1] PROPOSED FOLLOW-UP: 5 npm-test failures reproduce identically on clean base 33318e0 and are pre-existing, tracked by bob-cli-et (freshness-namespace reload event), bob-cli-f7 (keep-inbox forced check), bob-cli-eh (note-ready startup storm, relation-index startup replay), bob-cli-ff (schedule-work-log future Pending); excluded from paint_api completion

[2026-11-02T12:59:43Z · bob-cli-ft.3.1.1] paint_api done: api.blockMarks.render (listener-free span.bob-block-mark, both aria modes, pip, synthetic digit models, foreign ownerDocument) plus gated held/waiting/stale CSS (chevron M4 10.25 8 6.25l4 4 w2.1, repeat-mask reuse, 6px pip + 1.5px ring, 120ms/reduced-motion). Verified: 20 focused tests pass (contrast + classifier), build:check + validate + docs:check + just docs-check green, full npm test 5016/5023 with only 5 pre-existing failures reproducing identically on clean base 33318e0 (tracked: bob-cli-et/f7/eh/ff). Contrast: waiting P1-P4 4.87-5.83 and white-on-held 4.52 both themes (held darkened 4%/14%, ramp unchanged); recorded in docs/blocked-marks.md. Manifest 1.87.0, deployed to vault via bob plugins sync from this workspace. No editor/reading decorations (owned by 3.1.2/3.1.3).

## Dependencies

- **Blocks:** [bob-cli-ft.3.1.2](bob-cli-ft.3.1.2.md) ◐ · ⧖ 2026-11-02

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-ft.3.1.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-ft.3.1.1/README.md) | [bob-cli-ft.3.1.1](bob-cli-ft.3.1.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`311b151`](https://github.com/bobs-org/bob-cli/commit/311b15142f23f3fcbdfaed97db8ce17a692e5880) | docs(blocked-marks): record paint\_api calibration, tokens, and render contract | [bob-cli-ft.3.1.1](bob-cli-ft.3.1.1.md) | 2026-11-02 08:01:37 EST |
