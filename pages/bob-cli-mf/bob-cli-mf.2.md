# Bead: bob-cli-mf.2 — Pure arrangement engine

[Bead Pages](../README.md) / [bob-cli-mf](README.md) / bob-cli-mf.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.51.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.51.linker.w0.md) · **Assignee:** `bob-cli-mf.2` · **Size:** medium
**Created:** 2026-11-16 15:38:38 EST · **Closed:** 2026-11-16 16:24:11 EST
**Plan:** [202611/schema\_editor\_arrange\_and\_emoji.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/schema_editor_arrange_and_emoji.md)

## Description

arrange-engine: add a DOM-free projected-order model with nudges, edges, gap placement, local undo, anchor rebase, and a save marker. Add album and bank envelope compilers checked by a simulator, plus gap-hint labels and FLIP planning.

## Notes

[2026-11-16T21:23:49Z · bob-cli-mf.2] PROPOSED FOLLOW-UP: Full npm test has unrelated navigation contract failures tracked by bob-cli-md and the block-marks date-sensitive fixture guard tracked by bob-cli-m8; the three focused failures reproduced identically on the clean bob-plugins base e35afc1.

[2026-11-16T21:24:11Z · bob-cli-mf.2] Implemented the pure arrangement engine, compiler/simulator checks, undo/rebase/save markers, gap labels, and FLIP planning. Verified build and build:check, new suite 13/13, docs:check, clean-base reproduction of the unrelated full-test failures, and deployment of bob-ledger-tools 1.121.0.

## Dependencies

- **Depends on:** [bob-cli-mf.1](bob-cli-mf.1.md) ✓ · ⧖ 2026-11-16
- **Blocks:** [bob-cli-mf.4](bob-cli-mf.4.md) ◐ · ⧖ 2026-11-16

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-mf.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-mf.2/README.md) | [bob-cli-mf.2](bob-cli-mf.2.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@afbb325`](https://github.com/bobs-org/bob-plugins/commit/afbb325018212e38dadbab900ca3ae1d5bd8b8e6) | feat(bob-ledger-tools): add pure schema arrangement engine | [bob-cli-mf.2](bob-cli-mf.2.md) | 2026-11-16 16:37:00 EST |
