# Bead: bob-cli-j5.2.1.3 — Apply archive plans under the lock and expose preview and JSON

[Bead Pages](../README.md) / [bob-cli-j5.2.1](bob-cli-j5.2.1.md) / bob-cli-j5.2.1.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-j5.2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-j5.2.md) · **Assignee:** `bob-cli-j5.2.1.3` · **Size:** medium
**Created:** 2026-11-09 12:19:09 EST · **Closed:** 2026-11-09 15:10:02 EST
**Plan:** [202611/guarded\_archive\_writer.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/guarded_archive_writer.md)

## Description

archive-command: integrate bounded guarded retries with standalone and nightly execution, add dry-run and versioned JSON reports, preserve scoped Git behavior, and finish documentation and command regressions.

## Notes

[2026-11-09T20:09:42Z · bob-cli-j5.2.1.3] PROPOSED FOLLOW-UP: four lib tests fail on the clean base (HEAD 37df0e52) after the notebooks commit 0a74731b — native::completion::kinds::tests::every_value_arg_has_a_decision ("notebooks:root" has no kinds decision), native::catalog::tests::document_shape (87 vs 85), runner::tests::every_native_command_is_on_exactly_one_canonical_path (72 vs 70), runner::tests::subcommands_are_contiguous_in_section_order_and_alphabetical ("notebooks is out of alphabetical order in Vault"); reproduced identically with my changes stashed.

[2026-11-09T20:09:46Z · bob-cli-j5.2.1.3] PROPOSED FOLLOW-UP: just docs-check lint fails on the clean base with 3 word-budget errors — docs/reference/json-outputs.md (6117 words at base, cap 6000), docs/reference/mac-capture/capture-panel.md (6006) and keyboard.md (6028); this phase added ~26 words to json-outputs.md (one archive row); the later docs-check stages never run until these are trimmed. zensical build --strict passes.

[2026-11-09T20:10:02Z · bob-cli-j5.2.1.3] archive-command landed: standalone owns bob_sync.lock (30s bounded wait, lock_timeout exit 1) through plan/apply/Git; nightly run_collection runs under its own lock without reacquiring; apply uses task_status_hooks_write::apply_plan with tool task-archive (no unguarded writes, no vault_rewrite::run); whole-plan rebuild on VaultChanged/QuietPeriod/UnstableRead inside a separate 30s budget with injected clock/session/plan hooks; partial apply reports applied/deferred/recovery, skips Git, exits 1; Git is structured (touched-only commit+push, non-worktree skip, empty-plan skip, failure keeps applied changes); -n/--dry-run and -f/--format human|json added to parsing, completion_descriptor and help (dry-run: no lock/Git/state/dirs); one-line schema_version 1 JSON for every outcome; docs/task-archive.md + json-outputs.md + generated help updated. Verified: cargo test --lib native::collect_done (114 pass, run 4x), cargo test --test cli (3433 pass incl. 9 new move_done tests, nightly, aliases, help, docs_reference), just lint + cargo fmt --check clean, zensical strict build passes. Full workspace test: only 4 failures, all notebooks-related and reproduced identically on the clean base; just docs-check lint fails on the clean base (3 word-budget errors). Both recorded as PROPOSED FOLLOW-UP notes. No epic-symbol leftovers.

## Dependencies

- **Depends on:** [bob-cli-j5.2.1.2](bob-cli-j5.2.1.2.md) ✓ · ⧖ 2026-11-09

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-j5.2.1.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-j5.2.1.3/README.md) | [bob-cli-j5.2.1.3](bob-cli-j5.2.1.3.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`e802071`](https://github.com/bobs-org/bob-cli/commit/e802071f8d39039a5ae7c8b191ec456ca8557db0) | feat(archive): apply plans under the lock with dry-run preview and JSON report | [bob-cli-j5.2.1.3](bob-cli-j5.2.1.3.md) | 2026-11-09 15:10:57 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-j5.2.1.3][1] | Need the phase scope and design file | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-j5.2.1.3/README.md

<!-- sase:referenced-by:end -->
