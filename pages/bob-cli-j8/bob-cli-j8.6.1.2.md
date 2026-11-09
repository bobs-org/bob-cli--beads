# Bead: bob-cli-j8.6.1.2 — Notebook catalog cards and live chips in both Obsidian views

[Bead Pages](../README.md) / [bob-cli-j8.6.1](bob-cli-j8.6.1.md) / bob-cli-j8.6.1.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.bob-cli-j8.6](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-j8.6.md) · **Assignee:** `bob-cli-j8.6.1.2` · **Size:** medium
**Created:** 2026-11-09 15:15:01 EST · **Closed:** 2026-11-09 18:20:57 EST
**Plan:** [202611/notebook\_catalog\_ui.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/notebook_catalog_ui.md)

## Description

notebook-ui-catalog: use the shared notebook report to style and decorate generated catalogs in Reading view and Live Preview, including host hue, tree rules, row counts, recency, add-summary navigation, and the heading sync action; test both surfaces and preserve Markdown bytes and native links.

## Notes

[2026-11-09T23:20:57Z · bob-cli-j8.6.1.2] Notebook catalog UI landed in bob-ledger-tools (241b/c/d): generated [!notebooks] cards with live chips, host hue, ↻ sync, and add-summary. Verified node --test scripts/test-ledger-tools-notebook-catalog.cjs (19/19) plus notebooks-data/api neighbors; npm run build:check and validate passed; bob plugins sync --repo $PWD --no-pull deployed main.js and styles.css. Zero note-byte writes; 🧩 project groups skipped; LP gated on editorLivePreviewField with actual callout DOM paint. No leftover --epic-symbol entries.

## Dependencies

- **Depends on:** [bob-cli-j8.6.1.1](bob-cli-j8.6.1.1.md) ✓ · ⧖ 2026-11-09
- **Blocks:** [bob-cli-j8.6.1.3](bob-cli-j8.6.1.3.md) ◐ · ⧖ 2026-11-09

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-j8.6.1.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-j8.6.1.2/README.md) | [bob-cli-j8.6.1.2](bob-cli-j8.6.1.2.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@56b3604`](https://github.com/bobs-org/bob-plugins/commit/56b36047d004aec0fa3b7649c86ef9683ee475b1) | feat(ledger-tools): paint live notebook catalog chips in Reading and Live Preview | [bob-cli-j8.6.1.2](bob-cli-j8.6.1.2.md) | 2026-11-09 18:22:03 EST |
