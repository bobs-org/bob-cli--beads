# Bead: bob-cli-4s.1 — Configurable listen command contract and runner

[Bead Pages](../README.md) / [bob-cli-4s](README.md) / bob-cli-4s.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.research.3r.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.research.3r.linker.w0.md) · **Assignee:** `bob-cli-4s.1` · **Size:** small
**Created:** 2026-10-06 15:45:26 EDT · **Closed:** 2026-10-06 15:56:29 EDT
**Plan:** [202610/highlights\_create\_listen.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/highlights_create_listen.md)

## Description

listen-command: add highlights.listen_command plus its env override, a template parser with shell-quoted {target}/{pdf}/{audio}/{title} placeholders, a runner that streams output unchanged and verifies the MP3 written to {audio}, and a doctor row.

## Notes

[2026-10-06T19:56:03Z · bob-cli-4s.1] PROPOSED FOLLOW-UP: lib test listen_filter_renders_card_and_encoded_play_link fails identically on clean base (create.rs:1172 LaTeX card expectation)

[2026-10-06T19:56:07Z · bob-cli-4s.1] PROPOSED FOLLOW-UP: lib test completion kinds every_value_arg_has_a_decision fails identically on clean base (highlights create:audio lacks kinds decision)

[2026-10-06T19:56:29Z · bob-cli-4s.1] listen.rs contract+runner with 12 unit tests, listen_command config+env with 3 tests, doctor row; verified: cargo fmt/clippy clean, 119 highlights CLI tests pass, doctor rows shown live (none/ok/warn); 2 lib failures reproduce on clean base and were filed as PROPOSED FOLLOW-UPs

## Dependencies

- **Blocks:** [bob-cli-4s.5](bob-cli-4s.5.md) ◐ · ⧖ 2026-10-06

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-4s.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-4s.1/README.md) | [bob-cli-4s.1](bob-cli-4s.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`476f4ae`](https://github.com/bobs-org/bob-cli/commit/476f4ae1caa1e86c40611336ce9ccac24032e16f) | feat(highlights): add configurable listen command contract and runner | [bob-cli-4s.1](bob-cli-4s.1.md) | 2026-10-06 15:57:05 EDT |
