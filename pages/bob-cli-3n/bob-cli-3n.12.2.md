# Bead: bob-cli-3n.12.2 — Hooks dependency docs, Summary line, helper dedupe, and reconcile split

[Bead Pages](../README.md) / [bob-cli-3n.12](bob-cli-3n.12.md) / bob-cli-3n.12.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-3n.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-3n.land.md) · **Assignee:** `bob-cli-3n.12.2` · **Size:** medium
**Created:** 2026-10-02 23:24:08 EDT · **Closed:** 2026-10-03 00:05:39 EDT
**Plan:** [202610/task\_dep\_links\_fixes.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/task_dep_links_fixes.md)

## Description

hooks-docs-cleanup: add the Dependency lines, guarded-write, and Output docs, README and long_about, append the counts to Summary, dedupe the copied link helpers, split reconcile.rs, remove per-run whole-vault copies, and fill the DW/DR unit-test gaps.

## Notes

[2026-10-03T04:05:39Z · bob-cli-3n.12.2] hooks-docs-cleanup done: Dependency-lines section + Guard-rails quiet-interval + Output keys in docs, README/long_about updated, dependency counts appended to Summary (Dependencies line kept), helpers deduped (strikethrough/inline-code/vault-relative/block-link via shared task_dependencies impls; needless pub(crate) removed), reconcile.rs split 1465/289/198, sync clones touched-only + heal by_block once. Tests: DW1/DW2/DW3/DW6/DW15/DW16 added, DW5 placeholder replaced, DR table in fields.rs, archive_stayed e2e in move_done.rs. Verified: cargo fmt --check ok, cargo clippy exit 0 (pre-existing warnings only), cargo test full ok (16 suites, 0 failed incl. 1561 lib + 864 cli).

## Dependencies

- **Depends on:** [bob-cli-3n.12.1](bob-cli-3n.12.1.md) ✓ · ⧖ 2026-10-02
- **Blocks:** [bob-cli-3n.12.7](bob-cli-3n.12.7.md) ◐ · ⧖ 2026-10-02
- **Blocks:** [bob-cli-3n.12.8](bob-cli-3n.12.8.md) ◐ · ⧖ 2026-10-02

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-3n.12.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-3n.12.2/README.md) | [bob-cli-3n.12.2](bob-cli-3n.12.2.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`79e39af`](https://github.com/bobs-org/bob-cli/commit/79e39afe50a0bd2f65055e60d33fea31f51c25be) | docs(hooks): dependency docs, Summary counts, helper dedupe, reconcile split | [bob-cli-3n.12.2](bob-cli-3n.12.2.md) | 2026-10-03 00:07:15 EDT |
