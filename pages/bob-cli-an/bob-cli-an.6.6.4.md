# Bead: bob-cli-an.6.6.4 — Render web clips with static fonts so Highlights quotes keep whole words

[Bead Pages](../README.md) / [bob-cli-an.6.6](bob-cli-an.6.6.md) / bob-cli-an.6.6.4

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-an.6.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-an.6.land.md) · **Assignee:** `bob-cli-an.6.6.4` · **Size:** medium
**Created:** 2026-10-23 17:27:15 EDT · **Closed:** 2026-10-23 18:02:45 EDT
**Plan:** [202610/backlog\_batch3\_rfserver\_backups\_day\_zone\_webclip\_fonts\_ref\_paths.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/backlog_batch3_rfserver_backups_day_zone_webclip_fonts_ref_paths.md)

## Description

webclip-static-fonts: resolve bob-cli-85 by replacing the web-clip reader template's variable woff2 faces with static faces so Chromium embeds no Type 3 body fonts.

## Notes

[2026-10-23T22:01:44Z · bob-cli-an.6.6.4] Baseline variable woff2 fixture: pdffonts all Type 3 body fonts; PDFKit on Mac unknown=9/138 (6.52%) vs article.html vocab (splits: vic tl ttps zh lex apri ober iarskyi ko). Static CFF OTF reuse without conversion still Type 3 for Inter and Source Serif 4 SmText (Skia Type 3 for CFF/OTTO as well as variable fonts); JetBrains Mono was already CID TrueType.

[2026-10-23T22:01:48Z · bob-cli-an.6.6.4] Fix: share bob-cli-87.1 assets/print_fonts via src/print_fonts.rs include_bytes (crate must not duplicate ~6 MB faces); git rm 9 variable woff2; reader.css discrete static @font-face; print-time CFF→glyf TTF (fonttools Cu2QuPen max err 1.0, reverse_direction, TrueType maxp 1.0) so Chromium embeds CID TrueType. Converted fixture /tmp/bob-clip-font-probe-j9etn12j/render.pdf: Inter/SourceSerif4SmText/JetBrainsMono all CID TrueType, /Type3 absent, pdftotext 140 words same as baseline.

[2026-10-23T22:01:52Z · bob-cli-an.6.6.4] Validation: adapter --self-test ok (no Type 3 body fonts, cff-converts-to-truetype, leftover woff2 empty). print_fonts unit tests pass (ptr::eq shared bytes). just package-check --no-verify 7707872 bytes (7.35 MiB, under 8 MiB warn). PDFKit on Mac (ssh mac, spike/pdfkit_probe.swift): converted render.pdf unknown=0/134 (0.00%); baseline 6.52%. Under ~1.5% stop threshold; did not switch engines. Did not re-render existing library PDFs. Left bob-cli-85 open for the lander.

[2026-10-23T22:01:56Z · bob-cli-an.6.6.4] PROPOSED FOLLOW-UP: just docs-check fails on generated drift in docs/develop/decisions.md on this tree and on clean master — already tracked as bob-cli-b6; do not run docs-gen from this phase

[2026-10-23T22:02:45Z · bob-cli-an.6.6.4] Verified: reader uses shared print_fonts static faces; CFF converted to glyf at print time. Fixture PDF all CID TrueType, no Type 3. Adapter self-test ok. package-check 7.35 MiB. PDFKit on Mac unknown=0/134 (0.00%) vs Type 3 baseline 6.52%. pdftotext 140 words unchanged. Epic-symbols none. Left bob-cli-85 open for lander. docs/develop/decisions.md drift recorded as PROPOSED FOLLOW-UP (bob-cli-b6).

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-an.6.6.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-an.6.6.4/README.md) | [bob-cli-an.6.6.4](bob-cli-an.6.6.4.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`37594eb`](https://github.com/bobs-org/bob-cli/commit/37594eb22b89cd403a9fc95e811d1d4e7e421900) | fix(webclip): embed static CID TrueType faces instead of Type 3 | [bob-cli-an.6.6.4](bob-cli-an.6.6.4.md) | 2026-10-23 18:07:21 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-an.6.6.4][1] | Need current notes before recording PDFKit evidence and closing | 3 |
| read-by | [agent:bob-cli-an.6.6.6.5.6.land--2][2] | Review every ancestor phase note for unresolved follow-ups and completion | 1 |
| read-by | [agent:bob-cli-an.6.6.land][3] | Need the child scope and notes | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-an.6.6.4/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-an.6.6.6.5.6.land.md
[3]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-an.6.6.land.md

<!-- sase:referenced-by:end -->
