# Bead: bob-cli-q4.8.1.2 — Add the guarded editor adapter and cursor policy

[Bead Pages](../README.md) / [bob-cli-q4.8.1](bob-cli-q4.8.1.md) / bob-cli-q4.8.1.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-q4.8](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-q4.8.md) · **Assignee:** `bob-cli-q4.8.1.2` · **Size:** medium
**Created:** 2026-11-25 10:27:09 EST · **Closed:** 2026-11-25 11:34:08 EST
**Plan:** [202611/task\_settle\_twin.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/task_settle_twin.md)

## Description

editor-apply: add Tasks classification and daily-path adapters plus the synchronous editor application layer. Apply minimal changes atomically, preserve the approved cursor-stays policy, return mapped jump targets, and verify immediate undo and path safety. Keep the public namespace unpublished until scheduler completion.

## Notes

[2026-11-25T16:33:40Z · bob-cli-q4.8.1.2] PROPOSED FOLLOW-UP: 10 pre-existing task-status-cycler unit failures still reproduce on this tree and were recorded on bob-cli-q4.8.1.1 (clean-base HEAD 5ed3bd22): open-line NOTES-before-work-log plus 9 req-toggle/task-reqs-vectors NOTES/CRLF/newline cases. Cycler sources untouched by editor-apply.

[2026-11-25T16:33:48Z · bob-cli-q4.8.1.2] PROPOSED FOLLOW-UP: test-ledger-tools-frees-marks.cjs 200-link/2000-task 25ms budget failed in the full suite (66ms) and is the same load flake recorded on bob-cli-q4.8.1.1; perf tests in npm run test:perf all passed.

[2026-11-25T16:34:08Z · bob-cli-q4.8.1.2] editor-apply done: Tasks statusSettings snapshot + daily-path adapters (no getTasks, no daily-file IO); applyToEditor one-tx hunks (no setValue) with stay cursor + jumpTarget, inactive-leaf/path/preimage guards; staged join is one undo group, already-applied joins via cm.dispatch userEvent input, missing-cm transaction is a second undo. 15 editor tests + 10 vector/copy/regression tests pass; this.api.taskSettle unpublished; ledger-tools 1.159.0 deployed. Pre-existing 10 cycler + 1 frees-marks flake recorded as follow-ups.

## Dependencies

- **Depends on:** [bob-cli-q4.8.1.1](bob-cli-q4.8.1.1.md) ✓ · ⧖ 2026-11-25
- **Blocks:** [bob-cli-q4.8.1.3](bob-cli-q4.8.1.3.md) ◐ · ⧖ 2026-11-25

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-q4.8.1.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-q4.8.1.2/README.md) | [bob-cli-q4.8.1.2](bob-cli-q4.8.1.2.md) | 0 |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-q4.8.1.2][1] | Need the phase scope, design file, and DECISIONS before closing editor-apply | 5 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-q4.8.1.2/README.md

<!-- sase:referenced-by:end -->
