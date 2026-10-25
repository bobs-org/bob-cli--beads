# Bead: bob-cli-an.6.6.6.5.6.5.5.6.5 — Stop the ref\_library work-tree snapshots from reading transient .git files

[Bead Pages](../README.md) / [bob-cli-an.6.6.6.5.6.5.5.6](bob-cli-an.6.6.6.5.6.5.5.6.md) / bob-cli-an.6.6.6.5.6.5.5.6.5

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.land.md) · **Assignee:** `bob-cli-an.6.6.6.5.6.5.5.6.5` · **Size:** small
**Created:** 2026-10-25 08:44:09 EDT · **Closed:** 2026-10-25 08:56:43 EDT
**Plan:** [202610/backlog\_batch9\_epipe\_listen\_publish\_refresh\_flakes.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/backlog_batch9_epipe_listen_publish_refresh_flakes.md)

## Description

migrate-snapshot-prune: resolve bob-cli-c2 by pruning .git during traversal in the ref_library work-tree snapshot helpers so a vanishing git file cannot panic the walk.

## Notes

[2026-10-25T12:56:43Z · bob-cli-an.6.6.6.5.6.5.5.6.5] Pruned .git during traversal in all ref_library snapshot walkers (migrate_tasks, migrate_zorg, show, list, find, today; rename and mod already pruned) so vanishing transient git files cannot panic the walk; replaced migrate_zorg's silent read-skip with expect so work-tree writes are never masked. No test compared raw .git bytes, so no rev-parse substitution was needed. Verified: cargo test --test cli ref_library green 4x incl. 3x --test-threads=64 (132 passed), just check exit 0.

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.5](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.5/README.md) | [bob-cli-an.6.6.6.5.6.5.5.6.5](bob-cli-an.6.6.6.5.6.5.5.6.5.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`f255819`](https://github.com/bobs-org/bob-cli/commit/f255819acae8185061c0c3bd4300f74aa9f11f8a) | fix(ref-library): prune .git during snapshot traversal | [bob-cli-an.6.6.6.5.6.5.5.6.5](bob-cli-an.6.6.6.5.6.5.5.6.5.md) | 2026-10-25 08:58:14 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-an.6.6.6.5.6.5.5.6.5][1] | Need the phase scope and design file | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.5/README.md

<!-- sase:referenced-by:end -->
