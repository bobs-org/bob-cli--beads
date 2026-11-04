# Bead: bob-cli-go.4.1.1 — Resolve merge containers and transplant authored payloads

[Bead Pages](../README.md) / [bob-cli-go.4.1](bob-cli-go.4.1.md) / bob-cli-go.4.1.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.bob-cli-go.4](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-go.4.md) · **Assignee:** `bob-cli-go.4.1.1` · **Size:** medium
**Created:** 2026-11-03 18:14:56 EST · **Closed:** 2026-11-03 19:46:45 EST
**Plan:** [202611/task\_merge\_engine.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/task_merge_engine.md)

## Description

payload: define the pure merge request/context/result types, validate source identities, resolve task/drawer/section containers, and prepare ordered payload transplants with descendant-anchor repair. Test payloads, containers, and structural refusals. Keep this an internal preparation API until the integration phase completes it.

## Notes

[2026-11-04T00:46:27Z · bob-cli-go.4.1.1--2] PROPOSED FOLLOW-UP: Update the two catalog shape assertions still pinned at 67 while the generated catalog has 69 (native::catalog::tests::document_shape and catalog::protocol_1_parses_with_schema_version_one). The same 69-vs-67 failures are recorded on the clean baseline by bob-cli-gn #1-2 and independently corroborated by bob-cli-gl.5.1.2 #1-2; bob-cli-de is the earlier closed catalog-count repair. Route to the catalog owner during epic land triage.

[2026-11-04T00:46:45Z · bob-cli-go.4.1.1--2] Verified cargo fmt and all 15 focused task_merge tests. just check passes Clippy but full tests hit only the known clean-base catalog shape failures (69 vs 67), recorded as a proposed follow-up citing bob-cli-gn, bob-cli-gl.5.1.2, and bob-cli-de. epic-symbols reports no entries.

## Dependencies

- **Blocks:** [bob-cli-go.4.1.2](bob-cli-go.4.1.2.md) ✓ · ⧖ 2026-11-03

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-go.4.1.1](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-go.4.1.1.md) | [bob-cli-go.4.1.1](bob-cli-go.4.1.1.md) | 2 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`adf2082`](https://github.com/bobs-org/bob-cli/commit/adf20825f77d3adc059ae69e7809018e4b75bcbe) | fix(task-merge): resolve payload preparation failures | [bob-cli-go.4.1.1](bob-cli-go.4.1.1.md) | 2026-11-03 19:07:47 EST |
| bob-cli | [`672954d`](https://github.com/bobs-org/bob-cli/commit/672954d4bf2d740405230be9ee2e098ff33405e1) | test(task-merge): fix nested payload indentation assertion | [bob-cli-go.4.1.1](bob-cli-go.4.1.1.md) | 2026-11-03 19:48:45 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-gl.5.1.3--1][1] | Check whether existing task-merge or clean-base clippy work tracks the prepare_task_merge unused-import failure | 1 |
| read-by | [agent:bob-cli-go.4.1.1--1][2] | Need the phase scope, design file, prior notes, and required checks | 1 |
| read-by | [agent:bob-cli-go.4.1.1--2][2] | Need phase scope, notes, design, and required checks before final verification | 1 |
| read-by | [agent:bob-cli-go.4.1.land][3] | Need the child scope and notes | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-gl.5.1.3.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-go.4.1.1.md
[3]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-go.4.1.land.md

<!-- sase:referenced-by:end -->
