# Bead: bob-cli-7c.6 — Per-row destination override in the Obsidian picker

[Bead Pages](../README.md) / [bob-cli-7c](README.md) / bob-cli-7c.6

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.11.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.11.linker.w0.md) · **Assignee:** `bob-cli-7c.6` · **Size:** medium
**Created:** 2026-10-13 09:48:12 EDT · **Closed:** 2026-10-13 11:49:57 EDT
**Plan:** [202610/successor\_offers.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/successor_offers.md)

## Description

obsidian_destination: expose block-id-prompt's Pomodoro link picker as a versioned api, chain it from the successor picker's Ctrl+Shift+Enter to retarget rows, and make the cycler insert picks at an overridden existing or new entry.

## Notes

[2026-10-13T15:49:44Z · bob-cli-7c.6] PROPOSED FOLLOW-UP: 6 plugin-suite failures reproduce identically on the clean base tree (verified via stash): 4 in test-ledger-tools-unblocked-glyph.cjs, Keep-counts saturation in test-navigation-decision-card-handlers.cjs, and Pomodoro-line continuation in test-task-status-cycler-successor-wiring.cjs — triage as task beads, none caused by obsidian_destination

[2026-10-13T15:49:57Z · bob-cli-7c.6] obsidian_destination done: block-id-prompt api.pomodoroLinkPicker v1 (1.31.0), nav Ctrl+Shift+Enter retarget with hint gating (2.34.0), cycler override-aware insertion with preimage-checked existing and anchor-placed new placeholders recorded in receipt (1.39.0); docs/task-dependencies.md §12.13 updated; build:check green, focused suites 210/211 (1 pre-existing wiring failure, all 6 full-suite failures reproduce on clean base and are noted as follow-up); bob plugins sync clean

## Dependencies

- **Depends on:** [bob-cli-7c.4](bob-cli-7c.4.md) ✓ · ⧖ 2026-10-13
- **Depends on:** [bob-cli-7c.5](bob-cli-7c.5.md) ✓ · ⧖ 2026-10-13
- **Blocks:** [bob-cli-7c.8](bob-cli-7c.8.md) ◐ · ⧖ 2026-10-13

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-7c.6](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-7c.6/README.md) | [bob-cli-7c.6](bob-cli-7c.6.md) | 2 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`3f29da1`](https://github.com/bobs-org/bob-cli/commit/3f29da1c3b0fa8b42b40f442afaebaf184e43b0a) | docs(tasks): document per-row successor destination override (bob-cli-7c.6) | [bob-cli-7c.6](bob-cli-7c.6.md) | 2026-10-13 11:51:13 EDT |
| bob-plugins | [`bob-plugins@e5ef68c`](https://github.com/bobs-org/bob-plugins/commit/e5ef68c2999daebf9fc0189e095d930cf9104f59) | feat(plugins): per-row successor destination override in the Obsidian picker (bob-cli-7c.6) | [bob-cli-7c.6](bob-cli-7c.6.md) | 2026-10-13 11:52:28 EDT |
