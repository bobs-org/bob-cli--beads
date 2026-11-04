# Bead: bob-cli-h8.11 — Render emoji and uncovered symbols in generic ref PDFs

[Bead Pages](../README.md) / [bob-cli-h8](README.md) / bob-cli-h8.11

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.18c](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.18c.md) · **Assignee:** `bob-cli-h8.11` · **Size:** medium
**Created:** 2026-11-04 16:39:10 EST · **Closed:** 2026-11-04 17:41:40 EST
**Plan:** [202611/top\_ten\_bead\_bundles.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/top_ten_bead_bundles.md)

## Description

ref-pdf-emoji: route the generic pandoc-to-XeLaTeX render in highlights_ref/create.rs through the note-snapshot Noto Emoji fallback, so uncovered codepoints print and extract correctly. Add a golden extraction test, propose the PDF backfill as a follow-up, and close bob-cli-e9.

## Notes

[2026-11-04T22:41:07Z · bob-cli-h8.11] PROPOSED FOLLOW-UP: Regenerate existing generic Markdown reference PDFs in the vault so their visible glyphs and text layers pick up the Noto fallback fix from bob-cli-e9.

[2026-11-04T22:41:12Z · bob-cli-h8.11] PROPOSED FOLLOW-UP: Fix the eight strict-Clippy errors in h2 past-Pomodoro code (editor_pomodoro.rs:3268, 3288, 3298, 3309, 3680, 3743, 3815; past.rs:472). The same eight errors reproduce at clean HEAD d32e858d; already tracked in bob-cli-h2 note #3.

[2026-11-04T22:41:40Z · bob-cli-h8.11] Generic Markdown PDFs now use the note-snapshot glyph table and bundled Noto fallback; PDF text extraction passed for 🍅 prose, 🎲 inline code, and ▸ cross-face symbol. cargo fmt and the focused extraction test pass. just check fails at Clippy on eight errors reproduced identically at clean HEAD and recorded with bob-cli-h2 note #3; PDF backfill proposed. epic-symbols was empty.

## Dependencies

- **Depends on:** [bob-cli-h8.6](bob-cli-h8.6.md) ✓ · ⧖ 2026-11-04

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-h8.11](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-h8.11/README.md) | [bob-cli-h8.11](bob-cli-h8.11.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`0e11f8b`](https://github.com/bobs-org/bob-cli/commit/0e11f8b0e8c3974da3113fe15fd19fa3839c2368) | fix(highlights): preserve fallback glyphs in generic ref PDFs | [bob-cli-h8.11](bob-cli-h8.11.md) | 2026-11-04 17:42:48 EST |
