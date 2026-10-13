# Bead: bob-cli-78.2 — Reconcile derives, tags, and reverses the cascade

[Bead Pages](../README.md) / [bob-cli-78](README.md) / bob-cli-78.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.71](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.71.md) · **Assignee:** `bob-cli-78.2` · **Size:** medium
**Created:** 2026-10-13 03:14:27 EDT · **Closed:** 2026-10-13 04:52:12 EDT
**Plan:** [202610/subproject\_cascade.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/subproject_cascade.md)

## Description

cli-reconcile: add a shared Rust project-tree module (parent resolution, ancestors, descendants, tag predicate) and make reconcile block, tag, consume, promote, cycle-check, deproject descendant targets, and recover sub-projects per PDS1–PDS15.

## Notes

[2026-10-13T08:43:34Z · bob-cli-78.2--1] Verification and performance (2026-10-13):
- `RUST_TEST_THREADS=1 just check` reached the full suite; the CLI target reported 1,433 passed and 2 failed. The other reported targets passed, including the cascade tests.
- Re-ran the CLI suite from a clean archive of HEAD: 1,425 passed and the same 2 failed, `capture::r#ref::failed_percent_listen_worker_keeps_listen_retry_guidance` and `capture::r#ref::percent_listen_reference_runs_existing_worker_and_installs_audio`. These clean-base failures are already tracked by bob-cli-6m.
- Release `bob task reconcile --dry-run` timing on a 1.8 GB vault copy, 31 timed invocations per build: live-vault median baseline 4.944025s, current 4.984513s (+0.8%); synthetic two-level cascade median baseline 4.946344s, current 4.935995s (-0.2%).
PROPOSED FOLLOW-UP: Fix the two clean-base percent-listen CLI failures; they reproduce unchanged here and are tracked by bob-cli-6m.
PROPOSED FOLLOW-UP: Update glossary:project-task to describe inherited sub-project blocking; memory_glossary=no for this epic.

[2026-10-13T08:52:12Z · bob-cli-78.2--1] Cascade reconcile is complete. just check has only two percent-listen failures, reproduced on clean base and tracked by bob-cli-6m; cascade tests passed and performance medians and required follow-ups are recorded in the phase note.

## Dependencies

- **Depends on:** [bob-cli-78.1](bob-cli-78.1.md) ✓ · ⧖ 2026-10-13
- **Blocks:** [bob-cli-78.3](bob-cli-78.3.md) ✓ · ⧖ 2026-10-13
- **Blocks:** [bob-cli-78.4](bob-cli-78.4.md) ✓ · ⧖ 2026-10-13
- **Blocks:** [bob-cli-78.8](bob-cli-78.8.md) ◐ · ⧖ 2026-10-13

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-78.2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-78.2.md) | [bob-cli-78.2](bob-cli-78.2.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`96bf514`](https://github.com/bobs-org/bob-cli/commit/96bf514e6dc1d4535704bde59c4159ca9b50aa9d) | feat(projects): reconcile inherited sub-project blocking | [bob-cli-78.2](bob-cli-78.2.md) | 2026-10-13 04:53:27 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-78.2--1][1] | Need the phase scope and design file | 4 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-78.2.md

<!-- sase:referenced-by:end -->
