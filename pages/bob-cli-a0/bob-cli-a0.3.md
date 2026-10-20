# Bead: bob-cli-a0.3 — Bob visual identity and homepage

[Bead Pages](../README.md) / [bob-cli-a0](README.md) / bob-cli-a0.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.95](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.95.md) · **Assignee:** `bob-cli-a0.3` · **Size:** large
**Created:** 2026-10-19 18:55:42 EDT · **Closed:** 2026-10-19 23:00:47 EDT
**Plan:** [202610/bob\_public\_docs\_site.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/bob_public_docs_site.md)

## Description

theme: build the calm-notebook theme (tokens, self-hosted fonts, bullet-b mark, keycaps, bob-task fence, contract banner, provenance footer) and the homepage, verified with Playwright and axe.

## Notes

[2026-10-20T02:26:49Z · bob-cli-a0.3] Planning only: prepared a medium tale for one coder covering local fonts and deterministic identity assets, bob-task rendering, notebook CSS and shared overrides, the homepage, and Playwright/axe verification in both builders. Read the approved epic and canonical research; no earlier unfinished implementation notes were present. Identified absent U+2317 in bundled fonts and included a docs-only derivative fix. Validation and revalidation passed with zero warnings; no product files changed. Submitting through sase plan propose.

[2026-10-20T03:00:36Z · bob-cli-a0.3] PROPOSED FOLLOW-UP: base-theme axe findings remain after the theme phase. Reproduce with just docs-build then just docs-a11y and read target/docs/a11y/zensical/report.json (material report under target/docs/a11y/material/report.json). Remaining serious findings are base-theme/pre-existing, not new theme content: header drawer/search label attributes (aria-prohibited-attr in Zensical, aria-dialog-name in Material), Pygments code-token contrast inside pre-existing long contracts (capture.md), scrollable-region-focusable on pre-existing contract tables, and 200%-zoom reflow overflow from the off-canvas nav drawer (375 vs 360). The new homepage, bob-task fixture, tags, links, footer, keyboard skip-link/palette, no-JS core content, and local-font checks pass. Fix in a follow-up by overriding the base header/table/code token templates and styles.

[2026-10-20T03:00:47Z · bob-cli-a0.3] Implemented bob_docs_theme: local WOFF2 fonts (Inter-Regular 72064, Inter-Italic 71040, InterDisplay-SemiBold 73352, BobMono-Regular 96924; total 313380 < 450000; byte-stable check passes), deterministic identity assets (bob-mark.svg, favicon.svg/png, social-card.png 1200x630; media.yml registered), bob-task fence with today flag plus formatter/validator tests, notebook CSS with light/slate tokens and AA crimson pair, shared Jinja2/MiniJinja overrides (contract banner, mount-aware edit links via bob_edits, provenance footer, OG/Twitter), honest homepage (217 words, verified bob capture output from synthetic vault), Playwright+axe audit with vendored axe-core 4.14.0 (fixture zero violations; homepage only pre-existing header-attr findings; reports under target/docs/a11y/zensical and material). Verified: just docs-check passes (200 tests), strict Zensical build passes, Material 9.7 build passes with banners/provenance/tasks/fonts/metadata confirmed in HTML, fonts/assets check modes byte-stable, screenshots inspected in both schemes and all widths.

## Dependencies

- **Blocks:** [bob-cli-a0.10](bob-cli-a0.10.md) ✓ · ⧖ 2026-10-19
- **Depends on:** [bob-cli-a0.2](bob-cli-a0.2.md) ✓ · ⧖ 2026-10-19
- **Blocks:** [bob-cli-a0.5](bob-cli-a0.5.md) ◐ · ⧖ 2026-10-19
- **Blocks:** [bob-cli-a0.6](bob-cli-a0.6.md) ✓ · ⧖ 2026-10-19
- **Blocks:** [bob-cli-a0.7](bob-cli-a0.7.md) ✓ · ⧖ 2026-10-19

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-a0.3](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-a0.3.md) | [bob-cli-a0.3](bob-cli-a0.3.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`f8ef162`](https://github.com/bobs-org/bob-cli/commit/f8ef1628621b8be6c8188eeb0e8ea0046bd007d9) | feat(docs): complete Bob visual identity and homepage | [bob-cli-a0.3](bob-cli-a0.3.md) | 2026-10-19 23:04:00 EDT |
