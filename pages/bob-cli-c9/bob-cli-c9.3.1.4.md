# Bead: bob-cli-c9.3.1.4 — Enable rereads for single files, URLs, and note snapshots

[Bead Pages](../README.md) / [bob-cli-c9.3.1](bob-cli-c9.3.1.md) / bob-cli-c9.3.1.4

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-c9.3](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-c9.3.md) · **Assignee:** `bob-cli-c9.3.1.4` · **Size:** medium
**Created:** 2026-10-25 15:22:58 EDT · **Closed:** 2026-10-25 18:44:02 EDT
**Plan:** [202610/ref\_create\_reread.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/ref_create_reread.md)

## Description

single_sources: wire the shared reread plan into every single-source route with family defaults, flag guards, audio behavior, dry runs, and zero changes to earlier readings.

## Notes

[2026-10-25T22:44:02Z · bob-cli-c9.3.1.4] Single-source rereads enabled: shared preflight (recapture.rs) resolves URL/stem families before -P/fetch/adapter with -f remedy and overwrite interim naming the next stem; Markdown, local PDF, PDF URL, arXiv, article/-H, and same-day vault snapshots capture <root>__vN with family parent/type defaults, -N/-o guards, library-PDF refusal with source hint, -L attach preserved (narrates new reading under reread force with earlier-episode hint), stamped id, reread: report lines, and intact earlier readings. Verified: full CLI suite 2104 passed, lib 3488 passed, clippy gate clean, fmt clean, docs-gen + docs-check passed, epic-symbols clean.

## Dependencies

- **Depends on:** [bob-cli-c9.3.1.3](bob-cli-c9.3.1.3.md) ✓ · ⧖ 2026-10-25
- **Blocks:** [bob-cli-c9.3.1.5](bob-cli-c9.3.1.5.md) ◐ · ⧖ 2026-10-25

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-c9.3.1.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-c9.3.1.4/README.md) | [bob-cli-c9.3.1.4](bob-cli-c9.3.1.4.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`499294b`](https://github.com/bobs-org/bob-cli/commit/499294b3fa35a2a01a4b4173ed8bc9fea9764ae9) | feat(ref)!: enable rereads for single files, URLs, and note snapshots | [bob-cli-c9.3.1.4](bob-cli-c9.3.1.4.md) | 2026-10-25 18:45:24 EDT |
