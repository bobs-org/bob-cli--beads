# Bead: bob-cli-5j.1 — Render paired return links in Markdown PDFs

[Bead Pages](../README.md) / [bob-cli-5j](README.md) / bob-cli-5j.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.research.3x.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.research.3x.linker.w0.md) · **Assignee:** `bob-cli-5j.1` · **Size:** medium
**Created:** 2026-10-07 14:27:22 EDT · **Closed:** 2026-10-07 15:41:12 EDT
**Plan:** [202610/ref\_create\_return\_links.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/ref_create_return_links.md)

## Description

render: add a second pandoc Lua filter plus TeX macros that resolve, tag, and pair every eligible same-document link with a return-pill row at its target, unify the link ink, report pairing counts and dead-link warnings from bob, and cover it with filter, XeLaTeX, and CLI tests plus docs.

## Notes

[2026-10-07T19:18:53Z · bob-cli-5j.1] PROPOSED FOLLOW-UP: listen_filter_renders_card_and_encoded_play_link fails identically on clean base (expects \&-escaped URI in \BobListenCard output, pandoc 3.1.11.1 emits bare &); needs a task bead for the code-break filter URI escaping

[2026-10-07T19:34:42Z · bob-cli-5j.1] PROPOSED FOLLOW-UP: completion::kinds every_value_arg_has_a_decision fails identically on clean base; needs a task bead for the completion kinds coverage

[2026-10-07T19:38:03Z · bob-cli-5j.1] PROPOSED FOLLOW-UP: cli capture_url_with_markers_or_flags_stays_a_task fails identically on clean base (xclip needs an X display; headless environment issue)

[2026-10-07T19:41:12Z · bob-cli-5j.1] Render phase verified: return_links.lua filter plus return_links.tex macros tag every eligible same-document link and pair it with a return-pill row; create.rs runs both filters, unifies link ink, prints the links: line after pages: and dead/duplicate warnings on stderr. 19 return_links unit+filter tests, XeLaTeX integration (35 paired over 7 targets with dest/pill/page asserts on the stamped PDF), and the CLI links report test all pass; fmt and clippy clean; visual QA of a 2-page real render matches the spec. Full gate is red only on 3 failures that reproduce identically on the clean base (listen card URI escaping expectation, completion kinds decision test, xclip-no-display capture test), each recorded as a PROPOSED FOLLOW-UP note.

## Dependencies

- **Blocks:** [bob-cli-5j.2](bob-cli-5j.2.md) ◐ · ⧖ 2026-10-07

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-5j.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-5j.1/README.md) | [bob-cli-5j.1](bob-cli-5j.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`d4fab34`](https://github.com/bobs-org/bob-cli/commit/d4fab34ab6c4b2911624f849a95e9adfba48f101) | feat(highlights): render paired return links in Markdown PDFs | [bob-cli-5j.1](bob-cli-5j.1.md) | 2026-10-07 15:42:33 EDT |
