# Bead: bob-cli-ho.1 — Checklist stages in the bob-cli evaluator, CLI, and contract

[Bead Pages](../README.md) / [bob-cli-ho](README.md) / bob-cli-ho.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.193](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.193.md) · **Assignee:** `bob-cli-ho.1` · **Size:** medium
**Created:** 2026-11-05 18:44:50 EST · **Closed:** 2026-11-05 19:37:50 EST
**Plan:** [202611/gtd\_checklist\_stages.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/gtd_checklist_stages.md)

## Description

walk_order: parse and validate freshness.pre_stages/post_stages, resolve each PRE/POST row's stage, sort PRE/POST by stage rank then path and line, add three lints, schema-16 JSON, the human stage detail, the shared CS/SC fixture, and the freshness contract and guide docs.

## Notes

[2026-11-06T00:37:35Z · bob-cli-ho.1] PROPOSED FOLLOW-UP: lib tests every_table_entry_matches_the_tree (completion kinds) and public_leaves_are_entries_or_excluded (catalog) fail identically on the clean base tree (verified via stash); docs-check also fails on base with 4 undocumented BOB_GMAIL_* env errors. None is caused by the stages phase.

[2026-11-06T00:37:50Z · bob-cli-ho.1] walk_order done in accf2823: pre/post stage config with per-key invalid diagnostics, stage resolution + PRE/POST stage-first ordering with rank/total, 3 lints, schema-16 JSON + staged human output, shared CS/SC fixture (Rust source of truth, 26 vectors incl. CL1-CL12 untouched), end-to-end CLI test, contract/guide/reference docs. Verified: 161 lib freshness tests + 50 CLI freshness tests pass, fmt + full clippy gate clean, docs-check back to its 4 pre-existing base errors. 2 lib failures (completion kinds, catalog) reproduce identically on base and are recorded as PROPOSED FOLLOW-UP.

## Dependencies

- **Blocks:** [bob-cli-ho.3](bob-cli-ho.3.md) ✓ · ⧖ 2026-11-05
- **Blocks:** [bob-cli-ho.6](bob-cli-ho.6.md) ✓ · ⧖ 2026-11-05

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-ho.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-ho.1/README.md) | [bob-cli-ho.1](bob-cli-ho.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`8eecf0c`](https://github.com/bobs-org/bob-cli/commit/8eecf0c4ba01712cb8a7807439c622c484f17630) | feat(freshness): order PRE and POST review stages | [bob-cli-ho.1](bob-cli-ho.1.md) | 2026-11-05 19:39:18 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-ho.1][1] | Need the phase scope and design file | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-ho.1/README.md

<!-- sase:referenced-by:end -->
