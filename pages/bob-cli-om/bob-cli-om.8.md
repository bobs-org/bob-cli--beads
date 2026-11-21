# Bead: bob-cli-om.8 — bob capture-complete --links-only

[Bead Pages](../README.md) / [bob-cli-om](README.md) / bob-cli-om.8

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.5o.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.5o.linker.w0.md) · **Assignee:** `bob-cli-om.8` · **Size:** small
**Created:** 2026-11-21 10:32:18 EST · **Closed:** 2026-11-21 12:20:05 EST
**Plan:** [202611/prose\_wikilink\_completion.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/prose_wikilink_completion.md)

## Description

cli-links-only: add -L/--links-only and -S/--source-note to bob capture-complete. They complete only wikilink fields in plain prose and never apply capture grammar. Includes help, docs-gen, and tests.

## Notes

[2026-11-21T17:19:49Z · bob-cli-om.8] PROPOSED FOLLOW-UP: just docs-check lint fails on clean base too — docs/develop/plugins/plugin-apis.md over 8000-word budget (8165, tracked by bob-cli-ob) and docs/reference/vault-format.md over 6000-word budget (6016, tracked by bob-cli-oc); verified identical failure with changes stashed

[2026-11-21T17:20:05Z · bob-cli-om.8] Added -L/--links-only and -S/--source-note to bob capture-complete: plain-prose wikilink-only completion, same grammar/schema_version 1. Verified: 5 new CLI tests pass, full workspace suite green (exit 0), just lint green, docs-gen regenerated golden reference; docs-check budget failure is pre-existing on clean base (tracked by bob-cli-ob/bob-cli-oc)

## Dependencies

- **Depends on:** [bob-cli-om.1](bob-cli-om.1.md) ✓ · ⧖ 2026-11-21
- **Blocks:** [bob-cli-om.9](bob-cli-om.9.md) ✓ · ⧖ 2026-11-21

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-om.8](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-om.8/README.md) | [bob-cli-om.8](bob-cli-om.8.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`270b5b2`](https://github.com/bobs-org/bob-cli/commit/270b5b23fb38d15663c68efd85f3bde4161d4bd6) | feat(capture-complete): add -L/--links-only and -S/--source-note | [bob-cli-om.8](bob-cli-om.8.md) | 2026-11-21 12:21:19 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-om.7][1] | see sibling phase status and notes | 1 |
| read-by | [agent:bob-cli-om.8][2] | Need the phase scope and design file | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-om.7/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-om.8/README.md

<!-- sase:referenced-by:end -->
