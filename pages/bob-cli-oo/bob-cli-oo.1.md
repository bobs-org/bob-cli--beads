# Bead: bob-cli-oo.1 — Shared note cleaner, disjoint note spans, and prerequisite fixes

[Bead Pages](../README.md) / [bob-cli-oo](README.md) / bob-cli-oo.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.5q.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.5q.linker.w0.md) · **Assignee:** `bob-cli-oo.1` · **Size:** medium
**Created:** 2026-11-21 12:07:07 EST · **Closed:** 2026-11-21 12:52:09 EST
**Plan:** [202611/bank\_row\_notes.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/bank_row_notes.md)

## Description

note-grammar-parity: land the byte-identical shared note-cleaner vectors and the five-step cleaner in bob's Rust parser and the plugin tokenizer, add disjoint noteSpan/noteMarkerSpan/noteEditable, move 🔁 link insertion before flag/note, protect every `$` on a row, and document the tail order in docs/bank.md.

## Notes

[2026-11-21T17:51:40Z · bob-cli-oo.1] PROPOSED FOLLOW-UP: just docs-check fails on clean master — docs/reference/vault-format.md is 6016 words over the 6000 cap; docs/develop/plugins/plugin-apis.md warns at 8165/8000. Reproduced with docs/bank.md stashed; this phase did not cause it.

[2026-11-21T17:52:09Z · bob-cli-oo.1] Verified note-grammar-parity: byte-identical note_cleaner.json (19 vectors) in bob-cli and bob-plugins; five-step cleaner in grammar.rs and 241o; disjoint noteSpan/noteMarkerSpan/noteEditable; 🔁 insert before flag/note via bankSubscriptionInsertOffset(raw.length); token.dollars + BankDollarWidget for uncovered \$ including notes; docs/bank.md canonical tail. just check green. Isolated plugin tests pass (note-grammar 3, bank-marks 16, bank-subscription 10). npm perf fails under parallel just check were load flakes (isolated event-link-times/frees-marks/nav-stage all pass). bob plugins sync -p bob-ledger-tools descendant-deployed from 7b44b29 after proving c803a4e; no -F. Fragments 241o 821 / 241p 681 / 241hc 538. No leftover --epic-symbol. Glossary deferred to note-stage. docs-check over-budget is pre-existing (PROPOSED FOLLOW-UP).

## Dependencies

- **Blocks:** [bob-cli-oo.2](bob-cli-oo.2.md) ◐ · ⧖ 2026-11-21

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-oo.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-oo.1/README.md) | [bob-cli-oo.1](bob-cli-oo.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`baca870`](https://github.com/bobs-org/bob-cli/commit/baca8701459fb39fdeb783d5cdb95ac9f2b20b21) | feat(bank): share the five-step note cleaner and document tail order | [bob-cli-oo.1](bob-cli-oo.1.md) | 2026-11-21 12:53:38 EST |
