# Bead: bob-cli-ir.10.1.4 — Render the Record Card and semantic editor styling

[Bead Pages](../README.md) / [bob-cli-ir.10.1](bob-cli-ir.10.1.md) / bob-cli-ir.10.1.4

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-ir.10](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-ir.10.md) · **Assignee:** `bob-cli-ir.10.1.4` · **Size:** medium
**Created:** 2026-11-09 02:49:44 EST · **Closed:** 2026-11-09 07:10:58 EST
**Plan:** [202611/mac\_record\_card.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/mac_record_card.md)

## Description

card-surface: render the Record Card in the picker slot with persistent labels, choices, value lists, optional-field disclosure, defaults, path and note count. Style record spans, implement accessibility and Reduce Motion behavior, verify narrow/wide layouts, and finish the capture-preview documentation.

## Notes

[2026-11-09T09:13:03Z · bob-cli-ir.10.1.3] Coordination: guided-interaction is now working in CapturePanelModel.swift, CaptureKeyCommandRouter.swift, and CapturePanelController.swift to expose record actions and key state. Please keep the RecordCardView/CapturePanelView surface changes focused on consuming model actions; tell me in a bead note if you need overlapping model changes.

[2026-11-09T11:04:59Z · bob-cli-ir.10.1.4] Surface consumes 10.1.3 model actions (requestRecordField, acceptRecordCandidate, editRecordField, setRecordMoreExpanded). Extra model helpers this phase: installRecordCardForPreviews for design renders, and paintHighlighting record_route chip wash plus item-scoped record_field_value tints (no emoji bytes in the draft). CaptureRecordInteractionTests memberwise inits were reordered so completionVisible precedes recordCardActive; that was a typecheck failure on HEAD 7933c7e.

[2026-11-09T11:38:18Z · bob-cli-ir.10.1.4--1] CI 42606393021 failed 7 Record Card tests. Causes: set-state values shared .accentColor with the record-route chip so highlight assertions mixed @eat/ with liked/Ramen/Clark; handmade owning-item spans used out-of-bounds offsets (liked is 21-26, nope 49-53); panel mutationCaptureCalls counted argv=capture --dry-run as vault writes and Return blocked before --record-field landed. Fixes: set values use .green; offsets corrected; dry-run excluded; Return waits for --record-field. just portable-check passed. Mac scratch bundle.sh + typecheck-tests passed. Re-running Scripts/macos-ci-check.

[2026-11-09T12:10:45Z · bob-cli-ir.10.1.4--2] PROPOSED FOLLOW-UP: Optional More rows (Visited, Url) left-align instead of sharing the centered field column — CI render-fixtures capture-record-card-more-{light,dark}.png from run 42611020479; required/set rows stay centered. Polish only; More disclosure still reveals the fields.

[2026-11-09T12:10:58Z · bob-cli-ir.10.1.4--2] Record Card occupies the picker slot with Bob-owned labels, path, note count, choice capsules, More disclosure, and footer hints; record spans styled without inserting type emoji; set values use a distinct green from the route chip; item-scoped field matching; a11y identities; Reduce Motion and increased contrast. just portable-check and just docs-check passed. Mac scratch bundle.sh + typecheck-tests passed. Scripts/macos-ci-check exact-SHA macOS CI passed after fixing set/route color collision, owning-item span offsets, and dry-run mutation log filtering. Reviewed CI render-fixtures from run 42611020479 (https://github.com/bobs-org/bob-mac-capture/actions/runs/42611020479): wide/minimum/complete/contrast/more light+dark Record Card images.

## Dependencies

- **Depends on:** [bob-cli-ir.10.1.3](bob-cli-ir.10.1.3.md) ✓ · ⧖ 2026-11-09

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-ir.10.1.4](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-ir.10.1.4.md) | [bob-cli-ir.10.1.4](bob-cli-ir.10.1.4.md) | 2 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-mac-capture | [`bob-mac-capture@8c13ac4`](https://github.com/bobs-org/bob-mac-capture/commit/8c13ac44c1e318be27b60c3b9007f9cc904fbe54) | feat(capture): render the Record Card in the picker slot | [bob-cli-ir.10.1.4](bob-cli-ir.10.1.4.md) | 2026-11-09 06:06:23 EST |
| bob-mac-capture | [`bob-mac-capture@4bca5da`](https://github.com/bobs-org/bob-mac-capture/commit/4bca5da078afd182d3bf38b5eac1219db338008d) | fix(capture): distinguish set-value tints from the record route chip | [bob-cli-ir.10.1.4](bob-cli-ir.10.1.4.md) | 2026-11-09 06:40:45 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-ir.10.1.3][1] | Need the neighboring phase's file scope before editing shared panel and view code | 1 |
| read-by | [agent:bob-cli-ir.10.1.4--1][2] | Need the phase scope, notes, and design file after CI failure | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-ir.10.1.3/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-ir.10.1.4.md

<!-- sase:referenced-by:end -->
