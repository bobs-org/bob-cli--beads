# Bead: bob-cli-7w.1 — Template language core and bob capture -E

[Bead Pages](../README.md) / [bob-cli-7w](README.md) / bob-cli-7w.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.1j.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.1j.linker.w0.md) · **Assignee:** `bob-cli-7w.1` · **Size:** medium
**Created:** 2026-10-15 14:04:18 EDT · **Closed:** 2026-10-15 14:43:59 EDT
**Plan:** [202610/bulk\_capture\_templates.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/bulk_capture_templates.md)

## Description

language: add the pure template module (framing, placeholders, row lexer, expansion, bounds, issue vocabulary) and its first consumer, `bob capture -E, --expand`.

## Notes

[2026-10-15T18:43:46Z · bob-cli-7w.1--1] PROPOSED FOLLOW-UP: Add a decisions memory record that bulk template drafts are expanded before parsing — the epic decision declined this change for the phase.

[2026-10-15T18:43:59Z · bob-cli-7w.1--1] Implemented the pure template analyzer/expander and bob capture -E with JSON and identity output; updated glossary:bulk-capture. Verified cargo fmt, clippy, all 2,612 library tests, all 1,606 CLI tests, and the complete just check gate passed. Recorded the declined decision-memory change as a proposed follow-up; epic-symbol check reported none.

## Dependencies

- **Blocks:** [bob-cli-7w.2](bob-cli-7w.2.md) ◐ · ⧖ 2026-10-15

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-7w.1](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-7w.1.md) | [bob-cli-7w.1](bob-cli-7w.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`946c9b7`](https://github.com/bobs-org/bob-cli/commit/946c9b7d166a16a24868b9929a8e552563d5ed78) | feat(capture): add template language and expansion CLI | [bob-cli-7w.1](bob-cli-7w.1.md) | 2026-10-15 14:45:00 EDT |
