# Bead: bob-cli-q5.1.1.1 — Snooze row, clock, and resolved-state contracts

[Bead Pages](../README.md) / [bob-cli-q5.1.1](bob-cli-q5.1.1.md) / bob-cli-q5.1.1.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-q5.1](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-q5.1.md) · **Assignee:** `bob-cli-q5.1.1.1` · **Size:** medium
**Created:** 2026-11-25 10:36:15 EST · **Closed:** 2026-11-25 12:14:42 EST
**Plan:** [202611/snooze\_wake\_engine.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/snooze_wake_engine.md)

## Description

row-model: build src/native/snooze parsing, injected zoned time grammar, resolved row classification, and live_targets reader API. Establish docs/snooze.md and shared rows/when/live vectors with concrete schemas for all six vector groups. Reserve Snoozed as a structural H2. Follow the row-model section and inherited decisions; leave mutation, CLI, and reader integrations to their owners. Run focused conformance tests and applicable repository gates.

## Notes

[2026-11-25T17:14:19Z · bob-cli-q5.1.1.1] PROPOSED FOLLOW-UP: wispr summary test native::meetings::profile::tests::wispr_summary_renders_one_or_two_pages_with_stable_words fails identically on clean base (verified via stash); font/rendering environment issue, unrelated to snooze row-model

[2026-11-25T17:14:28Z · bob-cli-q5.1.1.1] PROPOSED FOLLOW-UP: just docs-check lint fails identically on clean base (verified via stash): docs/reference/plugins/bob-navigation-hotkeys.md exceeds reference budget (6068 words, cap 6000); pre-existing, unrelated to docs/snooze.md

[2026-11-25T17:14:42Z · bob-cli-q5.1.1.1] Row-model done and verified: src/native/snooze/{mod,parse,when,state,vectors}.rs with 23 snooze unit+vector tests passing; tests/fixtures/snooze/vectors.json (rows 16, when 19, live 13; snooze/wake/cleanup documented empty for mutation-planners); docs/snooze.md + contracts/nav registration via just docs-gen; Snoozed reserved as structural H2 with refusal in task-drawer resolve (new test). Gates: cargo fmt clean, workspace clippy clean, full lib suite sharded green (7508+319+61+245+998 pass; 7 parallel-flakes pass serially), drawer CLI integration 37 pass, docs_reference pass. Two pre-existing failures reproduce identically on clean base and are recorded as PROPOSED FOLLOW-UPs (wispr render test, docs-check plugin budget). epic-symbols clean.

## Dependencies

- **Blocks:** [bob-cli-q5.1.1.2](bob-cli-q5.1.1.2.md) ◐ · ⧖ 2026-11-25

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-q5.1.1.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-q5.1.1.1/README.md) | [bob-cli-q5.1.1.1](bob-cli-q5.1.1.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`cd59455`](https://github.com/bobs-org/bob-cli/commit/cd594550547b07285f54a181896b69c3233a29a3) | feat(snooze): add later-today row-model contracts, vectors, and docs | [bob-cli-q5.1.1.1](bob-cli-q5.1.1.1.md) | 2026-11-25 12:15:51 EST |
