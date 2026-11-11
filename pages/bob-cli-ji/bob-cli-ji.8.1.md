# Bead: bob-cli-ji.8.1 — Account-aware note fold, honest held rows, and accurate note provenance

[Bead Pages](../README.md) / [bob-cli-ji.8](bob-cli-ji.8.md) / bob-cli-ji.8.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.bob-cli-ji.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-ji.land.md) · **Assignee:** `bob-cli-ji.8.1` · **Size:** medium
**Created:** 2026-11-10 22:31:45 EST · **Closed:** 2026-11-10 23:03:45 EST
**Plan:** [202611/finish\_private\_gcal\_event\_notes.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/finish_private_gcal_event_notes.md)

## Description

engine: fold private notes per account so a foreign note never hides this account's note, report held rows as held (not updated, no duplicate gcal.row per run), make the note `fields` summary list only fields the note actually won, strip aliased title routes when a note route wins, and add the missing no-hold test.

## Notes

[2026-11-11T04:03:45Z · bob-cli-ji.8.1] Engine phase complete. Notes fold per (account, calendar, event/series); a newer foreign note no longer hides this account, and a clear under A clears only A. Held rows report action=held with the journaled buffer, skip vault writes and extra gcal.row, print no ~, and stay status=unchanged; a deliberate clear is never held. Provenance fields drop root unless the chosen root is note/series_note and drop bullets when description is off or the event is not a task. A winning note route strips an aliased title token (Breakfast @fam -> Breakfast). Verified: cargo test --test gcal_notes (21 passed, including two-account fold/clear, two-run hold, fields omit, aliased title, no-hold when malformed=0); cargo test --lib notes_fold and note_route; just check (fmt, clippy, workspace tests). No --epic-symbol leftovers. No fixtures changed.

## Dependencies

- **Blocks:** [bob-cli-ji.8.2](bob-cli-ji.8.2.md) ✓ · ⧖ 2026-11-10

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-ji.8.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-ji.8.1/README.md) | [bob-cli-ji.8.1](bob-cli-ji.8.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`54e650d`](https://github.com/bobs-org/bob-cli/commit/54e650d17699f9ff2362a40f20ae8e80e8b59585) | fix(gcal): fold private notes per account and report held rows honestly | [bob-cli-ji.8.1](bob-cli-ji.8.1.md) | 2026-11-10 23:04:40 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-ji.8.1][1] | Need notes and remaining work if any earlier agent left this open | 3 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-ji.8.1/README.md

<!-- sase:referenced-by:end -->
