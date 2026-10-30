# Bead: bob-cli-ee.1.1 — Capture type-marker grammar and new-task typing

[Bead Pages](../README.md) / [bob-cli-ee.1](bob-cli-ee.1.md) / bob-cli-ee.1.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ▸ plan · **Tier:** epic
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.bob-cli-ee.1](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-ee.1.md) · **Assignee:** `bob-cli-ee.1.1.land`
**Created:** 2026-10-30 04:33:10 EDT · **Closed:** 2026-10-30 09:35:45 EDT
**Plan:** [202610/capture\_type\_grammar.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/capture_type_grammar.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| implemented-by | [plan:202610/capture_type_grammar.md][1] | derived from the plan's `bead_id:` frontmatter field |

_Plus 3 automatic references — see [Referenced By](#referenced-by)._

[1]: https://github.com/bobs-org/bob-cli--plans/blob/main/202610/capture_type_grammar.md

<!-- sase:links:end -->

## Description

Complete bob-cli-ee.1 with one shared offset-preserving t: grammar, editor spans and diagnostics, new-task type writes and named-Pomodoro agreement, while preserving existing capture behavior and verifying its documentation.

## Notes

[2026-10-30T12:13:38Z · bob-cli-ee.1.1.land] LAND FOLLOW-UP TRIAGE: Used /sase_new_task, searched CI tasks across statuses, swept last-week CI tasks, inspected active epic scopes, and read bob-cli-ea and bob-cli-dh. Proposing child bob-cli-ee.1.1.1 note #1 (clone_on_copy in src/native/gcal/classify.rs:75) is RESOLVED: a0a6b497, already an ancestor of the first ee.1.1 commit, replaces start.clone() with *start and repairs the hidden bool_comparison too. This matches bob-cli-ea landing notes #3-4. Declined a new task or +1 because the defect is fixed; bob-cli-dh is a different sase-core issue, not a duplicate. The parent phase bob-cli-ee.1 note #1 records skipped decision memory: declined a new memory task because memory_record=no explicitly forbids that change, and no memory edits were made. There are no other PROPOSED FOLLOW-UP entries on the three children. Current epic-caused contract gaps are retained as remaining epic work in the repair tale, not deferred into tasks.

[2026-10-30T12:15:18Z · bob-cli-ee.1.1.land] LAND AUDIT before repair tale: Reviewed all notes on ee.1.1 and ee.1.1.1/.2/.3, source/diffs of 59d5a093/23ba4805/f40a625a, and both governing plans. Fetched origin/master=f40a625a. No non-epic commits since first implementation; the only intervening commit since epic creation is a0a6b497 (GCal lint/doc cleanup), already integrated and requiring no capture changes. Decisions honored: warn unknown types, config menu order reserved for ee.3, no memory edits; schema=1 and shared Pomodoro vectors unchanged. Existing-target refusal and completion-menu/Mac work correctly remain outer-phase seams. No epic-symbols entries for ee.1.1 or ee.1; no symvision recipe.
REMAINING EPIC WORK, reproduced against freshly built f40a625a in scratch vaults: inbox marker ignores mac_inbox task_type (passes empty route -> .md); #bui resolves to BUILD but t:fix succeeds because agreement checks raw selector; quoted t:"BUILD + FIX" writes an invalid composite field and editor emits no diagnostic; @sase+parent plus typed child and --route/--task typed child silently discard the marker; URL plus bare or bulleted marker-only continuation becomes task rather than reference; text @sase:id=x t:fix is accepted and closes/carries under BUILD with no task_theme result; kept explicit FIX with inherited WRITE prints from sase instead of this task. Ordinary marker execution errors lose their structured code. docs/task-types.md also retains contradictory omitted-on-no-change and set|cleared-only statements. Existing test coverage misses these branches (the lone conflict rollback test is dry-run only). The bounded medium tale sase_plan_capture_type_marker_closeout.md fixes these gaps, verifies the acceptance matrix, and must close ee.1.1, mark its plan done, then close parent phase ee.1 normally in its own turn. Do not close outer ee. Prior follow-up triage is in the preceding note. Governed just check is running as 653f60d72f319e18506e05e6db59ac83; result will be appended before proposal.

[2026-10-30T12:16:03Z · bob-cli-ee.1.1.land] LAND VERIFICATION: Governed just check (ToolRun 653f60d72f319e18506e05e6db59ac83) passed on f40a625a with exit 0 in 534325 ms: formatting, denied-Clippy gate, and full workspace test binaries. No code was changed during this audit; only the repair-plan proposal was authored. This confirms the ee.1.1.1 Clippy follow-up is resolved, but does not satisfy the independently reproduced contract gaps recorded above. git diff --check is clean. Keep epic and parent phase open pending the validated medium repair tale, whose final step owns their normal closeout.

[2026-10-30T13:35:45Z · bob-cli-ee.1.1.land--1] Verified grammar and writer repairs against the approved plan; all three descendant phases are closed and the linked plan is complete. Post-audit integration a0a6b497 is already present and has no overlapping capture changes. just all passed (exit 0); just docs-check passed all implemented gates (447 passed, 1 skipped because font-generation dependencies are absent); git diff --check is clean. Epic-symbols is empty. Follow-up triage: clone_on_copy was fixed by a0a6b497, so no task or corroboration; bob-cli-dh is a different repository; memory_record=no remains final, so no memory edit or task. No just symvision recipe is available.

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-ee.1.1.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-ee.1.1.land.md) | [bob-cli-ee.1.1](bob-cli-ee.1.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`41e8959`](https://github.com/bobs-org/bob-cli/commit/41e89597a70755763e27ce74138b05baa00e1c54) | feat(capture): complete type-marker grammar and writers | [bob-cli-ee.1.1](bob-cli-ee.1.1.md) | 2026-10-30 09:40:00 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-ee.1.1.2][1] | Need parent epic plan and DECISIONS | 1 |
| read-by | [agent:bob-cli-ee.1.1.3][2] | parent epic scope and decisions | 1 |
| read-by | [agent:bob-cli-ee.1.1.land--1][3] | Need the landing audit and child state | 3 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-ee.1.1.2/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-ee.1.1.3/README.md
[3]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-ee.1.1.land.md

<!-- sase:referenced-by:end -->
