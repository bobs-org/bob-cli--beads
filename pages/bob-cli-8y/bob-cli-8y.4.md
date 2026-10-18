# Bead: bob-cli-8y.4 — Dry-run, doctor, docs, live test, and acceptance

[Bead Pages](../README.md) / [bob-cli-8y](README.md) / bob-cli-8y.4

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.research.4r.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.research.4r.linker.w0.md) · **Assignee:** `bob-cli-8y.4` · **Size:** medium
**Created:** 2026-10-17 19:29:17 EDT · **Closed:** 2026-10-17 22:18:24 EDT
**Plan:** [202610/ref\_create\_mermaid\_figures.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/ref_create_mermaid_figures.md)

## Description

finish: add the browser-free dry-run count, the warn-only doctor row, the docs, a gated live end-to-end PDF test, the athena acceptance run on the 12-fence report, Mac acceptance per decision, the optional decision record, and follow-up notes.

## Notes

[2026-10-18T02:14:18Z · bob-cli-8y.4] ATHENA acceptance, 2026-10-17. Read `research:202610/merge_queue_fence_reassessment_explained.md` through its audited artifact ref (`file:explicit:20a31b0e7cfdc185f9d9a11c`) and imported the 12-fence report into a temporary vault with the workspace `cargo run --bin bob`; no real vault was touched. Warm paired imports with a TMPDIR path over 40 bytes: rendering disabled 5.66 s / 16 pages; rendering enabled 10.37 s / 21 pages, a +4.70 s delta for the 12-diagram batch. All 12 rendered. A source path with spaces and Japanese characters passed; 5 representative body-text checks passed and no Mermaid source leaked. Scale warnings: diagram 3 at 46%, diagram 5 at 49%. The separate first run took 52.88 s including the initial cargo build.

`pdffonts` output:
name                                 type              encoding         emb sub uni object ID
------------------------------------ ----------------- ---------------- --- --- --- ---------
MBMSZC+DejaVuSerif                   CID TrueType      Identity-H       yes yes yes      5  0
CVGMBK+DejaVuSerif-Bold              CID TrueType      Identity-H       yes yes yes      7  0
XFFOCL+DejaVuSansMono                CID TrueType      Identity-H       yes yes yes     13  0
PPBZAG+DejaVuSans-Bold               CID TrueType      Identity-H       yes yes yes     46  0
IDVQUY+DejaVuSansMono-Bold           CID TrueType      Identity-H       yes yes yes     52  0
AAAAAA+DejaVuSans                    CID TrueType      Identity-H       yes yes yes     66  0
AAAAAA+DejaVuSans                    CID TrueType      Identity-H       yes yes yes     84  0
DGUYOK+DejaVuSerif-Italic            CID TrueType      Identity-H       yes yes yes    110  0
AAAAAA+DejaVuSans                    CID TrueType      Identity-H       yes yes yes    104  0
AAAAAA+DejaVuSans                    CID TrueType      Identity-H       yes yes yes    116  0
AAAAAA+DejaVuSans                    CID TrueType      Identity-H       yes yes yes    137  0
AAAAAA+DejaVuSans                    CID TrueType      Identity-H       yes yes yes    157  0
JLVVYX+DejaVuSans                    CID TrueType      Identity-H       yes yes yes    166  0
AAAAAA+DejaVuSans                    CID TrueType      Identity-H       yes yes yes    175  0
AAAAAA+DejaVuSans                    CID TrueType      Identity-H       yes yes yes    198  0
AAAAAA+DejaVuSans                    CID TrueType      Identity-H       yes yes yes    216  0
AAAAAA+DejaVuSans                    CID TrueType      Identity-H       yes yes yes    238  0
AAAAAA+DejaVuSans                    CID TrueType      Identity-H       yes yes yes    265  0
AAAAAA+DejaVuSans                    CID TrueType      Identity-H       yes yes yes    290  0

`pdfimages -list` output (header only, no image rows):
page   num  type   width height color comp bpc  enc interp  object ID x-ppi y-ppi size ratio
--------------------------------------------------------------------------------------------

[2026-10-18T02:14:21Z · bob-cli-8y.4] Mac acceptance is manual per `mac_check=manual`; I did not touch the Mac. Bryan's checklist: recreate the same report into a scratch vault; select and highlight label text inside a diagram in Highlights; copy a body-text quote and confirm it is clean; confirm a malformed diagram shows its note and source.

[2026-10-18T02:14:25Z · bob-cli-8y.4] PROPOSED FOLLOW-UP: Consider landscape pages for diagrams below 0.5 scale — preserve vector readability for very wide diagrams.

[2026-10-18T02:14:28Z · bob-cli-8y.4] PROPOSED FOLLOW-UP: Route SVG image embeds through the same adapter operation — address the separate “Image not printable” case.

[2026-10-18T02:14:32Z · bob-cli-8y.4] PROPOSED FOLLOW-UP: Add a listen-skip marker for diagrams — let narration skip diagram labels when desired.

[2026-10-18T02:14:36Z · bob-cli-8y.4] PROPOSED FOLLOW-UP: Nudge `sase-research-artifacts` prompts toward `flowchart TD` and shorter labels — reduce small text in wide rendered figures.

[2026-10-18T02:14:39Z · bob-cli-8y.4] PROPOSED FOLLOW-UP: Re-evaluate `mmdr` with `svg2pdf` as a browser-free backend behind the same `{id, source} → PDF` interface — only if fixtures show faithful layout and selectable text.

[2026-10-18T02:14:42Z · bob-cli-8y.4] PROPOSED FOLLOW-UP: Reconsider the skipped `decisions:ref-create-renders-mermaid-in-the-adapter` memory record — this phase followed the final `decision_record=no` choice and made no memory edits.

[2026-10-18T02:14:46Z · bob-cli-8y.4] PROPOSED FOLLOW-UP: The SASE research file hook invokes the installed `bob`; schedule `just install` on the next planned Bob deployment for the feature to reach that hook. This phase did not reinstall Bob.

[2026-10-18T02:18:24Z · bob-cli-8y.4] Completed dry-run counts on both routes, warning-only Mermaid doctor status, docs, and gated live PDF test; live fixture passed font/raster checks and long-TMPDIR/path coverage. On athena rendered the 12-fence report in a scratch vault (12/12, +4.70s vs disabled); pdffonts had no Type 3 and pdfimages had no rows. just check, just check-web-clip-adapter, and git diff --check passed; epic-symbols reported none. Mac checklist and follow-ups are recorded on this phase.

## Dependencies

- **Depends on:** [bob-cli-8y.3](bob-cli-8y.3.md) ✓ · ⧖ 2026-10-17

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-8y.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-8y.4/README.md) | [bob-cli-8y.4](bob-cli-8y.4.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`99b2ac4`](https://github.com/bobs-org/bob-cli/commit/99b2ac4085705d021d332bee440d52897364cd17) | feat(highlights): finish Mermaid diagram acceptance | [bob-cli-8y.4](bob-cli-8y.4.md) | 2026-10-17 22:19:05 EDT |
