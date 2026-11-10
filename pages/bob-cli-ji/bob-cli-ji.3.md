# Bead: bob-cli-ji.3 — Note provenance in gcal.row and fail-safe reads

[Bead Pages](../README.md) / [bob-cli-ji](README.md) / bob-cli-ji.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.3z.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.3z.linker.w0.md) · **Assignee:** `bob-cli-ji.3` · **Size:** small
**Created:** 2026-11-10 05:59:46 EST · **Closed:** 2026-11-10 07:14:00 EST
**Plan:** [202611/private\_gcal\_event\_notes.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/private_gcal_event_notes.md)

## Description

hardening: journal which fields a private note contributed to each `gcal.row`, hold those fields with a warning when a note can no longer be read because journal lines are malformed, and word `kept_description` for the input that actually changed.

## Notes

[2026-11-10T12:13:52Z · bob-cli-ji.3] PROPOSED FOLLOW-UP: just docs-check fails on 4 unrelated reference pages over the 6000-word budget (json-outputs, mac-capture capture-previews/keyboard/protocol); untouched by this phase

[2026-11-10T12:14:00Z · bob-cli-ji.3] Provenance (note hash+fields on gcal.row), fail-safe hold with held warning + doctor hint, deliberate-clear exemption, kept_description note-vs-Google wording, Reliability docs in gcal-notes.md and gcal.md; verified: cargo fmt --check clean, cargo test gcal_notes 17/17, gcal_sync+gcal_list 69/69, lib gcal 232/232; just docs-check fails only on 4 pre-existing unrelated reference budget errors (recorded as follow-up)

## Dependencies

- **Depends on:** [bob-cli-ji.1](bob-cli-ji.1.md) ✓ · ⧖ 2026-11-10
- **Blocks:** [bob-cli-ji.6](bob-cli-ji.6.md) ✓ · ⧖ 2026-11-10

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-ji.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-ji.3/README.md) | [bob-cli-ji.3](bob-cli-ji.3.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`7ff24c8`](https://github.com/bobs-org/bob-cli/commit/7ff24c8241b1fefbed57906f5486367e3f86e14d) | feat(gcal): record note provenance in gcal.row and fail-safe reads | [bob-cli-ji.3](bob-cli-ji.3.md) | 2026-11-10 07:15:55 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-ji.3][1] | Recovery turn needs bead status to choose keep vs close for final declaration | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-ji.3/README.md

<!-- sase:referenced-by:end -->
