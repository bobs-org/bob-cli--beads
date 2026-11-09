# Bead: bob-cli-ir.12 — Mac updates, existing-record rows, and Similar records

[Bead Pages](../README.md) / [bob-cli-ir](README.md) / bob-cli-ir.12

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.1a0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.1a0.md) · **Assignee:** `bob-cli-ir.12` · **Size:** medium
**Created:** 2026-11-08 11:06:12 EST · **Closed:** 2026-11-09 13:12:08 EST
**Plan:** [202611/record\_notes.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/record_notes.md)

## Description

mac-record-revisits: present record updates as before-and-after property rows, show existing-record completion rows, and extend the Similar band to record items with the Add to it action.

## Notes

[2026-11-09T18:12:08Z · bob-cli-ir.12] Implemented mac-record-revisits in bob-mac-capture: update cards show before→after rows with +N notes (CaptureRecordField before/before_display, CaptureRecordRow changeText, RecordCardView + RecordNotePreviewView), record_target rows render status plus two field values (CaptureRecordTargetField, CompletionRowContent), Similar band accepts scope:record with Add to it splice/order/settle unchanged plus SIMILAR RECORDS copy and VoiceOver actions. Tests: new CaptureRecordRevisitsTests (9 pass) + updated CaptureRecordTests/CompletionRowContentTests; swift build + swift test green (2390 tests, 0 failures). Docs: capture-previews.md Record Card + Similar tasks. Mac typecheck/macos-ci not run from Linux; docs-check lint budget overages pre-existing on base.

## Dependencies

- **Depends on:** [bob-cli-ir.11](bob-cli-ir.11.md) ✓ · ⧖ 2026-11-08
- **Blocks:** [bob-cli-ir.13](bob-cli-ir.13.md) ◐ · ⧖ 2026-11-08
- **Depends on:** [bob-cli-ir.8](bob-cli-ir.8.md) ✓ · ⧖ 2026-11-08

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-ir.12](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-ir.12/README.md) | [bob-cli-ir.12](bob-cli-ir.12.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-mac-capture | [`bob-mac-capture@a5152aa`](https://github.com/bobs-org/bob-mac-capture/commit/a5152aa516fce9644c77624022f78973f8f9517b) | feat(mac-capture): show record updates, existing-record rows, and Similar records | [bob-cli-ir.12](bob-cli-ir.12.md) | 2026-11-09 13:13:48 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:d5][1] | Know which Mac record update UX has shipped for the user report | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.d5/README.md

<!-- sase:referenced-by:end -->
