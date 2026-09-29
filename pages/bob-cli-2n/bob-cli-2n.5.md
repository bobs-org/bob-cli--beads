# Bead: bob-cli-2n.5 — Capture docs for named and linked project tasks

[Bead Pages](../README.md) / [bob-cli-2n](README.md) / bob-cli-2n.5

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.35](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.35.md) · **Assignee:** `bob-cli-2n.5` · **Size:** small
**Created:** 2026-09-29 15:35:25 EDT · **Closed:** 2026-09-29 17:24:15 EDT
**Plan:** [202609/project\_task\_links.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202609/project_task_links.md)

## Description

docs: rewrite the capture guide's grammar tables, Project notes section, JSON contract, and capture-parse/capture-complete references for the new syntax, with the worked example.

## Notes

[2026-09-29T21:24:02Z · bob-cli-2n.5] PROPOSED FOLLOW-UP: just lint fails on clean tree — clippy single_element_loop in src/native/capture_parse.rs test (Plan =x loop); docs-only phase left it untouched

[2026-09-29T21:24:15Z · bob-cli-2n.5] Rewrote docs/capture.md (grammar tables, Project notes with verified worked example, JSON contract with task_links, capture-parse spans/modes/diagnostics, capture-complete project_task_block_id, interactive New ID flow) and docs/projects.md pointer. Verified worked example bytes, JSON, human output, error texts, parse spans, and completion JSON against the built binary in a temp vault; greps confirm no stale :block-id>+/:goog-exit+ forms or ^prj-linking claims remain. just fmt passes; just lint fails on pre-existing clippy single_element_loop in untouched src/native/capture_parse.rs (recorded as follow-up). No epic-symbol leftovers.

## Dependencies

- **Depends on:** [bob-cli-2n.3](bob-cli-2n.3.md) ✓ · ⧖ 2026-09-29
- **Depends on:** [bob-cli-2n.4](bob-cli-2n.4.md) ✓ · ⧖ 2026-09-29

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-2n.5](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-2n.5/README.md) | [bob-cli-2n.5](bob-cli-2n.5.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`42cd336`](https://github.com/bobs-org/bob-cli/commit/42cd3362d7b7cb0472df40a6267009b93add3b5a) | docs(capture): document named and linked project tasks | [bob-cli-2n.5](bob-cli-2n.5.md) | 2026-09-29 17:25:41 EDT |
