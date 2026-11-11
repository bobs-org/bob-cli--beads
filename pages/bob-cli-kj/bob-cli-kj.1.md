# Bead: bob-cli-kj.1 — Isolation-correct alias test teardowns

[Bead Pages](../README.md) / [bob-cli-kj](README.md) / bob-cli-kj.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.1bm](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.1bm.md) · **Assignee:** `bob-cli-kj.1` · **Size:** small
**Created:** 2026-11-11 17:20:03 EST · **Closed:** 2026-11-11 17:31:44 EST
**Plan:** [202611/impact\_ranked\_bead\_fixes.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/impact_ranked_bead_fixes.md)

## Description

mac-typecheck: fix the two @MainActor test classes that mutate ledgerSuites from nonisolated tearDown so bob-mac-capture `just typecheck-tests` passes on clean master (bead bob-cli-jy).

## Notes

[2026-11-11T22:31:44Z · bob-cli-kj.1] Fixed both alias test teardowns by accessing ledgerSuites inside MainActor.assumeIsolated. Verified just portable-check passed (2,499 tests, 1 skipped); macOS typecheck-tests reported PASS for all four targets, including BobMacCaptureTests. Scratch wrapper returned nonzero only because zsh reserves the cleanup variable name; removed the scratch directory manually.

## Dependencies

- **Blocks:** [bob-cli-kj.5](bob-cli-kj.5.md) ◐ · ⧖ 2026-11-11

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-kj.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-kj.1/README.md) | [bob-cli-kj.1](bob-cli-kj.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-mac-capture | [`bob-mac-capture@1e83c03`](https://github.com/bobs-org/bob-mac-capture/commit/1e83c032217a9d6c90827ee467e5c60b57069d88) | fix(tests): isolate alias ledger teardown on main actor | [bob-cli-kj.1](bob-cli-kj.1.md) | 2026-11-11 17:32:23 EST |
