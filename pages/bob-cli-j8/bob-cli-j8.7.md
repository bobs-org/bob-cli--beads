# Bead: bob-cli-j8.7 — Obsidian block-ID prompt, pickers, and Create notebook here

[Bead Pages](../README.md) / [bob-cli-j8](README.md) / bob-cli-j8.7

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.3x.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.3x.linker.w0.md) · **Assignee:** `bob-cli-j8.7` · **Size:** medium
**Created:** 2026-11-09 12:11:27 EST · **Closed:** 2026-11-09 15:31:10 EST
**Plan:** [202611/bob\_notebooks.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/bob_notebooks.md)

## Description

plugins-notebook-gestures: make the block-ID prompt suggest IDs for plain note bullets, classify notebooks (with a notebook icon) in navigation, filter the parent picker by the notebook parent rules, and add a Create notebook here command backed by `bob notebooks create`.

## Notes

[2026-11-09T20:30:46Z · bob-cli-j8.7] PROPOSED FOLLOW-UP: bob-plugins docs-check fails on the clean base with 3 over-budget bob-cli reference pages (reference/json-outputs.md 6143 words, mac-capture/capture-panel.md 6006, mac-capture/keyboard.md 6028; cap 6000) - trim or split them; also reference/plugins/bob-navigation-hotkeys.md now sits at 5999/6000 words, so any future addition there needs a trim or a new page

[2026-11-09T20:30:51Z · bob-cli-j8.7] PROPOSED FOLLOW-UP: bob-cli docs/notebooks.md could link the new bob-plugins Notebook gestures page (docs/notebook-gestures.md: block-ID naming of note bullets, notebook picker icon, parent rules, Create notebook here) - left to the notebooks-wrapup docs audit (bob-cli-j8.10)

[2026-11-09T20:31:10Z · bob-cli-j8.7] Implemented in bob-plugins (committed via the final declaration): block-ID prompt names plain note bullets in both 015 copies (+resolver null paths, [created::] stripped, 'note' fallback); notebook kind + notebook-tabs icon in getChildNoteInfo/pickers; parent picker hides notebooks for area/project/ref/record sources and offers only area/project/notebook to a notebook, with commit-time refusal and teaching empty state; Create notebook here command + modal backed by new ledger api.notebooks.create (bob notebooks create); task move and inbox routing verified never to offer notebooks. Verified: npm test 5826 pass/1 skipped, npm run validate, build:check, real bob notebooks create (built from this workspace) driven through the ledger API against a temp vault (success, notebook_exists, notebook_id_invalid, notebook_parent_missing). docs:check fails only on 3 pre-existing over-budget bob-cli pages that fail identically on the clean base (recorded as PROPOSED FOLLOW-UP). bob plugins sync deployed all three plugins; block-id-prompt needed -F because the vault copy came from another checkout's dirty build, verified byte-identical to committed HEAD a2045cc first.

## Dependencies

- **Blocks:** [bob-cli-j8.10](bob-cli-j8.10.md) ◐ · ⧖ 2026-11-09
- **Depends on:** [bob-cli-j8.2](bob-cli-j8.2.md) ✓ · ⧖ 2026-11-09

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-j8.7](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-j8.7/README.md) | [bob-cli-j8.7](bob-cli-j8.7.md) | 0 |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-j8.7][1] | Need the phase scope and design file | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-j8.7/README.md

<!-- sase:referenced-by:end -->
