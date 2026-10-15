# Bead: bob-cli-7x.2 — Vault link rewrite engine for a renamed bundle

[Bead Pages](../README.md) / [bob-cli-7x](README.md) / bob-cli-7x.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.1k.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.1k.linker.w0.md) · **Assignee:** `bob-cli-7x.2` · **Size:** medium
**Created:** 2026-10-15 15:25:59 EDT · **Closed:** 2026-10-15 15:55:13 EDT
**Plan:** [202610/bob\_ref\_rename.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/bob_ref_rename.md)

## Description

rename-links: in bob-cli, a pure module that, given old→new vault paths for a reference bundle, finds and rewrites every inbound wikilink, embed, and Markdown link across vault .md files (done/ and daily notes included), honoring the bare-stem uniqueness rule and skipping code, and reports ^h- fragments and [h::] follow-ups that cite the note.

## Notes

[2026-10-15T19:55:13Z · bob-cli-7x.2--2] Implemented deterministic vault link rewrite planning for wikilinks, embeds, Markdown links, unique bare-note links, and highlight findings; skips configured excluded paths and code. Fixed rustfmt, reran just check successfully (2,620 unit tests, 1,615 CLI tests, plus remaining suites); epic-symbol check found no leftovers.

## Dependencies

- **Blocks:** [bob-cli-7x.3](bob-cli-7x.3.md) ✓ · ⧖ 2026-10-15

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-7x.2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-7x.2.md) | [bob-cli-7x.2](bob-cli-7x.2.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`66c0dcd`](https://github.com/bobs-org/bob-cli/commit/66c0dcdc9e85ba01f808da6edb7b1508f2e9ffd6) | feat(ref-rename): plan inbound vault link rewrites | [bob-cli-7x.2](bob-cli-7x.2.md) | 2026-10-15 15:56:09 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-7x.2--2][1] | Need the phase scope and design file | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-7x.2.md

<!-- sase:referenced-by:end -->
