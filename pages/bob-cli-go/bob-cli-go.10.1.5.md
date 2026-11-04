# Bead: bob-cli-go.10.1.5 — Transfer documentation and integrated verification

[Bead Pages](../README.md) / [bob-cli-go.10.1](bob-cli-go.10.1.md) / bob-cli-go.10.1.5

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.bob-cli-go.10](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-go.10.md) · **Assignee:** `bob-cli-go.10.1.5` · **Size:** medium
**Created:** 2026-11-04 01:50:45 EST · **Closed:** 2026-11-04 08:03:54 EST
**Plan:** [202611/capture\_transfer.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/capture_transfer.md)

## Description

transfer-delivery: publish quoted help and transfer contracts, regenerate documentation, fill cross-item rollback and compatibility coverage, and run scratch-vault and repository gates. Supply closeout evidence for this child epic's land agent; no phase worker closes bob-cli-go.10 or bob-cli-go.

## Notes

[2026-11-04T13:03:25Z · bob-cli-go.10.1.5] PROPOSED FOLLOW-UP: docs token-coverage exact-spelling gap — tools/docs/tests/test_capture_token_coverage.py::test_every_capture_token_has_a_literal_query_at_its_heading fails on clean base (dad9e660 stashed): token spelling @route+id @route+id at #plus-child-target-run has no literal smoke query (existing query adds prose words). Transfer rows added here pass.

[2026-11-04T13:03:33Z · bob-cli-go.10.1.5] PROPOSED FOLLOW-UP: docs contracts drift-test blocked by memory frontmatter — tools/docs/tests/test_contracts.py::test_check_mode_reports_generated_page_drift_without_writing fails identically on clean base: repo fixture copy of sase/memory/glossary/task-merge.md has no frontmatter (same root cause as the bob-docs gen/drift gate owned by bob-cli-go memory closeout).

[2026-11-04T13:03:54Z · bob-cli-go.10.1.5] transfer-delivery done. Published: capture.md Moving-and-merging-tasks-with-> section + task_move/task_merge kinds + grammar-10 parse/JSON text; capture-syntax.md one >-transfer token row + #transfer section with 4 quoted scratch examples; 4 search_smoke queries; json-outputs.md + compatibility.md grammar-10 + transfer shapes; capture --help transfer paragraph + 4 quoted examples; task move --help quoted > example; docs-gen goldens regenerated (capture-parse/complete grammar 10, capture.md, task.md). Verified: cargo fmt clean, git diff --check clean, cargo clippy gate passed (just-check reached tests), 129 focused CLI tests pass (transfer/help/task_move/docs_reference), scratch vault with just-built binary: capture-parse reports task_merge+transfer drawer object at grammar 10, dry-run kind task_move with 2 moves, all 4 experience captures write expected blocks (moved/merged human lines, drawer/section targets, LINKED FROM provenance), reconcile converges, shell-guard smoke refuses with canonical copy. docs lint ok (trimmed capture-syntax.md to 6000-word cap). Pre-existing, reproduced identically on stashed tree: 5 lib arrow-false-positive failures + cli capture_bracketed_url (recorded in 10.1.4 note 1, persists; lexer fix deferred to land-agent triage), bob-docs gen/drift frontmatter block on sase/memory/glossary/task-merge.md (owned by bob-cli-go memory closeout, not edited here), docs token-coverage exact-spelling gap and contracts drift-test failure (filed as PROPOSED FOLLOW-UP on this bead). No memory/version/changelog edits; single grammar increment preserved; no epic-symbol leftovers.

## Dependencies

- **Depends on:** [bob-cli-go.10.1.4](bob-cli-go.10.1.4.md) ✓ · ⧖ 2026-11-04

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-go.10.1.5](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-go.10.1.5/README.md) | [bob-cli-go.10.1.5](bob-cli-go.10.1.5.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`d25080e`](https://github.com/bobs-org/bob-cli/commit/d25080e16cfa7f45f71ed285ae2739613069d7ab) | docs(capture): publish \> transfer contracts and grammar-10 references | [bob-cli-go.10.1.5](bob-cli-go.10.1.5.md) | 2026-11-04 08:05:40 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-go.10.1.5][1] | Need the phase scope and design file | 2 |
| read-by | [agent:bob-cli-go.10.1.land][2] | Need the child scope and notes | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-go.10.1.5/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-go.10.1.land/README.md

<!-- sase:referenced-by:end -->
