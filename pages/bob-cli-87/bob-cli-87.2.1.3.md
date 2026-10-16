# Bead: bob-cli-87.2.1.3 — Obsidian syntax and checkbox projection

[Bead Pages](../README.md) / [bob-cli-87.2.1](bob-cli-87.2.1.md) / bob-cli-87.2.1.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-87.2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-87.2.md) · **Assignee:** `bob-cli-87.2.1.3` · **Size:** medium
**Created:** 2026-10-16 07:26:13 EDT · **Closed:** 2026-10-16 09:32:23 EDT
**Plan:** [202610/snapshot\_view\_core.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/snapshot_view_core.md)

## Description

syntax: implement protected-code-aware inline and block projection, resolved links, images, comments, fields, tags, headings, checkboxes, callouts, and query placeholders. Exercise each construct with synthetic golden fixtures.

## Notes

[2026-10-16T13:32:23Z · bob-cli-87.2.1.3] Implemented note_snapshot/obsidian.rs: protected-code-aware inline+block projection (wikilinks with alias/same-note/external resolution, Note › excerpt block labels, images with width hints + missing placeholders, %%/HTML comment stripping, trailing block-ID anchors, collision-safe heading IDs with H1 shift + title candidate, all checkbox statuses via Tasks settings with unknown-symbol warnings, bookkeeping drop vs muted unknown fields/tags, Keep/quote chips, callouts, live-query placeholders, note embeds as PendingEmbed requests). 28 unit tests + syntax-coverage.projected.md golden with residue invariant. just check green: fmt, clippy gate, 2722 lib tests + all suites pass. No epic-symbol leftovers.

## Dependencies

- **Depends on:** [bob-cli-87.2.1.2](bob-cli-87.2.1.2.md) ✓ · ⧖ 2026-10-16
- **Blocks:** [bob-cli-87.2.1.4](bob-cli-87.2.1.4.md) ✓ · ⧖ 2026-10-16

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-87.2.1.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-87.2.1.3/README.md) | [bob-cli-87.2.1.3](bob-cli-87.2.1.3.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`8da6615`](https://github.com/bobs-org/bob-cli/commit/8da66156b8395c93a2d50ab3b415959db6bb1dee) | feat(note-snapshot): implement protected-code-aware obsidian syntax projection | [bob-cli-87.2.1.3](bob-cli-87.2.1.3.md) | 2026-10-16 09:33:56 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-87.2.1.3][1] | check phase notes for prior work remainder | 2 |
| read-by | [agent:bob-cli-87.2.1.land--1][2] | Review the third completed child scope and notes for landing completeness | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-87.2.1.3/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-87.2.1.land.md

<!-- sase:referenced-by:end -->
