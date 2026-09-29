# Bead: bob-cli-2n.1 — Project-note marker grammar: \`@route^id+#pomodoro\`, retire \`@route:id+\`

[Bead Pages](../README.md) / [bob-cli-2n](README.md) / bob-cli-2n.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.35](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.35.md) · **Assignee:** `bob-cli-2n.1` · **Size:** medium
**Created:** 2026-09-29 15:35:25 EDT · **Closed:** 2026-09-29 16:34:38 EDT
**Plan:** [202609/project\_task\_links.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202609/project_task_links.md)

## Description

marker: move the Pomodoro name onto the `^` project-note marker (`@route^id+#pomodoro`), retire the `:` project-note forms with teaching errors, stop linking or starring `^prj`, and keep execution, capture-parse, capture-complete, and help text in agreement.

## Notes

[2026-09-29T20:02:33Z · bob-cli-2n.1] PROPOSED FOLLOW-UP: clippy deny on tests/cli/capture/pomodoro_name.rs:808 (`|| true`, overly_complex_bool_expr) fails `cargo clippy --all-targets` on clean HEAD too — pre-existing, blocks `just lint` independently of marker phase

[2026-09-29T20:34:38Z · bob-cli-2n.1] Marker phase done: @route^id+#pomodoro parses (ProjectNote{pomodoro_name}), @route:id+ retired with teaching errors, ^prj never linked/starred ([ ]/[?]), execution/capture-parse/capture-complete/help aligned. Verified: cargo fmt --check clean, full cargo test green (1174 lib + 538 cli + all other targets, 0 failures), epic-symbols clean. Only clippy failure is the pre-existing pomodoro_name.rs:808 overly_complex_bool_expr on the untouched clean tree (already filed as PROPOSED FOLLOW-UP note #1).

## Dependencies

- **Blocks:** [bob-cli-2n.2](bob-cli-2n.2.md) ◐ · ⧖ 2026-09-29

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-2n.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-2n.1/README.md) | [bob-cli-2n.1](bob-cli-2n.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`65f5b43`](https://github.com/bobs-org/bob-cli/commit/65f5b43acafb3eedcb922f402a5d305c841652a0) | feat(capture): project-note pomodoro marker phase (@route^id+#pomodoro) | [bob-cli-2n.1](bob-cli-2n.1.md) | 2026-09-29 16:37:01 EDT |
