# Bead: bob-cli-ce.6 — Toasts, status chip, outcome adapters, and OS notifications

[Bead Pages](../README.md) / [bob-cli-ce](README.md) / bob-cli-ce.6

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.research.5c.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.research.5c.linker.w0.md) · **Assignee:** `bob-cli-ce.6` · **Size:** medium
**Created:** 2026-10-26 10:35:53 EDT · **Closed:** 2026-10-26 12:30:56 EDT
**Plan:** [202610/bob\_colon\_command\_mode.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/bob_colon_command_mode.md)

## Description

feedback: replace the runner's plain notices with the three-class toast cards and the live status-bar chip. It adds per-command outcome adapters and their action buttons, OS notifications for long unfocused runs, Rerun last command, and a Chromium preview harness for visual review.

## Notes

[2026-10-26T16:29:23Z · bob-cli-ce.6] PROPOSED FOLLOW-UP: Document the existing BOB_TEST_FIXTURE_PDF docs-lint exception — npm run docs:check fails on clean bob-cli source_store.rs:187; the same finding is already noted in bob-cli-ce.5 and bob-cli-c9.6, and no task bead exists to cite.

[2026-10-26T16:30:56Z · bob-cli-ce.6] Implemented and deployed bob-command-mode feedback (toast cards, live status chip, command outcome adapters/actions, long-run notifications, rerun-last-command, and Chromium preview harness). Verified npm run build, npm run validate, focused command-mode/runner suites (26/26 with NO_COLOR unset), and light/dark Chromium previews. npm run docs:check reports the pre-existing BOB_TEST_FIXTURE_PDF docs-lint issue, recorded as a proposed follow-up.

## Dependencies

- **Depends on:** [bob-cli-ce.5](bob-cli-ce.5.md) ✓ · ⧖ 2026-10-26
- **Blocks:** [bob-cli-ce.7](bob-cli-ce.7.md) ◐ · ⧖ 2026-10-26

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-ce.6](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-ce.6/README.md) | [bob-cli-ce.6](bob-cli-ce.6.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@90eb3c0`](https://github.com/bobs-org/bob-plugins/commit/90eb3c076039f867e679394d3aa88b5a31fd3fa1) | feat(bob-command-mode): add run feedback and rerun controls | [bob-cli-ce.6](bob-cli-ce.6.md) | 2026-10-26 12:31:35 EDT |
