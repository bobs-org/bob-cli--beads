# Bead: bob-cli-cc.4 — bob ref code read surface

[Bead Pages](../README.md) / [bob-cli-cc](README.md) / bob-cli-cc.4

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.research.5b.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.research.5b.linker.w0.md) · **Assignee:** `bob-cli-cc.4` · **Size:** medium
**Created:** 2026-10-26 09:00:55 EDT · **Closed:** 2026-10-26 11:39:27 EDT
**Plan:** [202610/ref\_code\_block\_copy.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/ref_code_block_copy.md)

## Description

code-cmd: add the read-only bob ref code command (human, json, markdown, raw, page filter, saved source) with its versioned JSON contract, bob-computed summaries and fenced forms, help, completion, and docs.

## Notes

[2026-10-26T15:39:27Z · bob-cli-cc.4] Implemented the read-only bob ref code command and its JSON, human, Markdown, raw, page-filter, and saved-source modes; updated help, completion, and reference docs. Verified cargo fmt --check, cargo check --bin bob, command help, and that no epic-symbol entries remain. No tests were run.

## Dependencies

- **Depends on:** [bob-cli-cc.3](bob-cli-cc.3.md) ✓ · ⧖ 2026-10-26
- **Blocks:** [bob-cli-cc.6](bob-cli-cc.6.md) ○ · ⧖ 2026-10-26
- **Blocks:** [bob-cli-cc.8](bob-cli-cc.8.md) ✓ · ⧖ 2026-10-26

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-cc.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-cc.4/README.md) | [bob-cli-cc.4](bob-cli-cc.4.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`fb28faa`](https://github.com/bobs-org/bob-cli/commit/fb28faa1af7094601f2762a03ff681301a836d50) | feat(ref): add saved code catalog read command | [bob-cli-cc.4](bob-cli-cc.4.md) | 2026-10-26 11:40:34 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-cc.4][1] | Need the phase scope and design file | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-cc.4/README.md

<!-- sase:referenced-by:end -->
