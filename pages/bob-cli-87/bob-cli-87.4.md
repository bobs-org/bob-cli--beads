# Bead: bob-cli-87.4 — Note print profile and two-step xelatex render

[Bead Pages](../README.md) / [bob-cli-87](README.md) / bob-cli-87.4

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.10l](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.10l.md) · **Assignee:** `bob-cli-87.4` · **Size:** large
**Created:** 2026-10-16 07:13:18 EDT · **Closed:** 2026-10-16 08:39:12 EDT
**Plan:** [202610/note\_snapshots.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/note_snapshots.md)

## Description

print-profile: implement note.tex (the design system), note.lua (contract to TeX, AST-preserving), and a pandoc-to-.tex-then-xelatex render that surfaces missing glyphs and errors, plus the doctor packages. Tested against a hand-written contract fixture.

## Notes

[2026-10-16T12:38:53Z · bob-cli-87.4] PROPOSED FOLLOW-UP: Image framing with a hairline in note snapshots. The renderer centers standalone images via Lua center-environment delimiters (no user paths in raw TeX args) and preserves width=62% from the projected contract, but does not yet draw the specified hairline frame. A TeX-side framing approach that avoids interpolating user asset paths into raw macro arguments (e.g. a breakable framed environment around the existing center block, or a Lua-safe image wrapper) should land in the create-wiring or a later polish phase. -r Record print-profile follow-up per approved plan

[2026-10-16T12:39:12Z · bob-cli-87.4] print-profile renderer done: render_note_pdf(projected_md, scratch, filters, meta)->RenderOutcome (pdf, NoteWarning MissingGlyph/Overfull>20pt deduplicated, return_links ReportOutcome) in note_snapshot/profile.rs with embedded note.tex/note.lua; GlyphCoverage per-role overrides direct U+25B8 to mono before Noto. Verified: hermetic fake pandoc/xelatex (reader flags commonmark_x-tex_math_dollars-emoji, no toc/number-sections/pdf-engine, filter order code-break>return-links>note, cwd=scratch, single-arg spaces, 2 passes + bounded 3rd on Rerun, stop on failure, 20pt boundary, missing-glyph/overfull/hint/absent-log paths); pandoc-gated contract TeX (6 statuses, chips/accent/label/muted/missing, embed/livequery/callout/compact, lane/appendix, masthead/nav safe bobsec labels, anchors, opt-out, specials/@BANK/$69k/:shortcode:, long-token allowbreak, dice fallback, triangular mono); real pandoc+xelatex contract (0 missing, 0 >20pt overfull, 0 Type3 via lopdf+pdffonts, bookmarks, Info Title/Subject, obsidian URIs, paired return links, pdftotext words/chips/no status symbols/ligature-safe/specials, footer 1/N, corpus+triangular regression); nav short (no p.) vs long >8pp (p.) with wrapped task+children; PNG visual (masthead/chips/indents/footer match; images centered, framing follow-up noted). just check green.

## Dependencies

- **Depends on:** [bob-cli-87.1](bob-cli-87.1.md) ✓ · ⧖ 2026-10-16
- **Blocks:** [bob-cli-87.5](bob-cli-87.5.md) ◐ · ⧖ 2026-10-16

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-87.4](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-87.4.md) | [bob-cli-87.4](bob-cli-87.4.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`1a57e47`](https://github.com/bobs-org/bob-cli/commit/1a57e47f67023a96de3e220642fd41c64ddf58fb) | feat(highlights): note snapshot print profile and two-step xelatex render | [bob-cli-87.4](bob-cli-87.4.md) | 2026-10-16 08:45:42 EDT |
