# Bead: bob-cli-fn.1 — Lists in bob capture and capture-parse

[Bead Pages](../README.md) / [bob-cli-fn](README.md) / bob-cli-fn.1

**Status:** ○ open · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.c1](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.c1.md) · **Assignee:** `bob-cli-fn.1` · **Size:** medium
**Created:** 2026-11-01 23:41:34 EST
**Plan:** [202611/capture\_route\_lists.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/capture_route_lists.md)

## Description

list-capture: split list headers into one capture item per bullet (zero-copy slices plus a list context), give list bullets the task-bullet grammar (` :id`, ` ^id`, per-task markers, refusals) in both the execution and editor parsers, wire planning, add the `list` JSON object and human summary, bump grammar to 6, and document the form.

## Notes

[2026-11-02T07:53:15Z · bob-cli-fn.1] PROPOSED FOLLOW-UP: base build break blocks just check - cargo check --lib fails identically on clean HEAD and this tree with no method named as_str for BufferPart (callers capture_pomodoros_agenda.rs:1205, capture/event_conflict.rs:358; from HEAD commit 1b796cd7). Tracked by bob-cli-fj; re-run just check after that bead lands.

[2026-11-02T07:53:22Z · bob-cli-fn.1] PROPOSED FOLLOW-UP: docs-check red on base - test_every_capture_token_has_a_literal_query_at_its_heading fails for 4 spellings (=/-split, =*-merge, @route+block-id#drawer, - #drawer with nested notes) in untouched capture-syntax.md / search_smoke.yml; needs owner triage.

[2026-11-02T07:53:31Z · bob-cli-fn.1] PROPOSED FOLLOW-UP: flaky test - native::task_complete keep_moving routing_is_lazy_and_narrow_with_shared_destination fails in full cargo test --lib runs but passes in isolation and in module runs; order-dependent, consider a flake bead.

[2026-11-02T07:53:37Z · bob-cli-fn.1] PROPOSED FOLLOW-UP: memory_list_decision_record stays declined - epic decision answer=false so no decisions strand was written; land agent to confirm no record is wanted.

[2026-11-02T07:53:43Z · bob-cli-fn.1] PROPOSED FOLLOW-UP: plan tension on lone-@ row - Header-outcomes says bob capture refuses @+bullets with the incomplete-route copy, but no such refusal exists in execution at HEAD, so @ keeps filing literally while parse stays incomplete/needs-route; tests pin actual, needs plan clarification.

## Dependencies

- **Blocks:** [bob-cli-fn.3](bob-cli-fn.3.md) ◐ · ⧖ 2026-11-01

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-fn.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-fn.1/README.md) | [bob-cli-fn.1](bob-cli-fn.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`0ebd071`](https://github.com/bobs-org/bob-cli/commit/0ebd0714f8d90de0b9be7616d7eff2dd305066aa) | feat(capture)!: file each list bullet as its own capture | [bob-cli-fn.1](bob-cli-fn.1.md) | 2026-11-02 02:55:11 EST |
