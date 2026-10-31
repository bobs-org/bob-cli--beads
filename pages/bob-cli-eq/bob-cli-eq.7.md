# Bead: bob-cli-eq.7 — Real-Obsidian verification, visual polish, and docs

[Bead Pages](../README.md) / [bob-cli-eq](README.md) / bob-cli-eq.7

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.b5](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.b5.md) · **Assignee:** `bob-cli-eq.7` · **Size:** medium
**Created:** 2026-10-30 16:10:20 EDT · **Closed:** 2026-10-30 20:50:25 EDT
**Plan:** [202610/obsidian\_task\_wikilinks.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/obsidian_task_wikilinks.md)

## Description

review: Chromium previews and a real-Obsidian e2e on athena, polish driven by the screenshots, the final docs pass, and deployment.

## Notes

[2026-10-31T00:48:34Z · bob-cli-eq.7] Chromium previews: 36 PNGs on athena via /usr/bin/google-chrome (scripts/preview-task-wikilink-picker.cjs). Live Obsidian e2e PASS on athena xvfb-run -a node scripts/obsidian-task-wikilink-e2e.cjs -e /snap/bin/obsidian (Live Preview + Source auto-open, burst, Enter/undo/Escape/Backspace, ID-less naming, Pomodoro link+promote+retype, fenced and Depends-On never open). Smoke: PASS (layout-ready 452ms, heap 72.5 MiB, 4 editor mounts). just docs-check PASS. npm run docs:check PASS. npm run build PASS. npm run validate PASS. npm test 4546 pass / 5 fail (unrelated; see follow-up). bob plugins sync --repo <bob-plugins> --no-pull copied block-id-prompt main.js+styles.css; refused bob-command-mode and bob-navigation-hotkeys from other workspace uncommitted deploys (did not -F).

[2026-10-31T00:48:35Z · bob-cli-eq.7] PROPOSED FOLLOW-UP: skipped decisions:obsidian-task-wikilinks-mirror-bob — decision_record=no forbids editing that strand; land agent should add it via /sase_memory_write when authorized.

[2026-10-31T00:48:36Z · bob-cli-eq.7] PROPOSED FOLLOW-UP: npm test 5 failures on this tree that this phase did not touch: test-block-id-prompt-task-wikilink-index-performance.cjs keystroke rank 13.1ms > 12ms budget; test-ledger-tools-freshness-namespace.cjs reload event; test-ledger-tools-gcal-events.cjs create listener; test-ledger-tools-note-ready.cjs startup storm 1!==2; test-ledger-tools-relation-index.cjs scan after layout-ready. Wikilink picker/runtime/pomodoro/e2e self-tests 28/28 pass.

[2026-10-31T00:50:25Z · bob-cli-eq.7] Verified: 36 Chromium PNGs (9 states x 900/600 x light/dark) via scripts/preview-task-wikilink-picker.cjs on athena; locator CSS keeps folder shrink + filename/id unclipped (done/2026/blender#^inst). Live Obsidian e2e PASS on athena xvfb-run -a node scripts/obsidian-task-wikilink-e2e.cjs -e /snap/bin/obsidian (Live Preview + Source auto-open/pair/escape, burst insert/caret/undo, backspace (), ID-less names, Pomodoro insert [[Tasks#^ready-work]] + promote [*] + [type:: FIX] + schedule/log, fenced/Depends-On never open). Smoke PASS 452ms/72.5MiB. just docs-check PASS. npm run docs:check PASS. npm run validate PASS. npm run build PASS (088 967, 089 154). Wikilink picker/runtime/pomodoro/e2e self-tests 28/28. bob plugins sync --no-pull copied block-id-prompt. decision_record=no skipped; follow-ups recorded. No leftover --epic-symbol entries.

## Dependencies

- **Depends on:** [bob-cli-eq.6](bob-cli-eq.6.md) ✓ · ⧖ 2026-10-30

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-eq.7](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-eq.7/README.md) | [bob-cli-eq.7](bob-cli-eq.7.md) | 2 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`3ca356c`](https://github.com/bobs-org/bob-cli/commit/3ca356c654c459137a3e667f5536c21a0461484b) | docs(guides): name (( as the fastest task wikilink path | [bob-cli-eq.7](bob-cli-eq.7.md) | 2026-10-30 20:51:43 EDT |
| bob-plugins | [`bob-plugins@8ef763a`](https://github.com/bobs-org/bob-plugins/commit/8ef763a8914b6784de534a88b92c57c7044bcc53) | feat(block-id-prompt): polish (( picker layout and add Obsidian e2e | [bob-cli-eq.7](bob-cli-eq.7.md) | 2026-10-30 20:52:09 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-eq.7][1] | Need the phase scope and design file | 5 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-eq.7/README.md

<!-- sase:referenced-by:end -->
