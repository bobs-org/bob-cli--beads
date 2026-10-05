# Bead: bob-cli-4f.3 — Split the ledger-tools freshness test suite

[Bead Pages](../README.md) / [bob-cli-4f](README.md) / bob-cli-4f.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.54](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.54.md) · **Assignee:** `bob-cli-4f.3` · **Size:** large
**Created:** 2026-10-04 21:42:18 EDT · **Closed:** 2026-10-04 22:37:39 EDT
**Plan:** [202610/split\_largest\_bob\_plugins\_js\_files\_1.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/split_largest_bob_plugins_js_files_1.md)

## Description

ledger-freshness-tests: split the 2895-line test-ledger-tools-freshness.cjs into a shared harness and per-area test files of at most 1000 lines each, losing no tests; the agent plans the final split.

## Notes

[2026-10-05T02:37:27Z · bob-cli-4f.3] PROPOSED FOLLOW-UP: Adopt ledger-tools-harness in existing sibling tests — freshness-footer and freshness-mark duplicate the same loader stubs; migrate compatible siblings in a separate refactor while preserving specialized surface stubs.

[2026-10-05T02:37:39Z · bob-cli-4f.3] Split 2895-line test-ledger-tools-freshness.cjs (base 2486da9) into ledger-tools-harness.cjs (345 lines) + six area files (placement 162, states 528, namespace 575, review-model 636, queue 268, tracking 501). Test-name multiset identical (57); moved blocks byte-identical to base (harness modulo dropped node:test require + new exports). Per-file: 4/12/8/11/12/10 pass; combined 57 pass, 0 fail/skip/cancel/todo. package.json lists the six explicitly, excludes old file and harness. README tree + testing section updated with explicit six-file run command. npm run build:check, npm test (1809 pass), npm run validate (6/6) all green. bob plugins sync --no-pull exit 0 (4 copied, 12 unchanged). epic-symbols clean.

## Dependencies

- **Depends on:** [bob-cli-4f.2](bob-cli-4f.2.md) ✓ · ⧖ 2026-10-04
- **Blocks:** [bob-cli-4f.4](bob-cli-4f.4.md) ✓ · ⧖ 2026-10-04

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-4f.3](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-4f.3.md) | [bob-cli-4f.3](bob-cli-4f.3.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@474d6fe`](https://github.com/bobs-org/bob-plugins/commit/474d6fe063f0096296728b52702e4331d0371be6) | refactor(test): split ledger-tools freshness suite | [bob-cli-4f.3](bob-cli-4f.3.md) | 2026-10-04 22:38:30 EDT |
