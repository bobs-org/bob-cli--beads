# Bead: bob-cli-ji.7 — Bob Mac Capture Event note mode

[Bead Pages](../README.md) / [bob-cli-ji](README.md) / bob-cli-ji.7

**Status:** ✓ closed · **Resolution:** (unrecorded) · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.3z.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.3z.linker.w0.md) · **Assignee:** `bob-cli-ji.7` · **Size:** large
**Created:** 2026-11-10 05:59:46 EST
**Plan:** [202611/private\_gcal\_event\_notes.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/private_gcal_event_notes.md)

## Description

mac: in the bob-mac-capture linked repo, add an Event note mode to the capture panel: open it with a chord, the status menu, or a Calendar-band row; pick from upcoming events, edit with bob's highlight spans, and see a live hatched time rail with the 'lands as' preview. Save, clear, and undo, all through `bob gcal note -f json`, with docs, tests, and green exact-SHA macOS CI.

## Notes

[2026-11-11T03:01:37Z · bob-cli-ji.7.1.land--8] VERIFICATION: Parent phase mac deliverables are complete under child epic bob-cli-ji.7.1; its six implementation phases are closed, the child epic is closed, and dependencies bob-cli-ji.4/bob-cli-ji.6 are closed. Bob just check and Athena portable-check passed. Exact-SHA macOS run 42947559531 at c90a69df63207a130c17c7ff62a2287455a734ac passed formatting, Build, and the editor test; remaining failures are only tracked CaptureAliasTipPanelTests in bob-cli-jx. Plan 202611/mac_event_note_mode.md is marked done.  was attempted but no symvision recipe exists in the bob-cli or bob-mac-capture Justfile. Parent epic bob-cli-ji remains open.

[2026-11-11T03:02:16Z · bob-cli-ji.7.1.land--8] CLOSEOUT DETAIL: `just symvision` was attempted from the bob-cli workspace and returned “Justfile does not contain recipe symvision”; `just --list` confirmed the recipe is absent from both the bob-cli and bob-mac-capture Justfiles.

## Dependencies

- **Depends on:** [bob-cli-ji.4](bob-cli-ji.4.md) ✓ · ⧖ 2026-11-10
- **Depends on:** [bob-cli-ji.6](bob-cli-ji.6.md) ✓ · ⧖ 2026-11-10

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-ji.7](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-ji.7.md) | [bob-cli-ji.7](bob-cli-ji.7.md) | 0 |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-ji.7.1.land--1][1] | Verify approved epic and parent phase deliverables before closeout | 1 |
| read-by | [agent:bob-cli-ji.7.1.land--5][1] | Inspect parent phase scope and closeout requirements | 1 |
| read-by | [agent:research.40.cld][2] | Check phase progress and notes for guide accuracy | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-ji.7.1.land.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.research.40.cld/README.md

<!-- sase:referenced-by:end -->
