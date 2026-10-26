# Bead: bob-cli-cc.3 — Write-once source store and the source\_markdown pointer

[Bead Pages](../README.md) / [bob-cli-cc](README.md) / bob-cli-cc.3

**Status:** ◐ in_progress · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.research.5b.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.research.5b.linker.w0.md) · **Assignee:** `bob-cli-cc.3` · **Size:** medium
**Created:** 2026-10-26 09:00:55 EDT
**Plan:** [202610/ref\_code\_block\_copy.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/ref_code_block_copy.md)

## Description

store: persist source.md plus code.json under .bob/ref-sources at create time, record the source_markdown pointer through every intake path, include the store in the ingest commit, warn when the catalog is gitignored, allow it in athena's vault .gitignore, and expose the pointer on RefRow.

## Dependencies

- **Depends on:** [bob-cli-cc.1](bob-cli-cc.1.md) ✓ · ⧖ 2026-10-26
- **Depends on:** [bob-cli-cc.2](bob-cli-cc.2.md) ✓ · ⧖ 2026-10-26
- **Blocks:** [bob-cli-cc.4](bob-cli-cc.4.md) ◐ · ⧖ 2026-10-26
- **Blocks:** [bob-cli-cc.5](bob-cli-cc.5.md) ◐ · ⧖ 2026-10-26
- **Blocks:** [bob-cli-cc.6](bob-cli-cc.6.md) ◐ · ⧖ 2026-10-26

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-cc.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-cc.3/README.md) | [bob-cli-cc.3](bob-cli-cc.3.md) | 0 |
