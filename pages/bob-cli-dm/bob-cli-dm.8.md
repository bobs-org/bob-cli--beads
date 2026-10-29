# Bead: bob-cli-dm.8 — Bob Mac Capture renders suggestions and theme changes

[Bead Pages](../README.md) / [bob-cli-dm](README.md) / bob-cli-dm.8

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.2s.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.2s.linker.w0.md) · **Assignee:** `bob-cli-dm.8` · **Size:** medium
**Created:** 2026-10-28 08:45:53 EDT · **Closed:** 2026-10-28 20:23:46 EDT
**Plan:** [202610/task\_theme\_suggestions.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/task_theme_suggestions.md)

## Description

mac-capture: decode the additive fields, preselect the suggested Pomodoro-name row, show the reason in the secondary slot, show the task-theme preview line, and make the Refs Link to Today card preselect and actually link the suggested row.

## Notes

[2026-10-29T00:23:46Z · bob-cli-dm.8] Implemented mac-capture phase in bob-mac-capture (uncommitted): decode theme_suggestion/suggested/suggestion_label on completion + refs-today models and task_theme on capture items (lossy decodeIfPresent, schema_version stays 1); preselect suggested pomodoro_name row on empty query with Suggested secondary + Suggested header and hue dot; task-theme preview line in link/toggle presentations, views, notifications, and VoiceOver; refs card preselects suggested row, sends .entry for non-default (fixes .automatic trap), synthetic New X Pomodoro first on create, reason in rowMeta; docs protocol/task-pickers/capture-previews/refs updated. Verified: swift test on athena 1745 tests 0 failures (incl 15 new), just docs-check passed, swift-format applied to changed lines. Not verified: macOS-only view/selection targets (mac offline) and live-bob fixture recording (workspace bob build deferred; fixtures are contract-derived with README provenance).

## Dependencies

- **Depends on:** [bob-cli-dm.2](bob-cli-dm.2.md) ✓ · ⧖ 2026-10-28
- **Depends on:** [bob-cli-dm.4](bob-cli-dm.4.md) ✓ · ⧖ 2026-10-28
- **Blocks:** [bob-cli-dm.9](bob-cli-dm.9.md) ◐ · ⧖ 2026-10-28

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-dm.8](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-dm.8/README.md) | [bob-cli-dm.8](bob-cli-dm.8.md) | 0 |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-dm.8][1] | Need the phase scope and design file | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-dm.8/README.md

<!-- sase:referenced-by:end -->
