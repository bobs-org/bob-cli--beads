# Bead: bob-cli-go.1 — Contract docs, canonical copy, and split vectors

[Bead Pages](../README.md) / [bob-cli-go](README.md) / bob-cli-go.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.36.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.36.linker.w0.md) · **Assignee:** `bob-cli-go.1` · **Size:** medium
**Created:** 2026-11-03 16:11:30 EST · **Closed:** 2026-11-03 17:01:48 EST
**Plan:** [202611/task\_move\_merge\_split.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/task_move_merge_split.md)

## Description

contract: write the task-merge and task-split contract pages, the relations §2/§21 merge-label contract, the many-source move docs, the shared copy table, and the byte-exact split conformance vectors that the Rust and JS planners must both pass.

## Notes

[2026-11-03T22:01:30Z · bob-cli-go.1] PROPOSED FOLLOW-UP: docs-check published-URLs gate fails on live-site drift — https://bobs-org.github.io/attachments/ and /reference/cli/attachments/ are published live but attachments.md never existed in this checkout; reproduces identically on the clean base tree (verified via stash + rebuild: 190 pages, same 2 failures)

[2026-11-03T22:01:48Z · bob-cli-go.1] Contract phase landed: docs/task-merge.md + docs/task-split.md (status admonitions naming merge-engine/merge-cli/merge-label/split-cli/nav-split phases), task-relations §2 merge exception + new §21 ML1-ML8 + merge_labels sample config, task-move -t section, tests/fixtures/task_split/vectors.json SP1-SP30 + README (mints from real mint_block_id probe), contracts.yml orders 29/30 + mkdocs llmstxt, regenerated indexes, test_contracts.py pins bumped 38->40. Verified: lint/drift/strict-build/links/edit-links/search-smoke/tutorial/media/docs-pytest-447 pass; lychee 0 errors. Only published-URLs fails, reproduced identically on clean base (recorded as follow-up). No Rust/JS written; no memory notes touched.

## Dependencies

- **Blocks:** [bob-cli-go.3](bob-cli-go.3.md) ✓ · ⧖ 2026-11-03
- **Blocks:** [bob-cli-go.4](bob-cli-go.4.md) ✓ · ⧖ 2026-11-03

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-go.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-go.1/README.md) | [bob-cli-go.1](bob-cli-go.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`8d2eb09`](https://github.com/bobs-org/bob-cli/commit/8d2eb09f6646faf3a17abb7998a7c1661a46044b) | docs(contract): task-merge and task-split contracts, merge-label relations, split vectors | [bob-cli-go.1](bob-cli-go.1.md) | 2026-11-03 17:12:02 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-go.1][1] | Need the phase scope and design file | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-go.1/README.md

<!-- sase:referenced-by:end -->
