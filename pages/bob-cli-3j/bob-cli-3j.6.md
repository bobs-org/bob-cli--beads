# Bead: bob-cli-3j.6 — Capture markers inside capture TEXT

[Bead Pages](../README.md) / [bob-cli-3j](README.md) / bob-cli-3j.6

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.46](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.46.md) · **Assignee:** `bob-cli-3j.6` · **Size:** medium
**Created:** 2026-10-02 11:06:16 EDT · **Closed:** 2026-10-02 13:04:31 EDT
**Plan:** [202610/bob\_shell\_completion.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/bob_shell_completion.md)

## Description

capture-text: complete capture markers at the end of the active TEXT word through an in-process capture_complete extraction, honoring the release gates (boundary, safe rows only, end of word only, no wikilinks), using the !prefix directive.

## Notes

[2026-10-02T17:04:15Z · bob-cli-3j.6] PROPOSED FOLLOW-UP: clippy deny overly_complex_bool_expr in tests/cli/capture/pomodoro_name.rs:808 (untouched by this phase) blocks just all; fix that boolean or allow the lint

[2026-10-02T17:04:31Z · bob-cli-3j.6] capture-text live: shell_completion extraction with full-set rows, !prefix (chars), gates (suffix/newline/boundary/safe-rows/wikilink-deferred); present TEXT slot for capture trio; 15 capture_text goldens + read-only TEXT slots pass; full cargo test green (1517+771); fmt clean; clippy blocked only by pre-existing pomodoro_name.rs deny (noted as follow-up)

## Dependencies

- **Depends on:** [bob-cli-3j.5](bob-cli-3j.5.md) ✓ · ⧖ 2026-10-02
- **Blocks:** [bob-cli-3j.7](bob-cli-3j.7.md) ✓ · ⧖ 2026-10-02

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-3j.6](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-3j.6/README.md) | [bob-cli-3j.6](bob-cli-3j.6.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`6b272e4`](https://github.com/bobs-org/bob-cli/commit/6b272e4af604242aa2dad2148ff20cf18a455b5b) | feat(completion): complete capture markers inside capture TEXT | [bob-cli-3j.6](bob-cli-3j.6.md) | 2026-10-02 13:09:58 EDT |
