# Bead: bob-cli-dm.6.1.1 — Task-aware picker inputs and shared theme preselection

[Bead Pages](../README.md) / [bob-cli-dm.6.1](bob-cli-dm.6.1.md) / bob-cli-dm.6.1.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.bob-cli-dm.6](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-dm.6.md) · **Assignee:** `bob-cli-dm.6.1.1` · **Size:** medium
**Created:** 2026-10-28 20:08:12 EDT · **Closed:** 2026-10-28 20:23:37 EDT
**Plan:** [202610/task\_theme\_link\_picker.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/task_theme_link_picker.md)

## Description

suggestion-model: add task context and the synchronous suggestion snapshot to both picker entry points, implement the shared preselection rule without changing Today order or typed-query ranking, and run the copied preselect vectors through the model.

## Notes

[2026-10-29T00:23:37Z · bob-cli-dm.6.1.1] Implemented task-aware picker inputs and shared preselection in both picker entry points; copied and passed all bob-cli preselect vectors. Verified npm run build, npm test (4084 passed), npm run validate, and BOB_CLI_DIR docs:check (448 docs tests passed); synced block-id-prompt to the vault. epic-symbols had no remaining entries.

## Dependencies

- **Blocks:** [bob-cli-dm.6.1.2](bob-cli-dm.6.1.2.md) ✓ · ⧖ 2026-10-28

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-dm.6.1.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-dm.6.1.1/README.md) | [bob-cli-dm.6.1.1](bob-cli-dm.6.1.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@97341c4`](https://github.com/bobs-org/bob-plugins/commit/97341c476226586a27c3cf4fa0cf7af12491cd82) | feat(block-id-prompt): add task-aware theme preselection | [bob-cli-dm.6.1.1](bob-cli-dm.6.1.1.md) | 2026-10-28 20:24:34 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-dm.6.1.1][1] | Need the phase scope and design file | 4 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-dm.6.1.1/README.md

<!-- sase:referenced-by:end -->
