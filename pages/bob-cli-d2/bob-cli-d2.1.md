# Bead: bob-cli-d2.1 — Newborn reference notes keep their birth source\_markdown pointer

[Bead Pages](../README.md) / [bob-cli-d2](README.md) / bob-cli-d2.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.14o](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.14o.md) · **Assignee:** `bob-cli-d2.1` · **Size:** small
**Created:** 2026-10-27 07:42:23 EDT · **Closed:** 2026-10-27 08:03:50 EDT
**Plan:** [202610/research\_ref\_saved\_markdown.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/research_ref_saved_markdown.md)

## Description

pointer-fix: make both PDF-sync executors carry the planned birth-only source_markdown pointer into the note they write (today they rebuild metadata and drop it), with regression tests for inline create intake and queued scan drains.

## Notes

[2026-10-27T12:03:50Z · bob-cli-d2.1] pointer-fix done: added carry_birth_only_metadata helper in sync.rs used by both PDF-sync executors (behavior identical to the inline copies already on master); extended -k + scan -i drain test to assert the filed note carries the exact birth pointer once with saved bytes present. Verified: focused suites green (scan_intake, store_gaps, ingest, lib highlights_ref 955 tests), just check and just docs-check pass, throwaway-vault create with dev binary files ref/chat/report.md with the reported source_markdown pointer and ref code reports available. No epic-symbol leftovers. Earlier master commit 017b6927 already carried the executor copies, docs, and most regression tests; this phase consolidated and closed the remaining gaps.

## Dependencies

- **Blocks:** [bob-cli-d2.3](bob-cli-d2.3.md) ✓ · ⧖ 2026-10-27

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-d2.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-d2.1/README.md) | [bob-cli-d2.1](bob-cli-d2.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`3a13ec6`](https://github.com/bobs-org/bob-cli/commit/3a13ec6f53ec78382dc225207bf822da5567df3a) | fix(ref): keep birth source\_markdown pointer on newborn notes | [bob-cli-d2.1](bob-cli-d2.1.md) | 2026-10-27 08:04:53 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-d2.1][1] | Need the phase scope and design file | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-d2.1/README.md

<!-- sase:referenced-by:end -->
