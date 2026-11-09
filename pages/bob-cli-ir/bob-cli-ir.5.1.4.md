# Bead: bob-cli-ir.5.1.4 — Publish the record capture contract and acceptance evidence

[Bead Pages](../README.md) / [bob-cli-ir.5.1](bob-cli-ir.5.1.md) / bob-cli-ir.5.1.4

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-ir.5](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-ir.5.md) · **Assignee:** `bob-cli-ir.5.1.4` · **Size:** small
**Created:** 2026-11-08 18:25:56 EST · **Closed:** 2026-11-08 22:58:20 EST
**Plan:** [202611/capture\_record\_creation.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/capture_record_creation.md)

## Description

record-contract: finish the capture documentation, apply the inherited approved Capture glossary correction, and run the cross-surface acceptance matrix for bob-cli-ir.5.

## Notes

[2026-11-09T03:16:56Z · bob-cli-ir.5.1.4] E2E transcript (isolated /tmp/bob-cli-ir-5.1.4-e2e.kFNZ0q, grammar 20, BOB_NOW=2026-10-07 13:40:00):
- capture-parse 'Ramen Nagi @eat/' → mode=record_note, needs=[record_value], missing=[status,category], notes=0, field kind=choices; complete draft notes=1, needs=[]
- dry-run JSON kind=record_note placement=created relative_target=eat/ramen_nagi.md; eat/ not created; human 'would create' / 'new restaurant'
- commit JSON same markdown as dry-run (216 bytes equal); no daily note; no mac_inbox.md
- duplicate → ok=false code=record_exists; bytes unchanged
- incomplete after task ('Buy milk' + 'Ippudo @eat/' missing category) → exit 2, draft with category:: …, files/bytes unchanged, no inbox
- %t bulk created eat/nagi_two.md and eat/nagi_three.md
- 'Blaze @eat' warning record_collection_route rewrite @eat → @eat/; applying rewrite → mode=record_note
- capture-targets JSON kind=record route=eat/ type=restaurant count=3; human 'Record folders'
glossary:capture already includes 'project note, or record note (a note of a config-declared record type, see docs/records.md)'; glossary:record-note does not exist (not linked). memory_glossary_record_note=no honored. just docs-gen + just docs-check passed. epic-symbols: none. Help goldens refreshed from live --help (capture about + records Vault line).

[2026-11-09T03:37:41Z · bob-cli-ir.5.1.4--1] just check recovery: capture_help_lists_options_alphabetically failed on the updated capture about text (this phase). native::catalog::tests::document_shape expected 79 entries after records CLI added 4 leaves (records-check/list/new/show); native::completion::kinds::tests::every_value_arg_has_a_decision missing records new:set and records new:stem. Fixed help assertion, catalog count 83, and FreeText kinds for records new set/stem/note. Isolated reruns passed.

[2026-11-09T03:58:20Z · bob-cli-ir.5.1.4--2] Record capture contract published: docs/capture.md Record notes, capture-syntax/json-outputs/records pages, capture CLI help. Isolated E2E (grammar 20): parse record_note, dry-run/commit 216-byte eat/ramen_nagi.md, record_exists duplicate, incomplete-after-task exit 2, %t bulk, @eat collection rewrite, capture-targets kind=record. Catalog 83 + records new --set/--stem/--note FreeText. just check passed inline after host completion refused missing Python stages. epic-symbols: none. Parent epic stays open.

## Dependencies

- **Depends on:** [bob-cli-ir.5.1.3](bob-cli-ir.5.1.3.md) ✓ · ⧖ 2026-11-08

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-ir.5.1.4](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-ir.5.1.4.md) | [bob-cli-ir.5.1.4](bob-cli-ir.5.1.4.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`e081e72`](https://github.com/bobs-org/bob-cli/commit/e081e729c5d30152df19e2a9173d067be6dacd8d) | docs(capture): publish the record note capture contract | [bob-cli-ir.5.1.4](bob-cli-ir.5.1.4.md) | 2026-11-08 22:59:07 EST |
