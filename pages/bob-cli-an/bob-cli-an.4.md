# Bead: bob-cli-an.4 — Preserve ignored vault content off host

[Bead Pages](../README.md) / [bob-cli-an](README.md) / bob-cli-an.4

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.12v](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.12v.md) · **Assignee:** `bob-cli-an.4` · **Size:** medium
**Created:** 2026-10-21 12:58:23 EDT · **Closed:** 2026-10-22 06:57:22 EDT
**Plan:** [202610/backlog\_security\_and\_durability.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/backlog_security_and_durability.md)

## Description

vault-content: resolve bob-cli-1g with an inventory, narrow ignore exceptions, durable copies, and a restore check, honoring the migration-material decision.

## Notes

[2026-10-22T10:56:53Z · bob-cli-an.4] Baseline (2026-10-22, athena live ~/bob): 387 ignored paths; excluding lit_review/xlib out-of-band trees, 111 remain. 79 are authored content in this bead scope: 22 _zorg_templates/zot/*.zot, 20 xmind/*.xmind, 23 _meta/migration/reports/*.tsv, _meta/migration/inventory.json (3.0MB), 6 _meta/migration/tools/*.py, puml/3b_ts.puml, gkeep_gdocs_inbox_dump.txt, needs_attn_notes.txt, selected/skipped_sources.txt, lib/docs textbundle info.json+text.markdown, lib/docs/sase_INSTALL. Total ~26MB, largest single file asset_link_graph.tsv 10.5MB (under 50/95MB gates). Apollo has 26 ignored (plugin builds, sdd, .sase, .bob/gkeep/migrate-tasks only; none of the 79). Mac has 388 ignored; all 79 overlapping authored files hash-identical to athena (sha256 match), so no divergent host variants. Strict secret scan of _meta/migration (api-key/password/private-key patterns) clean; __pycache__ is regenerable junk and stays excluded.

[2026-10-22T10:57:03Z · bob-cli-an.4] Fix (preserve decision honored): appended narrow re-includes to live ~/bob/.gitignore (!*.zot/xmind/puml/tsv/markdown/txt plus path-scoped _meta/migration inventory/reports/tools, lib/docs textbundle json+markdown, sase_INSTALL). .py/.json kept path-scoped so caches, plugin builds, sdd, .bob stay ignored. Background bob-vault-sync committed 4b62d0ac vault(athena): 80 files (.gitignore + 79 candidates, exact match to inventory, no junk) and merged/pushed; origin/master tree now holds all 80 blobs. Remaining exclusions justified: lit_review/xlib (out-of-band), plugin builds incl block-id-prompt (bob-plugins source), pyc/cache, editor/OS state, sdd machine-local, two over-limit old_lib PDFs (GitHub 100MB cap; athena old_lib backup copy retained), apollo-only migrate-tasks jsons (out of scope, see follow-up).

[2026-10-22T10:57:07Z · bob-cli-an.4] Validation: git check-ignore exit codes on live repo — 14/14 candidates trackable (exit 1), 10/10 negative cases still ignored (exit 0: pycache, both plugin builds, lit_review, xlib probe, over-limit PDF, sdd, .DS_Store, workspace.json, .bak). Blob-level restore check: all 79 live hash-objects equal origin/master blobs (0 mismatches); git-archive restore of all 80 paths from origin/master succeeds and .gitignore bytes match. Raw-byte diff on 22 CRLF TSVs is only git text=auto eol=lf normalization (content identical). Docs: new Authored content coverage section in docs/vault-git-sync.md; just docs-check 447 passed; just check exit 0.

[2026-10-22T10:57:14Z · bob-cli-an.4] PROPOSED FOLLOW-UP: decide tracking for apollo-only .bob/gkeep/migrate-tasks/*.json (4 files, ignored on apollo, outside bob-cli-1g extension gap; imports/ allowlist covers only .bob/gkeep/imports/*.json) — detail: if these are durable shared history like imports receipts, add a narrow !/.bob/gkeep/migrate-tasks/*.json re-include; if machine-local task state, record the exclusion justification.

[2026-10-22T10:57:22Z · bob-cli-an.4] Verified: 79 authored files inventoried identical on athena/mac with clean secret scan; narrow .gitignore re-includes added; vault(athena) commit 4b62d0ac pushed all 80 paths and origin/master holds all 80 blobs; check-ignore 14 trackable/10 still-ignored; blob-level restore 79/79 match (CRLF TSV diff is only eol=lf normalization); docs section added with just docs-check 447 passed and just check exit 0

## Dependencies

- **Depends on:** [bob-cli-an.2](bob-cli-an.2.md) ✓ · ⧖ 2026-10-21

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-an.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-an.4/README.md) | [bob-cli-an.4](bob-cli-an.4.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`019ffb5`](https://github.com/bobs-org/bob-cli/commit/019ffb5ac4ee1b122fc3a576509acf774a80cf31) | docs(vault-sync): document authored content coverage for vault git backup | [bob-cli-an.4](bob-cli-an.4.md) | 2026-10-22 06:58:44 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-an.4][1] | Need the phase scope and design file | 3 |
| read-by | [agent:bob-cli-an.6.6.6.5.6.land--2][2] | Review every ancestor phase note for unresolved follow-ups and completion | 1 |
| read-by | [agent:bob-cli-an.land][3] | Need the child scope and notes | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-an.4/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-an.6.6.6.5.6.land.md
[3]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-an.land.md

<!-- sase:referenced-by:end -->
