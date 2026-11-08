# Bead: bob-cli-iq.2 — Pure annotation locator

[Bead Pages](../README.md) / [bob-cli-iq](README.md) / bob-cli-iq.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.3o.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.3o.linker.w0.md) · **Assignee:** `bob-cli-iq.2` · **Size:** medium
**Created:** 2026-11-08 10:40:42 EST · **Closed:** 2026-11-08 10:53:52 EST
**Plan:** [202611/highlights\_annotation\_page\_jump.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/highlights_annotation_page_jump.md)

## Description

locator: in bob-plugins, a pure fragment that maps a ref-note line to its managed ^h- block. It returns the block kind, the 1-based page (caption or piece), a snippet, and the rail range. It also parses 🔖 links and the archive PDF wikilink. Tested against golden fixtures copied from bob-cli.

## Notes

[2026-11-08T15:53:52Z · bob-cli-iq.2] Locator fragment 677a ships: parseRefPageLabel, locateRefAnnotation, findRefAnnotationBlockLine, parseRefBookmarkLink, parseRefArchivePdfLink, mirrored on bob-cli generated-body grammar. 6 golden fixtures in scripts/fixtures/ref-annotations/; 14 new tests pass; full npm test 5709 pass/0 fail; npm run validate clean; bob-navigation-hotkeys synced to vault (-F over stale d45d8f7-era bundle, backup kept).

## Dependencies

- **Blocks:** [bob-cli-iq.3](bob-cli-iq.3.md) ◐ · ⧖ 2026-11-08

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-iq.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-iq.2/README.md) | [bob-cli-iq.2](bob-cli-iq.2.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@cedcb1c`](https://github.com/bobs-org/bob-plugins/commit/cedcb1c6b36b2021b94254c688fc1e0444ecfad0) | feat(navigation): add pure ref annotation locator for Highlights page jumps | [bob-cli-iq.2](bob-cli-iq.2.md) | 2026-11-08 10:55:05 EST |
