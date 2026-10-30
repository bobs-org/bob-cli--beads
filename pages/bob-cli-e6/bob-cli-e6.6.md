# Bead: bob-cli-e6.6 — Named captures keep the task type in agreement

[Bead Pages](../README.md) / [bob-cli-e6](README.md) / bob-cli-e6.6

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.2t.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.2t.linker.w0.md) · **Assignee:** `bob-cli-e6.6` · **Size:** medium
**Created:** 2026-10-29 16:16:34 EDT · **Closed:** 2026-10-29 21:27:10 EDT
**Plan:** [202610/task\_types.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/task_types.md)

## Description

capture-retype: replace the old theme write rule with the retype planner for every #NAME and =name capture form, including project-note bullets and exempt types such as PLAN.

## Notes

[2026-10-30T01:26:53Z · bob-cli-e6.6] PROPOSED FOLLOW-UP: native::capture_related::tests::archive_closed_window_respects_mtime fails on clean master — a done/ archive with mtime 40 days back still matches as closed_duplicate (completion 2026-10-01, days_ago 19)

[2026-10-30T01:27:10Z · bob-cli-e6.6] Named #NAME/#"NAME"/=name captures (new-task, existing-task, Ensure Next, project-note bullets) call routing::retype with keep_type=false. Acceptance CLI tests cover inherited BUILD+#fix, #build clear, #plan, #later label keep+warn, BUILD+FIX keep/retype, batch, dry-run, and project-note. just lint and just docs-check passed; 1026 CLI capture tests passed. just check still fails on pre-existing archive_closed_window_respects_mtime (reproduced on clean master).

## Dependencies

- **Depends on:** [bob-cli-e6.5](bob-cli-e6.5.md) ✓ · ⧖ 2026-10-29
- **Blocks:** [bob-cli-e6.7](bob-cli-e6.7.md) ○ · ⧖ 2026-10-29

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-e6.6](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-e6.6/README.md) | [bob-cli-e6.6](bob-cli-e6.6.md) | 0 |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-e6.6][1] | Need the phase scope and design file | 3 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-e6.6/README.md

<!-- sase:referenced-by:end -->
