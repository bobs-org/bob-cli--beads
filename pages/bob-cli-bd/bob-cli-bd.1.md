# Bead: bob-cli-bd.1 — Sidecar parser gates

[Bead Pages](../README.md) / [bob-cli-bd](README.md) / bob-cli-bd.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.2d.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.2d.linker.w0.md) · **Assignee:** `bob-cli-bd.1` · **Size:** medium
**Created:** 2026-10-24 07:59:21 EDT · **Closed:** 2026-10-24 08:34:49 EDT
**Plan:** [202610/ref\_note\_annotation\_sections.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/ref_note_annotation_sections.md)

## Description

gates: fix bob-cli-ba so hard-wrapped quote lines starting with `# ` stay quote text, and make sidecar page-heading detection level-aware so a `# P values` sticky is never a page break.

## Notes

[2026-10-24T12:34:08Z · bob-cli-bd.1] PROPOSED FOLLOW-UP: record annotation-sections design as decisions:annotation-sections-are-name-keyed-folds strand (epic auto-decision decision_record=no; skipped per plan gate, needs land-agent triage)

[2026-10-24T12:34:16Z · bob-cli-bd.1] PROPOSED FOLLOW-UP: add "Annotation Section" glossary term (epic auto-decision glossary_term=no; skipped per plan gate, needs land-agent triage)

[2026-10-24T12:34:25Z · bob-cli-bd.1] Vault check (read-only): base and phase builds both scan ~/bob dry-run clean (519 pdfs unchanged, notes[] empty). The two bead notes were already re-synced by vault commit deae6fd9 (kellys-mbp 08:30) with the fixed rendering; phase build reproduces it byte-identically. Retired ids ^h-43e982a8c300 and ^h-93e1d7136bfa have no links from other vault Markdown (only their own tombstones).

[2026-10-24T12:34:49Z · bob-cli-bd.1] Gates done and verified: quote-continuation fix (bob-cli-ba absorbed and closed) + level-aware page headings; 5 new sidecar tests, 631 highlights_ref tests pass, fmt+clippy gates clean, base-vs-phase dry-run vault scans identical (519 unchanged, notes[] empty, no dangling links to retired ids). Work uncommitted in phase workspace (4 files).

## Dependencies

- **Blocks:** [bob-cli-bd.2](bob-cli-bd.2.md) ◐ · ⧖ 2026-10-24

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-bd.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-bd.1/README.md) | [bob-cli-bd.1](bob-cli-bd.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`6ec2f16`](https://github.com/bobs-org/bob-cli/commit/6ec2f16a564fe99b5582b15daa52dfdb9e785e64) | feat(highlights): keep hard-wrapped hash lines in quotes and scope page headings by level | [bob-cli-bd.1](bob-cli-bd.1.md) | 2026-10-24 08:48:27 EDT |
