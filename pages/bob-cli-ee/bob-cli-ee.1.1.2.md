# Bead: bob-cli-ee.1.1.2 — Editor spans and transparent completion parsing

[Bead Pages](../README.md) / [bob-cli-ee.1.1](bob-cli-ee.1.1.md) / bob-cli-ee.1.1.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.bob-cli-ee.1](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-ee.1.md) · **Assignee:** `bob-cli-ee.1.1.2` · **Size:** medium
**Created:** 2026-10-30 04:33:10 EDT · **Closed:** 2026-10-30 06:49:15 EDT
**Plan:** [202610/capture\_type\_grammar.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/capture_type_grammar.md)

## Description

editor: consume the shared masked view before editor claims and existing completion detection. Add task_type spans, needs, diagnostics, shared exact-name resolution and ThemeRefs. Verify offsets, neighboring completion, rewrite, similar-task bodies and the masking invariant without implementing the new task_type completion menu owned by bob-cli-ee.3.

## Notes

[2026-10-30T10:49:15Z · bob-cli-ee.1.1.2] Editor consumes the shared masked view before all claims: task_type spans, TaskType need, and shared teaching diagnostics (needs-task, invalid, duplicate, not-applicable with execution-identical copy). Exact-name resolution prefers configured vocabulary, then catalog, with slug hyphen-fallback and no prefix matching. Verified: neighboring route/caret/query completion keeps original ranges, separator toggle preserves t:, bodies exclude markers (incl. related matching), masking-parity over grammar families plus execution/editor parity, ThemeRefs with authored name ranges, just check green (fmt, repo clippy gate, full workspace tests), epic-symbols clean.

## Dependencies

- **Depends on:** [bob-cli-ee.1.1.1](bob-cli-ee.1.1.1.md) ✓ · ⧖ 2026-10-30
- **Blocks:** [bob-cli-ee.1.1.3](bob-cli-ee.1.1.3.md) ✓ · ⧖ 2026-10-30

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-ee.1.1.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-ee.1.1.2/README.md) | [bob-cli-ee.1.1.2](bob-cli-ee.1.1.2.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`23ba480`](https://github.com/bobs-org/bob-cli/commit/23ba4805ecbdd6741b4e47d2e3a01b0317849640) | feat(capture): editor spans and transparent completion parsing | [bob-cli-ee.1.1.2](bob-cli-ee.1.1.2.md) | 2026-10-30 06:50:59 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-ee.1.1.2][1] | Check phase notes for earlier work | 4 |
| read-by | [agent:bob-cli-ee.1.1.land--1][2] | Verify the editor parsing child phase and its notes | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-ee.1.1.2/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-ee.1.1.land.md

<!-- sase:referenced-by:end -->
