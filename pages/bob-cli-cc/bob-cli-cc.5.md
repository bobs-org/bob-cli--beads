# Bead: bob-cli-cc.5 — Overwrite repointing and the doctor sources check

[Bead Pages](../README.md) / [bob-cli-cc](README.md) / bob-cli-cc.5

**Status:** ◐ in_progress · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.research.5b.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.research.5b.linker.w0.md) · **Assignee:** `bob-cli-cc.5` · **Size:** medium
**Created:** 2026-10-26 09:00:55 EDT
**Plan:** [202610/ref\_code\_block\_copy.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/ref_code_block_copy.md)

## Description

lifecycle: make -f overwrite stage, install, repoint, and roll back the store inside its transaction, and add a bob ref doctor ref-sources row for dangling pointers, digest mismatches, orphans, and an ignored catalog.

## Notes

[2026-10-26T15:09:29Z · bob-cli-c9.5.1.land] COORDINATION (from bob-cli-c9.5.1.land): annotated overwrite landed on master (ca6065af, 8a1679e5). Annotated overwrites run through the same prepare/execute transaction but also rename the old PDF to ref_history/<type>/<stem>__<date>__annotated.pdf and assets to <archive>.assets/, write a frozen note whose frontmatter is an allowlist built in overwrite.rs render_frozen_note (title/source_url/created/parent/replaced/status_when_replaced/highlights_count/annotated_pdf/annotated_pdf_sha256 + earlier lineage), and record v2 move-aware intents in overwrite/recovery.rs. When adding source-store paths to touched/created and repointing source_markdown, cover the annotated path too and decide explicitly whether the frozen note keeps the old source_markdown pointer. A bob-cli-c9.5.1 landing tale is concurrently hardening execute.rs/recovery.rs (atomic created-file publish, history paths out of the HEAD-restore set, symlinked-vault path handling).

## Dependencies

- **Blocks:** [bob-cli-cc.10](bob-cli-cc.10.md) ◐ · ⧖ 2026-10-26
- **Depends on:** [bob-cli-cc.3](bob-cli-cc.3.md) ✓ · ⧖ 2026-10-26

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-cc.5](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-cc.5/README.md) | [bob-cli-cc.5](bob-cli-cc.5.md) | 0 |
