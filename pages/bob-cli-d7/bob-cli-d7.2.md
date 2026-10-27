# Bead: bob-cli-d7.2 — Stop pandoc numbering headings the author already numbered

[Bead Pages](../README.md) / [bob-cli-d7](README.md) / bob-cli-d7.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.14v](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.14v.md) · **Assignee:** `bob-cli-d7.2` · **Size:** medium
**Created:** 2026-10-27 14:54:31 EDT · **Closed:** 2026-10-27 15:14:03 EDT
**Plan:** [202610/backlog\_batch\_a1.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/backlog_batch_a1.md)

## Description

manual-heading-numbers: teach the number_from_top_level Lua pass to leave self-numbered Markdown documents unnumbered but listed, cover it with filter tests and a scratch render, update docs/highlights-create.md, and close bob-cli-58.

## Notes

[2026-10-27T19:14:03Z · bob-cli-d7.2] Manual-heading double numbering fixed and covered: has_manual_number + self-numbered unnumbering in the number_from_top_level Lua pass (src/native/highlights_ref/create.rs), 5 new pandoc-backed filter tests (self-numbered/mixed/year-led/lone-H1+numbered/no-manual-numbers) — 14/14 section_numbering lib tests pass, scratch renders verified via pdftotext (fixture TOC '1. Summary' not '1 1. Summary'; real agent report keeps pandoc numbering), docs/highlights-create.md numbering paragraph updated, just docs-check and just check pass. Closed bob-cli-58 with evidence. No PROPOSED FOLLOW-UP items.

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-d7.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-d7.2/README.md) | [bob-cli-d7.2](bob-cli-d7.2.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`f771b19`](https://github.com/bobs-org/bob-cli/commit/f771b196562ae6b6f60e4c12a086e4cecc2f02de) | fix(ref): stop pandoc numbering self-numbered Markdown headings | [bob-cli-d7.2](bob-cli-d7.2.md) | 2026-10-27 15:15:23 EDT |
