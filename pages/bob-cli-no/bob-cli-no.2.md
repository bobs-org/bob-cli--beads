# Bead: bob-cli-no.2 — The -D/--delete flag, its delete gate, output, JSON, and docs

[Bead Pages](../README.md) / [bob-cli-no](README.md) / bob-cli-no.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.5j.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.5j.linker.w0.md) · **Assignee:** `bob-cli-no.2` · **Size:** medium
**Created:** 2026-11-19 14:47:07 EST · **Closed:** 2026-11-19 16:59:27 EST
**Plan:** [202611/bank\_import\_delete.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/bank_import_delete.md)

## Description

delete: add -D/--delete with an up-front check of each file, a gate that deletes only after the batch succeeds and only files whose bytes still match their digest, per-file outcomes, colored human output, an additive JSON `delete` object, exit codes, and the docs/bank.md and Monday guide rewrite.

## Notes

[2026-11-19T21:58:59Z · bob-cli-no.2] PROPOSED FOLLOW-UP: catalog lib test public_leaves_are_entries_or_excluded fails on clean base (periods/update leaf neither entry nor excluded); pre-existing, unrelated to delete phase.

[2026-11-19T21:59:06Z · bob-cli-no.2] PROPOSED FOLLOW-UP: just docs-check lint fails on clean base with mac-capture reference word budgets (capture-previews.md 6171 and keyboard.md 6027 words over 6000 cap); pre-existing, unrelated to delete phase.

[2026-11-19T21:59:27Z · bob-cli-no.2] Implemented bank import -D/--delete: up-front regular-file/vault gate (bank_import_delete_unsupported, exit 2), digest-gated post-commit cleanup with per-file outcomes, Would delete/Deleted/Kept human lines, additive JSON delete object, exit 1 with bank_delete_failed on cleanup failure, docs/bank.md subsection plus Monday guide rewrite with real-run sample. Verified: fmt clean, clippy clean, 463 lib bank tests + 109 cli bank tests pass (9 new delete tests); catalog lib-test and docs-check mac-capture budget failures reproduce identically on clean base and are recorded as PROPOSED FOLLOW-UP notes.

## Dependencies

- **Depends on:** [bob-cli-no.1](bob-cli-no.1.md) ✓ · ⧖ 2026-11-19
- **Blocks:** [bob-cli-no.3](bob-cli-no.3.md) ✓ · ⧖ 2026-11-19

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-no.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-no.2/README.md) | [bob-cli-no.2](bob-cli-no.2.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`c94a718`](https://github.com/bobs-org/bob-cli/commit/c94a718d3ca186696b872a5878b8176090b03460) | feat(bank): add import -D/--delete with digest-gated cleanup | [bob-cli-no.2](bob-cli-no.2.md) | 2026-11-19 17:01:15 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-no.2][1] | Need the phase scope and design file | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-no.2/README.md

<!-- sase:referenced-by:end -->
