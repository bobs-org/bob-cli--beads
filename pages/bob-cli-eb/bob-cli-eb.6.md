# Bead: bob-cli-eb.6 — Fidelity, page-count, and Mac probe acceptance

[Bead Pages](../README.md) / [bob-cli-eb](README.md) / bob-cli-eb.6

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.2u.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.2u.linker.w0.md) · **Assignee:** `bob-cli-eb.6` · **Size:** medium
**Created:** 2026-10-29 20:03:07 EDT · **Closed:** 2026-10-30 01:58:27 EDT
**Plan:** [202610/ref\_table\_layout\_for\_highlights.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/ref_table_layout_for_highlights.md)

## Description

acceptance: compare baseline and new renders of fixtures and real chat reports for text fidelity and page counts, rerun the PDFKit cell probe on the Mac (with a bulleted-record fallback), write the acceptance report and Bryan's manual checklist, and optionally record the decision.

## Notes

[2026-10-30T05:57:56Z · bob-cli-eb.6--3] PROPOSED FOLLOW-UP: Revisit the declined prose-table decision record — The epic selected decision_record = no, so this phase left the decisions memory unchanged; the land agent should consider recording the settled render behavior when deciding whether the design is durable.

[2026-10-30T05:58:05Z · bob-cli-eb.6--3] PROPOSED FOLLOW-UP: Resolve per-document page growth without shrinking text — Acceptance passes current text fidelity and Mac selection probes, but sase_core_maintainability_audit grows 19→20 pages and agents_tab_inbox_and_history_views grows 28→31 against the no-growth target; corpus total drops 140→134. Review whether selected record tables or spacing can satisfy the per-document limit while keeping body-size text and visibly separated rows.

[2026-10-30T05:58:27Z · bob-cli-eb.6--3] Verified eight-document baseline/current acceptance: current ordered text fidelity 1752/1752, both current Mac on-mode cell/phrase probes clean, and vault status unchanged. Acceptance report and both required follow-up notes are recorded. The per-document page limit remains unmet for two reports (+1 and +3 pages); Bryan's manual checklist is in the report.

## Dependencies

- **Depends on:** [bob-cli-eb.3](bob-cli-eb.3.md) ✓ · ⧖ 2026-10-29
- **Depends on:** [bob-cli-eb.4](bob-cli-eb.4.md) ✓ · ⧖ 2026-10-29

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-eb.6](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-eb.6.md) | [bob-cli-eb.6](bob-cli-eb.6.md) | 2 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`a3735b9`](https://github.com/bobs-org/bob-cli/commit/a3735b914939d208f038dd96573c4359b00eff53) | fix(ref): reduce record spacing for table PDFs | [bob-cli-eb.6](bob-cli-eb.6.md) | 2026-10-30 01:59:39 EDT |
| bob-cli--research | [`bob-cli--research@bae76a1`](https://github.com/bobs-org/bob-cli--research/commit/bae76a1bbd9b3e55140ad7db88954a741ef913e0) | docs(research): document table layout acceptance evidence | [bob-cli-eb.6](bob-cli-eb.6.md) | 2026-10-30 02:01:28 EDT |
