# Bead: bob-cli-ji.8.2 — Exact selection, argv pre-pass, orphans, and list/show fixes

[Bead Pages](../README.md) / [bob-cli-ji.8](bob-cli-ji.8.md) / bob-cli-ji.8.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.bob-cli-ji.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-ji.land.md) · **Assignee:** `bob-cli-ji.8.2` · **Size:** medium
**Created:** 2026-11-10 22:31:45 EST · **Closed:** 2026-11-11 00:03:38 EST
**Plan:** [202611/finish\_private\_gcal\_event\_notes.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/finish_private_gcal_event_notes.md)

## Description

select: build `-i`/URL previews from the pre-note Google event, honor this command's options anywhere before `--`, make the printed orphan clear commands work, keep lookup failures from becoming orphans, check cancelled/declined/gone before past-hiding, key the list JSON by mode, guard show by account, print the URL fallback warning, and enrich the picker rows.

## Notes

[2026-11-11T05:03:18Z · bob-cli-ji.8.2] PROPOSED FOLLOW-UP: gcal.note fold ties on (ts, host) when two hosts write the same key within one second; last-writer-wins then depends on host ordering, so a clear written in the same second as the note from another host could lose the fold — consider a monotonic tiebreak (path, line already cover same-host)

[2026-11-11T05:03:38Z · bob-cli-ji.8.2] All 9 select fixes land with tests: pre-note google_event clone (cleared preview shows Google values; regenerated tests/fixtures/gcal_note/json/cleared.json — the only fixture changed), argv pre-pass honors note options anywhere before -- with attached-value and -30min TEXT handling, orphan -c clears by key incl. bare series masters, lookup outages warn instead of orphaning, cancelled/declined/gone beat past-hiding with series judged by master status, list JSON keys by mode (-a=events), show warns on foreign-account notes, URL fallback warning prints with the error in human+JSON (GoogleError.with_warnings), enriched picker rows and scope prompt. Verified: cargo test --workspace 10472 passed 0 failed; fmt clean; clippy gate clean; docs-check shows only the 5 known mounted-page budget failures tracked by jz/h9.

## Dependencies

- **Depends on:** [bob-cli-ji.8.1](bob-cli-ji.8.1.md) ✓ · ⧖ 2026-11-10
- **Blocks:** [bob-cli-ji.8.3](bob-cli-ji.8.3.md) ◐ · ⧖ 2026-11-10

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-ji.8.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-ji.8.2/README.md) | [bob-cli-ji.8.2](bob-cli-ji.8.2.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`9660397`](https://github.com/bobs-org/bob-cli/commit/9660397de55695647da3a01c2f595e1560651058) | fix(gcal-notes): nine select fixes for note previews, options, clear, list/show | [bob-cli-ji.8.2](bob-cli-ji.8.2.md) | 2026-11-11 00:05:16 EST |
