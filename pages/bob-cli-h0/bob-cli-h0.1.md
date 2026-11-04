# Bead: bob-cli-h0.1 — Contract docs, copy tables, vectors, and the decision record

[Bead Pages](../README.md) / [bob-cli-h0](README.md) / bob-cli-h0.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.37.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.37.linker.w0.md) · **Assignee:** `bob-cli-h0.1` · **Size:** medium
**Created:** 2026-11-04 08:50:23 EST · **Closed:** 2026-11-04 09:14:03 EST
**Plan:** [202611/move\_choice.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/move_choice.md)

## Description

contract: write the `- ^^` contract into docs/capture.md and the reference pages (grammar rows, copy and refusal tables, the `move_choice` JSON, `-m`, MQ vectors) and, if accepted, the decisions record; no Rust changes.

## Notes

[2026-11-04T14:10:18Z · bob-cli-h0.1] PROPOSED FOLLOW-UP: Restore required front matter to the tracked task-merge glossary strand — docs-check fails after lint at generated drift; reproduced on clean 3741ce2e and already owned by bob-cli-go.13 (bob-cli-go note #8); this phase leaves memory untouched.

[2026-11-04T14:14:03Z · bob-cli-h0.1] Documented the - ^^ grammar, -m interface, move_choice JSON/refusal and consequence contracts, and MQ1–MQ19; no Rust or memory edits. Verified git diff --check and bob-docs lint pass. just docs-check passes lint but fails generated drift on sase/memory/glossary/task-merge.md for missing front matter; reproduced on clean 3741ce2e and owned by bob-cli-go.13. epic-symbols reports none.

## Dependencies

- **Blocks:** [bob-cli-h0.2](bob-cli-h0.2.md) ✓ · ⧖ 2026-11-04
- **Blocks:** [bob-cli-h0.3](bob-cli-h0.3.md) ◐ · ⧖ 2026-11-04

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-h0.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-h0.1/README.md) | [bob-cli-h0.1](bob-cli-h0.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`d216f7e`](https://github.com/bobs-org/bob-cli/commit/d216f7eb3bdefeaa233b5d0ed288b4c653f2df1a) | docs(capture): specify parent move choice contract | [bob-cli-h0.1](bob-cli-h0.1.md) | 2026-11-04 09:15:50 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-h0.1][1] | Verify final phase status and recorded follow-up before closing | 3 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-h0.1/README.md

<!-- sase:referenced-by:end -->
