# Bead: bob-cli-gl.6 — Bob Mac Capture move picker, Add block ID, shift-return chain, and span styling

[Bead Pages](../README.md) / [bob-cli-gl](README.md) / bob-cli-gl.6

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.35.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.35.linker.w0.md) · **Assignee:** `bob-cli-gl.6` · **Size:** medium
**Created:** 2026-11-03 13:39:31 EST · **Closed:** 2026-11-03 17:44:29 EST
**Plan:** [202611/capture\_move\_bullets.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/capture_move_bullets.md)

## Description

mac-picker: In bob-mac-capture (open it with /sase_repo), gate on the `project_task_move` need and spans and decode the new context, descriptor, and rows. Build the move picker on the scoped parent-task picker patterns, with the Add block ID flow, shift-return "move & add another", Esc and stale-draft handling, calm need status text, and new span colours. Update the docs and fixtures.

## Notes

[2026-11-03T22:44:29Z · bob-cli-gl.6] Implemented mac-picker move picker in bob-mac-capture: project_task_move gating, decoding, picker/index, Add block ID, Shift-Return chaining, Esc calm status, span colours, docs and MC1/MC2/MC4/MC5 fixtures with fake-bob handlers plus CaptureCore and panel tests. Verified: portable-check on athena passed (2072 tests, 0 failures); mac docs-check passed; BobMacCapture app targets unverified on Linux (need Mac typecheck-tests/CI).

## Dependencies

- **Depends on:** [bob-cli-gl.4](bob-cli-gl.4.md) ✓ · ⧖ 2026-11-03
- **Blocks:** [bob-cli-gl.7](bob-cli-gl.7.md) ✓ · ⧖ 2026-11-03

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-gl.6](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-gl.6/README.md) | [bob-cli-gl.6](bob-cli-gl.6.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-mac-capture | [`bob-mac-capture@c0dd1e2`](https://github.com/bobs-org/bob-mac-capture/commit/c0dd1e22de45ab52f8390f3b9e4167e0e70782b2) | feat(capture): add move picker for project-note move bullets | [bob-cli-gl.6](bob-cli-gl.6.md) | 2026-11-03 17:46:28 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-gl.6][1] | Need the phase scope and design file | 3 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-gl.6/README.md

<!-- sase:referenced-by:end -->
