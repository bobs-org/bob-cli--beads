# Bead: bob-cli-on.9 — Render requirements in Obsidian

[Bead Pages](../README.md) / [bob-cli-on](README.md) / bob-cli-on.9

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.1ex](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.1ex.md) · **Assignee:** `bob-cli-on.9` · **Size:** medium
**Created:** 2026-11-21 11:13:26 EST · **Closed:** 2026-11-21 17:25:26 EST
**Plan:** [202611/task\_requirements.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/task_requirements.md)

## Description

ledger-marks: draw the depth-aware ⌗ run in the owner's ink in Live Preview and Reading view with state styling, hidden unclickable checkboxes, the session toggle, tooltips, and freshness guards in bob-ledger-tools.

## Notes

[2026-11-21T18:10:20Z · bob-cli-on.9] PROPOSED FOLLOW-UP: Baseline just docs-check still fails on docs/reference/vault-format.md at 6037/6000 (tracked by bob-cli-oc); docs/develop/plugins/plugin-apis.md remains a tracked 8165/8000 warning (bob-cli-ob). This phase brought the bob-ledger-tools reference page under its cap.

[2026-11-21T18:17:07Z · bob-cli-on.9] PROPOSED FOLLOW-UP: After aligning bob-plugins to c4953d3, clean-base docs:check still reports docs/develop/plugins/plugin-apis.md 8274/8000 and docs/reference/plugins/bob-navigation-hotkeys.md 6247/6000 (tracked by bob-cli-ob), plus docs/reference/vault-format.md 6037/6000 (tracked by bob-cli-oc). The bob-ledger-tools reference page is now under cap.

[2026-11-21T18:20:23Z · bob-cli-on.9] PROPOSED FOLLOW-UP: Full npm test once missed the existing frees-marks 200-link/2000-task 25ms timing test (56ms); the isolated same test passed at 23.6ms. Existing tracker: bob-cli-io.

[2026-11-21T18:34:47Z · bob-cli-on.9] PROPOSED FOLLOW-UP: The latest full npm test also missed the existing frees-marks 200-link/2000-task 25ms timing test (27ms); isolated run passed at 23.6ms. The repeat is tracked by bob-cli-io.

[2026-11-21T22:25:26Z · bob-cli-on.9--2] Verified requirement and freshness coverage with 198 focused tests passing. Built bob-plugins and confirmed all generated plugins unchanged. A second full npm test passed: 8,423 unit tests, 0 failures, 4 skips, and all 13 perf tests; the initial full run had 2 transient failures. Docs inventory is current; docs:check still reports the tracked plugin-apis and navigation-hotkeys budget overages, and did not flag docs/bob-ledger-tools.md. Clean sync from the landed checkout succeeded twice without -F; final sync reports bob-ledger-tools up to date.

## Dependencies

- **Depends on:** [bob-cli-on.1](bob-cli-on.1.md) ✓ · ⧖ 2026-11-21
- **Blocks:** [bob-cli-on.16](bob-cli-on.16.md) ◐ · ⧖ 2026-11-21

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-on.9](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-on.9.md) | [bob-cli-on.9](bob-cli-on.9.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`250c305`](https://github.com/bobs-org/bob-cli/commit/250c3053d652d1d6b48299557fc8272a809bab88) | docs(tasks): document requirement marks | [bob-cli-on.9](bob-cli-on.9.md) | 2026-11-21 13:37:40 EST |
