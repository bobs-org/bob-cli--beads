# Bead: bob-cli-4f.1 — Split block-id-prompt main.js onto the fragment source build

[Bead Pages](../README.md) / [bob-cli-4f](README.md) / bob-cli-4f.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.54](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.54.md) · **Assignee:** `bob-cli-4f.1` · **Size:** large
**Created:** 2026-10-04 21:42:18 EDT · **Closed:** 2026-10-04 22:01:02 EDT
**Plan:** [202610/split\_largest\_bob\_plugins\_js\_files\_1.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/split_largest_bob_plugins_js_files_1.md)

## Description

block-id-prompt-source: move the 6880-line hand-edited block-id-prompt plugin onto src/fragments.json, with mixin-split plugin methods and every fragment at most 1000 lines, verified by parity checks; the agent plans the final split.

## Notes

[2026-10-05T02:01:02Z · bob-cli-4f.1] Parity: 64 helpers, 73 methods; npm test 1809/1809 and npm run validate pass; all 17 fragments syntax-check and are <=688 lines; bob plugins sync block-id-prompt 1.21.2 succeeded and vault reports synced.

## Dependencies

- **Blocks:** [bob-cli-4f.2](bob-cli-4f.2.md) ✓ · ⧖ 2026-10-04

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-4f.1](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-4f.1.md) | [bob-cli-4f.1](bob-cli-4f.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@03f0c17`](https://github.com/bobs-org/bob-plugins/commit/03f0c177989871805561e84cd16f7310cdbed32f) | refactor(block-id-prompt): split main.js onto the fragment source build | [bob-cli-4f.1](bob-cli-4f.1.md) | 2026-10-04 22:03:15 EDT |
