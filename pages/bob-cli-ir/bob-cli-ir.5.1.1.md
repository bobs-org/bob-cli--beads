# Bead: bob-cli-ir.5.1.1 — Recognize record items before task marker parsing

[Bead Pages](../README.md) / [bob-cli-ir.5.1](bob-cli-ir.5.1.md) / bob-cli-ir.5.1.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-ir.5](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-ir.5.md) · **Assignee:** `bob-cli-ir.5.1.1` · **Size:** medium
**Created:** 2026-11-08 18:25:56 EST · **Closed:** 2026-11-08 19:55:02 EST
**Plan:** [202611/capture\_record\_creation.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/capture_record_creation.md)

## Description

record-language: add shared record route claiming, opaque field and note parsing, marker refusals, editor spans, and fail-closed execution scaffolding.

## Notes

[2026-11-09T00:54:44Z · bob-cli-ir.5.1.1] PROPOSED FOLLOW-UP: just docs-check fails on word budget in docs/reference/mac-capture/{capture-panel,keyboard,protocol}.md (6088/6060/6014 words vs 6000 cap); untouched by record-language, reproduces on base tree

[2026-11-09T00:54:52Z · bob-cli-ir.5.1.1] PROPOSED FOLLOW-UP: one unidentified transient failure in cargo test --lib (5851 passed/1 failed), green on two reruns (5852 passed/0 failed); watch for recurrence before triaging as flake

[2026-11-09T00:55:02Z · bob-cli-ir.5.1.1] record-language done. Shared API: capture_language::record::{RecordRoutePolicy, RecordFieldInput, RecordNoteGroup, RecordNoteIntent, RecordNoteLine, classify_record_item, candidate_dirs}, capture_record::record_policy_for_draft (one memoized policy per invocation; parse+execution both use it); grammar 20. Execution of claimed records refuses fail-closed (exit 2, RECORD_EXECUTION_UNWIRED_MESSAGE, no writes) until record-writes. Verified: 28 new lib tests + 3 CLI tests pass; full lib 5852/0, full cli 3304/0, tasks/dataview parity green, just fmt+lint clean, docs-gen regen (capture-parse.md grammar 20). One transient lib failure (unnamed) green on two reruns; docs-check word-budget failure is pre-existing base-tree (both filed as PROPOSED FOLLOW-UP). No epic-symbols. Downstream: record-parse maps RecordNoteIntent to the records engine; record rows/completion belong to later phases.

## Dependencies

- **Blocks:** [bob-cli-ir.5.1.2](bob-cli-ir.5.1.2.md) ✓ · ⧖ 2026-11-08

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-ir.5.1.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-ir.5.1.1/README.md) | [bob-cli-ir.5.1.1](bob-cli-ir.5.1.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`83ad74e`](https://github.com/bobs-org/bob-cli/commit/83ad74e2f8138b6d94ba745380a9f012ce08d104) | feat(capture): add shared record route classifier with fail-closed execution | [bob-cli-ir.5.1.1](bob-cli-ir.5.1.1.md) | 2026-11-08 19:56:49 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-ir.5.1.1][1] | Confirm phase scope before closing | 2 |
| read-by | [agent:bob-cli-ir.5.1.3][2] | Need shared API and grammar revision recorded by record-language | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-ir.5.1.1/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-ir.5.1.3/README.md

<!-- sase:referenced-by:end -->
