# Bead: bob-cli-99.1 — Reading-task facts and blocked reasons in bob ref JSON

[Bead Pages](../README.md) / [bob-cli-99](README.md) / bob-cli-99.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.8z](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.8z.md) · **Assignee:** `bob-cli-99.1` · **Size:** medium
**Created:** 2026-10-18 13:02:21 EDT · **Closed:** 2026-10-18 14:04:59 EDT
**Plan:** [202610/reading\_board.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/reading_board.md)

## Description

ref-json: add task priority and scheduled date plus a typed `blocked_by` reason list (schedule, open prerequisites, blocked project) to every `bob ref` row, an optional human reason suffix, fixtures, tests, and docs/ref.md.

## Notes

[2026-10-18T18:04:11Z · bob-cli-99.1] PROPOSED FOLLOW-UP: skipped decisions:reading-board-is-bob-rendered — epic DECISIONS set memory_board_record=no, so the land agent should record the bob-drawn board (Bases kanban rejected) via sase_memory_write after this phase.

[2026-10-18T18:04:30Z · bob-cli-99.1] PROPOSED FOLLOW-UP: just all still fails on pre-existing highlights tests unrelated to this phase (pandoc_maps_every_contract_construct_to_tex panic "lifted link", already noted on bob-cli-87.13 / bob-cli-8w / bob-cli-8g.6; mermaid CLI diagrams_* and diagrams_swap_pdf_error_keeps_note_and_source from bob-cli-8y). They fail without this phase's files.

[2026-10-18T18:04:59Z · bob-cli-99.1] ref-json: blocked_by + task.priority/scheduled on every bob ref row; human dim reason suffix. Verified: cargo fmt/clippy clean for this change; ref_library unit+CLI tests pass; live vault bob ref list -s ready,next,wip -A -f json has blocked_by on every row (23 blocked all with a reason, 22 unblocked []); hand-checked scheduled (harvest_first_job_application_autofill until 2026-10-19), dependency (agent_instructions_budgeted_router after sase_memory__dynamic-agents-md), project (evals_through_goals_reading_list #prj_is_blocked on sase_post_blog); warm runtime 0.32s (0.30-0.35, target 0.35); docs/ref.md updated. epic-symbols none. Skipped memory_board_record and pre-existing mermaid/pandoc just-all failures recorded as PROPOSED FOLLOW-UP.

## Dependencies

- **Blocks:** [bob-cli-99.2](bob-cli-99.2.md) ✓ · ⧖ 2026-10-18
- **Blocks:** [bob-cli-99.4](bob-cli-99.4.md) ◐ · ⧖ 2026-10-18

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-99.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-99.1/README.md) | [bob-cli-99.1](bob-cli-99.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`b88195e`](https://github.com/bobs-org/bob-cli/commit/b88195e7d5b1f40ecca031260dd32922edfc0721) | feat(ref): add blocked\_by reasons and task priority/scheduled | [bob-cli-99.1](bob-cli-99.1.md) | 2026-10-18 14:06:48 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-99.1][1] | Need notes, remaining work, and whether earlier agent left remainder | 3 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-99.1/README.md

<!-- sase:referenced-by:end -->
