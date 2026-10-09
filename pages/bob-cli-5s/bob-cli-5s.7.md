# Bead: bob-cli-5s.7 — Hotkeys, Highlights takeover, menu, settings, and coexistence with Capture

[Bead Pages](../README.md) / [bob-cli-5s](README.md) / bob-cli-5s.7

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** `bbugyi200.apollo.5z` · **Assignee:** `bob-cli-5s.7` · **Size:** medium
**Created:** 2026-10-08 19:32:40 EDT · **Closed:** 2026-10-09 06:16:50 EDT
**Plan:** [202610/bob\_refs\_panel.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/bob_refs_panel.md)

## Description

refs-entry-points: wire the library and panel into AppDelegate, register the global ⌃⇧⌘R hotkey and the Highlights-frontmost takeover, add the References status-menu item and Settings section, keep only one Bob panel visible, refresh Today after captures, and test it all.

## Notes

[2026-10-09T10:05:19Z · bob-cli-5s.7] PROPOSED FOLLOW-UP: Add decisions strand refs-panel-is-a-thin-client (Bob Refs ranks bob reference index, opening never mutates vault); refs_decision_memory=%auto left it off

[2026-10-09T10:16:34Z · bob-cli-5s.7] PROPOSED FOLLOW-UP: master CI red on sibling refs-inspector errors (bob-cli-5s.8): RefsInspectorLoader.swift:291 calls String? thumbSHA as function, :466 missing await on async openTasks, RefsPanelModel.swift:229 self-use-before-init from inspector init rewrite; CI run 37916221821. Entry-points sources compile clean; unblocks entry-points tests once fixed.

[2026-10-09T10:16:50Z · bob-cli-5s.7] Entry points wired in bob-mac-capture (3aabee1, build fix e1d696e, pushed, tree clean): coordinator, takeover (cmdO default per decision), global hotkey, menu row, Settings References section, capture-success Today refresh, recheck re-point. CI 37916221821 shows zero errors in entry-points files; 16 new + 2 updated tests authored but unrun (no host Swift toolchain; test stage blocked by sibling inspector errors in bob-cli-5s.8, recorded as follow-up). No epic-symbols left.

## Dependencies

- **Depends on:** [bob-cli-5s.2](bob-cli-5s.2.md) ✓ · ⧖ 2026-10-08
- **Depends on:** [bob-cli-5s.6](bob-cli-5s.6.md) ✓ · ⧖ 2026-10-08
- **Blocks:** [bob-cli-5s.9](bob-cli-5s.9.md) ✓ · ⧖ 2026-10-08

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-5s.7](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-5s.7/README.md) | [bob-cli-5s.7](bob-cli-5s.7.md) | 2 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-mac-capture | [`bob-mac-capture@3aabee1`](https://github.com/bobs-org/bob-mac-capture/commit/3aabee1c536d4fd7610d97422065674e0ed0c984) | feat(refs): wire entry points — hotkeys, Highlights takeover, menu, settings | [bob-cli-5s.7](bob-cli-5s.7.md) | 2026-10-09 06:06:36 EDT |
| bob-mac-capture | [`bob-mac-capture@e1d696e`](https://github.com/bobs-org/bob-mac-capture/commit/e1d696e3730a56a3e759c3880d5a7cb0febab68d) | fix(refs): repair entry-points build — coordinator names, Sendable path | [bob-cli-5s.7](bob-cli-5s.7.md) | 2026-10-09 06:12:57 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-5s.7][1] | Need the phase scope and design file | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-5s.7/README.md

<!-- sase:referenced-by:end -->
