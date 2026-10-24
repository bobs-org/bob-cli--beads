# Bead: bob-cli-bj.4 — Shared vault-rewrite transaction extracted from bob themes rename

[Bead Pages](../README.md) / [bob-cli-bj](README.md) / bob-cli-bj.4

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.2e.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.2e.linker.w0.md) · **Assignee:** `bob-cli-bj.4` · **Size:** medium
**Created:** 2026-10-24 13:34:46 EDT · **Closed:** 2026-10-24 16:06:21 EDT
**Plan:** [202610/relation\_label\_vocabulary.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/relation_label_vocabulary.md)

## Description

rewrite-txn: extract lock, pre-sync, snapshot and stale check, dirty-path rules, atomic write with rollback, verify, single commit, and post-sync from the theme rename into one shared transaction, moving bob themes rename onto it byte-for-byte.

## Notes

[2026-10-24T20:05:56Z · bob-cli-bj.4] PROPOSED FOLLOW-UP: migrate `bob ref rename` onto src/native/vault_rewrite/ (it still carries its own lock/sync/commit transaction in ref_library); verify byte-identical output and land its transaction tests

[2026-10-24T20:06:07Z · bob-cli-bj.4] PROPOSED FOLLOW-UP: pre-existing gate failures reproduce identically on the clean base tree and are unrelated to rewrite-txn: lib every_value_arg_has_a_decision for themes rename:old/new (owned by epic bob-cli-bc), CLI completion::bash, completion::capture_text x2, help_options::capture_complete_help_lists_options_alphabetically, plus flaky capture::related perf gate and 2 completion::vault tests that pass in isolation on both trees

[2026-10-24T20:06:21Z · bob-cli-bj.4] Extracted src/native/vault_rewrite/ (lock_busy, not_a_worktree, sync_failed, stale_note, dirty_paths, verify_failed, one commit, post-sync-pending) and moved bob themes rename onto it. Verified: 8 new txn unit tests pass; themes lib 11 pass; themes_rename CLI 5 pass; fmt+clippy clean with no new warnings; full-gate failures reproduce identically on clean base (recorded as PROPOSED FOLLOW-UPs).

## Dependencies

- **Depends on:** [bob-cli-bj.2](bob-cli-bj.2.md) ✓ · ⧖ 2026-10-24
- **Blocks:** [bob-cli-bj.6](bob-cli-bj.6.md) ◐ · ⧖ 2026-10-24

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-bj.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-bj.4/README.md) | [bob-cli-bj.4](bob-cli-bj.4.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`fd9380c`](https://github.com/bobs-org/bob-cli/commit/fd9380cbaefb8ceb481a914ca6490b6f70e54143) | refactor(themes): extract rename transaction into vault\_rewrite module | [bob-cli-bj.4](bob-cli-bj.4.md) | 2026-10-24 16:07:40 EDT |
