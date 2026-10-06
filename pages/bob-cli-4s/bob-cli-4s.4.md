# Bead: bob-cli-4s.4 — create routes web article URLs through the clip engine

[Bead Pages](../README.md) / [bob-cli-4s](README.md) / bob-cli-4s.4

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.research.3r.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.research.3r.linker.w0.md) · **Assignee:** `bob-cli-4s.4` · **Size:** small
**Created:** 2026-10-06 15:45:26 EDT · **Closed:** 2026-10-06 17:01:57 EDT
**Plan:** [202610/highlights\_create\_listen.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/highlights_create_listen.md)

## Description

article-targets: refactor clip into a callable engine and route create's HTML and bot-walled URL targets through it with create's options, explicit companion audio support, and tests.

## Notes

[2026-10-06T21:01:27Z · bob-cli-4s.4] PROPOSED FOLLOW-UP: lib test every_value_arg_has_a_decision fails identically on clean base (highlights create:audio lacks kinds decision) — already tracked by task bead bob-cli-4j

[2026-10-06T21:01:31Z · bob-cli-4s.4] PROPOSED FOLLOW-UP: lib test listen_filter_renders_card_and_encoded_play_link fails identically on clean base (pandoc Lua-filter latex assertion)

[2026-10-06T21:01:35Z · bob-cli-4s.4] PROPOSED FOLLOW-UP: lib test missing_note_and_missing_section_are_warning_successes fails in parallel full-suite runs but passes in isolation, identically on clean base (order-dependent)

[2026-10-06T21:01:57Z · bob-cli-4s.4] Article route live: clip split into capture_article engine with Companion audio, create WebArticle routes through it with option mapping; 5 new CLI tests + shared fake_clip helper pass (CLI suite 1017/1017, highlights 129/129); fmt/clippy clean; 3 lib failures reproduce identically on clean base (recorded as follow-ups, kinds failure tracked by bob-cli-4j)

## Dependencies

- **Depends on:** [bob-cli-4s.3](bob-cli-4s.3.md) ✓ · ⧖ 2026-10-06
- **Blocks:** [bob-cli-4s.5](bob-cli-4s.5.md) ✓ · ⧖ 2026-10-06

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-4s.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-4s.4/README.md) | [bob-cli-4s.4](bob-cli-4s.4.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`0779e7d`](https://github.com/bobs-org/bob-cli/commit/0779e7d069958c5227fd5fbf746e6b85909e4ac7) | feat(highlights): route create WebArticle targets through clip engine | [bob-cli-4s.4](bob-cli-4s.4.md) | 2026-10-06 17:03:33 EDT |
