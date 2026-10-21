# Bead: bob-cli-am.2 — Rust pair model, planner, and reconcile projection

[Bead Pages](../README.md) / [bob-cli-am](README.md) / bob-cli-am.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.29.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.29.linker.w0.md) · **Assignee:** `bob-cli-am.2` · **Size:** medium
**Created:** 2026-10-21 10:08:37 EDT · **Closed:** 2026-10-21 11:33:52 EDT
**Plan:** [202610/undirected\_task\_relations.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/undirected_task_relations.md)

## Description

pair-core: add a pure pair-state and pair-write planner in task_relations, stop bare adds from stripping labels, teach reconcile to omit plain mirrors the target already names, and add the redundant_relation warning, all pinned by the LW and LR vectors.

## Notes

[2026-10-21T15:33:52Z · bob-cli-am.2] pair-core landed: pure pair planner (Link/State/ClearLabel/Swap/RemoveStatement/Unlink) pinned by LW4/LW15-LW23 unit vectors plus endpoint-swap property test; LW16 bare-add guard; reconcile omits plain mirrors the target already names (malformed names nobody) and emits redundant_relation; LR19 rewritten plus LR25-LR28; task-status-hooks.md documents the omission rule and new warning kind. Verified: cargo fmt clean, clippy gate no errors, lib 3166 passed, task_status_hooks 157 passed, capture 956 passed, just docs-check passed.

## Dependencies

- **Depends on:** [bob-cli-am.1](bob-cli-am.1.md) ✓ · ⧖ 2026-10-21
- **Blocks:** [bob-cli-am.3](bob-cli-am.3.md) ◐ · ⧖ 2026-10-21
- **Blocks:** [bob-cli-am.4](bob-cli-am.4.md) ◐ · ⧖ 2026-10-21
- **Blocks:** [bob-cli-am.5](bob-cli-am.5.md) ◐ · ⧖ 2026-10-21

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-am.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-am.2/README.md) | [bob-cli-am.2](bob-cli-am.2.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`dec8f87`](https://github.com/bobs-org/bob-cli/commit/dec8f8798debaf4ee3c3213559bfed6230abc0ca) | feat(relations): add pair planner, projection, and redundant warnings | [bob-cli-am.2](bob-cli-am.2.md) | 2026-10-21 11:35:25 EDT |
