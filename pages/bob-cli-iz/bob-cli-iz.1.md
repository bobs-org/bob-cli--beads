# Bead: bob-cli-iz.1 — Refuse to sync into a note Templater has not rendered

[Bead Pages](../README.md) / [bob-cli-iz](README.md) / bob-cli-iz.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.1aa](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.1aa.md) · **Assignee:** `bob-cli-iz.1` · **Size:** small
**Created:** 2026-11-09 07:12:09 EST · **Closed:** 2026-11-09 07:39:35 EST
**Plan:** [202611/gcal\_sync\_race\_force\_and\_skip\_reasons.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/gcal_sync_race_force_and_skip_reasons.md)

## Description

templater_guard: bob-cli. Detect pending Templater tags in the daily note and return a structured `waiting` (note_missing / pomodoros_missing / note_unrendered) instead of writing, including on the locked re-read. See plan section "Phase templater_guard".

## Notes

[2026-11-09T12:39:35Z · bob-cli-iz.1] Added src/native/templater.rs (first_pending_tag; skips fenced/inline code, scans frontmatter) and a typed WaitingReason in gcal/sync.rs (note_missing → note_unrendered → pomodoros_missing, also on the locked re-read). Human/JSON output, status.json reason, list header/VAULT cells 'waiting for Templater', doctor last_sync, docs/gcal.md and sync long_about updated. Verified: just check green, just docs-check green, new unit + integration tests (gcal_sync, gcal_list). The NoteChanged retry is covered by unit-testing the shared guard, since the harness can't simulate a concurrent edit.

## Dependencies

- **Blocks:** [bob-cli-iz.3](bob-cli-iz.3.md) ✓ · ⧖ 2026-11-09

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-iz.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-iz.1/README.md) | [bob-cli-iz.1](bob-cli-iz.1.md) | 2 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`665dbcb`](https://github.com/bobs-org/bob-mac-capture/commit/665dbcbbb82b9accc8d0a0ad23ac4480f2232449) | feat(gcal): refuse to sync into a note Templater has not rendered | [bob-cli-iz.1](bob-cli-iz.1.md) | 2026-11-09 20:22:16 EST |
| bob-mac-capture | `bob-mac-capture@665dbcb` | feat(gcal): refuse to sync into a note Templater has not rendered | [bob-cli-iz.1](bob-cli-iz.1.md) | 2026-11-09 20:22:16 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-iz.1][1] | Need the phase scope and design file | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-iz.1/README.md

<!-- sase:referenced-by:end -->
