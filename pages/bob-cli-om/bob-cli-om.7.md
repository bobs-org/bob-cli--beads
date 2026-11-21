# Bead: bob-cli-om.7 — Record Card typed stages and link-stage convergence

[Bead Pages](../README.md) / [bob-cli-om](README.md) / bob-cli-om.7

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.5o.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.5o.linker.w0.md) · **Assignee:** `bob-cli-om.7` · **Size:** medium
**Created:** 2026-11-21 10:32:18 EST · **Closed:** 2026-11-21 14:36:06 EST
**Plan:** [202611/prose\_wikilink\_completion.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/prose_wikilink_completion.md)

## Description

record-card: attach proseField to the Record Card's text, suggest, and list stages (S15). Converge the link stage onto the engine in field mode, retiring recordCardLinkCandidates and its bracket bug, and survive the per-keystroke repaint.

## Notes

[2026-11-21T19:35:31Z · bob-cli-om.7] Real-Chromium check (headless Playwright Chromium 1248 loading the built nav + ledger-tools bundles with Obsidian shims, trusted CDP input; no Obsidian binary on apollo): Record Card text stage — typing "best near [[cra" keeps the same textarea element and focus across per-keystroke repaints, band opens; Enter inserts [[cranford]] with no save; one Ctrl+Z restores "best near [[cra"; Esc closes only the band; Shift+Enter with band open saves nothing; held (autoRepeat) Enter after accept saves nothing; IME composition (imeSetComposition then commit) keeps the element, focus, and draft. Link stage (field mode) — "cra" + Tab inserts [[cranford]] without advancing; one Ctrl+Z restores "cra"; Enter accept then a second Enter saves field.set spot "[[cranford]]".

[2026-11-21T19:35:38Z · bob-cli-om.7] Discovered and fixed in nav 189b: acceptRow armed the held-Enter swallow on every acceptance, so after a Tab or click accept the next Enter was eaten (Record Card link stage needed Enter twice to save). Now only an Enter accept arms it; nav test "Tab and click accepts leave the next Enter to the host" pins it.

[2026-11-21T19:35:44Z · bob-cli-om.7] PROPOSED FOLLOW-UP: Move or relax two load-sensitive 25 ms budgets in test:unit — scripts/test-ledger-tools-event-link-times.cjs "perf — one build over a 200-link ledger stays under 25 ms" and scripts/test-ledger-tools-frees-marks.cjs "200-link / 2000-task build stays within the 25 ms budget" fail under parallel node --test at host load avg 130-150 (106-176 ms) and pass in isolation; move them to test:perf (concurrency 1) or measure CPU time like the prose perf test.

[2026-11-21T19:35:51Z · bob-cli-om.7] PROPOSED FOLLOW-UP: docs/bob-navigation-hotkeys.md exceeds the 6000-word reference budget on the clean base (6302 words after the modal-prompts phase; 6307 with this phase), so npm run docs:check fails at lint; split the Wikilink completion in prompts section (or other long sections) into its own page. develop/plugin-apis.md is also over its 8000-word warning budget (8308).

[2026-11-21T19:36:06Z · bob-cli-om.7] S15 landed in bob-plugins (ledger-tools 1.154.0, nav 2.100.0): proseField attaches to the Record Card text, suggest, and text/link list-item inputs (inline) and the link stage (field mode, link lists too) with sourcePath = record path; date/number/URL/choices stay literal. Typed stages keep their live input + band host across repaints (242o body reconcile around the kept stage, 242q painter reuses the input and never rewrites value mid-IME), with rebind as fallback. Explicit consumer: Esc/q/Ctrl+[ ladder calls backOut() first; typed-stage keys go to handleKeydown before Enter save, Tab, list Enter, and suggest cycling; an open band never lets Enter save. Retired recordCardLinkCandidates, the link list, pick-link, and the link branch of recordMoveSuggest; recordCardParseLinkDraft now splits target/subpath/|Alias. Docs: record-card.md Wikilink completion section, nav + plugin-apis notes. Verified: 13 new tests (scripts/test-ledger-tools-record-card-prose-field.cjs) + nav Tab/click swallow test; npm test 8290 pass with only 2 pre-existing load-sensitive 25 ms budgets failing (pass in isolation); test:perf 13/13; validate 12/12; strict docs build + offline link/fragment check pass (docs:check lint fails on the pre-existing nav reference word budget); real-Chromium CDP walkthrough of text and link stages (undo, IME, Esc, held Enter, Shift+Enter, save); bob plugins sync deployed.

## Dependencies

- **Blocks:** [bob-cli-om.10](bob-cli-om.10.md) ◐ · ⧖ 2026-11-21
- **Depends on:** [bob-cli-om.3](bob-cli-om.3.md) ✓ · ⧖ 2026-11-21

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-om.7](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-om.7/README.md) | [bob-cli-om.7](bob-cli-om.7.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@e6d7aed`](https://github.com/bobs-org/bob-plugins/commit/e6d7aed7fdc21825d56a785618e730e56af86a0b) | feat(ledger-tools): complete \[\[ links in the Record Card typed stages | [bob-cli-om.7](bob-cli-om.7.md) | 2026-11-21 14:36:58 EST |
