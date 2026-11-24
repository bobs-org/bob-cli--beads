# Bead: bob-cli-pw.1 — Structural notes normalizer, dossier source, and recap renderer

[Bead Pages](../README.md) / [bob-cli-pw](README.md) / bob-cli-pw.1

**Status:** ◐ in_progress · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.65.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.65.linker.w0.md) · **Assignee:** `bob-cli-pw.1` · **Size:** medium
**Created:** 2026-11-24 10:38:46 EST
**Plan:** [202611/meeting\_notes\_event\_refs.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/meeting_notes_event_refs.md)

## Description

notes-normalizer: pure Rust module that reads notes text, detects its shape, builds a MeetingNotes model without changing a word, and renders the round-trippable dossier Markdown plus the inert, digest-stamped recap region, with synthetic golden fixtures.

## Dependencies

- **Blocks:** [bob-cli-pw.3](bob-cli-pw.3.md) ◐ · ⧖ 2026-11-24
- **Blocks:** [bob-cli-pw.4](bob-cli-pw.4.md) ◐ · ⧖ 2026-11-24

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-pw.1](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-pw.1.md) | [bob-cli-pw.1](bob-cli-pw.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`dbf405e`](https://github.com/bobs-org/bob-cli/commit/dbf405e397b7081c5c5531590608637346e49dfc) | feat(meetings): add notes normalization and rendering | [bob-cli-pw.1](bob-cli-pw.1.md) | 2026-11-24 11:11:34 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-pl.1--4][1] | Check whether the normalizer phase already records the compile failures | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-pl.1.md

<!-- sase:referenced-by:end -->
