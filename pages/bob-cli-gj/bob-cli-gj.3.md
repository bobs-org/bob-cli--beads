# Bead: bob-cli-gj.3 — Bob Mac Capture note-pull preview, card, and notification

[Bead Pages](../README.md) / [bob-cli-gj](README.md) / bob-cli-gj.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.17g](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.17g.md) · **Assignee:** `bob-cli-gj.3` · **Size:** medium
**Created:** 2026-11-03 11:56:54 EST · **Closed:** 2026-11-04 09:50:52 EST
**Plan:** [202611/note\_pull.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/note_pull.md)

## Description

mac: decode `note_pull` results and render them. Covers the preview card with the Pull In verb, the Pull-In card glyph, tint, lanes, and footer, the calm empty state, the Shift-Return list helper, and notifications. Includes fixtures captured from the real bob and compiled, tested Swift.

## Notes

[2026-11-03T22:23:38Z · bob-cli-gj.2.1.4--4] Fixture handoff: tests/fixtures/note_pull/README.md; generator tests/fixtures/note_pull/generate.py; CLI outputs np1/{stdout.json,human.txt}, np2/{stdout.json,human.txt}, np10-empty/stdout.json, np10-folded/stdout.json, np12/stdout.json, np13/stdout.json, np16/{choice.json,routed.json}; benchmark tests/fixtures/note_pull/benchmark.py and performance.md. Producing source: HEAD 3d1822be plus verification working-tree changes (release rebuilt from that tree). Latest 20-sample p95: sase 82.60 ms (target 70 ms missed); mac_inbox 44.88 ms (empty-pull refusal on source vault).

[2026-11-04T14:25:15Z · bob-cli-gj.3--2] PROPOSED FOLLOW-UP: Fix docs-check generated drift: cached Bob CLI glossary strand task-merge.md lacks front matter; reproduced identically on clean Mac Capture base 2940666 after lint passed.

[2026-11-04T14:50:52Z · bob-cli-gj.3--4] Implemented note-pull decoding and presentation, Pull-In card behavior, calm empty refusal, Shift-Return list helper, notifications, real-bob fixtures, and docs. Verified portable-check and Mac scratch-copy bundle.sh plus just typecheck-tests pass; docs lint passes. Full docs-check remains blocked by the task-merge.md generated-drift failure reproduced on clean base 2940666 and recorded above as a proposed follow-up. epic-symbols reported none.

## Dependencies

- **Depends on:** [bob-cli-gj.2](bob-cli-gj.2.md) ✓ · ⧖ 2026-11-03

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-gj.3](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-gj.3.md) | [bob-cli-gj.3](bob-cli-gj.3.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-mac-capture | [`bob-mac-capture@206c4b8`](https://github.com/bobs-org/bob-mac-capture/commit/206c4b834917163683cf4ebe8bafc02a965840dd) | feat(capture): present note-pull offers in Mac Capture | [bob-cli-gj.3](bob-cli-gj.3.md) | 2026-11-04 09:51:52 EST |
