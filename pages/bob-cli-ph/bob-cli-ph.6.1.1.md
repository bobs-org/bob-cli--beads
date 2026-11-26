# Bead: bob-cli-ph.6.1.1 — Extract the shared place lexer and resolver without changing behavior

[Bead Pages](../README.md) / [bob-cli-ph.6.1](bob-cli-ph.6.1.md) / bob-cli-ph.6.1.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.bob-cli-ph.6](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-ph.6.md) · **Assignee:** `bob-cli-ph.6.1.1` · **Size:** medium
**Created:** 2026-11-25 08:39:52 EST · **Closed:** 2026-11-25 09:40:01 EST
**Plan:** [202611/capture\_true\_case\_drawers.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/capture_true_case_drawers.md)

## Description

shared-place: introduce capture_language/place.rs with TaskDrawer, ProjectSection, and NotebookSection adapters. Consolidate selector lexing and matching while preserving existing scope policies and passing existing suites unchanged. Remove obsolete selector helpers only after auditing their callers.

## Notes

[2026-11-25T14:40:01Z · bob-cli-ph.6.1.1] Extracted capture_language/place.rs with TaskDrawer, ProjectSection, and NotebookSection adapters; scanners and live resolvers wrap it. Dead select_drawer/match_drawer/suggest_drawer helpers removed after caller audit. Cross-scope tests cover quoted/key/slug/create, case-twin ambiguity, reserved nouns, near-miss thresholds, and notebook create-title casing. Existing capture_drawers, drawer_bullet, section_bullet, notebook, and exact_name suites pass; GRAMMAR_REVISION stays 29. Clippy -D unused plus project clippy_gate pass on --lib --tests. epic-symbols: none.

## Dependencies

- **Blocks:** [bob-cli-ph.6.1.2](bob-cli-ph.6.1.2.md) ✓ · ⧖ 2026-11-25

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-ph.6.1.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-ph.6.1.1/README.md) | [bob-cli-ph.6.1.1](bob-cli-ph.6.1.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`45a5434`](https://github.com/bobs-org/bob-cli/commit/45a54345f59c7cefec7121ac46f61fe34ba3fbf1) | refactor(capture): extract shared place lexer and resolver | [bob-cli-ph.6.1.1](bob-cli-ph.6.1.1.md) | 2026-11-25 09:41:35 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-ph.6.1.1][1] | Need the phase scope, design file, notes, and epic DECISIONS | 5 |
| read-by | [agent:bob-cli-ph.6.1.land][2] | Need the child scope and notes | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-ph.6.1.1/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-ph.6.1.land/README.md

<!-- sase:referenced-by:end -->
