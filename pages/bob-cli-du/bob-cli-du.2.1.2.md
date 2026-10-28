# Bead: bob-cli-du.2.1.2 — Extract reusable capture completion and aggregate nested outcomes

[Bead Pages](../README.md) / [bob-cli-du.2.1](bob-cli-du.2.1.md) / bob-cli-du.2.1.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.bob-cli-du.2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-du.2.md) · **Assignee:** `bob-cli-du.2.1.2` · **Size:** medium
**Created:** 2026-10-28 15:26:10 EDT · **Closed:** 2026-10-28 16:22:56 EDT
**Plan:** [202610/complete\_label\_capture.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/complete_label_capture.md)

## Description

shared-completion: extract complete_existing_task from the whole-item ! adapter, add omitted-by-default relation completion output, and generalize successor traversal, numbering, net filtering, and detail rendering while preserving existing capture behavior.

## Notes

[2026-10-28T20:22:56Z · bob-cli-du.2.1.2] Extracted complete_existing_task from plan_task_complete_item with identical ! behavior; added relation_completes[] and complete_effect CP7 plumbing omitted-by-default (schema v1); generalized all_unblocked/all_project_folds/unblocked_vecs_mut traversal, single-item nested numbering, net post-pass, surviving links, and print_task_complete_details reuse. Verified: 9 output unit tests (4 new), 1156 lib capture tests, 44 relations suites, 91 complete suites, 44 task_complete CLI, 16 inbox_route, 119 task_complete engine, 115 config, 39 vectors; cargo fmt clean and cargo check clean.

## Dependencies

- **Depends on:** [bob-cli-du.2.1.1](bob-cli-du.2.1.1.md) ✓ · ⧖ 2026-10-28
- **Blocks:** [bob-cli-du.2.1.3](bob-cli-du.2.1.3.md) ◐ · ⧖ 2026-10-28

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-du.2.1.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-du.2.1.2/README.md) | [bob-cli-du.2.1.2](bob-cli-du.2.1.2.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`4c55a59`](https://github.com/bobs-org/bob-cli/commit/4c55a595bfd6e6b025c4e053e3a16628a29e1d3b) | refactor(capture): extract shared task-complete completion path | [bob-cli-du.2.1.2](bob-cli-du.2.1.2.md) | 2026-10-28 16:24:52 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-du.2.1.2][1] | Need the phase scope and design file | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-du.2.1.2/README.md

<!-- sase:referenced-by:end -->
