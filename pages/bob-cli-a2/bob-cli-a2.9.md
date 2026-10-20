# Bead: bob-cli-a2.9 — nav relation grammar twin, planner, mint, writer, and api.relations

[Bead Pages](../README.md) / [bob-cli-a2](README.md) / bob-cli-a2.9

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.research.53.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.research.53.linker.w0.md) · **Assignee:** `bob-cli-a2.9` · **Size:** medium
**Created:** 2026-10-20 09:08:22 EDT · **Closed:** 2026-10-20 10:43:27 EDT
**Plan:** [202610/task\_relations.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/task_relations.md)

## Description

nav-writer: add the JS twin of the LINKS / LINKED FROM planners (LW and LM bytes equal to Rust) and applyRelationEdit. It writes one same-note transaction, mints inside the source's transaction, and sends cross-note mirror follow-ups with an honest failure suffix. Add the kill switch, notices, a machine-write annotation, and nav api.relations (removeLink now, openStage once the stages land, v1 after both). No UI.

## Notes

[2026-10-20T14:40:25Z · bob-cli-a2.9] --list

[2026-10-20T14:43:10Z · bob-cli-a2.9] PROPOSED FOLLOW-UP: Pre-existing npm test failures on clean master (identical with and without this phase): test-ledger-tools-unblocked-glyph.cjs Live Preview/Reading glyph tests (4 fails: 0!==1 / undefined.value); test-navigation-decision-card-handlers.cjs "Keep counts once and saturates at 999" (match against "Update Bob Ledger Tools to record review stats"); test-navigation-hotkeys-forward-promotion.cjs "forward conversion carries a Depends-On line and reverse restores it" (doesNotMatch /Work_ship#^prj/ after reverse, leftover BLOCKS). Recorded so land can triage; none are caused by applyRelationEdit.

[2026-10-20T14:43:27Z · bob-cli-a2.9] Nav-writer landed in bob-plugins 2.48.0: JS twin of LINKS/LINKED FROM planners (086; LW1–LW14, LK20, Rule 6), applyRelationEdit + same-note mint + cross-note follow-ups (594/595; LG1/2/4/6/13/14), relations.linked_from_lines kill switch, RELATIONS_MACHINE_WRITE_ANNOTATION skip in 600, notices with 🪢, nav api.relations v0 (removeLink works; openStage settles {ok:false,reason:unavailable}). inverse_phrases=builtin, linked_from_remove=yes. Glossary Task Relation already present; no decisions strand. Fragment sizes 086=793, 594=589, 595=177, 486=35. npm run build:check + validate + relation/blocks/mirror tests pass (72). Full npm test: 3311 pass, 6 fail identically on clean master (PROPOSED FOLLOW-UP noted). Deployed with bob plugins sync --repo <linked> -p bob-navigation-hotkeys. No leftover --epic-symbol entries.

## Dependencies

- **Blocks:** [bob-cli-a2.11](bob-cli-a2.11.md) ◐ · ⧖ 2026-10-20
- **Depends on:** [bob-cli-a2.3](bob-cli-a2.3.md) ✓ · ⧖ 2026-10-20

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-a2.9](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-a2.9/README.md) | [bob-cli-a2.9](bob-cli-a2.9.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@1497854`](https://github.com/bobs-org/bob-plugins/commit/1497854c7d20ed503eae4231ff9d50ec679cee97) | feat(bob-navigation-hotkeys): add relation planner, writer, and api.relations v0 | [bob-cli-a2.9](bob-cli-a2.9.md) | 2026-10-20 10:44:47 EDT |
