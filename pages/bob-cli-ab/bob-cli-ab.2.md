# Bead: bob-cli-ab.2 — Draft mode and the capture-related JSON contract

[Bead Pages](../README.md) / [bob-cli-ab](README.md) / bob-cli-ab.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.27.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.27.linker.w0.md) · **Assignee:** `bob-cli-ab.2` · **Size:** medium
**Created:** 2026-10-20 17:44:13 EDT · **Closed:** 2026-10-20 20:17:24 EDT
**Plan:** [202610/capture\_similar\_tasks\_band.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/capture_similar_tasks_band.md)

## Description

contract: accept a capture draft, gate task-creating items, exclude and report draft-linked tasks, emit item anchors, actions, defaults, and replacements as schema_version 1, with goldens, a perf gate, and docs.

## Notes

[2026-10-21T00:17:24Z · bob-cli-ab.2--2] Implemented capture draft mode and schema_version 1 JSON contract, including task-creation gating, linked-task reporting, anchors, actions, defaults, and replacements; updated docs and fixtures. Full just check passed, and epic-symbols reports no leftovers.

## Dependencies

- **Depends on:** [bob-cli-ab.1](bob-cli-ab.1.md) ✓ · ⧖ 2026-10-20
- **Blocks:** [bob-cli-ab.3](bob-cli-ab.3.md) ◐ · ⧖ 2026-10-20
- **Blocks:** [bob-cli-ab.4](bob-cli-ab.4.md) ◐ · ⧖ 2026-10-20

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-ab.2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-ab.2.md) | [bob-cli-ab.2](bob-cli-ab.2.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`062fc3d`](https://github.com/bobs-org/bob-cli/commit/062fc3da24646166a752f264bd3acec0dd75b4c1) | feat(capture-related): add draft JSON contract | [bob-cli-ab.2](bob-cli-ab.2.md) | 2026-10-20 20:18:13 EDT |
