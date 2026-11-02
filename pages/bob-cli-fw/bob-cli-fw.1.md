# Bead: bob-cli-fw.1 — bob-cli resolves, reports, and teaches the implied merge

[Bead Pages](../README.md) / [bob-cli-fw](README.md) / bob-cli-fw.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.173](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.173.md) · **Size:** medium
**Created:** 2026-11-02 09:55:54 EST · **Closed:** 2026-11-02 10:52:27 EST
**Plan:** [202611/merge\_next\_planned\_default.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/merge_next_planned_default.md)

## Description

bob: make dest-less `=*` / `=*<src>` complete merges that absorb the next planned Pomodoro below the source; add `source_role`, `absorbed[].role`, and `explicit` to the merge report, a `same as` CLI line, completion labels and `initial_selection`, a `merge_next_missing` error, tests, and docs.

## Notes

[2026-11-02T15:52:27Z · bob-cli-fw.1--4] Verified SCCACHE_DISABLE=1 just check && just docs-check; scratch-vault smoke passed for capture human/JSON, capture-parse, and capture-complete on =*; no phase epic symbols remain.

## Dependencies

- **Blocks:** [bob-cli-fw.2](bob-cli-fw.2.md) ◐ · ⧖ 2026-11-02

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-fw.1](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-fw.1.md) | [bob-cli-fw.1](bob-cli-fw.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`5088721`](https://github.com/bobs-org/bob-cli/commit/508872164ecc7f2c71fd4ec03c8fdd69acd9ccce) | feat(capture): merge the next planned Pomodoro by default | [bob-cli-fw.1](bob-cli-fw.1.md) | 2026-11-02 10:53:16 EST |
