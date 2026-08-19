# Bead: bob-cli-10.2 — Three-component \`@route+block-id#section\` marker grammar

[Bead Pages](../README.md) / [bob-cli-10](README.md) / bob-cli-10.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.085](https://github.com/bobs-org/bob-cli--agents/blob/main/families/bbugyi200.athena.085.md) · **Assignee:** `bob-cli-10.2` · **Size:** medium
**Created:** 2026-08-19 16:04:39 EDT · **Closed:** 2026-08-19 16:46:29 EDT
**Plan:** [202608/capture\_task\_sections.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202608/capture_task_sections.md)

## Description

grammar: extend bob-cli's capture grammar so a sub-bullet marker accepts a trailing `#<section>` component, with new span, need, and completion-field values, precise usage errors for every malformed shape, additive `capture-parse` output, updated help/README, and exhaustive lexical tests that keep the bare trailing `#` Pomodoro-note marker and `@route#section` note-bullet marker unchanged.

## Notes

[2026-08-19T20:46:29Z · bob-cli-10.2] Extended the sub-bullet family to @route+block-id#section: CaptureKind::SubBullet now carries Option<TaskSectionSelector>, MarkerParse populates block_id and section together, and capture-parse reports span sub_bullet_section plus need task_section. @foo+bar#req is a complete sub_bullet; @foo+bar# / @foo+#req / @foo+# are incomplete with ordered needs. Distinct usage errors for empty selector, disallowed selector chars, empty block-id with a selector, and empty route. Completion after # is task_section with the typed block_id; route/task contexts keep block_id=None and # is not in either replacement range. Insertion fail-closes on section: Some(_). Bare trailing # stays Pomodoro-note, @route#Ideas stays note-bullet, ^/: /:: unchanged; @foo+bad#section is now a valid sub-bullet. just fmt, just lint, just test, and git diff --check passed. No leftover --epic-symbol entries.

[2026-08-19T20:48:12Z · bob-cli-10.2] Extended the sub-bullet family to @route+block-id#section: CaptureKind::SubBullet now carries Option<TaskSectionSelector>, MarkerParse populates block_id and section together, and capture-parse reports span sub_bullet_section plus need task_section. @foo+bar#req is a complete sub_bullet; @foo+bar# / @foo+#req / @foo+# are incomplete with ordered needs. Distinct usage errors for empty selector, disallowed selector chars, empty block-id with a selector, and empty route. Completion after # is task_section with the typed block_id; route/task contexts keep block_id=None and # is not in either replacement range. Insertion fail-closes on section: Some(_). Bare trailing # stays Pomodoro-note, @route#Ideas stays note-bullet, ^/: /:: unchanged; @foo+bad#section is now a valid sub-bullet. just fmt, just lint, just test, and git diff --check passed. No leftover --epic-symbol entries.

## Dependencies

- **Depends on:** [bob-cli-10.1](bob-cli-10.1.md) ✓ · ⧖ 2026-08-19
- **Blocks:** [bob-cli-10.3](bob-cli-10.3.md) ✓ · ⧖ 2026-08-19
- **Blocks:** [bob-cli-10.4](bob-cli-10.4.md) ✓ · ⧖ 2026-08-19

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-10.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-10.2/README.md) | [bob-cli-10.2](bob-cli-10.2.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`8f95e87`](https://github.com/bobs-org/bob-cli/commit/8f95e87b5eb2403676ab12a898840dad00de5ad4) | feat(capture): parse @route+block-id#section sub-bullet markers | [bob-cli-10.2](bob-cli-10.2.md) | 2026-08-19 16:50:11 EDT |
