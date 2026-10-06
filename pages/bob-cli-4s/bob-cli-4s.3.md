# Bead: bob-cli-4s.3 — create accepts local PDFs, PDF URLs, and arXiv papers

[Bead Pages](../README.md) / [bob-cli-4s](README.md) / bob-cli-4s.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.research.3r.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.research.3r.linker.w0.md) · **Assignee:** `bob-cli-4s.3` · **Size:** medium
**Created:** 2026-10-06 15:45:26 EDT · **Closed:** 2026-10-06 16:45:26 EDT
**Plan:** [202610/highlights\_create\_listen.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/highlights_create_listen.md)

## Description

pdf-targets: add TARGET classification to create, a stamp-as-is PDF route with title, stem, and validation rules, private scratch staging, the new -N/-T flags and per-kind ref-type defaults, explicit --audio on every route, CLI tests with a fake curl, and docs/highlights-create.md.

## Notes

[2026-10-06T20:45:13Z · bob-cli-4s.3] PROPOSED FOLLOW-UP: lib every_value_arg_has_a_decision fails for highlights create:audio on clean base too (tracked by bob-cli-4j)

[2026-10-06T20:45:17Z · bob-cli-4s.3] PROPOSED FOLLOW-UP: lib listen_filter_renders_card_and_encoded_play_link ampersand escaping fails on clean base too (tracked by bob-cli-4u)

[2026-10-06T20:45:26Z · bob-cli-4s.3] pdf-targets done: TARGET classification, stamp-as-is PDF route with title/stem/validation, scratch staging, -N/-T and per-kind ref-type, explicit --audio on every route, curl doctor row, completion target *.{md,pdf}, help Targets section, 11 new CLI tests with fake curl, docs/highlights-create.md + links + README; verified cargo fmt --check, cargo clippy exit 0, cargo test --test cli 1012 passed, epic-symbols clean; 2 lib failures pre-existing on base (bob-cli-4j audio kinds, bob-cli-4u listen-card) recorded as follow-ups

## Dependencies

- **Depends on:** [bob-cli-4s.2](bob-cli-4s.2.md) ✓ · ⧖ 2026-10-06
- **Blocks:** [bob-cli-4s.4](bob-cli-4s.4.md) ◐ · ⧖ 2026-10-06

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-4s.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-4s.3/README.md) | [bob-cli-4s.3](bob-cli-4s.3.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`fa7c7b0`](https://github.com/bobs-org/bob-cli/commit/fa7c7b002931cface784e19e85778d151754a37a) | feat(highlights): accept markdown, local PDF, PDF URL, and arXiv targets in create | [bob-cli-4s.3](bob-cli-4s.3.md) | 2026-10-06 16:47:07 EDT |
