# Bead: bob-cli-c9.3.1.3 — Derive lineage and preserve reading identity during intake

[Bead Pages](../README.md) / [bob-cli-c9.3.1](bob-cli-c9.3.1.md) / bob-cli-c9.3.1.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-c9.3](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-c9.3.md) · **Assignee:** `bob-cli-c9.3.1.3` · **Size:** medium
**Created:** 2026-10-25 15:22:58 EDT · **Closed:** 2026-10-25 17:51:53 EDT
**Plan:** [202610/ref\_create\_reread.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/ref_create_reread.md)

## Description

reading_birth: derive earlier at birth, preserve reading task suffixes and aliases, and recheck reread occupancy under the intake locks for inline and queued filing.

## Notes

[2026-10-25T21:51:43Z · bob-cli-c9.3.1.3] PROPOSED FOLLOW-UP: full-scan raw intake moves lack the locked reread recheck — plan_xlib_intake/execute_xlib_intake_counting check destination existence only, so a fabricated id-only or other-type occupant would not stop a full `bob ref scan` move the way IntakeSession::ingest now refuses; consider sharing recheck_reread_occupancy with the full-scan move path

[2026-10-25T21:51:53Z · bob-cli-c9.3.1.3] reading_birth done: birth derives earlier: lineage (URL-set/source_note/title identity, chain-copy through dangling gaps) in plan_pdf_sync_v2, renders block-style earlier: outside projection/hash, executes with same lineage (fixed executor metadata rebuild), task IDs ref-<root>-vN with version-preserving truncation and -2-after-version collisions, Title (vN) aliases, locked intake occupancy recheck for __vN stems with queued-source preservation. Verified: 8 birth + 2 line unit tests, 5 CLI drain tests (queued reread, fabricated other-type/id-only collisions + recovery, ordinary version-looking birth, long-stem fitting, full scan, second-scan byte stability), full gate green (cargo fmt, repo clippy gate, cargo test: lib 3488 + CLI 2091, 0 failures). Follow-up noted for full-scan raw-move path.

## Dependencies

- **Depends on:** [bob-cli-c9.3.1.2](bob-cli-c9.3.1.2.md) ✓ · ⧖ 2026-10-25
- **Blocks:** [bob-cli-c9.3.1.4](bob-cli-c9.3.1.4.md) ✓ · ⧖ 2026-10-25

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-c9.3.1.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-c9.3.1.3/README.md) | [bob-cli-c9.3.1.3](bob-cli-c9.3.1.3.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`291efa6`](https://github.com/bobs-org/bob-cli/commit/291efa6b374695cace353fab593504d5c0cc6600) | feat(highlights): derive birth earlier lineage and reading-aware ref task IDs | [bob-cli-c9.3.1.3](bob-cli-c9.3.1.3.md) | 2026-10-25 17:53:00 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-c9.3.1.3][1] | Need the phase scope and design file | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-c9.3.1.3/README.md

<!-- sase:referenced-by:end -->
