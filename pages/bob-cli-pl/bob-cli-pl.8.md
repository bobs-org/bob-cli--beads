# Bead: bob-cli-pl.8 — The Lives under stage with consequence preview and catalog refresh (bob-plugins)

[Bead Pages](../README.md) / [bob-cli-pl](README.md) / bob-cli-pl.8

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.5y.linker.w1](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.5y.linker.w1.md) · **Assignee:** `bob-cli-pl.8` · **Size:** medium
**Created:** 2026-11-22 20:56:41 EST · **Closed:** 2026-11-25 18:27:41 EST
**Plan:** [202611/area\_project\_cards.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/area_project_cards.md)

## Description

editor-parent: add the restricted home picker (reusing the nav-hotkeys parent picker model), the bob dry-run consequence preview, and post-apply catalog syncs inside the guarded session, with byte-exact undo.

## Notes

[2026-11-25T23:27:41Z · bob-cli-pl.8] Implemented editor-parent in bob-plugins. Nav: new 735-parent-picker-choose.js exposes versioned api.parentPicker v1 (list/validate/choose) reusing the 208 picker model with no writes, wired into fragments.json and docs/develop/plugin-apis.md. Ledger: new 298aa parent stage replaces the generic-text parent handler via the setting-handler seam — ranked home list with kind/hue pips and refusal text, dry-run setting.set parent consequence preview with Enter on current preview only, post-apply run of exactly bob's syncs[] through apiAreasSync/apiProjectsSync/apiAlbumSync/apiNotebookSync with Refreshing/refreshed/undo reporting, and undo re-running the same syncs; 682 gesture untouched. Docs updated in property-editor.md and bob-navigation-hotkeys.md. Verified: npm run build + build:check clean, validate 12/12, docs inventory check clean, 74 tests pass (2 new files + parent-change + settings-rows + setting-actions), 86 more pass (stages/entrypoints/shell/album-record/e2e). docs:check lint fails identically on the clean tree (pre-existing word-budget overruns). bob plugins sync refused per AGENTS.md — sibling workspaces hold uncommitted deployed builds and agents still running — so no -F; land agent syncs.

## Dependencies

- **Depends on:** [bob-cli-pl.6](bob-cli-pl.6.md) ✓ · ⧖ 2026-11-22
- **Blocks:** [bob-cli-pl.9](bob-cli-pl.9.md) ◐ · ⧖ 2026-11-22

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-pl.8](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-pl.8/README.md) | [bob-cli-pl.8](bob-cli-pl.8.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@0d319a5`](https://github.com/bobs-org/bob-plugins/commit/0d319a535b5e59ff905153400165fdcbaaf9575e) | feat(property-editor): Lives under stage with consequence preview and catalog refresh | [bob-cli-pl.8](bob-cli-pl.8.md) | 2026-11-25 18:36:34 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-pl.8][1] | Need the phase scope and design file | 1 |
| read-by | [agent:fx][2] | Map the pl epic dependency graph | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-pl.8/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.fx/README.md

<!-- sase:referenced-by:end -->
