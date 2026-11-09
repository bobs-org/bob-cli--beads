# Bead: bob-cli-ir.10.1.4 — Render the Record Card and semantic editor styling

[Bead Pages](../README.md) / [bob-cli-ir.10.1](bob-cli-ir.10.1.md) / bob-cli-ir.10.1.4

**Status:** ◐ in_progress · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-ir.10](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-ir.10.md) · **Assignee:** `bob-cli-ir.10.1.4` · **Size:** medium
**Created:** 2026-11-09 02:49:44 EST
**Plan:** [202611/mac\_record\_card.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/mac_record_card.md)

## Description

card-surface: render the Record Card in the picker slot with persistent labels, choices, value lists, optional-field disclosure, defaults, path and note count. Style record spans, implement accessibility and Reduce Motion behavior, verify narrow/wide layouts, and finish the capture-preview documentation.

## Notes

[2026-11-09T09:13:03Z · bob-cli-ir.10.1.3] Coordination: guided-interaction is now working in CapturePanelModel.swift, CaptureKeyCommandRouter.swift, and CapturePanelController.swift to expose record actions and key state. Please keep the RecordCardView/CapturePanelView surface changes focused on consuming model actions; tell me in a bead note if you need overlapping model changes.

[2026-11-09T11:04:59Z · bob-cli-ir.10.1.4] Surface consumes 10.1.3 model actions (requestRecordField, acceptRecordCandidate, editRecordField, setRecordMoreExpanded). Extra model helpers this phase: installRecordCardForPreviews for design renders, and paintHighlighting record_route chip wash plus item-scoped record_field_value tints (no emoji bytes in the draft). CaptureRecordInteractionTests memberwise inits were reordered so completionVisible precedes recordCardActive; that was a typecheck failure on HEAD 7933c7e.

## Dependencies

- **Depends on:** [bob-cli-ir.10.1.3](bob-cli-ir.10.1.3.md) ✓ · ⧖ 2026-11-09

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-ir.10.1.4](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-ir.10.1.4.md) | [bob-cli-ir.10.1.4](bob-cli-ir.10.1.4.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-mac-capture | [`bob-mac-capture@8c13ac4`](https://github.com/bobs-org/bob-mac-capture/commit/8c13ac44c1e318be27b60c3b9007f9cc904fbe54) | feat(capture): render the Record Card in the picker slot | [bob-cli-ir.10.1.4](bob-cli-ir.10.1.4.md) | 2026-11-09 06:06:23 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-ir.10.1.3][1] | Need the neighboring phase's file scope before editing shared panel and view code | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-ir.10.1.3/README.md

<!-- sase:referenced-by:end -->
