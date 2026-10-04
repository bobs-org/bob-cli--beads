# Bead: bob-cli-47.5 — Split scripts/test-task-status-cycler.cjs

[Bead Pages](../README.md) / [bob-cli-47](README.md) / bob-cli-47.5

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.4z](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.4z.md) · **Assignee:** `bob-cli-47.5` · **Size:** large
**Created:** 2026-10-04 07:13:46 EDT · **Closed:** 2026-10-04 10:08:05 EDT
**Plan:** [202610/split\_largest\_bob\_plugins\_js\_files.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/split_largest_bob_plugins_js_files.md)

## Description

split-task-status-cycler-tests: reuse the harness convention to split the 179 cycler tests into per-area files. Keep the stub-assigned MarkdownView/TestModal classes shared through the harness.

## Notes

[2026-10-04T14:08:05Z · bob-cli-47.5] Split scripts/test-task-status-cycler.cjs into scripts/task-status-cycler-harness.cjs plus eleven per-area files. All 185 unique test names and complete top-level test bodies match the pre-split snapshot byte-for-byte; all 19 moved helper/fixture bodies are identical. node --check passes on the harness and area files. wc -l is at most 1000 for every created or touched hand-edited file (largest area file 903 lines; harness 460). Original scripts/test-task-status-cycler.cjs is gone and no remaining references to that exact filename. node --test scripts/test-task-status-cycler-*.cjs: 185 pass, 0 fail/skip/cancel, runtime names match the saved baseline. npm test: 1764 pass, 0 fail/skip/cancel. npm run validate: 6/6 plugins valid. npm run build:check passed. git diff --check clean. bob plugins sync --no-pull against the opened linked checkout: task-status-cycler up to date; also copied already-committed block-id-prompt and bob-ledger-tools drift that was in this checkout. sase bead epic-symbols bob-cli-47.5: no entries.

## Dependencies

- **Depends on:** [bob-cli-47.4](bob-cli-47.4.md) ✓ · ⧖ 2026-10-04

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-47.5](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-47.5.md) | [bob-cli-47.5](bob-cli-47.5.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@b854201`](https://github.com/bobs-org/bob-plugins/commit/b8542019284ca72e2dfe36b60c523edbe47b36ed) | refactor(test): split task-status-cycler suite | [bob-cli-47.5](bob-cli-47.5.md) | 2026-10-04 10:09:02 EDT |
