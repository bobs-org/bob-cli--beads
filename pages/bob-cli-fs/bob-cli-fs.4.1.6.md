# Bead: bob-cli-fs.4.1.6 — Complete conformance and measure Apollo budgets

[Bead Pages](../README.md) / [bob-cli-fs.4.1](bob-cli-fs.4.1.md) / bob-cli-fs.4.1.6

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-fs.4](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-fs.4.md) · **Assignee:** `bob-cli-fs.4.1.6` · **Size:** medium
**Created:** 2026-11-02 12:29:13 EST · **Closed:** 2026-11-02 17:50:52 EST
**Plan:** [202611/capture\_relation\_successors.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/capture_relation_successors.md)

## Description

verification: audit capture-expressible SA cases, fill integration coverage, measure release builds on an Apollo scratch copy, document results, and provide full gate evidence.

## Notes

[2026-11-02T22:31:10Z · bob-cli-fs.4.1.6--4] Verified capture SA coverage (SA22/23/26/28/36 plus existing SA1–SA21 parks/dones), relation_successors tests green, previous-daily relative-path skip for SA28, SA1/SA4 human+JSON smokes, just docs-check passed, epic-symbols empty. Apollo isolated scratch (4.0G, 6848 md files, rustc 1.95.0, Xeon 8168): hello/x medians 29.59/31.11 ms meet 40ms vs pre-feature 8c7e7103; x* 360.72 ms, ! 356.28 ms, dependents-pass add +12.76 ms miss 70ms/5ms (baseline already 170.79/219.87/+15.11). Recorded in docs/task-dependencies.md §12.7. just check pending host verify.

[2026-11-02T22:50:52Z · bob-cli-fs.4.1.6--5] Verified capture SA coverage (SA22/23/26/28/36 plus existing SA1–SA21 parks/dones and both kill switches), previous-daily relative-path skip for SA28, SA1/SA4 human+JSON smokes, relation_successors tests, just docs-check, and sase tool run check (c679dba95152eaa6cf74a18d6462b3f9). Apollo isolated scratch (4.0G, 6848 md files, rustc 1.95.0, Xeon 8168): hello/x medians 29.59/31.11 ms meet 40ms vs pre-feature 8c7e7103; x* 360.72 ms, ! 356.28 ms, dependents-pass add +12.76 ms miss 70ms/5ms (baseline already 170.79/219.87/+15.11). Recorded in docs/task-dependencies.md §12.7. epic-symbols empty.

## Dependencies

- **Depends on:** [bob-cli-fs.4.1.5](bob-cli-fs.4.1.5.md) ✓ · ⧖ 2026-11-02

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-fs.4.1.6](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-fs.4.1.6.md) | [bob-cli-fs.4.1.6](bob-cli-fs.4.1.6.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`c20263c`](https://github.com/bobs-org/bob-cli/commit/c20263c6f0f3b4f2a720641a1ae579c5c9b68489) | fix(capture): skip previous-daily relation sources by relative path | [bob-cli-fs.4.1.6](bob-cli-fs.4.1.6.md) | 2026-11-02 17:51:45 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-fs.4.1.6--5][1] | Need the phase scope and design file | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-fs.4.1.6.md

<!-- sase:referenced-by:end -->
