# Bead: bob-cli-87.13.1 — Projection fixes for badge rows, block-ref labels, file links, and kickers

[Bead Pages](../README.md) / [bob-cli-87.13](bob-cli-87.13.md) / bob-cli-87.13.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-87.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-87.land.md) · **Assignee:** `bob-cli-87.13.1` · **Size:** medium
**Created:** 2026-10-17 10:11:19 EDT · **Closed:** 2026-10-17 10:51:12 EDT
**Plan:** [202610/note\_snapshot\_landing\_repairs.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/note_snapshot_landing_repairs.md)

## Description

projection-fixes: drop generated status-chip rows from real notes, label same-note block refs with their task text, keep intraword underscores in excerpts, resolve links to existing vault files outside the note set, and never print the generic [[area]] parent in the kicker.

## Notes

[2026-10-17T14:51:12Z · bob-cli-87.13.1--1] Verified projection-fixes: generated Markdown badge rows with percent-encoded nested anchors are dropped (bob-generated-badge-row golden; no ⚪/🔵/🔴/🟢 residue and no dead #Tasks local links); same-note BLOCKS/DEPENDS ON [[#^id]] labels use block excerpts including omitted-closed and -C restored cases, with residue invariant allowing only missing ^gone (bob-same-note-block-refs golden); excerpt cleaner keeps sase_blog/snake_case_name and unwraps _emph_; content links resolve unique excluded files (lib/chat sidecar, member-over-lib, pdf/png/refs.base) while .hidden and missing stay unresolved; generic [[area]]/[[AREA]] parent kicker is bare AREA. just check passed (fmt, clippy, lib+CLI tests). No leftover --epic-symbol entries.

## Dependencies

- **Blocks:** [bob-cli-87.13.4](bob-cli-87.13.4.md) ✓ · ⧖ 2026-10-17

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-87.13.1](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-87.13.1.md) | [bob-cli-87.13.1](bob-cli-87.13.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`9ef336c`](https://github.com/bobs-org/bob-cli/commit/9ef336cccbb9e11a0809ef9669406818df18acfc) | fix(note-snapshot): drop badge rows and resolve vault file links | [bob-cli-87.13.1](bob-cli-87.13.1.md) | 2026-10-17 10:52:16 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-87.13.1--1][1] | Need remaining notes and recorded work from earlier agent | 3 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-87.13.1.md

<!-- sase:referenced-by:end -->
