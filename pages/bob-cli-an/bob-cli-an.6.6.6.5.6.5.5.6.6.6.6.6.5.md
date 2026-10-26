# Bead: bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.5 — Reduce native bob query --tasks time and memory cost

[Bead Pages](../README.md) / [bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6](bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.md) / bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.5

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.land.md) · **Assignee:** `bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.5` · **Size:** large
**Created:** 2026-10-26 10:47:09 EDT · **Closed:** 2026-10-26 11:28:45 EDT
**Plan:** [202610/backlog\_batch13\_vault\_integrity\_and\_perf\_1.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/backlog_batch13_vault_integrity_and_perf_1.md)

## Description

tasks-query-cost: resolve bob-cli-6k by profiling the native Tasks query path, finding the source of repeated note reads and memory amplification, and proving improvements with regression coverage.

## Notes

[2026-10-26T15:00:03Z · bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.5] Planning investigation on clean base 92706cb4: src/native/dataview.rs::run_native unconditionally builds NativeVault/DataviewIndex before dispatching Tasks or TasksNote; both then build TaskIndex and never consume the Dataview index. QueryContext reads origin frontmatter independently. This explains duplicate whole-vault reads; PageDraft/list_object also allocate unused page/list metadata. No runtime measurements or implementation changes yet. Authored a medium tale for narrow dispatch separation, lightweight explicit-origin compatibility, a capped-memory CLI regression, comparable before/after wall-time/RSS/read-count evidence, and just check. Validation passed with zero warnings. No epic-symbol entries found. Submitting through sase plan propose; phase and target bob-cli-6k remain open for implementation and parent landing respectively.

[2026-10-26T15:28:37Z · bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.5] /tmp/tasks_query_cost/bead_note.txt --reason-file

[2026-10-26T15:28:45Z · bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.5] Avoid unused Dataview index in native Tasks: dispatch builds index only for Source/DQL, Tasks uses lightweight origin check. Before 4.33s/267MB empty paths, 5.14s/371MB empty json, 12470 md opens; after 0.45s/54MB, 1.37s/153MB, 6235 opens, same SHAs; DQL unchanged 3.79s. Capped regression fails on base (SIGABRT alloc) passes on fix. just check passes.

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.5](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.5.md) | [bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.5](bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.5.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`f73f926`](https://github.com/bobs-org/bob-cli/commit/f73f926d72451cbaad4f5b22553c1860d3c8f490) | perf(query): avoid unused Dataview index in native Tasks queries | [bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.5](bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.5.md) | 2026-10-26 11:30:15 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.land][1] | Need the child scope and notes | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.land.md

<!-- sase:referenced-by:end -->
