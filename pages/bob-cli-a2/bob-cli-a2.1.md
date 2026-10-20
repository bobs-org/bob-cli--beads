# Bead: bob-cli-a2.1 — Task-relation contract, capture grammar, wire names, and vectors

[Bead Pages](../README.md) / [bob-cli-a2](README.md) / bob-cli-a2.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.research.53.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.research.53.linker.w0.md) · **Assignee:** `bob-cli-a2.1` · **Size:** medium
**Created:** 2026-10-20 09:08:22 EDT · **Closed:** 2026-10-20 09:22:25 EDT
**Plan:** [202610/task\_relations.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/task_relations.md)

## Description

contract: write docs/task-relations.md (grammar, slot, identity, projection, inertness, invariants, writers, gestures, chips, kill switch, outputs, and every vector table). Add the registry and MC rows in task-dependencies.md, the `~` / `~~` capture sections and wire names, capture-syntax rows, vault-format, task-status-hooks, and configuration. Docs only.

## Notes

[2026-10-20T13:22:10Z · bob-cli-a2.1] PROPOSED FOLLOW-UP: docs-check test_templates_in_material and test_component_chips_in_material fail on missing python module github-callouts in the mkdocs env; reproduces identically on the clean tree with changes stashed

[2026-10-20T13:22:14Z · bob-cli-a2.1] PROPOSED FOLLOW-UP: contract phase skipped docs/reference/glossary.md because it is generated from the glossary memory web and only rollout may edit memory; rollout step 5 already owns the Task relation term and Task Link sentence

[2026-10-20T13:22:25Z · bob-cli-a2.1] Contract landed: new docs/task-relations.md with Rules 1-14 plus LK/LW/LR/LX/LP/LG/LC vectors, registry and MC10-MC17 rows in task-dependencies.md, ~ / ~~ sections and wire fields in capture.md and capture-syntax.md, vault-format lines, task-status-hooks relation pass, relations.linked_from_lines config, completion markers, nav wired. just docs-check passes except 2 pre-existing material-builder failures from missing github-callouts module, reproduced on the clean tree.

## Dependencies

- **Blocks:** [bob-cli-a2.2](bob-cli-a2.2.md) ✓ · ⧖ 2026-10-20
- **Blocks:** [bob-cli-a2.3](bob-cli-a2.3.md) ◐ · ⧖ 2026-10-20

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-a2.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-a2.1/README.md) | [bob-cli-a2.1](bob-cli-a2.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`ae9629e`](https://github.com/bobs-org/bob-cli/commit/ae9629ecd69c9227c314cb9d0e6c5d65a892efd9) | docs(task-relations): add task-relations contract page and wire relation lines | [bob-cli-a2.1](bob-cli-a2.1.md) | 2026-10-20 09:23:41 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-a2.1][1] | Need the phase scope and design file | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-a2.1/README.md

<!-- sase:referenced-by:end -->
