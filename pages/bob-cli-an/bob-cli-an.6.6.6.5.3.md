# Bead: bob-cli-an.6.6.6.5.3 — Reuse a completed Pomodoro's canonical name on the link form

[Bead Pages](../README.md) / [bob-cli-an.6.6.6.5](bob-cli-an.6.6.6.5.md) / bob-cli-an.6.6.6.5.3

**Status:** ◐ in_progress · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-an.6.6.6.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-an.6.6.6.land.md) · **Assignee:** `bob-cli-an.6.6.6.5.3` · **Size:** small
**Created:** 2026-10-24 07:37:07 EDT
**Plan:** [202610/backlog\_batch5\_highlights\_render\_pomodoro\_name\_duplicate\_link\_mac\_ci.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/backlog_batch5_highlights_render_pomodoro_name_duplicate_link_mac_ci.md)

## Description

pomodoro-name-reuse: resolve bob-cli-bb by naming a CompletedOnly placeholder from the completed entry, not from canonicalize_pomodoro_name(selector).

## Notes

[2026-10-24T12:03:52Z · bob-cli-an.6.6.6.5.3] Verified: link/child-insert/start all reuse completed DEEP WORK (was DEEP-WORK). Added completed_only_reuse_name helper in capture_pomodoros.rs; used by named_creation_name, insert_named_placeholder (relocation), insert_named_pomodoro_child_block, plan_pomodoro_start, project_note. 3 new CLI regressions in tests/cli/capture/pomodoro_link.rs (link_form_reuses..., link_with_start_moves..., link_with_start_creates...) failed pre-fix, pass post-fix. Focused suites green (214 pomodoro CLI, 35 toggle/link/project CLI, 21 capture_pomodoros + 61 task_toggle + 153 completion unit). just check exit=0 on retry (3234 lib + 1985 cli); first full run hit two parallel-run flakes (curl ETXTBSY, ingest lock timing) that pass on both trees in isolation. Task bead bob-cli-bb left open for the lander.

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-an.6.6.6.5.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-an.6.6.6.5.3/README.md) | [bob-cli-an.6.6.6.5.3](bob-cli-an.6.6.6.5.3.md) | 0 |
