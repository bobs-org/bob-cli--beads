# Bead: bob-cli-pw.3 — Meeting dossier print profile

[Bead Pages](../README.md) / [bob-cli-pw](README.md) / bob-cli-pw.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.65.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.65.linker.w0.md) · **Assignee:** `bob-cli-pw.3` · **Size:** medium
**Created:** 2026-11-24 10:38:46 EST · **Closed:** 2026-11-24 14:44:10 EST
**Plan:** [202611/meeting\_notes\_event\_refs.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/meeting_notes_event_refs.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| related | file:explicit:43a892cc8bc0c50b3d85597a | attached via sase artifact create --bead |
| related | file:explicit:e2f35a8b6d3bd8b7f9d9a737 | attached via sase artifact create --bead |
| related | file:explicit:f2d39d019595790f65456db8 | attached via sase artifact create --bead |

_Plus 1 automatic references — see [Referenced By](#referenced-by)._

<!-- sase:links:end -->

## Description

dossier-print: a meeting print profile beside the note-snapshot profile (shared fonts, glyph coverage, warnings) that renders the dossier Markdown into a one-to-two-page PDF with a title card, TL;DR box, next-steps table, sections, provenance, and an optional transcript appendix.

## Notes

[2026-11-24T19:43:49Z · bob-cli-pw.3] PROPOSED FOLLOW-UP: just lint fails identically on the clean base tree with 9 clippy errors in src/native/props/{cli,contract/read}.rs (collapsible_if, for_kv_map, manual_pattern_char_comparison, map_identity); already recorded on bob-cli-pw.4, bob-cli-px.1, and bob-cli-px.2.

[2026-11-24T19:44:10Z · bob-cli-pw.3] Meeting print profile lands beside the snapshot engine (render_profile_pdf). Real xelatex: Wispr fixture is 1 page with title card, TL;DR box, hoisted next-steps table, sections, provenance; transcript fixture is 2 pages with the appendix on page 2. PDF Info Title/Subject/Keywords asserted. Word-order and no-TOC/no-overfull checks passed. Visual PNGs attached as file:explicit:e2f35a8b6d3bd8b7f9d9a737, file:explicit:43a892cc8bc0c50b3d85597a, file:explicit:f2d39d019595790f65456db8. Tests: meetings::profile 4/4, render_tex header_packages, snapshot fake-commands. just lint fails on clean-tree props clippy (follow-up).

## Dependencies

- **Depends on:** [bob-cli-pw.1](bob-cli-pw.1.md) ✓ · ⧖ 2026-11-24
- **Blocks:** [bob-cli-pw.5](bob-cli-pw.5.md) ◐ · ⧖ 2026-11-24

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-pw.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-pw.3/README.md) | [bob-cli-pw.3](bob-cli-pw.3.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`2b3817f`](https://github.com/bobs-org/bob-cli/commit/2b3817fee2c1cb43f02600ece3f52ba9147c6eaa) | feat(meetings): add a dossier print profile beside note snapshots | [bob-cli-pw.3](bob-cli-pw.3.md) | 2026-11-24 15:02:25 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-pw.3][1] | Need the phase scope, design file, notes, and DECISIONS | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-pw.3/README.md

<!-- sase:referenced-by:end -->
