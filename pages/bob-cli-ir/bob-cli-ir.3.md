# Bead: bob-cli-ir.3 — bob records list, show, check, and new

[Bead Pages](../README.md) / [bob-cli-ir](README.md) / bob-cli-ir.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.1a0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.1a0.md) · **Assignee:** `bob-cli-ir.3` · **Size:** medium
**Created:** 2026-11-08 11:06:11 EST · **Closed:** 2026-11-08 19:02:58 EST
**Plan:** [202611/record\_notes.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/record_notes.md)

## Description

records-cli: add the bob records command group (list, show, check, new) with polished output, JSON, shell completion, catalog entries, and generated CLI docs.

## Notes

[2026-11-09T00:01:58Z · bob-cli-ir.3] PROPOSED FOLLOW-UP: Trim the three existing Mac Capture reference pages to the 6000-word budget — just docs-check still reports capture-panel.md 6088, keyboard.md 6060, and protocol.md 6014 words; all three files are unchanged from this phase base. Existing tracking: bob-cli-iu note #1/#2 and follow-up #3 record the same overage and cause.

[2026-11-09T00:02:58Z · bob-cli-ir.3] Implemented records list/show/check/new with JSON, completion/catalog wiring, generated CLI docs, and the authorized Capture glossary update. Verified cargo check; records CLI list/show/check/new integration tests, alphabetical help tests, catalog coverage, and just docs-gen pass. just docs-check still reports three unchanged Mac Capture word-budget overages; recorded as PROPOSED FOLLOW-UP citing bob-cli-iu. epic-symbols is empty.

## Dependencies

- **Depends on:** [bob-cli-ir.1](bob-cli-ir.1.md) ✓ · ⧖ 2026-11-08
- **Depends on:** [bob-cli-ir.2](bob-cli-ir.2.md) ✓ · ⧖ 2026-11-08
- **Blocks:** [bob-cli-ir.4](bob-cli-ir.4.md) ✓ · ⧖ 2026-11-08

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-ir.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-ir.3/README.md) | [bob-cli-ir.3](bob-cli-ir.3.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`3e68a53`](https://github.com/bobs-org/bob-cli/commit/3e68a53acd5c75feaf4f26fb6dab206f2a1a84aa) | feat(records): add records CLI and docs | [bob-cli-ir.3](bob-cli-ir.3.md) | 2026-11-08 19:04:25 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-ir.3][1] | Final scope, notes, and close readiness check | 3 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-ir.3/README.md

<!-- sase:referenced-by:end -->
