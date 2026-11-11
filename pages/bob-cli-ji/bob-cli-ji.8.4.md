# Bead: bob-cli-ji.8.4 — Finish -e, -A, the doctor notes check, and the fragile-description hint

[Bead Pages](../README.md) / [bob-cli-ji.8](bob-cli-ji.8.md) / bob-cli-ji.8.4

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.bob-cli-ji.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-ji.land.md) · **Assignee:** `bob-cli-ji.8.4` · **Size:** medium
**Created:** 2026-11-10 22:31:45 EST · **Closed:** 2026-11-11 01:22:50 EST
**Plan:** [202611/finish\_private\_gcal\_event\_notes.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/finish_private_gcal_event_notes.md)

## Description

extras: bring `-e` (TTY, vi fallback, git scissors, Edit again loop, empty clears), `-A` (bare buffers, existing-note refusal, success wording), the doctor `notes` check (shared fold, cancelled/declined/series orphans, 25-lookup cap, malformed records, per-issue fixes), and the `bob gcal list` fragile hint (conditions, wording, `fragile_directives` JSON) up to the approved plan, with tests and docs.

## Notes

[2026-11-11T06:22:25Z · bob-cli-ji.8.4] PROPOSED FOLLOW-UP: refresh Bob Mac Capture Tests/Fixtures/gcal-note copies from bob-cli tests/fixtures/gcal_note/json (changed: ambiguous.json, applied.json, both_scopes.json, cleared.json, google_reasons.json, inherited_reasons.json, invalid.json, list_all.json, preview.json, preview_match.json, saved.json, saved_elsewhere.json, saved_sync_failed.json, series_scope.json, show.json, show_preview_match.json, unchanged.json, waiting_states.json) and rerun its gcal-note tests

[2026-11-11T06:22:50Z · bob-cli-ji.8.4] Finished extras: -e requires a TTY (BOB_GCAL_ASSUME_TTY), uses $VISUAL then $EDITOR then vi, git scissors, Edit again? [Y/n], empty clears or reports unchanged; -A adopts Google directive/reason lines including bare -N/+M and -0/+0, refuses an existing note, exits 2 when nothing to adopt, -A -e prefills adopted lines, success says they now live in Bob too; doctor notes uses journal::load_notes, reports N private notes, warns on orphans (gone/cancelled/declined/series), unresolved routes, foreign-account notes, malformed gcal.note records, 25-lookup cap, and non-not-found lookup errors as not checked, with a first-offender fix; list prints the ⚑ hint and JSON fragile_directives only for guest tasks with Google Bob lines and no private note. just check passed. This phase changed no golden fixtures. Across the epic, tests/fixtures/gcal_note/json changed: ambiguous.json, applied.json, both_scopes.json, cleared.json, google_reasons.json, inherited_reasons.json, invalid.json, list_all.json, preview.json, preview_match.json, saved.json, saved_elsewhere.json, saved_sync_failed.json, series_scope.json, show.json, show_preview_match.json, unchanged.json, waiting_states.json. Recorded PROPOSED FOLLOW-UP to refresh Bob Mac Capture gcal-note fixture copies.

## Dependencies

- **Depends on:** [bob-cli-ji.8.3](bob-cli-ji.8.3.md) ✓ · ⧖ 2026-11-10

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-ji.8.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-ji.8.4/README.md) | [bob-cli-ji.8.4](bob-cli-ji.8.4.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`ba7a1c9`](https://github.com/bobs-org/bob-cli/commit/ba7a1c9092a368dded96c3ec95dee72c0261f7b0) | feat(gcal): finish private event note extras | [bob-cli-ji.8.4](bob-cli-ji.8.4.md) | 2026-11-11 01:25:11 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-ji.8.4][1] | Need the phase scope, design file, notes, and DECISIONS | 4 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-ji.8.4/README.md

<!-- sase:referenced-by:end -->
