# Bead: bob-cli-4s.2 — URL fetcher, arXiv identity and metadata, and shared dedupe

[Bead Pages](../README.md) / [bob-cli-4s](README.md) / bob-cli-4s.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.research.3r.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.research.3r.linker.w0.md) · **Assignee:** `bob-cli-4s.2` · **Size:** small
**Created:** 2026-10-06 15:45:26 EDT · **Closed:** 2026-10-06 16:04:38 EDT
**Plan:** [202610/highlights\_create\_listen.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/highlights_create_listen.md)

## Description

fetch-arxiv: add a curl-based fetcher that validates every redirect hop, arXiv URL parsing that mirrors sase-listen, arXiv API metadata, the short-title stem rule, and a shared dedupe module with arXiv and legacy url keys.

## Notes

[2026-10-06T20:03:50Z · bob-cli-4s.2] PROPOSED FOLLOW-UP: create::tests::listen_filter_renders_card_and_encoded_play_link fails identically on clean base tree (likely 4s.1 territory)

[2026-10-06T20:03:56Z · bob-cli-4s.2] PROPOSED FOLLOW-UP: completion::kinds every_value_arg_has_a_decision fails identically on clean base tree; capture_pomodoros missing_note test flakes under parallel runs

[2026-10-06T20:04:38Z · bob-cli-4s.2] fetch.rs (curl, manual redirects, exit-code map), arxiv.rs (sase-listen verbatim tables, Atom metadata, author display), short_title_stem + pdf_meta.rs, arXiv dedupe key, sources.rs (legacy url, source_pdf/audio). Verified: cargo fmt clean, clippy 0 errors, all 113 highlights CLI tests pass incl. new legacy-url test, lib unit tests pass; only failures are 2 pre-existing base failures (recorded as follow-ups) plus a pre-existing parallel flake

## Dependencies

- **Blocks:** [bob-cli-4s.3](bob-cli-4s.3.md) ◐ · ⧖ 2026-10-06

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-4s.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-4s.2/README.md) | [bob-cli-4s.2](bob-cli-4s.2.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`fb77b56`](https://github.com/bobs-org/bob-cli/commit/fb77b56e3b6b20776787ab809631a7a64a777be2) | feat(highlights): add native highlights\_ref fetch, arxiv, clip, and dedupe | [bob-cli-4s.2](bob-cli-4s.2.md) | 2026-10-06 16:06:43 EDT |
