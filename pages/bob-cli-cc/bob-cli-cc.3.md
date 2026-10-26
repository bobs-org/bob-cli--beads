# Bead: bob-cli-cc.3 — Write-once source store and the source\_markdown pointer

[Bead Pages](../README.md) / [bob-cli-cc](README.md) / bob-cli-cc.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.research.5b.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.research.5b.linker.w0.md) · **Assignee:** `bob-cli-cc.3` · **Size:** medium
**Created:** 2026-10-26 09:00:55 EDT · **Closed:** 2026-10-26 11:17:26 EDT
**Plan:** [202610/ref\_code\_block\_copy.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/ref_code_block_copy.md)

## Description

store: persist source.md plus code.json under .bob/ref-sources at create time, record the source_markdown pointer through every intake path, include the store in the ingest commit, warn when the catalog is gitignored, allow it in athena's vault .gitignore, and expose the pointer on RefRow.

## Notes

[2026-10-26T15:17:26Z · bob-cli-cc.3] Store phase landed: source_store write-once module with code.json v1, birth pointer via find_birth_store in sync, RefRow.source_markdown + show markdown row, create wiring for markdown/-M/snapshot with source_markdown/code lines and dry-run planned pointer, ingest commit includes store (pre-sync no-op per spec), shared vault_git helper, docs (highlights-create Saved Markdown, ref-sync pointer, vault-git-sync Reference sources, vault-format tree, json-outputs additive), vault ~/bob allowlist committed as 4c463bdd and vault-sync clean. Verified: cargo fmt/clippy clean, cargo test --lib 3585 ok, highlights integration 511 ok, ref_library 143 ok, source_store unit 3 ok.

## Dependencies

- **Depends on:** [bob-cli-cc.1](bob-cli-cc.1.md) ✓ · ⧖ 2026-10-26
- **Depends on:** [bob-cli-cc.2](bob-cli-cc.2.md) ✓ · ⧖ 2026-10-26
- **Blocks:** [bob-cli-cc.4](bob-cli-cc.4.md) ✓ · ⧖ 2026-10-26
- **Blocks:** [bob-cli-cc.5](bob-cli-cc.5.md) ✓ · ⧖ 2026-10-26
- **Blocks:** [bob-cli-cc.6](bob-cli-cc.6.md) ✓ · ⧖ 2026-10-26

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-cc.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-cc.3/README.md) | [bob-cli-cc.3](bob-cli-cc.3.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`009060f`](https://github.com/bobs-org/bob-cli/commit/009060f9b4b2b09f67c1d7754a23c9c64923a412) | feat(highlights-ref): write-once source store and source\_markdown pointer | [bob-cli-cc.3](bob-cli-cc.3.md) | 2026-10-26 11:18:37 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-cc.3][1] | Need the phase scope and design file | 2 |
| read-by | [agent:bob-cli-cc.5][2] | Need store phase outcomes that lifecycle depends on | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-cc.3/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-cc.5/README.md

<!-- sase:referenced-by:end -->
