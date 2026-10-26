# Bead: bob-cli-cc.5 — Overwrite repointing and the doctor sources check

[Bead Pages](../README.md) / [bob-cli-cc](README.md) / bob-cli-cc.5

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.research.5b.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.research.5b.linker.w0.md) · **Assignee:** `bob-cli-cc.5` · **Size:** medium
**Created:** 2026-10-26 09:00:55 EDT · **Closed:** 2026-10-26 12:19:14 EDT
**Plan:** [202610/ref\_code\_block\_copy.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/ref_code_block_copy.md)

## Description

lifecycle: make -f overwrite stage, install, repoint, and roll back the store inside its transaction, and add a bob ref doctor ref-sources row for dangling pointers, digest mismatches, orphans, and an ignored catalog.

## Notes

[2026-10-26T15:09:29Z · bob-cli-c9.5.1.land] COORDINATION (from bob-cli-c9.5.1.land): annotated overwrite landed on master (ca6065af, 8a1679e5). Annotated overwrites run through the same prepare/execute transaction but also rename the old PDF to ref_history/<type>/<stem>__<date>__annotated.pdf and assets to <archive>.assets/, write a frozen note whose frontmatter is an allowlist built in overwrite.rs render_frozen_note (title/source_url/created/parent/replaced/status_when_replaced/highlights_count/annotated_pdf/annotated_pdf_sha256 + earlier lineage), and record v2 move-aware intents in overwrite/recovery.rs. When adding source-store paths to touched/created and repointing source_markdown, cover the annotated path too and decide explicitly whether the frozen note keeps the old source_markdown pointer. A bob-cli-c9.5.1 landing tale is concurrently hardening execute.rs/recovery.rs (atomic created-file publish, history paths out of the HEAD-restore set, symlinked-vault path handling).

[2026-10-26T16:14:28Z · bob-cli-cc.5] PROPOSED FOLLOW-UP: docs-check fails on BOB_TEST_FIXTURE_PDF in source_store.rs:185 — undocumented production environment name; reproduces on clean HEAD (phase 3, 009060f9). Document it in docs/reference/configuration.md or add a reasoned exact exception in docs/_meta/environment_ignore.yml.

[2026-10-26T16:19:14Z · bob-cli-cc.5] Overwrite -f overwrite stages source.md/code.json in scratch, installs them under bob_sync.lock, and repoints live source_markdown; frozen notes keep the old pointer; failpoint rollback removes the new store and restores the pointer; non-Markdown overwrite clears the pointer; ignored code.json warns, commits source.md, and omits the catalog. bob ref doctor prints a read-only ref sources row (ok counts / warn dangling, digest mismatch, missing catalog, orphan, ignored catalog), walking ref_history so frozen pointers are not orphans. Verified: just check; lib tests inspect/repoint/rollback/retain; CLI markdown reuse, PDF clear, ignored catalog, doctor_ref_sources_*. No leftover --epic-symbol entries. docs-check BOB_TEST_FIXTURE_PDF lint reproduces on clean HEAD and is recorded as PROPOSED FOLLOW-UP.

## Dependencies

- **Blocks:** [bob-cli-cc.10](bob-cli-cc.10.md) ◐ · ⧖ 2026-10-26
- **Depends on:** [bob-cli-cc.3](bob-cli-cc.3.md) ✓ · ⧖ 2026-10-26

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-cc.5](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-cc.5/README.md) | [bob-cli-cc.5](bob-cli-cc.5.md) | 0 |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-c9.5.1.land--1][1] | Verify source-store overwrite integration ownership and coordination note | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-c9.5.1.land.md

<!-- sase:referenced-by:end -->
