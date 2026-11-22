# Bead: bob-cli-on.15.1.4 — Render requirement branches and wire their keyboard actions

[Bead Pages](../README.md) / [bob-cli-on.15.1](bob-cli-on.15.1.md) / bob-cli-on.15.1.4

**Status:** ◐ in_progress · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-on.15](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-on.15.md) · **Assignee:** `bob-cli-on.15.1.4` · **Size:** medium
**Created:** 2026-11-22 14:56:48 EST
**Plan:** [202611/mac\_requirement\_close\_card.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/mac_requirement_close_card.md)

## Description

card_ui: render requirement sections first with bob-authored copy, depth glyphs, branch folds, consequences, scope summaries and accessible states. Wire Ctrl+X, Ctrl+Shift+X, Ctrl+Shift+T, Space/Tab and Ctrl+J through the existing router, controller and reason/recall UI. Preserve ordinary offer behavior, text focus, mark-all exclusions and Esc semantics; follow the card_ui section.

## Notes

[2026-11-22T23:20:55Z · bob-cli-on.15.1.4] card_ui implementation landed for review: requirement sections with Bob copy/scope/history, depth glyphs, folds, consequences, summary and accessible states; Ctrl+X Met, Ctrl+Shift+X Drop, Ctrl+Shift+T Carry, Space Carry-plus-pull, Tab advance, Ctrl+J pin through router/controller/reason-recall UI. Portable: just portable-check green (2699 tests, 0 failures). Scratch Mac: bundle.sh exit 0, just typecheck-tests PASS all 4 targets. macOS CI staged as p2rf1k via Scripts/macos-ci-check; exact-SHA verdict pending.

## Dependencies

- **Depends on:** [bob-cli-on.15.1.3](bob-cli-on.15.1.3.md) ✓ · ⧖ 2026-11-22
- **Blocks:** [bob-cli-on.15.1.5](bob-cli-on.15.1.5.md) ◐ · ⧖ 2026-11-22

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-on.15.1.4](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-on.15.1.4.md) | [bob-cli-on.15.1.4](bob-cli-on.15.1.4.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-mac-capture | [`bob-mac-capture@7006f3e`](https://github.com/bobs-org/bob-mac-capture/commit/7006f3e7f8a3f3b4ec266029b3934bac62605551) | feat(capture): render requirement branches and wire their keyboard actions | [bob-cli-on.15.1.4](bob-cli-on.15.1.4.md) | 2026-11-22 18:23:32 EST |
