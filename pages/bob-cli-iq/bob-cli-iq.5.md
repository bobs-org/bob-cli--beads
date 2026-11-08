# Bead: bob-cli-iq.5 — Availability chip, rail, and 📖 tooltip

[Bead Pages](../README.md) / [bob-cli-iq](README.md) / bob-cli-iq.5

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.3o.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.3o.linker.w0.md) · **Assignee:** `bob-cli-iq.5` · **Size:** medium
**Created:** 2026-11-08 10:40:43 EST · **Closed:** 2026-11-08 12:15:02 EST
**Plan:** [202611/highlights\_annotation\_page\_jump.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/highlights_annotation_page_jump.md)

## Description

hints: a status-bar chip and a line rail, both driven by the dry resolver, show what ⌘↵ will open. Adds a session toggle and the ledger-tools 📖 tooltip mention. Tests that the hint always matches what the key does.

## Notes

[2026-11-08T17:15:02Z · bob-cli-iq.5] Availability chip, highlighter rail, session toggle, and 📖 tooltip landed in bob-plugins. Fragment 677d (969 lines) plus 714 exports; chip click uses cached openHighlightsTarget; macOS-only chip mount keeps bracket-mode at one status item. Verified: npm run validate; docs:inventory:check; docs:check; 8/8 test-navigation-highlights-hints.cjs (chip states, keycaps, cached click, rail, debounce/skip-paint, unload, hint⇔key, toggle); related ref-pdf, notice, ledger tooltip, and bracket-mode suites green (71+16). bob plugins sync --no-pull deployed navigation-hotkeys main.js/styles.css and ledger-tools main.js. No --epic-symbol leftovers. Did not edit decisions-web (page_jump_decision_record=no).

## Dependencies

- **Depends on:** [bob-cli-iq.4](bob-cli-iq.4.md) ✓ · ⧖ 2026-11-08

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-iq.5](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-iq.5/README.md) | [bob-cli-iq.5](bob-cli-iq.5.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@fbf45e2`](https://github.com/bobs-org/bob-plugins/commit/fbf45e2572366d28cb7237d031d8e521dc9254f2) | feat(navigation): add Highlights availability chip, rail, and tooltip | [bob-cli-iq.5](bob-cli-iq.5.md) | 2026-11-08 12:16:26 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-iq.5][1] | Need full notes, design file, and remaining work details | 4 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-iq.5/README.md

<!-- sase:referenced-by:end -->
