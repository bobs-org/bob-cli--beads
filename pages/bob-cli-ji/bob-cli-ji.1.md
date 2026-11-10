# Bead: bob-cli-ji.1 — Note store and per-field layering engine

[Bead Pages](../README.md) / [bob-cli-ji](README.md) / bob-cli-ji.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.3z.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.3z.linker.w0.md) · **Assignee:** `bob-cli-ji.1` · **Size:** medium
**Created:** 2026-11-10 05:59:46 EST · **Closed:** 2026-11-10 06:47:14 EST
**Plan:** [202611/private\_gcal\_event\_notes.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/private_gcal_event_notes.md)

## Description

engine: add the `gcal.note` journal record and its last-writer-wins fold, parse notes on the plain-text description path, and layer occurrence and series notes over Google's description in `snapshot::fetch_day`. Give the root a note-first source, keep note bullets outside the cap, mark notes in `list` and `sync`, add list JSON identity fields, and test it all with hand-written journal records.

## Notes

[2026-11-10T11:46:59Z · bob-cli-ji.1] PROPOSED FOLLOW-UP: just docs-check fails on clean master with mount bob-mac-capture -> reference/mac-capture collision (source ships index.md vs committed docs/reference/mac-capture/index.md) — same as bob-cli-jf / prior notes on bob-cli-j5.8 and bob-cli-j8.5; contract pytest and bob-docs gen succeeded for gcal-notes

[2026-11-10T11:47:14Z · bob-cli-ji.1] Engine: gcal.note journal (last-writer-wins fold, load_notes/append_note, excluded from newest/malformed), plain-text parse_note with per-side set flags, apply_notes layering, snapshot apply after from_google, RootSourceKind Note/SeriesNote, uncapped note bullets, list/sync summaries and ✎, additive list JSON identity. Verified: cargo fmt, clippy, cargo test --workspace (14 tests/gcal_notes.rs cases), just docs-gen, tools/docs contract pytest. just docs-check fails identically on clean master (mac-capture mount); recorded as PROPOSED FOLLOW-UP.

## Dependencies

- **Blocks:** [bob-cli-ji.2](bob-cli-ji.2.md) ◐ · ⧖ 2026-11-10
- **Blocks:** [bob-cli-ji.3](bob-cli-ji.3.md) ◐ · ⧖ 2026-11-10

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-ji.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-ji.1/README.md) | [bob-cli-ji.1](bob-cli-ji.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`4219d70`](https://github.com/bobs-org/bob-cli/commit/4219d70a75d81299cb9321bf194508abcbb96367) | feat(gcal): layer private event notes over Google descriptions | [bob-cli-ji.1](bob-cli-ji.1.md) | 2026-11-10 06:48:22 EST |
