# Bead: bob-cli-c9.3.1.5 — Finish collection rereads and the public contract

[Bead Pages](../README.md) / [bob-cli-c9.3.1](bob-cli-c9.3.1.md) / bob-cli-c9.3.1.5

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-c9.3](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-c9.3.md) · **Assignee:** `bob-cli-c9.3.1.5` · **Size:** medium
**Created:** 2026-10-25 15:22:59 EDT · **Closed:** 2026-10-25 19:14:59 EDT
**Plan:** [202610/ref\_create\_reread.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/ref_create_reread.md)

## Description

collections_acceptance: enable exact URL-set collection rereads, complete help and documentation, and verify the phase-wide acceptance matrix.

## Notes

[2026-10-25T23:14:59Z · bob-cli-c9.3.1.5] Exact URL-set collection rereads work: reversed-order sets select the family and file <root>__vN with newest-reading parent/type defaults, id==stem, preserved argument order, earlier: lineage, versioned reading task, and no changes to earlier notes/PDFs. Partial overlaps (subset/superset, incl. one URL vs collection) refuse under every force mode before fetch/adapter with hint -f recaptures only the exact URL set of <stem>; unrelated same-set families ask for -N and member selection proceeds; queued-only exact sets replace under both modes and refuse without force; -o/non-member -N refuse exit 2; overwrite (adopted and explicit) names the pending reread exit 2; -f -L narrates the new reading vs attach; failed parts write nothing and skip compose. Help Recapture paragraph and docs/highlights-create.md Dedupe/Listen plus new Recapture section and docs/ref.md Identity updated; docs-gen clean, docs-check green. Verified: cargo fmt --check, clippy gate, cargo test --no-fail-fast green (lib 3488 + CLI 2112 incl. 8 new collection reread tests, 0 failures); second scan stable; doctor shows no duplicate_identity.

## Dependencies

- **Depends on:** [bob-cli-c9.3.1.4](bob-cli-c9.3.1.4.md) ✓ · ⧖ 2026-10-25

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-c9.3.1.5](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-c9.3.1.5/README.md) | [bob-cli-c9.3.1.5](bob-cli-c9.3.1.5.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`9923063`](https://github.com/bobs-org/bob-cli/commit/9923063e3288b15380c6da99f3d877911d6b7944) | feat(highlights): collection rereads use shared recapture preflight | [bob-cli-c9.3.1.5](bob-cli-c9.3.1.5.md) | 2026-10-25 19:16:13 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-c9.3.1.5][1] | Need the phase scope and design file | 1 |
| read-by | [agent:bob-cli-c9.3.1.6.land--1][2] | Need descendant status, notes, and remaining follow-ups before closing bob-cli-c9.3.1 | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-c9.3.1.5/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-c9.3.1.6.land.md

<!-- sase:referenced-by:end -->
