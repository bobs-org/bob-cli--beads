# Bead: bob-cli-go.4.1.2 — Repoint dependencies and retire sources with provenance

[Bead Pages](../README.md) / [bob-cli-go.4.1](bob-cli-go.4.1.md) / bob-cli-go.4.1.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.bob-cli-go.4](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-go.4.md) · **Assignee:** `bob-cli-go.4.1.2` · **Size:** medium
**Created:** 2026-11-03 18:14:56 EST · **Closed:** 2026-11-03 20:31:51 EST
**Plan:** [202611/task\_merge\_engine.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/task_merge_engine.md)

## Description

retirement: add snapshot-only dependency repointing and cycle validation, relation or Cancel Log provenance, cancellation/recovery composition, idempotency, and prerequisite and successor reports. Test graph invariants, managed history, and label-only handling of closed sources. Extract the shared overlap filter needed by MG19.

## Notes

[2026-11-04T01:31:23Z · bob-cli-go.4.1.2] PROPOSED FOLLOW-UP: flaky timing test september_shaped_vault_finishes_fast (src/native/capture_pomodoros_agenda.rs) failed once under full-suite load (263ms wall clock) and passes in isolation; unrelated to retirement (task_merge + config/relations only). Consider raising its bound or marking it load-insensitive.

[2026-11-04T01:31:51Z · bob-cli-go.4.1.2] Retirement landed: src/native/task_merge/retirement.rs (repoint w/ BLOCKS mirrors+fields, batch cycle validation, LINKS/LINKED FROM + section Cancel Log provenance, plan_task_cancel composition, idempotency classifier, prereq/successor reports) + MG19 shared overlap helper (config/relations.rs delegates, byte-identical warnings). Verified: cargo fmt clean, cargo clippy gate clean, 28/28 task_merge tests incl. MG5-MG9/MG13/MG16/MG19; full workspace suite 4877 passed with 1 unrelated load-flake (september_shaped_vault_finishes_fast, passes solo, noted as follow-up). No epic-symbol entries.

## Dependencies

- **Depends on:** [bob-cli-go.4.1.1](bob-cli-go.4.1.1.md) ✓ · ⧖ 2026-11-03
- **Blocks:** [bob-cli-go.4.1.3](bob-cli-go.4.1.3.md) ✓ · ⧖ 2026-11-03

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-go.4.1.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-go.4.1.2/README.md) | [bob-cli-go.4.1.2](bob-cli-go.4.1.2.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`751c769`](https://github.com/bobs-org/bob-cli/commit/751c769f02147873f0b2d2dacf092636e9190ec7) | feat(task-merge)!: retire sources with repointing and provenance | [bob-cli-go.4.1.2](bob-cli-go.4.1.2.md) | 2026-11-03 20:33:26 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-gl.5.1.3--1][1] | Check whether the active task-merge integration phase owns the baseline unused preparation import | 1 |
| read-by | [agent:bob-cli-go.4.1.2][2] | Need the phase scope and design file | 1 |
| read-by | [agent:bob-cli-go.4.1.land][3] | Need the child scope and notes | 1 |
| read-by | [agent:bob-cli-go.4.1.land--1][3] | Recheck dependency and retirement scope, MG19 guidance, and notes before parent epic closeout | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-gl.5.1.3.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-go.4.1.2/README.md
[3]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-go.4.1.land.md

<!-- sase:referenced-by:end -->
